# 更新SQL作业<a name="dli_02_0229"></a>

## 功能介绍<a name="s89ff8bc59cba4c3b94dc17e85c8fa1ea"></a>

该API用于修改Flink SQL作业。

## 调试<a name="section556523314214"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=DLI&api=UpdateFlinkSql)中调试该接口。

## URI<a name="sef21e3efc2a44a84a03adad33a1ae006"></a>

-   URI格式

    PUT /v1.0/\{project\_id\}/streaming/sql-jobs/\{job\_id\}

-   参数说明

    **表 1**  URI参数说明

    <a name="t219b031199884ac1bb9e91158ddc9efb"></a>
    <table><thead align="left"><tr id="r04005eeda24e4db9b06516450d4d56af"><th class="cellrowborder" valign="top" width="15.120000000000001%" id="mcps1.2.5.1.1"><p id="a80847df5e5dc448caa46a2ff258fa2c4"><a name="a80847df5e5dc448caa46a2ff258fa2c4"></a><a name="a80847df5e5dc448caa46a2ff258fa2c4"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="11.700000000000001%" id="mcps1.2.5.1.2"><p id="af54fc16087b049c98f748c1a2faace17"><a name="af54fc16087b049c98f748c1a2faace17"></a><a name="af54fc16087b049c98f748c1a2faace17"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="13.18%" id="mcps1.2.5.1.3"><p id="p886083518157"><a name="p886083518157"></a><a name="p886083518157"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="60%" id="mcps1.2.5.1.4"><p id="a484a3e0ce14846799c727ccbd4075d6c"><a name="a484a3e0ce14846799c727ccbd4075d6c"></a><a name="a484a3e0ce14846799c727ccbd4075d6c"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="r8022e11be3f54ad290cf8c848a56a550"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.5.1.1 "><p id="p1262440203315"><a name="p1262440203315"></a><a name="p1262440203315"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.700000000000001%" headers="mcps1.2.5.1.2 "><p id="p1016041415356"><a name="p1016041415356"></a><a name="p1016041415356"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.18%" headers="mcps1.2.5.1.3 "><p id="p78602358152"><a name="p78602358152"></a><a name="p78602358152"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.5.1.4 "><p id="p1768719515356"><a name="p1768719515356"></a><a name="p1768719515356"></a>项目编号，用于资源隔离。获取方式请参考<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    <tr id="row1266684418111"><td class="cellrowborder" valign="top" width="15.120000000000001%" headers="mcps1.2.5.1.1 "><p id="p12289184791118"><a name="p12289184791118"></a><a name="p12289184791118"></a>job_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.700000000000001%" headers="mcps1.2.5.1.2 "><p id="p112897475113"><a name="p112897475113"></a><a name="p112897475113"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.18%" headers="mcps1.2.5.1.3 "><p id="p1860113521510"><a name="p1860113521510"></a><a name="p1860113521510"></a>Long</p>
    </td>
    <td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.5.1.4 "><p id="p128964741114"><a name="p128964741114"></a><a name="p128964741114"></a>作业ID。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求消息<a name="s3afece1037ea4f62aeffb3db49b97f70"></a>

**表 2**  请求参数说明

