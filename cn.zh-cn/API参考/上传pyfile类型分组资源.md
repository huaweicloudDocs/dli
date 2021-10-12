# 上传pyfile类型分组资源<a name="dli_02_0170"></a>

## 功能介绍<a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_s1f0e4fd3d502405199f36f78e68721aa"></a>

该API用于在project下的上传pyfile类型模块。

>![](public_sys-resources/icon-note.gif) **说明：** 
>上传同名pyfile类型模块时，新模块将会覆盖旧模块。

## 调试<a name="section556523314214"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=DLI&api=UploadPythonFiles)中调试该接口。

## URI<a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_s9e1b8ec5b57c422a942b19835da7d66e"></a>

-   URI格式：

    POST /v2.0/\{project\_id\}/resources/pyfiles

-   参数说明

    **表 1**  URI参数说明

    <a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_zh-cn_topic_0069077803_table60779388"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_zh-cn_topic_0069077803_row61411666"><th class="cellrowborder" valign="top" width="15.870000000000001%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_a420a62a594f9410eaea229ffc8037a61"><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_a420a62a594f9410eaea229ffc8037a61"></a><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_a420a62a594f9410eaea229ffc8037a61"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="10.39%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p873025824211"><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p873025824211"></a><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p873025824211"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="10.79%" id="mcps1.2.5.1.3"><p id="p111031126520"><a name="p111031126520"></a><a name="p111031126520"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="62.949999999999996%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_a692d3cd97b464aed90ba6d841900a4a5"><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_a692d3cd97b464aed90ba6d841900a4a5"></a><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_a692d3cd97b464aed90ba6d841900a4a5"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_zh-cn_topic_0069077803_row48589216"><td class="cellrowborder" valign="top" width="15.870000000000001%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p43412436"><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p43412436"></a><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p43412436"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.39%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p26746391"><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p26746391"></a><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_zh-cn_topic_0069077803_p26746391"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.79%" headers="mcps1.2.5.1.3 "><p id="p610419212515"><a name="p610419212515"></a><a name="p610419212515"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.949999999999996%" headers="mcps1.2.5.1.4 "><p id="p1310472724012"><a name="p1310472724012"></a><a name="p1310472724012"></a>项目编号，用于资源隔离。获取方式请参考<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_section20458182103"></a>

**表 2**  请求参数

<a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_table179951251504"></a>
<table><thead align="left"><tr id="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_row21116408"><th class="cellrowborder" valign="top" width="18.310000000000002%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_p221862014"><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_p221862014"></a><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_p221862014"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="12.64%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_p173767015"><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_p173767015"></a><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_p173767015"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="17.69%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_p2486705"><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_p2486705"></a><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_p2486705"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="51.35999999999999%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_p4746002"><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_p4746002"></a><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_p4746002"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_row1573617015"><td class="cellrowborder" valign="top" width="18.310000000000002%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0142813186_zh-cn_topic_0103345072_p12331150116"><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_p12331150116"></a><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_p12331150116"></a>paths</p>
</td>
<td class="cellrowborder" valign="top" width="12.64%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0142813186_zh-cn_topic_0103345072_p53321202013"><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_p53321202013"></a><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_p53321202013"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0142813186_zh-cn_topic_0103345072_p123324013118"><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_p123324013118"></a><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_p123324013118"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0142813186_zh-cn_topic_0103345072_p1033215011114"><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_p1033215011114"></a><a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_p1033215011114"></a>用户OBS对象路径列表，OBS对象路径为OBS对象URL。</p>
</td>
</tr>
<tr id="zh-cn_topic_0142813186_row7807841507"><td class="cellrowborder" valign="top" width="18.310000000000002%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0142813186_p21031919165319"><a name="zh-cn_topic_0142813186_p21031919165319"></a><a name="zh-cn_topic_0142813186_p21031919165319"></a>group</p>
</td>
<td class="cellrowborder" valign="top" width="12.64%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0142813186_p610351913531"><a name="zh-cn_topic_0142813186_p610351913531"></a><a name="zh-cn_topic_0142813186_p610351913531"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0142813186_p9103141910537"><a name="zh-cn_topic_0142813186_p9103141910537"></a><a name="zh-cn_topic_0142813186_p9103141910537"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0142813186_p2103319135315"><a name="zh-cn_topic_0142813186_p2103319135315"></a><a name="zh-cn_topic_0142813186_p2103319135315"></a>所属资源分组名。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="zh-cn_topic_0142813183_zh-cn_topic_0103345073_zh-cn_topic_0102902533_sd1ecb66580054b2ea403be8b2272a2c7"></a>

