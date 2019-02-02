# 提交SQL作业（推荐）<a name="dli_02_0102"></a>

## 功能介绍<a name="s51df1f9bf4784cf4a56c09b3973a2adc"></a>

该API用于通过执行SQL语句的方式向集群提交作业。

作业包含以下类型：DDL、DCL、IMPORT、QUERY和INSERT。其中，IMPORT与[导入数据](导入数据.md)的功能一致，区别仅在于实现方式不同。

另外，用户可使用其他API来对作业进行查询和管理。具体操作有：

-   [查询作业状态](查询作业状态.md)
-   [查询作业详细信息](查询作业详细信息.md)
-   [查看作业结果（推荐）](查看作业结果（推荐）.md)
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
    <th class="cellrowborder" valign="top" width="8.91089108910891%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0069077806_p9981547619"><a name="zh-cn_topic_0069077806_p9981547619"></a><a name="zh-cn_topic_0069077806_p9981547619"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="79.20792079207921%" id="mcps1.2.4.1.3"><p id="a9de737854caf4be3a07db76909948f18"><a name="a9de737854caf4be3a07db76909948f18"></a><a name="a9de737854caf4be3a07db76909948f18"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row5320171434012"><td class="cellrowborder" valign="top" width="11.881188118811881%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0069077803_p43412436"><a name="zh-cn_topic_0069077803_p43412436"></a><a name="zh-cn_topic_0069077803_p43412436"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.91089108910891%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0069077803_p26746391"><a name="zh-cn_topic_0069077803_p26746391"></a><a name="zh-cn_topic_0069077803_p26746391"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="79.20792079207921%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0069077803_p18974100"><a name="zh-cn_topic_0069077803_p18974100"></a><a name="zh-cn_topic_0069077803_p18974100"></a>项目编号，用于资源隔离。获取方式请参考<a href="获取项目编号.md">获取项目编号</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="s46f967e8024f453cb6cd43f3af264950"></a>

**表 2**  请求参数

<a name="table6376584143542"></a>
<table><thead align="left"><tr id="row19110893143542"><th class="cellrowborder" valign="top" width="13%" id="mcps1.2.5.1.1"><p id="p42934984143542"><a name="p42934984143542"></a><a name="p42934984143542"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="8%" id="mcps1.2.5.1.2"><p id="p55181642143542"><a name="p55181642143542"></a><a name="p55181642143542"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="p40528033143542"><a name="p40528033143542"></a><a name="p40528033143542"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="69%" id="mcps1.2.5.1.4"><p id="p61545269143542"><a name="p61545269143542"></a><a name="p61545269143542"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row16818917143542"><td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.5.1.1 "><p id="p4478514143542"><a name="p4478514143542"></a><a name="p4478514143542"></a>sql</p>
</td>
<td class="cellrowborder" valign="top" width="8%" headers="mcps1.2.5.1.2 "><p id="p27215339143542"><a name="p27215339143542"></a><a name="p27215339143542"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="p56958849143542"><a name="p56958849143542"></a><a name="p56958849143542"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="69%" headers="mcps1.2.5.1.4 "><p id="p1036145143542"><a name="p1036145143542"></a><a name="p1036145143542"></a>待执行的SQL语句。</p>
</td>
</tr>
<tr id="row48821488143542"><td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.5.1.1 "><p id="p17152532143542"><a name="p17152532143542"></a><a name="p17152532143542"></a>currentdb</p>
</td>
<td class="cellrowborder" valign="top" width="8%" headers="mcps1.2.5.1.2 "><p id="p47177872143542"><a name="p47177872143542"></a><a name="p47177872143542"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="p63311321143542"><a name="p63311321143542"></a><a name="p63311321143542"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="69%" headers="mcps1.2.5.1.4 "><p id="p27943382143542"><a name="p27943382143542"></a><a name="p27943382143542"></a>SQL语句执行所在的数据库。当创建新数据库时，不需要提供此参数。</p>
</td>
</tr>
<tr id="row47659205154318"><td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.5.1.1 "><p id="p1846530915443"><a name="p1846530915443"></a><a name="p1846530915443"></a>queue_name</p>
</td>
<td class="cellrowborder" valign="top" width="8%" headers="mcps1.2.5.1.2 "><p id="p3009358515443"><a name="p3009358515443"></a><a name="p3009358515443"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="p6674625215443"><a name="p6674625215443"></a><a name="p6674625215443"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="69%" headers="mcps1.2.5.1.4 "><p id="p32836715443"><a name="p32836715443"></a><a name="p32836715443"></a>待提交作业的资源队列名称，名称只能包含数字、英文字母和下划线，但不能是纯数字，且不能以下划线开头。</p>
</td>
</tr>
<tr id="row57451725143542"><td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.5.1.1 "><p id="p36740211143542"><a name="p36740211143542"></a><a name="p36740211143542"></a>conf</p>
</td>
<td class="cellrowborder" valign="top" width="8%" headers="mcps1.2.5.1.2 "><p id="p23167106143542"><a name="p23167106143542"></a><a name="p23167106143542"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="p64596322143542"><a name="p64596322143542"></a><a name="p64596322143542"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="69%" headers="mcps1.2.5.1.4 "><p id="p23997108143542"><a name="p23997108143542"></a><a name="p23997108143542"></a>用户以“key/value”的形式设置用于此作业的配置参数。目前支持的配置项请参考<a href="#table0995047105710">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  conf参数说明

