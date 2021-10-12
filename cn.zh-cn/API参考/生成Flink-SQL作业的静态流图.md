# 生成Flink SQL作业的静态流图<a name="dli_02_0316"></a>

## 功能介绍<a name="s89ff8bc59cba4c3b94dc17e85c8fa1ea"></a>

该API用于生成flink SQL作业的静态流图。

## 调试<a name="section556523314214"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=DLI&api=CreateStreamGraph)中调试该接口。

## URI<a name="sef21e3efc2a44a84a03adad33a1ae006"></a>

-   URI格式

    POST /v3/\{project\_id\}/streaming/jobs/\{job\_id\}/gen-graph

-   参数说明

    **表 1**  URI参数说明

    <a name="t219b031199884ac1bb9e91158ddc9efb"></a>
    <table><thead align="left"><tr id="r04005eeda24e4db9b06516450d4d56af"><th class="cellrowborder" valign="top" width="11.63%" id="mcps1.2.5.1.1"><p id="a80847df5e5dc448caa46a2ff258fa2c4"><a name="a80847df5e5dc448caa46a2ff258fa2c4"></a><a name="a80847df5e5dc448caa46a2ff258fa2c4"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="10.979999999999999%" id="mcps1.2.5.1.2"><p id="af54fc16087b049c98f748c1a2faace17"><a name="af54fc16087b049c98f748c1a2faace17"></a><a name="af54fc16087b049c98f748c1a2faace17"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="11.76%" id="mcps1.2.5.1.3"><p id="p201051414144319"><a name="p201051414144319"></a><a name="p201051414144319"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="65.63%" id="mcps1.2.5.1.4"><p id="a484a3e0ce14846799c727ccbd4075d6c"><a name="a484a3e0ce14846799c727ccbd4075d6c"></a><a name="a484a3e0ce14846799c727ccbd4075d6c"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="r8022e11be3f54ad290cf8c848a56a550"><td class="cellrowborder" valign="top" width="11.63%" headers="mcps1.2.5.1.1 "><p id="p1262440203315"><a name="p1262440203315"></a><a name="p1262440203315"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.979999999999999%" headers="mcps1.2.5.1.2 "><p id="p1016041415356"><a name="p1016041415356"></a><a name="p1016041415356"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.76%" headers="mcps1.2.5.1.3 "><p id="p1710515149436"><a name="p1710515149436"></a><a name="p1710515149436"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="65.63%" headers="mcps1.2.5.1.4 "><p id="p1768719515356"><a name="p1768719515356"></a><a name="p1768719515356"></a>项目编号，用于资源隔离。获取方式请参考<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="s3afece1037ea4f62aeffb3db49b97f70"></a>

**表 2**  请求参数说明

