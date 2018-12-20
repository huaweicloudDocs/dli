# 使用SparkSQL方式对接RDS<a name="dli_01_0346"></a>

## 创建表<a name="section1121311279328"></a>

1.  利用createDataFrame\(\)创建包含id，name，age三个字段的DataFrame，并初始化数据。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >DataFrame初始字段名为下划线加数字，例如“\_1”， 用户可以字段重命名。  

    ```
        import java.util.Properties;  
      //创建DataFrame，初始化DataFrame数据
      var dataFrame = spark.createDataFrame(List((1,\"Jack\",18))); 
      
      //字段重命名
      val df = dataFrame.withColumnRenamed(\"_1\",\"id\")  
                        .withColumnRenamed(\"_2\",\"name\")  
                        .withColumnRenamed(\"_3\",\"age\");    
    ```

2.  将DataFrame写入RDS，就可在RDS中建表，写入的方式请参见[向RDS写入数据](#section66122508139)。

## 从RDS读取表数据<a name="section1612367543"></a>

-   方式一：read.format\(\)方法

    read.format\(“jdbc”\)指定jdbc的连接方式，并且在option中指定数据源，比如连接设置的url，要读取的数据库表dbtable等，并且将读取到的数据转换为DataFrame。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >-   option支持url、driver、dbtable、partitionColumn、lowerBound、upperBound以及numPartitions选项。  
    >-   url是跨源连接地址。  

    ```
    //连接配置
    val url = "jdbc:mysql://to-rds-1174405062-ljDSiO73.datasource.com:3306";  
    val dbtable = "rds_test.customer_test";  
    val userName = "root";  
    val password = "test";  
    
    //从JDBC加载数据源，返回DataFrame
    val jdbcDF = spark.read  
                      .format("jdbc")  
                      .option("url", url)  
                      .option("dbtable", dbtable)  
                      .option("user", userName)  
                      .option("password", password)  
                      .load() 
    ```

-   方式二：read.jdbc\(\)方法

    只需要提供url，待查询的表名以及相关属性。

    ```
    val connectionProperties = new Properties()  
    connectionProperties.put("user", userName)  
    connectionProperties.put("password", password)  
    val jdbcDF2 = spark.read.jdbc(url,dbtable, connectionProperties)
    ```


## 删除行或列<a name="section72086226614"></a>

-   删除行（假如要删除id=1的用户，使用下列语句进行过滤，保存至RDS，则再次查询返回的DataFrame中不包含id=1的用户。）

    ```
    //过滤掉id=1的用户
    var newDF = df.filter("id!=1")
    newDF.show()
    +---+----+---+  
    | id|name|age|  
    +---+----+---+  
    |  2|Tom | 15|  
    +---+----+---+  
    |  3|Jack|  7|  
    +---+----+---+  
    ```

-   删除列（假如要删除id这一列，使用下列语句进行过滤，保存至RDS，则再次查询返回的DataFrame中不包含id这一列。）

    ```
    Var newDF = df.drop("id")
    newDF.show()
      +----+---+
      |name|age|
      +----+---+
      |Kimi|  5|
      | Tom| 15|
      |Jack|  7|
      +----+---+ 
    ```


## 修改列名<a name="section144441291497"></a>

```
df.withColumnRenamed("name","names").
```

## 查询数据<a name="section1824317540105"></a>

将上述使用read.format\(\)或者read.jdbc\(\)方法读取到的dateFrame注册为临时表，就可使用sql语句进行数据查询了。

```
 //DataFrame注册为临时表，执行sql语句
    df.registerTempTable("customer_test");  
    val result = spark.sql("select * from customer_test where id = 1"); 
          
    result.show();  
    //样例输出
   +---+----+---+  
    | id|name|age|  
   +---+----+---+  
    |  1|Kimi|  5|  
   +---+----+---+  
```

## 向RDS写入数据<a name="section66122508139"></a>

-   方式一：write.format\(\)方法

    ```
    jdbcDF.write  
               .format("jdbc")  
               .option("url", url)  
               .option("dbtable", dbtable)  
               .option("user", username)  
               .option("password", password)  
               .save() 
    ```

-   方式二：write.jdbc\(\)方法

    ```
    val connectionProperties = new Properties()    
    connectionProperties.put("user", userName)    
    connectionProperties.put("password", password)    
    jdbcDF2.write.jdbc(url, dbtable, connectionProperties)
    ```


## DataFrame相关操作<a name="section9516135714239"></a>

-   where：条件查询

    where方法中可传入包含and和or的条件筛选表达式，返回条件过滤后的DataFrame对象。示例如下：

    ```
     jdbcDF.where("id = 1 or age <=10").show()  
    
      //样例输出  
    +---+----+---+  
      | id|name|age|  
    +---+----+---+  
      |  1|Kimi|  5|  
      |  3|Jack|  7|  
    +---+----+---+  
    ```

-   filter：条件筛选

    filter同where的使用方式一致，传入条件筛选表达式，返回过滤后的结果 。示例如下：

    ```
    jdbcDF.fliter("id = 1 or age <=10").show()
    ```

-   select：查询指定字段

    传入待查询的字段名，返回指定字段的DataFrame对象，并且可指定多个字段进行查询 。示例如下：

    ```
     jdbcDF.select("id").show( )  
    //样例输出  
      +---+  
       | id|  
      +---+  
       |  1|  
       |  2|  
       |  3|  
      +---+  
     jdbcDF.select("id" , "name").show( )  
    //样例输出  
    +---+----+  
     | id|name|  
    +---+----+  
     |  1|Kimi|  
     |  2| Tom|  
     |  3|Jack|  
    +---+----+ 
    ```

-   selectExpr：对字段进行特殊处理

    可使用selectExpr方法修改字段名，也可以对指定字段进行特殊处理，返回修改后的DataFrame对象。示例如下，查询id字段，name字段取别名name\_test，age数据加1：

    ```
    jdbcDF.show()  
    //样例输出  
    +---+----+---+  
     | id|name|age|  
    +---+----+---+  
     |  1|Kimi|  5|  
     |  2| Tom| 15|  
     |  3|Jack|  7|  
    +---+----+---+  
    jdbcDF .selectExpr("id" , "name as name_test" , "age+1" ).show()  
    //样例输出  
    +---+---------+---------+  
     |id |name_test|(age + 1)|  
    +---+---------+---------+  
     |1  |Kimi     |6       |  
     |2  |Tom     |16     |  
     |3  |Jack      |8       |  
    +---+---------+---------+
    ```

-   col：获取指定字段

    不同于select方法，col方法每次只能获取一个字段，且返回对象为Column类型。示例如下：

    ```
    val idCol = jdbcDF.col("id") 
    ```

-   drop：删除指定字段

    传入要删除的指定字段，返回不包含此字段的DataFrame对象，并且每次只能指定一个字段删除。示例如下：

    ```
     jdbcDF.drop("id").show() 
     +----+---+
     |name|age|
     +----+---+
     |Kimi|  5|
     | Tom| 15|
     |Jack|  7|
     +----+---+ 
    ```

-   groupBy

    如统计各性别人数，示例如下：

    ```
    df.groupBy("gender").count()
    ```


