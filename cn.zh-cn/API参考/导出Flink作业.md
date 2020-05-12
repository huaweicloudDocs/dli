# 导出Flink作业<a name="dli_02_0254"></a>

## 功能介绍<a name="s89ff8bc59cba4c3b94dc17e85c8fa1ea"></a>

导出Flink作业数据。

## URI<a name="sef21e3efc2a44a84a03adad33a1ae006"></a>

-   URI格式

    POST /v1.0/\{project\_id\}/streaming/jobs/export

-   参数说明

    **表 1**  URI参数说明

    <a name="t219b031199884ac1bb9e91158ddc9efb"></a>
    <table><thead align="left"><tr id="r04005eeda24e4db9b06516450d4d56af"><th class="cellrowborder" valign="top" width="12.58%" id="mcps1.2.4.1.1"><p id="a80847df5e5dc448caa46a2ff258fa2c4"><a name="a80847df5e5dc448caa46a2ff258fa2c4"></a><a name="a80847df5e5dc448caa46a2ff258fa2c4"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="11.87%" id="mcps1.2.4.1.2"><p id="af54fc16087b049c98f748c1a2faace17"><a name="af54fc16087b049c98f748c1a2faace17"></a><a name="af54fc16087b049c98f748c1a2faace17"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="75.55%" id="mcps1.2.4.1.3"><p id="a484a3e0ce14846799c727ccbd4075d6c"><a name="a484a3e0ce14846799c727ccbd4075d6c"></a><a name="a484a3e0ce14846799c727ccbd4075d6c"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="r8022e11be3f54ad290cf8c848a56a550"><td class="cellrowborder" valign="top" width="12.58%" headers="mcps1.2.4.1.1 "><p id="p1262440203315"><a name="p1262440203315"></a><a name="p1262440203315"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.87%" headers="mcps1.2.4.1.2 "><p id="p1016041415356"><a name="p1016041415356"></a><a name="p1016041415356"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="75.55%" headers="mcps1.2.4.1.3 "><p id="p1768719515356"><a name="p1768719515356"></a><a name="p1768719515356"></a>项目编号，用于资源隔离。获取方式请参考<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="s3afece1037ea4f62aeffb3db49b97f70"></a>

-   请求样例

    ```
    {
        "obs_dir": "obs-test",
        "is_selected": true,
        "job_selected": [100]
    }
    ```

