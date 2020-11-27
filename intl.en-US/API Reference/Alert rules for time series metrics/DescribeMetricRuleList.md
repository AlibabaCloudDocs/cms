# DescribeMetricRuleList

Queries alert rules.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeMetricRuleList&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeMetricRuleList|The operation that you want to perform. Set the value to DescribeMetricRuleList. |
|Namespace|String|No|acs\_ecs\_dashboard|The namespace of the service.

 **Note:** For more information, see [DescribeSystemEventMetaList](~~114972~~) or [Metrics](~~163515~~). |
|MetricName|String|No|cpu\_total|The name of the metric.

 **Note:** For more information, see [DescribeSystemEventMetaList](~~114972~~) or [Metrics](~~163515~~). |
|EnableState|Boolean|No|true|Specifies whether to query enabled or disabled alert rules. Valid values:

 -   true: Enabled alert rules are queried.
-   false: Disabled alert rule are queried. |
|Page|Integer|No|1|The number of the page to return. Default value: 1. |
|PageSize|Integer|No|10|The number of entries to return on each page. Default value: 10. |
|AlertState|String|No|ALARM|The status of the alert rule. Valid values:

 -   OK: Alert rules with no active alert are queried.
-   ALARM: Alert rules with active alerts are queried.
-   INSUFFICIENT\_DATA: Alert rules with no alert data are queried. |
|Dimensions|String|No|\{"instanceId":"i-2ze2d6j5uhg20x47\*\*\*\*"\}|The dimensions that specify the resources for which you want to query metric data.

 Set the value to a set of key-value pairs. A typical key-value pair is `instanceId:i-2ze2d6j5uhg20x47 ****`.

 **Note:** Dimensions must be formatted as a JSON string in a specified order. |
|RuleName|String|No|rule1|The name of the alert rule.

 **Note:** This parameter supports fuzzy match. |
|GroupId|String|No|123456|The ID of the application group. |
|RuleIds|String|No|a151cd6023eacee2f0978e03863cc1697c8950812\*\*\*\*|The ID of the alert rule.

 **Note:** You can specify up to 20 IDs at a time. Separate multiple IDs with commas \(,\). |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|0E657631-CD6C-4C24-9637-98D000B9272C|The ID of the request. |
|Code|Integer|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Total|String|21|The total number of the returned entries. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |
|Alarms|Array of Alarm| |The details of the alert rules. |
|Alarm| | | |
|AlertState|String|OK|The status of the alert rule. Valid values:

 -   OK: The alert rule has no active alert.
-   ALARM: The alert rule has at least one active alert.
-   INSUFFICIENT\_DATA: The alert rule has no data. |
|ContactGroups|String|Alice|The alert groups. |
|Dimensions|String|\[\{\}\]|The dimensions that specify the resources for which you want to query metric data.

 The value is a set of key-value pairs. A typical key-value pair is `instanceId:i-2ze2d6j5uhg20x47 ****`.

 **Note:** Dimensions must be formatted as a JSON string in a specified order. |
|EffectiveInterval|String|00:00-23:59|The time period during which the alert rule is effective. |
|EnableState|Boolean|true|Indicates whether the alert rule is enabled. Valid values:

 -   true: The alert rule is enabled.
-   false: The alert rule is disabled. |
|Escalations|Struct| |The conditions that trigger different levels of alerts. |
|Critical|Struct| |The condition that triggers critical-level alerts. |
|ComparisonOperator|String|GreaterThanOrEqualToThreshold|The comparison operator of the threshold for critical-level alerts. Valid values:

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
|PreCondition|String|$Average\>80|The additional condition that triggers critical-level alerts. The additional condition takes effect when the value of the ComparisonOperator parameter is GreaterThanYesterday, LessThanYesterday, GreaterThanLastWeek, LessThanLastWeek, GreaterThanLastPeriod, or LessThanLastPeriod.

 Assume that the values of the PreCondition, ComparisonOperator, and Threshold parameters are $Average\>80, GreaterThanYesterday, and 10. An alert is triggered only when the average metric value is greater than 80 and 10% greater than the average metric value at the same time yesterday.

 **Note:** $Average is a placeholder that consists of `a dollar sign ($) and the statistical aggregation method`. Cloud Monitor replaces the placeholder with the aggregated value or original value before value comparison. |
