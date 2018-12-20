# Spark作业管理<a name="dli_01_0385"></a>

## 操作场景<a name="zh-cn_topic_0093946892_section31579140143928"></a>

Spark作业为在Spark作业编辑窗口中提交的作业。

## 作业列表<a name="section12526165519235"></a>

作业列表显示所有的Spark作业，作业数量较多时，系统分页显示，您可以查看任何状态下的作业。

>![](public_sys-resources/icon-note.gif) **说明：**   
>作业执行成功后，作业记录只保存6小时。  

**表 1**  作业列表参数

<a name="zh-cn_topic_0122090417_table3950169215120"></a>
<table><thead align="left"><tr id="zh-cn_topic_0122090417_row2555468715120"><th class="cellrowborder" valign="top" width="21.18%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0122090417_p4021197415120"><a name="zh-cn_topic_0122090417_p4021197415120"></a><a name="zh-cn_topic_0122090417_p4021197415120"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="78.82000000000001%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0122090417_p3594448915120"><a name="zh-cn_topic_0122090417_p3594448915120"></a><a name="zh-cn_topic_0122090417_p3594448915120"></a>参数说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0122090417_row46758327132"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p16413434141957"><a name="zh-cn_topic_0122090417_p16413434141957"></a><a name="zh-cn_topic_0122090417_p16413434141957"></a>作业ID</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0122090417_p54419740141957"><a name="zh-cn_topic_0122090417_p54419740141957"></a><a name="zh-cn_topic_0122090417_p54419740141957"></a>所提交Spark作业的ID，由系统默认生成。</p>
</td>
</tr>
<tr id="zh-cn_topic_0122090417_row32873162171713"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p45480448171713"><a name="zh-cn_topic_0122090417_p45480448171713"></a><a name="zh-cn_topic_0122090417_p45480448171713"></a>作业名称</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0122090417_p18579134217227"><a name="zh-cn_topic_0122090417_p18579134217227"></a><a name="zh-cn_topic_0122090417_p18579134217227"></a>所提交Spark作业的名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0122090417_row31011923151038"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p10671857151038"><a name="zh-cn_topic_0122090417_p10671857151038"></a><a name="zh-cn_topic_0122090417_p10671857151038"></a>作业状态</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0122090417_p59114099151038"><a name="zh-cn_topic_0122090417_p59114099151038"></a><a name="zh-cn_topic_0122090417_p59114099151038"></a>作业的状态信息，包括如下。</p>
<a name="zh-cn_topic_0122090417_ul32930526154023"></a><a name="zh-cn_topic_0122090417_ul32930526154023"></a><ul id="zh-cn_topic_0122090417_ul32930526154023"><li>starting：正在启动</li><li>running：正在执行任务</li><li>dead：session已退出</li><li>success：session运行成功</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0122090417_row36301606171658"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p14394959151048"><a name="zh-cn_topic_0122090417_p14394959151048"></a><a name="zh-cn_topic_0122090417_p14394959151048"></a>所属集群</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0122090417_p51238775151048"><a name="zh-cn_topic_0122090417_p51238775151048"></a><a name="zh-cn_topic_0122090417_p51238775151048"></a>所提交Spark作业所在的集群。</p>
</td>
</tr>
<tr id="zh-cn_topic_0122090417_row6424839516213"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p50569641162134"><a name="zh-cn_topic_0122090417_p50569641162134"></a><a name="zh-cn_topic_0122090417_p50569641162134"></a>创建时间</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0122090417_p18910361162145"><a name="zh-cn_topic_0122090417_p18910361162145"></a><a name="zh-cn_topic_0122090417_p18910361162145"></a>每个作业的创建时间，可按创建时间顺序或倒序显示作业列表。</p>
</td>
</tr>
<tr id="zh-cn_topic_0122090417_row1662880815250"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p475621615250"><a name="zh-cn_topic_0122090417_p475621615250"></a><a name="zh-cn_topic_0122090417_p475621615250"></a>操作</p>
</td>
<td class="cellrowborder" valign="top" width="78.82000000000001%" headers="mcps1.2.3.1.2 "><a name="zh-cn_topic_0122090417_ul181927155164"></a><a name="zh-cn_topic_0122090417_ul181927155164"></a><ul id="zh-cn_topic_0122090417_ul181927155164"><li>删除</li><li>日志详情<a name="zh-cn_topic_0122090417_ul94511619309"></a><a name="zh-cn_topic_0122090417_ul94511619309"></a><ul id="zh-cn_topic_0122090417_ul94511619309"><li>当作业状态在“starting”，显示“提交日志”。</li><li>当作业状态在“success”，显示“提交日志”和“运行日志”。</li></ul>
</li></ul>
</td>
</tr>
</tbody>
</table>

## 查找作业<a name="section9242154518244"></a>

1.  在DLI管理控制台的顶部菜单栏中，选择“作业管理“。
2.  在“作业管理“页面，选择“状态”、“作业条数”和“所属集群”，输入“作业ID”。

    系统将根据设置的过滤条件，在作业列表显示符合对应条件的作业。

    **图 1**  查找Spark作业结果<a name="zh-cn_topic_0122090417_fig034812273716"></a>  
    ![](figures/查找Spark作业结果.png "查找Spark作业结果")


## 查看作业详情<a name="zh-cn_topic_0122090417_section15292102065813"></a>

在“作业管理“页面，选中一条作业，单击该作业ID左侧的![](figures/icon-展开.png)或在“操作”列中单击“日志详情”，可查看该条作业的相关日志。

## 终止作业<a name="zh-cn_topic_0122090417_section3753111385816"></a>

在“作业管理“页面，单击“操作”列的“删除“，删除作业。

