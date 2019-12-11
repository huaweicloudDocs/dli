# 检查SQL语法<a name="dli_02_0107"></a>

## 功能介绍<a name="s15d8cb8e7b7f4b47acbc825ca34ae180"></a>

该API用于检查SQL语法。

## URI<a name="sec7331dc70ce415da2d94a4062c0e286"></a>

-   URI格式：

    POST /v1.0/\{project\_id\}/jobs/check-sql

-   参数说明

    **表 1**  URI 参数

    <a name="zh-cn_topic_0069077896_table12850938"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0069077896_row26986831"><th class="cellrowborder" valign="top" width="12.120000000000001%" id="mcps1.2.4.1.1"><p id="ac4350eeb47b04ac3842d18c867bd44eb"><a name="ac4350eeb47b04ac3842d18c867bd44eb"></a><a name="ac4350eeb47b04ac3842d18c867bd44eb"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="10%" id="mcps1.2.4.1.2"><p id="a9c7aa8e702fe45d598376fcd31c9f5ce"><a name="a9c7aa8e702fe45d598376fcd31c9f5ce"></a><a name="a9c7aa8e702fe45d598376fcd31c9f5ce"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="77.88000000000001%" id="mcps1.2.4.1.3"><p id="a319b72a499674bd8befd20b6a9358879"><a name="a319b72a499674bd8befd20b6a9358879"></a><a name="a319b72a499674bd8befd20b6a9358879"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row134331617104113"><td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0069077803_p43412436"><a name="zh-cn_topic_0069077803_p43412436"></a><a name="zh-cn_topic_0069077803_p43412436"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0069077803_p26746391"><a name="zh-cn_topic_0069077803_p26746391"></a><a name="zh-cn_topic_0069077803_p26746391"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.88000000000001%" headers="mcps1.2.4.1.3 "><p id="p1310472724012"><a name="p1310472724012"></a><a name="p1310472724012"></a>项目编号，用于资源隔离。获取方式请参考<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="sf71ef29ac20f4a86b617e33b97566e44"></a>

**表 2**  请求参数

<a name="table6376584143542"></a>
<table><thead align="left"><tr id="row19110893143542"><th class="cellrowborder" valign="top" width="11.98989898989899%" id="mcps1.2.5.1.1"><p id="p42934984143542"><a name="p42934984143542"></a><a name="p42934984143542"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.383838383838384%" id="mcps1.2.5.1.2"><p id="p55181642143542"><a name="p55181642143542"></a><a name="p55181642143542"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="12.000000000000002%" id="mcps1.2.5.1.3"><p id="p40528033143542"><a name="p40528033143542"></a><a name="p40528033143542"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="65.62626262626263%" id="mcps1.2.5.1.4"><p id="p61545269143542"><a name="p61545269143542"></a><a name="p61545269143542"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row16818917143542"><td class="cellrowborder" valign="top" width="11.98989898989899%" headers="mcps1.2.5.1.1 "><p id="p4478514143542"><a name="p4478514143542"></a><a name="p4478514143542"></a>sql</p>
</td>
<td class="cellrowborder" valign="top" width="10.383838383838384%" headers="mcps1.2.5.1.2 "><p id="p27215339143542"><a name="p27215339143542"></a><a name="p27215339143542"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="12.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p56958849143542"><a name="p56958849143542"></a><a name="p56958849143542"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="65.62626262626263%" headers="mcps1.2.5.1.4 "><p id="p1036145143542"><a name="p1036145143542"></a><a name="p1036145143542"></a>待执行的SQL语句。</p>
</td>
</tr>
<tr id="row48821488143542"><td class="cellrowborder" valign="top" width="11.98989898989899%" headers="mcps1.2.5.1.1 "><p id="p17152532143542"><a name="p17152532143542"></a><a name="p17152532143542"></a>currentdb</p>
</td>
<td class="cellrowborder" valign="top" width="10.383838383838384%" headers="mcps1.2.5.1.2 "><p id="p47177872143542"><a name="p47177872143542"></a><a name="p47177872143542"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="12.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p63311321143542"><a name="p63311321143542"></a><a name="p63311321143542"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="65.62626262626263%" headers="mcps1.2.5.1.4 "><p id="p27943382143542"><a name="p27943382143542"></a><a name="p27943382143542"></a>SQL语句执行所在的数据库。</p>
<div class="note" id="note2355567214459"><a name="note2355567214459"></a><a name="note2355567214459"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul59257121144616"></a><a name="ul59257121144616"></a><ul id="ul59257121144616"><li>在SQL里面已经包含db_name的情况下可以不选该参数，例如SQL为：<i><b><span class="cmdname" style="font-family:Arial" id="cmdname24207892144758"><a name="cmdname24207892144758"></a><a name="cmdname24207892144758"></a>select * from db1.t1</span></b></i>。</li><li>SQL里面不包含db_name时，不选该参数或者选错该参数均会导致语法校验不通过。</li></ul>
</div></div>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="s3cacdc89985c49fa9b00c879e3880d15"></a>

