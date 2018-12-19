# 提交dna-germline作业<a name="dli_02_0140"></a>

## 功能介绍<a name="section13287428103611"></a>

创建、提交并执行基因作业。

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
<table><thead align="left"><tr id="row6476182803617"><th class="cellrowborder" valign="top" width="14.000000000000002%" id="mcps1.2.5.1.1"><p id="p7476142811364"><a name="p7476142811364"></a><a name="p7476142811364"></a>参数名</p>
</th>
<th class="cellrowborder" valign="top" width="9%" id="mcps1.2.5.1.2"><p id="p16476102818360"><a name="p16476102818360"></a><a name="p16476102818360"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="11.25%" id="mcps1.2.5.1.3"><p id="p147652813365"><a name="p147652813365"></a><a name="p147652813365"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="65.75%" id="mcps1.2.5.1.4"><p id="p447622833612"><a name="p447622833612"></a><a name="p447622833612"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row11476132833616"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p0476152810369"><a name="p0476152810369"></a><a name="p0476152810369"></a>job_type</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p5476628133611"><a name="p5476628133611"></a><a name="p5476628133611"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="11.25%" headers="mcps1.2.5.1.3 "><p id="p2476202818368"><a name="p2476202818368"></a><a name="p2476202818368"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="65.75%" headers="mcps1.2.5.1.4 "><p id="p11476162810366"><a name="p11476162810366"></a><a name="p11476162810366"></a>作业类型，对于DNA-Germline作业为：<span class="parmvalue" id="parmvalue931133812598"><a name="parmvalue931133812598"></a><a name="parmvalue931133812598"></a>“DNA_GERMLINE”</span>。</p>
</td>
</tr>
<tr id="row17476828143615"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p19476162803619"><a name="p19476162803619"></a><a name="p19476162803619"></a>input</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p9476328153611"><a name="p9476328153611"></a><a name="p9476328153611"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="11.25%" headers="mcps1.2.5.1.3 "><p id="p847672812361"><a name="p847672812361"></a><a name="p847672812361"></a>Array[String]</p>
</td>
<td class="cellrowborder" valign="top" width="65.75%" headers="mcps1.2.5.1.4 "><p id="p19676154814477"><a name="p19676154814477"></a><a name="p19676154814477"></a>输入文件的路径。</p>
<a name="ul941712599472"></a><a name="ul941712599472"></a><ul id="ul941712599472"><li>当输入文件类型为FASTQ时，必须有两个输入文件。<div class="note" id="note1080012315201"><a name="note1080012315201"></a><a name="note1080012315201"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p118011631132019"><a name="p118011631132019"></a><a name="p118011631132019"></a>FASTQ类型的文件后缀必须为“.fastq”，“.fq”，“.fastq.gz”和“.fq.gz”这四种中的一种。</p>
</div></div>
</li><li>当输入文件类型为BAM时，只能有一个输入文件。</li></ul>
</td>
</tr>
<tr id="row8477328193612"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p16477152815366"><a name="p16477152815366"></a><a name="p16477152815366"></a>output</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p16477122823611"><a name="p16477122823611"></a><a name="p16477122823611"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="11.25%" headers="mcps1.2.5.1.3 "><p id="p6477182853620"><a name="p6477182853620"></a><a name="p6477182853620"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="65.75%" headers="mcps1.2.5.1.4 "><p id="p18477728173614"><a name="p18477728173614"></a><a name="p18477728173614"></a>输出文件路径。</p>
</td>
</tr>
<tr id="row1247712814367"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p1147712810366"><a name="p1147712810366"></a><a name="p1147712810366"></a>file_type</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p247752817366"><a name="p247752817366"></a><a name="p247752817366"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="11.25%" headers="mcps1.2.5.1.3 "><p id="p54779288366"><a name="p54779288366"></a><a name="p54779288366"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="65.75%" headers="mcps1.2.5.1.4 "><p id="p5477142814363"><a name="p5477142814363"></a><a name="p5477142814363"></a>针对DNA类型的作业目前仅支持FASTQ和BAM两种类型的输入文件。</p>
</td>
</tr>
<tr id="row184771028183617"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p1847712823618"><a name="p1847712823618"></a><a name="p1847712823618"></a>ref</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p34771828193615"><a name="p34771828193615"></a><a name="p34771828193615"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="11.25%" headers="mcps1.2.5.1.3 "><p id="p847702863615"><a name="p847702863615"></a><a name="p847702863615"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="65.75%" headers="mcps1.2.5.1.4 "><p id="p11477152863617"><a name="p11477152863617"></a><a name="p11477152863617"></a>参考基因库的文件。</p>
</td>
</tr>
<tr id="row547752813615"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p104771328123617"><a name="p104771328123617"></a><a name="p104771328123617"></a>knownsites</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p1347742816363"><a name="p1347742816363"></a><a name="p1347742816363"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="11.25%" headers="mcps1.2.5.1.3 "><p id="p14477182893615"><a name="p14477182893615"></a><a name="p14477182893615"></a>Array[String]</p>
</td>
<td class="cellrowborder" valign="top" width="65.75%" headers="mcps1.2.5.1.4 "><p id="p5477142817365"><a name="p5477142817365"></a><a name="p5477142817365"></a>异常基因的比对文件列表，可以选择多个文件。具体请参考<a href="#table664016193569">表3</a>。</p>
</td>
</tr>
<tr id="row8841105712311"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p1084217579320"><a name="p1084217579320"></a><a name="p1084217579320"></a>engine</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p1084212571316"><a name="p1084212571316"></a><a name="p1084212571316"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.25%" headers="mcps1.2.5.1.3 "><p id="p17842125713312"><a name="p17842125713312"></a><a name="p17842125713312"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="65.75%" headers="mcps1.2.5.1.4 "><p id="p984225716318"><a name="p984225716318"></a><a name="p984225716318"></a>计算引擎，支持gatk和tensorflow两种，默认为gatk。其中，tensorflow计算引擎利用深度学习模型进行变异检测，相较于gatk具有更高准确率，当前仅支持排过序并且建立好索引的bam类型输入。</p>
</td>
</tr>
<tr id="row15477828153615"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p174775286367"><a name="p174775286367"></a><a name="p174775286367"></a>fastq_to_sam_conf</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p10477162833610"><a name="p10477162833610"></a><a name="p10477162833610"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.25%" headers="mcps1.2.5.1.3 "><p id="p947716288367"><a name="p947716288367"></a><a name="p947716288367"></a>Array[String]</p>
</td>
<td class="cellrowborder" valign="top" width="65.75%" headers="mcps1.2.5.1.4 "><p id="p8477142817362"><a name="p8477142817362"></a><a name="p8477142817362"></a>执行FastqToSam方法时业务相关的配置项，用户可手动添加。具体可参考<a href="#table56408147518">表4</a>。</p>
<div class="note" id="note15644147192311"><a name="note15644147192311"></a><a name="note15644147192311"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p464614719234"><a name="p464614719234"></a><a name="p464614719234"></a>当engine选择tensorflow时，不支持该配置项。</p>
</div></div>
</td>
</tr>
<tr id="row817763831811"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p7177113816182"><a name="p7177113816182"></a><a name="p7177113816182"></a>bwaspark_conf</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p1571062391915"><a name="p1571062391915"></a><a name="p1571062391915"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.25%" headers="mcps1.2.5.1.3 "><p id="p147101123111919"><a name="p147101123111919"></a><a name="p147101123111919"></a>Array[String]</p>
</td>
<td class="cellrowborder" valign="top" width="65.75%" headers="mcps1.2.5.1.4 "><p id="p101771738171817"><a name="p101771738171817"></a><a name="p101771738171817"></a>执行GATK BwaSpark方法时业务相关的配置项，用户可手动添加。</p>
<div class="note" id="note621205716240"><a name="note621205716240"></a><a name="note621205716240"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul398444762520"></a><a name="ul398444762520"></a><ul id="ul398444762520"><li>暂不支持关于输出文件格式以及输入输出路径相关的配置项。</li><li>当engine选择tensorflow时，不支持该配置项。</li></ul>
</div></div>
</td>
</tr>
<tr id="row46786415180"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p1667884171815"><a name="p1667884171815"></a><a name="p1667884171815"></a>read_pipeline_spark_conf</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p20913192461917"><a name="p20913192461917"></a><a name="p20913192461917"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.25%" headers="mcps1.2.5.1.3 "><p id="p179136244192"><a name="p179136244192"></a><a name="p179136244192"></a>Array[String]</p>
</td>
<td class="cellrowborder" valign="top" width="65.75%" headers="mcps1.2.5.1.4 "><p id="p667810411184"><a name="p667810411184"></a><a name="p667810411184"></a>执行GATK ReadsPipelineSpark方法时业务相关的配置项，用户可手动添加。</p>
<div class="note" id="note1741981116265"><a name="note1741981116265"></a><a name="note1741981116265"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul2211123910263"></a><a name="ul2211123910263"></a><ul id="ul2211123910263"><li>暂不支持关于输出文件格式以及输入输出路径相关的配置项。</li><li>当engine选择tensorflow时，不支持该配置项。</li></ul>
</div></div>
</td>
</tr>
<tr id="row147081313227"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p16470111322213"><a name="p16470111322213"></a><a name="p16470111322213"></a>is_export_bam</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p9470161362216"><a name="p9470161362216"></a><a name="p9470161362216"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.25%" headers="mcps1.2.5.1.3 "><p id="p347010135226"><a name="p347010135226"></a><a name="p347010135226"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="65.75%" headers="mcps1.2.5.1.4 "><p id="p1247071320224"><a name="p1247071320224"></a><a name="p1247071320224"></a>是否导出BQSR bam文件，默认值为false。</p>
<div class="note" id="note5441919102715"><a name="note5441919102715"></a><a name="note5441919102715"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p2044619152714"><a name="p2044619152714"></a><a name="p2044619152714"></a>当engine选择tensorflow时，不支持导出BQSR bam文件。</p>
</div></div>
</td>
</tr>
<tr id="row12711124515252"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p17131845172519"><a name="p17131845172519"></a><a name="p17131845172519"></a>bam_output</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p1571354512252"><a name="p1571354512252"></a><a name="p1571354512252"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.25%" headers="mcps1.2.5.1.3 "><p id="p5713164542511"><a name="p5713164542511"></a><a name="p5713164542511"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="65.75%" headers="mcps1.2.5.1.4 "><p id="p57131455250"><a name="p57131455250"></a><a name="p57131455250"></a>中间BAQSR bam文件输出路径，若<span class="parmname" id="parmname46303611408"><a name="parmname46303611408"></a><a name="parmname46303611408"></a>“is_export_bam”</span>为<span class="parmvalue" id="parmvalue1382714015407"><a name="parmvalue1382714015407"></a><a name="parmvalue1382714015407"></a>“true”</span>，该参数为必选。</p>
</td>
</tr>
<tr id="row2045418420480"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.1 "><p id="p1046924213485"><a name="p1046924213485"></a><a name="p1046924213485"></a>is_output_gvcf</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p134691442104811"><a name="p134691442104811"></a><a name="p134691442104811"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.25%" headers="mcps1.2.5.1.3 "><p id="p1246914211489"><a name="p1246914211489"></a><a name="p1246914211489"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="65.75%" headers="mcps1.2.5.1.4 "><p id="p84691142124812"><a name="p84691142124812"></a><a name="p84691142124812"></a>输出文件格式是否为GVCF，默认值为“false”。设置为“true”时，输出文件的路径必须是已经存在的OBS目录或者是以g.vcf为后缀的文件名。</p>
<div class="note" id="note52174062416"><a name="note52174062416"></a><a name="note52174062416"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p321440192418"><a name="p321440192418"></a><a name="p321440192418"></a>当engine选择tensorflow时，不支持导出GVCF文件。</p>
</div></div>
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
<tbody><tr id="row156401219145620"><td class="cellrowborder" rowspan="7" valign="top" width="15%" headers="mcps1.2.3.1.1 "><p id="p176401191567"><a name="p176401191567"></a><a name="p176401191567"></a>HG19</p>
<p id="p161292611818"><a name="p161292611818"></a><a name="p161292611818"></a></p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.2.3.1.2 "><p id="p29871058972"><a name="p29871058972"></a><a name="p29871058972"></a>1000g_phase1.indels.hg19.sites.vcf</p>
</td>
</tr>
<tr id="row546216511718"><td class="cellrowborder" valign="top" headers="mcps1.2.3.1.1 "><p id="p174639510713"><a name="p174639510713"></a><a name="p174639510713"></a>dbsnp_138.hg19.vcf</p>
</td>
</tr>
<tr id="row4189171911812"><td class="cellrowborder" valign="top" headers="mcps1.2.3.1.1 "><p id="p10189219983"><a name="p10189219983"></a><a name="p10189219983"></a>1000g_omni2.5.hg19.sites.vcf</p>
</td>
</tr>
<tr id="row1719114269817"><td class="cellrowborder" valign="top" headers="mcps1.2.3.1.1 "><p id="p17191162611817"><a name="p17191162611817"></a><a name="p17191162611817"></a>1000g_phase1.snps.high_confidence.hg19.sites.vcf</p>
</td>
</tr>
<tr id="row2019117261981"><td class="cellrowborder" valign="top" headers="mcps1.2.3.1.1 "><p id="p1619182610812"><a name="p1619182610812"></a><a name="p1619182610812"></a>mills_and_1000g_gold_standard.indels.hg19.sites.vcf</p>
</td>
</tr>
<tr id="row93998494814"><td class="cellrowborder" valign="top" headers="mcps1.2.3.1.1 "><p id="p1539984917814"><a name="p1539984917814"></a><a name="p1539984917814"></a>hapmap_3.3.hg19.sites.vcf</p>
</td>
</tr>
<tr id="row20129161812"><td class="cellrowborder" valign="top" headers="mcps1.2.3.1.1 "><p id="p21291564811"><a name="p21291564811"></a><a name="p21291564811"></a>ncbi.hg19_dbsnp147.vcf</p>
</td>
</tr>
<tr id="row18672125216112"><td class="cellrowborder" rowspan="6" valign="top" width="15%" headers="mcps1.2.3.1.1 "><p id="p5672752512"><a name="p5672752512"></a><a name="p5672752512"></a>HG38</p>
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

