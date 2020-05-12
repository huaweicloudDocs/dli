# 新建SQL作业<a name="dli_02_0228"></a>

## 功能介绍<a name="s89ff8bc59cba4c3b94dc17e85c8fa1ea"></a>

创建Flink SQL作业。

## URI<a name="sef21e3efc2a44a84a03adad33a1ae006"></a>

-   URI格式

    POST /v1.0/\{project\_id\}/streaming/sql-jobs

-   参数说明

    **表 1**  URI参数说明

    <a name="t219b031199884ac1bb9e91158ddc9efb"></a>
    <table><thead align="left"><tr id="r04005eeda24e4db9b06516450d4d56af"><th class="cellrowborder" valign="top" width="16.97%" id="mcps1.2.4.1.1"><p id="a80847df5e5dc448caa46a2ff258fa2c4"><a name="a80847df5e5dc448caa46a2ff258fa2c4"></a><a name="a80847df5e5dc448caa46a2ff258fa2c4"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.94%" id="mcps1.2.4.1.2"><p id="af54fc16087b049c98f748c1a2faace17"><a name="af54fc16087b049c98f748c1a2faace17"></a><a name="af54fc16087b049c98f748c1a2faace17"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="65.09%" id="mcps1.2.4.1.3"><p id="a484a3e0ce14846799c727ccbd4075d6c"><a name="a484a3e0ce14846799c727ccbd4075d6c"></a><a name="a484a3e0ce14846799c727ccbd4075d6c"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="r8022e11be3f54ad290cf8c848a56a550"><td class="cellrowborder" valign="top" width="16.97%" headers="mcps1.2.4.1.1 "><p id="a2b526eb27eb241248b0586fd54086598"><a name="a2b526eb27eb241248b0586fd54086598"></a><a name="a2b526eb27eb241248b0586fd54086598"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.94%" headers="mcps1.2.4.1.2 "><p id="p1016041415356"><a name="p1016041415356"></a><a name="p1016041415356"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="65.09%" headers="mcps1.2.4.1.3 "><p id="p1768719515356"><a name="p1768719515356"></a><a name="p1768719515356"></a>项目编号，用于资源隔离。获取方式请参考<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="s3afece1037ea4f62aeffb3db49b97f70"></a>

-   请求样例

    ```
    {
        "name": "myjob",
        "desc": "这是个做字符记数的作业",
        "template_id": 100000,
        "queue_name": "testQueue",
        "sql_body": "select * from source_table",
        "run_mode": "exclusive_cluster",
        "cu_number": 2,
        "parallel_number": 1,
        "checkpoint_enabled": false,
        "checkpoint_mode": "exactly_once",
        "checkpoint_interval": 0,
        "obs_bucket": "my_obs_bucket",
        "log_enabled": false,
        "restart_when_exception": false,
        "idle_state_retention": 3600,
        "job_type": "flink_sql_job",
        
     
     
     
        "dirty_data_strategy": "0",
        "udf_jar_url": "group/test.jar"
    }
    ```

