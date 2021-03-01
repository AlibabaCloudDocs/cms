# DescribeActiveMetricRuleList

Queries details about one-click alert rules.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeActiveMetricRuleList&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeActiveMetricRuleList|The operation that you want to perform. Set the value to DescribeActiveMetricRuleList. |
|Product|String|Yes|ecs|The abbreviation of the service name. The following services support one-click alert:

-   ecs: Elastic Compute Service \(ECS\)
-   rds: ApsaraDB for RDS
-   slb: Server Load Balancer \(SLB\)
-   redis\_standard: ApsaraDB for Redis of the standard architecture
-   redis\_sharding: ApsaraDB for Redis of the cluster architecture
-   redis\_splitrw: ApsaraDB for Redis of the read/write splitting architecture
-   mongodb: ApsaraDB for MongoDB of the replica set architecture
-   mongodb\_sharding: ApsaraDB for MongoDB of the sharded cluster architecture
-   hbase: ApsaraDB for HBase
-   elasticsearch: Elasticsearch
-   opensearch: Open Search |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|AlertList|Array of Alert|N/A|The details of the alert rules. |
|Alert|N/A|N/A|N/A|
|AlertState|String|OK|The status of the alert rule. Valid values:

-   OK: The alert rule has no active alert.
-   ALARM: The alert rule has at least one active alert.
-   INSUFFICIENT\_DATA: The alert rule has no data. |
|ContactGroups|String|ECS\_Group|The alert group that receives alert notifications. |
|Dimensions|String|""|The dimensions that specify the resources for which you want to query monitoring data.

The value is a collection of key-value pairs. A typical key-value pair is `instanceId:XXXXXX`.

The key and value must be 1 to 64 bytes in length, respectively. Excessive bytes are truncated from the string.

The key and value can contain letters, digits, periods \(.\), hyphens \(-\), underscores \(\_\), forward slashes \(/\), and backslashes \(\\\).

**Note:** Dimensions must be organized in a JSON string and follow the required order. |
|EffectiveInterval|String|00:00-23:59|The time period during which the alert rule is effective. |
|EnableState|Boolean|true|Indicates whether the alert rule is enabled. Valid values:

-   true: The alert rule is enabled.
-   false: The alert rule is disabled. |
|Escalations|Struct|N/A|The conditions for triggering different levels of alerts. |
|Critical|Struct|N/A|The condition for triggering critical-level alerts. |
|ComparisonOperator|String|GreaterThanThreshold|The comparison operator of the threshold for critical-level alerts. Valid values:

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
|Statistics|String|Average|The statistical aggregation method for critical-level alerts. |
|Threshold|String|99|The threshold for critical-level alerts. |
|Times|String|3|The consecutive number of times for which the metric value is measured before a critical-level alert is triggered. |
|Info|Struct|N/A|The condition for triggering info-level alerts. |
|ComparisonOperator|String|GreaterThanThreshold|The comparison operator of the threshold for info-level alerts. Valid values:

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
|Statistics|String|Average|The statistical aggregation method for info-level alerts. |
|Threshold|String|95|The threshold for info-level alerts. |
|Times|String|3|The consecutive number of times for which the metric value is measured before an info-level alert is triggered. |
|Warn|Struct|N/A|The condition for triggering warn-level alerts. |
|ComparisonOperator|String|GreaterThanThreshold|The comparison operator of the threshold for critical-level alerts. Valid values:

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
|Statistics|String|Average|The statistical aggregation method for warn-level alerts. |
|Threshold|String|80|The threshold of warn-level alerts. |
|Times|String|3|The consecutive number of times for which the metric value is measured before a warn-level alert is triggered. |
|MailSubject|String|ECS\_Bucket|The subject of the alert notification email. |
|MetricName|String|cpu\_total|The name of the metric. |
|Namespace|String|acs\_ecs\_dashboard|The namespace of the service. For more information, see [Appendix 1: Metrics](~~163515~~). |
|NoEffectiveInterval|String|00:00-06:00|The time period during which the alert rule is ineffective. |
|Period|String|60|The aggregation period of the monitoring data. Unit: seconds. The default value is the minimum aggregation period, indicating that the metric is polled at the highest frequency. Typically, you do not need to specify the minimum aggregation period. |
|Resources|String|\[\{"resource":"\_ALL"\}\]|The resources that are associated with the alert rule. A one-click alert rule is associated with all resources. The return value is fixed. |
|RuleId|String|ruleIdxxxx|The ID of the alert rule. |
|RuleName|String|myAlert|The name of the alert rule. |
|SilenceTime|String|86400|The mute period during which new alerts are not sent even if the trigger conditions are met. Unit: seconds. Default value: 86400. |
|Webhook|String|http://www.aliyun.com|The callback URL. |
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Datapoints|Array of Alarm|N/A|The details of the alert rules. |
|Alarm|N/A|N/A|N/A|
|ComparisonOperator|String|\>|The comparison operator that is used in the alert rule. Valid values:

