# 使用ODBC连接服务端<a name="dli_01_0265"></a>

## 前提条件<a name="section12655972162948"></a>

-   已安装Java运行环境，且为java 1.8版本32位安装包。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >认证鉴权方式采用华为云账号密码方式时，可不安装Java环境。采用AK/SK认证方式依赖Java运行环境，需要安装Java运行环境。  


-   已安装编译示例代码的软件：Visual Studio 2012。
-   仅支持Windows 2012及以上版本操作系统。

## 操作步骤<a name="section2946158316655"></a>

1.  <a name="li2444737817101"></a>解压安装包。

    将“dli-odbc-<version\>\_Release.zip”解压到C盘根目录。安装目录可自行调整，建议安装到C盘根目录。

2.  注册ODBC驱动。

    1.  打开Windows操作系统“开始”菜单，输入cmd命令。
    2.  在命令行窗口，进入“dli-odbc-<version\>\_Release.zip”解压目录下的windows目录。例如：“C:\\DLI\_odbc\\windows”。
    3.  执行命令：

        **.\\odbcreg /i DLIODBC dliodbc.dll C:\\DLI\_odbc\\windows**

        其中“DLIODBC”为注册ODBC驱动的名称，“C:\\DLI\_odbc\\windows ”为“DLIODBC”解压目录下的Windows目录，用户需根据实际目录做相应修改。

    4.  输入“y”获取执行结果。

    ```
    ODBCREG - to register or unregister ODBC driver
    Proceeding to register...
      driver: DLIODBC
         dll: dliodbc.dll
        path: C:\DLI_odbc\windows
    Confirm(y/n)
    DLIODBC installed/registered successfully
    ```

3.  打开驱动管理器，查看驱动程序。

    目前DLI服务只提供32位ODBC驱动程序，ODBC数据源管理器也需要使用32位版本。

    -   64位操作系统请使用：C:\\Windows\\SysWOW64\\odbcad32.exe
    -   32位操作系统请使用：C:\\Windows\\System32\\odbcad32.exe

    在驱动管理器的“驱动程序”页签下，查看是否存在名称为“DLIODBC”的驱动程序。

4.  配置环境变量。认证鉴权方式采用华为云账号密码方式时，可跳过该步骤。采用AK/SK方式时，需要执行该步骤。
    1.  配置环境变量。

        配置与修改如下系统变量：

        -   变量：JAVA\_CLIENT\_DLL

            值：C:\\Program Files \(x86\)\\java\\jdk1.8.0\_161\\jre\\bin\\client\\jvm.dll

        -   变量: Path

            值：C:\\Program Files \(x86\)\\java\\jdk1.8.0\_161\\jre\\bin\\client;%Path%


        >![](public_sys-resources/icon-note.gif) **说明：**   
        >以上两个变量值仅作参考，请根据实际安装目录配置。  

    2.  重启系统，使环境变量配置生效。

