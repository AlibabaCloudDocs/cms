# API概览

本文列出了云监控所有可调用的API及相关描述。

**说明：** API调用次数限制：20次/秒。

## 应用分组

|API|描述|
|---|--|
|[CreateMonitorGroup](/cn.zh-CN/API参考/应用分组/CreateMonitorGroup.md)|调用CreateMonitorGroup接口创建应用分组。|
|[CreateMonitorGroupInstances](/cn.zh-CN/API参考/应用分组/CreateMonitorGroupInstances.md)|调用CreateMonitorGroupInstances接口添加指定资源到指定应用分组。|
|[CreateMonitorGroupByResourceGroupId](/cn.zh-CN/API参考/应用分组/CreateMonitorGroupByResourceGroupId.md)|调用CreateMonitorGroupByResourceGroupId接口通过资源组创建应用分组。|
|[CreateMonitorGroupNotifyPolicy](/cn.zh-CN/API参考/应用分组/CreateMonitorGroupNotifyPolicy.md)|调用CreateMonitorGroupNotifyPolicy接口创建暂停应用分组报警通知的策略。|
|[CreateGroupMonitoringAgentProcess](/cn.zh-CN/API参考/应用分组/CreateGroupMonitoringAgentProcess.md)|调用CreateGroupMonitoringAgentProcess接口创建组进程监控。|
|[PutMonitorGroupDynamicRule](/cn.zh-CN/API参考/应用分组/PutMonitorGroupDynamicRule.md)|调用PutMonitorGroupDynamicRule接口为应用分组创建或修改动态报警规则。|
|[ModifyMonitorGroupInstances](/cn.zh-CN/API参考/应用分组/ModifyMonitorGroupInstances.md)|调用ModifyMonitorGroupInstances接口修改应用分组中的资源。|
|[ModifyMonitorGroup](/cn.zh-CN/API参考/应用分组/ModifyMonitorGroup.md)|调用ModifyMonitorGroup接口修改应用分组。|
|[ModifyGroupMonitoringAgentProcess](/cn.zh-CN/API参考/应用分组/ModifyGroupMonitoringAgentProcess.md)|调用ModifyGroupMonitoringAgentProcess接口修改应用分组内的进程监控。|
|[DescribeMonitorGroupDynamicRules](/cn.zh-CN/API参考/应用分组/DescribeMonitorGroupDynamicRules.md)|调用DescribeMonitorGroupDynamicRules接口查询指定应用分组的动态规则列表。|
|[DescribeMonitorGroupInstanceAttribute](/cn.zh-CN/API参考/应用分组/DescribeMonitorGroupInstanceAttribute.md)|调用DescribeMonitorGroupInstanceAttribute接口查询应用分组的资源详情。|
|[DescribeMonitorGroupCategories](/cn.zh-CN/API参考/应用分组/DescribeMonitorGroupCategories.md)|调用DescribeMonitorGroupCategories接口查询指定应用分组的资源列表和每个云服务的资源数量。|
|[DescribeMonitorGroups](/cn.zh-CN/API参考/应用分组/DescribeMonitorGroups.md)|调用DescribeMonitorGroups接口查询应用分组列表。|
|[DescribeMonitorGroupInstances](/cn.zh-CN/API参考/应用分组/DescribeMonitorGroupInstances.md)|调用DescribeMonitorGroupInstances接口查询指定应用分组内包含的资源列表。|
|[DescribeGroupMonitoringAgentProcess](/cn.zh-CN/API参考/应用分组/DescribeGroupMonitoringAgentProcess.md)|调用DescribeGroupMonitoringAgentProcess接口获取组进程监控任务列表。|
|[DescribeMonitorGroupNotifyPolicyList](/cn.zh-CN/API参考/应用分组/DescribeMonitorGroupNotifyPolicyList.md)|调用DescribeMonitorGroupNotifyPolicyList接口查询应用分组的报警通知暂停策略列表。|
|[DeleteMonitorGroupNotifyPolicy](/cn.zh-CN/API参考/应用分组/DeleteMonitorGroupNotifyPolicy.md)|调用DeleteMonitorGroupNotifyPolicy接口删除暂停指定应用分组报警通知策略。|
|[DeleteMonitorGroupInstances](/cn.zh-CN/API参考/应用分组/DeleteMonitorGroupInstances.md)|调用DeleteMonitorGroupInstances接口删除应用分组内的资源实例。|
|[DeleteMonitorGroupDynamicRule](/cn.zh-CN/API参考/应用分组/DeleteMonitorGroupDynamicRule.md)|调用DeleteMonitorGroupDynamicRule接口删除指定应用分组的动态规则。|
|[DeleteMonitorGroup](/cn.zh-CN/API参考/应用分组/DeleteMonitorGroup.md)|调用DeleteMonitorGroup接口删除指定的应用分组。|
|[DeleteGroupMonitoringAgentProcess](/cn.zh-CN/API参考/应用分组/DeleteGroupMonitoringAgentProcess.md)|调用DeleteGroupMonitoringAgentProcess接口删除组进程监控任务。|
|[CreateGroupMetricRules](/cn.zh-CN/API参考/应用分组/CreateGroupMetricRules.md)|调用CreateGroupMetricRules接口批量为应用分组创建报警规则。|
|[PutGroupMetricRule](/cn.zh-CN/API参考/应用分组/PutGroupMetricRule.md)|调用PutGroupMetricRule接口创建或修改应用分组的报警规则。|
|[CreateHostAvailability](/cn.zh-CN/API参考/应用分组/可用性监控/CreateHostAvailability.md)|调用CreateHostAvailability接口创建可用性监控任务。|
|[ModifyHostAvailability](/cn.zh-CN/API参考/应用分组/可用性监控/ModifyHostAvailability.md)|调用ModifyHostAvailability接口修改可用性监控任务。|
|[DeleteHostAvailability](/cn.zh-CN/API参考/应用分组/可用性监控/DeleteHostAvailability.md)|调用DeleteHostAvailability接口删除可用性监控任务。|
|[EnableHostAvailability](/cn.zh-CN/API参考/应用分组/可用性监控/EnableHostAvailability.md)|调用EnableHostAvailability接口启用指定可用性监控任务。|
|[DescribeHostAvailabilityList](/cn.zh-CN/API参考/应用分组/可用性监控/DescribeHostAvailabilityList.md)|调用DescribeHostAvailabilityList接口查询可用性监控任务列表。|
|[DescribeUnhealthyHostAvailability](/cn.zh-CN/API参考/应用分组/可用性监控/DescribeUnhealthyHostAvailability.md)|调用DescribeUnhealthyHostAvailability接口查询探测结果异常的服务器列表。|
|[DisableHostAvailability](/cn.zh-CN/API参考/应用分组/可用性监控/DisableHostAvailability.md)|调用DisableHostAvailability接口禁用指定可用性监控任务。|
|[AddTags](/cn.zh-CN/API参考/应用分组/标签/AddTags.md)|调用AddTags接口为资源创建标签。|
|[DescribeTagValueList](/cn.zh-CN/API参考/应用分组/标签/DescribeTagValueList.md)|调用DescribeTagValueList接口查询标签值列表。|
|[DescribeTagKeyList](/cn.zh-CN/API参考/应用分组/标签/DescribeTagKeyList.md)|调用DescribeTagKeyList接口查询标签键列表。|
|[RemoveTags](/cn.zh-CN/API参考/应用分组/标签/RemoveTags.md)|调用RemoveTags接口删除标签。|
|[CreateDynamicTagGroup](/cn.zh-CN/API参考/应用分组/标签/CreateDynamicTagGroup.md)|调用CreateDynamicTagGroup接口使用云服务的标签自动同步创建应用分组。|
|[DescribeProductResourceTagKeyList](/cn.zh-CN/API参考/应用分组/标签/DescribeProductResourceTagKeyList.md)|调用DescribeProductResourceTagKeyList接口获取对应地域下云资源的所有标签键列表。|
|[DescribeDynamicTagRuleList](/cn.zh-CN/API参考/应用分组/标签/DescribeDynamicTagRuleList.md)|调用DescribeDynamicTagRuleList接口查询智能标签的规则列表。|
|[DeleteDynamicTagGroup](/cn.zh-CN/API参考/应用分组/标签/DeleteDynamicTagGroup.md)|调用DeleteDynamicTagGroup接口删除智能标签规则。|

