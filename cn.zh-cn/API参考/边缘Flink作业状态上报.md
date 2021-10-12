# 边缘Flink作业状态上报<a name="dli_02_0287"></a>

## 功能介绍<a name="s9b3bf6d5478e4f40809183a8e4c945c8"></a>

该API用于处理边缘Flink作业状态上报信息。

## 调试<a name="section556523314214"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=DLI&api=ChangeFlinkJobStatusReport)中调试该接口。

## URI<a name="s6a7bbfd0e1f9428cb2a117c6209d3ecc"></a>

-   URI格式

    POST /v1/\{project\_id\}/edgesrv/job-report

-   参数说明

    **表 1**  URI参数说明

    <a name="tbaca857a157e4997b5dbb988edcf993c"></a>
    <table><thead align="left"><tr id="r03e4a55add6647aca133cd70d01d82aa"><th class="cellrowborder" valign="top" width="14.12%" id="mcps1.2.5.1.1"><p id="aa631a19e68664105b7cc08c51b3bd00d"><a name="aa631a19e68664105b7cc08c51b3bd00d"></a><a name="aa631a19e68664105b7cc08c51b3bd00d"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.85%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0064335565_p141410194812"><a name="zh-cn_topic_0064335565_p141410194812"></a><a name="zh-cn_topic_0064335565_p141410194812"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="14.299999999999999%" id="mcps1.2.5.1.3"><p id="p161812192366"><a name="p161812192366"></a><a name="p161812192366"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="58.730000000000004%" id="mcps1.2.5.1.4"><p id="a3119b8debd144b84aa0801c3b984f22d"><a name="a3119b8debd144b84aa0801c3b984f22d"></a><a name="a3119b8debd144b84aa0801c3b984f22d"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="rc2d25e8962944b0b9d498c736bc7c1df"><td class="cellrowborder" valign="top" width="14.12%" headers="mcps1.2.5.1.1 "><p id="p3492262515356"><a name="p3492262515356"></a><a name="p3492262515356"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.85%" headers="mcps1.2.5.1.2 "><p id="p1016041415356"><a name="p1016041415356"></a><a name="p1016041415356"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.299999999999999%" headers="mcps1.2.5.1.3 "><p id="p13182219143613"><a name="p13182219143613"></a><a name="p13182219143613"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.730000000000004%" headers="mcps1.2.5.1.4 "><p id="p1310472724012"><a name="p1310472724012"></a><a name="p1310472724012"></a>项目编号，用于资源隔离。获取方式请参考<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="s90a833072d73410195d15a24ded71831"></a>

