# 更新Flink Jar作业<a name="dli_02_0231"></a>

## 功能介绍<a name="s89ff8bc59cba4c3b94dc17e85c8fa1ea"></a>

该API用于更新用户自定义作业，目前仅支持Jar格式，运行在独享队列中。

## 调试<a name="section556523314214"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=DLI&api=UpdateFlinkJar)中调试该接口。

## URI<a name="sef21e3efc2a44a84a03adad33a1ae006"></a>

-   URI格式

    PUT /v1.0/\{project\_id\}/streaming/flink-jobs/\{job\_id\}

-   参数说明

    **表 1**  URI参数说明

    <a name="t219b031199884ac1bb9e91158ddc9efb"></a>
    <table><thead align="left"><tr id="r04005eeda24e4db9b06516450d4d56af"><th class="cellrowborder" valign="top" width="17.47%" id="mcps1.2.5.1.1"><p id="a80847df5e5dc448caa46a2ff258fa2c4"><a name="a80847df5e5dc448caa46a2ff258fa2c4"></a><a name="a80847df5e5dc448caa46a2ff258fa2c4"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="11.62%" id="mcps1.2.5.1.2"><p id="af54fc16087b049c98f748c1a2faace17"><a name="af54fc16087b049c98f748c1a2faace17"></a><a name="af54fc16087b049c98f748c1a2faace17"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="11.39%" id="mcps1.2.5.1.3"><p id="p32272013232"><a name="p32272013232"></a><a name="p32272013232"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="59.519999999999996%" id="mcps1.2.5.1.4"><p id="a484a3e0ce14846799c727ccbd4075d6c"><a name="a484a3e0ce14846799c727ccbd4075d6c"></a><a name="a484a3e0ce14846799c727ccbd4075d6c"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="r8022e11be3f54ad290cf8c848a56a550"><td class="cellrowborder" valign="top" width="17.47%" headers="mcps1.2.5.1.1 "><p id="p1262440203315"><a name="p1262440203315"></a><a name="p1262440203315"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.62%" headers="mcps1.2.5.1.2 "><p id="p1016041415356"><a name="p1016041415356"></a><a name="p1016041415356"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.39%" headers="mcps1.2.5.1.3 "><p id="p1623820142310"><a name="p1623820142310"></a><a name="p1623820142310"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="59.519999999999996%" headers="mcps1.2.5.1.4 "><p id="p1768719515356"><a name="p1768719515356"></a><a name="p1768719515356"></a>项目编号，用于资源隔离。获取方式请参考<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    <tr id="row14405113219254"><td class="cellrowborder" valign="top" width="17.47%" headers="mcps1.2.5.1.1 "><p id="p12397103222510"><a name="p12397103222510"></a><a name="p12397103222510"></a>job_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.62%" headers="mcps1.2.5.1.2 "><p id="p6397173282519"><a name="p6397173282519"></a><a name="p6397173282519"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.39%" headers="mcps1.2.5.1.3 "><p id="p52372052319"><a name="p52372052319"></a><a name="p52372052319"></a>Long</p>
    </td>
    <td class="cellrowborder" valign="top" width="59.519999999999996%" headers="mcps1.2.5.1.4 "><p id="p139783292519"><a name="p139783292519"></a><a name="p139783292519"></a>作业ID。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="s3afece1037ea4f62aeffb3db49b97f70"></a>

**表 2**  参数说明

