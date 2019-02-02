# 查询rna-diffExpr作业<a name="dli_02_0150"></a>

## 功能介绍<a name="section6968756197"></a>

查询所有已经提交的RNA差异表达分析作业的信息，包括作业状态、运行时间等。

## URI<a name="section169693561590"></a>

-   URI格式

    GET /v2.0/\{project\_id\}/gene/jobs?job\_type=RNA\_DIFF\_EXPR&limit=limit&offset=offset&start=start\_time&end=end\_time

-   参数说明

    **表 1**  URI参数

    <a name="table129761556598"></a>
    <table><thead align="left"><tr id="row1826735713913"><th class="cellrowborder" valign="top" width="11.88888888888889%" id="mcps1.2.4.1.1"><p id="p226717571598"><a name="p226717571598"></a><a name="p226717571598"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="8.262626262626263%" id="mcps1.2.4.1.2"><p id="p8267195712917"><a name="p8267195712917"></a><a name="p8267195712917"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="79.84848484848484%" id="mcps1.2.4.1.3"><p id="p11267457995"><a name="p11267457995"></a><a name="p11267457995"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1026714572915"><td class="cellrowborder" valign="top" width="11.88888888888889%" headers="mcps1.2.4.1.1 "><p id="p17267757296"><a name="p17267757296"></a><a name="p17267757296"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.262626262626263%" headers="mcps1.2.4.1.2 "><p id="p14267557694"><a name="p14267557694"></a><a name="p14267557694"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="79.84848484848484%" headers="mcps1.2.4.1.3 "><p id="p82675571912"><a name="p82675571912"></a><a name="p82675571912"></a>项目编号。</p>
    </td>
    </tr>
    <tr id="row1226716573912"><td class="cellrowborder" valign="top" width="11.88888888888889%" headers="mcps1.2.4.1.1 "><p id="p690111461916"><a name="p690111461916"></a><a name="p690111461916"></a>job_type</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.262626262626263%" headers="mcps1.2.4.1.2 "><p id="p9901746512"><a name="p9901746512"></a><a name="p9901746512"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="79.84848484848484%" headers="mcps1.2.4.1.3 "><p id="p14901346515"><a name="p14901346515"></a><a name="p14901346515"></a>作业类型，对于rna-diffExpr作业为：<span class="parmvalue" id="parmvalue1479322015820"><a name="parmvalue1479322015820"></a><a name="parmvalue1479322015820"></a>“RNA_DIFF_EXPR”</span>。</p>
    </td>
    </tr>
    <tr id="row1426711571890"><td class="cellrowborder" valign="top" width="11.88888888888889%" headers="mcps1.2.4.1.1 "><p id="p1826713571397"><a name="p1826713571397"></a><a name="p1826713571397"></a>limit</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.262626262626263%" headers="mcps1.2.4.1.2 "><p id="p1026795710912"><a name="p1026795710912"></a><a name="p1026795710912"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="79.84848484848484%" headers="mcps1.2.4.1.3 "><p id="p22671457796"><a name="p22671457796"></a><a name="p22671457796"></a>每页显示作业记录的条数，范围: [1, 100]，默认值：10。</p>
    </td>
    </tr>
    <tr id="row1826855715912"><td class="cellrowborder" valign="top" width="11.88888888888889%" headers="mcps1.2.4.1.1 "><p id="p8267357993"><a name="p8267357993"></a><a name="p8267357993"></a>offset</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.262626262626263%" headers="mcps1.2.4.1.2 "><p id="p132678578917"><a name="p132678578917"></a><a name="p132678578917"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="79.84848484848484%" headers="mcps1.2.4.1.3 "><p id="p2268155713918"><a name="p2268155713918"></a><a name="p2268155713918"></a>作业记录查询的偏移量，计算方式：limit * (待查询的页码 -1)。例如，设定limit=10，则查看第一页作业记录的offset=0，表示没有偏移量；查看第二页作业记录的offset=10，表示当前作业记录的偏移量为10，即从第11条记录开始查看；以此类推。默认值：0。</p>
    </td>
    </tr>
    <tr id="row22682057196"><td class="cellrowborder" valign="top" width="11.88888888888889%" headers="mcps1.2.4.1.1 "><p id="p192681657995"><a name="p192681657995"></a><a name="p192681657995"></a>start</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.262626262626263%" headers="mcps1.2.4.1.2 "><p id="p22680574914"><a name="p22680574914"></a><a name="p22680574914"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="79.84848484848484%" headers="mcps1.2.4.1.3 "><p id="p172681157494"><a name="p172681157494"></a><a name="p172681157494"></a>用于查询开始时间在该时间点之后的作业。时间格式为unix时间戳，单位：毫秒。</p>
    </td>
    </tr>
    <tr id="row210824618400"><td class="cellrowborder" valign="top" width="11.88888888888889%" headers="mcps1.2.4.1.1 "><p id="p132686579919"><a name="p132686579919"></a><a name="p132686579919"></a>end</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.262626262626263%" headers="mcps1.2.4.1.2 "><p id="p112689571297"><a name="p112689571297"></a><a name="p112689571297"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="79.84848484848484%" headers="mcps1.2.4.1.3 "><p id="p1426817576910"><a name="p1426817576910"></a><a name="p1426817576910"></a>用于查询开始时间在该时间点之前的作业。时间格式为unix时间戳，单位：毫秒。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="section3414034164017"></a>

无请求参数。

## 响应消息<a name="section2101574914"></a>

-   返回码

    200

-   响应参数可参见[表2](查询所有dna-germline作业.md#table192695719914)

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
                "owner": "h00251609",
                "duration": 16731,
                "status": "FINISHED",
                "progress": "1/1",
                "request": "{\"output\":\"s3a://diff-expr/out/7115da95-e409-402b-a30c-6e8700654d4d.csv\",\"ref\":\"hg19\",\"job_type\":\"RNA_DIFF_EXPR\",\"inputs\":[{\"group_name\":\"K\",\"group_inputs\":[{\"sample_name\":\"SRR6354710_2M\",\"files\":[\"s3a://diff-expr/SRR6354710_2M_R1.fastq.gz\",\"s3a://diff-expr/SRR6354710_2M_R2.fastq.gz\"]},{\"sample_name\":\"SRR6354711_2M\",\"files\":[\"s3a://diff-expr/SRR6354711_2M_R1.fastq.gz\",\"s3a://diff-expr/SRR6354711_2M_R2.fastq.gz\"]}]},{\"group_name\":\"W\",\"group_inputs\":[{\"sample_name\":\"SRR6354714_2M\",\"files\":[\"s3a://diff-expr/SRR6354714_2M_R1.fastq.gz\",\"s3a://diff-expr/SRR6354714_2M_R2.fastq.gz\"]},{\"sample_name\":\"SRR6354715_2M\",\"files\":[\"s3a://diff-expr/SRR6354715_2M_R1.fastq.gz\",\"s3a://diff-expr/SRR6354715_2M_R2.fastq.gz\"]}]}],\"gtf\":\"gencode.v17.annotation.gtf\",\"bed\":\"s3a://diff-expr/hg19_rRNA.bed\", \"library_type\":\"fr-firststrand\"}",
                "message": "",
                "job_id": "7115da95-e409-402b-a30c-6e8700654d4d",
                "start_time": 1537448098842
            }
        ]
    }
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >调用接口出错后，将不会返回上述结果，而是返回错误码和错误信息，详细介绍请参见[错误码](错误码.md)。  


