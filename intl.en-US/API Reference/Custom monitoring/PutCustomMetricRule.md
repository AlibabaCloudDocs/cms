# PutCustomMetricRule

Creates a custom alert rule.

Before you call this operation, call the PutCustomMetric operation to report custom monitoring data. For more information, see [PutCustomMetric](~~115004~~).

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=PutCustomMetricRule&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|PutCustomMetricRule|The operation that you want to perform. Set the value to PutCustomMetricRule. |
|ComparisonOperator|String|Yes|\>=|The comparison operator before the threshold. Valid values:

 -   `>=`
-   =
-   `<=`
-   `>`
-   `<`
-   `! =` |
|ContactGroups|String|Yes|ECS\_Group|The alert contact group that receives alert notifications. Separate multiple contact groups with commas \(,\). |
|EvaluationCount|Integer|Yes|3|The consecutive number of times for which the metric value is measured before an alert is triggered. |
|Level|String|Yes|CRITICAL|The level of the alert. Valid values:

 -   CRITICAL: critical issue
-   WARN: warning
-   INFO: information |
|MetricName|String|Yes|cpu\_total|The name of the metric.

 **Note:** For more information about how to obtain the metric name, see [DescribeCustomMetricList](~~115005~~). |
|Resources|String|Yes|\[\{"groupId":7378\*\*\*\*,"dimension":"instanceId=i-hp3543t5e4sudb3s\*\*\*\*"\}\]|The custom monitoring data to which the alert rule applies. The value includes the application group ID to which the custom monitoring data belongs and the dimension to which the metric belongs. |
|RuleId|String|Yes|MyRuleId1|The ID of the alert rule.

 **Note:** You can specify an existing ID to modify the corresponding alert rule or specify a new ID to create an alert rule. |
|Statistics|String|Yes|Average|The method used to calculate metric values that trigger alerts. |
|Threshold|String|Yes|90|The alert threshold. |
|GroupId|String|No|7378\*\*\*\*|The ID of the application group to which the custom monitoring data belongs.

 **Note:** The value 0 indicates that the reported custom monitoring data does not belong to any application group. |
|RuleName|String|No|CpuUsage|The name of the alert rule. |
|Webhook|String|No|https://www.aliyun.com|The callback URL to which a POST request is sent when an alert is triggered based on the alert rule. |
|EffectiveInterval|String|No|00:00-23:59|The time period during which the alert rule is effective. Valid values: 00:00 to 23:59. |
|SilenceTime|Integer|No|86400|The mute period during which notifications are not repeatedly sent for an alert. Unit: seconds. Default value: 86400. The default value indicates one day.

 **Note:** Only one alert notification is sent during each mute period even if the metric value consecutively exceeds the alert threshold several times. |
|Period|String|No|300|The cycle that is used to aggregate custom monitoring data. Unit: seconds. Set the value to an integral multiple of 60. The original reporting cycle of custom monitoring data is used by default. |
|EmailSubject|String|No|ECS instance|The subject of the alert notification email. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

 **Note:** The value 200 indicates that the call was successful. |
|Message|String|ComparisonOperator is mandatory for this action.|The returned message. If the call is successful, the return value is null. If the call fails, an error message is returned. |
|RequestId|String|65D50468-ECEF-48F1-A6E1-D952E89D9432|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |

## Examples

Sample request

```
http(s)://[Endpoint]/? Action=PutCustomMetricRule
&ComparisonOperator=>=
&ContactGroups=ECS_Group
&EvaluationCount=3
&Level=CRITICAL
&MetricName=cpu_total
&Resources=[{"groupId":7378****,"dimension":"instanceId=i-hp3543t5e4sudb3s****"}]
&RuleId=MyRuleId1
&Statistics=Average
&Threshold=90
&<Common request parameters>
```

Sample success responses

`XML` format

```
<PutCustomMetricRuleResponse>
	  <Message></Message>
	  <Code>200</Code>
	  <Success>true</Success>
</PutCustomMetricRuleResponse>
```

`JSON` format

```
{
	"Message": "",
	"Code": "200",
	"Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

