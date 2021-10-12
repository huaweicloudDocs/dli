# 新建Flink Jar作业<a name="dli_02_0230"></a>

## 功能介绍<a name="s89ff8bc59cba4c3b94dc17e85c8fa1ea"></a>

该API用于创建用户自定义的作业，目前支持jar格式，运行在独享队列中。

## 调试<a name="section556523314214"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=DLI&api=CreateFlinkJar)中调试该接口。

## URI<a name="sef21e3efc2a44a84a03adad33a1ae006"></a>

-   URI格式

    POST /v1.0/\{project\_id\}/streaming/flink-jobs

-   参数说明

    **表 1**  URI参数说明

    <a name="t219b031199884ac1bb9e91158ddc9efb"></a>
    <table><thead align="left"><tr id="r04005eeda24e4db9b06516450d4d56af"><th class="cellrowborder" valign="top" width="16.82%" id="mcps1.2.5.1.1"><p id="a80847df5e5dc448caa46a2ff258fa2c4"><a name="a80847df5e5dc448caa46a2ff258fa2c4"></a><a name="a80847df5e5dc448caa46a2ff258fa2c4"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.2%" id="mcps1.2.5.1.2"><p id="af54fc16087b049c98f748c1a2faace17"><a name="af54fc16087b049c98f748c1a2faace17"></a><a name="af54fc16087b049c98f748c1a2faace17"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="10.42%" id="mcps1.2.5.1.3"><p id="p138331863114"><a name="p138331863114"></a><a name="p138331863114"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="60.56%" id="mcps1.2.5.1.4"><p id="a484a3e0ce14846799c727ccbd4075d6c"><a name="a484a3e0ce14846799c727ccbd4075d6c"></a><a name="a484a3e0ce14846799c727ccbd4075d6c"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="r8022e11be3f54ad290cf8c848a56a550"><td class="cellrowborder" valign="top" width="16.82%" headers="mcps1.2.5.1.1 "><p id="p1262440203315"><a name="p1262440203315"></a><a name="p1262440203315"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.2%" headers="mcps1.2.5.1.2 "><p id="p1016041415356"><a name="p1016041415356"></a><a name="p1016041415356"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.42%" headers="mcps1.2.5.1.3 "><p id="p14833188133115"><a name="p14833188133115"></a><a name="p14833188133115"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.56%" headers="mcps1.2.5.1.4 "><p id="p1768719515356"><a name="p1768719515356"></a><a name="p1768719515356"></a>项目编号，用于资源隔离。获取方式请参考<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="s3afece1037ea4f62aeffb3db49b97f70"></a>

**表 2**  参数说明

