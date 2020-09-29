# List of operations by function

The following tables list API operations available for use in Cloud Monitor.

## Monitoring data on time series metrics of cloud services

|Operation|Description|
|---------|-----------|
|[DeleteExporterOutput](/intl.en-US/API Reference/Monitoring data on time series metrics of cloud services/DeleteExporterOutput.md)|Deletes a configuration set for exporting monitoring data.|
|[DeleteExporterRule](/intl.en-US/API Reference/Monitoring data on time series metrics of cloud services/DeleteExporterRule.md)|Deletes a data export rule.|
|[DescribeExporterOutputList](/intl.en-US/API Reference/Monitoring data on time series metrics of cloud services/DescribeExporterOutputList.md)|Queries configuration sets for exporting monitoring data.|
|[DescribeExporterRuleList](/intl.en-US/API Reference/Monitoring data on time series metrics of cloud services/DescribeExporterRuleList.md)|Queries data export rules.|
|[DescribeMetricLast](/intl.en-US/API Reference/Monitoring data on time series metrics of cloud services/DescribeMetricLast.md)|Queries the latest monitoring data of a metric.|
|[PutExporterOutput](/intl.en-US/API Reference/Monitoring data on time series metrics of cloud services/PutExporterOutput.md)|Creates or modifies a configuration set for exporting monitoring data.|
|[DescribeMetricMetaList](/intl.en-US/API Reference/Monitoring data on time series metrics of cloud services/DescribeMetricMetaList.md)|Queries the descriptions of time series metrics that are supported in Cloud Monitor.|
|[PutExporterRule](/intl.en-US/API Reference/Monitoring data on time series metrics of cloud services/PutExporterRule.md)|Creates or modifies a data export rule.|
|[DescribeMetricList](/intl.en-US/API Reference/Monitoring data on time series metrics of cloud services/DescribeMetricList.md)|Queries the monitoring data on a time series metric of a cloud service in a specified period.|
|[DescribeMetricData](/intl.en-US/API Reference/Monitoring data on time series metrics of cloud services/DescribeMetricData.md)|Queries the monitoring data on a time series metric of a cloud service in a specified period.|
|[DescribeProjectMeta](/intl.en-US/API Reference/Monitoring data on time series metrics of cloud services/DescribeProjectMeta.md)|Queries information about monitored services in Cloud Monitor.|

## Alert rules for time series metrics

|Operation|Description|
|---------|-----------|
|[DescribeProductsOfActiveMetricRule](/intl.en-US/API Reference/Alert rules for time series metrics/DescribeProductsOfActiveMetricRule.md)|Queries the services for which one-click alert is enabled.|
|[EnableActiveMetricRule](/intl.en-US/API Reference/Alert rules for time series metrics/EnableActiveMetricRule.md)|Enables one-click alert for a service.|
|[DescribeActiveMetricRuleList](/intl.en-US/API Reference/Alert rules for time series metrics/DescribeActiveMetricRuleList.md)|Queries details about one-click alert rules.|
|[PutResourceMetricRule](/intl.en-US/API Reference/Alert rules for time series metrics/PutResourceMetricRule.md)|Creates an alert rule for a performance metric of a resource.|
|[DescribeMetricRuleList](/intl.en-US/API Reference/Alert rules for time series metrics/DescribeMetricRuleList.md)|Queries alert rules.|
|[DeleteMetricRules](/intl.en-US/API Reference/Alert rules for time series metrics/DeleteMetricRules.md)|Deletes one or more alert rules.|
|[DisableMetricRules](/intl.en-US/API Reference/Alert rules for time series metrics/DisableMetricRules.md)|Disables one or more alert rules.|
|[DescribeMetricRuleCount](/intl.en-US/API Reference/Alert rules for time series metrics/DescribeMetricRuleCount.md)|Queries the number of alert rules in each state.|
|[CreateGroupMetricRules](/intl.en-US/API Reference/Alert rules for time series metrics/CreateGroupMetricRules.md)|Creates multiple alert rules for an application group at a time.|
|[DisableActiveMetricRule](/intl.en-US/API Reference/Alert rules for time series metrics/DisableActiveMetricRule.md)|Disables one-click alert for a service.|
|[EnableMetricRules](/intl.en-US/API Reference/Alert rules for time series metrics/EnableMetricRules.md)|Enables one or more alert rules.|
|[DescribeAlertHistoryList](/intl.en-US/API Reference/Alert rules for time series metrics/DescribeAlertHistoryList.md)|Queries historical alerts.|
|[PutGroupMetricRule](/intl.en-US/API Reference/Alert rules for time series metrics/PutGroupMetricRule.md)|Creates or modifies an alert rule for an application group.|
|[DescribeAlertingMetricRuleResources](/intl.en-US/API Reference/Alert rules for time series metrics/DescribeAlertingMetricRuleResources.md)|Queries the resources with active alerts triggered based on an alert rule.|
|[PutMetricRuleTargets](/intl.en-US/API Reference/Alert rules for time series metrics/PutMetricRuleTargets.md)|Adds or modifies the message resource of an alert rule.|
|[DescribeMetricRuleTargets](/intl.en-US/API Reference/Alert rules for time series metrics/DescribeMetricRuleTargets.md)|Queries the message resources of an alert rule.|
|[DeleteMetricRuleTargets](/intl.en-US/API Reference/Alert rules for time series metrics/DeleteMetricRuleTargets.md)|Deletes the message resources of an alert rule.|
|[CreateMetricRuleResources](/intl.en-US/API Reference/Alert rules for time series metrics/CreateMetricRuleResources.md)|Associates resources with an alert rule.|
|[DeleteMetricRuleResources](/intl.en-US/API Reference/Alert rules for time series metrics/DeleteMetricRuleResources.md)|Disassociates resources from an alert rule.|

