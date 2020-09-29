# ModifyMetricRuleTemplate

Modifies an alert template.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=ModifyMetricRuleTemplate&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ModifyMetricRuleTemplate|The operation that you want to perform. Set the value to ModifyMetricRuleTemplate. |
|TemplateId|Long|Yes|123456|The ID of the alert template. |
|RestVersion|Long|Yes|0|The version of the alert template to be modified.

**Note:** The version changes with the number of times that the alert template is modified. |
|Name|String|No|test123|The name of the alert template. |
|Description|String|No|ECS\_template1|The description of the alert template. |
|AlertTemplates.N.MetricName|String|No|cpu\_total|The name of the metric. Valid values of N: 1 to 200.

**Note:** You can call the [DescribeSystemEventMetaList](~~114972~~) operation to query the names of metrics. |
|AlertTemplates.N.RuleName|String|No|rule1|The name of the alert rule. Valid values of N: 1 to 200. |
|AlertTemplates.N.Category|String|No|ecs|The abbreviation of the service name. Valid values of N: 1 to 200. Valid values:

-   ecs: Elastic Compute Service \(ECS\) instances provided by Alibaba Cloud and hosts not provided by Alibaba Cloud
-   rds: ApsaraDB for RDS
-   ads: AnalyticDB
-   slb: Server Load Balancer \(SLB\)
-   vpc: Virtual Private Cloud \(VPC\)
-   apigateway: API Gateway
-   cdn: Alibaba Cloud Content Delivery Network \(CDN\)
-   cs: Container Service for Swarm
-   dcdn: Dynamic Route for CDN
-   ddos: Anti-DDoS
-   eip: Elastic IP Address \(EIP\)
-   elasticsearch: Elasticsearch
-   emr: E-MapReduce
-   ess: Auto Scaling
-   hbase: ApsaraDB for HBase
-   iot\_edge: IoT Edge
-   kvstore\_sharding: ApsaraDB for Redis of the cluster architecture
-   kvstore\_splitrw: ApsaraDB for Redis of the read/write splitting architecture
-   kvstore\_standard: ApsaraDB for Redis of the standard architecture
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
-   scdn: Secure Content Delivery Network \(SCDN\)
-   sharebandwidthpackages: EIP Bandwidth Plan
-   sls: Log Service
-   vpn: VPN Gateway |
|AlertTemplates.N.Namespace|String|No|acs\_ecs\_dashboard|The namespace of the service. Valid values of N: 1 to 200.

Specify the value in the format of acs\_Service name.

**Note:** You can call the [DescribeProjectMeta](~~114916~~) operation to query the namespace of each service. |
|AlertTemplates.N.Period|Integer|No|60|The aggregation period of the monitoring data, namely, the interval at which the alert system aggregates monitoring data. Valid values of N: 1 to 200.

**Note:** If the value is set to 300 seconds, the monitoring data is collected every 300 seconds. If the monitoring data is reported every 1 minute, the alert system calculates the average, maximum, and minimum values of the monitoring data of 5 minutes and checks whether the aggregated values exceed the threshold. We recommend that you set this parameter with other parameters to avoid unexpected alerts. |
|AlertTemplates.N.Selector|String|No|\{"disk":"/"\}|The dimension of the alert. It is an extended field. Valid values of N: 1 to 200.

Assume that an alert template is applied to an application group, this parameter is set to `{"disk":"/"}`, and the MetricName parameter is set to `DiskUtilization`. The generated alert rule is applied to the root disk partition \(`"/"`\) of all instances in the application group to which the alert template is applied.

**Note:** You can call the [DescribeSystemEventMetaList](~~114972~~) operation to query the valid values of this parameter. |
|AlertTemplates.N.Escalations.Critical.Statistics|String|No|Average|The statistical aggregation method for critical-level alerts. Valid values of N: 1 to 200.

**Note:** You can call the [DescribeSystemEventMetaList](~~114972~~) operation to query the valid values of this parameter. |
|AlertTemplates.N.Escalations.Critical.ComparisonOperator|String|No|GreaterThanOrEqualToThreshold|The comparison operator of the threshold for critical-level alerts. Valid values of N: 1 to 200. Valid values:

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
|AlertTemplates.N.Escalations.Critical.Threshold|String|No|90|The threshold for critical-level alerts. Valid values of N: 1 to 200. |
|AlertTemplates.N.Escalations.Critical.Times|Integer|No|3|The consecutive number of times for which the metric value is measured before a critical-level alert is triggered. Valid values of N: 1 to 200. |
|AlertTemplates.N.Escalations.Warn.Statistics|String|No|Average|The statistical aggregation method for warn-level alerts. Valid values of N: 1 to 200.

**Note:** You can call the [DescribeSystemEventMetaList](~~114972~~) operation to query the valid values of this parameter. |
|AlertTemplates.N.Escalations.Warn.ComparisonOperator|String|No|GreaterThanOrEqualToThreshold|The comparison operator of the threshold for warn-level alerts. Valid values of N: 1 to 200. Valid values:

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
|AlertTemplates.N.Escalations.Warn.Threshold|String|No|90|The threshold for warn-level alerts. Valid values of N: 1 to 200. |
|AlertTemplates.N.Escalations.Warn.Times|Integer|No|3|The consecutive number of times for which the metric value is measured before a warn-level alert is triggered. Valid values of N: 1 to 200. |
|AlertTemplates.N.Escalations.Info.Statistics|String|No|Average|The statistical aggregation method of the threshold for info-level alerts. Valid values of N: 1 to 200.

**Note:** You can call the [DescribeSystemEventMetaList](~~114972~~) operation to query the valid values of this parameter. |
|AlertTemplates.N.Escalations.Info.ComparisonOperator|String|No|GreaterThanOrEqualToThreshold|The comparison operator of the threshold for info-level alerts. Valid values of N: 1 to 200. Valid values:

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
|AlertTemplates.N.Escalations.Info.Threshold|String|No|90|The threshold for info-level alerts. Valid values of N: 1 to 200. |
|AlertTemplates.N.Escalations.Info.Times|Integer|No|3|The consecutive number of times for which the metric value is measured before an info-level alert is triggered. Valid values of N: 1 to 200. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|9E07117F-F6AE-4F1C-81E8-36FBB4892235|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |
|Code|Integer|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Message|String|The Request is not authorization.|The returned message. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=ModifyMetricRuleTemplate
&TemplateId=123456
&RestVersion=0
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ModifyMetricRuleTemplateResponse>
          <RequestId>97EAC0E2-CD54-4183-95AC-F0C113024E18</RequestId>
          <Code>200</Code>
          <Success>true</Success>
</ModifyMetricRuleTemplateResponse>
```

`JSON` format

```
{
    "RequestId": "5F78F035-3369-4360-810E-D5CC5E774336",
    "Code": 200,
    "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

