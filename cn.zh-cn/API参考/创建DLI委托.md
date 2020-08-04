# 创建DLI委托<a name="dli_02_0299"></a>

## 功能介绍<a name="section18998185384911"></a>

该API用于创建DLI用户委托。

## URI<a name="s9e1b8ec5b57c422a942b19835da7d66e"></a>

-   URI格式：

    POST  /v2/\{project\_id\}/agency

-   参数说明

    **表 1**  URI参数

    <a name="zh-cn_topic_0069077803_table60779388"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0069077803_row61411666"><th class="cellrowborder" valign="top" width="15.03%" id="mcps1.2.4.1.1"><p id="a420a62a594f9410eaea229ffc8037a61"><a name="a420a62a594f9410eaea229ffc8037a61"></a><a name="a420a62a594f9410eaea229ffc8037a61"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="11.27%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0069077803_p873025824211"><a name="zh-cn_topic_0069077803_p873025824211"></a><a name="zh-cn_topic_0069077803_p873025824211"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="73.7%" id="mcps1.2.4.1.3"><p id="a692d3cd97b464aed90ba6d841900a4a5"><a name="a692d3cd97b464aed90ba6d841900a4a5"></a><a name="a692d3cd97b464aed90ba6d841900a4a5"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0069077803_row48589216"><td class="cellrowborder" valign="top" width="15.03%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0069077803_p43412436"><a name="zh-cn_topic_0069077803_p43412436"></a><a name="zh-cn_topic_0069077803_p43412436"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.27%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0069077803_p26746391"><a name="zh-cn_topic_0069077803_p26746391"></a><a name="zh-cn_topic_0069077803_p26746391"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="73.7%" headers="mcps1.2.4.1.3 "><p id="p1310472724012"><a name="p1310472724012"></a><a name="p1310472724012"></a>项目编号，用于资源隔离。获取方式请参考<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="section20458182103"></a>

**表 2**  请求参数

<a name="table127313925813"></a>
<table><thead align="left"><tr id="row137326917589"><th class="cellrowborder" valign="top" width="8.74%" id="mcps1.2.5.1.1"><p id="p12732995582"><a name="p12732995582"></a><a name="p12732995582"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="9.49%" id="mcps1.2.5.1.2"><p id="p1573239185818"><a name="p1573239185818"></a><a name="p1573239185818"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="13.139999999999999%" id="mcps1.2.5.1.3"><p id="p144204427586"><a name="p144204427586"></a><a name="p144204427586"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="68.63%" id="mcps1.2.5.1.4"><p id="p1473219916588"><a name="p1473219916588"></a><a name="p1473219916588"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row273218965810"><td class="cellrowborder" valign="top" width="8.74%" headers="mcps1.2.5.1.1 "><p id="p1144183305813"><a name="p1144183305813"></a><a name="p1144183305813"></a>roles</p>
</td>
<td class="cellrowborder" valign="top" width="9.49%" headers="mcps1.2.5.1.2 "><p id="p1144633185817"><a name="p1144633185817"></a><a name="p1144633185817"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="13.139999999999999%" headers="mcps1.2.5.1.3 "><p id="p184201442105819"><a name="p184201442105819"></a><a name="p184201442105819"></a>Array of String</p>
</td>
<td class="cellrowborder" valign="top" width="68.63%" headers="mcps1.2.5.1.4 "><p id="p193112404590"><a name="p193112404590"></a><a name="p193112404590"></a>角色。目前只支持：obs_adm、dis_adm、ctable_adm、vpc_netadm、smn_adm、te_admin。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="sd1ecb66580054b2ea403be8b2272a2c7"></a>

**表 3**  响应参数

