# Spark作业管理<a name="dli_01_0385"></a>

## 操作场景<a name="zh-cn_topic_0093946892_section31579140143928"></a>

Spark作业为在Spark作业编辑窗口中提交的作业。

## 作业列表<a name="section12526165519235"></a>

作业列表显示所有的Spark作业，作业数量较多时，系统分页显示，您可以查看任何状态下的作业。

>![](public_sys-resources/icon-note.gif) **说明：**   
>作业执行成功后，作业记录只保存6小时。  

**表 1**  作业列表参数

<a name="zh-cn_topic_0122090417_table3950169215120"></a>
<table><thead align="left"><tr id="zh-cn_topic_0122090417_row2555468715120"><th class="cellrowborder" valign="top" width="16.07%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0122090417_p4021197415120"><a name="zh-cn_topic_0122090417_p4021197415120"></a><a name="zh-cn_topic_0122090417_p4021197415120"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="83.93%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0122090417_p3594448915120"><a name="zh-cn_topic_0122090417_p3594448915120"></a><a name="zh-cn_topic_0122090417_p3594448915120"></a>参数说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0122090417_row46758327132"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p16413434141957"><a name="zh-cn_topic_0122090417_p16413434141957"></a><a name="zh-cn_topic_0122090417_p16413434141957"></a>作业ID</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0122090417_p54419740141957"><a name="zh-cn_topic_0122090417_p54419740141957"></a><a name="zh-cn_topic_0122090417_p54419740141957"></a>所提交Spark作业的ID，由系统默认生成。</p>
</td>
</tr>
<tr id="zh-cn_topic_0122090417_row32873162171713"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p45480448171713"><a name="zh-cn_topic_0122090417_p45480448171713"></a><a name="zh-cn_topic_0122090417_p45480448171713"></a>作业名称</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0122090417_p18579134217227"><a name="zh-cn_topic_0122090417_p18579134217227"></a><a name="zh-cn_topic_0122090417_p18579134217227"></a>所提交Spark作业的名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0122090417_row31011923151038"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p10671857151038"><a name="zh-cn_topic_0122090417_p10671857151038"></a><a name="zh-cn_topic_0122090417_p10671857151038"></a>作业状态</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0122090417_p59114099151038"><a name="zh-cn_topic_0122090417_p59114099151038"></a><a name="zh-cn_topic_0122090417_p59114099151038"></a>作业的状态信息，包括如下。</p>
<a name="zh-cn_topic_0122090417_ul32930526154023"></a><a name="zh-cn_topic_0122090417_ul32930526154023"></a><ul id="zh-cn_topic_0122090417_ul32930526154023"><li>启动中：正在启动</li><li>运行中：正在执行任务</li><li>已失败：session已退出</li><li>已成功：session运行成功</li><li>恢复中：正在恢复任务</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0122090417_row36301606171658"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p14394959151048"><a name="zh-cn_topic_0122090417_p14394959151048"></a><a name="zh-cn_topic_0122090417_p14394959151048"></a>所属集群</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0122090417_p51238775151048"><a name="zh-cn_topic_0122090417_p51238775151048"></a><a name="zh-cn_topic_0122090417_p51238775151048"></a>所提交Spark作业所在的集群。</p>
</td>
</tr>
<tr id="zh-cn_topic_0122090417_row6424839516213"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p50569641162134"><a name="zh-cn_topic_0122090417_p50569641162134"></a><a name="zh-cn_topic_0122090417_p50569641162134"></a>创建时间</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0122090417_p18910361162145"><a name="zh-cn_topic_0122090417_p18910361162145"></a><a name="zh-cn_topic_0122090417_p18910361162145"></a>每个作业的创建时间，可按创建时间顺序或倒序显示作业列表。</p>
</td>
</tr>
<tr id="row1536633125019"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="p145363334505"><a name="p145363334505"></a><a name="p145363334505"></a>最后修改时间</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><p id="p153603315013"><a name="p153603315013"></a><a name="p153603315013"></a>作业运行完成的时间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0122090417_row1662880815250"><td class="cellrowborder" valign="top" width="16.07%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0122090417_p475621615250"><a name="zh-cn_topic_0122090417_p475621615250"></a><a name="zh-cn_topic_0122090417_p475621615250"></a>操作</p>
</td>
<td class="cellrowborder" valign="top" width="83.93%" headers="mcps1.2.3.1.2 "><a name="zh-cn_topic_0122090417_ul181927155164"></a><a name="zh-cn_topic_0122090417_ul181927155164"></a><ul id="zh-cn_topic_0122090417_ul181927155164"><li>删除：删除当前作业。</li><li>日志详情<a name="zh-cn_topic_0122090417_ul94511619309"></a><a name="zh-cn_topic_0122090417_ul94511619309"></a><ul id="zh-cn_topic_0122090417_ul94511619309"><li>当作业状态在“运行中”，“日志类型”显示“提交日志”。</li><li>当作业状态在“已成功”或“已失败”，“日志类型”显示“提交日志”和“运行日志”。</li></ul>
</li><li>重新执行：重新执行当前作业。</li><li>Spark UI：单击后，将跳转至Spark任务运行情况界面。</li></ul>
</td>
</tr>
</tbody>
</table>

## 查找作业<a name="section9242154518244"></a>

1.  在DLI管理控制台的顶部菜单栏中，选择“作业管理“。
2.  在“作业管理“页面，选择“状态”和“所属集群”。

    系统将根据设置的过滤条件，在作业列表显示符合对应条件的作业。

    **图 1**  查找Spark作业结果<a name="zh-cn_topic_0122090417_fig034812273716"></a>  
    ![](figures/查找Spark作业结果.png "查找Spark作业结果")


## 查看作业详情<a name="zh-cn_topic_0122090417_section15292102065813"></a>

在“作业管理“页面，选中一条作业，单击该作业ID左侧的![](figures/icon-展开.png)或在“操作”列中单击“日志详情”，可查看该条作业的相关日志。

## 终止作业<a name="zh-cn_topic_0122090417_section3753111385816"></a>

在“作业管理“页面，单击“操作”列的“删除“，删除作业。

## 创建消息通知主题<a name="section176748522033"></a>

确定创建消息通知主题后，您可在消息通知服务的“主题管理”页面中，对对应的主题“添加订阅”，选择不同方式（例如短信或者邮件等）进行订阅；订阅成功后，若作业失败，则系统将会自动发送消息到您指定的订阅终端。具体操作如下：

1.  在Spark作业管理页面，单击![](figures/icon-创建消息通知主题.png)，弹出[图2](#fig969753431112)所示对话框。

    **图 2**  创建消息通知主题<a name="fig969753431112"></a>  
    ![](figures/创建消息通知主题.png "创建消息通知主题")

2.  单击“确定”。弹出[图3](#fig12471323125315)所示对话框。

    **图 3**  创建主题成功<a name="fig12471323125315"></a>  
    ![](figures/创建主题成功.png "创建主题成功")

3.  单击[图3](#fig12471323125315)中“主题管理”，跳转至消息通知服务“主题管理”页面。

    **图 4**  主题管理<a name="fig361113238574"></a>  
    ![](figures/主题管理.png "主题管理")

4.  在[图4](#fig361113238574)对应主题的“操作”栏中，单击“添加订阅”，即可在[图5](#fig075918101718)对话框中，选择“协议”，确定订阅方式。

    **图 5**  添加订阅<a name="fig075918101718"></a>  
    ![](figures/添加订阅.png "添加订阅")

5.  返回[图3](#fig12471323125315)所在页面，单击“确定”，完成创建消息通知主题。

