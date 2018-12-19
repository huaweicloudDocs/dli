# 提交rna-diffExpr作业<a name="dli_02_0149"></a>

## 功能介绍<a name="section6968756197"></a>

创建、提交并执行RNA差异表达分析作业。

## URI<a name="section169693561590"></a>

-   URI格式

    POST /v2.0/\{project\_id\}/gene/jobs

-   参数说明

    **表 1**  URI参数

    <a name="table129761556598"></a>
    <table><thead align="left"><tr id="row1826735713913"><th class="cellrowborder" valign="top" width="17.171717171717173%" id="mcps1.2.4.1.1"><p id="p226717571598"><a name="p226717571598"></a><a name="p226717571598"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.121212121212121%" id="mcps1.2.4.1.2"><p id="p8267195712917"><a name="p8267195712917"></a><a name="p8267195712917"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="70.70707070707071%" id="mcps1.2.4.1.3"><p id="p11267457995"><a name="p11267457995"></a><a name="p11267457995"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1026714572915"><td class="cellrowborder" valign="top" width="17.171717171717173%" headers="mcps1.2.4.1.1 "><p id="p1547552803615"><a name="p1547552803615"></a><a name="p1547552803615"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.2.4.1.2 "><p id="p19475828123613"><a name="p19475828123613"></a><a name="p19475828123613"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="70.70707070707071%" headers="mcps1.2.4.1.3 "><p id="p134756284367"><a name="p134756284367"></a><a name="p134756284367"></a>项目编号。获取方法，请参见<a href="获取项目编号.md">获取项目编号</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="section3414034164017"></a>

**表 2**  请求参数

