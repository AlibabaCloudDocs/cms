# PutGroupMetricRule

Creates or modifies an alert rule for an application group.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=PutGroupMetricRule&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|PutGroupMetricRule|The operation that you want to perform. Set the value to PutGroupMetricRule. |
|Category|String|Yes|ecs|The name of the cloud service. Valid values:

 -   ecs: Elastic Compute Service \(ECS\) instances that are provided by Alibaba Cloud and hosts that are not provided by Alibaba Cloud
-   rds: ApsaraDB RDS
-   ads: AnalyticDB
-   slb: Server Load Balancer \(SLB\)
-   vpc: Virtual Private Cloud \(VPC\)
-   apigateway: API Gateway
-   cdn: Alibaba Cloud Content Delivery Network \(CDN\)
-   cs: Container Service for Swarm
-   dcdn: Dynamic Route for CDN \(DCDN\)
-   ddos: Anti-DDoS
-   eip: Elastic IP Address \(EIP\)
-   elasticsearch: Elasticsearch
-   emr: E-MapReduce
-   ess: Auto Scaling
-   hbase: ApsaraDB for HBase
-   iot\_edge: IoT Edge
-   k8s\_pod: pods in Container Service for Kubernetes \(ACK\)
-   kvstore\_sharding: ApsaraDB for Redis of the cluster master-replica architecture
-   kvstore\_splitrw: ApsaraDB for Redis of the read/write splitting architecture
-   kvstore\_standard: ApsaraDB for Redis of the standard master-replica architecture
-   memcache: ApsaraDB for Memcache
-   mns: Message Service \(MNS\)
-   mongodb: ApsaraDB for MongoDB of the replica set architecture
-   mongodb\_cluster: ApsaraDB for MongoDB of the cluster architecture
-   mongodb\_sharding: ApsaraDB for MongoDB of the sharded cluster architecture
-   mq\_topic: MNS topics
-   ocs: ApsaraDB for Memcache of earlier versions
-   opensearch: Open Search
-   oss: Object Storage Service \(OSS\)
-   polardb: PolarDB
-   petadata: HybridDB for MySQL
-   scdn: Secure CDN \(SCDN\)
-   sharebandwidthpackages: EIP Bandwidth Plan
-   sls: Log Service
-   vpn: VPN Gateway |
|GroupId|String|Yes|123456|The ID of the application group. |
|MetricName|String|Yes|cpu\_total|The name of the metric.

 **Note:** For more information, see [Metrics](~~163515~~). |
|Namespace|String|Yes|acs\_ecs\_dashboard|The namespace of the cloud service.

 **Note:** For more information, see [Metrics](~~163515~~). |
|RuleId|String|Yes|bfae2ca5b4e07d2c7278772eccda169808c7b\*\*\*\*|The ID of the alert rule. |
|RuleName|String|Yes|rule1|The name of the alert rule. |
|Dimensions|String|No|\[\{"instanceId":"i-m5e1qg6uo38rztr4\*\*\*\*"\}\]|The dimensions that specify the resources for which you want to query metric data

 Set the value to a set of key-value pairs. A typical pair is `instanceId:i-m5e1qg6uo38rztr4****`.

 The key and value can be 1 to 64 bytes in length. Excessive characters are truncated.

 The key and value can contain letters, digits, periods \(.\), hyphens \(-\), underscores \(\_\), forward slashes \(/\), and backslashes \(\\\).

 **Note:** Dimensions must be formatted as a JSON string in a specified order. |
|EffectiveInterval|String|No|00:00-23:59|The time period during which the alert rule is effective. |
|NoEffectiveInterval|String|No|00:00-05:30|The time period during which the alert rule is ineffective. |
|SilenceTime|Integer|No|86400|The mute period during which new alerts are not reported even if the alert trigger conditions are met. Unit: seconds. Default value: 86400. |
|Period|String|No|60|The aggregation period of the metric data. Unit: seconds. The value is an integral multiple of 60. Default value: 300. |
|Interval|String|No|60|The interval at which Cloud Monitor checks whether the alert rule is triggered. Unit: seconds.

 **Note:** We recommend that you set this interval to the data aggregation period. If this interval is shorter than the data aggregation period, alerts cannot be triggered due to insufficient data. |
|Webhook|String|No|https://www.aliyun.com|The callback URL. |
|EmailSubject|String|No|ECS instance|The subject of the alert notification email. |
|ContactGroups|String|No|ECS\_Group1|The alert groups that receive alert notifications for the application group. |
|Escalations.Critical.Statistics|String|No|Average|The statistical aggregation method for critical-level alerts.

 **Note:** For more information, see [DescribeMetricMetaList](~~98846~~). |
