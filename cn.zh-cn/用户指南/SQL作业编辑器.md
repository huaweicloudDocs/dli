# SQL作业编辑器<a name="dli_01_0320"></a>

SQL作业编辑器支持使用SQL语句执行数据查询操作。支持SQL2003，兼容SparkSQL，详细语法描述请参见[《数据湖探索SQL语法参考》](https://support.huaweicloud.com/sqlreference-dli/dli_08_0001.html)。

在总览页面单击SQL作业右上角![](figures/icon-创建作业-4.png)，可进入SQL作业“作业编辑器”页面。

## 界面说明<a name="zh-cn_topic_0093946815_section56922894165137"></a>

介绍“作业编辑器“页面中的区域和按键功能。

**图 1**  SQL作业导航栏<a name="fig452563612140"></a>  
![](figures/SQL作业导航栏.png "SQL作业导航栏")

**表 1**  导航栏按键说明

<a name="table1357419814715"></a>
<table><thead align="left"><tr id="row105761087712"><th class="cellrowborder" valign="top" width="5.75%" id="mcps1.2.4.1.1"><p id="p1545152013421"><a name="p1545152013421"></a><a name="p1545152013421"></a>序号</p>
</th>
<th class="cellrowborder" valign="top" width="13.34%" id="mcps1.2.4.1.2"><p id="p6536192015152"><a name="p6536192015152"></a><a name="p6536192015152"></a>按键</p>
</th>
<th class="cellrowborder" valign="top" width="80.91000000000001%" id="mcps1.2.4.1.3"><p id="p5539122041514"><a name="p5539122041514"></a><a name="p5539122041514"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row5510457102015"><td class="cellrowborder" valign="top" width="5.75%" headers="mcps1.2.4.1.1 "><p id="p0545142084214"><a name="p0545142084214"></a><a name="p0545142084214"></a>6</p>
</td>
<td class="cellrowborder" valign="top" width="13.34%" headers="mcps1.2.4.1.2 "><p id="p451112576203"><a name="p451112576203"></a><a name="p451112576203"></a>数据库</p>
</td>
<td class="cellrowborder" valign="top" width="80.91000000000001%" headers="mcps1.2.4.1.3 "><p id="p75761589710"><a name="p75761589710"></a><a name="p75761589710"></a>显示已有的数据库及其下所有的表。</p>
<div class="note" id="note21812225470"><a name="note21812225470"></a><a name="note21812225470"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul10186152210479"></a><a name="ul10186152210479"></a><ul id="ul10186152210479"><li>单击数据库名，将显示该数据库中的表。</li><li>单击表名，将在表名下显示该表中的元数据，最多可显示20个元数据。</li><li>双击表名，将在作业编辑窗口自动输入SQL查询语句。</li></ul>
</div></div>
</td>
</tr>
<tr id="row0576181717"><td class="cellrowborder" valign="top" width="5.75%" headers="mcps1.2.4.1.1 "><p id="p754512016421"><a name="p754512016421"></a><a name="p754512016421"></a>7</p>
</td>
<td class="cellrowborder" valign="top" width="13.34%" headers="mcps1.2.4.1.2 "><p id="p2576081473"><a name="p2576081473"></a><a name="p2576081473"></a>队列</p>
</td>
<td class="cellrowborder" valign="top" width="80.91000000000001%" headers="mcps1.2.4.1.3 "><p id="p582103264711"><a name="p582103264711"></a><a name="p582103264711"></a>显示已有的队列。</p>
</td>
</tr>
<tr id="row1157678977"><td class="cellrowborder" valign="top" width="5.75%" headers="mcps1.2.4.1.1 "><p id="p254572034211"><a name="p254572034211"></a><a name="p254572034211"></a>8</p>
</td>
<td class="cellrowborder" valign="top" width="13.34%" headers="mcps1.2.4.1.2 "><p id="p0576138971"><a name="p0576138971"></a><a name="p0576138971"></a>隐藏/显示</p>
</td>
<td class="cellrowborder" valign="top" width="80.91000000000001%" headers="mcps1.2.4.1.3 "><p id="p135761987719"><a name="p135761987719"></a><a name="p135761987719"></a>隐藏/显示导航栏。</p>
</td>
</tr>
<tr id="row95761281676"><td class="cellrowborder" valign="top" width="5.75%" headers="mcps1.2.4.1.1 "><p id="p15545520164216"><a name="p15545520164216"></a><a name="p15545520164216"></a>9</p>
</td>
<td class="cellrowborder" valign="top" width="13.34%" headers="mcps1.2.4.1.2 "><p id="p17576168971"><a name="p17576168971"></a><a name="p17576168971"></a>创建</p>
</td>
<td class="cellrowborder" valign="top" width="80.91000000000001%" headers="mcps1.2.4.1.3 "><p id="p1740318544551"><a name="p1740318544551"></a><a name="p1740318544551"></a>包括创建队列、数据库和表。</p>
</td>
</tr>
<tr id="row1857619810717"><td class="cellrowborder" valign="top" width="5.75%" headers="mcps1.2.4.1.1 "><p id="p1654572011426"><a name="p1654572011426"></a><a name="p1654572011426"></a>10</p>
</td>
<td class="cellrowborder" valign="top" width="13.34%" headers="mcps1.2.4.1.2 "><p id="p189637104529"><a name="p189637104529"></a><a name="p189637104529"></a>刷新</p>
</td>
<td class="cellrowborder" valign="top" width="80.91000000000001%" headers="mcps1.2.4.1.3 "><p id="p1296341016522"><a name="p1296341016522"></a><a name="p1296341016522"></a>包括刷新已有的队列、数据库和表列表。</p>
</td>
</tr>
</tbody>
</table>

**图 2**  SQL作业编辑窗口<a name="fig12259471592"></a>  
![](figures/SQL作业编辑窗口.png "SQL作业编辑窗口")

**表 2**  作业编辑窗口说明

<a name="table18913103220552"></a>
<table><thead align="left"><tr id="row169141932105516"><th class="cellrowborder" valign="top" width="6.297029702970297%" id="mcps1.2.4.1.1"><p id="p233145451119"><a name="p233145451119"></a><a name="p233145451119"></a>序号</p>
</th>
<th class="cellrowborder" valign="top" width="11.306930693069306%" id="mcps1.2.4.1.2"><p id="p660634117106"><a name="p660634117106"></a><a name="p660634117106"></a>按键</p>
</th>
<th class="cellrowborder" valign="top" width="82.3960396039604%" id="mcps1.2.4.1.3"><p id="p1161019414106"><a name="p1161019414106"></a><a name="p1161019414106"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1591463215551"><td class="cellrowborder" valign="top" width="6.297029702970297%" headers="mcps1.2.4.1.1 "><p id="p93385451112"><a name="p93385451112"></a><a name="p93385451112"></a>11</p>
</td>
<td class="cellrowborder" valign="top" width="11.306930693069306%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0093946815_p42476751171120"><a name="zh-cn_topic_0093946815_p42476751171120"></a><a name="zh-cn_topic_0093946815_p42476751171120"></a>队列名</p>
</td>
<td class="cellrowborder" valign="top" width="82.3960396039604%" headers="mcps1.2.4.1.3 "><p id="p1045411185210"><a name="p1045411185210"></a><a name="p1045411185210"></a>下拉选择需要使用的队列。如果没有可用队列，此处显示“请选择队列”，请先创建队列。</p>
</td>
</tr>
<tr id="row79141324554"><td class="cellrowborder" valign="top" width="6.297029702970297%" headers="mcps1.2.4.1.1 "><p id="p1233654161115"><a name="p1233654161115"></a><a name="p1233654161115"></a>12</p>
</td>
<td class="cellrowborder" valign="top" width="11.306930693069306%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0093946815_p15920355171120"><a name="zh-cn_topic_0093946815_p15920355171120"></a><a name="zh-cn_topic_0093946815_p15920355171120"></a>数据库名</p>
</td>
<td class="cellrowborder" valign="top" width="82.3960396039604%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0093946815_p14480403171120"><a name="zh-cn_topic_0093946815_p14480403171120"></a><a name="zh-cn_topic_0093946815_p14480403171120"></a>下拉选择需要使用的数据库。如果没有可用数据库，此处显示“请选择数据库”，请先创建数据库。</p>
<div class="note" id="note163344794910"><a name="note163344794910"></a><a name="note163344794910"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p563324794919"><a name="p563324794919"></a><a name="p563324794919"></a>如果SQL语句中指定了表所在的数据库，则此处选择的数据库无效。</p>
</div></div>
</td>
</tr>
<tr id="row79148327558"><td class="cellrowborder" valign="top" width="6.297029702970297%" headers="mcps1.2.4.1.1 "><p id="p73375471110"><a name="p73375471110"></a><a name="p73375471110"></a>13</p>
</td>
<td class="cellrowborder" valign="top" width="11.306930693069306%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0093946815_p20122653171120"><a name="zh-cn_topic_0093946815_p20122653171120"></a><a name="zh-cn_topic_0093946815_p20122653171120"></a>执行</p>
</td>
<td class="cellrowborder" valign="top" width="82.3960396039604%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0093946815_p19322157171120"><a name="zh-cn_topic_0093946815_p19322157171120"></a><a name="zh-cn_topic_0093946815_p19322157171120"></a>执行作业编辑窗口中的SQL语句。</p>
</td>
</tr>
<tr id="row591433295513"><td class="cellrowborder" valign="top" width="6.297029702970297%" headers="mcps1.2.4.1.1 "><p id="p163325401111"><a name="p163325401111"></a><a name="p163325401111"></a>14</p>
</td>
<td class="cellrowborder" valign="top" width="11.306930693069306%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0093946815_p10118717157"><a name="zh-cn_topic_0093946815_p10118717157"></a><a name="zh-cn_topic_0093946815_p10118717157"></a>格式化</p>
</td>
<td class="cellrowborder" valign="top" width="82.3960396039604%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0093946815_p819621917157"><a name="zh-cn_topic_0093946815_p819621917157"></a><a name="zh-cn_topic_0093946815_p819621917157"></a>格式化SQL语句。</p>
<div class="note" id="note11930151811175"><a name="note11930151811175"></a><a name="note11930151811175"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p793271811715"><a name="p793271811715"></a><a name="p793271811715"></a>若窗口中没有SQL语句，该按键禁用。</p>
</div></div>
</td>
</tr>
<tr id="row121419147521"><td class="cellrowborder" valign="top" width="6.297029702970297%" headers="mcps1.2.4.1.1 "><p id="p11510146522"><a name="p11510146522"></a><a name="p11510146522"></a>15</p>
</td>
<td class="cellrowborder" valign="top" width="11.306930693069306%" headers="mcps1.2.4.1.2 "><p id="p1715141418529"><a name="p1715141418529"></a><a name="p1715141418529"></a>语法参考</p>
</td>
<td class="cellrowborder" valign="top" width="82.3960396039604%" headers="mcps1.2.4.1.3 "><p id="p515161410521"><a name="p515161410521"></a><a name="p515161410521"></a>《数据湖探索SQL语法参考》链接。</p>
</td>
</tr>
<tr id="row17600951132211"><td class="cellrowborder" valign="top" width="6.297029702970297%" headers="mcps1.2.4.1.1 "><p id="p1600115118227"><a name="p1600115118227"></a><a name="p1600115118227"></a>15</p>
</td>
<td class="cellrowborder" valign="top" width="11.306930693069306%" headers="mcps1.2.4.1.2 "><p id="p14722170162310"><a name="p14722170162310"></a><a name="p14722170162310"></a>设置</p>
</td>
<td class="cellrowborder" valign="top" width="82.3960396039604%" headers="mcps1.2.4.1.3 "><p id="p13725140112319"><a name="p13725140112319"></a><a name="p13725140112319"></a>以“key/value”的形式设置提交SQL作业的属性。详细内容请参见《数据湖探索API参考》&gt;<a href="https://support.huaweicloud.com/api-dli/dli_02_0102.html" target="_blank" rel="noopener noreferrer">《提交SQL作业（推荐）》</a>&gt;“表2 请求参数”中“conf”参数的说明。最多可设置10个属性。</p>
</td>
</tr>
<tr id="row1791418324558"><td class="cellrowborder" valign="top" width="6.297029702970297%" headers="mcps1.2.4.1.1 "><p id="p1933175491115"><a name="p1933175491115"></a><a name="p1933175491115"></a>16</p>
</td>
<td class="cellrowborder" valign="top" width="11.306930693069306%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0093946815_p60099992171120"><a name="zh-cn_topic_0093946815_p60099992171120"></a><a name="zh-cn_topic_0093946815_p60099992171120"></a>更多</p>
</td>
<td class="cellrowborder" valign="top" width="82.3960396039604%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0093946815_p36261170171120"><a name="zh-cn_topic_0093946815_p36261170171120"></a><a name="zh-cn_topic_0093946815_p36261170171120"></a>包括：</p>
<a name="ul59151629162312"></a><a name="ul59151629162312"></a><ul id="ul59151629162312"><li>语法校验：判断SQL语句编写是否正确。</li><li>设为模板：将常用的SQL语句设为模板。具体操作请参见<a href="SQL模板管理.md">SQL模板管理</a>。</li><li>选择模板：选择已保存为模板的SQL语句。</li><li>切换主题：选择白底黑字或黑底白字。</li></ul>
</td>
</tr>
<tr id="row102037812149"><td class="cellrowborder" valign="top" width="6.297029702970297%" headers="mcps1.2.4.1.1 "><p id="p3334540115"><a name="p3334540115"></a><a name="p3334540115"></a>17</p>
</td>
<td class="cellrowborder" valign="top" width="11.306930693069306%" headers="mcps1.2.4.1.2 "><p id="p1920319815141"><a name="p1920319815141"></a><a name="p1920319815141"></a>光标位置</p>
</td>
<td class="cellrowborder" valign="top" width="82.3960396039604%" headers="mcps1.2.4.1.3 "><p id="p1420316811418"><a name="p1420316811418"></a><a name="p1420316811418"></a>标识光标在作业编辑窗口中的位置（行，列）。</p>
</td>
</tr>
<tr id="row52031287149"><td class="cellrowborder" valign="top" width="6.297029702970297%" headers="mcps1.2.4.1.1 "><p id="p1133175471115"><a name="p1133175471115"></a><a name="p1133175471115"></a>18</p>
</td>
<td class="cellrowborder" valign="top" width="11.306930693069306%" headers="mcps1.2.4.1.2 "><p id="p414053541419"><a name="p414053541419"></a><a name="p414053541419"></a>快捷键</p>
</td>
<td class="cellrowborder" valign="top" width="82.3960396039604%" headers="mcps1.2.4.1.3 "><p id="p142031189146"><a name="p142031189146"></a><a name="p142031189146"></a>快捷键介绍具体请参考<a href="#table209301155311">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  快捷键说明

<a name="table209301155311"></a>
<table><thead align="left"><tr id="row3931151518319"><th class="cellrowborder" valign="top" width="22.759999999999998%" id="mcps1.2.3.1.1"><p id="p49315151839"><a name="p49315151839"></a><a name="p49315151839"></a>快捷键</p>
</th>
<th class="cellrowborder" valign="top" width="77.24%" id="mcps1.2.3.1.2"><p id="p119313159314"><a name="p119313159314"></a><a name="p119313159314"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row119311915038"><td class="cellrowborder" valign="top" width="22.759999999999998%" headers="mcps1.2.3.1.1 "><p id="p1393131514314"><a name="p1393131514314"></a><a name="p1393131514314"></a>Ctrl+R或Ctrl+Enter</p>
</td>
<td class="cellrowborder" valign="top" width="77.24%" headers="mcps1.2.3.1.2 "><p id="p15931161514320"><a name="p15931161514320"></a><a name="p15931161514320"></a>执行SQL。通过按下键盘上的Ctrl+R或Ctrl + Enter，您可以执行SQL语句。</p>
</td>
</tr>
<tr id="row1793118157315"><td class="cellrowborder" valign="top" width="22.759999999999998%" headers="mcps1.2.3.1.1 "><p id="p093181512318"><a name="p093181512318"></a><a name="p093181512318"></a>Ctrl+F</p>
</td>
<td class="cellrowborder" valign="top" width="77.24%" headers="mcps1.2.3.1.2 "><p id="p179321615337"><a name="p179321615337"></a><a name="p179321615337"></a>格式化SQL。通过按下键盘上的Ctrl + F，您可以将SQL语句格式化。</p>
</td>
</tr>
<tr id="row19751851161216"><td class="cellrowborder" valign="top" width="22.759999999999998%" headers="mcps1.2.3.1.1 "><p id="p1977172910156"><a name="p1977172910156"></a><a name="p1977172910156"></a>Ctrl+Q</p>
</td>
<td class="cellrowborder" valign="top" width="77.24%" headers="mcps1.2.3.1.2 "><p id="p1977152921516"><a name="p1977152921516"></a><a name="p1977152921516"></a>语法校验。通过按下键盘上的Ctrl + Q，您可以对SQL语句进行语法校验。</p>
</td>
</tr>
<tr id="row159326153319"><td class="cellrowborder" valign="top" width="22.759999999999998%" headers="mcps1.2.3.1.1 "><p id="p1093215151731"><a name="p1093215151731"></a><a name="p1093215151731"></a>Ctrl+Z</p>
</td>
<td class="cellrowborder" valign="top" width="77.24%" headers="mcps1.2.3.1.2 "><p id="p19325151236"><a name="p19325151236"></a><a name="p19325151236"></a>回退。通过按下键盘上的Ctrl + Z，您可以将作业编辑窗口中的SQL语句回退到前一步操作的状态。例如，将格式化的SQL语句，回退到格式化之前。类似于常用的撤销功能。</p>
</td>
</tr>
<tr id="row166952451254"><td class="cellrowborder" valign="top" width="22.759999999999998%" headers="mcps1.2.3.1.1 "><p id="p1069618456512"><a name="p1069618456512"></a><a name="p1069618456512"></a>Tab</p>
</td>
<td class="cellrowborder" valign="top" width="77.24%" headers="mcps1.2.3.1.2 "><p id="p869674517515"><a name="p869674517515"></a><a name="p869674517515"></a>自动联想。通过按下键盘上的Tab键，您可以快速寻找所需的SQL语句关键词，数据库名和表名。</p>
<div class="note" id="note184721025102919"><a name="note184721025102919"></a><a name="note184721025102919"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul1147232519297"></a><a name="ul1147232519297"></a><ul id="ul1147232519297"><li>按下Tab键时，需保证鼠标光标位于作业编辑窗口中。</li><li>若在作业编辑窗口中没有内容，提示的内容将按照数字，字母顺序排列。</li><li>若在作业编辑窗口中给出关键词的首字母，提示的内容将包含以此首字母开头的SQL语句关键词，数据库名和表名。</li></ul>
</div></div>
</td>
</tr>
<tr id="row10251103142919"><td class="cellrowborder" valign="top" width="22.759999999999998%" headers="mcps1.2.3.1.1 "><p id="p172521317293"><a name="p172521317293"></a><a name="p172521317293"></a>F11</p>
</td>
<td class="cellrowborder" valign="top" width="77.24%" headers="mcps1.2.3.1.2 "><p id="p16252231112914"><a name="p16252231112914"></a><a name="p16252231112914"></a>全屏。通过按下键盘上的F11，您可将SQL作业编辑器窗口全屏。再次按下F11，将从全屏复原。</p>
</td>
</tr>
</tbody>
</table>

**图 3**  SQL语句执行结果窗口<a name="fig20565174552915"></a>  
![](figures/SQL语句执行结果窗口.png "SQL语句执行结果窗口")

**表 4**  SQL语句执行结果窗口说明

<a name="table191717406376"></a>
<table><thead align="left"><tr id="row1517115405378"><th class="cellrowborder" valign="top" width="7.5200000000000005%" id="mcps1.2.4.1.1"><p id="p1395619720284"><a name="p1395619720284"></a><a name="p1395619720284"></a>序号</p>
</th>
<th class="cellrowborder" valign="top" width="22.32%" id="mcps1.2.4.1.2"><p id="p9265164803810"><a name="p9265164803810"></a><a name="p9265164803810"></a>按键</p>
</th>
<th class="cellrowborder" valign="top" width="70.16%" id="mcps1.2.4.1.3"><p id="p15268114814387"><a name="p15268114814387"></a><a name="p15268114814387"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row6171164015374"><td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.2.4.1.1 "><p id="p39561771287"><a name="p39561771287"></a><a name="p39561771287"></a>20</p>
</td>
<td class="cellrowborder" valign="top" width="22.32%" headers="mcps1.2.4.1.2 "><p id="p171584213411"><a name="p171584213411"></a><a name="p171584213411"></a>图表展示</p>
</td>
<td class="cellrowborder" valign="top" width="70.16%" headers="mcps1.2.4.1.3 "><p id="p6715114283415"><a name="p6715114283415"></a><a name="p6715114283415"></a>以图形/表格的形式展示查询结果。</p>
</td>
</tr>
<tr id="row21719402371"><td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.2.4.1.1 "><p id="p59565782814"><a name="p59565782814"></a><a name="p59565782814"></a>21</p>
</td>
<td class="cellrowborder" valign="top" width="22.32%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0093946815_p31901983172641"><a name="zh-cn_topic_0093946815_p31901983172641"></a><a name="zh-cn_topic_0093946815_p31901983172641"></a>导出结果</p>
</td>
<td class="cellrowborder" valign="top" width="70.16%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0093946815_p33923791172641"><a name="zh-cn_topic_0093946815_p33923791172641"></a><a name="zh-cn_topic_0093946815_p33923791172641"></a>将查询结果导出到OBS。具体操作介绍请参考<a href="SQL作业管理.md#section1152211221244">导出结果</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  SQL语句执行历史窗口说明

<a name="table1326105014228"></a>
<table><thead align="left"><tr id="row72623501226"><th class="cellrowborder" valign="top" width="10.311398354876617%" id="mcps1.2.4.1.1"><p id="p7262950192211"><a name="p7262950192211"></a><a name="p7262950192211"></a>序号</p>
</th>
<th class="cellrowborder" valign="top" width="20.48570309439875%" id="mcps1.2.4.1.2"><p id="p14262750172213"><a name="p14262750172213"></a><a name="p14262750172213"></a>区域</p>
</th>
<th class="cellrowborder" valign="top" width="69.20289855072464%" id="mcps1.2.4.1.3"><p id="p72631250142216"><a name="p72631250142216"></a><a name="p72631250142216"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row182641050102219"><td class="cellrowborder" valign="top" width="10.311398354876617%" headers="mcps1.2.4.1.1 "><p id="p3264550132212"><a name="p3264550132212"></a><a name="p3264550132212"></a>22</p>
</td>
<td class="cellrowborder" valign="top" width="20.48570309439875%" headers="mcps1.2.4.1.2 "><p id="p22643505228"><a name="p22643505228"></a><a name="p22643505228"></a>执行历史（最近一周）</p>
</td>
<td class="cellrowborder" valign="top" width="69.20289855072464%" headers="mcps1.2.4.1.3 "><a name="ul2264125020229"></a><a name="ul2264125020229"></a><ul id="ul2264125020229"><li>执行历史（最近一周）：显示最近一周提交的作业的信息。包括：<a name="ul18264135092218"></a><a name="ul18264135092218"></a><ul id="ul18264135092218"><li>队列名称</li><li>创建时间</li><li>状态</li><li>执行语句</li><li>操作：重新执行/终止/SparkUI/下载到本地</li></ul>
<p id="p62655503226"><a name="p62655503226"></a><a name="p62655503226"></a>可以通过以下方式筛选执行历史：</p>
<a name="ul1126535015221"></a><a name="ul1126535015221"></a><ul id="ul1126535015221"><li>在右上角选择队列名称或输入执行语句</li><li>在列表中选择创建时间顺序/倒序排列</li><li>在列表中选择作业状态</li></ul>
</li></ul>
</td>
</tr>
</tbody>
</table>

## 操作步骤<a name="zh-cn_topic_0093946815_section6030699152035"></a>

1.  登录数据湖探索管理控制台，选择SQL作业，单击“创建作业”，进入“作业编辑器“页面。
2.  在当前SQL作业编辑窗口右上方的“队列”列表中选择所使用的队列，默认选择“default“。创建队列操作步骤请参见[创建队列](创建队列.md)。
3.  在“数据库”列表中选择所使用的数据库和表，例如选择数据库“qw“和表“qw“。创建数据库和表操作步骤请参见[创建数据库和表](创建数据库和表.md)。
4.  在SQL作业编辑窗口输入SQL查询语句：

    ```
    SELECT * FROM qw.qw
    ```

    或者双击左侧表名“qw”，上述查询语句会自动在作业编辑窗口输入。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >当作业编辑窗口没有输入SQL语句时，“执行”和“格式化”两个按钮不可用。  

5.  单击“更多”中的“语法校验“，确认SQL语句书写是否正确。
    1.  若语法校验失败，请参考[《数据湖探索SQL语法参考》](https://support.huaweicloud.com/sqlreference-dli/dli_08_0002.html)，检查SQL语句准确性。
    2.  若语法校验通过，单击“执行”，阅读并同意隐私协议，单击“确定”后执行SQL语句。
    3.  SQL语句执行成功后，在SQL作业编辑窗口下方会显示执行结果。

6.  （可选）在执行结果窗口，单击右上![](figures/icon-柱状图.png)，上述查询结果将以图形形式呈现。再单击![](figures/icon-表格.png)，查询结果可切换回表格形式。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >-   若执行结果中无数值列，则无法进行图形化。  
    >-   图形类型包括柱状图、折线图、扇形图。  
    >-   柱状图和折线图的X轴可为任意一列，Y轴仅支持数值类型的列，扇形图对应图例和指标。  


## 作业编辑窗口操作技巧<a name="zh-cn_topic_0093946815_section6563159171817"></a>

-   在SQL作业编辑窗口中导入SQL语句的简便方法
    -   可以双击左侧导航栏列表中的表名，即可将选定表的查询语句导入SQL语句编辑窗口中，单击“执行”，即可完成查询。
    -   可以将表名、列名直接拖拽入作业编辑窗口中，编写SQL语句。
    -   可以通过单击“更多”，选择“设为模板”，将对应的SQL语句保存为模板，供将来执行使用。

        需要使用时，通过单击“更多”，选择“选择模板”，在已有模板中双击所需的SQL语句，导入SQL作业编辑窗口中，单击“执行”，或根据需要进行修改后执行。

    -   可以批量执行SQL语句。

-   作业编辑窗口的特点

    作业编辑窗口具有以下三个特点。

    -   颜色突出显示 - 常用语法采用不同颜色突出显示。
    -   注释支持 - 支持单行注释和多行注释。以“--”开头，后续内容即为注释。
    -   光标位置显示 - 可以用于确认位于作业编辑窗口内的鼠标光标的列号和行号。


