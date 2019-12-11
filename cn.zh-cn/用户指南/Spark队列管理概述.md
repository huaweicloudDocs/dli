# Spark队列管理概述<a name="dli_01_0411"></a>

DLI用户可在全托管Spark队列上进行数据分析。

Spark队列管理主要包括如下功能：

-   [创建队列](Spark创建队列.md)
-   [删除队列](删除队列-0.md)
-   [分配至项目](分配至项目-1.md)
-   [修改队列网段](修改队列网段-2.md)
-   [创建消息通知主题](创建消息通知主题.md)

## 队列管理页面<a name="section1616314111518"></a>

队列管理页面显示用户创建所有的队列，您可以查看队列名称、队列容量、状态、所有者、创建时间等信息。队列列表默认按创建时间排列，创建时间最近的队列显示在最前端。

**表 1**  队列管理参数

<a name="table3950169215120"></a>
<table><thead align="left"><tr id="row2555468715120"><th class="cellrowborder" valign="top" width="19.35%" id="mcps1.2.3.1.1"><p id="p4021197415120"><a name="p4021197415120"></a><a name="p4021197415120"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="80.65%" id="mcps1.2.3.1.2"><p id="p3594448915120"><a name="p3594448915120"></a><a name="p3594448915120"></a>参数说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row166602455180"><td class="cellrowborder" valign="top" width="19.35%" headers="mcps1.2.3.1.1 "><p id="p566264517181"><a name="p566264517181"></a><a name="p566264517181"></a>名称</p>
</td>
<td class="cellrowborder" valign="top" width="80.65%" headers="mcps1.2.3.1.2 "><p id="p1366294513188"><a name="p1366294513188"></a><a name="p1366294513188"></a>创建的队列名称。</p>
</td>
</tr>
<tr id="row46758327132"><td class="cellrowborder" valign="top" width="19.35%" headers="mcps1.2.3.1.1 "><p id="p16413434141957"><a name="p16413434141957"></a><a name="p16413434141957"></a>队列规格</p>
</td>
<td class="cellrowborder" valign="top" width="80.65%" headers="mcps1.2.3.1.2 "><p id="p1066329135619"><a name="p1066329135619"></a><a name="p1066329135619"></a>创建的队列大小，单位：CU。</p>
<p id="p54419740141957"><a name="p54419740141957"></a><a name="p54419740141957"></a>CU是队列的计价单位。 1CU= 4Core 16GMem。不同规格的队列对应的计算能力不一样，规格越高计算能力越好。</p>
</td>
</tr>
<tr id="row16482169194812"><td class="cellrowborder" valign="top" width="19.35%" headers="mcps1.2.3.1.1 "><p id="p164838915484"><a name="p164838915484"></a><a name="p164838915484"></a>计费方式</p>
</td>
<td class="cellrowborder" valign="top" width="80.65%" headers="mcps1.2.3.1.2 "><a name="ul19201142341011"></a><a name="ul19201142341011"></a><ul id="ul19201142341011"><li>按需/CU时：按CU时计费。</li><li>包年包月：<a name="ul422427141014"></a><a name="ul422427141014"></a><ul id="ul422427141014"><li>包年</li><li>包月</li></ul>
</li></ul>
</td>
</tr>
<tr id="row32873162171713"><td class="cellrowborder" valign="top" width="19.35%" headers="mcps1.2.3.1.1 "><p id="p45480448171713"><a name="p45480448171713"></a><a name="p45480448171713"></a>状态</p>
</td>
<td class="cellrowborder" valign="top" width="80.65%" headers="mcps1.2.3.1.2 "><p id="p54281846202213"><a name="p54281846202213"></a><a name="p54281846202213"></a>所创建的队列状态。包括：</p>
<a name="ul169018539319"></a><a name="ul169018539319"></a><ul id="ul169018539319"><li>已成功（AVAILABLE）</li><li>已冻结（SUSPENDED）</li></ul>
</td>
</tr>
<tr id="row31011923151038"><td class="cellrowborder" valign="top" width="19.35%" headers="mcps1.2.3.1.1 "><p id="p10671857151038"><a name="p10671857151038"></a><a name="p10671857151038"></a>所有者</p>
</td>
<td class="cellrowborder" valign="top" width="80.65%" headers="mcps1.2.3.1.2 "><p id="p89431923510"><a name="p89431923510"></a><a name="p89431923510"></a>队列的所有者。</p>
</td>
</tr>
<tr id="row36301606171658"><td class="cellrowborder" valign="top" width="19.35%" headers="mcps1.2.3.1.1 "><p id="p14394959151048"><a name="p14394959151048"></a><a name="p14394959151048"></a>创建时间</p>
</td>
<td class="cellrowborder" valign="top" width="80.65%" headers="mcps1.2.3.1.2 "><p id="p51238775151048"><a name="p51238775151048"></a><a name="p51238775151048"></a>创建队列的时间。</p>
</td>
</tr>
<tr id="row6424839516213"><td class="cellrowborder" valign="top" width="19.35%" headers="mcps1.2.3.1.1 "><p id="p50569641162134"><a name="p50569641162134"></a><a name="p50569641162134"></a>描述</p>
</td>
<td class="cellrowborder" valign="top" width="80.65%" headers="mcps1.2.3.1.2 "><p id="p18910361162145"><a name="p18910361162145"></a><a name="p18910361162145"></a>创建队列时，对队列的描述。如果无描述，则显示“--”。</p>
</td>
</tr>
<tr id="row911162819515"><td class="cellrowborder" valign="top" width="19.35%" headers="mcps1.2.3.1.1 "><p id="p11111132814519"><a name="p11111132814519"></a><a name="p11111132814519"></a>所属项目</p>
</td>
<td class="cellrowborder" valign="top" width="80.65%" headers="mcps1.2.3.1.2 "><p id="p197403611524"><a name="p197403611524"></a><a name="p197403611524"></a>显示所建队列所属的企业项目。如果不属于企业项目，则显示“--”。</p>
<p id="p101111128145113"><a name="p101111128145113"></a><a name="p101111128145113"></a>企业项目是一种云资源管理方式，企业项目管理服务提供统一的云资源按项目管理，以及项目内的资源管理、成员管理。关于如何设置企业项目请参考《<a href="https://support.huaweicloud.com/usermanual-em/zh-cn_topic_0108763975.html" target="_blank" rel="noopener noreferrer">企业管理用户指南</a>》。</p>
<div class="note" id="note1358194815815"><a name="note1358194815815"></a><a name="note1358194815815"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p16581348175819"><a name="p16581348175819"></a><a name="p16581348175819"></a>只有开通了企业管理服务的用户才显示该参数。</p>
</div></div>
</td>
</tr>
<tr id="row1662880815250"><td class="cellrowborder" valign="top" width="19.35%" headers="mcps1.2.3.1.1 "><p id="p475621615250"><a name="p475621615250"></a><a name="p475621615250"></a>操作</p>
</td>
<td class="cellrowborder" valign="top" width="80.65%" headers="mcps1.2.3.1.2 "><a name="ul15800707615"></a><a name="ul15800707615"></a><ul id="ul15800707615"><li>删除：删除所选队列。<div class="note" id="note117011010355"><a name="note117011010355"></a><a name="note117011010355"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p77161015357"><a name="p77161015357"></a><a name="p77161015357"></a>删除队列后无法恢复，请谨慎操作。</p>
</div></div>
</li><li>激活：激活已冻结的队列。</li><li>分配至项目：修改所选队列所属的企业项目。<div class="note" id="note98048571133"><a name="note98048571133"></a><a name="note98048571133"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p19804657131310"><a name="p19804657131310"></a><a name="p19804657131310"></a>只有开通了企业管理服务的用户才显示该参数。</p>
</div></div>
</li><li>修改网段：建议使用网段：10.0.0.0/8~26，172.16.0.0/12~26，192.168.0.0/16~26。</li><li>续费/退订：根据需要选择续费或者退订。<div class="note" id="note85628275377"><a name="note85628275377"></a><a name="note85628275377"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1556352753715"><a name="p1556352753715"></a><a name="p1556352753715"></a>只有包年包月计费有“续费/退订”操作。</p>
</div></div>
</li></ul>
</td>
</tr>
</tbody>
</table>

