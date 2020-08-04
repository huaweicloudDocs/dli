# 提交SQL作业（推荐）<a name="dli_02_0102"></a>

## 功能介绍<a name="s51df1f9bf4784cf4a56c09b3973a2adc"></a>

该API用于通过执行SQL语句的方式向队列提交作业。

作业包含以下类型：DDL、DCL、IMPORT、QUERY和INSERT。其中，IMPORT与[导入数据](导入数据.md)的功能一致，区别仅在于实现方式不同。

另外，用户可使用其他API来对作业进行查询和管理。具体操作有：

-   [查询作业状态](查询作业状态.md)
-   [查询作业详细信息](查询作业详细信息.md)
-   [查询作业结果（推荐）](查询作业结果（推荐）.md)
-   [导出查询结果](导出查询结果.md)
-   [查询所有作业](查询所有作业.md)
-   [取消作业（推荐）](取消作业（推荐）.md)

>![](public_sys-resources/icon-note.gif) **说明：** 
>该API当响应消息中“job\_type“为“DCL“时，为同步操作。

## URI<a name="s807a09edd221483999c7c51233072a4a"></a>

-   URI格式：

    POST /v1.0/\{project\_id\}/jobs/submit-job

-   参数说明

    **表 1**  URI参数

    <a name="zh-cn_topic_0069077806_table9770605"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0069077806_row35653836"><th class="cellrowborder" valign="top" width="11.881188118811881%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0069077806_p14983541266"><a name="zh-cn_topic_0069077806_p14983541266"></a><a name="zh-cn_topic_0069077806_p14983541266"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="13.8019801980198%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0069077806_p9981547619"><a name="zh-cn_topic_0069077806_p9981547619"></a><a name="zh-cn_topic_0069077806_p9981547619"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="74.31683168316832%" id="mcps1.2.4.1.3"><p id="a9de737854caf4be3a07db76909948f18"><a name="a9de737854caf4be3a07db76909948f18"></a><a name="a9de737854caf4be3a07db76909948f18"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row5320171434012"><td class="cellrowborder" valign="top" width="11.881188118811881%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0069077803_p43412436"><a name="zh-cn_topic_0069077803_p43412436"></a><a name="zh-cn_topic_0069077803_p43412436"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.8019801980198%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0069077803_p26746391"><a name="zh-cn_topic_0069077803_p26746391"></a><a name="zh-cn_topic_0069077803_p26746391"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.31683168316832%" headers="mcps1.2.4.1.3 "><p id="p1310472724012"><a name="p1310472724012"></a><a name="p1310472724012"></a>项目编号，用于资源隔离。获取方式请参考<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="s46f967e8024f453cb6cd43f3af264950"></a>

**表 2**  请求参数

