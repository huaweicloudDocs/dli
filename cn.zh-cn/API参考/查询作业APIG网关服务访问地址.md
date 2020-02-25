# 查询作业APIG网关服务访问地址<a name="dli_02_0239"></a>

## 功能介绍<a name="section1085315417531"></a>

查询作业APIG网关服务访问地址。

## URI<a name="section217610222531"></a>

-   URI格式

    GET /v1.0/\{project\_id\}/streaming/jobs/\{job\_id\}/apig-sinks

-   参数说明

    **表 1**  URI参数说明

    <a name="table0238153645318"></a>
    <table><thead align="left"><tr id="row1423933635315"><th class="cellrowborder" valign="top" width="14.601460146014599%" id="mcps1.2.4.1.1"><p id="p17153144195310"><a name="p17153144195310"></a><a name="p17153144195310"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.781678167816782%" id="mcps1.2.4.1.2"><p id="p415344115539"><a name="p415344115539"></a><a name="p415344115539"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="68.61686168616862%" id="mcps1.2.4.1.3"><p id="p8154114117534"><a name="p8154114117534"></a><a name="p8154114117534"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row323973613531"><td class="cellrowborder" valign="top" width="14.601460146014599%" headers="mcps1.2.4.1.1 "><p id="p141542411531"><a name="p141542411531"></a><a name="p141542411531"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.781678167816782%" headers="mcps1.2.4.1.2 "><p id="p0154541125317"><a name="p0154541125317"></a><a name="p0154541125317"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="68.61686168616862%" headers="mcps1.2.4.1.3 "><p id="p1768719515356"><a name="p1768719515356"></a><a name="p1768719515356"></a>项目编号，用于资源隔离。获取方式请参考<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    <tr id="row198271549124815"><td class="cellrowborder" valign="top" width="14.601460146014599%" headers="mcps1.2.4.1.1 "><p id="p18828204918486"><a name="p18828204918486"></a><a name="p18828204918486"></a>job_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.781678167816782%" headers="mcps1.2.4.1.2 "><p id="p6829449114810"><a name="p6829449114810"></a><a name="p6829449114810"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="68.61686168616862%" headers="mcps1.2.4.1.3 "><p id="p182994916483"><a name="p182994916483"></a><a name="p182994916483"></a>作业ID。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="section16587206105411"></a>

无

## 响应消息<a name="section17131775410"></a>

-   响应样例

    ```
    {
        "is_success": "true",
        "message": "查询作业网关服务访问地址成功",
        "apig_sinks": {
            "sinks": [
                {
                    "app_id": "dc7a574571bb4749bdab401a004601c4",
                    "name": "OVER_SPEED_WARNING",
                    "url": "https://ae67828f8f0c4d42b419a1320252f1b7.apigw.cn-north-7.myhuaweicloud.com/154/OVER_SPEED_WARNING",
                    "encode": "csv",
                    "delimiter": ",",
                    "attrs": [
                        {
                            "name": "OVER_SPEED_MESSAGE",
                            "type": "STRING"
                        }
                    ]
                }
            ]
        }
    }
    ```

