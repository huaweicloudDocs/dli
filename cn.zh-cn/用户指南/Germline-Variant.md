# Germline Variant<a name="dli_01_0393"></a>

## Germline Variant页面说明<a name="section8244204903017"></a>

DLI全托管式的DNA测序流程, 基于GATK4.0标准测序流程进行分布式优化, 性能相对于单机版测序流程提升10倍有余。目前支持人类样本的WGS\(全基因组测序\)和WES\(外显子测序\)流程。

**图 1**  Germline Variant<a name="fig48381724346"></a>  
![](figures/Germline-Variant.png "Germline-Variant")

Germline Variant页面显示所有的基因作业，作业数量较多时，系统分页显示，您可以查看所有历史提交的作业。作业列表默认按创建时间排列，可选择升序或降序排列；也可以选择时间范围，查看特定时间范围内提交的作业。

**表 1**  作业列表参数

<a name="table3950169215120"></a>
<table><thead align="left"><tr id="row2555468715120"><th class="cellrowborder" valign="top" width="21.18%" id="mcps1.2.3.1.1"><p id="p4021197415120"><a name="p4021197415120"></a><a name="p4021197415120"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="78.82000000000001%" id="mcps1.2.3.1.2"><p id="p3594448915120"><a name="p3594448915120"></a><a name="p3594448915120"></a>参数说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row46758327132"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p16413434141957"><a name="p16413434141957"></a><a name="p16413434141957"></a>创建时间</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p54419740141957"><a name="p54419740141957"></a><a name="p54419740141957"></a>每个作业的创建时间，目前按创建时间倒序显示作业列表。</p>
</td>
</tr>
<tr id="row32873162171713"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p45480448171713"><a name="p45480448171713"></a><a name="p45480448171713"></a>文件类型</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p11135145010402"><a name="p11135145010402"></a><a name="p11135145010402"></a>有FASTQ和BAM两种类型的输入文件。</p>
</td>
</tr>
<tr id="row31011923151038"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p10671857151038"><a name="p10671857151038"></a><a name="p10671857151038"></a>作业状态</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p59114099151038"><a name="p59114099151038"></a><a name="p59114099151038"></a>作业的状态信息，包括如下六种状态。</p>
<a name="ul32930526154023"></a><a name="ul32930526154023"></a><ul id="ul32930526154023"><li>提交（launching）</li><li>运行中（running）</li><li>完成（finished）</li><li>失败（failed）</li><li>取消（cancelled）</li><li>取消中（canceling）</li></ul>
</td>
</tr>
<tr id="row36301606171658"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p14394959151048"><a name="p14394959151048"></a><a name="p14394959151048"></a>作业ID</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p51238775151048"><a name="p51238775151048"></a><a name="p51238775151048"></a>所提交基因作业的ID，由系统默认生成的唯一标识。</p>
</td>
</tr>
<tr id="row2019117553311"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p11193756334"><a name="p11193756334"></a><a name="p11193756334"></a>用户名</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p21939516333"><a name="p21939516333"></a><a name="p21939516333"></a>提交基因作业的用户名称。</p>
</td>
</tr>
<tr id="row6424839516213"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p50569641162134"><a name="p50569641162134"></a><a name="p50569641162134"></a>运行时长</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p18910361162145"><a name="p18910361162145"></a><a name="p18910361162145"></a>作业运行的时间长度。</p>
</td>
</tr>
<tr id="row1662880815250"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p475621615250"><a name="p475621615250"></a><a name="p475621615250"></a>进度</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p1356922117439"><a name="p1356922117439"></a><a name="p1356922117439"></a>作业运行的进度， 例如：1/3表示总共有三个步骤，当前执行到第一步。</p>
</td>
</tr>
<tr id="row83661120381"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p1368191218383"><a name="p1368191218383"></a><a name="p1368191218383"></a>操作</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p636820125386"><a name="p636820125386"></a><a name="p636820125386"></a>终止作业。</p>
<div class="note" id="note64975375514"><a name="note64975375514"></a><a name="note64975375514"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="p149712345511"><a name="p149712345511"></a><a name="p149712345511"></a>只能终止“提交中”或“运行中”的作业。</p>
</div></div>
</td>
</tr>
</tbody>
</table>

## 创建作业<a name="section1235315355212"></a>

