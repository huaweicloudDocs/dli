# 直连CloudTable集群访问（对等连接\)<a name="dli_01_0341"></a>

在使用此方式访问CloudTable时，需要先创建对等连接。

## SQL应用<a name="section595418571814"></a>

使用SQL方式编写一个完整的对接OpenTSDB代码的步骤如下：

1.  创建SparkSession。

    ```
    import org.apache.spark.sql.SparkSession
    val sparkSession = SparkSession.builder().getOrCreate()
    ```

2.  创建关联OpenTSDB的表。

    ```
    sparkSession.sql("create table opentsdb_test using opentsdb options(
           \"host\"=\"opentsdb-6w4fqys11xr8ble.mycloudtable.com:4242\", 
           \"metric\"=\"city\", 
           \"tags\"=\"location,name\")
    ")
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >host地址为OpenTSDB链接地址，可在CloudTable服务的集群信息中获取。  

3.  导入数据到OpenTSDB。

    ```
    sparkSession.sql("insert into opentsdb_test values(\"futian\", \"huangwei\", \"2018-05-03 00:00:00\", 30.0)")
    ```

4.  读取OpenTSDB上的数据。

    ```
    sparkSession.sql("select * from opentsdb_test").collect()
    ```


## RDD应用<a name="section1897212327910"></a>

使用Spark RDD方式编写一个完整的对接OpenTSDB代码的步骤如下：

1.  创建SparkSession。

    ```
    import scala.collection.mutable
    import org.apache.spark.sql.Row
    import org.apache.spark.rdd.RDD
    import org.apache.spark.sql.types._
    import org.apache.spark.sql.SparkSession
    val sparkSession = SparkSession.builder().getOrCreate()
    ```

2.  创建关联OpenTSDB的表。

    ```
    sparkSession.sql("create table opentsdb_test using opentsdb options(
           \"host\"=\"opentsdb-6w4fqys11xr8ble.mycloudtable.com:4242\", 
           \"metric\"=\"city\", 
           \"tags\"=\"location,name\")
    ")
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >host地址为OpenTSDB链接地址，可在CloudTable服务的集群信息中获取。  

3.  构造导入到OpenTSDB的数据。

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

4.  导入数据到OpenTSDB。

    ```
    sparkSession.createDataFrame(rddData, new StructType(attrs))
          .write
          .insertInto("opentsdb_test")
    ```

5.  读取OpenTSDB上的数据。

    ```
    // 准备访问OpenTSDB需要的参数
    val map = new mutable.HashMap[String, String]()
    map("metric") = "city"
    map("tags") = "location,name"
    map("host") = "opentsdb-6w4fqys11xr8ble.mycloudtable.com:4242"
    sparkSession.read.format("opentsdb").options(map.toMap).load().collect
    ```


