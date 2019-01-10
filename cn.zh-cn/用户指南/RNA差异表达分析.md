# RNA差异表达分析<a name="dli_01_0394"></a>

## RNA差异表达分析概述<a name="section8244204903017"></a>

有参RNA-Seq差异表达分析流程。该流程一键式地完成了FASTQ文件的过滤，参考基因组的比对，不同样本（组）间基因表达的差异进行分析等处理，并最终输出差异表达及GO/KEGG富集分析结果。

>![](public_sys-resources/icon-note.gif) **说明：**   
>提交RNA差异表达分析作业需进行实名认证，并且需要进行委托授权。具体操作请参考[准备工作](准备工作.md)。  

## 创建作业<a name="section393363684419"></a>

**图 1**  RNA差异表达分析创建作业<a name="fig5850193418534"></a>  
![](figures/RNA差异表达分析创建作业.png "RNA差异表达分析创建作业")

1.  数据导入

    **图 2**  RNA差异表达分析数据导入<a name="fig16945784146"></a>  
    ![](figures/RNA差异表达分析数据导入.png "RNA差异表达分析数据导入")

    在“样本信息”中，输入样本名称（自定义），选择输入文件的OBS路径。可根据需要添加样本组。例如：

    **图 3**  数据导入示例<a name="fig166114414305"></a>  
    ![](figures/数据导入示例.png "数据导入示例")

2.  基本参数配置

    **图 4**  RNA差异表达分析基本参数配置<a name="fig2521134601810"></a>  
    ![](figures/RNA差异表达分析基本参数配置.png "RNA差异表达分析基本参数配置")

    **表 1**  参数说明

    <a name="table34159998103738"></a>
    <table><thead align="left"><tr id="row18398987103738"><th class="cellrowborder" valign="top" width="15.646464646464645%" id="mcps1.2.4.1.1"><p id="p13922998103738"><a name="p13922998103738"></a><a name="p13922998103738"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="57.28282828282828%" id="mcps1.2.4.1.2"><p id="p54021066103738"><a name="p54021066103738"></a><a name="p54021066103738"></a>描述</p>
    </th>
    <th class="cellrowborder" valign="top" width="27.070707070707066%" id="mcps1.2.4.1.3"><p id="p13630189103738"><a name="p13630189103738"></a><a name="p13630189103738"></a>示例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row37659849105931"><td class="cellrowborder" valign="top" width="15.646464646464645%" headers="mcps1.2.4.1.1 "><p id="p30548909105931"><a name="p30548909105931"></a><a name="p30548909105931"></a>接头序列</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.28282828282828%" headers="mcps1.2.4.1.2 "><p id="p58542558105931"><a name="p58542558105931"></a><a name="p58542558105931"></a>测序过程中使用的adapter序列，用于去除输入数据中的对应序列。</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.070707070707066%" headers="mcps1.2.4.1.3 "><p id="p45477491748"><a name="p45477491748"></a><a name="p45477491748"></a>-</p>
    </td>
    </tr>
    <tr id="row16943758105944"><td class="cellrowborder" valign="top" width="15.646464646464645%" headers="mcps1.2.4.1.1 "><p id="p30267119105944"><a name="p30267119105944"></a><a name="p30267119105944"></a>参考基因组序列</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.28282828282828%" headers="mcps1.2.4.1.2 "><p id="p127371727548"><a name="p127371727548"></a><a name="p127371727548"></a>基因行业内标准的基因库，目前支持hg19和hg38。</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.070707070707066%" headers="mcps1.2.4.1.3 "><p id="p1354613491044"><a name="p1354613491044"></a><a name="p1354613491044"></a>hg19</p>
    </td>
    </tr>
    <tr id="row8664577112415"><td class="cellrowborder" valign="top" width="15.646464646464645%" headers="mcps1.2.4.1.1 "><p id="p30742160112415"><a name="p30742160112415"></a><a name="p30742160112415"></a>基因注释</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.28282828282828%" headers="mcps1.2.4.1.2 "><p id="p21681018173311"><a name="p21681018173311"></a><a name="p21681018173311"></a>参考基因组注释文件，来源于gencode数据库。</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.070707070707066%" headers="mcps1.2.4.1.3 "><p id="p16543249247"><a name="p16543249247"></a><a name="p16543249247"></a>gencode.v17.annotation.gtf</p>
    </td>
    </tr>
    <tr id="row1161063874114"><td class="cellrowborder" valign="top" width="15.646464646464645%" headers="mcps1.2.4.1.1 "><p id="p5610153818417"><a name="p5610153818417"></a><a name="p5610153818417"></a>输出质控文件</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.28282828282828%" headers="mcps1.2.4.1.2 "><p id="p961010383416"><a name="p961010383416"></a><a name="p961010383416"></a>选择“是”，需选择质控注释文件。默认值为“否”。</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.070707070707066%" headers="mcps1.2.4.1.3 "><p id="p19610538154120"><a name="p19610538154120"></a><a name="p19610538154120"></a>否</p>
    </td>
    </tr>
    <tr id="row1549165112513"><td class="cellrowborder" valign="top" width="15.646464646464645%" headers="mcps1.2.4.1.1 "><p id="p950135116517"><a name="p950135116517"></a><a name="p950135116517"></a>质控注释文件</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.28282828282828%" headers="mcps1.2.4.1.2 "><p id="p15508519512"><a name="p15508519512"></a><a name="p15508519512"></a>RSeQC质控所需要的基因注释文件。</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.070707070707066%" headers="mcps1.2.4.1.3 "><p id="p1450951185110"><a name="p1450951185110"></a><a name="p1450951185110"></a>-</p>
    </td>
    </tr>
    <tr id="row208095231057"><td class="cellrowborder" valign="top" width="15.646464646464645%" headers="mcps1.2.4.1.1 "><p id="p12809623556"><a name="p12809623556"></a><a name="p12809623556"></a>建库方式</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.28282828282828%" headers="mcps1.2.4.1.2 "><p id="p17168201893319"><a name="p17168201893319"></a><a name="p17168201893319"></a>输入数据的链特异性建库方式。</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.070707070707066%" headers="mcps1.2.4.1.3 "><p id="p28108231257"><a name="p28108231257"></a><a name="p28108231257"></a>fr-unstranded</p>
    </td>
    </tr>
    <tr id="row562270711021"><td class="cellrowborder" valign="top" width="15.646464646464645%" headers="mcps1.2.4.1.1 "><p id="p5278609511021"><a name="p5278609511021"></a><a name="p5278609511021"></a>输出路径</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.28282828282828%" headers="mcps1.2.4.1.2 "><p id="p1216614183333"><a name="p1216614183333"></a><a name="p1216614183333"></a>存放分析结果的OBS路径。</p>
    </td>
    <td class="cellrowborder" valign="top" width="27.070707070707066%" headers="mcps1.2.4.1.3 "><p id="p25421649942"><a name="p25421649942"></a><a name="p25421649942"></a>-</p>
    </td>
    </tr>
    </tbody>
    </table>