<a name="table11209133616498"></a>
<table><thead align="left"><tr id="row1621093613496"><th class="cellrowborder" valign="top" width="23.52%" id="mcps1.2.5.1.1"><p id="p82102036194919"><a name="p82102036194919"></a><a name="p82102036194919"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="12.33%" id="mcps1.2.5.1.2"><p id="p17210143634912"><a name="p17210143634912"></a><a name="p17210143634912"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="14.44%" id="mcps1.2.5.1.3"><p id="p15210436174916"><a name="p15210436174916"></a><a name="p15210436174916"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="49.71%" id="mcps1.2.5.1.4"><p id="p62101436144911"><a name="p62101436144911"></a><a name="p62101436144911"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row9210193614919"><td class="cellrowborder" valign="top" width="23.52%" headers="mcps1.2.5.1.1 "><p id="p1813915305540"><a name="p1813915305540"></a><a name="p1813915305540"></a><span>sql_body</span></p>
</td>
<td class="cellrowborder" valign="top" width="12.33%" headers="mcps1.2.5.1.2 "><p id="p12107369490"><a name="p12107369490"></a><a name="p12107369490"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.44%" headers="mcps1.2.5.1.3 "><p id="p14210736184920"><a name="p14210736184920"></a><a name="p14210736184920"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.71%" headers="mcps1.2.5.1.4 "><p id="p8501636105418"><a name="p8501636105418"></a><a name="p8501636105418"></a>SQL。</p>
</td>
</tr>
<tr id="row68519283358"><td class="cellrowborder" valign="top" width="23.52%" headers="mcps1.2.5.1.1 "><p id="p398143055414"><a name="p398143055414"></a><a name="p398143055414"></a><span>cu_number</span></p>
</td>
<td class="cellrowborder" valign="top" width="12.33%" headers="mcps1.2.5.1.2 "><p id="p128531028143515"><a name="p128531028143515"></a><a name="p128531028143515"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.44%" headers="mcps1.2.5.1.3 "><p id="p20853112863510"><a name="p20853112863510"></a><a name="p20853112863510"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="49.71%" headers="mcps1.2.5.1.4 "><p id="p097113575418"><a name="p097113575418"></a><a name="p097113575418"></a>CU总数。</p>
</td>
</tr>
<tr id="row129641482552"><td class="cellrowborder" valign="top" width="23.52%" headers="mcps1.2.5.1.1 "><p id="p209655488551"><a name="p209655488551"></a><a name="p209655488551"></a><span>manager</span>_<span>cu_number</span></p>
</td>
<td class="cellrowborder" valign="top" width="12.33%" headers="mcps1.2.5.1.2 "><p id="p1596544825513"><a name="p1596544825513"></a><a name="p1596544825513"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.44%" headers="mcps1.2.5.1.3 "><p id="p1596554816550"><a name="p1596554816550"></a><a name="p1596554816550"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="49.71%" headers="mcps1.2.5.1.4 "><p id="p4965348135511"><a name="p4965348135511"></a><a name="p4965348135511"></a>管理单元CU数。</p>
</td>
</tr>
<tr id="row7965204825518"><td class="cellrowborder" valign="top" width="23.52%" headers="mcps1.2.5.1.1 "><p id="p254015503566"><a name="p254015503566"></a><a name="p254015503566"></a>parallel_number</p>
</td>
<td class="cellrowborder" valign="top" width="12.33%" headers="mcps1.2.5.1.2 "><p id="p165419508567"><a name="p165419508567"></a><a name="p165419508567"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.44%" headers="mcps1.2.5.1.3 "><p id="p89659481550"><a name="p89659481550"></a><a name="p89659481550"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="49.71%" headers="mcps1.2.5.1.4 "><p id="p3965164812554"><a name="p3965164812554"></a><a name="p3965164812554"></a>最大并行度。</p>
</td>
</tr>
<tr id="row13632219574"><td class="cellrowborder" valign="top" width="23.52%" headers="mcps1.2.5.1.1 "><p id="p1928953514572"><a name="p1928953514572"></a><a name="p1928953514572"></a>tm_cus</p>
</td>
<td class="cellrowborder" valign="top" width="12.33%" headers="mcps1.2.5.1.2 "><p id="p252615525910"><a name="p252615525910"></a><a name="p252615525910"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.44%" headers="mcps1.2.5.1.3 "><p id="p1941320175812"><a name="p1941320175812"></a><a name="p1941320175812"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="49.71%" headers="mcps1.2.5.1.4 "><p id="p10289123535718"><a name="p10289123535718"></a><a name="p10289123535718"></a>单个taskManagerCU数量。</p>
</td>
</tr>
<tr id="row177162213575"><td class="cellrowborder" valign="top" width="23.52%" headers="mcps1.2.5.1.1 "><p id="p1929033505710"><a name="p1929033505710"></a><a name="p1929033505710"></a>tm_slot_num</p>
</td>
<td class="cellrowborder" valign="top" width="12.33%" headers="mcps1.2.5.1.2 "><p id="p1526254593"><a name="p1526254593"></a><a name="p1526254593"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.44%" headers="mcps1.2.5.1.3 "><p id="p141120115819"><a name="p141120115819"></a><a name="p141120115819"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="49.71%" headers="mcps1.2.5.1.4 "><p id="p1344620185590"><a name="p1344620185590"></a><a name="p1344620185590"></a>单个taskManager Slot数量。</p>
</td>
</tr>
<tr id="row7852217574"><td class="cellrowborder" valign="top" width="23.52%" headers="mcps1.2.5.1.1 "><p id="p1429013565718"><a name="p1429013565718"></a><a name="p1429013565718"></a>operator_config</p>
</td>
<td class="cellrowborder" valign="top" width="12.33%" headers="mcps1.2.5.1.2 "><p id="p652610517591"><a name="p652610517591"></a><a name="p652610517591"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.44%" headers="mcps1.2.5.1.3 "><p id="p1290235175713"><a name="p1290235175713"></a><a name="p1290235175713"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.71%" headers="mcps1.2.5.1.4 "><p id="p165355296594"><a name="p165355296594"></a><a name="p165355296594"></a>算子的配置。</p>
</td>
</tr>
<tr id="row88172216571"><td class="cellrowborder" valign="top" width="23.52%" headers="mcps1.2.5.1.1 "><p id="p1529017351575"><a name="p1529017351575"></a><a name="p1529017351575"></a>static_estimator</p>
</td>
<td class="cellrowborder" valign="top" width="12.33%" headers="mcps1.2.5.1.2 "><p id="p6287188590"><a name="p6287188590"></a><a name="p6287188590"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.44%" headers="mcps1.2.5.1.3 "><p id="p22901359579"><a name="p22901359579"></a><a name="p22901359579"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="49.71%" headers="mcps1.2.5.1.4 "><p id="p1947193825916"><a name="p1947193825916"></a><a name="p1947193825916"></a>是否静态资源预估。</p>
</td>
</tr>
<tr id="row136102051185718"><td class="cellrowborder" valign="top" width="23.52%" headers="mcps1.2.5.1.1 "><p id="p5819026586"><a name="p5819026586"></a><a name="p5819026586"></a>job_type</p>
</td>
<td class="cellrowborder" valign="top" width="12.33%" headers="mcps1.2.5.1.2 "><p id="p5287483591"><a name="p5287483591"></a><a name="p5287483591"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.44%" headers="mcps1.2.5.1.3 "><p id="p1081918219588"><a name="p1081918219588"></a><a name="p1081918219588"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.71%" headers="mcps1.2.5.1.4 "><p id="p138195218580"><a name="p138195218580"></a><a name="p138195218580"></a>作业类型。只支持flink_opensource_sql_job类型作业。</p>
</td>
</tr>
<tr id="row9610451125713"><td class="cellrowborder" valign="top" width="23.52%" headers="mcps1.2.5.1.1 "><p id="p148192025580"><a name="p148192025580"></a><a name="p148192025580"></a>graph_type</p>
</td>
<td class="cellrowborder" valign="top" width="12.33%" headers="mcps1.2.5.1.2 "><p id="p1287158125917"><a name="p1287158125917"></a><a name="p1287158125917"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.44%" headers="mcps1.2.5.1.3 "><p id="p181982185811"><a name="p181982185811"></a><a name="p181982185811"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.71%" headers="mcps1.2.5.1.4 "><p id="p134625013501"><a name="p134625013501"></a><a name="p134625013501"></a>流图类型。当前支持以下两种流图类型。</p>
<a name="ul14347142155017"></a><a name="ul14347142155017"></a><ul id="ul14347142155017"><li>简化流图：simple_graph</li><li>静态流图：job_graph</li></ul>
</td>
</tr>
<tr id="row64561624115312"><td class="cellrowborder" valign="top" width="23.52%" headers="mcps1.2.5.1.1 "><p id="p432792704815"><a name="p432792704815"></a><a name="p432792704815"></a>static_estimator_config</p>
</td>
<td class="cellrowborder" valign="top" width="12.33%" headers="mcps1.2.5.1.2 "><p id="p1432702717489"><a name="p1432702717489"></a><a name="p1432702717489"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.44%" headers="mcps1.2.5.1.3 "><p id="p12327182716481"><a name="p12327182716481"></a><a name="p12327182716481"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.71%" headers="mcps1.2.5.1.4 "><p id="p1732815276486"><a name="p1732815276486"></a><a name="p1732815276486"></a>每个算子的流量/命中率配置，json格式的字符串。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="se2bf80cdb76541308f69f258ea4b1bd6"></a>