<a name="table19317132814368"></a>
<table><thead align="left"><tr id="row6476182803617"><th class="cellrowborder" valign="top" width="11.020000000000001%" id="mcps1.2.5.1.1"><p id="p7476142811364"><a name="p7476142811364"></a><a name="p7476142811364"></a>参数名</p>
</th>
<th class="cellrowborder" valign="top" width="12.58%" id="mcps1.2.5.1.2"><p id="p16476102818360"><a name="p16476102818360"></a><a name="p16476102818360"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="15.590000000000002%" id="mcps1.2.5.1.3"><p id="p147652813365"><a name="p147652813365"></a><a name="p147652813365"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60.809999999999995%" id="mcps1.2.5.1.4"><p id="p447622833612"><a name="p447622833612"></a><a name="p447622833612"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row17476828143615"><td class="cellrowborder" valign="top" width="11.020000000000001%" headers="mcps1.2.5.1.1 "><p id="p0476152810369"><a name="p0476152810369"></a><a name="p0476152810369"></a>job_type</p>
</td>
<td class="cellrowborder" valign="top" width="12.58%" headers="mcps1.2.5.1.2 "><p id="p5476628133611"><a name="p5476628133611"></a><a name="p5476628133611"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="15.590000000000002%" headers="mcps1.2.5.1.3 "><p id="p2476202818368"><a name="p2476202818368"></a><a name="p2476202818368"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60.809999999999995%" headers="mcps1.2.5.1.4 "><p id="p11476162810366"><a name="p11476162810366"></a><a name="p11476162810366"></a>作业类型，对于RNA差异表达分析作业为：<span class="parmvalue" id="parmvalue1479322015820"><a name="parmvalue1479322015820"></a><a name="parmvalue1479322015820"></a>“RNA_DIFF_EXPR”</span>。</p>
</td>
</tr>
<tr id="row8477328193612"><td class="cellrowborder" valign="top" width="11.020000000000001%" headers="mcps1.2.5.1.1 "><p id="p19476162803619"><a name="p19476162803619"></a><a name="p19476162803619"></a>inputs</p>
</td>
<td class="cellrowborder" valign="top" width="12.58%" headers="mcps1.2.5.1.2 "><p id="p9476328153611"><a name="p9476328153611"></a><a name="p9476328153611"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="15.590000000000002%" headers="mcps1.2.5.1.3 "><p id="p847672812361"><a name="p847672812361"></a><a name="p847672812361"></a>Array[RnaGroup]</p>
</td>
<td class="cellrowborder" valign="top" width="60.809999999999995%" headers="mcps1.2.5.1.4 "><p id="p19676154814477"><a name="p19676154814477"></a><a name="p19676154814477"></a>输入实验组及对照组列表，组详情可参加<a href="#table94842054488">表3</a>。</p>
</td>
</tr>
<tr id="row184771028183617"><td class="cellrowborder" valign="top" width="11.020000000000001%" headers="mcps1.2.5.1.1 "><p id="p16477152815366"><a name="p16477152815366"></a><a name="p16477152815366"></a>output</p>
</td>
<td class="cellrowborder" valign="top" width="12.58%" headers="mcps1.2.5.1.2 "><p id="p16477122823611"><a name="p16477122823611"></a><a name="p16477122823611"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="15.590000000000002%" headers="mcps1.2.5.1.3 "><p id="p6477182853620"><a name="p6477182853620"></a><a name="p6477182853620"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60.809999999999995%" headers="mcps1.2.5.1.4 "><p id="p18477728173614"><a name="p18477728173614"></a><a name="p18477728173614"></a>差异表达分析结果输出路径。</p>
</td>
</tr>
<tr id="row71532041132513"><td class="cellrowborder" valign="top" width="11.020000000000001%" headers="mcps1.2.5.1.1 "><p id="p12153441112511"><a name="p12153441112511"></a><a name="p12153441112511"></a>adapt</p>
</td>
<td class="cellrowborder" valign="top" width="12.58%" headers="mcps1.2.5.1.2 "><p id="p16153154102511"><a name="p16153154102511"></a><a name="p16153154102511"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.590000000000002%" headers="mcps1.2.5.1.3 "><p id="p91531741152511"><a name="p91531741152511"></a><a name="p91531741152511"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60.809999999999995%" headers="mcps1.2.5.1.4 "><p id="p111537418256"><a name="p111537418256"></a><a name="p111537418256"></a>接头序列。如已过滤，则应为空。</p>
</td>
</tr>
<tr id="row1811316545118"><td class="cellrowborder" valign="top" width="11.020000000000001%" headers="mcps1.2.5.1.1 "><p id="p1847712823618"><a name="p1847712823618"></a><a name="p1847712823618"></a>ref</p>
</td>
<td class="cellrowborder" valign="top" width="12.58%" headers="mcps1.2.5.1.2 "><p id="p34771828193615"><a name="p34771828193615"></a><a name="p34771828193615"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="15.590000000000002%" headers="mcps1.2.5.1.3 "><p id="p847702863615"><a name="p847702863615"></a><a name="p847702863615"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60.809999999999995%" headers="mcps1.2.5.1.4 "><p id="p11477152863617"><a name="p11477152863617"></a><a name="p11477152863617"></a>参考基因库文件，当前支持<span class="parmvalue" id="parmvalue2912122514313"><a name="parmvalue2912122514313"></a><a name="parmvalue2912122514313"></a>“hg19”</span>、<span class="parmvalue" id="parmvalue726918314318"><a name="parmvalue726918314318"></a><a name="parmvalue726918314318"></a>“hg38”</span>两种。</p>
</td>
</tr>
<tr id="row15477828153615"><td class="cellrowborder" valign="top" width="11.020000000000001%" headers="mcps1.2.5.1.1 "><p id="p17524521125218"><a name="p17524521125218"></a><a name="p17524521125218"></a>gtf</p>
</td>
<td class="cellrowborder" valign="top" width="12.58%" headers="mcps1.2.5.1.2 "><p id="p16522162115215"><a name="p16522162115215"></a><a name="p16522162115215"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="15.590000000000002%" headers="mcps1.2.5.1.3 "><p id="p10521182195212"><a name="p10521182195212"></a><a name="p10521182195212"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60.809999999999995%" headers="mcps1.2.5.1.4 "><p id="p1252112218522"><a name="p1252112218522"></a><a name="p1252112218522"></a>基因注释文件。可选文件列表如下：</p>
<a name="ul286742616172"></a><a name="ul286742616172"></a><ul id="ul286742616172"><li>hg19对应的gtf支持<span class="parmvalue" id="parmvalue19865152615175"><a name="parmvalue19865152615175"></a><a name="parmvalue19865152615175"></a>“gencode.v17.annotation.gtf”</span></li><li>hg38对应的gtf支持<span class="parmvalue" id="parmvalue5867162611175"><a name="parmvalue5867162611175"></a><a name="parmvalue5867162611175"></a>“gencode.v28.annotation.gtf”</span></li></ul>
</td>
</tr>
<tr id="row1356218203715"><td class="cellrowborder" valign="top" width="11.020000000000001%" headers="mcps1.2.5.1.1 "><p id="p12563138103714"><a name="p12563138103714"></a><a name="p12563138103714"></a>is_export_qc</p>
</td>
<td class="cellrowborder" valign="top" width="12.58%" headers="mcps1.2.5.1.2 "><p id="p1856368183711"><a name="p1856368183711"></a><a name="p1856368183711"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.590000000000002%" headers="mcps1.2.5.1.3 "><p id="p256310853715"><a name="p256310853715"></a><a name="p256310853715"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60.809999999999995%" headers="mcps1.2.5.1.4 "><p id="p145634811379"><a name="p145634811379"></a><a name="p145634811379"></a>是否输出质控报告，默认为false</p>
</td>
</tr>
<tr id="row8274733132811"><td class="cellrowborder" valign="top" width="11.020000000000001%" headers="mcps1.2.5.1.1 "><p id="p142745337288"><a name="p142745337288"></a><a name="p142745337288"></a>bed</p>
</td>
<td class="cellrowborder" valign="top" width="12.58%" headers="mcps1.2.5.1.2 "><p id="p727453332819"><a name="p727453332819"></a><a name="p727453332819"></a>"is_export_qc"为true时该字段必选</p>
</td>
<td class="cellrowborder" valign="top" width="15.590000000000002%" headers="mcps1.2.5.1.3 "><p id="p02741333112817"><a name="p02741333112817"></a><a name="p02741333112817"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60.809999999999995%" headers="mcps1.2.5.1.4 "><p id="p1327414335284"><a name="p1327414335284"></a><a name="p1327414335284"></a>RSeQC质控所需要的基因注释文件OBS路径，该路径所在桶需与输入文件所在桶一致</p>
</td>
</tr>
<tr id="row0963184512615"><td class="cellrowborder" valign="top" width="11.020000000000001%" headers="mcps1.2.5.1.1 "><p id="p149630453269"><a name="p149630453269"></a><a name="p149630453269"></a>library_type</p>
</td>
<td class="cellrowborder" valign="top" width="12.58%" headers="mcps1.2.5.1.2 "><p id="p12963114552611"><a name="p12963114552611"></a><a name="p12963114552611"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.590000000000002%" headers="mcps1.2.5.1.3 "><p id="p129638456267"><a name="p129638456267"></a><a name="p129638456267"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60.809999999999995%" headers="mcps1.2.5.1.4 "><p id="p12963945172618"><a name="p12963945172618"></a><a name="p12963945172618"></a>建库方式，包括：<span class="parmvalue" id="parmvalue677415875610"><a name="parmvalue677415875610"></a><a name="parmvalue677415875610"></a>“fr-unstranded”</span>, <span class="parmvalue" id="parmvalue164450297574"><a name="parmvalue164450297574"></a><a name="parmvalue164450297574"></a>“fr-firststrand”</span>, <span class="parmvalue" id="parmvalue141874975710"><a name="parmvalue141874975710"></a><a name="parmvalue141874975710"></a>“fr-secondstrand”</span>三种类型，默认为<span class="parmvalue" id="parmvalue174641096580"><a name="parmvalue174641096580"></a><a name="parmvalue174641096580"></a>“fr-unstranded”</span>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  RnaGroup信息

