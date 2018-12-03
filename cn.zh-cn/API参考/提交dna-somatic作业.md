# 提交dna-somatic作业<a name="dli_02_0153"></a>

## 功能介绍<a name="section13287428103611"></a>

创建、提交并执行体细胞突变检测作业。

## URI<a name="section52924285361"></a>

-   URI格式

    POST /v2.0/\{project\_id\}/gene/jobs

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
<table><thead align="left"><tr id="row6476182803617"><th class="cellrowborder" valign="top" width="20.31%" id="mcps1.2.5.1.1"><p id="p7476142811364"><a name="p7476142811364"></a><a name="p7476142811364"></a>参数名</p>
</th>
<th class="cellrowborder" valign="top" width="5.67%" id="mcps1.2.5.1.2"><p id="p16476102818360"><a name="p16476102818360"></a><a name="p16476102818360"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="14.67%" id="mcps1.2.5.1.3"><p id="p147652813365"><a name="p147652813365"></a><a name="p147652813365"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="59.35%" id="mcps1.2.5.1.4"><p id="p447622833612"><a name="p447622833612"></a><a name="p447622833612"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row11476132833616"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.1 "><p id="p0476152810369"><a name="p0476152810369"></a><a name="p0476152810369"></a>job_type</p>
</td>
<td class="cellrowborder" valign="top" width="5.67%" headers="mcps1.2.5.1.2 "><p id="p5476628133611"><a name="p5476628133611"></a><a name="p5476628133611"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.5.1.3 "><p id="p2476202818368"><a name="p2476202818368"></a><a name="p2476202818368"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.35%" headers="mcps1.2.5.1.4 "><p id="p11476162810366"><a name="p11476162810366"></a><a name="p11476162810366"></a>作业类型，对于DNA-Somatic作业为：<span class="parmvalue" id="parmvalue931133812598"><a name="parmvalue931133812598"></a><a name="parmvalue931133812598"></a><b>DNA_SOMATIC</b></span>。</p>
</td>
</tr>
<tr id="row17476828143615"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.1 "><p id="p19476162803619"><a name="p19476162803619"></a><a name="p19476162803619"></a>inputs</p>
</td>
<td class="cellrowborder" valign="top" width="5.67%" headers="mcps1.2.5.1.2 "><p id="p9476328153611"><a name="p9476328153611"></a><a name="p9476328153611"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.5.1.3 "><p id="p847672812361"><a name="p847672812361"></a><a name="p847672812361"></a>Array[SampleObject]</p>
</td>
<td class="cellrowborder" valign="top" width="59.35%" headers="mcps1.2.5.1.4 "><p id="p19676154814477"><a name="p19676154814477"></a><a name="p19676154814477"></a>输入文件列表，组详情可参照<a href="#dli_02_0153__table94842054488">表5</a>。</p>
</td>
</tr>
<tr id="row8477328193612"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.1 "><p id="p16477152815366"><a name="p16477152815366"></a><a name="p16477152815366"></a>output</p>
</td>
<td class="cellrowborder" valign="top" width="5.67%" headers="mcps1.2.5.1.2 "><p id="p16477122823611"><a name="p16477122823611"></a><a name="p16477122823611"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.5.1.3 "><p id="p6477182853620"><a name="p6477182853620"></a><a name="p6477182853620"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.35%" headers="mcps1.2.5.1.4 "><p id="p18477728173614"><a name="p18477728173614"></a><a name="p18477728173614"></a>输出文件路径。</p>
</td>
</tr>
<tr id="row1247712814367"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.1 "><p id="p1147712810366"><a name="p1147712810366"></a><a name="p1147712810366"></a>file_type</p>
</td>
<td class="cellrowborder" valign="top" width="5.67%" headers="mcps1.2.5.1.2 "><p id="p247752817366"><a name="p247752817366"></a><a name="p247752817366"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.5.1.3 "><p id="p54779288366"><a name="p54779288366"></a><a name="p54779288366"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.35%" headers="mcps1.2.5.1.4 "><p id="p5477142814363"><a name="p5477142814363"></a><a name="p5477142814363"></a>针对DNA类型的作业目前仅支持FASTQ和BAM两种类型的输入文件。</p>
</td>
</tr>
<tr id="row184771028183617"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.1 "><p id="p1847712823618"><a name="p1847712823618"></a><a name="p1847712823618"></a>ref</p>
</td>
<td class="cellrowborder" valign="top" width="5.67%" headers="mcps1.2.5.1.2 "><p id="p34771828193615"><a name="p34771828193615"></a><a name="p34771828193615"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.5.1.3 "><p id="p847702863615"><a name="p847702863615"></a><a name="p847702863615"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.35%" headers="mcps1.2.5.1.4 "><p id="p11477152863617"><a name="p11477152863617"></a><a name="p11477152863617"></a>参考基因库的文件。</p>
<div class="note" id="note1943417304916"><a name="note1943417304916"></a><a name="note1943417304916"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="p94345301911"><a name="p94345301911"></a><a name="p94345301911"></a>目前只支持hg38。</p>
</div></div>
</td>
</tr>
<tr id="row547752813615"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.1 "><p id="p192713232182"><a name="p192713232182"></a><a name="p192713232182"></a>tumor_sample_name</p>
</td>
<td class="cellrowborder" valign="top" width="5.67%" headers="mcps1.2.5.1.2 "><p id="p1526112351815"><a name="p1526112351815"></a><a name="p1526112351815"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.5.1.3 "><p id="p82516231187"><a name="p82516231187"></a><a name="p82516231187"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.35%" headers="mcps1.2.5.1.4 "><p id="p8237235187"><a name="p8237235187"></a><a name="p8237235187"></a>肿瘤样本的样本名。由英文字母、数字、下划线和中划线组成，长度为[1-128]个字符。</p>
</td>
</tr>
<tr id="row55101510217"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.1 "><p id="p1723620202110"><a name="p1723620202110"></a><a name="p1723620202110"></a>normal_sample_name</p>
</td>
<td class="cellrowborder" valign="top" width="5.67%" headers="mcps1.2.5.1.2 "><p id="p1325152092120"><a name="p1325152092120"></a><a name="p1325152092120"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.5.1.3 "><p id="p52852017217"><a name="p52852017217"></a><a name="p52852017217"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.35%" headers="mcps1.2.5.1.4 "><p id="p1031112082113"><a name="p1031112082113"></a><a name="p1031112082113"></a>正常样本的样本名。由英文字母、数字、下划线和中划线组成，长度为[1-128]个字符。</p>
<div class="note" id="note1106251131012"><a name="note1106251131012"></a><a name="note1106251131012"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="p161061651131011"><a name="p161061651131011"></a><a name="p161061651131011"></a>如果file_type指定为BAM时，该名称必须与BAM文件中的名称一致。</p>
</div></div>
</td>
</tr>
<tr id="row8841105712311"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.1 "><p id="p104771328123617"><a name="p104771328123617"></a><a name="p104771328123617"></a>knownsites</p>
</td>
<td class="cellrowborder" valign="top" width="5.67%" headers="mcps1.2.5.1.2 "><p id="p1347742816363"><a name="p1347742816363"></a><a name="p1347742816363"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.5.1.3 "><p id="p14477182893615"><a name="p14477182893615"></a><a name="p14477182893615"></a>Array[String]</p>
</td>
<td class="cellrowborder" valign="top" width="59.35%" headers="mcps1.2.5.1.4 "><p id="p5477142817365"><a name="p5477142817365"></a><a name="p5477142817365"></a>异常基因的比对文件列表，可以选择多个文件。具体请参考<a href="#dli_02_0153__table664016193569">表3</a>。</p>
</td>
</tr>
<tr id="row15477828153615"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.1 "><p id="p174775286367"><a name="p174775286367"></a><a name="p174775286367"></a>fastq_to_sam_conf</p>
</td>
<td class="cellrowborder" valign="top" width="5.67%" headers="mcps1.2.5.1.2 "><p id="p10477162833610"><a name="p10477162833610"></a><a name="p10477162833610"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.5.1.3 "><p id="p947716288367"><a name="p947716288367"></a><a name="p947716288367"></a>Array[String]</p>
</td>
<td class="cellrowborder" valign="top" width="59.35%" headers="mcps1.2.5.1.4 "><p id="p8477142817362"><a name="p8477142817362"></a><a name="p8477142817362"></a>执行FastqToSam过程中业务相关的配置项，用户可手动添加。具体可参考<a href="#dli_02_0153__table92006772114">表4</a>。</p>
</td>
</tr>
<tr id="row817763831811"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.1 "><p id="p7177113816182"><a name="p7177113816182"></a><a name="p7177113816182"></a>bwaspark_conf</p>
</td>
<td class="cellrowborder" valign="top" width="5.67%" headers="mcps1.2.5.1.2 "><p id="p1571062391915"><a name="p1571062391915"></a><a name="p1571062391915"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.5.1.3 "><p id="p147101123111919"><a name="p147101123111919"></a><a name="p147101123111919"></a>Array[String]</p>
</td>
<td class="cellrowborder" valign="top" width="59.35%" headers="mcps1.2.5.1.4 "><p id="p101771738171817"><a name="p101771738171817"></a><a name="p101771738171817"></a>执行GATK BwaSpark方法中业务相关的配置项，用户可手动添加。</p>
<div class="note" id="note27210135198"><a name="note27210135198"></a><a name="note27210135198"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="p1472211351914"><a name="p1472211351914"></a><a name="p1472211351914"></a>暂不支持关于输出文件格式以及输入输出路径相关的配置项。</p>
</div></div>
</td>
</tr>
<tr id="row46786415180"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.1 "><p id="p1667884171815"><a name="p1667884171815"></a><a name="p1667884171815"></a>read_pipeline_spark_conf</p>
</td>
<td class="cellrowborder" valign="top" width="5.67%" headers="mcps1.2.5.1.2 "><p id="p20913192461917"><a name="p20913192461917"></a><a name="p20913192461917"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.5.1.3 "><p id="p179136244192"><a name="p179136244192"></a><a name="p179136244192"></a>Array[String]</p>
</td>
<td class="cellrowborder" valign="top" width="59.35%" headers="mcps1.2.5.1.4 "><p id="p667810411184"><a name="p667810411184"></a><a name="p667810411184"></a>执行GATK ReadsPipelineSpark方法中业务相关的配置项，用户可手动添加。</p>
<div class="note" id="note1117473114185"><a name="note1117473114185"></a><a name="note1117473114185"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="p8174631161815"><a name="p8174631161815"></a><a name="p8174631161815"></a>暂不支持关于输出文件格式以及输入输出路径相关的配置项。</p>
</div></div>
</td>
</tr>
<tr id="row147081313227"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.1 "><p id="p619653517220"><a name="p619653517220"></a><a name="p619653517220"></a>intervals</p>
</td>
<td class="cellrowborder" valign="top" width="5.67%" headers="mcps1.2.5.1.2 "><p id="p9470161362216"><a name="p9470161362216"></a><a name="p9470161362216"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.5.1.3 "><p id="p18773165420226"><a name="p18773165420226"></a><a name="p18773165420226"></a>Array[String]</p>
</td>
<td class="cellrowborder" valign="top" width="59.35%" headers="mcps1.2.5.1.4 "><p id="p159923308235"><a name="p159923308235"></a><a name="p159923308235"></a>interval文件，目前仅支持 wgs_calling_regions.hg38.interval_list。</p>
</td>
</tr>
<tr id="row12711124515252"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.1 "><p id="p17131845172519"><a name="p17131845172519"></a><a name="p17131845172519"></a>pon</p>
</td>
<td class="cellrowborder" valign="top" width="5.67%" headers="mcps1.2.5.1.2 "><p id="p1571354512252"><a name="p1571354512252"></a><a name="p1571354512252"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.5.1.3 "><p id="p5713164542511"><a name="p5713164542511"></a><a name="p5713164542511"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.35%" headers="mcps1.2.5.1.4 "><p id="p193746227257"><a name="p193746227257"></a><a name="p193746227257"></a>panel of normals文件，目前仅支持 somatic-hg38-1000g_pon.hg38.vcf.gz。</p>
</td>
</tr>
<tr id="row2045418420480"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.1 "><p id="p1619835362518"><a name="p1619835362518"></a><a name="p1619835362518"></a>germline_resource</p>
</td>
<td class="cellrowborder" valign="top" width="5.67%" headers="mcps1.2.5.1.2 "><p id="p134691442104811"><a name="p134691442104811"></a><a name="p134691442104811"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.5.1.3 "><p id="p67148115275"><a name="p67148115275"></a><a name="p67148115275"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.35%" headers="mcps1.2.5.1.4 "><p id="p84691142124812"><a name="p84691142124812"></a><a name="p84691142124812"></a>生殖细胞突变的vcf文件，目前仅支持 somatic-hg38faf-only-gnomad.hg38.vcf.gz。</p>
</td>
</tr>
<tr id="row53355211292"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.1 "><p id="p933175212920"><a name="p933175212920"></a><a name="p933175212920"></a>mutect_is_export_bam</p>
</td>
<td class="cellrowborder" valign="top" width="5.67%" headers="mcps1.2.5.1.2 "><p id="p19335528293"><a name="p19335528293"></a><a name="p19335528293"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.5.1.3 "><p id="p1933165242917"><a name="p1933165242917"></a><a name="p1933165242917"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="59.35%" headers="mcps1.2.5.1.4 "><p id="p933135219292"><a name="p933135219292"></a><a name="p933135219292"></a>是否输出mutect2步骤生成的bam文件，默认值为false。</p>
</td>
</tr>
<tr id="row514821653111"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.1 "><p id="p7148916113114"><a name="p7148916113114"></a><a name="p7148916113114"></a>mutect_bam_output</p>
</td>
<td class="cellrowborder" valign="top" width="5.67%" headers="mcps1.2.5.1.2 "><p id="p1514801619313"><a name="p1514801619313"></a><a name="p1514801619313"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.5.1.3 "><p id="p3148141643110"><a name="p3148141643110"></a><a name="p3148141643110"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.35%" headers="mcps1.2.5.1.4 "><p id="p17817725203412"><a name="p17817725203412"></a><a name="p17817725203412"></a>mutect2输出bam文件路径。mutect_is_export_bam为true时必选，否则不需要设置。</p>
</td>
</tr>
<tr id="row163331512183616"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.1 "><p id="p4334712143620"><a name="p4334712143620"></a><a name="p4334712143620"></a>mutect_calls_variant</p>
</td>
<td class="cellrowborder" valign="top" width="5.67%" headers="mcps1.2.5.1.2 "><p id="p1033421253614"><a name="p1033421253614"></a><a name="p1033421253614"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.5.1.3 "><p id="p193349121361"><a name="p193349121361"></a><a name="p193349121361"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.35%" headers="mcps1.2.5.1.4 "><p id="p1533441213615"><a name="p1533441213615"></a><a name="p1533441213615"></a>突变频率库。</p>
<div class="note" id="note29888217134"><a name="note29888217134"></a><a name="note29888217134"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="p59888217135"><a name="p59888217135"></a><a name="p59888217135"></a>目前只支持small_exac_common_3.hg38.vcf.gz。</p>
</div></div>
</td>
</tr>
<tr id="row793018145363"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.1 "><p id="p209301141366"><a name="p209301141366"></a><a name="p209301141366"></a>is_filter_by_orientationBias</p>
</td>
<td class="cellrowborder" valign="top" width="5.67%" headers="mcps1.2.5.1.2 "><p id="p9930514133610"><a name="p9930514133610"></a><a name="p9930514133610"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.5.1.3 "><p id="p5930114113610"><a name="p5930114113610"></a><a name="p5930114113610"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="59.35%" headers="mcps1.2.5.1.4 "><p id="p1793081412365"><a name="p1793081412365"></a><a name="p1793081412365"></a>是否根据orientation bias过滤，默认值为false。</p>
</td>
</tr>
<tr id="row384611713610"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.1 "><p id="p1584618178361"><a name="p1584618178361"></a><a name="p1584618178361"></a>artifact_modes</p>
</td>
<td class="cellrowborder" valign="top" width="5.67%" headers="mcps1.2.5.1.2 "><p id="p3846151783613"><a name="p3846151783613"></a><a name="p3846151783613"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.5.1.3 "><p id="p79941243183814"><a name="p79941243183814"></a><a name="p79941243183814"></a>Array[String]</p>
</td>
<td class="cellrowborder" valign="top" width="59.35%" headers="mcps1.2.5.1.4 "><p id="p108461617113615"><a name="p108461617113615"></a><a name="p108461617113615"></a>filter_by_orientationBias步骤参数。</p>
</td>
</tr>
<tr id="row11166202362"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.1 "><p id="p8117152083612"><a name="p8117152083612"></a><a name="p8117152083612"></a>is_filter_by_alignmentArtifacts</p>
</td>
<td class="cellrowborder" valign="top" width="5.67%" headers="mcps1.2.5.1.2 "><p id="p1117420143619"><a name="p1117420143619"></a><a name="p1117420143619"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.5.1.3 "><p id="p161171520163615"><a name="p161171520163615"></a><a name="p161171520163615"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="59.35%" headers="mcps1.2.5.1.4 "><p id="p1111710207360"><a name="p1111710207360"></a><a name="p1111710207360"></a>是否根据alignment artifacts过滤，默认值为false。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  Knownsites种类