## Host monitoring

|Operation|Description|
|---------|-----------|
|[DeleteMonitoringAgentProcess](/intl.en-US/API Reference/Host monitoring/DeleteMonitoringAgentProcess.md)|Disables monitoring on a process.|
|[DescribeMonitoringAgentStatuses](/intl.en-US/API Reference/Host monitoring/DescribeMonitoringAgentStatuses.md)|Queries the status of the Cloud Monitor agent.|
|[DescribeMonitoringAgentProcesses](/intl.en-US/API Reference/Host monitoring/DescribeMonitoringAgentProcesses.md)|Queries monitored processes.|
|[DescribeMonitoringAgentAccessKey](/intl.en-US/API Reference/Host monitoring/DescribeMonitoringAgentAccessKey.md)|Queries the AccessKey ID and AccessKey secret required for installing the Cloud Monitor agent on a host that is not an Elastic Compute Service \(ECS\) instance.|
|[UninstallMonitoringAgent](/intl.en-US/API Reference/Host monitoring/UninstallMonitoringAgent.md)|Uninstalls the Cloud Monitor agent from a host that is not an ECS instance.|
|[InstallMonitoringAgent](/intl.en-US/API Reference/Host monitoring/InstallMonitoringAgent.md)|Installs the Cloud Monitor agent on a specified ECS instance. This operation is applicable only to ECS instances.|
|[CreateMonitoringAgentProcess](/intl.en-US/API Reference/Host monitoring/CreateMonitoringAgentProcess.md)|Creates a task to monitor a specified process.|
|[DescribeMonitoringAgentHosts](/intl.en-US/API Reference/Host monitoring/DescribeMonitoringAgentHosts.md)|Queries hosts with and without the Cloud Monitor agent installed.|
|[DescribeMonitoringAgentConfig](/intl.en-US/API Reference/Host monitoring/DescribeMonitoringAgentConfig.md)|Queries the configuration of the Cloud Monitor agent.|
|[CreateMonitorAgentProcess](/intl.en-US/API Reference/Host monitoring/CreateMonitorAgentProcess.md)|Creates a task to monitor a specified process.|
|[ModifyHostInfo](/intl.en-US/API Reference/Host monitoring/ModifyHostInfo.md)|Modifies the display information of a host that is not an ECS instance.|

## Alert groups

|Operation|Description|
|---------|-----------|
|[DescribeContactListByContactGroup](/intl.en-US/API Reference/Alert groups/DescribeContactListByContactGroup.md)|Queries the alert contacts in an alert group.|
|[DeleteContactGroup](/intl.en-US/API Reference/Alert groups/DeleteContactGroup.md)|Deletes an alert group.|
|[DescribeContactGroupList](/intl.en-US/API Reference/Alert groups/DescribeContactGroupList.md)|Queries alert groups.|
|[PutContact](/intl.en-US/API Reference/Alert groups/PutContact.md)|Creates or modifies an alert contact.|
|[DeleteContact](/intl.en-US/API Reference/Alert groups/DeleteContact.md)|Deletes an alert contact.|
|[DescribeContactList](/intl.en-US/API Reference/Alert groups/DescribeContactList.md)|Queries alert contacts.|
|[PutContactGroup](/intl.en-US/API Reference/Alert groups/PutContactGroup.md)|Creates or modifies an alert group.|

## Availability monitoring

