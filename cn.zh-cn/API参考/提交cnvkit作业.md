# 提交cnvkit作业<a name="dli_02_0156"></a>

## 功能介绍<a name="section13287428103611"></a>

创建、提交并执行cnvkit作业。

## URI<a name="section52924285361"></a>

-   URI格式

    POST /v2.0/\{project\_id\}/gene/tools/cnvkit

-   参数说明

    **表 1**  URI参数

    <a name="table18299172853614"></a>
    <table><thead align="left"><tr id="row947592853614"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.4.1.1"><p id="p1347513282368"><a name="p1347513282368"></a><a name="p1347513282368"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p74757287366"><a name="p74757287366"></a><a name="p74757287366"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="50%" id="mcps1.2.4.1.3"><p id="p1475182833610"><a name="p1475182833610"></a><a name="p1475182833610"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row16475152833619"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.1 "><p id="p1547552803615"><a name="p1547552803615"></a><a name="p1547552803615"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p19475828123613"><a name="p19475828123613"></a><a name="p19475828123613"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p134756284367"><a name="p134756284367"></a><a name="p134756284367"></a>项目编号。获取方法，请参见<a href="获取项目编号.md">获取项目编号</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="section1831452873613"></a>

**表 2**  请求参数

<a name="table19317132814368"></a>
<table><thead align="left"><tr id="row6476182803617"><th class="cellrowborder" valign="top" width="14.000000000000002%" id="mcps1.2.5.1.1"><p id="p7476142811364"><a name="p7476142811364"></a><a name="p7476142811364"></a>参数名</p>
</th>
<th class="cellrowborder" valign="top" width="9%" id="mcps1.2.5.1.2"><p id="p16476102818360"><a name="p16476102818360"></a><a name="p16476102818360"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="14.000000000000002%" id="mcps1.2.5.1.3"><p id="p147652813365"><a name="p147652813365"></a><a name="p147652813365"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="63%" id="mcps1.2.5.1.4"><p id="p447622833612"><a name="p447622833612"></a><a name="p447622833612"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row17476828143615"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p1314104871213"><a name="p1314104871213"></a><a name="p1314104871213"></a>experimental_inputs</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p9476328153611"><a name="p9476328153611"></a><a name="p9476328153611"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p847672812361"><a name="p847672812361"></a><a name="p847672812361"></a>Array[String]</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><div class="p" id="p19676154814477"><a name="p19676154814477"></a><a name="p19676154814477"></a>待测样本的路径。<div class="note" id="note1080012315201"><a name="note1080012315201"></a><a name="note1080012315201"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p118011631132019"><a name="p118011631132019"></a><a name="p118011631132019"></a>现阶段仅接受排序、标记/去除重复之后的BAM文件</p>
</div></div>
</div>
</td>
</tr>
<tr id="row77714148278"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p10528141511272"><a name="p10528141511272"></a><a name="p10528141511272"></a>control_inputs</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p20529161552719"><a name="p20529161552719"></a><a name="p20529161552719"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p8531181519277"><a name="p8531181519277"></a><a name="p8531181519277"></a>Array[String]</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><div class="p" id="p1453261542719"><a name="p1453261542719"></a><a name="p1453261542719"></a>对照样本的路径。<div class="note" id="note185338155274"><a name="note185338155274"></a><a name="note185338155274"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p9536101532717"><a name="p9536101532717"></a><a name="p9536101532717"></a>现阶段仅接受排序、标记/去除重复之后的BAM文件</p>
</div></div>
</div>
</td>
</tr>
<tr id="row8477328193612"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p16477152815366"><a name="p16477152815366"></a><a name="p16477152815366"></a>output_dir</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p16477122823611"><a name="p16477122823611"></a><a name="p16477122823611"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p6477182853620"><a name="p6477182853620"></a><a name="p6477182853620"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p18477728173614"><a name="p18477728173614"></a><a name="p18477728173614"></a>存放输出结果的OBS文件夹路径。</p>
</td>
</tr>
<tr id="row184771028183617"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p1847712823618"><a name="p1847712823618"></a><a name="p1847712823618"></a>ref</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p34771828193615"><a name="p34771828193615"></a><a name="p34771828193615"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p847702863615"><a name="p847702863615"></a><a name="p847702863615"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p11477152863617"><a name="p11477152863617"></a><a name="p11477152863617"></a>参考基因组文件。</p>
</td>
</tr>
<tr id="row113875567118"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p7387165671116"><a name="p7387165671116"></a><a name="p7387165671116"></a>bed</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p11387195621110"><a name="p11387195621110"></a><a name="p11387195621110"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p1159104333311"><a name="p1159104333311"></a><a name="p1159104333311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p7387145631112"><a name="p7387145631112"></a><a name="p7387145631112"></a>外显子区域Bed文件或interval文件。</p>
</td>
</tr>
<tr id="row1811316545118"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p101137542114"><a name="p101137542114"></a><a name="p101137542114"></a>has_annotate</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p121131554161110"><a name="p121131554161110"></a><a name="p121131554161110"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p179051018353"><a name="p179051018353"></a><a name="p179051018353"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p131132054111117"><a name="p131132054111117"></a><a name="p131132054111117"></a>是否使用注释文件。</p>
</td>
</tr>
<tr id="row15477828153615"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p174775286367"><a name="p174775286367"></a><a name="p174775286367"></a>annotation_file</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p10477162833610"><a name="p10477162833610"></a><a name="p10477162833610"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p947716288367"><a name="p947716288367"></a><a name="p947716288367"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p1687113185379"><a name="p1687113185379"></a><a name="p1687113185379"></a>注释文件。当has_annotate为true时，该参数必选。</p>
</td>
</tr>
<tr id="row113781706390"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p137811014391"><a name="p137811014391"></a><a name="p137811014391"></a>target_conf</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p537811017397"><a name="p537811017397"></a><a name="p537811017397"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p237870143915"><a name="p237870143915"></a><a name="p237870143915"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p153781203390"><a name="p153781203390"></a><a name="p153781203390"></a>子步骤target可选参数配置，应用于用户上传的外显子区域Bed文件或interval文件。</p>
</td>
</tr>
<tr id="row1363317215391"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p1263316263913"><a name="p1263316263913"></a><a name="p1263316263913"></a>antitarget_conf</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p582916389401"><a name="p582916389401"></a><a name="p582916389401"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p1212935044014"><a name="p1212935044014"></a><a name="p1212935044014"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p14736173118436"><a name="p14736173118436"></a><a name="p14736173118436"></a>子步骤antitarget可选参数配置，应用于用户上传的外显子区域Bed文件或interval文件。</p>
</td>
</tr>
<tr id="row147311513395"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p573118515397"><a name="p573118515397"></a><a name="p573118515397"></a>coverage_conf</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p1597211392406"><a name="p1597211392406"></a><a name="p1597211392406"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p1579155018408"><a name="p1579155018408"></a><a name="p1579155018408"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p16732135103910"><a name="p16732135103910"></a><a name="p16732135103910"></a>子步骤coverage可选参数配置，应用于对照组和待测组的所有样本。</p>
</td>
</tr>
<tr id="row1219017815396"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p1019017843919"><a name="p1019017843919"></a><a name="p1019017843919"></a>sex_conf</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p1569134054012"><a name="p1569134054012"></a><a name="p1569134054012"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p64186518405"><a name="p64186518405"></a><a name="p64186518405"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p519098183916"><a name="p519098183916"></a><a name="p519098183916"></a>子步骤sex可选参数配置，应用于对照组和待测组的所有样本。</p>
</td>
</tr>
<tr id="row1671216153911"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p867131633910"><a name="p867131633910"></a><a name="p867131633910"></a>reference_conf</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p1713214113402"><a name="p1713214113402"></a><a name="p1713214113402"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p82185214409"><a name="p82185214409"></a><a name="p82185214409"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p1671168398"><a name="p1671168398"></a><a name="p1671168398"></a>子步骤reference可选参数配置，应用于对照组样本。</p>
</td>
</tr>
<tr id="row1251101883914"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p192531618183917"><a name="p192531618183917"></a><a name="p192531618183917"></a>fix_conf</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p7634194194019"><a name="p7634194194019"></a><a name="p7634194194019"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p176811541409"><a name="p176811541409"></a><a name="p176811541409"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p125391819399"><a name="p125391819399"></a><a name="p125391819399"></a>子步骤fix可选参数配置， 应用于待测组样本。</p>
</td>
</tr>
<tr id="row9533132023916"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p9533720103918"><a name="p9533720103918"></a><a name="p9533720103918"></a>segment_conf</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p221315426402"><a name="p221315426402"></a><a name="p221315426402"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p6495135554010"><a name="p6495135554010"></a><a name="p6495135554010"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p14533112017392"><a name="p14533112017392"></a><a name="p14533112017392"></a>子步骤segment可选参数配置，应用于待测组样本。</p>
</td>
</tr>
<tr id="row1852982211392"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p252922213912"><a name="p252922213912"></a><a name="p252922213912"></a>genemetrics_conf</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p135631343164017"><a name="p135631343164017"></a><a name="p135631343164017"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p18599562405"><a name="p18599562405"></a><a name="p18599562405"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p1352912223911"><a name="p1352912223911"></a><a name="p1352912223911"></a>子步骤genemetrics可选参数配置，应用于待测组样本。</p>
</td>
</tr>
<tr id="row15522122716397"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p125222027133920"><a name="p125222027133920"></a><a name="p125222027133920"></a>call_conf</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p9119944164018"><a name="p9119944164018"></a><a name="p9119944164018"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p95451561404"><a name="p95451561404"></a><a name="p95451561404"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p185222272398"><a name="p185222272398"></a><a name="p185222272398"></a>子步骤call可选参数配置，应用于待测组样本。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="section134515287360"></a>

