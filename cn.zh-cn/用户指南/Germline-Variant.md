# Germline Variant<a name="dli_01_0393"></a>

## Germline Variant概述<a name="section8244204903017"></a>

DLI全托管式的DNA测序流程, 基于GATK4.0标准测序流程进行分布式优化, 性能相对于单机版测序流程提升10倍有余。目前支持人类样本的WGS\(全基因组测序\)和WES\(外显子测序\)流程。

>![](public_sys-resources/icon-note.gif) **说明：**   
>提交Germline Variant作业需进行实名认证，并且需要进行委托授权。具体操作请参考[准备工作](准备工作.md)。  

## 创建作业<a name="section137181944132313"></a>

**图 1**  Germline Variant创建作业<a name="fig93451497275"></a>  
![](figures/Germline-Variant创建作业.png "Germline-Variant创建作业")

1.  数据导入。

    **图 2**  Germline Variant数据导入<a name="fig8733134573117"></a>  
    ![](figures/Germline-Variant数据导入.png "Germline-Variant数据导入")

    **表 1**  参数说明

    <a name="table2010883415300"></a>
    <table><thead align="left"><tr id="row111151534153010"><th class="cellrowborder" valign="top" width="13.25%" id="mcps1.2.4.1.1"><p id="p11117734133018"><a name="p11117734133018"></a><a name="p11117734133018"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="74.42%" id="mcps1.2.4.1.2"><p id="p111803463010"><a name="p111803463010"></a><a name="p111803463010"></a>描述</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.33%" id="mcps1.2.4.1.3"><p id="p12121334143014"><a name="p12121334143014"></a><a name="p12121334143014"></a>示例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row121231434203019"><td class="cellrowborder" valign="top" width="13.25%" headers="mcps1.2.4.1.1 "><p id="p9124103411301"><a name="p9124103411301"></a><a name="p9124103411301"></a>文件类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.42%" headers="mcps1.2.4.1.2 "><p id="p2012863412302"><a name="p2012863412302"></a><a name="p2012863412302"></a>选择FASTQ或BAM类型的输入文件。</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.33%" headers="mcps1.2.4.1.3 "><p id="p111291034143010"><a name="p111291034143010"></a><a name="p111291034143010"></a>FASTQ</p>
    </td>
    </tr>
    <tr id="row11381434123019"><td class="cellrowborder" valign="top" width="13.25%" headers="mcps1.2.4.1.1 "><p id="p7139103411301"><a name="p7139103411301"></a><a name="p7139103411301"></a>输入路径</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.42%" headers="mcps1.2.4.1.2 "><p id="p1214173412306"><a name="p1214173412306"></a><a name="p1214173412306"></a>选择文件所在的OBS路径。</p>
    <a name="ul4142934153015"></a><a name="ul4142934153015"></a><ul id="ul4142934153015"><li>当输入文件类型为FASTQ时，需要指定两个OBS上的FASTQ文件路径。</li><li>当输入文件类型为BAM时，需要指定一个OBS上的BAM文件路径。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="12.33%" headers="mcps1.2.4.1.3 "><p id="p19146123416308"><a name="p19146123416308"></a><a name="p19146123416308"></a>-</p>
    </td>
    </tr>
    </tbody>
    </table>