|Operation|Description|
|---------|-----------|
|[CreateHostAvailability](/intl.en-US/API Reference/Availability monitoring/CreateHostAvailability.md)|Creates an availability monitoring task.|
|[DeleteHostAvailability](/intl.en-US/API Reference/Availability monitoring/DeleteHostAvailability.md)|Deletes one or more availability monitoring tasks.|
|[EnableHostAvailability](/intl.en-US/API Reference/Availability monitoring/EnableHostAvailability.md)|Enables one or more availability monitoring tasks.|
|[ModifyHostAvailability](/intl.en-US/API Reference/Availability monitoring/ModifyHostAvailability.md)|Modifies an availability monitoring task.|
|[DescribeHostAvailabilityList](/intl.en-US/API Reference/Availability monitoring/DescribeHostAvailabilityList.md)|Queries availability monitoring tasks.|
|[DescribeUnhealthyHostAvailability](/intl.en-US/API Reference/Availability monitoring/DescribeUnhealthyHostAvailability.md)|Queries unhealthy instances.|
|[DisableHostAvailability](/intl.en-US/API Reference/Availability monitoring/DisableHostAvailability.md)|Disables one or more availability monitoring tasks.|

## Global configurations of the Cloud Monitor agent

|Operation|Description|
|---------|-----------|
|[DescribeMonitoringConfig](/intl.en-US/API Reference/Global configurations/DescribeMonitoringConfig.md)|Queries the global configurations of the Cloud Monitor agent.|
|[PutMonitoringConfig](/intl.en-US/API Reference/Global configurations/PutMonitoringConfig.md)|Sets global configurations for the Cloud Monitor agent. For example, you can enable automatic agent installation or one-click alert.|

## System events of cloud services

|Operation|Description|
|---------|-----------|
|[SendDryRunSystemEvent](/intl.en-US/API Reference/System events of cloud services/SendDryRunSystemEvent.md)|Simulates a system event to test whether the response after an alert is triggered is as expected.|
|[DescribeSystemEventMetaList](/intl.en-US/API Reference/System events of cloud services/DescribeSystemEventMetaList.md)|Queries the meta information of system events.|
|[DescribeSystemEventCount](/intl.en-US/API Reference/System events of cloud services/DescribeSystemEventCount.md)|Queries the number of times that a system event occurred in a specified time period.|
|[DescribeSystemEventAttribute](/intl.en-US/API Reference/System events of cloud services/DescribeSystemEventAttribute.md)|Queries the details of a system event occurred in a specified time period.|
|[DescribeSystemEventHistogram](/intl.en-US/API Reference/System events of cloud services/DescribeSystemEventHistogram.md)|Queries the number of times that a system event occurred during each interval of a time period.|

## Alert templates for time series metrics

|Operation|Description|
|---------|-----------|
|[DescribeMetricRuleTemplateList](/intl.en-US/API Reference/Alert templates for time series metrics/DescribeMetricRuleTemplateList.md)|Queries alert templates.|
|[ApplyMetricRuleTemplate](/intl.en-US/API Reference/Alert templates for time series metrics/ApplyMetricRuleTemplate.md)|Applies an alert template to an application group to generate alert rules.|
|[DescribeMetricRuleTemplateAttribute](/intl.en-US/API Reference/Alert templates for time series metrics/DescribeMetricRuleTemplateAttribute.md)|Queries the details of an alert template.|
|[CreateMetricRuleTemplate](/intl.en-US/API Reference/Alert templates for time series metrics/CreateMetricRuleTemplate.md)|Creates an alert template.|
|[ModifyMetricRuleTemplate](/intl.en-US/API Reference/Alert templates for time series metrics/ModifyMetricRuleTemplate.md)|Modifies an alert template.|
|[DeleteMetricRuleTemplate](/intl.en-US/API Reference/Alert templates for time series metrics/DeleteMetricRuleTemplate.md)|Deletes an alert template.|

## Event-triggered alert rules

