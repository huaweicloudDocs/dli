# 使用SQL方式对接RDS<a name="dli_01_0347"></a>

通过JDBC连接到RDS数据库执行sql语句。

## 创建表<a name="section98731756518"></a>

```
val sql = "create table customer(id int,name varchar(20),age int)"
  try {    
     Class.forName(driver)    
     conn = DriverManager.getConnection(url, userName, password)    
     val statement = conn.createStatement();  
     statement. executeUpdate (sql)    
   } catch {    
        case ex => ex.printStackTrace()    
   }    
  finally {    
     if (conn != null) {    
        conn.close()    
    }    
  }  
```

## 删除表<a name="section156681412195310"></a>

```
val sql = "drop table customer"
  try {  
      Class.forName(driver)  
    conn = DriverManager.getConnection(url, userName, password)  
     val statement = conn.createStatement();
     statement. executeUpdate (sql)  
   } catch {  
      case ex => ex.printStackTrace()  
  }  
  finally {  
    if (conn != null) {  
      conn.close()  
    }  
  }  
```

## 插入数据<a name="section794132215553"></a>

当DataFrame数据量比较大的时候，建议使用以下方式写入RDS数据库，而不是使用上述write方法。

```
 import java.sql.{Connection, DriverManager, SQLException}  

var conn:Connection = null

 // dataFrame转换成RDD,通过遍历RDD写入到RDS中
jdbcDF.rdd.foreachPartition(it => {  
   val sql = "insert into customer values(?,?)"
   val batchNum = 100
   var count = 0
  try {  
    Class.forName(driver)  
    conn = DriverManager.getConnection(url_local, userName, password)  
    val statement = conn.prepareStatement(sql)  
    conn.setAutoCommit(false)  
    while (it.hasNext) {  
      count+=1;  
      val it1 = it.next()  
      statement.setInt(1, it1.getAs("id"))  
      statement.setString(2, it1.getAs("name"))  
  
       statement.addBatch()  
      statement.clearParameters()  

      //批量处理
      if (count % batchNum == 0) {  
        statement.executeBatch()  
       }  
    }  
     statement.executeBatch()  
    conn.commit()  
   } catch {  
    case ex: SQLException => conn.rollback()  
     case ex => ex.printStackTrace()  
  }  
  finally {  
    if (conn != null) {  
      conn.close()  
    }  
   }  
}) 
```

## 查询数据<a name="section159678400590"></a>

```
    var conn:Connection = null  
    val sql = "select * from customer"
      try {  
      Class.forName(driver)  
      conn = DriverManager.getConnection(url, userName, password)  
      val statement = conn.createStatement()  
 
      val resultSet = statement.executeQuery(sql)  
      while (resultSet.next()) {  
      val id = resultSet.getInt("id")  
      val name = resultSet.getString("name")  
      val age = resultSet.getInt("age")  
      println("id:"+id+" name:"+name+" age:"+age)  
      }  
     } catch {  
      case ex => ex.printStackTrace()  
     }  
    finally {  
      if (conn != null) {  
          conn.close()  
       }  
    }  
```

