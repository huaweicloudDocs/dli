# Spark跨源连接<a name="dli_01_0405"></a>

## 操作场景<a name="zh-cn_topic_0142697328_section31579140143928"></a>

DLI Spark跨源连接可用于访问CloudTable，DWS，RDS，CSS数据源。具体功能介绍请参考《数据湖探索开发指南》\>[《使用DLI跨源能力》](https://support.huaweicloud.com/devg-dli/dli_09_0020.html)。

## 连接列表<a name="zh-cn_topic_0142697328_section1616314111518"></a>

连接列表显示创建的所有跨源连接，连接数量较多时，系统分页显示。

**表 1**  Spark跨源连接列表参数

<a name="zh-cn_topic_0142697328_table3950169215120"></a>
<table><thead align="left"><tr id="zh-cn_topic_0142697328_row2555468715120"><th class="cellrowborder" valign="top" width="21.18%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0142697328_p4021197415120"><a name="zh-cn_topic_0142697328_p4021197415120"></a><a name="zh-cn_topic_0142697328_p4021197415120"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="78.82000000000001%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0142697328_p3594448915120"><a name="zh-cn_topic_0142697328_p3594448915120"></a><a name="zh-cn_topic_0142697328_p3594448915120"></a>参数说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0142697328_row46758327132"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0142697328_p16413434141957"><a name="zh-cn_topic_0142697328_p16413434141957"></a><a name="zh-cn_topic_0142697328_p16413434141957"></a>连接名称</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0142697328_p54419740141957"><a name="zh-cn_topic_0142697328_p54419740141957"></a><a name="zh-cn_topic_0142697328_p54419740141957"></a>所创建的跨源连接名称。</p>
<a name="zh-cn_topic_0142697328_ul109681518191720"></a><a name="zh-cn_topic_0142697328_ul109681518191720"></a><ul id="zh-cn_topic_0142697328_ul109681518191720"><li>名称只能包含数字、英文字母、下划线和中划线。不能为空。</li><li>输入长度不能超过64个字符。</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0142697328_row32873162171713"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0142697328_p45480448171713"><a name="zh-cn_topic_0142697328_p45480448171713"></a><a name="zh-cn_topic_0142697328_p45480448171713"></a>连接状态</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0142697328_p59114099151038"><a name="zh-cn_topic_0142697328_p59114099151038"></a><a name="zh-cn_topic_0142697328_p59114099151038"></a>跨源连接的状态信息，包括如下三种状态。</p>
<a name="zh-cn_topic_0142697328_ul32930526154023"></a><a name="zh-cn_topic_0142697328_ul32930526154023"></a><ul id="zh-cn_topic_0142697328_ul32930526154023"><li>创建中</li><li>已激活</li><li>失败</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0142697328_row31011923151038"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0142697328_p10671857151038"><a name="zh-cn_topic_0142697328_p10671857151038"></a><a name="zh-cn_topic_0142697328_p10671857151038"></a>服务类型</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0142697328_p122801954164819"><a name="zh-cn_topic_0142697328_p122801954164819"></a><a name="zh-cn_topic_0142697328_p122801954164819"></a>目前支持访问四种类型数据源。</p>
<a name="zh-cn_topic_0142697328_ul127459715563"></a><a name="zh-cn_topic_0142697328_ul127459715563"></a><ul id="zh-cn_topic_0142697328_ul127459715563"><li>表格存储服务 CloudTable</li><li>数据仓库服务 DWS</li><li>云数据库（关系型数据库） RDS</li><li>云搜索服务 CSS</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0142697328_row36301606171658"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0142697328_p14394959151048"><a name="zh-cn_topic_0142697328_p14394959151048"></a><a name="zh-cn_topic_0142697328_p14394959151048"></a>连接地址</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0142697328_p1483474582618"><a name="zh-cn_topic_0142697328_p1483474582618"></a><a name="zh-cn_topic_0142697328_p1483474582618"></a>跨源连接创建成功后将显示连接地址，可用于DLI访问其他数据源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0142697328_row6424839516213"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0142697328_p50569641162134"><a name="zh-cn_topic_0142697328_p50569641162134"></a><a name="zh-cn_topic_0142697328_p50569641162134"></a>目的地址</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0142697328_p18910361162145"><a name="zh-cn_topic_0142697328_p18910361162145"></a><a name="zh-cn_topic_0142697328_p18910361162145"></a>连接其他数据源的地址。不同服务的地址略有不同。</p>
<a name="zh-cn_topic_0142697328_ul67221730122312"></a><a name="zh-cn_topic_0142697328_ul67221730122312"></a><ul id="zh-cn_topic_0142697328_ul67221730122312"><li>表格存储服务 CloudTable：ZK链接地址</li><li>数据仓库服务 DWS：内网IP：端口<div class="note" id="note41513398539"><a name="note41513398539"></a><a name="note41513398539"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1215193905319"><a name="p1215193905319"></a><a name="p1215193905319"></a>DWS有两个内网IP，不能同时使用两个内网IP，任意选择其中一个即可。</p>
</div></div>
</li><li>云数据库（关系型数据库） RDS：内网地址：数据库端口</li><li>云搜索服务 CSS：内网地址：端口</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0142697328_row2449114254419"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0142697328_p1845010423449"><a name="zh-cn_topic_0142697328_p1845010423449"></a><a name="zh-cn_topic_0142697328_p1845010423449"></a>创建时间</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0142697328_p114506429448"><a name="zh-cn_topic_0142697328_p114506429448"></a><a name="zh-cn_topic_0142697328_p114506429448"></a>每个连接的创建时间，可按创建时间顺序或倒序显示连接列表。</p>
</td>
</tr>
<tr id="zh-cn_topic_0142697328_row1883611569448"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0142697328_p13837165614445"><a name="zh-cn_topic_0142697328_p13837165614445"></a><a name="zh-cn_topic_0142697328_p13837165614445"></a>进度</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0142697328_p883775614448"><a name="zh-cn_topic_0142697328_p883775614448"></a><a name="zh-cn_topic_0142697328_p883775614448"></a>连接创建的进度， 用百分比表示。</p>
</td>
</tr>
<tr id="zh-cn_topic_0142697328_row1662880815250"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0142697328_p475621615250"><a name="zh-cn_topic_0142697328_p475621615250"></a><a name="zh-cn_topic_0142697328_p475621615250"></a>操作</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0142697328_p94999298154"><a name="zh-cn_topic_0142697328_p94999298154"></a><a name="zh-cn_topic_0142697328_p94999298154"></a>删除。当连接状态在<span class="parmname" id="zh-cn_topic_0142697328_parmname1819151571614"><a name="zh-cn_topic_0142697328_parmname1819151571614"></a><a name="zh-cn_topic_0142697328_parmname1819151571614"></a>“创建中”</span>时，连接不可删除。</p>
</td>
</tr>
</tbody>
</table>

## 创建连接<a name="zh-cn_topic_0142697328_section73391334165211"></a>

1.  创建需要访问的数据源。例如，需要访问CloudTable数据源，请先在CloudTable服务中购买集群。

    **图 1**  CloudTable购买集群<a name="zh-cn_topic_0142697328_fig1866711408220"></a>  
    ![](figures/CloudTable购买集群-1.png "CloudTable购买集群-1")

    如果已有可用集群，可不用重新购买。

2.  在Spark作业的顶部菜单栏中，选择“跨源连接“。
3.  在“跨源连接“页面，单击![](figures/icon-创建连接.png)。

    输入连接名称，选择服务类型，安全组，虚拟私有云，子网，输入目的地址，详细参数介绍请参见[表2](#zh-cn_topic_0142697328_table24931148155220)。

    **图 2**  Spark创建连接<a name="zh-cn_topic_0142697328_fig375913217530"></a>  
    ![](figures/Spark创建连接.png "Spark创建连接")

    **表 2**  Spark跨源连接参数说明

    <a name="zh-cn_topic_0142697328_table24931148155220"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0142697328_row1149712486527"><th class="cellrowborder" valign="top" width="15.24%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0142697328_p349916487526"><a name="zh-cn_topic_0142697328_p349916487526"></a><a name="zh-cn_topic_0142697328_p349916487526"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="84.76%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0142697328_p115011548105211"><a name="zh-cn_topic_0142697328_p115011548105211"></a><a name="zh-cn_topic_0142697328_p115011548105211"></a>参数说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0142697328_row1350324845215"><td class="cellrowborder" valign="top" width="15.24%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0142697328_p8504184814524"><a name="zh-cn_topic_0142697328_p8504184814524"></a><a name="zh-cn_topic_0142697328_p8504184814524"></a>连接名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="84.76%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0142697328_p1550604814528"><a name="zh-cn_topic_0142697328_p1550604814528"></a><a name="zh-cn_topic_0142697328_p1550604814528"></a>所创建的跨源连接名称。</p>
    <a name="zh-cn_topic_0142697328_ul185072486523"></a><a name="zh-cn_topic_0142697328_ul185072486523"></a><ul id="zh-cn_topic_0142697328_ul185072486523"><li>名称只能包含数字、英文字母、下划线和中划线。不能为空。</li><li>输入长度不能超过64个字符。</li></ul>
    </td>
    </tr>
    <tr id="row791816590583"><td class="cellrowborder" valign="top" width="15.24%" headers="mcps1.2.3.1.1 "><p id="p119191259175816"><a name="p119191259175816"></a><a name="p119191259175816"></a>队列</p>
    </td>
    <td class="cellrowborder" valign="top" width="84.76%" headers="mcps1.2.3.1.2 "><p id="p891920595585"><a name="p891920595585"></a><a name="p891920595585"></a>提交Spark作业所在的队列。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0142697328_row105181748125210"><td class="cellrowborder" valign="top" width="15.24%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0142697328_p15181748105215"><a name="zh-cn_topic_0142697328_p15181748105215"></a><a name="zh-cn_topic_0142697328_p15181748105215"></a>服务类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="84.76%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0142697328_p2051984815523"><a name="zh-cn_topic_0142697328_p2051984815523"></a><a name="zh-cn_topic_0142697328_p2051984815523"></a>目前支持访问四种类型数据源。</p>
    <a name="zh-cn_topic_0142697328_ul25191248185210"></a><a name="zh-cn_topic_0142697328_ul25191248185210"></a><ul id="zh-cn_topic_0142697328_ul25191248185210"><li>表格存储服务 CloudTable</li><li>数据仓库服务 DWS</li><li>云数据库（关系型数据库） RDS</li><li>云搜索服务 CSS</li></ul>
    </td>
    </tr>
    <tr id="zh-cn_topic_0142697328_row85241748185212"><td class="cellrowborder" valign="top" width="15.24%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0142697328_p352404835217"><a name="zh-cn_topic_0142697328_p352404835217"></a><a name="zh-cn_topic_0142697328_p352404835217"></a>安全组</p>
    </td>
    <td class="cellrowborder" valign="top" width="84.76%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0142697328_p1952584895212"><a name="zh-cn_topic_0142697328_p1952584895212"></a><a name="zh-cn_topic_0142697328_p1952584895212"></a>选择对应的安全组信息。不同服务的安全组信息，可在创建对应的服务集群或实例时由系统提供，或查看已有集群或数据库实例信息。请参考<a href="#zh-cn_topic_0142697328_fig87571359173616">图3</a>。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0142697328_row7764655142317"><td class="cellrowborder" valign="top" width="15.24%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0142697328_p16764105532311"><a name="zh-cn_topic_0142697328_p16764105532311"></a><a name="zh-cn_topic_0142697328_p16764105532311"></a>虚拟私有云</p>
    </td>
    <td class="cellrowborder" valign="top" width="84.76%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0142697328_p1676416559237"><a name="zh-cn_topic_0142697328_p1676416559237"></a><a name="zh-cn_topic_0142697328_p1676416559237"></a>选择对应的虚拟私有云信息。不同服务的虚拟私有云信息，可在创建对应的服务集群或实例时由系统提供，或查看已有集群或数据库实例信息。请参考<a href="#zh-cn_topic_0142697328_fig87571359173616">图3</a>。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0142697328_row1095810374248"><td class="cellrowborder" valign="top" width="15.24%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0142697328_p1495903712415"><a name="zh-cn_topic_0142697328_p1495903712415"></a><a name="zh-cn_topic_0142697328_p1495903712415"></a>子网</p>
    </td>
    <td class="cellrowborder" valign="top" width="84.76%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0142697328_p1795918371243"><a name="zh-cn_topic_0142697328_p1795918371243"></a><a name="zh-cn_topic_0142697328_p1795918371243"></a>选择对应的子网信息。不同服务的子网信息，可在创建对应的服务集群或实例时由系统提供，或查看已有集群或数据库实例信息。请参考<a href="#zh-cn_topic_0142697328_fig87571359173616">图3</a>。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0142697328_row135261748155213"><td class="cellrowborder" valign="top" width="15.24%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0142697328_p2052610483527"><a name="zh-cn_topic_0142697328_p2052610483527"></a><a name="zh-cn_topic_0142697328_p2052610483527"></a>目的地址</p>
    </td>
    <td class="cellrowborder" valign="top" width="84.76%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0142697328_p6526144817523"><a name="zh-cn_topic_0142697328_p6526144817523"></a><a name="zh-cn_topic_0142697328_p6526144817523"></a>连接其他数据源的地址。不同服务的地址略有不同。请参考<a href="#zh-cn_topic_0142697328_fig87571359173616">图3</a>。</p>
    <a name="zh-cn_topic_0142697328_ul9527124812520"></a><a name="zh-cn_topic_0142697328_ul9527124812520"></a><ul id="zh-cn_topic_0142697328_ul9527124812520"><li>表格存储服务 CloudTable：ZK链接地址</li><li>数据仓库服务 DWS：内网IP：端口</li><li>云数据库（关系型数据库） RDS：内网地址：数据库端口</li><li>云搜索服务 CSS：内网地址：端口</li></ul>
    </td>
    </tr>
    </tbody>
    </table>

    **图 3**  CloudTable集群信息<a name="zh-cn_topic_0142697328_fig87571359173616"></a>  
    ![](figures/CloudTable集群信息-2.png "CloudTable集群信息-2")

4.  单击“确定“，完成连接创建。

## 查找连接<a name="zh-cn_topic_0142697328_section9644161019415"></a>

在“跨源连接“页面，可在搜索框中输入连接名称关键字，查找与之匹配的连接。

## 查看连接详情<a name="zh-cn_topic_0142697328_section1960402414173"></a>

在“跨源连接“页面，选中一条连接，单击该连接对应的![](figures/icon-展开.png)，可查看该条连接的详细信息。

包括：连接名称，连接地址，服务类型，连接ID，目的地址，日志详情。

>![](public_sys-resources/icon-note.gif) **说明：**   
>当“连接状态“为“失败“，“日志详情“显示“失败原因“。  

## 删除连接<a name="zh-cn_topic_0142697328_section8647175812179"></a>

在“跨源连接“页面，可单击“操作”列的“删除“，删除不需要的连接。

>![](public_sys-resources/icon-note.gif) **说明：**   
>当“连接状态“为“创建中“时，连接不可删除。  

