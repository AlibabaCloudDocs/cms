# CreateHostAvailability

Creates an availability monitoring task.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=CreateHostAvailability&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CreateHostAvailability|The operation that you want to perform. Set the value to CreateHostAvailability. |
|AlertConfig.NotifyType|Integer|Yes|2|The alert notification method.

 
 Set the value to 0. The value 0 indicates that alert notifications are sent by using emails and DingTalk chatbots. |
|AlertConfigEscalationList.N.MetricName|String|Yes|HttpStatus|The metric for which the alert feature is enabled. Valid values of N: 1 to 21. Valid values of the AlertConfigEscalationList.N.MetricName parameter:

 -   HttpStatus: HTTP status code
-   HttpLatency: HTTP response time
-   TelnetStatus: TELNET status code
-   TelnetLatency: TELNET response time
-   PingLostRate: PING packet loss rate |
|GroupId|Long|Yes|12345|The ID of the application group. |
|TaskName|String|Yes|task1|The name of the availability monitoring task. The name must be 4 to 100 characters in length and can contain letters, digits, and underscores \(\_\). |
|TaskType|String|Yes|HTTP|The type of the task. Valid values:

 -   PING
-   TELNET
-   HTTP |
|TaskScope|String|No|GROUP|The monitoring range of the availability monitoring task. Valid values:

 -   GROUP: monitors all Elastic Compute Service \(ECS\) instances in the application group
-   GROUP\_SPEC\_INSTANCE: monitors specific ECS instances in the application group The TaskScope and InstanceList.N parameters must be used in pairs. |
|TaskOption.HttpURI|String|No|https://www.aliyun.com|The URI that is monitored. This parameter is returned if the TaskType parameter is set to HTTP. |
|TaskOption.TelnetOrPingHost|String|No|www.aliyun.com|The domain name or IP address to be monitored.

 **Note:** Set this parameter if the TaskType parameter is set to PING or TELNET. |
|TaskOption.HttpResponseCharset|String|No|UTF-8|The character set that is used in the HTTP response. |
|TaskOption.HttpPostContent|String|No|params1=paramsValue1|The post body in the HTTP request. |
|TaskOption.HttpResponseMatchContent|String|No|ok|The response to the HTTP request. |
|TaskOption.HttpMethod|String|No|GET|The HTTP request method. Valid values:

 -   GET
-   POST
-   HEAD

 **Note:** Set this parameter if the TaskType parameter is set to HTTP. |
|TaskOption.HttpNegative|Boolean|No|true|The method to trigger an alert. The alert can be triggered based on whether the specified alert rule is included in the response body. Valid values:

 -   true: If the HTTP response body includes the alert rule, an alert is triggered.
-   false: If the HTTP response does not include the alert rule, an alert is triggered.

 **Note:** This parameter takes effects if the TaskType parameter is set to HTTP. |
|AlertConfig.StartTime|Integer|No|0|The beginning of the time period during which the alert rule is effective. Valid values: 0 to 23.

 **Note:** If the threshold is exceeded and an alert is triggered not during the effective period, the alert notification is not sent. |
|AlertConfig.EndTime|Integer|No|23|The end of the time period during which the alert rule is effective. Valid values: 0 to 23.

 **Note:** If the threshold is exceeded and an alert is triggered not during the effective period, the alert notification is not sent. |
|AlertConfig.SilenceTime|Integer|No|86400|The mute period during which notifications are not repeatedly sent for an alert. Unit: seconds. Default value: 86400. The default value indicates one day. |
|AlertConfig.WebHook|String|No|https://www.aliyun.com/webhook.json|The callback URL. |
|AlertConfigEscalationList.N.Aggregate|String|No|Value|The method used to calculate metric values that trigger alerts. Valid values of N: 1 to 21. The following points describe the correspondence between metrics and calculation methods:

 -   HttpStatus: Value
-   HttpLatency: Average
-   TelnetStatus: Value
-   TelnetLatency: Average
-   PingLostRate: Average

 **Note:** The value Value indicates the original value and is used for metrics such as status codes. The value Average indicates the average value and is used for metrics such as latency and packet loss rates. |
|AlertConfigEscalationList.N.Times|Integer|No|3|The consecutive number of times for which the metric value is measured before an alert is triggered. Valid values of N: 1 to 21. |
|AlertConfigEscalationList.N.Operator|String|No|\>|The comparison operator that is used in the alert rule. Valid values of N: 1 to 21. Valid values:

 -   `>`
-   `>=`
-   `<`
-   `<=`
-   `=` |
|AlertConfigEscalationList.N.Value|String|No|90|The alert threshold. Valid values of N: 1 to 21. |
|InstanceList.N|RepeatList|No|i-absdfkwl321\*\*\*\*|The ECS instances to be monitored. Valid values of N: 1 to 21.

 **Note:** If this parameter is not specified, all instances in the application group are monitored. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|ACBDBB40-DFB6-4F4C-8957-51FFB233969C|The ID of the request. |
|Code|String|200|The HTTP status code.

 **Note:** The value 200 indicates that the call was successful. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |
|TaskId|Long|12345|The ID of the availability monitoring task. |
|Message|String|Resources already exist.|The error message. |

## Examples

Sample request

```
http(s)://[Endpoint]/? Action=CreateHostAvailability
&AlertConfig.1otifyType=2
&GroupId=12345
&TaskName=task1
&TaskType=HTTP
&AlertConfigEscalationList.N.MetricName=HttpStatus
&<Common request parameters>
```

Sample success responses

`XML` format

```
<CreateHostAvailabilityResponse>
	  <TaskId>91****</TaskId>
	  <RequestId>CDA78493-F10F-485F-98AD-B4C0B40AB225</RequestId>
	  <Code>200</Code>
	  <Success>true</Success>
</CreateHostAvailabilityResponse>
```

`JSON` format

```
{
	"TaskId": "91****",
	"RequestId": "CDA78493-F10F-485F-98AD-B4C0B40AB225",
	"Code": 200,
	"Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