<a name="table167338273210"></a>
<table><thead align="left"><tr id="row473492772112"><th class="cellrowborder" valign="top" width="21.21%" id="mcps1.2.5.1.1"><p id="p1473442722114"><a name="p1473442722114"></a><a name="p1473442722114"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="11.89%" id="mcps1.2.5.1.2"><p id="p162850283265"><a name="p162850283265"></a><a name="p162850283265"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="11.360000000000001%" id="mcps1.2.5.1.3"><p id="p1886715014454"><a name="p1886715014454"></a><a name="p1886715014454"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="55.54%" id="mcps1.2.5.1.4"><p id="p1873432716213"><a name="p1873432716213"></a><a name="p1873432716213"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row137341727132113"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p6734122720213"><a name="p6734122720213"></a><a name="p6734122720213"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p16241141810311"><a name="p16241141810311"></a><a name="p16241141810311"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p394123011411"><a name="p394123011411"></a><a name="p394123011411"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p12734427152118"><a name="p12734427152118"></a><a name="p12734427152118"></a>作业名称。长度限制：0-57个字符。</p>
</td>
</tr>
<tr id="row157341727112111"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p37343278217"><a name="p37343278217"></a><a name="p37343278217"></a>desc</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p16241121816313"><a name="p16241121816313"></a><a name="p16241121816313"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p134186214816"><a name="p134186214816"></a><a name="p134186214816"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p207341827192110"><a name="p207341827192110"></a><a name="p207341827192110"></a>作业描述。长度限制：0-512个字符。</p>
</td>
</tr>
<tr id="row16658203116445"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p621523961515"><a name="p621523961515"></a><a name="p621523961515"></a>queue_name</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p1721515390153"><a name="p1721515390153"></a><a name="p1721515390153"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p82151339141519"><a name="p82151339141519"></a><a name="p82151339141519"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p821553918157"><a name="p821553918157"></a><a name="p821553918157"></a>队列名称。长度限制：1-128个字符。</p>
</td>
</tr>
<tr id="row573417279212"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p1773410271210"><a name="p1773410271210"></a><a name="p1773410271210"></a>cu_number</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p9285328122610"><a name="p9285328122610"></a><a name="p9285328122610"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p191902533811"><a name="p191902533811"></a><a name="p191902533811"></a><span>Integer</span></p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p157341327112113"><a name="p157341327112113"></a><a name="p157341327112113"></a>用户为作业选择的CU数量。默认值为“2”。</p>
</td>
</tr>
<tr id="row7559945576"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p1855915451171"><a name="p1855915451171"></a><a name="p1855915451171"></a>manager_cu_number</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p15285102816263"><a name="p15285102816263"></a><a name="p15285102816263"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p152915285475"><a name="p152915285475"></a><a name="p152915285475"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p1056011451171"><a name="p1056011451171"></a><a name="p1056011451171"></a>用户为作业选择的管理节点CU数量，对应为flink jobmanager数量。默认值为“1”。</p>
</td>
</tr>
<tr id="row873413275210"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p978704819454"><a name="p978704819454"></a><a name="p978704819454"></a>parallel_number</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p728517285262"><a name="p728517285262"></a><a name="p728517285262"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p14728172409"><a name="p14728172409"></a><a name="p14728172409"></a><span>Integer</span></p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p15964644992"><a name="p15964644992"></a><a name="p15964644992"></a>用户为作业选择的并发量。默认值为“1”。</p>
</td>
</tr>
<tr id="row1679750142215"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p19797100225"><a name="p19797100225"></a><a name="p19797100225"></a>log_enabled</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p228517281267"><a name="p228517281267"></a><a name="p228517281267"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p585014405335"><a name="p585014405335"></a><a name="p585014405335"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p167975032213"><a name="p167975032213"></a><a name="p167975032213"></a>是否开启作业日志。</p>
<a name="ul960951941319"></a><a name="ul960951941319"></a><ul id="ul960951941319"><li>开启：true</li><li>关闭：false</li><li>默认：false</li></ul>
</td>
</tr>
<tr id="row5797130182213"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p127987013227"><a name="p127987013227"></a><a name="p127987013227"></a>obs_bucket</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p52851928142618"><a name="p52851928142618"></a><a name="p52851928142618"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p244659164112"><a name="p244659164112"></a><a name="p244659164112"></a><span>String</span></p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p14798100122220"><a name="p14798100122220"></a><a name="p14798100122220"></a>当<span class="parmname" id="parmname829214507283"><a name="parmname829214507283"></a><a name="parmname829214507283"></a>“log_enabled”</span>为<span class="parmvalue" id="parmvalue287010219291"><a name="parmvalue287010219291"></a><a name="parmvalue287010219291"></a>“true”</span>时，用户授权保存日志的OBS路。</p>
</td>
</tr>
<tr id="row1611453494219"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p911463474212"><a name="p911463474212"></a><a name="p911463474212"></a>smn_topic</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p1228772813267"><a name="p1228772813267"></a><a name="p1228772813267"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p285034019338"><a name="p285034019338"></a><a name="p285034019338"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p211453410422"><a name="p211453410422"></a><a name="p211453410422"></a>当作业异常时，向该SMN主题推送告警信息。</p>
</td>
</tr>
<tr id="row1667713917350"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p1767811915356"><a name="p1767811915356"></a><a name="p1767811915356"></a>main_class</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p17287112813264"><a name="p17287112813264"></a><a name="p17287112813264"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p18966151111382"><a name="p18966151111382"></a><a name="p18966151111382"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p867818923519"><a name="p867818923519"></a><a name="p867818923519"></a>作业入口类。</p>
</td>
</tr>
<tr id="row1567815917356"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p1067811920359"><a name="p1067811920359"></a><a name="p1067811920359"></a>entrypoint_args</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p182871828172619"><a name="p182871828172619"></a><a name="p182871828172619"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p1696618119384"><a name="p1696618119384"></a><a name="p1696618119384"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p1367814923518"><a name="p1367814923518"></a><a name="p1367814923518"></a>作业入口类参数，多个参数之间空格分隔。</p>
</td>
</tr>
<tr id="row0400711104617"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p8559173762410"><a name="p8559173762410"></a><a name="p8559173762410"></a>restart_when_exception</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p256063714247"><a name="p256063714247"></a><a name="p256063714247"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p84861029174011"><a name="p84861029174011"></a><a name="p84861029174011"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p85601437192419"><a name="p85601437192419"></a><a name="p85601437192419"></a>是否开启异常重启功能，默认值为“false”。</p>
</td>
</tr>
<tr id="row990643862714"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p8948157185118"><a name="p8948157185118"></a><a name="p8948157185118"></a>entrypoint</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p119484755116"><a name="p119484755116"></a><a name="p119484755116"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p49487710511"><a name="p49487710511"></a><a name="p49487710511"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p14948375511"><a name="p14948375511"></a><a name="p14948375511"></a>用户已上传到DLI资源管理系统的程序包名，用户自定义作业主类所在的jar包。</p>
</td>
</tr>
<tr id="row11904133882719"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p7233155624618"><a name="p7233155624618"></a><a name="p7233155624618"></a>dependency_jars</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p42331956124615"><a name="p42331956124615"></a><a name="p42331956124615"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p9233155654619"><a name="p9233155654619"></a><a name="p9233155654619"></a><span>Array of Strings</span></p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p8233135664619"><a name="p8233135664619"></a><a name="p8233135664619"></a>用户已上传到DLI资源管理系统的程序包名，用户自定义作业的其他依赖包。</p>
<p id="p19536182203415"><a name="p19536182203415"></a><a name="p19536182203415"></a>示例“myGroup/test.jar,myGroup/test1.jar”。</p>
</td>
</tr>
<tr id="row10453145518316"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p174899543309"><a name="p174899543309"></a><a name="p174899543309"></a>dependency_files</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p1548919541305"><a name="p1548919541305"></a><a name="p1548919541305"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p748975419303"><a name="p748975419303"></a><a name="p748975419303"></a><span>Array of Strings</span></p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p12748153919317"><a name="p12748153919317"></a><a name="p12748153919317"></a>用户已上传到DLI资源管理系统的资源包名，用户自定义作业的依赖文件。</p>
<p id="p948945412308"><a name="p948945412308"></a><a name="p948945412308"></a>示例："myGroup/test.cvs,myGroup/test1.csv"</p>
</td>
</tr>
<tr id="row92590405160"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p62741531828"><a name="p62741531828"></a><a name="p62741531828"></a>tm_cus</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p1827415533218"><a name="p1827415533218"></a><a name="p1827415533218"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p132740531925"><a name="p132740531925"></a><a name="p132740531925"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p9274165315217"><a name="p9274165315217"></a><a name="p9274165315217"></a>每个taskmanager的CU数，默认值为“1”。</p>
</td>
</tr>
<tr id="row1257340101614"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p122748531625"><a name="p122748531625"></a><a name="p122748531625"></a>tm_slot_num</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p1274125315210"><a name="p1274125315210"></a><a name="p1274125315210"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p1327455313218"><a name="p1327455313218"></a><a name="p1327455313218"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p4275145317210"><a name="p4275145317210"></a><a name="p4275145317210"></a>每个taskmanager的slot数，默认值为“(parallel_number*tm_cus)/(cu_number-manager_cu_number)”。</p>
</td>
</tr>
<tr id="row106081039142813"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p9514112812492"><a name="p9514112812492"></a><a name="p9514112812492"></a>feature</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p16514112824913"><a name="p16514112824913"></a><a name="p16514112824913"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p19514182854915"><a name="p19514182854915"></a><a name="p19514182854915"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p1460244195120"><a name="p1460244195120"></a><a name="p1460244195120"></a>作业特性。表示用户作业使用的Flink镜像类型。</p>
<a name="ul358410443526"></a><a name="ul358410443526"></a><ul id="ul358410443526"><li>basic：表示使用DLI提供的基础Flink镜像。</li><li>custom：表示使用用户自定义的Flink镜像。</li></ul>
</td>
</tr>
<tr id="row106081139152816"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p8515162804917"><a name="p8515162804917"></a><a name="p8515162804917"></a>flink_version</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p10515128154916"><a name="p10515128154916"></a><a name="p10515128154916"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p5515102864914"><a name="p5515102864914"></a><a name="p5515102864914"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p7413142220535"><a name="p7413142220535"></a><a name="p7413142220535"></a>Flink版本。当用户设置<span class="parmname" id="parmname846018533539"><a name="parmname846018533539"></a><a name="parmname846018533539"></a>“feature”</span>为<span class="parmvalue" id="parmvalue5322558125318"><a name="parmvalue5322558125318"></a><a name="parmvalue5322558125318"></a>“basic”</span>时，该参数生效。用户可通过与<span class="parmname" id="parmname2833151105416"><a name="parmname2833151105416"></a><a name="parmname2833151105416"></a>“feature”</span>参数配合使用，指定作业运行使用的DLI基础Flink镜像的版本。</p>
</td>
</tr>
<tr id="row16071239192819"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p2051522884917"><a name="p2051522884917"></a><a name="p2051522884917"></a>image</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p351414518540"><a name="p351414518540"></a><a name="p351414518540"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p4515928104918"><a name="p4515928104918"></a><a name="p4515928104918"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p7183123618559"><a name="p7183123618559"></a><a name="p7183123618559"></a>自定义镜像。格式为：组织名/镜像名:镜像版本。</p>
<p id="p3744101605514"><a name="p3744101605514"></a><a name="p3744101605514"></a>当用户设置<span class="parmname" id="parmname138247425555"><a name="parmname138247425555"></a><a name="parmname138247425555"></a>“feature”</span>为<span class="parmvalue" id="parmvalue2059854718551"><a name="parmvalue2059854718551"></a><a name="parmvalue2059854718551"></a>“custom”</span>时，该参数生效。用户可通过与<span class="parmname" id="parmname9777102175614"><a name="parmname9777102175614"></a><a name="parmname9777102175614"></a>“feature”</span>参数配合使用，指定作业运行使用自定义的Flink镜像。关于如何使用自定义镜像，请参考《<a href="https://support.huaweicloud.com/usermanual-dli/dli_01_0494.html" target="_blank" rel="noopener noreferrer">数据湖探索用户指南</a>》。</p>
</td>
</tr>
<tr id="row10334442111816"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p2335124251810"><a name="p2335124251810"></a><a name="p2335124251810"></a>resume_checkpoint</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p173354422187"><a name="p173354422187"></a><a name="p173354422187"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p113357429186"><a name="p113357429186"></a><a name="p113357429186"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p233519428187"><a name="p233519428187"></a><a name="p233519428187"></a>异常重启是否从checkpoint恢复。</p>
</td>
</tr>
<tr id="row1335174201818"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p3543245162311"><a name="p3543245162311"></a><a name="p3543245162311"></a>resume_max_num</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p9541245182312"><a name="p9541245182312"></a><a name="p9541245182312"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p185409459238"><a name="p185409459238"></a><a name="p185409459238"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p1549119459232"><a name="p1549119459232"></a><a name="p1549119459232"></a>异常重试最大次数，单位：次/小时。取值范围：-1或大于0。默认值为“-1”，表示无限次数。</p>
</td>
</tr>
<tr id="row8336174231812"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p1336124261814"><a name="p1336124261814"></a><a name="p1336124261814"></a>checkpoint_path</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p153361942171813"><a name="p153361942171813"></a><a name="p153361942171813"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p73361242191816"><a name="p73361242191816"></a><a name="p73361242191816"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p633644216183"><a name="p633644216183"></a><a name="p633644216183"></a>用户Jar中checkpoint的储存地址，不同作业路径需要保持不同。</p>
</td>
</tr>
<tr id="row173425118576"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.5.1.1 "><p id="p95362034690"><a name="p95362034690"></a><a name="p95362034690"></a>runtime_config</p>
</td>
<td class="cellrowborder" valign="top" width="11.89%" headers="mcps1.2.5.1.2 "><p id="p165376345912"><a name="p165376345912"></a><a name="p165376345912"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.360000000000001%" headers="mcps1.2.5.1.3 "><p id="p25373349919"><a name="p25373349919"></a><a name="p25373349919"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.54%" headers="mcps1.2.5.1.4 "><p id="p1153712346915"><a name="p1153712346915"></a><a name="p1153712346915"></a>Flink作业运行时自定义优化参数。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="se2bf80cdb76541308f69f258ea4b1bd6"></a>