<a name="table167338273210"></a>
<table><thead align="left"><tr id="row473492772112"><th class="cellrowborder" valign="top" width="24.349999999999998%" id="mcps1.2.5.1.1"><p id="p1473442722114"><a name="p1473442722114"></a><a name="p1473442722114"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="11.83%" id="mcps1.2.5.1.2"><p id="p924151853112"><a name="p924151853112"></a><a name="p924151853112"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="12.049999999999999%" id="mcps1.2.5.1.3"><p id="p137119461396"><a name="p137119461396"></a><a name="p137119461396"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="51.77%" id="mcps1.2.5.1.4"><p id="p1873432716213"><a name="p1873432716213"></a><a name="p1873432716213"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row137341727132113"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p6734122720213"><a name="p6734122720213"></a><a name="p6734122720213"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p16241141810311"><a name="p16241141810311"></a><a name="p16241141810311"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p394123011411"><a name="p394123011411"></a><a name="p394123011411"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p12734427152118"><a name="p12734427152118"></a><a name="p12734427152118"></a>作业名称。长度限制：0-57个字符。</p>
</td>
</tr>
<tr id="row157341727112111"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p37343278217"><a name="p37343278217"></a><a name="p37343278217"></a>desc</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p16241121816313"><a name="p16241121816313"></a><a name="p16241121816313"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p134186214816"><a name="p134186214816"></a><a name="p134186214816"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p207341827192110"><a name="p207341827192110"></a><a name="p207341827192110"></a>作业描述。长度限制：0-512个字符。</p>
</td>
</tr>
<tr id="row668327131518"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p621523961515"><a name="p621523961515"></a><a name="p621523961515"></a>queue_name</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p1721515390153"><a name="p1721515390153"></a><a name="p1721515390153"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p82151339141519"><a name="p82151339141519"></a><a name="p82151339141519"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p821553918157"><a name="p821553918157"></a><a name="p821553918157"></a>队列名称。长度限制：1-128个字符。</p>
</td>
</tr>
<tr id="row573417279212"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p1773410271210"><a name="p1773410271210"></a><a name="p1773410271210"></a>cu_number</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p1524121873112"><a name="p1524121873112"></a><a name="p1524121873112"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p191902533811"><a name="p191902533811"></a><a name="p191902533811"></a><span>Integer</span></p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p157341327112113"><a name="p157341327112113"></a><a name="p157341327112113"></a>用户为作业选择的CU数量。</p>
</td>
</tr>
<tr id="row8381047124211"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p3942456173617"><a name="p3942456173617"></a><a name="p3942456173617"></a>manager_cu_number</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p1494215615362"><a name="p1494215615362"></a><a name="p1494215615362"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p3942135673612"><a name="p3942135673612"></a><a name="p3942135673612"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p29421456113614"><a name="p29421456113614"></a><a name="p29421456113614"></a>用户为作业选择的管理节点CU数量，对应为flink jobmanager数量。默认值为“1”。</p>
</td>
</tr>
<tr id="row873413275210"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p978704819454"><a name="p978704819454"></a><a name="p978704819454"></a>parallel_number</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p12439184316"><a name="p12439184316"></a><a name="p12439184316"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p14728172409"><a name="p14728172409"></a><a name="p14728172409"></a><span>Integer</span></p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p15964644992"><a name="p15964644992"></a><a name="p15964644992"></a>用户为作业选择的并发量。</p>
</td>
</tr>
<tr id="row1679750142215"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p19797100225"><a name="p19797100225"></a><a name="p19797100225"></a>log_enabled</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p1124310189313"><a name="p1124310189313"></a><a name="p1124310189313"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p585014405335"><a name="p585014405335"></a><a name="p585014405335"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p201891638534"><a name="p201891638534"></a><a name="p201891638534"></a>是否开启作业日志。</p>
<a name="ul960951941319"></a><a name="ul960951941319"></a><ul id="ul960951941319"><li>开启：true</li><li>关闭：false</li><li>默认：false</li></ul>
</td>
</tr>
<tr id="row5797130182213"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p127987013227"><a name="p127987013227"></a><a name="p127987013227"></a>obs_bucket</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p10243181816311"><a name="p10243181816311"></a><a name="p10243181816311"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p244659164112"><a name="p244659164112"></a><a name="p244659164112"></a><span>String</span></p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p14798100122220"><a name="p14798100122220"></a><a name="p14798100122220"></a>当<span class="parmname" id="parmname20575220114617"><a name="parmname20575220114617"></a><a name="parmname20575220114617"></a>“log_enabled”</span>为<span class="parmvalue" id="parmvalue14261642114617"><a name="parmvalue14261642114617"></a><a name="parmvalue14261642114617"></a>“true”</span>时, 用户授权保存作业日志的OBS桶名。</p>
</td>
</tr>
<tr id="row16913193319413"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p391319334411"><a name="p391319334411"></a><a name="p391319334411"></a>smn_topic</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p152434182319"><a name="p152434182319"></a><a name="p152434182319"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p285034019338"><a name="p285034019338"></a><a name="p285034019338"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p1491312333417"><a name="p1491312333417"></a><a name="p1491312333417"></a>当作业异常时，向该SMN主题推送告警信息。</p>
</td>
</tr>
<tr id="row1667713917350"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p1767811915356"><a name="p1767811915356"></a><a name="p1767811915356"></a>main_class</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p1524331818315"><a name="p1524331818315"></a><a name="p1524331818315"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p18966151111382"><a name="p18966151111382"></a><a name="p18966151111382"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p867818923519"><a name="p867818923519"></a><a name="p867818923519"></a>作业入口类。</p>
</td>
</tr>
<tr id="row1567815917356"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p1067811920359"><a name="p1067811920359"></a><a name="p1067811920359"></a>entrypoint_args</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p92431918103111"><a name="p92431918103111"></a><a name="p92431918103111"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p1696618119384"><a name="p1696618119384"></a><a name="p1696618119384"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p1367814923518"><a name="p1367814923518"></a><a name="p1367814923518"></a>作业入口类参数，多个参数之间空格分隔。</p>
</td>
</tr>
<tr id="row181283543917"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p8559173762410"><a name="p8559173762410"></a><a name="p8559173762410"></a>restart_when_exception</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p256063714247"><a name="p256063714247"></a><a name="p256063714247"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p84861029174011"><a name="p84861029174011"></a><a name="p84861029174011"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p85601437192419"><a name="p85601437192419"></a><a name="p85601437192419"></a>是否开启异常重启功能，默认值为“false”。</p>
</td>
</tr>
<tr id="row48781249517"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p8948157185118"><a name="p8948157185118"></a><a name="p8948157185118"></a>entrypoint</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p119484755116"><a name="p119484755116"></a><a name="p119484755116"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p49487710511"><a name="p49487710511"></a><a name="p49487710511"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p14948375511"><a name="p14948375511"></a><a name="p14948375511"></a>用户已上传到DLI资源管理系统的程序包名，用户自定义作业主类所在的jar包。</p>
</td>
</tr>
<tr id="row1823375616469"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p7233155624618"><a name="p7233155624618"></a><a name="p7233155624618"></a>dependency_jars</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p42331956124615"><a name="p42331956124615"></a><a name="p42331956124615"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p9233155654619"><a name="p9233155654619"></a><a name="p9233155654619"></a>Array of Strings</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p8233135664619"><a name="p8233135664619"></a><a name="p8233135664619"></a>用户已上传到DLI资源管理系统的程序包名，用户自定义作业的其他依赖包。</p>
<p id="p19536182203415"><a name="p19536182203415"></a><a name="p19536182203415"></a>示例“myGroup/test.jar,myGroup/test1.jar”。</p>
</td>
</tr>
<tr id="row17488175413010"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p174899543309"><a name="p174899543309"></a><a name="p174899543309"></a>dependency_files</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p1548919541305"><a name="p1548919541305"></a><a name="p1548919541305"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p748975419303"><a name="p748975419303"></a><a name="p748975419303"></a>Array of Strings</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p12748153919317"><a name="p12748153919317"></a><a name="p12748153919317"></a>用户已上传到DLI资源管理系统的资源包名，用户自定义作业的依赖文件。</p>
<p id="p948945412308"><a name="p948945412308"></a><a name="p948945412308"></a>示例："myGroup/test.cvs,myGroup/test1.csv"。</p>
<p id="p12932165261213"><a name="p12932165261213"></a><a name="p12932165261213"></a>通过在应用程序中添加以下内容可访问对应的依赖文件。其中，<span class="parmname" id="parmname107641928104518"><a name="parmname107641928104518"></a><a name="parmname107641928104518"></a>“fileName”</span>为需要访问的文件名，<span class="parmname" id="parmname3771161885511"><a name="parmname3771161885511"></a><a name="parmname3771161885511"></a>“ClassName”</span>为需要访问该文件的类名。</p>
<pre class="screen" id="screen43817144438"><a name="screen43817144438"></a><a name="screen43817144438"></a>ClassName.class.getClassLoader().getResource("userData/fileName")</pre>
</td>
</tr>
<tr id="row1427415315216"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p62741531828"><a name="p62741531828"></a><a name="p62741531828"></a>tm_cus</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p1827415533218"><a name="p1827415533218"></a><a name="p1827415533218"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p132740531925"><a name="p132740531925"></a><a name="p132740531925"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p9274165315217"><a name="p9274165315217"></a><a name="p9274165315217"></a>每个taskmanager的CU数，默认值为“1”。</p>
</td>
</tr>
<tr id="row15274853229"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p122748531625"><a name="p122748531625"></a><a name="p122748531625"></a>tm_slot_num</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p1274125315210"><a name="p1274125315210"></a><a name="p1274125315210"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p1327455313218"><a name="p1327455313218"></a><a name="p1327455313218"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p4275145317210"><a name="p4275145317210"></a><a name="p4275145317210"></a>每个taskmanager的slot数，默认值为“(parallel_number*tm_cus)/(cu_number-manager_cu_number)”。</p>
</td>
</tr>
<tr id="row251342814499"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p9514112812492"><a name="p9514112812492"></a><a name="p9514112812492"></a>feature</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p16514112824913"><a name="p16514112824913"></a><a name="p16514112824913"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p19514182854915"><a name="p19514182854915"></a><a name="p19514182854915"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p1460244195120"><a name="p1460244195120"></a><a name="p1460244195120"></a>作业特性。表示用户作业使用的Flink镜像类型。</p>
<a name="ul358410443526"></a><a name="ul358410443526"></a><ul id="ul358410443526"><li>basic：表示使用DLI提供的基础Flink镜像。</li><li>custom：表示使用用户自定义的Flink镜像。</li></ul>
</td>
</tr>
<tr id="row651552814492"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p8515162804917"><a name="p8515162804917"></a><a name="p8515162804917"></a>flink_version</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p10515128154916"><a name="p10515128154916"></a><a name="p10515128154916"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p5515102864914"><a name="p5515102864914"></a><a name="p5515102864914"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p7413142220535"><a name="p7413142220535"></a><a name="p7413142220535"></a>Flink版本。当用户设置<span class="parmname" id="parmname846018533539"><a name="parmname846018533539"></a><a name="parmname846018533539"></a>“feature”</span>为<span class="parmvalue" id="parmvalue5322558125318"><a name="parmvalue5322558125318"></a><a name="parmvalue5322558125318"></a>“basic”</span>时，该参数生效。用户可通过与<span class="parmname" id="parmname2833151105416"><a name="parmname2833151105416"></a><a name="parmname2833151105416"></a>“feature”</span>参数配合使用，指定作业运行使用的DLI基础Flink镜像的版本。</p>
</td>
</tr>
<tr id="row2515172894920"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p2051522884917"><a name="p2051522884917"></a><a name="p2051522884917"></a>image</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p351414518540"><a name="p351414518540"></a><a name="p351414518540"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p4515928104918"><a name="p4515928104918"></a><a name="p4515928104918"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p7183123618559"><a name="p7183123618559"></a><a name="p7183123618559"></a>自定义镜像。格式为：组织名/镜像名:镜像版本。</p>
<p id="p3744101605514"><a name="p3744101605514"></a><a name="p3744101605514"></a>当用户设置<span class="parmname" id="parmname138247425555"><a name="parmname138247425555"></a><a name="parmname138247425555"></a>“feature”</span>为<span class="parmvalue" id="parmvalue2059854718551"><a name="parmvalue2059854718551"></a><a name="parmvalue2059854718551"></a>“custom”</span>时，该参数生效。用户可通过与<span class="parmname" id="parmname9777102175614"><a name="parmname9777102175614"></a><a name="parmname9777102175614"></a>“feature”</span>参数配合使用，指定作业运行使用自定义的Flink镜像。关于如何使用自定义镜像，请参考《<a href="https://support.huaweicloud.com/usermanual-dli/dli_01_0494.html" target="_blank" rel="noopener noreferrer">数据湖探索用户指南</a>》。</p>
</td>
</tr>
<tr id="row8139104392613"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p2335124251810"><a name="p2335124251810"></a><a name="p2335124251810"></a>resume_checkpoint</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p173354422187"><a name="p173354422187"></a><a name="p173354422187"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p113357429186"><a name="p113357429186"></a><a name="p113357429186"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p233519428187"><a name="p233519428187"></a><a name="p233519428187"></a>异常重启是否从checkpoint恢复。</p>
</td>
</tr>
<tr id="row7137124342615"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p3543245162311"><a name="p3543245162311"></a><a name="p3543245162311"></a>resume_max_num</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p9541245182312"><a name="p9541245182312"></a><a name="p9541245182312"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p185409459238"><a name="p185409459238"></a><a name="p185409459238"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p1549119459232"><a name="p1549119459232"></a><a name="p1549119459232"></a>异常重试最大次数，单位：次/小时。取值范围：-1或大于0。默认值为“-1”，表示无限次数。</p>
</td>
</tr>
<tr id="row91351143152614"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p1336124261814"><a name="p1336124261814"></a><a name="p1336124261814"></a>checkpoint_path</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p153361942171813"><a name="p153361942171813"></a><a name="p153361942171813"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p73361242191816"><a name="p73361242191816"></a><a name="p73361242191816"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p633644216183"><a name="p633644216183"></a><a name="p633644216183"></a>用户Jar中checkpoint的储存地址，不同作业路径需要保持不同。</p>
</td>
</tr>
<tr id="row11947101815413"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p912055285516"><a name="p912055285516"></a><a name="p912055285516"></a>tags</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p712010527557"><a name="p712010527557"></a><a name="p712010527557"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p13120195215519"><a name="p13120195215519"></a><a name="p13120195215519"></a>Array of Objects</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p10120125235516"><a name="p10120125235516"></a><a name="p10120125235516"></a>Flink jar作业的标签。具体请参考<a href="#table9391124139">表3</a>。</p>
</td>
</tr>
<tr id="row3617637115710"><td class="cellrowborder" valign="top" width="24.349999999999998%" headers="mcps1.2.5.1.1 "><p id="p95362034690"><a name="p95362034690"></a><a name="p95362034690"></a>runtime_config</p>
</td>
<td class="cellrowborder" valign="top" width="11.83%" headers="mcps1.2.5.1.2 "><p id="p165376345912"><a name="p165376345912"></a><a name="p165376345912"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.049999999999999%" headers="mcps1.2.5.1.3 "><p id="p25373349919"><a name="p25373349919"></a><a name="p25373349919"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.77%" headers="mcps1.2.5.1.4 "><p id="p1153712346915"><a name="p1153712346915"></a><a name="p1153712346915"></a>Flink作业运行时自定义优化参数。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  tags参数