<a name="tcedd9d5bece544898da42c15fe855a72"></a>
<table><thead align="left"><tr id="r263212cfc24b4f7ab11ba179dc95f8d5"><th class="cellrowborder" valign="top" width="25.06%" id="mcps1.2.5.1.1"><p id="aa71bb56aa6ba48488d66e68a44744488"><a name="aa71bb56aa6ba48488d66e68a44744488"></a><a name="aa71bb56aa6ba48488d66e68a44744488"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="14.940000000000001%" id="mcps1.2.5.1.2"><p id="adfb457c202dc4709b315aa6d0a384fdf"><a name="adfb457c202dc4709b315aa6d0a384fdf"></a><a name="adfb457c202dc4709b315aa6d0a384fdf"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="15%" id="mcps1.2.5.1.3"><p id="a07ad11538b854ab4997a0c69b2fa1ff5"><a name="a07ad11538b854ab4997a0c69b2fa1ff5"></a><a name="a07ad11538b854ab4997a0c69b2fa1ff5"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="45%" id="mcps1.2.5.1.4"><p id="a27603242143846be8ed4173686b0b27b"><a name="a27603242143846be8ed4173686b0b27b"></a><a name="a27603242143846be8ed4173686b0b27b"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="rd59ae95756ea47c28d7aa24b2a057881"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="a71daee1cc06048ae818e104254c9166d"><a name="a71daee1cc06048ae818e104254c9166d"></a><a name="a71daee1cc06048ae818e104254c9166d"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="p5890154754117"><a name="p5890154754117"></a><a name="p5890154754117"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="a3b4b1f2ddd81469dbc22dc9de316fc9b"><a name="a3b4b1f2ddd81469dbc22dc9de316fc9b"></a><a name="a3b4b1f2ddd81469dbc22dc9de316fc9b"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="a4de8fb2d168546a9adf40df6d59ce095"><a name="a4de8fb2d168546a9adf40df6d59ce095"></a><a name="a4de8fb2d168546a9adf40df6d59ce095"></a>作业名称。长度限制：0-57个字符。</p>
</td>
</tr>
<tr id="rc32461e6ae584faebd86e6a27d35ad52"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="a78edaa1801254949b38999fa2b76cb9b"><a name="a78edaa1801254949b38999fa2b76cb9b"></a><a name="a78edaa1801254949b38999fa2b76cb9b"></a>desc</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="aa5ebc166527543019d7799ddf643663f"><a name="aa5ebc166527543019d7799ddf643663f"></a><a name="aa5ebc166527543019d7799ddf643663f"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="ad6a32cc0ba694cea9fe5f132dd482a0b"><a name="ad6a32cc0ba694cea9fe5f132dd482a0b"></a><a name="ad6a32cc0ba694cea9fe5f132dd482a0b"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="a6311275524c844f4aa133f8f5818d0c0"><a name="a6311275524c844f4aa133f8f5818d0c0"></a><a name="a6311275524c844f4aa133f8f5818d0c0"></a>作业描述。长度限制：0-512个字符。</p>
</td>
</tr>
<tr id="row15798193244110"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="p17928153443914"><a name="p17928153443914"></a><a name="p17928153443914"></a>queue_name</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="p89278346396"><a name="p89278346396"></a><a name="p89278346396"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="p1292519344391"><a name="p1292519344391"></a><a name="p1292519344391"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p18919434113920"><a name="p18919434113920"></a><a name="p18919434113920"></a>队列名称。长度限制：1-128个字符。</p>
</td>
</tr>
<tr id="r38ed7748501049b3a7f15541cb4bdc4b"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="a80f760ee3fc749cda8a968aa352adb03"><a name="a80f760ee3fc749cda8a968aa352adb03"></a><a name="a80f760ee3fc749cda8a968aa352adb03"></a>sql_body</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="a340bf6a8cdce459ebdb06f53dd44204d"><a name="a340bf6a8cdce459ebdb06f53dd44204d"></a><a name="a340bf6a8cdce459ebdb06f53dd44204d"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="ab0cf8c891059456883c2149d7b794ba1"><a name="ab0cf8c891059456883c2149d7b794ba1"></a><a name="ab0cf8c891059456883c2149d7b794ba1"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="ac9cd898aa62e4b4c81ae3645e8d767e0"><a name="ac9cd898aa62e4b4c81ae3645e8d767e0"></a><a name="ac9cd898aa62e4b4c81ae3645e8d767e0"></a>Stream SQL语句，至少包含source, query, sink三个部分。长度限制：0-1024*1024个字符。</p>
</td>
</tr>
<tr id="r6d6edee93eb44b018bb642182c0e6228"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="aecea9fa299d942e88e78fba90c276a5b"><a name="aecea9fa299d942e88e78fba90c276a5b"></a><a name="aecea9fa299d942e88e78fba90c276a5b"></a>run_mode</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="aba11f8fa96ff477e8af2e81aabc0d8de"><a name="aba11f8fa96ff477e8af2e81aabc0d8de"></a><a name="aba11f8fa96ff477e8af2e81aabc0d8de"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="a1c9f0e6238ad4ce69be9eafbb38d73d9"><a name="a1c9f0e6238ad4ce69be9eafbb38d73d9"></a><a name="a1c9f0e6238ad4ce69be9eafbb38d73d9"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p79611213113"><a name="p79611213113"></a><a name="p79611213113"></a>作业运行模式：</p>
<a name="ul15289751193715"></a><a name="ul15289751193715"></a><ul id="ul15289751193715"><li>shared_cluster：共享。</li><li>exclusive_cluster：独享。</li><li>edge_node：边缘节点。</li></ul>
<p id="p12234112771417"><a name="p12234112771417"></a><a name="p12234112771417"></a>默认值为<span class="parmvalue" id="parmvalue10216234151415"><a name="parmvalue10216234151415"></a><a name="parmvalue10216234151415"></a>“shared_cluster”</span>。</p>
</td>
</tr>
<tr id="r7661b89ca2e94401ab63183ad079e920"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="a7e069f0f27af4abab440433e570c4763"><a name="a7e069f0f27af4abab440433e570c4763"></a><a name="a7e069f0f27af4abab440433e570c4763"></a>cu_number</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="a4b43c1e99deb4082b3f21179c1477b1f"><a name="a4b43c1e99deb4082b3f21179c1477b1f"></a><a name="a4b43c1e99deb4082b3f21179c1477b1f"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="adf45245d5ce04f61afc160b115d2412b"><a name="adf45245d5ce04f61afc160b115d2412b"></a><a name="adf45245d5ce04f61afc160b115d2412b"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p4369141103814"><a name="p4369141103814"></a><a name="p4369141103814"></a>用户为作业选择的CU数量。默认值为“2”。</p>
</td>
</tr>
<tr id="r589617809d1e42868f5a1aa6a3dbf196"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="a79683da069714592913a65f1f28389bc"><a name="a79683da069714592913a65f1f28389bc"></a><a name="a79683da069714592913a65f1f28389bc"></a>parallel_number</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="a3081bb162d8a41cda78080611d26e443"><a name="a3081bb162d8a41cda78080611d26e443"></a><a name="a3081bb162d8a41cda78080611d26e443"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="a714864b01e3b4f948edf105756d06630"><a name="a714864b01e3b4f948edf105756d06630"></a><a name="a714864b01e3b4f948edf105756d06630"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="a5c667b50c56f47dbb9bee32c10d72ba0"><a name="a5c667b50c56f47dbb9bee32c10d72ba0"></a><a name="a5c667b50c56f47dbb9bee32c10d72ba0"></a>用户设置的作业并行数目。默认值为“1”。</p>
</td>
</tr>
<tr id="r4751eede45fe4cb3856249640bbc3c77"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="p686005151439"><a name="p686005151439"></a><a name="p686005151439"></a>checkpoint_enabled</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="a582fb4ae115d44e79559c249bfcafab6"><a name="a582fb4ae115d44e79559c249bfcafab6"></a><a name="a582fb4ae115d44e79559c249bfcafab6"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="a32e117ff1f8940e79eb14e009be0e7ab"><a name="a32e117ff1f8940e79eb14e009be0e7ab"></a><a name="a32e117ff1f8940e79eb14e009be0e7ab"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p4191338101210"><a name="p4191338101210"></a><a name="p4191338101210"></a>是否开启作业自动快照功能。</p>
<a name="ul960951941319"></a><a name="ul960951941319"></a><ul id="ul960951941319"><li>开启：true</li><li>关闭：false</li><li>默认：false</li></ul>
</td>
</tr>
<tr id="rbef8b00389c343f1a6acb6261756d967"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="p32848831151439"><a name="p32848831151439"></a><a name="p32848831151439"></a>checkpoint_mode</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="ac3897cc29eb1495b9bbee471c304e326"><a name="ac3897cc29eb1495b9bbee471c304e326"></a><a name="ac3897cc29eb1495b9bbee471c304e326"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="af4e810f37b724bb4860e63e51fc32e05"><a name="af4e810f37b724bb4860e63e51fc32e05"></a><a name="af4e810f37b724bb4860e63e51fc32e05"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p228619524239"><a name="p228619524239"></a><a name="p228619524239"></a>快照模式,。两种可选：</p>
<a name="ul133371056182314"></a><a name="ul133371056182314"></a><ul id="ul133371056182314"><li>1：表示exactly_once，数据只被消费一次。</li><li>2：at_least_once，数据至少被消费一次。</li></ul>
<p id="p1972956121218"><a name="p1972956121218"></a><a name="p1972956121218"></a>默认值为1。</p>
</td>
</tr>
<tr id="rbdbc4a1a7b9d41b0873a21b5c8c515a4"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="p13880183918268"><a name="p13880183918268"></a><a name="p13880183918268"></a>checkpoint_interval</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="p186384642711"><a name="p186384642711"></a><a name="p186384642711"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="p1664216614270"><a name="p1664216614270"></a><a name="p1664216614270"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p5880113952617"><a name="p5880113952617"></a><a name="p5880113952617"></a>快照时间间隔。单位为秒，默认值为<span class="parmvalue" id="parmvalue992093518194"><a name="parmvalue992093518194"></a><a name="parmvalue992093518194"></a>“10”</span>。</p>
</td>
</tr>
<tr id="r7c856f9629304e7bb100c8794d29caf1"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="p32635548151439"><a name="p32635548151439"></a><a name="p32635548151439"></a>obs_bucket</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="af1ba5522fd1e4cb1856c94e5e69a665d"><a name="af1ba5522fd1e4cb1856c94e5e69a665d"></a><a name="af1ba5522fd1e4cb1856c94e5e69a665d"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="a9a24d2aea7e342e2891e5daf0bf14743"><a name="a9a24d2aea7e342e2891e5daf0bf14743"></a><a name="a9a24d2aea7e342e2891e5daf0bf14743"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="a1ce1860d24414e2081b94e41c906d4f7"><a name="a1ce1860d24414e2081b94e41c906d4f7"></a><a name="a1ce1860d24414e2081b94e41c906d4f7"></a>当<span class="parmname" id="parmname1053712595910"><a name="parmname1053712595910"></a><a name="parmname1053712595910"></a>“checkpoint_enabled”</span>为<span class="parmvalue" id="parmvalue3715181511595"><a name="parmvalue3715181511595"></a><a name="parmvalue3715181511595"></a>“true”</span>时，该参数是用户授权保存快照的OBS路径。</p>
<p id="p18511124216591"><a name="p18511124216591"></a><a name="p18511124216591"></a>当<span class="parmname" id="parmname1785618526598"><a name="parmname1785618526598"></a><a name="parmname1785618526598"></a>“log_enabled”</span> 为<span class="parmvalue" id="parmvalue4244115813597"><a name="parmvalue4244115813597"></a><a name="parmvalue4244115813597"></a>“true”</span>时，该参数是用户授权保存作业日志的OBS路径。</p>
</td>
</tr>
<tr id="row13972369443"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="p29331592151433"><a name="p29331592151433"></a><a name="p29331592151433"></a>log_enabled</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="a01071703297a4354bb6cb18ba6572f3f"><a name="a01071703297a4354bb6cb18ba6572f3f"></a><a name="a01071703297a4354bb6cb18ba6572f3f"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="a279c155d38614fc486c897f82f6a3a8f"><a name="a279c155d38614fc486c897f82f6a3a8f"></a><a name="a279c155d38614fc486c897f82f6a3a8f"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="a8819ccc464094137afa687b48d8f62b2"><a name="a8819ccc464094137afa687b48d8f62b2"></a><a name="a8819ccc464094137afa687b48d8f62b2"></a>是否开启作业的日志上传到用户的OBS功能。默认为<span class="parmvalue" id="parmvalue18333947602"><a name="parmvalue18333947602"></a><a name="parmvalue18333947602"></a>“false”</span>。</p>
</td>
</tr>
<tr id="row133265345358"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="p27391449182012"><a name="p27391449182012"></a><a name="p27391449182012"></a>smn_topic</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="p1773919491205"><a name="p1773919491205"></a><a name="p1773919491205"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="p147398499204"><a name="p147398499204"></a><a name="p147398499204"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p67391449142016"><a name="p67391449142016"></a><a name="p67391449142016"></a>当作业异常时，向该SMN主题推送告警信息。</p>
</td>
</tr>
<tr id="row153621144471"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="p12884615665"><a name="p12884615665"></a><a name="p12884615665"></a>restart_when_exception</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="p1414410363514"><a name="p1414410363514"></a><a name="p1414410363514"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="p1714403618511"><a name="p1714403618511"></a><a name="p1714403618511"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p314419367515"><a name="p314419367515"></a><a name="p314419367515"></a>是否开启作业异常自动重启。默认为<span class="parmvalue" id="parmvalue52961551300"><a name="parmvalue52961551300"></a><a name="parmvalue52961551300"></a>“false”</span>。</p>
</td>
</tr>
<tr id="row25271748175"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="p1888312819610"><a name="p1888312819610"></a><a name="p1888312819610"></a>idle_state_retention</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="p21931256755"><a name="p21931256755"></a><a name="p21931256755"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="p1119385615510"><a name="p1119385615510"></a><a name="p1119385615510"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p15193856757"><a name="p15193856757"></a><a name="p15193856757"></a>空闲状态过期周期，单位为秒，默认值为<span class="parmvalue" id="parmvalue321164543410"><a name="parmvalue321164543410"></a><a name="parmvalue321164543410"></a>“3600”</span>。</p>
</td>
</tr>
<tr id="row240012396412"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="p12217143121118"><a name="p12217143121118"></a><a name="p12217143121118"></a>edge_group_ids</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="p1721753113116"><a name="p1721753113116"></a><a name="p1721753113116"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="p1921773141113"><a name="p1921773141113"></a><a name="p1921773141113"></a><span>Array of Strings</span></p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p19919221166"><a name="p19919221166"></a><a name="p19919221166"></a>边缘计算组ID列表, 多个ID以逗号分隔。</p>
</td>
</tr>
<tr id="row61241615163812"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="p1842823984611"><a name="p1842823984611"></a><a name="p1842823984611"></a><span>dirty_data_strategy</span></p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="p164285395469"><a name="p164285395469"></a><a name="p164285395469"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="p94281539184614"><a name="p94281539184614"></a><a name="p94281539184614"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p1842883912463"><a name="p1842883912463"></a><a name="p1842883912463"></a>作业脏数据策略。</p>
<a name="ul14821163115417"></a><a name="ul14821163115417"></a><ul id="ul14821163115417"><li>“2:obsDir”：保存，obsDir表示脏数据存储路径。</li><li>“1”：抛出异常。</li><li>“0”：忽略。</li></ul>
<p id="p17304143102218"><a name="p17304143102218"></a><a name="p17304143102218"></a>默认值为“0”。</p>
</td>
</tr>
<tr id="row9273944104119"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="p19470241751"><a name="p19470241751"></a><a name="p19470241751"></a>udf_jar_url</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="p19474241851"><a name="p19474241851"></a><a name="p19474241851"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="p1894820241519"><a name="p1894820241519"></a><a name="p1894820241519"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p894882416512"><a name="p894882416512"></a><a name="p894882416512"></a>用户已上传到DLI资源管理系统的资源包名，用户sql作业的udf jar通过该参数传入。</p>
</td>
</tr>
<tr id="row1665234414101"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="p1841414505107"><a name="p1841414505107"></a><a name="p1841414505107"></a>manager_cu_number</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="p1441435061018"><a name="p1441435061018"></a><a name="p1441435061018"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="p141575071016"><a name="p141575071016"></a><a name="p141575071016"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p9415145081017"><a name="p9415145081017"></a><a name="p9415145081017"></a>用户为作业选择的管理单元（jobmanager）CU数量，默认值为“1”。</p>
</td>
</tr>
<tr id="row1016815010417"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="p62741531828"><a name="p62741531828"></a><a name="p62741531828"></a>tm_cus</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="p1827415533218"><a name="p1827415533218"></a><a name="p1827415533218"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="p132740531925"><a name="p132740531925"></a><a name="p132740531925"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p9274165315217"><a name="p9274165315217"></a><a name="p9274165315217"></a>每个taskmanager的CU数，默认值为“1”。</p>
</td>
</tr>
<tr id="row101673018413"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="p122748531625"><a name="p122748531625"></a><a name="p122748531625"></a>tm_slot_num</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="p1274125315210"><a name="p1274125315210"></a><a name="p1274125315210"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="p1327455313218"><a name="p1327455313218"></a><a name="p1327455313218"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p4275145317210"><a name="p4275145317210"></a><a name="p4275145317210"></a>每个taskmanager的slot数，默认值为“(parallel_number*tm_cus)/(cu_number-manager_cu_number)”。</p>
</td>
</tr>
<tr id="row255289141416"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="p455329181418"><a name="p455329181418"></a><a name="p455329181418"></a>operator_config</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="p25531093140"><a name="p25531093140"></a><a name="p25531093140"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="p10553129141411"><a name="p10553129141411"></a><a name="p10553129141411"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p855316917148"><a name="p855316917148"></a><a name="p855316917148"></a>算子的并行度配置。</p>
</td>
</tr>
<tr id="row16531919152715"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="p2335124251810"><a name="p2335124251810"></a><a name="p2335124251810"></a>resume_checkpoint</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="p173354422187"><a name="p173354422187"></a><a name="p173354422187"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="p113357429186"><a name="p113357429186"></a><a name="p113357429186"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p233519428187"><a name="p233519428187"></a><a name="p233519428187"></a>异常重启是否从checkpoint恢复。</p>
</td>
</tr>
<tr id="row145301819172713"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="p3543245162311"><a name="p3543245162311"></a><a name="p3543245162311"></a>resume_max_num</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="p9541245182312"><a name="p9541245182312"></a><a name="p9541245182312"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="p185409459238"><a name="p185409459238"></a><a name="p185409459238"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p1549119459232"><a name="p1549119459232"></a><a name="p1549119459232"></a>异常重试最大次数，单位：次/小时。取值范围：-1或大于0。默认值为“-1”，表示无限次数。</p>
</td>
</tr>
<tr id="row23271527124812"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="p432792704815"><a name="p432792704815"></a><a name="p432792704815"></a>static_estimator_config</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="p1432702717489"><a name="p1432702717489"></a><a name="p1432702717489"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="p12327182716481"><a name="p12327182716481"></a><a name="p12327182716481"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p1732815276486"><a name="p1732815276486"></a><a name="p1732815276486"></a>每个算子的流量/命中率配置，json格式的字符串。例如：</p>
<pre class="screen" id="screen113231649135711"><a name="screen113231649135711"></a><a name="screen113231649135711"></a>{"operator_list":[{"id":"0a448493b4782967b150582570326227","rate_factor":0.55},{"id":"6d2677a0ecc3fd8df0b72ec675edf8f4","rate_factor":1},{"id":"ea632d67b7d595e5b851708ae9ad79d6","rate_factor":0.55},{"id":"bc764cd8ddf7a0cff126f51c16239658","output_rate":2000}]}</pre>
</td>
</tr>
<tr id="row153693415915"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.5.1.1 "><p id="p95362034690"><a name="p95362034690"></a><a name="p95362034690"></a>runtime_config</p>
</td>
<td class="cellrowborder" valign="top" width="14.940000000000001%" headers="mcps1.2.5.1.2 "><p id="p165376345912"><a name="p165376345912"></a><a name="p165376345912"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.3 "><p id="p25373349919"><a name="p25373349919"></a><a name="p25373349919"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.5.1.4 "><p id="p1153712346915"><a name="p1153712346915"></a><a name="p1153712346915"></a>Flink作业运行时自定义优化参数。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="se2bf80cdb76541308f69f258ea4b1bd6"></a>