<a name="table94842054488"></a>
<table><thead align="left"><tr id="row114871654981"><th class="cellrowborder" valign="top" width="14.141414141414144%" id="mcps1.2.5.1.1"><p id="p204897542083"><a name="p204897542083"></a><a name="p204897542083"></a>参数名</p>
</th>
<th class="cellrowborder" valign="top" width="8.080808080808081%" id="mcps1.2.5.1.2"><p id="p104892054987"><a name="p104892054987"></a><a name="p104892054987"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="15.151515151515152%" id="mcps1.2.5.1.3"><p id="p34911354487"><a name="p34911354487"></a><a name="p34911354487"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="62.62626262626263%" id="mcps1.2.5.1.4"><p id="p44911854883"><a name="p44911854883"></a><a name="p44911854883"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row34931654382"><td class="cellrowborder" valign="top" width="14.141414141414144%" headers="mcps1.2.5.1.1 "><p id="p04931154780"><a name="p04931154780"></a><a name="p04931154780"></a>group_name</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p049512541980"><a name="p049512541980"></a><a name="p049512541980"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="15.151515151515152%" headers="mcps1.2.5.1.3 "><p id="p1949618541685"><a name="p1949618541685"></a><a name="p1949618541685"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="62.62626262626263%" headers="mcps1.2.5.1.4 "><p id="p994264613130"><a name="p994264613130"></a><a name="p994264613130"></a>组标识名。英文字母起头，由英文字母、数字、下划线和中划线组成，长度为[1-128]个字符。</p>
</td>
</tr>
<tr id="row549635412811"><td class="cellrowborder" valign="top" width="14.141414141414144%" headers="mcps1.2.5.1.1 "><p id="p1549715417817"><a name="p1549715417817"></a><a name="p1549715417817"></a>group_inputs</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p749917544814"><a name="p749917544814"></a><a name="p749917544814"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="15.151515151515152%" headers="mcps1.2.5.1.3 "><p id="p10499754485"><a name="p10499754485"></a><a name="p10499754485"></a>Array[RnaSample]</p>
</td>
<td class="cellrowborder" valign="top" width="62.62626262626263%" headers="mcps1.2.5.1.4 "><p id="p95011541683"><a name="p95011541683"></a><a name="p95011541683"></a>该组包含的样本列表，样本信息详情可参考<a href="#table61801720201611">表4</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  RnaSample信息