3.  差异表达分析

    **图 5**  差异表达分析<a name="fig649863113413"></a>  
    ![](figures/差异表达分析.png "差异表达分析")

    勾选需要对比的样本。例如，“对照组”选择“test1”，“实验组”选择“test2”。单击![](figures/icon-增加组.png)，表示对比“test1”和“test2”。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >可勾选多组样本。  

4.  单击“提交”。

## 作业列表<a name="section1321193764413"></a>

**图 6**  RNA差异表达分析作业列表<a name="fig417123764416"></a>  
![](figures/RNA差异表达分析作业列表.png "RNA差异表达分析作业列表")

作业列表显示所有的RNA差异表达分析作业，作业数量较多时，系统分页显示，您可以查看所有历史提交的作业。作业列表默认按创建时间降序排列，可切换为按时间升序排列；也可以选择时间范围，查看特定时间范围内提交的作业。

**表 2**  作业列表参数

<a name="table1420337144417"></a>
<table><thead align="left"><tr id="row717133713445"><th class="cellrowborder" valign="top" width="21.18%" id="mcps1.2.3.1.1"><p id="p10171037124419"><a name="p10171037124419"></a><a name="p10171037124419"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="78.82000000000001%" id="mcps1.2.3.1.2"><p id="p18171837164411"><a name="p18171837164411"></a><a name="p18171837164411"></a>参数说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row3172037174416"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p15171937204417"><a name="p15171937204417"></a><a name="p15171937204417"></a>创建时间</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p121743711445"><a name="p121743711445"></a><a name="p121743711445"></a>每个作业的创建时间，目前按创建时间倒序显示作业列表。</p>
</td>
</tr>
<tr id="row5199378440"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p417103744413"><a name="p417103744413"></a><a name="p417103744413"></a>作业状态</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p11177375442"><a name="p11177375442"></a><a name="p11177375442"></a>作业的状态信息，包括如下六种状态。</p>
<a name="ul101814378442"></a><a name="ul101814378442"></a><ul id="ul101814378442"><li>提交中（launching）</li><li>运行中（running）</li><li>已成功（finished）</li><li>已失败（failed）</li><li>已删除（deleted）</li><li>未知异常（unknown）</li></ul>
</td>
</tr>
<tr id="row161953714418"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p2191137184413"><a name="p2191137184413"></a><a name="p2191137184413"></a>作业ID</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p14191837204414"><a name="p14191837204414"></a><a name="p14191837204414"></a>所提交基因作业的ID，由系统默认生成的唯一标识。</p>
</td>
</tr>
<tr id="row2020537174418"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p519163744413"><a name="p519163744413"></a><a name="p519163744413"></a>用户名</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p2019133764416"><a name="p2019133764416"></a><a name="p2019133764416"></a>提交基因作业的用户名称。</p>
</td>
</tr>
<tr id="row42053714411"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p102033774414"><a name="p102033774414"></a><a name="p102033774414"></a>运行时长</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p1620163714420"><a name="p1620163714420"></a><a name="p1620163714420"></a>作业运行的时间长度。</p>
</td>
</tr>
<tr id="row1820103719447"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p52073744414"><a name="p52073744414"></a><a name="p52073744414"></a>进度</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p620113794412"><a name="p620113794412"></a><a name="p620113794412"></a>作业运行的进度， 例如：1/1表示该作业有一个步骤，当前已完成。</p>
</td>
</tr>
</tbody>
</table>

-   查找作业

    在[图6](#fig417123764416)右上侧“日期”栏，单击![](figures/icon-日期.png)选择“开始时间”和“结束时间”，可查找对应时间段内提交的作业。

-   查看作业详情

    在[图6](#fig417123764416)页面，选中一条作业，单击该作业对应的![](figures/icon-展开.png)，可查看该条作业的详细信息。

    -   基本配置

        包括：参考基因组序列，建库方式，基因注释，输出路径，输出质控文件，质控注释文件，接头序列。

    -   样本信息

        **图 7**  RNA差异表达分析作业详情<a name="fig187315426564"></a>  
        ![](figures/RNA差异表达分析作业详情.png "RNA差异表达分析作业详情")



## 流程介绍<a name="section193935119520"></a>

**图 8**  RNA差异表达分析流程介绍<a name="fig1171410531162"></a>  
![](figures/RNA差异表达分析流程介绍.png "RNA差异表达分析流程介绍")

