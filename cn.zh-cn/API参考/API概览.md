# API概览<a name="dli_02_0181"></a>

本章节介绍了目前DLI所提供的API列表。

**表 1**  DLI API列表

<a name="table124291373019"></a>
<table><thead align="left"><tr id="row1357718371307"><th class="cellrowborder" valign="top" width="18.98%" id="mcps1.2.4.1.1"><p id="p1557712371803"><a name="p1557712371803"></a><a name="p1557712371803"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="16.18%" id="mcps1.2.4.1.2"><p id="p557783719014"><a name="p557783719014"></a><a name="p557783719014"></a>子类型</p>
</th>
<th class="cellrowborder" valign="top" width="64.84%" id="mcps1.2.4.1.3"><p id="p135771037406"><a name="p135771037406"></a><a name="p135771037406"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row857819371607"><td class="cellrowborder" rowspan="5" valign="top" width="18.98%" headers="mcps1.2.4.1.1 "><p id="p165781373012"><a name="p165781373012"></a><a name="p165781373012"></a>SQL作业相关API</p>
<p id="p3138137576"><a name="p3138137576"></a><a name="p3138137576"></a></p>
<p id="p49969161378"><a name="p49969161378"></a><a name="p49969161378"></a></p>
<p id="p942134112712"><a name="p942134112712"></a><a name="p942134112712"></a></p>
<p id="p64225411472"><a name="p64225411472"></a><a name="p64225411472"></a></p>
</td>
<td class="cellrowborder" valign="top" width="16.18%" headers="mcps1.2.4.1.2 "><p id="p85783371108"><a name="p85783371108"></a><a name="p85783371108"></a>队列相关API</p>
</td>
<td class="cellrowborder" valign="top" width="64.84%" headers="mcps1.2.4.1.3 "><p id="p357833718014"><a name="p357833718014"></a><a name="p357833718014"></a>包括创建队列、删除队列和查询队列列表。</p>
</td>
</tr>
<tr id="row95789371020"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p145785371104"><a name="p145785371104"></a><a name="p145785371104"></a>数据库相关API</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p345317441251"><a name="p345317441251"></a><a name="p345317441251"></a>包括创建数据库、删除数据库、查看所有数据库和修改数据库用户。</p>
</td>
</tr>
<tr id="row18137571175"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1513810718710"><a name="p1513810718710"></a><a name="p1513810718710"></a>表相关API</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p513837677"><a name="p513837677"></a><a name="p513837677"></a>包括创建表、删除表、查看所有表、描述表信息和预览表内容。</p>
</td>
</tr>
<tr id="row11996916275"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p99961416375"><a name="p99961416375"></a><a name="p99961416375"></a>作业相关API</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p169961916475"><a name="p169961916475"></a><a name="p169961916475"></a>包括提交SQL作业、导入数据、导出数据、查询作业状态、查询作业详细信息、查看作业结果、导出查询结果、查询所有作业、取消作业和检查SQL语法。</p>
</td>
</tr>
<tr id="row164211241273"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p742217412072"><a name="p742217412072"></a><a name="p742217412072"></a>权限相关API</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p142214112719"><a name="p142214112719"></a><a name="p142214112719"></a>包括队列赋权、查看队列的使用者、数据赋权、查看数据库的使用者、查看表的使用者和查看表的用户权限。</p>
</td>
</tr>
<tr id="row1557823714019"><td class="cellrowborder" rowspan="6" valign="top" width="18.98%" headers="mcps1.2.4.1.1 "><p id="p65781737203"><a name="p65781737203"></a><a name="p65781737203"></a>Spark作业相关API</p>
<p id="p4675152461517"><a name="p4675152461517"></a><a name="p4675152461517"></a></p>
<p id="p7676182421516"><a name="p7676182421516"></a><a name="p7676182421516"></a></p>
</td>
<td class="cellrowborder" valign="top" width="16.18%" headers="mcps1.2.4.1.2 "><p id="p757814373011"><a name="p757814373011"></a><a name="p757814373011"></a>队列相关API</p>
</td>
<td class="cellrowborder" valign="top" width="64.84%" headers="mcps1.2.4.1.3 "><p id="p257917378019"><a name="p257917378019"></a><a name="p257917378019"></a>包括创建队列、删除队列、获取指定队列信息和获取全部队列信息。</p>
</td>
</tr>
<tr id="row18579133720020"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1857963715013"><a name="p1857963715013"></a><a name="p1857963715013"></a>会话相关API</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1457920371609"><a name="p1457920371609"></a><a name="p1457920371609"></a>包括创建会话、删除会话、查看会话列表、查看会话信息、查看会话状态和查看会话日志。</p>
</td>
</tr>
<tr id="row6579103713011"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p12579133718018"><a name="p12579133718018"></a><a name="p12579133718018"></a>语句相关API</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p145793372001"><a name="p145793372001"></a><a name="p145793372001"></a>包括创建语句、取消语句执行、查看语句列表和查看语句信息。</p>
</td>
</tr>
<tr id="row4579637907"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p175791837609"><a name="p175791837609"></a><a name="p175791837609"></a>批处理相关API</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1579193711010"><a name="p1579193711010"></a><a name="p1579193711010"></a>包括创建批处理作业、删除批处理作业、获取批处理作业列表、获取批处理作业详情、获取批处理作业状态和获取批处理作业日志。</p>
</td>
</tr>
<tr id="row10674024161515"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1675124131518"><a name="p1675124131518"></a><a name="p1675124131518"></a>资源包相关API</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p7675132416156"><a name="p7675132416156"></a><a name="p7675132416156"></a>包括上传资源包、删除资源包、查看资源包列表和查看资源包。</p>
</td>
</tr>
<tr id="row18676102411153"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1767682491519"><a name="p1767682491519"></a><a name="p1767682491519"></a>分组资源相关API</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1667618248152"><a name="p1667618248152"></a><a name="p1667618248152"></a>包括上传分组资源、查看分组资源列表、上传jar类型分组资源、上传pyfile类型分组资源、上传file类型分组资源、查看组内资源包和删除组内资源包。</p>
</td>
</tr>
<tr id="row1430308191911"><td class="cellrowborder" valign="top" width="18.98%" headers="mcps1.2.4.1.1 "><p id="p63034831919"><a name="p63034831919"></a><a name="p63034831919"></a>经典型跨源连接相关API</p>
</td>
<td class="cellrowborder" valign="top" width="16.18%" headers="mcps1.2.4.1.2 "><p id="p030311811911"><a name="p030311811911"></a><a name="p030311811911"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="64.84%" headers="mcps1.2.4.1.3 "><p id="p1730411851919"><a name="p1730411851919"></a><a name="p1730411851919"></a>包括创建经典型跨源连接、删除经典型跨源连接、查询经典型跨源连接和查询经典型跨源连接列表。</p>
</td>
</tr>
<tr id="row92719553245"><td class="cellrowborder" valign="top" width="18.98%" headers="mcps1.2.4.1.1 "><p id="p7271175592420"><a name="p7271175592420"></a><a name="p7271175592420"></a>增强型跨源连接相关API</p>
</td>
<td class="cellrowborder" valign="top" width="16.18%" headers="mcps1.2.4.1.2 "><p id="p12271655132410"><a name="p12271655132410"></a><a name="p12271655132410"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="64.84%" headers="mcps1.2.4.1.3 "><p id="p13271555162413"><a name="p13271555162413"></a><a name="p13271555162413"></a>包括创建增强型跨源连接、删除增强型跨源连接、查询增强型跨源连接、查询增强型跨源连接列表、绑定队列和解绑队列。</p>
</td>
</tr>
</tbody>
</table>

