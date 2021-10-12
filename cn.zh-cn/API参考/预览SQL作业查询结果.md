# 预览SQL作业查询结果<a name="dli_02_0312"></a>

## 功能介绍<a name="s25c520608f924620832c60c39296fb4f"></a>

该API用于在执行SQL查询语句的作业完成后，查看该作业执行的结果。目前仅支持查看“QUERY”类型作业的执行结果。

该API只能查看前1000条的结果记录，且不支持分页查询。若要查看全部的结果记录，需要先导出查询结果再进行查看，详细请参见[导出查询结果](导出查询结果.md)。

## 调试<a name="section556523314214"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=DLI&api=ShowJobResult)中调试该接口。

## URI<a name="s46248c92bcac4e63baf217574b85b423"></a>

-   URI格式：

    GET /v1.0/\{project\_id\}/jobs/\{job\_id\}/preview


-   参数说明

    **表 1**  URI 参数

    <a name="table18337867015"></a>
    <table><thead align="left"><tr id="row2334162017"><th class="cellrowborder" valign="top" width="16.919999999999998%" id="mcps1.2.5.1.1"><p id="p19334261015"><a name="p19334261015"></a><a name="p19334261015"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="10.23%" id="mcps1.2.5.1.2"><p id="p6334861108"><a name="p6334861108"></a><a name="p6334861108"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.479999999999999%" id="mcps1.2.5.1.3"><p id="p17119637183714"><a name="p17119637183714"></a><a name="p17119637183714"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="60.370000000000005%" id="mcps1.2.5.1.4"><p id="p8334268015"><a name="p8334268015"></a><a name="p8334268015"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row7929145544017"><td class="cellrowborder" valign="top" width="16.919999999999998%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0069077803_p43412436"><a name="zh-cn_topic_0069077803_p43412436"></a><a name="zh-cn_topic_0069077803_p43412436"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.23%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0069077803_p26746391"><a name="zh-cn_topic_0069077803_p26746391"></a><a name="zh-cn_topic_0069077803_p26746391"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.479999999999999%" headers="mcps1.2.5.1.3 "><p id="p3119183723712"><a name="p3119183723712"></a><a name="p3119183723712"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.370000000000005%" headers="mcps1.2.5.1.4 "><p id="p1310472724012"><a name="p1310472724012"></a><a name="p1310472724012"></a>项目编号，用于资源隔离。获取方式请参考<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    <tr id="row73351761701"><td class="cellrowborder" valign="top" width="16.919999999999998%" headers="mcps1.2.5.1.1 "><p id="p173340614018"><a name="p173340614018"></a><a name="p173340614018"></a>job_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.23%" headers="mcps1.2.5.1.2 "><p id="p123344611019"><a name="p123344611019"></a><a name="p123344611019"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.479999999999999%" headers="mcps1.2.5.1.3 "><p id="p9120113716371"><a name="p9120113716371"></a><a name="p9120113716371"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.370000000000005%" headers="mcps1.2.5.1.4 "><p id="p20335106301"><a name="p20335106301"></a><a name="p20335106301"></a>作业ID。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 2**  query参数

    <a name="table1701101045811"></a>
    <table><thead align="left"><tr id="row77021110185813"><th class="cellrowborder" valign="top" width="16.919999999999998%" id="mcps1.2.5.1.1"><p id="p270214100585"><a name="p270214100585"></a><a name="p270214100585"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.57%" id="mcps1.2.5.1.2"><p id="p177021410155813"><a name="p177021410155813"></a><a name="p177021410155813"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="14.469999999999999%" id="mcps1.2.5.1.3"><p id="p57021110145813"><a name="p57021110145813"></a><a name="p57021110145813"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="56.04%" id="mcps1.2.5.1.4"><p id="p16702111012588"><a name="p16702111012588"></a><a name="p16702111012588"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row11703131011581"><td class="cellrowborder" valign="top" width="16.919999999999998%" headers="mcps1.2.5.1.1 "><p id="p17031610195820"><a name="p17031610195820"></a><a name="p17031610195820"></a>page-size</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.57%" headers="mcps1.2.5.1.2 "><p id="p2703171065815"><a name="p2703171065815"></a><a name="p2703171065815"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.469999999999999%" headers="mcps1.2.5.1.3 "><p id="p1670331015817"><a name="p1670331015817"></a><a name="p1670331015817"></a>Long</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.04%" headers="mcps1.2.5.1.4 "><p id="p18703201015818"><a name="p18703201015818"></a><a name="p18703201015818"></a>结果行数，范围: [1, 1000]。默认值为：1000。</p>
    </td>
    </tr>
    <tr id="row1870315109586"><td class="cellrowborder" valign="top" width="16.919999999999998%" headers="mcps1.2.5.1.1 "><p id="p177041210165813"><a name="p177041210165813"></a><a name="p177041210165813"></a>queue-name</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.57%" headers="mcps1.2.5.1.2 "><p id="p1370481065811"><a name="p1370481065811"></a><a name="p1370481065811"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.469999999999999%" headers="mcps1.2.5.1.3 "><p id="p1970416109587"><a name="p1970416109587"></a><a name="p1970416109587"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="56.04%" headers="mcps1.2.5.1.4 "><p id="p470410107589"><a name="p470410107589"></a><a name="p470410107589"></a>指定获取作业结果的执行队列名称。若不指定则使用默认的系统队列。</p>
    </td>
    </tr>
    </tbody>
    </table>

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >带入query参数的URL示例如下：
    >GET /v1.0/\{project\_id\}/jobs/\{job\_id\}/preview?page-size=_\{size\}_&queue-name=_\{queue\_name\}_