-   返回码

    201


-   响应参数

**表 3**  响应参数

<a name="table8348112818368"></a>
<table><thead align="left"><tr id="row11478132863610"><th class="cellrowborder" valign="top" width="29.409999999999997%" id="mcps1.2.4.1.1"><p id="p04782028173616"><a name="p04782028173616"></a><a name="p04782028173616"></a>参数名</p>
</th>
<th class="cellrowborder" valign="top" width="17.65%" id="mcps1.2.4.1.2"><p id="p34781128193612"><a name="p34781128193612"></a><a name="p34781128193612"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="52.94%" id="mcps1.2.4.1.3"><p id="p1347917286364"><a name="p1347917286364"></a><a name="p1347917286364"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row18479182813362"><td class="cellrowborder" valign="top" width="29.409999999999997%" headers="mcps1.2.4.1.1 "><p id="p12479202810367"><a name="p12479202810367"></a><a name="p12479202810367"></a>instance_id</p>
</td>
<td class="cellrowborder" valign="top" width="17.65%" headers="mcps1.2.4.1.2 "><p id="p54794288369"><a name="p54794288369"></a><a name="p54794288369"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.4.1.3 "><p id="p4479428183614"><a name="p4479428183614"></a><a name="p4479428183614"></a>作业ID，可用于获取作业状态。</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section910624615450"></a>