<a name="table6376584143542"></a>
<table><thead align="left"><tr id="row19110893143542"><th class="cellrowborder" valign="top" width="14.549999999999999%" id="mcps1.2.5.1.1"><p id="p42934984143542"><a name="p42934984143542"></a><a name="p42934984143542"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.79%" id="mcps1.2.5.1.2"><p id="p55181642143542"><a name="p55181642143542"></a><a name="p55181642143542"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="16.3%" id="mcps1.2.5.1.3"><p id="p40528033143542"><a name="p40528033143542"></a><a name="p40528033143542"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="58.36%" id="mcps1.2.5.1.4"><p id="p61545269143542"><a name="p61545269143542"></a><a name="p61545269143542"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row16818917143542"><td class="cellrowborder" valign="top" width="14.549999999999999%" headers="mcps1.2.5.1.1 "><p id="p4478514143542"><a name="p4478514143542"></a><a name="p4478514143542"></a>sql</p>
</td>
<td class="cellrowborder" valign="top" width="10.79%" headers="mcps1.2.5.1.2 "><p id="p27215339143542"><a name="p27215339143542"></a><a name="p27215339143542"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="16.3%" headers="mcps1.2.5.1.3 "><p id="p56958849143542"><a name="p56958849143542"></a><a name="p56958849143542"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="58.36%" headers="mcps1.2.5.1.4 "><p id="p1036145143542"><a name="p1036145143542"></a><a name="p1036145143542"></a>待执行的SQL语句。</p>
</td>
</tr>
<tr id="row48821488143542"><td class="cellrowborder" valign="top" width="14.549999999999999%" headers="mcps1.2.5.1.1 "><p id="p17152532143542"><a name="p17152532143542"></a><a name="p17152532143542"></a>currentdb</p>
</td>
<td class="cellrowborder" valign="top" width="10.79%" headers="mcps1.2.5.1.2 "><p id="p47177872143542"><a name="p47177872143542"></a><a name="p47177872143542"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.3%" headers="mcps1.2.5.1.3 "><p id="p63311321143542"><a name="p63311321143542"></a><a name="p63311321143542"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="58.36%" headers="mcps1.2.5.1.4 "><p id="p27943382143542"><a name="p27943382143542"></a><a name="p27943382143542"></a>SQL语句执行所在的数据库。当创建新数据库时，不需要提供此参数。</p>
</td>
</tr>
<tr id="row47659205154318"><td class="cellrowborder" valign="top" width="14.549999999999999%" headers="mcps1.2.5.1.1 "><p id="p1846530915443"><a name="p1846530915443"></a><a name="p1846530915443"></a>queue_name</p>
</td>
<td class="cellrowborder" valign="top" width="10.79%" headers="mcps1.2.5.1.2 "><p id="p3009358515443"><a name="p3009358515443"></a><a name="p3009358515443"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.3%" headers="mcps1.2.5.1.3 "><p id="p6674625215443"><a name="p6674625215443"></a><a name="p6674625215443"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="58.36%" headers="mcps1.2.5.1.4 "><p id="p32836715443"><a name="p32836715443"></a><a name="p32836715443"></a>待提交作业的队列名称，名称只能包含数字、英文字母和下划线，但不能是纯数字，且不能以下划线开头。</p>
</td>
</tr>
<tr id="row57451725143542"><td class="cellrowborder" valign="top" width="14.549999999999999%" headers="mcps1.2.5.1.1 "><p id="p36740211143542"><a name="p36740211143542"></a><a name="p36740211143542"></a>conf</p>
</td>
<td class="cellrowborder" valign="top" width="10.79%" headers="mcps1.2.5.1.2 "><p id="p23167106143542"><a name="p23167106143542"></a><a name="p23167106143542"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.3%" headers="mcps1.2.5.1.3 "><p id="p64596322143542"><a name="p64596322143542"></a><a name="p64596322143542"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="58.36%" headers="mcps1.2.5.1.4 "><p id="p23997108143542"><a name="p23997108143542"></a><a name="p23997108143542"></a>用户以“key/value”的形式设置用于此作业的配置参数。目前支持的配置项请参考<a href="#table334825142314">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  conf参数说明