-   请求样例

    **表 2**  请求参数说明

    <a name="t3c2a16bb2526480f9ae1cfcc5bd53cd9"></a>
    <table><thead align="left"><tr id="rb6596f648dee4d66b67623a5a840bc08"><th class="cellrowborder" valign="top" width="20.97%" id="mcps1.2.5.1.1"><p id="a50ff33b347ac4474b6c7e31bff2ea607"><a name="a50ff33b347ac4474b6c7e31bff2ea607"></a><a name="a50ff33b347ac4474b6c7e31bff2ea607"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="11.15%" id="mcps1.2.5.1.2"><p id="a464d26a0587d4b39af84eee1ff9edc54"><a name="a464d26a0587d4b39af84eee1ff9edc54"></a><a name="a464d26a0587d4b39af84eee1ff9edc54"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.03%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0064335565_p748325710328"><a name="zh-cn_topic_0064335565_p748325710328"></a><a name="zh-cn_topic_0064335565_p748325710328"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="48.85%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0064335565_p216409810328"><a name="zh-cn_topic_0064335565_p216409810328"></a><a name="zh-cn_topic_0064335565_p216409810328"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row18018213527"><td class="cellrowborder" valign="top" width="20.97%" headers="mcps1.2.5.1.1 "><p id="p1022312314525"><a name="p1022312314525"></a><a name="p1022312314525"></a>jobs</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.15%" headers="mcps1.2.5.1.2 "><p id="p14223123117529"><a name="p14223123117529"></a><a name="p14223123117529"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.03%" headers="mcps1.2.5.1.3 "><p id="p7223531125214"><a name="p7223531125214"></a><a name="p7223531125214"></a>Array of Objects</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.85%" headers="mcps1.2.5.1.4 "><p id="p79381661876"><a name="p79381661876"></a><a name="p79381661876"></a>作业信息列表。具体请参考<a href="#table6710132516619">表3</a>。</p>
    </td>
    </tr>
    <tr id="row7819142805213"><td class="cellrowborder" valign="top" width="20.97%" headers="mcps1.2.5.1.1 "><p id="p4223931145220"><a name="p4223931145220"></a><a name="p4223931145220"></a>msg_confirm_topic</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.15%" headers="mcps1.2.5.1.2 "><p id="p622343119520"><a name="p622343119520"></a><a name="p622343119520"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.03%" headers="mcps1.2.5.1.3 "><p id="p17245195114714"><a name="p17245195114714"></a><a name="p17245195114714"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.85%" headers="mcps1.2.5.1.4 "><p id="p16418141712"><a name="p16418141712"></a><a name="p16418141712"></a>消息确认topic。</p>
    </td>
    </tr>
    <tr id="row17820828205217"><td class="cellrowborder" valign="top" width="20.97%" headers="mcps1.2.5.1.1 "><p id="p11224331185211"><a name="p11224331185211"></a><a name="p11224331185211"></a>message_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.15%" headers="mcps1.2.5.1.2 "><p id="p1922418316527"><a name="p1922418316527"></a><a name="p1922418316527"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.03%" headers="mcps1.2.5.1.3 "><p id="p75313549713"><a name="p75313549713"></a><a name="p75313549713"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.85%" headers="mcps1.2.5.1.4 "><p id="p105214228719"><a name="p105214228719"></a><a name="p105214228719"></a>消息id。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  jobs参数说明

    <a name="table6710132516619"></a>
    <table><thead align="left"><tr id="row471013252618"><th class="cellrowborder" valign="top" width="13.04%" id="mcps1.2.5.1.1"><p id="p187101825666"><a name="p187101825666"></a><a name="p187101825666"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="11.39%" id="mcps1.2.5.1.2"><p id="p1271082515615"><a name="p1271082515615"></a><a name="p1271082515615"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="11.899999999999999%" id="mcps1.2.5.1.3"><p id="p1371172513616"><a name="p1371172513616"></a><a name="p1371172513616"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="63.67%" id="mcps1.2.5.1.4"><p id="p471132515617"><a name="p471132515617"></a><a name="p471132515617"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row171117259619"><td class="cellrowborder" valign="top" width="13.04%" headers="mcps1.2.5.1.1 "><p id="p1852926491"><a name="p1852926491"></a><a name="p1852926491"></a>job_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.39%" headers="mcps1.2.5.1.2 "><p id="p452913619910"><a name="p452913619910"></a><a name="p452913619910"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.899999999999999%" headers="mcps1.2.5.1.3 "><p id="p185293614918"><a name="p185293614918"></a><a name="p185293614918"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.67%" headers="mcps1.2.5.1.4 "><p id="p210415172092"><a name="p210415172092"></a><a name="p210415172092"></a>作业ID。</p>
    </td>
    </tr>
    <tr id="row1171119252061"><td class="cellrowborder" valign="top" width="13.04%" headers="mcps1.2.5.1.1 "><p id="p155291460920"><a name="p155291460920"></a><a name="p155291460920"></a>status</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.39%" headers="mcps1.2.5.1.2 "><p id="p13529765920"><a name="p13529765920"></a><a name="p13529765920"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.899999999999999%" headers="mcps1.2.5.1.3 "><p id="p3529762916"><a name="p3529762916"></a><a name="p3529762916"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.67%" headers="mcps1.2.5.1.4 "><p id="p15321182216918"><a name="p15321182216918"></a><a name="p15321182216918"></a>作业状态。</p>
    </td>
    </tr>
    <tr id="row1371110251767"><td class="cellrowborder" valign="top" width="13.04%" headers="mcps1.2.5.1.1 "><p id="p10530166697"><a name="p10530166697"></a><a name="p10530166697"></a>create_time</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.39%" headers="mcps1.2.5.1.2 "><p id="p145301661592"><a name="p145301661592"></a><a name="p145301661592"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.899999999999999%" headers="mcps1.2.5.1.3 "><p id="p8530160911"><a name="p8530160911"></a><a name="p8530160911"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.67%" headers="mcps1.2.5.1.4 "><p id="p13835122714916"><a name="p13835122714916"></a><a name="p13835122714916"></a>时间戳。</p>
    </td>
    </tr>
    <tr id="row1271215251563"><td class="cellrowborder" valign="top" width="13.04%" headers="mcps1.2.5.1.1 "><p id="p8530161396"><a name="p8530161396"></a><a name="p8530161396"></a>exceptions</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.39%" headers="mcps1.2.5.1.2 "><p id="p5530761794"><a name="p5530761794"></a><a name="p5530761794"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.899999999999999%" headers="mcps1.2.5.1.3 "><p id="p15530961293"><a name="p15530961293"></a><a name="p15530961293"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.67%" headers="mcps1.2.5.1.4 "><p id="p359114326916"><a name="p359114326916"></a><a name="p359114326916"></a>作业异常信息。</p>
    </td>
    </tr>
    <tr id="row534945811816"><td class="cellrowborder" valign="top" width="13.04%" headers="mcps1.2.5.1.1 "><p id="p65301566911"><a name="p65301566911"></a><a name="p65301566911"></a>metrics</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.39%" headers="mcps1.2.5.1.2 "><p id="p7530661294"><a name="p7530661294"></a><a name="p7530661294"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.899999999999999%" headers="mcps1.2.5.1.3 "><p id="p105301661695"><a name="p105301661695"></a><a name="p105301661695"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.67%" headers="mcps1.2.5.1.4 "><p id="p1678420371498"><a name="p1678420371498"></a><a name="p1678420371498"></a>作业指标信息。</p>
    </td>
    </tr>
    <tr id="row53505587810"><td class="cellrowborder" valign="top" width="13.04%" headers="mcps1.2.5.1.1 "><p id="p16530461499"><a name="p16530461499"></a><a name="p16530461499"></a>plan</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.39%" headers="mcps1.2.5.1.2 "><p id="p353186992"><a name="p353186992"></a><a name="p353186992"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.899999999999999%" headers="mcps1.2.5.1.3 "><p id="p75311261992"><a name="p75311261992"></a><a name="p75311261992"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.67%" headers="mcps1.2.5.1.4 "><p id="p19182425910"><a name="p19182425910"></a><a name="p19182425910"></a>作业执行计划。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 响应消息<a name="sb9b709576ce84cc5aeb28d9133e7741b"></a>

