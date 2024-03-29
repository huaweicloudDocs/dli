# 准备Flink作业数据<a name="dli_01_0454"></a>

创建Flink作业需要输入数据源和数据输出通道，即常说的Source和Sink。用户使用其他服务作为数据源或输出通道时，需要先开通相应服务。

Flink作业支持以下数据源和输出通道：

-   DIS数据源和输出通道

    如果用户作业需要DIS作为数据源和输出通道时，则要先开通数据接入服务（DIS）。

    用户如何开通DIS服务，具体操作请参见[《数据接入服务用户指南》](https://support.huaweicloud.com/usermanual-dis/dis_01_0601.html)中的“开通DIS通道“章节。

    申请DIS通道后，用户可以将本地数据通过DIS通道不断上传至DIS服务，实现向Flink作业提供实时流数据源，具体操作请参见[《数据接入服务用户指南》](https://support.huaweicloud.com/usermanual-dis/dis_01_0603.html)中的“发送数据到DIS服务“章节。

    样例数据如下所示：

    ```
    1,lilei,bmw320i,28
    2,hanmeimei,audia4,27
    ```

-   OBS数据源

    如果用户作业需要对象存储服务（OBS）作为数据源，则要先开通OBS服务，具体操作请参见[《对象存储服务控制台指南》](https://support.huaweicloud.com/obs/index.html)中的“开通OBS服务“章节。

    开通OBS服务后，用户需要将本地文件通过Internet上传至OBS指定的位置，具体操作请参见[《对象存储服务控制台指南》](https://support.huaweicloud.com/obs/index.html)中的“上传文件“章节。

-   RDS输出通道

    如果用户作业需要RDS作为输出通道，需要创建RDS实例，具体操作请参见[《关系型数据库快速入门》](https://support.huaweicloud.com/qs-rds/zh-cn_topic_0046585334.html)中“购买实例“章节。

-   SMN输出通道

    如果用户作业需要SMN作为输出通道，需要先在SMN中创建主题，获取URN资源标识，再添加订阅。具体操作请参见[《消息通知服务快速入门》](https://support.huaweicloud.com/qs-smn/smn_ug_0004.html)。

-   Kafka数据源和输出通道

    如果用户作业需要Kafka作为数据源和输出通道，则必须要通过创建增强型跨源连接与Kafka进行对接，具体操作请参见[增强型跨源连接（推荐）](增强型跨源连接（推荐）.md)。

    如果Kafka服务端的端口监听在hostname上，则需要将Kafka Broker节点的hostname和ip的对应关系添加到跨源连接中。

-   CloudTable数据源和输出通道

    如果用户作业需要CloudTable作为数据源和输出通道，需要先在CloudTable中创建集群，获取集群ID。具体操作请参见[《表格存储服务用户指南》](https://support.huaweicloud.com/cloudtable/index.html)《表格存储服务用户指南》中的“入门“章节。

-   云搜索服务输出通道

    如果用户作业需要云搜索服务作为输出通道，需要先在云搜索服务中创建集群，获取集群内网访问地址。具体操作请参见[《云搜索服务用户指南》](https://support.huaweicloud.com/css/index.html)中的“入门“章节。

-   DCS输出通道

    如果用户作业需要DCS作为输出通道，需要先在DCS中创建Redis类型的缓存实例，获取Redis实例连接地址。具体操作请参见[《分布式缓存服务用户指南》](https://support.huaweicloud.com/usermanual-dcs/dcs-ug-0312003.html)中的“入门“章节。


