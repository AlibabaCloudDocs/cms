# PutCustomEventRule

Creates an alert rule for a custom event.

Before you call this operation, call the PutCustomEvent operation to report the monitoring data of the custom event. For more information, see [PutCustomEvent](~~115012~~).

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=PutCustomEventRule&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|PutCustomEventRule|The operation that you want to perform. Set the value to PutCustomEventRule. |
|ContactGroups|String|Yes|ECS\_Group|The alert contact group that receives alert notifications. Separate multiple contact groups with commas \(,\). |
|EventName|String|Yes|HostDown|The name of the custom event. For more information about how to obtain the event name, see [DescribeCustomEventAttribute](~~115262~~). |
|GroupId|String|Yes|7378\*\*\*\*|The ID of the application group. For more information about how to obtain the group ID, see [DescribeCustomEventAttribute](~~115262~~).

 **Note:** The value 0 indicates that the reported custom event does not belong to any application Group. |
|Level|String|Yes|CRITICAL|The level of the alert. Valid values:

 -   CRITICAL: critical issue
-   WARN: warning
-   INFO: information |
|RuleId|String|Yes|CustomRuleId1|The ID of the alert rule.

 **Note:** You can specify an existing ID to modify the corresponding alert rule or specify a new ID to create an alert rule. |
|RuleName|String|Yes|CustomeRule|The name of the alert rule. |
|Threshold|String|Yes|99|The alert threshold. |
|Webhook|String|No|https://www.aliyun.com|The callback URL to which a POST request is sent when an alert is triggered based on the alert rule. |
|EffectiveInterval|String|No|00:00-23:59|The time period during which the alert rule is effective. Valid values: 00:00 to 23:59. |
|Period|String|No|60|The cycle that is used to aggregate monitoring data of the custom event. Unit: seconds. Set the value to an integral multiple of 60. Default value: 300. |
|EmailSubject|String|No|ECS instance|The subject of the alert notification email. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

 **Note:** The value 200 indicates that the call was successful. |
|Message|String|The request has failed due to a temporary failure of the server.|The error message. |
|RequestId|String|AD5DCD82-BD1C-405F-BAED-32302DE9F498|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |

## Examples

Sample request

```
http(s)://[Endpoint]/? Action=PutCustomEventRule
&ContactGroups=ECS_Group
&EventName=HostDown
&GroupId=7378****
&Level=CRITICAL
&RuleId=CustomRuleId1
&RuleName=CustomeRule
&Threshold=99
&<Common request parameters>
```

Sample success responses

`XML` format

```
<PutCustomEventRuleResponse>
	  <RequestId>AD5DCD82-BD1C-405F-BAED-32302DE9F498</RequestId>
	  <Code>200</Code>
	  <Success>true</Success>
</PutCustomEventRuleResponse>
```

`JSON` format

```
{
	"RequestId": "AD5DCD82-BD1C-405F-BAED-32302DE9F498",
	"Code": "200",
	"Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

