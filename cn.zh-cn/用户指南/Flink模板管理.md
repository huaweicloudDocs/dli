# Flink模板管理<a name="dli_01_0464"></a>

作业模板是指用户在使用SQL类型作业时，系统提供的SQL作业相关的模板。用户在实际使用SQL作业时可以在已有的模板中进行修改SQL语句，来实现实际的作业逻辑需求，可以节约用户编辑SQL语句的时间。用户也可以自定义作业模板，根据自己的习惯和方法创建作业模板，方便后续作业可以直接调用或修改。用户可以在“作业模板“页面中创建模板和管理模板。

本章内容包含如下：

-   [自定义模板列表](#section4777152184911)
-   [新建模板](#section5417513171115)
-   [基于模板新建作业](#section123515484542)
-   [查看模板详情](#section1695414016571)
-   [修改模板](#section735234815411)
-   [删除模板](#section1035264818548)

## 自定义模板列表<a name="section4777152184911"></a>

“作业模板“页面的自定义模板列表显示所有的自定义作业模板，自定义模板列表参数说明如[表 1](#table17778105244916)所示。

**表 1**  自定义模板列表参数

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
<td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><a name="ul1460194517206"></a><a name="ul1460194517206"></a><ul id="ul1460194517206"><li>单击<span class="uicontrol" id="uicontrol134593452200"><a name="uicontrol134593452200"></a><a name="uicontrol134593452200"></a>“编辑”</span>，对已经创建好的模板进行修改。</li><li>单击<span class="uicontrol" id="uicontrol17459745102017"><a name="uicontrol17459745102017"></a><a name="uicontrol17459745102017"></a>“新建作业”</span>，直接在该模板下创建作业，创建完后，系统跳转到<span class="menucascade" id="menucascade114599453208"><a name="menucascade114599453208"></a><a name="menucascade114599453208"></a>“<span class="uicontrol" id="uicontrol1045914453200"><a name="uicontrol1045914453200"></a><a name="uicontrol1045914453200"></a>作业管理</span>”</span>下的作业编辑页面。</li><li>单击<span class="uicontrol" id="uicontrol104601845102013"><a name="uicontrol104601845102013"></a><a name="uicontrol104601845102013"></a>“删除”</span>，将已经创建的模板删除。</li></ul>
</td>
</tr>
</tbody>
</table>

**表 2**  按钮说明

<a name="table12339177175420"></a>
<table><thead align="left"><tr id="row10339107195419"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.3.1.1"><p id="p43397785411"><a name="p43397785411"></a><a name="p43397785411"></a>按钮</p>
</th>
<th class="cellrowborder" valign="top" width="80%" id="mcps1.2.3.1.2"><p id="p1233919711548"><a name="p1233919711548"></a><a name="p1233919711548"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row16648164442513"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p13648194482513"><a name="p13648194482513"></a><a name="p13648194482513"></a>新建</p>
</td>
<td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p964864419256"><a name="p964864419256"></a><a name="p964864419256"></a>单击<span class="uicontrol" id="uicontrol1688981902614"><a name="uicontrol1688981902614"></a><a name="uicontrol1688981902614"></a>“新建”</span>，创建一个自定义模板。</p>
</td>
</tr>
<tr id="row15404541162512"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p1404154152510"><a name="p1404154152510"></a><a name="p1404154152510"></a>删除</p>
</td>
<td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p164041141122513"><a name="p164041141122513"></a><a name="p164041141122513"></a>单击<span class="uicontrol" id="uicontrol663414100278"><a name="uicontrol663414100278"></a><a name="uicontrol663414100278"></a>“删除”</span>，删除一个或者多个自定义模板。</p>
</td>
</tr>
<tr id="row133406755419"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p534015716544"><a name="p534015716544"></a><a name="p534015716544"></a><a name="image7847194632212"></a><a name="image7847194632212"></a><span><img id="image7847194632212" src="figures/icon-cs-query.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p20801256192218"><a name="p20801256192218"></a><a name="p20801256192218"></a>在搜索框中输入模板名称，单击<a name="image969374181816"></a><a name="image969374181816"></a><span><img id="image969374181816" src="figures/icon-cs-query.png"></span>，搜索模板。</p>
</td>
</tr>
<tr id="row934067205412"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p1834011710544"><a name="p1834011710544"></a><a name="p1834011710544"></a><a name="image16154650172317"></a><a name="image16154650172317"></a><span><img id="image16154650172317" src="figures/icon-cs-refresh.png"></span></p>
</td>
<td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p11911557172315"><a name="p11911557172315"></a><a name="p11911557172315"></a>单击<a name="image743414119197"></a><a name="image743414119197"></a><span><img id="image743414119197" src="figures/icon-cs-refresh.png"></span>，手动刷新模板列表。</p>
</td>
</tr>
</tbody>
</table>

## 新建模板<a name="section5417513171115"></a>

创建作业模板，有以下四种方法。

-   进入“作业模板“页面新建模板。
    1.  在DLI管理控制台的左侧导航栏中，单击“作业模板“\>“Flink模板“，单击“自定义模板“页签。
    2.  单击页面右上角“新建模板“，弹出“新建模板“页面。
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

        **表 4**  功能介绍

        <a name="table57746157116"></a>
        <table><thead align="left"><tr id="row97759154113"><th class="cellrowborder" valign="top" width="19.75%" id="mcps1.2.3.1.1"><p id="p1977531516120"><a name="p1977531516120"></a><a name="p1977531516120"></a>名称</p>
        </th>
        <th class="cellrowborder" valign="top" width="80.25%" id="mcps1.2.3.1.2"><p id="p1477501514119"><a name="p1477501514119"></a><a name="p1477501514119"></a>描述</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row11775131511117"><td class="cellrowborder" valign="top" width="19.75%" headers="mcps1.2.3.1.1 "><p id="p4776151514117"><a name="p4776151514117"></a><a name="p4776151514117"></a>SQL语句编辑区域</p>
        </td>
        <td class="cellrowborder" valign="top" width="80.25%" headers="mcps1.2.3.1.2 "><p id="p883019141171"><a name="p883019141171"></a><a name="p883019141171"></a>输入详细的SQL语句，实现业务逻辑功能。SQL语句的编写请参考<a href="https://support.huaweicloud.com/sqlreference-dli/dli_08_0219.html" target="_blank" rel="noopener noreferrer">《数据湖探索SQL语法参考》</a>。</p>
        </td>
        </tr>
        <tr id="row877691510116"><td class="cellrowborder" valign="top" width="19.75%" headers="mcps1.2.3.1.1 "><p id="p127779153118"><a name="p127779153118"></a><a name="p127779153118"></a>保存</p>
        </td>
        <td class="cellrowborder" valign="top" width="80.25%" headers="mcps1.2.3.1.2 "><p id="p277716151116"><a name="p277716151116"></a><a name="p277716151116"></a>保存用户编写的SQL语句。</p>
        </td>
        </tr>
        <tr id="row187777152118"><td class="cellrowborder" valign="top" width="19.75%" headers="mcps1.2.3.1.1 "><p id="p16777101517111"><a name="p16777101517111"></a><a name="p16777101517111"></a>另存为</p>
        </td>
        <td class="cellrowborder" valign="top" width="80.25%" headers="mcps1.2.3.1.2 "><p id="p2077718152112"><a name="p2077718152112"></a><a name="p2077718152112"></a>可选功能，将新建模板另存为一个作业模板。</p>
        </td>
        </tr>
        <tr id="row982893814405"><td class="cellrowborder" valign="top" width="19.75%" headers="mcps1.2.3.1.1 "><p id="p3828143812406"><a name="p3828143812406"></a><a name="p3828143812406"></a><a name="image364171114251"></a><a name="image364171114251"></a><span><img id="image364171114251" src="figures/icon-cs-update.png"></span></p>
        </td>
        <td class="cellrowborder" valign="top" width="80.25%" headers="mcps1.2.3.1.2 "><p id="p9828938194011"><a name="p9828938194011"></a><a name="p9828938194011"></a>可选功能，修改模板名称和描述。</p>
        </td>
        </tr>
        <tr id="row15379135241612"><td class="cellrowborder" valign="top" width="19.75%" headers="mcps1.2.3.1.1 "><p id="p1637916528169"><a name="p1637916528169"></a><a name="p1637916528169"></a><a name="image19816443172514"></a><a name="image19816443172514"></a><span><img id="image19816443172514" src="figures/icon-cs-sql.png"></span></p>
        </td>
        <td class="cellrowborder" valign="top" width="80.25%" headers="mcps1.2.3.1.2 "><p id="p173809528166"><a name="p173809528166"></a><a name="p173809528166"></a>可选功能，将SQL格式化，将SQL语句格式化后，需要重新编辑SQL语句。</p>
        </td>
        </tr>
        <tr id="row15591758111619"><td class="cellrowborder" valign="top" width="19.75%" headers="mcps1.2.3.1.1 "><p id="p11593583164"><a name="p11593583164"></a><a name="p11593583164"></a><a name="image1680381415265"></a><a name="image1680381415265"></a><span><img id="image1680381415265" src="figures/icon-cs-theme.png"></span></p>
        </td>
        <td class="cellrowborder" valign="top" width="80.25%" headers="mcps1.2.3.1.2 "><p id="p1459115811610"><a name="p1459115811610"></a><a name="p1459115811610"></a>可选功能，设置页面主题，可以设置字体大小，自动换行和页面风格。</p>
        </td>
        </tr>
        <tr id="row111752975113"><td class="cellrowborder" valign="top" width="19.75%" headers="mcps1.2.3.1.1 "><p id="p14119132935113"><a name="p14119132935113"></a><a name="p14119132935113"></a><a name="image4182547132719"></a><a name="image4182547132719"></a><span><img id="image4182547132719" src="figures/icon-cs-help.png"></span></p>
        </td>
        <td class="cellrowborder" valign="top" width="80.25%" headers="mcps1.2.3.1.2 "><p id="p181199292517"><a name="p181199292517"></a><a name="p181199292517"></a>可选功能，帮助中心，为用户提供产品文档，帮助用户详细了解产品含义以及使用方法。</p>
        </td>
        </tr>
        </tbody>
        </table>

    5.  SQL语句编辑区域，输入SQL语句，实现业务逻辑功能。SQL语句的编写请参考[《数据湖探索SQL语法参考》](https://support.huaweicloud.com/sqlreference-dli/dli_08_0219.html)。
    6.  SQL编辑完成后，单击“保存“。

        创建模板成功后，在自定义模板列表中会显示创建的模板。用户可以直接单击模板“操作“列的“新建作业“基于模板创建作业。新建作业请参考[创建Flink SQL作业](创建Flink-SQL作业.md)。


-   基于现有作业模板新建模板
    1.  在DLI管理控制台的左侧导航栏中，单击“作业模板“\>“Flink模板“，单击“自定义模板“页签。
    2.  在自定义模板列表中，选中一个作业模板，单击“操作“列中的“编辑“，进入“模板编辑“页面。
    3.  单击“另存为“，弹出“模板另存为“窗口。
    4.  输入“名称“和“描述“，单击“确认“，完成另存一个新模板。


-   基于新建作业新建模板
    1.  在DLI管理控制台的左侧导航栏中，单击“作业管理“\>“Flink作业“，进入“Flink作业“页面。
    2.  单击右上角“新建作业“，弹出“新建作业“页面。
    3.  配置作业信息，输入“名称”和“描述”，选择“模板”。
    4.  单击“确认“，进入“作业编辑“页面。
    5.  SQL编辑完成后，单击“设为模板“，弹出“设为模板“窗口。
    6.  输入“名称“和“描述“，单击“确认“，完成另存一个新模板。

-   基于现有作业新建模板
    1.  在DLI管理控制台的左侧导航栏中，单击“作业管理“\>“Flink作业“，进入“Flink作业“页面。
    2.  在作业列表中，选择一个需要设置为模板的作业，在“操作“列单击“编辑“，进入“作业编辑“页面。
    3.  单击右上角“更多“\>“设为模板“，弹出“设为模板“窗口。
    4.  输入“名称“和“描述“，单击“确认“，完成将作业设置为模板的操作。


## 基于模板新建作业<a name="section123515484542"></a>

用户可以基于样例模板或者自定义模板新建作业。

1.  在DLI管理控制台的左侧导航栏中，单击“作业模板“\>“Flink模板“。
2.  在样例模板列表中，单击对应模板“操作“列中的“新建作业“。具体操作步骤请参见[创建Flink SQL作业](创建Flink-SQL作业.md)。

    **图 3**  基于模板新建作业<a name="fig1761143817119"></a>  
    ![](figures/基于模板新建作业.png "基于模板新建作业")


## 查看模板详情<a name="section1695414016571"></a>

1.  在DLI管理控制台的左侧导航栏中，单击“作业模板“\>“Flink模板“。
2.  在样例模板列表或者自定义模板列表的“名称“一列中，单击需要查看的模板名称，进入“模板信息“页面。

    显示当前模板的描述和SQL语句等信息。

3.  （可选）当查看自定义模板时，单击右上方的“编辑“，进入“编辑“页面，可对模板进行修改。

## 修改模板<a name="section735234815411"></a>

用户创建完自定义模板后，可以根据实际需求修改自定义模板，样例模板不支持修改。

1.  在DLI管理控制台的左侧导航栏中，单击“作业模板“\>“Flink模板“，单击“自定义模板“页签。
2.  在自定义模板列表中，选择一个需要修改的模板，单击“操作“列中的“编辑“，进入“编辑“页面。
3.  在SQL语句编辑区，根据需要修改SQL语句。
4.  （可选）单击![](figures/icon-cs-update.png)修改模板的名称和描述。
5.  单击“保存“，保存修改的内容。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >用户也可以通过“模板信息“页面进入“编辑“页面。具体操作如下：  
    >1.  在自定义模板列表中，选中一个需要修改的模板，在“名称“列单击对应的作业模板名称，进入“模板信息“页面。  
    >2.  单击“编辑“，进入“编辑“页面。  


## 删除模板<a name="section1035264818548"></a>

用户可以根据需求删除不需要的自定义模板，样例模板不支持删除。模板删除后无法恢复，请谨慎操作。

1.  在DLI管理控制台的左侧导航栏中，单击“作业模板“\>“Flink模板“，单击“自定义模板“页签。
2.  在自定义模板列表中，勾选需要删除的模板，支持多选，单击自定义模板列表左上方的“删除“。

    用户也可以在自定义模板列表中，勾选需要删除的模板，单击“操作“栏中“删除“，删除对应的模板。

3.  在弹出的删除确认窗口中，单击“确认“。