<a name="table9391124139"></a>
<table><thead align="left"><tr id="row1440020130"><th class="cellrowborder" valign="top" width="14.899999999999999%" id="mcps1.2.5.1.1"><p id="p194012219139"><a name="p194012219139"></a><a name="p194012219139"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="10.83%" id="mcps1.2.5.1.2"><p id="p540724136"><a name="p540724136"></a><a name="p540724136"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="16.470000000000002%" id="mcps1.2.5.1.3"><p id="p840162161315"><a name="p840162161315"></a><a name="p840162161315"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="57.8%" id="mcps1.2.5.1.4"><p id="p16401271318"><a name="p16401271318"></a><a name="p16401271318"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row194013231317"><td class="cellrowborder" valign="top" width="14.899999999999999%" headers="mcps1.2.5.1.1 "><p id="p13401329138"><a name="p13401329138"></a><a name="p13401329138"></a>key</p>
</td>
<td class="cellrowborder" valign="top" width="10.83%" headers="mcps1.2.5.1.2 "><p id="p940102141313"><a name="p940102141313"></a><a name="p940102141313"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="16.470000000000002%" headers="mcps1.2.5.1.3 "><p id="p64019231317"><a name="p64019231317"></a><a name="p64019231317"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="57.8%" headers="mcps1.2.5.1.4 "><p id="p5401021139"><a name="p5401021139"></a><a name="p5401021139"></a>标签的键。</p>
</td>
</tr>
<tr id="row1141142181320"><td class="cellrowborder" valign="top" width="14.899999999999999%" headers="mcps1.2.5.1.1 "><p id="p164118215134"><a name="p164118215134"></a><a name="p164118215134"></a>value</p>
</td>
<td class="cellrowborder" valign="top" width="10.83%" headers="mcps1.2.5.1.2 "><p id="p1141112181317"><a name="p1141112181317"></a><a name="p1141112181317"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="16.470000000000002%" headers="mcps1.2.5.1.3 "><p id="p174114281318"><a name="p174114281318"></a><a name="p174114281318"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="57.8%" headers="mcps1.2.5.1.4 "><p id="p16411125137"><a name="p16411125137"></a><a name="p16411125137"></a>标签的值。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="se2bf80cdb76541308f69f258ea4b1bd6"></a>

