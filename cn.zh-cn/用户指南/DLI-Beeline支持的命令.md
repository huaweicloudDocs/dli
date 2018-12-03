# DLI Beeline支持的命令<a name="dli_01_0280"></a>

DLI Beeline支持一系列命令，每个命令以 ！ 这个符号开始，例如!connect。具体请参考[表1](#table18133261151627)。

**表 1**  DLI Beeline支持的命令

<a name="table18133261151627"></a>
<table><thead align="left"><tr id="row59856934151627"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p9158444151639"><a name="p9158444151639"></a><a name="p9158444151639"></a><strong id="b65940620151647"><a name="b65940620151647"></a><a name="b65940620151647"></a>命令</strong></p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p3636489151639"><a name="p3636489151639"></a><a name="p3636489151639"></a><strong id="b39589998151647"><a name="b39589998151647"></a><a name="b39589998151647"></a>描述</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row1892907715175"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p3012072215175"><a name="p3012072215175"></a><a name="p3012072215175"></a>!connect</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p2385943615175"><a name="p2385943615175"></a><a name="p2385943615175"></a>通过输入连接参数的方式连接到DLI服务，若不输入参数，则加载默认的“connection.properties”文件连接。</p>
</td>
</tr>
<tr id="row210323015175"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1233334215175"><a name="p1233334215175"></a><a name="p1233334215175"></a>!help</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p5947667015175"><a name="p5947667015175"></a><a name="p5947667015175"></a>打印命令行的帮助文档。</p>
</td>
</tr>
<tr id="row23369215175"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p616680015175"><a name="p616680015175"></a><a name="p616680015175"></a>!history</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p2974875215175"><a name="p2974875215175"></a><a name="p2974875215175"></a>展示命令行执行历史。</p>
</td>
</tr>
<tr id="row5222174815175"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1067725115175"><a name="p1067725115175"></a><a name="p1067725115175"></a>!outputformat</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p5955098915175"><a name="p5955098915175"></a><a name="p5955098915175"></a>设置查询结果的输出格式，支持table,vertical,csv2,dsv,tsv2,xmlattr,xmlelements，每一种格式的具体说明详参见<a href="查询输出格式.md">查询输出格式</a>。</p>
</td>
</tr>
<tr id="row5799819915175"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p6034537315175"><a name="p6034537315175"></a><a name="p6034537315175"></a>!properties</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p5613706815175"><a name="p5613706815175"></a><a name="p5613706815175"></a>通过加载“connection.properties”文件连接到DLI服务。该功能与!connect相同，但是可以指定连接配置文件。</p>
</td>
</tr>
<tr id="row5864002715175"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p5462471615175"><a name="p5462471615175"></a><a name="p5462471615175"></a>!quit</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p6252586515175"><a name="p6252586515175"></a><a name="p6252586515175"></a>退出beeline会话。</p>
</td>
</tr>
<tr id="row2142863915175"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1443712415175"><a name="p1443712415175"></a><a name="p1443712415175"></a>!run</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p2855636115175"><a name="p2855636115175"></a><a name="p2855636115175"></a>执行一个SQL脚本。使用方法：</p>
<p id="p5568065815175"><a name="p5568065815175"></a><a name="p5568065815175"></a><i><b><span class="cmdname" style="font-family:Arial" id="cmdname4889739091227"><a name="cmdname4889739091227"></a><a name="cmdname4889739091227"></a>!run &lt;scriptfile&gt;</span></b></i></p>
</td>
</tr>
<tr id="row4712020215175"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p5744654515175"><a name="p5744654515175"></a><a name="p5744654515175"></a>!save</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p2265853115175"><a name="p2265853115175"></a><a name="p2265853115175"></a>将当前的会话属性保存至beeline.properties中，下次开启beeline时会自动加载这些属性。</p>
</td>
</tr>
<tr id="row3506173915175"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p928905715175"><a name="p928905715175"></a><a name="p928905715175"></a>!script</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p29461927203018"><a name="p29461927203018"></a><a name="p29461927203018"></a>将执行的命令保存至一个文件中。例如：</p>
<p id="p1421616215175"><a name="p1421616215175"></a><a name="p1421616215175"></a><i><b><span class="cmdname" style="font-family:Arial" id="cmdname267781059125"><a name="cmdname267781059125"></a><a name="cmdname267781059125"></a>!script /tmp/mysession.script</span></b></i></p>
<p id="p1065847515175"><a name="p1065847515175"></a><a name="p1065847515175"></a>执行该语句之后，后续的命令将被保存至“/tmp/mysession.script”。</p>
<p id="p2881741915175"><a name="p2881741915175"></a><a name="p2881741915175"></a>再次执行!script，结束脚本记录。执行如下语句，将会重新执行记录下来的命令。</p>
<p id="p1684052614316"><a name="p1684052614316"></a><a name="p1684052614316"></a><i><b><span class="cmdname" style="font-family:Arial" id="cmdname5953542391047"><a name="cmdname5953542391047"></a><a name="cmdname5953542391047"></a>!run /tmp/mysession.script</span></b></i></p>
</td>
</tr>
<tr id="row2626537015175"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p2541823415175"><a name="p2541823415175"></a><a name="p2541823415175"></a>!set</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p390911335312"><a name="p390911335312"></a><a name="p390911335312"></a>设置Beeline变量，例如：</p>
<p id="p85556479316"><a name="p85556479316"></a><a name="p85556479316"></a><i><b><span class="cmdname" style="font-family:Arial" id="cmdname181038091126"><a name="cmdname181038091126"></a><a name="cmdname181038091126"></a>!set color true</span></b></i></p>
<p id="p4561104415175"><a name="p4561104415175"></a><a name="p4561104415175"></a>!set后面不接参数则显示所有变量值。</p>
</td>
</tr>
<tr id="row4020107615175"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1563696615175"><a name="p1563696615175"></a><a name="p1563696615175"></a>!sh</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p310311133215"><a name="p310311133215"></a><a name="p310311133215"></a>执行一个Shell脚本。例如：</p>
<p id="p220063059104"><a name="p220063059104"></a><a name="p220063059104"></a><i><b><span class="cmdname" style="font-family:Arial" id="cmdname1220143791113"><a name="cmdname1220143791113"></a><a name="cmdname1220143791113"></a>!sh &lt;shellscript&gt;</span></b></i></p>
</td>
</tr>
<tr id="row446678615175"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p3426974615175"><a name="p3426974615175"></a><a name="p3426974615175"></a>!sql</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p434131418324"><a name="p434131418324"></a><a name="p434131418324"></a>显性地执行一条SQL语句，beeline中不带命令的语句默认会转换成!sql命令，sql语句必须以分号结尾。例如：</p>
<p id="p241261619958"><a name="p241261619958"></a><a name="p241261619958"></a><i><b><span class="cmdname" style="font-family:Arial" id="cmdname172274539117"><a name="cmdname172274539117"></a><a name="cmdname172274539117"></a>!sql &lt;sql&gt;</span></b></i></p>
</td>
</tr>
<tr id="row795285015175"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p932731915175"><a name="p932731915175"></a><a name="p932731915175"></a>!dliconf</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1731537815175"><a name="p1731537815175"></a><a name="p1731537815175"></a>查看DLI 自定义配置。</p>
</td>
</tr>
</tbody>
</table>

