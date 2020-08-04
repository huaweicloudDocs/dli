# Flink作业管理概述<a name="dli_01_0403"></a>

在Flink作业管理页面可提交Flink作业。目前有以下作业类型：

-   Flink SQL作业：使用SQL语句定义作业，可以提交到任意队列上。
-   Flink自定义作业：基于Flink API的自定义Jar包作业，可以运行在独享队列上。
-   Flink SQL边缘作业（公测）：通过SQL对边缘设备数据进行分析，可部署到边缘节点上。

Flink作业管理主要包括如下功能：

-   [Flink作业权限管理](Flink作业权限管理.md)
-   [创建Flink SQL作业](创建Flink-SQL作业.md)
-   [创建Flink自定义作业](创建Flink自定义作业.md)
-   [创建Flink SQL边缘作业](创建Flink-SQL边缘作业.md)
-   [调试作业](调试作业.md)
-   [编辑作业](操作作业.md#section1950210297542)
-   [启动作业](操作作业.md#section20957159163012)
-   [停止作业](操作作业.md#section8678193324114)
-   [删除作业](操作作业.md#section1691624195713)
-   [导出作业](操作作业.md#section135831511323)
-   [导入作业](操作作业.md#section75781665389)
-   [名称和描述修改](操作作业.md#section15861321183619)
-   [导入保存点](操作作业.md#section83412445175)
-   [触发保存点](操作作业.md#section11401152191015)
-   [作业详情](作业详情.md)

以及查看“使用指南”和“使用视频”。

## 委托权限设置<a name="section12518143518488"></a>

DLI执行Flink作业需要进行委托授权，可在第一次登录管理控制台时进行设置，也可在“全局配置”\>“[服务授权](服务授权.md)”中进行修改。

具体权限如下：

-   Tenant Administrator\(全局服务\)：DLI Flink作业访问和使用OBS或者DWS数据源、日志转储（包括桶授权）、开启checkpoint、作业导入导出等，需要获得访问和使用OBS（对象存储服务）的Tenant Administrator权限。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >由于云服务缓存需要时间，该权限60分钟左右才能生效。

-   DIS Administrator：DLI Flink作业访问和使用DIS数据源，需要获得访问和使用DIS（数据接入服务）的DIS Administrator权限。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >由于云服务缓存需要时间，该权限30分钟左右才能生效。

-   CloudTable Administrator：DLI Flink作业访问和使用CloudTable数据源，需要获得访问和使用CloudTable（表格存储服务）的CloudTable Administrator限。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >由于云服务缓存需要时间，该权限3分钟左右才能生效。

-   Tenant Administrator\(项目级\)：DLI 边缘Flink作业执行需要使用IEF（智能边缘平台）服务，IEF服务必须具有Tenant Administrator权限才能运行。使用其他必须具有Tenant Administrator权限才能运行的服务也需要获得该权限。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >由于云服务缓存需要时间，该权限3分钟左右才能生效。


## 作业管理页面<a name="section12526165519235"></a>

在总览页面单击“Flink作业”简介，或在左侧导航栏单击“作业管理”\>“Flink作业”，可进入Flink作业管理页面。Flink作业管理页面显示所有的Flink作业，作业数量较多时，系统分页显示，您可以查看任何状态下的作业。

**表 1**  作业管理参数

<a name="zh-cn_topic_0122090417_table3950169215120"></a>
<table><thead align="left"><tr id="zh-cn_topic_0122090417_row2555468715120"><th class="cellrowborder" valign="top" width="16.07%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0122090417_p4021197415120"><a name="zh-cn_topic_0122090417_p4021197415120"></a><a name="zh-cn_topic_0122090417_p4021197415120"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="83.93%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0122090417_p3594448915120"><a name="zh-cn_topic_0122090417_p3594448915120"></a><a name="zh-cn_topic_0122090417_p3594448915120"></a>参数说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0122090417_row46758327132"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p16413434141957"><a name="zh-cn_topic_0122090417_p16413434141957"></a><a name="zh-cn_topic_0122090417_p16413434141957"></a>ID</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0122090417_p54419740141957"><a name="zh-cn_topic_0122090417_p54419740141957"></a><a name="zh-cn_topic_0122090417_p54419740141957"></a>所提交Flink作业的ID，由系统默认生成。</p>
</td>
</tr>
<tr id="zh-cn_topic_0122090417_row32873162171713"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p45480448171713"><a name="zh-cn_topic_0122090417_p45480448171713"></a><a name="zh-cn_topic_0122090417_p45480448171713"></a>名称</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0122090417_p18579134217227"><a name="zh-cn_topic_0122090417_p18579134217227"></a><a name="zh-cn_topic_0122090417_p18579134217227"></a>所提交Flink作业的名称。</p>
</td>
</tr>
<tr id="row3289513151315"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="p102901113161318"><a name="p102901113161318"></a><a name="p102901113161318"></a>类型</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><p id="p1029001315135"><a name="p1029001315135"></a><a name="p1029001315135"></a>所提交Flink作业的类型。包括：</p>
<a name="ul864114454138"></a><a name="ul864114454138"></a><ul id="ul864114454138"><li>Flink SQL：Flink SQL作业</li><li>Flink Jar：Flink自定义作业</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0122090417_row31011923151038"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p10671857151038"><a name="zh-cn_topic_0122090417_p10671857151038"></a><a name="zh-cn_topic_0122090417_p10671857151038"></a>状态</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0122090417_p59114099151038"><a name="zh-cn_topic_0122090417_p59114099151038"></a><a name="zh-cn_topic_0122090417_p59114099151038"></a>作业的状态信息，包括：</p>
<a name="zh-cn_topic_0122090417_ul32930526154023"></a><a name="zh-cn_topic_0122090417_ul32930526154023"></a><ul id="zh-cn_topic_0122090417_ul32930526154023"><li>草稿</li><li>提交中</li><li>提交失败</li><li>运行中（开始计费，提交作业后，返回正常结果）</li><li>运行异常（停止计费。作业发生运行时异常，停止运行作业）</li><li>停止中</li><li>已停止</li><li>停止失败</li><li>保存点创建中</li><li>因欠费被停止（结束计费。用户账户欠费，作业停止）</li><li>欠费作业恢复中（用户账户欠费，账户充值，作业恢复中）</li><li>已完成</li></ul>
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
<tr id="row154491330202418"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="p144501930192415"><a name="p144501930192415"></a><a name="p144501930192415"></a>企业项目</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><p id="p101111128145113"><a name="p101111128145113"></a><a name="p101111128145113"></a>企业项目是一种云资源管理方式，企业项目管理服务提供统一的云资源按项目管理，以及项目内的资源管理、成员管理。关于如何设置企业项目请参考《<a href="https://support.huaweicloud.com/usermanual-em/zh-cn_topic_0108763975.html" target="_blank" rel="noopener noreferrer">企业管理用户指南</a>》。</p>
<div class="note" id="note1358194815815"><a name="note1358194815815"></a><a name="note1358194815815"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p16581348175819"><a name="p16581348175819"></a><a name="p16581348175819"></a>只有开通了企业管理服务的用户才显示该参数。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0122090417_row1662880815250"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p475621615250"><a name="zh-cn_topic_0122090417_p475621615250"></a><a name="zh-cn_topic_0122090417_p475621615250"></a>操作</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><a name="zh-cn_topic_0122090417_ul181927155164"></a><a name="zh-cn_topic_0122090417_ul181927155164"></a><ul id="zh-cn_topic_0122090417_ul181927155164"><li>编辑：编辑已经创建好的作业。具体请参见<a href="操作作业.md#section1950210297542">编辑作业</a>。</li><li>启动：启动作业并运行。具体请参见<a href="操作作业.md#section20957159163012">启动作业</a>。</li><li>更多<a name="ul2162826144010"></a><a name="ul2162826144010"></a><ul id="ul2162826144010"><li>FlinkUI：单击后，将跳转至Flink任务运行情况界面。</li><li>停止：停止“提交中”或“运行中”的作业。</li><li>删除：删除作业。<div class="note" id="note386711433506"><a name="note386711433506"></a><a name="note386711433506"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p16867104316506"><a name="p16867104316506"></a><a name="p16867104316506"></a>作业删除后不可恢复，请谨慎操作。</p>
</div></div>
</li><li>名称和描述修改：修改作业名称和描述。</li><li>导入保存点：导入原实时流计算服务作业导出的数据。</li><li>触发保存点：“运行中”的作业可以“触发保存点”，保存作业的状态信息。</li><li>权限管理：查看作业对应的用户权限信息以及对其他用户授权。</li></ul>
</li></ul>
</td>
</tr>
</tbody>
</table>

