# 创建用户并授权使用DLI<a name="dli_01_0418"></a>

本章节通过简单的用户组授权方法，将DLI服务的策略授予用户组，并将用户添加至用户组中，从而使用户拥有对应的DLI权限，操作流程如[图1](#fig4118155455715)所示。

## 前提条件<a name="section3299192113013"></a>

-   “DLI Service User”属于角色。
-   给用户组授权之前，请您了解用户组可以添加的DLI权限，并结合实际需求进行选择，DLI支持的系统权限，请参见：[DLI权限](权限管理概述.md#section6224422143120)。

## 示例流程<a name="section63665495717"></a>

**图 1**  给用户授权DLI权限流程<a name="fig4118155455715"></a>  
![](figures/给用户授权DLI权限流程.jpg "给用户授权DLI权限流程")

1.  <a name="li79820451378"></a>[创建用户组并授权](https://support.huaweicloud.com/usermanual-iam/iam_03_0001.html)

    在IAM控制台创建用户组，并授予DLI服务普通用户权限“DLI Service User”。

2.  [创建用户并加入用户组](https://support.huaweicloud.com/usermanual-iam/iam_02_0001.html)

    在IAM控制台创建用户，并将其加入[1](#li79820451378)中创建的用户组。

3.  [用户登录](https://support.huaweicloud.com/usermanual-iam/iam_01_0552.html)并验证权限

    使用新创建的用户登录控制台，切换至授权区域，验证权限：

    -   在“服务列表”中选择数据湖探索，进入DLI主界面，如果在“队列管理”页面可以查看队列列表，但是单击右上角“购买队列”，无法购买DLI队列（假设当前权限仅包含DLI Service User），表示“DLI Service User”已生效。
    -   在“服务列表”中选择除数据湖探索外（假设当前策略仅包含DLI Service User）的任一服务，若提示权限不足，表示“DLI Service User”已生效。


## 更多操作<a name="section3349026153513"></a>

-   创建子用户请参考《[如何创建子用户](https://support.huaweicloud.com/dli_faq/dli_03_0018.html)》。
-   修改用户策略请参考《[如何修改用户策略](https://support.huaweicloud.com/dli_faq/dli_03_0019.html)》。