<a name="table334825142314"></a>
<table><thead align="left"><tr id="row66396519230"><th class="cellrowborder" valign="top" width="29.43%" id="mcps1.2.4.1.1"><p id="p463913514234"><a name="p463913514234"></a><a name="p463913514234"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="15.85%" id="mcps1.2.4.1.2"><p id="p2639158232"><a name="p2639158232"></a><a name="p2639158232"></a>默认值</p>
</th>
<th class="cellrowborder" valign="top" width="54.72%" id="mcps1.2.4.1.3"><p id="p1963920542313"><a name="p1963920542313"></a><a name="p1963920542313"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1363935122313"><td class="cellrowborder" valign="top" width="29.43%" headers="mcps1.2.4.1.1 "><p id="p56404542316"><a name="p56404542316"></a><a name="p56404542316"></a>spark.sql.files.maxRecordsPerFile</p>
</td>
<td class="cellrowborder" valign="top" width="15.85%" headers="mcps1.2.4.1.2 "><p id="p1864016519235"><a name="p1864016519235"></a><a name="p1864016519235"></a>0</p>
</td>
<td class="cellrowborder" valign="top" width="54.72%" headers="mcps1.2.4.1.3 "><p id="p186405592312"><a name="p186405592312"></a><a name="p186405592312"></a>要写入单个文件的最大记录数。如果该值为零或为负，则没有限制。</p>
</td>
</tr>
<tr id="row8640135142317"><td class="cellrowborder" valign="top" width="29.43%" headers="mcps1.2.4.1.1 "><p id="p664017510239"><a name="p664017510239"></a><a name="p664017510239"></a>spark.sql.autoBroadcastJoinThreshold</p>
</td>
<td class="cellrowborder" valign="top" width="15.85%" headers="mcps1.2.4.1.2 "><p id="p1664018542314"><a name="p1664018542314"></a><a name="p1664018542314"></a>209715200</p>
</td>
<td class="cellrowborder" valign="top" width="54.72%" headers="mcps1.2.4.1.3 "><p id="p15640157231"><a name="p15640157231"></a><a name="p15640157231"></a>配置执行连接时显示所有工作节点的表的最大字节大小。通过将此值设置为<span class="parmvalue" id="parmvalue10816165872414"><a name="parmvalue10816165872414"></a><a name="parmvalue10816165872414"></a>“-1”</span>，可以禁用显示。</p>
<div class="note" id="note1562136162513"><a name="note1562136162513"></a><a name="note1562136162513"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p166418366254"><a name="p166418366254"></a><a name="p166418366254"></a>当前仅支持运行命令<b><span class="cmdname" id="cmdname86941634172615"><a name="cmdname86941634172615"></a><a name="cmdname86941634172615"></a>ANALYZE TABLE COMPUTE statistics noscan</span></b>的配置单元元存储表，和直接根据数据文件计算统计信息的基于文件的数据源表。</p>
</div></div>
</td>
</tr>
<tr id="row364020522314"><td class="cellrowborder" valign="top" width="29.43%" headers="mcps1.2.4.1.1 "><p id="p146401254236"><a name="p146401254236"></a><a name="p146401254236"></a>spark.sql.shuffle.partitions</p>
</td>
<td class="cellrowborder" valign="top" width="15.85%" headers="mcps1.2.4.1.2 "><p id="p176409516238"><a name="p176409516238"></a><a name="p176409516238"></a>4096</p>
</td>
<td class="cellrowborder" valign="top" width="54.72%" headers="mcps1.2.4.1.3 "><p id="p186400514233"><a name="p186400514233"></a><a name="p186400514233"></a>为连接或聚合过滤数据时使用的默认分区数。</p>
</td>
</tr>
<tr id="row1664018513237"><td class="cellrowborder" valign="top" width="29.43%" headers="mcps1.2.4.1.1 "><p id="p464005132313"><a name="p464005132313"></a><a name="p464005132313"></a>spark.sql.dynamicPartitionOverwrite.enabled</p>
</td>
<td class="cellrowborder" valign="top" width="15.85%" headers="mcps1.2.4.1.2 "><p id="p4640185132312"><a name="p4640185132312"></a><a name="p4640185132312"></a>false</p>
</td>
<td class="cellrowborder" valign="top" width="54.72%" headers="mcps1.2.4.1.3 "><p id="p96408511235"><a name="p96408511235"></a><a name="p96408511235"></a>在动态模式下，Spark不会删除前面的分区，只覆盖那些运行时没有写入数据的分区。</p>
</td>
</tr>
<tr id="row56403510234"><td class="cellrowborder" valign="top" width="29.43%" headers="mcps1.2.4.1.1 "><p id="p106403522310"><a name="p106403522310"></a><a name="p106403522310"></a>spark.sql.files.maxPartitionBytes</p>
</td>
<td class="cellrowborder" valign="top" width="15.85%" headers="mcps1.2.4.1.2 "><p id="p9640175112311"><a name="p9640175112311"></a><a name="p9640175112311"></a>134217728</p>
</td>
<td class="cellrowborder" valign="top" width="54.72%" headers="mcps1.2.4.1.3 "><p id="p6640759237"><a name="p6640759237"></a><a name="p6640759237"></a>读取文件时要打包到单个分区中的最大字节数。</p>
</td>
</tr>
<tr id="row1364118532316"><td class="cellrowborder" valign="top" width="29.43%" headers="mcps1.2.4.1.1 "><p id="p1641751235"><a name="p1641751235"></a><a name="p1641751235"></a>spark.sql.badRecordsPath</p>
</td>
<td class="cellrowborder" valign="top" width="15.85%" headers="mcps1.2.4.1.2 "><p id="p206411656232"><a name="p206411656232"></a><a name="p206411656232"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="54.72%" headers="mcps1.2.4.1.3 "><p id="p46411552315"><a name="p46411552315"></a><a name="p46411552315"></a>Bad Records的路径。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="s04b3bd00c07846478613d3718f637112"></a>

**表 4**  响应参数

