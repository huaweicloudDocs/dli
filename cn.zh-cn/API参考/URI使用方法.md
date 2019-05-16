# URI使用方法<a name="dli_02_0002"></a>

请求URI由如下部分组成。

**\{URI-scheme\} :// \{**Endpoint**\} / \{resource-path\} ? \{query-string\}**

尽管请求URI包含在请求消息头中，但大多数语言或框架都要求您从请求消息中单独传递它，所以我们在此单独拿出来强调。

URI中的参数说明如[表1](#t1797260c744a4e1a85d354f259cae55a)所示。

**表 1**  URI中的参数说明

<a name="t1797260c744a4e1a85d354f259cae55a"></a>
<table><thead align="left"><tr id="r6dceed05bcc649d2b032accbb2980a31"><th class="cellrowborder" valign="top" width="15.17%" id="mcps1.2.3.1.1"><p id="a3446b6b785cb432bae9f45aef9177041"><a name="a3446b6b785cb432bae9f45aef9177041"></a><a name="a3446b6b785cb432bae9f45aef9177041"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="84.83000000000001%" id="mcps1.2.3.1.2"><p id="abe71244a12ac45308e99d4bbf975a9f8"><a name="abe71244a12ac45308e99d4bbf975a9f8"></a><a name="abe71244a12ac45308e99d4bbf975a9f8"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row106982018513"><td class="cellrowborder" valign="top" width="15.17%" headers="mcps1.2.3.1.1 "><p id="p136991001517"><a name="p136991001517"></a><a name="p136991001517"></a>URI-scheme</p>
</td>
<td class="cellrowborder" valign="top" width="84.83000000000001%" headers="mcps1.2.3.1.2 "><p id="p56992017520"><a name="p56992017520"></a><a name="p56992017520"></a>表示用于传输请求的协议。DLI的API都必须采用https。</p>
</td>
</tr>
<tr id="rb217758afff146a1b40b0dcbb28a4ae1"><td class="cellrowborder" valign="top" width="15.17%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0035614179_p480227019422"><a name="zh-cn_topic_0035614179_p480227019422"></a><a name="zh-cn_topic_0035614179_p480227019422"></a>Endpoint</p>
</td>
<td class="cellrowborder" valign="top" width="84.83000000000001%" headers="mcps1.2.3.1.2 "><p id="ad82b3484a1be43ddadf436efbe15285e"><a name="ad82b3484a1be43ddadf436efbe15285e"></a><a name="ad82b3484a1be43ddadf436efbe15285e"></a>指定承载REST服务端点的服务器域名或IP，从<a href="https://developer.huaweicloud.com/endpoint?DLI" target="_blank" rel="noopener noreferrer">地区和终端节点</a>中获取。</p>
</td>
</tr>
<tr id="refeed61892004ea682639be281a1a707"><td class="cellrowborder" valign="top" width="15.17%" headers="mcps1.2.3.1.1 "><p id="p1797614317513"><a name="p1797614317513"></a><a name="p1797614317513"></a>resource-path</p>
</td>
<td class="cellrowborder" valign="top" width="84.83000000000001%" headers="mcps1.2.3.1.2 "><p id="a90409cbb8b1c49c4ad4d3cfee16f475e"><a name="a90409cbb8b1c49c4ad4d3cfee16f475e"></a><a name="a90409cbb8b1c49c4ad4d3cfee16f475e"></a>资源路径，即API访问路径。从具体接口的URI模块获取，例如“v3/auth/tokens”。</p>
</td>
</tr>
<tr id="row19939365518"><td class="cellrowborder" valign="top" width="15.17%" headers="mcps1.2.3.1.1 "><p id="p393966455"><a name="p393966455"></a><a name="p393966455"></a>Query string</p>
</td>
<td class="cellrowborder" valign="top" width="84.83000000000001%" headers="mcps1.2.3.1.2 "><p id="p159401867517"><a name="p159401867517"></a><a name="p159401867517"></a>可选参数，例如API版本或资源选择标准。</p>
</td>
</tr>
</tbody>
</table>