-   参数说明

    **表 2**  请求参数说明

    <a name="tcedd9d5bece544898da42c15fe855a72"></a>
    <table><thead align="left"><tr id="r263212cfc24b4f7ab11ba179dc95f8d5"><th class="cellrowborder" valign="top" width="20.849999999999998%" id="mcps1.2.5.1.1"><p id="aa71bb56aa6ba48488d66e68a44744488"><a name="aa71bb56aa6ba48488d66e68a44744488"></a><a name="aa71bb56aa6ba48488d66e68a44744488"></a>参数名</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.120000000000001%" id="mcps1.2.5.1.2"><p id="adfb457c202dc4709b315aa6d0a384fdf"><a name="adfb457c202dc4709b315aa6d0a384fdf"></a><a name="adfb457c202dc4709b315aa6d0a384fdf"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="11.64%" id="mcps1.2.5.1.3"><p id="a07ad11538b854ab4997a0c69b2fa1ff5"><a name="a07ad11538b854ab4997a0c69b2fa1ff5"></a><a name="a07ad11538b854ab4997a0c69b2fa1ff5"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="55.38999999999999%" id="mcps1.2.5.1.4"><p id="a27603242143846be8ed4173686b0b27b"><a name="a27603242143846be8ed4173686b0b27b"></a><a name="a27603242143846be8ed4173686b0b27b"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="rab514ea502754f9d88a6ca5cd27e6f9b"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p24236235151446"><a name="p24236235151446"></a><a name="p24236235151446"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="a3f01c30693ef41f9ab8913a733a8dcae"><a name="a3f01c30693ef41f9ab8913a733a8dcae"></a><a name="a3f01c30693ef41f9ab8913a733a8dcae"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="a4c806296e81547638d0ed294d9a3ca63"><a name="a4c806296e81547638d0ed294d9a3ca63"></a><a name="a4c806296e81547638d0ed294d9a3ca63"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="ace897a9e7d9d47a1895664dd49e10fe5"><a name="ace897a9e7d9d47a1895664dd49e10fe5"></a><a name="ace897a9e7d9d47a1895664dd49e10fe5"></a>作业名称。长度限制：0-57个字符。</p>
    </td>
    </tr>
    <tr id="rd59ae95756ea47c28d7aa24b2a057881"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p60911214151446"><a name="p60911214151446"></a><a name="p60911214151446"></a>desc</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="a3db6910eff34455caa5af7c1be07ff39"><a name="a3db6910eff34455caa5af7c1be07ff39"></a><a name="a3db6910eff34455caa5af7c1be07ff39"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="a3b4b1f2ddd81469dbc22dc9de316fc9b"><a name="a3b4b1f2ddd81469dbc22dc9de316fc9b"></a><a name="a3b4b1f2ddd81469dbc22dc9de316fc9b"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="a4de8fb2d168546a9adf40df6d59ce095"><a name="a4de8fb2d168546a9adf40df6d59ce095"></a><a name="a4de8fb2d168546a9adf40df6d59ce095"></a>作业描述。长度限制：0-512个字符。</p>
    </td>
    </tr>
    <tr id="rc32461e6ae584faebd86e6a27d35ad52"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p45216947151446"><a name="p45216947151446"></a><a name="p45216947151446"></a>template_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="aa5ebc166527543019d7799ddf643663f"><a name="aa5ebc166527543019d7799ddf643663f"></a><a name="aa5ebc166527543019d7799ddf643663f"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="ad6a32cc0ba694cea9fe5f132dd482a0b"><a name="ad6a32cc0ba694cea9fe5f132dd482a0b"></a><a name="ad6a32cc0ba694cea9fe5f132dd482a0b"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="a6311275524c844f4aa133f8f5818d0c0"><a name="a6311275524c844f4aa133f8f5818d0c0"></a><a name="a6311275524c844f4aa133f8f5818d0c0"></a>模板Id。</p>
    <p id="p1438412141206"><a name="p1438412141206"></a><a name="p1438412141206"></a>如果<span class="parmname" id="parmname3795113375013"><a name="parmname3795113375013"></a><a name="parmname3795113375013"></a>“template_id”</span>和<span class="parmname" id="parmname113041406507"><a name="parmname113041406507"></a><a name="parmname113041406507"></a>“sql_body”</span>都不为空，优先选择<span class="parmname" id="parmname178092114519"><a name="parmname178092114519"></a><a name="parmname178092114519"></a>“sql_body”</span>的内容；如果<span class="parmname" id="parmname1583133812519"><a name="parmname1583133812519"></a><a name="parmname1583133812519"></a>“template_id”</span>不为空，<span class="parmname" id="parmname85051251185116"><a name="parmname85051251185116"></a><a name="parmname85051251185116"></a>“sql_body”</span>为空，选择<span class="parmname" id="parmname1095861165211"><a name="parmname1095861165211"></a><a name="parmname1095861165211"></a>“template_id”</span>的内容填充<span class="parmname" id="parmname6520142215522"><a name="parmname6520142215522"></a><a name="parmname6520142215522"></a>“sql_body”</span>。</p>
    </td>
    </tr>
    <tr id="row71872872118"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p17928153443914"><a name="p17928153443914"></a><a name="p17928153443914"></a>queue_name</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p89278346396"><a name="p89278346396"></a><a name="p89278346396"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="p1292519344391"><a name="p1292519344391"></a><a name="p1292519344391"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="p18919434113920"><a name="p18919434113920"></a><a name="p18919434113920"></a>队列名称。长度限制：1-128个字符。</p>
    </td>
    </tr>
    <tr id="r38ed7748501049b3a7f15541cb4bdc4b"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p30775898151446"><a name="p30775898151446"></a><a name="p30775898151446"></a>sql_body</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="a340bf6a8cdce459ebdb06f53dd44204d"><a name="a340bf6a8cdce459ebdb06f53dd44204d"></a><a name="a340bf6a8cdce459ebdb06f53dd44204d"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="ab0cf8c891059456883c2149d7b794ba1"><a name="ab0cf8c891059456883c2149d7b794ba1"></a><a name="ab0cf8c891059456883c2149d7b794ba1"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="ac9cd898aa62e4b4c81ae3645e8d767e0"><a name="ac9cd898aa62e4b4c81ae3645e8d767e0"></a><a name="ac9cd898aa62e4b4c81ae3645e8d767e0"></a>Stream SQL语句，至少包含source, query, sink三个部分。长度限制：1024*1024个字符。</p>
    </td>
    </tr>
    <tr id="r6d6edee93eb44b018bb642182c0e6228"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p51971590151446"><a name="p51971590151446"></a><a name="p51971590151446"></a>run_mode</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="aba11f8fa96ff477e8af2e81aabc0d8de"><a name="aba11f8fa96ff477e8af2e81aabc0d8de"></a><a name="aba11f8fa96ff477e8af2e81aabc0d8de"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="a1c9f0e6238ad4ce69be9eafbb38d73d9"><a name="a1c9f0e6238ad4ce69be9eafbb38d73d9"></a><a name="a1c9f0e6238ad4ce69be9eafbb38d73d9"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="p79611213113"><a name="p79611213113"></a><a name="p79611213113"></a>作业运行模式：</p>
    <a name="ul15289751193715"></a><a name="ul15289751193715"></a><ul id="ul15289751193715"><li>shared_cluster：共享。</li><li>exclusive_cluster：独享。</li></ul>
    <p id="p19772114195416"><a name="p19772114195416"></a><a name="p19772114195416"></a>默认值为“shared_cluster”。</p>
    </td>
    </tr>
    <tr id="r7661b89ca2e94401ab63183ad079e920"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p19885945151446"><a name="p19885945151446"></a><a name="p19885945151446"></a>cu_number</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="a4b43c1e99deb4082b3f21179c1477b1f"><a name="a4b43c1e99deb4082b3f21179c1477b1f"></a><a name="a4b43c1e99deb4082b3f21179c1477b1f"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="adf45245d5ce04f61afc160b115d2412b"><a name="adf45245d5ce04f61afc160b115d2412b"></a><a name="adf45245d5ce04f61afc160b115d2412b"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="a37e9360fa1d44cf0b3fafc4bbe29cc2d"><a name="a37e9360fa1d44cf0b3fafc4bbe29cc2d"></a><a name="a37e9360fa1d44cf0b3fafc4bbe29cc2d"></a>用户为作业选择的CU数。默认值为“2”。</p>
    </td>
    </tr>
    <tr id="r589617809d1e42868f5a1aa6a3dbf196"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p19578767151446"><a name="p19578767151446"></a><a name="p19578767151446"></a>parallel_number</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="a3081bb162d8a41cda78080611d26e443"><a name="a3081bb162d8a41cda78080611d26e443"></a><a name="a3081bb162d8a41cda78080611d26e443"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="a714864b01e3b4f948edf105756d06630"><a name="a714864b01e3b4f948edf105756d06630"></a><a name="a714864b01e3b4f948edf105756d06630"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="a5c667b50c56f47dbb9bee32c10d72ba0"><a name="a5c667b50c56f47dbb9bee32c10d72ba0"></a><a name="a5c667b50c56f47dbb9bee32c10d72ba0"></a>用户设置的作业并行数目。默认值为“1”。</p>
    </td>
    </tr>
    <tr id="r4751eede45fe4cb3856249640bbc3c77"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p686005151439"><a name="p686005151439"></a><a name="p686005151439"></a>checkpoint_enabled</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="a582fb4ae115d44e79559c249bfcafab6"><a name="a582fb4ae115d44e79559c249bfcafab6"></a><a name="a582fb4ae115d44e79559c249bfcafab6"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="a32e117ff1f8940e79eb14e009be0e7ab"><a name="a32e117ff1f8940e79eb14e009be0e7ab"></a><a name="a32e117ff1f8940e79eb14e009be0e7ab"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="p4191338101210"><a name="p4191338101210"></a><a name="p4191338101210"></a>是否开启作业自动快照功能。</p>
    <a name="ul960951941319"></a><a name="ul960951941319"></a><ul id="ul960951941319"><li>开启：true</li><li>关闭：false</li><li>默认：false</li></ul>
    </td>
    </tr>
    <tr id="rbef8b00389c343f1a6acb6261756d967"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p32848831151439"><a name="p32848831151439"></a><a name="p32848831151439"></a>checkpoint_mode</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="ac3897cc29eb1495b9bbee471c304e326"><a name="ac3897cc29eb1495b9bbee471c304e326"></a><a name="ac3897cc29eb1495b9bbee471c304e326"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="af4e810f37b724bb4860e63e51fc32e05"><a name="af4e810f37b724bb4860e63e51fc32e05"></a><a name="af4e810f37b724bb4860e63e51fc32e05"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="p228619524239"><a name="p228619524239"></a><a name="p228619524239"></a>快照模式,。两种可选：</p>
    <a name="ul133371056182314"></a><a name="ul133371056182314"></a><ul id="ul133371056182314"><li>exactly_once：数据只被消费一次。</li><li>at_least_once：数据至少被消费一次。</li></ul>
    <p id="p1972956121218"><a name="p1972956121218"></a><a name="p1972956121218"></a>默认值为<span class="parmvalue" id="parmvalue17711380134"><a name="parmvalue17711380134"></a><a name="parmvalue17711380134"></a>“exactly_once”</span>。</p>
    </td>
    </tr>
    <tr id="row14878123920261"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p13880183918268"><a name="p13880183918268"></a><a name="p13880183918268"></a>checkpoint_interval</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p186384642711"><a name="p186384642711"></a><a name="p186384642711"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="p1664216614270"><a name="p1664216614270"></a><a name="p1664216614270"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="p5880113952617"><a name="p5880113952617"></a><a name="p5880113952617"></a>快照时间间隔, 单位为秒，默认值为<span class="parmvalue" id="parmvalue137215497343"><a name="parmvalue137215497343"></a><a name="parmvalue137215497343"></a>“10”</span>。</p>
    </td>
    </tr>
    <tr id="rbdbc4a1a7b9d41b0873a21b5c8c515a4"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p32635548151439"><a name="p32635548151439"></a><a name="p32635548151439"></a>obs_bucket</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="af1ba5522fd1e4cb1856c94e5e69a665d"><a name="af1ba5522fd1e4cb1856c94e5e69a665d"></a><a name="af1ba5522fd1e4cb1856c94e5e69a665d"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="a9a24d2aea7e342e2891e5daf0bf14743"><a name="a9a24d2aea7e342e2891e5daf0bf14743"></a><a name="a9a24d2aea7e342e2891e5daf0bf14743"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="a1ce1860d24414e2081b94e41c906d4f7"><a name="a1ce1860d24414e2081b94e41c906d4f7"></a><a name="a1ce1860d24414e2081b94e41c906d4f7"></a>当<span class="parmname" id="parmname1053712595910"><a name="parmname1053712595910"></a><a name="parmname1053712595910"></a>“checkpoint_enabled”</span>为<span class="parmvalue" id="parmvalue3715181511595"><a name="parmvalue3715181511595"></a><a name="parmvalue3715181511595"></a>“true”</span>时，该参数是用户授权保存快照的OBS路径。</p>
    <p id="p18511124216591"><a name="p18511124216591"></a><a name="p18511124216591"></a>当<span class="parmname" id="parmname1785618526598"><a name="parmname1785618526598"></a><a name="parmname1785618526598"></a>“log_enabled”</span> 为<span class="parmvalue" id="parmvalue4244115813597"><a name="parmvalue4244115813597"></a><a name="parmvalue4244115813597"></a>“true”</span>时，该参数是用户授权保存作业日志的OBS路径。</p>
    </td>
    </tr>
    <tr id="r7c856f9629304e7bb100c8794d29caf1"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p29331592151433"><a name="p29331592151433"></a><a name="p29331592151433"></a>log_enabled</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="a01071703297a4354bb6cb18ba6572f3f"><a name="a01071703297a4354bb6cb18ba6572f3f"></a><a name="a01071703297a4354bb6cb18ba6572f3f"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="a279c155d38614fc486c897f82f6a3a8f"><a name="a279c155d38614fc486c897f82f6a3a8f"></a><a name="a279c155d38614fc486c897f82f6a3a8f"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="a8819ccc464094137afa687b48d8f62b2"><a name="a8819ccc464094137afa687b48d8f62b2"></a><a name="a8819ccc464094137afa687b48d8f62b2"></a>是否开启作业的日志上传到用户的OBS功能。默认为<span class="parmvalue" id="parmvalue18333947602"><a name="parmvalue18333947602"></a><a name="parmvalue18333947602"></a>“false”</span>。</p>
    </td>
    </tr>
    <tr id="row1973917493203"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p27391449182012"><a name="p27391449182012"></a><a name="p27391449182012"></a>smn_topic</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p1773919491205"><a name="p1773919491205"></a><a name="p1773919491205"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="p147398499204"><a name="p147398499204"></a><a name="p147398499204"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="p67391449142016"><a name="p67391449142016"></a><a name="p67391449142016"></a>当作业异常时，向该SMN主题推送告警信息。</p>
    </td>
    </tr>
    <tr id="row014411362057"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p12884615665"><a name="p12884615665"></a><a name="p12884615665"></a>restart_when_exception</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p1414410363514"><a name="p1414410363514"></a><a name="p1414410363514"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="p1714403618511"><a name="p1714403618511"></a><a name="p1714403618511"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="p314419367515"><a name="p314419367515"></a><a name="p314419367515"></a>是否开启作业异常自动重启。默认为<span class="parmvalue" id="parmvalue52961551300"><a name="parmvalue52961551300"></a><a name="parmvalue52961551300"></a>“false”</span>。</p>
    </td>
    </tr>
    <tr id="row71935566513"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p1888312819610"><a name="p1888312819610"></a><a name="p1888312819610"></a>idle_state_retention</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p21931256755"><a name="p21931256755"></a><a name="p21931256755"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="p1119385615510"><a name="p1119385615510"></a><a name="p1119385615510"></a>Int</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="p15193856757"><a name="p15193856757"></a><a name="p15193856757"></a>空闲状态过期周期，单位为秒，默认值为<span class="parmvalue" id="parmvalue321164543410"><a name="parmvalue321164543410"></a><a name="parmvalue321164543410"></a>“3600”</span>。</p>
    </td>
    </tr>
    <tr id="row1321714314112"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p1921793115118"><a name="p1921793115118"></a><a name="p1921793115118"></a>job_type</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p192177311117"><a name="p192177311117"></a><a name="p192177311117"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="p112174313119"><a name="p112174313119"></a><a name="p112174313119"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="p597173717169"><a name="p597173717169"></a><a name="p597173717169"></a>作业类型：flink_sql_job和flink_sql_edge_job。</p>
    <a name="ul14520163841811"></a><a name="ul14520163841811"></a><ul id="ul14520163841811"><li><span class="parmname" id="parmname1748418271424"><a name="parmname1748418271424"></a><a name="parmname1748418271424"></a>“run_mode”</span>为<span class="parmvalue" id="parmvalue15545194114212"><a name="parmvalue15545194114212"></a><a name="parmvalue15545194114212"></a>“edge_node”</span>时，作业类型须为<span class="parmvalue" id="parmvalue13231105016210"><a name="parmvalue13231105016210"></a><a name="parmvalue13231105016210"></a>“flink_sql_edge_job”</span>。</li><li><span class="parmname" id="parmname161164111317"><a name="parmname161164111317"></a><a name="parmname161164111317"></a>“run_mode”</span>为<span class="parmvalue" id="parmvalue107543111135"><a name="parmvalue107543111135"></a><a name="parmvalue107543111135"></a>“shared_cluster”</span>和<span class="parmvalue" id="parmvalue9376163016313"><a name="parmvalue9376163016313"></a><a name="parmvalue9376163016313"></a>“exclusive_cluster”</span>时，作业类型须为<span class="parmvalue" id="parmvalue896194012318"><a name="parmvalue896194012318"></a><a name="parmvalue896194012318"></a>“flink_sql_job”</span>。</li><li>默认值：<span class="parmvalue" id="parmvalue1468113274417"><a name="parmvalue1468113274417"></a><a name="parmvalue1468113274417"></a>“flink_sql_job”</span>。</li></ul>
    </td>
    </tr>
    <tr id="row1977812466369"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p1842823984611"><a name="p1842823984611"></a><a name="p1842823984611"></a><span>dirty_data_strategy</span></p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p164285395469"><a name="p164285395469"></a><a name="p164285395469"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="p94281539184614"><a name="p94281539184614"></a><a name="p94281539184614"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="p1842883912463"><a name="p1842883912463"></a><a name="p1842883912463"></a>作业脏数据策略。</p>
    <a name="ul14821163115417"></a><a name="ul14821163115417"></a><ul id="ul14821163115417"><li>“<span>2:obs-wan-wulan3/jobs</span>”：保存</li><li>“1”：抛出异常</li><li>“0”：忽略</li></ul>
    <p id="p17304143102218"><a name="p17304143102218"></a><a name="p17304143102218"></a>默认值为“0”。</p>
    </td>
    </tr>
    <tr id="row16141247203911"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p19470241751"><a name="p19470241751"></a><a name="p19470241751"></a>udf_jar_url</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p19474241851"><a name="p19474241851"></a><a name="p19474241851"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="p1894820241519"><a name="p1894820241519"></a><a name="p1894820241519"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="p894882416512"><a name="p894882416512"></a><a name="p894882416512"></a>用户已上传到DLI资源管理系统的资源包名，用户sql作业的udf jar通过该参数传入。</p>
    </td>
    </tr>
    <tr id="row21601724348"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p3942456173617"><a name="p3942456173617"></a><a name="p3942456173617"></a>manager_cu_number</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p1494215615362"><a name="p1494215615362"></a><a name="p1494215615362"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="p3942135673612"><a name="p3942135673612"></a><a name="p3942135673612"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="p29421456113614"><a name="p29421456113614"></a><a name="p29421456113614"></a>用户为作业选择的管理单元（jobmanager）CU数量，默认值为“1”。</p>
    </td>
    </tr>
    <tr id="row10739195520211"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p62741531828"><a name="p62741531828"></a><a name="p62741531828"></a>tm_cus</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p1827415533218"><a name="p1827415533218"></a><a name="p1827415533218"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="p132740531925"><a name="p132740531925"></a><a name="p132740531925"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="p9274165315217"><a name="p9274165315217"></a><a name="p9274165315217"></a>每个taskmanager的CU数，默认值为“1”。</p>
    </td>
    </tr>
    <tr id="row773817551425"><td class="cellrowborder" valign="top" width="20.849999999999998%" headers="mcps1.2.5.1.1 "><p id="p122748531625"><a name="p122748531625"></a><a name="p122748531625"></a>tm_slot_num</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p1274125315210"><a name="p1274125315210"></a><a name="p1274125315210"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.5.1.3 "><p id="p1327455313218"><a name="p1327455313218"></a><a name="p1327455313218"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="55.38999999999999%" headers="mcps1.2.5.1.4 "><p id="p4275145317210"><a name="p4275145317210"></a><a name="p4275145317210"></a>每个taskmanager的slot数，默认值为“(parallel_number*tm_cus)/(cu_number-manager_cu_number)”。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 响应消息<a name="se2bf80cdb76541308f69f258ea4b1bd6"></a>

