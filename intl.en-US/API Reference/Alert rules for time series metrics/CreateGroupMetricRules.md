# CreateGroupMetricRules

Creates multiple alert rules for an application group at a time.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=CreateGroupMetricRules&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CreateGroupMetricRules|The operation that you want to perform. Set the value to CreateGroupMetricRules. |
|GroupId|Long|Yes|123456|The ID of the application group. |
|GroupMetricRules.N.Category|String|Yes|ecs|The name of the cloud service. Valid values of N: 1 to 200. Valid values:

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
-   emr: E-MapReduce \(EMR\)
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
|GroupMetricRules.N.MetricName|String|Yes|cpu\_total|The name of the metric. Valid values of N: 1 to 200.

 **Note:** For more information, see [DescribeMetricMetaList](~~98846~~) or [Metrics](~~163515~~). |
|GroupMetricRules.N.Namespace|String|Yes|acs\_ecs\_dashboard|The namespace of the service. Valid values of N: 1 to 200.

 **Note:** For more information, see [DescribeMetricMetaList](~~98846~~) or [Metrics](~~163515~~). |
|GroupMetricRules.N.RuleId|String|Yes|bfae2ca5b4e07d2c7278772eccda169808c7b\*\*\*\*|The ID of the alert rule. Valid values of N: 1 to 200. |
|GroupMetricRules.N.RuleName|String|Yes|ECS\_Rule1|The name of the alert rule. Valid values of N: 1 to 200. |
|GroupMetricRules.N.Dimensions|String|No|\[\{"instanceId":"i-m5e1qg6uo38rztr4\*\*\*\*"\}\]|The expanded resource dimensions. Valid values of N: 1 to 200.

 **Note:** This API operation associates all instances in the application group with the alert rule. You can set this parameter to associate the resources of the instance with the alert rule. For example, if you need to associate the root partitions of all instances in the application group with the alert rule, set this parameter to `[ {"dskName":"/"} ]`. |
|GroupMetricRules.N.EffectiveInterval|String|No|00:00-23:59|The time period during which the alert rule is effective. Valid values of N: 1 to 200. |
|GroupMetricRules.N.NoEffectiveInterval|String|No|00:00-05:30|The time period during which the alert rule is ineffective. Valid values of N: 1 to 200. |
|GroupMetricRules.N.SilenceTime|Integer|No|86400|The mute period during which new alerts are not sent even if the trigger conditions are met. Unit: seconds. Minimum value: 3600. Default value: 86400.

 Valid values of N: 1 to 200. |
|GroupMetricRules.N.Period|String|No|60|The aggregation period of the metric data. The value is an integral multiple of 60. Unit: seconds. Default value: 300.

 Valid values of N: 1 to 200.

 **Note:** If you set this parameter to 300 seconds, the average of the 5-minute metric data is used to determine whether to trigger an alert. |
|GroupMetricRules.N.Interval|String|No|60|The interval at which Cloud Monitor checks whether the alert rule is triggered. The default value is the lowest frequency at which the metric is polled. Unit: seconds.

 Valid values of N: 1 to 200.

 **Note:** We recommend that you set this interval to the data aggregation period. If this interval is shorter than the data aggregation period, alerts cannot be triggered due to insufficient data. |
|GroupMetricRules.N.Webhook|String|No|https://www.aliyun.com|The callback URL. Valid values of N: 1 to 200. |
|GroupMetricRules.N.EmailSubject|String|No|ECS\_Instance1|The subject of the alert notification email. Valid values of N: 1 to 200. |
|GroupMetricRules.N.Escalations.Critical.Statistics|String|No|Average|The statistical aggregation method for critical-level alerts. Valid values of N: 1 to 200.

 **Note:** For more information, see [DescribeSystemEventMetaList](~~114972~~). |
|GroupMetricRules.N.Escalations.Critical.ComparisonOperator|String|No|GreaterThanOrEqualToThreshold|The comparison operator of the threshold for critical-level alerts. Valid values of N: 1 to 200. Valid values:

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
|GroupMetricRules.N.Escalations.Critical.Threshold|String|No|90|The threshold for critical-level alerts. Valid values of N: 1 to 200. |
|GroupMetricRules.N.Escalations.Critical.Times|Integer|No|3|The consecutive number of times for which the metric value is measured before a critical-level alert is triggered. Valid values of N: 1 to 200. |
|GroupMetricRules.N.Escalations.Warn.Statistics|String|No|Average|The statistical aggregation method for warn-level alerts. Valid values of N: 1 to 200.

 **Note:** For more information, see [DescribeSystemEventMetaList](~~114972~~). |