## 请求消息<a name="se4ec083d06454f1d82589db5de2c43cc"></a>

无请求参数。

## 响应消息<a name="s26e44e4c19ae431ab7d5d8758c986eb8"></a>

**表 3**  响应参数

<a name="table1175762563013"></a>
<table><thead align="left"><tr id="row17758142518307"><th class="cellrowborder" valign="top" width="14.55145514551455%" id="mcps1.2.5.1.1"><p id="p727713523308"><a name="p727713523308"></a><a name="p727713523308"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="11.061106110611062%" id="mcps1.2.5.1.2"><p id="p7363240460"><a name="p7363240460"></a><a name="p7363240460"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="16.881688168816883%" id="mcps1.2.5.1.3"><p id="p171211130123515"><a name="p171211130123515"></a><a name="p171211130123515"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="57.505750575057505%" id="mcps1.2.5.1.4"><p id="p112771852113019"><a name="p112771852113019"></a><a name="p112771852113019"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1175852593012"><td class="cellrowborder" valign="top" width="14.55145514551455%" headers="mcps1.2.5.1.1 "><p id="p375822523018"><a name="p375822523018"></a><a name="p375822523018"></a>is_success</p>
</td>
<td class="cellrowborder" valign="top" width="11.061106110611062%" headers="mcps1.2.5.1.2 "><p id="p73631845467"><a name="p73631845467"></a><a name="p73631845467"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.881688168816883%" headers="mcps1.2.5.1.3 "><p id="p3812181519518"><a name="p3812181519518"></a><a name="p3812181519518"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="57.505750575057505%" headers="mcps1.2.5.1.4 "><p id="p862011251763"><a name="p862011251763"></a><a name="p862011251763"></a>执行请求是否成功。<span class="parmvalue" id="parmvalue6163363216617"><a name="parmvalue6163363216617"></a><a name="parmvalue6163363216617"></a>“true”</span>表示请求执行成功。</p>
</td>
</tr>
<tr id="row1875812533016"><td class="cellrowborder" valign="top" width="14.55145514551455%" headers="mcps1.2.5.1.1 "><p id="p975882514303"><a name="p975882514303"></a><a name="p975882514303"></a>message</p>
</td>
<td class="cellrowborder" valign="top" width="11.061106110611062%" headers="mcps1.2.5.1.2 "><p id="p163631243463"><a name="p163631243463"></a><a name="p163631243463"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.881688168816883%" headers="mcps1.2.5.1.3 "><p id="p18813715254"><a name="p18813715254"></a><a name="p18813715254"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="57.505750575057505%" headers="mcps1.2.5.1.4 "><p id="a9a27f692c352434fbfde0c951e23503b"><a name="a9a27f692c352434fbfde0c951e23503b"></a><a name="a9a27f692c352434fbfde0c951e23503b"></a>系统提示信息，执行成功时，信息可能为空。</p>
</td>
</tr>
<tr id="row147582025103017"><td class="cellrowborder" valign="top" width="14.55145514551455%" headers="mcps1.2.5.1.1 "><p id="p5758132513309"><a name="p5758132513309"></a><a name="p5758132513309"></a>job_id</p>
</td>
<td class="cellrowborder" valign="top" width="11.061106110611062%" headers="mcps1.2.5.1.2 "><p id="p1936319416466"><a name="p1936319416466"></a><a name="p1936319416466"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.881688168816883%" headers="mcps1.2.5.1.3 "><p id="p48139153518"><a name="p48139153518"></a><a name="p48139153518"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="57.505750575057505%" headers="mcps1.2.5.1.4 "><p id="p19620152516611"><a name="p19620152516611"></a><a name="p19620152516611"></a>作业ID。</p>
</td>
</tr>
<tr id="row57581125183017"><td class="cellrowborder" valign="top" width="14.55145514551455%" headers="mcps1.2.5.1.1 "><p id="p1975812254301"><a name="p1975812254301"></a><a name="p1975812254301"></a>job_type</p>
</td>
<td class="cellrowborder" valign="top" width="11.061106110611062%" headers="mcps1.2.5.1.2 "><p id="p136394104616"><a name="p136394104616"></a><a name="p136394104616"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.881688168816883%" headers="mcps1.2.5.1.3 "><p id="p168137152053"><a name="p168137152053"></a><a name="p168137152053"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="57.505750575057505%" headers="mcps1.2.5.1.4 "><p id="p19547103314618"><a name="p19547103314618"></a><a name="p19547103314618"></a>作业类型，包含DDL、DCL、IMPORT、EXPORT、QUERY、INSERT、DATA_MIGRATION、UPDATE、DELETE、RESTART_QUEUE、SCALE_QUEUE。</p>
<p id="p263831915266"><a name="p263831915266"></a><a name="p263831915266"></a>目前仅支持查看“QUERY”类型作业的执行结果。</p>
</td>
</tr>
<tr id="row8145205326"><td class="cellrowborder" valign="top" width="14.55145514551455%" headers="mcps1.2.5.1.1 "><p id="p015520103215"><a name="p015520103215"></a><a name="p015520103215"></a>row_count</p>
</td>
<td class="cellrowborder" valign="top" width="11.061106110611062%" headers="mcps1.2.5.1.2 "><p id="p4363134184610"><a name="p4363134184610"></a><a name="p4363134184610"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.881688168816883%" headers="mcps1.2.5.1.3 "><p id="p48131815251"><a name="p48131815251"></a><a name="p48131815251"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="57.505750575057505%" headers="mcps1.2.5.1.4 "><p id="p14151820183218"><a name="p14151820183218"></a><a name="p14151820183218"></a>作业结果总条数。</p>
</td>
</tr>
<tr id="row10990152253217"><td class="cellrowborder" valign="top" width="14.55145514551455%" headers="mcps1.2.5.1.1 "><p id="p19901122113216"><a name="p19901122113216"></a><a name="p19901122113216"></a>input_size</p>
</td>
<td class="cellrowborder" valign="top" width="11.061106110611062%" headers="mcps1.2.5.1.2 "><p id="p53631546466"><a name="p53631546466"></a><a name="p53631546466"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.881688168816883%" headers="mcps1.2.5.1.3 "><p id="p94349351478"><a name="p94349351478"></a><a name="p94349351478"></a>long</p>
</td>
<td class="cellrowborder" valign="top" width="57.505750575057505%" headers="mcps1.2.5.1.4 "><p id="p119901622103210"><a name="p119901622103210"></a><a name="p119901622103210"></a>作业执行过程中扫描的数据量。</p>
</td>
</tr>
<tr id="row8419638163220"><td class="cellrowborder" valign="top" width="14.55145514551455%" headers="mcps1.2.5.1.1 "><p id="p541923816325"><a name="p541923816325"></a><a name="p541923816325"></a>schema</p>
</td>
<td class="cellrowborder" valign="top" width="11.061106110611062%" headers="mcps1.2.5.1.2 "><p id="p4363104134612"><a name="p4363104134612"></a><a name="p4363104134612"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.881688168816883%" headers="mcps1.2.5.1.3 "><p id="p27869361976"><a name="p27869361976"></a><a name="p27869361976"></a>Array of  Objects</p>
</td>
<td class="cellrowborder" valign="top" width="57.505750575057505%" headers="mcps1.2.5.1.4 "><p id="p20419143820327"><a name="p20419143820327"></a><a name="p20419143820327"></a>作业结果列名称和类型。</p>
</td>
</tr>
<tr id="row13066311577"><td class="cellrowborder" valign="top" width="14.55145514551455%" headers="mcps1.2.5.1.1 "><p id="p667317416715"><a name="p667317416715"></a><a name="p667317416715"></a>rows</p>
</td>
<td class="cellrowborder" valign="top" width="11.061106110611062%" headers="mcps1.2.5.1.2 "><p id="p173631042463"><a name="p173631042463"></a><a name="p173631042463"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="16.881688168816883%" headers="mcps1.2.5.1.3 "><p id="p378683612717"><a name="p378683612717"></a><a name="p378683612717"></a>Array of Strings</p>
</td>
<td class="cellrowborder" valign="top" width="57.505750575057505%" headers="mcps1.2.5.1.4 "><p id="p93071431874"><a name="p93071431874"></a><a name="p93071431874"></a>作业结果集。</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section3290817714576"></a>