<a name="table664016193569"></a>
<table><thead align="left"><tr id="row1764051935610"><th class="cellrowborder" valign="top" width="15%" id="mcps1.2.3.1.1"><p id="p4640201911561"><a name="p4640201911561"></a><a name="p4640201911561"></a>基因库</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.2.3.1.2"><p id="p1064051965618"><a name="p1064051965618"></a><a name="p1064051965618"></a>基因库文件</p>
</th>
</tr>
</thead>
<tbody><tr id="row18672125216112"><td class="cellrowborder" rowspan="6" valign="top" width="15%" headers="mcps1.2.3.1.1 "><p id="p5672752512"><a name="p5672752512"></a><a name="p5672752512"></a>HG38</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.2.3.1.2 "><p id="p668092019216"><a name="p668092019216"></a><a name="p668092019216"></a>1000g_omni2.5.hg38.vcf</p>
</td>
</tr>
<tr id="row16072301997"><td class="cellrowborder" valign="top" headers="mcps1.2.3.1.1 "><p id="p160715301596"><a name="p160715301596"></a><a name="p160715301596"></a>1000g_phase1.snps.high_confidence.hg38.vcf</p>
</td>
</tr>
<tr id="row42432352910"><td class="cellrowborder" valign="top" headers="mcps1.2.3.1.1 "><p id="p1624312359914"><a name="p1624312359914"></a><a name="p1624312359914"></a>dbsnp_146.hg38.vcf</p>
</td>
</tr>
<tr id="row6827739995"><td class="cellrowborder" valign="top" headers="mcps1.2.3.1.1 "><p id="p128271393912"><a name="p128271393912"></a><a name="p128271393912"></a>hapmap_3.3.hg38.vcf</p>
</td>
</tr>
<tr id="row282783917917"><td class="cellrowborder" valign="top" headers="mcps1.2.3.1.1 "><p id="p482718397912"><a name="p482718397912"></a><a name="p482718397912"></a>homo_sapiens_assembly38.known_indels.vcf</p>
</td>
</tr>
<tr id="row1322916443910"><td class="cellrowborder" valign="top" headers="mcps1.2.3.1.1 "><p id="p122299446920"><a name="p122299446920"></a><a name="p122299446920"></a>mills_and_1000g_gold_standard.indels.hg38.vcf</p>
</td>
</tr>
</tbody>
</table>