**表 3**  响应参数说明

<a name="t5995d65f65ba4ebca8606202112b407e"></a>
<table><thead align="left"><tr id="ra7acea51e4b4437e917d21fe99f130a3"><th class="cellrowborder" valign="top" width="16.439999999999998%" id="mcps1.2.5.1.1"><p id="a5af940f2267747ef871c67c86a0be82e"><a name="a5af940f2267747ef871c67c86a0be82e"></a><a name="a5af940f2267747ef871c67c86a0be82e"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="15.370000000000001%" id="mcps1.2.5.1.2"><p id="abcfbd3a651704d539626f3a41cc744f5"><a name="abcfbd3a651704d539626f3a41cc744f5"></a><a name="abcfbd3a651704d539626f3a41cc744f5"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="13.86%" id="mcps1.2.5.1.3"><p id="a2351d8d266444ad3ad1c09540d6d81cc"><a name="a2351d8d266444ad3ad1c09540d6d81cc"></a><a name="a2351d8d266444ad3ad1c09540d6d81cc"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="54.33%" id="mcps1.2.5.1.4"><p id="af7ea6a3f59844bdf99d51e90d570be4c"><a name="af7ea6a3f59844bdf99d51e90d570be4c"></a><a name="af7ea6a3f59844bdf99d51e90d570be4c"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row2418154742"><td class="cellrowborder" valign="top" width="16.439999999999998%" headers="mcps1.2.5.1.1 "><p id="p10253165219311"><a name="p10253165219311"></a><a name="p10253165219311"></a>is_success</p>
</td>
<td class="cellrowborder" valign="top" width="15.370000000000001%" headers="mcps1.2.5.1.2 "><p id="p8253115273111"><a name="p8253115273111"></a><a name="p8253115273111"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="13.86%" headers="mcps1.2.5.1.3 "><p id="p7253352153116"><a name="p7253352153116"></a><a name="p7253352153116"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="54.33%" headers="mcps1.2.5.1.4 "><p id="p8253152103110"><a name="p8253152103110"></a><a name="p8253152103110"></a>执行请求是否成功。“true”表示请求执行成功。</p>
</td>
</tr>
<tr id="row64180541741"><td class="cellrowborder" valign="top" width="16.439999999999998%" headers="mcps1.2.5.1.1 "><p id="a4aba020b918e457a8a3d15e7ebaeb20d"><a name="a4aba020b918e457a8a3d15e7ebaeb20d"></a><a name="a4aba020b918e457a8a3d15e7ebaeb20d"></a>message</p>
</td>
<td class="cellrowborder" valign="top" width="15.370000000000001%" headers="mcps1.2.5.1.2 "><p id="p11374111319494"><a name="p11374111319494"></a><a name="p11374111319494"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="13.86%" headers="mcps1.2.5.1.3 "><p id="ac85edc0a27d044b0ad524a4124e59e4c"><a name="ac85edc0a27d044b0ad524a4124e59e4c"></a><a name="ac85edc0a27d044b0ad524a4124e59e4c"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="54.33%" headers="mcps1.2.5.1.4 "><p id="ac087aec9dfcc407ba244ad3e96b23257"><a name="ac087aec9dfcc407ba244ad3e96b23257"></a><a name="ac087aec9dfcc407ba244ad3e96b23257"></a>消息内容。</p>
</td>
</tr>
<tr id="row13575616163215"><td class="cellrowborder" valign="top" width="16.439999999999998%" headers="mcps1.2.5.1.1 "><p id="p1457691643219"><a name="p1457691643219"></a><a name="p1457691643219"></a>job</p>
</td>
<td class="cellrowborder" valign="top" width="15.370000000000001%" headers="mcps1.2.5.1.2 "><p id="p3576151610328"><a name="p3576151610328"></a><a name="p3576151610328"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="13.86%" headers="mcps1.2.5.1.3 "><p id="p5576316153211"><a name="p5576316153211"></a><a name="p5576316153211"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="54.33%" headers="mcps1.2.5.1.4 "><p id="p15761162327"><a name="p15761162327"></a><a name="p15761162327"></a>作业更新信息。具体请参考<a href="#table128621016345">表4</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  job参数说明

