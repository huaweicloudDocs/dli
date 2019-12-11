# 提交SQL作业（废弃）<a name="dli_02_0018"></a>

## 功能介绍<a name="s51df1f9bf4784cf4a56c09b3973a2adc"></a>

该API用于通过执行SQL语句的方式向队列提交作业。

作业包含以下类型：DDL、DCL、IMPORT、EXPORT、QUERY和INSERT。其中，IMPORT和EXPORT分别与[导入数据](导入数据.md)和与[导出数据](导出数据.md)的功能一致，区别仅在于实现方式不同。

另外，用户可使用其他API来对作业进行查询和管理。具体操作有：

-   [查询作业状态](查询作业状态.md)
-   [查询作业详细信息](查询作业详细信息.md)
-   [查询作业结果（废弃）](查询作业结果（废弃）.md)
-   [导出查询结果](导出查询结果.md)
-   [查询所有作业](查询所有作业.md)
-   [取消作业（废弃）](取消作业（废弃）.md)

>![](public_sys-resources/icon-note.gif) **说明：**   
>-   该API当响应消息中“job\_type“为“DCL“时，为同步操作。  
>-   本章节介绍的API已过时，推荐使用[提交SQL作业（推荐）](提交SQL作业（推荐）.md)介绍的API。  

## URI<a name="s807a09edd221483999c7c51233072a4a"></a>

-   URI格式：

    POST /v1.0/\{project\_id\}/queues/\{queue\_name\}/jobs/submit-job

-   参数说明

    **表 1**  URI参数

    <a name="zh-cn_topic_0069077806_table9770605"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0069077806_row35653836"><th class="cellrowborder" valign="top" width="14.67%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0069077806_p14983541266"><a name="zh-cn_topic_0069077806_p14983541266"></a><a name="zh-cn_topic_0069077806_p14983541266"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="10.33%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0069077806_p9981547619"><a name="zh-cn_topic_0069077806_p9981547619"></a><a name="zh-cn_topic_0069077806_p9981547619"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="75%" id="mcps1.2.4.1.3"><p id="a9de737854caf4be3a07db76909948f18"><a name="a9de737854caf4be3a07db76909948f18"></a><a name="a9de737854caf4be3a07db76909948f18"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row5320171434012"><td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0069077803_p43412436"><a name="zh-cn_topic_0069077803_p43412436"></a><a name="zh-cn_topic_0069077803_p43412436"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.33%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0069077803_p26746391"><a name="zh-cn_topic_0069077803_p26746391"></a><a name="zh-cn_topic_0069077803_p26746391"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="75%" headers="mcps1.2.4.1.3 "><p id="p1310472724012"><a name="p1310472724012"></a><a name="p1310472724012"></a>项目编号，用于资源隔离。获取方式请参考<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0069077806_row44704179"><td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0069077806_p64268748"><a name="zh-cn_topic_0069077806_p64268748"></a><a name="zh-cn_topic_0069077806_p64268748"></a>queue_name</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.33%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0069077806_p38386134"><a name="zh-cn_topic_0069077806_p38386134"></a><a name="zh-cn_topic_0069077806_p38386134"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="75%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0069077806_p22269177"><a name="zh-cn_topic_0069077806_p22269177"></a><a name="zh-cn_topic_0069077806_p22269177"></a>当前所在的队列的名称，此SQL若需使用资源将使用该队列的资源进行计算。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="s46f967e8024f453cb6cd43f3af264950"></a>

**表 2**  请求参数