-   请求样例：

    ```
    {  
        "experimental_inputs" : ["s3a://genes/cnvkit/Son_S2_ALL.sort.mkdup.bam"],
        "control_inputs": ["s3a://genes/cnvkit/Father_S5_ALL.sort.mkdup.bam","s3a://genes/cnvkit/Mather_S1_ALL.sort.mkdup.bam"],
        "output_dir": "s3a://genes/cnvkit/output/",
        "ref": "s3a://genes/cnvkit/hg38.filtered.fa",
        "bed": "s3a://genes/cnvkit/tEXOME2_ext50.bed",
        "has_annotate": false,
        "annotation_file": "s3a://genes/cnvkit/gencode.v29.annotation.gff3",
    
        "target_conf": "--split",
        "antitarget_conf": "-a 100000",
        "reference_conf":"--no-rmask",
        "coverage_conf":"-q 10 -p 5",
        "fix_conf": "--no-rmask",
        "segment_conf":"-m cbs  --drop-low-coverage -t 0.001  --drop-outliers 5",
        "genemetrics_conf":"--drop-low-coverage -a 0.001 -b 150 --mean",
        "call_conf":"--center mean  --center-at 0 --drop-low-coverage",
        "sex_conf":"-y"
    }
    ```


-   成功响应样例:

    ```
    {
      "instanc_id": "00000000-0000-0001-0000-000000000002"
    }
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >调用接口出错后，将不会返回上述结果，而是返回错误码和错误信息，详细介绍请参见[错误码](错误码.md)。  