<a name="table128621016345"></a>
<table><thead align="left"><tr id="row88741014347"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p1487161063413"><a name="p1487161063413"></a><a name="p1487161063413"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="15%" id="mcps1.2.5.1.2"><p id="p1287810113413"><a name="p1287810113413"></a><a name="p1287810113413"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="12.57%" id="mcps1.2.5.1.3"><p id="p128817104349"><a name="p128817104349"></a><a name="p128817104349"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="47.43%" id="mcps1.2.5.1.4"><p id="p1788151013347"><a name="p1788151013347"></a><a name="p1788151013347"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row2090131017345"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1905104345"><a name="p1905104345"></a><a name="p1905104345"></a>update_time</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.2 "><p id="p89016106346"><a name="p89016106346"></a><a name="p89016106346"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.57%" headers="mcps1.2.5.1.3 "><p id="p4901103344"><a name="p4901103344"></a><a name="p4901103344"></a>Long</p>
</td>
<td class="cellrowborder" valign="top" width="47.43%" headers="mcps1.2.5.1.4 "><p id="p59012101344"><a name="p59012101344"></a><a name="p59012101344"></a>作业更新时间，单位为毫秒。</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section931494182219"></a>

-   请求样例

    ```
    {
        "name": "test1",
        "desc": "job for test",
        "job_type": "flink_jar_job",
        "queue_name": "testQueue",
        "manager_cu_number": 1,
        "cu_number": 2,
        "parallel_number": 1,
        "log_enabled": false,
        "main_class": "org.apache.flink.examples.streaming.JavaQueueStream",
        "restart_when_exception": false,
        "entrypoint": "FemaleInfoCollec.jar",
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
      "message": "更新flink作业成功",
      "job": { 
         "update_time": 1516952770835 
      } 
    }
    ```


