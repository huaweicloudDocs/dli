# 上传jar类型分组资源<a name="dli_02_0169"></a>

## 功能介绍<a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_s1f0e4fd3d502405199f36f78e68721aa"></a>

该API用于在project下上传jar类型分组资源。

>![](public_sys-resources/icon-note.gif) **说明：**   
>上传同名资源模块时，新模块将会覆盖旧模块。  

## URI<a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_s9e1b8ec5b57c422a942b19835da7d66e"></a>

-   URI格式：

    POST /v2.0/\{project\_id\}/resources/jars

-   参数说明

    **表 1**  URI参数说明

    <a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_zh-cn_topic_0069077803_table60779388"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_zh-cn_topic_0069077803_row61411666"><th class="cellrowborder" valign="top" width="13.209999999999999%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_a420a62a594f9410eaea229ffc8037a61"><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_a420a62a594f9410eaea229ffc8037a61"></a><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_a420a62a594f9410eaea229ffc8037a61"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.6%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_zh-cn_topic_0069077803_p873025824211"><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_zh-cn_topic_0069077803_p873025824211"></a><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_zh-cn_topic_0069077803_p873025824211"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="68.19%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_a692d3cd97b464aed90ba6d841900a4a5"><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_a692d3cd97b464aed90ba6d841900a4a5"></a><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_a692d3cd97b464aed90ba6d841900a4a5"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_zh-cn_topic_0069077803_row48589216"><td class="cellrowborder" valign="top" width="13.209999999999999%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_zh-cn_topic_0069077803_p43412436"><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_zh-cn_topic_0069077803_p43412436"></a><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_zh-cn_topic_0069077803_p43412436"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.6%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_zh-cn_topic_0069077803_p26746391"><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_zh-cn_topic_0069077803_p26746391"></a><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_zh-cn_topic_0069077803_p26746391"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="68.19%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_zh-cn_topic_0069077803_p18974100"><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_zh-cn_topic_0069077803_p18974100"></a><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_zh-cn_topic_0069077803_p18974100"></a>项目编号，用于资源隔离。获取方式请参考<a href="获取项目编号.md">获取项目编号</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_section20458182103"></a>