**表 3**  响应参数

<a name="zh-cn_topic_0142813183_table051933920813"></a>
<table><thead align="left"><tr id="zh-cn_topic_0142813183_row852411395818"><th class="cellrowborder" valign="top" width="16.85%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0142813183_p452513399816"><a name="zh-cn_topic_0142813183_p452513399816"></a><a name="zh-cn_topic_0142813183_p452513399816"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="10.83%" id="mcps1.2.5.1.2"><p id="p7267177395"><a name="p7267177395"></a><a name="p7267177395"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="15.229999999999999%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0142813183_p95271639882"><a name="zh-cn_topic_0142813183_p95271639882"></a><a name="zh-cn_topic_0142813183_p95271639882"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="57.089999999999996%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0142813183_p125299391183"><a name="zh-cn_topic_0142813183_p125299391183"></a><a name="zh-cn_topic_0142813183_p125299391183"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0142813183_row353014398813"><td class="cellrowborder" valign="top" width="16.85%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0142813183_p0558193912915"><a name="zh-cn_topic_0142813183_p0558193912915"></a><a name="zh-cn_topic_0142813183_p0558193912915"></a>group_name</p>
</td>
<td class="cellrowborder" valign="top" width="10.83%" headers="mcps1.2.5.1.2 "><p id="p8267117153915"><a name="p8267117153915"></a><a name="p8267117153915"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.229999999999999%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0142813183_p255893916917"><a name="zh-cn_topic_0142813183_p255893916917"></a><a name="zh-cn_topic_0142813183_p255893916917"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="57.089999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0142813183_p1855817392092"><a name="zh-cn_topic_0142813183_p1855817392092"></a><a name="zh-cn_topic_0142813183_p1855817392092"></a>模块名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0142813183_row253515391481"><td class="cellrowborder" valign="top" width="16.85%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0142813183_p13558123916911"><a name="zh-cn_topic_0142813183_p13558123916911"></a><a name="zh-cn_topic_0142813183_p13558123916911"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="10.83%" headers="mcps1.2.5.1.2 "><p id="p19267157183916"><a name="p19267157183916"></a><a name="p19267157183916"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.229999999999999%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0142813183_p205591391992"><a name="zh-cn_topic_0142813183_p205591391992"></a><a name="zh-cn_topic_0142813183_p205591391992"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="57.089999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0142813183_p35594391919"><a name="zh-cn_topic_0142813183_p35594391919"></a><a name="zh-cn_topic_0142813183_p35594391919"></a>上传分组资源状态。</p>
</td>
</tr>
<tr id="zh-cn_topic_0142813183_row56285413914"><td class="cellrowborder" valign="top" width="16.85%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0142813183_p135592391891"><a name="zh-cn_topic_0142813183_p135592391891"></a><a name="zh-cn_topic_0142813183_p135592391891"></a>resources</p>
</td>
<td class="cellrowborder" valign="top" width="10.83%" headers="mcps1.2.5.1.2 "><p id="p172674718392"><a name="p172674718392"></a><a name="p172674718392"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.229999999999999%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0142813183_p555920398916"><a name="zh-cn_topic_0142813183_p555920398916"></a><a name="zh-cn_topic_0142813183_p555920398916"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="57.089999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0142813183_p105595392916"><a name="zh-cn_topic_0142813183_p105595392916"></a><a name="zh-cn_topic_0142813183_p105595392916"></a>该模块包含的资源包名列表。</p>
</td>
</tr>
<tr id="row15250103117368"><td class="cellrowborder" valign="top" width="16.85%" headers="mcps1.2.5.1.1 "><p id="p17251143113617"><a name="p17251143113617"></a><a name="p17251143113617"></a>details</p>
</td>
<td class="cellrowborder" valign="top" width="10.83%" headers="mcps1.2.5.1.2 "><p id="p10251113133615"><a name="p10251113133615"></a><a name="p10251113133615"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.229999999999999%" headers="mcps1.2.5.1.3 "><p id="p13251183153619"><a name="p13251183153619"></a><a name="p13251183153619"></a>Array of body</p>
</td>
<td class="cellrowborder" valign="top" width="57.089999999999996%" headers="mcps1.2.5.1.4 "><p id="p6251163103615"><a name="p6251163103615"></a><a name="p6251163103615"></a>分组资源包的详细信息。具体请参考<a href="#zh-cn_topic_0103345070_table111231336220">表4</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0142813183_row53798101497"><td class="cellrowborder" valign="top" width="16.85%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0142813183_p15559139391"><a name="zh-cn_topic_0142813183_p15559139391"></a><a name="zh-cn_topic_0142813183_p15559139391"></a>create_time</p>
</td>
<td class="cellrowborder" valign="top" width="10.83%" headers="mcps1.2.5.1.2 "><p id="p13267172397"><a name="p13267172397"></a><a name="p13267172397"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.229999999999999%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0142813183_p1055916391492"><a name="zh-cn_topic_0142813183_p1055916391492"></a><a name="zh-cn_topic_0142813183_p1055916391492"></a>Long</p>
</td>
<td class="cellrowborder" valign="top" width="57.089999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0142813183_p8559839798"><a name="zh-cn_topic_0142813183_p8559839798"></a><a name="zh-cn_topic_0142813183_p8559839798"></a>模块上传的unix时间戳。</p>
</td>
</tr>
<tr id="zh-cn_topic_0142813183_row1538239489"><td class="cellrowborder" valign="top" width="16.85%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0142813183_p65593391794"><a name="zh-cn_topic_0142813183_p65593391794"></a><a name="zh-cn_topic_0142813183_p65593391794"></a>update_time</p>
</td>
<td class="cellrowborder" valign="top" width="10.83%" headers="mcps1.2.5.1.2 "><p id="p926777153919"><a name="p926777153919"></a><a name="p926777153919"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.229999999999999%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0142813183_p055913396910"><a name="zh-cn_topic_0142813183_p055913396910"></a><a name="zh-cn_topic_0142813183_p055913396910"></a>Long</p>
</td>
<td class="cellrowborder" valign="top" width="57.089999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0142813183_p9559439094"><a name="zh-cn_topic_0142813183_p9559439094"></a><a name="zh-cn_topic_0142813183_p9559439094"></a>模块更新的unix时间戳。</p>
</td>
</tr>
<tr id="row7148120153319"><td class="cellrowborder" valign="top" width="16.85%" headers="mcps1.2.5.1.1 "><p id="p1047414300516"><a name="p1047414300516"></a><a name="p1047414300516"></a>is_async</p>
</td>
<td class="cellrowborder" valign="top" width="10.83%" headers="mcps1.2.5.1.2 "><p id="p2047453014513"><a name="p2047453014513"></a><a name="p2047453014513"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.229999999999999%" headers="mcps1.2.5.1.3 "><p id="p1747403019517"><a name="p1747403019517"></a><a name="p1747403019517"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="57.089999999999996%" headers="mcps1.2.5.1.4 "><p id="p7474173019511"><a name="p7474173019511"></a><a name="p7474173019511"></a>是否使用异步方式上传资源包。默认值为“false”，表示不使用异步方式。推荐使用异步方式上传资源包。</p>
</td>
</tr>
<tr id="row55561943127"><td class="cellrowborder" valign="top" width="16.85%" headers="mcps1.2.5.1.1 "><p id="p1291831513129"><a name="p1291831513129"></a><a name="p1291831513129"></a>owner</p>
</td>
<td class="cellrowborder" valign="top" width="10.83%" headers="mcps1.2.5.1.2 "><p id="p10290923101217"><a name="p10290923101217"></a><a name="p10290923101217"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.229999999999999%" headers="mcps1.2.5.1.3 "><p id="p199192154121"><a name="p199192154121"></a><a name="p199192154121"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="57.089999999999996%" headers="mcps1.2.5.1.4 "><p id="p491951591219"><a name="p491951591219"></a><a name="p491951591219"></a>资源包拥有者。</p>
</td>
</tr>
<tr id="row910931974019"><td class="cellrowborder" valign="top" width="16.85%" headers="mcps1.2.5.1.1 "><p id="p1651043015362"><a name="p1651043015362"></a><a name="p1651043015362"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="10.83%" headers="mcps1.2.5.1.2 "><p id="p13510123023619"><a name="p13510123023619"></a><a name="p13510123023619"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.229999999999999%" headers="mcps1.2.5.1.3 "><p id="p95109307363"><a name="p95109307363"></a><a name="p95109307363"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="57.089999999999996%" headers="mcps1.2.5.1.4 "><p id="p2510230103616"><a name="p2510230103616"></a><a name="p2510230103616"></a>资源模块描述。</p>
</td>
</tr>
<tr id="row11119194409"><td class="cellrowborder" valign="top" width="16.85%" headers="mcps1.2.5.1.1 "><p id="p1772416436343"><a name="p1772416436343"></a><a name="p1772416436343"></a>module_name</p>
</td>
<td class="cellrowborder" valign="top" width="10.83%" headers="mcps1.2.5.1.2 "><p id="p572419433348"><a name="p572419433348"></a><a name="p572419433348"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.229999999999999%" headers="mcps1.2.5.1.3 "><p id="p12724543183417"><a name="p12724543183417"></a><a name="p12724543183417"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="57.089999999999996%" headers="mcps1.2.5.1.4 "><p id="p37246432349"><a name="p37246432349"></a><a name="p37246432349"></a>资源模块名</p>
</td>
</tr>
<tr id="row19111131914015"><td class="cellrowborder" valign="top" width="16.85%" headers="mcps1.2.5.1.1 "><p id="p4724204393413"><a name="p4724204393413"></a><a name="p4724204393413"></a>module_type</p>
</td>
<td class="cellrowborder" valign="top" width="10.83%" headers="mcps1.2.5.1.2 "><p id="p35291456144014"><a name="p35291456144014"></a><a name="p35291456144014"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.229999999999999%" headers="mcps1.2.5.1.3 "><p id="p572420437345"><a name="p572420437345"></a><a name="p572420437345"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="57.089999999999996%" headers="mcps1.2.5.1.4 "><p id="p1264102883811"><a name="p1264102883811"></a><a name="p1264102883811"></a>资源模块类型。</p>
<a name="ul148307107399"></a><a name="ul148307107399"></a><ul id="ul148307107399"><li>jar：用户jar文件;</li><li>pyFile：用户python文件;</li><li>file：用户文件。</li></ul>
</td>
</tr>
</tbody>
</table>

