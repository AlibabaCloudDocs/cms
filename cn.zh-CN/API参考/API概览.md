# API概览 {#doc_14254 .concept}

云监控为您提供以下API接口。

## 云产品时序指标类监控数据 {#section_2xy_e7n_i8e .section}

|API|描述|
|---|--|
|[DescribeProjectMeta](intl.zh-CN/API参考/云产品时序指标类监控数据/DescribeProjectMeta.md)|查询接入的云产品信息，包括产品的描述信息， namespace和Labels。|
|[DescribeMetricLast](intl.zh-CN/API参考/云产品时序指标类监控数据/DescribeMetricLast.md)|查询指定监控对象的最新监控数据。|
|[DescribeMetricMetaList](intl.zh-CN/API参考/云产品时序指标类监控数据/DescribeMetricMetaList.md)|查询云监控开放的时序类监控项的监控项描述。|
|[DescribeMetricList](intl.zh-CN/API参考/云产品时序指标类监控数据/DescribeMetricList.md)|查询指定时间段内的云产品时序指标监控数据。|
|[DescribeMetricData](intl.zh-CN/API参考/云产品时序指标类监控数据/DescribeMetricData.md)|查询指定时间段内的云产品时序指标监控数据。|
|[DescribeMetricTop](intl.zh-CN/API参考/云产品时序指标类监控数据/DescribeMetricTop.md)|查询指定时间段内排序后的云产品时序指标监控数据。|

## 报警联系人组 {#section_2n5_b7f_0qs .section}

|API|描述|
|---|--|
|[DescribeContactListByContactGroup](intl.zh-CN/API参考/报警联系人组/DescribeContactListByContactGroup.md)|查询一个报警联系人组下的报警联系人列表。|
|[DeleteContactGroup](intl.zh-CN/API参考/报警联系人组/DeleteContactGroup.md)|删除报警联系人组。|
|[DescribeContactGroupList](intl.zh-CN/API参考/报警联系人组/DescribeContactGroupList.md)|查询报警联系人组列表。|
|[PutContact](intl.zh-CN/API参考/报警联系人组/PutContact.md)|创建或者修改报警联系人信息。|
|[DeleteContact](intl.zh-CN/API参考/报警联系人组/DeleteContact.md)|删除报警联系人。|
|[DescribeContactList](intl.zh-CN/API参考/报警联系人组/DescribeContactList.md)|查询报警联系人列表。|
|[PutContactGroup](intl.zh-CN/API参考/报警联系人组/PutContactGroup.md)|创建或者修改报警联系人组。|

## 时序指标报警规则 {#section_5xu_7jj_jma .section}

|API|描述|
|---|--|
|[ListContactGroup](intl.zh-CN/API参考/时序指标报警规则/ListContactGroup.md)|查询云账号下对应的报警规则联系人组。|
|[DescribeProductsOfActiveMetricRule](intl.zh-CN/API参考/时序指标报警规则/DescribeProductsOfActiveMetricRule.md)|查询开通一键告警产品的列表。|
|[EnableActiveMetricRule](intl.zh-CN/API参考/时序指标报警规则/EnableActiveMetricRule.md)|启用一键报警产品。|
|[DescribeActiveMetricRuleList](intl.zh-CN/API参考/时序指标报警规则/DescribeActiveMetricRuleList.md)|查询一键报警规则的列表详情。|
|[PutResourceMetricRule](intl.zh-CN/API参考/时序指标报警规则/PutResourceMetricRule.md)|对单个资源的性能指标设置阈值报警规则。|
|[DeleteMetricRules](intl.zh-CN/API参考/时序指标报警规则/DeleteMetricRules.md)|删除一个或者多个报警规则。|
|[DescribeMetricRuleCount](intl.zh-CN/API参考/时序指标报警规则/DescribeMetricRuleCount.md)|分类查询报警规则的数量。|
|[DisableActiveMetricRule](intl.zh-CN/API参考/时序指标报警规则/DisableActiveMetricRule.md)|禁用一键告警。|
|[EnableMetricRules](intl.zh-CN/API参考/时序指标报警规则/EnableMetricRules.md)|启用一个或多个报警规则。|
|[DescribeMetricRuleList](intl.zh-CN/API参考/时序指标报警规则/DescribeMetricRuleList.md)|查询报警规则列表。|
|[DisableMetricRules](intl.zh-CN/API参考/时序指标报警规则/DisableMetricRules.md)|禁用一个或多个报警规则。|
|[CreateGroupMetricRules](intl.zh-CN/API参考/时序指标报警规则/CreateGroupMetricRules.md)|批量创建应用分组报警规则。|
|[DescribeAlertHistoryList](intl.zh-CN/API参考/时序指标报警规则/DescribeAlertHistoryList.md)|查询报警历史。|
|[PutGroupMetricRule](intl.zh-CN/API参考/时序指标报警规则/PutGroupMetricRule.md)|创建或者修改组报警规则。|
|[DescribeAlertingMetricRuleResources](intl.zh-CN/API参考/时序指标报警规则/DescribeAlertingMetricRuleResources.md)|查询一个报警规则下正在报警的资源。|
|[PutMetricRuleTargets](intl.zh-CN/API参考/时序指标报警规则/PutMetricRuleTargets.md)|添加或者修改报警规则的目标。|
|[DescribeMetricRuleTargets](intl.zh-CN/API参考/时序指标报警规则/DescribeMetricRuleTargets.md)|查询报警规则关联目标。|
|[DeleteMetricRuleTargets](intl.zh-CN/API参考/时序指标报警规则/DeleteMetricRuleTargets.md)|删除一个报警规则的目标。|

