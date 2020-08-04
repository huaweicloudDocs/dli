# 创建Spark作业<a name="dli_01_0384"></a>

Spark作业编辑页面支持执行Spark作业，为用户提供全托管式的Spark计算服务。

在总览页面，单击Spark作业右上角的“创建作业”，或在Spark作业管理页面，单击右上角的“创建作业”，均可进入Spark作业编辑页面。

进入Spark作业编辑页面，页面会提示系统将创建DLI临时数据桶。该桶用于存储使用DLI服务产生的临时数据，例如：作业日志、作业结果等。如果不创建该桶，将无法查看作业日志。可以通过[配置生命周期规则](https://support.huaweicloud.com/usermanual-obs/obs_03_0335.html)，实现定时删除OBS桶中的对象或者定时转换对象的存储类别。桶名称为系统默认。

## 界面说明<a name="zh-cn_topic_0115200017_zh-cn_topic_0093946815_section56922894165137"></a>

-   左侧导航栏

    在创建Spark作业页面，左侧导航栏包括“队列“页签和“程序包“页签。

    **图 1**  Spark作业编辑页面导航栏<a name="zh-cn_topic_0115200017_fig452563612140"></a>  
    ![](figures/Spark作业编辑页面导航栏.png "Spark作业编辑页面导航栏")

    **表 1**  左侧导航栏说明

    <a name="zh-cn_topic_0115200017_table1357419814715"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0115200017_row105761087712"><th class="cellrowborder" valign="top" width="7.329267073292671%" id="mcps1.2.5.1.1"><p id="p2046364916199"><a name="p2046364916199"></a><a name="p2046364916199"></a>序号</p>
    </th>
    <th class="cellrowborder" valign="top" width="13.638636136386362%" id="mcps1.2.5.1.2"><p id="p1177132235719"><a name="p1177132235719"></a><a name="p1177132235719"></a>页签/按键</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.518048195180484%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0115200017_p6536192015152"><a name="zh-cn_topic_0115200017_p6536192015152"></a><a name="zh-cn_topic_0115200017_p6536192015152"></a>页签/按键名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="59.51404859514048%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0115200017_p5539122041514"><a name="zh-cn_topic_0115200017_p5539122041514"></a><a name="zh-cn_topic_0115200017_p5539122041514"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0115200017_row0576181717"><td class="cellrowborder" valign="top" width="7.329267073292671%" headers="mcps1.2.5.1.1 "><p id="p1846414494193"><a name="p1846414494193"></a><a name="p1846414494193"></a>1</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.638636136386362%" headers="mcps1.2.5.1.2 "><p id="p2772152211579"><a name="p2772152211579"></a><a name="p2772152211579"></a><a name="image91413515593"></a><a name="image91413515593"></a><span><img id="image91413515593" src="figures/zh-cn_image_0264374451.png"></span></p>
    </td>
    <td class="cellrowborder" valign="top" width="19.518048195180484%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0115200017_p2576081473"><a name="zh-cn_topic_0115200017_p2576081473"></a><a name="zh-cn_topic_0115200017_p2576081473"></a>队列</p>
    </td>
    <td class="cellrowborder" valign="top" width="59.51404859514048%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0115200017_p17576681978"><a name="zh-cn_topic_0115200017_p17576681978"></a><a name="zh-cn_topic_0115200017_p17576681978"></a>显示已有的队列。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0115200017_row1157678977"><td class="cellrowborder" valign="top" width="7.329267073292671%" headers="mcps1.2.5.1.1 "><p id="p7464049201918"><a name="p7464049201918"></a><a name="p7464049201918"></a>2</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.638636136386362%" headers="mcps1.2.5.1.2 "><p id="p57725223578"><a name="p57725223578"></a><a name="p57725223578"></a><a name="image7542172920595"></a><a name="image7542172920595"></a><span><img id="image7542172920595" src="figures/zh-cn_image_0264374479.png"></span></p>
    </td>
    <td class="cellrowborder" valign="top" width="19.518048195180484%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0115200017_p0576138971"><a name="zh-cn_topic_0115200017_p0576138971"></a><a name="zh-cn_topic_0115200017_p0576138971"></a>程序包</p>
    </td>
    <td class="cellrowborder" valign="top" width="59.51404859514048%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0115200017_p135761987719"><a name="zh-cn_topic_0115200017_p135761987719"></a><a name="zh-cn_topic_0115200017_p135761987719"></a>显示已有的程序包。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0115200017_row95761281676"><td class="cellrowborder" valign="top" width="7.329267073292671%" headers="mcps1.2.5.1.1 "><p id="p94641349181918"><a name="p94641349181918"></a><a name="p94641349181918"></a>3</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.638636136386362%" headers="mcps1.2.5.1.2 "><p id="p157726220576"><a name="p157726220576"></a><a name="p157726220576"></a><a name="image11701591599"></a><a name="image11701591599"></a><span><img id="image11701591599" src="figures/zh-cn_image_0264374589.png"></span></p>
    </td>
    <td class="cellrowborder" valign="top" width="19.518048195180484%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0115200017_p17576168971"><a name="zh-cn_topic_0115200017_p17576168971"></a><a name="zh-cn_topic_0115200017_p17576168971"></a>创建</p>
    </td>
    <td class="cellrowborder" valign="top" width="59.51404859514048%" headers="mcps1.2.5.1.4 "><p id="p1175412222117"><a name="p1175412222117"></a><a name="p1175412222117"></a>创建队列/程序包。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0115200017_row1857619810717"><td class="cellrowborder" valign="top" width="7.329267073292671%" headers="mcps1.2.5.1.1 "><p id="p046416495193"><a name="p046416495193"></a><a name="p046416495193"></a>4</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.638636136386362%" headers="mcps1.2.5.1.2 "><p id="p13772122155718"><a name="p13772122155718"></a><a name="p13772122155718"></a><a name="image59893191002"></a><a name="image59893191002"></a><span><img id="image59893191002" src="figures/zh-cn_image_0264374665.png"></span></p>
    </td>
    <td class="cellrowborder" valign="top" width="19.518048195180484%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0115200017_p18576198871"><a name="zh-cn_topic_0115200017_p18576198871"></a><a name="zh-cn_topic_0115200017_p18576198871"></a>刷新</p>
    </td>
    <td class="cellrowborder" valign="top" width="59.51404859514048%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0115200017_p657617815713"><a name="zh-cn_topic_0115200017_p657617815713"></a><a name="zh-cn_topic_0115200017_p657617815713"></a>包括刷新已有的队列和程序包列表。</p>
    </td>
    </tr>
    <tr id="row181911018124413"><td class="cellrowborder" valign="top" width="7.329267073292671%" headers="mcps1.2.5.1.1 "><p id="p1192151811440"><a name="p1192151811440"></a><a name="p1192151811440"></a>5</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.638636136386362%" headers="mcps1.2.5.1.2 "><p id="p207721122145717"><a name="p207721122145717"></a><a name="p207721122145717"></a><a name="image105704451306"></a><a name="image105704451306"></a><span><img id="image105704451306" src="figures/zh-cn_image_0264374835.png"></span></p>
    </td>
    <td class="cellrowborder" valign="top" width="19.518048195180484%" headers="mcps1.2.5.1.3 "><p id="p1219211184449"><a name="p1219211184449"></a><a name="p1219211184449"></a>搜索</p>
    </td>
    <td class="cellrowborder" valign="top" width="59.51404859514048%" headers="mcps1.2.5.1.4 "><p id="p151926184441"><a name="p151926184441"></a><a name="p151926184441"></a>在程序包页签，可以输入程序包名称进行搜索。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   作业编辑窗口

    在作业编辑窗口，可以选择使用“表单模式“或者“API模式“进行参数设置。

    以下以“表单模式“页面进行说明，“API模式“即采用API接口模式设置参数及参数值，具体请参考《[数据湖探索API参考](https://support.huaweicloud.com/api-dli/dli_02_0124.html)》。

    -   选择运行队列：具体参数请参考[表2](#zh-cn_topic_0115200017_table18913103220552)。

        **图 2**  创建Spark作业-选择运行队列<a name="fig497172012450"></a>  
        ![](figures/创建Spark作业-选择运行队列.png "创建Spark作业-选择运行队列")

        **表 2**  运行队列参数说明

        <a name="zh-cn_topic_0115200017_table18913103220552"></a>
        <table><thead align="left"><tr id="zh-cn_topic_0115200017_row169141932105516"><th class="cellrowborder" valign="top" width="17.34%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0115200017_p660634117106"><a name="zh-cn_topic_0115200017_p660634117106"></a><a name="zh-cn_topic_0115200017_p660634117106"></a>参数名称</p>
        </th>
        <th class="cellrowborder" valign="top" width="82.66%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0115200017_p1161019414106"><a name="zh-cn_topic_0115200017_p1161019414106"></a><a name="zh-cn_topic_0115200017_p1161019414106"></a>参数描述</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="zh-cn_topic_0115200017_row102037812149"><td class="cellrowborder" valign="top" width="17.34%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0115200017_p1920319815141"><a name="zh-cn_topic_0115200017_p1920319815141"></a><a name="zh-cn_topic_0115200017_p1920319815141"></a>所属队列</p>
        </td>
        <td class="cellrowborder" valign="top" width="82.66%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0115200017_p1420316811418"><a name="zh-cn_topic_0115200017_p1420316811418"></a><a name="zh-cn_topic_0115200017_p1420316811418"></a>下拉选择要使用的队列。</p>
        </td>
        </tr>
        </tbody>
        </table>

    -   作业配置：具体参数请参考[表3](#table161519411416)。

        **图 3**  创建Spark作业-作业配置<a name="zh-cn_topic_0115200017_fig12259471592"></a>  
        ![](figures/创建Spark作业-作业配置.png "创建Spark作业-作业配置")

        **表 3**  作业配置参数说明

        <a name="table161519411416"></a>
        <table><thead align="left"><tr id="row186160413410"><th class="cellrowborder" valign="top" width="17.34%" id="mcps1.2.3.1.1"><p id="p6616194114116"><a name="p6616194114116"></a><a name="p6616194114116"></a>参数名称</p>
        </th>
        <th class="cellrowborder" valign="top" width="82.66%" id="mcps1.2.3.1.2"><p id="p86163413416"><a name="p86163413416"></a><a name="p86163413416"></a>参数描述</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row19617649416"><td class="cellrowborder" valign="top" width="17.34%" headers="mcps1.2.3.1.1 "><p id="p1961711416418"><a name="p1961711416418"></a><a name="p1961711416418"></a>作业名称</p>
        </td>
        <td class="cellrowborder" valign="top" width="82.66%" headers="mcps1.2.3.1.2 "><p id="p13617154174113"><a name="p13617154174113"></a><a name="p13617154174113"></a>设置作业名称。</p>
        </td>
        </tr>
        <tr id="row1461712412419"><td class="cellrowborder" valign="top" width="17.34%" headers="mcps1.2.3.1.1 "><p id="p11617184194112"><a name="p11617184194112"></a><a name="p11617184194112"></a>应用程序</p>
        </td>
        <td class="cellrowborder" valign="top" width="82.66%" headers="mcps1.2.3.1.2 "><p id="p1961874124118"><a name="p1961874124118"></a><a name="p1961874124118"></a>选择需要执行的程序包。包括“.jar”和“.py”两种类型。</p>
        </td>
        </tr>
        <tr id="row561813464110"><td class="cellrowborder" valign="top" width="17.34%" headers="mcps1.2.3.1.1 "><p id="p461812424116"><a name="p461812424116"></a><a name="p461812424116"></a>主类</p>
        </td>
        <td class="cellrowborder" valign="top" width="82.66%" headers="mcps1.2.3.1.2 "><p id="p16687114615526"><a name="p16687114615526"></a><a name="p16687114615526"></a>输入主类名称。当应用程序类型为“.jar”时，主类名称不能为空。</p>
        </td>
        </tr>
        <tr id="row136181414419"><td class="cellrowborder" valign="top" width="17.34%" headers="mcps1.2.3.1.1 "><p id="p136191549415"><a name="p136191549415"></a><a name="p136191549415"></a>应用程序参数</p>
        </td>
        <td class="cellrowborder" valign="top" width="82.66%" headers="mcps1.2.3.1.2 "><p id="p126191141419"><a name="p126191141419"></a><a name="p126191141419"></a>用户自定义参数，多个参数以逗号分隔。</p>
        </td>
        </tr>
        <tr id="row20647136165314"><td class="cellrowborder" valign="top" width="17.34%" headers="mcps1.2.3.1.1 "><p id="p196495619531"><a name="p196495619531"></a><a name="p196495619531"></a>Spark参数</p>
        </td>
        <td class="cellrowborder" valign="top" width="82.66%" headers="mcps1.2.3.1.2 "><p id="p464986135314"><a name="p464986135314"></a><a name="p464986135314"></a>以“key/value”的形式设置提交Spark作业的属性，多个参数以Enter键分隔。具体参数请参考<a href="https://spark.apache.org/docs/latest/configuration.html" target="_blank" rel="noopener noreferrer">Spark Configuration</a>。</p>
        </td>
        </tr>
        <tr id="row196014274377"><td class="cellrowborder" valign="top" width="17.34%" headers="mcps1.2.3.1.1 "><p id="p1458634211326"><a name="p1458634211326"></a><a name="p1458634211326"></a>依赖jar包</p>
        </td>
        <td class="cellrowborder" valign="top" width="82.66%" headers="mcps1.2.3.1.2 "><p id="p175851042153219"><a name="p175851042153219"></a><a name="p175851042153219"></a>运行spark作业依赖的jars。</p>
        </td>
        </tr>
        <tr id="row12662161114381"><td class="cellrowborder" valign="top" width="17.34%" headers="mcps1.2.3.1.1 "><p id="p166620111381"><a name="p166620111381"></a><a name="p166620111381"></a>依赖Python文件</p>
        </td>
        <td class="cellrowborder" valign="top" width="82.66%" headers="mcps1.2.3.1.2 "><p id="p66621911103817"><a name="p66621911103817"></a><a name="p66621911103817"></a>运行spark作业依赖的py-files。</p>
        </td>
        </tr>
        <tr id="row15191336193816"><td class="cellrowborder" valign="top" width="17.34%" headers="mcps1.2.3.1.1 "><p id="p16520103618382"><a name="p16520103618382"></a><a name="p16520103618382"></a>其他依赖文件</p>
        </td>
        <td class="cellrowborder" valign="top" width="82.66%" headers="mcps1.2.3.1.2 "><p id="p10520143643819"><a name="p10520143643819"></a><a name="p10520143643819"></a>运行spark作业依赖的其他files。</p>
        </td>
        </tr>
        <tr id="row11895591189"><td class="cellrowborder" valign="top" width="17.34%" headers="mcps1.2.3.1.1 "><p id="p41904593813"><a name="p41904593813"></a><a name="p41904593813"></a>依赖分组</p>
        </td>
        <td class="cellrowborder" valign="top" width="82.66%" headers="mcps1.2.3.1.2 "><p id="p121901659982"><a name="p121901659982"></a><a name="p121901659982"></a>在创建程序包时，如果选择了分组，在此处选择对应的分组，则可以同时选中该分组中的所有程序包和文件。创建程序包操作请参考<a href="创建程序包.md">创建程序包</a>。</p>
        </td>
        </tr>
        <tr id="row1989081215461"><td class="cellrowborder" valign="top" width="17.34%" headers="mcps1.2.3.1.1 "><p id="p1689213127465"><a name="p1689213127465"></a><a name="p1689213127465"></a>作业失败重试</p>
        </td>
        <td class="cellrowborder" valign="top" width="82.66%" headers="mcps1.2.3.1.2 "><p id="p19892111204612"><a name="p19892111204612"></a><a name="p19892111204612"></a>作业失败后是否进行重试。</p>
        <p id="p9810115810589"><a name="p9810115810589"></a><a name="p9810115810589"></a>选择“是”需要配置以下参数：</p>
        <p id="p15293152413592"><a name="p15293152413592"></a><a name="p15293152413592"></a><span class="parmname" id="parmname14976809017"><a name="parmname14976809017"></a><a name="parmname14976809017"></a>“最大重试次数”</span>：设置作业失败重试次数，最大值为“100”。</p>
        </td>
        </tr>
        <tr id="row5835182513420"><td class="cellrowborder" valign="top" width="17.34%" headers="mcps1.2.3.1.1 "><p id="p883517255416"><a name="p883517255416"></a><a name="p883517255416"></a>高级配置</p>
        </td>
        <td class="cellrowborder" valign="top" width="82.66%" headers="mcps1.2.3.1.2 "><a name="ul33251307256"></a><a name="ul33251307256"></a><ul id="ul33251307256"><li>暂不配置</li><li>现在配置：包括以下两项参数<a name="ul13639162018275"></a><a name="ul13639162018275"></a><ul id="ul13639162018275"><li>选择依赖资源：具体参数请参考<a href="#table1386622213325">表4</a>。</li><li>计算资源规格：具体参数请参考<a href="#table1680231613596">表5</a>。</li></ul>
        </li></ul>
        </td>
        </tr>
        </tbody>
        </table>

        **图 4**  创建Spark作业-高级配置<a name="fig1677120501207"></a>  
        ![](figures/创建Spark作业-高级配置.png "创建Spark作业-高级配置")

        **表 4**  选择依赖资源参数说明

        <a name="table1386622213325"></a>
        <table><thead align="left"><tr id="row686782223211"><th class="cellrowborder" valign="top" width="17.34%" id="mcps1.2.3.1.1"><p id="p88673225321"><a name="p88673225321"></a><a name="p88673225321"></a>参数名称</p>
        </th>
        <th class="cellrowborder" valign="top" width="82.66%" id="mcps1.2.3.1.2"><p id="p186710224326"><a name="p186710224326"></a><a name="p186710224326"></a>参数描述</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row93181334192819"><td class="cellrowborder" valign="top" width="17.34%" headers="mcps1.2.3.1.1 "><p id="p731993492819"><a name="p731993492819"></a><a name="p731993492819"></a>Module名称</p>
        </td>
        <td class="cellrowborder" valign="top" width="82.66%" headers="mcps1.2.3.1.2 "><div class="p" id="p231983472818"><a name="p231983472818"></a><a name="p231983472818"></a>DLI系统提供的用于执行跨源作业的依赖模块，访问各个不同的服务，选择不同的模块：<a name="ul863182613314"></a><a name="ul863182613314"></a><ul id="ul863182613314"><li>CloudTable/MRS HBase: sys.datasource.hbase</li><li>CloudTable/MRS OpenTSDB: sys.datasource.opentsdb</li><li>RDS MySQL: sys.datasource.rds</li><li>RDS PostGre: sys.datasource.rds</li><li>DWS: sys.datasource.dws</li><li>CSS: sys.datasource.css</li></ul>
        </div>
        </td>
        </tr>
        <tr id="row1986852214329"><td class="cellrowborder" valign="top" width="17.34%" headers="mcps1.2.3.1.1 "><p id="p19589142173217"><a name="p19589142173217"></a><a name="p19589142173217"></a>资源包</p>
        </td>
        <td class="cellrowborder" valign="top" width="82.66%" headers="mcps1.2.3.1.2 "><p id="p1458714253220"><a name="p1458714253220"></a><a name="p1458714253220"></a>运行spark作业依赖的jar包。</p>
        </td>
        </tr>
        </tbody>
        </table>

        **表 5**  计算资源规格参数说明

        <a name="table1680231613596"></a>
        <table><thead align="left"><tr id="row178031916155915"><th class="cellrowborder" valign="top" width="24.779999999999998%" id="mcps1.2.3.1.1"><p id="p180318161599"><a name="p180318161599"></a><a name="p180318161599"></a>参数名称</p>
        </th>
        <th class="cellrowborder" valign="top" width="75.22%" id="mcps1.2.3.1.2"><p id="p4803121685913"><a name="p4803121685913"></a><a name="p4803121685913"></a>参数描述</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row178035164597"><td class="cellrowborder" valign="top" width="24.779999999999998%" headers="mcps1.2.3.1.1 "><p id="p1080317167594"><a name="p1080317167594"></a><a name="p1080317167594"></a>资源规格</p>
        </td>
        <td class="cellrowborder" valign="top" width="75.22%" headers="mcps1.2.3.1.2 "><p id="p15898137632"><a name="p15898137632"></a><a name="p15898137632"></a>下拉选择所需的资源规格。系统提供3种资源规格供您选择。资源规格中如下配置项支持修改：</p>
        <a name="ul48974013311"></a><a name="ul48974013311"></a><ul id="ul48974013311"><li>Executor内存</li><li>Executor CPU核数</li><li>Executor个数</li><li>driver CPU核数</li><li>driver内存</li></ul>
        <p id="p1846015514416"><a name="p1846015514416"></a><a name="p1846015514416"></a>最终配置结果以修改后数据为准。</p>
        </td>
        </tr>
        <tr id="row1480315166592"><td class="cellrowborder" valign="top" width="24.779999999999998%" headers="mcps1.2.3.1.1 "><p id="p9804141611596"><a name="p9804141611596"></a><a name="p9804141611596"></a>Executor内存</p>
        </td>
        <td class="cellrowborder" valign="top" width="75.22%" headers="mcps1.2.3.1.2 "><p id="p114821442750"><a name="p114821442750"></a><a name="p114821442750"></a>在所选资源规格基础上自定义Executor内存规格。</p>
        </td>
        </tr>
        <tr id="row1780481665912"><td class="cellrowborder" valign="top" width="24.779999999999998%" headers="mcps1.2.3.1.1 "><p id="p1780441685919"><a name="p1780441685919"></a><a name="p1780441685919"></a>Executor CPU核数</p>
        </td>
        <td class="cellrowborder" valign="top" width="75.22%" headers="mcps1.2.3.1.2 "><p id="p5480124210511"><a name="p5480124210511"></a><a name="p5480124210511"></a>在所选资源规格基础上自定义Executor CPU核数。</p>
        </td>
        </tr>
        <tr id="row1680411613593"><td class="cellrowborder" valign="top" width="24.779999999999998%" headers="mcps1.2.3.1.1 "><p id="p4804716205912"><a name="p4804716205912"></a><a name="p4804716205912"></a>Executor个数</p>
        </td>
        <td class="cellrowborder" valign="top" width="75.22%" headers="mcps1.2.3.1.2 "><p id="p114793421458"><a name="p114793421458"></a><a name="p114793421458"></a>在所选资源规格基础上自定义Executor个数。</p>
        </td>
        </tr>
        <tr id="row15805416115914"><td class="cellrowborder" valign="top" width="24.779999999999998%" headers="mcps1.2.3.1.1 "><p id="p1680511610597"><a name="p1680511610597"></a><a name="p1680511610597"></a>driver CPU核数</p>
        </td>
        <td class="cellrowborder" valign="top" width="75.22%" headers="mcps1.2.3.1.2 "><p id="p1947517421358"><a name="p1947517421358"></a><a name="p1947517421358"></a>在所选资源规格基础上自定义Driver CPU核数。</p>
        </td>
        </tr>
        <tr id="row1029553211514"><td class="cellrowborder" valign="top" width="24.779999999999998%" headers="mcps1.2.3.1.1 "><p id="p1529713323518"><a name="p1529713323518"></a><a name="p1529713323518"></a>driver内存</p>
        </td>
        <td class="cellrowborder" valign="top" width="75.22%" headers="mcps1.2.3.1.2 "><p id="p629793214514"><a name="p629793214514"></a><a name="p629793214514"></a>在所选资源规格基础上自定义Driver内存规格。</p>
        </td>
        </tr>
        </tbody>
        </table>



## 创建Spark作业步骤<a name="section21590507141153"></a>

1.  在Spark作业编辑页面中，输入相关参数，具体请参考关于[图3](#zh-cn_topic_0115200017_fig12259471592)的说明。
2.  单击Spark作业编辑页面右上方“执行”，提交作业，页面显示“批处理作业提交成功”。
3.  （可选）可在“Spark作业”管理页面查看提交作业的状态及日志。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >作业执行成功后，作业记录只保存6小时。