**表 4**  details参数说明

<a name="zh-cn_topic_0103345070_table111231336220"></a>
<table><thead align="left"><tr id="zh-cn_topic_0103345070_row1212512372214"><th class="cellrowborder" valign="top" width="18.08%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0103345070_p1112513318227"><a name="zh-cn_topic_0103345070_p1112513318227"></a><a name="zh-cn_topic_0103345070_p1112513318227"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="11.87%" id="mcps1.2.5.1.2"><p id="p1840182919108"><a name="p1840182919108"></a><a name="p1840182919108"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="15.370000000000001%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0103345070_p112620342217"><a name="zh-cn_topic_0103345070_p112620342217"></a><a name="zh-cn_topic_0103345070_p112620342217"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="54.67999999999999%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0103345070_p912873182218"><a name="zh-cn_topic_0103345070_p912873182218"></a><a name="zh-cn_topic_0103345070_p912873182218"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0103345070_row812818312218"><td class="cellrowborder" valign="top" width="18.08%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0103345070_p0227151292217"><a name="zh-cn_topic_0103345070_p0227151292217"></a><a name="zh-cn_topic_0103345070_p0227151292217"></a>create_time</p>
</td>
<td class="cellrowborder" valign="top" width="11.87%" headers="mcps1.2.5.1.2 "><p id="p540116290105"><a name="p540116290105"></a><a name="p540116290105"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.370000000000001%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0103345070_p612916315229"><a name="zh-cn_topic_0103345070_p612916315229"></a><a name="zh-cn_topic_0103345070_p612916315229"></a>Long</p>
</td>
<td class="cellrowborder" valign="top" width="54.67999999999999%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0103345070_p312943182213"><a name="zh-cn_topic_0103345070_p312943182213"></a><a name="zh-cn_topic_0103345070_p312943182213"></a>资源包上传的unix时间。是单位为“毫秒”的时间戳。</p>
</td>
</tr>
<tr id="zh-cn_topic_0103345070_row894391515221"><td class="cellrowborder" valign="top" width="18.08%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0103345070_p139441615122212"><a name="zh-cn_topic_0103345070_p139441615122212"></a><a name="zh-cn_topic_0103345070_p139441615122212"></a>update_time</p>
</td>
<td class="cellrowborder" valign="top" width="11.87%" headers="mcps1.2.5.1.2 "><p id="p1140122910101"><a name="p1140122910101"></a><a name="p1140122910101"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.370000000000001%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0103345070_p99441415122211"><a name="zh-cn_topic_0103345070_p99441415122211"></a><a name="zh-cn_topic_0103345070_p99441415122211"></a>Long</p>
</td>
<td class="cellrowborder" valign="top" width="54.67999999999999%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0103345070_p12782122112311"><a name="zh-cn_topic_0103345070_p12782122112311"></a><a name="zh-cn_topic_0103345070_p12782122112311"></a>更新已上传资源包的unix时间。是单位为“毫秒”的时间戳。</p>
</td>
</tr>
<tr id="zh-cn_topic_0103345070_row360652516227"><td class="cellrowborder" valign="top" width="18.08%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0103345070_p960610257220"><a name="zh-cn_topic_0103345070_p960610257220"></a><a name="zh-cn_topic_0103345070_p960610257220"></a>resource_type</p>
</td>
<td class="cellrowborder" valign="top" width="11.87%" headers="mcps1.2.5.1.2 "><p id="p14011129181013"><a name="p14011129181013"></a><a name="p14011129181013"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.370000000000001%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0103345070_p1060672592211"><a name="zh-cn_topic_0103345070_p1060672592211"></a><a name="zh-cn_topic_0103345070_p1060672592211"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="54.67999999999999%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0103345070_p1560611254223"><a name="zh-cn_topic_0103345070_p1560611254223"></a><a name="zh-cn_topic_0103345070_p1560611254223"></a>资源类型，此处为pyFile。</p>
</td>
</tr>
<tr id="zh-cn_topic_0103345070_row981813205222"><td class="cellrowborder" valign="top" width="18.08%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0103345070_p1281822011226"><a name="zh-cn_topic_0103345070_p1281822011226"></a><a name="zh-cn_topic_0103345070_p1281822011226"></a>resource_name</p>
</td>
<td class="cellrowborder" valign="top" width="11.87%" headers="mcps1.2.5.1.2 "><p id="p440162914108"><a name="p440162914108"></a><a name="p440162914108"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.370000000000001%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0103345070_p3818192002212"><a name="zh-cn_topic_0103345070_p3818192002212"></a><a name="zh-cn_topic_0103345070_p3818192002212"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="54.67999999999999%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0103345070_p6819320152218"><a name="zh-cn_topic_0103345070_p6819320152218"></a><a name="zh-cn_topic_0103345070_p6819320152218"></a>资源名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0103345070_row1045112238221"><td class="cellrowborder" valign="top" width="18.08%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0103345070_p104511323182217"><a name="zh-cn_topic_0103345070_p104511323182217"></a><a name="zh-cn_topic_0103345070_p104511323182217"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="11.87%" headers="mcps1.2.5.1.2 "><p id="p840242951018"><a name="p840242951018"></a><a name="p840242951018"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.370000000000001%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0103345070_p10451523122217"><a name="zh-cn_topic_0103345070_p10451523122217"></a><a name="zh-cn_topic_0103345070_p10451523122217"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="54.67999999999999%" headers="mcps1.2.5.1.4 "><a name="ul13242203019348"></a><a name="ul13242203019348"></a><ul id="ul13242203019348"><li>"UPLOADING"表示正在上传。</li><li>"READY"表示资源包已上传。</li><li>"FAILED"表示资源包上传失败。</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0103345070_row7933118142218"><td class="cellrowborder" valign="top" width="18.08%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0103345070_p15933918192212"><a name="zh-cn_topic_0103345070_p15933918192212"></a><a name="zh-cn_topic_0103345070_p15933918192212"></a>underlying_name</p>
</td>
<td class="cellrowborder" valign="top" width="11.87%" headers="mcps1.2.5.1.2 "><p id="p1640213295102"><a name="p1640213295102"></a><a name="p1640213295102"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.370000000000001%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0103345070_p5933151810225"><a name="zh-cn_topic_0103345070_p5933151810225"></a><a name="zh-cn_topic_0103345070_p5933151810225"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="54.67999999999999%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0103345070_p693319187227"><a name="zh-cn_topic_0103345070_p693319187227"></a><a name="zh-cn_topic_0103345070_p693319187227"></a>资源包在队列中的名字。</p>
</td>
</tr>
<tr id="row51918271652"><td class="cellrowborder" valign="top" width="18.08%" headers="mcps1.2.5.1.1 "><p id="p179119526411"><a name="p179119526411"></a><a name="p179119526411"></a>is_async</p>
</td>
<td class="cellrowborder" valign="top" width="11.87%" headers="mcps1.2.5.1.2 "><p id="p6929521245"><a name="p6929521245"></a><a name="p6929521245"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.370000000000001%" headers="mcps1.2.5.1.3 "><p id="p4921521841"><a name="p4921521841"></a><a name="p4921521841"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="54.67999999999999%" headers="mcps1.2.5.1.4 "><p id="p1892105212416"><a name="p1892105212416"></a><a name="p1892105212416"></a>是否异步上传资源包。</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="zh-cn_topic_0142813186_zh-cn_topic_0103345072_zh-cn_topic_0102902533_section17446171164041"></a>

