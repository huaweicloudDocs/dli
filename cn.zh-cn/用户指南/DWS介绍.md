# DWS介绍<a name="dli_01_0371"></a>

## 基本概念<a name="zh-cn_topic_0117736646_section1164215581616"></a>

数据仓库服务（Data Warehouse Service，简称DWS）是一种基于公有云基础架构和平台的在线分析型数据库，为用户的海量数据提供挖掘和分析服务，提供即开即用、可扩展且完全托管的分析型数据库服务。兼容PostgreSQL生态，可基于标准SQL，结合商业智能\(BI\)工具，经济高效地对海量数据进行挖掘和分析，使用成本大大低于传统数仓库。

## 准备工作<a name="zh-cn_topic_0117736646_section7322141516348"></a>

连接DWS需要指定带DWS驱动包的资源模块（此资源模块已预设好）。

具体指定方式为，在创建session的时候，指定要使用的资源模块，并配置优先使用此资源模块的jar包。

步骤如下：

1.  创建Session的POST请求BODY体结构。

    ```
    {
    "kind": "spark",
    "cluster_name":"opentsdbtest3",
    "sc_type":"A",
    "modules":["dli.dataSource.dws"], //dli.dataSource.dws资源模块中带有dws驱动包
    "conf":{"spark.yarn.user.classpath.first":"true"}//配置优先使用资源模块中的jar包
    }
    ```

2.  使用此Session提交spark作业来连接DWS。