**表 3**  响应参数说明

<a name="table864065813431"></a>
<table><thead align="left"><tr id="row17641185813437"><th class="cellrowborder" valign="top" width="16.439999999999998%" id="mcps1.2.5.1.1"><p id="p1164195820435"><a name="p1164195820435"></a><a name="p1164195820435"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="12.46%" id="mcps1.2.5.1.2"><p id="p66412588434"><a name="p66412588434"></a><a name="p66412588434"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20.49%" id="mcps1.2.5.1.3"><p id="p9641458194311"><a name="p9641458194311"></a><a name="p9641458194311"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50.61%" id="mcps1.2.5.1.4"><p id="p186411358194312"><a name="p186411358194312"></a><a name="p186411358194312"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row2418154742"><td class="cellrowborder" valign="top" width="16.439999999999998%" headers="mcps1.2.5.1.1 "><p id="p10253165219311"><a name="p10253165219311"></a><a name="p10253165219311"></a>is_success</p>
</td>
<td class="cellrowborder" valign="top" width="12.46%" headers="mcps1.2.5.1.2 "><p id="p8253115273111"><a name="p8253115273111"></a><a name="p8253115273111"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20.49%" headers="mcps1.2.5.1.3 "><p id="p7253352153116"><a name="p7253352153116"></a><a name="p7253352153116"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="50.61%" headers="mcps1.2.5.1.4 "><p id="p8253152103110"><a name="p8253152103110"></a><a name="p8253152103110"></a>执行请求是否成功。“true”表示请求执行成功。</p>
</td>
</tr>
<tr id="row64180541741"><td class="cellrowborder" valign="top" width="16.439999999999998%" headers="mcps1.2.5.1.1 "><p id="p17641165884319"><a name="p17641165884319"></a><a name="p17641165884319"></a>message</p>
</td>
<td class="cellrowborder" valign="top" width="12.46%" headers="mcps1.2.5.1.2 "><p id="p1064295812435"><a name="p1064295812435"></a><a name="p1064295812435"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20.49%" headers="mcps1.2.5.1.3 "><p id="p4642058174318"><a name="p4642058174318"></a><a name="p4642058174318"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50.61%" headers="mcps1.2.5.1.4 "><p id="p146421758194310"><a name="p146421758194310"></a><a name="p146421758194310"></a>消息内容。</p>
</td>
</tr>
<tr id="row13575616163215"><td class="cellrowborder" valign="top" width="16.439999999999998%" headers="mcps1.2.5.1.1 "><p id="p1457691643219"><a name="p1457691643219"></a><a name="p1457691643219"></a>job</p>
</td>
<td class="cellrowborder" valign="top" width="12.46%" headers="mcps1.2.5.1.2 "><p id="p3576151610328"><a name="p3576151610328"></a><a name="p3576151610328"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20.49%" headers="mcps1.2.5.1.3 "><p id="p5576316153211"><a name="p5576316153211"></a><a name="p5576316153211"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50.61%" headers="mcps1.2.5.1.4 "><p id="p15761162327"><a name="p15761162327"></a><a name="p15761162327"></a>作业更新信息。具体请参考<a href="#table128621016345">表4</a>。</p>
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
<td class="cellrowborder" valign="top" width="47.43%" headers="mcps1.2.5.1.4 "><p id="p59012101344"><a name="p59012101344"></a><a name="p59012101344"></a>作业更新时间，毫秒数。</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section1141183661614"></a>