5.  配置日志参数。

    打开在[1](#li2444737817101)中解压的安装包，进入log.properties文件，例如：“C:\\DLI\_odbc\\windows\\log.properties”，修改以下配置。

    1.  日志输出级别：“log4cplus.rootLogger=INFO,DLILog”。

        建议级别设置为“INFO“；定位问题时，可以调整为“DEBUG“。

    2.  日志输出路径：“log4cplus.appender.DLILog.File=C:\\DLI\_odbc\\windows\\log\\dli\_odbc.log”。

        日志输出路径建议为安装路径下log目录，根据实际安装路径配置。


6.  <a name="li65930874174932"></a>配置数据源。
    1.  准备数据源配置文件。

        打开“C:\\DLI\_odbc\\windows”目录下odbc.ini文件，修改以下配置项。

        >![](public_sys-resources/icon-note.gif) **说明：**   
        >除DRIVER外，其他配置项均可在应用程序中通过连接参数配置，此处可不配置。认证鉴权相关参数建议在应用程序中通过连接参数配置。  

        ```
        [ODBC]
        DRIVER=DLIODBC  ## 配置实际注册的DLI驱动名
        HOST=dli.cn-north-1.myhuaweicloud.com  ## 配置实际对接的DLI服务Endpoint
        REGION=cn-north-1  ## 配置实际对接的DLI服务Region
        PROJECTID=  ## 根据登陆华为云DLI服务的实际账户配置
        AUTHMODE=0  ## 0 表示为华为云账号密码认证；1 表示为AK/SK认证
        ACCOUNT=    ## 配置为登陆华为云的账号
        USER=       ## 使用华为云账号登陆时，同上配置为华为云账号；当使用IAM用户登陆时，配置为IAM子用户
        PASSWORD=   ## 配置用户登陆密码
        AK=         ## 配置用户的AK
        SK=         ## 配置用户的SK
        QUEUENAME=default   ## 配置实际使用的DLI队列名称
        DATABASE=   ## 配置实际使用的数据库名称
        USEPROXY=0
        ```

    2.  添加用户数据源。

        **.\\odbcreg.exe /d DLIODBCUserDS C:\\DLI\_odbc\\windows\\odbc.ini**

        其中“DLIODBCUserDS”为用户数据源名称，在应用程序中使用。

        确认打印的内容是否和在[1](#li2444737817101)解压的文件odbc.ini”文件内容一致，确认一致后输入“y”。

    3.  打开驱动管理器，查看用户数据源。

        目前DLI服务只提供32位ODBC驱动程序，ODBC数据源管理器也需要使用32位版本。

        -   64位操作系统请使用：C:\\Windows\\SysWOW64\\odbcad32.exe
        -   32位操作系统请使用：C:\\Windows\\System32\\odbcad32.exe

        在驱动管理器的“用户DSN”页签下，查看是否存在名称为“DLIODBCUserDS”的数据源。

    4.  添加系统数据源。

        **.\\odbcreg.exe /s DLIODBCSysDS C:\\DLI\_odbc\\windows\\odbc.ini**

        其中“DLIODBCSysDS”为系统数据源名称，在应用程序中使用。

        确认打印的内容是否和在[1](#li2444737817101)解压的文件“odbc.ini”文件内容一致，确认一致后输入“y”。

    5.  打开驱动管理器，查看系统数据源。

        目前DLI服务只提供32位ODBC驱动程序，ODBC数据源管理器也需要使用32位版本。

        -   64位操作系统请使用：C:\\Windows\\SysWOW64\\odbcad32.exe
        -   32位操作系统请使用：C:\\Windows\\System32\\odbcad32.exe

        在驱动管理器的“系统DSN”页签下，查看是否存在名称为“DLIODBCSysDS”的数据源。



## 示例<a name="section2480263418554"></a>

```
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Data;
using System.Data.Odbc;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            string connectionString = "DSN=DLIODBCSysDS;AUTHMODE=0;ACCOUNT=xxx;USER=xxx;PASSWORD=xxx";

            string queryString = "show tables;";
            OdbcCommand command = new OdbcCommand(queryString);

            using (OdbcConnection connection = new OdbcConnection(connectionString))
            {

                OdbcDataReader reader;
                try
                {
                    command.Connection = connection;

                    connection.Open();

                    reader = command.ExecuteReader();

                    while (reader.Read())
                    {
                        Console.WriteLine("\t{0}\t{1}\t{2}", 
reader[0], reader[1], reader[2]);
                    }

                    reader.Dispose();
                    reader.Close();

                }
                catch (Exception ex)
                {
                    Console.WriteLine(ex.Message);
                }
            }

            command.Dispose();
        }
    }
}
```

>![](public_sys-resources/icon-note.gif) **说明：**   
>1.  示例为C\#样例代码。  
>2.  将代码样例中“string connectionString”指定的dsn驱动修改为[6](#li65930874174932)注册的数据源。  