<a name="zh-cn_topic_0069077806_table43107464"></a>
<table><thead align="left"><tr id="zh-cn_topic_0069077806_row12322941"><th class="cellrowborder" valign="top" width="12.11%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0069077806_p17344522714"><a name="zh-cn_topic_0069077806_p17344522714"></a><a name="zh-cn_topic_0069077806_p17344522714"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.66%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0069077806_p3324582718"><a name="zh-cn_topic_0069077806_p3324582718"></a><a name="zh-cn_topic_0069077806_p3324582718"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="16.88%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0069077806_p1633452272"><a name="zh-cn_topic_0069077806_p1633452272"></a><a name="zh-cn_topic_0069077806_p1633452272"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="61.35%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0069077806_p18354562712"><a name="zh-cn_topic_0069077806_p18354562712"></a><a name="zh-cn_topic_0069077806_p18354562712"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0069077806_row42891778"><td class="cellrowborder" valign="top" width="12.11%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0069077806_p51681963"><a name="zh-cn_topic_0069077806_p51681963"></a><a name="zh-cn_topic_0069077806_p51681963"></a>is_success</p>
</td>
<td class="cellrowborder" valign="top" width="9.66%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0069077806_p25489436"><a name="zh-cn_topic_0069077806_p25489436"></a><a name="zh-cn_topic_0069077806_p25489436"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="16.88%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0069077806_p51378430"><a name="zh-cn_topic_0069077806_p51378430"></a><a name="zh-cn_topic_0069077806_p51378430"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="61.35%" headers="mcps1.2.5.1.4 "><p id="p4367201211150"><a name="p4367201211150"></a><a name="p4367201211150"></a>请求发送是否成功。<span class="parmvalue" id="parmvalue3175800916327"><a name="parmvalue3175800916327"></a><a name="parmvalue3175800916327"></a>“true”</span>表示请求发送成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0069077806_row8129598"><td class="cellrowborder" valign="top" width="12.11%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0069077806_p54517712"><a name="zh-cn_topic_0069077806_p54517712"></a><a name="zh-cn_topic_0069077806_p54517712"></a>message</p>
</td>
<td class="cellrowborder" valign="top" width="9.66%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0069077806_p53858575"><a name="zh-cn_topic_0069077806_p53858575"></a><a name="zh-cn_topic_0069077806_p53858575"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="16.88%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0069077806_p468450"><a name="zh-cn_topic_0069077806_p468450"></a><a name="zh-cn_topic_0069077806_p468450"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="61.35%" headers="mcps1.2.5.1.4 "><p id="a4fa277540d3e42e48cec2027a36ca6bc"><a name="a4fa277540d3e42e48cec2027a36ca6bc"></a><a name="a4fa277540d3e42e48cec2027a36ca6bc"></a>系统提示信息，执行成功时，信息可能为空。</p>
</td>
</tr>
<tr id="zh-cn_topic_0069077806_row5956164"><td class="cellrowborder" valign="top" width="12.11%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0069077806_p12687257"><a name="zh-cn_topic_0069077806_p12687257"></a><a name="zh-cn_topic_0069077806_p12687257"></a>job_id</p>
</td>
<td class="cellrowborder" valign="top" width="9.66%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0069077806_p21034911"><a name="zh-cn_topic_0069077806_p21034911"></a><a name="zh-cn_topic_0069077806_p21034911"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="16.88%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0069077806_p26106237"><a name="zh-cn_topic_0069077806_p26106237"></a><a name="zh-cn_topic_0069077806_p26106237"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="61.35%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0069077806_p34230492"><a name="zh-cn_topic_0069077806_p34230492"></a><a name="zh-cn_topic_0069077806_p34230492"></a>此SQL语句将生成并提交一个新作业，返回此作业的ID，可用于获取作业状态和作业结果。</p>
</td>
</tr>
<tr id="zh-cn_topic_0069077806_row39638980"><td class="cellrowborder" valign="top" width="12.11%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0069077806_p56640774"><a name="zh-cn_topic_0069077806_p56640774"></a><a name="zh-cn_topic_0069077806_p56640774"></a>job_type</p>
</td>
<td class="cellrowborder" valign="top" width="9.66%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0069077806_p24499997"><a name="zh-cn_topic_0069077806_p24499997"></a><a name="zh-cn_topic_0069077806_p24499997"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="16.88%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0069077806_p38342769"><a name="zh-cn_topic_0069077806_p38342769"></a><a name="zh-cn_topic_0069077806_p38342769"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="61.35%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0069077806_p18756585"><a name="zh-cn_topic_0069077806_p18756585"></a><a name="zh-cn_topic_0069077806_p18756585"></a>作业类型。</p>
<a name="ud0cff9a09ee641b3a42e353020764dc1"></a><a name="ud0cff9a09ee641b3a42e353020764dc1"></a><ul id="ud0cff9a09ee641b3a42e353020764dc1"><li>DDL</li><li>DCL</li><li>IMPORT</li><li>EXPORT</li><li>QUERY</li><li>INSERT</li></ul>
</td>
</tr>
<tr id="row1822483371311"><td class="cellrowborder" valign="top" width="12.11%" headers="mcps1.2.5.1.1 "><p id="p18224933171318"><a name="p18224933171318"></a><a name="p18224933171318"></a>schema</p>
</td>
<td class="cellrowborder" valign="top" width="9.66%" headers="mcps1.2.5.1.2 "><p id="p92257338139"><a name="p92257338139"></a><a name="p92257338139"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.88%" headers="mcps1.2.5.1.3 "><p id="p1822514331138"><a name="p1822514331138"></a><a name="p1822514331138"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="61.35%" headers="mcps1.2.5.1.4 "><p id="p152251533161319"><a name="p152251533161319"></a><a name="p152251533161319"></a>当语句类型为DDL时，返回其结果的列名称及类型。</p>
</td>
</tr>
<tr id="zh-cn_topic_0069077806_row34591542"><td class="cellrowborder" valign="top" width="12.11%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0069077806_p50451552"><a name="zh-cn_topic_0069077806_p50451552"></a><a name="zh-cn_topic_0069077806_p50451552"></a>rows</p>
</td>
<td class="cellrowborder" valign="top" width="9.66%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0069077806_p60043939"><a name="zh-cn_topic_0069077806_p60043939"></a><a name="zh-cn_topic_0069077806_p60043939"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.88%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0069077806_p31720870"><a name="zh-cn_topic_0069077806_p31720870"></a><a name="zh-cn_topic_0069077806_p31720870"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="61.35%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0069077806_p19253649"><a name="zh-cn_topic_0069077806_p19253649"></a><a name="zh-cn_topic_0069077806_p19253649"></a>当语句类型为DDL时，直接返回其执行结果。</p>
</td>
</tr>
<tr id="row0688520181920"><td class="cellrowborder" valign="top" width="12.11%" headers="mcps1.2.5.1.1 "><p id="p222905218240"><a name="p222905218240"></a><a name="p222905218240"></a>job_mode</p>
</td>
<td class="cellrowborder" valign="top" width="9.66%" headers="mcps1.2.5.1.2 "><p id="p3229125212417"><a name="p3229125212417"></a><a name="p3229125212417"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.88%" headers="mcps1.2.5.1.3 "><p id="p922911524243"><a name="p922911524243"></a><a name="p922911524243"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="61.35%" headers="mcps1.2.5.1.4 "><p id="p4229105292420"><a name="p4229105292420"></a><a name="p4229105292420"></a>作业执行模式：</p>
<a name="ul194411241202517"></a><a name="ul194411241202517"></a><ul id="ul194411241202517"><li>async：异步</li><li>sync：同步</li></ul>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section57434560164325"></a>

-   请求样例：

    ```
    {
        "currentdb": "db1",
        "sql": "desc table1",
        "queue_name": "default",
        "conf": [
            "dli.sql.shuffle.partitions = 200"
        ]
    }
    ```

-   成功响应样例：

    ```
    {
      "is_success": true,
      "message": "{""}",
      "job_id": "8ecb0777-9c70-4529-9935-29ea0946039c",
      "job_type": "DDL",
      "job_mode":"sync",
      "schema": [
        {
          "col_name": "string"
        },
        {
          "data_type": "string"
        },
        {
          "comment": "string"
        }
      ],
      "rows": [
        [
          "c1",
          "int",
          null
        ],
        [
          "c2",
          "string",
          null
        ]
      ]
    }
    ```

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >调用API出错后，将不会返回上述结果，而是返回错误码和错误信息，详细介绍请参见[错误码](错误码.md)。


