# SQL模板管理<a name="dli_01_0021"></a>

为了便捷快速的执行SQL操作，DLI支持定制模板或将正在使用的SQL语句保存为模板。保存模板后，不需编写SQL语句，可通过模板直接执行SQL操作。

SQL模板包括样例模板和自定义模板。当前系统默认的样例模板包括22条标准的TPC-H查询语句，可以满足用户大部分的TPC-H需求场景测试。

SQL模板管理主要包括如下功能：

-   [样例模板](#section1039614583412)
-   [自定义模板](#section1616314111518)
-   [创建模板](#section73391334165211)
-   [执行模板](#section1936164995213)
-   [查找模板](#section1045610354536)
-   [修改模板](#section08698165316)
-   [删除模板](#section1317681345320)

## 表格设置<a name="section18354320771"></a>

在“SQL模板”页面右上角，单击“设置”可以选择是否按照分组展示模板。

![](figures/12-1SQL模板管理-zh.png)

如果选择“按分组展示”，有以下三种展示方式：

-   展开第一个分组
-   全部展开
-   全部收起

**图 1**  SQL模板显示设置<a name="fig8560194210405"></a>  
![](figures/SQL模板显示设置.png "SQL模板显示设置")

## 样例模板<a name="section1039614583412"></a>

当前样例模板包括22条标准的TPC-H查询语句，您可以查看模板名称、描述、语句等信息。

**表 1**  模板管理参数

<a name="table10396104513419"></a>
<table><thead align="left"><tr id="row1139794519348"><th class="cellrowborder" valign="top" width="8.959999999999999%" id="mcps1.2.3.1.1"><p id="p43973456348"><a name="p43973456348"></a><a name="p43973456348"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="91.03999999999999%" id="mcps1.2.3.1.2"><p id="p1239715459348"><a name="p1239715459348"></a><a name="p1239715459348"></a>参数说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1239717456343"><td class="cellrowborder" valign="top" width="8.959999999999999%" headers="mcps1.2.3.1.1 "><p id="p16397114513343"><a name="p16397114513343"></a><a name="p16397114513343"></a>名称</p>
</td>
<td class="cellrowborder" valign="top" width="91.03999999999999%" headers="mcps1.2.3.1.2 "><p id="p33975457349"><a name="p33975457349"></a><a name="p33975457349"></a>模板名称。</p>
<a name="ul1397745133416"></a><a name="ul1397745133416"></a><ul id="ul1397745133416"><li>模板名称只能包含数字、英文字母和下划线，但不能是纯数字，不能以下划线开头，且不能为空。</li><li>输入长度不能超过50个字符。</li></ul>
</td>
</tr>
<tr id="row18397124533419"><td class="cellrowborder" valign="top" width="8.959999999999999%" headers="mcps1.2.3.1.1 "><p id="p2397345193412"><a name="p2397345193412"></a><a name="p2397345193412"></a>描述</p>
</td>
<td class="cellrowborder" valign="top" width="91.03999999999999%" headers="mcps1.2.3.1.2 "><p id="p1939744514347"><a name="p1939744514347"></a><a name="p1939744514347"></a>所创建模板的相应描述。</p>
</td>
</tr>
<tr id="row1397194519342"><td class="cellrowborder" valign="top" width="8.959999999999999%" headers="mcps1.2.3.1.1 "><p id="p3397144517343"><a name="p3397144517343"></a><a name="p3397144517343"></a>语句</p>
</td>
<td class="cellrowborder" valign="top" width="91.03999999999999%" headers="mcps1.2.3.1.2 "><p id="p1939764510348"><a name="p1939764510348"></a><a name="p1939764510348"></a>创建为模板的SQL语句。</p>
</td>
</tr>
<tr id="row3398104553417"><td class="cellrowborder" valign="top" width="8.959999999999999%" headers="mcps1.2.3.1.1 "><p id="p8398345163416"><a name="p8398345163416"></a><a name="p8398345163416"></a>操作</p>
</td>
<td class="cellrowborder" valign="top" width="91.03999999999999%" headers="mcps1.2.3.1.2 "><p id="p186751516144318"><a name="p186751516144318"></a><a name="p186751516144318"></a>执行：单击“执行”将跳转至SQL编辑器页面，可根据需要进行修改或直接执行操作。具体请参考<a href="#section1936164995213">执行模板</a>。</p>
</td>
</tr>
</tbody>
</table>

当前已有的样例模板包括如下场景：

-   价格摘要报告查询
-   最小代价供应商分析
-   运送优先级分析
-   订单优先级检查分析
-   当地供应商数量分析
-   预测收入变化分析
-   货运量分析
-   国家市场份额分析
-   产品类型利润估量分析
-   返修零件分析
-   重要库存标志分析
-   货运模式和命令优先分析
-   消费者分配分析
-   促销效果分析
-   最高贡献供应商分析
-   零件/供应商关系分析
-   小批量订单收入分析
-   大订单顾客分析
-   折扣收入分析
-   潜在零件改进分析
-   不能按时交货供应商分析
-   全球销售机会分析

## 自定义模板<a name="section1616314111518"></a>

自定义模板页面显示用户创建的所有模板，您可以查看模板名称、描述、语句等信息。

**表 2**  模板管理参数

<a name="table3950169215120"></a>
<table><thead align="left"><tr id="row2555468715120"><th class="cellrowborder" valign="top" width="8.959999999999999%" id="mcps1.2.3.1.1"><p id="p4021197415120"><a name="p4021197415120"></a><a name="p4021197415120"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="91.03999999999999%" id="mcps1.2.3.1.2"><p id="p3594448915120"><a name="p3594448915120"></a><a name="p3594448915120"></a>参数说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row46758327132"><td class="cellrowborder" valign="top" width="8.959999999999999%" headers="mcps1.2.3.1.1 "><p id="p16413434141957"><a name="p16413434141957"></a><a name="p16413434141957"></a>名称</p>
</td>
<td class="cellrowborder" valign="top" width="91.03999999999999%" headers="mcps1.2.3.1.2 "><p id="p3967018201720"><a name="p3967018201720"></a><a name="p3967018201720"></a>模板名称。</p>
<a name="ul109681518191720"></a><a name="ul109681518191720"></a><ul id="ul109681518191720"><li>模板名称只能包含数字、英文字母和下划线，但不能是纯数字，不能以下划线开头，且不能为空。</li><li>输入长度不能超过50个字符。</li></ul>
</td>
</tr>
<tr id="row32873162171713"><td class="cellrowborder" valign="top" width="8.959999999999999%" headers="mcps1.2.3.1.1 "><p id="p207117291176"><a name="p207117291176"></a><a name="p207117291176"></a>描述</p>
</td>
<td class="cellrowborder" valign="top" width="91.03999999999999%" headers="mcps1.2.3.1.2 "><p id="p9714102981715"><a name="p9714102981715"></a><a name="p9714102981715"></a>所创建模板的相应描述。</p>
</td>
</tr>
<tr id="row31011923151038"><td class="cellrowborder" valign="top" width="8.959999999999999%" headers="mcps1.2.3.1.1 "><p id="p10671857151038"><a name="p10671857151038"></a><a name="p10671857151038"></a>语句</p>
</td>
<td class="cellrowborder" valign="top" width="91.03999999999999%" headers="mcps1.2.3.1.2 "><p id="p89431923510"><a name="p89431923510"></a><a name="p89431923510"></a>创建为模板的SQL语句。</p>
</td>
</tr>
<tr id="row1662880815250"><td class="cellrowborder" valign="top" width="8.959999999999999%" headers="mcps1.2.3.1.1 "><p id="p475621615250"><a name="p475621615250"></a><a name="p475621615250"></a>操作</p>
</td>
<td class="cellrowborder" valign="top" width="91.03999999999999%" headers="mcps1.2.3.1.2 "><a name="ul15800707615"></a><a name="ul15800707615"></a><ul id="ul15800707615"><li>执行：单击“执行”将跳转至SQL编辑器页面，可根据需要进行修改或直接执行操作。具体请参考<a href="#section1936164995213">执行模板</a>。</li><li>修改：单击“修改”可在弹出的<span class="wintitle" id="wintitle1112873217225"><a name="wintitle1112873217225"></a><a name="wintitle1112873217225"></a>“修改模板”</span>对话框中，根据需要修改模板的信息。具体请参考<a href="#section08698165316">修改模板</a>。</li></ul>
</td>
</tr>
</tbody>
</table>

## 创建模板<a name="section73391334165211"></a>

创建模板的操作入口有两个，分别在“作业模板“和“SQL编辑器“页面。

-   在“作业模板“页面创建模板。
    1.  在管理控制台左侧，单击“作业模板“\>“SQL模板“。
    2.  在“SQL模板“页面，单击右上角“创建模板”。

        输入模板名称、语句和描述信息，详细参数介绍请参见[表3](#table8760202135313)。

        **图 2**  创建模板<a name="fig375913217530"></a>  
        ![](figures/创建模板.png "创建模板")

        **表 3**  参数说明

        <a name="table8760202135313"></a>
        <table><thead align="left"><tr id="row1175916216534"><th class="cellrowborder" valign="top" width="10.83%" id="mcps1.2.3.1.1"><p id="p11759202116537"><a name="p11759202116537"></a><a name="p11759202116537"></a>参数名称</p>
        </th>
        <th class="cellrowborder" valign="top" width="89.17%" id="mcps1.2.3.1.2"><p id="p1575912112538"><a name="p1575912112538"></a><a name="p1575912112538"></a>描述</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row1776092113537"><td class="cellrowborder" valign="top" width="10.83%" headers="mcps1.2.3.1.1 "><p id="p14760132114535"><a name="p14760132114535"></a><a name="p14760132114535"></a>名称</p>
        </td>
        <td class="cellrowborder" valign="top" width="89.17%" headers="mcps1.2.3.1.2 "><p id="p14760162111532"><a name="p14760162111532"></a><a name="p14760162111532"></a>模板名称。</p>
        <a name="ul176014214537"></a><a name="ul176014214537"></a><ul id="ul176014214537"><li>模板名称只能包含数字、英文字母和下划线，但不能是纯数字，不能以下划线开头，且不能为空。</li><li>输入长度不能超过50个字符。</li></ul>
        </td>
        </tr>
        <tr id="row1921112512330"><td class="cellrowborder" valign="top" width="10.83%" headers="mcps1.2.3.1.1 "><p id="p721117573312"><a name="p721117573312"></a><a name="p721117573312"></a>语句</p>
        </td>
        <td class="cellrowborder" valign="top" width="89.17%" headers="mcps1.2.3.1.2 "><p id="p162121450334"><a name="p162121450334"></a><a name="p162121450334"></a>需要保存为模板的SQL语句。</p>
        </td>
        </tr>
        <tr id="row8760122115310"><td class="cellrowborder" valign="top" width="10.83%" headers="mcps1.2.3.1.1 "><p id="p6760162175317"><a name="p6760162175317"></a><a name="p6760162175317"></a>描述</p>
        </td>
        <td class="cellrowborder" valign="top" width="89.17%" headers="mcps1.2.3.1.2 "><p id="p13760102118531"><a name="p13760102118531"></a><a name="p13760102118531"></a>该模板的相应描述。</p>
        </td>
        </tr>
        <tr id="row18481020155119"><td class="cellrowborder" valign="top" width="10.83%" headers="mcps1.2.3.1.1 "><p id="p684972045112"><a name="p684972045112"></a><a name="p684972045112"></a>分组设置</p>
        </td>
        <td class="cellrowborder" valign="top" width="89.17%" headers="mcps1.2.3.1.2 "><a name="ul187917655212"></a><a name="ul187917655212"></a><ul id="ul187917655212"><li>已有分组</li><li>创建新分组</li><li>不分组</li></ul>
        </td>
        </tr>
        <tr id="row1084922017517"><td class="cellrowborder" valign="top" width="10.83%" headers="mcps1.2.3.1.1 "><p id="p1184952015113"><a name="p1184952015113"></a><a name="p1184952015113"></a>分组名称</p>
        </td>
        <td class="cellrowborder" valign="top" width="89.17%" headers="mcps1.2.3.1.2 "><p id="p15849720175114"><a name="p15849720175114"></a><a name="p15849720175114"></a><span class="parmname" id="parmname69501567522"><a name="parmname69501567522"></a><a name="parmname69501567522"></a>“分组设置”</span>选择“已有分组”或者“创建新分组”时，需要填写分组名称。</p>
        </td>
        </tr>
        </tbody>
        </table>

    3.  单击“确定“，完成模板创建。

-   在“SQL编辑器“页面创建模板。
    1.  在管理控制台左侧，单击“SQL编辑器“。
    2.  单击SQL作业编辑窗口右上方的“更多”，选择“设为模板”，可将编辑窗口中的SQL语句设置为模板。

        输入模板名称、语句和描述信息，详细介绍请参见[表3](#table8760202135313)。

    3.  单击“确定“，完成模板创建。


## 执行模板<a name="section1936164995213"></a>

执行模板的操作入口有两个，分别在“作业模板“和“SQL编辑器“页面。

-   通过“作业模板“页面执行模板。
    1.  在管理控制台左侧，单击“作业模板“\>“SQL模板“。
    2.  在“SQL模板“页面，勾选相应的模板，单击“操作“列的“执行“，将跳转至“SQL编辑器“页面，并在SQL作业编辑窗口中自动输入对应的SQL语句。
    3.  在SQL作业编辑窗口右上方，单击“执行”运行SQL语句，执行结束后，可以在SQL作业编辑窗口下方区域中查看执行结果。

-   通过“SQL编辑器“页面执行模板。
    1.  在管理控制台左侧，单击“SQL编辑器“。
    2.  单击SQL作业编辑窗口右上方的“更多”，选择“选择模板“。
    3.  在选择模板对话框中单击对应的SQL语句模板，其将自动输入SQL作业编辑窗口。
    4.  单击“执行”运行SQL语句，执行结束后，可以在SQL作业编辑窗口下方区域中查看执行结果。


## 查找模板<a name="section1045610354536"></a>

在“SQL模板“页面，可在右上方搜索框中输入模板名称关键字，查找与之匹配的模板。

## 修改模板<a name="section08698165316"></a>

1.  在“SQL模板“页面，选中需修改的模板，单击“操作“列的“修改“。
2.  在弹出的“修改模板“对话框中，根据需要修改模板的名称、语句和描述。
3.  单击“确定“，保存修改结果。

## 删除模板<a name="section1317681345320"></a>

在“SQL模板“页面，勾选一个或多个待删除的模板，单击“删除”，可删除选中的模板。

