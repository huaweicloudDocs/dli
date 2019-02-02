# 查询select-variants作业<a name="dli_02_0148"></a>

## 功能介绍<a name="section6968756197"></a>

查询所有已经提交的select-variants作业的信息，包括作业状态、运行时间等。

## URI<a name="section169693561590"></a>

-   URI格式

    GET /v2.0/\{project\_id\}/gene/tools/select-variants?limit=limit&offset=offset&start=start\_time&end=end\_time

-   参数说明

    **表 1**  URI参数

    <a name="table129761556598"></a>
    <table><thead align="left"><tr id="row1826735713913"><th class="cellrowborder" valign="top" width="11.252525252525253%" id="mcps1.2.4.1.1"><p id="p226717571598"><a name="p226717571598"></a><a name="p226717571598"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="8.535353535353536%" id="mcps1.2.4.1.2"><p id="p8267195712917"><a name="p8267195712917"></a><a name="p8267195712917"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="80.21212121212122%" id="mcps1.2.4.1.3"><p id="p11267457995"><a name="p11267457995"></a><a name="p11267457995"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1026714572915"><td class="cellrowborder" valign="top" width="11.252525252525253%" headers="mcps1.2.4.1.1 "><p id="p17267757296"><a name="p17267757296"></a><a name="p17267757296"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.535353535353536%" headers="mcps1.2.4.1.2 "><p id="p14267557694"><a name="p14267557694"></a><a name="p14267557694"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="80.21212121212122%" headers="mcps1.2.4.1.3 "><p id="p82675571912"><a name="p82675571912"></a><a name="p82675571912"></a>项目编号。</p>
    </td>
    </tr>
    <tr id="row1226716573912"><td class="cellrowborder" valign="top" width="11.252525252525253%" headers="mcps1.2.4.1.1 "><p id="p1826713571397"><a name="p1826713571397"></a><a name="p1826713571397"></a>limit</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.535353535353536%" headers="mcps1.2.4.1.2 "><p id="p1026795710912"><a name="p1026795710912"></a><a name="p1026795710912"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="80.21212121212122%" headers="mcps1.2.4.1.3 "><p id="p22671457796"><a name="p22671457796"></a><a name="p22671457796"></a>每页显示作业记录的条数，范围: [1, 100]，默认值：10。</p>
    </td>
    </tr>
    <tr id="row1426711571890"><td class="cellrowborder" valign="top" width="11.252525252525253%" headers="mcps1.2.4.1.1 "><p id="p8267357993"><a name="p8267357993"></a><a name="p8267357993"></a>offset</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.535353535353536%" headers="mcps1.2.4.1.2 "><p id="p132678578917"><a name="p132678578917"></a><a name="p132678578917"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="80.21212121212122%" headers="mcps1.2.4.1.3 "><p id="p2268155713918"><a name="p2268155713918"></a><a name="p2268155713918"></a>作业记录查询的偏移量，计算方式：limit * (待查询的页码 -1)。例如，设定limit=10，则查看第一页作业记录的offset=0，表示没有偏移量；查看第二页作业记录的offset=10，表示当前作业记录的偏移量为10，即从第11条记录开始查看；以此类推。默认值：0。</p>
    </td>
    </tr>
    <tr id="row1826855715912"><td class="cellrowborder" valign="top" width="11.252525252525253%" headers="mcps1.2.4.1.1 "><p id="p192681657995"><a name="p192681657995"></a><a name="p192681657995"></a>start</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.535353535353536%" headers="mcps1.2.4.1.2 "><p id="p22680574914"><a name="p22680574914"></a><a name="p22680574914"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="80.21212121212122%" headers="mcps1.2.4.1.3 "><p id="p172681157494"><a name="p172681157494"></a><a name="p172681157494"></a>用于查询开始时间在该时间点之后的作业。时间格式为unix时间戳，单位：毫秒。</p>
    </td>
    </tr>
    <tr id="row22682057196"><td class="cellrowborder" valign="top" width="11.252525252525253%" headers="mcps1.2.4.1.1 "><p id="p132686579919"><a name="p132686579919"></a><a name="p132686579919"></a>end</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.535353535353536%" headers="mcps1.2.4.1.2 "><p id="p112689571297"><a name="p112689571297"></a><a name="p112689571297"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="80.21212121212122%" headers="mcps1.2.4.1.3 "><p id="p1426817576910"><a name="p1426817576910"></a><a name="p1426817576910"></a>用于查询开始时间在该时间点之前的作业。时间格式为unix时间戳，单位：毫秒。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="section3414034164017"></a>

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
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p17797847195112"><a name="p17797847195112"></a><a name="p17797847195112"></a>输出vcf文件路径或存在的OBS文件夹路径。</p>
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
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p38151847135110"><a name="p38151847135110"></a><a name="p38151847135110"></a>Array[String]</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p08161547165113"><a name="p08161547165113"></a><a name="p08161547165113"></a>interval文件。</p>
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

