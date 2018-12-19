# 查询所有dna-germline作业<a name="dli_02_0141"></a>

## 功能介绍<a name="section6968756197"></a>

查询所有已经提交的作业的信息，包括作业状态、运行时间等。

## URI<a name="section169693561590"></a>

-   URI格式

    GET /v2.0/\{project\_id\}/gene/jobs?job\_type=DNA\_GERMLINE&limit=limit&offset=offset&start=start\_time&end=end\_time

-   参数说明

    **表 1**  URI参数

    <a name="table129761556598"></a>
    <table><thead align="left"><tr id="row1826735713913"><th class="cellrowborder" valign="top" width="17.171717171717173%" id="mcps1.2.4.1.1"><p id="p226717571598"><a name="p226717571598"></a><a name="p226717571598"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.121212121212121%" id="mcps1.2.4.1.2"><p id="p8267195712917"><a name="p8267195712917"></a><a name="p8267195712917"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="70.70707070707071%" id="mcps1.2.4.1.3"><p id="p11267457995"><a name="p11267457995"></a><a name="p11267457995"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1026714572915"><td class="cellrowborder" valign="top" width="17.171717171717173%" headers="mcps1.2.4.1.1 "><p id="p17267757296"><a name="p17267757296"></a><a name="p17267757296"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.2.4.1.2 "><p id="p14267557694"><a name="p14267557694"></a><a name="p14267557694"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="70.70707070707071%" headers="mcps1.2.4.1.3 "><p id="p82675571912"><a name="p82675571912"></a><a name="p82675571912"></a>项目编号。</p>
    </td>
    </tr>
    <tr id="row289917465117"><td class="cellrowborder" valign="top" width="17.171717171717173%" headers="mcps1.2.4.1.1 "><p id="p690111461916"><a name="p690111461916"></a><a name="p690111461916"></a>job_type</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.2.4.1.2 "><p id="p9901746512"><a name="p9901746512"></a><a name="p9901746512"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="70.70707070707071%" headers="mcps1.2.4.1.3 "><p id="p14901346515"><a name="p14901346515"></a><a name="p14901346515"></a>作业类型，对于dna-germline作业为：<span class="parmvalue" id="parmvalue931133812598"><a name="parmvalue931133812598"></a><a name="parmvalue931133812598"></a>“DNA_GERMLINE”</span>。</p>
    </td>
    </tr>
    <tr id="row1226716573912"><td class="cellrowborder" valign="top" width="17.171717171717173%" headers="mcps1.2.4.1.1 "><p id="p1826713571397"><a name="p1826713571397"></a><a name="p1826713571397"></a>limit</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.2.4.1.2 "><p id="p1026795710912"><a name="p1026795710912"></a><a name="p1026795710912"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="70.70707070707071%" headers="mcps1.2.4.1.3 "><p id="p22671457796"><a name="p22671457796"></a><a name="p22671457796"></a>每页显示作业记录的条数，范围: [1, 100]，默认值：10。</p>
    </td>
    </tr>
    <tr id="row1426711571890"><td class="cellrowborder" valign="top" width="17.171717171717173%" headers="mcps1.2.4.1.1 "><p id="p8267357993"><a name="p8267357993"></a><a name="p8267357993"></a>offset</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.2.4.1.2 "><p id="p132678578917"><a name="p132678578917"></a><a name="p132678578917"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="70.70707070707071%" headers="mcps1.2.4.1.3 "><p id="p2268155713918"><a name="p2268155713918"></a><a name="p2268155713918"></a>作业记录查询的偏移量，计算方式：limit * (待查询的页码 -1)。例如，设定limit=10，则查看第一页作业记录的offset=0，表示没有偏移量；查看第二页作业记录的offset=10，表示当前作业记录的偏移量为10，即从第11条记录开始查看；以此类推。默认值：0。</p>
    </td>
    </tr>
    <tr id="row1826855715912"><td class="cellrowborder" valign="top" width="17.171717171717173%" headers="mcps1.2.4.1.1 "><p id="p192681657995"><a name="p192681657995"></a><a name="p192681657995"></a>start</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.2.4.1.2 "><p id="p22680574914"><a name="p22680574914"></a><a name="p22680574914"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="70.70707070707071%" headers="mcps1.2.4.1.3 "><p id="p172681157494"><a name="p172681157494"></a><a name="p172681157494"></a>用于查询开始时间在该时间点之后的作业。时间格式为unix时间戳，单位：毫秒。</p>
    </td>
    </tr>
    <tr id="row22682057196"><td class="cellrowborder" valign="top" width="17.171717171717173%" headers="mcps1.2.4.1.1 "><p id="p132686579919"><a name="p132686579919"></a><a name="p132686579919"></a>end</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.2.4.1.2 "><p id="p112689571297"><a name="p112689571297"></a><a name="p112689571297"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="70.70707070707071%" headers="mcps1.2.4.1.3 "><p id="p1426817576910"><a name="p1426817576910"></a><a name="p1426817576910"></a>用于查询开始时间在该时间点之前的作业。时间格式为unix时间戳，单位：毫秒。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="section3414034164017"></a>