2.  基本参数配置。
    -   若输入文件为FASTQ类型，需配置如下参数：

        **图 3**  FASTQ类型参数配置<a name="fig117435485412"></a>  
        ![](figures/FASTQ类型参数配置.png "FASTQ类型参数配置")

    -   若输入文件为BAM类型，需配置如下参数：

        -   执行引擎选择GATK

            **图 4**  BAM类型参数配置<a name="fig427012635910"></a>  
            ![](figures/BAM类型参数配置.png "BAM类型参数配置")

        -   执行引擎选择Tensorflow

            **图 5**  执行引擎Tensorflow参数配置<a name="fig147891321102"></a>  
            ![](figures/执行引擎Tensorflow参数配置.png "执行引擎Tensorflow参数配置")


        **表 2**  参数说明

        <a name="table25749533543"></a>
        <table><thead align="left"><tr id="row16583353145419"><th class="cellrowborder" valign="top" width="13.25%" id="mcps1.2.4.1.1"><p id="p358513539545"><a name="p358513539545"></a><a name="p358513539545"></a>参数名称</p>
        </th>
        <th class="cellrowborder" valign="top" width="77.18%" id="mcps1.2.4.1.2"><p id="p258515365418"><a name="p258515365418"></a><a name="p258515365418"></a>描述</p>
        </th>
        <th class="cellrowborder" valign="top" width="9.569999999999999%" id="mcps1.2.4.1.3"><p id="p1158845319548"><a name="p1158845319548"></a><a name="p1158845319548"></a>示例</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row1869515111719"><td class="cellrowborder" valign="top" width="13.25%" headers="mcps1.2.4.1.1 "><p id="p1715991610719"><a name="p1715991610719"></a><a name="p1715991610719"></a>执行引擎</p>
        </td>
        <td class="cellrowborder" valign="top" width="77.18%" headers="mcps1.2.4.1.2 "><p id="p1016315167719"><a name="p1016315167719"></a><a name="p1016315167719"></a>选择BAM类型的输入文件时，需要选择对应的执行引擎，如下所示：</p>
        <a name="ul11651316376"></a><a name="ul11651316376"></a><ul id="ul11651316376"><li>GATK：标准GATK流程</li><li>Tensorflow：利用深度学习模型进行变异检测</li></ul>
        </td>
        <td class="cellrowborder" valign="top" width="9.569999999999999%" headers="mcps1.2.4.1.3 "><p id="p131741716177"><a name="p131741716177"></a><a name="p131741716177"></a>GATK</p>
        </td>
        </tr>
        <tr id="row10620155317542"><td class="cellrowborder" valign="top" width="13.25%" headers="mcps1.2.4.1.1 "><p id="p762205315416"><a name="p762205315416"></a><a name="p762205315416"></a>输出GVCF</p>
        </td>
        <td class="cellrowborder" valign="top" width="77.18%" headers="mcps1.2.4.1.2 "><p id="p20623145305419"><a name="p20623145305419"></a><a name="p20623145305419"></a>选择是否输出GVCF格式文件。</p>
        </td>
        <td class="cellrowborder" valign="top" width="9.569999999999999%" headers="mcps1.2.4.1.3 "><p id="p1762555319548"><a name="p1762555319548"></a><a name="p1762555319548"></a>否</p>
        </td>
        </tr>
        <tr id="row962795375414"><td class="cellrowborder" valign="top" width="13.25%" headers="mcps1.2.4.1.1 "><p id="p18630175312542"><a name="p18630175312542"></a><a name="p18630175312542"></a>输出路径</p>
        </td>
        <td class="cellrowborder" valign="top" width="77.18%" headers="mcps1.2.4.1.2 "><p id="p16321253175411"><a name="p16321253175411"></a><a name="p16321253175411"></a>基因检测结果的OBS输出路径。</p>
        </td>
        <td class="cellrowborder" valign="top" width="9.569999999999999%" headers="mcps1.2.4.1.3 "><p id="p1963515312541"><a name="p1963515312541"></a><a name="p1963515312541"></a>-</p>
        </td>
        </tr>
        <tr id="row156354531547"><td class="cellrowborder" valign="top" width="13.25%" headers="mcps1.2.4.1.1 "><p id="p1263819536544"><a name="p1263819536544"></a><a name="p1263819536544"></a>参考基因</p>
        </td>
        <td class="cellrowborder" valign="top" width="77.18%" headers="mcps1.2.4.1.2 "><p id="p1564005395416"><a name="p1564005395416"></a><a name="p1564005395416"></a>基因行业内标准的基因库，目前支持hg19和hg38。</p>
        </td>
        <td class="cellrowborder" valign="top" width="9.569999999999999%" headers="mcps1.2.4.1.3 "><p id="p206424538542"><a name="p206424538542"></a><a name="p206424538542"></a>hg38</p>
        </td>
        </tr>
        <tr id="row17643155311544"><td class="cellrowborder" valign="top" width="13.25%" headers="mcps1.2.4.1.1 "><p id="p1064515325412"><a name="p1064515325412"></a><a name="p1064515325412"></a>已知变异基因集</p>
        </td>
        <td class="cellrowborder" valign="top" width="77.18%" headers="mcps1.2.4.1.2 "><p id="p18646253205411"><a name="p18646253205411"></a><a name="p18646253205411"></a>根据给定的下拉框，选择需要进行比对的已知变异基因集合，可以多选。</p>
        </td>
        <td class="cellrowborder" valign="top" width="9.569999999999999%" headers="mcps1.2.4.1.3 "><p id="p1764875395415"><a name="p1764875395415"></a><a name="p1764875395415"></a>-</p>
        </td>
        </tr>
        <tr id="row76501535546"><td class="cellrowborder" valign="top" width="13.25%" headers="mcps1.2.4.1.1 "><p id="p1065214531543"><a name="p1065214531543"></a><a name="p1065214531543"></a>BQSR文件导出</p>
        </td>
        <td class="cellrowborder" valign="top" width="77.18%" headers="mcps1.2.4.1.2 "><p id="p1265335325419"><a name="p1265335325419"></a><a name="p1265335325419"></a>比对文件导出。基因检测过程中间会生成BAM类型的文件，用户可以选择将这个BAM文件保存至OBS，以供日后使用。</p>
        </td>
        <td class="cellrowborder" valign="top" width="9.569999999999999%" headers="mcps1.2.4.1.3 "><p id="p465535312544"><a name="p465535312544"></a><a name="p465535312544"></a>-</p>
        </td>
        </tr>
        <tr id="row176568536544"><td class="cellrowborder" valign="top" width="13.25%" headers="mcps1.2.4.1.1 "><p id="p665895310547"><a name="p665895310547"></a><a name="p665895310547"></a>高级选项</p>
        </td>
        <td class="cellrowborder" valign="top" width="77.18%" headers="mcps1.2.4.1.2 "><p id="p5661185317545"><a name="p5661185317545"></a><a name="p5661185317545"></a>打开高级选项，可在基因变异检测过程中，进行参数设置，参数格式为“key value”。具体描述请参考<a href="#table19583102475616">表3</a>。</p>
        </td>
        <td class="cellrowborder" valign="top" width="9.569999999999999%" headers="mcps1.2.4.1.3 "><p id="p8662175313549"><a name="p8662175313549"></a><a name="p8662175313549"></a>-</p>
        </td>
        </tr>
        </tbody>
        </table>

        **表 3**  高级选项参数说明

        <a name="table19583102475616"></a>
        <table><thead align="left"><tr id="row559342411563"><th class="cellrowborder" valign="top" width="22.182218221822183%" id="mcps1.2.4.1.1"><p id="p155951624155613"><a name="p155951624155613"></a><a name="p155951624155613"></a>参数名称</p>
        </th>
        <th class="cellrowborder" valign="top" width="68.21682168216822%" id="mcps1.2.4.1.2"><p id="p9597102425618"><a name="p9597102425618"></a><a name="p9597102425618"></a>描述</p>
        </th>
        <th class="cellrowborder" valign="top" width="9.6009600960096%" id="mcps1.2.4.1.3"><p id="p959922415614"><a name="p959922415614"></a><a name="p959922415614"></a>示例</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row3602182425611"><td class="cellrowborder" valign="top" width="22.182218221822183%" headers="mcps1.2.4.1.1 "><p id="p16040242560"><a name="p16040242560"></a><a name="p16040242560"></a>FastqToSam</p>
        </td>
        <td class="cellrowborder" valign="top" width="68.21682168216822%" headers="mcps1.2.4.1.2 "><p id="p1606112495611"><a name="p1606112495611"></a><a name="p1606112495611"></a>执行FastqToSam方法时业务相关的配置项，用户可手动添加。</p>
        </td>
        <td class="cellrowborder" valign="top" width="9.6009600960096%" headers="mcps1.2.4.1.3 "><p id="p4608142425612"><a name="p4608142425612"></a><a name="p4608142425612"></a>-</p>
        </td>
        </tr>
        <tr id="row1860942435618"><td class="cellrowborder" valign="top" width="22.182218221822183%" headers="mcps1.2.4.1.1 "><p id="p3612324175619"><a name="p3612324175619"></a><a name="p3612324175619"></a>BwaSpark</p>
        </td>
        <td class="cellrowborder" valign="top" width="68.21682168216822%" headers="mcps1.2.4.1.2 "><p id="p1561312455619"><a name="p1561312455619"></a><a name="p1561312455619"></a>执行GATK BwaSpark方法时业务相关的配置项，用户可手动添加。</p>
        <div class="note" id="note186141246563"><a name="note186141246563"></a><a name="note186141246563"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p18615424115616"><a name="p18615424115616"></a><a name="p18615424115616"></a>暂不支持关于输出文件格式以及输入输出路径相关的配置项。</p>
        </div></div>
        </td>
        <td class="cellrowborder" valign="top" width="9.6009600960096%" headers="mcps1.2.4.1.3 "><p id="p16617142413567"><a name="p16617142413567"></a><a name="p16617142413567"></a>-</p>
        </td>
        </tr>
        <tr id="row17617122425612"><td class="cellrowborder" valign="top" width="22.182218221822183%" headers="mcps1.2.4.1.1 "><p id="p9619124155610"><a name="p9619124155610"></a><a name="p9619124155610"></a>ReadsPipelineSpark</p>
        </td>
        <td class="cellrowborder" valign="top" width="68.21682168216822%" headers="mcps1.2.4.1.2 "><p id="p10621112425610"><a name="p10621112425610"></a><a name="p10621112425610"></a>执行GATK ReadsPipelineSpark方法时业务相关的配置项，用户可手动添加。</p>
        <div class="note" id="note2062392414566"><a name="note2062392414566"></a><a name="note2062392414566"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p12624224195613"><a name="p12624224195613"></a><a name="p12624224195613"></a>暂不支持关于输出文件格式以及输入输出路径相关的配置项。</p>
        </div></div>
        </td>
        <td class="cellrowborder" valign="top" width="9.6009600960096%" headers="mcps1.2.4.1.3 "><p id="p1062712445615"><a name="p1062712445615"></a><a name="p1062712445615"></a>-</p>
        </td>
        </tr>
        </tbody>
        </table>


