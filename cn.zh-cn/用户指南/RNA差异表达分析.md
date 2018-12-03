# RNA差异表达分析<a name="dli_01_0394"></a>

## RNA差异表达分析页面说明<a name="section8244204903017"></a>

DLI全托管的有参考基因组的RNA差异表达分析流程。该流程一键式地完成了FASTQ文件的过滤，参考基因组的对齐，count矩阵的生成，不同样本（组）基因表达的差异分析等处理，并最终输出差异分析结果。

**图 1**  RNA差异表达分析<a name="fig48381724346"></a>  
![](figures/RNA差异表达分析.png "RNA差异表达分析")

RNA差异表达分析页面显示所有的基因作业，作业数量较多时，系统分页显示，您可以查看所有历史提交的作业。作业列表默认按创建时间排列，可选择升序或降序排列；也可以选择时间范围，查看特定时间范围内提交的作业。

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
<tr id="row31011923151038"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p10671857151038"><a name="p10671857151038"></a><a name="p10671857151038"></a>作业状态</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p59114099151038"><a name="p59114099151038"></a><a name="p59114099151038"></a>作业的状态信息，包括如下六种状态。</p>
<a name="ul691214351291"></a><a name="ul691214351291"></a><ul id="ul691214351291"><li>提交中（launching）</li><li>运行中（running）</li><li>已成功（finished）</li><li>已失败（failed）</li><li>已删除（deleted）</li><li>未知异常（unknown）</li></ul>
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
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p1356922117439"><a name="p1356922117439"></a><a name="p1356922117439"></a>作业运行的进度， 例如：1/1表示该作业有一个步骤，当前已完成。</p>
</td>
</tr>
</tbody>
</table>

## 创建作业<a name="section1235315355212"></a>

