# 使用DLI Beeline连接服务端<a name="dli_01_0279"></a>

## 前提条件<a name="section29764247143636"></a>

使用DLI Beeline的机器安装JDK 1.7或以上版本并配置环境变量，推荐在Linux环境下使用Beeline工具。

## 操作步骤<a name="section66557662143929"></a>

1.  下载并解压工具包“dli-beeline-<version\>-bin.tar.gz”，其中version为版本号，以实际版本号为准。
2.  进入解压目录，里面有三个子目录bin、conf、lib，分别存放了Beeline相关的执行脚本、配置文件和依赖包。
3.  进入配置文件conf目录，将“connection.properties.template”重命名成“connection.properties”，并配置连接参数（具体连接参数请参考[使用JDBC连接服务端](使用JDBC连接服务端.md)中的[表2](使用JDBC连接服务端.md#table7064698105347)和[表3](使用JDBC连接服务端.md#table31567601152339)）。
4.  进入执行脚本bin目录，启动beeline脚本，执行连接命令即可执行SQL语句，如下所示：

    ```
    %bin/beeline
    Start Beeline
    Welcome to DLI service !
    beeline> !connect
    Connecting from the default connection.properties
    Connecting to jdbc:dli://dli.cn-north-1.myhuaweicloud.com/8fc20d97a4444cafba3c3a8639380003
    Connected to: DLI service
    jdbc:dli://dli.cn-north-1.myhuaweicloud... (not set)> show databases;
    +--------------------+
    |    databaseName    |
    +--------------------+
    | bjhk               |
    | db_xd              |
    | dimensions_adgame  |
    | odbc_db            |
    | sdk_db             |
    | tpch_csv_1024      |
    | tpch_csv_4g_new    |
    | tpchnewtest        |
    | tpchtest           |
    | xunjian            |
    +--------------------+
    10 rows selected (0.338 seconds)
    ```

    用户也可以在启动beeline脚本时通过命令行选项设置连接参数，如下所示，如果连接参数不全，Beeline会提示补全相关信息。

    ```
    %bin/beeline -u 'jdbc:dli://dli.cn-north-1.myhuaweicloud.com/8fc20d97a4444cafba3c3a8639380003? authenticationmode=aksk'
    Start Beeline
    Connecting to jdbc:dli://dli.cn-north-1.myhuaweicloud.com/8fc20d97a4444cafba3c3a8639380003?usehttpproxy=true;proxyhost=10.186.60.154;proxyport=3128;authenticationmode=aksk
    Enter region name: cn-north-1
    Enter service name: DLI
    Enter access key(AK): <real access key>
    Enter secret key(SK): ****************************************
    Enter queue name: default
    Connected to: DLI service
    Welcome to DLI service !
    jdbc:dli://dli.cn-north-1.myhuaweicloud... (not set)> 
    ```