## 响应消息<a name="section2101574914"></a>

-   返回码

    200

-   响应参数

**表 3**  响应参数

<a name="table192695719914"></a>
<table><thead align="left"><tr id="row82696574918"><th class="cellrowborder" valign="top" width="15.120000000000001%" id="mcps1.2.4.1.1"><p id="p102691857892"><a name="p102691857892"></a><a name="p102691857892"></a>参数名</p>
</th>
<th class="cellrowborder" valign="top" width="12.790000000000001%" id="mcps1.2.4.1.2"><p id="p12269185711914"><a name="p12269185711914"></a><a name="p12269185711914"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="72.09%" id="mcps1.2.4.1.3"><p id="p192698571294"><a name="p192698571294"></a><a name="p192698571294"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row5269257198"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p1226915571998"><a name="p1226915571998"></a><a name="p1226915571998"></a>count</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p1726911578913"><a name="p1726911578913"></a><a name="p1726911578913"></a>int</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p527011570915"><a name="p527011570915"></a><a name="p527011570915"></a>返回的作业个数。</p>
</td>
</tr>
<tr id="row89762011203411"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p109761711113420"><a name="p109761711113420"></a><a name="p109761711113420"></a>instances</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p19976101143410"><a name="p19976101143410"></a><a name="p19976101143410"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p4976111183419"><a name="p4976111183419"></a><a name="p4976111183419"></a>具体请参考<a href="#table1066213340337">表4</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  select-variant参数