-   参数说明

    **表 2**  请求参数说明

    <a name="table11209133616498"></a>
    <table><thead align="left"><tr id="row1621093613496"><th class="cellrowborder" valign="top" width="15.58%" id="mcps1.2.5.1.1"><p id="p82102036194919"><a name="p82102036194919"></a><a name="p82102036194919"></a>参数名</p>
    </th>
    <th class="cellrowborder" valign="top" width="11.82%" id="mcps1.2.5.1.2"><p id="p17210143634912"><a name="p17210143634912"></a><a name="p17210143634912"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.83%" id="mcps1.2.5.1.3"><p id="p15210436174916"><a name="p15210436174916"></a><a name="p15210436174916"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="59.77%" id="mcps1.2.5.1.4"><p id="p62101436144911"><a name="p62101436144911"></a><a name="p62101436144911"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row9210193614919"><td class="cellrowborder" valign="top" width="15.58%" headers="mcps1.2.5.1.1 "><p id="p122101936164915"><a name="p122101936164915"></a><a name="p122101936164915"></a><span>obs_dir</span></p>
    </td>
    <td class="cellrowborder" valign="top" width="11.82%" headers="mcps1.2.5.1.2 "><p id="p12107369490"><a name="p12107369490"></a><a name="p12107369490"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.83%" headers="mcps1.2.5.1.3 "><p id="p14210736184920"><a name="p14210736184920"></a><a name="p14210736184920"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="59.77%" headers="mcps1.2.5.1.4 "><p id="p14949172263716"><a name="p14949172263716"></a><a name="p14949172263716"></a>OBS路径，用于保存导出的作业文件。</p>
    </td>
    </tr>
    <tr id="row68519283358"><td class="cellrowborder" valign="top" width="15.58%" headers="mcps1.2.5.1.1 "><p id="p58539281359"><a name="p58539281359"></a><a name="p58539281359"></a><span>is_selected</span></p>
    </td>
    <td class="cellrowborder" valign="top" width="11.82%" headers="mcps1.2.5.1.2 "><p id="p128531028143515"><a name="p128531028143515"></a><a name="p128531028143515"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.83%" headers="mcps1.2.5.1.3 "><p id="p20853112863510"><a name="p20853112863510"></a><a name="p20853112863510"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="59.77%" headers="mcps1.2.5.1.4 "><p id="p4149102623818"><a name="p4149102623818"></a><a name="p4149102623818"></a>是否导出指定的作业。</p>
    </td>
    </tr>
    <tr id="row038520335354"><td class="cellrowborder" valign="top" width="15.58%" headers="mcps1.2.5.1.1 "><p id="p173851233103518"><a name="p173851233103518"></a><a name="p173851233103518"></a><span>job_selected</span></p>
    </td>
    <td class="cellrowborder" valign="top" width="11.82%" headers="mcps1.2.5.1.2 "><p id="p1638583313358"><a name="p1638583313358"></a><a name="p1638583313358"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.83%" headers="mcps1.2.5.1.3 "><p id="p438663353517"><a name="p438663353517"></a><a name="p438663353517"></a>[Long]</p>
    </td>
    <td class="cellrowborder" valign="top" width="59.77%" headers="mcps1.2.5.1.4 "><p id="p1976111153391"><a name="p1976111153391"></a><a name="p1976111153391"></a>当<span class="parmname" id="parmname14960133320395"><a name="parmname14960133320395"></a><a name="parmname14960133320395"></a>“is_selected”</span>为<span class="parmvalue" id="parmvalue1270884343920"><a name="parmvalue1270884343920"></a><a name="parmvalue1270884343920"></a>“true”</span>时，该参数是待导出作业的ID集合。</p>
    <div class="note" id="note7829151619401"><a name="note7829151619401"></a><a name="note7829151619401"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p78401116184010"><a name="p78401116184010"></a><a name="p78401116184010"></a>当<span class="parmname" id="parmname168173232401"><a name="parmname168173232401"></a><a name="parmname168173232401"></a>“is_selected”</span>为<span class="parmvalue" id="parmvalue98181223134016"><a name="parmvalue98181223134016"></a><a name="parmvalue98181223134016"></a>“true”</span>时，该参数为必选。</p>
    </div></div>
    </td>
    </tr>
    </tbody>
    </table>


## 响应消息<a name="se2bf80cdb76541308f69f258ea4b1bd6"></a>

-   响应样例

    ```
    {
        "is_success": true,
        "message": "导出作业成功",
        "zip_files": ["obs-test/aggregate_1582677879475.zip"]
    }
    ```

