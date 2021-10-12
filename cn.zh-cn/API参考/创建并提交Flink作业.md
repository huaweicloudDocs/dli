# 创建并提交Flink作业<a name="dli_02_0310"></a>

## 场景描述<a name="section851316282599"></a>

本章节指导用户通过API创建并运行Flink自定义作业。API的调用方法请参见[如何调用API](如何调用API.md)。

## 约束限制<a name="section155144213214"></a>

-   新队列第一次运行作业时，需要一定的时间，通常为6\~10分钟。

## 涉及接口<a name="section13856162971"></a>

-   [创建队列](创建队列-0.md)：创建队列。
-   [上传分组资源](上传分组资源.md)：上传Flink自定义作业所需的资源包。
-   [查询组内资源包](查询组内资源包.md)：确认上传的资源包是否正确。
-   [创建Flink自定义作业](新建Flink-Jar作业.md)：创建Flink自定义作业。
-   [批量运行作业](批量运行作业.md)：运行Flink自定义作业。

## 操作步骤<a name="section2742155213719"></a>

1.  创建通用队列。具体请参考[创建队列](创建队列.md)。其中，需要将请求参数"resource\_mode"设置为“1”，创建专属队列。
2.  上传Flink自定义作业资源包。具体请参考[2](创建并提交Spark作业.md#li117291344122510)
3.  查询组内资源包。具体请参考[3](创建并提交Spark作业.md#li970315312304)
4.  创建Flink自定义作业。
    -   接口相关信息

        URI格式：POST /v1.0/\{project\_id\}/streaming/flink-jobs

        -   \{project\_id\}信息请从[获取项目ID](获取项目ID.md)获取。
        -   请求参数说明详情，请参见[创建数据库](创建数据库.md)。

    -   请求示例
        -   描述：在项目ID为48cc2c48765f481480c7db940d6409d1项目下，创建Flink自定义作业。
        -   示例URL：POST https://\{endpoint\}/v1.0/48cc2c48765f481480c7db940d6409d1/streaming/flink-jobs

            \{endpoint\}信息请从[地区和终端节点](https://developer.huaweicloud.com/endpoint?DLI)获取。

        -   Body：

            ```
            {
                "name": "test",
                "desc": "job for test",
                "queue_name": "testQueue",
                "manager_cu_number": 1,
                "cu_number": 2,
                "parallel_number": 1,
                "tm_cus": 1,
                "tm_slot_num": 1,
                "log_enabled": true,
                "obs_bucket": "bucketName",
                "smn_topic": "topic",
                "main_class": "org.apache.flink.examples.streaming.JavaQueueStream",
                "restart_when_exception": false,
                "entrypoint": "javaQueueStream.jar",
                "entrypoint_args":"-windowSize 2000 -rate3",
                "dependency_jars": [
                    "myGroup/test.jar",
                    "myGroup/test1.jar"
                ],
                "dependency_files": [
                    "myGroup/test.csv",
                    "myGroup/test1.csv"
                ]
            }
            ```

    -   响应示例

        ```
        {
          "is_success": true,
          "message": "新建flink作业成功",
          "job": {
            "job_id": 138,
            "status_name": "job_init",
            "status_desc": ""
          }
        }
        ```

5.  批量运行作业。
    -   接口相关信息

        URI格式：POST /v1.0/\{project\_id\}/streaming/jobs/run

        -   \{project\_id\}信息请从[获取项目ID](获取项目ID.md)获取。
        -   请求参数说明详情，请参见[批量运行作业](批量运行作业.md)。

    -   请求示例
        -   描述：在项目ID为48cc2c48765f481480c7db940d6409d1项目下，运行job\_id为298765和298766的作业。
        -   示例URL：POST https://\{endpoint\}/v1.0/48cc2c48765f481480c7db940d6409d1/streaming/jobs/run

            \{endpoint\}信息请从[地区和终端节点](https://developer.huaweicloud.com/endpoint?DLI)获取。

        -   Body：

            ```
            {
                "job_ids": [131,130,138,137],
                "resume_savepoint": true
            }
            ```

    -   响应示例

        ```
        [
            {
                "is_success": "true",
                "message": "作业提交请求下发成功"
            },
            {
                "is_success": "true",
                "message": "作业提交请求下发成功"
            },
            {
                "is_success": "true",
                "message": "作业提交请求下发成功"
            },
            {
                "is_success": "true",
                "message": "作业提交请求下发成功"
            }
        ]
        ```