在[图1](#fig48381724346)中，单击![](figures/zh-cn_image_0133412546.png)，进入[图2](#fig5850193418534)页面。

**图 2**  创建Germline Variant作业<a name="fig5850193418534"></a>  
![](figures/创建Germline-Variant作业.png "创建Germline-Variant作业")

参见[表2](#table34159998103738)输入相关参数。

**表 2**  参数说明

<a name="table34159998103738"></a>
<table><thead align="left"><tr id="row18398987103738"><th class="cellrowborder" valign="top" width="13.25%" id="mcps1.2.4.1.1"><p id="p13922998103738"><a name="p13922998103738"></a><a name="p13922998103738"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="79.63%" id="mcps1.2.4.1.2"><p id="p54021066103738"><a name="p54021066103738"></a><a name="p54021066103738"></a>描述</p>
</th>
<th class="cellrowborder" valign="top" width="7.12%" id="mcps1.2.4.1.3"><p id="p13630189103738"><a name="p13630189103738"></a><a name="p13630189103738"></a>示例</p>
</th>
</tr>
</thead>
<tbody><tr id="row40392508173520"><td class="cellrowborder" valign="top" width="13.25%" headers="mcps1.2.4.1.1 "><p id="p66792880173521"><a name="p66792880173521"></a><a name="p66792880173521"></a>文件类型</p>
</td>
<td class="cellrowborder" valign="top" width="79.63%" headers="mcps1.2.4.1.2 "><p id="p41514219173521"><a name="p41514219173521"></a><a name="p41514219173521"></a>FASTQ和BAM类型的输入文件。</p>
</td>
<td class="cellrowborder" valign="top" width="7.12%" headers="mcps1.2.4.1.3 "><p id="p7208591173521"><a name="p7208591173521"></a><a name="p7208591173521"></a>FASTQ</p>
</td>
</tr>
<tr id="row21981226113610"><td class="cellrowborder" valign="top" width="13.25%" headers="mcps1.2.4.1.1 "><p id="p2198226113611"><a name="p2198226113611"></a><a name="p2198226113611"></a>执行引擎</p>
</td>
<td class="cellrowborder" valign="top" width="79.63%" headers="mcps1.2.4.1.2 "><p id="p1819822643614"><a name="p1819822643614"></a><a name="p1819822643614"></a>选择BAM类型的输入文件时，需要选择对应的执行引擎，如下所示：</p>
<a name="ul12896193018372"></a><a name="ul12896193018372"></a><ul id="ul12896193018372"><li>GATK：标准GATK流程</li><li>Tensorflow：利用深度学习模型进行变异检测</li></ul>
</td>
<td class="cellrowborder" valign="top" width="7.12%" headers="mcps1.2.4.1.3 "><p id="p1199122603620"><a name="p1199122603620"></a><a name="p1199122603620"></a>GATK</p>
</td>
</tr>
<tr id="row16142559103738"><td class="cellrowborder" valign="top" width="13.25%" headers="mcps1.2.4.1.1 "><p id="p32478935103738"><a name="p32478935103738"></a><a name="p32478935103738"></a>输入路径</p>
</td>
<td class="cellrowborder" valign="top" width="79.63%" headers="mcps1.2.4.1.2 "><p id="p7250915246"><a name="p7250915246"></a><a name="p7250915246"></a>输入文件所在的OBS路径。</p>
<a name="ul196801533248"></a><a name="ul196801533248"></a><ul id="ul196801533248"><li>当输入文件类型为FASTQ时，需要指定两个OBS上的FASTQ文件路径。</li><li>当输入文件类型为BAM时，需要指定一个OBS上的BAM文件路径。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="7.12%" headers="mcps1.2.4.1.3 "><p id="p354811491243"><a name="p354811491243"></a><a name="p354811491243"></a>-</p>
</td>
</tr>
<tr id="row092512615107"><td class="cellrowborder" valign="top" width="13.25%" headers="mcps1.2.4.1.1 "><p id="p2926526141019"><a name="p2926526141019"></a><a name="p2926526141019"></a>输出GVCF</p>
</td>
<td class="cellrowborder" valign="top" width="79.63%" headers="mcps1.2.4.1.2 "><p id="p192682631012"><a name="p192682631012"></a><a name="p192682631012"></a>选择是否输出GVCF格式文件。</p>
</td>
<td class="cellrowborder" valign="top" width="7.12%" headers="mcps1.2.4.1.3 "><p id="p9926152614105"><a name="p9926152614105"></a><a name="p9926152614105"></a>-</p>
</td>
</tr>
<tr id="row37659849105931"><td class="cellrowborder" valign="top" width="13.25%" headers="mcps1.2.4.1.1 "><p id="p30548909105931"><a name="p30548909105931"></a><a name="p30548909105931"></a>输出路径</p>
</td>
<td class="cellrowborder" valign="top" width="79.63%" headers="mcps1.2.4.1.2 "><p id="p58542558105931"><a name="p58542558105931"></a><a name="p58542558105931"></a>基因检测结果的OBS输出路径。</p>
</td>
<td class="cellrowborder" valign="top" width="7.12%" headers="mcps1.2.4.1.3 "><p id="p45477491748"><a name="p45477491748"></a><a name="p45477491748"></a>-</p>
</td>
</tr>
<tr id="row16943758105944"><td class="cellrowborder" valign="top" width="13.25%" headers="mcps1.2.4.1.1 "><p id="p30267119105944"><a name="p30267119105944"></a><a name="p30267119105944"></a>参考基因</p>
</td>
<td class="cellrowborder" valign="top" width="79.63%" headers="mcps1.2.4.1.2 "><p id="p127371727548"><a name="p127371727548"></a><a name="p127371727548"></a>基因行业内标准的基因库，目前支持hg19和hg38。</p>
</td>
<td class="cellrowborder" valign="top" width="7.12%" headers="mcps1.2.4.1.3 "><p id="p1354613491044"><a name="p1354613491044"></a><a name="p1354613491044"></a>hg38</p>
</td>
</tr>
<tr id="row8664577112415"><td class="cellrowborder" valign="top" width="13.25%" headers="mcps1.2.4.1.1 "><p id="p30742160112415"><a name="p30742160112415"></a><a name="p30742160112415"></a>已知变异基因集</p>
</td>
<td class="cellrowborder" valign="top" width="79.63%" headers="mcps1.2.4.1.2 "><p id="p7087027112415"><a name="p7087027112415"></a><a name="p7087027112415"></a>根据给定的下拉框，选择需要进行比对的已知变异基因集合，可以多选。</p>
</td>
<td class="cellrowborder" valign="top" width="7.12%" headers="mcps1.2.4.1.3 "><p id="p16543249247"><a name="p16543249247"></a><a name="p16543249247"></a>-</p>
</td>
</tr>
<tr id="row208095231057"><td class="cellrowborder" valign="top" width="13.25%" headers="mcps1.2.4.1.1 "><p id="p12809623556"><a name="p12809623556"></a><a name="p12809623556"></a>BQSR文件导出</p>
</td>
<td class="cellrowborder" valign="top" width="79.63%" headers="mcps1.2.4.1.2 "><p id="p16809923756"><a name="p16809923756"></a><a name="p16809923756"></a>比对文件导出。基因检测过程中间会生成BAM类型的文件，用户可以选择将这个BAM文件保存至OBS，以供日后使用。</p>
</td>
<td class="cellrowborder" valign="top" width="7.12%" headers="mcps1.2.4.1.3 "><p id="p28108231257"><a name="p28108231257"></a><a name="p28108231257"></a>-</p>
</td>
</tr>
<tr id="row562270711021"><td class="cellrowborder" valign="top" width="13.25%" headers="mcps1.2.4.1.1 "><p id="p5278609511021"><a name="p5278609511021"></a><a name="p5278609511021"></a>高级选项</p>
</td>
<td class="cellrowborder" valign="top" width="79.63%" headers="mcps1.2.4.1.2 "><p id="p193211543162817"><a name="p193211543162817"></a><a name="p193211543162817"></a>打开高级选项，可在基因变异检测过程中，进行参数设置，参数格式为“key value”。具体描述请参考<a href="#dli_01_0393__table31006304347">表3</a>。</p>
</td>
<td class="cellrowborder" valign="top" width="7.12%" headers="mcps1.2.4.1.3 "><p id="p25421649942"><a name="p25421649942"></a><a name="p25421649942"></a>-</p>
</td>
</tr>
</tbody>
</table>

**表 3**  高级选项参数说明

<a name="table31006304347"></a>
<table><thead align="left"><tr id="row2101113013417"><th class="cellrowborder" valign="top" width="19.491949194919492%" id="mcps1.2.4.1.1"><p id="p110113003410"><a name="p110113003410"></a><a name="p110113003410"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="47.17471747174717%" id="mcps1.2.4.1.2"><p id="p151012301343"><a name="p151012301343"></a><a name="p151012301343"></a>描述</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p410183053420"><a name="p410183053420"></a><a name="p410183053420"></a>示例</p>
</th>
</tr>
</thead>
<tbody><tr id="row1610310305348"><td class="cellrowborder" valign="top" width="19.491949194919492%" headers="mcps1.2.4.1.1 "><p id="p7103113011348"><a name="p7103113011348"></a><a name="p7103113011348"></a>FastqToSam</p>
</td>
<td class="cellrowborder" valign="top" width="47.17471747174717%" headers="mcps1.2.4.1.2 "><p id="p8477142817362"><a name="p8477142817362"></a><a name="p8477142817362"></a>执行FastqToSam方法时业务相关的配置项，用户可手动添加。</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p1210317305341"><a name="p1210317305341"></a><a name="p1210317305341"></a>-</p>
</td>
</tr>
<tr id="row1310303033416"><td class="cellrowborder" valign="top" width="19.491949194919492%" headers="mcps1.2.4.1.1 "><p id="p161031630183410"><a name="p161031630183410"></a><a name="p161031630183410"></a>BwaSpark</p>
</td>
<td class="cellrowborder" valign="top" width="47.17471747174717%" headers="mcps1.2.4.1.2 "><p id="p379142518238"><a name="p379142518238"></a><a name="p379142518238"></a>执行GATK BwaSpark方法时业务相关的配置项，用户可手动添加。</p>
<div class="note" id="note36541013204911"><a name="note36541013204911"></a><a name="note36541013204911"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="p9654101319492"><a name="p9654101319492"></a><a name="p9654101319492"></a>暂不支持关于输出文件格式以及输入输出路径相关的配置项。</p>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p710315301341"><a name="p710315301341"></a><a name="p710315301341"></a>-</p>
</td>
</tr>
<tr id="row510353093412"><td class="cellrowborder" valign="top" width="19.491949194919492%" headers="mcps1.2.4.1.1 "><p id="p16103730203418"><a name="p16103730203418"></a><a name="p16103730203418"></a>ReadsPipelineSpark</p>
</td>
<td class="cellrowborder" valign="top" width="47.17471747174717%" headers="mcps1.2.4.1.2 "><p id="p667810411184"><a name="p667810411184"></a><a name="p667810411184"></a>执行GATK ReadsPipelineSpark方法时业务相关的配置项，用户可手动添加。</p>
<div class="note" id="note154013330499"><a name="note154013330499"></a><a name="note154013330499"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="p840103315498"><a name="p840103315498"></a><a name="p840103315498"></a>暂不支持关于输出文件格式以及输入输出路径相关的配置项。</p>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p6103630103420"><a name="p6103630103420"></a><a name="p6103630103420"></a>-</p>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **说明：**   
>提交Germline Variant作业需进行实名认证，并且需要进行委托授权。具体操作请参考[准备工作](准备工作.md)。  

## 查找作业<a name="section178081651114414"></a>

在[图1](#fig48381724346)右上侧“日期”栏，单击![](figures/zh-cn_image_0133412552.png)选择“开始时间”和“结束时间”，可查找对应时间段内提交的作业。

## 查看作业详情<a name="section7216175035112"></a>

在[图1](#fig48381724346)页面，选中一条作业，单击该作业对应的![](figures/zh-cn_image_0133412554.png)，可查看该条作业的详细信息。

包括：输入路径，输出路径，文件类型，参考基因，已知变异基因集，输出GVCF，FastqToSam参数，BwaSpark参数，ReadPipelineSpark参数（若输入文件为BAM，则只显示该参数），BQSR文件导出（创建作业时，若没有选择，则不显示），执行引擎（若输入文件为BAM，则显示该参数），日志详情（如果作业执行失败，会显示失败原因）。

**图 3**  Germline Variant作业详情<a name="fig187315426564"></a>  
![](figures/Germline-Variant作业详情.png "Germline-Variant作业详情")

