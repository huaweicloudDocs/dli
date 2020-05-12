# SQL作业管理<a name="dli_01_0017"></a>

SQL作业包括在SQL作业编辑器窗口执行SQL语句，导入数据和导出数据等操作。

SQL作业管理主要包括如下功能：

-   [查找作业](#section71552447166)
-   [查看作业详情](#section1960402414173)
-   [终止作业](#section8647175812179)
-   [导出结果](#section1152211221244)

以及查看“使用指南”和“使用视频”。

## 作业管理页面<a name="section1616314111518"></a>

在总览页面单击“SQL作业”简介，或在左侧导航栏单击“作业管理”\>“SQL作业”，可进入SQL作业管理页面。SQL作业管理页面显示所有SQL作业，作业数量较多时，系统分页显示，可根据需要跳转至指定页面。您可以查看任何状态下的作业。作业列表默认按创建时间降序排列，创建时间最近的作业显示在最前端。

**表 1**  作业管理参数

<a name="table3950169215120"></a>
<table><thead align="left"><tr id="row2555468715120"><th class="cellrowborder" valign="top" width="21.18%" id="mcps1.2.3.1.1"><p id="p4021197415120"><a name="p4021197415120"></a><a name="p4021197415120"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="78.82000000000001%" id="mcps1.2.3.1.2"><p id="p3594448915120"><a name="p3594448915120"></a><a name="p3594448915120"></a>参数说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row42211426202515"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p132212262258"><a name="p132212262258"></a><a name="p132212262258"></a>队列名称</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p16221102632515"><a name="p16221102632515"></a><a name="p16221102632515"></a>作业所属队列的名称。</p>
</td>
</tr>
<tr id="row46758327132"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p16413434141957"><a name="p16413434141957"></a><a name="p16413434141957"></a>创建时间</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p54419740141957"><a name="p54419740141957"></a><a name="p54419740141957"></a>每个作业的创建时间，可按创建时间顺序或倒序显示作业列表。</p>
</td>
</tr>
<tr id="row32873162171713"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p45480448171713"><a name="p45480448171713"></a><a name="p45480448171713"></a>作业类型</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p60037708171713"><a name="p60037708171713"></a><a name="p60037708171713"></a>作业的类型，包括如下。</p>
<a name="ul29348869174358"></a><a name="ul29348869174358"></a><ul id="ul29348869174358"><li>IMPORT：导入数据到DLI的作业。</li><li>EXPORT：从DLI导出数据的作业。</li><li>DCL：包括传统DCL，以及队列权限相关的操作。</li><li>DDL：与传统DDL操作一致，即创建和删除数据库，创建和删除表的作业。</li><li>QUERY：执行SQL查询数据的作业。</li><li>INSERT：执行SQL插入数据的作业。</li><li>UPDATE：更新数据。</li><li>DELETE：删除SQL作业。</li><li>DATA_MIGRATION：数据迁移。</li><li>RESTART_QUEUE：重启队列。</li></ul>
</td>
</tr>
<tr id="row31011923151038"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p10671857151038"><a name="p10671857151038"></a><a name="p10671857151038"></a>状态</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p59114099151038"><a name="p59114099151038"></a><a name="p59114099151038"></a>作业的状态信息，包括如下。</p>
<a name="ul32930526154023"></a><a name="ul32930526154023"></a><ul id="ul32930526154023"><li>提交中</li><li>运行中</li><li>已取消</li><li>已成功</li><li>已失败</li></ul>
</td>
</tr>
<tr id="row36301606171658"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p14394959151048"><a name="p14394959151048"></a><a name="p14394959151048"></a>执行语句</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p51238775151048"><a name="p51238775151048"></a><a name="p51238775151048"></a>作业的具体SQL语句以及导出、建表的操作，此处展示操作的描述。</p>
<p id="p1938144453219"><a name="p1938144453219"></a><a name="p1938144453219"></a>单击<a name="image14502620163211"></a><a name="image14502620163211"></a><span><img id="image14502620163211" src="figures/icon-复制.png"></span>可复制对应的语句。</p>
</td>
</tr>
<tr id="row6424839516213"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p50569641162134"><a name="p50569641162134"></a><a name="p50569641162134"></a>运行时长</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p18910361162145"><a name="p18910361162145"></a><a name="p18910361162145"></a>作业的运行时长。</p>
</td>
</tr>
<tr id="row1662880815250"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p475621615250"><a name="p475621615250"></a><a name="p475621615250"></a>操作</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><a name="ul181927155164"></a><a name="ul181927155164"></a><ul id="ul181927155164"><li>终止。<a name="ul968854181713"></a><a name="ul968854181713"></a><ul id="ul968854181713"><li>当作业状态在<span class="parmname" id="parmname1819151571614"><a name="parmname1819151571614"></a><a name="parmname1819151571614"></a>“提交中”</span>和<span class="parmname" id="parmname17191181517165"><a name="parmname17191181517165"></a><a name="parmname17191181517165"></a>“运行中”</span>时，<span class="uicontrol" id="uicontrol1319121521618"><a name="uicontrol1319121521618"></a><a name="uicontrol1319121521618"></a>“终止”</span>按钮才生效。</li><li>当作业状态为<span class="parmvalue" id="parmvalue101910157167"><a name="parmvalue101910157167"></a><a name="parmvalue101910157167"></a>“已成功”</span>、<span class="parmvalue" id="parmvalue19191131541612"><a name="parmvalue19191131541612"></a><a name="parmvalue19191131541612"></a>“已失败”</span>、<span class="parmvalue" id="parmvalue5191515141610"><a name="parmvalue5191515141610"></a><a name="parmvalue5191515141610"></a>“已取消”</span>的作业不能终止。</li><li>当<span class="uicontrol" id="uicontrol1319291521614"><a name="uicontrol1319291521614"></a><a name="uicontrol1319291521614"></a>“终止”</span>按钮为灰色时，表示无法执行终止操作。</li></ul>
</li></ul>
<a name="ul1875134719182"></a><a name="ul1875134719182"></a><ul id="ul1875134719182"><li>SparkUI：单击后，将跳转至Spark任务运行情况界面。</li><li>QUERY作业和异步DDL作业除上述操作外，还包括：<a name="ul14392109145620"></a><a name="ul14392109145620"></a><ul id="ul14392109145620"><li>下载到本地<div class="note" id="note9951439175515"><a name="note9951439175515"></a><a name="note9951439175515"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p29975685513"><a name="p29975685513"></a><a name="p29975685513"></a>异步DDL和QUERY语句支持将结果下载到本地。操作如下：</p>
<p id="p159623945518"><a name="p159623945518"></a><a name="p159623945518"></a>单击执行成功的异步DDL或QUERY语句“操作”列中的“下载到本地”，在提示窗口单击“确认”。此时，“操作”列中的“下载到本地”将变为“立即下载”。单击“立即下载”将对应结果下载到本地</p>
</div></div>
</li><li>更多：查看结果、导出结果、导出日志</li></ul>
</li><li>EXPORT作业除上述操作外，还包括：<a name="ul5161951101019"></a><a name="ul5161951101019"></a><ul id="ul5161951101019"><li>立即下载</li></ul>
</li></ul>
</td>
</tr>
</tbody>
</table>

## 查找作业<a name="section71552447166"></a>

在“SQL作业“页面，可以通过以下方式对作业进行过滤筛选，在页面中显示符合对应条件的作业。

-   选择队列名称
-   设置日期范围
-   输入执行语句/作业ID
-   选择创建时间顺序/倒序排列
-   选择作业类型
-   选择作业状态
-   选择运行时长顺序/倒序排列

## 查看作业详情<a name="section1960402414173"></a>

在“SQL作业“页面，选中一条作业，单击该作业对应的![](figures/icon-展开.png)，可查看该条作业的详细信息。

不同类型的作业，显示的作业详情不同。以导入数据作业，建表作业和查询作业为例说明。

-   导入数据（load data）作业（作业类型：IMPORT），包括以下信息：队列名称，作业ID，创建时间，作业类型，作业状态，执行语句，运行时长，已扫描数据，执行用户，结果条数，扫描数据条数，错误记录条数，数据库名称，表名，文件格式，表头，引用字符，分隔符，数据源路径，转义字符，导入开始时间，导入结束时间，日期格式，时间戳格式。
-   建表（create table）作业（作业类型：DDL），包括以下信息：队列名称，作业ID，创建时间，作业类型，作业状态，执行语句，运行时长，已扫描数据，执行用户。
-   查询（select）作业（作业类型：QUERY），包括以下信息：队列名称，作业ID，创建时间，作业类型，作业状态，执行语句，运行时长，结果条数（运行成功，可导出结果），已扫描数据，执行用户，结果状态（运行成功，可查看结果；运行失败，显示失败原因）。

## 终止作业<a name="section8647175812179"></a>

在“SQL作业“页面，可单击“操作”列的“终止“，终止“提交中”或“运行中”的作业。

## 导出结果<a name="section1152211221244"></a>

导出结果的操作入口有两个，分别在“SQL作业“和“SQL编辑器“页面。

-   在“作业管理”\>“SQL作业“页面，可单击对应作业“操作”列“更多”中的“导出结果“，可导出执行查询后的结果。
-   在“SQL编辑器“页面，查询语句执行成功后，在“查看结果“页签右侧，单击“导出结果”，可导出执行查询后的结果。

>![](public_sys-resources/icon-note.gif) **说明：**   
>若执行结果中无数值列，则无法导出结果。  

**图 1**  导出结果<a name="fig914972320541"></a>  
![](figures/导出结果.png "导出结果")

**表 2**  参数说明

<a name="table7742063143659"></a>
<table><thead align="left"><tr id="row48986708143659"><th class="cellrowborder" valign="top" width="13.8%" id="mcps1.2.3.1.1"><p id="p8500389143659"><a name="p8500389143659"></a><a name="p8500389143659"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="86.2%" id="mcps1.2.3.1.2"><p id="p17442940143659"><a name="p17442940143659"></a><a name="p17442940143659"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row55162434145333"><td class="cellrowborder" valign="top" width="13.8%" headers="mcps1.2.3.1.1 "><p id="p21307823145337"><a name="p21307823145337"></a><a name="p21307823145337"></a>数据源格式</p>
</td>
<td class="cellrowborder" valign="top" width="86.2%" headers="mcps1.2.3.1.2 "><p id="p48212085145337"><a name="p48212085145337"></a><a name="p48212085145337"></a>导出数据的文件格式。当前只支持csv格式。</p>
</td>
</tr>
<tr id="row33984858114535"><td class="cellrowborder" valign="top" width="13.8%" headers="mcps1.2.3.1.1 "><p id="p1310090114535"><a name="p1310090114535"></a><a name="p1310090114535"></a>队列</p>
</td>
<td class="cellrowborder" valign="top" width="86.2%" headers="mcps1.2.3.1.2 "><p id="p39008475114535"><a name="p39008475114535"></a><a name="p39008475114535"></a>选择队列。</p>
</td>
</tr>
<tr id="row1774342414552"><td class="cellrowborder" valign="top" width="13.8%" headers="mcps1.2.3.1.1 "><p id="p2547309214552"><a name="p2547309214552"></a><a name="p2547309214552"></a>压缩格式</p>
</td>
<td class="cellrowborder" valign="top" width="86.2%" headers="mcps1.2.3.1.2 "><p id="p5005459614552"><a name="p5005459614552"></a><a name="p5005459614552"></a>导出数据的压缩方式，选择如下压缩方式。</p>
<a name="ul35000658144913"></a><a name="ul35000658144913"></a><ul id="ul35000658144913"><li>none</li><li>bzip2</li><li>deflate</li><li>gzip</li></ul>
</td>
</tr>
<tr id="row6367025143659"><td class="cellrowborder" valign="top" width="13.8%" headers="mcps1.2.3.1.1 "><p id="p3346061614541"><a name="p3346061614541"></a><a name="p3346061614541"></a>存储路径</p>
</td>
<td class="cellrowborder" valign="top" width="86.2%" headers="mcps1.2.3.1.2 "><p id="p595910502214"><a name="p595910502214"></a><a name="p595910502214"></a>输入或选择OBS的路径。路径须以<span class="parmname" id="parmname64912034172226"><a name="parmname64912034172226"></a><a name="parmname64912034172226"></a>“s3a://”</span>开头。</p>
<div class="note" id="note248113592220"><a name="note248113592220"></a><a name="note248113592220"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul2932240315"></a><a name="ul2932240315"></a><ul id="ul2932240315"><li>选择OBS桶后，请在文本框中定义文件夹名称，若该文件夹不存在，则会在OBS中创建。</li><li>文件夹名称不能包含下列特殊字符：\ / : * ? " &lt; &gt; |，并且不能以“.”开头和结尾。</li></ul>
</div></div>
</td>
</tr>
<tr id="row48430784114641"><td class="cellrowborder" valign="top" width="13.8%" headers="mcps1.2.3.1.1 "><p id="p30579455114641"><a name="p30579455114641"></a><a name="p30579455114641"></a>导出方式</p>
</td>
<td class="cellrowborder" valign="top" width="86.2%" headers="mcps1.2.3.1.2 "><p id="p61016786114641"><a name="p61016786114641"></a><a name="p61016786114641"></a>导出数据的保存方式。</p>
<a name="ul625034191496"></a><a name="ul625034191496"></a><ul id="ul625034191496"><li>随导出创建指定路径：指定的导出目录必须不存在，如果指定目录已经存在，系统将返回错误信息，无法执行导出操作。</li><li>覆盖指定路径：在指定目录下新建文件，会删除已有文件。</li></ul>
</td>
</tr>
<tr id="row1218154413337"><td class="cellrowborder" valign="top" width="13.8%" headers="mcps1.2.3.1.1 "><p id="p44720296144515"><a name="p44720296144515"></a><a name="p44720296144515"></a>高级选项</p>
</td>
<td class="cellrowborder" valign="top" width="86.2%" headers="mcps1.2.3.1.2 "><p id="p3371134919382"><a name="p3371134919382"></a><a name="p3371134919382"></a>表头：无/有</p>
<p id="p1066994820411"><a name="p1066994820411"></a><a name="p1066994820411"></a>设置导出数据是否含表头。当<span class="parmname" id="parmname45661651135412"><a name="parmname45661651135412"></a><a name="parmname45661651135412"></a>“导出格式”</span>为<span class="parmvalue" id="parmvalue75661651195411"><a name="parmvalue75661651195411"></a><a name="parmvalue75661651195411"></a>“csv”</span>时该参数有效。当前只支持csv格式。</p>
<p id="p1262888185911"><a name="p1262888185911"></a><a name="p1262888185911"></a>选中<span class="parmname" id="parmname15361161464715"><a name="parmname15361161464715"></a><a name="parmname15361161464715"></a>“高级选项”</span>，勾选<span class="parmname" id="parmname1353042144718"><a name="parmname1353042144718"></a><a name="parmname1353042144718"></a>“表头:无”</span>前的方框，<span class="parmname" id="parmname063982314814"><a name="parmname063982314814"></a><a name="parmname063982314814"></a>“表头:无”</span>显示为<span class="parmname" id="parmname1790112818475"><a name="parmname1790112818475"></a><a name="parmname1790112818475"></a>“表头:有”</span>，表示有表头；去勾选即为<span class="parmname" id="parmname171354719481"><a name="parmname171354719481"></a><a name="parmname171354719481"></a>“表头:无”</span>，表示无表头。</p>
</td>
</tr>
</tbody>
</table>

