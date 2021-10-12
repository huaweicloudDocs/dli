# 创建并提交SQL作业<a name="dli_02_0308"></a>

## 场景描述<a name="section851316282599"></a>

本章节指导用户通过API创建并查询SQL作业。API的调用方法请参见[如何调用API](如何调用API.md)。

## 约束限制<a name="section155144213214"></a>

-   新队列第一次运行作业时，需要一定的时间，通常为6\~10分钟。

## 涉及接口<a name="section13856162971"></a>

-   [创建队列](创建队列-0.md)：创建队列。
-   [创建数据库](创建数据库.md)：创建数据库。
-   [创建表](创建表.md)：创建表。
-   [导入数据](导入数据.md)：导入待查询的数据。
-   [查询作业详细信息](查询作业详细信息.md)：查询导入数据是否正确。
-   [提交SQL作业](提交SQL作业（推荐）.md)：提交查询作业。

## 操作步骤<a name="section2742155213719"></a>

1.  创建SQL队列。具体请参考[创建队列](创建队列.md)。
2.  创建数据库。
    -   接口相关信息

        URI格式：POST /v1.0/\{project\_id\}/databases

        -   \{project\_id\}信息请从[获取项目ID](获取项目ID.md)获取。
        -   请求参数说明详情，请参见[创建数据库](创建数据库.md)。

    -   请求示例
        -   描述：在项目ID为48cc2c48765f481480c7db940d6409d1的项目下创建一个名称为db1的数据库。
        -   示例URL：POST https://\{endpoint\}/v1.0/48cc2c48765f481480c7db940d6409d1/databases

            \{endpoint\}信息请从[地区和终端节点](https://developer.huaweicloud.com/endpoint?DLI)获取。

        -   Body：

            ```
            {
                 "database_name": "db1",
                 "description": "this is for test"
            }
            ```

    -   响应示例

        ```
        {
          "is_success": true,
          "message": ""
        }
        ```

3.  创建表。
    -   接口相关信息

        URI格式：POST /v1.0/\{project\_id\}/databases/\{database\_name\}/tables

        -   \{project\_id\}信息请从[获取项目ID](获取项目ID.md)获取。
        -   请求参数说明详情，请参见[创建表](创建表.md)。

    -   请求示例
        -   描述：在项目ID为48cc2c48765f481480c7db940d6409d1的项目下，在数据库db1中新建名称为tb1的表。
        -   示例URL：POST https://\{endpoint\}/v1.0/48cc2c48765f481480c7db940d6409d1/databases/db1/tables

            \{endpoint\}信息请从[地区和终端节点](https://developer.huaweicloud.com/endpoint?DLI)获取。

        -   Body：

            ```
            {
              "table_name": "tb1",
              "data_location": "OBS",
              "description": "",
              "data_type": "csv",
              "data_path": "obs://obs/path1/test.csv",
              "columns": [
              {
                 "column_name": "column1",
                 "type": "string",
                 "description": "",
                 "is_partition_column": true
              },
              {
                 "column_name": "column2",
                 "type": "string",
                 "description": "",
                 "is_partition_column": false
              }
              ],
              "with_column_header": true,
              "delimiter": ",",
              "quote_char": "\"",
              "escape_char": "\\",
              "date_format": "yyyy-MM-dd",
              "timestamp_format": "yyyy-MM-dd HH:mm:ss"
            }
            ```

    -   响应示例

        ```
        {
          "is_success": true,
          "message": ""
        }
        ```

4.  （可选）如果创建表时，表中没有数据，可使用[导入数据](导入数据.md)接口将数据导入表中。
5.  （可选）导入数据后，可使用[查询作业详细信息](查询作业详细信息.md)接口确认导入的数据是否正确。
6.  提交查询作业。
    -   接口相关信息

        URI格式：POST /v1.0/\{project\_id\}/jobs/submit-job

        -   \{project\_id\}信息请从[获取项目ID](获取项目ID.md)获取。
        -   请求参数说明详情，请参见[创建数据库](创建数据库.md)。

    -   请求示例
        -   描述：在项目ID为48cc2c48765f481480c7db940d6409d1的项目下，提交SQL作业，用户查询数据库db1中表tb1的数据。
        -   示例URL：POST https://\{endpoint\}/v1.0/48cc2c48765f481480c7db940d6409d1/jobs/submit-job

            \{endpoint\}信息请从[地区和终端节点](https://developer.huaweicloud.com/endpoint?DLI)获取。

        -   Body：

            ```
            {
                "currentdb": "db1",
                "sql": "select * from tb1 limit 10",
                "queue_name": "queue1"
            }
            ```

    -   响应示例

        ```
        {
          "is_success": true,
          "message": "",
          "job_id":""95fcc908-9f1b-446c-8643-5653891d9fd9",
          "job_type": "QUERY",
          "job_mode": "async"
        }
        ```