**表 4**  fastq\_to\_sam\_conf配置项说明

<a name="table92006772114"></a>
<table><thead align="left"><tr id="row82157792119"><th class="cellrowborder" valign="top" width="18.9%" id="mcps1.2.4.1.1"><p id="p3886228142112"><a name="p3886228142112"></a><a name="p3886228142112"></a>配置项</p>
</th>
<th class="cellrowborder" valign="top" width="12.22%" id="mcps1.2.4.1.2"><p id="p128931028182119"><a name="p128931028182119"></a><a name="p128931028182119"></a>默认值</p>
</th>
<th class="cellrowborder" valign="top" width="68.88%" id="mcps1.2.4.1.3"><p id="p7897028172120"><a name="p7897028172120"></a><a name="p7897028172120"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1222812713216"><td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.1 "><p id="p1490174719313"><a name="p1490174719313"></a><a name="p1490174719313"></a>-RG</p>
</td>
<td class="cellrowborder" valign="top" width="12.22%" headers="mcps1.2.4.1.2 "><p id="p1094547123111"><a name="p1094547123111"></a><a name="p1094547123111"></a>A</p>
</td>
<td class="cellrowborder" valign="top" width="68.88%" headers="mcps1.2.4.1.3 "><p id="p209954733117"><a name="p209954733117"></a><a name="p209954733117"></a>读取组的名称。</p>
</td>
</tr>
<tr id="row5241475216"><td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.1 "><p id="p191031447103118"><a name="p191031447103118"></a><a name="p191031447103118"></a>-SM</p>
</td>
<td class="cellrowborder" valign="top" width="12.22%" headers="mcps1.2.4.1.2 "><p id="p13105114723115"><a name="p13105114723115"></a><a name="p13105114723115"></a>SM1</p>
</td>
<td class="cellrowborder" valign="top" width="68.88%" headers="mcps1.2.4.1.3 "><p id="p201091447123115"><a name="p201091447123115"></a><a name="p201091447123115"></a>样本名称，将写入BAM文件头中。</p>
</td>
</tr>
<tr id="row161761126103111"><td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.1 "><p id="p3111184793110"><a name="p3111184793110"></a><a name="p3111184793110"></a>-PL</p>
</td>
<td class="cellrowborder" valign="top" width="12.22%" headers="mcps1.2.4.1.2 "><p id="p12113184716312"><a name="p12113184716312"></a><a name="p12113184716312"></a>illumina</p>
</td>
<td class="cellrowborder" valign="top" width="68.88%" headers="mcps1.2.4.1.3 "><p id="p1311624773115"><a name="p1311624773115"></a><a name="p1311624773115"></a>平台类型，将写入BAM文件头中。</p>
</td>
</tr>
<tr id="row1717792618317"><td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.1 "><p id="p712119476316"><a name="p712119476316"></a><a name="p712119476316"></a>-SO</p>
</td>
<td class="cellrowborder" valign="top" width="12.22%" headers="mcps1.2.4.1.2 "><p id="p1712314713116"><a name="p1712314713116"></a><a name="p1712314713116"></a>queryname</p>
</td>
<td class="cellrowborder" valign="top" width="68.88%" headers="mcps1.2.4.1.3 "><p id="p21268472318"><a name="p21268472318"></a><a name="p21268472318"></a>BAM文件的排序方式。</p>
</td>
</tr>
<tr id="row77001731123120"><td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.1 "><p id="p613115471311"><a name="p613115471311"></a><a name="p613115471311"></a>-MR</p>
</td>
<td class="cellrowborder" valign="top" width="12.22%" headers="mcps1.2.4.1.2 "><p id="p2135174711315"><a name="p2135174711315"></a><a name="p2135174711315"></a>200000</p>
</td>
<td class="cellrowborder" valign="top" width="68.88%" headers="mcps1.2.4.1.3 "><p id="p61391947163116"><a name="p61391947163116"></a><a name="p61391947163116"></a>每个BAM文件中包含的记录数。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  SampleObject信息

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
<tbody><tr id="row34931654382"><td class="cellrowborder" valign="top" width="14.141414141414144%" headers="mcps1.2.5.1.1 "><p id="p04931154780"><a name="p04931154780"></a><a name="p04931154780"></a>sample_type</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p049512541980"><a name="p049512541980"></a><a name="p049512541980"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="15.151515151515152%" headers="mcps1.2.5.1.3 "><p id="p1949618541685"><a name="p1949618541685"></a><a name="p1949618541685"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="62.62626262626263%" headers="mcps1.2.5.1.4 "><p id="p17207123717190"><a name="p17207123717190"></a><a name="p17207123717190"></a>样本类型。仅支持 tumor 和 normal 两种类型。</p>
</td>
</tr>
<tr id="row549635412811"><td class="cellrowborder" valign="top" width="14.141414141414144%" headers="mcps1.2.5.1.1 "><p id="p1549715417817"><a name="p1549715417817"></a><a name="p1549715417817"></a>sample_inputs</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p749917544814"><a name="p749917544814"></a><a name="p749917544814"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="15.151515151515152%" headers="mcps1.2.5.1.3 "><p id="p10499754485"><a name="p10499754485"></a><a name="p10499754485"></a>Array[String]</p>
</td>
<td class="cellrowborder" valign="top" width="62.62626262626263%" headers="mcps1.2.5.1.4 "><a name="ul941712599472"></a><a name="ul941712599472"></a><ul id="ul941712599472"><li>当输入文件类型为FASTQ时，必须有两个输入文件。<div class="note" id="note1080012315201"><a name="note1080012315201"></a><a name="note1080012315201"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="p118011631132019"><a name="p118011631132019"></a><a name="p118011631132019"></a>FASTQ类型的文件后缀必须为“.fastq”，“.fq”，“.fastq.gz”和“.fq.gz”这四种中的一种。</p>
</div></div>
</li><li>当输入文件类型为BAM时，只能有一个输入文件。<div class="note" id="note1699419591189"><a name="note1699419591189"></a><a name="note1699419591189"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="p5994135961818"><a name="p5994135961818"></a><a name="p5994135961818"></a>文件类型为BAM时，必须提供BQSR比对之后的BAM文件。</p>
</div></div>
</li></ul>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="section134515287360"></a>