无请求参数。

## 响应消息<a name="section2101574914"></a>

-   返回码

    200

-   响应参数

**表 2**  响应参数

<a name="table192695719914"></a>
<table><thead align="left"><tr id="row82696574918"><th class="cellrowborder" valign="top" width="15.120000000000001%" id="mcps1.2.4.1.1"><p id="p102691857892"><a name="p102691857892"></a><a name="p102691857892"></a>参数名</p>
</th>
<th class="cellrowborder" valign="top" width="12.790000000000001%" id="mcps1.2.4.1.2"><p id="p12269185711914"><a name="p12269185711914"></a><a name="p12269185711914"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="72.09%" id="mcps1.2.4.1.3"><p id="p192698571294"><a name="p192698571294"></a><a name="p192698571294"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row5269257198"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p1226915571998"><a name="p1226915571998"></a><a name="p1226915571998"></a>job_count</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p1726911578913"><a name="p1726911578913"></a><a name="p1726911578913"></a>int</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p527011570915"><a name="p527011570915"></a><a name="p527011570915"></a>返回的作业个数。</p>
</td>
</tr>
<tr id="row89762011203411"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p109761711113420"><a name="p109761711113420"></a><a name="p109761711113420"></a>jobs</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p19976101143410"><a name="p19976101143410"></a><a name="p19976101143410"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p4976111183419"><a name="p4976111183419"></a><a name="p4976111183419"></a>具体请参考<a href="#table1066213340337">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  jobs参数

