# DLI资源<a name="dli_01_0417"></a>

资源是服务中存在的对象。在DLI中，资源如下，您可以在创建自定义策略时，通过指定资源路径来选择特定资源。

**表 1**  DLI的指定资源与对应路径

<a name="table17762145616578"></a>
<table><thead align="left"><tr id="row1691118561571"><th class="cellrowborder" valign="top" width="17.77%" id="mcps1.2.4.1.1"><p id="p9912105615575"><a name="p9912105615575"></a><a name="p9912105615575"></a>指定资源</p>
</th>
<th class="cellrowborder" valign="top" width="22.74%" id="mcps1.2.4.1.2"><p id="p10130637163016"><a name="p10130637163016"></a><a name="p10130637163016"></a>资源名称</p>
</th>
<th class="cellrowborder" valign="top" width="59.489999999999995%" id="mcps1.2.4.1.3"><p id="p13912105611577"><a name="p13912105611577"></a><a name="p13912105611577"></a>资源路径</p>
</th>
</tr>
</thead>
<tbody><tr id="row59128562574"><td class="cellrowborder" valign="top" width="17.77%" headers="mcps1.2.4.1.1 "><p id="p204333213513"><a name="p204333213513"></a><a name="p204333213513"></a>queue</p>
</td>
<td class="cellrowborder" valign="top" width="22.74%" headers="mcps1.2.4.1.2 "><p id="p1113119377307"><a name="p1113119377307"></a><a name="p1113119377307"></a>DLI队列</p>
</td>
<td class="cellrowborder" valign="top" width="59.489999999999995%" headers="mcps1.2.4.1.3 "><p id="p86653855311"><a name="p86653855311"></a><a name="p86653855311"></a>queues.queuename</p>
</td>
</tr>
<tr id="row2230131615118"><td class="cellrowborder" valign="top" width="17.77%" headers="mcps1.2.4.1.1 "><p id="p184313212518"><a name="p184313212518"></a><a name="p184313212518"></a>database</p>
</td>
<td class="cellrowborder" valign="top" width="22.74%" headers="mcps1.2.4.1.2 "><p id="p11131237143019"><a name="p11131237143019"></a><a name="p11131237143019"></a>DLI数据库</p>
</td>
<td class="cellrowborder" valign="top" width="59.489999999999995%" headers="mcps1.2.4.1.3 "><p id="p166568175319"><a name="p166568175319"></a><a name="p166568175319"></a>databases.dbname</p>
</td>
</tr>
<tr id="row1095412247517"><td class="cellrowborder" valign="top" width="17.77%" headers="mcps1.2.4.1.1 "><p id="p64393235116"><a name="p64393235116"></a><a name="p64393235116"></a>table</p>
</td>
<td class="cellrowborder" valign="top" width="22.74%" headers="mcps1.2.4.1.2 "><p id="p12131133753010"><a name="p12131133753010"></a><a name="p12131133753010"></a>DLI表</p>
</td>
<td class="cellrowborder" valign="top" width="59.489999999999995%" headers="mcps1.2.4.1.3 "><p id="p56665812534"><a name="p56665812534"></a><a name="p56665812534"></a>databases.dbname.tables.tbname</p>
</td>
</tr>
<tr id="row395411241511"><td class="cellrowborder" valign="top" width="17.77%" headers="mcps1.2.4.1.1 "><p id="p3431432125114"><a name="p3431432125114"></a><a name="p3431432125114"></a>column</p>
</td>
<td class="cellrowborder" valign="top" width="22.74%" headers="mcps1.2.4.1.2 "><p id="p313123753011"><a name="p313123753011"></a><a name="p313123753011"></a>DLI列</p>
</td>
<td class="cellrowborder" valign="top" width="59.489999999999995%" headers="mcps1.2.4.1.3 "><p id="p6666198145313"><a name="p6666198145313"></a><a name="p6666198145313"></a>databases.dbname.tables.tbname.columns.colname</p>
</td>
</tr>
<tr id="row630345682110"><td class="cellrowborder" valign="top" width="17.77%" headers="mcps1.2.4.1.1 "><p id="p994510338234"><a name="p994510338234"></a><a name="p994510338234"></a>jobs</p>
</td>
<td class="cellrowborder" valign="top" width="22.74%" headers="mcps1.2.4.1.2 "><p id="p494553372318"><a name="p494553372318"></a><a name="p494553372318"></a>DLI Flink作业</p>
</td>
<td class="cellrowborder" valign="top" width="59.489999999999995%" headers="mcps1.2.4.1.3 "><p id="p1794553314234"><a name="p1794553314234"></a><a name="p1794553314234"></a>jobs.flink.jobid</p>
</td>
</tr>
<tr id="row1823511125249"><td class="cellrowborder" valign="top" width="17.77%" headers="mcps1.2.4.1.1 "><p id="p19236141217246"><a name="p19236141217246"></a><a name="p19236141217246"></a>resource</p>
</td>
<td class="cellrowborder" valign="top" width="22.74%" headers="mcps1.2.4.1.2 "><p id="p15236151217244"><a name="p15236151217244"></a><a name="p15236151217244"></a>DLI程序包</p>
</td>
<td class="cellrowborder" valign="top" width="59.489999999999995%" headers="mcps1.2.4.1.3 "><p id="p523711215247"><a name="p523711215247"></a><a name="p523711215247"></a>resources.resourcename</p>
</td>
</tr>
<tr id="row3895191612240"><td class="cellrowborder" valign="top" width="17.77%" headers="mcps1.2.4.1.1 "><p id="p48957164240"><a name="p48957164240"></a><a name="p48957164240"></a>group</p>
</td>
<td class="cellrowborder" valign="top" width="22.74%" headers="mcps1.2.4.1.2 "><p id="p18895191612415"><a name="p18895191612415"></a><a name="p18895191612415"></a>DLI程序包组</p>
</td>
<td class="cellrowborder" valign="top" width="59.489999999999995%" headers="mcps1.2.4.1.3 "><p id="p2895191612411"><a name="p2895191612411"></a><a name="p2895191612411"></a>groups.groupname</p>
</td>
</tr>
<tr id="row1466512915114"><td class="cellrowborder" valign="top" width="17.77%" headers="mcps1.2.4.1.1 "><p id="p184415322519"><a name="p184415322519"></a><a name="p184415322519"></a>datasourceauth</p>
</td>
<td class="cellrowborder" valign="top" width="22.74%" headers="mcps1.2.4.1.2 "><p id="p4131193710306"><a name="p4131193710306"></a><a name="p4131193710306"></a>DLI跨源认证信息</p>
</td>
<td class="cellrowborder" valign="top" width="59.489999999999995%" headers="mcps1.2.4.1.3 "><p id="p266618125317"><a name="p266618125317"></a><a name="p266618125317"></a>datasourceauth.name</p>
</td>
</tr>
</tbody>
</table>