**表 4**  响应参数说明

<a name="t0d27d7cf309a4b078789fdce81be4b36"></a>
<table><thead align="left"><tr id="rb20a976e281f4bb7bf0c3d7458d6ddf7"><th class="cellrowborder" valign="top" width="21.15%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0064335565_p42893210328"><a name="zh-cn_topic_0064335565_p42893210328"></a><a name="zh-cn_topic_0064335565_p42893210328"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="11.31%" id="mcps1.2.5.1.2"><p id="aa5a1673b8e9149d09001628e9caa78d9"><a name="aa5a1673b8e9149d09001628e9caa78d9"></a><a name="aa5a1673b8e9149d09001628e9caa78d9"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="22.54%" id="mcps1.2.5.1.3"><p id="afd1d2e67cf4b4a3e8d2a5a02c7d145f1"><a name="afd1d2e67cf4b4a3e8d2a5a02c7d145f1"></a><a name="afd1d2e67cf4b4a3e8d2a5a02c7d145f1"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="45%" id="mcps1.2.5.1.4"><p id="a82881821f59f40c0b0bb4b6b34d6ea76"><a name="a82881821f59f40c0b0bb4b6b34d6ea76"></a><a name="a82881821f59f40c0b0bb4b6b34d6ea76"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="raf7543ddbbd7434680507661da53b6f6"><td class="cellrowborder" valign="top" width="21.15%" headers="mcps1.2.5.1.1 "><p id="p19731617125720"><a name="p19731617125720"></a><a name="p19731617125720"></a>is_success</p>
</td>
<td class="cellrowborder" valign="top" width="11.31%" headers="mcps1.2.5.1.2 "><p id="p1497341705714"><a name="p1497341705714"></a><a name="p1497341705714"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="22.54%" headers="mcps1.2.5.1.3 "><p id="p1297214176578"><a name="p1297214176578"></a><a name="p1297214176578"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p109711817125720"><a name="p109711817125720"></a><a name="p109711817125720"></a>执行请求是否成功。<span class="parmvalue" id="parmvalue1801866516843"><a name="parmvalue1801866516843"></a><a name="parmvalue1801866516843"></a>“true”</span>表示请求执行成功。</p>
</td>
</tr>
<tr id="row146054616226"><td class="cellrowborder" valign="top" width="21.15%" headers="mcps1.2.5.1.1 "><p id="p166111464229"><a name="p166111464229"></a><a name="p166111464229"></a>message</p>
</td>
<td class="cellrowborder" valign="top" width="11.31%" headers="mcps1.2.5.1.2 "><p id="p146224619228"><a name="p146224619228"></a><a name="p146224619228"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="22.54%" headers="mcps1.2.5.1.3 "><p id="p12625467227"><a name="p12625467227"></a><a name="p12625467227"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p1162144612211"><a name="p1162144612211"></a><a name="p1162144612211"></a>消息内容。</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section1474273123711"></a>