<a name="table61801720201611"></a>
<table><thead align="left"><tr id="row4185112013166"><th class="cellrowborder" valign="top" width="14.141414141414144%" id="mcps1.2.5.1.1"><p id="p418672013163"><a name="p418672013163"></a><a name="p418672013163"></a>参数名</p>
</th>
<th class="cellrowborder" valign="top" width="8.080808080808081%" id="mcps1.2.5.1.2"><p id="p181888203162"><a name="p181888203162"></a><a name="p181888203162"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="15.151515151515152%" id="mcps1.2.5.1.3"><p id="p10188182011164"><a name="p10188182011164"></a><a name="p10188182011164"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="62.62626262626263%" id="mcps1.2.5.1.4"><p id="p61891620151617"><a name="p61891620151617"></a><a name="p61891620151617"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row181901720141617"><td class="cellrowborder" valign="top" width="14.141414141414144%" headers="mcps1.2.5.1.1 "><p id="p01922209161"><a name="p01922209161"></a><a name="p01922209161"></a>sample_name</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p141937201167"><a name="p141937201167"></a><a name="p141937201167"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="15.151515151515152%" headers="mcps1.2.5.1.3 "><p id="p9194420121615"><a name="p9194420121615"></a><a name="p9194420121615"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="62.62626262626263%" headers="mcps1.2.5.1.4 "><p id="p11196142041618"><a name="p11196142041618"></a><a name="p11196142041618"></a>样本标识名。英文字母起头，由英文字母、数字、下划线和中划线组成，长度为[1-128]个字符。</p>
</td>
</tr>
<tr id="row9196320121616"><td class="cellrowborder" valign="top" width="14.141414141414144%" headers="mcps1.2.5.1.1 "><p id="p21977204169"><a name="p21977204169"></a><a name="p21977204169"></a>files</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p131991520161610"><a name="p131991520161610"></a><a name="p131991520161610"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="15.151515151515152%" headers="mcps1.2.5.1.3 "><p id="p19200172041616"><a name="p19200172041616"></a><a name="p19200172041616"></a>Array[String]</p>
</td>
<td class="cellrowborder" valign="top" width="62.62626262626263%" headers="mcps1.2.5.1.4 "><p id="p520062011163"><a name="p520062011163"></a><a name="p520062011163"></a>该样本包含的文件列表。</p>
<div class="note" id="note1080012315201"><a name="note1080012315201"></a><a name="note1080012315201"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p118011631132019"><a name="p118011631132019"></a><a name="p118011631132019"></a>当前文件类型必须为.fastq.gz，且文件必须有两个。</p>
</div></div>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **说明：**   
>用户所有输入输出文件需使用同一个OBS桶。  