-   请求样例

    ```
    {
        "name": "myjob",
        "desc": "这是我的第一个作业",
        "queue_name": "testQueue",
        "sql_body": "select * from source_table",
        "run_mode": "shared_cluster",
        "cu_number": 4,
        "parallel_number": 4,
        "checkpoint_enabled": false,
        "checkpoint_mode": "exactly_once",
        "checkpoint_interval": 10,
        "obs_bucket": "",
        "log_enabled": false,
        "smn_topic": "",
        "restart_when_exception": false,
        "idle_state_retention": 3600,
        "edge_group_ids": [
            "62de1e1c-066e-48a8-a79d-f461a31b2ee1",
            "2eb00f85-99f2-4144-bcb7-d39ff47f9002"
        ],
        "dirty_data_strategy": "0",
        "udf_jar_url": "group/test.jar"
    }
    ```

-   响应样例

    ```
    {
        "is_success": "true",
        "message": "作业更新成功",
        "job": {
            "update_time": 1578905682534
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
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="af86844c7bb364c48b6300df1af164af2"><a name="af86844c7bb364c48b6300df1af164af2"></a><a name="af86844c7bb364c48b6300df1af164af2"></a>作业更新成功。</p>
</td>
</tr>
<tr id="row642813610440"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p104285674412"><a name="p104285674412"></a><a name="p104285674412"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p154287617445"><a name="p154287617445"></a><a name="p154287617445"></a>输入参数无效。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section13596141025715"></a>

调用接口出错后，将不会返回上述结果，而是返回错误码和错误信息，更多介绍请参见[错误码](错误码.md)。