## 主机监控

|API|描述|
|---|--|
|[DeleteMonitoringAgentProcess](/cn.zh-CN/API参考/主机监控/DeleteMonitoringAgentProcess.md)|调用DeleteMonitoringAgentProcess接口删除进程监控。|
|[DescribeMonitoringAgentStatuses](/cn.zh-CN/API参考/主机监控/DescribeMonitoringAgentStatuses.md)|调用DescribeMonitoringAgentStatuses接口查询云监控插件运行状态。|
|[DescribeMonitoringAgentProcesses](/cn.zh-CN/API参考/主机监控/DescribeMonitoringAgentProcesses.md)|调用DescribeMonitoringAgentProcesses接口查询进程监控列表。|
|[DescribeMonitoringAgentAccessKey](/cn.zh-CN/API参考/主机监控/DescribeMonitoringAgentAccessKey.md)|调用DescribeMonitoringAgentAccessKey接口查询非阿里云主机安装云监控插件时所需要的AccessKey ID和AccessKey Secret。|
|[UninstallMonitoringAgent](/cn.zh-CN/API参考/主机监控/UninstallMonitoringAgent.md)|调用UninstallMonitoringAgent接口卸载非阿里云主机的云监控插件。|
|[InstallMonitoringAgent](/cn.zh-CN/API参考/主机监控/InstallMonitoringAgent.md)|调用InstallMonitoringAgent接口对指定ECS实例安装云监控插件。|
|[CreateMonitoringAgentProcess](/cn.zh-CN/API参考/主机监控/CreateMonitoringAgentProcess.md)|调用CreateMonitoringAgentProcess接口创建进程监控。|
|[DescribeMonitoringAgentHosts](/cn.zh-CN/API参考/主机监控/DescribeMonitoringAgentHosts.md)|调用DescribeMonitoringAgentHosts接口查询所有已安装和未安装云监控插件的主机列表。|
|[DescribeMonitoringAgentConfig](/cn.zh-CN/API参考/主机监控/DescribeMonitoringAgentConfig.md)|调用DescribeMonitoringAgentConfig接口查询云监控插件的配置信息。|
|[CreateMonitorAgentProcess](/cn.zh-CN/API参考/主机监控/CreateMonitorAgentProcess.md)|调用CreateMonitorAgentProcess接口创建进程监控。|
|[ModifyHostInfo](/cn.zh-CN/API参考/主机监控/ModifyHostInfo.md)|调用ModifyHostInfo接口修改非阿里云的主机显示信息。|
|[DescribeMonitoringConfig](/cn.zh-CN/API参考/主机监控/DescribeMonitoringConfig.md)|调用DescribeMonitoringConfig接口查询云监控插件的全局配置。|
|[PutMonitoringConfig](/cn.zh-CN/API参考/主机监控/PutMonitoringConfig.md)|调用PutMonitoringConfig接口设置云监控插件的全局配置。|
|[DeleteExporterOutput](/cn.zh-CN/API参考/云产品监控/DeleteExporterOutput.md)|调用DeleteExporterOutput接口删除监控数据导出配置。|
|[DescribeExporterOutputList](/cn.zh-CN/API参考/云产品监控/DescribeExporterOutputList.md)|调用DeleteExporterRule接口删除监控数据导出规则。|
|[DescribeExporterOutputList](/cn.zh-CN/API参考/云产品监控/DescribeExporterOutputList.md)|调用DescribeExporterOutputList接口查询监控数据导出列表。|
|[DescribeExporterRuleList](/cn.zh-CN/API参考/云产品监控/DescribeExporterRuleList.md)|调用DescribeExporterRuleList接口查询数据导出规则列表。|
|[PutExporterOutput](/cn.zh-CN/API参考/云产品监控/PutExporterOutput.md)|调用PutExporterOutput接口创建或修改一个监控数据导出配置。|
|[PutExporterRule](/cn.zh-CN/API参考/云产品监控/PutExporterRule.md)|调用PutExporterRule接口创建或修改数据导出规则。|
|[DescribeProjectMeta](/cn.zh-CN/API参考/云产品监控/DescribeProjectMeta.md)|调用DescribeProjectMeta接口查询云监控支持云服务的监控项列表。|
|[DescribeMetricLast](/cn.zh-CN/API参考/云产品监控/DescribeMetricLast.md#)|调用DescribeMetricLast接口查询指定监控项的最新监控数据。|
|[DescribeMetricMetaList](/cn.zh-CN/API参考/云产品监控/DescribeMetricMetaList.md)|调用DescribeMetricMetaList接口查询云监控开放的监控项描述。|
|[DescribeMetricList](/cn.zh-CN/API参考/云产品监控/DescribeMetricList.md)|调用DescribeMetricList接口查询指定云服务的监控数据。|
|[DescribeMetricData](/cn.zh-CN/API参考/云产品监控/DescribeMetricData.md)|调用DescribeMetricData接口查询指定时间段内云服务的监控数据。|
|[DescribeMetricTop](/cn.zh-CN/API参考/云产品监控/DescribeMetricTop.md)|调用DescribeMetricTop接口查询排序后的指定云服务的监控数据。|
|[DescribeMonitorResourceQuotaAttribute](/cn.zh-CN/API参考/云产品监控/DescribeMonitorResourceQuotaAttribute.md)|调用DescribeMonitorResourceQuotaAttribute接口查询云监控各个资源的配额。|

## 事件监控

|API|描述|
|---|--|
|[SendDryRunSystemEvent](/cn.zh-CN/API参考/事件监控/系统事件/SendDryRunSystemEvent.md)|调用SendDryRunSystemEvent接口调试资源的系统事件。|
|[DescribeSystemEventMetaList](/cn.zh-CN/API参考/事件监控/系统事件/DescribeSystemEventMetaList.md)|调用DescribeSystemEventMetaList接口查询系统事件的Meta信息。|
|[DescribeSystemEventCount](/cn.zh-CN/API参考/事件监控/系统事件/DescribeSystemEventCount.md)|调用DescribeSystemEventCount接口查询各个云服务指定时间段内事件的数量。|
|[DescribeSystemEventAttribute](/cn.zh-CN/API参考/事件监控/系统事件/DescribeSystemEventAttribute.md)|调用DescribeSystemEventAttribute接口查询系统事件详情。|
|[DescribeSystemEventHistogram](/cn.zh-CN/API参考/事件监控/系统事件/DescribeSystemEventHistogram.md)|调用DescribeSystemEventHistogram接口查询系统事件的时段数量分布图（柱状图）。|
|[DescribeCustomEventCount](/cn.zh-CN/API参考/事件监控/自定义事件/DescribeCustomEventCount.md)|调用DescribeCustomEventCount接口查询自定义事件的统计结果。|
|[DescribeCustomEventAttribute](/cn.zh-CN/API参考/事件监控/自定义事件/DescribeCustomEventAttribute.md)|调用DescribeCustomEventAttribute接口查询自定义事件的详情。|
|[PutCustomEvent](/cn.zh-CN/API参考/事件监控/自定义事件/PutCustomEvent.md)|调用PutCustomEvent接口上报自定义事件的监控数据。|
|[DescribeCustomEventHistogram](/cn.zh-CN/API参考/事件监控/自定义事件/DescribeCustomEventHistogram.md)|调用DescribeCustomEventHistogram接口查询自定义上报事件的分时段数量分布图。|

## 自定义监控

|API|描述|
|---|--|
|[PutCustomMetric](/cn.zh-CN/API参考/自定义监控/PutCustomMetric.md)|调用PutCustomMetric接口上报自定义监控数据。|
|[PutCustomMetricRule](/cn.zh-CN/API参考/自定义监控/PutCustomMetricRule.md)|调用PutCustomMetricRule接口创建自定义监控报警规则。|
|[DescribeCustomMetricList](/cn.zh-CN/API参考/自定义监控/DescribeCustomMetricList.md)|调用DescribeCustomMetricList接口查询上报的自定义监控数据。|
|[DeleteCustomMetric](/cn.zh-CN/API参考/自定义监控/DeleteCustomMetric.md)|调用DeleteCustomMetric接口删除上报的自定义监控数据。|

## 日志监控

|API|描述|
|---|--|
|[DescribeLogMonitorList](/cn.zh-CN/API参考/日志监控/DescribeLogMonitorList.md)|调用DescribeLogMonitorList接口获取日志监控列表。|
|[DescribeLogMonitorAttribute](/cn.zh-CN/API参考/日志监控/DescribeLogMonitorAttribute.md)|调用DescribeLogMonitorAttribute接口获取日志监控详情。|
|[DeleteLogMonitor](/cn.zh-CN/API参考/日志监控/DeleteLogMonitor.md)|调用DeleteLogMonitor接口删除日志监控。|
|[PutLogMonitor](/cn.zh-CN/API参考/日志监控/PutLogMonitor.md)|调用PutLogMonitor接口创建或修改日志监控。|

## 站点监控

|API|描述|
|---|--|
|[DisableSiteMonitors](/cn.zh-CN/API参考/站点监控/DisableSiteMonitors.md)|调用DisableSiteMonitors接口禁用一个或多个站点监控任务。|
|[DescribeSiteMonitorQuota](/cn.zh-CN/API参考/站点监控/DescribeSiteMonitorQuota.md)|调用DescribeSiteMonitorQuota接口查询站点监控的配额以及版本。|
|[DescribeSiteMonitorAttribute](/cn.zh-CN/API参考/站点监控/DescribeSiteMonitorAttribute.md)|调用DescribeSiteMonitorAttribute接口查询站点监控详细信息。|
|[DeleteSiteMonitors](/cn.zh-CN/API参考/站点监控/DeleteSiteMonitors.md)|调用DeleteSiteMonitors接口删除站点监控的探测任务。|
|[DescribeSiteMonitorISPCityList](/cn.zh-CN/API参考/站点监控/DescribeSiteMonitorISPCityList.md)|调用DescribeSiteMonitorISPCityList接口查询创建任务的探测点列表。|
|[DescribeSiteMonitorData](/cn.zh-CN/API参考/站点监控/DescribeSiteMonitorData.md)|调用DescribeSiteMonitorData接口查询任务的细粒度监控数据。|
|[DescribeSiteMonitorStatistics](/cn.zh-CN/API参考/站点监控/DescribeSiteMonitorStatistics.md)|调用DescribeSiteMonitorStatistics接口查询指定站点监控任务的平均统计数据。|
|[CreateSiteMonitor](/cn.zh-CN/API参考/站点监控/CreateSiteMonitor.md)|调用CreateSiteMonitor接口创建站点监控的监控任务。|
|[ModifySiteMonitor](/cn.zh-CN/API参考/站点监控/ModifySiteMonitor.md)|调用ModifySiteMonitor接口修改站点监控任务。|
|[EnableSiteMonitors](/cn.zh-CN/API参考/站点监控/EnableSiteMonitors.md)|调用EnableSiteMonitors接口启用一个或多个站点监控任务。|
|[DescribeSiteMonitorList](/cn.zh-CN/API参考/站点监控/DescribeSiteMonitorList.md)|调用DescribeSiteMonitorList接口查询站点监控任务列表。|
|[DeleteExporterOutput](/cn.zh-CN/API参考/云产品监控/DeleteExporterOutput.md)|调用DeleteExporterOutput接口删除监控数据导出配置。|
|[DeleteExporterRule](/cn.zh-CN/API参考/云产品监控/DeleteExporterRule.md)|调用DeleteExporterRule接口删除监控数据导出规则。|
|[DescribeExporterOutputList](/cn.zh-CN/API参考/云产品监控/DescribeExporterOutputList.md)|调用DescribeExporterOutputList接口查询监控数据导出列表。|
|[DescribeExporterRuleList](/cn.zh-CN/API参考/云产品监控/DescribeExporterRuleList.md)|调用DescribeExporterRuleList接口查询数据导出规则列表。|
|[PutExporterOutput](/cn.zh-CN/API参考/云产品监控/PutExporterOutput.md)|调用PutExporterOutput接口创建或修改一个监控数据导出配置。|
|[PutExporterRule](/cn.zh-CN/API参考/云产品监控/PutExporterRule.md)|调用PutExporterRule接口创建或修改数据导出规则。|
|[DescribeProjectMeta](/cn.zh-CN/API参考/云产品监控/DescribeProjectMeta.md)|调用DescribeProjectMeta接口查询云监控支持云服务的监控项列表。|
|[DescribeMetricLast](/cn.zh-CN/API参考/云产品监控/DescribeMetricLast.md#)|调用DescribeMetricLast接口查询指定监控项的最新监控数据。|
|[DescribeMetricMetaList](/cn.zh-CN/API参考/云产品监控/DescribeMetricMetaList.md)|调用DescribeMetricMetaList接口查询云监控开放的监控项描述。|
|[DescribeMetricList](/cn.zh-CN/API参考/云产品监控/DescribeMetricList.md)|调用DescribeMetricList接口查询指定云服务的监控数据。|
|[DescribeMetricData](/cn.zh-CN/API参考/云产品监控/DescribeMetricData.md)|调用DescribeMetricData接口查询指定时间段内云服务的监控数据。|
|[DescribeMetricTop](/cn.zh-CN/API参考/云产品监控/DescribeMetricTop.md)|调用DescribeMetricTop接口查询排序后的指定云服务的监控数据。|
|[DescribeMonitorResourceQuotaAttribute](/cn.zh-CN/API参考/云产品监控/DescribeMonitorResourceQuotaAttribute.md)|调用DescribeMonitorResourceQuotaAttribute接口查询云监控各个资源的配额。|

## 云产品监控

|API|描述|
|---|--|
|[DeleteExporterOutput](/cn.zh-CN/API参考/云产品监控/DeleteExporterOutput.md)|调用DeleteExporterOutput接口删除监控数据导出配置。|
|[DeleteExporterRule](/cn.zh-CN/API参考/云产品监控/DeleteExporterRule.md)|调用DeleteExporterRule接口删除监控数据导出规则。|
|[DescribeExporterOutputList](/cn.zh-CN/API参考/云产品监控/DescribeExporterOutputList.md)|调用DescribeExporterOutputList接口查询监控数据导出列表。|
|[DescribeExporterRuleList](/cn.zh-CN/API参考/云产品监控/DescribeExporterRuleList.md)|调用DescribeExporterRuleList接口查询数据导出规则列表。|
|[PutExporterOutput](/cn.zh-CN/API参考/云产品监控/PutExporterOutput.md)|调用PutExporterOutput接口创建或修改一个监控数据导出配置。|
|[PutExporterRule](/cn.zh-CN/API参考/云产品监控/PutExporterRule.md)|调用PutExporterRule接口创建或修改数据导出规则。|
|[DescribeProjectMeta](/cn.zh-CN/API参考/云产品监控/DescribeProjectMeta.md)|调用DescribeProjectMeta接口查询云监控支持云服务的监控项列表。|
|[DescribeMetricLast](/cn.zh-CN/API参考/云产品监控/DescribeMetricLast.md)|调用DescribeMetricLast接口查询指定监控项的最新监控数据。|
|[DescribeMetricMetaList](/cn.zh-CN/API参考/云产品监控/DescribeMetricMetaList.md)|调用DescribeMetricMetaList接口查询云监控开放的监控项描述。|
|[DescribeMetricList](/cn.zh-CN/API参考/云产品监控/DescribeMetricList.md)|调用DescribeMetricList接口查询指定云服务的监控数据。|
|[DescribeMetricData](/cn.zh-CN/API参考/云产品监控/DescribeMetricData.md)|调用DescribeMetricData接口查询指定时间段内云服务的监控数据。|
|[DescribeMetricTop](/cn.zh-CN/API参考/云产品监控/DescribeMetricTop.md)|调用DescribeMetricTop接口查询排序后的指定云服务的监控数据。|
|[DescribeMonitorResourceQuotaAttribute](/cn.zh-CN/API参考/云产品监控/DescribeMonitorResourceQuotaAttribute.md)|调用DescribeMonitorResourceQuotaAttribute接口查询云监控各个资源的配额。|

## 报警服务

|API|描述|
|---|--|
|[DescribeAlertHistoryList](/cn.zh-CN/API参考/报警服务/报警历史/DescribeAlertHistoryList.md)|调用DescribeAlertHistoryList接口查询报警历史详情。|
|[DescribeAlertLogCount](/cn.zh-CN/API参考/报警服务/报警历史/DescribeAlertLogCount.md)|调用DescribeAlertLogCount接口统计报警历史。|
|[DescribeAlertLogHistogram](/cn.zh-CN/API参考/报警服务/报警历史/DescribeAlertLogHistogram.md)|调用DescribeAlertLogHistogram接口查询报警历史的直方图列表。|
|[DescribeAlertLogList](/cn.zh-CN/API参考/报警服务/报警历史/DescribeAlertLogList.md)|调用DescribeAlertLogList接口查询报警历史。|
|[ApplyMetricRuleTemplate](/cn.zh-CN/API参考/报警服务/报警模板/ApplyMetricRuleTemplate.md)|调用ApplyMetricRuleTemplate接口将报警模板应用到应用分组并生成报警规则。|
|[DescribeMetricRuleTemplateAttribute](/cn.zh-CN/API参考/报警服务/报警模板/DescribeMetricRuleTemplateAttribute.md)|调用DescribeMetricRuleTemplateAttribute接口查询报警模板详情。|
|[DeleteMetricRuleTemplate](/cn.zh-CN/API参考/报警服务/报警模板/DeleteMetricRuleTemplate.md)|调用DeleteMetricRuleTemplate接口删除报警规则模板。|
|[ModifyMetricRuleTemplate](/cn.zh-CN/API参考/报警服务/报警模板/ModifyMetricRuleTemplate.md)|调用ModifyMetricRuleTemplate接口修改报警模板。|
|[CreateMetricRuleTemplate](/cn.zh-CN/API参考/报警服务/报警模板/CreateMetricRuleTemplate.md)|调用CreateMetricRuleTemplate接口创建报警模板。|
|[DescribeMetricRuleTemplateList](/cn.zh-CN/API参考/报警服务/报警模板/DescribeMetricRuleTemplateList.md)|调用DescribeMetricRuleTemplateList接口查询报警模板列表。|
|[PutResourceMetricRule](/cn.zh-CN/API参考/报警服务/阈值报警规则/PutResourceMetricRule.md)|调用PutResourceMetricRule接口对单个资源的性能指标设置阈值报警规则。|
|[DeleteMetricRules](/cn.zh-CN/API参考/报警服务/阈值报警规则/DeleteMetricRules.md)|调用DeleteMetricRules接口删除一个或多个报警规则。|
|[DescribeMetricRuleCount](/cn.zh-CN/API参考/报警服务/阈值报警规则/DescribeMetricRuleCount.md)|调用DescribeMetricRuleCount接口获取各种状态报警规则的数量。|
|[EnableMetricRules](/cn.zh-CN/API参考/报警服务/阈值报警规则/EnableMetricRules.md)|调用EnableMetricRules接口启用一个或多个报警规则。|
|[DescribeMetricRuleList](/cn.zh-CN/API参考/报警服务/阈值报警规则/DescribeMetricRuleList.md)|调用DescribeMetricRuleList接口查询报警规则列表。|
|[DisableMetricRules](/cn.zh-CN/API参考/报警服务/阈值报警规则/DisableMetricRules.md)|调用DisableMetricRules接口禁用报警规则。|
|[DescribeAlertingMetricRuleResources](/cn.zh-CN/API参考/报警服务/阈值报警规则/DescribeAlertingMetricRuleResources.md)|调用DescribeAlertingMetricRuleResources接口查询指定报警规则下报警的资源。|
|[PutMetricRuleTargets](/cn.zh-CN/API参考/报警服务/阈值报警规则/PutMetricRuleTargets.md)|调用PutMetricRuleTargets接口添加或者修改报警规则的目标。|
|[DescribeMetricRuleTargets](/cn.zh-CN/API参考/报警服务/阈值报警规则/DescribeMetricRuleTargets.md)|调用DescribeMetricRuleTargets接口查询报警规则关联目标。|
|[DeleteMetricRuleTargets](/cn.zh-CN/API参考/报警服务/阈值报警规则/DeleteMetricRuleTargets.md)|调用DeleteMetricRuleTargets接口删除一个报警规则的目标。|
|[CreateMetricRuleResources](/cn.zh-CN/API参考/报警服务/阈值报警规则/CreateMetricRuleResources.md)|调用CreateMetricRuleResources接口创建一个报警规则关联的资源。|
|[DeleteMetricRuleResources](/cn.zh-CN/API参考/报警服务/阈值报警规则/DeleteMetricRuleResources.md)|调用DeleteMetricRuleResources接口删除报警规则关联的资源。|
|[DescribeEventRuleAttribute](/cn.zh-CN/API参考/报警服务/事件报警规则/DescribeEventRuleAttribute.md)|调用DescribeEventRuleAttribute接口查询指定报警规则的详情。|
|[PutEventRuleTargets](/cn.zh-CN/API参考/报警服务/事件报警规则/PutEventRuleTargets.md)|调用PutEventRuleTargets接口添加或修改规则的发送目标。|
|[DeleteEventRuleTargets](/cn.zh-CN/API参考/报警服务/事件报警规则/DeleteEventRuleTargets.md)|调用DeleteEventRuleTargets接口删除事件报警通知目标。|
|[EnableEventRules](/cn.zh-CN/API参考/报警服务/事件报警规则/EnableEventRules.md)|调用EnableEventRules接口启用一个或者多个事件监控报警规则。|
|[DescribeEventRuleList](/cn.zh-CN/API参考/报警服务/事件报警规则/DescribeEventRuleList.md)|调用DescribeEventRuleList接口查询事件报警规则列表。|
|[DeleteEventRules](/cn.zh-CN/API参考/报警服务/事件报警规则/DeleteEventRules.md)|调用DeleteEventRules接口删除事件报警规则。|
|[DisableEventRules](/cn.zh-CN/API参考/报警服务/事件报警规则/DisableEventRules.md)|调用DisableEventRule接口禁用一个或多个事件报警规则。|
|[PutEventRule](/cn.zh-CN/API参考/报警服务/事件报警规则/PutEventRule.md)|调用PutEventRule接口创建或修改事件的报警规则。|
|[DescribeEventRuleTargetList](/cn.zh-CN/API参考/报警服务/事件报警规则/DescribeEventRuleTargetList.md)|调用DescribeEventRuleTargetList接口查询指定事件报警规则的报警目标。|
|[PutCustomEventRule](/cn.zh-CN/API参考/报警服务/事件报警规则/PutCustomEventRule.md)|调用PutCustomEventRule接口创建自定义事件报警规则。|
|[PutContactGroup](/cn.zh-CN/API参考/报警服务/报警联系人/PutContactGroup.md)|调用PutContactGroup接口创建或修改报警联系组。|
|[DescribeContactList](/cn.zh-CN/API参考/报警服务/报警联系人/DescribeContactList.md)|调用DescribeContactList接口查询报警联系人列表。|
|[DeleteContact](/cn.zh-CN/API参考/报警服务/报警联系人/DeleteContact.md)|调用DeleteContact接口删除报警联系人。|
|[PutContact](/cn.zh-CN/API参考/报警服务/报警联系人/PutContact.md)|调用PutContact接口创建或修改报警联系人信息。|
|[DescribeContactGroupList](/cn.zh-CN/API参考/报警服务/报警联系人/DescribeContactGroupList.md)|调用DescribeContactGroupList接口查询报警联系组列表。|
|[DeleteContactGroup](/cn.zh-CN/API参考/报警服务/报警联系人/DeleteContactGroup.md)|调用DeleteContactGroup接口删除报警联系人组。|
|[DescribeContactListByContactGroup](/cn.zh-CN/API参考/报警服务/报警联系人/DescribeContactListByContactGroup.md)|调用DescribeContactListByContactGroup接口查询报警联系组中的报警联系人列表。|
|[DescribeProductsOfActiveMetricRule](/cn.zh-CN/API参考/报警服务/一键报警/DescribeProductsOfActiveMetricRule.md)|调用DescribeProductsOfActiveMetricRule接口查询开通一键报警规则的云服务列表。|
|[EnableActiveMetricRule](/cn.zh-CN/API参考/报警服务/一键报警/EnableActiveMetricRule.md)|调用EnableActiveMetricRule接口启用一键报警规则。|
|[DescribeActiveMetricRuleList](/cn.zh-CN/API参考/报警服务/一键报警/DescribeActiveMetricRuleList.md)|调用DescribeActiveMetricRuleList接口查询一键报警规则的列表详情。|
|[DisableActiveMetricRule](/cn.zh-CN/API参考/报警服务/一键报警/DisableActiveMetricRule.md)|调用DisableActiveMetricRule接口禁用一键报警规则。|

