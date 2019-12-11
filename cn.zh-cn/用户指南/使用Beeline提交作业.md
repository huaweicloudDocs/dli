# 使用Beeline提交作业<a name="dli_01_0276"></a>

## DLI Beeline简介<a name="section159401845155918"></a>

DLI Beeline是一个用于连接DLI服务的客户端命令行交互工具，该工具基于DLI JDBC实现，提供SQL命令交互和批量SQL脚本执行的功能。

## DLI 客户端工具下载<a name="section17581174216018"></a>

您可以在DLI管理控制台下载DLI客户端工具。

1.  登录DLI管理控制台。
2.  单击总览页右侧“常用链接”中的“[SDK下载](https://uquery-sdk.obs-website.cn-north-1.myhuaweicloud.com/)”。
3.  在“DLI SDK DOWNLOAD”页面，单击“huaweicloud-dli-clientkit-<version\>”即可下载DLI客户端工具。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >DLI客户端空间命名为“huaweicloud-dli-clientkit-<version\>-bin.tar.gz”，支持在Linux环境中使用，且依赖JDK 1.8及以上版本。  


## 使用DLI Beeline连接服务端<a name="section177954376119"></a>

使用DLI Beeline的机器安装JDK 1.8或以上版本并配置环境变量，推荐在Linux环境下使用Beeline工具。

1.  下载并解压工具包“huaweicloud-dli-clientkit-<version\>-bin.tar.gz”，其中version为版本号，以实际版本号为准。
2.  进入解压目录，里面有三个子目录bin、conf、lib，分别存放了Beeline相关的执行脚本、配置文件和依赖包。
3.  进入配置文件conf目录，将“connection.properties.template”重命名成“connection.properties”，并配置连接参数（具体连接参数请参考《数据湖探索SDK参考》\>[使用JDBC连接服务端](https://support.huaweicloud.com/sdkreference-dli/dli_04_0066.html)中的“表2-数据库连接参数”和“表3-属性项”）。
4.  进入执行脚本bin目录，启动beeline脚本，执行连接命令即可执行SQL语句，如下所示：

    ```
    %bin/beeline
    Start Beeline
    Welcome to DLI service !
    beeline> !connect
    Connecting from the default connection.properties
    Connecting to jdbc:dli://dli.cn-north-1.myhuaweicloud.com/8fc20d97a4444cafba3c3a8639380003
    Connected to: DLI service
    jdbc:dli://dli.cn-north-1.myhuaweicloud... (not set)> show databases;
    +--------------------+
    |    databaseName    |
    +--------------------+
    | bjhk               |
    | db_xd              |
    | dimensions_adgame  |
    | odbc_db            |
    | sdk_db             |
    | tpch_csv_1024      |
    | tpch_csv_4g_new    |
    | tpchnewtest        |
    | tpchtest           |
    | xunjian            |
    +--------------------+
    10 rows selected (0.338 seconds)
    ```

    用户也可以在启动beeline脚本时通过命令行选项设置连接参数，如下所示，如果连接参数不全，Beeline会提示补全相关信息。

    ```
    %bin/beeline -u 'jdbc:dli://dli.cn-north-1.myhuaweicloud.com/8fc20d97a4444cafba3c3a8639380003? authenticationmode=aksk'
    Start Beeline
    Connecting to jdbc:dli://dli.cn-north-1.myhuaweicloud.com/8fc20d97a4444cafba3c3a8639380003?usehttpproxy=true;proxyhost=10.186.60.154;proxyport=3128;authenticationmode=aksk
    Enter region name: cn-north-1
    Enter service name: DLI
    Enter access key(AK): <real access key>
    Enter secret key(SK): ****************************************
    Enter queue name: default
    Connected to: DLI service
    Welcome to DLI service !
    jdbc:dli://dli.cn-north-1.myhuaweicloud... (not set)> 
    ```


## DLI Beeline支持的命令<a name="section3583203214220"></a>

DLI Beeline支持一系列命令，每个命令以 ！ 这个符号开始，例如!connect。具体请参考[表1](#table18133261151627)。

**表 1**  DLI Beeline支持的命令

<a name="table18133261151627"></a>
<table><thead align="left"><tr id="row59856934151627"><th class="cellrowborder" valign="top" width="14.67%" id="mcps1.2.3.1.1"><p id="p9158444151639"><a name="p9158444151639"></a><a name="p9158444151639"></a><strong id="b65940620151647"><a name="b65940620151647"></a><a name="b65940620151647"></a>命令</strong></p>
</th>
<th class="cellrowborder" valign="top" width="85.33%" id="mcps1.2.3.1.2"><p id="p3636489151639"><a name="p3636489151639"></a><a name="p3636489151639"></a><strong id="b39589998151647"><a name="b39589998151647"></a><a name="b39589998151647"></a>描述</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row1892907715175"><td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.3.1.1 "><p id="p3012072215175"><a name="p3012072215175"></a><a name="p3012072215175"></a>!connect</p>
</td>
<td class="cellrowborder" valign="top" width="85.33%" headers="mcps1.2.3.1.2 "><p id="p2385943615175"><a name="p2385943615175"></a><a name="p2385943615175"></a>通过输入连接参数的方式连接到DLI服务，若不输入参数，则加载默认的“connection.properties”文件连接。</p>
</td>
</tr>
<tr id="row210323015175"><td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.3.1.1 "><p id="p1233334215175"><a name="p1233334215175"></a><a name="p1233334215175"></a>!help</p>
</td>
<td class="cellrowborder" valign="top" width="85.33%" headers="mcps1.2.3.1.2 "><p id="p5947667015175"><a name="p5947667015175"></a><a name="p5947667015175"></a>打印命令行的帮助文档。</p>
</td>
</tr>
<tr id="row23369215175"><td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.3.1.1 "><p id="p616680015175"><a name="p616680015175"></a><a name="p616680015175"></a>!history</p>
</td>
<td class="cellrowborder" valign="top" width="85.33%" headers="mcps1.2.3.1.2 "><p id="p2974875215175"><a name="p2974875215175"></a><a name="p2974875215175"></a>展示命令行执行历史。</p>
</td>
</tr>
<tr id="row5222174815175"><td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.3.1.1 "><p id="p1067725115175"><a name="p1067725115175"></a><a name="p1067725115175"></a>!outputformat</p>
</td>
<td class="cellrowborder" valign="top" width="85.33%" headers="mcps1.2.3.1.2 "><p id="p5955098915175"><a name="p5955098915175"></a><a name="p5955098915175"></a>设置查询结果的输出格式，支持table,vertical,csv2,dsv,tsv2,xmlattr,xmlelements，每一种格式的具体说明详参见<a href="#section109004517511">查询输出格式</a>。</p>
</td>
</tr>
<tr id="row5799819915175"><td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.3.1.1 "><p id="p6034537315175"><a name="p6034537315175"></a><a name="p6034537315175"></a>!properties</p>
</td>
<td class="cellrowborder" valign="top" width="85.33%" headers="mcps1.2.3.1.2 "><p id="p5613706815175"><a name="p5613706815175"></a><a name="p5613706815175"></a>通过加载“connection.properties”文件连接到DLI服务。该功能与!connect相同，但是可以指定连接配置文件。</p>
</td>
</tr>
<tr id="row5864002715175"><td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.3.1.1 "><p id="p5462471615175"><a name="p5462471615175"></a><a name="p5462471615175"></a>!quit</p>
</td>
<td class="cellrowborder" valign="top" width="85.33%" headers="mcps1.2.3.1.2 "><p id="p6252586515175"><a name="p6252586515175"></a><a name="p6252586515175"></a>退出beeline会话。</p>
</td>
</tr>
<tr id="row2142863915175"><td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.3.1.1 "><p id="p1443712415175"><a name="p1443712415175"></a><a name="p1443712415175"></a>!run</p>
</td>
<td class="cellrowborder" valign="top" width="85.33%" headers="mcps1.2.3.1.2 "><p id="p2855636115175"><a name="p2855636115175"></a><a name="p2855636115175"></a>执行一个SQL脚本。使用方法：</p>
<p id="p5568065815175"><a name="p5568065815175"></a><a name="p5568065815175"></a><i><b><span class="cmdname" style="font-family:Arial" id="cmdname206586211433"><a name="cmdname206586211433"></a><a name="cmdname206586211433"></a>!run &lt;scriptfile&gt;</span></b></i></p>
</td>
</tr>
<tr id="row4712020215175"><td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.3.1.1 "><p id="p5744654515175"><a name="p5744654515175"></a><a name="p5744654515175"></a>!save</p>
</td>
<td class="cellrowborder" valign="top" width="85.33%" headers="mcps1.2.3.1.2 "><p id="p2265853115175"><a name="p2265853115175"></a><a name="p2265853115175"></a>将当前的会话属性保存至beeline.properties中，下次开启beeline时会自动加载这些属性。</p>
</td>
</tr>
<tr id="row3506173915175"><td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.3.1.1 "><p id="p928905715175"><a name="p928905715175"></a><a name="p928905715175"></a>!script</p>
</td>
<td class="cellrowborder" valign="top" width="85.33%" headers="mcps1.2.3.1.2 "><p id="p29461927203018"><a name="p29461927203018"></a><a name="p29461927203018"></a>将执行的命令保存至一个文件中。例如：</p>
<p id="p1421616215175"><a name="p1421616215175"></a><a name="p1421616215175"></a><i><b><span class="cmdname" style="font-family:Arial" id="cmdname196581321930"><a name="cmdname196581321930"></a><a name="cmdname196581321930"></a>!script /tmp/mysession.script</span></b></i></p>
<p id="p1065847515175"><a name="p1065847515175"></a><a name="p1065847515175"></a>执行该语句之后，后续的命令将被保存至“/tmp/mysession.script”。</p>
<p id="p2881741915175"><a name="p2881741915175"></a><a name="p2881741915175"></a>再次执行!script，结束脚本记录。执行如下语句，将会重新执行记录下来的命令。</p>
<p id="p1684052614316"><a name="p1684052614316"></a><a name="p1684052614316"></a><i><b><span class="cmdname" style="font-family:Arial" id="cmdname196584216315"><a name="cmdname196584216315"></a><a name="cmdname196584216315"></a>!run /tmp/mysession.script</span></b></i></p>
</td>
</tr>
<tr id="row2626537015175"><td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.3.1.1 "><p id="p2541823415175"><a name="p2541823415175"></a><a name="p2541823415175"></a>!set</p>
</td>
<td class="cellrowborder" valign="top" width="85.33%" headers="mcps1.2.3.1.2 "><p id="p390911335312"><a name="p390911335312"></a><a name="p390911335312"></a>设置Beeline变量，例如：</p>
<p id="p85556479316"><a name="p85556479316"></a><a name="p85556479316"></a><i><b><span class="cmdname" style="font-family:Arial" id="cmdname865814217318"><a name="cmdname865814217318"></a><a name="cmdname865814217318"></a>!set color true</span></b></i></p>
<p id="p4561104415175"><a name="p4561104415175"></a><a name="p4561104415175"></a>!set后面不接参数则显示所有变量值。</p>
</td>
</tr>
<tr id="row4020107615175"><td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.3.1.1 "><p id="p1563696615175"><a name="p1563696615175"></a><a name="p1563696615175"></a>!sh</p>
</td>
<td class="cellrowborder" valign="top" width="85.33%" headers="mcps1.2.3.1.2 "><p id="p310311133215"><a name="p310311133215"></a><a name="p310311133215"></a>执行一个Shell脚本。例如：</p>
<p id="p220063059104"><a name="p220063059104"></a><a name="p220063059104"></a><i><b><span class="cmdname" style="font-family:Arial" id="cmdname865892116317"><a name="cmdname865892116317"></a><a name="cmdname865892116317"></a>!sh &lt;shellscript&gt;</span></b></i></p>
</td>
</tr>
<tr id="row446678615175"><td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.3.1.1 "><p id="p3426974615175"><a name="p3426974615175"></a><a name="p3426974615175"></a>!sql</p>
</td>
<td class="cellrowborder" valign="top" width="85.33%" headers="mcps1.2.3.1.2 "><p id="p434131418324"><a name="p434131418324"></a><a name="p434131418324"></a>显性地执行一条SQL语句，beeline中不带命令的语句默认会转换成!sql命令，sql语句必须以分号结尾。例如：</p>
<p id="p241261619958"><a name="p241261619958"></a><a name="p241261619958"></a><i><b><span class="cmdname" style="font-family:Arial" id="cmdname16581721336"><a name="cmdname16581721336"></a><a name="cmdname16581721336"></a>!sql &lt;sql&gt;</span></b></i></p>
</td>
</tr>
<tr id="row795285015175"><td class="cellrowborder" valign="top" width="14.67%" headers="mcps1.2.3.1.1 "><p id="p932731915175"><a name="p932731915175"></a><a name="p932731915175"></a>!dliconf</p>
</td>
<td class="cellrowborder" valign="top" width="85.33%" headers="mcps1.2.3.1.2 "><p id="p1731537815175"><a name="p1731537815175"></a><a name="p1731537815175"></a>查看DLI 自定义配置。</p>
</td>
</tr>
</tbody>
</table>

## DLI Beeline支持的命令行选项<a name="section1726116551338"></a>

DLI Beeline支持的启动命令行选项请参考[表2](#table65880635152220)。

**表 2**  DLI Beeline支持的启动命令行选项

<a name="table65880635152220"></a>
<table><thead align="left"><tr id="row37154795152220"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p12623506152244"><a name="p12623506152244"></a><a name="p12623506152244"></a><strong id="b53165773152334"><a name="b53165773152334"></a><a name="b53165773152334"></a>命令行选项</strong></p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p15871098152244"><a name="p15871098152244"></a><a name="p15871098152244"></a><strong id="b38684688152248"><a name="b38684688152248"></a><a name="b38684688152248"></a>描述</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row1671668115232"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p4302842115232"><a name="p4302842115232"></a><a name="p4302842115232"></a>-u &lt;database URL&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p5124101233315"><a name="p5124101233315"></a><a name="p5124101233315"></a>连接DLI JDBC的url，其中url需要采用单引号括起来。使用方式：</p>
<p id="p6275003715232"><a name="p6275003715232"></a><a name="p6275003715232"></a><b><span class="cmdname" id="cmdname0557183619330"><a name="cmdname0557183619330"></a><a name="cmdname0557183619330"></a>beeline –u db_URL</span></b></p>
</td>
</tr>
<tr id="row5405319215232"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p5722201815232"><a name="p5722201815232"></a><a name="p5722201815232"></a>-e &lt;query&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p447192015232"><a name="p447192015232"></a><a name="p447192015232"></a>需要执行的SQL语句,可以输入多条语句，以分号间隔，语句需要采用单引号括起来。</p>
</td>
</tr>
<tr id="row1346245015232"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p3880466515232"><a name="p3880466515232"></a><a name="p3880466515232"></a>-f &lt;file&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p5617012415232"><a name="p5617012415232"></a><a name="p5617012415232"></a>需要执行的脚本文件。</p>
</td>
</tr>
<tr id="row895236815232"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1161405215232"><a name="p1161405215232"></a><a name="p1161405215232"></a>--dliconf property=value</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p121413615232"><a name="p121413615232"></a><a name="p121413615232"></a>待设置的DLI属性。</p>
</td>
</tr>
<tr id="row845124815232"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1269020915232"><a name="p1269020915232"></a><a name="p1269020915232"></a>--property-file=&lt;property-file&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p2127401515232"><a name="p2127401515232"></a><a name="p2127401515232"></a>通过指定的方式获取连接属性文件并连接到DLI服务。</p>
</td>
</tr>
<tr id="row2330864815232"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p661007015232"><a name="p661007015232"></a><a name="p661007015232"></a>--help</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p6565362415232"><a name="p6565362415232"></a><a name="p6565362415232"></a>打印命令行选项帮助。</p>
</td>
</tr>
</tbody>
</table>

## 查询输出格式<a name="section109004517511"></a>

DLI Beeline支持多种查询结果输出格式，输出格式可以通过!outputformat指定。DLI Beeline支持的输出格式包括：table，vertical，csv2，dsv，tsv2，xmlattr，xmlelements。

-   **table**

    table格式输出的结果以表的形式展示，例如：

    **!outputformat table**

    **select id, value, comment from test\_table;**

    ```
    +-----+---------+-----------------+
    | id  |  value  |     comment     |
    +-----+---------+-----------------+
    | 1   | Value1  | Test comment 1  |
    | 2   | Value2  | Test comment 2  |
    | 3   | Value3  | Test comment 3  |
    +-----+---------+-----------------+
    ```

-   **vertical**

    以行为单元组织数据，每一个属性以key-value的形式展示，例如：

    **!outputformat vertical**

    **select id, value, comment from test\_table;**

    ```
    id       1
    value    Value1
    comment  Test comment 1
    id       2
    value    Value2
    comment  Test comment 2
    id       3
    value    Value3
    comment  Test comment 3
    ```

-   **csv2**

    以纯文本形式存储表格数据（数字和文本），使用逗号（,）作为分隔符，例如：

    **!outputformat csv2**

    **select id, value, comment from test\_table;**

    ```
    id,value,comment
    1,Value1,Test comment 1
    2,Value2,Test comment 2
    3,Value3,Test comment 3
    ```

-   **dsv**

    每一行储存一条记录， 每条记录的各个字段间以制表符作为分隔，例如：

    **!outputformat dsv**

    **select id, value, comment from test\_table;**

    ```
    id|value |comment
    1 |Value1|Test comment 1
    2 |Value2|Test comment 2
    3 |Value3|Test comment 3
    ```

-   **tsv2**

    每一行储存一条记录， 每条记录的各个字段间以空格作为分隔，例如：

    **!outputformat tsv2**

    **select id, value, comment from test\_table;**

    ```
    id value      comment
    1  Value1Test comment 1
    2  Value2Test comment 2
    3  Value3Test comment 3
    ```

-   **xmlattr**

    用于在SQL查询返回的 XML 元素中设置属性的函数，例如：

    **!outputformat xmlattr**

    **select id, value, comment from test\_table;**

    ```
    <resultset>
      <result id="1" value="Value1" comment="Test comment 1"/>
      <result id="2" value="Value2" comment="Test comment 2"/>
      <result id="3" value="Value3" comment="Test comment 3"/>
    </resultset>
    ```

-   **xmlelements**

    将一个关系值转换为XML元素的函数，格式为<elementName\>值</elementName\>，例如：

    **!outputformat xmlelements**

    **select id, value, comment from test\_table;**

    ```
    <resultset>
      <result>
        <id>1</id>
        <value>Value1</value>
        <comment>Test comment 1</comment>
      </result>
      <result>
        <id>2</id>
        <value>Value2</value>
        <comment>Test comment 2</comment>
      </result>
      <result>
        <id>3</id>
        <value>Value3</value>
        <comment>Test comment 3</comment>
      </result>
    </resultset>
    ```