**表 4**  响应参数说明

<a name="t5995d65f65ba4ebca8606202112b407e"></a>
<table><thead align="left"><tr id="ra7acea51e4b4437e917d21fe99f130a3"><th class="cellrowborder" valign="top" width="19.25%" id="mcps1.2.5.1.1"><p id="a5af940f2267747ef871c67c86a0be82e"><a name="a5af940f2267747ef871c67c86a0be82e"></a><a name="a5af940f2267747ef871c67c86a0be82e"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="14.44%" id="mcps1.2.5.1.2"><p id="abcfbd3a651704d539626f3a41cc744f5"><a name="abcfbd3a651704d539626f3a41cc744f5"></a><a name="abcfbd3a651704d539626f3a41cc744f5"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="13.370000000000001%" id="mcps1.2.5.1.3"><p id="a2351d8d266444ad3ad1c09540d6d81cc"><a name="a2351d8d266444ad3ad1c09540d6d81cc"></a><a name="a2351d8d266444ad3ad1c09540d6d81cc"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="52.94%" id="mcps1.2.5.1.4"><p id="af7ea6a3f59844bdf99d51e90d570be4c"><a name="af7ea6a3f59844bdf99d51e90d570be4c"></a><a name="af7ea6a3f59844bdf99d51e90d570be4c"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row2418154742"><td class="cellrowborder" valign="top" width="19.25%" headers="mcps1.2.5.1.1 "><p id="p2827183519"><a name="p2827183519"></a><a name="p2827183519"></a>is_success</p>
</td>
<td class="cellrowborder" valign="top" width="14.44%" headers="mcps1.2.5.1.2 "><p id="p6362111364911"><a name="p6362111364911"></a><a name="p6362111364911"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="13.370000000000001%" headers="mcps1.2.5.1.3 "><p id="p118601817517"><a name="p118601817517"></a><a name="p118601817517"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.5.1.4 "><p id="p1487318359"><a name="p1487318359"></a><a name="p1487318359"></a>执行请求是否成功。“true”表示请求执行成功。</p>
</td>
</tr>
<tr id="row64180541741"><td class="cellrowborder" valign="top" width="19.25%" headers="mcps1.2.5.1.1 "><p id="a4aba020b918e457a8a3d15e7ebaeb20d"><a name="a4aba020b918e457a8a3d15e7ebaeb20d"></a><a name="a4aba020b918e457a8a3d15e7ebaeb20d"></a>message</p>
</td>
<td class="cellrowborder" valign="top" width="14.44%" headers="mcps1.2.5.1.2 "><p id="p11374111319494"><a name="p11374111319494"></a><a name="p11374111319494"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="13.370000000000001%" headers="mcps1.2.5.1.3 "><p id="ac85edc0a27d044b0ad524a4124e59e4c"><a name="ac85edc0a27d044b0ad524a4124e59e4c"></a><a name="ac85edc0a27d044b0ad524a4124e59e4c"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.5.1.4 "><p id="ac087aec9dfcc407ba244ad3e96b23257"><a name="ac087aec9dfcc407ba244ad3e96b23257"></a><a name="ac087aec9dfcc407ba244ad3e96b23257"></a>消息内容。</p>
</td>
</tr>
<tr id="row15874961669"><td class="cellrowborder" valign="top" width="19.25%" headers="mcps1.2.5.1.1 "><p id="p933863862615"><a name="p933863862615"></a><a name="p933863862615"></a>job</p>
</td>
<td class="cellrowborder" valign="top" width="14.44%" headers="mcps1.2.5.1.2 "><p id="p9338638122617"><a name="p9338638122617"></a><a name="p9338638122617"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="13.370000000000001%" headers="mcps1.2.5.1.3 "><p id="p33383387265"><a name="p33383387265"></a><a name="p33383387265"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.5.1.4 "><p id="p18338103822617"><a name="p18338103822617"></a><a name="p18338103822617"></a>作业状态信息。具体请参考<a href="#table86492245453">表5</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  job参数说明

