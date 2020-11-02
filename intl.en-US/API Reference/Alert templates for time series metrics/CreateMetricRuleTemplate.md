# CreateMetricRuleTemplate

Creates an alert template.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=CreateMetricRuleTemplate&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CreateMetricRuleTemplate|The operation that you want to perform. Set the value to CreateMetricRuleTemplate. |
|Name|String|Yes|Template1|The name of the alert template. |
|AlertTemplates.N.MetricName|String|Yes|cpu\_total|The name of the metric. Valid values of N: 1 to 200.

**Note:** For more information, see [DescribeMetricMetaList](~~98846~~) or [Appendix 1: Metrics](~~28619~~). |
|AlertTemplates.N.RuleName|String|Yes|My CPU monitoring|The name of the alert rule. Valid values of N: 1 to 200. |
|AlertTemplates.N.Category|String|Yes|ecs|The abbreviation of the service name. Valid values of N: 1 to 200. Valid values of the AlertTemplates.N.Category parameter:

-   ecs: Elastic Compute Service \(ECS\) instances that are provided by Alibaba Cloud and hosts that are not provided by Alibaba Cloud
-   rds: ApsaraDB RDS
-   ads: AnalyticDB
-   slb: Server Load Balancer \(SLB\)
-   vpc: Virtual Private Cloud \(VPC\)
-   apigateway: API Gateway
-   cdn: Alibaba Cloud CDN
-   cs: Container Service for Swarm
-   dcdn: Dynamic Route for CDN \(DCDN\)
-   ddos: Anti-DDoS
-   eip: Elastic IP Address \(EIP\)
-   elasticsearch: Elasticsearch
-   emr: E-MapReduce
-   ess: Auto Scaling
-   hbase: ApsaraDB for HBase
-   iot\_edge: IoT Edge
-   k8s\_pod: pods in Container Service for Kubernetes
-   kvstore\_sharding: ApsaraDB for Redis of the cluster master-replica architecture
-   kvstore\_splitrw: ApsaraDB for Redis of the read/write splitting architecture
-   kvstore\_standard: ApsaraDB for Redis of the standard master-replica architecture
-   memcache: ApsaraDB for Memcache
-   mns: Message Service \(MNS\)
-   mongodb: ApsaraDB for MongoDB of the replica set architecture
-   mongodb\_cluster: ApsaraDB for MongoDB of the standalone architecture
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
|AlertTemplates.N.Namespace|String|Yes|acs\_ecs\_dashboard|The namespace of the service. Valid values of N: 1 to 200.

**Note:** For more information, see [DescribeMetricMetaList](~~98846~~) or [Appendix 1: Metrics](~~28619~~). |
|Description|String|No|ECS\_Template1|The description of the alert template. |
|AlertTemplates.N.Period|Integer|No|60|The aggregation period of the monitoring data. Unit: seconds.

The default value is the minimum aggregation period. Typically, you do not need to specify the minimum aggregation period.

Valid values of N: 1 to 200. |
|AlertTemplates.N.Selector|String|No|\{"disk":"/"\}|The dimension of the alert. It is an extended field. Valid values of N: 1 to 200. |
|AlertTemplates.N.Escalations.Critical.Statistics|String|No|Average|The statistical aggregation method for critical-level alerts. Valid values of N: 1 to 200. |
|AlertTemplates.N.Escalations.Critical.ComparisonOperator|String|No|GreaterThanOrEqualToThreshold|The comparison operator of the threshold for critical-level alerts. Valid values of N: 1 to 200. Valid values of the AlertTemplates.N.Escalations.Critical.ComparisonOperator parameter:

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
|AlertTemplates.N.Escalations.Warn.Statistics|String|No|Average|The statistical aggregation method for warn-level alerts. Valid values of N: 1 to 200. |
|AlertTemplates.N.Escalations.Warn.ComparisonOperator|String|No|GreaterThanOrEqualToThreshold|The comparison operator of the threshold for warn-level alerts. Valid values of N: 1 to 200. Valid values of the AlertTemplates.N.Escalations.Warn.ComparisonOperator parameter:

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
|AlertTemplates.N.Escalations.Info.Statistics|String|No|Average|The statistical aggregation method for info-level alerts. Valid values of N: 1 to 200. |
|AlertTemplates.N.Escalations.Info.ComparisonOperator|String|No|GreaterThanOrEqualToThreshold|The comparison operator of the threshold for info-level alerts. Valid values of N: 1 to 200. Valid values of the AlertTemplates.N.Escalations.Info.ComparisonOperator parameter:

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
|AlertTemplates.N.Webhook|String|No|http://ww.aliyun.com|The callback URL to which a POST request is sent when an alert is triggered based on the alert rule. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|9763ED1A-4D09-41BF-851E-310421750204|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |
|Code|Integer|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Id|Long|12345|The ID of the alert template. |
|Message|String|The Request is not authorization.|The returned message. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=CreateMetricRuleTemplate
&Name=Template1
&AlertTemplates.1.MetricName=cpu_total
&AlertTemplates.1.RuleName=My CPU monitoring
&AlertTemplates.1.Category=ecs
&AlertTemplates.1.1amespace=acs_ecs_dashboard
&<Common request parameters>
```

Sample success responses

`XML` format

```
<CreateMetricRuleTemplateResponse>
          <RequestId>9763ED1A-4D09-41BF-851E-310421750204</RequestId>
          <Id>12345</Id>
          <Success>true</Success>
          <Code>200</Code>
</CreateMetricRuleTemplateResponse>
```

`JSON` format

```
{
    "RequestId": "9763ED1A-4D09-41BF-851E-310421750204",
    "Id": 12345,
    "Success": true,
    "Code": 200
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