-   响应样例

    ```
    {
        "is_success": "true",
        "message": "创建作业成功",
        "job": {
            "job_id": 148,
            "status_name": "job_init",
            "status_desc": ""
        }
    }
    ```

-   参数说明

    **表 3**  响应参数说明

    <a name="t5995d65f65ba4ebca8606202112b407e"></a>
    <table><thead align="left"><tr id="ra7acea51e4b4437e917d21fe99f130a3"><th class="cellrowborder" valign="top" width="19.25%" id="mcps1.2.5.1.1"><p id="a5af940f2267747ef871c67c86a0be82e"><a name="a5af940f2267747ef871c67c86a0be82e"></a><a name="a5af940f2267747ef871c67c86a0be82e"></a>参数名</p>
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
    <td class="cellrowborder" valign="top" width="13.370000000000001%" headers="mcps1.2.5.1.3 "><p id="p118601817517"><a name="p118601817517"></a><a name="p118601817517"></a>String</p>
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
    <td class="cellrowborder" valign="top" width="13.370000000000001%" headers="mcps1.2.5.1.3 "><p id="p33383387265"><a name="p33383387265"></a><a name="p33383387265"></a>object</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.5.1.4 "><p id="p18338103822617"><a name="p18338103822617"></a><a name="p18338103822617"></a>作业状态信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 4**  job参数说明

    <a name="table86492245453"></a>
    <table><thead align="left"><tr id="row176501524184518"><th class="cellrowborder" valign="top" width="19.25%" id="mcps1.2.5.1.1"><p id="p18650152414511"><a name="p18650152414511"></a><a name="p18650152414511"></a>参数名</p>
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
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.5.1.4 "><p id="p565313246452"><a name="p565313246452"></a><a name="p565313246452"></a>当前状态描述。</p>
    </td>
    </tr>
    </tbody>
    </table>


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
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p828449123817"><a name="p828449123817"></a><a name="p828449123817"></a>创建作业成功。</p>
</td>
</tr>
<tr id="row264510302300"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p19646163033015"><a name="p19646163033015"></a><a name="p19646163033015"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p47552616316"><a name="p47552616316"></a><a name="p47552616316"></a>输入参数无效。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section13596141025715"></a>

调用接口出错后，将不会返回上述结果，而是返回错误码和错误信息，更多介绍请参见[错误码](错误码.md)。

**表 6**  错误码

<a name="zh-cn_topic_0207595520_table847819307387"></a>
<table><thead align="left"><tr id="zh-cn_topic_0207595520_row2479163016383"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0207595520_p114796309389"><a name="zh-cn_topic_0207595520_p114796309389"></a><a name="zh-cn_topic_0207595520_p114796309389"></a>错误码</p>
</th>
<th class="cellrowborder" valign="top" width="70%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0207595520_p1647973053817"><a name="zh-cn_topic_0207595520_p1647973053817"></a><a name="zh-cn_topic_0207595520_p1647973053817"></a>错误信息</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0207595520_row1047920308387"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p156228116372"><a name="p156228116372"></a><a name="p156228116372"></a>DLI.11032</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p737816382373"><a name="p737816382373"></a><a name="p737816382373"></a>SMN主题不存在请用户选择一个可用SMN主题</p>
</td>
</tr>
</tbody>
</table>