<a name="table86492245453"></a>
<table><thead align="left"><tr id="row176501524184518"><th class="cellrowborder" valign="top" width="19.25%" id="mcps1.2.5.1.1"><p id="p18650152414511"><a name="p18650152414511"></a><a name="p18650152414511"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="14.44%" id="mcps1.2.5.1.2"><p id="p10650424204518"><a name="p10650424204518"></a><a name="p10650424204518"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="13.370000000000001%" id="mcps1.2.5.1.3"><p id="p865022420455"><a name="p865022420455"></a><a name="p865022420455"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="52.94%" id="mcps1.2.5.1.4"><p id="p10650192416454"><a name="p10650192416454"></a><a name="p10650192416454"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1965211245455"><td class="cellrowborder" valign="top" width="19.25%" headers="mcps1.2.5.1.1 "><p id="p265214241459"><a name="p265214241459"></a><a name="p265214241459"></a>job_id</p>
</td>
<td class="cellrowborder" valign="top" width="14.44%" headers="mcps1.2.5.1.2 "><p id="p176521824104518"><a name="p176521824104518"></a><a name="p176521824104518"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="13.370000000000001%" headers="mcps1.2.5.1.3 "><p id="p965292416455"><a name="p965292416455"></a><a name="p965292416455"></a>Long</p>
</td>
<td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.5.1.4 "><p id="p26525248455"><a name="p26525248455"></a><a name="p26525248455"></a>作业ID。</p>
</td>
</tr>
<tr id="row1465210242456"><td class="cellrowborder" valign="top" width="19.25%" headers="mcps1.2.5.1.1 "><p id="p1465252404513"><a name="p1465252404513"></a><a name="p1465252404513"></a>status_name</p>
</td>
<td class="cellrowborder" valign="top" width="14.44%" headers="mcps1.2.5.1.2 "><p id="p8652624134510"><a name="p8652624134510"></a><a name="p8652624134510"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="13.370000000000001%" headers="mcps1.2.5.1.3 "><p id="p665282413457"><a name="p665282413457"></a><a name="p665282413457"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.5.1.4 "><p id="p156531124134510"><a name="p156531124134510"></a><a name="p156531124134510"></a>当前状态名称。</p>
</td>
</tr>
<tr id="row1865352464519"><td class="cellrowborder" valign="top" width="19.25%" headers="mcps1.2.5.1.1 "><p id="p1665314248452"><a name="p1665314248452"></a><a name="p1665314248452"></a>status_desc</p>
</td>
<td class="cellrowborder" valign="top" width="14.44%" headers="mcps1.2.5.1.2 "><p id="p15653122464517"><a name="p15653122464517"></a><a name="p15653122464517"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="13.370000000000001%" headers="mcps1.2.5.1.3 "><p id="p14653024114510"><a name="p14653024114510"></a><a name="p14653024114510"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.5.1.4 "><p id="p565313246452"><a name="p565313246452"></a><a name="p565313246452"></a>当前状态描述。包含异常状态原因及建议。</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section1572521517329"></a>