<a name="table0995047105710"></a>
<table><thead align="left"><tr id="row1899634735718"><th class="cellrowborder" valign="top" width="27.810000000000002%" id="mcps1.2.3.1.1"><p id="p499615477576"><a name="p499615477576"></a><a name="p499615477576"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="72.19%" id="mcps1.2.3.1.2"><p id="p1599618476576"><a name="p1599618476576"></a><a name="p1599618476576"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row4996647165719"><td class="cellrowborder" valign="top" width="27.810000000000002%" headers="mcps1.2.3.1.1 "><p id="p599684745716"><a name="p599684745716"></a><a name="p599684745716"></a>dli.sql.autoBroadcastJoinThreshold</p>
</td>
<td class="cellrowborder" valign="top" width="72.19%" headers="mcps1.2.3.1.2 "><p id="p1999664775720"><a name="p1999664775720"></a><a name="p1999664775720"></a>自动使用BroadcastJoin的数据量阈值。</p>
</td>
</tr>
<tr id="row1399694719578"><td class="cellrowborder" valign="top" width="27.810000000000002%" headers="mcps1.2.3.1.1 "><p id="p13996347135720"><a name="p13996347135720"></a><a name="p13996347135720"></a>dli.sql.shuffle.partitions</p>
</td>
<td class="cellrowborder" valign="top" width="72.19%" headers="mcps1.2.3.1.2 "><p id="p1699684710571"><a name="p1699684710571"></a><a name="p1699684710571"></a>指定Shuffle过程中Partition的个数。</p>
</td>
</tr>
<tr id="row18496151319011"><td class="cellrowborder" valign="top" width="27.810000000000002%" headers="mcps1.2.3.1.1 "><p id="p6996547105719"><a name="p6996547105719"></a><a name="p6996547105719"></a>dli.sql.multiLevelDir.enabled</p>
</td>
<td class="cellrowborder" valign="top" width="72.19%" headers="mcps1.2.3.1.2 "><p id="p19996154717576"><a name="p19996154717576"></a><a name="p19996154717576"></a>OBS表的指定目录或OBS表分区表的分区目录下有子目录时，是否查询子目录的内容；默认不查询。</p>
</td>
</tr>
<tr id="row20996647105715"><td class="cellrowborder" valign="top" width="27.810000000000002%" headers="mcps1.2.3.1.1 "><p id="p204131117801"><a name="p204131117801"></a><a name="p204131117801"></a>dli.sql.dynamicPartitionOverwrite.enabled</p>
</td>
<td class="cellrowborder" valign="top" width="72.19%" headers="mcps1.2.3.1.2 "><p id="p03876172011"><a name="p03876172011"></a><a name="p03876172011"></a>在动态分区模式时，只会重写查询中的数据涉及的分区，未涉及的分区不删除。</p>
</td>
</tr>
<tr id="row79568586212"><td class="cellrowborder" valign="top" width="27.810000000000002%" headers="mcps1.2.3.1.1 "><p id="p199565584216"><a name="p199565584216"></a><a name="p199565584216"></a>dli.sql.files.maxPartitionBytes</p>
</td>
<td class="cellrowborder" valign="top" width="72.19%" headers="mcps1.2.3.1.2 "><p id="p895616583219"><a name="p895616583219"></a><a name="p895616583219"></a>最大分区字节数。设置一个分区可以处理的最大字节数，当一个文件或分区大小大于这个值时会被拆分到多个分区。</p>
</td>
</tr>
<tr id="row3229125343618"><td class="cellrowborder" valign="top" width="27.810000000000002%" headers="mcps1.2.3.1.1 "><p id="p523012535362"><a name="p523012535362"></a><a name="p523012535362"></a>dli.sql.badRecordsPath</p>
</td>
<td class="cellrowborder" valign="top" width="72.19%" headers="mcps1.2.3.1.2 "><p id="p2230145383612"><a name="p2230145383612"></a><a name="p2230145383612"></a>INSERT类型作业执行过程的bad records的存储目录。建议与<span class="parmvalue" id="parmvalue19990322495"><a name="parmvalue19990322495"></a><a name="parmvalue19990322495"></a>“DROPMALFORMED”</span>这一数据源ParseMode结合使用。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="s04b3bd00c07846478613d3718f637112"></a>

