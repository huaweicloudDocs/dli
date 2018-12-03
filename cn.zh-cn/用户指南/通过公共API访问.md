# 通过公共API访问<a name="dli_01_0331"></a>

## SQL应用<a name="section5842111061"></a>

使用SQL方式编写一个完整的对接HBase代码的步骤如下：

1.  创建SparkSession。

    ```
    import org.apache.spark.sql.SparkSession
    val sparkSession = SparkSession.builder().getOrCreate()
    ```

2.  传入认证参数。

    ```
    val sparkConf = sparkSession.conf
    sparkConf.set(\"spark.sql.datasource.cloudtable.api.domain\", \"cloudtable-api.cloudtable.com:8080\") 
    sparkConf.set(\"spark.sql.datasource.cloudtable.token\", \"Your_token_value \")
    sparkConf.set(\"spark.sql.datasource.cloudtable.projectid\", \"Your_project_id\")
    ```

3.  创建关联Hbase表。

    ```
    sparkSession.sql("create table ct_test(id int, name string) using cloudtable options(
           \"clusterid\"=\"834f2b81-9a24-42ed-98a9-4513221ef202\", 
           \"TableName\"=\"table_in_ct\", 
           \"RowKey\"=\"id\",
        \"Cols\"=\"name:CF1.C1\")
    ")
    ```

4.  导入数据到Hbase。

    ```
    sparkSession.sql("insert into ct_test values(1, \"huawei\")")
    ```

5.  读取Hbase上的数据。

    ```
    sparkSession.sql("select * from ct_test").collect()
    ```


## RDD应用<a name="section123367326614"></a>

使用RDD方式编写一个完整的对接HBase代码的步骤如下：

1.  创建SparkSession。

    ```
    import scala.collection.mutable
    import org.apache.spark.sql.{Row, SparkSession}
    import org.apache.spark.rdd.RDD
    import org.apache.spark.sql.types._
    val sparkSession = SparkSession.builder().getOrCreate()
    ```

2.  传入认证参数。

    ```
    val sparkConf = sparkSession. conf
    sparkConf.set(\"spark.sql.datasource.cloudtable.api.domain\", \"cloudtable-api.cloudtable.com:8080\") 
    sparkConf.set(\"spark.sql.datasource.cloudtable.token\", \"Your_token_value \")
    sparkConf.set(\"spark.sql.datasource.cloudtable.projectid\", \"Your_project_id\")
    ```

3.  使用创建关联Hbase表的sql语句创建一张HBase表。

    ```
    sparkSession.sql("create table ct_test(id int, name string) using cloudtable options(
        \"clusterid\"=\"834f2b81-9a24-42ed-98a9-4513221ef202\", 
        \"TableName\"=\"table_in_ct\", 
        \"RowKey\"=\"id\",
        \"Cols\"=\"name:CF1.C1\")
    ")
    ```

4.  构造导入到Hbase的数据。

    ```
    // 构造schema
    val attrId = new StructField("id", IntegerType)
    val attrName = new StructField("name", StringType)
    val attrs = Array(attrId, attrName)
     
    // 根据schema的类型构造数据    
    val mutableRow: Seq[Any] = Seq(2, "huawei")
    val rddData: RDD[Row] = sparkSession.sparkContext.parallelize(Array(Row.fromSeq(mutableRow)), 1)
    ```

5.  导入数据到Hbase。

    ```
    sparkSession.createDataFrame(rddData, new StructType(attrs))
        .write
        .insertInto("ct_test")
    ```

6.  读取Hbase上的数据。

    ```
    val map = new mutable.HashMap[String, String]()
    map("TableName") = "table_in_ct"
    map("RowKey") = "id"
    map("Cols") = "name:CF1.C1"
    map("clusterid") = "834f2b81-9a24-42ed-98a9-4513221ef202"
    sparkSession.read.schema(new StructType(attrs)).format("cloudtable").options(map.toMap).load().collect
    ```


