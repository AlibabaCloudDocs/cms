# 云监控对接Grafana

云监控为云上用户提供常用云产品的监控数据和用户自定义上报的监控数据。在可视化展示层面，除了在云监控控制台查看监控图表外，您还可以将云监控的数据添加到Grafana中展示。

1.  安装Grafana。

    **说明：**

    -   如果您已安装Grafana，则请忽略本操作。
    -   Grafana的其他安装步骤，请参见[Grafana官方文档](http://docs.grafana.org/installation/?spm=a2c63.p38356.a3.23.7f634246zuXN5l)。
    1.  安装Grafana软件。

        本文以Grafana部署在Linux的CentOS系统上为例，介绍其安装方法。

        -   安装方式一：

            yum installhttps://dl.grafana.com/oss/release/grafana-5.3.4-1.x86\_64.rpm

        -   安装方式二：

            wgethttps://dl.grafana.com/oss/release/grafana-5.3.4-1.x86\_64.rpm

            sudo yum localinstallgrafana-5.3.4-1.x86\_64.rpm

    2.  执行如下命令启动Grafana服务。

        service grafana-server start

    3.  （可选）安装Grafana面板插件。

        如果您需要Grafana面板，则执行如下命令安装面板插件，例如：Pie chart（饼状图）插件。

        grafana-cli plugins install grafana-piechart-panel

        **说明：** Grafana面板的其他插件的安装方法，请参见[Panels插件](https://grafana.com/grafana/plugins?orderBy=weight&direction=asc&type=panel)。

2.  安装云监控数据源服务插件。

    1.  确认Grafana插件的安装目录。

        例如：Linux的CentOS系统的插件目录为/var/lib/grafana/plugins/。

    2.  执行如下命令安装插件。

        cd /var/lib/grafana/plugins/

        git clone https://github.com/aliyun/aliyun-cms-grafana.git

    3.  执行如下命令重启Grafana服务。

        service grafana-server restart

    您也可以下载aliyun-cms-grafana.zip插件，解压后上传到Grafana服务器的/var/lib/grafana/plugins/目录下，重启Grafana服务。

    **说明：** 此插件版本目前不支持对监控数据设置报警。

3.  配置云监控数据源服务插件。

    Grafana安装成功后，默认访问端口为：3000，用户名：admin。

    **说明：** 请您首次登录Grafana时，修改默认密码，以免带来安全隐患。

    1.  登录Grafana。

    2.  单击左上方的**Configuration**，在弹出的列表中选**Data Sources**。

    3.  进入Data Sources页面，单击右上方的**Add data source**，添加新的数据源。

    4.  填写云监控数据源的配置项。

        |配置项|配置内容|
        |---|----|
        |**Name**|请您根据所需自定义一个新数据源的名称。|
        |**type**|**Type**请选择**CMS Grafana Service**。|
        |**HTTP**|URL样例：`http://metrics.cn-shanghai.aliyuncs.com`，不同域选择请参考[云监控接入地址](/cn.zh-CN/API参考/调用API.md)。|
        |**Access**|使用默认值即可。|
        |**Auth**|使用默认值即可。|
        |**cloudmonitor service details**|分别填写具备读取权限的AccessKey信息。建议使用子账号的AccessKey。|

        配置示例如下图所示。

        ![Grafana设置](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0690287951/p73947.png)

    5.  单击**Save &Test**。

4.  添加和配置Dashboard。

    1.  单击左上方的**Dashboards**，在弹出的列表中选**Manage**，进入Manage页面。

        ![Manage](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0690287951/p39940.png)

    2.  单击**Dashboard**，创建Dashboard。

        您可以选择创建一个**Folder**后，再创建**Dashboard**，您也可以导入其他Dashboard。

    3.  配置Graph图表。

        1.  在**New Panel**的**Add**下选择**Graph**图表。
        2.  单击**Pannel Title**，在弹出的窗口中单击**Edit**。
        3.  在**Metrics**配置中，选择**datasource**为**cms-grafana**，配置参数Project、Metric、period、Y轴和X轴。

            Project、Metric、Period等参数详情，请参见[QueryMetricList](/cn.zh-CN/API参考/云产品时序指标类监控数据/DescribeMetricList.md)。

            |参数|说明|
            |--|--|
            |**Group**|云账户所在云监控的应用分组。|
            |**Dimensions**|Project与Metric所在监控项最新监控数据的实例集合，若选Group，则为该Group下的实例。|
            |**Y-column**|可支持多选。|
            |**X-column**|timestamp。|
            |**Y-column describe**|对Y-column的区分描述。|

            **说明：**

            -   如果您需要了解更多Graph信息，请单击[Graph](https://grafana.com/docs/grafana/latest/features/panels/graph/)。
            -   所有参数均可按照[QueryMetricList](/cn.zh-CN/API参考/云产品时序指标类监控数据/DescribeMetricList.md)的要求手动输入。
            -   所有已选择或已输入参数均可输入null取消。
            -   如果对应场景下Dimensions的提示信息不全，则需要刷新或按照样例手动输入InstanceId的值即可。
            ![Metrics](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0690287951/p73950.png)

            自定义监控的部分参数信息需要手动输入，参数说明如下表所示。

            |参数|说明|
            |--|--|
            |**Project**|acs\_customMetric\_+云账号ID。|
            |**Metric**|上报监控数据的metricName。|
            |**Period**|上报监控数据时的Period。|
            |**Group**|上报监控数据时的Metric对应的分组ID。|
            |**Dimensions**|上报监控数据时的Dimension，暂不支持下拉选择，只支持输入单个Dimension，若输入多个，默认选第一个。 **说明：** 如果云监控控制台的dimensions格式为`env:public, step:5-ReadFromAlertOnline`，则请用`&`替换示例中的`,`后拼接输入。 |
            |**Y-column**|上报监控数据时的Average、Maximum、Minimum、Sum、SampleCount、P10、P20、P99等。|
            |**X-column**|timestamp。|

            ![自定义监控](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0690287951/p39967.png)

        4.  配置Singlestat面板。
            1.  在**New Panel**的**Add**下选择**Singlestat**。
            2.  单击**Pannel Title**，在弹出的窗口中单击**Edit**。
            3.  配置**Metric**相关参数。

                **说明：** 如果您需了解更多[Singlestat](http://docs.grafana.org/features/panels/singlestat/)信息，请单击[Graph](http://docs.grafana.org/features/panels/graph/)。

                ![配置Singlestat面板](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0690287951/p39968.png)

    4.  配置Variables。

        Variables支持**Type**类型为**Query**和**Custom**。

        -   配置**Type**为**Query**。

            支持函数如下表所示。

            |变量|定义|说明|示例|
            |--|--|--|--|
            |`$namespace`|`namespace(filter)`|按filter过滤云产品监控项，filter可为null。云产品监控项请参见[概述](/cn.zh-CN/附录1 云产品监控项/概述.md)。|`namespace(ecs)`|
            |`$metric`|`metric($namespace,filter)`|按namespace和filter过滤云产品监控项，namespace可为variable，必选，filter可为null。云产品监控项请参见[概述](/cn.zh-CN/附录1 云产品监控项/概述.md)。|`metric($namespace,disk)`、`metric($namespace,null)`、`metric(acs_ecs_dashboard,disk)`|
            |`$tagsFilter`|`tagsFilter(type, regionId, tagType, tagKey)`|获取当前账户下的对应实例绑定标签的`Key`和`Key:/:Value`集合，暂时只支持[ListTagResources](/cn.zh-CN/API参考/标签/ListTagResources.md)和[查询标签](/cn.zh-CN/API 参考/标签/查询标签.md)。 type：`ECS/RDS`，tagType：`key/value`。

**说明：** 需要对AccessKey授权云服务器ECS和云数据库RDS版的权限。

|            -   获取当前账户下绑定标签的Key列表。`tagFilter(RDS, cn-beijing, key, null)`
            -   获取当前账户下绑定标签的`Key:/:Value`列表。`tagFilter(RDS, cn-beijing, value, null)` |
            |`$tags`|`tags(type, regionId, resourceType, resourceId_array, tag_array)`|获取当前账户下的对应实例绑定标签的instanceId集合，暂时只支持[ListTagResources](/cn.zh-CN/API参考/标签/ListTagResources.md)和[查询标签](/cn.zh-CN/API 参考/标签/查询标签.md)。             -   type：`ECS/RDS`
            -   resourceType：`instance(ECS)/INSTANCE(RDS)`
            -   resourceId\_array：需过滤的instanceId集合，ResourceId.N

示例：`[instanceId_1,instanceId_2,instanceId_3]`

            -   tag\_array：需过滤标签集合`Tag.N.Key`和`Tag.N.Value`，参数以`key:/:value`或`key`形式填入。

示例：`[key1:/:value1,key2:/:value2,key3:/:value3] or [key1,key2,key3]`

**说明：** 需要对AccessKey授权云服务器ECS和云数据库RDS版的权限。

|获取当前账户下北京地域的RDS的instanceId集合。`tag(RDS,cn-beijing, INSTANCE, [instanceId_1,instanceId_2], [key1:/:value1,key2:/:value2])`|
            |`$dimension`|`dimension($namespace,metric,filterFirst,filterSecond)`|获取当前账户下的dimensions列表。 filterFirst\[g99hxhnnyr;1egdhoza;kty4zk40hh\] or /dev/vda1

filterSecond \[g99hxhnnyr;1egdhoza;kty4zk40hh\] or /dev/vda1

|            -   `dimension(acs_ecs_dashboard,diskusage_used,i-2zed,/dev/vd),`
            -   `dimension($namespace,$metric,[i-2zed;i-2zeg;i-2zeb],/dev/vda1),`
            -   `dimension($namespace,$metric,i-2zed;i-2zeg;i-2zeb,/dev/vda1),`
            -   `dimension($namespace,$metric,/dev/vda1,[i-2zed;i-2zeg;i-2zeb]),`
            -   `dimension($namespace,$metric,/dev/vda1,null)` |

            在**Dashboard settings**页面单击**Variables**，进入添加Variables后，添加要配置的变量，样例如下图所示。

            ![Variables](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0690287951/p73977.png)

            添加或修改某个变量，标签形式，使用**Value groups/tags**模块，样例如下图所示。

            ![Value Groups](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/0690287951/p73980.png)

            将所需的变量按配置完毕后，需在对应的panel配置对应变量，变量获取用`$变量名`，样例如下图所示。

            ![Panel](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1690287951/p73982.png)

            **说明：** 具体文档描述可见插件里README文件；在src路径下有该案例的`json(ecs,rds)`文件，可供导入配置。

        -   配置**Type**为**Custom**。

            在**Dashboard settings**页面，单击**Variables**，进入添加Variables后添加要配置的变量，样例如下图所示。

            ![Variables](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1690287951/p73983.png)

            将所需的变量按配置完毕后，需在对应的面板配置对应变量，变量获取用`$变量名`，样例如下图所示。

            ![panel](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1690287951/p73984.png)

            **说明：** 支持对project、metric、period、group、dimensions、ycol的variables的custom类型，模版配置过程中，建议您按照以上名称命名变量。

5.  查看结果。

    通过Grafana创建阿里云监控Dashboard并查看监控结果。

    ![Dashboard](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1690287951/p39971.png)

    ![Dashboard](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1690287951/p39973.png)


