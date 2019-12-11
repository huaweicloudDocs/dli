# Spark创建队列<a name="dli_01_0363"></a>

## 操作场景<a name="zh-cn_topic_0122016943_zh-cn_topic_0093946917_section6253115815414"></a>

使用DLI全托管式的Spark计算服务，首先需要创建队列。

## 操作步骤<a name="zh-cn_topic_0122016943_zh-cn_topic_0093946917_section14223343145314"></a>

1.  创建队列的操作入口有三个，分别在SQL作业控制台所有页面、“队列管理“页面和“作业编辑器“页面。
    -   单击SQL作业控制台所有页面右上角![](figures/zh-cn_image_0198727399.png)创建队列。
    -   在“队列管理“页面创建队列。
        1.  在DLI管理控制台的顶部菜单栏中，选择“队列管理“。
        2.  在“队列管理“左侧，单击![](figures/zh-cn_image_0188099630.png)创建队列。

    -   在“作业编辑器“页面创建队列。
        1.  在DLI管理控制台的顶部菜单栏中，选择“作业编辑器“。
        2.  在左侧导航栏的![](figures/icon-队列.png)页签，单击“队列”右侧的![](figures/icon-新增sql.png)创建队列。

2.  在“购买队列“页面，进行资源选型，参见[表1](#zh-cn_topic_0093946917_table103571321132511)设置相关参数。

    **图 1**  Spark购买队列-包年包月<a name="fig8950440172118"></a>  
    ![](figures/Spark购买队列-包年包月.png "Spark购买队列-包年包月")

    **图 2**  Spark购买队列-按需计费<a name="fig82316612214"></a>  
    ![](figures/Spark购买队列-按需计费.png "Spark购买队列-按需计费")

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >创建队列需要完成华为云实名认证。  

    **表 1**  参数说明

    <a name="zh-cn_topic_0093946917_table103571321132511"></a>
    <table><thead align="left"><tr id="dli_01_0013_row16358192162519"><th class="cellrowborder" valign="top" width="13.13%" id="mcps1.2.3.1.1"><p id="dli_01_0013_p1935816218255"><a name="dli_01_0013_p1935816218255"></a><a name="dli_01_0013_p1935816218255"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="86.87%" id="mcps1.2.3.1.2"><p id="dli_01_0013_p143581421162513"><a name="dli_01_0013_p143581421162513"></a><a name="dli_01_0013_p143581421162513"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="dli_01_0013_row75931534268"><td class="cellrowborder" valign="top" width="13.13%" headers="mcps1.2.3.1.1 "><p id="dli_01_0013_p55941553192614"><a name="dli_01_0013_p55941553192614"></a><a name="dli_01_0013_p55941553192614"></a>计费模式</p>
    </td>
    <td class="cellrowborder" valign="top" width="86.87%" headers="mcps1.2.3.1.2 "><a name="dli_01_0013_ul114121349277"></a><a name="dli_01_0013_ul114121349277"></a><ul id="dli_01_0013_ul114121349277"><li>包年/包月</li><li>按需计费：建议购买<a href="https://account.huaweicloud.com/usercenter/?agencyId=af8fcc08b5d9416ebdc15b3a84483263&amp;region=cn-north-1&amp;locale=zh-cn#/buyservice/commonCloud?pkgCode=dli_cuh" target="_blank" rel="noopener noreferrer">cu时套餐包</a>享受优惠。</li></ul>
    </td>
    </tr>
    <tr id="dli_01_0013_row987812482720"><td class="cellrowborder" valign="top" width="13.13%" headers="mcps1.2.3.1.1 "><p id="dli_01_0013_p587912492711"><a name="dli_01_0013_p587912492711"></a><a name="dli_01_0013_p587912492711"></a>当前区域</p>
    </td>
    <td class="cellrowborder" valign="top" width="86.87%" headers="mcps1.2.3.1.2 "><p id="dli_01_0013_p108791224142713"><a name="dli_01_0013_p108791224142713"></a><a name="dli_01_0013_p108791224142713"></a>选择创建队列的区域。不同的地域之间资源不互通，每个地域需分别购买，请根据您的实际需求慎重选择。</p>
    </td>
    </tr>
    <tr id="dli_01_0013_row2358621122514"><td class="cellrowborder" valign="top" width="13.13%" headers="mcps1.2.3.1.1 "><p id="dli_01_0013_p19359721102519"><a name="dli_01_0013_p19359721102519"></a><a name="dli_01_0013_p19359721102519"></a>队列名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="86.87%" headers="mcps1.2.3.1.2 "><p id="dli_01_0013_p10359132172511"><a name="dli_01_0013_p10359132172511"></a><a name="dli_01_0013_p10359132172511"></a>队列的名称。</p>
    <a name="dli_01_0013_ul1235902112514"></a><a name="dli_01_0013_ul1235902112514"></a><ul id="dli_01_0013_ul1235902112514"><li>只能包含数字、英文字母和下划线，但不能是纯数字，不能以下划线开头，且不能为空。</li><li>输入长度不能超过128个字符。</li></ul>
    </td>
    </tr>
    <tr id="dli_01_0013_row835962152512"><td class="cellrowborder" valign="top" width="13.13%" headers="mcps1.2.3.1.1 "><p id="dli_01_0013_p1735920215258"><a name="dli_01_0013_p1735920215258"></a><a name="dli_01_0013_p1735920215258"></a>队列类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="86.87%" headers="mcps1.2.3.1.2 "><a name="dli_01_0013_ul1984112139342"></a><a name="dli_01_0013_ul1984112139342"></a><ul id="dli_01_0013_ul1984112139342"><li>SQL队列</li><li>Spark队列</li></ul>
    </td>
    </tr>
    <tr id="dli_01_0013_row535992116253"><td class="cellrowborder" valign="top" width="13.13%" headers="mcps1.2.3.1.1 "><p id="dli_01_0013_p2036092132519"><a name="dli_01_0013_p2036092132519"></a><a name="dli_01_0013_p2036092132519"></a>队列规格</p>
    </td>
    <td class="cellrowborder" valign="top" width="86.87%" headers="mcps1.2.3.1.2 "><p id="dli_01_0013_p436072119250"><a name="dli_01_0013_p436072119250"></a><a name="dli_01_0013_p436072119250"></a>按需选择队列规格。包括<span class="parmvalue" id="dli_01_0013_parmvalue10360192112511"><a name="dli_01_0013_parmvalue10360192112511"></a><a name="dli_01_0013_parmvalue10360192112511"></a>“4CUs”</span>、<span class="parmvalue" id="dli_01_0013_parmvalue14360121162519"><a name="dli_01_0013_parmvalue14360121162519"></a><a name="dli_01_0013_parmvalue14360121162519"></a>“16CUs”</span>、<span class="parmvalue" id="dli_01_0013_parmvalue536012122519"><a name="dli_01_0013_parmvalue536012122519"></a><a name="dli_01_0013_parmvalue536012122519"></a>“64CUs”</span>和<span class="parmvalue" id="dli_01_0013_parmvalue183603213252"><a name="dli_01_0013_parmvalue183603213252"></a><a name="dli_01_0013_parmvalue183603213252"></a>“128CUs”</span>四种规格。当剩余CU配额小于上述规格时，则不能创建队列。</p>
    </td>
    </tr>
    <tr id="dli_01_0013_row21784437128"><td class="cellrowborder" valign="top" width="13.13%" headers="mcps1.2.3.1.1 "><p id="dli_01_0013_p47271145191218"><a name="dli_01_0013_p47271145191218"></a><a name="dli_01_0013_p47271145191218"></a>企业项目</p>
    </td>
    <td class="cellrowborder" valign="top" width="86.87%" headers="mcps1.2.3.1.2 "><p id="dli_01_0013_p672884514124"><a name="dli_01_0013_p672884514124"></a><a name="dli_01_0013_p672884514124"></a>若所建队列属于企业项目，可选择对应的企业项目。</p>
    <p id="dli_01_0013_p127281445171215"><a name="dli_01_0013_p127281445171215"></a><a name="dli_01_0013_p127281445171215"></a>企业项目是一种云资源管理方式，企业项目管理服务提供统一的云资源按项目管理，以及项目内的资源管理、成员管理。关于如何设置企业项目请参考《<a href="https://support.huaweicloud.com/usermanual-em/zh-cn_topic_0108763975.html" target="_blank" rel="noopener noreferrer">企业管理用户指南</a>》。</p>
    <div class="note" id="dli_01_0013_note10728164511122"><a name="dli_01_0013_note10728164511122"></a><a name="dli_01_0013_note10728164511122"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="dli_01_0013_p1728184551214"><a name="dli_01_0013_p1728184551214"></a><a name="dli_01_0013_p1728184551214"></a>只有开通了企业管理服务的用户才显示该参数。</p>
    </div></div>
    </td>
    </tr>
    <tr id="dli_01_0013_row2362202118256"><td class="cellrowborder" valign="top" width="13.13%" headers="mcps1.2.3.1.1 "><p id="dli_01_0013_p1436211213254"><a name="dli_01_0013_p1436211213254"></a><a name="dli_01_0013_p1436211213254"></a>描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="86.87%" headers="mcps1.2.3.1.2 "><p id="dli_01_0013_p20362621202511"><a name="dli_01_0013_p20362621202511"></a><a name="dli_01_0013_p20362621202511"></a>所创建队列的相应描述。输入长度不能超过256个字符。</p>
    </td>
    </tr>
    <tr id="dli_01_0013_row17641173612523"><td class="cellrowborder" valign="top" width="13.13%" headers="mcps1.2.3.1.1 "><p id="dli_01_0013_p2064215366521"><a name="dli_01_0013_p2064215366521"></a><a name="dli_01_0013_p2064215366521"></a>购买时长</p>
    </td>
    <td class="cellrowborder" valign="top" width="86.87%" headers="mcps1.2.3.1.2 "><p id="dli_01_0013_p96421936115210"><a name="dli_01_0013_p96421936115210"></a><a name="dli_01_0013_p96421936115210"></a>选择“包年/包月”计费模式时，需要选择“购买时长”。购买时长约长，优惠越多。可勾选“自动续费”，按月购买，自动续费周期为1个月。按年购买，自动续费周期为1年。</p>
    </td>
    </tr>
    <tr id="dli_01_0013_row1263194513559"><td class="cellrowborder" valign="top" width="13.13%" headers="mcps1.2.3.1.1 "><p id="dli_01_0013_p166424525514"><a name="dli_01_0013_p166424525514"></a><a name="dli_01_0013_p166424525514"></a>高级配置</p>
    </td>
    <td class="cellrowborder" valign="top" width="86.87%" headers="mcps1.2.3.1.2 "><p id="dli_01_0013_p53511541152715"><a name="dli_01_0013_p53511541152715"></a><a name="dli_01_0013_p53511541152715"></a>选择“包年/包月”计费模式时，需要选择“高级配置”。</p>
    <a name="dli_01_0013_ul69325112568"></a><a name="dli_01_0013_ul69325112568"></a><ul id="dli_01_0013_ul69325112568"><li>默认配置：由系统自动配置。</li><li>自定义配置：选择<span class="parmname" id="dli_01_0013_parmname177444560284"><a name="dli_01_0013_parmname177444560284"></a><a name="dli_01_0013_parmname177444560284"></a>“网段”</span>。<p id="dli_01_0013_p1563395442018"><a name="dli_01_0013_p1563395442018"></a><a name="dli_01_0013_p1563395442018"></a><span class="parmname" id="dli_01_0013_parmname1956031299"><a name="dli_01_0013_parmname1956031299"></a><a name="dli_01_0013_parmname1956031299"></a>“网段”</span>：包年包月队列支持指定使用的网段范围，支持修改，请参考<a href="修改队列网段.md">修改队列网段</a>。不同资源可使用的网段范围分别如下：</p>
    <a name="dli_01_0013_ul1857418223222"></a><a name="dli_01_0013_ul1857418223222"></a><ul id="dli_01_0013_ul1857418223222"><li>4cu:<p id="dli_01_0013_p1484111268227"><a name="dli_01_0013_p1484111268227"></a><a name="dli_01_0013_p1484111268227"></a>10.0.0.0/8 ~ 10.255.255.192/26</p>
    <p id="dli_01_0013_p189901128112216"><a name="dli_01_0013_p189901128112216"></a><a name="dli_01_0013_p189901128112216"></a>172.16.0.0/12 ~ 172.31.255.192/26</p>
    <p id="dli_01_0013_p18487931102217"><a name="dli_01_0013_p18487931102217"></a><a name="dli_01_0013_p18487931102217"></a>192.168.0.0/16 ~ 192.168.255.192/26</p>
    </li><li>16cu:<p id="dli_01_0013_p18950163392218"><a name="dli_01_0013_p18950163392218"></a><a name="dli_01_0013_p18950163392218"></a>10.0.0.0/8 ~ 10.255.255.0/24</p>
    <p id="dli_01_0013_p3586183642218"><a name="dli_01_0013_p3586183642218"></a><a name="dli_01_0013_p3586183642218"></a>172.16.0.0/12 ~ 172.31.255.0/24</p>
    <p id="dli_01_0013_p670913817224"><a name="dli_01_0013_p670913817224"></a><a name="dli_01_0013_p670913817224"></a>192.168.0.0/16 ~ 192.168.255.0/24</p>
    </li><li>64cu:<p id="dli_01_0013_p1957213421226"><a name="dli_01_0013_p1957213421226"></a><a name="dli_01_0013_p1957213421226"></a>10.0.0.0/8 ~ 10.255.252.0/22</p>
    <p id="dli_01_0013_p24661646112215"><a name="dli_01_0013_p24661646112215"></a><a name="dli_01_0013_p24661646112215"></a>172.16.0.0/12 ~ 172.31.252.0/22</p>
    <p id="dli_01_0013_p696444816225"><a name="dli_01_0013_p696444816225"></a><a name="dli_01_0013_p696444816225"></a>192.168.0.0/16 ~ 192.168.252.0/22</p>
    </li><li>128cu:<p id="dli_01_0013_p5718135162218"><a name="dli_01_0013_p5718135162218"></a><a name="dli_01_0013_p5718135162218"></a>10.0.0.0/8 ~ 10.255.252.0/21</p>
    <p id="dli_01_0013_p636216541223"><a name="dli_01_0013_p636216541223"></a><a name="dli_01_0013_p636216541223"></a>172.16.0.0/12 ~ 172.31.252.0/21</p>
    <p id="dli_01_0013_p6569165717224"><a name="dli_01_0013_p6569165717224"></a><a name="dli_01_0013_p6569165717224"></a>192.168.0.0/16 ~ 192.168.252.0/21</p>
    </li></ul>
    </li></ul>
    </td>
    </tr>
    </tbody>
    </table>

3.  单击“下一步“，确认配置。
4.  配置确认无误，单击“立即购买“进行支付。

    如果队列名称已存在，单击“立即购买“时，系统会提示“队列名称重复”错误，可返回“上一步“进行修改。

5.  单击“确认付款“后，系统会自动跳转至“队列管理“页面。