在[图1](#fig48381724346)中，单击![](figures/zh-cn_image_0133412546.png)，进入[图2](#fig5850193418534)页面。

**图 2**  创建RNA差异表达分析作业<a name="fig5850193418534"></a>  
![](figures/创建RNA差异表达分析作业.png "创建RNA差异表达分析作业")

1.  数据导入

    **图 3**  RNA差异表达分析数据导入<a name="fig16945784146"></a>  
    ![](figures/RNA差异表达分析数据导入.png "RNA差异表达分析数据导入")

    在“样本信息”中，输入样本名称，选择输入文件OBS路径，根据需要增加样本组。

    例如：

    **图 4**  数据导入示例<a name="fig166114414305"></a>  
    ![](figures/数据导入示例.png "数据导入示例")

2.  基本配置

    **图 5**  RNA差异表达分析基本配置<a name="fig2521134601810"></a>  
    ![](figures/RNA差异表达分析基本配置.png "RNA差异表达分析基本配置")

    参见[表2](#table34159998103738)输入相关参数。

    **表 2**  参数说明

    <a name="table34159998103738"></a>
    <table><thead align="left"><tr id="row18398987103738"><th class="cellrowborder" valign="top" width="12.606060606060607%" id="mcps1.2.4.1.1"><p id="p13922998103738"><a name="p13922998103738"></a><a name="p13922998103738"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="61.7979797979798%" id="mcps1.2.4.1.2"><p id="p54021066103738"><a name="p54021066103738"></a><a name="p54021066103738"></a>描述</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.5959595959596%" id="mcps1.2.4.1.3"><p id="p13630189103738"><a name="p13630189103738"></a><a name="p13630189103738"></a>示例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row37659849105931"><td class="cellrowborder" valign="top" width="12.606060606060607%" headers="mcps1.2.4.1.1 "><p id="p30548909105931"><a name="p30548909105931"></a><a name="p30548909105931"></a>接头序列</p>
    </td>
    <td class="cellrowborder" valign="top" width="61.7979797979798%" headers="mcps1.2.4.1.2 "><p id="p58542558105931"><a name="p58542558105931"></a><a name="p58542558105931"></a>测序过程中使用的adapter序列，用于去除输入数据中的对应序列。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.5959595959596%" headers="mcps1.2.4.1.3 "><p id="p45477491748"><a name="p45477491748"></a><a name="p45477491748"></a>-</p>
    </td>
    </tr>
    <tr id="row16943758105944"><td class="cellrowborder" valign="top" width="12.606060606060607%" headers="mcps1.2.4.1.1 "><p id="p30267119105944"><a name="p30267119105944"></a><a name="p30267119105944"></a>参考基因</p>
    </td>
    <td class="cellrowborder" valign="top" width="61.7979797979798%" headers="mcps1.2.4.1.2 "><p id="p127371727548"><a name="p127371727548"></a><a name="p127371727548"></a>基因行业内标准的基因库，目前支持hg19和hg38。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.5959595959596%" headers="mcps1.2.4.1.3 "><p id="p1354613491044"><a name="p1354613491044"></a><a name="p1354613491044"></a>hg19</p>
    </td>
    </tr>
    <tr id="row8664577112415"><td class="cellrowborder" valign="top" width="12.606060606060607%" headers="mcps1.2.4.1.1 "><p id="p30742160112415"><a name="p30742160112415"></a><a name="p30742160112415"></a>基因注释</p>
    </td>
    <td class="cellrowborder" valign="top" width="61.7979797979798%" headers="mcps1.2.4.1.2 "><p id="p21681018173311"><a name="p21681018173311"></a><a name="p21681018173311"></a>参考基因组注释文件，来源于gencode数据库。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.5959595959596%" headers="mcps1.2.4.1.3 "><p id="p16543249247"><a name="p16543249247"></a><a name="p16543249247"></a>gencode.v17.annotation.gtf</p>
    </td>
    </tr>
    <tr id="row1161063874114"><td class="cellrowborder" valign="top" width="12.606060606060607%" headers="mcps1.2.4.1.1 "><p id="p5610153818417"><a name="p5610153818417"></a><a name="p5610153818417"></a>输出质控文件</p>
    </td>
    <td class="cellrowborder" valign="top" width="61.7979797979798%" headers="mcps1.2.4.1.2 "><p id="p961010383416"><a name="p961010383416"></a><a name="p961010383416"></a>选择“是”，需选择质控注释文件。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.5959595959596%" headers="mcps1.2.4.1.3 "><p id="p19610538154120"><a name="p19610538154120"></a><a name="p19610538154120"></a>否</p>
    </td>
    </tr>
    <tr id="row1549165112513"><td class="cellrowborder" valign="top" width="12.606060606060607%" headers="mcps1.2.4.1.1 "><p id="p950135116517"><a name="p950135116517"></a><a name="p950135116517"></a>质控注释文件</p>
    </td>
    <td class="cellrowborder" valign="top" width="61.7979797979798%" headers="mcps1.2.4.1.2 "><p id="p15508519512"><a name="p15508519512"></a><a name="p15508519512"></a>RSeQC质控所需要的基因注释文件。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.5959595959596%" headers="mcps1.2.4.1.3 "><p id="p1450951185110"><a name="p1450951185110"></a><a name="p1450951185110"></a>-</p>
    </td>
    </tr>
    <tr id="row208095231057"><td class="cellrowborder" valign="top" width="12.606060606060607%" headers="mcps1.2.4.1.1 "><p id="p12809623556"><a name="p12809623556"></a><a name="p12809623556"></a>建库方式</p>
    </td>
    <td class="cellrowborder" valign="top" width="61.7979797979798%" headers="mcps1.2.4.1.2 "><p id="p17168201893319"><a name="p17168201893319"></a><a name="p17168201893319"></a>输入数据的链特异性建库方式。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.5959595959596%" headers="mcps1.2.4.1.3 "><p id="p28108231257"><a name="p28108231257"></a><a name="p28108231257"></a>fr-unstranded</p>
    </td>
    </tr>
    <tr id="row562270711021"><td class="cellrowborder" valign="top" width="12.606060606060607%" headers="mcps1.2.4.1.1 "><p id="p5278609511021"><a name="p5278609511021"></a><a name="p5278609511021"></a>输出路径</p>
    </td>
    <td class="cellrowborder" valign="top" width="61.7979797979798%" headers="mcps1.2.4.1.2 "><p id="p1216614183333"><a name="p1216614183333"></a><a name="p1216614183333"></a>存放分析结果的OBS路径。</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.5959595959596%" headers="mcps1.2.4.1.3 "><p id="p25421649942"><a name="p25421649942"></a><a name="p25421649942"></a>-</p>
    </td>
    </tr>
    </tbody>
    </table>

3.  差异表达分析

    **图 6**  差异表达分析<a name="fig649863113413"></a>  
    ![](figures/差异表达分析.png "差异表达分析")

    勾选需要对比的样本。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >可勾选多组样本。  

4.  单击“确定”。

>![](public_sys-resources/icon-note.gif) **说明：**   
>提交RNA差异表达分析作业需进行实名认证，并且需要进行委托授权。具体操作请参考[准备工作](准备工作.md)。  

## 查找作业<a name="section178081651114414"></a>

在[图1](#fig48381724346)右上侧“日期”栏，单击![](figures/zh-cn_image_0133412552.png)选择“开始时间”和“结束时间”，可查找对应时间段内提交的作业。

## 查看作业详情<a name="section7216175035112"></a>

在[图1](#fig48381724346)页面，选中一条作业，单击该作业对应的![](figures/zh-cn_image_0133412554.png)，可查看该条作业的详细信息。

-   基本配置

    包括：参考基因，建库方式，基因注释，输出路径，输出质控文件，质控注释文件，接头序列。

-   样本信息

**图 7**  RNA差异表达分析作业详情<a name="fig187315426564"></a>  
![](figures/RNA差异表达分析作业详情.png "RNA差异表达分析作业详情")

