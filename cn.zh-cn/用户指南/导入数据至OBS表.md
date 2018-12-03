# 导入数据至OBS表<a name="dli_01_0376"></a>

## 操作场景<a name="section10579446195716"></a>

-   支持将OBS上的数据导入到DLI中创建的OBS表中。
-   导入数据的OBS表可为分区表，也可为非分区表。
-   创建OBS表时指定的路径必须是文件夹，若建表路径是文件将导致导入数据失败。
-   若将csv格式数据导入分区表，需在数据源中将分区列放在最后一列。
-   导入数据时只能指定一个路径，路径中不能包含逗号。
-   当OBS的目录下有同名文件夹和文件时，数据导入指向该路径会优先指向文件而非文件夹。
-   不支持并发提交同一张表的导入任务。
-   导入文件支持CSV，Parquet，ORC和JSON四种格式，且文本格式仅支持UTF-8。

## 前提条件<a name="section46923850144935"></a>

待导入的数据已存储到OBS上。

## 操作步骤<a name="section3156178164610"></a>

1.  在DLI管理控制台顶部菜单栏中，选择“数据管理“。
2.  单击需导入数据的OBS表对应的数据库，展开该数据库下的表。
3.  选中目标OBS表，在“详情“页面，单击“导入“，弹出“导入数据“对话框。

    **图 1**  导入数据至OBS<a name="fig6547469614368"></a>  
    ![](figures/导入数据至OBS.png "导入数据至OBS")

