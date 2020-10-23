# Control permissions of RAM users

Yon can control the permissions of Resource Access Management \(RAM\) users to manage monitoring data, alert rules, alert contacts, and alert groups in Cloud Monitor.

## Permissions

Permissions that can be granted to RAM users include read-only and management permissions. A RAM user with read-only permissions can only view monitoring data and alert data.

## Authentication types

Cloud Monitor also supports authentication based on the access time or IP address, and multi-factor authentication \(MFA\).

## Resource description

You can describe resources only by using the wildcard character \(\*\), which indicates all resources. Fine-grained resource description is not supported.

## Action description

-   Actions on monitoring data

    Actions on monitoring data are divided into the following two types: actions that display instances of Alibaba Cloud services and actions that query monitoring data of Cloud Monitor. When you authorize a RAM user to view monitoring data in the Cloud Monitor console, you must grant the permissions to perform both the preceding two types of actions to the RAM user.

    The following table describes the actions on monitoring data.

    |Alibaba Cloud service|Action|
    |:--------------------|:-----|
    |Cloud Monitor|DescribeMetricList|
    |Cloud Monitor|DescribeMetricLast|
    |Elastic Compute Service \(ECS\)|DescribeInstances|
    |ApsaraDB RDS|DescribeDBInstances|
    |Server Load Balancer \(SLB\)|DescribeLoadBalancer\*|
    |Object Storage Service \(OSS\)|ListBuckets|
    |ApsaraDB for Memcache|DescribeInstances|
    |Elastic IP Address \(EIP\)|DescribeEipAddresses|
    |ApsaraDB for Redis|DescribeInstances|
    |Message Service \(MNS\)|ListQueue|
    |CDN|DescribeUserDomains|

-   Actions on alert data

    Actions on alert data allow RAM users to manage alert rules, alert contacts, and alert groups, and subscribe to events. Actions on alert data are divided into query actions and management actions.

    The following table describes the query actions on alert data.

    |Action|Description|
    |:-----|:----------|
    |DescribeMetricRuleList|Queries alert rules.|
    |DescribeMetricRuleTemplateList|Queries alert templates.|
    |DescribeAlertHistoryList|Queries the alert history.|
    |DescribeContactGroupList|Queries alert groups.|
    |DescribeContactList|Queries alert contacts.|

    The following table describes the management actions on alert data.

    |Action|Description|
    |:-----|:----------|
    |PutResourceMetricRule|Creates or modifies an alert rule for an instance.|
    |PutGroupMetricRule|Creates or modifies an alert rule for an application group.|
    |DeleteMetricRules|Deletes alert rules.|
    |DisableMetricRules|Disables alert rules.|
    |EnableMetricRules|Enables alert rules.|
    |PutContact|Creates or modifies an alert contact.|
    |DeleteContact|Deletes an alert contact.|
    |PutContactGroup|Creates an alert group.|
    |DeleteContactGroup|Deletes an alert group.|


In the Cloud Monitor API of version 2019-01-01, the names of API operations are optimized. API operations whose names start with Describe are read-only API operations. Other API operations are management API operations.

