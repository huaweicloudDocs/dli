# 上传file类型分组资源<a name="dli_02_0171"></a>

## 功能介绍<a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_s1f0e4fd3d502405199f36f78e68721aa"></a>

该API用于在project下上传file类型模块。

>![](public_sys-resources/icon-note.gif) **说明：**   
>上传同名file模块时，新模块将会覆盖旧模块。  

## URI<a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_s9e1b8ec5b57c422a942b19835da7d66e"></a>

-   URI格式：

    POST /v2.0/\{project\_id\}/resources/files

-   参数说明

    **表 1**  URI参数说明

    <a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_zh-cn_topic_0069077803_table60779388"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_zh-cn_topic_0069077803_row61411666"><th class="cellrowborder" valign="top" width="12.67%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_a420a62a594f9410eaea229ffc8037a61"><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_a420a62a594f9410eaea229ffc8037a61"></a><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_a420a62a594f9410eaea229ffc8037a61"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="13.209999999999999%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p873025824211"><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p873025824211"></a><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p873025824211"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="74.11999999999999%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_a692d3cd97b464aed90ba6d841900a4a5"><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_a692d3cd97b464aed90ba6d841900a4a5"></a><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_a692d3cd97b464aed90ba6d841900a4a5"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_zh-cn_topic_0069077803_row48589216"><td class="cellrowborder" valign="top" width="12.67%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p43412436"><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p43412436"></a><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p43412436"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.209999999999999%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p26746391"><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p26746391"></a><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p26746391"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.11999999999999%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p18974100"><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p18974100"></a><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p18974100"></a>项目编号，用于资源隔离。获取方式请参考<a href="获取项目编号.md">获取项目编号</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_section20458182103"></a>

请求参数如[表2](#zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_table179951251504)所示。

**表 2**  请求参数

<a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_table179951251504"></a>
<table><thead align="left"><tr id="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_row21116408"><th class="cellrowborder" valign="top" width="10.03%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_p221862014"><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_p221862014"></a><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_p221862014"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="9.15%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_p173767015"><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_p173767015"></a><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_p173767015"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="14.39%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_p2486705"><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_p2486705"></a><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_p2486705"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="66.43%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_p4746002"><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_p4746002"></a><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_p4746002"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_row1573617015"><td class="cellrowborder" valign="top" width="10.03%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0142813187_zh-cn_topic_0103345073_p12331150116"><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_p12331150116"></a><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_p12331150116"></a>paths</p>
</td>
<td class="cellrowborder" valign="top" width="9.15%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0142813187_zh-cn_topic_0103345073_p53321202013"><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_p53321202013"></a><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_p53321202013"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.39%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0142813187_zh-cn_topic_0103345073_p123324013118"><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_p123324013118"></a><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_p123324013118"></a>List of String</p>
</td>
<td class="cellrowborder" valign="top" width="66.43%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0142813187_zh-cn_topic_0103345073_p1033215011114"><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_p1033215011114"></a><a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_p1033215011114"></a>用户OBS对象路径列表，OBS对象路径为OBS对象URL。</p>
</td>
</tr>
<tr id="zh-cn_topic_0142813187_row158181227115617"><td class="cellrowborder" valign="top" width="10.03%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0142813187_p21031919165319"><a name="zh-cn_topic_0142813187_p21031919165319"></a><a name="zh-cn_topic_0142813187_p21031919165319"></a>group</p>
</td>
<td class="cellrowborder" valign="top" width="9.15%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0142813187_p610351913531"><a name="zh-cn_topic_0142813187_p610351913531"></a><a name="zh-cn_topic_0142813187_p610351913531"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.39%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0142813187_p9103141910537"><a name="zh-cn_topic_0142813187_p9103141910537"></a><a name="zh-cn_topic_0142813187_p9103141910537"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="66.43%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0142813187_p2103319135315"><a name="zh-cn_topic_0142813187_p2103319135315"></a><a name="zh-cn_topic_0142813187_p2103319135315"></a>所属资源分组名。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_sd1ecb66580054b2ea403be8b2272a2c7"></a>

**响应参数**

响应参数可参考[表3](上传jar类型分组资源.md#zh-cn_topic_0103345069_zh-cn_topic_0102902530_zh-cn_topic_0069077927_table56638444)。

## 示例<a name="zh-cn_topic_0142813187_zh-cn_topic_0103345073_zh-cn_topic_0102902533_section17446171164041"></a>

-   请求样例：

    ```
    {
        "paths": [
            https: //xkftest.obs.huawei.com/spark.py,
            "https://xkftest.obs.huawei.com/spark.msi"
        ]"group": " gatk"
    }
    ```

-   成功响应样例：

    ```
    {
        "group_name": "gatk",
        "status": "READY",
        "resources": [
            "spark.py ",
            " spark.msi"
        ],
        "create_time": 1521532893736,
        "update_time": 1521552364503
    }
    ```


