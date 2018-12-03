# DLI Beeline支持的命令行选项<a name="dli_01_0281"></a>

DLI Beeline支持的启动命令行选项请参考[表1](#table65880635152220)。

**表 1**  DLI Beeline支持的启动命令行选项

<a name="table65880635152220"></a>
<table><thead align="left"><tr id="row37154795152220"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p12623506152244"><a name="p12623506152244"></a><a name="p12623506152244"></a><strong id="b53165773152334"><a name="b53165773152334"></a><a name="b53165773152334"></a>命令行选项</strong></p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p15871098152244"><a name="p15871098152244"></a><a name="p15871098152244"></a><strong id="b38684688152248"><a name="b38684688152248"></a><a name="b38684688152248"></a>描述</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row1671668115232"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p4302842115232"><a name="p4302842115232"></a><a name="p4302842115232"></a>-u &lt;database URL&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p5124101233315"><a name="p5124101233315"></a><a name="p5124101233315"></a>连接DLI JDBC的url，其中url需要采用单引号括起来。使用方式：</p>
<p id="p6275003715232"><a name="p6275003715232"></a><a name="p6275003715232"></a><b><span class="cmdname" id="cmdname0557183619330"><a name="cmdname0557183619330"></a><a name="cmdname0557183619330"></a>beeline –u db_URL</span></b></p>
</td>
</tr>
<tr id="row5405319215232"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p5722201815232"><a name="p5722201815232"></a><a name="p5722201815232"></a>-e &lt;query&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p447192015232"><a name="p447192015232"></a><a name="p447192015232"></a>需要执行的SQL语句,可以输入多条语句，以分号间隔，语句需要采用单引号括起来。</p>
</td>
</tr>
<tr id="row1346245015232"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p3880466515232"><a name="p3880466515232"></a><a name="p3880466515232"></a>-f &lt;file&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p5617012415232"><a name="p5617012415232"></a><a name="p5617012415232"></a>需要执行的脚本文件。</p>
</td>
</tr>
<tr id="row895236815232"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1161405215232"><a name="p1161405215232"></a><a name="p1161405215232"></a>--dliconf property=value</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p121413615232"><a name="p121413615232"></a><a name="p121413615232"></a>待设置的DLI属性。</p>
</td>
</tr>
<tr id="row845124815232"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1269020915232"><a name="p1269020915232"></a><a name="p1269020915232"></a>--property-file=&lt;property-file&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p2127401515232"><a name="p2127401515232"></a><a name="p2127401515232"></a>通过指定的方式获取连接属性文件并连接到DLI服务。</p>
</td>
</tr>
<tr id="row2330864815232"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p661007015232"><a name="p661007015232"></a><a name="p661007015232"></a>--help</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p6565362415232"><a name="p6565362415232"></a><a name="p6565362415232"></a>打印命令行选项帮助。</p>
</td>
</tr>
</tbody>
</table>