|Statistics|String|Average|The statistical aggregation method for critical-level alerts. |
|Threshold|String|90|The threshold for critical-level alerts. |
|Times|Integer|3|The consecutive number of times for which the metric value is measured before a critical-level alert is triggered. |
|Info|Struct| |The condition that triggers info-level alerts. |
|ComparisonOperator|String|GreaterThanOrEqualToThreshold|The comparison operator of the threshold for info-level alerts. Valid values:

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
|PreCondition|String|$Average\>80|The additional condition that triggers info-level alerts. The additional condition takes effect when the value of the ComparisonOperator parameter is GreaterThanYesterday, LessThanYesterday, GreaterThanLastWeek, LessThanLastWeek, GreaterThanLastPeriod, or LessThanLastPeriod.

 Assume that the values of the PreCondition, ComparisonOperator, and Threshold parameters are $Average\>80, GreaterThanYesterday, and 10. An alert is triggered only when the average metric value is greater than 80 and 10% greater than the average metric value at the same time yesterday.

 **Note:** $Average is a placeholder that consists of `a dollar sign ($) and the statistical aggregation method`. Cloud Monitor replaces the placeholder with the aggregated value or original value before value comparison. |
|Statistics|String|Average|The statistical aggregation method for info-level alerts. |
|Threshold|String|90|The threshold for info-level alerts. |
|Times|Integer|1|The consecutive number of times for which the metric value is measured before an info-level alert is triggered. |
|Warn|Struct| |The condition that triggers warn-level alerts. |
|ComparisonOperator|String|GreaterThanOrEqualToThreshold|The comparison operator of the threshold for warn-level alerts. Valid values:

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
|PreCondition|String|$Average\>80|The additional condition that triggers warn-level alerts. The additional condition takes effect when the value of the ComparisonOperator parameter is GreaterThanYesterday, LessThanYesterday, GreaterThanLastWeek, LessThanLastWeek, GreaterThanLastPeriod, or LessThanLastPeriod.

 Assume that the values of the PreCondition, ComparisonOperator, and Threshold parameters are $Average\>80, GreaterThanYesterday, and 10. An alert is triggered only when the average metric value is greater than 80 and 10% greater than the average metric value at the same time yesterday.

 **Note:** $Average is a placeholder that consists of `a dollar sign ($) and the statistical aggregation method`. Cloud Monitor replaces the placeholder with the aggregated value or original value before value comparison. |
|Statistics|String|Average|The statistical aggregation method for warn-level alerts. |
|Threshold|String|90|The threshold for warn-level alerts. |
|Times|Integer|3|The consecutive number of times for which the metric value is measured before a warn-level alert is triggered. |
|GroupId|String|123456|The ID of the application group. |
|GroupName|String|ECS\_Group|The name of the application group.

 **Note:** If the alert rule is associated with an application group, the name of the application group is returned in this parameter. |
|MailSubject|String|ECS\_Bucket|The subject of the alert notification email. |
|MetricName|String|cpu\_total|The name of the metric. |
|Namespace|String|acs\_ecs\_dashboard|The namespace of the service.

 **Note:** For more information, see [Metrics](~~163515~~). |