-   参数说明

    **表 2**  响应参数说明

    <a name="table6601145019588"></a>
    <table><thead align="left"><tr id="row16024504586"><th class="cellrowborder" valign="top" width="18.96%" id="mcps1.2.5.1.1"><p id="p13171718165912"><a name="p13171718165912"></a><a name="p13171718165912"></a>参数名</p>
    </th>
    <th class="cellrowborder" valign="top" width="14.08%" id="mcps1.2.5.1.2"><p id="p8171111895916"><a name="p8171111895916"></a><a name="p8171111895916"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.19%" id="mcps1.2.5.1.3"><p id="p15172141825914"><a name="p15172141825914"></a><a name="p15172141825914"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="49.769999999999996%" id="mcps1.2.5.1.4"><p id="p3172918155916"><a name="p3172918155916"></a><a name="p3172918155916"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row14602750145820"><td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.5.1.1 "><p id="p398915579384"><a name="p398915579384"></a><a name="p398915579384"></a>is_success</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.08%" headers="mcps1.2.5.1.2 "><p id="p1298910578382"><a name="p1298910578382"></a><a name="p1298910578382"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.19%" headers="mcps1.2.5.1.3 "><p id="p698915713389"><a name="p698915713389"></a><a name="p698915713389"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.769999999999996%" headers="mcps1.2.5.1.4 "><p id="p72931723124015"><a name="p72931723124015"></a><a name="p72931723124015"></a>请求是否成功。</p>
    </td>
    </tr>
    <tr id="row1360205011581"><td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.5.1.1 "><p id="p1799055763813"><a name="p1799055763813"></a><a name="p1799055763813"></a>message</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.08%" headers="mcps1.2.5.1.2 "><p id="p13990165714380"><a name="p13990165714380"></a><a name="p13990165714380"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.19%" headers="mcps1.2.5.1.3 "><p id="p1799175711388"><a name="p1799175711388"></a><a name="p1799175711388"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.769999999999996%" headers="mcps1.2.5.1.4 "><p id="p11519532144013"><a name="p11519532144013"></a><a name="p11519532144013"></a>消息内容。</p>
    </td>
    </tr>
    <tr id="row9602150135820"><td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.5.1.1 "><p id="p1099175773816"><a name="p1099175773816"></a><a name="p1099175773816"></a>apig_sinks</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.08%" headers="mcps1.2.5.1.2 "><p id="p1335310354015"><a name="p1335310354015"></a><a name="p1335310354015"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.19%" headers="mcps1.2.5.1.3 "><p id="p209911257123810"><a name="p209911257123810"></a><a name="p209911257123810"></a>Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.769999999999996%" headers="mcps1.2.5.1.4 "><p id="p18479104717404"><a name="p18479104717404"></a><a name="p18479104717404"></a>作业审计日志信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  apig\_sinks参数说明

    <a name="table491862583818"></a>
    <table><thead align="left"><tr id="row79181825183815"><th class="cellrowborder" valign="top" width="18.96%" id="mcps1.2.5.1.1"><p id="p10919125143814"><a name="p10919125143814"></a><a name="p10919125143814"></a>参数名</p>
    </th>
    <th class="cellrowborder" valign="top" width="14.08%" id="mcps1.2.5.1.2"><p id="p1491942593811"><a name="p1491942593811"></a><a name="p1491942593811"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.19%" id="mcps1.2.5.1.3"><p id="p149194253387"><a name="p149194253387"></a><a name="p149194253387"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="49.769999999999996%" id="mcps1.2.5.1.4"><p id="p1891911259380"><a name="p1891911259380"></a><a name="p1891911259380"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row16920102593810"><td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.5.1.1 "><p id="p09201325133812"><a name="p09201325133812"></a><a name="p09201325133812"></a>app_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.08%" headers="mcps1.2.5.1.2 "><p id="p1092118259382"><a name="p1092118259382"></a><a name="p1092118259382"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.19%" headers="mcps1.2.5.1.3 "><p id="p10921142516387"><a name="p10921142516387"></a><a name="p10921142516387"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.769999999999996%" headers="mcps1.2.5.1.4 "><p id="p1292110255380"><a name="p1292110255380"></a><a name="p1292110255380"></a>用户作业sink输出的应用Id。</p>
    </td>
    </tr>
    <tr id="row132427437546"><td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.5.1.1 "><p id="p1492218252389"><a name="p1492218252389"></a><a name="p1492218252389"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.08%" headers="mcps1.2.5.1.2 "><p id="p592210256389"><a name="p592210256389"></a><a name="p592210256389"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.19%" headers="mcps1.2.5.1.3 "><p id="p1792214252382"><a name="p1792214252382"></a><a name="p1792214252382"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.769999999999996%" headers="mcps1.2.5.1.4 "><p id="p129221525133814"><a name="p129221525133814"></a><a name="p129221525133814"></a>用户作业sink输出流的名称。</p>
    </td>
    </tr>
    <tr id="row173111591548"><td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.5.1.1 "><p id="p741291118551"><a name="p741291118551"></a><a name="p741291118551"></a>url</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.08%" headers="mcps1.2.5.1.2 "><p id="p341271111555"><a name="p341271111555"></a><a name="p341271111555"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.19%" headers="mcps1.2.5.1.3 "><p id="p1841215111555"><a name="p1841215111555"></a><a name="p1841215111555"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.769999999999996%" headers="mcps1.2.5.1.4 "><p id="p541312117559"><a name="p541312117559"></a><a name="p541312117559"></a>用户作业sink输出流的APIG网关服务访问地址。</p>
    </td>
    </tr>
    <tr id="row15294154012554"><td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.5.1.1 "><p id="p4395982567"><a name="p4395982567"></a><a name="p4395982567"></a>encode</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.08%" headers="mcps1.2.5.1.2 "><p id="p13951885620"><a name="p13951885620"></a><a name="p13951885620"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.19%" headers="mcps1.2.5.1.3 "><p id="p7395483567"><a name="p7395483567"></a><a name="p7395483567"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.769999999999996%" headers="mcps1.2.5.1.4 "><p id="p17396781567"><a name="p17396781567"></a><a name="p17396781567"></a>用户作业sink输出流的格式，比如csv。</p>
    </td>
    </tr>
    <tr id="row16641145585512"><td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.5.1.1 "><p id="p173964818562"><a name="p173964818562"></a><a name="p173964818562"></a>delimiter</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.08%" headers="mcps1.2.5.1.2 "><p id="p53973818561"><a name="p53973818561"></a><a name="p53973818561"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.19%" headers="mcps1.2.5.1.3 "><p id="p103971583562"><a name="p103971583562"></a><a name="p103971583562"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.769999999999996%" headers="mcps1.2.5.1.4 "><p id="p7397178145613"><a name="p7397178145613"></a><a name="p7397178145613"></a>用户作业sink输出流的分隔符，比如逗号。</p>
    </td>
    </tr>
    <tr id="row19583132518573"><td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.5.1.1 "><p id="p189231025133820"><a name="p189231025133820"></a><a name="p189231025133820"></a>attrs</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.08%" headers="mcps1.2.5.1.2 "><p id="p1492332573815"><a name="p1492332573815"></a><a name="p1492332573815"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.19%" headers="mcps1.2.5.1.3 "><p id="p189232259383"><a name="p189232259383"></a><a name="p189232259383"></a>无</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.769999999999996%" headers="mcps1.2.5.1.4 "><p id="p17923162553811"><a name="p17923162553811"></a><a name="p17923162553811"></a>用户作业sink输出流的属性信息。请参见<a href="#table0373153274111">表4</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 4**  attrs参数说明

    <a name="table0373153274111"></a>
    <table><thead align="left"><tr id="row1437415326410"><th class="cellrowborder" valign="top" width="18.96%" id="mcps1.2.5.1.1"><p id="p33744327412"><a name="p33744327412"></a><a name="p33744327412"></a>参数名</p>
    </th>
    <th class="cellrowborder" valign="top" width="14.08%" id="mcps1.2.5.1.2"><p id="p937433217412"><a name="p937433217412"></a><a name="p937433217412"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.19%" id="mcps1.2.5.1.3"><p id="p1437413294110"><a name="p1437413294110"></a><a name="p1437413294110"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="49.769999999999996%" id="mcps1.2.5.1.4"><p id="p173742326418"><a name="p173742326418"></a><a name="p173742326418"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row16388183212412"><td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.5.1.1 "><p id="p838820321412"><a name="p838820321412"></a><a name="p838820321412"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.08%" headers="mcps1.2.5.1.2 "><p id="p93889327411"><a name="p93889327411"></a><a name="p93889327411"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.19%" headers="mcps1.2.5.1.3 "><p id="p1388203234112"><a name="p1388203234112"></a><a name="p1388203234112"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.769999999999996%" headers="mcps1.2.5.1.4 "><p id="p163889321411"><a name="p163889321411"></a><a name="p163889321411"></a>用户作业sink输出流的属性名称。</p>
    </td>
    </tr>
    <tr id="row1038833234115"><td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.2.5.1.1 "><p id="p43883320415"><a name="p43883320415"></a><a name="p43883320415"></a>type</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.08%" headers="mcps1.2.5.1.2 "><p id="p2388632154116"><a name="p2388632154116"></a><a name="p2388632154116"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.19%" headers="mcps1.2.5.1.3 "><p id="p1388832144120"><a name="p1388832144120"></a><a name="p1388832144120"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.769999999999996%" headers="mcps1.2.5.1.4 "><p id="p19389332114113"><a name="p19389332114113"></a><a name="p19389332114113"></a>用户作业sink输出流的属性类型。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 状态码<a name="section1917293620545"></a>

