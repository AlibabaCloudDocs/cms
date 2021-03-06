# Elasticsearch监控 {#concept_cvv_lld_zdb .concept}

云监控通过监控Elasticsearch的集群状态、集群查询QPS、集群写入QPS等监控项，帮助您监测Elasticsearch服务的使用情况，并支持您对监控项设置报警规则。

在您购买Elasticsearch后，云监控会自动对上述监控项收集数据。

## 监控服务 {#section_lsc_hnd_zdb .section}

-   **监控项说明** 

    |监控项|维度|单位|最小监控粒度|
    |:--|:-|:-|:-----|
    |集群状态|集群维度| |1分钟|
    |集群查询QPS|集群维度|Count/Second|1分钟|
    |集群写入QPS|集群维度|Count/Second|1分钟|
    |节点CPU使用率|节点维度|%|1分钟|
    |节点磁盘使用率|节点维度|%|1分钟|
    |节点HeapMemory使用率|节点维度|%|1分钟|
    |节点load\_1m|节点维度| |1分钟|
    |节点FullGc次数|节点维度|Count|1分钟|
    |节点Exception次数|节点维度|Count|1分钟|
    |集群快照状态|集群维度|-1代表没有快照； 0代表成功； 1代表进行中； 2代表失败|1分钟|

    **说明：** 

    -   监控数据最多保存 31 天。
    -   最多可连续查看 14 天的监控数据。
-   **查看监控数据** 
    1.  登录[云监控控制台](https://cms-intl.console.aliyun.com)。
    2.  单击左侧导航栏中**云服务监控**下的**Elasticsearch**，进入Elasticsearch监控列表页面。
    3.  单击实例名称或**操作**中的**监控图表**，即可进入实例监控图表页面，查看各项指标。
    4.  单击页面上方的**时间范围**快速选择按钮或自定义时间范围，监控数据最长支持查看连续14天的监控数据。
    5.  （可选）单击监控图右上角的放大按钮，可查看监控大图。

## 报警服务 {#section_jdy_m4d_zdb .section}

-   **设置报警规则** 
    1.  登录[云监控控制台](https://cms-intl.console.aliyun.com)。
    2.  单击左侧导航栏中**云服务监控**下的**Elasticsearch**，进入Elasticsearch监控列表页面。
    3.  单击实例名称或**操作**中的**监控图表**，即可进入实例监控图表页面。
    4.  单击监控图右上角的铃铛图标或页面右上角的**创建报警规则**，选择资源范围、根据参数设置报警规则，选择通知方式，单击**确认**即可。
-   **参数说明** 

    报警规则参数相关说明，请参见[报警规则参数说明](intl.zh-CN/用户指南/报警服务/报警规则/报警规则参数说明.md#)。