-   请求样例：

    ```
    {
        "paths": [
            "https://test.obs.huawei.com/dli_tf.py"
        ],
        "group": " gatk"
    }
    ```

-   成功响应样例：

    ```
    {
        "group_name": "gatk",
        "status": "READY",
        "resources": [
            "dli_tf.py"
        ],
        "details":[
            {
              "create_time":1608804435312,
              "update_time":1608804435312,
              "resource_type":"pyFile",
              "resource_name":"dli_tf.py",
              "status":"READY",
              "underlying_name":"dli_tf.py"
            }
           ],
        "create_time": 1521532893736,
        "update_time": 1521552364503,
        "is_async":false
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
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p104431642124811"><a name="p104431642124811"></a><a name="p104431642124811"></a>上传成功。</p>
</td>
</tr>
<tr id="row44937531727"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p184941532219"><a name="p184941532219"></a><a name="p184941532219"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p2049413539219"><a name="p2049413539219"></a><a name="p2049413539219"></a>请求错误。</p>
</td>
</tr>
<tr id="row65331212142411"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p5537171216249"><a name="p5537171216249"></a><a name="p5537171216249"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p953813124249"><a name="p953813124249"></a><a name="p953813124249"></a>内部服务器错误。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section13596141025715"></a>

调用接口出错后，将不会返回上述结果，而是返回错误码和错误信息，更多介绍请参见[错误码](错误码.md)。