**表 3**  响应参数说明

<a name="t5995d65f65ba4ebca8606202112b407e"></a>
<table><thead align="left"><tr id="ra7acea51e4b4437e917d21fe99f130a3"><th class="cellrowborder" valign="top" width="14.84%" id="mcps1.2.5.1.1"><p id="a5af940f2267747ef871c67c86a0be82e"><a name="a5af940f2267747ef871c67c86a0be82e"></a><a name="a5af940f2267747ef871c67c86a0be82e"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="12.47%" id="mcps1.2.5.1.2"><p id="abcfbd3a651704d539626f3a41cc744f5"><a name="abcfbd3a651704d539626f3a41cc744f5"></a><a name="abcfbd3a651704d539626f3a41cc744f5"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="17.23%" id="mcps1.2.5.1.3"><p id="a2351d8d266444ad3ad1c09540d6d81cc"><a name="a2351d8d266444ad3ad1c09540d6d81cc"></a><a name="a2351d8d266444ad3ad1c09540d6d81cc"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="55.46%" id="mcps1.2.5.1.4"><p id="af7ea6a3f59844bdf99d51e90d570be4c"><a name="af7ea6a3f59844bdf99d51e90d570be4c"></a><a name="af7ea6a3f59844bdf99d51e90d570be4c"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="rca1bdb55f4dc497ca8fee7537232f274"><td class="cellrowborder" valign="top" width="14.84%" headers="mcps1.2.5.1.1 "><p id="p1045315113248"><a name="p1045315113248"></a><a name="p1045315113248"></a>is_success</p>
</td>
<td class="cellrowborder" valign="top" width="12.47%" headers="mcps1.2.5.1.2 "><p id="p15453131112419"><a name="p15453131112419"></a><a name="p15453131112419"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.23%" headers="mcps1.2.5.1.3 "><p id="p6453411132414"><a name="p6453411132414"></a><a name="p6453411132414"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="55.46%" headers="mcps1.2.5.1.4 "><p id="p05081222182420"><a name="p05081222182420"></a><a name="p05081222182420"></a>执行请求是否成功。“true”表示请求执行成功。</p>
</td>
</tr>
<tr id="r3900d023a26e45dea9a0ad9dd60d8ab1"><td class="cellrowborder" valign="top" width="14.84%" headers="mcps1.2.5.1.1 "><p id="p645351113242"><a name="p645351113242"></a><a name="p645351113242"></a>message</p>
</td>
<td class="cellrowborder" valign="top" width="12.47%" headers="mcps1.2.5.1.2 "><p id="p1445410112249"><a name="p1445410112249"></a><a name="p1445410112249"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.23%" headers="mcps1.2.5.1.3 "><p id="p1845441117241"><a name="p1845441117241"></a><a name="p1845441117241"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.46%" headers="mcps1.2.5.1.4 "><p id="p1573323415243"><a name="p1573323415243"></a><a name="p1573323415243"></a>系统提示信息，执行成功时，信息可能为空。</p>
</td>
</tr>
<tr id="row26371718116"><td class="cellrowborder" valign="top" width="14.84%" headers="mcps1.2.5.1.1 "><p id="p26167121818"><a name="p26167121818"></a><a name="p26167121818"></a>error_code</p>
</td>
<td class="cellrowborder" valign="top" width="12.47%" headers="mcps1.2.5.1.2 "><p id="p261671219110"><a name="p261671219110"></a><a name="p261671219110"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.23%" headers="mcps1.2.5.1.3 "><p id="p196164123114"><a name="p196164123114"></a><a name="p196164123114"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.46%" headers="mcps1.2.5.1.4 "><p id="p106381211319"><a name="p106381211319"></a><a name="p106381211319"></a>错误码。</p>
</td>
</tr>
<tr id="row21031568411"><td class="cellrowborder" valign="top" width="14.84%" headers="mcps1.2.5.1.1 "><p id="p64152422112"><a name="p64152422112"></a><a name="p64152422112"></a>stream_graph</p>
</td>
<td class="cellrowborder" valign="top" width="12.47%" headers="mcps1.2.5.1.2 "><p id="p1520313541617"><a name="p1520313541617"></a><a name="p1520313541617"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.23%" headers="mcps1.2.5.1.3 "><p id="p9415542818"><a name="p9415542818"></a><a name="p9415542818"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.46%" headers="mcps1.2.5.1.4 "><p id="p1741684216113"><a name="p1741684216113"></a><a name="p1741684216113"></a>静态流图的描述信息。</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section339884412434"></a>