**表 5**  状态码

<a name="table4977135213576"></a>
<table><thead align="left"><tr id="row179782052175714"><th class="cellrowborder" valign="top" width="24.33%" id="mcps1.2.3.1.1"><p id="p16978165212576"><a name="p16978165212576"></a><a name="p16978165212576"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="75.67%" id="mcps1.2.3.1.2"><p id="p397895235715"><a name="p397895235715"></a><a name="p397895235715"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row2978155215711"><td class="cellrowborder" valign="top" width="24.33%" headers="mcps1.2.3.1.1 "><p id="p1479101375814"><a name="p1479101375814"></a><a name="p1479101375814"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="75.67%" headers="mcps1.2.3.1.2 "><p id="p1231195616516"><a name="p1231195616516"></a><a name="p1231195616516"></a>查询作业APIG网关服务访问地址成功。</p>
</td>
</tr>
<tr id="row13209231584"><td class="cellrowborder" valign="top" width="24.33%" headers="mcps1.2.3.1.1 "><p id="p1792161316584"><a name="p1792161316584"></a><a name="p1792161316584"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="75.67%" headers="mcps1.2.3.1.2 "><p id="p179210138589"><a name="p179210138589"></a><a name="p179210138589"></a>输入参数无效。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section13596141025715"></a>