4.  参见[表1](#table49355631144515)填写导入数据相关信息。

    **表 1**  参数说明

    <a name="table49355631144515"></a>
    <table><thead align="left"><tr id="row54525213144515"><th class="cellrowborder" valign="top" width="13%" id="mcps1.2.4.1.1"><p id="p42357757144515"><a name="p42357757144515"></a><a name="p42357757144515"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="71%" id="mcps1.2.4.1.2"><p id="p8426325144515"><a name="p8426325144515"></a><a name="p8426325144515"></a>描述</p>
    </th>
    <th class="cellrowborder" valign="top" width="16%" id="mcps1.2.4.1.3"><p id="p11443709144515"><a name="p11443709144515"></a><a name="p11443709144515"></a>示例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row26115376112250"><td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.4.1.1 "><p id="p77092811237"><a name="p77092811237"></a><a name="p77092811237"></a>数据库名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="71%" headers="mcps1.2.4.1.2 "><p id="p6244524411237"><a name="p6244524411237"></a><a name="p6244524411237"></a>当前表所在的数据库。</p>
    </td>
    <td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.4.1.3 "><p id="p2489997111237"><a name="p2489997111237"></a><a name="p2489997111237"></a>-</p>
    </td>
    </tr>
    <tr id="row14920175112255"><td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.4.1.1 "><p id="p3268612711237"><a name="p3268612711237"></a><a name="p3268612711237"></a>表名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="71%" headers="mcps1.2.4.1.2 "><p id="p3033060511237"><a name="p3033060511237"></a><a name="p3033060511237"></a>当前表名称。</p>
    </td>
    <td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.4.1.3 "><p id="p4085990711237"><a name="p4085990711237"></a><a name="p4085990711237"></a>-</p>
    </td>
    </tr>
    <tr id="row21841419112331"><td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.4.1.1 "><p id="p6532867112340"><a name="p6532867112340"></a><a name="p6532867112340"></a>文件格式</p>
    </td>
    <td class="cellrowborder" valign="top" width="71%" headers="mcps1.2.4.1.2 "><p id="p59400238112340"><a name="p59400238112340"></a><a name="p59400238112340"></a>导入数据源的文件格式。导入支持CSV，Parquet，ORC和JSON四种格式。</p>
    </td>
    <td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.4.1.3 "><p id="p46689986112340"><a name="p46689986112340"></a><a name="p46689986112340"></a>Parquet</p>
    </td>
    </tr>
    <tr id="row249814981126"><td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.4.1.1 "><p id="p102354871126"><a name="p102354871126"></a><a name="p102354871126"></a>队列</p>
    </td>
    <td class="cellrowborder" valign="top" width="71%" headers="mcps1.2.4.1.2 "><p id="p237681411126"><a name="p237681411126"></a><a name="p237681411126"></a>选择队列。</p>
    </td>
    <td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.4.1.3 "><p id="p461712431126"><a name="p461712431126"></a><a name="p461712431126"></a>-</p>
    </td>
    </tr>
    <tr id="row6511315111245"><td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.4.1.1 "><p id="p1090727411249"><a name="p1090727411249"></a><a name="p1090727411249"></a>数据源路径</p>
    </td>
    <td class="cellrowborder" valign="top" width="71%" headers="mcps1.2.4.1.2 "><p id="p1107399111249"><a name="p1107399111249"></a><a name="p1107399111249"></a>直接输入路径或单击<a name="image32022923112640"></a><a name="image32022923112640"></a><span><img id="image32022923112640" src="figures/zh-cn_image_0123511535.png" width="17.958900289535457" height="15.393344056606322"></span>选择OBS的路径，若没有合适的桶可直接跳转OBS创建。路径须以<span class="parmname" id="parmname2457806011249"><a name="parmname2457806011249"></a><a name="parmname2457806011249"></a><b>s3a://</b></span>开头。</p>
    </td>
    <td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.4.1.3 "><p id="p4466585811249"><a name="p4466585811249"></a><a name="p4466585811249"></a>s3a://DLI/sampledata.csv</p>
    </td>
    </tr>
    <tr id="row54051486144515"><td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.4.1.1 "><p id="p44720296144515"><a name="p44720296144515"></a><a name="p44720296144515"></a>表头</p>
    </td>
    <td class="cellrowborder" valign="top" width="71%" headers="mcps1.2.4.1.2 "><p id="p1262888185911"><a name="p1262888185911"></a><a name="p1262888185911"></a>当<span class="parmname" id="parmname3628138105919"><a name="parmname3628138105919"></a><a name="parmname3628138105919"></a><b>数据格式</b></span>为<span class="parmvalue" id="parmvalue146286818592"><a name="parmvalue146286818592"></a><a name="parmvalue146286818592"></a><b>CSV</b></span>时该参数有效。</p>
    <p id="p37255200172441"><a name="p37255200172441"></a><a name="p37255200172441"></a>设置导入数据源是否含表头。选中<span class="parmvalue" id="parmvalue51149381152733"><a name="parmvalue51149381152733"></a><a name="parmvalue51149381152733"></a><b>高级选项</b></span>，勾选表头前的方框表示有表头，去勾选表示无表头。</p>
    </td>
    <td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.4.1.3 "><p id="p64462148144515"><a name="p64462148144515"></a><a name="p64462148144515"></a>-</p>
    </td>
    </tr>
    <tr id="row10344328144515"><td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.4.1.1 "><p id="p16701332144515"><a name="p16701332144515"></a><a name="p16701332144515"></a>自定义分隔符</p>
    </td>
    <td class="cellrowborder" valign="top" width="71%" headers="mcps1.2.4.1.2 "><p id="p3770121155918"><a name="p3770121155918"></a><a name="p3770121155918"></a>当<span class="parmname" id="parmname15770721175920"><a name="parmname15770721175920"></a><a name="parmname15770721175920"></a><b>数据格式</b></span>为<span class="parmvalue" id="parmvalue577062118594"><a name="parmvalue577062118594"></a><a name="parmvalue577062118594"></a><b>CSV</b></span>，勾选自定义分隔符前的方框时，该参数有效。</p>
    <p id="p28567101144515"><a name="p28567101144515"></a><a name="p28567101144515"></a>支持选择如下分隔符。</p>
    <a name="ul2131564615213"></a><a name="ul2131564615213"></a><ul id="ul2131564615213"><li>逗号(,)</li><li>竖线(|)</li><li>制表符(\t)</li><li>控制符(\001)</li><li>其他：输入自定义分隔符</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.4.1.3 "><p id="p38640381152118"><a name="p38640381152118"></a><a name="p38640381152118"></a>默认值：逗号(,)</p>
    </td>
    </tr>
    <tr id="row52424162144515"><td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.4.1.1 "><p id="p25990090144515"><a name="p25990090144515"></a><a name="p25990090144515"></a>自定义引用字符</p>
    </td>
    <td class="cellrowborder" valign="top" width="71%" headers="mcps1.2.4.1.2 "><p id="p0100431175920"><a name="p0100431175920"></a><a name="p0100431175920"></a>当<span class="parmname" id="parmname151000311591"><a name="parmname151000311591"></a><a name="parmname151000311591"></a><b>数据格式</b></span>为<span class="parmvalue" id="parmvalue19100103119595"><a name="parmvalue19100103119595"></a><a name="parmvalue19100103119595"></a><b>CSV</b></span>，勾选自定义引用字符前的方框时，该参数有效。</p>
    <p id="p23945735154540"><a name="p23945735154540"></a><a name="p23945735154540"></a>支持选择如下引用字符。</p>
    <a name="ul33790457152252"></a><a name="ul33790457152252"></a><ul id="ul33790457152252"><li>单引号(')</li><li>双引号(")</li><li>其他：输入自定义引用字符</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.4.1.3 "><p id="p5707000515235"><a name="p5707000515235"></a><a name="p5707000515235"></a>默认值：单引号(')</p>
    </td>
    </tr>
    <tr id="row63070367144515"><td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.4.1.1 "><p id="p2055418144515"><a name="p2055418144515"></a><a name="p2055418144515"></a>自定义转义字符</p>
    </td>
    <td class="cellrowborder" valign="top" width="71%" headers="mcps1.2.4.1.2 "><p id="p19444153865912"><a name="p19444153865912"></a><a name="p19444153865912"></a>当<span class="parmname" id="parmname124444389593"><a name="parmname124444389593"></a><a name="parmname124444389593"></a><b>数据格式</b></span>为<span class="parmvalue" id="parmvalue9444113875919"><a name="parmvalue9444113875919"></a><a name="parmvalue9444113875919"></a><b>CSV</b></span>，并在自定义转义字符前的方框打勾时，该参数有效。</p>
    <p id="p10664332154555"><a name="p10664332154555"></a><a name="p10664332154555"></a>选中高级选项，支持选择如下转义字符。</p>
    <a name="ul806711515245"></a><a name="ul806711515245"></a><ul id="ul806711515245"><li>反斜杠(\)</li><li>其他：输入自定义转义字符</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.4.1.3 "><p id="p19593506152412"><a name="p19593506152412"></a><a name="p19593506152412"></a>默认值：反斜杠(\)</p>
    </td>
    </tr>
    <tr id="row27500407144515"><td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.4.1.1 "><p id="p30762396144515"><a name="p30762396144515"></a><a name="p30762396144515"></a>日期格式</p>
    </td>
    <td class="cellrowborder" valign="top" width="71%" headers="mcps1.2.4.1.2 "><p id="p1784915111018"><a name="p1784915111018"></a><a name="p1784915111018"></a>当<span class="parmname" id="parmname1219616248016"><a name="parmname1219616248016"></a><a name="parmname1219616248016"></a><b>数据格式</b></span>为<span class="parmvalue" id="parmvalue1284217371206"><a name="parmvalue1284217371206"></a><a name="parmvalue1284217371206"></a><b>CSV</b></span>和<span class="parmvalue" id="parmvalue115595441809"><a name="parmvalue115595441809"></a><a name="parmvalue115595441809"></a><b>JSON</b></span>时此参数有效。</p>
    <p id="p11426781144515"><a name="p11426781144515"></a><a name="p11426781144515"></a>选中<span class="parmvalue" id="parmvalue8726182144515"><a name="parmvalue8726182144515"></a><a name="parmvalue8726182144515"></a><b>高级选项</b></span>，该参数表示表中日期的格式，默认格式为<span class="parmname" id="parmname39411477155041"><a name="parmname39411477155041"></a><a name="parmname39411477155041"></a><b>yyyy-MM-dd</b></span>。日期格式字符定义详见<a href="https://support.huaweicloud.com/sqlreference-uquery/uquery_08_0100.html" target="_blank" rel="noopener noreferrer">加载数据</a>中的“表3 日期及时间模式字符定义”。</p>
    </td>
    <td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.4.1.3 "><p id="p8624556144515"><a name="p8624556144515"></a><a name="p8624556144515"></a>2000-01-01</p>
    </td>
    </tr>
    <tr id="row639781049130"><td class="cellrowborder" valign="top" width="13%" headers="mcps1.2.4.1.1 "><p id="p389320299130"><a name="p389320299130"></a><a name="p389320299130"></a>时间戳格式</p>
    </td>
    <td class="cellrowborder" valign="top" width="71%" headers="mcps1.2.4.1.2 "><p id="p34074178118"><a name="p34074178118"></a><a name="p34074178118"></a>当<span class="parmname" id="parmname1374022216119"><a name="parmname1374022216119"></a><a name="parmname1374022216119"></a><b>数据格式</b></span>为<span class="parmvalue" id="parmvalue274042211115"><a name="parmvalue274042211115"></a><a name="parmvalue274042211115"></a><b>CSV</b></span>和<span class="parmvalue" id="parmvalue1574110221215"><a name="parmvalue1574110221215"></a><a name="parmvalue1574110221215"></a><b>JSON</b></span>时此参数有效。</p>
    <p id="p28390848155126"><a name="p28390848155126"></a><a name="p28390848155126"></a>选中<span class="parmvalue" id="parmvalue42192596155126"><a name="parmvalue42192596155126"></a><a name="parmvalue42192596155126"></a><b>高级选项</b></span>，该参数表示表中时间戳的格式，默认格式为<span class="parmname" id="parmname22543377155126"><a name="parmname22543377155126"></a><a name="parmname22543377155126"></a><b>yyyy-MM-dd HH:mm:ss</b></span>。时间戳格式字符定义详见<a href="https://support.huaweicloud.com/sqlreference-uquery/uquery_08_0100.html" target="_blank" rel="noopener noreferrer">加载数据</a>中的“表3 日期及时间模式字符定义”。</p>
    </td>
    <td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.4.1.3 "><p id="p167064109130"><a name="p167064109130"></a><a name="p167064109130"></a>2000-01-01 09:00:00</p>
    </td>
    </tr>
    </tbody>
    </table>

5.  单击“确定“，系统开始导入数据。
6.  （可选）可以在“作业管理“页面，查看该导入作业的状态以及执行结果。
7.  在“预览“页面，可查看导入的内容。

