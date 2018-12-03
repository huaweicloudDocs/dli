# 云审计服务支持的DLI操作列表<a name="dli_01_0318"></a>

数据湖探索作为serverless 的大数据分析查询服务，提供针对云存储的SQL查询分析能力。

通过云审计服务，您可以记录与DLI服务相关的操作事件，便于日后的查询、审计和回溯。

**表 1**  云审计服务支持的DLI操作列表

<a name="table176071319307"></a>
<table><thead align="left"><tr id="row126081316301"><th class="cellrowborder" valign="top" width="33.333333333333336%" id="mcps1.2.4.1.1"><p id="p560873133018"><a name="p560873133018"></a><a name="p560873133018"></a><strong id="b141960236329"><a name="b141960236329"></a><a name="b141960236329"></a>操作名称</strong></p>
</th>
<th class="cellrowborder" valign="top" width="33.333333333333336%" id="mcps1.2.4.1.2"><p id="p11608203123018"><a name="p11608203123018"></a><a name="p11608203123018"></a><strong id="b1820052373213"><a name="b1820052373213"></a><a name="b1820052373213"></a>资源类型</strong></p>
</th>
<th class="cellrowborder" valign="top" width="33.333333333333336%" id="mcps1.2.4.1.3"><p id="p1060893133016"><a name="p1060893133016"></a><a name="p1060893133016"></a><strong id="b132021223133210"><a name="b132021223133210"></a><a name="b132021223133210"></a>事件名称</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row1160883111307"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p890674819315"><a name="p890674819315"></a><a name="p890674819315"></a>创建数据库</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p1890714481318"><a name="p1890714481318"></a><a name="p1890714481318"></a>database</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p2910124820319"><a name="p2910124820319"></a><a name="p2910124820319"></a>createDatabase</p>
</td>
</tr>
<tr id="row1860812318306"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p69102048113118"><a name="p69102048113118"></a><a name="p69102048113118"></a>删除数据库</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p791214811314"><a name="p791214811314"></a><a name="p791214811314"></a>database</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p991313489316"><a name="p991313489316"></a><a name="p991313489316"></a>dropDatabase</p>
</td>
</tr>
<tr id="row10610143117308"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p4919104883115"><a name="p4919104883115"></a><a name="p4919104883115"></a>创建表</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p892024811319"><a name="p892024811319"></a><a name="p892024811319"></a>table</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p9925134883120"><a name="p9925134883120"></a><a name="p9925134883120"></a>createTable</p>
</td>
</tr>
<tr id="row2610183116307"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p13927184843114"><a name="p13927184843114"></a><a name="p13927184843114"></a>删除表</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p5927134811310"><a name="p5927134811310"></a><a name="p5927134811310"></a>table</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p7929184819313"><a name="p7929184819313"></a><a name="p7929184819313"></a>dropTable</p>
</td>
</tr>
<tr id="row1466721015114"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p143577321913"><a name="p143577321913"></a><a name="p143577321913"></a>导出表数据</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p15357143212110"><a name="p15357143212110"></a><a name="p15357143212110"></a>table</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p235715321915"><a name="p235715321915"></a><a name="p235715321915"></a>exportData</p>
</td>
</tr>
<tr id="row36694101112"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p1135720323119"><a name="p1135720323119"></a><a name="p1135720323119"></a>导入表数据</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p17357193212116"><a name="p17357193212116"></a><a name="p17357193212116"></a>table</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p14357153219117"><a name="p14357153219117"></a><a name="p14357153219117"></a>importData</p>
</td>
</tr>
<tr id="row961113112306"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p199566482315"><a name="p199566482315"></a><a name="p199566482315"></a>创建队列</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p19561848193110"><a name="p19561848193110"></a><a name="p19561848193110"></a>queue</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p1957154873115"><a name="p1957154873115"></a><a name="p1957154873115"></a>createQueue</p>
</td>
</tr>
<tr id="row261183103010"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p19581148203115"><a name="p19581148203115"></a><a name="p19581148203115"></a>删除队列</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p4960194815314"><a name="p4960194815314"></a><a name="p4960194815314"></a>queue</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p0960248133112"><a name="p0960248133112"></a><a name="p0960248133112"></a>dropQueue</p>
</td>
</tr>
<tr id="row17611133114301"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p18967174814312"><a name="p18967174814312"></a><a name="p18967174814312"></a>使用队列</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p1996774853120"><a name="p1996774853120"></a><a name="p1996774853120"></a>queue</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p139691448153112"><a name="p139691448153112"></a><a name="p139691448153112"></a>useQueue</p>
</td>
</tr>
<tr id="row19385491309"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p178655117111"><a name="p178655117111"></a><a name="p178655117111"></a>资源授权</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p2086661617"><a name="p2086661617"></a><a name="p2086661617"></a>queue</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p1867616118"><a name="p1867616118"></a><a name="p1867616118"></a>shareQueue</p>
</td>
</tr>
<tr id="row23816498017"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p188703111119"><a name="p188703111119"></a><a name="p188703111119"></a>取消任务</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p28711214117"><a name="p28711214117"></a><a name="p28711214117"></a>queue</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p168735110113"><a name="p168735110113"></a><a name="p168735110113"></a>cancelJob</p>
</td>
</tr>
<tr id="row1735014015414"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p106221747174517"><a name="p106221747174517"></a><a name="p106221747174517"></a>冻结资源</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p5621114713455"><a name="p5621114713455"></a><a name="p5621114713455"></a>resource</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p16617147194510"><a name="p16617147194510"></a><a name="p16617147194510"></a>freezeResource</p>
</td>
</tr>
<tr id="row14487228124519"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p648912864512"><a name="p648912864512"></a><a name="p648912864512"></a>解冻资源</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p4489122814514"><a name="p4489122814514"></a><a name="p4489122814514"></a>resource</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p7489202817459"><a name="p7489202817459"></a><a name="p7489202817459"></a>activeResource</p>
</td>
</tr>
<tr id="row2035018401346"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p1793717503514"><a name="p1793717503514"></a><a name="p1793717503514"></a>终止资源</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p3937155010518"><a name="p3937155010518"></a><a name="p3937155010518"></a>resource</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p1593718506517"><a name="p1593718506517"></a><a name="p1593718506517"></a>terminateResource</p>
</td>
</tr>
<tr id="row5350114014417"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p69371750659"><a name="p69371750659"></a><a name="p69371750659"></a>资源清理</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p13938450651"><a name="p13938450651"></a><a name="p13938450651"></a>user</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p209381450655"><a name="p209381450655"></a><a name="p209381450655"></a>clean-resource</p>
</td>
</tr>
<tr id="row1835034015413"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p15938150756"><a name="p15938150756"></a><a name="p15938150756"></a>数据授权</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p993816501059"><a name="p993816501059"></a><a name="p993816501059"></a>data</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p29383509513"><a name="p29383509513"></a><a name="p29383509513"></a>shareData</p>
</td>
</tr>
<tr id="row9351640046"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p2093816507512"><a name="p2093816507512"></a><a name="p2093816507512"></a>导出查询结果</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p393817501519"><a name="p393817501519"></a><a name="p393817501519"></a>data</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p6938105017519"><a name="p6938105017519"></a><a name="p6938105017519"></a>exportResult</p>
</td>
</tr>
<tr id="row203519401046"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p393815501519"><a name="p393815501519"></a><a name="p393815501519"></a>保存模板</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p39381508510"><a name="p39381508510"></a><a name="p39381508510"></a>sqlStore</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p693819501858"><a name="p693819501858"></a><a name="p693819501858"></a>saveSQLTemplate</p>
</td>
</tr>
<tr id="row435120403410"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p893811508516"><a name="p893811508516"></a><a name="p893811508516"></a>更新模板</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p89399501752"><a name="p89399501752"></a><a name="p89399501752"></a>sqlStore</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p139391950158"><a name="p139391950158"></a><a name="p139391950158"></a>updateSQLTemplate</p>
</td>
</tr>
<tr id="row835114401746"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p14939150859"><a name="p14939150859"></a><a name="p14939150859"></a>删除模板</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p59397503512"><a name="p59397503512"></a><a name="p59397503512"></a>sqlStore</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p2939165014510"><a name="p2939165014510"></a><a name="p2939165014510"></a>deleteSQLTemplate</p>
</td>
</tr>
<tr id="row9351640846"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p1793910506517"><a name="p1793910506517"></a><a name="p1793910506517"></a>创建数据上传任务</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p16939350352"><a name="p16939350352"></a><a name="p16939350352"></a>uploader</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p209391850955"><a name="p209391850955"></a><a name="p209391850955"></a>createJob</p>
</td>
</tr>
<tr id="row113511740345"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p49391507520"><a name="p49391507520"></a><a name="p49391507520"></a>获取数据上传任务鉴权</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p12338102315112"><a name="p12338102315112"></a><a name="p12338102315112"></a>uploader</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p2939115015518"><a name="p2939115015518"></a><a name="p2939115015518"></a>getAuthInfo</p>
</td>
</tr>
<tr id="row113511401746"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p1893985019519"><a name="p1893985019519"></a><a name="p1893985019519"></a>提交上传任务数据</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p8198172712113"><a name="p8198172712113"></a><a name="p8198172712113"></a>uploader</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p494025017510"><a name="p494025017510"></a><a name="p494025017510"></a>commitJob</p>
</td>
</tr>
<tr id="row13518401343"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p12940125011511"><a name="p12940125011511"></a><a name="p12940125011511"></a>更新配额</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.2 "><p id="p294014501951"><a name="p294014501951"></a><a name="p294014501951"></a>quota</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p179401502057"><a name="p179401502057"></a><a name="p179401502057"></a>updateQuota</p>
</td>
</tr>
</tbody>
</table>