3.  单击“提交”。

## 作业列表<a name="section368833171215"></a>

**图 6**  Germline Variant作业列表<a name="fig15853644132319"></a>  
![](figures/Germline-Variant作业列表.png "Germline-Variant作业列表")

作业列表显示所有的Germline Variant作业，作业数量较多时，系统分页显示，您可以查看所有历史提交的作业。作业列表默认按创建时间排列，可选择升序或降序排列；也可以选择时间范围，查看特定时间范围内提交的作业。

**表 4**  作业列表参数

<a name="table1985719445234"></a>
<table><thead align="left"><tr id="row185419444235"><th class="cellrowborder" valign="top" width="21.18%" id="mcps1.2.3.1.1"><p id="p1185410448233"><a name="p1185410448233"></a><a name="p1185410448233"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="78.82000000000001%" id="mcps1.2.3.1.2"><p id="p18854164412310"><a name="p18854164412310"></a><a name="p18854164412310"></a>参数说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row3854044162316"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p585417447233"><a name="p585417447233"></a><a name="p585417447233"></a>创建时间</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p1885417444234"><a name="p1885417444234"></a><a name="p1885417444234"></a>每个作业的创建时间，目前按创建时间倒序显示作业列表。</p>
</td>
</tr>
<tr id="row285474452317"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p4854144462314"><a name="p4854144462314"></a><a name="p4854144462314"></a>文件类型</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p15854204412311"><a name="p15854204412311"></a><a name="p15854204412311"></a>有FASTQ和BAM两种类型的输入文件。</p>
</td>
</tr>
<tr id="row2855134432310"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p9854104413232"><a name="p9854104413232"></a><a name="p9854104413232"></a>作业状态</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p1385412448231"><a name="p1385412448231"></a><a name="p1385412448231"></a>作业的状态信息，包括如下六种状态。</p>
<a name="ul1385594452311"></a><a name="ul1385594452311"></a><ul id="ul1385594452311"><li>提交（launching）</li><li>运行中（running）</li><li>完成（finished）</li><li>失败（failed）</li><li>取消（cancelled）</li><li>取消中（canceling）</li></ul>
</td>
</tr>
<tr id="row1585510448230"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p5855204442311"><a name="p5855204442311"></a><a name="p5855204442311"></a>作业ID</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p1185510444231"><a name="p1185510444231"></a><a name="p1185510444231"></a>所提交基因作业的ID，由系统默认生成的唯一标识。</p>
</td>
</tr>
<tr id="row19855144472314"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p12855244152310"><a name="p12855244152310"></a><a name="p12855244152310"></a>用户名</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p3855194417231"><a name="p3855194417231"></a><a name="p3855194417231"></a>提交基因作业的用户名称。</p>
</td>
</tr>
<tr id="row158554442233"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p198556441234"><a name="p198556441234"></a><a name="p198556441234"></a>运行时长</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p685519445231"><a name="p685519445231"></a><a name="p685519445231"></a>作业运行的时间长度。</p>
</td>
</tr>
<tr id="row138571744182316"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p17855184432311"><a name="p17855184432311"></a><a name="p17855184432311"></a>进度</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p1857124412239"><a name="p1857124412239"></a><a name="p1857124412239"></a>作业运行的进度， 例如：1/3表示总共有三个步骤，当前执行到第一步。</p>
</td>
</tr>
<tr id="row18572445232"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p1685714482310"><a name="p1685714482310"></a><a name="p1685714482310"></a>操作</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p685712446239"><a name="p685712446239"></a><a name="p685712446239"></a>终止作业。</p>
<div class="note" id="note128573442234"><a name="note128573442234"></a><a name="note128573442234"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p285719446236"><a name="p285719446236"></a><a name="p285719446236"></a>只能终止“提交中”或“运行中”的作业。</p>
</div></div>
</td>
</tr>
</tbody>
</table>

-   查找作业

    在[图6](#fig15853644132319)右上侧“日期”栏，单击![](figures/icon-日期.png)选择“开始时间”和“结束时间”，可查找对应时间段内提交的作业。

-   查看作业详情

    在[图6](#fig15853644132319)页面，选中一条作业，单击该作业对应的![](figures/icon-展开.png)，可查看该条作业的详细信息。

    包括：输入路径，输出路径，文件类型，参考基因，已知变异基因集，输出GVCF，FastqToSam参数，BwaSpark参数，ReadPipelineSpark参数（若输入文件为BAM，则只显示该参数），BQSR文件导出（创建作业时，若没有选择，则不显示），执行引擎（若输入文件为BAM，则显示该参数），日志详情（如果作业执行失败，会显示失败原因）。

    **图 7**  Germline Variant作业详情<a name="fig187315426564"></a>  
    ![](figures/Germline-Variant作业详情.png "Germline-Variant作业详情")


## 流程介绍<a name="section1235315355212"></a>

**图 8**  Germline Variant流程介绍<a name="fig5850193418534"></a>  
![](figures/Germline-Variant流程介绍.png "Germline-Variant流程介绍")