-   请求样例

    ```
    {
        "jobs": [
            {
                "create_time": 1591104868201,
                "job_id": 99270,
                "exceptions": {
                    "error_id": "Agent.51000",
                    "error_type": "JOB_SUBMIT_EXCEPTION",
                    "error_cause": "agent_submit_job_exception_error",
                    "exception": "",
                    "error_time": "2020-06-02 13:34:28"
                },
                "status": "job_submit_fail"
            }
        ],
        "msg_confirm_topic": "hw/events/messages/dli/message/confirm",
        "message_id": "uuid"
    }
    ```

-   响应样例

    ```
    {
        "is_success": "true",
        "message": "IEF Flink作业状态信息上报成功"
    }
    ```


## 状态码<a name="sf39cfd445ad24e9e82754fcb0027179d"></a>

状态码如[表5](#tb12870f1c5f24b27abd55ca24264af36)所示。

**表 5**  状态码

<a name="tb12870f1c5f24b27abd55ca24264af36"></a>
<table><thead align="left"><tr id="r8d54231f95b14c01a5e55e95f3b2e838"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.3.1.1"><p id="ab49d21f312644072a331f43e92baf853"><a name="ab49d21f312644072a331f43e92baf853"></a><a name="ab49d21f312644072a331f43e92baf853"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="70%" id="mcps1.2.3.1.2"><p id="aea1d3bd107bb4c499da79a88832d256c"><a name="aea1d3bd107bb4c499da79a88832d256c"></a><a name="aea1d3bd107bb4c499da79a88832d256c"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="r211ad4eb571d4d938e5579998723174e"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="a3153e07b3a9749adba92599fe6628fbf"><a name="a3153e07b3a9749adba92599fe6628fbf"></a><a name="a3153e07b3a9749adba92599fe6628fbf"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p104431642124811"><a name="p104431642124811"></a><a name="p104431642124811"></a>IEF Flink作业状态信息上报成功。</p>
</td>
</tr>
<tr id="row44937531727"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p184941532219"><a name="p184941532219"></a><a name="p184941532219"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p2049413539219"><a name="p2049413539219"></a><a name="p2049413539219"></a>请求错误。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section13596141025715"></a>

调用接口出错后，将不会返回上述结果，而是返回错误码和错误信息，更多介绍请参见[错误码](错误码.md)。

