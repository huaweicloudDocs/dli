# 创建Spark集群<a name="dli_01_0313"></a>

开通DLI服务之后，用户需向创建集群接口发送RESTful请求，创建全托管式Spark集群。

1.  创建集群。调用创建集群接口（URI格式为：POST /v2.0/\{project\_id\}/clusters），在请求体参数中填写cluster\_name, cu\_count和description字段。
    -   请求参数说明

        <a name="table18210937211"></a>
        <table><thead align="left"><tr id="row18208039215"><th class="cellrowborder" valign="top" width="25%" id="mcps1.1.5.1.1"><p id="p10208631321"><a name="p10208631321"></a><a name="p10208631321"></a>名称</p>
        </th>
        <th class="cellrowborder" valign="top" width="15%" id="mcps1.1.5.1.2"><p id="p7208163129"><a name="p7208163129"></a><a name="p7208163129"></a>是否必选</p>
        </th>
        <th class="cellrowborder" valign="top" width="15%" id="mcps1.1.5.1.3"><p id="p13208731726"><a name="p13208731726"></a><a name="p13208731726"></a>参数类型</p>
        </th>
        <th class="cellrowborder" valign="top" width="45%" id="mcps1.1.5.1.4"><p id="p22086319211"><a name="p22086319211"></a><a name="p22086319211"></a>说明</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row05091642141"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.1 "><p id="p19510134210420"><a name="p19510134210420"></a><a name="p19510134210420"></a>cluster_name</p>
        </td>
        <td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.5.1.2 "><p id="p8510184217415"><a name="p8510184217415"></a><a name="p8510184217415"></a>是</p>
        </td>
        <td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.5.1.3 "><p id="p551119423410"><a name="p551119423410"></a><a name="p551119423410"></a>String</p>
        </td>
        <td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.5.1.4 "><p id="p13511442446"><a name="p13511442446"></a><a name="p13511442446"></a>创建的集群名。</p>
        </td>
        </tr>
        <tr id="row1208531524"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.1 "><p id="p72081535215"><a name="p72081535215"></a><a name="p72081535215"></a>cu_count</p>
        </td>
        <td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.5.1.2 "><p id="p2020810315215"><a name="p2020810315215"></a><a name="p2020810315215"></a>是</p>
        </td>
        <td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.5.1.3 "><p id="p720816315218"><a name="p720816315218"></a><a name="p720816315218"></a>Integer</p>
        </td>
        <td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.5.1.4 "><p id="p1198319511890"><a name="p1198319511890"></a><a name="p1198319511890"></a>与集群绑定的计算单元个数, 同时是计费的单元。</p>
        </td>
        </tr>
        <tr id="row16433153514198"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.1 "><p id="p134331635111913"><a name="p134331635111913"></a><a name="p134331635111913"></a>description</p>
        </td>
        <td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.5.1.2 "><p id="p5433143551914"><a name="p5433143551914"></a><a name="p5433143551914"></a>否</p>
        </td>
        <td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.5.1.3 "><p id="p164331435151918"><a name="p164331435151918"></a><a name="p164331435151918"></a>String</p>
        </td>
        <td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.5.1.4 "><p id="p54338358195"><a name="p54338358195"></a><a name="p54338358195"></a>集群描述信息。</p>
        </td>
        </tr>
        </tbody>
        </table>

    -   请求样例：

        ```
        {
        	"cluster_name": "cluster1",
        	"cu_count": 4,
        	"description": "test"
        }
        ```

    -   查看响应，返回201，表示创建集群请求成功。

2.  获取集群状态。调用获取指定集群信息接口（URI格式为：GET /v2.0/\{project\_id\}/clusters/\{cluster\_name\}），查看集群当前状态，响应样例：

    ```
     {
        "create_time": 1508143955000, 
        "cu_count": 4, 
        "description": "test", 
        "owner": "tenant1", 
        "cluster_name": "cluster1",
        "status": "AVAILABLE"
     }
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >创建集群成功后，立刻获取集群信息，集群状态（status字段）为CREATING，需要等待大概二十分钟，集群状态才会变化为AVAILABLE。集群状态为AVAILABLE时，表示集群创建完成。  