|Operation|Description|
|---------|-----------|
|[DescribeEventRuleAttribute](/intl.en-US/API Reference/Event-triggered alert rules/DescribeEventRuleAttribute.md)|Queries the details of an event-triggered alert rule.|
|[PutEventRuleTargets](/intl.en-US/API Reference/Event-triggered alert rules/PutEventRuleTargets.md)|Adds or modifies the targets to which alert notifications are sent based on an event-triggered alert rule.|
|[DeleteEventRuleTargets](/intl.en-US/API Reference/Event-triggered alert rules/DeleteEventRuleTargets.md)|Deletes the targets to which alert notifications are sent based on an event-triggered alert rule.|
|[EnableEventRules](/intl.en-US/API Reference/Event-triggered alert rules/EnableEventRules.md)|Enables one or more event-triggered alert rules.|
|[DescribeEventRuleList](/intl.en-US/API Reference/Event-triggered alert rules/DescribeEventRuleList.md)|Queries event-triggered alert rules.|
|[DeleteEventRules](/intl.en-US/API Reference/Event-triggered alert rules/DeleteEventRules.md)|Deletes one or more event-triggered alert rules.|
|[DisableEventRules](/intl.en-US/API Reference/Event-triggered alert rules/DisableEventRules.md)|Disables one or more event-triggered alert rules.|
|[PutEventRule](/intl.en-US/API Reference/Event-triggered alert rules/PutEventRule.md)|Creates or modifies an event-triggered alert rule.|
|[DescribeEventRuleTargetList](/intl.en-US/API Reference/Event-triggered alert rules/DescribeEventRuleTargetList.md)|Queries the targets of an event-triggered alert rule.|

## Custom monitoring

|Operation|Description|
|---------|-----------|
|[PutCustomMetric](/intl.en-US/API Reference/Custom monitoring/PutCustomMetric.md)|Reports monitoring data.|
|[DescribeCustomMetricList](/intl.en-US/API Reference/Custom monitoring/DescribeCustomMetricList.md)|Queries the reported monitoring data.|
|[DeleteCustomMetric](/intl.en-US/API Reference/Custom monitoring/DeleteCustomMetric.md)|Deletes the reported monitoring data of a metric.|

## Custom events

|Operation|Description|
|---------|-----------|
|[DescribeCustomEventCount](/intl.en-US/API Reference/Custom events/DescribeCustomEventCount.md)|Queries the number of times that a custom event occurred in a specified time period.|
|[DescribeCustomEventAttribute](/intl.en-US/API Reference/Custom events/DescribeCustomEventAttribute.md)|Queries the details of a custom event occurred in a specified time period.|
|[PutCustomEvent](/intl.en-US/API Reference/Custom events/PutCustomEvent.md)|Reports one or more custom events.|
|[DescribeCustomEventHistogram](/intl.en-US/API Reference/Custom events/DescribeCustomEventHistogram.md)|Queries the number of times that a custom event occurred during each interval of a time period.|

## Application groups

|Operation|Description|
|---------|-----------|
|[DeleteMonitorGroupInstances](/intl.en-US/API Reference/Application groups/DeleteMonitorGroupInstances.md)|Deletes instances from an application group.|
|[PutMonitorGroupDynamicRule](/intl.en-US/API Reference/Application groups/PutMonitorGroupDynamicRule.md)|Creates or modifies a rule to dynamically add instances of a service that meet the rule to an application group.|
|[DeleteMonitorGroupDynamicRule](/intl.en-US/API Reference/Application groups/DeleteMonitorGroupDynamicRule.md)|Deletes a rule that is used to dynamically add instances of a service that meet the rule to an application group.|
|[ModifyMonitorGroupInstances](/intl.en-US/API Reference/Application groups/ModifyMonitorGroupInstances.md)|Changes the instances added to an application group.|
|[DescribeMonitorGroupDynamicRules](/intl.en-US/API Reference/Application groups/DescribeMonitorGroupDynamicRules.md)|Queries the rules that are used to dynamically add instances of services that meet the rules to an application group.|
|[CreateMonitorGroupNotifyPolicy](/intl.en-US/API Reference/Application groups/CreateMonitorGroupNotifyPolicy.md)|Creates a policy to pause alert notifications for an application group.|
|[DescribeMonitorGroupInstanceAttribute](/intl.en-US/API Reference/Application groups/DescribeMonitorGroupInstanceAttribute.md)|Queries detailed information about the instances in an application group.|
|[DescribeMonitorGroupCategories](/intl.en-US/API Reference/Application groups/DescribeMonitorGroupCategories.md)|Queries the services to which the resources in an application group belong and the number of instances that belong to each service in the application group.|
|[CreateMonitorGroup](/intl.en-US/API Reference/Application groups/CreateMonitorGroup.md)|Creates an application group.|
|[CreateMonitorGroupInstances](/intl.en-US/API Reference/Application groups/CreateMonitorGroupInstances.md)|Adds resources to an application group.|
|[DeleteMonitorGroupNotifyPolicy](/intl.en-US/API Reference/Application groups/DeleteMonitorGroupNotifyPolicy.md)|Deletes a policy that is used to pause alert notifications for an application group.|
|[ModifyMonitorGroup](/intl.en-US/API Reference/Application groups/ModifyMonitorGroup.md)|Modifies an application group.|
|[DescribeMonitorGroupNotifyPolicyList](/intl.en-US/API Reference/Application groups/DescribeMonitorGroupNotifyPolicyList.md)|Queries policies that are used to pause alert notifications for an application group.|
|[DescribeMonitorGroupInstances](/intl.en-US/API Reference/Application groups/DescribeMonitorGroupInstances.md)|Queries the resources in an application group.|
|[DeleteMonitorGroup](/intl.en-US/API Reference/Application groups/DeleteMonitorGroup.md)|Deletes an application group.|
|[DescribeMonitorGroups](/intl.en-US/API Reference/Application groups/DescribeMonitorGroups.md)|Queries application groups.|
|[CreateGroupMonitoringAgentProcess](/intl.en-US/API Reference/Application groups/CreateGroupMonitoringAgentProcess.md)|Creates a process monitoring task for an application group.|
|[DescribeGroupMonitoringAgentProcess](/intl.en-US/API Reference/Application groups/DescribeGroupMonitoringAgentProcess.md)|Queries a process monitoring tasks for an application group.|
|[ModifyGroupMonitoringAgentProcess](/intl.en-US/API Reference/Application groups/ModifyGroupMonitoringAgentProcess.md)|Modifies a process monitoring task for an application group.|
|[DeleteGroupMonitoringAgentProcess](/intl.en-US/API Reference/Application groups/DeleteGroupMonitoringAgentProcess.md)|Deletes a process monitoring task for an application group.|