<a name="zh-cn_topic_0069077927_table56638444"></a>
<table><thead align="left"><tr id="zh-cn_topic_0069077927_row48911609"><th class="cellrowborder" valign="top" width="19.79%" id="mcps1.2.5.1.1"><p id="ae076f6b3f1bf463b9cc087fc566253d5"><a name="ae076f6b3f1bf463b9cc087fc566253d5"></a><a name="ae076f6b3f1bf463b9cc087fc566253d5"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.43%" id="mcps1.2.5.1.2"><p id="p12583123083811"><a name="p12583123083811"></a><a name="p12583123083811"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="9.9%" id="mcps1.2.5.1.3"><p id="a59685f4525af4d82a623288ff8ccb0f4"><a name="a59685f4525af4d82a623288ff8ccb0f4"></a><a name="a59685f4525af4d82a623288ff8ccb0f4"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60.88%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0069077927_p632718127368"><a name="zh-cn_topic_0069077927_p632718127368"></a><a name="zh-cn_topic_0069077927_p632718127368"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0069077927_row27919264"><td class="cellrowborder" valign="top" width="19.79%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0069077927_p46867877"><a name="zh-cn_topic_0069077927_p46867877"></a><a name="zh-cn_topic_0069077927_p46867877"></a>is_success</p>
</td>
<td class="cellrowborder" valign="top" width="9.43%" headers="mcps1.2.5.1.2 "><p id="p9584230133817"><a name="p9584230133817"></a><a name="p9584230133817"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="9.9%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0069077927_p7327597"><a name="zh-cn_topic_0069077927_p7327597"></a><a name="zh-cn_topic_0069077927_p7327597"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60.88%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0069077927_p56664447"><a name="zh-cn_topic_0069077927_p56664447"></a><a name="zh-cn_topic_0069077927_p56664447"></a>请求执行是否成功。<span class="parmvalue" id="parmvalue15544115155755"><a name="parmvalue15544115155755"></a><a name="parmvalue15544115155755"></a>“true”</span>表示请求执行成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0069077927_row40217981"><td class="cellrowborder" valign="top" width="19.79%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0069077927_p36431005"><a name="zh-cn_topic_0069077927_p36431005"></a><a name="zh-cn_topic_0069077927_p36431005"></a>message</p>
</td>
<td class="cellrowborder" valign="top" width="9.43%" headers="mcps1.2.5.1.2 "><p id="p95842301382"><a name="p95842301382"></a><a name="p95842301382"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="9.9%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0069077927_p49163111"><a name="zh-cn_topic_0069077927_p49163111"></a><a name="zh-cn_topic_0069077927_p49163111"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60.88%" headers="mcps1.2.5.1.4 "><p id="a4fa277540d3e42e48cec2027a36ca6bc"><a name="a4fa277540d3e42e48cec2027a36ca6bc"></a><a name="a4fa277540d3e42e48cec2027a36ca6bc"></a>系统提示信息，执行成功时，信息可能为空。</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section17446171164041"></a>

-   请求样例：
    -   **描述:**

        创建DLI用户委托。

    -   **示例URL:**

        POST https://dli.cn-north-1.myhuaweicloud.com/v2/330e068af1334c9782f4226acc00a2e2/agency

    -   **值:**

        ```
        {
            "roles": [
                "ctable_adm",
                "vpc_netadm",
                "dis_adm",
                "smn_adm",
                "obs_adm"
            ]
        }
        ```


-   成功响应样例：

    ```
    {
        "is_success": true,
        "message": ""
    }
    ```


## 状态码<a name="s1b495ba11cd9411c9ad2ee50103334a7"></a>

状态码如[表4](#t43c1f1c0ba344f4cbcb270953d9cca2a)所示。

**表 4**  状态码

<a name="t43c1f1c0ba344f4cbcb270953d9cca2a"></a>
<table><thead align="left"><tr id="r2ad0f008ce2248a1800a3e8b77226a56"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.3.1.1"><p id="afa33b7f5b0ac4d008ebcf6493f629b24"><a name="afa33b7f5b0ac4d008ebcf6493f629b24"></a><a name="afa33b7f5b0ac4d008ebcf6493f629b24"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="70%" id="mcps1.2.3.1.2"><p id="af801170b350b4f8ba3b575c7ddb8b13e"><a name="af801170b350b4f8ba3b575c7ddb8b13e"></a><a name="af801170b350b4f8ba3b575c7ddb8b13e"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="r0b449b1d3b8c498ea3e6cce16c80a14c"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="a8c63a97e3bad402ebaead0bd99cad632"><a name="a8c63a97e3bad402ebaead0bd99cad632"></a><a name="a8c63a97e3bad402ebaead0bd99cad632"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p528373855714"><a name="p528373855714"></a><a name="p528373855714"></a>创建成功。</p>
</td>
</tr>
<tr id="row1012873412149"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p1912813348145"><a name="p1912813348145"></a><a name="p1912813348145"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p154287617445"><a name="p154287617445"></a><a name="p154287617445"></a>请求失败。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section13596141025715"></a>

调用接口出错后，将不会返回上述结果，而是返回错误码和错误信息，更多介绍请参见[错误码](错误码.md)。