-   请求样例

    ```
    {
       "cu_number": 4,
       "manager_cu_number": 1,
       "parallel_number": 4,
       "tm_cus": 1,
       "tm_slot_num": 1,
       "sql_body": "",
       "operator_config": "",
       "static_estimator": true,
       "job_type": "flink_opensource_sql_job",
       "graph_type": "job_graph"
     }
    ```

-   响应样例

    ```
    {
        "is_success": true,
        "message": "",
        "error_code": "",
        "stream_graph": "{\n  \"nodes\" : [ {\n    \"id\" : 1,\n    \"operator_id\" : \"bc764cd8ddf7a0cff126f51c16239658\",\n    \"type\" : \"Source\",\n    
     \"contents\" : \"kafkaSource\",\n    \"parallelism\" : 1\n  }, {\n    \"id\" : 2,\n    \"operator_id\" : \"0a448493b4782967b150582570326227\",\n    \"type\" : \"select\",\n    \"contents\" : \"car_id, car_owner, car_brand, car_speed\",\n    \"parallelism\" : 1,\n    \"predecessors\" : [ {\n      \"id\" : 1\n    } ]\n  }, {\n    \"id\" : 4,\n    \"operator_id\" : \"6d2677a0ecc3fd8df0b72ec675edf8f4\",\n    \"type\" : \"Sink\",\n    \"contents\" : \"kafkaSink\",\n    \"parallelism\" : 1,\n    \"predecessors\" : [ {\n      \"id\" : 2\n    } ]\n  } ]\n}"
    }
    ```