<a name="table6376584143542"></a>
<table><thead align="left"><tr id="row19110893143542"><th class="cellrowborder" valign="top" width="11.87%" id="mcps1.2.5.1.1"><p id="p42934984143542"><a name="p42934984143542"></a><a name="p42934984143542"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.19%" id="mcps1.2.5.1.2"><p id="p55181642143542"><a name="p55181642143542"></a><a name="p55181642143542"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10.36%" id="mcps1.2.5.1.3"><p id="p40528033143542"><a name="p40528033143542"></a><a name="p40528033143542"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="68.58%" id="mcps1.2.5.1.4"><p id="p61545269143542"><a name="p61545269143542"></a><a name="p61545269143542"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row16818917143542"><td class="cellrowborder" valign="top" width="11.87%" headers="mcps1.2.5.1.1 "><p id="p4478514143542"><a name="p4478514143542"></a><a name="p4478514143542"></a>sql</p>
</td>
<td class="cellrowborder" valign="top" width="9.19%" headers="mcps1.2.5.1.2 "><p id="p27215339143542"><a name="p27215339143542"></a><a name="p27215339143542"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10.36%" headers="mcps1.2.5.1.3 "><p id="p56958849143542"><a name="p56958849143542"></a><a name="p56958849143542"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="68.58%" headers="mcps1.2.5.1.4 "><p id="p1036145143542"><a name="p1036145143542"></a><a name="p1036145143542"></a>待执行的SQL语句。</p>
</td>
</tr>
<tr id="row48821488143542"><td class="cellrowborder" valign="top" width="11.87%" headers="mcps1.2.5.1.1 "><p id="p17152532143542"><a name="p17152532143542"></a><a name="p17152532143542"></a>currentdb</p>
</td>
<td class="cellrowborder" valign="top" width="9.19%" headers="mcps1.2.5.1.2 "><p id="p47177872143542"><a name="p47177872143542"></a><a name="p47177872143542"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="10.36%" headers="mcps1.2.5.1.3 "><p id="p63311321143542"><a name="p63311321143542"></a><a name="p63311321143542"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="68.58%" headers="mcps1.2.5.1.4 "><p id="p27943382143542"><a name="p27943382143542"></a><a name="p27943382143542"></a>SQL语句执行所在的数据库。当创建新数据库时，不需要提供此参数。</p>
</td>
</tr>
<tr id="row57451725143542"><td class="cellrowborder" valign="top" width="11.87%" headers="mcps1.2.5.1.1 "><p id="p36740211143542"><a name="p36740211143542"></a><a name="p36740211143542"></a>conf</p>
</td>
<td class="cellrowborder" valign="top" width="9.19%" headers="mcps1.2.5.1.2 "><p id="p23167106143542"><a name="p23167106143542"></a><a name="p23167106143542"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="10.36%" headers="mcps1.2.5.1.3 "><p id="p64596322143542"><a name="p64596322143542"></a><a name="p64596322143542"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="68.58%" headers="mcps1.2.5.1.4 "><p id="p23997108143542"><a name="p23997108143542"></a><a name="p23997108143542"></a>用户定义适用于此作业的配置参数。目前支持的配置项：</p>
<a name="ul45587104143542"></a><a name="ul45587104143542"></a><ul id="ul45587104143542"><li>dli.sql.join.preferSortMergeJoin（是否优先使用SortMergeJoin）</li><li>dli.sql.autoBroadcastJoinThreshold（自动使用BroadcastJoin的数据量阈值）</li><li>dli.sql.caseSensitive（sql语句是否大小写敏感）</li><li>dli.sql.shuffle.partitions（指定Shuffle过程中Partition的个数）</li><li>dli.sql.cbo.enabled（是否打开CBO优化策略）</li><li>dli.sql.cbo.joinReorder.enabled（开启CBO优化时，是否允许重新调整join的顺序）</li></ul>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="s04b3bd00c07846478613d3718f637112"></a>

**表 3**  响应参数

