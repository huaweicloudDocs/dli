# 创建Flink SQL作业<a name="dli_01_0455"></a>

本章节介绍如何新建Flink SQL作业。Flink SQL是一种由用户根据自己的逻辑需求编写作业的方式。用SQL表达业务逻辑，可以简便快捷的实现业务。目前Flink SQL作业支持两种Flink SQL语句编辑方式：SQL编辑器和可视化编辑器。本章节主要介绍使用SQL编辑器编写Flink SQL作业的方式。

关于可视化编辑器的介绍请参见[可视化编辑器](可视化编辑器.md)。

## 前提条件<a name="section9243114805018"></a>

创建Flink SQL作业时，需要事先准备数据源以及数据输出通道，具体内容请参见[准备数据](准备数据.md)。

## 操作步骤<a name="section28145411519"></a>

1.  在DLI管理控制台的左侧导航栏中，单击“作业管理“\>“Flink作业“，进入“Flink作业“页面。
2.  在“Flink作业“页面右上角单击“新建作业“，弹出“新建作业“对话框。

    **图 1**  新建Flink SQL作业<a name="fig33241940467"></a>  
    ![](figures/新建Flink-SQL作业.png "新建Flink-SQL作业")

3.  配置作业信息。

    **表 1**  作业配置信息

    <a name="table153641658144118"></a>
    <table><thead align="left"><tr id="row43591258104111"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.3.1.1"><p id="p16359125844114"><a name="p16359125844114"></a><a name="p16359125844114"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="80%" id="mcps1.2.3.1.2"><p id="p16359205812417"><a name="p16359205812417"></a><a name="p16359205812417"></a>参数说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row16360958134110"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p173601258144118"><a name="p173601258144118"></a><a name="p173601258144118"></a>类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p236016585419"><a name="p236016585419"></a><a name="p236016585419"></a>Flink SQL作业：用户采用编辑SQL语句来启动作业。</p>
    </td>
    </tr>
    <tr id="row18361135814119"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p113601858194116"><a name="p113601858194116"></a><a name="p113601858194116"></a>名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p0360185884112"><a name="p0360185884112"></a><a name="p0360185884112"></a>作业名称，只能由字母、中文、数字、中划线和下划线组成，并且长度为1～57字节。</p>
    <div class="note" id="note133611758114113"><a name="note133611758114113"></a><a name="note133611758114113"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1836116582413"><a name="p1836116582413"></a><a name="p1836116582413"></a>作业名称必须是唯一的。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row93625589418"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p183619581415"><a name="p183619581415"></a><a name="p183619581415"></a>描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p17362758174118"><a name="p17362758174118"></a><a name="p17362758174118"></a>作业的相关描述，长度为0～512字节。</p>
    </td>
    </tr>
    <tr id="row936416582415"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p14362135844120"><a name="p14362135844120"></a><a name="p14362135844120"></a>编辑器</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p63641258114114"><a name="p63641258114114"></a><a name="p63641258114114"></a>支持<span class="parmvalue" id="parmvalue1736265817414"><a name="parmvalue1736265817414"></a><a name="parmvalue1736265817414"></a>“SQL编辑器”</span>和<span class="parmvalue" id="parmvalue4362658194111"><a name="parmvalue4362658194111"></a><a name="parmvalue4362658194111"></a>“可视化编辑器”</span>，默认选择<span class="parmvalue" id="parmvalue10364758194110"><a name="parmvalue10364758194110"></a><a name="parmvalue10364758194110"></a>“SQL编辑器”</span>。</p>
    </td>
    </tr>
    <tr id="row53646587415"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p2364958104115"><a name="p2364958104115"></a><a name="p2364958104115"></a>模板</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p136435815417"><a name="p136435815417"></a><a name="p136435815417"></a>当编辑器选择<span class="parmvalue" id="parmvalue83644587419"><a name="parmvalue83644587419"></a><a name="parmvalue83644587419"></a>“SQL编辑器”</span>时，该参数有效。</p>
    <p id="p15364458144115"><a name="p15364458144115"></a><a name="p15364458144115"></a>用户可以选择样例模板或自定义的作业模板。关于模板的详细信息，请参见<a href="Flink模板管理.md">Flink模板管理</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