## 状态码<a name="s1b495ba11cd9411c9ad2ee50103334a7"></a>

状态码如[表4](#t43c1f1c0ba344f4cbcb270953d9cca2a)所示。

**表 4**  状态码

<a name="t43c1f1c0ba344f4cbcb270953d9cca2a"></a>
<table><thead align="left"><tr id="r2ad0f008ce2248a1800a3e8b77226a56"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.3.1.1"><p id="afa33b7f5b0ac4d008ebcf6493f629b24"><a name="afa33b7f5b0ac4d008ebcf6493f629b24"></a><a name="afa33b7f5b0ac4d008ebcf6493f629b24"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="70%" id="mcps1.2.3.1.2"><p id="af801170b350b4f8ba3b575c7ddb8b13e"><a name="af801170b350b4f8ba3b575c7ddb8b13e"></a><a name="af801170b350b4f8ba3b575c7ddb8b13e"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="r0b449b1d3b8c498ea3e6cce16c80a14c"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="a8c63a97e3bad402ebaead0bd99cad632"><a name="a8c63a97e3bad402ebaead0bd99cad632"></a><a name="a8c63a97e3bad402ebaead0bd99cad632"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="af86844c7bb364c48b6300df1af164af2"><a name="af86844c7bb364c48b6300df1af164af2"></a><a name="af86844c7bb364c48b6300df1af164af2"></a>操作成功。</p>
</td>
</tr>
<tr id="row1232118139110"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p14321113711"><a name="p14321113711"></a><a name="p14321113711"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p1832191314113"><a name="p1832191314113"></a><a name="p1832191314113"></a>输入参数无效。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section13596141025715"></a>

调用接口出错后，将不会返回上述结果，而是返回错误码和错误信息，更多介绍请参见[错误码](错误码.md)。