**表 4**  响应参数

<a name="zh-cn_topic_0069077806_table43107464"></a>
<table><thead align="left"><tr id="zh-cn_topic_0069077806_row12322941"><th class="cellrowborder" valign="top" width="10.81%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0069077806_p17344522714"><a name="zh-cn_topic_0069077806_p17344522714"></a><a name="zh-cn_topic_0069077806_p17344522714"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="8.540000000000001%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0069077806_p3324582718"><a name="zh-cn_topic_0069077806_p3324582718"></a><a name="zh-cn_topic_0069077806_p3324582718"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10.549999999999999%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0069077806_p1633452272"><a name="zh-cn_topic_0069077806_p1633452272"></a><a name="zh-cn_topic_0069077806_p1633452272"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="70.1%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0069077806_p18354562712"><a name="zh-cn_topic_0069077806_p18354562712"></a><a name="zh-cn_topic_0069077806_p18354562712"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0069077806_row42891778"><td class="cellrowborder" valign="top" width="10.81%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0069077806_p51681963"><a name="zh-cn_topic_0069077806_p51681963"></a><a name="zh-cn_topic_0069077806_p51681963"></a>is_success</p>
</td>
<td class="cellrowborder" valign="top" width="8.540000000000001%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0069077806_p25489436"><a name="zh-cn_topic_0069077806_p25489436"></a><a name="zh-cn_topic_0069077806_p25489436"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10.549999999999999%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0069077806_p51378430"><a name="zh-cn_topic_0069077806_p51378430"></a><a name="zh-cn_topic_0069077806_p51378430"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="70.1%" headers="mcps1.2.5.1.4 "><p id="p4367201211150"><a name="p4367201211150"></a><a name="p4367201211150"></a>当<span class="parmname" id="parmname20849116111318"><a name="parmname20849116111318"></a><a name="parmname20849116111318"></a>“job_type”</span>为<span class="parmvalue" id="parmvalue2347564101624"><a name="parmvalue2347564101624"></a><a name="parmvalue2347564101624"></a>“DCL”</span>时，为请求执行是否成功。<span class="parmvalue" id="parmvalue218731155923"><a name="parmvalue218731155923"></a><a name="parmvalue218731155923"></a>“true”</span>表示请求执行成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0069077806_row8129598"><td class="cellrowborder" valign="top" width="10.81%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0069077806_p54517712"><a name="zh-cn_topic_0069077806_p54517712"></a><a name="zh-cn_topic_0069077806_p54517712"></a>message</p>
</td>
<td class="cellrowborder" valign="top" width="8.540000000000001%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0069077806_p53858575"><a name="zh-cn_topic_0069077806_p53858575"></a><a name="zh-cn_topic_0069077806_p53858575"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10.549999999999999%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0069077806_p468450"><a name="zh-cn_topic_0069077806_p468450"></a><a name="zh-cn_topic_0069077806_p468450"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="70.1%" headers="mcps1.2.5.1.4 "><p id="a4fa277540d3e42e48cec2027a36ca6bc"><a name="a4fa277540d3e42e48cec2027a36ca6bc"></a><a name="a4fa277540d3e42e48cec2027a36ca6bc"></a>系统提示信息，执行成功时，信息可能为空。</p>
</td>
</tr>
<tr id="zh-cn_topic_0069077806_row5956164"><td class="cellrowborder" valign="top" width="10.81%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0069077806_p12687257"><a name="zh-cn_topic_0069077806_p12687257"></a><a name="zh-cn_topic_0069077806_p12687257"></a>job_id</p>
</td>
<td class="cellrowborder" valign="top" width="8.540000000000001%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0069077806_p21034911"><a name="zh-cn_topic_0069077806_p21034911"></a><a name="zh-cn_topic_0069077806_p21034911"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10.549999999999999%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0069077806_p26106237"><a name="zh-cn_topic_0069077806_p26106237"></a><a name="zh-cn_topic_0069077806_p26106237"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="70.1%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0069077806_p34230492"><a name="zh-cn_topic_0069077806_p34230492"></a><a name="zh-cn_topic_0069077806_p34230492"></a>此SQL语句将生成并提交一个新作业，返回此作业的ID，可用于获取作业状态和作业结果。</p>
</td>
</tr>
<tr id="zh-cn_topic_0069077806_row39638980"><td class="cellrowborder" valign="top" width="10.81%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0069077806_p56640774"><a name="zh-cn_topic_0069077806_p56640774"></a><a name="zh-cn_topic_0069077806_p56640774"></a>job_type</p>
</td>
<td class="cellrowborder" valign="top" width="8.540000000000001%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0069077806_p24499997"><a name="zh-cn_topic_0069077806_p24499997"></a><a name="zh-cn_topic_0069077806_p24499997"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10.549999999999999%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0069077806_p38342769"><a name="zh-cn_topic_0069077806_p38342769"></a><a name="zh-cn_topic_0069077806_p38342769"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="70.1%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0069077806_p18756585"><a name="zh-cn_topic_0069077806_p18756585"></a><a name="zh-cn_topic_0069077806_p18756585"></a>作业类型。</p>
<a name="ud0cff9a09ee641b3a42e353020764dc1"></a><a name="ud0cff9a09ee641b3a42e353020764dc1"></a><ul id="ud0cff9a09ee641b3a42e353020764dc1"><li>DDL</li><li>DCL</li><li>IMPORT</li><li>EXPORT</li><li>QUERY</li><li>INSERT</li></ul>
</td>
</tr>
<tr id="row1822483371311"><td class="cellrowborder" valign="top" width="10.81%" headers="mcps1.2.5.1.1 "><p id="p18224933171318"><a name="p18224933171318"></a><a name="p18224933171318"></a>schema</p>
</td>
<td class="cellrowborder" valign="top" width="8.540000000000001%" headers="mcps1.2.5.1.2 "><p id="p92257338139"><a name="p92257338139"></a><a name="p92257338139"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="10.549999999999999%" headers="mcps1.2.5.1.3 "><p id="p1822514331138"><a name="p1822514331138"></a><a name="p1822514331138"></a>Array</p>
</td>
<td class="cellrowborder" valign="top" width="70.1%" headers="mcps1.2.5.1.4 "><p id="p152251533161319"><a name="p152251533161319"></a><a name="p152251533161319"></a>当语句类型为DDL时，返回其结果的列名称及类型。</p>
</td>
</tr>
<tr id="zh-cn_topic_0069077806_row34591542"><td class="cellrowborder" valign="top" width="10.81%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0069077806_p50451552"><a name="zh-cn_topic_0069077806_p50451552"></a><a name="zh-cn_topic_0069077806_p50451552"></a>rows</p>
</td>
<td class="cellrowborder" valign="top" width="8.540000000000001%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0069077806_p60043939"><a name="zh-cn_topic_0069077806_p60043939"></a><a name="zh-cn_topic_0069077806_p60043939"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="10.549999999999999%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0069077806_p31720870"><a name="zh-cn_topic_0069077806_p31720870"></a><a name="zh-cn_topic_0069077806_p31720870"></a>Array</p>
</td>
<td class="cellrowborder" valign="top" width="70.1%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0069077806_p19253649"><a name="zh-cn_topic_0069077806_p19253649"></a><a name="zh-cn_topic_0069077806_p19253649"></a>当语句类型为DDL时，直接返回其执行结果。</p>
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
      "message": "",
      "job_id": "8ecb0777-9c70-4529-9935-29ea0946039c",
      "job_type": "DDL",
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