-   请求样例：

    ```
    None
    ```

-   成功响应样例：

    ```
    {
      "is_success": true,
      "message": "",
      "job_id": "ead0b276-8ed4-4eb5-b520-58f1511e7033",
      "job_type": "QUERY",
      "row_count": 1,
      "input_size": 74,
      "schema": [
        {
          "c1": "int"
        },
        {
          "c2": "string"
        }
      ],
      "rows": [
        [
          23,
          "sda"
        ]
      ]
    }
    ```


## 状态码<a name="sf39cfd445ad24e9e82754fcb0027179d"></a>

状态码如[表4](#tb12870f1c5f24b27abd55ca24264af36)所示。

**表 4**  状态码

<a name="tb12870f1c5f24b27abd55ca24264af36"></a>
<table><thead align="left"><tr id="r8d54231f95b14c01a5e55e95f3b2e838"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.3.1.1"><p id="ab49d21f312644072a331f43e92baf853"><a name="ab49d21f312644072a331f43e92baf853"></a><a name="ab49d21f312644072a331f43e92baf853"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="70%" id="mcps1.2.3.1.2"><p id="aea1d3bd107bb4c499da79a88832d256c"><a name="aea1d3bd107bb4c499da79a88832d256c"></a><a name="aea1d3bd107bb4c499da79a88832d256c"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="r211ad4eb571d4d938e5579998723174e"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="a3153e07b3a9749adba92599fe6628fbf"><a name="a3153e07b3a9749adba92599fe6628fbf"></a><a name="a3153e07b3a9749adba92599fe6628fbf"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p104431642124811"><a name="p104431642124811"></a><a name="p104431642124811"></a>查询成功。</p>
</td>
</tr>
<tr id="row44937531727"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p184941532219"><a name="p184941532219"></a><a name="p184941532219"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p2049413539219"><a name="p2049413539219"></a><a name="p2049413539219"></a>请求错误。</p>
</td>
</tr>
<tr id="row65331212142411"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p5537171216249"><a name="p5537171216249"></a><a name="p5537171216249"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p953813124249"><a name="p953813124249"></a><a name="p953813124249"></a>内部服务器错误。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section13596141025715"></a>

调用接口出错后，将不会返回上述结果，而是返回错误码和错误信息，更多介绍请参见[错误码](错误码.md)。

