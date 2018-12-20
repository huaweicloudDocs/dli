# SQL跨源连接<a name="dli_01_0403"></a>

## 操作场景<a name="section31579140143928"></a>

DLI SQL跨源连接可用于访问CloudTable，DWS，RDS等其他数据源。具体的SQL语法参考请参考[CloudTable表](https://support.huaweicloud.com/sqlreference-dli/dli_08_0119.html)，[DWS表](https://support.huaweicloud.com/sqlreference-dli/dli_08_0192.html)和[RDS表](https://support.huaweicloud.com/sqlreference-dli/dli_08_0196.html)。

## 连接列表<a name="section1616314111518"></a>

连接列表显示创建的所有跨源连接，连接数量较多时，系统分页显示。

**表 1**  SQL跨源连接列表参数

<a name="table3950169215120"></a>
<table><thead align="left"><tr id="row2555468715120"><th class="cellrowborder" valign="top" width="21.18%" id="mcps1.2.3.1.1"><p id="p4021197415120"><a name="p4021197415120"></a><a name="p4021197415120"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="78.82000000000001%" id="mcps1.2.3.1.2"><p id="p3594448915120"><a name="p3594448915120"></a><a name="p3594448915120"></a>参数说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row46758327132"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p16413434141957"><a name="p16413434141957"></a><a name="p16413434141957"></a>连接名称</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p54419740141957"><a name="p54419740141957"></a><a name="p54419740141957"></a>所创建的跨源连接名称。</p>
<a name="ul109681518191720"></a><a name="ul109681518191720"></a><ul id="ul109681518191720"><li>名称只能包含数字、英文字母、下划线和中划线。不能为空。</li><li>输入长度不能超过64个字符。</li></ul>
</td>
</tr>
<tr id="row32873162171713"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p45480448171713"><a name="p45480448171713"></a><a name="p45480448171713"></a>连接状态</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p59114099151038"><a name="p59114099151038"></a><a name="p59114099151038"></a>跨源连接的状态信息，包括如下三种状态。</p>
<a name="ul32930526154023"></a><a name="ul32930526154023"></a><ul id="ul32930526154023"><li>创建中</li><li>已激活</li><li>失败</li></ul>
</td>
</tr>
<tr id="row31011923151038"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p10671857151038"><a name="p10671857151038"></a><a name="p10671857151038"></a>服务类型</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p122801954164819"><a name="p122801954164819"></a><a name="p122801954164819"></a>目前支持访问三种类型数据源。</p>
<a name="ul127459715563"></a><a name="ul127459715563"></a><ul id="ul127459715563"><li>表格存储服务 CloudTable</li><li>数据仓库服务 DWS</li><li>关系型数据库 RDS</li></ul>
</td>
</tr>
<tr id="row36301606171658"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p14394959151048"><a name="p14394959151048"></a><a name="p14394959151048"></a>连接地址</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p1483474582618"><a name="p1483474582618"></a><a name="p1483474582618"></a>使用DLI访问其他数据源的地址。</p>
<div class="note" id="note79771723317"><a name="note79771723317"></a><a name="note79771723317"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul18891815103110"></a><a name="ul18891815103110"></a><ul id="ul18891815103110"><li>跨源链接创建成功后显示连接地址。</li><li>创建CloudTable关联表时，指定连接地址或目的地址均可。</li><li>创建DWS或RD关联表时，只能指定连接地址。</li></ul>
</div></div>
</td>
</tr>
<tr id="row6424839516213"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p50569641162134"><a name="p50569641162134"></a><a name="p50569641162134"></a>目的地址</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p18910361162145"><a name="p18910361162145"></a><a name="p18910361162145"></a>连接其他数据源的地址。不同服务的地址略有不同。</p>
<a name="ul67221730122312"></a><a name="ul67221730122312"></a><ul id="ul67221730122312"><li>表格存储服务 CloudTable：ZK链接地址</li><li>数据仓库服务 DWS：内网IP：端口<div class="note" id="note7374154634916"><a name="note7374154634916"></a><a name="note7374154634916"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p16374446124914"><a name="p16374446124914"></a><a name="p16374446124914"></a>DWS有两个内网IP，不能同时使用两个内网IP，任意选择其中一个即可。</p>
</div></div>
</li><li>关系型数据库 RDS：内网地址：数据库端口</li></ul>
</td>
</tr>
<tr id="row2449114254419"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p1845010423449"><a name="p1845010423449"></a><a name="p1845010423449"></a>创建时间</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p114506429448"><a name="p114506429448"></a><a name="p114506429448"></a>每个连接的创建时间，可按创建时间顺序或倒序显示连接列表。</p>
</td>
</tr>
<tr id="row1883611569448"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p13837165614445"><a name="p13837165614445"></a><a name="p13837165614445"></a>进度</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p883775614448"><a name="p883775614448"></a><a name="p883775614448"></a>连接创建的进度， 用百分比表示。</p>
</td>
</tr>
<tr id="row1662880815250"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="p475621615250"><a name="p475621615250"></a><a name="p475621615250"></a>操作</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="p94999298154"><a name="p94999298154"></a><a name="p94999298154"></a>删除。当连接状态在<span class="parmname" id="parmname1819151571614"><a name="parmname1819151571614"></a><a name="parmname1819151571614"></a>“创建中”</span>时，连接不可删除。</p>
</td>
</tr>
</tbody>
</table>

## 创建连接<a name="section73391334165211"></a>

1.  创建需要访问的数据源。例如，需要访问CloudTable数据源，请先在CloudTable服务中购买集群。

    **图 1**  CloudTable购买集群<a name="fig1866711408220"></a>  
    ![](figures/CloudTable购买集群.png "CloudTable购买集群")

    如果已有可用集群，可不用重新购买。

2.  在SQL作业的顶部菜单栏中，选择“跨源连接“。
3.  在“跨源连接“页面，单击![](figures/icon-创建连接.png)创建连接。

    输入连接名称，选择服务类型，安全组，虚拟私有云，子网，输入目的地址，详细参数介绍请参见[表2](#table24931148155220)。

    **图 2**  SQL创建连接<a name="fig375913217530"></a>  
    ![](figures/SQL创建连接.png "SQL创建连接")

    **表 2**  参数说明

    <a name="table24931148155220"></a>
    <table><thead align="left"><tr id="row1149712486527"><th class="cellrowborder" valign="top" width="15.920000000000002%" id="mcps1.2.3.1.1"><p id="p349916487526"><a name="p349916487526"></a><a name="p349916487526"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="84.08%" id="mcps1.2.3.1.2"><p id="p115011548105211"><a name="p115011548105211"></a><a name="p115011548105211"></a>参数说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1350324845215"><td class="cellrowborder" valign="top" width="15.920000000000002%" headers="mcps1.2.3.1.1 "><p id="p8504184814524"><a name="p8504184814524"></a><a name="p8504184814524"></a>连接名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="84.08%" headers="mcps1.2.3.1.2 "><p id="p1550604814528"><a name="p1550604814528"></a><a name="p1550604814528"></a>所创建的跨源连接名称。</p>
    <a name="ul185072486523"></a><a name="ul185072486523"></a><ul id="ul185072486523"><li>名称只能包含数字、英文字母、下划线和中划线。不能为空。</li><li>输入长度不能超过64个字符。</li></ul>
    </td>
    </tr>
    <tr id="row105181748125210"><td class="cellrowborder" valign="top" width="15.920000000000002%" headers="mcps1.2.3.1.1 "><p id="p15181748105215"><a name="p15181748105215"></a><a name="p15181748105215"></a>服务类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="84.08%" headers="mcps1.2.3.1.2 "><p id="p2051984815523"><a name="p2051984815523"></a><a name="p2051984815523"></a>目前支持访问三种类型数据源。</p>
    <a name="ul25191248185210"></a><a name="ul25191248185210"></a><ul id="ul25191248185210"><li>表格存储服务 CloudTable</li><li>数据仓库服务 DWS</li><li>关系型数据库 RDS</li></ul>
    </td>
    </tr>
    <tr id="row85241748185212"><td class="cellrowborder" valign="top" width="15.920000000000002%" headers="mcps1.2.3.1.1 "><p id="p352404835217"><a name="p352404835217"></a><a name="p352404835217"></a>安全组</p>
    </td>
    <td class="cellrowborder" valign="top" width="84.08%" headers="mcps1.2.3.1.2 "><p id="p1952584895212"><a name="p1952584895212"></a><a name="p1952584895212"></a>选择对应的安全组信息。不同服务的安全组信息，可在创建对应的服务集群或实例时由系统提供，或查看已有集群或数据库实例信息。请参考<a href="#fig87571359173616">图3</a>。</p>
    </td>
    </tr>
    <tr id="row7764655142317"><td class="cellrowborder" valign="top" width="15.920000000000002%" headers="mcps1.2.3.1.1 "><p id="p16764105532311"><a name="p16764105532311"></a><a name="p16764105532311"></a>虚拟私有云</p>
    </td>
    <td class="cellrowborder" valign="top" width="84.08%" headers="mcps1.2.3.1.2 "><p id="p1676416559237"><a name="p1676416559237"></a><a name="p1676416559237"></a>选择对应的虚拟私有云信息。不同服务的虚拟私有云信息，可在创建对应的服务集群或实例时由系统提供，或查看已有集群或数据库实例信息。请参考<a href="#fig87571359173616">图3</a>。</p>
    </td>
    </tr>
    <tr id="row1095810374248"><td class="cellrowborder" valign="top" width="15.920000000000002%" headers="mcps1.2.3.1.1 "><p id="p1495903712415"><a name="p1495903712415"></a><a name="p1495903712415"></a>子网</p>
    </td>
    <td class="cellrowborder" valign="top" width="84.08%" headers="mcps1.2.3.1.2 "><p id="p1795918371243"><a name="p1795918371243"></a><a name="p1795918371243"></a>选择对应的子网信息。不同服务的子网信息，可在创建对应的服务集群或实例时由系统提供，或查看已有集群或数据库实例信息。请参考<a href="#fig87571359173616">图3</a>。</p>
    </td>
    </tr>
    <tr id="row135261748155213"><td class="cellrowborder" valign="top" width="15.920000000000002%" headers="mcps1.2.3.1.1 "><p id="p2052610483527"><a name="p2052610483527"></a><a name="p2052610483527"></a>目的地址</p>
    </td>
    <td class="cellrowborder" valign="top" width="84.08%" headers="mcps1.2.3.1.2 "><p id="p6526144817523"><a name="p6526144817523"></a><a name="p6526144817523"></a>连接其他数据源的地址。不同服务的地址略有不同。请参考<a href="#fig87571359173616">图3</a>。</p>
    <a name="ul9527124812520"></a><a name="ul9527124812520"></a><ul id="ul9527124812520"><li>表格存储服务 CloudTable：ZK链接地址</li><li>数据仓库服务 DWS：内网IP：端口</li><li>关系型数据库 RDS：内网地址：数据库端口</li></ul>
    </td>
    </tr>
    </tbody>
    </table>

    **图 3**  CloudTable集群信息<a name="fig87571359173616"></a>  
    ![](figures/CloudTable集群信息.png "CloudTable集群信息")

4.  单击“确定“，完成连接创建。

## 查找连接<a name="section9644161019415"></a>

在“跨源连接“页面，可在搜索框中输入连接名称关键字，查找与之匹配的连接。

## 查看连接详情<a name="section1960402414173"></a>

在“跨源连接“页面，选中一条连接，单击该连接对应的![](figures/icon-展开.png)，可查看该条连接的详细信息。

包括：连接名称，连接地址，服务类型，连接ID，目的地址，日志详情。

>![](public_sys-resources/icon-note.gif) **说明：**   
>当“连接状态“为“失败“，“日志详情“显示“失败原因“。  

## 删除连接<a name="section8647175812179"></a>

在“跨源连接“页面，可单击“操作”列的“删除“，删除不需要的连接。

>![](public_sys-resources/icon-note.gif) **说明：**   
>当“连接状态“为“创建中“时，连接不可删除。  

