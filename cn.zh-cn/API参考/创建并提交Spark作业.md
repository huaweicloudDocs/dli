# 创建并提交Spark作业<a name="dli_02_0309"></a>

## 场景描述<a name="section851316282599"></a>

本章节指导用户通过API创建并提交Spark作业。API的调用方法请参见[如何调用API](如何调用API.md)。

## 约束限制<a name="section155144213214"></a>

-   新队列第一次运行作业时，需要一定的时间，通常为6\~10分钟。

## 涉及接口<a name="section13856162971"></a>

-   [创建队列](创建队列-0.md)：创建队列。
-   [上传分组资源](上传分组资源.md)：上传Spark作业所需的资源包。
-   [查询组内资源包](查询组内资源包.md)：确认上传的资源包是否正确。
-   [创建批处理作业](创建批处理作业.md)：创建并提交Spark批处理作业。
-   [查询批处理作业状态](查询批处理作业状态.md)：查看批处理作业状态。
-   [查询批处理作业日志](查询批处理作业日志.md)：查看批处理作业日志。

## 操作步骤<a name="section2742155213719"></a>

1.  创建通用队列。具体请参考[创建队列](创建队列.md)。
2.  上传分组资源。
    -   接口相关信息

        URI格式：POST /v2.0/\{project\_id\}/resources

        -   \{project\_id\}信息请从[获取项目ID](获取项目ID.md)获取。
        -   请求参数说明详情，请参见[上传分组资源](上传分组资源.md)。

    -   请求示例
        -   描述：在项目ID为48cc2c48765f481480c7db940d6409d1的项目下上传gatk分组中的资源。
        -   示例URL：POST https://\{endpoint\}/v2.0/48cc2c48765f481480c7db940d6409d1/resources

            \{endpoint\}信息请从[地区和终端节点](https://developer.huaweicloud.com/endpoint?DLI)获取。

        -   Body：

            ```
            {
                "paths": [
                    "https://xkftest.obs.huawei.com/txr_test/jars/spark-sdv-app.jar"
                ],
                "kind": "jar",
                "group": "gatk",
                "is_async":"true"
            }
            ```

    -   响应示例

        ```
        {
            "group_name": "gatk",
            "status": "READY",
            "resources": [
                "spark-sdv-app.jar",
                "wordcount",
                "wordcount.py"
            ],
            "details": [
                {
                    "create_time": 0,
                    "update_time": 0,
                    "resource_type": "jar",
                    "resource_name": "spark-sdv-app.jar",
                    "status": "READY",
                    "underlying_name": "987e208d-d46e-4475-a8c0-a62f0275750b_spark-sdv-app.jar"
                },
                {
                    "create_time": 0,
                    "update_time": 0,
                    "resource_type": "jar",
                    "resource_name": "wordcount",
                    "status": "READY",
                    "underlying_name": "987e208d-d46e-4475-a8c0-a62f0275750b_wordcount"
                },
                {
                    "create_time": 0,
                    "update_time": 0,
                    "resource_type": "jar",
                    "resource_name": "wordcount.py",
                    "status": "READY",
                    "underlying_name": "987e208d-d46e-4475-a8c0-a62f0275750b_wordcount.py"
                }
            ],
            "create_time": 1551334579654,
            "update_time": 1551345369070
        }
        ```

3.  查看组内资源包。
    -   接口相关信息

        URI格式：GET /v2.0/\{project\_id\}/resources/\{resource\_name\}

        -   \{project\_id\}信息请从[获取项目ID](获取项目ID.md)获取。
        -   查询参数说明详情，请参见[创建表](创建表.md)。

    -   请求示例
        -   描述：查询项目ID为48cc2c48765f481480c7db940d6409d1下gatk组中的名为luxor-router-1.1.1.jar的资源包。
        -   示例URL：GET https://\{endpoint\}/v2.0/48cc2c48765f481480c7db940d6409d1/resources/luxor-router-1.1.1.jar?group=gatk

            \{endpoint\}信息请从[地区和终端节点](https://developer.huaweicloud.com/endpoint?DLI)获取。

        -   Body：

            ```
            {}
            ```

    -   响应示例

        ```
        {
            "create_time": 1522055409139,
            "update_time": 1522228350501,
            "resource_type": "jar",
            "resource_name": "luxor-router-1.1.1.jar",
            "status": "uploading",
            "underlying_name": "7885d26e-c532-40f3-a755-c82c442f19b8_luxor-router-1.1.1.jar",
            "owner": "****"
        }
        ```

4.  创建并提交Spark批处理作业。
    -   接口相关信息

        URI格式：POST /v2.0/\{project\_id\}/batches

        -   \{project\_id\}信息请从[获取项目ID](获取项目ID.md)获取。
        -   请求参数说明详情，请参见[创建批处理作业](创建批处理作业.md)。

    -   请求示例
        -   描述：在项目ID为48cc2c48765f481480c7db940d6409d1项目下，在队列queue1中创建名称为TestDemo4的批处理作业。
        -   示例URL：POST https://\{endpoint\}/v2.0/48cc2c48765f481480c7db940d6409d1/batches

            \{endpoint\}信息请从[地区和终端节点](https://developer.huaweicloud.com/endpoint?DLI)获取。

        -   Body：

            ```
            {
              "sc_type": "A",
              "jars": [
               
            "spark-examples_2.11-2.1.0.luxor.jar"
              ],
              "driverMemory": "1G",
              "driverCores": 1,
              "executorMemory": "1G",
              "executorCores": 1,
              "numExecutors": 1,
              "queue": "cce_general",
              "file":
            "spark-examples_2.11-2.1.0.luxor.jar",
              "className":
            "org.apache.spark.examples.SparkPi",
              "minRecoveryDelayTime": 10000,
              "maxRetryTimes": 20
            }
            ```

    -   响应示例

        ```
        {
          "id": "07a3e4e6-9a28-4e92-8d3f-9c538621a166",
          "appId": "",
          "name": "",
          "owner": "test1",
          "proxyUser": "",
          "state": "starting",
          "kind": "",
          "log": [],
          "sc_type": "CUSTOMIZED",
          "cluster_name": "aaa",
          "queue": "aaa",
          "image": "",
          "create_time": 1607589874156,
          "update_time": 1607589874156
        }
        ```

5.  查询批处理作业状态。
    -   接口相关信息

        URI格式：GET /v2.0/\{project\_id\}/batches/\{batch\_id\}/state

        -   \{project\_id\}信息请从[获取项目ID](获取项目ID.md)获取。
        -   查询参数说明详情，请参见[查询批处理作业状态](查询批处理作业状态.md)。

    -   请求示例
        -   描述：查询项目ID为48cc2c48765f481480c7db940d6409d1项目下的ID为0a324461-d9d9-45da-a52a-3b3c7a3d809e的批处理作业状态。
        -   示例URL：GET https://\{endpoint\}/v2.0/48cc2c48765f481480c7db940d6409d1/batches/0a324461-d9d9-45da-a52a-3b3c7a3d809e/state

            \{endpoint\}信息请从[地区和终端节点](https://developer.huaweicloud.com/endpoint?DLI)获取。

        -   Body：

            ```
            {}
            ```

    -   响应示例

        ```
        {
           "id":"0a324461-d9d9-45da-a52a-3b3c7a3d809e",
           "state":"Success"
        }
        ```

6.  查询批处理作业日志。
    -   接口相关信息

        URI格式：GET /v2.0/\{project\_id\}/batches/\{batch\_id\}/log

        -   \{project\_id\}信息请从[获取项目ID](获取项目ID.md)获取。
        -   查询参数说明详情，请参见[查询批处理作业日志](查询批处理作业日志.md)。

    -   请求示例
        -   描述：查询项目ID为48cc2c48765f481480c7db940d6409d1下的ID为0a324461-d9d9-45da-a52a-3b3c7a3d809e的批处理作业的后台日志。
        -   示例URL：GET https://\{endpoint\}/v2.0/48cc2c48765f481480c7db940d6409d1/batches/0a324461-d9d9-45da-a52a-3b3c7a3d809e/log

            \{endpoint\}信息请从[地区和终端节点](https://developer.huaweicloud.com/endpoint?DLI)获取。

        -   Body：

            ```
            {}
            ```

    -   响应示例

        ```
        {
            "id": "0a324461-d9d9-45da-a52a-3b3c7a3d809e",
            "from": 0,
            "total": 3,
            "log": [
                   "stdout: ",
                    "stderr: ",
                    "YARN Diagnostics: "
            ]
        }
        ```