## 主机监控 {#section_rxw_cnz_aui .section}

|API|描述|
|---|--|
|[DeleteMonitoringAgentProcess](intl.zh-CN/API参考/主机监控/DeleteMonitoringAgentProcess.md)|删除进程监控。|
|[DescribeMonitoringAgentStatuses](intl.zh-CN/API参考/主机监控/DescribeMonitoringAgentStatuses.md)|查询云监控插件运行状态。|
|[DescribeMonitoringAgentProcesses](intl.zh-CN/API参考/主机监控/DescribeMonitoringAgentProcesses.md)|查询进程监控列表。|
|[DescribeMonitoringAgentAccessKey](intl.zh-CN/API参考/主机监控/DescribeMonitoringAgentAccessKey.md)|查询非阿里云ECS主机安装云监控插件时所需要的AccessKey和AccessSecret。|
|[UninstallMonitoringAgent](intl.zh-CN/API参考/主机监控/UninstallMonitoringAgent.md)|卸载非阿里云主机监控插件。|
|[InstallMonitoringAgent](intl.zh-CN/API参考/主机监控/InstallMonitoringAgent.md)|对指定ECS安装云监控插件。不适用于非阿里云ECS 的服务器。|
|[DescribeMonitoringAgentHosts](intl.zh-CN/API参考/主机监控/DescribeMonitoringAgentHosts.md)|查询安装云监控插件的主机列表。|
|[DescribeMonitoringAgentConfig](intl.zh-CN/API参考/主机监控/DescribeMonitoringAgentConfig.md)|查询云监控插件的配置信息。|
|[CreateMonitorAgentProcess](intl.zh-CN/API参考/主机监控/CreateMonitorAgentProcess.md)|创建进程监控。|

## 应用分组 {#section_lvo_iyx_rfh .section}

|API|描述|
|---|--|
|[CreateMonitorGroupNotifyPolicy](intl.zh-CN/API参考/应用分组/CreateMonitorGroupNotifyPolicy.md)|创建暂停应用分组报警通知的策略。|
|[DeleteMonitorGroupNotifyPolicy](intl.zh-CN/API参考/应用分组/DeleteMonitorGroupNotifyPolicy.md)|删除指定应用分组的报警通知暂停策略。|
|[DescribeMonitorGroupNotifyPolicyList](intl.zh-CN/API参考/应用分组/DescribeMonitorGroupNotifyPolicyList.md)|查询应用分组的报警通知暂停策略列表。|
|[DeleteMonitorGroupInstances](intl.zh-CN/API参考/应用分组/DeleteMonitorGroupInstances.md)|删除应用分组内的资源实例。|
|[PutMonitorGroupDynamicRule](intl.zh-CN/API参考/应用分组/PutMonitorGroupDynamicRule.md)|创建或者修改一个应用分组的动态规则，满足规则描述的资源会自动添加到应用分组中。|
|[DeleteMonitorGroupDynamicRule](intl.zh-CN/API参考/应用分组/DeleteMonitorGroupDynamicRule.md)|删除指定应用分组的动态规则。|
|[ModifyMonitorGroupInstances](intl.zh-CN/API参考/应用分组/ModifyMonitorGroupInstances.md)|修改应用分组中的资源。|
|[DescribeMonitorGroupDynamicRules](intl.zh-CN/API参考/应用分组/DescribeMonitorGroupDynamicRules.md)|查询应用分组动态规则的列表。|
|[DescribeMonitorGroupInstanceAttribute](intl.zh-CN/API参考/应用分组/DescribeMonitorGroupInstanceAttribute.md)|查询应用分组的资源实例详情。|
|[DescribeMonitorGroupCategories](intl.zh-CN/API参考/应用分组/DescribeMonitorGroupCategories.md)|查询指定应用分组的产品资源列表和每个产品的资源数量。|
|[CreateMonitorGroup](intl.zh-CN/API参考/应用分组/CreateMonitorGroup.md)|创建一个应用分组。|
|[CreateMonitorGroupInstances](intl.zh-CN/API参考/应用分组/CreateMonitorGroupInstances.md)|添加资源到应用分组。|
|[DescribeMonitorGroups](intl.zh-CN/API参考/应用分组/DescribeMonitorGroups.md)|查询应用分组列表。|
|[ModifyMonitorGroup](intl.zh-CN/API参考/应用分组/ModifyMonitorGroup.md)|修改应用分组。|
|[DescribeMonitorGroupInstances](intl.zh-CN/API参考/应用分组/DescribeMonitorGroupInstances.md)|查询指定应用分组内包含的资源列表。|
|[DeleteMonitorGroup](intl.zh-CN/API参考/应用分组/DeleteMonitorGroup.md)|删除指定的应用分组。|