## 响应消息<a name="section2101574914"></a>

-   返回码

    201

-   响应参数

**表 5**  响应参数

<a name="table192695719914"></a>
<table><thead align="left"><tr id="row82696574918"><th class="cellrowborder" valign="top" width="15.120000000000001%" id="mcps1.2.4.1.1"><p id="p102691857892"><a name="p102691857892"></a><a name="p102691857892"></a>参数名</p>
</th>
<th class="cellrowborder" valign="top" width="12.790000000000001%" id="mcps1.2.4.1.2"><p id="p12269185711914"><a name="p12269185711914"></a><a name="p12269185711914"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="72.09%" id="mcps1.2.4.1.3"><p id="p192698571294"><a name="p192698571294"></a><a name="p192698571294"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row89762011203411"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p12479202810367"><a name="p12479202810367"></a><a name="p12479202810367"></a>job_id</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p54794288369"><a name="p54794288369"></a><a name="p54794288369"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p4479428183614"><a name="p4479428183614"></a><a name="p4479428183614"></a>作业ID，可用于获取作业状态。</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section320217117419"></a>

-   请求样例：

    ```
    {
        "job_type": "RNA_DIFF_EXPR",
        "inputs" : [
           {
              "group_name": "K",
              "group_inputs": [
                   {
                       "sample_name": "SRR6354710_2M",
                       "files": ["s3a://diff-expr/SRR6354710_2M_R1.fastq.gz", "s3a://diff-expr/SRR6354710_2M_R2.fastq.gz"]
                   },
                   {
                       "sample_name": "SRR6354711_2M",
                       "files": ["s3a://diff-expr/SRR6354711_2M_R1.fastq.gz", "s3a://diff-expr/SRR6354711_2M_R2.fastq.gz"]
                   }
              ]
           },
           {
              "group_name": "W",
              "group_inputs": [
                   {
                       "sample_name": "SRR6354714_2M",
                       "files": ["s3a://diff-expr/SRR6354714_2M_R1.fastq.gz", "s3a://diff-expr/SRR6354714_2M_R2.fastq.gz"]
                   },
                   {
                       "sample_name": "SRR6354715_2M",
                       "files": ["s3a://diff-expr/SRR6354715_2M_R1.fastq.gz", "s3a://diff-expr/SRR6354715_2M_R2.fastq.gz"]
                   }
              ]
           }
        ],
       "adapt": "CATGATTGATGGTGCCTACAG",
       "ref": "hg19",
       "gtf": "gencode.v17.annotation.gtf",
       "is_export_qc": true,
       "bed": "s3a://diff-expr/hg19_rRNA.bed"
       "library_type": "fr-firststrand",
       "output": "s3a://diff-expr/out"
    }
    ```


-   成功响应样例:

    ```
    {
      "job_id": "00000000-0000-0001-0000-000000000002"
    }
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >调用接口出错后，将不会返回上述结果，而是返回错误码和错误信息，详细介绍请参见[错误码](错误码.md)。  