<a name="table1066213340337"></a>
<table><thead align="left"><tr id="row1966683414337"><th class="cellrowborder" valign="top" width="15.120000000000001%" id="mcps1.2.4.1.1"><p id="p466873416331"><a name="p466873416331"></a><a name="p466873416331"></a>参数名</p>
</th>
<th class="cellrowborder" valign="top" width="12.790000000000001%" id="mcps1.2.4.1.2"><p id="p766812345333"><a name="p766812345333"></a><a name="p766812345333"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="72.09%" id="mcps1.2.4.1.3"><p id="p1669193412333"><a name="p1669193412333"></a><a name="p1669193412333"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1167516342336"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p15677193417334"><a name="p15677193417334"></a><a name="p15677193417334"></a>job_id</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p367743414333"><a name="p367743414333"></a><a name="p367743414333"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p967823493319"><a name="p967823493319"></a><a name="p967823493319"></a>基因作业的唯一ID。</p>
</td>
</tr>
<tr id="row15679113473318"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p106811234153313"><a name="p106811234153313"></a><a name="p106811234153313"></a>request</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p6682193410335"><a name="p6682193410335"></a><a name="p6682193410335"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p1468233483317"><a name="p1468233483317"></a><a name="p1468233483317"></a>提交该作业时的请求体。</p>
</td>
</tr>
<tr id="row368312346331"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p1968353413316"><a name="p1968353413316"></a><a name="p1968353413316"></a>owner</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p96841349338"><a name="p96841349338"></a><a name="p96841349338"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p146851234133312"><a name="p146851234133312"></a><a name="p146851234133312"></a>提交该作业的用户名。</p>
</td>
</tr>
<tr id="row10685123433312"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p13687103417339"><a name="p13687103417339"></a><a name="p13687103417339"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p12687934153313"><a name="p12687934153313"></a><a name="p12687934153313"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p14689183493310"><a name="p14689183493310"></a><a name="p14689183493310"></a>作业当前状态，包含提交（LAUNCHING）、运行中（RUNNING）、完成（FINISHED）、失败（FAILED）、取消（CANCELLED）、取消中（CANCELING）</p>
</td>
</tr>
<tr id="row768915341337"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p1169016348335"><a name="p1169016348335"></a><a name="p1169016348335"></a>progress</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p20692134113311"><a name="p20692134113311"></a><a name="p20692134113311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p2069414345332"><a name="p2069414345332"></a><a name="p2069414345332"></a>作业当前执行的进度。如：1/3表示总共有3个步骤，当前执行到第一步。</p>
</td>
</tr>
<tr id="row136941349334"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p1169493413319"><a name="p1169493413319"></a><a name="p1169493413319"></a>start_time</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p1695113410330"><a name="p1695113410330"></a><a name="p1695113410330"></a>Timestamp</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p669503417331"><a name="p669503417331"></a><a name="p669503417331"></a>作业开始的时间。</p>
</td>
</tr>
<tr id="row969673423316"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p106971534183316"><a name="p106971534183316"></a><a name="p106971534183316"></a>duration</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p76986349336"><a name="p76986349336"></a><a name="p76986349336"></a>Long</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p27001334113310"><a name="p27001334113310"></a><a name="p27001334113310"></a>作业执行的时间, 单位秒。</p>
</td>
</tr>
<tr id="row117002348336"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.4.1.1 "><p id="p17009343338"><a name="p17009343338"></a><a name="p17009343338"></a>message</p>
</td>
<td class="cellrowborder" valign="top" width="12.790000000000001%" headers="mcps1.2.4.1.2 "><p id="p970103453316"><a name="p970103453316"></a><a name="p970103453316"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="72.09%" headers="mcps1.2.4.1.3 "><p id="p107031134133310"><a name="p107031134133310"></a><a name="p107031134133310"></a>作业执行失败时，显示失败的原因。</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section320217117419"></a>

-   请求样例：

    ```
    None
    ```


-   成功响应样例:

    ```
    {
        "job_count": 1,
        "jobs": [
            {
                "owner": "username",
                "duration": 48452,
                "status": "RUNNING",
                "progress": "1/3",
                "request": "{\"job_type\":\"DNA_GERMLINE\",\"input\":[\"s3a://hzw/NA12878_small.bam\"],\"output\":\"s3a://uquery/aas/test/bbf4c994-b53d-4d88-b15c-97e45a29d14f.vcf\",\"file_type\":\"BAM\",\"ref\":\"hg38\",\"knownsites\":[\"mills_and_1000g_gold_standard.indels.hg38.vcf\"],\"fastq_ubam_conf\":[\"-PL\",\"illumina\",\"-SM\",\"SM1\",\"-MR\",\"2000000\"],\"bwaspark_conf\":null,\"read_pipeline_spark_conf\":null,
                "message": null,
                "job_id": "180b9816-fb9f-454a-9537-09bee18834e0",
                "start_time": 1532605670471
            }
        ]
    }
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >调用接口出错后，将不会返回上述结果，而是返回错误码和错误信息，详细介绍请参见[错误码](错误码.md)。  


