# 取消dna-germline作业<a name="dli_02_0152"></a>

## 功能介绍<a name="section6968756197"></a>

取消指定的基因作业。

## URI<a name="zh-cn_topic_0103343296_zh-cn_topic_0102902518_s9e1b8ec5b57c422a942b19835da7d66e"></a>

-   URI格式

    DELETE /v2.0/\{project\_id\}/gene/jobs/\{job\_id\}

-   URI参数

    **表 1**  URI参数

    <a name="table18299172853614"></a>
    <table><thead align="left"><tr id="row947592853614"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.4.1.1"><p id="p1347513282368"><a name="p1347513282368"></a><a name="p1347513282368"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p74757287366"><a name="p74757287366"></a><a name="p74757287366"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="50%" id="mcps1.2.4.1.3"><p id="p1475182833610"><a name="p1475182833610"></a><a name="p1475182833610"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row16475152833619"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.1 "><p id="p079502341110"><a name="p079502341110"></a><a name="p079502341110"></a>job_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1879642316111"><a name="p1879642316111"></a><a name="p1879642316111"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p1779742315114"><a name="p1779742315114"></a><a name="p1779742315114"></a>基因作业Id</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="section3414034164017"></a>

无请求参数。

## 响应消息<a name="section2101574914"></a>

-   返回码

    200

-   响应参数

    **表 2**  响应参数

    <a name="table192695719914"></a>
    <table><thead align="left"><tr id="row82696574918"><th class="cellrowborder" valign="top" width="9.520000000000001%" id="mcps1.2.4.1.1"><p id="p102691857892"><a name="p102691857892"></a><a name="p102691857892"></a>参数名</p>
    </th>
    <th class="cellrowborder" valign="top" width="8.72%" id="mcps1.2.4.1.2"><p id="p12269185711914"><a name="p12269185711914"></a><a name="p12269185711914"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="81.76%" id="mcps1.2.4.1.3"><p id="p192698571294"><a name="p192698571294"></a><a name="p192698571294"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row5269257198"><td class="cellrowborder" valign="top" width="9.520000000000001%" headers="mcps1.2.4.1.1 "><p id="p39381452101113"><a name="p39381452101113"></a><a name="p39381452101113"></a>message</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.72%" headers="mcps1.2.4.1.2 "><p id="p17938105271117"><a name="p17938105271117"></a><a name="p17938105271117"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="81.76%" headers="mcps1.2.4.1.3 "><p id="p494085212113"><a name="p494085212113"></a><a name="p494085212113"></a>若作业当前状态为完成（FINISHED）、失败（FAILED）、取消（CANCELLED）、取消中（CANCELING）时，则该作业无法取消。</p>
    </td>
    </tr>
    </tbody>
    </table>

    示例

    -   请求样例：

        ```
        None
        ```


    -   成功响应样例:

        ```
        {}
        ```


    >![](public_sys-resources/icon-note.gif) **说明：**   
    >调用接口出错后，将不会返回上述结果，而是返回错误码和错误信息，详细介绍请参见[错误码](错误码.md)。  


