# Flink作业详情<a name="dli_01_0462"></a>

创建作业后，用户可以通过查看作业详情，了解如下信息：

-   [查看作业详情](#section18786181516319)
-   [查看作业监控](#section93781115103311)
-   [查看作业任务列表](#section11677164916529)
-   [查看作业执行计划](#section9397163320)
-   [查看提交作业日志](#section18556377020)
-   [查看作业运行日志](#section91816183316)
-   [查看作业标签](#section19193157121312)

## 查看作业详情<a name="section18786181516319"></a>

用户创建完作业并运行后，用户可以查看作业的详细信息，包括作业的SQL语句和参数设置信息，如果是 jar作业只可以看到参数设置信息。

1.  在DLI管理控制台的左侧导航栏中，单击“作业管理“\>“Flink作业“，进入Flink作业管理页面。
2.  单击需要查看的作业名称，进入“作业详情“页面。

    在“作业详情“页签，用户可以查看作业的SQL语句、参数设置信息和总费用。

    以某个Flink SQL作业为例进行说明。

    **表 1**  参数说明

    <a name="table134266557103"></a>
    <table><thead align="left"><tr id="row9427155161016"><th class="cellrowborder" valign="top" width="25.3%" id="mcps1.2.3.1.1"><p id="p242719550104"><a name="p242719550104"></a><a name="p242719550104"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="74.7%" id="mcps1.2.3.1.2"><p id="p18427755181018"><a name="p18427755181018"></a><a name="p18427755181018"></a>参数说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row13348135518010"><td class="cellrowborder" valign="top" width="25.3%" headers="mcps1.2.3.1.1 "><p id="p19284133351213"><a name="p19284133351213"></a><a name="p19284133351213"></a>作业状态</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.7%" headers="mcps1.2.3.1.2 "><p id="p32841833181213"><a name="p32841833181213"></a><a name="p32841833181213"></a>作业名称右侧为作业当前的状态。</p>
    </td>
    </tr>
    <tr id="row49896498173"><td class="cellrowborder" valign="top" width="25.3%" headers="mcps1.2.3.1.1 "><p id="p34571726172514"><a name="p34571726172514"></a><a name="p34571726172514"></a>ID</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.7%" headers="mcps1.2.3.1.2 "><p id="p74576268254"><a name="p74576268254"></a><a name="p74576268254"></a>作业ID。</p>
    </td>
    </tr>
    <tr id="row619451745920"><td class="cellrowborder" valign="top" width="25.3%" headers="mcps1.2.3.1.1 "><p id="p1099014497177"><a name="p1099014497177"></a><a name="p1099014497177"></a>作业类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.7%" headers="mcps1.2.3.1.2 "><p id="p1699004916175"><a name="p1699004916175"></a><a name="p1699004916175"></a>作业类型，如Flink SQL作业。</p>
    </td>
    </tr>
    <tr id="row124561026152515"><td class="cellrowborder" valign="top" width="25.3%" headers="mcps1.2.3.1.1 "><p id="p13284183351211"><a name="p13284183351211"></a><a name="p13284183351211"></a>所属队列</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.7%" headers="mcps1.2.3.1.2 "><p id="p576522893316"><a name="p576522893316"></a><a name="p576522893316"></a>如果作业所属队列是共享队列，则显示共享队列。</p>
    <p id="p88601346"><a name="p88601346"></a><a name="p88601346"></a>如果作业所属队列是自定义的独享队列，则显示具体队列名称。</p>
    </td>
    </tr>
    <tr id="row1328315336123"><td class="cellrowborder" valign="top" width="25.3%" headers="mcps1.2.3.1.1 "><p id="p1928473331214"><a name="p1928473331214"></a><a name="p1928473331214"></a>运行模式</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.7%" headers="mcps1.2.3.1.2 "><p id="p1372416127263"><a name="p1372416127263"></a><a name="p1372416127263"></a>如果作业所属队列是共享队列，则作业的运行模式是共享模式。</p>
    <p id="p19135181632711"><a name="p19135181632711"></a><a name="p19135181632711"></a>如果作业所属队列是自定义的独享队列，则作业的运行模式是独占模式。</p>
    </td>
    </tr>
    <tr id="row1028453301219"><td class="cellrowborder" valign="top" width="25.3%" headers="mcps1.2.3.1.1 "><p id="p14271155141012"><a name="p14271155141012"></a><a name="p14271155141012"></a>CU数量</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.7%" headers="mcps1.2.3.1.2 "><p id="p54271355201015"><a name="p54271355201015"></a><a name="p54271355201015"></a>作业配置的CU数量。</p>
    </td>
    </tr>
    <tr id="row528418336121"><td class="cellrowborder" valign="top" width="25.3%" headers="mcps1.2.3.1.1 "><p id="p332434717599"><a name="p332434717599"></a><a name="p332434717599"></a>管理单元</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.7%" headers="mcps1.2.3.1.2 "><p id="p10322847185917"><a name="p10322847185917"></a><a name="p10322847185917"></a>作业配置的管理单元CU数量。</p>
    </td>
    </tr>
    <tr id="row12427185512105"><td class="cellrowborder" valign="top" width="25.3%" headers="mcps1.2.3.1.1 "><p id="p1167413518189"><a name="p1167413518189"></a><a name="p1167413518189"></a>并行数</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.7%" headers="mcps1.2.3.1.2 "><p id="p6156175975313"><a name="p6156175975313"></a><a name="p6156175975313"></a>作业配置的同时运行Flink作业的任务数。</p>
    </td>
    </tr>
    <tr id="row6673103521816"><td class="cellrowborder" valign="top" width="25.3%" headers="mcps1.2.3.1.1 "><p id="p13327451192616"><a name="p13327451192616"></a><a name="p13327451192616"></a>保存作业日志</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.7%" headers="mcps1.2.3.1.2 "><p id="p1732765117262"><a name="p1732765117262"></a><a name="p1732765117262"></a>开启或关闭。</p>
    </td>
    </tr>
    <tr id="row11206165011514"><td class="cellrowborder" valign="top" width="25.3%" headers="mcps1.2.3.1.1 "><p id="p14177711113211"><a name="p14177711113211"></a><a name="p14177711113211"></a>异常自动重启</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.7%" headers="mcps1.2.3.1.2 "><p id="p7178161114329"><a name="p7178161114329"></a><a name="p7178161114329"></a>开启或关闭。</p>
    </td>
    </tr>
    <tr id="row94272553105"><td class="cellrowborder" valign="top" width="25.3%" headers="mcps1.2.3.1.1 "><p id="p1015311472158"><a name="p1015311472158"></a><a name="p1015311472158"></a>从Checkpoint恢复</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.7%" headers="mcps1.2.3.1.2 "><p id="p1242725541013"><a name="p1242725541013"></a><a name="p1242725541013"></a>开启或关闭。</p>
    </td>
    </tr>
    <tr id="row47911726476"><td class="cellrowborder" valign="top" width="25.3%" headers="mcps1.2.3.1.1 "><p id="p4791226675"><a name="p4791226675"></a><a name="p4791226675"></a>单TM所占CU数</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.7%" headers="mcps1.2.3.1.2 "><p id="p8791142610710"><a name="p8791142610710"></a><a name="p8791142610710"></a>作业配置的每个TaskManager所占CU数量。</p>
    </td>
    </tr>
    <tr id="row879117261674"><td class="cellrowborder" valign="top" width="25.3%" headers="mcps1.2.3.1.1 "><p id="p1083413454715"><a name="p1083413454715"></a><a name="p1083413454715"></a>单TM Slot</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.7%" headers="mcps1.2.3.1.2 "><p id="p179212620711"><a name="p179212620711"></a><a name="p179212620711"></a>作业配置的每个TaskManager Slot数量。</p>
    </td>
    </tr>
    <tr id="row43634532713"><td class="cellrowborder" valign="top" width="25.3%" headers="mcps1.2.3.1.1 "><p id="p1363205311717"><a name="p1363205311717"></a><a name="p1363205311717"></a>开启Checkpoint</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.7%" headers="mcps1.2.3.1.2 "><p id="p136320531675"><a name="p136320531675"></a><a name="p136320531675"></a>开启或关闭。</p>
    </td>
    </tr>
    <tr id="row942885511015"><td class="cellrowborder" valign="top" width="25.3%" headers="mcps1.2.3.1.1 "><p id="p1242817552100"><a name="p1242817552100"></a><a name="p1242817552100"></a>Checkpoint间隔（s）</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.7%" headers="mcps1.2.3.1.2 "><p id="p1428115513109"><a name="p1428115513109"></a><a name="p1428115513109"></a>将作业运行的中间结果保存到OBS的间隔时间。</p>
    </td>
    </tr>
    <tr id="row20428165531017"><td class="cellrowborder" valign="top" width="25.3%" headers="mcps1.2.3.1.1 "><p id="p194284559109"><a name="p194284559109"></a><a name="p194284559109"></a>Checkpoint模式</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.7%" headers="mcps1.2.3.1.2 "><p id="p9279173651910"><a name="p9279173651910"></a><a name="p9279173651910"></a>Checkpoint 模式：</p>
    <a name="ul7279123621911"></a><a name="ul7279123621911"></a><ul id="ul7279123621911"><li>AtLeastOnce：事件至少被处理一次</li><li>ExactlyOnce：事件仅被处理一次</li></ul>
    </td>
    </tr>
    <tr id="row17842202617373"><td class="cellrowborder" valign="top" width="25.3%" headers="mcps1.2.3.1.1 "><p id="p2319751285"><a name="p2319751285"></a><a name="p2319751285"></a>空闲状态保留时长</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.7%" headers="mcps1.2.3.1.2 "><p id="p153193511082"><a name="p153193511082"></a><a name="p153193511082"></a>用于清除GroupBy或Window经过最大保留时间后仍未更新的中间状态。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 查看作业监控<a name="section93781115103311"></a>

用户可以通过云监控服务（CES）查看作业数据输入输出的详细信息。

1.  在DLI管理控制台的左侧导航栏中，单击“作业管理“\>“Flink作业“，进入Flink作业管理页面。
2.  单击需要查看的作业名称，进入“作业详情“页面。

    单击页面右上角的“作业监控“，将跳转至云监控服务（CES）。

    ![](figures/8-2-13Flink作业详情作业监控-zh.png)

    Flink 作业包含如下监控指标。

    **表 2**  Flink作业监控指标

    <a name="table5145123113817"></a>
    <table><thead align="left"><tr id="row1015823120383"><th class="cellrowborder" valign="top" width="28.000000000000004%" id="mcps1.2.3.1.1"><p id="p1716513312385"><a name="p1716513312385"></a><a name="p1716513312385"></a>指标名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="72%" id="mcps1.2.3.1.2"><p id="p71705312382"><a name="p71705312382"></a><a name="p71705312382"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1017713123816"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.3.1.1 "><p id="p181351419103913"><a name="p181351419103913"></a><a name="p181351419103913"></a>Flink作业数据输入速率</p>
    </td>
    <td class="cellrowborder" valign="top" width="72%" headers="mcps1.2.3.1.2 "><p id="p2014531963919"><a name="p2014531963919"></a><a name="p2014531963919"></a>展示用户Flink作业的数据输入速率，供监控和调试使用。单位：条/秒。</p>
    </td>
    </tr>
    <tr id="row5513169938"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.3.1.1 "><p id="p6903183316"><a name="p6903183316"></a><a name="p6903183316"></a>Flink作业数据输出速率</p>
    </td>
    <td class="cellrowborder" valign="top" width="72%" headers="mcps1.2.3.1.2 "><p id="p59016180318"><a name="p59016180318"></a><a name="p59016180318"></a>展示用户Flink作业的数据输出速率，供监控和调试使用。单位：条/秒。</p>
    </td>
    </tr>
    <tr id="row4187163173819"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.3.1.1 "><p id="p3192113133817"><a name="p3192113133817"></a><a name="p3192113133817"></a>Flink作业数据输入总数</p>
    </td>
    <td class="cellrowborder" valign="top" width="72%" headers="mcps1.2.3.1.2 "><p id="p819714311388"><a name="p819714311388"></a><a name="p819714311388"></a>展示用户Flink作业的数据输入总数，供监控和调试使用。单位：条。</p>
    </td>
    </tr>
    <tr id="row98391434835"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.3.1.1 "><p id="p650435515382"><a name="p650435515382"></a><a name="p650435515382"></a>Flink作业数据输出总数</p>
    </td>
    <td class="cellrowborder" valign="top" width="72%" headers="mcps1.2.3.1.2 "><p id="p7504105519382"><a name="p7504105519382"></a><a name="p7504105519382"></a>展示用户Flink作业的数据输出总数，供监控和调试使用。单位：条。</p>
    </td>
    </tr>
    <tr id="row46413441321"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.3.1.1 "><p id="p166534412215"><a name="p166534412215"></a><a name="p166534412215"></a>Flink作业字节输入速率</p>
    </td>
    <td class="cellrowborder" valign="top" width="72%" headers="mcps1.2.3.1.2 "><p id="p1465444023"><a name="p1465444023"></a><a name="p1465444023"></a>展示用户Flink作业每秒输入的字节数。单位：字节/秒。</p>
    </td>
    </tr>
    <tr id="row520964337"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.3.1.1 "><p id="p1720919415316"><a name="p1720919415316"></a><a name="p1720919415316"></a>Flink作业字节输出速率</p>
    </td>
    <td class="cellrowborder" valign="top" width="72%" headers="mcps1.2.3.1.2 "><p id="p020934136"><a name="p020934136"></a><a name="p020934136"></a>展示用户Flink作业每秒输出的字节数。单位：字节/秒。</p>
    </td>
    </tr>
    <tr id="row19707742049"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.3.1.1 "><p id="p77261850340"><a name="p77261850340"></a><a name="p77261850340"></a>Flink作业字节输入总数</p>
    </td>
    <td class="cellrowborder" valign="top" width="72%" headers="mcps1.2.3.1.2 "><p id="p17081541247"><a name="p17081541247"></a><a name="p17081541247"></a>展示用户Flink作业字节的输入总数。单位：字节。</p>
    </td>
    </tr>
    <tr id="row2070874947"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.3.1.1 "><p id="p172612501844"><a name="p172612501844"></a><a name="p172612501844"></a>Flink作业字节输出总数</p>
    </td>
    <td class="cellrowborder" valign="top" width="72%" headers="mcps1.2.3.1.2 "><p id="p47081543419"><a name="p47081543419"></a><a name="p47081543419"></a>展示用户Flink作业字节的输出总数。单位：字节。</p>
    </td>
    </tr>
    <tr id="row91712112331"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.3.1.1 "><p id="p1971961912331"><a name="p1971961912331"></a><a name="p1971961912331"></a>Flink作业CPU使用率</p>
    </td>
    <td class="cellrowborder" valign="top" width="72%" headers="mcps1.2.3.1.2 "><p id="p217211113312"><a name="p217211113312"></a><a name="p217211113312"></a>展示用户Flink作业的CPU使用率。单位：%。</p>
    </td>
    </tr>
    <tr id="row125551313163310"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.3.1.1 "><p id="p1537112593320"><a name="p1537112593320"></a><a name="p1537112593320"></a>Flink作业内存使用率</p>
    </td>
    <td class="cellrowborder" valign="top" width="72%" headers="mcps1.2.3.1.2 "><p id="p855631319331"><a name="p855631319331"></a><a name="p855631319331"></a>展示用户Flink作业的内存使用率。单位：%。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 查看作业任务列表<a name="section11677164916529"></a>

用户可以查看作业运行时每个任务的详细信息，例如任务的开始时间、收发字节数和运行时长等。

>![](public_sys-resources/icon-note.gif) **说明：** 
>如果数据为零，表示没有从数据源接收到数据。

1.  在DLI管理控制台的左侧导航栏中，单击“作业管理“\>“Flink作业“，进入Flink作业管理页面。
2.  单击需要查看的作业名称，进入“作业详情“页面。
3.  在“任务列表“页签，可以查看任务的节点信息。

    ![](figures/8-2-13FLink作业详情-任务列表-zh.png)

    -   查看算子任务列表

        **表 3**  算子任务列表参数

        <a name="table19353957173012"></a>
        <table><thead align="left"><tr id="row334914572300"><th class="cellrowborder" valign="top" width="26%" id="mcps1.2.3.1.1"><p id="p10349185753019"><a name="p10349185753019"></a><a name="p10349185753019"></a>参数</p>
        </th>
        <th class="cellrowborder" valign="top" width="74%" id="mcps1.2.3.1.2"><p id="p20349175763013"><a name="p20349175763013"></a><a name="p20349175763013"></a>说明</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row435075713307"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.3.1.1 "><p id="p4349155713302"><a name="p4349155713302"></a><a name="p4349155713302"></a>名称</p>
        </td>
        <td class="cellrowborder" valign="top" width="74%" headers="mcps1.2.3.1.2 "><p id="p14350175710309"><a name="p14350175710309"></a><a name="p14350175710309"></a>算子名称。</p>
        </td>
        </tr>
        <tr id="row935055717304"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.3.1.1 "><p id="p0350145763015"><a name="p0350145763015"></a><a name="p0350145763015"></a>持续时间</p>
        </td>
        <td class="cellrowborder" valign="top" width="74%" headers="mcps1.2.3.1.2 "><p id="p035010573306"><a name="p035010573306"></a><a name="p035010573306"></a>算子运行的持续时间。</p>
        </td>
        </tr>
        <tr id="row11350115710308"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.3.1.1 "><p id="p1435015575300"><a name="p1435015575300"></a><a name="p1435015575300"></a>并行数</p>
        </td>
        <td class="cellrowborder" valign="top" width="74%" headers="mcps1.2.3.1.2 "><p id="p133502571304"><a name="p133502571304"></a><a name="p133502571304"></a>算子中并行的Task的个数。</p>
        </td>
        </tr>
        <tr id="row23502057173015"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.3.1.1 "><p id="p183501857203012"><a name="p183501857203012"></a><a name="p183501857203012"></a>任务</p>
        </td>
        <td class="cellrowborder" valign="top" width="74%" headers="mcps1.2.3.1.2 "><p id="p131723695719"><a name="p131723695719"></a><a name="p131723695719"></a>算子的任务有以下几种：</p>
        <a name="ul271025611574"></a><a name="ul271025611574"></a><ul id="ul271025611574"><li>红色数字表示已失败的Task个数。</li><li>浅灰色数字表示已取消的Task个数。</li><li>黄色数字表示取消中的Task个数。</li><li>绿色数字表示已完成的Task个数。</li><li>蓝色数字表示运行中的Task个数。</li><li>天蓝色数字表示部署中的Task个数。</li><li>深灰色数字表示排队中的Task个数。</li></ul>
        </td>
        </tr>
        <tr id="row19350757193016"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.3.1.1 "><p id="p11350115783020"><a name="p11350115783020"></a><a name="p11350115783020"></a>状态</p>
        </td>
        <td class="cellrowborder" valign="top" width="74%" headers="mcps1.2.3.1.2 "><p id="p83509578304"><a name="p83509578304"></a><a name="p83509578304"></a>算子任务对应的状态。</p>
        </td>
        </tr>
        <tr id="row9228121841310"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.3.1.1 "><p id="p722851817131"><a name="p722851817131"></a><a name="p722851817131"></a>反压状态</p>
        </td>
        <td class="cellrowborder" valign="top" width="74%" headers="mcps1.2.3.1.2 "><p id="p922891818132"><a name="p922891818132"></a><a name="p922891818132"></a>算子的工作负荷状态。包含如下几种状态：</p>
        <a name="ul16378220278"></a><a name="ul16378220278"></a><ul id="ul16378220278"><li>OK：表示工作负荷正常。</li><li>LOW：表示工作负荷略高。DLI处理数据的速度比较快。</li><li>HIGH：表示工作负荷高。源端输入数据的速度比较慢。</li></ul>
        </td>
        </tr>
        <tr id="row4860838276"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.3.1.1 "><p id="p0862153818711"><a name="p0862153818711"></a><a name="p0862153818711"></a>时延</p>
        </td>
        <td class="cellrowborder" valign="top" width="74%" headers="mcps1.2.3.1.2 "><p id="p08623387711"><a name="p08623387711"></a><a name="p08623387711"></a>指事件从源端算子到达本算子的过程中消耗的时间，单位为毫秒（ms）。</p>
        </td>
        </tr>
        <tr id="row10351185711305"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.3.1.1 "><p id="p18350557103013"><a name="p18350557103013"></a><a name="p18350557103013"></a>发送的记录数</p>
        </td>
        <td class="cellrowborder" valign="top" width="74%" headers="mcps1.2.3.1.2 "><p id="p13501957103010"><a name="p13501957103010"></a><a name="p13501957103010"></a>算子发送数据的记录。</p>
        </td>
        </tr>
        <tr id="row3351165713300"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.3.1.1 "><p id="p1735155714307"><a name="p1735155714307"></a><a name="p1735155714307"></a>发送的字节数</p>
        </td>
        <td class="cellrowborder" valign="top" width="74%" headers="mcps1.2.3.1.2 "><p id="p20351145715309"><a name="p20351145715309"></a><a name="p20351145715309"></a>算子发送的字节数。</p>
        </td>
        </tr>
        <tr id="row1035111575306"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.3.1.1 "><p id="p13351115723016"><a name="p13351115723016"></a><a name="p13351115723016"></a>接收的字节数</p>
        </td>
        <td class="cellrowborder" valign="top" width="74%" headers="mcps1.2.3.1.2 "><p id="p123515571300"><a name="p123515571300"></a><a name="p123515571300"></a>算子接收的字节数。</p>
        </td>
        </tr>
        <tr id="row18351145783013"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.3.1.1 "><p id="p535125713309"><a name="p535125713309"></a><a name="p535125713309"></a>收到的记录数</p>
        </td>
        <td class="cellrowborder" valign="top" width="74%" headers="mcps1.2.3.1.2 "><p id="p1835175717307"><a name="p1835175717307"></a><a name="p1835175717307"></a>算子收到数据的记录。</p>
        </td>
        </tr>
        <tr id="row2352105753018"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.3.1.1 "><p id="p1235195723019"><a name="p1235195723019"></a><a name="p1235195723019"></a>开始时间</p>
        </td>
        <td class="cellrowborder" valign="top" width="74%" headers="mcps1.2.3.1.2 "><p id="p10351175717309"><a name="p10351175717309"></a><a name="p10351175717309"></a>算子运行开始时间。</p>
        </td>
        </tr>
        <tr id="row135365783018"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.3.1.1 "><p id="p173521657123013"><a name="p173521657123013"></a><a name="p173521657123013"></a>结束时间</p>
        </td>
        <td class="cellrowborder" valign="top" width="74%" headers="mcps1.2.3.1.2 "><p id="p1078363810354"><a name="p1078363810354"></a><a name="p1078363810354"></a>算子运行结束时间。</p>
        </td>
        </tr>
        </tbody>
        </table>

    -   单击算子名称前的![](figures/icon-cs-expand.png)，可以查看对应算子的并发任务列表。

        **表 4**  Task任务列表参数

        <a name="table3355165733015"></a>
        <table><thead align="left"><tr id="row83541575301"><th class="cellrowborder" valign="top" width="27%" id="mcps1.2.3.1.1"><p id="p9354205713015"><a name="p9354205713015"></a><a name="p9354205713015"></a>参数</p>
        </th>
        <th class="cellrowborder" valign="top" width="73%" id="mcps1.2.3.1.2"><p id="p435485714305"><a name="p435485714305"></a><a name="p435485714305"></a>说明</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row03542057193014"><td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.3.1.1 "><p id="p4161632193117"><a name="p4161632193117"></a><a name="p4161632193117"></a>开始时间</p>
        </td>
        <td class="cellrowborder" valign="top" width="73%" headers="mcps1.2.3.1.2 "><p id="p8354757113015"><a name="p8354757113015"></a><a name="p8354757113015"></a>Task任务运行开始时间。</p>
        </td>
        </tr>
        <tr id="row16354557133015"><td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.3.1.1 "><p id="p10161732113115"><a name="p10161732113115"></a><a name="p10161732113115"></a>结束时间</p>
        </td>
        <td class="cellrowborder" valign="top" width="73%" headers="mcps1.2.3.1.2 "><p id="p20354135733011"><a name="p20354135733011"></a><a name="p20354135733011"></a>Task任务运行结束时间。</p>
        </td>
        </tr>
        <tr id="row1935565712304"><td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.3.1.1 "><p id="p483411366314"><a name="p483411366314"></a><a name="p483411366314"></a>持续时间</p>
        </td>
        <td class="cellrowborder" valign="top" width="73%" headers="mcps1.2.3.1.2 "><p id="p153550571304"><a name="p153550571304"></a><a name="p153550571304"></a>Task任务运行的持续时间。</p>
        </td>
        </tr>
        <tr id="row5355135773010"><td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.3.1.1 "><p id="p122631493211"><a name="p122631493211"></a><a name="p122631493211"></a>接收的字节数</p>
        </td>
        <td class="cellrowborder" valign="top" width="73%" headers="mcps1.2.3.1.2 "><p id="p1435535773019"><a name="p1435535773019"></a><a name="p1435535773019"></a>Task任务接收的字节数。</p>
        </td>
        </tr>
        <tr id="row235513574305"><td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.3.1.1 "><p id="p1722617149329"><a name="p1722617149329"></a><a name="p1722617149329"></a>接受的记录数</p>
        </td>
        <td class="cellrowborder" valign="top" width="73%" headers="mcps1.2.3.1.2 "><p id="p14355135716303"><a name="p14355135716303"></a><a name="p14355135716303"></a>Task任务收到的记录。</p>
        </td>
        </tr>
        <tr id="row15355165733019"><td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.3.1.1 "><p id="p1093243919324"><a name="p1093243919324"></a><a name="p1093243919324"></a>发送的字节数</p>
        </td>
        <td class="cellrowborder" valign="top" width="73%" headers="mcps1.2.3.1.2 "><p id="p1355057143020"><a name="p1355057143020"></a><a name="p1355057143020"></a>Task任务发送的字节数。</p>
        </td>
        </tr>
        <tr id="row1048618383323"><td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.3.1.1 "><p id="p393223923216"><a name="p393223923216"></a><a name="p393223923216"></a>发送的记录数</p>
        </td>
        <td class="cellrowborder" valign="top" width="73%" headers="mcps1.2.3.1.2 "><p id="p1486113812329"><a name="p1486113812329"></a><a name="p1486113812329"></a>Task任务发送的记录。</p>
        </td>
        </tr>
        <tr id="row548733843220"><td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.3.1.1 "><p id="p194878383327"><a name="p194878383327"></a><a name="p194878383327"></a>失败尝试次数</p>
        </td>
        <td class="cellrowborder" valign="top" width="73%" headers="mcps1.2.3.1.2 "><p id="p1848733833217"><a name="p1848733833217"></a><a name="p1848733833217"></a>Task挂掉后恢复尝试次数。</p>
        </td>
        </tr>
        <tr id="row16487203843218"><td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.3.1.1 "><p id="p1048783893214"><a name="p1048783893214"></a><a name="p1048783893214"></a>节点</p>
        </td>
        <td class="cellrowborder" valign="top" width="73%" headers="mcps1.2.3.1.2 "><p id="p1448723863215"><a name="p1448723863215"></a><a name="p1448723863215"></a>算子所在的节点IP</p>
        </td>
        </tr>
        <tr id="row9487338143218"><td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.3.1.1 "><p id="p1548716387321"><a name="p1548716387321"></a><a name="p1548716387321"></a>状态</p>
        </td>
        <td class="cellrowborder" valign="top" width="73%" headers="mcps1.2.3.1.2 "><p id="p20487193813210"><a name="p20487193813210"></a><a name="p20487193813210"></a>Task状态有以下几种：</p>
        <a name="ul198404599454"></a><a name="ul198404599454"></a><ul id="ul198404599454"><li>SCHEDULED：Task计划预热。</li><li>DEPLOYING：Task正在部署。</li><li>RUNNING：Task正在运行。</li><li>FINISHED：Task运行结束。</li><li>CANCELING：Task正在取消。</li><li>CANCELED：Task取消成功。</li><li>FAILED：Task运行失败。</li></ul>
        </td>
        </tr>
        </tbody>
        </table>



## 查看作业执行计划<a name="section9397163320"></a>

用户通过查看执行计划了解到运行中的作业的算子流向。

1.  在DLI管理控制台的左侧导航栏中，单击“作业管理“\>“Flink作业“，进入Flink作业管理页面。
2.  单击需要查看的作业名称，进入“作业详情“页面。

    ![](figures/8-2-13FLink作业详情-作业执行计划-zh.png)

    在“执行计划“页签可以查看作业的算子流向。

    单击对应的节点，在页面右侧显示对应的信息。

    -   滚动鼠标滚轮或者单击![](figures/icon-cs-zoom.png)可对流图进行缩放查看。
    -   流图展示当前运行作业的实时算子流图信息。


## 查看提交作业日志<a name="section18556377020"></a>

用户可以通过查看提交日志排查提交作业异常的故障。

1.  在DLI管理控制台的左侧导航栏中，单击“作业管理“\>“Flink作业“，进入Flink作业管理页面。
2.  单击需要查看的作业名称，进入“作业详情“页面。
3.  在“提交日志“页签，可以查看提交作业的过程信息。

    ![](figures/8-2-13FLink作业详情-提交作业日志-zh.png)


## 查看作业运行日志<a name="section91816183316"></a>

用户可以通过查看运行日志排查作业运行异常的故障。

1.  在DLI管理控制台的左侧导航栏中，单击“作业管理“\>“Flink作业“，进入Flink作业管理页面。
2.  单击需要查看的作业名称，进入“作业详情“页面。
3.  在“运行日志“页签，可以查看运行中作业的JobManager和TaskManager信息。

    ![](figures/8-2-13FLink作业详情-查看作业运行日志-zh.png)

    JobManager和TaskManager信息每分钟刷新一次，默认展示最近一分钟的运行日志，用户也可以单击“历史日志“查看更多日志信息。

    如果作业配置了保存作业日志的OBS桶，更多历史日志信息可以到保存日志的OBS桶中下载查看。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >在OBS中，上传文件的具体方式和要求可以参考《对象存储服务快速入门》\>“[上传对象](https://support.huaweicloud.com/qs-obs/obs_qs_0008.html)”。

    如果作业没有运行，则无法查看TaskManager信息。


## 查看作业标签<a name="section19193157121312"></a>

用户可以查看、添加、修改和删除作业标签。

1.  在DLI管理控制台的左侧导航栏中，单击“作业管理“\>“Flink作业“，进入Flink作业管理页面。
2.  单击需要查看的作业名称，进入“作业详情“页面。
3.  在“标签“页签，显示当前作业的标签信息。

    ![](figures/8-2-13FLink作业详情-标签-zh.png)

    更多关于作业标签的详细信息，请参见[标签管理](标签管理.md)。


