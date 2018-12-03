# 通过公共API访问OpenTSDB<a name="dli_01_0338"></a>

## SQL应用<a name="section1299118503718"></a>

使用SQL方式编写一个完整的对接OpenTSDB代码的步骤如下：

1.  创建SparkSession。

    ```
    import org.apache.spark.sql.SparkSession
    val sparkSession = SparkSession.builder().getOrCreate()
    ```

2.  传入认证参数。

    ```
    val sparkConf = sparkSession. conf
    sparkConf.set(\"spark.sql.datasource.cloudtable.api.domain\", \"cloudtable-api.cloudtable.com:8080\") 
    sparkConf.set(\"spark.sql.datasource.cloudtable.token\", \"Your_token_value \")
    sparkConf.set(\"spark.sql.datasource.cloudtable.projectid\", \"Your_project_id\")
    ```

3.  创建关联OpenTSDB表。

    ```
    sparkSession.sql("create table opentsdb_test using opentsdb options(
           \"clusterid\"=\"834f2b81-9a24-42ed-98a9-4513221ef202\", 
           \"metric\"=\"city\", 
           \"tags\"=\"location,name\")
    ")
    ```

4.  导入数据到OpenTSDB。

    ```
    sparkSession.sql("insert into opentsdb_test values(\"futian\", \"huangwei\", \"2018-05-03 00:00:00\", 30.0)")
    ```

5.  读取OpenTSDB上的数据。

    ```
    sparkSession.sql("select * from opentsdb_test").collect()
    ```


## RDD应用<a name="section15740231788"></a>

使用RDD方式编写一个完整的对接OpenTSDB代码的步骤如下：

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
    val sparkConf = sparkSession.conf
    sparkConf.set(\"spark.sql.datasource.cloudtable.api.domain\", \"cloudtable-api.cloudtable.com:8080\") 
    sparkConf.set(\"spark.sql.datasource.cloudtable.token\", \"Your_token_value \")
    sparkConf.set(\"spark.sql.datasource.cloudtable.projectid\", \"Your_project_id\")
    ```

3.  使用创建关联OpenTSDB表的sql语句创建一张OpenTSDB表。

    ```
    sparkSession.sql("create table opentsdb_test using opentsdb options(
        \"clusterid\"=\"834f2b81-9a24-42ed-98a9-4513221ef202\", 
        \"metric\"=\"city\",
        \"tags\"=\"location,name\")
    ")
    ```

4.  构造导入到OpenTSDB的数据。

    ```
    // 构造schema
    val attrTag1Location = new StructField("location", StringType)
    val attrTag2Name = new StructField("name", StringType)
    val attrTimestamp = new StructField("timestamp", LongType)
    val attrValue = new StructField("value", DoubleType)
    val attrs = Array(attrTag1Location, attrTag2Name, attrTimestamp, attrValue)
     
    // 根据schema的类型构造数据
    val mutableRow: Seq[Any] = Seq("futian", "huawei", 123456L, 30.0)
    val rddData: RDD[Row] = sparkSession.sparkContext.parallelize(Array(Row.fromSeq(mutableRow)), 1)
    ```

5.  导入数据到OpenTSDB。

    ```
    sparkSession.createDataFrame(rddData, new StructType(attrs))
          .write
          .insertInto("opentsdb_test")
    ```

6.  读取OpenTSDB上的数据。

    ```
    // 准备访问OpenTSDB需要的参数
    val map = new mutable.HashMap[String, String]()
    map("metric") = "city"
    map("tags") = "location,name"
    map("clusterid") = "834f2b81-9a24-42ed-98a9-4513221ef202"
    sparkSession.read.format("opentsdb").options(map.toMap).load().collect
    ```