## 状态码<a name="s1b495ba11cd9411c9ad2ee50103334a7"></a>

状态码如[表5](#t43c1f1c0ba344f4cbcb270953d9cca2a)所示。

**表 5**  状态码

<a name="t43c1f1c0ba344f4cbcb270953d9cca2a"></a>
<table><thead align="left"><tr id="r2ad0f008ce2248a1800a3e8b77226a56"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.3.1.1"><p id="afa33b7f5b0ac4d008ebcf6493f629b24"><a name="afa33b7f5b0ac4d008ebcf6493f629b24"></a><a name="afa33b7f5b0ac4d008ebcf6493f629b24"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="70%" id="mcps1.2.3.1.2"><p id="af801170b350b4f8ba3b575c7ddb8b13e"><a name="af801170b350b4f8ba3b575c7ddb8b13e"></a><a name="af801170b350b4f8ba3b575c7ddb8b13e"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="r0b449b1d3b8c498ea3e6cce16c80a14c"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="a8c63a97e3bad402ebaead0bd99cad632"><a name="a8c63a97e3bad402ebaead0bd99cad632"></a><a name="a8c63a97e3bad402ebaead0bd99cad632"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="af86844c7bb364c48b6300df1af164af2"><a name="af86844c7bb364c48b6300df1af164af2"></a><a name="af86844c7bb364c48b6300df1af164af2"></a>更新Flink自定义作业成功。</p>
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

