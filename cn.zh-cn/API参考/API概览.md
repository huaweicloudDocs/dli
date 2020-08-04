# API概览<a name="dli_02_0181"></a>

本章节介绍了目前DLI所提供的API列表。

**表 1**  DLI API列表

<a name="table124291373019"></a>
<table><thead align="left"><tr id="row1357718371307"><th class="cellrowborder" valign="top" width="18.98%" id="mcps1.2.4.1.1"><p id="p1557712371803"><a name="p1557712371803"></a><a name="p1557712371803"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="15.22%" id="mcps1.2.4.1.2"><p id="p557783719014"><a name="p557783719014"></a><a name="p557783719014"></a>子类型</p>
</th>
<th class="cellrowborder" valign="top" width="65.8%" id="mcps1.2.4.1.3"><p id="p135771037406"><a name="p135771037406"></a><a name="p135771037406"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row458164335714"><td class="cellrowborder" valign="top" width="18.98%" headers="mcps1.2.4.1.1 "><p id="p536002145819"><a name="p536002145819"></a><a name="p536002145819"></a>权限相关API</p>
</td>
<td class="cellrowborder" valign="top" width="15.22%" headers="mcps1.2.4.1.2 "><p id="p658212431575"><a name="p658212431575"></a><a name="p658212431575"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="65.8%" headers="mcps1.2.4.1.3 "><p id="p2582943205716"><a name="p2582943205716"></a><a name="p2582943205716"></a>包括队列赋权、查看队列的使用者、数据赋权、查看数据库的使用者、查看表的使用者、查看表的用户权限和查看赋权对象使用者权限信息。</p>
</td>
</tr>
<tr id="row17108152642017"><td class="cellrowborder" valign="top" width="18.98%" headers="mcps1.2.4.1.1 "><p id="p111052616209"><a name="p111052616209"></a><a name="p111052616209"></a>委托相关API</p>
</td>
<td class="cellrowborder" valign="top" width="15.22%" headers="mcps1.2.4.1.2 "><p id="p91103263207"><a name="p91103263207"></a><a name="p91103263207"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="65.8%" headers="mcps1.2.4.1.3 "><p id="p7110126112019"><a name="p7110126112019"></a><a name="p7110126112019"></a>包括获取DLI委托信息和创建DLI委托。</p>
</td>
</tr>
<tr id="row62118542816"><td class="cellrowborder" valign="top" width="18.98%" headers="mcps1.2.4.1.1 "><p id="p32216549813"><a name="p32216549813"></a><a name="p32216549813"></a>队列相关API（推荐）</p>
</td>
<td class="cellrowborder" valign="top" width="15.22%" headers="mcps1.2.4.1.2 "><p id="p7221354586"><a name="p7221354586"></a><a name="p7221354586"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="65.8%" headers="mcps1.2.4.1.3 "><p id="p14221154483"><a name="p14221154483"></a><a name="p14221154483"></a>包括创建队列、删除队列、查询所有队列、修改队列网段、重启/扩容/缩容队列和查询队列详情、创建指定地址连通性测试请求、查询指定地址连通性请求、创建队列定时扩缩容计划、查询队列定时扩缩容计划、批量删除队列定时扩缩容计划、单个删除队列定时扩缩容计划、修改队列定时扩缩容计划。</p>
</td>
</tr>
<tr id="row95789371020"><td class="cellrowborder" rowspan="4" valign="top" width="18.98%" headers="mcps1.2.4.1.1 "><p id="p17848115812101"><a name="p17848115812101"></a><a name="p17848115812101"></a>SQL作业相关API</p>
<p id="p1636313681113"><a name="p1636313681113"></a><a name="p1636313681113"></a></p>
</td>
<td class="cellrowborder" valign="top" width="15.22%" headers="mcps1.2.4.1.2 "><p id="p145785371104"><a name="p145785371104"></a><a name="p145785371104"></a>数据库相关API</p>
</td>
<td class="cellrowborder" valign="top" width="65.8%" headers="mcps1.2.4.1.3 "><p id="p345317441251"><a name="p345317441251"></a><a name="p345317441251"></a>包括创建数据库、删除数据库、查看所有数据库和修改数据库用户。</p>
</td>
</tr>
<tr id="row18137571175"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1513810718710"><a name="p1513810718710"></a><a name="p1513810718710"></a>表相关API</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p513837677"><a name="p513837677"></a><a name="p513837677"></a>包括创建表、删除表、查询所有表、描述表信息、预览表内容、修改表用户和获取分区信息列表。</p>
</td>
</tr>
<tr id="row11996916275"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p99961416375"><a name="p99961416375"></a><a name="p99961416375"></a>作业相关API</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p169961916475"><a name="p169961916475"></a><a name="p169961916475"></a>包括导入数据、导出数据、提交SQL作业、取消作业、查询所有作业、查询作业结果、查询作业状态、查询作业详细信息、检查SQL语法和导出查询结果。</p>
</td>
</tr>
<tr id="row123631363115"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p14363123614119"><a name="p14363123614119"></a><a name="p14363123614119"></a>上传数据相关API</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p183631236161111"><a name="p183631236161111"></a><a name="p183631236161111"></a>包括创建上传作业、提交上传作业。</p>
</td>
</tr>
<tr id="row181621174496"><td class="cellrowborder" valign="top" width="18.98%" headers="mcps1.2.4.1.1 "><p id="p4320142815498"><a name="p4320142815498"></a><a name="p4320142815498"></a>Flink作业相关API</p>
</td>
<td class="cellrowborder" valign="top" width="15.22%" headers="mcps1.2.4.1.2 "><p id="p173201528144919"><a name="p173201528144919"></a><a name="p173201528144919"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="65.8%" headers="mcps1.2.4.1.3 "><p id="p1320202812495"><a name="p1320202812495"></a><a name="p1320202812495"></a>包括OBS授权给DLI服务、新建SQL作业、更新SQL作业、新建Flink自定义作业、更新Flink自定义作业、批量运行作业、查询作业列表、查询作业详情、查询作业执行计划、查询作业监控信息、查询作业APIG网关服务访问地址、批量停止作业、删除作业、批量删除作业、导出Flink作业、导入Flink作业、创建IEF消息通道、边缘Flink作业状态上报、边缘Flink作业Action回调、IEF系统事件上报。</p>
</td>
</tr>
<tr id="row18579133720020"><td class="cellrowborder" rowspan="3" valign="top" width="18.98%" headers="mcps1.2.4.1.1 "><p id="p65781737203"><a name="p65781737203"></a><a name="p65781737203"></a>Spark作业相关API</p>
</td>
<td class="cellrowborder" valign="top" width="15.22%" headers="mcps1.2.4.1.2 "><p id="p1857963715013"><a name="p1857963715013"></a><a name="p1857963715013"></a>会话相关API</p>
</td>
<td class="cellrowborder" valign="top" width="65.8%" headers="mcps1.2.4.1.3 "><p id="p1457920371609"><a name="p1457920371609"></a><a name="p1457920371609"></a>包括创建会话、取消会话、查看会话列表、查看会话信息、查看会话状态和查看会话日志。</p>
</td>
</tr>
<tr id="row6579103713011"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p12579133718018"><a name="p12579133718018"></a><a name="p12579133718018"></a>语句相关API</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p145793372001"><a name="p145793372001"></a><a name="p145793372001"></a>包括创建语句、取消语句执行、查看语句列表和查看语句信息。</p>
</td>
</tr>
<tr id="row4579637907"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p175791837609"><a name="p175791837609"></a><a name="p175791837609"></a>批处理相关API</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1579193711010"><a name="p1579193711010"></a><a name="p1579193711010"></a>包括创建批处理作业、删除批处理作业、查询批处理作业列表、查询批处理作业详情、查询批处理作业状态和查询批处理作业日志。</p>
</td>
</tr>
<tr id="row8261122810619"><td class="cellrowborder" valign="top" width="18.98%" headers="mcps1.2.4.1.1 "><p id="p19261928866"><a name="p19261928866"></a><a name="p19261928866"></a>资源包相关API</p>
</td>
<td class="cellrowborder" valign="top" width="15.22%" headers="mcps1.2.4.1.2 "><p id="p571513551617"><a name="p571513551617"></a><a name="p571513551617"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="65.8%" headers="mcps1.2.4.1.3 "><p id="p1667618248152"><a name="p1667618248152"></a><a name="p1667618248152"></a>包括上传资源包、删除资源包、查询所有资源包、查询指定资源包、上传分组资源、查询分组资源列表、上传jar类型分组资源、上传pyfile类型分组资源、上传file类型分组资源、查询组内资源包和删除组内资源包。</p>
</td>
</tr>
<tr id="row1357176226"><td class="cellrowborder" valign="top" width="18.98%" headers="mcps1.2.4.1.1 "><p id="p14751141514214"><a name="p14751141514214"></a><a name="p14751141514214"></a>Flink作业模板相关API</p>
</td>
<td class="cellrowborder" valign="top" width="15.22%" headers="mcps1.2.4.1.2 "><p id="p275119159214"><a name="p275119159214"></a><a name="p275119159214"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="65.8%" headers="mcps1.2.4.1.3 "><p id="p7751141520214"><a name="p7751141520214"></a><a name="p7751141520214"></a>包括新建模板、更新模板、删除模板和查询模板列表。</p>
</td>
</tr>
<tr id="row1430308191911"><td class="cellrowborder" valign="top" width="18.98%" headers="mcps1.2.4.1.1 "><p id="p63034831919"><a name="p63034831919"></a><a name="p63034831919"></a>经典型跨源连接相关API</p>
</td>
<td class="cellrowborder" valign="top" width="15.22%" headers="mcps1.2.4.1.2 "><p id="p030311811911"><a name="p030311811911"></a><a name="p030311811911"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="65.8%" headers="mcps1.2.4.1.3 "><p id="p1730411851919"><a name="p1730411851919"></a><a name="p1730411851919"></a>包括创建经典型跨源连接、删除经典型跨源连接、查询经典型跨源连接列表和查询经典型跨源连接。</p>
</td>
</tr>
<tr id="row92719553245"><td class="cellrowborder" valign="top" width="18.98%" headers="mcps1.2.4.1.1 "><p id="p7271175592420"><a name="p7271175592420"></a><a name="p7271175592420"></a>增强型跨源连接相关API</p>
</td>
<td class="cellrowborder" valign="top" width="15.22%" headers="mcps1.2.4.1.2 "><p id="p12271655132410"><a name="p12271655132410"></a><a name="p12271655132410"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="65.8%" headers="mcps1.2.4.1.3 "><p id="p13271555162413"><a name="p13271555162413"></a><a name="p13271555162413"></a>包括创建增强型跨源连接、删除增强型跨源连接、查询增强型跨源连接列表、查询增强型跨源连接、绑定队列、解绑队列、修改主机信息和查询增强型跨源授权信息。</p>
</td>
</tr>
<tr id="row11857171322"><td class="cellrowborder" valign="top" width="18.98%" headers="mcps1.2.4.1.1 "><p id="p1384851128"><a name="p1384851128"></a><a name="p1384851128"></a>全局变量相关API</p>
</td>
<td class="cellrowborder" valign="top" width="15.22%" headers="mcps1.2.4.1.2 "><p id="p208487110215"><a name="p208487110215"></a><a name="p208487110215"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="65.8%" headers="mcps1.2.4.1.3 "><p id="p18848918212"><a name="p18848918212"></a><a name="p18848918212"></a>包括创建全局变量、删除全局变量、修改全局变量和查询所有全局变量。</p>
</td>
</tr>
</tbody>
</table>

