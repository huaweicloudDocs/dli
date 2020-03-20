# 云审计服务支持的DLI操作列表说明<a name="dli_01_0318"></a>

数据湖探索服务（Data Lake Insight，简称DLI）是完全托管的数据分析服务，用户无需管理任何服务器，即开即用；服务支持标准SQL，完全兼容Spark生态接口，提供云上多态数据的统一分析能力。

通过云审计服务，您可以记录与DLI服务相关的操作事件，便于日后的查询、审计和回溯。

**表 1**  云审计服务支持的DLI操作列表

<a name="table176071319307"></a>
<table><thead align="left"><tr id="row126081316301"><th class="cellrowborder" valign="top" width="33.62626262626263%" id="mcps1.2.4.1.1"><p id="p560873133018"><a name="p560873133018"></a><a name="p560873133018"></a><strong id="b141960236329"><a name="b141960236329"></a><a name="b141960236329"></a>操作名称</strong></p>
</th>
<th class="cellrowborder" valign="top" width="33.04040404040404%" id="mcps1.2.4.1.2"><p id="p11608203123018"><a name="p11608203123018"></a><a name="p11608203123018"></a><strong id="b1820052373213"><a name="b1820052373213"></a><a name="b1820052373213"></a>资源类型</strong></p>
</th>
<th class="cellrowborder" valign="top" width="33.333333333333336%" id="mcps1.2.4.1.3"><p id="p1060893133016"><a name="p1060893133016"></a><a name="p1060893133016"></a><strong id="b132021223133210"><a name="b132021223133210"></a><a name="b132021223133210"></a>事件名称</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row1160883111307"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p890674819315"><a name="p890674819315"></a><a name="p890674819315"></a>创建数据库</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p1890714481318"><a name="p1890714481318"></a><a name="p1890714481318"></a>database</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p2910124820319"><a name="p2910124820319"></a><a name="p2910124820319"></a>createDatabase</p>
</td>
</tr>
<tr id="row1860812318306"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p69102048113118"><a name="p69102048113118"></a><a name="p69102048113118"></a>删除数据库</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p791214811314"><a name="p791214811314"></a><a name="p791214811314"></a>database</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p991313489316"><a name="p991313489316"></a><a name="p991313489316"></a>dropDatabase</p>
</td>
</tr>
<tr id="row165981513136"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p1159918131035"><a name="p1159918131035"></a><a name="p1159918131035"></a>修改数据库所有者</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p259912132318"><a name="p259912132318"></a><a name="p259912132318"></a>database</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p175999131238"><a name="p175999131238"></a><a name="p175999131238"></a>alterDatabaseOwner</p>
</td>
</tr>
<tr id="row10610143117308"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p4919104883115"><a name="p4919104883115"></a><a name="p4919104883115"></a>创建表</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p892024811319"><a name="p892024811319"></a><a name="p892024811319"></a>table</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p9925134883120"><a name="p9925134883120"></a><a name="p9925134883120"></a>createTable</p>
</td>
</tr>
<tr id="row2610183116307"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p13927184843114"><a name="p13927184843114"></a><a name="p13927184843114"></a>删除表</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p5927134811310"><a name="p5927134811310"></a><a name="p5927134811310"></a>table</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p7929184819313"><a name="p7929184819313"></a><a name="p7929184819313"></a>dropTable</p>
</td>
</tr>
<tr id="row1466721015114"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p143577321913"><a name="p143577321913"></a><a name="p143577321913"></a>导出表数据</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p15357143212110"><a name="p15357143212110"></a><a name="p15357143212110"></a>table</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p235715321915"><a name="p235715321915"></a><a name="p235715321915"></a>exportData</p>
</td>
</tr>
<tr id="row36694101112"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p1135720323119"><a name="p1135720323119"></a><a name="p1135720323119"></a>导入表数据</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p17357193212116"><a name="p17357193212116"></a><a name="p17357193212116"></a>table</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p14357153219117"><a name="p14357153219117"></a><a name="p14357153219117"></a>importData</p>
</td>
</tr>
<tr id="row1569093412818"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p46904341783"><a name="p46904341783"></a><a name="p46904341783"></a>修改表的所有者</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p9690113419810"><a name="p9690113419810"></a><a name="p9690113419810"></a>table</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p169011348816"><a name="p169011348816"></a><a name="p169011348816"></a>alterTableOwner</p>
</td>
</tr>
<tr id="row961113112306"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p199566482315"><a name="p199566482315"></a><a name="p199566482315"></a>创建队列</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p19561848193110"><a name="p19561848193110"></a><a name="p19561848193110"></a>queue</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p1957154873115"><a name="p1957154873115"></a><a name="p1957154873115"></a>createQueue</p>
</td>
</tr>
<tr id="row261183103010"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p19581148203115"><a name="p19581148203115"></a><a name="p19581148203115"></a>删除队列</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p4960194815314"><a name="p4960194815314"></a><a name="p4960194815314"></a>queue</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p0960248133112"><a name="p0960248133112"></a><a name="p0960248133112"></a>dropQueue</p>
</td>
</tr>
<tr id="row17611133114301"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p18967174814312"><a name="p18967174814312"></a><a name="p18967174814312"></a>使用队列</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p1996774853120"><a name="p1996774853120"></a><a name="p1996774853120"></a>queue</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p139691448153112"><a name="p139691448153112"></a><a name="p139691448153112"></a>useQueue</p>
</td>
</tr>
<tr id="row19385491309"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p178655117111"><a name="p178655117111"></a><a name="p178655117111"></a>队列授权</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p2086661617"><a name="p2086661617"></a><a name="p2086661617"></a>queue</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p1867616118"><a name="p1867616118"></a><a name="p1867616118"></a>shareQueue</p>
</td>
</tr>
<tr id="row1560410188718"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p10605131818714"><a name="p10605131818714"></a><a name="p10605131818714"></a>更新队列</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p0605718577"><a name="p0605718577"></a><a name="p0605718577"></a>queue</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p6605201810719"><a name="p6605201810719"></a><a name="p6605201810719"></a>updateQueue</p>
</td>
</tr>
<tr id="row23816498017"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p188703111119"><a name="p188703111119"></a><a name="p188703111119"></a>取消作业</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p28711214117"><a name="p28711214117"></a><a name="p28711214117"></a>queue</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p168735110113"><a name="p168735110113"></a><a name="p168735110113"></a>cancelJob</p>
</td>
</tr>
<tr id="row1735014015414"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p106221747174517"><a name="p106221747174517"></a><a name="p106221747174517"></a>冻结资源</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p5621114713455"><a name="p5621114713455"></a><a name="p5621114713455"></a>resource</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p16617147194510"><a name="p16617147194510"></a><a name="p16617147194510"></a>freezeResource</p>
</td>
</tr>
<tr id="row14487228124519"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p648912864512"><a name="p648912864512"></a><a name="p648912864512"></a>解冻资源</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p4489122814514"><a name="p4489122814514"></a><a name="p4489122814514"></a>resource</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p7489202817459"><a name="p7489202817459"></a><a name="p7489202817459"></a>activeResource</p>
</td>
</tr>
<tr id="row2035018401346"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p4785121313123"><a name="p4785121313123"></a><a name="p4785121313123"></a>终止资源</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p3937155010518"><a name="p3937155010518"></a><a name="p3937155010518"></a>resource</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p1593718506517"><a name="p1593718506517"></a><a name="p1593718506517"></a>terminateResource</p>
</td>
</tr>
<tr id="row167958130911"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p1979511134919"><a name="p1979511134919"></a><a name="p1979511134919"></a>上传资源</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p127952013694"><a name="p127952013694"></a><a name="p127952013694"></a>resources</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p579513131898"><a name="p579513131898"></a><a name="p579513131898"></a>uploadResources</p>
</td>
</tr>
<tr id="row5350114014417"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p69371750659"><a name="p69371750659"></a><a name="p69371750659"></a>资源清理</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p13938450651"><a name="p13938450651"></a><a name="p13938450651"></a>user</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p209381450655"><a name="p209381450655"></a><a name="p209381450655"></a>clean-resource</p>
</td>
</tr>
<tr id="row1835034015413"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p15938150756"><a name="p15938150756"></a><a name="p15938150756"></a>数据授权</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p993816501059"><a name="p993816501059"></a><a name="p993816501059"></a>data</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p29383509513"><a name="p29383509513"></a><a name="p29383509513"></a>shareData</p>
</td>
</tr>
<tr id="row9351640046"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p2093816507512"><a name="p2093816507512"></a><a name="p2093816507512"></a>导出查询结果</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p393817501519"><a name="p393817501519"></a><a name="p393817501519"></a>data</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p6938105017519"><a name="p6938105017519"></a><a name="p6938105017519"></a>exportResult</p>
</td>
</tr>
<tr id="row203519401046"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p393815501519"><a name="p393815501519"></a><a name="p393815501519"></a>保存模板</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p39381508510"><a name="p39381508510"></a><a name="p39381508510"></a>sqlStore</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p693819501858"><a name="p693819501858"></a><a name="p693819501858"></a>saveSQLTemplate</p>
</td>
</tr>
<tr id="row435120403410"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p893811508516"><a name="p893811508516"></a><a name="p893811508516"></a>更新模板</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p89399501752"><a name="p89399501752"></a><a name="p89399501752"></a>sqlStore</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p139391950158"><a name="p139391950158"></a><a name="p139391950158"></a>updateSQLTemplate</p>
</td>
</tr>
<tr id="row835114401746"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p14939150859"><a name="p14939150859"></a><a name="p14939150859"></a>删除模板</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p59397503512"><a name="p59397503512"></a><a name="p59397503512"></a>sqlStore</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p2939165014510"><a name="p2939165014510"></a><a name="p2939165014510"></a>deleteSQLTemplate</p>
</td>
</tr>
<tr id="row9351640846"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p1793910506517"><a name="p1793910506517"></a><a name="p1793910506517"></a>创建数据上传任务</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p16939350352"><a name="p16939350352"></a><a name="p16939350352"></a>uploader</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p209391850955"><a name="p209391850955"></a><a name="p209391850955"></a>createJob</p>
</td>
</tr>
<tr id="row113511740345"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p49391507520"><a name="p49391507520"></a><a name="p49391507520"></a>获取数据上传任务鉴权</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p12338102315112"><a name="p12338102315112"></a><a name="p12338102315112"></a>uploader</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p2939115015518"><a name="p2939115015518"></a><a name="p2939115015518"></a>getAuthInfo</p>
</td>
</tr>
<tr id="row113511401746"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p1893985019519"><a name="p1893985019519"></a><a name="p1893985019519"></a>提交上传任务数据</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p8198172712113"><a name="p8198172712113"></a><a name="p8198172712113"></a>uploader</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p494025017510"><a name="p494025017510"></a><a name="p494025017510"></a>commitJob</p>
</td>
</tr>
<tr id="row13518401343"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p12940125011511"><a name="p12940125011511"></a><a name="p12940125011511"></a>更新配额</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p294014501951"><a name="p294014501951"></a><a name="p294014501951"></a>quota</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p179401502057"><a name="p179401502057"></a><a name="p179401502057"></a>updateQuota</p>
</td>
</tr>
<tr id="row2945351716"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p89512351912"><a name="p89512351912"></a><a name="p89512351912"></a>上传jars文件</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p7951935214"><a name="p7951935214"></a><a name="p7951935214"></a>jars</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p49583515115"><a name="p49583515115"></a><a name="p49583515115"></a>uploadJars</p>
</td>
</tr>
<tr id="row54511419128"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p1645213193212"><a name="p1645213193212"></a><a name="p1645213193212"></a>上传pyfiles文件</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p1045251916219"><a name="p1045251916219"></a><a name="p1045251916219"></a>pyfiles</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p2045215191728"><a name="p2045215191728"></a><a name="p2045215191728"></a>uploadPyFiles</p>
</td>
</tr>
<tr id="row1770864219716"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p1870917421478"><a name="p1870917421478"></a><a name="p1870917421478"></a>队列排序</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p77101542271"><a name="p77101542271"></a><a name="p77101542271"></a>order</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p371034216711"><a name="p371034216711"></a><a name="p371034216711"></a>orderQueue</p>
</td>
</tr>
<tr id="row686612562515"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p11866155614514"><a name="p11866155614514"></a><a name="p11866155614514"></a>创建跨源连接</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p1986615562517"><a name="p1986615562517"></a><a name="p1986615562517"></a>datasource</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p48667561852"><a name="p48667561852"></a><a name="p48667561852"></a>createConn</p>
</td>
</tr>
<tr id="row165301288407"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p5531285409"><a name="p5531285409"></a><a name="p5531285409"></a>查询跨源连接</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p85311789407"><a name="p85311789407"></a><a name="p85311789407"></a>datasource</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p853111817409"><a name="p853111817409"></a><a name="p853111817409"></a>listDSConnections</p>
</td>
</tr>
<tr id="row3507145014415"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p145071150144116"><a name="p145071150144116"></a><a name="p145071150144116"></a>创建主题</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p1550715016415"><a name="p1550715016415"></a><a name="p1550715016415"></a>smn</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p1550714503418"><a name="p1550714503418"></a><a name="p1550714503418"></a>createTopic</p>
</td>
</tr>
<tr id="row448892204716"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p144883204718"><a name="p144883204718"></a><a name="p144883204718"></a>上传资源包</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p174896234710"><a name="p174896234710"></a><a name="p174896234710"></a>pkgresource</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p148911214714"><a name="p148911214714"></a><a name="p148911214714"></a>uploadResources</p>
</td>
</tr>
<tr id="row92786274820"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p2278102104818"><a name="p2278102104818"></a><a name="p2278102104818"></a>DLI授权</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p927817294811"><a name="p927817294811"></a><a name="p927817294811"></a>agency</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p1727816219483"><a name="p1727816219483"></a><a name="p1727816219483"></a>isTrustDLI</p>
</td>
</tr>
<tr id="row1658454985411"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p4584164912548"><a name="p4584164912548"></a><a name="p4584164912548"></a>创建批处理作业</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p1858484917541"><a name="p1858484917541"></a><a name="p1858484917541"></a>batch</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p16584749115415"><a name="p16584749115415"></a><a name="p16584749115415"></a>createBatch</p>
</td>
</tr>
<tr id="row18157165219552"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p1115795218553"><a name="p1115795218553"></a><a name="p1115795218553"></a>删除批处理作业</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p81571352185513"><a name="p81571352185513"></a><a name="p81571352185513"></a>batch</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p715765225517"><a name="p715765225517"></a><a name="p715765225517"></a>deleteBatch</p>
</td>
</tr>
<tr id="row4441237840"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p544193718411"><a name="p544193718411"></a><a name="p544193718411"></a>取消批处理作业</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p14411371244"><a name="p14411371244"></a><a name="p14411371244"></a>batch</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p84411377415"><a name="p84411377415"></a><a name="p84411377415"></a>cancelBatch</p>
</td>
</tr>
<tr id="row3847110325"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p184819101124"><a name="p184819101124"></a><a name="p184819101124"></a>创建会话</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p1284812101218"><a name="p1284812101218"></a><a name="p1284812101218"></a>session</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p168489101326"><a name="p168489101326"></a><a name="p168489101326"></a>createSession</p>
</td>
</tr>
<tr id="row1043915377218"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p11439193712217"><a name="p11439193712217"></a><a name="p11439193712217"></a>删除会话</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p1043910372212"><a name="p1043910372212"></a><a name="p1043910372212"></a>session</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p1439237425"><a name="p1439237425"></a><a name="p1439237425"></a>deleteSession</p>
</td>
</tr>
<tr id="row121811328848"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p1718114289420"><a name="p1718114289420"></a><a name="p1718114289420"></a>查询会话列表</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p918114281040"><a name="p918114281040"></a><a name="p918114281040"></a>session</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p71815281418"><a name="p71815281418"></a><a name="p71815281418"></a>getSessionList</p>
</td>
</tr>
<tr id="row973081019318"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p2073015101310"><a name="p2073015101310"></a><a name="p2073015101310"></a>查询会话状态</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p167309103314"><a name="p167309103314"></a><a name="p167309103314"></a>session</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p973171017318"><a name="p973171017318"></a><a name="p973171017318"></a>getSessionState</p>
</td>
</tr>
<tr id="row7239193215319"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p1623973213319"><a name="p1623973213319"></a><a name="p1623973213319"></a>查询会话详情</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p162391332836"><a name="p162391332836"></a><a name="p162391332836"></a>session</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p192391532538"><a name="p192391532538"></a><a name="p192391532538"></a>getSessionDetail</p>
</td>
</tr>
<tr id="row93901711845"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p63911511347"><a name="p63911511347"></a><a name="p63911511347"></a>查询会话日志</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p83911411249"><a name="p83911411249"></a><a name="p83911411249"></a>session</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p143911812046"><a name="p143911812046"></a><a name="p143911812046"></a>getSessionLog</p>
</td>
</tr>
<tr id="row0264622864"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p182642221862"><a name="p182642221862"></a><a name="p182642221862"></a>创建注释</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p1226512221868"><a name="p1226512221868"></a><a name="p1226512221868"></a>statement</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p92651122760"><a name="p92651122760"></a><a name="p92651122760"></a>createStatement</p>
</td>
</tr>
<tr id="row14602397620"><td class="cellrowborder" valign="top" width="33.62626262626263%" headers="mcps1.2.4.1.1 "><p id="p04610391613"><a name="p04610391613"></a><a name="p04610391613"></a>取消注释</p>
</td>
<td class="cellrowborder" valign="top" width="33.04040404040404%" headers="mcps1.2.4.1.2 "><p id="p946120391262"><a name="p946120391262"></a><a name="p946120391262"></a>statement</p>
</td>
<td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.3 "><p id="p5461193913614"><a name="p5461193913614"></a><a name="p5461193913614"></a>cancelStatement</p>
</td>
</tr>
</tbody>
</table>

关于如何开通云审计服务以及如何查看追踪事件，请参考《[云审计服务快速入门](https://support.huaweicloud.com/qs-cts/cts_02_0001.html)》中的相关章节。

关于云审计服务事件结构的关键字段详解，请参见《云审计服务用户指南》中的[事件结构](https://support.huaweicloud.com/usermanual-cts/cts_03_0010.html)和[事件样例](https://support.huaweicloud.com/usermanual-cts/cts_03_0011.html)。