|GroupMetricRules.N.Escalations.Warn.ComparisonOperator|String|No|GreaterThanOrEqualToThreshold|The comparison operator of the threshold for warn-level alerts. Valid values of N: 1 to 200. Valid values:

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
|GroupMetricRules.N.Escalations.Warn.Threshold|String|No|90|The threshold for warn-level alerts. Valid values of N: 1 to 200. |
|GroupMetricRules.N.Escalations.Warn.Times|Integer|No|3|The consecutive number of times for which the metric value is measured before a warn-level alert is triggered. Valid values of N: 1 to 200. |
|GroupMetricRules.N.Escalations.Info.Statistics|String|No|Average|The statistical aggregation method for info-level alerts. Valid values of N: 1 to 200.

 **Note:** For more information, see [DescribeSystemEventMetaList](~~114972~~). |
|GroupMetricRules.N.Escalations.Info.ComparisonOperator|String|No|GreaterThanOrEqualToThreshold|The comparison operator of the threshold for info-level alerts. Valid values of N: 1 to 200. Valid values:

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
|GroupMetricRules.N.Escalations.Info.Threshold|String|No|90|The threshold for info-level alerts. Valid values of N: 1 to 200. |
|GroupMetricRules.N.Escalations.Info.Times|Integer|No|3|The consecutive number of times for which the metric value is measured before an info-level alert is triggered. Valid values of N: 1 to 200. |

You must specify at least one of the following three alert levels: critical, warn, and info. Otherwise, the alert rule cannot be created.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|Integer|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Message|String|The Request is not authorization.|The error message. |
|RequestId|String|461CF2CD-2FC3-4B26-8645-7BD27E7D0F1D|The ID of the request. |
|Resources|Array of AlertResult| |The results of creating the alert rules. |
|AlertResult| | | |
|Code|Integer|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Message|String|Metric not found.|The error message. |
|RuleId|String|a151cd6023eacee2f0978e03863cc1697c89508\*\*\*\*|The ID of the alert rule. |
|RuleName|String|ECS\_Rule1|The name of the alert rule. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=CreateGroupMetricRules
&GroupId=123456
&GroupMetricRules.1.Category=ecs
&GroupMetricRules.1.MetricName=cpu_total
&GroupMetricRules.1.1amespace=acs_ecs_dashboard
&GroupMetricRules.1.RuleId=bfae2ca5b4e07d2c7278772eccda169808c7b****
&GroupMetricRules.1.RuleName=ECS_Rule1
&GroupMetricRules.1.Escalations.Critical.Statistics=Average
&GroupMetricRules.1.Escalations.Critical.ComparisonOperator=GreaterThanOrEqualToThreshold
&GroupMetricRules.1.Escalations.Critical.Threshold=90
&GroupMetricRules.1.Escalations.Critical.Times=3
&<Common request parameters>
```

Sample success responses

`XML` format

```
<CreateGroupMetricRulesResponse>
	  <RequestId>65D50468-ECEF-48F1-A6E1-D952E89D9436</RequestId>
	  <Success>true</Success>
	  <Code>200</Code>
	  <Resources>
		    <AlertResult>
			      <RuleId>a151cd6023eacee2f0978e03863cc1697c89508****</RuleId>
			      <Success>true</Success>
			      <RuleName>ECS_Rule1</RuleName>
			      <Code>200</Code>
		    </AlertResult>
		    <AlertResult>
			      <Message>Metric not found. </Message>
			      <RuleId>hyu91929****</RuleId>
			      <Success>false</Success>
			      <RuleName>ECS_Rule2</RuleName>
			      <Code>404</Code>
		    </AlertResult>
	  </Resources>
</CreateGroupMetricRulesResponse>
```

`JSON` format

```
{
    "RequestId": "65D50468-ECEF-48F1-A6E1-D952E89D9436",
    "Success": "true",
    "Code": "200",
    "Resources": {
        "AlertResult": [
            {
                "RuleId": "a151cd6023eacee2f0978e03863cc1697c89508****",
                "Success": "true",
                "RuleName": "ECS_Rule1",
                "Code": "200"
            },
            {
                "Message": "Metric not found.",
                "RuleId": "hyu91929****",
                "Success": "false",
                "RuleName": "ECS_Rule2",
                "Code": "404"
            }
        ]
    }
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

