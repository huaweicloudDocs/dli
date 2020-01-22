# DLI自定义策略<a name="dli_01_0451"></a>

如果系统预置的DLI权限，不满足您的授权要求，可以创建自定义策略。自定义策略中可以添加的授权项（Action）请参考[权限策略和授权项](https://support.huaweicloud.com/api-dli/dli_02_0201.html)。

目前华为云支持以下两种方式创建自定义策略：

-   可视化视图创建自定义策略：无需了解策略语法，按可视化视图导航栏选择云服务、操作、资源、条件等策略内容，可自动生成策略。
-   JSON视图创建自定义策略：可以在选择策略模板后，根据具体需求编辑策略内容；也可以直接在编辑框内编写JSON格式的策略内容。

具体创建步骤请参见：[创建自定义策略](https://support.huaweicloud.com/usermanual-iam/iam_01_0605.html)。本章为您介绍常用的DLI自定义策略样例。

## DLI自定义策略样例<a name="section1493518251395"></a>

-   示例1：允许
    -   授权用户拥有在所有区域中所有数据库的创建表权限

        ```
        {
            "Version": "1.1",
            "Statement": [
                {
                    "Effect": "Allow",
                    "Action": [
                        "dli:database:create_table"
                    ],
                    "Resource": [
                        "dli:*:*:database:*"
                    ]
                }
            ]
        }
        ```

    -   授权用户拥有在所在区域中数据库db中表tb中列col的查询权限

        ```
        {
            "Version": "1.1",
            "Statement": [
                {
                    "Effect": "Allow",
                    "Action": [
                        "dli:column:select"
                    ],
                    "Resource": [
                        "dli:cn-north-7:*:column:databases.db.tables.tb.columns.col"
                    ]
                }
            ]
        }
        ```


-   示例2：拒绝

    拒绝策略需要同时配合其他策略使用，否则没有实际作用。用户被授予的策略中，一个授权项的作用如果同时存在Allow和Deny，则遵循Deny优先。

    -   授权用户不能创建数据库，删除数据库，提交作业（default队列除外），删除表

        ```
        {
            "Version": "1.1",
            "Statement": [
                {
                    "Effect": "Deny",
                    "Action": [
                        "dli:database:create_database",
                        "dli:database:drop_database",
                        "dli:queue:submit_job",
                        "dli:table:drop_table"
                    ],
                    "Resource": [
                        "dli:*:*:database:*",
                        "dli:*:*:queue:*",
                        "dli:*:*:table:*"
                    ]
                }
            ]
        }
        ```

    -   授权用户不能在队列名为demo的队列上提交作业

        ```
        {
            "Version": "1.1",
            "Statement": [
                {
                    "Effect": "Deny",
                    "Action": [
                        "dli:queue:submit_job"
                    ],
                    "Resource": [
                        "dli:*:*:queue:queues.demo"
                    ]
                }
            ]
        }
        ```