|NoEffectiveInterval|String|00:00-23:59|The time period during which the alert rule is ineffective. |
|Period|String|60|The statistical period. |
|Resources|String|\[\{\\"instanceId\\":\\"i-a2d5q7pm3f9yr29e\*\*\*\*\\"\},\{\\"instanceId\\":\\"i-a2d5q7pm3f9yr29e\*\*\*\*\\"\}|The resources that are associated with the alert rule. |
|RuleId|String|a151cd6023eacee2f0978e03863cc1697c895012\*\*\*\*|The ID of the alert rule. |
|RuleName|String|ECS\_CPU|The name of the alert rule. |
|SilenceTime|Integer|86400|The mute period during which new alerts are not sent even if the trigger conditions are met. Unit: seconds. Default value: 86400. Minimum value: 3600.

 Only one alert is reported during each mute period even if the metric value consecutively exceeds the alert rule threshold several times. |
|SourceType|String|METRIC|The type of the alert rule. Valid value: METRIC. This value indicates an alert rule for time series metrics. |
|Webhook|String|http://www.aliyun.com|The callback URL. |
|Message|String|The Request is not authorization.|The error message. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeMetricRuleList
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeMetricRuleListResponse>
		  <RequestId>0E657631-CD6C-4C24-9637-98D000B9272C</RequestId>
		  <Total>21</Total>
		  <Alarms>
			    <Alarm>
				      <GroupName>ECS_Group</GroupName>
				      <NoEffectiveInterval>00:00-23:59</NoEffectiveInterval>
				      <SilenceTime>86400</SilenceTime>
				      <ContactGroups>Alice</ContactGroups>
				      <MailSubject>ECS_Bucket</MailSubject>
				      <RuleId>a151cd6023eacee2f0978e03863cc1697c895012****</RuleId>
				      <SourceType>METRIC</SourceType>
				      <Period>60</Period>
				      <Dimensions>[{}]</Dimensions>
				      <EffectiveInterval>00:00-23:59</EffectiveInterval>
				      <Namespace>acs_ecs_dashboard</Namespace>
				      <AlertState>OK</AlertState>
				      <GroupId>123456</GroupId>
				      <MetricName>cpu_total</MetricName>
				      <EnableState>true</EnableState>
				      <Webhook>http://www.aliyun.com</Webhook>
				      <Resources>[{\\\"instanceId\\\":\\\"i-a2d5q7pm3f9yr29e****\\\"},{\\\"instanceId\\\":\\\"i-a2d5q7pm3f9yr29e****\\\"}</Resources>
				      <RuleName>ECS_CPU</RuleName>
			    </Alarm>
			    <Alarm>
				      <Escalations>
					        <Critical>
						          <ComparisonOperator>GreaterThanOrEqualToThreshold</ComparisonOperator>
						          <Times>3</Times>
						          <Statistics>Average</Statistics>
						          <Threshold>90</Threshold>
					        </Critical>
					        <Info>
						          <ComparisonOperator>GreaterThanOrEqualToThreshold</ComparisonOperator>
						          <Times>3</Times>
						          <Statistics>Average</Statistics>
						          <Threshold>90</Threshold>
					        </Info>
					        <Warn>
						          <ComparisonOperator>GreaterThanOrEqualToThreshold</ComparisonOperator>
						          <Times>3</Times>
						          <Statistics>Average</Statistics>
						          <Threshold>90</Threshold>
					        </Warn>
				      </Escalations>
			    </Alarm>
		  </Alarms>
		  <Code>200</Code>
		  <Success>true</Success>
</DescribeMetricRuleListResponse>
```

`JSON` format

```
{
    "RequestId":"0E657631-CD6C-4C24-9637-98D000B9272C",
    "Total":"21",
    "Alarms":{
        "Alarm":[
            {
                "GroupName":"ECS_Group",
                "NoEffectiveInterval":"00:00-23:59",
                "SilenceTime":"86400",
                "ContactGroups":"Alice",
                "MailSubject":"ECS_Bucket",
                "RuleId":"a151cd6023eacee2f0978e03863cc1697c895012****",
                "SourceType":"METRIC",
                "Period":"60",
                "Dimensions":"[{}]",
                "EffectiveInterval":"00:00-23:59",
                "Namespace":"acs_ecs_dashboard",
                "AlertState":"OK",
                "GroupId":"123456",
                "MetricName":"cpu_total",
                "EnableState":"true",
                "Webhook":"http://www.aliyun.com",
                "Resources":"[{\\\"instanceId\\\":\\\"i-a2d5q7pm3f9yr29e****\\\"},{\\\"instanceId\\\":\\\"i-a2d5q7pm3f9yr29e****\\\"}",
                "RuleName":"ECS_CPU"
            },
            {
                "Escalations":{
                    "Critical":{
                        "ComparisonOperator":"GreaterThanOrEqualToThreshold",
                        "Times":"3",
                        "Statistics":"Average",
                        "Threshold":"90"
                    },
                    "Info":{
                        "ComparisonOperator":"GreaterThanOrEqualToThreshold",
                        "Times":"3",
                        "Statistics":"Average",
                        "Threshold":"90"
                    },
                    "Warn":{
                        "ComparisonOperator":"GreaterThanOrEqualToThreshold",
                        "Times":"3",
                        "Statistics":"Average",
                        "Threshold":"90"
                    }
                }
            }]
    },
    "Code":"200",
    "Success":"true"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