-   参数说明

    **表 3**  响应参数说明

    <a name="t5995d65f65ba4ebca8606202112b407e"></a>
    <table><thead align="left"><tr id="ra7acea51e4b4437e917d21fe99f130a3"><th class="cellrowborder" valign="top" width="14.84%" id="mcps1.2.5.1.1"><p id="a5af940f2267747ef871c67c86a0be82e"><a name="a5af940f2267747ef871c67c86a0be82e"></a><a name="a5af940f2267747ef871c67c86a0be82e"></a>参数名</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.47%" id="mcps1.2.5.1.2"><p id="abcfbd3a651704d539626f3a41cc744f5"><a name="abcfbd3a651704d539626f3a41cc744f5"></a><a name="abcfbd3a651704d539626f3a41cc744f5"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="11.51%" id="mcps1.2.5.1.3"><p id="a2351d8d266444ad3ad1c09540d6d81cc"><a name="a2351d8d266444ad3ad1c09540d6d81cc"></a><a name="a2351d8d266444ad3ad1c09540d6d81cc"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="61.18%" id="mcps1.2.5.1.4"><p id="af7ea6a3f59844bdf99d51e90d570be4c"><a name="af7ea6a3f59844bdf99d51e90d570be4c"></a><a name="af7ea6a3f59844bdf99d51e90d570be4c"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="rca1bdb55f4dc497ca8fee7537232f274"><td class="cellrowborder" valign="top" width="14.84%" headers="mcps1.2.5.1.1 "><p id="p1045315113248"><a name="p1045315113248"></a><a name="p1045315113248"></a>is_success</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.47%" headers="mcps1.2.5.1.2 "><p id="p15453131112419"><a name="p15453131112419"></a><a name="p15453131112419"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.51%" headers="mcps1.2.5.1.3 "><p id="p6453411132414"><a name="p6453411132414"></a><a name="p6453411132414"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="61.18%" headers="mcps1.2.5.1.4 "><p id="p05081222182420"><a name="p05081222182420"></a><a name="p05081222182420"></a>执行请求是否成功。“true”表示请求执行成功。</p>
    </td>
    </tr>
    <tr id="r3900d023a26e45dea9a0ad9dd60d8ab1"><td class="cellrowborder" valign="top" width="14.84%" headers="mcps1.2.5.1.1 "><p id="p645351113242"><a name="p645351113242"></a><a name="p645351113242"></a>message</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.47%" headers="mcps1.2.5.1.2 "><p id="p1445410112249"><a name="p1445410112249"></a><a name="p1445410112249"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.51%" headers="mcps1.2.5.1.3 "><p id="p1845441117241"><a name="p1845441117241"></a><a name="p1845441117241"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="61.18%" headers="mcps1.2.5.1.4 "><p id="p1573323415243"><a name="p1573323415243"></a><a name="p1573323415243"></a>系统提示信息，执行成功时，信息可能为空。</p>
    </td>
    </tr>
    <tr id="row21031568411"><td class="cellrowborder" valign="top" width="14.84%" headers="mcps1.2.5.1.1 "><p id="p81041556174120"><a name="p81041556174120"></a><a name="p81041556174120"></a><span>zip_files</span></p>
    </td>
    <td class="cellrowborder" valign="top" width="12.47%" headers="mcps1.2.5.1.2 "><p id="p2010413566417"><a name="p2010413566417"></a><a name="p2010413566417"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.51%" headers="mcps1.2.5.1.3 "><p id="p1410420561419"><a name="p1410420561419"></a><a name="p1410420561419"></a>[String]</p>
    </td>
    <td class="cellrowborder" valign="top" width="61.18%" headers="mcps1.2.5.1.4 "><p id="p10807332204210"><a name="p10807332204210"></a><a name="p10807332204210"></a>导出的作业zip包文件名，保存在OBS上。</p>
    </td>
    </tr>
    </tbody>
    </table>


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
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="af86844c7bb364c48b6300df1af164af2"><a name="af86844c7bb364c48b6300df1af164af2"></a><a name="af86844c7bb364c48b6300df1af164af2"></a>导出作业成功。</p>
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

**表 5**  错误码

<a name="zh-cn_topic_0207595520_table847819307387"></a>
<table><thead align="left"><tr id="zh-cn_topic_0207595520_row2479163016383"><th class="cellrowborder" valign="top" width="16.29%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0207595520_p114796309389"><a name="zh-cn_topic_0207595520_p114796309389"></a><a name="zh-cn_topic_0207595520_p114796309389"></a>错误码</p>
</th>
<th class="cellrowborder" valign="top" width="83.71%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0207595520_p1647973053817"><a name="zh-cn_topic_0207595520_p1647973053817"></a><a name="zh-cn_topic_0207595520_p1647973053817"></a>错误信息</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0207595520_row1047920308387"><td class="cellrowborder" valign="top" width="16.29%" headers="mcps1.2.3.1.1 "><p id="p195911332456"><a name="p195911332456"></a><a name="p195911332456"></a>DLI.29001</p>
</td>
<td class="cellrowborder" valign="top" width="83.71%" headers="mcps1.2.3.1.2 "><p id="p192441956104515"><a name="p192441956104515"></a><a name="p192441956104515"></a>Failed for parse obs path</p>
</td>
</tr>
</tbody>
</table>