<a name="table1066213340337"></a>
<table><thead align="left"><tr id="row1966683414337"><th class="cellrowborder" valign="top" width="15.120000000000001%" id="mcps1.2.4.1.1"><p id="p466873416331"><a name="p466873416331"></a><a name="p466873416331"></a>参数名</p>
</th>
<th class="cellrowborder" valign="top" width="12.790000000000001%" id="mcps1.2.4.1.2"><p id="p766812345333"><a name="p766812345333"></a><a name="p766812345333"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="72.09%" id="mcps1.2.4.1.3"><p id="p1669193412333"><a name="p1669193412333"></a><a name="p1669193412333"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1167516342336"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p15677193417334"><a name="p15677193417334"></a><a name="p15677193417334"></a>instance_id</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p367743414333"><a name="p367743414333"></a><a name="p367743414333"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p967823493319"><a name="p967823493319"></a><a name="p967823493319"></a>select-variants作业的唯一ID。</p>
</td>
</tr>
<tr id="row368312346331"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p1968353413316"><a name="p1968353413316"></a><a name="p1968353413316"></a>owner</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p96841349338"><a name="p96841349338"></a><a name="p96841349338"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p146851234133312"><a name="p146851234133312"></a><a name="p146851234133312"></a>提交该作业的用户名。</p>
</td>
</tr>
<tr id="row10685123433312"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p13687103417339"><a name="p13687103417339"></a><a name="p13687103417339"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p12687934153313"><a name="p12687934153313"></a><a name="p12687934153313"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p14689183493310"><a name="p14689183493310"></a><a name="p14689183493310"></a>作业当前状态，包含提交中（LAUNCHING）、运行中（RUNNING）、已完成（FINISHED）、已失败（FAILED）、已删除（DELETED），未知异常（UNKNOWN）。</p>
</td>
</tr>
<tr id="row136941349334"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p1169493413319"><a name="p1169493413319"></a><a name="p1169493413319"></a>start_time</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p1695113410330"><a name="p1695113410330"></a><a name="p1695113410330"></a>Timestamp</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p669503417331"><a name="p669503417331"></a><a name="p669503417331"></a>作业开始的时间。</p>
</td>
</tr>
<tr id="row969673423316"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p106971534183316"><a name="p106971534183316"></a><a name="p106971534183316"></a>duration</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p76986349336"><a name="p76986349336"></a><a name="p76986349336"></a>Long</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p27001334113310"><a name="p27001334113310"></a><a name="p27001334113310"></a>作业执行的时间, 单位秒。</p>
</td>
</tr>
<tr id="row117002348336"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p17009343338"><a name="p17009343338"></a><a name="p17009343338"></a>message</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p970103453316"><a name="p970103453316"></a><a name="p970103453316"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p107031134133310"><a name="p107031134133310"></a><a name="p107031134133310"></a>作业执行失败时，显示失败的原因。</p>
</td>
</tr>
<tr id="row5115163155015"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p6115103117501"><a name="p6115103117501"></a><a name="p6115103117501"></a>input</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p1011513155010"><a name="p1011513155010"></a><a name="p1011513155010"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p18115193135012"><a name="p18115193135012"></a><a name="p18115193135012"></a>输入vcf文件的路径。</p>
</td>
</tr>
<tr id="row1140075013500"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p184001150185010"><a name="p184001150185010"></a><a name="p184001150185010"></a>output</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p1040011508506"><a name="p1040011508506"></a><a name="p1040011508506"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p18477728173614"><a name="p18477728173614"></a><a name="p18477728173614"></a>输出vcf文件路径。</p>
</td>
</tr>
<tr id="row1573014569508"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p20730195675017"><a name="p20730195675017"></a><a name="p20730195675017"></a>intervals</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p18251550348"><a name="p18251550348"></a><a name="p18251550348"></a>Array[String]</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p131132054111117"><a name="p131132054111117"></a><a name="p131132054111117"></a>interval文件。</p>
</td>
</tr>
<tr id="row20515517511"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p185116520515"><a name="p185116520515"></a><a name="p185116520515"></a>ref</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p17526518512"><a name="p17526518512"></a><a name="p17526518512"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p1273015675016"><a name="p1273015675016"></a><a name="p1273015675016"></a>该作业选择的参考基因库的文件。</p>
</td>
</tr>
<tr id="row37698105514"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p177691210175117"><a name="p177691210175117"></a><a name="p177691210175117"></a>conf</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p14744859175119"><a name="p14744859175119"></a><a name="p14744859175119"></a>Array[String]</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p1776981005112"><a name="p1776981005112"></a><a name="p1776981005112"></a>配置项，暂时未开放设置。</p>
</td>
</tr>
<tr id="row1636218186511"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p536212183516"><a name="p536212183516"></a><a name="p536212183516"></a>select_type</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p153621918175118"><a name="p153621918175118"></a><a name="p153621918175118"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p183621718145119"><a name="p183621718145119"></a><a name="p183621718145119"></a>该作业选择的变异种类</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section320217117419"></a>

-   请求样例：

    ```
    None
    ```


-   成功响应样例:

    ```
    {
      "count": 1,
      "instances": [
        {  
             "instance_id": "b9d3785e-e3e2-4059-8c65-bfe09d81c2de",
                "owner": "h00251609",
                "status": "FINISHED",
                "start_time": 1536281615654,
                "duration": 67,
                "message": "",
                "input": "s3a://pvc-195465fd-a1d3-11e8-8f70-fa163efe22dd/total.vcf",
                "output": "s3a://pvc-195465fd-a1d3-11e8-8f70-fa163efe22dd/a.vcf",
                "intervals": [
                    "s3a://pvc-195465fd-a1d3-11e8-8f70-fa163efe22dd/tEXOME2_ext50.bed"
                ],
                "ref": "hg19",
                "conf": [],
                "select_type": "SNP"
         }
      ]
    }
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >调用接口出错后，将不会返回上述结果，而是返回错误码和错误信息，详细介绍请参见[错误码](错误码.md)。  