## 可用性监控 {#section_pjs_w3k_zpf .section}

|API|描述|
|---|--|
|[CreateHostAvailability](intl.zh-CN/API参考/可用性监控/CreateHostAvailability.md)|创建可用性监控任务。|
|[DeleteHostAvailability](intl.zh-CN/API参考/可用性监控/DeleteHostAvailability.md)|删除可用性监控任务。|
|[ModifyHostAvailability](intl.zh-CN/API参考/可用性监控/ModifyHostAvailability.md)|修改可用性监控任务。|
|[EnableHostAvailability](intl.zh-CN/API参考/可用性监控/EnableHostAvailability.md)|启用可用性监控任务。|
|[DescribeHostAvailabilityList](intl.zh-CN/API参考/可用性监控/DescribeHostAvailabilityList.md)|查询可用性监控任务列表。|
|[DescribeUnhealthyHostAvailability](intl.zh-CN/API参考/可用性监控/DescribeUnhealthyHostAvailability.md)|查询探测结果异常的服务器列表。|
|[DisableHostAvailability](intl.zh-CN/API参考/可用性监控/DisableHostAvailability.md)|禁用一个可用性监控任务。|

## 全局配置 {#section_ijd_wcz_amy .section}

|API|描述|
|---|--|
|[DescribeMonitoringConfig](intl.zh-CN/API参考/全局配置/DescribeMonitoringConfig.md)|查询云监控全局配置，例如开启自动安装云监控插件以及一键告警等。|
|[PutMonitoringConfig](intl.zh-CN/API参考/全局配置/PutMonitoringConfig.md)|设置云监控插件全局配置，例如开始自动安装插件以及一键报警等。|

## 云产品事件类监控数据 {#section_tbi_4ux_vao .section}

|API|描述|
|---|--|
|[DescribeSystemEventHistogram](intl.zh-CN/API参考/云产品事件类监控数据/DescribeSystemEventHistogram.md)|查询系统事件的时段数量分布图（柱状图\)。|
|[SendDryRunSystemEvent](intl.zh-CN/API参考/云产品事件类监控数据/SendDryRunSystemEvent.md)|触发一个用于调试的系统事件，用于调试事件下游配置的触发逻辑是否符合预期。|
|[DescribeSystemEventMetaList](intl.zh-CN/API参考/云产品事件类监控数据/DescribeSystemEventMetaList.md)|查询系统事件的Meta信息。|
|[DescribeSystemEventCount](intl.zh-CN/API参考/云产品事件类监控数据/DescribeSystemEventCount.md)|查询各个产品指定时间段内事件的数量。|
|[DescribeSystemEventAttribute](intl.zh-CN/API参考/云产品事件类监控数据/DescribeSystemEventAttribute.md)|查询系统事件详情。|

## 时序指标报警模板 {#section_dca_9lu_k9x .section}

|API|描述|
|---|--|
|[ApplyMetricRuleTemplate](intl.zh-CN/API参考/时序指标报警模板/ApplyMetricRuleTemplate.md)|将报警模板应用到分组，生成报警规则。|
|[DescribeMetricRuleTemplateAttribute](intl.zh-CN/API参考/时序指标报警模板/DescribeMetricRuleTemplateAttribute.md)|查询报警模板的详情。|
|[ModifyMetricRuleTemplate](intl.zh-CN/API参考/时序指标报警模板/ModifyMetricRuleTemplate.md)|修改报警模板。|
|[DescribeMetricRuleTemplateList](intl.zh-CN/API参考/时序指标报警模板/DescribeMetricRuleTemplateList.md)|查询报警模板列表。|
|[CreateMetricRuleTemplate](intl.zh-CN/API参考/时序指标报警模板/CreateMetricRuleTemplate.md)|创建报警规则模板。|
|[DeleteMetricRuleTemplate](intl.zh-CN/API参考/时序指标报警模板/DeleteMetricRuleTemplate.md)|删除报警规则模板。|

