# 导入数据至DLI表的方式<a name="dli_01_0420"></a>

## 通过OBS导入数据<a name="section133251856125910"></a>

在DLI管理控制台，将存储在OBS服务上的数据导入DLI表中入口有两个，分别在“数据管理“\>“库表管理“\>“表管理“页面和“SQL编辑器“页面。具体操作请参考[导入数据](导入数据.md)。

## 通过CDM导入数据<a name="section28435121978"></a>

通过云数据迁移服务（Cloud Data Migration，简称CDM）将OBS上的数据导入到DLI需要创建CDM队列，具体创建CDM队列的方式请参见《云数据迁移服务用户指南》的[使用CDM迁移OBS的数据到DLI](https://support.huaweicloud.com/usermanual-cdm/cdm_01_0080.html)章节。请注意以下关键配置：

-   DLI所在的VPC与CDM队列的VPC一致。
-   需要创建两个连接，即DLI连接，OBS连接。
-   传输数据的文件格式支持“CSV格式“和“JSON格式“。

## 通过DIS导入数据<a name="section85731517984"></a>

通过数据接入服务（Data Ingestion Service，简称DIS）将数据导入到DLI需要开通DIS通道，详细开通方式参见《数据接入服务用户指南》的[开通DIS通道](https://support.huaweicloud.com/usermanual-dis/zh-cn_topic_0034903799.html)章节。

配置DIS通道时，“转储服务类型“选择“DLI“，并选择DLI的数据库和表。