## Site monitoring

|Operation|Description|
|---------|-----------|
|[DescribeSiteMonitorData](/intl.en-US/API Reference/Site monitoring/DescribeSiteMonitorData.md)|Queries the fine-grained monitoring data of a site monitoring task.|
|[DisableSiteMonitors](/intl.en-US/API Reference/Site monitoring/DisableSiteMonitors.md)|Disables one or more site monitoring tasks.|
|[DescribeSiteMonitorQuota](/intl.en-US/API Reference/Site monitoring/DescribeSiteMonitorQuota.md)|Queries the quota and version of site monitoring.|
|[DescribeSiteMonitorAttribute](/intl.en-US/API Reference/Site monitoring/DescribeSiteMonitorAttribute.md)|Queries the details about a site monitoring task.|
|[DeleteSiteMonitors](/intl.en-US/API Reference/Site monitoring/DeleteSiteMonitors.md)|Deletes one or more site monitoring tasks.|
|[DescribeSiteMonitorISPCityList](/intl.en-US/API Reference/Site monitoring/DescribeSiteMonitorISPCityList.md)|Queries the detection points that are available for creating site monitoring tasks.|
|[DescribeSiteMonitorStatistics](/intl.en-US/API Reference/Site monitoring/DescribeSiteMonitorStatistics.md)|Queries the statistics of a site monitoring task in a specified period.|
|[CreateSiteMonitor](/intl.en-US/API Reference/Site monitoring/CreateSiteMonitor.md)|Creates a site monitoring task.|
|[EnableSiteMonitors](/intl.en-US/API Reference/Site monitoring/EnableSiteMonitors.md)|Enables one or more site monitoring tasks.|
|[ModifySiteMonitor](/intl.en-US/API Reference/Site monitoring/ModifySiteMonitor.md)|Modifies a site monitoring task.|
|[DescribeSiteMonitorList](/intl.en-US/API Reference/Site monitoring/DescribeSiteMonitorList.md)|Queries site monitoring tasks.|

## Tags

|Operation|Description|
|---------|-----------|
|[AddTags](/intl.en-US/API Reference/Tags/AddTags.md)|Creates one or more tags for the specified resources.|
|[DescribeTagValueList](/intl.en-US/API Reference/Tags/DescribeTagValueList.md)|Queries tag values.|
|[DescribeTagKeyList](/intl.en-US/API Reference/Tags/DescribeTagKeyList.md)|Queries tag keys.|
|[RemoveTags](/intl.en-US/API Reference/Tags/RemoveTags.md)|Deletes one or more tags.|

## Log monitoring

|Operation|Description|
|---------|-----------|
|[DescribeLogMonitorList](/intl.en-US/API Reference/Log monitoring/DescribeLogMonitorList.md)|Queries log monitoring metrics.|
|[DescribeLogMonitorAttribute](/intl.en-US/API Reference/Log monitoring/DescribeLogMonitorAttribute.md)|Queries the details of a log monitoring metric.|
|[DeleteLogMonitor](/intl.en-US/API Reference/Log monitoring/DeleteLogMonitor.md)|Deletes a log monitoring metric.|
|[PutLogMonitor](/intl.en-US/API Reference/Log monitoring/PutLogMonitor.md)|Creates or modifies a log monitoring metric.|

