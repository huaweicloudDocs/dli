# 使用JDBC连接服务端<a name="dli_01_0225"></a>

## 操作场景<a name="section4984415014219"></a>

在Linux或Windows环境下您可以使用JDBC应用程序连接DLI服务服务端。

DLI支持13种数据类型，每一种类型都可以映射成一种JDBC类型，在使用JDBC连接服务器时，请使用映射后的JAVA类型，映射关系如[表1](#table74891852105113)所示。 

**表 1**  数据类型映射

<a name="table74891852105113"></a>
<table><thead align="left"><tr id="row145045529518"><th class="cellrowborder" valign="top" width="33.083308330833084%" id="mcps1.2.4.1.1"><p id="p7506185265115"><a name="p7506185265115"></a><a name="p7506185265115"></a>DLI类型</p>
</th>
<th class="cellrowborder" valign="top" width="33.83338333833383%" id="mcps1.2.4.1.2"><p id="p2050825215515"><a name="p2050825215515"></a><a name="p2050825215515"></a>JDBC类型</p>
</th>
<th class="cellrowborder" valign="top" width="33.083308330833084%" id="mcps1.2.4.1.3"><p id="p11512135215118"><a name="p11512135215118"></a><a name="p11512135215118"></a>JAVA类型</p>
</th>
</tr>
</thead>
<tbody><tr id="row13515105235119"><td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.1 "><p id="p14519205235114"><a name="p14519205235114"></a><a name="p14519205235114"></a>INT</p>
</td>
<td class="cellrowborder" valign="top" width="33.83338333833383%" headers="mcps1.2.4.1.2 "><p id="p152114529514"><a name="p152114529514"></a><a name="p152114529514"></a>INTEGER</p>
</td>
<td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.3 "><p id="p10524115215110"><a name="p10524115215110"></a><a name="p10524115215110"></a>java.lang.Integer</p>
</td>
</tr>
<tr id="row17525152135110"><td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.1 "><p id="p45281652195112"><a name="p45281652195112"></a><a name="p45281652195112"></a>STRING</p>
</td>
<td class="cellrowborder" valign="top" width="33.83338333833383%" headers="mcps1.2.4.1.2 "><p id="p753135225113"><a name="p753135225113"></a><a name="p753135225113"></a>VARCHAR</p>
</td>
<td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.3 "><p id="p1953512526518"><a name="p1953512526518"></a><a name="p1953512526518"></a>java.lang.String</p>
</td>
</tr>
<tr id="row1853685210514"><td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.1 "><p id="p175397521512"><a name="p175397521512"></a><a name="p175397521512"></a>FLOAT</p>
</td>
<td class="cellrowborder" valign="top" width="33.83338333833383%" headers="mcps1.2.4.1.2 "><p id="p17541552125114"><a name="p17541552125114"></a><a name="p17541552125114"></a>FLOAT</p>
</td>
<td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.3 "><p id="p1354419526519"><a name="p1354419526519"></a><a name="p1354419526519"></a>java.lang.Float</p>
</td>
</tr>
<tr id="row13545952205110"><td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.1 "><p id="p0549185295115"><a name="p0549185295115"></a><a name="p0549185295115"></a>DOUBLE</p>
</td>
<td class="cellrowborder" valign="top" width="33.83338333833383%" headers="mcps1.2.4.1.2 "><p id="p1255115529512"><a name="p1255115529512"></a><a name="p1255115529512"></a>DOUBLE</p>
</td>
<td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.3 "><p id="p1855413529511"><a name="p1855413529511"></a><a name="p1855413529511"></a>java.lang.Double</p>
</td>
</tr>
<tr id="row3555252145110"><td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.1 "><p id="p1557105213511"><a name="p1557105213511"></a><a name="p1557105213511"></a>DECIMAL</p>
</td>
<td class="cellrowborder" valign="top" width="33.83338333833383%" headers="mcps1.2.4.1.2 "><p id="p1156085214511"><a name="p1156085214511"></a><a name="p1156085214511"></a>DECIMAL</p>
</td>
<td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.3 "><p id="p185631552175118"><a name="p185631552175118"></a><a name="p185631552175118"></a>java.math.BigDecimal</p>
</td>
</tr>
<tr id="row456475215515"><td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.1 "><p id="p13566115216519"><a name="p13566115216519"></a><a name="p13566115216519"></a>BOOLEAN</p>
</td>
<td class="cellrowborder" valign="top" width="33.83338333833383%" headers="mcps1.2.4.1.2 "><p id="p15681852145112"><a name="p15681852145112"></a><a name="p15681852145112"></a>BOOLEAN</p>
</td>
<td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.3 "><p id="p7570165218518"><a name="p7570165218518"></a><a name="p7570165218518"></a>java.lang.Boolean</p>
</td>
</tr>
<tr id="row35721652135120"><td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.1 "><p id="p1257415211512"><a name="p1257415211512"></a><a name="p1257415211512"></a>SMALLINT/SHORT</p>
</td>
<td class="cellrowborder" valign="top" width="33.83338333833383%" headers="mcps1.2.4.1.2 "><p id="p05751752155115"><a name="p05751752155115"></a><a name="p05751752155115"></a>SMALLINT</p>
</td>
<td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.3 "><p id="p14578052135119"><a name="p14578052135119"></a><a name="p14578052135119"></a>java.lang.Short</p>
</td>
</tr>
<tr id="row18580155285116"><td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.1 "><p id="p11583175295113"><a name="p11583175295113"></a><a name="p11583175295113"></a>TINYINT</p>
</td>
<td class="cellrowborder" valign="top" width="33.83338333833383%" headers="mcps1.2.4.1.2 "><p id="p9585155213512"><a name="p9585155213512"></a><a name="p9585155213512"></a>TINYINT</p>
</td>
<td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.3 "><p id="p958835285110"><a name="p958835285110"></a><a name="p958835285110"></a>java.lang.Short</p>
</td>
</tr>
<tr id="row35897527518"><td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.1 "><p id="p659115220512"><a name="p659115220512"></a><a name="p659115220512"></a>BIGINT/LONG</p>
</td>
<td class="cellrowborder" valign="top" width="33.83338333833383%" headers="mcps1.2.4.1.2 "><p id="p125931052115110"><a name="p125931052115110"></a><a name="p125931052115110"></a>BIGINT</p>
</td>
<td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.3 "><p id="p195961852185115"><a name="p195961852185115"></a><a name="p195961852185115"></a>java.lang.Long</p>
</td>
</tr>
<tr id="row1359785210512"><td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.1 "><p id="p65991652135119"><a name="p65991652135119"></a><a name="p65991652135119"></a>TIMESTAMP</p>
</td>
<td class="cellrowborder" valign="top" width="33.83338333833383%" headers="mcps1.2.4.1.2 "><p id="p76021252155115"><a name="p76021252155115"></a><a name="p76021252155115"></a>TIMESTAMP</p>
</td>
<td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.3 "><p id="p10605125285116"><a name="p10605125285116"></a><a name="p10605125285116"></a>java.sql.Timestamp</p>
</td>
</tr>
<tr id="row16607352145111"><td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.1 "><p id="p146090526517"><a name="p146090526517"></a><a name="p146090526517"></a>CHAR</p>
</td>
<td class="cellrowborder" valign="top" width="33.83338333833383%" headers="mcps1.2.4.1.2 "><p id="p9614115213512"><a name="p9614115213512"></a><a name="p9614115213512"></a>CHAR</p>
</td>
<td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.3 "><p id="p1561610523516"><a name="p1561610523516"></a><a name="p1561610523516"></a>Java.lang.Character</p>
</td>
</tr>
<tr id="row96178529512"><td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.1 "><p id="p156196521516"><a name="p156196521516"></a><a name="p156196521516"></a>VARCHAR</p>
</td>
<td class="cellrowborder" valign="top" width="33.83338333833383%" headers="mcps1.2.4.1.2 "><p id="p0621165255117"><a name="p0621165255117"></a><a name="p0621165255117"></a>VARCHAR</p>
</td>
<td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.3 "><p id="p9624135275119"><a name="p9624135275119"></a><a name="p9624135275119"></a>java.lang.String</p>
</td>
</tr>
<tr id="row186271252195117"><td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.1 "><p id="p1563165214515"><a name="p1563165214515"></a><a name="p1563165214515"></a>DATE</p>
</td>
<td class="cellrowborder" valign="top" width="33.83338333833383%" headers="mcps1.2.4.1.2 "><p id="p6635195218515"><a name="p6635195218515"></a><a name="p6635195218515"></a>DATE</p>
</td>
<td class="cellrowborder" valign="top" width="33.083308330833084%" headers="mcps1.2.4.1.3 "><p id="p16381152185115"><a name="p16381152185115"></a><a name="p16381152185115"></a>java.sql.Date</p>
</td>
</tr>
</tbody>
</table>

## 操作步骤<a name="section51761783175346"></a>

1.  在使用JDBC的机器中安装JDK，JDK版本为1.7或以上版本，并配置环境变量。
2.  参考[下载JDBC或ODBC驱动包](下载JDBC或ODBC驱动包.md)章节，获取DLI JDBC驱动包“huaweicloud-dli-jdbc-<version\>.zip”，解压，获得“huaweicloud-dli-jdbc-<version\>-jar-with-dependencies.jar”。
3.  在使用JDBC的机器中，将“huaweicloud-dli-jdbc-1.1.1-jar-with-dependencies.jar”添加至Java工程的“classpath“路径下。
4.  DLI JDBC提供两种身份认证模式连接到DLI服务，即Token和AK/SK。获取Token和AK/SK的方法请参见[认证](认证.md)。
5.  使用Class.forName（）加载DLI JDBC驱动程序。

    **Class.forName\("com.huawei.dli.jdbc.DliDriver"\);**

6.  通过DriverManager的GetConnection方法创建Connection。

    **Connection conn = DriverManager.getConnection\(String url, Properties info\);**

    其中JDBC的配置项通过url传入，请参考[表2](#table7064698105347)配置参数。JDBC配置对象，除了在url中以分号间隔设置配置项外，还可以通过Info对象动态设置属性项，具体属性项参见[表3](#table31567601152339)。 

    **表 2**  数据库连接参数

    <a name="table7064698105347"></a>
    <table><thead align="left"><tr id="row65073311105347"><th class="cellrowborder" valign="top" width="24.25%" id="mcps1.2.3.1.1"><p id="p59586123105347"><a name="p59586123105347"></a><a name="p59586123105347"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="75.75%" id="mcps1.2.3.1.2"><p id="p61746676105347"><a name="p61746676105347"></a><a name="p61746676105347"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row18849173105347"><td class="cellrowborder" valign="top" width="24.25%" headers="mcps1.2.3.1.1 "><p id="p50388005105347"><a name="p50388005105347"></a><a name="p50388005105347"></a>url</p>
    </td>
    <td class="cellrowborder" valign="top" width="75.75%" headers="mcps1.2.3.1.2 "><p id="p54896577105347"><a name="p54896577105347"></a><a name="p54896577105347"></a>url的格式如下。</p>
    <p id="p59619235143640"><a name="p59619235143640"></a><a name="p59619235143640"></a>jdbc:dli://&lt;endPoint&gt;/projectId? &lt;key1&gt;=&lt;val1&gt;;&lt;key2&gt;=&lt;val2&gt;…</p>
    <a name="ul079115391211"></a><a name="ul079115391211"></a><ul id="ul079115391211"><li>endpoint指DLI的域名。projectId指项目ID。在<a href="https://developer.huaweicloud.com/endpoint" target="_blank" rel="noopener noreferrer">地区和终端节点</a>获取DLI对应的Endpoint，从公有云“用户名”&gt;“我的凭证”页面获取项目编号。</li><li><span class="parmname" id="parmname11811939422"><a name="parmname11811939422"></a><a name="parmname11811939422"></a>“？”</span>后面接其他配置项，每个配置项以<span class="parmname" id="parmname198134391527"><a name="parmname198134391527"></a><a name="parmname198134391527"></a>“key=value”</span>的形式列出，配置项之间以<span class="parmname" id="parmname18157391211"><a name="parmname18157391211"></a><a name="parmname18157391211"></a>“;”</span>隔开，这些配置项也可以通过Info对象传入。</li></ul>
    </td>
    </tr>
    <tr id="row24307152105347"><td class="cellrowborder" valign="top" width="24.25%" headers="mcps1.2.3.1.1 "><p id="p22722282105347"><a name="p22722282105347"></a><a name="p22722282105347"></a>Info</p>
    </td>
    <td class="cellrowborder" valign="top" width="75.75%" headers="mcps1.2.3.1.2 "><p id="p54391264144914"><a name="p54391264144914"></a><a name="p54391264144914"></a>Info传入自定义的配置项,若Info没有属性项传入，可设为null。配置格式为：info.setProperty("属性项", "属性值")。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  属性项

    <a name="table31567601152339"></a>
    <table><thead align="left"><tr id="row36532279152339"><th class="cellrowborder" valign="top" width="22.222222222222225%" id="mcps1.2.5.1.1"><p id="p27119155155349"><a name="p27119155155349"></a><a name="p27119155155349"></a>属性项</p>
    </th>
    <th class="cellrowborder" valign="top" width="22.222222222222225%" id="mcps1.2.5.1.2"><p id="p49167942155349"><a name="p49167942155349"></a><a name="p49167942155349"></a>必须配置</p>
    </th>
    <th class="cellrowborder" valign="top" width="10.101010101010102%" id="mcps1.2.5.1.3"><p id="p23180374155349"><a name="p23180374155349"></a><a name="p23180374155349"></a>默认值</p>
    </th>
    <th class="cellrowborder" valign="top" width="45.45454545454546%" id="mcps1.2.5.1.4"><p id="p65670986155349"><a name="p65670986155349"></a><a name="p65670986155349"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row30320199152339"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p26912549155542"><a name="p26912549155542"></a><a name="p26912549155542"></a>queuename</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.2 "><p id="p32432850155542"><a name="p32432850155542"></a><a name="p32432850155542"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.101010101010102%" headers="mcps1.2.5.1.3 "><p id="p9815175155542"><a name="p9815175155542"></a><a name="p9815175155542"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.45454545454546%" headers="mcps1.2.5.1.4 "><p id="p56831725155542"><a name="p56831725155542"></a><a name="p56831725155542"></a>DLI服务的队列名称。</p>
    </td>
    </tr>
    <tr id="row63719185152339"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p24158859155542"><a name="p24158859155542"></a><a name="p24158859155542"></a>databasename</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.2 "><p id="p10710594155542"><a name="p10710594155542"></a><a name="p10710594155542"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.101010101010102%" headers="mcps1.2.5.1.3 "><p id="p62251748155542"><a name="p62251748155542"></a><a name="p62251748155542"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.45454545454546%" headers="mcps1.2.5.1.4 "><p id="p9226843155542"><a name="p9226843155542"></a><a name="p9226843155542"></a>数据库名称。</p>
    </td>
    </tr>
    <tr id="row36990844152339"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p15482763155542"><a name="p15482763155542"></a><a name="p15482763155542"></a>authenticationmode</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.2 "><p id="p46144292155542"><a name="p46144292155542"></a><a name="p46144292155542"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.101010101010102%" headers="mcps1.2.5.1.3 "><p id="p46700206155542"><a name="p46700206155542"></a><a name="p46700206155542"></a>token</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.45454545454546%" headers="mcps1.2.5.1.4 "><p id="p24620369155542"><a name="p24620369155542"></a><a name="p24620369155542"></a>身份认证方式，当前支持两种：token或aksk。</p>
    </td>
    </tr>
    <tr id="row49918453152339"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p30182485155542"><a name="p30182485155542"></a><a name="p30182485155542"></a>accesskey</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.2 "><p id="p28862203155542"><a name="p28862203155542"></a><a name="p28862203155542"></a>authenticationmode=aksk时必须配置</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.101010101010102%" headers="mcps1.2.5.1.3 "><p id="p56137143155542"><a name="p56137143155542"></a><a name="p56137143155542"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.45454545454546%" headers="mcps1.2.5.1.4 "><p id="p50814702155542"><a name="p50814702155542"></a><a name="p50814702155542"></a>AK/SK认证密钥，获取方式请参考<a href="认证.md">认证</a>。</p>
    </td>
    </tr>
    <tr id="row42867189152339"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p66934242155542"><a name="p66934242155542"></a><a name="p66934242155542"></a>secretkey</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.2 "><p id="p52964496155542"><a name="p52964496155542"></a><a name="p52964496155542"></a>authenticationmode=aksk时必须配置</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.101010101010102%" headers="mcps1.2.5.1.3 "><p id="p62265750155542"><a name="p62265750155542"></a><a name="p62265750155542"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.45454545454546%" headers="mcps1.2.5.1.4 "><p id="p10360989155542"><a name="p10360989155542"></a><a name="p10360989155542"></a>AK/SK认证密钥，获取方式请参考<a href="认证.md">认证</a>。</p>
    </td>
    </tr>
    <tr id="row26132409152339"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p36968499155542"><a name="p36968499155542"></a><a name="p36968499155542"></a>regionname</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.2 "><p id="p41658418155542"><a name="p41658418155542"></a><a name="p41658418155542"></a>authenticationmode=aksk时必须配置</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.101010101010102%" headers="mcps1.2.5.1.3 "><p id="p18888686155542"><a name="p18888686155542"></a><a name="p18888686155542"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.45454545454546%" headers="mcps1.2.5.1.4 "><p id="p221544815249"><a name="p221544815249"></a><a name="p221544815249"></a>区域名称，获取方式请参考<a href="认证.md">认证</a>。</p>
    </td>
    </tr>
    <tr id="row45735434152339"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p8700049155542"><a name="p8700049155542"></a><a name="p8700049155542"></a>servicename</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.2 "><p id="p33615355155542"><a name="p33615355155542"></a><a name="p33615355155542"></a>authenticationmode=aksk时必须配置</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.101010101010102%" headers="mcps1.2.5.1.3 "><p id="p38489254155542"><a name="p38489254155542"></a><a name="p38489254155542"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.45454545454546%" headers="mcps1.2.5.1.4 "><p id="p30621882155542"><a name="p30621882155542"></a><a name="p30621882155542"></a>服务名称，获取方式请参考<a href="认证.md">认证</a>。</p>
    </td>
    </tr>
    <tr id="row13967320155445"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p43209165155542"><a name="p43209165155542"></a><a name="p43209165155542"></a>token</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.2 "><p id="p10281485155542"><a name="p10281485155542"></a><a name="p10281485155542"></a>authenticationmode=token时必须配置</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.101010101010102%" headers="mcps1.2.5.1.3 "><p id="p27493937155542"><a name="p27493937155542"></a><a name="p27493937155542"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.45454545454546%" headers="mcps1.2.5.1.4 "><p id="p12416418155542"><a name="p12416418155542"></a><a name="p12416418155542"></a>Token认证，认证方式请参考<a href="认证.md">认证</a>。</p>
    </td>
    </tr>
    <tr id="row53630162155451"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p58980992155542"><a name="p58980992155542"></a><a name="p58980992155542"></a>charset</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.2 "><p id="p12731087155542"><a name="p12731087155542"></a><a name="p12731087155542"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.101010101010102%" headers="mcps1.2.5.1.3 "><p id="p24585159155542"><a name="p24585159155542"></a><a name="p24585159155542"></a>UTF-8</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.45454545454546%" headers="mcps1.2.5.1.4 "><p id="p45240847155542"><a name="p45240847155542"></a><a name="p45240847155542"></a>JDBC编码方式。</p>
    </td>
    </tr>
    <tr id="row37026246155458"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p30125388155542"><a name="p30125388155542"></a><a name="p30125388155542"></a>usehttpproxy</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.2 "><p id="p24237364155542"><a name="p24237364155542"></a><a name="p24237364155542"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.101010101010102%" headers="mcps1.2.5.1.3 "><p id="p17069481155542"><a name="p17069481155542"></a><a name="p17069481155542"></a>false</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.45454545454546%" headers="mcps1.2.5.1.4 "><p id="p40450706155542"><a name="p40450706155542"></a><a name="p40450706155542"></a>是否使用访问代理。</p>
    </td>
    </tr>
    <tr id="row2933267015554"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p27773721155542"><a name="p27773721155542"></a><a name="p27773721155542"></a>proxyhost</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.2 "><p id="p35078900155542"><a name="p35078900155542"></a><a name="p35078900155542"></a>usehttpproxy=true时必须配置</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.101010101010102%" headers="mcps1.2.5.1.3 "><p id="p22818656155542"><a name="p22818656155542"></a><a name="p22818656155542"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.45454545454546%" headers="mcps1.2.5.1.4 "><p id="p36371844155542"><a name="p36371844155542"></a><a name="p36371844155542"></a>访问代理host。</p>
    </td>
    </tr>
    <tr id="row46965394155514"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p7073623155542"><a name="p7073623155542"></a><a name="p7073623155542"></a>proxyport</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.2 "><p id="p36092624155542"><a name="p36092624155542"></a><a name="p36092624155542"></a>usehttpproxy=true时必须配置</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.101010101010102%" headers="mcps1.2.5.1.3 "><p id="p37821437155542"><a name="p37821437155542"></a><a name="p37821437155542"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.45454545454546%" headers="mcps1.2.5.1.4 "><p id="p43637575155542"><a name="p43637575155542"></a><a name="p43637575155542"></a>访问代理端口。</p>
    </td>
    </tr>
    <tr id="row137821327122215"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p17881427172216"><a name="p17881427172216"></a><a name="p17881427172216"></a>dli.sql.checkNoResultQuery</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.2 "><p id="p17788142792217"><a name="p17788142792217"></a><a name="p17788142792217"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.101010101010102%" headers="mcps1.2.5.1.3 "><p id="p87882027132219"><a name="p87882027132219"></a><a name="p87882027132219"></a>false</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.45454545454546%" headers="mcps1.2.5.1.4 "><p id="p9148172623514"><a name="p9148172623514"></a><a name="p9148172623514"></a>是否允许调用executeQuery接口执行没有返回结果的语句（如DDL）。</p>
    <a name="ul564813417352"></a><a name="ul564813417352"></a><ul id="ul564813417352"><li>“false”表示允许调用。</li><li>“true”表示不允许调用。</li></ul>
    </td>
    </tr>
    <tr id="row13949192314125"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p18950132351218"><a name="p18950132351218"></a><a name="p18950132351218"></a>jobtimeout</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.2 "><p id="p595032371216"><a name="p595032371216"></a><a name="p595032371216"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="10.101010101010102%" headers="mcps1.2.5.1.3 "><p id="p995072311210"><a name="p995072311210"></a><a name="p995072311210"></a>300</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.45454545454546%" headers="mcps1.2.5.1.4 "><p id="p89501323171218"><a name="p89501323171218"></a><a name="p89501323171218"></a>提交作业终止时间，单位：秒。</p>
    </td>
    </tr>
    </tbody>
    </table>

7.  创建Statement对象并提交SQL到DLI服务。

    **Statement statement = conn.createStatement\(\);**

    **statement.execute\("select \* from tb1"\);**

8.  获取结果。

    **ResultSet rs = statement.getResultSet\(\);**

9.  显示结果。

    ```
    while (rs.next()) {
    int a = rs.getInt(1);
    int b = rs.getInt(2);
    }
    ```

10. 关闭连接。

    **conn.close\(\);**


## 示例<a name="section4858632153443"></a>

```
import java.sql.*;
import java.util.Properties;

public class DLIJdbcDriverExample {

    private static final String X_AUTH_TOKEN_VALUE = "<realtoken>";
    public static void main(String[] args) throws ClassNotFoundException, SQLException {
        Connection conn = null;
        try {
            Class.forName("com.huawei.dli.jdbc.DliDriver");
            String url = "jdbc:dli://<endpoint>/<projectId>?databasename=db1;queuename=testqueue";
            Properties info = new Properties();
            info.setProperty("token", X_AUTH_TOKEN_VALUE);
            conn = DriverManager.getConnection(url, info);
            Statement statement = conn.createStatement();
            statement.execute("select * from tb1");
            ResultSet rs = statement.getResultSet();
            int line = 0;
            while (rs.next()) {
                line ++;
                int a = rs.getInt(1);
                int b = rs.getInt(2);
                System.out.println("Line:" + line + ":" + a + "," + b);
            }
            statement.execute("describe tb1");
            ResultSet rs1 = statement.getResultSet();
            line = 0;
            while (rs1.next()) {
                line ++;
                String a = rs1.getString(1);
                String b = rs1.getString(2);
                System.out.println("Line:" + line + ":" + a + "," + b);
            }
        } catch (SQLException ex) {
        } finally {
            if (conn != null) {
                conn.close();
            }
        }
    }
}
```

