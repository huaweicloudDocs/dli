# Flink作业概述<a name="dli_01_0403"></a>

## 操作场景<a name="zh-cn_topic_0093946892_section31579140143928"></a>

在Flink作业管理页面可提交Flink作业。目前有以下作业类型：

-   Flink SQL作业：使用SQL语句定义作业，可以提交到任意队列上。
-   Flink SQL边缘作业（公测）：通过SQL对边缘设备数据进行分析，可部署到边缘节点上。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >开通Flink SQL边缘作业公测后可见。  

-   Flink自定义作业：基于Flink API的自定义Jar包作业，可以运行在独享队列上。

Flink作业管理主要包括如下功能：

-   [创建Flink SQL作业](创建Flink-SQL作业.md)
-   [创建Flink SQL边缘作业](创建Flink-SQL边缘作业.md)
-   [创建Flink自定义作业](创建Flink自定义作业.md)
-   [调试作业](调试作业.md)
-   [可视化编辑器](可视化编辑器.md)
-   [Sink可视化](Sink可视化.md)
-   [编辑作业](操作作业.md#section1950210297542)
-   [启动作业](操作作业.md#section20957159163012)
-   [停止作业](操作作业.md#section8678193324114)
-   [删除作业](操作作业.md#section1691624195713)
-   [名称和描述修改](操作作业.md#section15861321183619)
-   [作业详情](作业详情.md)

## 作业管理页面<a name="section12526165519235"></a>

作业管理页面显示所有的Flink作业，作业数量较多时，系统分页显示，您可以查看任何状态下的作业。

**表 1**  作业管理参数

<a name="zh-cn_topic_0122090417_table3950169215120"></a>
<table><thead align="left"><tr id="zh-cn_topic_0122090417_row2555468715120"><th class="cellrowborder" valign="top" width="16.07%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0122090417_p4021197415120"><a name="zh-cn_topic_0122090417_p4021197415120"></a><a name="zh-cn_topic_0122090417_p4021197415120"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="83.93%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0122090417_p3594448915120"><a name="zh-cn_topic_0122090417_p3594448915120"></a><a name="zh-cn_topic_0122090417_p3594448915120"></a>参数说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0122090417_row46758327132"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p16413434141957"><a name="zh-cn_topic_0122090417_p16413434141957"></a><a name="zh-cn_topic_0122090417_p16413434141957"></a>作业ID</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0122090417_p54419740141957"><a name="zh-cn_topic_0122090417_p54419740141957"></a><a name="zh-cn_topic_0122090417_p54419740141957"></a>所提交Flink作业的ID，由系统默认生成。</p>
</td>
</tr>
<tr id="zh-cn_topic_0122090417_row32873162171713"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p45480448171713"><a name="zh-cn_topic_0122090417_p45480448171713"></a><a name="zh-cn_topic_0122090417_p45480448171713"></a>作业名称</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0122090417_p18579134217227"><a name="zh-cn_topic_0122090417_p18579134217227"></a><a name="zh-cn_topic_0122090417_p18579134217227"></a>所提交Flink作业的名称。</p>
</td>
</tr>
<tr id="row3289513151315"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="p102901113161318"><a name="p102901113161318"></a><a name="p102901113161318"></a>作业类型</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><p id="p1029001315135"><a name="p1029001315135"></a><a name="p1029001315135"></a>所提交Flink作业的类型。包括：</p>
<a name="ul864114454138"></a><a name="ul864114454138"></a><ul id="ul864114454138"><li>Flink SQL作业</li><li>Flink SQL边缘作业</li><li>Flink自定义作业</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0122090417_row31011923151038"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p10671857151038"><a name="zh-cn_topic_0122090417_p10671857151038"></a><a name="zh-cn_topic_0122090417_p10671857151038"></a>作业状态</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0122090417_p59114099151038"><a name="zh-cn_topic_0122090417_p59114099151038"></a><a name="zh-cn_topic_0122090417_p59114099151038"></a>作业的状态信息，包括：</p>
<a name="zh-cn_topic_0122090417_ul32930526154023"></a><a name="zh-cn_topic_0122090417_ul32930526154023"></a><ul id="zh-cn_topic_0122090417_ul32930526154023"><li>草稿</li><li>运行中</li><li>空闲</li><li>已完成</li><li>已停止</li><li>提交中</li><li>提交失败</li><li>运行异常</li><li>停止中</li><li>停止失败</li><li>因欠费被停止</li><li>欠费作业恢复中</li><li>保存点创建中</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0122090417_row36301606171658"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p14394959151048"><a name="zh-cn_topic_0122090417_p14394959151048"></a><a name="zh-cn_topic_0122090417_p14394959151048"></a>描述</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0122090417_p51238775151048"><a name="zh-cn_topic_0122090417_p51238775151048"></a><a name="zh-cn_topic_0122090417_p51238775151048"></a>所提交Flink作业的描述。</p>
</td>
</tr>
<tr id="row4736911141810"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="p1973721141811"><a name="p1973721141811"></a><a name="p1973721141811"></a>用户名</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><p id="p373781161815"><a name="p373781161815"></a><a name="p373781161815"></a>提交作业的用户名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0122090417_row6424839516213"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p50569641162134"><a name="zh-cn_topic_0122090417_p50569641162134"></a><a name="zh-cn_topic_0122090417_p50569641162134"></a>创建时间</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0122090417_p18910361162145"><a name="zh-cn_topic_0122090417_p18910361162145"></a><a name="zh-cn_topic_0122090417_p18910361162145"></a>每个作业的创建时间，可按创建时间顺序或倒序显示作业列表。</p>
</td>
</tr>
<tr id="row15840729143612"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="p13841152911367"><a name="p13841152911367"></a><a name="p13841152911367"></a>开始时间</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><p id="p20841122983612"><a name="p20841122983612"></a><a name="p20841122983612"></a>Flink作业开始运行的时间。</p>
</td>
</tr>
<tr id="row1536633125019"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="p145363334505"><a name="p145363334505"></a><a name="p145363334505"></a>运行时长</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><p id="p153603315013"><a name="p153603315013"></a><a name="p153603315013"></a>作业运行所消耗的时间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0122090417_row1662880815250"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p475621615250"><a name="zh-cn_topic_0122090417_p475621615250"></a><a name="zh-cn_topic_0122090417_p475621615250"></a>操作</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><a name="zh-cn_topic_0122090417_ul181927155164"></a><a name="zh-cn_topic_0122090417_ul181927155164"></a><ul id="zh-cn_topic_0122090417_ul181927155164"><li>编辑：编辑已经创建好的作业。具体请参见<a href="操作作业.md#section1950210297542">编辑作业</a>。</li><li>启动：启动作业并运行。具体请参见<a href="操作作业.md#section20957159163012">启动作业</a>。</li><li>停止：停止“提交中”或“运行中”的作业。</li><li>删除：删除作业。<div class="note" id="note386711433506"><a name="note386711433506"></a><a name="note386711433506"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p16867104316506"><a name="p16867104316506"></a><a name="p16867104316506"></a>作业删除后不可恢复，请谨慎操作。</p>
</div></div>
</li><li>Sink可视化：将Sink流中的数字类型的数据以图表方式实时展示。<div class="note" id="note1372459391"><a name="note1372459391"></a><a name="note1372459391"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1748114516397"><a name="p1748114516397"></a><a name="p1748114516397"></a>只有“运行中”的Flink SQL作业并可查看Sink可视化信息。</p>
</div></div>
</li><li>名称和描述修改：修改作业名称和描述。</li></ul>
</td>
</tr>
</tbody>
</table>

