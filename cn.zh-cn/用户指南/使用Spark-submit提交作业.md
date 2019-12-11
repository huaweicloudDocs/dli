# 使用Spark-submit提交作业<a name="dli_01_0423"></a>

## DLI Spark-submit简介<a name="section159401845155918"></a>

DLI Spark-submit是一个用于提交Spark作业到DLI服务端的命令行工具，该工具提供与开源Spark兼容的命令行。

## DLI 客户端工具下载<a name="section22631635783"></a>

您可以在DLI管理控制台下载DLI客户端工具。

1.  登录DLI管理控制台。
2.  单击总览页右侧“常用链接”中的“[SDK下载](https://uquery-sdk.obs-website.cn-north-1.myhuaweicloud.com/)”。
3.  在“DLI SDK DOWNLOAD”页面，单击“huaweicloud-dli-clientkit-<version\>”即可下载DLI客户端工具。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >DLI客户端空间命名为“huaweicloud-dli-clientkit-<version\>-bin.tar.gz”，支持在Linux环境中使用，且依赖JDK 1.8及以上版本。  


## 配置DLI Spark-submit<a name="section203255161411"></a>

使用DLI Beeline的机器安装JDK 1.8或以上版本并配置环境变量，推荐在Linux环境下使用Beeline工具。

1.  下载并解压工具包“huaweicloud-dli-clientkit-<version\>-bin.tar.gz”，其中version为版本号，以实际版本号为准。
2.  进入解压目录，里面有三个子目录bin、conf、lib，分别存放了Spark-submit相关的执行脚本、配置文件和依赖包。
3.  进入配置文件conf目录，修改“client.properties”中的配置项，（具体配置项参考[表1](#table571552873114)）。

    **表 1**  DLI 客户端工具配置参数

    <a name="table571552873114"></a>
    <table><thead align="left"><tr id="row10713182823115"><th class="cellrowborder" valign="top" width="12.839999999999998%" id="mcps1.2.5.1.1"><p id="p27119155155349"><a name="p27119155155349"></a><a name="p27119155155349"></a>属性项</p>
    </th>
    <th class="cellrowborder" valign="top" width="10.13%" id="mcps1.2.5.1.2"><p id="p49167942155349"><a name="p49167942155349"></a><a name="p49167942155349"></a>必须配置</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.46%" id="mcps1.2.5.1.3"><p id="p23180374155349"><a name="p23180374155349"></a><a name="p23180374155349"></a>默认值</p>
    </th>
    <th class="cellrowborder" valign="top" width="55.57%" id="mcps1.2.5.1.4"><p id="p65670986155349"><a name="p65670986155349"></a><a name="p65670986155349"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row765513114239"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.5.1.1 "><p id="p865661182312"><a name="p865661182312"></a><a name="p865661182312"></a>dliEndPont</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.13%" headers="mcps1.2.5.1.2 "><p id="p106578110234"><a name="p106578110234"></a><a name="p106578110234"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.46%" headers="mcps1.2.5.1.3 "><p id="p136572116239"><a name="p136572116239"></a><a name="p136572116239"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.57%" headers="mcps1.2.5.1.4 "><p id="p15657518233"><a name="p15657518233"></a><a name="p15657518233"></a>DLI服务的域名。在<a href="https://developer.huaweicloud.com/endpoint?DLI" target="_blank" rel="noopener noreferrer">地区和终端节点</a>获取DLI对应区域的域名。</p>
    <p id="p312510316239"><a name="p312510316239"></a><a name="p312510316239"></a>如果不配置，程序根据region参数来确定华为云对应区域的域名。</p>
    </td>
    </tr>
    <tr id="row27131428163110"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.5.1.1 "><p id="p371342817318"><a name="p371342817318"></a><a name="p371342817318"></a>obsEndPoint</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.13%" headers="mcps1.2.5.1.2 "><p id="p971342818315"><a name="p971342818315"></a><a name="p971342818315"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.46%" headers="mcps1.2.5.1.3 "><p id="p571322863114"><a name="p571322863114"></a><a name="p571322863114"></a>obs.myhuaweicloud.com</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.57%" headers="mcps1.2.5.1.4 "><p id="p47131028203117"><a name="p47131028203117"></a><a name="p47131028203117"></a>OBS服务的域名。在<a href="https://developer.huaweicloud.com/endpoint?DLI" target="_blank" rel="noopener noreferrer">地区和终端节点</a>获取OBS对应区域的域名。</p>
    </td>
    </tr>
    <tr id="row1771562811317"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.5.1.1 "><p id="p1071316281314"><a name="p1071316281314"></a><a name="p1071316281314"></a>bucketName</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.13%" headers="mcps1.2.5.1.2 "><p id="p107151228113118"><a name="p107151228113118"></a><a name="p107151228113118"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.46%" headers="mcps1.2.5.1.3 "><p id="p127151228103110"><a name="p127151228103110"></a><a name="p127151228103110"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.57%" headers="mcps1.2.5.1.4 "><p id="p3715152803112"><a name="p3715152803112"></a><a name="p3715152803112"></a>OBS上的桶名称。该桶用于存放Spark程序中使用的jar包、Python程序文件、配置文件等。</p>
    </td>
    </tr>
    <tr id="row5715128163118"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.5.1.1 "><p id="p5715132883110"><a name="p5715132883110"></a><a name="p5715132883110"></a>obsPath</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.13%" headers="mcps1.2.5.1.2 "><p id="p13715102811312"><a name="p13715102811312"></a><a name="p13715102811312"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.46%" headers="mcps1.2.5.1.3 "><p id="p67151281317"><a name="p67151281317"></a><a name="p67151281317"></a>dli-spark-submit-resources</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.57%" headers="mcps1.2.5.1.4 "><p id="p1771572819316"><a name="p1771572819316"></a><a name="p1771572819316"></a>OBS上存放jar包、Python程序文件、配置文件等的目录，改目录在bucketName指定的桶下。如果该目录不存在，程序会自动创建。</p>
    </td>
    </tr>
    <tr id="row147502589331"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.5.1.1 "><p id="p20751858133310"><a name="p20751858133310"></a><a name="p20751858133310"></a>localFilePath</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.13%" headers="mcps1.2.5.1.2 "><p id="p97517581338"><a name="p97517581338"></a><a name="p97517581338"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.46%" headers="mcps1.2.5.1.3 "><p id="p137511558123313"><a name="p137511558123313"></a><a name="p137511558123313"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.57%" headers="mcps1.2.5.1.4 "><p id="p1947213712368"><a name="p1947213712368"></a><a name="p1947213712368"></a>存放Spark程序中使用的jar包、Python程序文件、配置文件等的本地目录。</p>
    <p id="p47524581335"><a name="p47524581335"></a><a name="p47524581335"></a>程序会自动将Spark程序依赖到的相关文件上传的OBS路径，并加载到DLI服务端资源包。</p>
    </td>
    </tr>
    <tr id="row4715182812316"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.5.1.1 "><p id="p1715182816312"><a name="p1715182816312"></a><a name="p1715182816312"></a>ak</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.13%" headers="mcps1.2.5.1.2 "><p id="p9715182863112"><a name="p9715182863112"></a><a name="p9715182863112"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.46%" headers="mcps1.2.5.1.3 "><p id="p9715528123112"><a name="p9715528123112"></a><a name="p9715528123112"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.57%" headers="mcps1.2.5.1.4 "><p id="p2715192883114"><a name="p2715192883114"></a><a name="p2715192883114"></a>用户的Access Key。</p>
    </td>
    </tr>
    <tr id="row12280456104419"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.5.1.1 "><p id="p7281125694415"><a name="p7281125694415"></a><a name="p7281125694415"></a>sk</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.13%" headers="mcps1.2.5.1.2 "><p id="p628145604410"><a name="p628145604410"></a><a name="p628145604410"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.46%" headers="mcps1.2.5.1.3 "><p id="p6281185644413"><a name="p6281185644413"></a><a name="p6281185644413"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.57%" headers="mcps1.2.5.1.4 "><p id="p22811756124410"><a name="p22811756124410"></a><a name="p22811756124410"></a>用户的Secret Key。</p>
    </td>
    </tr>
    <tr id="row596810814520"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.5.1.1 "><p id="p14968589452"><a name="p14968589452"></a><a name="p14968589452"></a>projectId</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.13%" headers="mcps1.2.5.1.2 "><p id="p1696910854519"><a name="p1696910854519"></a><a name="p1696910854519"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.46%" headers="mcps1.2.5.1.3 "><p id="p7969381452"><a name="p7969381452"></a><a name="p7969381452"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.57%" headers="mcps1.2.5.1.4 "><p id="p996918154519"><a name="p996918154519"></a><a name="p996918154519"></a>用户访问的DLI服务使用的项目编号。</p>
    </td>
    </tr>
    <tr id="row10516594514"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.5.1.1 "><p id="p16545104517"><a name="p16545104517"></a><a name="p16545104517"></a>region</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.13%" headers="mcps1.2.5.1.2 "><p id="p2611518456"><a name="p2611518456"></a><a name="p2611518456"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.46%" headers="mcps1.2.5.1.3 "><p id="p2619534518"><a name="p2619534518"></a><a name="p2619534518"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.57%" headers="mcps1.2.5.1.4 "><p id="p10645104510"><a name="p10645104510"></a><a name="p10645104510"></a>对接的DLI服务的Region，例如：cn-north-1。</p>
    </td>
    </tr>
    </tbody>
    </table>

    根据Spark应用程序的需要，修改“spark-defaults.conf”中的配置项，配置项兼容开源Spark配置项，参考开源Spark的配置项说明。


## 使用Spark-submit提交Spark作业<a name="section223712146331"></a>

1.  进入工具文件bin目录，执行spark-submit命令，并携带相关参数。

    命令执行格式：

    ```
    spark-submit [options] <app jar | python file> [app arguments]
    ```

    **表 2**  DLI Spark-submit参数列表

    <a name="table7810194416426"></a>
    <table><thead align="left"><tr id="row180874434217"><th class="cellrowborder" valign="top" width="17.59%" id="mcps1.2.4.1.1"><p id="p128085447429"><a name="p128085447429"></a><a name="p128085447429"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.83%" id="mcps1.2.4.1.2"><p id="p20808174410425"><a name="p20808174410425"></a><a name="p20808174410425"></a>参数值</p>
    </th>
    <th class="cellrowborder" valign="top" width="60.58%" id="mcps1.2.4.1.3"><p id="p14808194434219"><a name="p14808194434219"></a><a name="p14808194434219"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row6809124404213"><td class="cellrowborder" valign="top" width="17.59%" headers="mcps1.2.4.1.1 "><p id="p480814454218"><a name="p480814454218"></a><a name="p480814454218"></a>--class</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.83%" headers="mcps1.2.4.1.2 "><p id="p19808134424215"><a name="p19808134424215"></a><a name="p19808134424215"></a>&lt;CLASS_NAME&gt;</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.58%" headers="mcps1.2.4.1.3 "><p id="p857611954917"><a name="p857611954917"></a><a name="p857611954917"></a>提交的Java/Scala应用程序的主类名称。</p>
    </td>
    </tr>
    <tr id="row181017443420"><td class="cellrowborder" valign="top" width="17.59%" headers="mcps1.2.4.1.1 "><p id="p180954484210"><a name="p180954484210"></a><a name="p180954484210"></a>--conf</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.83%" headers="mcps1.2.4.1.2 "><p id="p128091544154216"><a name="p128091544154216"></a><a name="p128091544154216"></a>&lt;PROP=VALUE&gt;</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.58%" headers="mcps1.2.4.1.3 "><p id="p18573919184914"><a name="p18573919184914"></a><a name="p18573919184914"></a>Spark程序的参数，可以通过在conf目录下的spark-defaults.conf中配置。如果命令中与配置文件中同时配置，优先使用命令指定的参数值。</p>
    <div class="note" id="note81016135509"><a name="note81016135509"></a><a name="note81016135509"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p311113145012"><a name="p311113145012"></a><a name="p311113145012"></a>多个conf时，格式为：--conf key1=value1 --conf key2=value2</p>
    </div></div>
    </td>
    </tr>
    <tr id="row1081094419421"><td class="cellrowborder" valign="top" width="17.59%" headers="mcps1.2.4.1.1 "><p id="p2810164444211"><a name="p2810164444211"></a><a name="p2810164444211"></a>--jars</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.83%" headers="mcps1.2.4.1.2 "><p id="p7810124416429"><a name="p7810124416429"></a><a name="p7810124416429"></a>&lt;JARS&gt;</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.58%" headers="mcps1.2.4.1.3 "><p id="p2571111934914"><a name="p2571111934914"></a><a name="p2571111934914"></a>Spark应用依赖的jar包名称，存在多个时使用","分割。jar包文件需要提前保存在client.properties文件中localFilePath配置的本地路径中。</p>
    </td>
    </tr>
    <tr id="row1681064410424"><td class="cellrowborder" valign="top" width="17.59%" headers="mcps1.2.4.1.1 "><p id="p20810134417428"><a name="p20810134417428"></a><a name="p20810134417428"></a>--name</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.83%" headers="mcps1.2.4.1.2 "><p id="p081094419427"><a name="p081094419427"></a><a name="p081094419427"></a>&lt;NAME&gt;</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.58%" headers="mcps1.2.4.1.3 "><p id="p1254641904913"><a name="p1254641904913"></a><a name="p1254641904913"></a>Spark应用的名称。</p>
    </td>
    </tr>
    <tr id="row77075745011"><td class="cellrowborder" valign="top" width="17.59%" headers="mcps1.2.4.1.1 "><p id="p1707127105020"><a name="p1707127105020"></a><a name="p1707127105020"></a>--queue</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.83%" headers="mcps1.2.4.1.2 "><p id="p1370720717507"><a name="p1370720717507"></a><a name="p1370720717507"></a>&lt;QUEUE_NAME&gt;</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.58%" headers="mcps1.2.4.1.3 "><p id="p37074719505"><a name="p37074719505"></a><a name="p37074719505"></a>DLI服务端Spark队列名称，作业会提交到该队列中执行。</p>
    </td>
    </tr>
    <tr id="row739012085011"><td class="cellrowborder" valign="top" width="17.59%" headers="mcps1.2.4.1.1 "><p id="p93916015502"><a name="p93916015502"></a><a name="p93916015502"></a>--py-files</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.83%" headers="mcps1.2.4.1.2 "><p id="p7391160165018"><a name="p7391160165018"></a><a name="p7391160165018"></a>&lt;PY_FILES&gt;</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.58%" headers="mcps1.2.4.1.3 "><p id="p439118085013"><a name="p439118085013"></a><a name="p439118085013"></a>Spark应用依赖的Python程序文件名称，存在多个时使用","分割。Python程序文件文件需要提前保存在client.properties文件中localFilePath配置的本地路面中。</p>
    </td>
    </tr>
    <tr id="row03121526155019"><td class="cellrowborder" valign="top" width="17.59%" headers="mcps1.2.4.1.1 "><p id="p2312162612504"><a name="p2312162612504"></a><a name="p2312162612504"></a>-s,--skip-upload-resources</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.83%" headers="mcps1.2.4.1.2 "><p id="p331272625012"><a name="p331272625012"></a><a name="p331272625012"></a>&lt;all | app | deps&gt;</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.58%" headers="mcps1.2.4.1.3 "><p id="p123125269502"><a name="p123125269502"></a><a name="p123125269502"></a>是否跳过，将jar包、Python程序文件、配置文件上传到OBS和加载到DLI服务端资源列表。当相关资源文件已经加载到DLI服务资源列表中，可以使用该参数跳过该步骤。</p>
    <p id="p988914164412"><a name="p988914164412"></a><a name="p988914164412"></a>不携带该参数时，默认会上传和加载命令中的所有资源文件到DLI服务中。</p>
    <a name="ul15146455105118"></a><a name="ul15146455105118"></a><ul id="ul15146455105118"><li>all：跳过所有资源文件的上传和加载</li><li>app：跳过Spark应用程序文件的上传和加载</li><li>deps：跳过所有依赖文件的上传和加载</li></ul>
    </td>
    </tr>
    <tr id="row783621125114"><td class="cellrowborder" valign="top" width="17.59%" headers="mcps1.2.4.1.1 "><p id="p68369145118"><a name="p68369145118"></a><a name="p68369145118"></a>-h,--help</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.83%" headers="mcps1.2.4.1.2 "><p id="p88361011518"><a name="p88361011518"></a><a name="p88361011518"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.58%" headers="mcps1.2.4.1.3 "><p id="p3836141115117"><a name="p3836141115117"></a><a name="p3836141115117"></a>打印命令帮助</p>
    </td>
    </tr>
    </tbody>
    </table>

    命令举例：

    ```
    ./spark-submit --name Spark_PI --queue spark_queue --skip-upload-resources all --class org.apache.spark.examples.SparkPi spark-examples_2.11-2.1.0.luxor.jar 10
    ./spark-submit --name WordCount --queue spark_queue word_count.py
    ```