请求参数如[表2](#zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_table179951251504)所示。

**表 2**  请求参数

<a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_table179951251504"></a>
<table><thead align="left"><tr id="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_row21116408"><th class="cellrowborder" valign="top" width="13.69%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_p221862014"><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_p221862014"></a><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_p221862014"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="12.55%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_p173767015"><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_p173767015"></a><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_p173767015"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="15.690000000000001%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_p2486705"><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_p2486705"></a><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_p2486705"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="58.07%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_p4746002"><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_p4746002"></a><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_p4746002"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_row1573617015"><td class="cellrowborder" valign="top" width="13.69%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0142813185_zh-cn_topic_0103345071_p12331150116"><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_p12331150116"></a><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_p12331150116"></a>paths</p>
</td>
<td class="cellrowborder" valign="top" width="12.55%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0142813185_zh-cn_topic_0103345071_p53321202013"><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_p53321202013"></a><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_p53321202013"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="15.690000000000001%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0142813185_zh-cn_topic_0103345071_p123324013118"><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_p123324013118"></a><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_p123324013118"></a>List of String</p>
</td>
<td class="cellrowborder" valign="top" width="58.07%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0142813185_zh-cn_topic_0103345071_p1033215011114"><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_p1033215011114"></a><a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_p1033215011114"></a>用户OBS对象路径列表，OBS对象路径为OBS对象URL。</p>
</td>
</tr>
<tr id="zh-cn_topic_0142813185_row1289152462516"><td class="cellrowborder" valign="top" width="13.69%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0142813185_p21031919165319"><a name="zh-cn_topic_0142813185_p21031919165319"></a><a name="zh-cn_topic_0142813185_p21031919165319"></a>group</p>
</td>
<td class="cellrowborder" valign="top" width="12.55%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0142813185_p610351913531"><a name="zh-cn_topic_0142813185_p610351913531"></a><a name="zh-cn_topic_0142813185_p610351913531"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="15.690000000000001%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0142813185_p9103141910537"><a name="zh-cn_topic_0142813185_p9103141910537"></a><a name="zh-cn_topic_0142813185_p9103141910537"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="58.07%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0142813185_p2103319135315"><a name="zh-cn_topic_0142813185_p2103319135315"></a><a name="zh-cn_topic_0142813185_p2103319135315"></a>所属资源分组名。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_sd1ecb66580054b2ea403be8b2272a2c7"></a>

**响应参数**

**表 3**  响应参数说明

<a name="zh-cn_topic_0103345069_zh-cn_topic_0102902530_zh-cn_topic_0069077927_table56638444"></a>
<table><thead align="left"><tr id="zh-cn_topic_0103345069_zh-cn_topic_0102902530_zh-cn_topic_0069077927_row48911609"><th class="cellrowborder" valign="top" width="14.12%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0103345069_zh-cn_topic_0102902530_ae076f6b3f1bf463b9cc087fc566253d5"><a name="zh-cn_topic_0103345069_zh-cn_topic_0102902530_ae076f6b3f1bf463b9cc087fc566253d5"></a><a name="zh-cn_topic_0103345069_zh-cn_topic_0102902530_ae076f6b3f1bf463b9cc087fc566253d5"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="12.29%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0103345069_zh-cn_topic_0102902530_a59685f4525af4d82a623288ff8ccb0f4"><a name="zh-cn_topic_0103345069_zh-cn_topic_0102902530_a59685f4525af4d82a623288ff8ccb0f4"></a><a name="zh-cn_topic_0103345069_zh-cn_topic_0102902530_a59685f4525af4d82a623288ff8ccb0f4"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="73.59%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0103345069_zh-cn_topic_0102902530_zh-cn_topic_0069077927_p632718127368"><a name="zh-cn_topic_0103345069_zh-cn_topic_0102902530_zh-cn_topic_0069077927_p632718127368"></a><a name="zh-cn_topic_0103345069_zh-cn_topic_0102902530_zh-cn_topic_0069077927_p632718127368"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0103345069_zh-cn_topic_0102902530_row1458133461718"><td class="cellrowborder" valign="top" width="14.12%" headers="mcps1.2.4.1.1 "><p id="p9109112219199"><a name="p9109112219199"></a><a name="p9109112219199"></a>module_name</p>
</td>
<td class="cellrowborder" valign="top" width="12.29%" headers="mcps1.2.4.1.2 "><p id="p151091122131920"><a name="p151091122131920"></a><a name="p151091122131920"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="73.59%" headers="mcps1.2.4.1.3 "><p id="p61091722101915"><a name="p61091722101915"></a><a name="p61091722101915"></a>资源模块名。</p>
</td>
</tr>
<tr id="row29122021590"><td class="cellrowborder" valign="top" width="14.12%" headers="mcps1.2.4.1.1 "><p id="p45091837186"><a name="p45091837186"></a><a name="p45091837186"></a>module_type</p>
</td>
<td class="cellrowborder" valign="top" width="12.29%" headers="mcps1.2.4.1.2 "><p id="p1850911310189"><a name="p1850911310189"></a><a name="p1850911310189"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="73.59%" headers="mcps1.2.4.1.3 "><p id="p050933161816"><a name="p050933161816"></a><a name="p050933161816"></a>资源模块类型，具体可参考<a href="#zh-cn_topic_0103345069_table399612265336">表4</a>。</p>
</td>
</tr>
<tr id="row1230416516598"><td class="cellrowborder" valign="top" width="14.12%" headers="mcps1.2.4.1.1 "><p id="p12915652134"><a name="p12915652134"></a><a name="p12915652134"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="12.29%" headers="mcps1.2.4.1.2 "><p id="p159161556136"><a name="p159161556136"></a><a name="p159161556136"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="73.59%" headers="mcps1.2.4.1.3 "><p id="p186892422817"><a name="p186892422817"></a><a name="p186892422817"></a>"UPLOADING"表示正在上传。</p>
<p id="p11500113182814"><a name="p11500113182814"></a><a name="p11500113182814"></a>"READY"表示模块包已上传。</p>
<p id="p19171510139"><a name="p19171510139"></a><a name="p19171510139"></a>"FAILED"表示模块包上传失败。</p>
</td>
</tr>
<tr id="row390811715915"><td class="cellrowborder" valign="top" width="14.12%" headers="mcps1.2.4.1.1 "><p id="p13504224111511"><a name="p13504224111511"></a><a name="p13504224111511"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="12.29%" headers="mcps1.2.4.1.2 "><p id="p65041124111515"><a name="p65041124111515"></a><a name="p65041124111515"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="73.59%" headers="mcps1.2.4.1.3 "><p id="p9504724161510"><a name="p9504724161510"></a><a name="p9504724161510"></a>资源模块描述。</p>
</td>
</tr>
<tr id="row4201110145912"><td class="cellrowborder" valign="top" width="14.12%" headers="mcps1.2.4.1.1 "><p id="p125238157159"><a name="p125238157159"></a><a name="p125238157159"></a>resources</p>
</td>
<td class="cellrowborder" valign="top" width="12.29%" headers="mcps1.2.4.1.2 "><p id="p752331519152"><a name="p752331519152"></a><a name="p752331519152"></a>List of String</p>
</td>
<td class="cellrowborder" valign="top" width="73.59%" headers="mcps1.2.4.1.3 "><p id="p75238153159"><a name="p75238153159"></a><a name="p75238153159"></a>该资源模块包含的资源包名列表。</p>
</td>
</tr>
<tr id="row122231213105910"><td class="cellrowborder" valign="top" width="14.12%" headers="mcps1.2.4.1.1 "><p id="p1890011591314"><a name="p1890011591314"></a><a name="p1890011591314"></a>create_time</p>
</td>
<td class="cellrowborder" valign="top" width="12.29%" headers="mcps1.2.4.1.2 "><p id="p0902551133"><a name="p0902551133"></a><a name="p0902551133"></a>Long</p>
</td>
<td class="cellrowborder" valign="top" width="73.59%" headers="mcps1.2.4.1.3 "><p id="p139033591313"><a name="p139033591313"></a><a name="p139033591313"></a>资源模块上传的unix时间戳。</p>
</td>
</tr>
<tr id="row1159917159594"><td class="cellrowborder" valign="top" width="14.12%" headers="mcps1.2.4.1.1 "><p id="p1790420571316"><a name="p1790420571316"></a><a name="p1790420571316"></a>update_time</p>
</td>
<td class="cellrowborder" valign="top" width="12.29%" headers="mcps1.2.4.1.2 "><p id="p1690519581315"><a name="p1690519581315"></a><a name="p1690519581315"></a>Long</p>
</td>
<td class="cellrowborder" valign="top" width="73.59%" headers="mcps1.2.4.1.3 "><p id="p199061756134"><a name="p199061756134"></a><a name="p199061756134"></a>资源模块更新的unix时间戳。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  资源模块类型说明

<a name="zh-cn_topic_0103345069_table399612265336"></a>
<table><thead align="left"><tr id="zh-cn_topic_0103345069_row7997526203318"><th class="cellrowborder" valign="top" width="22.58%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0103345069_p799752614334"><a name="zh-cn_topic_0103345069_p799752614334"></a><a name="zh-cn_topic_0103345069_p799752614334"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="77.42%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0103345069_p3997142610332"><a name="zh-cn_topic_0103345069_p3997142610332"></a><a name="zh-cn_topic_0103345069_p3997142610332"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0103345069_row1499782619333"><td class="cellrowborder" valign="top" width="22.58%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0103345069_p1199718260334"><a name="zh-cn_topic_0103345069_p1199718260334"></a><a name="zh-cn_topic_0103345069_p1199718260334"></a>jar</p>
</td>
<td class="cellrowborder" valign="top" width="77.42%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0103345069_p6997172615334"><a name="zh-cn_topic_0103345069_p6997172615334"></a><a name="zh-cn_topic_0103345069_p6997172615334"></a>用户jar文件。</p>
</td>
</tr>
<tr id="zh-cn_topic_0103345069_row5997132613314"><td class="cellrowborder" valign="top" width="22.58%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0103345069_p11997326103318"><a name="zh-cn_topic_0103345069_p11997326103318"></a><a name="zh-cn_topic_0103345069_p11997326103318"></a>pyFile</p>
</td>
<td class="cellrowborder" valign="top" width="77.42%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0103345069_p18997182663319"><a name="zh-cn_topic_0103345069_p18997182663319"></a><a name="zh-cn_topic_0103345069_p18997182663319"></a>用户python文件。</p>
</td>
</tr>
<tr id="zh-cn_topic_0103345069_row6571522163414"><td class="cellrowborder" valign="top" width="22.58%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0103345069_p1577228344"><a name="zh-cn_topic_0103345069_p1577228344"></a><a name="zh-cn_topic_0103345069_p1577228344"></a>file</p>
</td>
<td class="cellrowborder" valign="top" width="77.42%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0103345069_p257132215341"><a name="zh-cn_topic_0103345069_p257132215341"></a><a name="zh-cn_topic_0103345069_p257132215341"></a>用户文件。</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="zh-cn_topic_0142813185_zh-cn_topic_0103345071_zh-cn_topic_0102902532_section17446171164041"></a>

-   请求样例：

    ```
    {
        "paths": [
            "https://xkftest.obs.huawei.com/spark.jar",
            "https://xkftest.obs.huawei.com/tika-core-1.18.jar",
            "https://xkftest.obs.huawei.com/s3fs-2.2.2.jar"
        ],
        "group": "gatk"
    }
    ```

-   成功响应样例：

    ```
    {
        {
            "group_name": "gatk",
            "status": "READY",
            "resources": [
                "gatk.jar",
                "tika-core-1.18.jar",
                "s3fs-2.2.2.jar"
            ],
            "create_time": 1521532893736,
            "update_time": 1521552364503
        }
    ```