-   返回码

    201


-   响应参数

**表 6**  响应参数

<a name="table8348112818368"></a>
<table><thead align="left"><tr id="row11478132863610"><th class="cellrowborder" valign="top" width="29.409999999999997%" id="mcps1.2.4.1.1"><p id="p04782028173616"><a name="p04782028173616"></a><a name="p04782028173616"></a>参数名</p>
</th>
<th class="cellrowborder" valign="top" width="17.65%" id="mcps1.2.4.1.2"><p id="p34781128193612"><a name="p34781128193612"></a><a name="p34781128193612"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="52.94%" id="mcps1.2.4.1.3"><p id="p1347917286364"><a name="p1347917286364"></a><a name="p1347917286364"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row18479182813362"><td class="cellrowborder" valign="top" width="29.409999999999997%" headers="mcps1.2.4.1.1 "><p id="p12479202810367"><a name="p12479202810367"></a><a name="p12479202810367"></a>job_id</p>
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
    "job_type": "DNA_SOMATIC",
        "inputs" : [
           {
              "sample_type": "tumor",
              "sample_inputs": ["s3a://genes/somatic/tumor_1.fastq.gz", "s3a://genes/somatic/tumor_2.fastq.gz"]
           },
          {
              "sample_type": "normal",
              "sample_inputs": ["s3a://genes/somatic/normal_1.fastq.gz", "s3a://genes/somatic/normal_2.fastq.gz"]
           }
        ],
        "file_type": "fastq",
        "output": "s3a://genes/somatic/out.vcf",
        "ref": "hg38",
        "tumor_sample_name": "HCC1143_tumor",
        "normal_sample_name": "HCC1143_normal",
        "knownsites": ["1000g_omni2.5.hg38.vcf"],
        "intervals": ["wgs_calling_regions.hg38.interval_list"],
        "pon": "somatic-hg38-1000g_pon.hg38.vcf.gz",
        "germline_resource": "somatic-hg38faf-only-gnomad.hg38.vcf.gz",
        "mutect_is_export_bam": false,
        "mutect_calls_variant": "small_exac_common_3.hg38.vcf.gz",
        "is_filter_by_orientationBias": false,
        "artifact_modes": ["G/T"],
        "is_filter_by_alignmentArtifacts": false
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