-   请求样例

    ```
    {
        "name": "test",
        "desc": "job for test",
        "queue_name": "testQueue",
        "manager_cu_number": 1,
        "cu_number": 2,
        "parallel_number": 1,
        "tm_cus": 1,
        "tm_slot_num": 1,
        "log_enabled": true,
        "obs_bucket": "bucketName",
        "smn_topic": "topic",
        "main_class": "org.apache.flink.examples.streaming.JavaQueueStream",
        "restart_when_exception": false,
        "entrypoint": "javaQueueStream.jar",
        "entrypoint_args":"-windowSize 2000 -rate3",
        "dependency_jars": [
            "myGroup/test.jar",
            "myGroup/test1.jar"
        ],
        "dependency_files": [
            "myGroup/test.csv",
            "myGroup/test1.csv"
        ]
    }
    ```

-   响应样例

    ```
    {
      "is_success": true,
      "message": "新建flink作业成功",
      "job": {
        "job_id": 138,
        "status_name": "job_init",
        "status_desc": ""
      }
    }
    ```


## 状态码<a name="s1b495ba11cd9411c9ad2ee50103334a7"></a>

状态码如[表6](#t43c1f1c0ba344f4cbcb270953d9cca2a)所示。

**表 6**  状态码

<a name="t43c1f1c0ba344f4cbcb270953d9cca2a"></a>
<table><thead align="left"><tr id="r2ad0f008ce2248a1800a3e8b77226a56"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.3.1.1"><p id="afa33b7f5b0ac4d008ebcf6493f629b24"><a name="afa33b7f5b0ac4d008ebcf6493f629b24"></a><a name="afa33b7f5b0ac4d008ebcf6493f629b24"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="70%" id="mcps1.2.3.1.2"><p id="af801170b350b4f8ba3b575c7ddb8b13e"><a name="af801170b350b4f8ba3b575c7ddb8b13e"></a><a name="af801170b350b4f8ba3b575c7ddb8b13e"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="r0b449b1d3b8c498ea3e6cce16c80a14c"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="a8c63a97e3bad402ebaead0bd99cad632"><a name="a8c63a97e3bad402ebaead0bd99cad632"></a><a name="a8c63a97e3bad402ebaead0bd99cad632"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="af86844c7bb364c48b6300df1af164af2"><a name="af86844c7bb364c48b6300df1af164af2"></a><a name="af86844c7bb364c48b6300df1af164af2"></a>新建Flink自定义作业成功。</p>
</td>
</tr>
<tr id="row1012873412149"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p1912813348145"><a name="p1912813348145"></a><a name="p1912813348145"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p154287617445"><a name="p154287617445"></a><a name="p154287617445"></a>输入参数无效。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section13596141025715"></a>

调用接口出错后，将不会返回上述结果，而是返回错误码和错误信息，更多介绍请参见[错误码](错误码.md)。

