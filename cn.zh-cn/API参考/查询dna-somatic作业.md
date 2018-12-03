# 查询dna-somatic作业<a name="dli_02_0154"></a>

## 功能介绍<a name="section6968756197"></a>

查询所有已经提交的体细胞肿瘤检测作业的信息，包括作业状态、运行时间等。

## URI<a name="section169693561590"></a>

-   URI格式

    GET /v2.0/\{project\_id\}/gene/jobs?job\_type=DNA\_SOMATIC&limit=limit&offset=offset&start=start\_time&end=end\_time

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
    <tr id="row1226716573912"><td class="cellrowborder" valign="top" width="17.171717171717173%" headers="mcps1.2.4.1.1 "><p id="p690111461916"><a name="p690111461916"></a><a name="p690111461916"></a>job_type</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.2.4.1.2 "><p id="p9901746512"><a name="p9901746512"></a><a name="p9901746512"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="70.70707070707071%" headers="mcps1.2.4.1.3 "><p id="p14901346515"><a name="p14901346515"></a><a name="p14901346515"></a>作业类型，对于dna_somatic作业为：<span class="parmvalue" id="parmvalue1479322015820"><a name="parmvalue1479322015820"></a><a name="parmvalue1479322015820"></a><b>DNA_SOMATIC</b></span>。</p>
    </td>
    </tr>
    <tr id="row1426711571890"><td class="cellrowborder" valign="top" width="17.171717171717173%" headers="mcps1.2.4.1.1 "><p id="p1826713571397"><a name="p1826713571397"></a><a name="p1826713571397"></a>limit</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.2.4.1.2 "><p id="p1026795710912"><a name="p1026795710912"></a><a name="p1026795710912"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="70.70707070707071%" headers="mcps1.2.4.1.3 "><p id="p22671457796"><a name="p22671457796"></a><a name="p22671457796"></a>每页显示作业记录的条数，范围: [1, 100]，默认值：10。</p>
    </td>
    </tr>
    <tr id="row1826855715912"><td class="cellrowborder" valign="top" width="17.171717171717173%" headers="mcps1.2.4.1.1 "><p id="p8267357993"><a name="p8267357993"></a><a name="p8267357993"></a>offset</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.2.4.1.2 "><p id="p132678578917"><a name="p132678578917"></a><a name="p132678578917"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="70.70707070707071%" headers="mcps1.2.4.1.3 "><p id="p2268155713918"><a name="p2268155713918"></a><a name="p2268155713918"></a>作业记录查询的偏移量，计算方式：limit * (待查询的页码 -1)。例如，设定limit=10，则查看第一页作业记录的offset=0，表示没有偏移量；查看第二页作业记录的offset=10，表示当前作业记录的偏移量为10，即从第11条记录开始查看；以此类推。默认值：0。</p>
    </td>
    </tr>
    <tr id="row22682057196"><td class="cellrowborder" valign="top" width="17.171717171717173%" headers="mcps1.2.4.1.1 "><p id="p192681657995"><a name="p192681657995"></a><a name="p192681657995"></a>start</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.2.4.1.2 "><p id="p22680574914"><a name="p22680574914"></a><a name="p22680574914"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="70.70707070707071%" headers="mcps1.2.4.1.3 "><p id="p172681157494"><a name="p172681157494"></a><a name="p172681157494"></a>用于查询开始时间在该时间点之后的作业。时间格式为unix时间戳，单位：毫秒。</p>
    </td>
    </tr>
    <tr id="row210824618400"><td class="cellrowborder" valign="top" width="17.171717171717173%" headers="mcps1.2.4.1.1 "><p id="p132686579919"><a name="p132686579919"></a><a name="p132686579919"></a>end</p>
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
                "duration": 2770,
                "status": "RUNNING",
                "progress": "6/7",
                "request": "{\"output\":\"s3a://genes/somatic/gwjfastqout.vcf\",\"ref\":\"hg38\",\"intervals\":[\"wgs_calling_regions.hg38.interval_list\"],\"conf\":null,\"access_encoded_key\":null,\"secret_encoded_key\":null,\"job_type\":\"DNA_SOMATIC\",\"inputs\":[{\"sample_type\":\"tumor\",\"sample_inputs\":[\"s3a://genes/somatic/tumor_1.fastq.gz\",\"s3a://genes/somatic/tumor_2.fastq.gz\"]},{\"sample_type\":\"normal\",\"sample_inputs\":[\"s3a://genes/somatic/normal_1.fastq.gz\",\"s3a://genes/somatic/normal_2.fastq.gz\"]}],\"tumor_sample_name\":\"HCC1143_tumor\",\"normal_sample_name\":\"HCC1143_normal\",\"file_type\":\"fastq\",\"knownsites\":[\"1000g_omni2.5.hg38.vcf\"],\"fastq_ubam_conf\":null,\"bwaspark_conf\":null,\"read_pipeline_spark_conf\":null,\"pon\":\"somatic-hg38-1000g_pon.hg38.vcf.gz\",\"germline_resource\":\"somatic-hg38faf-only-gnomad.hg38.vcf.gz\",\"mutect_is_export_bam\":false,\"mutect_bam_output\":\"s3a://genes/somatic/test.bam\",\"mutect_calls_variant\":\"small_exac_common_3.hg38.vcf.gz\",\"is_filter_by_orientationBias\":false,\"artifact_modes\":[\"G/T\"],\"is_filter_by_alignmentArtifacts\":false,\"expect_time\":8}",
                "message": null,
                "job_id": "c0619372-983d-4861-9133-69a518fca074",
                "start_time": 1540954644485
            }
         ]
    }
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >调用接口出错后，将不会返回上述结果，而是返回错误码和错误信息，详细介绍请参见[错误码](错误码.md)。  