**表 3**  响应参数

<a name="zh-cn_topic_0069077896_table33203075"></a>
<table><thead align="left"><tr id="zh-cn_topic_0069077896_row35922485"><th class="cellrowborder" valign="top" width="11.87%" id="mcps1.2.5.1.1"><p id="a5212f67c295f4ae7a136c5eb4d263e47"><a name="a5212f67c295f4ae7a136c5eb4d263e47"></a><a name="a5212f67c295f4ae7a136c5eb4d263e47"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.24%" id="mcps1.2.5.1.2"><p id="p6901173019816"><a name="p6901173019816"></a><a name="p6901173019816"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="11.41%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0069077896_p944819142913"><a name="zh-cn_topic_0069077896_p944819142913"></a><a name="zh-cn_topic_0069077896_p944819142913"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="67.47999999999999%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0069077896_p944851413912"><a name="zh-cn_topic_0069077896_p944851413912"></a><a name="zh-cn_topic_0069077896_p944851413912"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0069077896_row12898672"><td class="cellrowborder" valign="top" width="11.87%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0069077896_p38159543"><a name="zh-cn_topic_0069077896_p38159543"></a><a name="zh-cn_topic_0069077896_p38159543"></a>is_success</p>
</td>
<td class="cellrowborder" valign="top" width="9.24%" headers="mcps1.2.5.1.2 "><p id="p1690110300812"><a name="p1690110300812"></a><a name="p1690110300812"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.41%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0069077896_p48699120"><a name="zh-cn_topic_0069077896_p48699120"></a><a name="zh-cn_topic_0069077896_p48699120"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="67.47999999999999%" headers="mcps1.2.5.1.4 "><p id="p1216075194811"><a name="p1216075194811"></a><a name="p1216075194811"></a>执行请求是否成功。<span class="parmvalue" id="parmvalue2253974916747"><a name="parmvalue2253974916747"></a><a name="parmvalue2253974916747"></a>“true”</span>表示请求执行成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0069077896_row1070040"><td class="cellrowborder" valign="top" width="11.87%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0069077896_p19564417"><a name="zh-cn_topic_0069077896_p19564417"></a><a name="zh-cn_topic_0069077896_p19564417"></a>message</p>
</td>
<td class="cellrowborder" valign="top" width="9.24%" headers="mcps1.2.5.1.2 "><p id="p199017301087"><a name="p199017301087"></a><a name="p199017301087"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="11.41%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0069077896_p49998030"><a name="zh-cn_topic_0069077896_p49998030"></a><a name="zh-cn_topic_0069077896_p49998030"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="67.47999999999999%" headers="mcps1.2.5.1.4 "><p id="a4fa277540d3e42e48cec2027a36ca6bc"><a name="a4fa277540d3e42e48cec2027a36ca6bc"></a><a name="a4fa277540d3e42e48cec2027a36ca6bc"></a>系统提示信息，执行成功时，信息可能为空。</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section43379838151112"></a>

-   请求样例：

    ```
    {
       "currentdb": "db1",
       "sql": "select * from t1"   
    }
    ```

-   成功响应样例：

    ```
    {
      "is_success": true,
      "message": ""
    }
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >调用接口出错后，将不会返回上述结果，而是返回错误码和错误信息，详细介绍请参见[错误码](错误码.md)。  