4.  单击“确认“，进入作业“编辑“页面。
5.  编辑作业。

    **图 2**  作业编辑<a name="fig3464194555517"></a>  
    ![](figures/作业编辑.png "作业编辑")

    在SQL语句编辑区域，输入详细的SQL语句。相关SQL语句请参考[《数据湖探索SQL语法参考》](https://support.huaweicloud.com/sqlreference-dli/dli_08_0219.html)。

6.  单击“语义校验“，确保语义校验成功。
    -   只有语义校验成功后，才可以执行“调试“或“提交“作业的操作。
    -   如果校验成功，提示“SQL语义校验成功”。
    -   如果校验失败，会在错误的SQL语句前面显示红色的“X”记号，鼠标移动到“X”号上可查看详细错误，请根据错误提示修改SQL语句。

7.  设置作业运行参数。

    **图 3**  设置Flink SQL作业运行参数<a name="fig329324084817"></a>  
    ![](figures/设置Flink-SQL作业运行参数.png "设置Flink-SQL作业运行参数")

    **表 2**  作业运行参数说明

    <a name="table122291210192018"></a>
    <table><thead align="left"><tr id="row9220121016203"><th class="cellrowborder" valign="top" width="22.189999999999998%" id="mcps1.2.3.1.1"><p id="p18220131016207"><a name="p18220131016207"></a><a name="p18220131016207"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="77.81%" id="mcps1.2.3.1.2"><p id="p1322061019206"><a name="p1322061019206"></a><a name="p1322061019206"></a>参数说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1922015100201"><td class="cellrowborder" valign="top" width="22.189999999999998%" headers="mcps1.2.3.1.1 "><p id="p3220610102011"><a name="p3220610102011"></a><a name="p3220610102011"></a>CUs</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.81%" headers="mcps1.2.3.1.2 "><p id="p1722091013204"><a name="p1722091013204"></a><a name="p1722091013204"></a>CUs为DLI计费单位，1核4G的资源配置。</p>
    </td>
    </tr>
    <tr id="row192221910132017"><td class="cellrowborder" valign="top" width="22.189999999999998%" headers="mcps1.2.3.1.1 "><p id="p12220610192013"><a name="p12220610192013"></a><a name="p12220610192013"></a>并行数</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.81%" headers="mcps1.2.3.1.2 "><p id="p52201810162014"><a name="p52201810162014"></a><a name="p52201810162014"></a>并行数是指同时运行Flink SQL作业的任务数。</p>
    <div class="note" id="note9222131016207"><a name="note9222131016207"></a><a name="note9222131016207"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p52221810162013"><a name="p52221810162013"></a><a name="p52221810162013"></a>并行数不能大于计算单元（CUs-1）的4倍。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row322751016206"><td class="cellrowborder" valign="top" width="22.189999999999998%" headers="mcps1.2.3.1.1 "><p id="p1522251012200"><a name="p1522251012200"></a><a name="p1522251012200"></a>开启Checkpoint</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.81%" headers="mcps1.2.3.1.2 "><p id="p7222191002017"><a name="p7222191002017"></a><a name="p7222191002017"></a>设置是否开启作业快照，开启后可基于Checkpoint（一致性检查点）恢复作业。</p>
    <div class="p" id="p2226131010208"><a name="p2226131010208"></a><a name="p2226131010208"></a>如下两个参数是勾选<span class="uicontrol" id="uicontrol32221510132020"><a name="uicontrol32221510132020"></a><a name="uicontrol32221510132020"></a>“开启Checkpoint”</span>后有效：<a name="ul1922641017209"></a><a name="ul1922641017209"></a><ul id="ul1922641017209"><li>Checkpoint间隔：Checkpoint的时间间隔，单位为秒，输入范围 1~999999，默认值为10s。</li><li>Checkpoint 模式：支持如下两种模式：<a name="ul1022611017200"></a><a name="ul1022611017200"></a><ul id="ul1022611017200"><li>AtLeastOnce：事件至少被处理一次。</li><li>ExactlyOnce：事件仅被处理一次。</li></ul>
    </li></ul>
    </div>
    </td>
    </tr>
    <tr id="row12227171052018"><td class="cellrowborder" valign="top" width="22.189999999999998%" headers="mcps1.2.3.1.1 "><p id="p122741014207"><a name="p122741014207"></a><a name="p122741014207"></a>保存作业日志</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.81%" headers="mcps1.2.3.1.2 "><div class="p" id="p822731020204"><a name="p822731020204"></a><a name="p822731020204"></a>设置是否将作业运行时的日志信息保存到OBS。<div class="note" id="note13227161015208"><a name="note13227161015208"></a><a name="note13227161015208"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p9227171092019"><a name="p9227171092019"></a><a name="p9227171092019"></a>如果同时勾选了<span class="uicontrol" id="uicontrol1522701012202"><a name="uicontrol1522701012202"></a><a name="uicontrol1522701012202"></a>“开启Checkpoint”</span>和<span class="uicontrol" id="uicontrol22271410172014"><a name="uicontrol22271410172014"></a><a name="uicontrol22271410172014"></a>“保存作业日志”</span>，OBS授权一次即可。</p>
    </div></div>
    </div>
    </td>
    </tr>
    <tr id="row1922816108200"><td class="cellrowborder" valign="top" width="22.189999999999998%" headers="mcps1.2.3.1.1 "><p id="p17227510152015"><a name="p17227510152015"></a><a name="p17227510152015"></a>OBS桶</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.81%" headers="mcps1.2.3.1.2 "><p id="p82281010112018"><a name="p82281010112018"></a><a name="p82281010112018"></a>当勾选<span class="parmname" id="parmname14228201018202"><a name="parmname14228201018202"></a><a name="parmname14228201018202"></a>“开启Checkpoint”</span>或<span class="parmname" id="parmname422820104209"><a name="parmname422820104209"></a><a name="parmname422820104209"></a>“保存作业日志”</span>时，该参数有效。</p>
    <p id="p1228151015201"><a name="p1228151015201"></a><a name="p1228151015201"></a>选择OBS桶用于保存用户Checkpoint和作业日志信息。</p>
    <p id="p522819107206"><a name="p522819107206"></a><a name="p522819107206"></a>如果选择的OBS桶是未授权状态，需要单击<span class="uicontrol" id="uicontrol11228141002017"><a name="uicontrol11228141002017"></a><a name="uicontrol11228141002017"></a>“OBS授权”</span>。</p>
    </td>
    </tr>
    <tr id="row1788112311913"><td class="cellrowborder" valign="top" width="22.189999999999998%" headers="mcps1.2.3.1.1 "><p id="p1178862351913"><a name="p1178862351913"></a><a name="p1178862351913"></a>作业异常告警</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.81%" headers="mcps1.2.3.1.2 "><p id="p7788172313199"><a name="p7788172313199"></a><a name="p7788172313199"></a>设置是否将作业异常告警信息，如作业出现运行异常或者欠费情况，以SMN的方式通知用户。</p>
    </td>
    </tr>
    <tr id="row1756231145112"><td class="cellrowborder" valign="top" width="22.189999999999998%" headers="mcps1.2.3.1.1 "><p id="p077653010246"><a name="p077653010246"></a><a name="p077653010246"></a>主题名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.81%" headers="mcps1.2.3.1.2 "><p id="p2776103042418"><a name="p2776103042418"></a><a name="p2776103042418"></a>当勾选<span class="parmname" id="parmname12851183392517"><a name="parmname12851183392517"></a><a name="parmname12851183392517"></a>“开启作业异常告警”</span>时，该参数有效。</p>
    <p id="p31481256122518"><a name="p31481256122518"></a><a name="p31481256122518"></a>选择一个自定义的SMN主题。如何自定义SMN主题，请参见<a href="https://support.huaweicloud.com/smn/index.html" target="_blank" rel="noopener noreferrer">《消息通知服务用户指南》</a>中<span class="filepath" id="filepath1056574617338"><a name="filepath1056574617338"></a><a name="filepath1056574617338"></a>“创建主题”</span>章节。</p>
    </td>
    </tr>
    <tr id="row1325629124615"><td class="cellrowborder" valign="top" width="22.189999999999998%" headers="mcps1.2.3.1.1 "><p id="p1326112954611"><a name="p1326112954611"></a><a name="p1326112954611"></a>异常自动重启</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.81%" headers="mcps1.2.3.1.2 "><p id="p43261629114616"><a name="p43261629114616"></a><a name="p43261629114616"></a>设置是否启动异常自动重启功能，当作业异常时将自动重启并恢复作业。</p>
    </td>
    </tr>
    <tr id="row421610457473"><td class="cellrowborder" valign="top" width="22.189999999999998%" headers="mcps1.2.3.1.1 "><p id="p921774514475"><a name="p921774514475"></a><a name="p921774514475"></a>空闲状态保留时长</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.81%" headers="mcps1.2.3.1.2 "><p id="p1521716451473"><a name="p1521716451473"></a><a name="p1521716451473"></a>用于清除GroupBy或Window经过最大保留时间后仍未更新的中间状态，默认设置为1小时。</p>
    </td>
    </tr>
    <tr id="row060951717141"><td class="cellrowborder" valign="top" width="22.189999999999998%" headers="mcps1.2.3.1.1 "><p id="p126091517171414"><a name="p126091517171414"></a><a name="p126091517171414"></a>脏数据策略</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.81%" headers="mcps1.2.3.1.2 "><p id="p146091173141"><a name="p146091173141"></a><a name="p146091173141"></a>选择处理脏数据的策略。支持如下三种策略：忽略，抛出异常和保存脏数据到OBS。默认选择忽略。</p>
    </td>
    </tr>
    <tr id="row112293102204"><td class="cellrowborder" valign="top" width="22.189999999999998%" headers="mcps1.2.3.1.1 "><p id="p12291910132014"><a name="p12291910132014"></a><a name="p12291910132014"></a>作业所属队列</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.81%" headers="mcps1.2.3.1.2 "><p id="p72291810132012"><a name="p72291810132012"></a><a name="p72291810132012"></a>默认选择<span class="parmvalue" id="parmvalue12292103206"><a name="parmvalue12292103206"></a><a name="parmvalue12292103206"></a>“共享队列”</span>，用户也可以选择自定义的独享队列。</p>
    <div class="note" id="note126945231017"><a name="note126945231017"></a><a name="note126945231017"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p11408165613126"><a name="p11408165613126"></a><a name="p11408165613126"></a>当子用户在创建作业时，子用户只能选择已经被分配的队列。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row13260161215"><td class="cellrowborder" valign="top" width="22.189999999999998%" headers="mcps1.2.3.1.1 "><p id="p17900175112265"><a name="p17900175112265"></a><a name="p17900175112265"></a>UDF Jar</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.81%" headers="mcps1.2.3.1.2 "><p id="p98321338147"><a name="p98321338147"></a><a name="p98321338147"></a>当作业所属集群选择独享集群时，该参数有效。在选择UDF Jar之前需要将对应的jar包上传至OBS桶中，并在<span class="menucascade" id="menucascade132601332513"><a name="menucascade132601332513"></a><a name="menucascade132601332513"></a>“<span class="uicontrol" id="uicontrol13260930514"><a name="uicontrol13260930514"></a><a name="uicontrol13260930514"></a>数据管理&gt;程序包管理</span>”</span>中创建程序包，具体操作请参考<a href="创建程序包.md">创建程序包</a>。</p>
    <p id="p85110151218"><a name="p85110151218"></a><a name="p85110151218"></a>用户可以在SQL中调用插入Jar包中的自定义函数。</p>
    <p id="p4151757171810"><a name="p4151757171810"></a><a name="p4151757171810"></a>关于自定义函数的详细内容，请参见《<a href="https://support.huaweicloud.com/sqlreference-dli/dli_08_0099.html" target="_blank" rel="noopener noreferrer">数据湖探索SQL语法参考</a>》。</p>
    </td>
    </tr>
    </tbody>
    </table>

8.  单击“保存“，保存作业和相关参数。
9.  单击“提交“，进入“作业配置清单“页面，单击“确认“，将作业提交并启动。

    提交作业后，系统将自动跳转到Flink作业管理页面，新创建的作业将显示在作业列表中，在“状态“列中可以查看作业状态。作业提交成功后，状态将由“提交中“变为“运行中“。运行完成后显示“已完成”。

    如果作业状态为“提交失败“或“运行异常“，表示作业提交或运行失败。用户可以在作业列表中的“状态“列中，将鼠标移动到状态图标上查看错误信息，单击![](figures/icon-cs-copy.png)可以复制错误信息。根据错误信息解决故障后，重新提交。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >其他功能按钮说明如下：  
    >-   调试：对作业进行调试。具体操作请参见[调试作业](调试作业.md)。  
    >-   SQL格式化：将SQL格式化，将SQL语句格式化后，需要重新编辑SQL语句。  
    >-   更多 \> 名称和描述修改：修改作业名称和描述。  
    >-   更多 \> 另存为：将新建作业另存为一个新作业。  
    >-   更多 \> 设为模板：将新创建的作业设置为作业模板。  
    >-   更多 \> 主题设置：设置页面主题，可以设置字体大小，自动换行和页面风格。  
    >-   更多 \> 帮助：跳转至帮助中心，为用户提供SQL语法参考。  