|Escalations.Critical.ComparisonOperator|String|No|GreaterThanOrEqualToThreshold|The comparison operator of the threshold for critical-level alerts. Valid values:

 -   GreaterThanOrEqualToThreshold: greater than or equal to the threshold
-   GreaterThanThreshold: greater than the threshold
-   LessThanOrEqualToThreshold: less than or equal to the threshold
-   LessThanThreshold: less than the threshold
-   NotEqualToThreshold: not equal to the threshold
-   GreaterThanYesterday: greater than the metric value at the same time yesterday
-   LessThanYesterday: less than the metric value at the same time yesterday
-   GreaterThanLastWeek: greater than the metric value at the same time last week
-   LessThanLastWeek: less than the metric value at the same time last week
-   GreaterThanLastPeriod: greater than the metric value in the last monitoring cycle
-   LessThanLastPeriod: less than the metric value in the last monitoring cycle |
|Escalations.Critical.Threshold|String|No|90|The threshold for critical-level alerts. |
|Escalations.Critical.Times|Integer|No|3|The consecutive number of times for which the metric value is measured before a critical-level alert is triggered. |
|Escalations.Warn.Statistics|String|No|Average|The statistical aggregation method for warn-level alerts.

 **Note:** For more information, see [DescribeMetricMetaList](~~98846~~). |
|Escalations.Warn.ComparisonOperator|String|No|GreaterThanOrEqualToThreshold|The comparison operator of the threshold for warn-level alerts. Valid values:

 -   GreaterThanOrEqualToThreshold: greater than or equal to the threshold
-   GreaterThanThreshold: greater than the threshold
-   LessThanOrEqualToThreshold: less than or equal to the threshold
-   LessThanThreshold: less than the threshold
-   NotEqualToThreshold: not equal to the threshold
-   GreaterThanYesterday: greater than the metric value at the same time yesterday
-   LessThanYesterday: less than the metric value at the same time yesterday
-   GreaterThanLastWeek: greater than the metric value at the same time last week
-   LessThanLastWeek: less than the metric value at the same time last week
-   GreaterThanLastPeriod: greater than the metric value in the last monitoring cycle
-   LessThanLastPeriod: less than the metric value in the last monitoring cycle |
|Escalations.Warn.Threshold|String|No|90|The threshold for warn-level alerts. |
|Escalations.Warn.Times|Integer|No|3|The consecutive number of times for which the metric value is measured before a warn-level alert is triggered. |
|Escalations.Info.Statistics|String|No|Average|The statistical aggregation method for info-level alerts.

 **Note:** For more information, see [DescribeMetricMetaList](~~98846~~). |
|Escalations.Info.ComparisonOperator|String|No|GreaterThanOrEqualToThreshold|The comparison operator of the threshold for info-level alerts. Valid values:

 -   GreaterThanOrEqualToThreshold: greater than or equal to the threshold
-   GreaterThanThreshold: greater than the threshold
-   LessThanOrEqualToThreshold: less than or equal to the threshold
-   LessThanThreshold: less than the threshold
-   NotEqualToThreshold: not equal to the threshold
-   GreaterThanYesterday: greater than the metric value at the same time yesterday
-   LessThanYesterday: less than the metric value at the same time yesterday
-   GreaterThanLastWeek: greater than the metric value at the same time last week
-   LessThanLastWeek: less than the metric value at the same time last week
-   GreaterThanLastPeriod: greater than the metric value in the last monitoring cycle
-   LessThanLastPeriod: less than the metric value in the last monitoring cycle |
|Escalations.Info.Threshold|String|No|90|The threshold for info-level alerts. |
|Escalations.Info.Times|Integer|No|3|The consecutive number of times for which the metric value is measured before an info-level alert is triggered. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|461CF2CD-2FC3-4B26-8645-7BD27E7D0F1D|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |
|Code|String|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Message|String|The Request is not authorization.|The error message. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=PutGroupMetricRule
&Category=ecs
&GroupId=123456
&MetricName=cpu_total
&Namespace=acs_ecs_dashboard
&RuleId=bfae2ca5b4e07d2c7278772eccda169808c7b****
&RuleName=rule1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<PutGroupMetricRuleResponse>
	  <RequestId>26C766DE-E759-4B38-8B23-28589C491CEF</RequestId>
	  <Code>200</Code>
	  <Success>true</Success>
</PutGroupMetricRuleResponse>
```

`JSON` format

```
{
    "RequestId":"26C766DE-E759-4B38-8B23-28589C491CEF",
    "Code":200,
    "Success":true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