## 事件报警规则 {#section_f2n_dtk_zvl .section}

|API|描述|
|---|--|
|[DescribeEventRuleAttribute](intl.zh-CN/API参考/事件报警规则/DescribeEventRuleAttribute.md)|查询指定规则的详情。|
|[PutEventRuleTargets](intl.zh-CN/API参考/事件报警规则/PutEventRuleTargets.md)|添加或者修改规则的发送目标。|
|[DeleteEventRuleTargets](intl.zh-CN/API参考/事件报警规则/DeleteEventRuleTargets.md)|删除事件报警通知目标。|
|[EnableEventRules](intl.zh-CN/API参考/事件报警规则/EnableEventRules.md)|启用一个或者多个事件监控报警规则。|
|[DescribeEventRuleList](intl.zh-CN/API参考/事件报警规则/DescribeEventRuleList.md)|查询事件报警的列表。|
|[DeleteEventRules](intl.zh-CN/API参考/事件报警规则/DeleteEventRules.md)|删除事件报警规则。|
|[DisableEventRules](intl.zh-CN/API参考/事件报警规则/DisableEventRules.md)|禁用一个或者多个事件报警规则。|
|[PutEventRule](intl.zh-CN/API参考/事件报警规则/PutEventRule.md)|创建或者修改事件的报警规则。|
|[DescribeEventRuleTargetList](intl.zh-CN/API参考/事件报警规则/DescribeEventRuleTargetList.md)|查询指定事件报警规则的报警目标。|

## 自定义监控 {#section_aqo_fnf_v5u .section}

|API|描述|
|---|--|
|[PutCustomMetric](intl.zh-CN/API参考/自定义监控/PutCustomMetric.md)|上报自定义监控数据。|
|[DescribeCustomMetricList](intl.zh-CN/API参考/自定义监控/DescribeCustomMetricList.md)|查询上报的自定义监控数据。|
|[DeleteCustomMetric](intl.zh-CN/API参考/自定义监控/DeleteCustomMetric.md)|删除自定义监控上报数据。|

## 自定义事件 {#section_cd6_6tp_fjr .section}

|API|描述|
|---|--|
|[DescribeCustomEventCount](intl.zh-CN/API参考/自定义事件/DescribeCustomEventCount.md)|查询自定义事件的统计结果。按照产品统计每个产品自定义事件数量。|
|[DescribeCustomEventAttribute](intl.zh-CN/API参考/自定义事件/DescribeCustomEventAttribute.md)|查询自定义事件的详情。|
|[DescribeCustomEventHistogram](intl.zh-CN/API参考/自定义事件/DescribeCustomEventHistogram.md)|查询自定义上报的事件的分时段数量分布图。|
|[PutCustomEvent](intl.zh-CN/API参考/自定义事件/PutCustomEvent.md)|上报自定义事件数据监控数据。|

## 站点监控 {#section_syl_xni_qf9 .section}

|API|描述|
|---|--|
|[DisableSiteMonitors](intl.zh-CN/API参考/站点监控/DisableSiteMonitors.md)|禁用站点监控探测任务。|
|[DescribeSiteMonitorQuota](intl.zh-CN/API参考/站点监控/DescribeSiteMonitorQuota.md)|查询站点监控的配额以及版本。|
|[DescribeSiteMonitorAttribute](intl.zh-CN/API参考/站点监控/DescribeSiteMonitorAttribute.md)|查询站点监控详细信息。|
|[DeleteSiteMonitors](intl.zh-CN/API参考/站点监控/DeleteSiteMonitors.md)|删除站点监控的探测任务。|
|[DescribeSiteMonitorISPCityList](intl.zh-CN/API参考/站点监控/DescribeSiteMonitorISPCityList.md)|查询可用于创建任务的探测点列表。|
|[DescribeSiteMonitorData](intl.zh-CN/API参考/站点监控/DescribeSiteMonitorData.md)|查询任务的细粒度监控数据。|
|[DescribeSiteMonitorStatistics](intl.zh-CN/API参考/站点监控/DescribeSiteMonitorStatistics.md)|查询指定任务一段时间内的平均统计数据。|
|[CreateSiteMonitor](intl.zh-CN/API参考/站点监控/CreateSiteMonitor.md)|创建站点监控的探测任务。|
|[ModifySiteMonitor](intl.zh-CN/API参考/站点监控/ModifySiteMonitor.md)|修改站点监控探测任务|
|[EnableSiteMonitors](intl.zh-CN/API参考/站点监控/EnableSiteMonitors.md)|启用一个或者多个站点监控探测任务。|
|[DescribeSiteMonitorList](intl.zh-CN/API参考/站点监控/DescribeSiteMonitorList.md)|查询站点监控任务列表。|

