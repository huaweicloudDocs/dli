# Flink模板管理<a name="dli_01_0464"></a>

Flink模板包括样例模板和自定义模板。用户可以在已有的样例模板中进行修改，来实现实际的作业逻辑需求，节约编辑SQL语句的时间。也可以根据自己的习惯和方法自定义作业模板，方便后续可以直接调用或修改。

Flink模板管理主要包括如下功能：

-   [样例模板](#section3576173115914)
-   [自定义模板](#section4777152184911)
-   [新建模板](#section5417513171115)
-   [基于模板新建作业](#section123515484542)
-   [修改模板](#section735234815411)
-   [删除模板](#section1035264818548)

## 样例模板<a name="section3576173115914"></a>

样例模板列表显示已有的样例作业模板，样例模板列表参数说明如[表 1](#table17778105244916)所示。

**表 1**  样例模板列表参数

<a name="table1648113116167"></a>
<table><thead align="left"><tr id="row64828111162"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.3.1.1"><p id="p9482412165"><a name="p9482412165"></a><a name="p9482412165"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="80%" id="mcps1.2.3.1.2"><p id="p8482101141614"><a name="p8482101141614"></a><a name="p8482101141614"></a>参数说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1248221171613"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p1948219117166"><a name="p1948219117166"></a><a name="p1948219117166"></a>名称</p>
</td>
<td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p448216181618"><a name="p448216181618"></a><a name="p448216181618"></a>模板名称，只能由英文、中文、数字、中划线和下划线组成，并且长度为1～64个字符。</p>
</td>
</tr>
<tr id="row18482141141615"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p1148271131614"><a name="p1148271131614"></a><a name="p1148271131614"></a>描述</p>
</td>
<td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p1848213120160"><a name="p1848213120160"></a><a name="p1848213120160"></a>模板的相关描述，且长度为0～512个字符。</p>
</td>
</tr>
<tr id="row104837115166"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p13483171171614"><a name="p13483171171614"></a><a name="p13483171171614"></a>操作</p>
</td>
<td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p123372411717"><a name="p123372411717"></a><a name="p123372411717"></a><span class="uicontrol" id="uicontrol174844191611"><a name="uicontrol174844191611"></a><a name="uicontrol174844191611"></a>“创建作业”</span>：直接在该模板下创建作业，创建完后，系统跳转到<span class="menucascade" id="menucascade54848111162"><a name="menucascade54848111162"></a><a name="menucascade54848111162"></a>“<span class="uicontrol" id="uicontrol1048420181615"><a name="uicontrol1048420181615"></a><a name="uicontrol1048420181615"></a>作业管理</span>”</span>下的作业编辑页面。</p>
</td>
</tr>
</tbody>
</table>

当前已有的样例模板包括如下场景：

-   NGINX访问日志实时ETL入库
-   套牌车辆检测
-   电子围栏告警
-   车辆偏航告警
-   车辆超速告警
-   流式随机森林异常检测
-   CloudTable-DLI Flink-CloudTable
-   DIS-DLI Flink-CSS\(Elasticsearch\)
-   DIS-DLI Flink-CloudTable\(OpenTSDB\)
-   DIS-DLI Flink-CloudTable
-   DIS-DLI Flink-DCS
-   DIS-DLI Flink-DDS\(MongoDB\)
-   DIS-DLI Flink-DIS
-   DIS-DLI Flink-OBS-DWS
-   DIS-DLI Flink-SMN
-   Kafka-DLI Flink-Kafka
-   OBS-DLI Flink-RDS
-   Stream-Join-Table\(DCS\)
-   Stream-Join-Table\(RDS\)

## 自定义模板<a name="section4777152184911"></a>

自定义模板列表显示所有的自定义作业模板，自定义模板列表参数说明如[表 1](#table17778105244916)所示。

**表 2**  自定义模板列表参数

<a name="table17778105244916"></a>
<table><thead align="left"><tr id="row97781952154913"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.3.1.1"><p id="p6778195215495"><a name="p6778195215495"></a><a name="p6778195215495"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="80%" id="mcps1.2.3.1.2"><p id="p3778145244918"><a name="p3778145244918"></a><a name="p3778145244918"></a>参数说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1477895215491"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p777817528498"><a name="p777817528498"></a><a name="p777817528498"></a>名称</p>
</td>
<td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p6778452184915"><a name="p6778452184915"></a><a name="p6778452184915"></a>模板名称，只能由英文、中文、数字、中划线和下划线组成，并且长度为1～64个字符。</p>
</td>
</tr>
<tr id="row577885210496"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p20778145214918"><a name="p20778145214918"></a><a name="p20778145214918"></a>描述</p>
</td>
<td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p18778852124911"><a name="p18778852124911"></a><a name="p18778852124911"></a>模板的相关描述，且长度为0～512个字符。</p>
</td>
</tr>
<tr id="row377885219499"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p477815218498"><a name="p477815218498"></a><a name="p477815218498"></a>创建时间</p>
</td>
<td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p5778152104917"><a name="p5778152104917"></a><a name="p5778152104917"></a>创建模板的时间。</p>
</td>
</tr>
<tr id="row8778852154910"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p4778145218497"><a name="p4778145218497"></a><a name="p4778145218497"></a>更新时间</p>
</td>
<td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p1677835204916"><a name="p1677835204916"></a><a name="p1677835204916"></a>最后修改模板的时间。</p>
</td>
</tr>
<tr id="row27784522494"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p1577818528492"><a name="p1577818528492"></a><a name="p1577818528492"></a>操作</p>
</td>
<td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><a name="ul1460194517206"></a><a name="ul1460194517206"></a><ul id="ul1460194517206"><li><span class="uicontrol" id="uicontrol134593452200"><a name="uicontrol134593452200"></a><a name="uicontrol134593452200"></a>“编辑”</span>：对已经创建好的模板进行修改。</li><li><span class="uicontrol" id="uicontrol17459745102017"><a name="uicontrol17459745102017"></a><a name="uicontrol17459745102017"></a>“创建作业”</span>：直接在该模板下创建作业，创建完后，系统跳转到<span class="menucascade" id="menucascade114599453208"><a name="menucascade114599453208"></a><a name="menucascade114599453208"></a>“<span class="uicontrol" id="uicontrol1045914453200"><a name="uicontrol1045914453200"></a><a name="uicontrol1045914453200"></a>作业管理</span>”</span>下的作业编辑页面。</li><li><span class="uicontrol" id="uicontrol104601845102013"><a name="uicontrol104601845102013"></a><a name="uicontrol104601845102013"></a>“删除”</span>：将已经创建的模板删除。</li></ul>
</td>
</tr>
</tbody>
</table>

## 新建模板<a name="section5417513171115"></a>

创建作业模板，有以下四种方法。

-   进入“作业模板“页面新建模板。
    1.  在DLI管理控制台的左侧导航栏中，单击“作业模板“\>“Flink模板“。
    2.  单击页面右上角“创建模板“，弹出“创建模板“页面。
    3.  输入“名称“和“描述“。

        **图 1**  新建模板<a name="fig262345011527"></a>  
        ![](figures/新建模板.png "新建模板")

        **表 3**  模板配置信息

        <a name="table54210431747"></a>
        <table><thead align="left"><tr id="row042184317411"><th class="cellrowborder" valign="top" width="14.14%" id="mcps1.2.3.1.1"><p id="p442111432040"><a name="p442111432040"></a><a name="p442111432040"></a>参数</p>
        </th>
        <th class="cellrowborder" valign="top" width="85.86%" id="mcps1.2.3.1.2"><p id="p15421164310415"><a name="p15421164310415"></a><a name="p15421164310415"></a>参数说明</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row1421174311418"><td class="cellrowborder" valign="top" width="14.14%" headers="mcps1.2.3.1.1 "><p id="p14219435417"><a name="p14219435417"></a><a name="p14219435417"></a>名称</p>
        </td>
        <td class="cellrowborder" valign="top" width="85.86%" headers="mcps1.2.3.1.2 "><p id="p942116438414"><a name="p942116438414"></a><a name="p942116438414"></a>模板名称，只能由字母、中文、数字、中划线和下划线组成，并且长度为1～64个字符。</p>
        <div class="note" id="note96156558515"><a name="note96156558515"></a><a name="note96156558515"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p166161552517"><a name="p166161552517"></a><a name="p166161552517"></a>模板名称必须是唯一的。</p>
        </div></div>
        </td>
        </tr>
        <tr id="row154213431043"><td class="cellrowborder" valign="top" width="14.14%" headers="mcps1.2.3.1.1 "><p id="p5421104318412"><a name="p5421104318412"></a><a name="p5421104318412"></a>描述</p>
        </td>
        <td class="cellrowborder" valign="top" width="85.86%" headers="mcps1.2.3.1.2 "><p id="p04214433416"><a name="p04214433416"></a><a name="p04214433416"></a>模板的相关描述，且长度为0～512字符。</p>
        </td>
        </tr>
        </tbody>
        </table>

    4.  单击“确认“，进入“编辑“页面。

        **图 2**  编辑作业模板<a name="fig1523173015213"></a>  
        ![](figures/编辑作业模板.png "编辑作业模板")

        按照从左到右，从上到下的顺序说明如下：

        **表 4**  界面介绍

        <a name="table57746157116"></a>
        <table><thead align="left"><tr id="row97759154113"><th class="cellrowborder" valign="top" width="18.98%" id="mcps1.2.3.1.1"><p id="p1977531516120"><a name="p1977531516120"></a><a name="p1977531516120"></a>功能</p>
        </th>
        <th class="cellrowborder" valign="top" width="81.02000000000001%" id="mcps1.2.3.1.2"><p id="p1477501514119"><a name="p1477501514119"></a><a name="p1477501514119"></a>描述</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row552923111371"><td class="cellrowborder" valign="top" width="18.98%" headers="mcps1.2.3.1.1 "><p id="p1653023193715"><a name="p1653023193715"></a><a name="p1653023193715"></a>名称</p>
        </td>
        <td class="cellrowborder" valign="top" width="81.02000000000001%" headers="mcps1.2.3.1.2 "><p id="p1053014316376"><a name="p1053014316376"></a><a name="p1053014316376"></a>可以修改模板名称。</p>
        </td>
        </tr>
        <tr id="row148316183817"><td class="cellrowborder" valign="top" width="18.98%" headers="mcps1.2.3.1.1 "><p id="p1083101173811"><a name="p1083101173811"></a><a name="p1083101173811"></a>描述</p>
        </td>
        <td class="cellrowborder" valign="top" width="81.02000000000001%" headers="mcps1.2.3.1.2 "><p id="p283191123820"><a name="p283191123820"></a><a name="p283191123820"></a>可以修改模板描述。</p>
        </td>
        </tr>
        <tr id="row776216413916"><td class="cellrowborder" valign="top" width="18.98%" headers="mcps1.2.3.1.1 "><p id="p1876294103914"><a name="p1876294103914"></a><a name="p1876294103914"></a>保存方式</p>
        </td>
        <td class="cellrowborder" valign="top" width="81.02000000000001%" headers="mcps1.2.3.1.2 "><a name="ul17263191433914"></a><a name="ul17263191433914"></a><ul id="ul17263191433914"><li>修改：将修改保存至当前的模板中。</li><li>新增：将修改另存为新的模板。</li></ul>
        </td>
        </tr>
        <tr id="row11775131511117"><td class="cellrowborder" valign="top" width="18.98%" headers="mcps1.2.3.1.1 "><p id="p4776151514117"><a name="p4776151514117"></a><a name="p4776151514117"></a>SQL语句编辑区域</p>
        </td>
        <td class="cellrowborder" valign="top" width="81.02000000000001%" headers="mcps1.2.3.1.2 "><p id="p883019141171"><a name="p883019141171"></a><a name="p883019141171"></a>输入详细的SQL语句，实现业务逻辑功能。SQL语句的编写请参考<a href="https://support.huaweicloud.com/sqlreference-dli/dli_08_0219.html" target="_blank" rel="noopener noreferrer">《数据湖探索SQL语法参考》</a>。</p>
        </td>
        </tr>
        <tr id="row877691510116"><td class="cellrowborder" valign="top" width="18.98%" headers="mcps1.2.3.1.1 "><p id="p127779153118"><a name="p127779153118"></a><a name="p127779153118"></a>保存</p>
        </td>
        <td class="cellrowborder" valign="top" width="81.02000000000001%" headers="mcps1.2.3.1.2 "><p id="p277716151116"><a name="p277716151116"></a><a name="p277716151116"></a>保存修改。</p>
        </td>
        </tr>
        <tr id="row982893814405"><td class="cellrowborder" valign="top" width="18.98%" headers="mcps1.2.3.1.1 "><p id="p3828143812406"><a name="p3828143812406"></a><a name="p3828143812406"></a>创建作业</p>
        </td>
        <td class="cellrowborder" valign="top" width="81.02000000000001%" headers="mcps1.2.3.1.2 "><p id="p9828938194011"><a name="p9828938194011"></a><a name="p9828938194011"></a>使用当前模板创建作业。</p>
        </td>
        </tr>
        <tr id="row15379135241612"><td class="cellrowborder" valign="top" width="18.98%" headers="mcps1.2.3.1.1 "><p id="p1637916528169"><a name="p1637916528169"></a><a name="p1637916528169"></a>格式化</p>
        </td>
        <td class="cellrowborder" valign="top" width="81.02000000000001%" headers="mcps1.2.3.1.2 "><p id="p173809528166"><a name="p173809528166"></a><a name="p173809528166"></a>对SQL语句进行格式化，将SQL语句格式化后，需要重新编辑SQL语句。</p>
        </td>
        </tr>
        <tr id="row15591758111619"><td class="cellrowborder" valign="top" width="18.98%" headers="mcps1.2.3.1.1 "><p id="p11593583164"><a name="p11593583164"></a><a name="p11593583164"></a><a name="image7160122812416"></a><a name="image7160122812416"></a><span><img id="image7160122812416" src="figures/zh-cn_image_0238333104.png"></span></p>
        </td>
        <td class="cellrowborder" valign="top" width="81.02000000000001%" headers="mcps1.2.3.1.2 "><p id="p1459115811610"><a name="p1459115811610"></a><a name="p1459115811610"></a>更改页面风格（黑色底或白色底）。</p>
        </td>
        </tr>
        </tbody>
        </table>

    5.  在SQL语句编辑区域，输入SQL语句，实现业务逻辑功能。SQL语句的编写请参考[《数据湖探索SQL语法参考》](https://support.huaweicloud.com/sqlreference-dli/dli_08_0219.html)。
    6.  SQL编辑完成后，单击右上角的“保存“，完成创建模板。
    7.  （可选）如果不需要进行修改，也可以单击右上角的“创建作业“基于当前模板创建作业。创建作业请参考[创建Flink SQL作业](创建Flink-SQL作业.md)和[创建Flink自定义作业](创建Flink自定义作业.md)。

-   基于现有作业模板新建模板
    1.  在DLI管理控制台的左侧导航栏中，单击“作业模板“\>“Flink模板“，单击“自定义模板“页签。
    2.  在自定义模板列表中，单击所需作业模板“操作“列中的“编辑“，进入“模板编辑“页面。
    3.  修改完成后，“保存方式”选择“新增”。
    4.  单击右上角“保存“，完成另存一个新模板。


-   基于新建作业新建模板
    1.  在DLI管理控制台的左侧导航栏中，单击“作业管理“\>“Flink作业“，进入“Flink作业“页面。
    2.  单击右上角“创建作业“，弹出“创建作业“页面。
    3.  配置作业信息，输入“名称”和“描述”，选择“模板”。
    4.  单击“确认“，进入“作业编辑“页面。
    5.  SQL编辑完成后，单击“设为模板“，弹出“设为模板“窗口。
    6.  输入“名称“和“描述“，单击“确认“，完成另存一个新模板。

-   基于现有作业新建模板
    1.  在DLI管理控制台的左侧导航栏中，单击“作业管理“\>“Flink作业“，进入“Flink作业“页面。
    2.  在作业列表中，选择一个需要设置为模板的作业，在“操作“列单击“编辑“，进入“作业编辑“页面。
    3.  SQL编辑完成后，单击“设为模板“，弹出“设为模板“窗口。
    4.  输入“名称“和“描述“，单击“确认“，完成另存一个新模板。


## 基于模板新建作业<a name="section123515484542"></a>

用户可以基于样例模板或者自定义模板新建作业。

1.  在DLI管理控制台的左侧导航栏中，单击“作业模板“\>“Flink模板“。
2.  在样例模板列表中，单击对应模板“操作“列中的“创建作业“。创建作业请参考[创建Flink SQL作业](创建Flink-SQL作业.md)和[创建Flink自定义作业](创建Flink自定义作业.md)。

## 修改模板<a name="section735234815411"></a>

用户创建完自定义模板后，可以根据实际需求修改自定义模板。样例模板不支持修改，但是可以查看。

1.  在DLI管理控制台的左侧导航栏中，单击“作业模板“\>“Flink模板“，单击“自定义模板“页签。
2.  在自定义模板列表中，选择一个需要修改的模板，单击模板名称或该模板“操作“列中的“编辑“，进入“编辑“页面。
3.  在SQL语句编辑区，根据需要修改SQL语句。
4.  “保存方式”选择“修改”。
5.  单击右上角“保存“，保存当前模板修改的内容。

## 删除模板<a name="section1035264818548"></a>

用户可以根据需求删除不需要的自定义模板，不支持删除样例模板。模板删除后无法恢复，请谨慎操作。

1.  在DLI管理控制台的左侧导航栏中，单击“作业模板“\>“Flink模板“，单击“自定义模板“页签。
2.  在自定义模板列表中，勾选需要删除的模板，支持多选，单击自定义模板列表左上方的“删除“。

    用户也可以在自定义模板列表中，勾选需要删除的模板，单击“操作“栏中“删除“，删除对应的模板。

3.  在弹出的删除确认窗口中，单击“确认“。

