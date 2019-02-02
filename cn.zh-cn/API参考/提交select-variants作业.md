# 提交select-variants作业<a name="dli_02_0147"></a>

## 功能介绍<a name="section13287428103611"></a>

创建、提交并执行select-variants作业。

## URI<a name="section52924285361"></a>

-   URI格式

    POST /v2.0/\{project\_id\}/gene/tools/select-variants

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
<tbody><tr id="row17476828143615"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p19476162803619"><a name="p19476162803619"></a><a name="p19476162803619"></a>input</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p9476328153611"><a name="p9476328153611"></a><a name="p9476328153611"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p847672812361"><a name="p847672812361"></a><a name="p847672812361"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><div class="p" id="p19676154814477"><a name="p19676154814477"></a><a name="p19676154814477"></a>输入vcf文件的路径。<div class="note" id="note1080012315201"><a name="note1080012315201"></a><a name="note1080012315201"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p118011631132019"><a name="p118011631132019"></a><a name="p118011631132019"></a>vcf类型的文件后缀必须为“.vcf”，不支持“.g.vcf”类型。</p>
</div></div>
</div>
</td>
</tr>
<tr id="row8477328193612"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p16477152815366"><a name="p16477152815366"></a><a name="p16477152815366"></a>output</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p16477122823611"><a name="p16477122823611"></a><a name="p16477122823611"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p6477182853620"><a name="p6477182853620"></a><a name="p6477182853620"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p18477728173614"><a name="p18477728173614"></a><a name="p18477728173614"></a>输出vcf文件路径或存在的OBS文件夹路径。</p>
</td>
</tr>
<tr id="row184771028183617"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p1847712823618"><a name="p1847712823618"></a><a name="p1847712823618"></a>ref</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p34771828193615"><a name="p34771828193615"></a><a name="p34771828193615"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p847702863615"><a name="p847702863615"></a><a name="p847702863615"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p11477152863617"><a name="p11477152863617"></a><a name="p11477152863617"></a>参考基因库的文件。</p>
</td>
</tr>
<tr id="row113875567118"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p7387165671116"><a name="p7387165671116"></a><a name="p7387165671116"></a>select_type</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p11387195621110"><a name="p11387195621110"></a><a name="p11387195621110"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p1159104333311"><a name="p1159104333311"></a><a name="p1159104333311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p7387145631112"><a name="p7387145631112"></a><a name="p7387145631112"></a>选择需要包括的变异种类，可选类型包括：INDEL, SNP, MIXED, MNP, SYMBOLIC。</p>
</td>
</tr>
<tr id="row1811316545118"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p101137542114"><a name="p101137542114"></a><a name="p101137542114"></a>intervals</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p121131554161110"><a name="p121131554161110"></a><a name="p121131554161110"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p18251550348"><a name="p18251550348"></a><a name="p18251550348"></a>Array[String]</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p131132054111117"><a name="p131132054111117"></a><a name="p131132054111117"></a>interval文件。</p>
</td>
</tr>
<tr id="row15477828153615"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p174775286367"><a name="p174775286367"></a><a name="p174775286367"></a>conf</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p10477162833610"><a name="p10477162833610"></a><a name="p10477162833610"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p947716288367"><a name="p947716288367"></a><a name="p947716288367"></a>Map</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p8477142817362"><a name="p8477142817362"></a><a name="p8477142817362"></a>执行过程中业务相关的配置项，暂时未开放设置。</p>
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
        "input": "s3a://bucket/path/a.vcf", 
        "output": "s3a://bucket/dir/out.vcf",
        "ref": "hg38",
        "select_type": "SNP",
        "intervals": ["s3a://bucket/path/interval.bed"]
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


