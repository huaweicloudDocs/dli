# 将DLI数据导出至OBS<a name="dli_01_0010"></a>

## 操作场景<a name="section10579446195716"></a>

-   支持将数据从DLI表或OBS表导出到OBS服务，导出操作将在OBS服务新建文件夹，导出结果存储在此文件夹中。
-   支持导出CSV格式的文件，且文本格式仅支持UTF-8。

## 操作步骤<a name="section42958999144515"></a>

1.  导出数据的操作入口有两个，分别在“数据管理“和“作业编辑器“页面。
    -   在“数据管理“页面导出数据。
        1.  在SQL作业管理控制台的顶部菜单栏中，选择“数据管理“。
        2.  在“数据管理“页面，单击需导出数据对应数据库名称，进入该数据库“表管理”页面。
        3.  选中目标表，单击“操作”栏中的“更多“，选择“导出“。

    -   在“作业编辑器“页面导出数据。
        1.  在SQL作业管理控制台的顶部菜单栏中，选择“作业编辑器“。
        2.  SQL语句执行成功后，在执行结果窗口右侧，单击“导出结果“，弹出“导出数据“对话框。


2.  在“导出数据“对话框，参考[表1](#table7742063143659)填写导出数据相关信息。

    **图 1**  导出数据<a name="fig627344359518"></a>  
    ![](figures/导出数据.png "导出数据")

    **表 1**  参数说明

    <a name="table7742063143659"></a>
    <table><thead align="left"><tr id="row48986708143659"><th class="cellrowborder" valign="top" width="13.8%" id="mcps1.2.3.1.1"><p id="p8500389143659"><a name="p8500389143659"></a><a name="p8500389143659"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="86.2%" id="mcps1.2.3.1.2"><p id="p17442940143659"><a name="p17442940143659"></a><a name="p17442940143659"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row55162434145333"><td class="cellrowborder" valign="top" width="13.8%" headers="mcps1.2.3.1.1 "><p id="p21307823145337"><a name="p21307823145337"></a><a name="p21307823145337"></a>数据库名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="86.2%" headers="mcps1.2.3.1.2 "><p id="p48212085145337"><a name="p48212085145337"></a><a name="p48212085145337"></a>当前表所在的数据库，该值不可修改。</p>
    </td>
    </tr>
    <tr id="row54786783145255"><td class="cellrowborder" valign="top" width="13.8%" headers="mcps1.2.3.1.1 "><p id="p5670283814532"><a name="p5670283814532"></a><a name="p5670283814532"></a>表名</p>
    </td>
    <td class="cellrowborder" valign="top" width="86.2%" headers="mcps1.2.3.1.2 "><p id="p2952718314532"><a name="p2952718314532"></a><a name="p2952718314532"></a>当前表名称，该值不可修改。</p>
    </td>
    </tr>
    <tr id="row59287839143659"><td class="cellrowborder" valign="top" width="13.8%" headers="mcps1.2.3.1.1 "><p id="p37585653143659"><a name="p37585653143659"></a><a name="p37585653143659"></a>导出格式</p>
    </td>
    <td class="cellrowborder" valign="top" width="86.2%" headers="mcps1.2.3.1.2 "><p id="p24539023143659"><a name="p24539023143659"></a><a name="p24539023143659"></a>导出数据的文件格式。当前只支持csv格式。</p>
    </td>
    </tr>
    <tr id="row33984858114535"><td class="cellrowborder" valign="top" width="13.8%" headers="mcps1.2.3.1.1 "><p id="p1310090114535"><a name="p1310090114535"></a><a name="p1310090114535"></a>队列</p>
    </td>
    <td class="cellrowborder" valign="top" width="86.2%" headers="mcps1.2.3.1.2 "><p id="p39008475114535"><a name="p39008475114535"></a><a name="p39008475114535"></a>选择队列。</p>
    </td>
    </tr>
    <tr id="row1774342414552"><td class="cellrowborder" valign="top" width="13.8%" headers="mcps1.2.3.1.1 "><p id="p2547309214552"><a name="p2547309214552"></a><a name="p2547309214552"></a>压缩格式</p>
    </td>
    <td class="cellrowborder" valign="top" width="86.2%" headers="mcps1.2.3.1.2 "><p id="p5005459614552"><a name="p5005459614552"></a><a name="p5005459614552"></a>导出数据的压缩方式，选择如下压缩方式。</p>
    <a name="ul35000658144913"></a><a name="ul35000658144913"></a><ul id="ul35000658144913"><li>none</li><li>bzip2</li><li>deflate</li><li>gzip</li></ul>
    </td>
    </tr>
    <tr id="row6367025143659"><td class="cellrowborder" valign="top" width="13.8%" headers="mcps1.2.3.1.1 "><p id="p3346061614541"><a name="p3346061614541"></a><a name="p3346061614541"></a>导出路径</p>
    </td>
    <td class="cellrowborder" valign="top" width="86.2%" headers="mcps1.2.3.1.2 "><a name="ul194291955145519"></a><a name="ul194291955145519"></a><ul id="ul194291955145519"><li>直接输入OBS路径或单击<a name="image07131523648"></a><a name="image07131523648"></a><span><img id="image07131523648" src="figures/icon-浏览.png"></span>选择OBS的路径。路径须以<span class="parmname" id="parmname64912034172226"><a name="parmname64912034172226"></a><a name="parmname64912034172226"></a>“s3a://”</span>开头。</li><li>导出路径必须为OBS桶中不存在的文件夹，即用户需在OBS目标路径后创建一个新文件夹。</li><li>文件夹名称不能包含下列特殊字符：\ / : * ? " &lt; &gt; |，并且不能以“.”开头和结尾。</li></ul>
    </td>
    </tr>
    <tr id="row48430784114641"><td class="cellrowborder" valign="top" width="13.8%" headers="mcps1.2.3.1.1 "><p id="p30579455114641"><a name="p30579455114641"></a><a name="p30579455114641"></a>导出方式</p>
    </td>
    <td class="cellrowborder" valign="top" width="86.2%" headers="mcps1.2.3.1.2 "><p id="p61016786114641"><a name="p61016786114641"></a><a name="p61016786114641"></a>导出数据的保存方式。</p>
    <a name="ul625034191496"></a><a name="ul625034191496"></a><ul id="ul625034191496"><li>导出到已有OBS目录：在指定目录下新建文件，会删除已有文件。</li><li>随导出自建OBS目录：指定的导出目录必须不存在，如果指定目录已经存在，系统将返回错误信息，无法执行导出操作。</li></ul>
    </td>
    </tr>
    <tr id="row1218154413337"><td class="cellrowborder" valign="top" width="13.8%" headers="mcps1.2.3.1.1 "><p id="p44720296144515"><a name="p44720296144515"></a><a name="p44720296144515"></a>表头</p>
    </td>
    <td class="cellrowborder" valign="top" width="86.2%" headers="mcps1.2.3.1.2 "><p id="p1262888185911"><a name="p1262888185911"></a><a name="p1262888185911"></a>当<span class="parmname" id="parmname3628138105919"><a name="parmname3628138105919"></a><a name="parmname3628138105919"></a>“导出格式”</span>为<span class="parmvalue" id="parmvalue146286818592"><a name="parmvalue146286818592"></a><a name="parmvalue146286818592"></a>“CSV”</span>时该参数有效。当前只支持CSV格式。</p>
    <p id="p37255200172441"><a name="p37255200172441"></a><a name="p37255200172441"></a>设置导出数据是否含表头。选中<span class="parmvalue" id="parmvalue51149381152733"><a name="parmvalue51149381152733"></a><a name="parmvalue51149381152733"></a>“高级选项”</span>，勾选表头前的方框表示有表头，去勾选表示无表头。</p>
    </td>
    </tr>
    </tbody>
    </table>

3.  单击“确定“即可导出数据。
4.  （可选）您可以在“作业管理“查看导出作业的“作业状态“、“执行语句“等信息。
    1.  在“作业类型“中选择“EXPORT“，输入导出数据的时间段，即可查询出对应条件下的作业列表。
    2.  单击导出作业的![](figures/icon-展开.png)，可查看导出作业的详细信息。


