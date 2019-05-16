# 通过CDM导入数据<a name="dli_01_0254"></a>

通过云数据迁移服务（Cloud Data Migration，简称CDM）将OBS上的数据导入到DLI需要创建CDM集群，具体创建CDM集群的方式请参见《云数据迁移服务用户指南》的[使用CDM迁移OBS的数据到DLI](https://support.huaweicloud.com/usermanual-cdm/cdm_01_0080.html)章节。请注意以下关键配置：

-   DLI所在的VPC与CDM集群的VPC一致。
-   需要创建两个连接，即DLI连接，OBS连接。
-   传输数据的文件格式支持“CSV格式“和“JSON格式“。