<a name="table56408147518"></a>
<table><tbody><tr id="row369211419518"><td class="cellrowborder" valign="top" width="14.000000000000002%"><p id="p116921414859"><a name="p116921414859"></a><a name="p116921414859"></a>配置项</p>
</td>
<td class="cellrowborder" valign="top" width="18%"><p id="p176922143515"><a name="p176922143515"></a><a name="p176922143515"></a>默认值</p>
</td>
<td class="cellrowborder" valign="top" width="68%"><p id="p1369219141052"><a name="p1369219141052"></a><a name="p1369219141052"></a>说明</p>
</td>
</tr>
<tr id="row56921141155"><td class="cellrowborder" valign="top" width="14.000000000000002%"><p id="p176921714958"><a name="p176921714958"></a><a name="p176921714958"></a>-RG</p>
</td>
<td class="cellrowborder" valign="top" width="18%"><p id="p17692814450"><a name="p17692814450"></a><a name="p17692814450"></a>A</p>
</td>
<td class="cellrowborder" valign="top" width="68%"><p id="p66921214652"><a name="p66921214652"></a><a name="p66921214652"></a>读取组的名称。</p>
</td>
</tr>
<tr id="row14692171417512"><td class="cellrowborder" valign="top" width="14.000000000000002%"><p id="p16692161420511"><a name="p16692161420511"></a><a name="p16692161420511"></a>-SM</p>
</td>
<td class="cellrowborder" valign="top" width="18%"><p id="p669201411510"><a name="p669201411510"></a><a name="p669201411510"></a>SM1</p>
</td>
<td class="cellrowborder" valign="top" width="68%"><p id="p36926141252"><a name="p36926141252"></a><a name="p36926141252"></a>样本名称，将写入BAM文件头中。</p>
</td>
</tr>
<tr id="row36921114658"><td class="cellrowborder" valign="top" width="14.000000000000002%"><p id="p969220141753"><a name="p969220141753"></a><a name="p969220141753"></a>-PL</p>
</td>
<td class="cellrowborder" valign="top" width="18%"><p id="p769212141955"><a name="p769212141955"></a><a name="p769212141955"></a>illumina</p>
</td>
<td class="cellrowborder" valign="top" width="68%"><p id="p10692191412514"><a name="p10692191412514"></a><a name="p10692191412514"></a>平台类型，将写入BAM文件头中。</p>
</td>
</tr>
<tr id="row16692214859"><td class="cellrowborder" valign="top" width="14.000000000000002%"><p id="p206927143517"><a name="p206927143517"></a><a name="p206927143517"></a>-SO</p>
</td>
<td class="cellrowborder" valign="top" width="18%"><p id="p269213147514"><a name="p269213147514"></a><a name="p269213147514"></a>queryname</p>
</td>
<td class="cellrowborder" valign="top" width="68%"><p id="p1769211419515"><a name="p1769211419515"></a><a name="p1769211419515"></a>BAM文件的排序方式。</p>
</td>
</tr>
<tr id="row19692141419511"><td class="cellrowborder" valign="top" width="14.000000000000002%"><p id="p1269212142510"><a name="p1269212142510"></a><a name="p1269212142510"></a>-MR</p>
</td>
<td class="cellrowborder" valign="top" width="18%"><p id="p166921914058"><a name="p166921914058"></a><a name="p166921914058"></a>200000</p>
</td>
<td class="cellrowborder" valign="top" width="68%"><p id="p1269218141759"><a name="p1269218141759"></a><a name="p1269218141759"></a>每个BAM文件中包含的记录数。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="section134515287360"></a>

-   返回码

    201


-   响应参数

**表 5**  响应参数

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

## 示例-<a name="section910624615450"></a>

-   请求样例：

    ```
    {  
        "job_type": "DNA_GERMLINE",
        "input": ["s3a://bucket/path/a_1.fastq.gz", "s3a://bucket/path/a_2.fastq.gz"],
        "output": "s3a://bucket/dir/out.vcf",
        "file_type": "FASTQ",
        "ref": "hg38",
        "knownsites": ["1000g_omni2.5.hg38.vcf"],
        "fastq_to_sam_conf": ["-PL", "illumina", "-SM", "SM1", "-MR", "2000000"],
        "bwaspark_conf": ["--bam-output", "s3a://bucket/bamfile.bam"],
        "read_pipeline_spark_conf": ["--emit-ref-confidence", "GVCF"]
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