调用接口出错后，将不会返回上述结果，而是返回错误码和错误信息，更多介绍请参见[错误码](错误码.md)。

**表 6**  错误码

<a name="zh-cn_topic_0207595520_table847819307387"></a>
<table><thead align="left"><tr id="zh-cn_topic_0207595520_row2479163016383"><th class="cellrowborder" valign="top" width="12.09%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0207595520_p114796309389"><a name="zh-cn_topic_0207595520_p114796309389"></a><a name="zh-cn_topic_0207595520_p114796309389"></a>错误码</p>
</th>
<th class="cellrowborder" valign="top" width="87.91%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0207595520_p1647973053817"><a name="zh-cn_topic_0207595520_p1647973053817"></a><a name="zh-cn_topic_0207595520_p1647973053817"></a>错误信息</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0207595520_row1047920308387"><td class="cellrowborder" valign="top" width="12.09%" headers="mcps1.2.3.1.1 "><p id="p144831125183313"><a name="p144831125183313"></a><a name="p144831125183313"></a>DLI.11098</p>
</td>
<td class="cellrowborder" valign="top" width="87.91%" headers="mcps1.2.3.1.2 "><p id="p87705518332"><a name="p87705518332"></a><a name="p87705518332"></a>获取用户作业的网关访问地址失败，错误原因：Not a existed sql job or not running. 请稍后重试。</p>
</td>
</tr>
</tbody>
</table>