<a name="zh-cn_topic_0069077806_table43107464"></a>
<table><thead align="left"><tr id="zh-cn_topic_0069077806_row12322941"><th class="cellrowborder" valign="top" width="11.524752475247526%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0069077806_p17344522714"><a name="zh-cn_topic_0069077806_p17344522714"></a><a name="zh-cn_topic_0069077806_p17344522714"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="11.16831683168317%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0069077806_p3324582718"><a name="zh-cn_topic_0069077806_p3324582718"></a><a name="zh-cn_topic_0069077806_p3324582718"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="9.217821782178218%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0069077806_p1633452272"><a name="zh-cn_topic_0069077806_p1633452272"></a><a name="zh-cn_topic_0069077806_p1633452272"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="68.08910891089108%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0069077806_p18354562712"><a name="zh-cn_topic_0069077806_p18354562712"></a><a name="zh-cn_topic_0069077806_p18354562712"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0069077806_row42891778"><td class="cellrowborder" valign="top" width="11.524752475247526%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0069077806_p51681963"><a name="zh-cn_topic_0069077806_p51681963"></a><a name="zh-cn_topic_0069077806_p51681963"></a>is_success</p>
</td>
<td class="cellrowborder" valign="top" width="11.16831683168317%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0069077806_p25489436"><a name="zh-cn_topic_0069077806_p25489436"></a><a name="zh-cn_topic_0069077806_p25489436"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="9.217821782178218%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0069077806_p51378430"><a name="zh-cn_topic_0069077806_p51378430"></a><a name="zh-cn_topic_0069077806_p51378430"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="68.08910891089108%" headers="mcps1.2.5.1.4 "><p id="p4367201211150"><a name="p4367201211150"></a><a name="p4367201211150"></a>当<span class="parmname" id="parmname22679521103338"><a name="parmname22679521103338"></a><a name="parmname22679521103338"></a>“job_type”</span>为<span class="parmvalue" id="parmvalue25101895103338"><a name="parmvalue25101895103338"></a><a name="parmvalue25101895103338"></a>“DCL”</span>时，为请求执行是否成功。<span class="parmvalue" id="parmvalue19987651103338"><a name="parmvalue19987651103338"></a><a name="parmvalue19987651103338"></a>“true”</span>表示请求执行成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0069077806_row8129598"><td class="cellrowborder" valign="top" width="11.524752475247526%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0069077806_p54517712"><a name="zh-cn_topic_0069077806_p54517712"></a><a name="zh-cn_topic_0069077806_p54517712"></a>message</p>
</td>
<td class="cellrowborder" valign="top" width="11.16831683168317%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0069077806_p53858575"><a name="zh-cn_topic_0069077806_p53858575"></a><a name="zh-cn_topic_0069077806_p53858575"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="9.217821782178218%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0069077806_p468450"><a name="zh-cn_topic_0069077806_p468450"></a><a name="zh-cn_topic_0069077806_p468450"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="68.08910891089108%" headers="mcps1.2.5.1.4 "><p id="a4fa277540d3e42e48cec2027a36ca6bc"><a name="a4fa277540d3e42e48cec2027a36ca6bc"></a><a name="a4fa277540d3e42e48cec2027a36ca6bc"></a>系统提示信息，执行成功时，信息可能为空。</p>
</td>
</tr>
<tr id="zh-cn_topic_0069077806_row5956164"><td class="cellrowborder" valign="top" width="11.524752475247526%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0069077806_p12687257"><a name="zh-cn_topic_0069077806_p12687257"></a><a name="zh-cn_topic_0069077806_p12687257"></a>job_id</p>
</td>
<td class="cellrowborder" valign="top" width="11.16831683168317%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0069077806_p21034911"><a name="zh-cn_topic_0069077806_p21034911"></a><a name="zh-cn_topic_0069077806_p21034911"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="9.217821782178218%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0069077806_p26106237"><a name="zh-cn_topic_0069077806_p26106237"></a><a name="zh-cn_topic_0069077806_p26106237"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="68.08910891089108%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0069077806_p34230492"><a name="zh-cn_topic_0069077806_p34230492"></a><a name="zh-cn_topic_0069077806_p34230492"></a>此SQL语句将生成并提交一个新作业，返回此作业的ID，可用于获取作业状态和作业结果。</p>
</td>
</tr>
<tr id="zh-cn_topic_0069077806_row39638980"><td class="cellrowborder" valign="top" width="11.524752475247526%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0069077806_p56640774"><a name="zh-cn_topic_0069077806_p56640774"></a><a name="zh-cn_topic_0069077806_p56640774"></a>job_type</p>
</td>
<td class="cellrowborder" valign="top" width="11.16831683168317%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0069077806_p24499997"><a name="zh-cn_topic_0069077806_p24499997"></a><a name="zh-cn_topic_0069077806_p24499997"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="9.217821782178218%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0069077806_p38342769"><a name="zh-cn_topic_0069077806_p38342769"></a><a name="zh-cn_topic_0069077806_p38342769"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="68.08910891089108%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0069077806_p18756585"><a name="zh-cn_topic_0069077806_p18756585"></a><a name="zh-cn_topic_0069077806_p18756585"></a>作业类型。</p>
<a name="ud0cff9a09ee641b3a42e353020764dc1"></a><a name="ud0cff9a09ee641b3a42e353020764dc1"></a><ul id="ud0cff9a09ee641b3a42e353020764dc1"><li>DDL</li><li>DCL</li><li>IMPORT</li><li>EXPORT</li><li>QUERY</li><li>INSERT</li></ul>
</td>
</tr>
<tr id="row1822483371311"><td class="cellrowborder" valign="top" width="11.524752475247526%" headers="mcps1.2.5.1.1 "><p id="p18224933171318"><a name="p18224933171318"></a><a name="p18224933171318"></a>schema</p>
</td>
<td class="cellrowborder" valign="top" width="11.16831683168317%" headers="mcps1.2.5.1.2 "><p id="p92257338139"><a name="p92257338139"></a><a name="p92257338139"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="9.217821782178218%" headers="mcps1.2.5.1.3 "><p id="p1822514331138"><a name="p1822514331138"></a><a name="p1822514331138"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="68.08910891089108%" headers="mcps1.2.5.1.4 "><p id="p152251533161319"><a name="p152251533161319"></a><a name="p152251533161319"></a>当语句类型为DDL时，返回其结果的列名称及类型。</p>
</td>
</tr>
<tr id="zh-cn_topic_0069077806_row34591542"><td class="cellrowborder" valign="top" width="11.524752475247526%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0069077806_p50451552"><a name="zh-cn_topic_0069077806_p50451552"></a><a name="zh-cn_topic_0069077806_p50451552"></a>rows</p>
</td>
<td class="cellrowborder" valign="top" width="11.16831683168317%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0069077806_p60043939"><a name="zh-cn_topic_0069077806_p60043939"></a><a name="zh-cn_topic_0069077806_p60043939"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="9.217821782178218%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0069077806_p31720870"><a name="zh-cn_topic_0069077806_p31720870"></a><a name="zh-cn_topic_0069077806_p31720870"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="68.08910891089108%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0069077806_p19253649"><a name="zh-cn_topic_0069077806_p19253649"></a><a name="zh-cn_topic_0069077806_p19253649"></a>当语句类型为DDL时，直接返回其执行结果。</p>
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