-   `>`
-   `<`
-   `>=`
-   `<=`
-   `=`
-   `=` |
|ContactGroups|String|ECS\_Group|The alert group that receives alert notifications. |
|Enable|String|true|Indicates whether the alert rule is enabled. Valid values:

-   true: The alert rule is enabled.
-   false: The alert rule is disabled. |
|EndTime|String|24|The beginning of the time period during which the alert rule is effective. Unit: hours. For example, the value 23 indicates `23:59:59`. |
|EvaluationCount|String|3|The consecutive number of times for which the metric value is measured before an alert is triggered. |
|MetricName|String|cpu\_total|The name of the metric. |
|Namespace|String|acs\_ecs\_dashboard|The namespace of the service. For more information, see [Appendix 1: Metrics](~~163515~~). |
|Period|String|60|The aggregation period of the monitoring data. Unit: seconds. The default value is the minimum aggregation period, indicating that the metric is polled at the highest frequency. Typically, you do not need to specify the minimum aggregation period. |
|RuleId|String|a151cd6023eacee2f0978e03863cc1697c89508\*\*\*\*|The ID of the alert rule. |
|RuleName|String|SystemDefault\_acs\_rds\_dashboard\_CpuUsage|The name of the alert rule. |
|SilenceTime|String|86400|The mute period during which new alerts are not sent even if the trigger conditions are met. Unit: seconds. Default value: 86400. |
|StartTime|String|00|The end of the time period during which the alert rule is effective. Unit: hours. For example, the value 00 indicates `00:00:00`. |
|State|String|Enable|Indicates whether the alert rule is enabled. |
|Statistics|String|Average|The statistical aggregation method. |
|Threshold|String|90|The threshold of the metric value. |
|Webhook|String|http://www.aliyun.com|The callback URL. |
|Message|String|The Request is not authorization.|The returned message. |
|RequestId|String|F82E6667-7811-4BA0-842F-5B2DC42BBAAD|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DescribeActiveMetricRuleList
&Product=ecs
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeActiveMetricRuleListResponse>
          <AlertList>
                <Alert>
                      <SilenceTime>86400</SilenceTime>
                      <ContactGroups>ECS_Group</ContactGroups>
                      <NoEffectiveInterval></NoEffectiveInterval>
                      <MailSubject>${serviceType}-${metricName}-${levelDescription}</MailSubject>
                      <RuleId>SystemDefault_acs_rds_dashboard_IOPSUsage</RuleId>
                      <Period>300</Period>
                      <Dimensions></Dimensions>
                      <EffectiveInterval></EffectiveInterval>
                      <Namespace>acs_rds_dashboard</Namespace>
                      <AlertState>INSUFFICIENT_DATA</AlertState>
                      <MetricName>IOPSUsage</MetricName>
                      <EnableState>true</EnableState>
                      <Escalations>
                            <Critical></Critical>
                            <Info>
                                  <ComparisonOperator>GreaterThanThreshold</ComparisonOperator>
                                  <Times>5</Times>
                                  <Statistics>Average</Statistics>
                                  <Threshold>80</Threshold>
                            </Info>
                            <Warn></Warn>
                      </Escalations>
                      <Webhook></Webhook>
                      <Resources>[{\"resource\":\"_ALL\"}]</Resources>
                      <RuleName>SystemDefault_acs_rds_dashboard_IOPSUsage</RuleName>
                </Alert>
                <Alert>
                      <SilenceTime>86400</SilenceTime>
                      <ContactGroups>ECS_Group</ContactGroups>
                      <NoEffectiveInterval></NoEffectiveInterval>
                      <MailSubject>${serviceType}-${metricName}-${levelDescription}</MailSubject>
                      <RuleId>SystemDefault_acs_rds_dashboard_CpuUsage</RuleId>
                      <Period>300</Period>
                      <Dimensions></Dimensions>
                      <EffectiveInterval></EffectiveInterval>
                      <Namespace>acs_rds_dashboard</Namespace>
                      <AlertState>INSUFFICIENT_DATA</AlertState>
                      <MetricName>CpuUsage</MetricName>
                      <EnableState>true</EnableState>
                      <Escalations>
                            <Critical></Critical>
                            <Info>
                                  <ComparisonOperator>GreaterThanThreshold</ComparisonOperator>
                                  <Times>5</Times>
                                  <Statistics>Average</Statistics>
                                  <Threshold>80</Threshold>
                            </Info>
                            <Warn></Warn>
                      </Escalations>
                      <Webhook></Webhook>
                      <Resources>[{\"resource\":\"_ALL\"}]</Resources>
                      <RuleName>SystemDefault_acs_rds_dashboard_CpuUsage</RuleName>
                </Alert>
          </AlertList>
          <Datapoints>
                <Alarm>
                      <SilenceTime>86400</SilenceTime>
                      <ContactGroups>[\"Alice\"]</ContactGroups>
                      <ComparisonOperator>GreaterThanThreshold</ComparisonOperator>
                      <EndTime></EndTime>
                      <RuleId>SystemDefault_acs_rds_dashboard_IOPSUsage</RuleId>
                      <StartTime></StartTime>
                      <Period>300</Period>
                      <EvaluationCount>5</EvaluationCount>
                      <Statistics>Average</Statistics>
                      <Namespace>acs_rds_dashboard</Namespace>
                      <MetricName>IOPSUsage</MetricName>
                      <State>INSUFFICIENT_DATA</State>
                      <Enable>true</Enable>
                      <Webhook></Webhook>
                      <RuleName>SystemDefault_acs_rds_dashboard_IOPSUsage</RuleName>
                      <Threshold>80</Threshold>
                </Alarm>
                <Alarm>
                      <SilenceTime>86400</SilenceTime>
                      <ContactGroups>[\"Jim\"]</ContactGroups>
                      <ComparisonOperator>GreaterThanThreshold</ComparisonOperator>
                      <EndTime></EndTime>
                      <RuleId>SystemDefault_acs_rds_dashboard_CpuUsage</RuleId>
                      <StartTime></StartTime>
                      <Period>300</Period>
                      <EvaluationCount>5</EvaluationCount>
                      <Statistics>Average</Statistics>
                      <Namespace>acs_rds_dashboard</Namespace>
                      <MetricName>CpuUsage</MetricName>
                      <State>INSUFFICIENT_DATA</State>
                      <Enable>true</Enable>
                      <Webhook></Webhook>
                      <RuleName>SystemDefault_acs_rds_dashboard_CpuUsage</RuleName>
                      <Threshold>80</Threshold>
                </Alarm>
          </Datapoints>
          <Code>200</Code>
          <Success>true</Success>
</DescribeActiveMetricRuleListResponse>
```

`JSON` format

```
{
    "AlertList": {
        "Alert": [
            {
                "SilenceTime": 86400,
                "ContactGroups": "ECS_Group",
                "NoEffectiveInterval": "",
                "MailSubject": "${serviceType}-${metricName}-${levelDescription}",
                "RuleId": "SystemDefault_acs_rds_dashboard_IOPSUsage",
                "Period": 300,
                "Dimensions": "",
                "EffectiveInterval": "",
                "Namespace": "acs_rds_dashboard",
                "AlertState": "INSUFFICIENT_DATA",
                "MetricName": "IOPSUsage",
                "EnableState": true,
                "Escalations": {
                    "Critical": {},
                    "Info": {
                        "ComparisonOperator": "GreaterThanThreshold",
                        "Times": 5,
                        "Statistics": "Average",
                        "Threshold": "80"
                    },
                    "Warn": {}
                },
                "Webhook": "",
                "Resources": "[{\"resource\":\"_ALL\"}]",
                "RuleName": "SystemDefault_acs_rds_dashboard_IOPSUsage"
            },
            {
                "SilenceTime": 86400,
                "ContactGroups": "ECS_Group",
                "NoEffectiveInterval": "",
                "MailSubject": "${serviceType}-${metricName}-${levelDescription}",
                "RuleId": "SystemDefault_acs_rds_dashboard_CpuUsage",
                "Period": 300,
                "Dimensions": "",
                "EffectiveInterval": "",
                "Namespace": "acs_rds_dashboard",
                "AlertState": "INSUFFICIENT_DATA",
                "MetricName": "CpuUsage",
                "EnableState": true,
                "Escalations": {
                    "Critical": {},
                    "Info": {
                        "ComparisonOperator": "GreaterThanThreshold",
                        "Times": 5,
                        "Statistics": "Average",
                        "Threshold": "80"
                    },
                    "Warn": {}
                },
                "Webhook": "",
                "Resources": "[{\"resource\":\"_ALL\"}]",
                "RuleName": "SystemDefault_acs_rds_dashboard_CpuUsage"
            } 
        ]
    },
    "Datapoints": {
        "Alarm": [
            {
                "SilenceTime": 86400,
                "ContactGroups": "[\"Alice\"]",
                "ComparisonOperator": "GreaterThanThreshold",
                "EndTime": "",
                "RuleId": "SystemDefault_acs_rds_dashboard_IOPSUsage",
                "StartTime": "",
                "Period": 300,
                "EvaluationCount": 5,
                "Statistics": "Average",
                "Namespace": "acs_rds_dashboard",
                "MetricName": "IOPSUsage",
                "State": "INSUFFICIENT_DATA",
                "Enable": true,
                "Webhook": "",
                "RuleName": "SystemDefault_acs_rds_dashboard_IOPSUsage",
                "Threshold": "80"
            },
            {
                "SilenceTime": 86400,
                "ContactGroups": "[\"Jim\"]",
                "ComparisonOperator": "GreaterThanThreshold",
                "EndTime": "",
                "RuleId": "SystemDefault_acs_rds_dashboard_CpuUsage",
                "StartTime": "",
                "Period": 300,
                "EvaluationCount": 5,
                "Statistics": "Average",
                "Namespace": "acs_rds_dashboard",
                "MetricName": "CpuUsage",
                "State": "INSUFFICIENT_DATA",
                "Enable": true,
                "Webhook": "",
                "RuleName": "SystemDefault_acs_rds_dashboard_CpuUsage",
                "Threshold": "80"
            } 
        ]
    },
    "Code": "200",
    "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

