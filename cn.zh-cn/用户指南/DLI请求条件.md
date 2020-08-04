# DLI请求条件<a name="dli_01_0475"></a>

您可以在创建自定义策略时，通过添加“请求条件”（Condition元素）来控制策略何时生效。请求条件包括条件键和运算符，条件键表示策略语句的 Condition 元素，分为全局级条件键和服务级条件键。[全局级条件键](https://support.huaweicloud.com/usermanual-iam/iam_01_0017.html)（前缀为g:）适用于所有操作，服务级条件键（前缀为服务缩写，如dli）仅适用于对应服务的操作。运算符与条件键一起使用，构成完整的条件判断语句。

DLI通过IAM预置了一组条件键，例如，您可以先使用hw:SourceIp条件键检查请求者的IP地址，然后再允许执行操作。下表显示了适用于DLI服务特定的条件键。

**表 1**  DLI请求条件

<a name="table198664321589"></a>
<table><thead align="left"><tr id="row1538733145813"><th class="cellrowborder" valign="top" width="25.509999999999998%" id="mcps1.2.4.1.1"><p id="p338173325815"><a name="p338173325815"></a><a name="p338173325815"></a>DLI条件键</p>
</th>
<th class="cellrowborder" valign="top" width="25.28%" id="mcps1.2.4.1.2"><p id="p738933175812"><a name="p738933175812"></a><a name="p738933175812"></a>运算符</p>
</th>
<th class="cellrowborder" valign="top" width="49.21%" id="mcps1.2.4.1.3"><p id="p17398335586"><a name="p17398335586"></a><a name="p17398335586"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row143919330583"><td class="cellrowborder" valign="top" width="25.509999999999998%" headers="mcps1.2.4.1.1 "><p id="p19919142173917"><a name="p19919142173917"></a><a name="p19919142173917"></a>g:CurrentTime</p>
</td>
<td class="cellrowborder" valign="top" width="25.28%" headers="mcps1.2.4.1.2 "><p id="p155913814012"><a name="p155913814012"></a><a name="p155913814012"></a>Date and time</p>
</td>
<td class="cellrowborder" valign="top" width="49.21%" headers="mcps1.2.4.1.3 "><p id="p17727152964018"><a name="p17727152964018"></a><a name="p17727152964018"></a>接收到鉴权请求的时间。</p>
<div class="note" id="note1351115310408"><a name="note1351115310408"></a><a name="note1351115310408"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1261205354015"><a name="p1261205354015"></a><a name="p1261205354015"></a>以<span class="parmname" id="parmname129181181071"><a name="parmname129181181071"></a><a name="parmname129181181071"></a>“ISO 8601”</span>格式表示，例如：2012-11-11T23:59:59Z。</p>
</div></div>
</td>
</tr>
<tr id="row3745155113913"><td class="cellrowborder" valign="top" width="25.509999999999998%" headers="mcps1.2.4.1.1 "><p id="p16919152112397"><a name="p16919152112397"></a><a name="p16919152112397"></a>g:MFAPresent</p>
</td>
<td class="cellrowborder" valign="top" width="25.28%" headers="mcps1.2.4.1.2 "><p id="p056013824016"><a name="p056013824016"></a><a name="p056013824016"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="49.21%" headers="mcps1.2.4.1.3 "><p id="p672712912402"><a name="p672712912402"></a><a name="p672712912402"></a>用户登录时是否使用了多因素认证。</p>
</td>
</tr>
<tr id="row14691705398"><td class="cellrowborder" valign="top" width="25.509999999999998%" headers="mcps1.2.4.1.1 "><p id="p12919321193915"><a name="p12919321193915"></a><a name="p12919321193915"></a>g:UserId</p>
</td>
<td class="cellrowborder" valign="top" width="25.28%" headers="mcps1.2.4.1.2 "><p id="p456015854016"><a name="p456015854016"></a><a name="p456015854016"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.21%" headers="mcps1.2.4.1.3 "><p id="p172782916402"><a name="p172782916402"></a><a name="p172782916402"></a>当前登录的用户ID。</p>
</td>
</tr>
<tr id="row836712155397"><td class="cellrowborder" valign="top" width="25.509999999999998%" headers="mcps1.2.4.1.1 "><p id="p5919162113919"><a name="p5919162113919"></a><a name="p5919162113919"></a>g:UserName</p>
</td>
<td class="cellrowborder" valign="top" width="25.28%" headers="mcps1.2.4.1.2 "><p id="p3560488402"><a name="p3560488402"></a><a name="p3560488402"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.21%" headers="mcps1.2.4.1.3 "><p id="p13727129144018"><a name="p13727129144018"></a><a name="p13727129144018"></a>当前登录的用户名。</p>
</td>
</tr>
<tr id="row15368315143920"><td class="cellrowborder" valign="top" width="25.509999999999998%" headers="mcps1.2.4.1.1 "><p id="p991912214397"><a name="p991912214397"></a><a name="p991912214397"></a>g:ProjectName</p>
</td>
<td class="cellrowborder" valign="top" width="25.28%" headers="mcps1.2.4.1.2 "><p id="p4560178124011"><a name="p4560178124011"></a><a name="p4560178124011"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.21%" headers="mcps1.2.4.1.3 "><p id="p9727729194010"><a name="p9727729194010"></a><a name="p9727729194010"></a>当前登录的Project。</p>
</td>
</tr>
<tr id="row136916154397"><td class="cellrowborder" valign="top" width="25.509999999999998%" headers="mcps1.2.4.1.1 "><p id="p159190217393"><a name="p159190217393"></a><a name="p159190217393"></a>g:DomainName</p>
</td>
<td class="cellrowborder" valign="top" width="25.28%" headers="mcps1.2.4.1.2 "><p id="p15560889409"><a name="p15560889409"></a><a name="p15560889409"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.21%" headers="mcps1.2.4.1.3 "><p id="p07271829124010"><a name="p07271829124010"></a><a name="p07271829124010"></a>当前登录的Domain。</p>
</td>
</tr>
</tbody>
</table>

