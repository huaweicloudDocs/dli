# JDBC API参考<a name="dli_01_0226"></a>

DLI JDBC Driver支持JDBC标准的众多API，也有部分API不支持用户调用，例如涉及事务调用的API“prepareCall“，调用这类API将抛出“SQLFeatureNotSupportedException“异常。API详情请参考JDBC官网[https://docs.oracle.com/javase/8/docs/api/java/sql/package-summary.html](https://docs.oracle.com/javase/8/docs/api/java/sql/package-summary.html)。

## 支持的API列表<a name="section5630371115934"></a>

DLI JDBC Driver支持的API列表如下，对可能与JDBC标准产生歧义的地方加以备注说明。

-   Connection API支持的常用方法签名：
    -   Statement createStatement\(\)
    -   PreparedStatement prepareStatement\(String sql\)
    -   void close\(\)
    -   boolean isClosed\(\)
    -   DatabaseMetaData getMetaData\(\)
    -   PreparedStatement prepareStatement\(String sql, int resultSetType, int resultSetConcurrency\)

-   Driver API支持的常用方法签名：
    -   Connection connect\(String url, Properties info\)
    -   boolean acceptsURL\(String url\)
    -   DriverPropertyInfo\[\] getPropertyInfo\(String url, Properties info\)

-   ResultSetMetaData API支持的常用方法签名：
    -   String getColumnClassName\(int column\)
    -   int getColumnCount\(\)
    -   int getColumnDisplaySize\(int column\)
    -   String getColumnLabel\(int column\)
    -   String getColumnName\(int column\)
    -   int getColumnType\(int column\)
    -   String getColumnTypeName\(int column\)
    -   int getPrecision\(int column\)
    -   int getScale\(int column\)
    -   boolean isCaseSensitive\(int column\)

-   Statement API支持的常用方法签名：
    -   ResultSet executeQuery\(String sql\)
    -   int executeUpdate\(String sql\)
    -   boolean execute\(String sql\)
    -   void close\(\)
    -   int getMaxRows\(\)
    -   void setMaxRows\(int max\)
    -   int getQueryTimeout\(\)
    -   void setQueryTimeout\(int seconds\)
    -   void cancel\(\)
    -   ResultSet getResultSet\(\)
    -   int getUpdateCount\(\)
    -   boolean isClosed\(\)

-   PreparedStatement API支持的常用方法签名：
    -   void clearParameters\(\)
    -   boolean execute\(\)
    -   ResultSet executeQuery\(\)
    -   int executeUpdate\(\)
    -   PreparedStatement Set系列方法

-   ResultSet API支持的常用方法签名：
    -   int getRow\(\)
    -   boolean isClosed\(\)
    -   boolean next\(\)
    -   void close\(\)
    -   int findColumn\(String columnLabel\)
    -   boolean wasNull\(\)
    -   get系列方法

-   DatabaseMetaData API支持的常用方法签名
    -   ResultSet getCatalogs\(\)

        >![](public_sys-resources/icon-note.gif) **说明：**   
        >在DLI服务中没有Catalog的概念，返回空的ResultSet。  

    -   ResultSet getColumns\(String catalog, String schemaPattern,

        String tableNamePattern, String columnNamePattern\)

    -   Connection getConnection\(\)
    -   getTables\(String catalog, String schemaPattern,String tableNamePattern, String types\[\]\)

        >![](public_sys-resources/icon-note.gif) **说明：**   
        >该方法不采纳Catalog参数，schemaPattern对应DLI服务的database的概念。  

    -   ResultSet getTableTypes\(\)
    -   ResultSet getSchemas\(\)
    -   ResultSet getSchemas\(String catalog, String schemaPattern\)


