# 永洪BI添加数据源<a name="dli_01_0233"></a>

## 操作场景<a name="section26616723151647"></a>

在永洪SaaS生产环境中添加DLI的数据源。

## 操作步骤<a name="section42550629162142"></a>

1.  在永洪SaaS生产环境主页，单击左侧导航栏中的“添加数据源”，请参见[图1](#fig276520981542)。

    **图 1**  添加数据源<a name="fig276520981542"></a>  
    ![](figures/添加数据源.png "添加数据源")

2.  “选择数据源类型”页面中，新建数据源类型选择“GENERIC”。请参见[图2](#fig697408381542)。

    **图 2**  选择数据源类型<a name="fig697408381542"></a>  
    ![](figures/选择数据源类型.png "选择数据源类型")

3.  添加数据源的相关配置，请参见[图3](#fig3754626481542)。

    “驱动“栏填写DLI JDBC的驱动：com.huawei.dli.jdbc.DliDriver。

    “URL“ 栏选择“自定义协议“，后面填写DLI jdbc的URL，URL的格式见[表1](#table1128019181542)，属性配置项说明见[表2](#table3788775181542)。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >-   “表结构模式“可填写需访问的数据库名称，如果填写，后续创建数据集时，刷新表，页面上只可见该数据库下的表。如果不填写，后续创建数据集时，刷新表，页面上会显示所有数据库下的表。创建数据集请参考[永洪BI创建数据集](永洪BI创建数据集.md)。  
    >-   其他选项不需要填写，也无需勾选“需要登录”选项。  

    **图 3**  添加数据源配置<a name="fig3754626481542"></a>  
    ![](figures/添加数据源配置.png "添加数据源配置")

    **表 1**  数据库连接参数

    <a name="table1128019181542"></a>
    <table><thead align="left"><tr id="row968146681542"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p5151195281542"><a name="p5151195281542"></a><a name="p5151195281542"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p1171858781542"><a name="p1171858781542"></a><a name="p1171858781542"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row3370798981542"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p4600127081542"><a name="p4600127081542"></a><a name="p4600127081542"></a>URL</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p3511535081542"><a name="p3511535081542"></a><a name="p3511535081542"></a>URL的格式如下。</p>
    <p id="p708227581542"><a name="p708227581542"></a><a name="p708227581542"></a><strong id="b6522801516319"><a name="b6522801516319"></a><a name="b6522801516319"></a><em id="i5018122416319"><a name="i5018122416319"></a><a name="i5018122416319"></a>jdbc:dli://&lt;endPoint&gt;/&lt;projectId&gt;?&lt;key1&gt;=&lt;val1&gt;;&lt;key2&gt;=&lt;val2&gt;</em><em id="i2577107481542"><a name="i2577107481542"></a><a name="i2577107481542"></a>…</em></strong></p>
    <div class="note" id="note1118670681542"><a name="note1118670681542"></a><a name="note1118670681542"></a><span class="notetitle"> NOTE: </span><div class="notebody"><a name="ul4598221081542"></a><a name="ul4598221081542"></a><ul id="ul4598221081542"><li>endpoint指DLI的域名，具体请参考<a href="https://developer.huaweicloud.com/endpoint" target="_blank" rel="noopener noreferrer">地区和终端节点</a>。</li><li>projectId指项目编号，从公有云“基本信息&gt;我的凭证”页面获取项编号。</li><li>“？”后面接其他配置项，每个配置项以“key=value”的形式列出，配置项之间以“;”隔开，详见<a href="#dli_01_0233__table3788775181542">表2</a></li></ul>
    </div></div>
    </td>
    </tr>
    </tbody>
    </table>

    **表 2**  属性配置项

    <a name="table3788775181542"></a>
    <table><thead align="left"><tr id="row863464781542"><th class="cellrowborder" valign="top" width="22%" id="mcps1.2.5.1.1"><p id="p5552404081542"><a name="p5552404081542"></a><a name="p5552404081542"></a>属性项（key）</p>
    </th>
    <th class="cellrowborder" valign="top" width="23%" id="mcps1.2.5.1.2"><p id="p115343181542"><a name="p115343181542"></a><a name="p115343181542"></a>必须配置</p>
    </th>
    <th class="cellrowborder" valign="top" width="12%" id="mcps1.2.5.1.3"><p id="p2631911981542"><a name="p2631911981542"></a><a name="p2631911981542"></a>默认值（value）</p>
    </th>
    <th class="cellrowborder" valign="top" width="43%" id="mcps1.2.5.1.4"><p id="p5147387981542"><a name="p5147387981542"></a><a name="p5147387981542"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row5183638581542"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.1 "><p id="p2831781681542"><a name="p2831781681542"></a><a name="p2831781681542"></a>queuename</p>
    </td>
    <td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.5.1.2 "><p id="p1204176181542"><a name="p1204176181542"></a><a name="p1204176181542"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.5.1.3 "><p id="p3585861981542"><a name="p3585861981542"></a><a name="p3585861981542"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="43%" headers="mcps1.2.5.1.4 "><p id="p1886705481542"><a name="p1886705481542"></a><a name="p1886705481542"></a>DLI服务的队列名称。</p>
    </td>
    </tr>
    <tr id="row540118381542"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.1 "><p id="p6387428281542"><a name="p6387428281542"></a><a name="p6387428281542"></a>databasename</p>
    </td>
    <td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.5.1.2 "><p id="p643433681542"><a name="p643433681542"></a><a name="p643433681542"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.5.1.3 "><p id="p5141924481542"><a name="p5141924481542"></a><a name="p5141924481542"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="43%" headers="mcps1.2.5.1.4 "><p id="p420920381542"><a name="p420920381542"></a><a name="p420920381542"></a>默认访问的数据库，URL中若不填此项，访问数据库的表时需采用db.table方式（如 select * from dbother.tabletest）。</p>
    </td>
    </tr>
    <tr id="row3788276181542"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.1 "><p id="p4861065581542"><a name="p4861065581542"></a><a name="p4861065581542"></a>authenticationmode</p>
    </td>
    <td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.5.1.2 "><p id="p4514895781542"><a name="p4514895781542"></a><a name="p4514895781542"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.5.1.3 "><p id="p3318686781542"><a name="p3318686781542"></a><a name="p3318686781542"></a>token</p>
    </td>
    <td class="cellrowborder" valign="top" width="43%" headers="mcps1.2.5.1.4 "><p id="p378170681542"><a name="p378170681542"></a><a name="p378170681542"></a>身份认证方式，可以是token或aksk，永洪BI对接建议采用aksk认证方式。</p>
    </td>
    </tr>
    <tr id="row1841039881542"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.1 "><p id="p540053681542"><a name="p540053681542"></a><a name="p540053681542"></a>accesskey</p>
    </td>
    <td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.5.1.2 "><p id="p3479024781542"><a name="p3479024781542"></a><a name="p3479024781542"></a>authenticationmode=aksk时必须配置</p>
    </td>
    <td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.5.1.3 "><p id="p6654661181542"><a name="p6654661181542"></a><a name="p6654661181542"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="43%" headers="mcps1.2.5.1.4 "><p id="p5987961281542"><a name="p5987961281542"></a><a name="p5987961281542"></a>参考<a href="永洪BI对接准备工作.md">永洪BI对接准备工作</a>。</p>
    </td>
    </tr>
    <tr id="row2363432781542"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.1 "><p id="p3147585681542"><a name="p3147585681542"></a><a name="p3147585681542"></a>secretkey</p>
    </td>
    <td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.5.1.2 "><p id="p6651644681542"><a name="p6651644681542"></a><a name="p6651644681542"></a>authenticationmode=aksk时必须配置</p>
    </td>
    <td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.5.1.3 "><p id="p1912305681542"><a name="p1912305681542"></a><a name="p1912305681542"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="43%" headers="mcps1.2.5.1.4 "><p id="p4917354681542"><a name="p4917354681542"></a><a name="p4917354681542"></a>参考<a href="永洪BI对接准备工作.md">永洪BI对接准备工作</a>。</p>
    </td>
    </tr>
    <tr id="row4106431681542"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.1 "><p id="p1138235481542"><a name="p1138235481542"></a><a name="p1138235481542"></a>regionname</p>
    </td>
    <td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.5.1.2 "><p id="p4955546281542"><a name="p4955546281542"></a><a name="p4955546281542"></a>authenticationmode=aksk时必须配置</p>
    </td>
    <td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.5.1.3 "><p id="p5456947981542"><a name="p5456947981542"></a><a name="p5456947981542"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="43%" headers="mcps1.2.5.1.4 "><p id="p5270274981542"><a name="p5270274981542"></a><a name="p5270274981542"></a>具体请参考http://developer.huaweicloud.com/dev/endpoint。</p>
    </td>
    </tr>
    <tr id="row1800290281542"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.1 "><p id="p3403453281542"><a name="p3403453281542"></a><a name="p3403453281542"></a>servicename</p>
    </td>
    <td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.5.1.2 "><p id="p533367081542"><a name="p533367081542"></a><a name="p533367081542"></a>authenticationmode=aksk时必须配置</p>
    </td>
    <td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.5.1.3 "><p id="p2937414181542"><a name="p2937414181542"></a><a name="p2937414181542"></a>-</p>
    </td>
    <td class="cellrowborder" valign="top" width="43%" headers="mcps1.2.5.1.4 "><p id="p602178981542"><a name="p602178981542"></a><a name="p602178981542"></a>由于是对接DLI，所以servicename=dli。</p>
    </td>
    </tr>
    <tr id="row1747364324213"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.1 "><p id="p17881427172216"><a name="p17881427172216"></a><a name="p17881427172216"></a>dli.sql.checkNoResultQuery</p>
    </td>
    <td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.5.1.2 "><p id="p17788142792217"><a name="p17788142792217"></a><a name="p17788142792217"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.5.1.3 "><p id="p87882027132219"><a name="p87882027132219"></a><a name="p87882027132219"></a>false</p>
    </td>
    <td class="cellrowborder" valign="top" width="43%" headers="mcps1.2.5.1.4 "><p id="p1948134194414"><a name="p1948134194414"></a><a name="p1948134194414"></a>是否允许调用executeQuery接口执行没有返回结果的语句（如DDL）。</p>
    <a name="ul1147419597345"></a><a name="ul1147419597345"></a><ul id="ul1147419597345"><li>“false”表示允许调用。</li><li>“true”表示不允许调用。</li></ul>
    <div class="note" id="note775915164312"><a name="note775915164312"></a><a name="note775915164312"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="p6759131614316"><a name="p6759131614316"></a><a name="p6759131614316"></a>当dli.sql.checkNoResultQuery=false时，非查询语句会执行两次。</p>
    </div></div>
    </td>
    </tr>
    </tbody>
    </table>

4.  在“添加数据源配置”页面工具栏中单击“测试连接”，测试通过后，单击“保存”，填写数据源名称，保存该数据源。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >目前没有根目录保存权限，需保存到已建文件夹目录下。  


