# CreateGroupMonitoringAgentProcess

Creates a process monitoring task for an application group.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=CreateGroupMonitoringAgentProcess&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CreateGroupMonitoringAgentProcess|The operation that you want to perform. Set the value to CreateGroupMonitoringAgentProcess. |
|AlertConfig.N.ComparisonOperator|String|Yes|GreaterThanOrEqualToThreshold|The comparison operator of the threshold. Valid values:

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
|AlertConfig.N.EscalationsLevel|String|Yes|warn|The level of the alert. Default value: critical. Valid values:

-   critical
-   warn
-   info |
|AlertConfig.N.Threshold|String|Yes|5|The threshold of the metric value. |
|AlertConfig.N.Times|String|Yes|3|The number of times for which the threshold can be consecutively exceeded. Default value: 3.

**Note:** A metric triggers an alert only after the metric value reaches the threshold consecutively for the specified times. |
|GroupId|String|Yes|123456|The ID of the application group. |
|ProcessName|String|Yes|test1|The name of the process monitoring task. |
|MatchExpressFilterRelation|String|No|and|The logical operator used between conditional expressions that are used to match instances. Valid values:

-   all
-   and
-   or |
|MatchExpress.N.Name|String|No|name1|The criteria based on which the instances are matched.

**Note:** Set the value to name, indicating that the instances are matched based on instance name. |
|MatchExpress.N.Function|String|No|startWith|The method that is used to match the instances. Default value: all. Valid values:

-   all
-   startWith
-   endWith
-   contains
-   notContains
-   equals |
|MatchExpress.N.Value|String|No|portalHost|The keyword used to match the instance name. |
|AlertConfig.N.EffectiveInterval|String|No|00:00-23:59|The time period during which the alert rule is effective. |
|AlertConfig.N.NoEffectiveInterval|String|No|00:00-23:59|The time period during which the specified alert rule is ineffective. |
|AlertConfig.N.SilenceTime|String|No|86400|The mute period during which new alerts are not sent even if the trigger conditions are met. Unit: seconds. Minimum value: 3600, which is equivalent to one hour. Default value: 86400, which is equivalent to one day.

**Note:** Only one alert notification is sent during each mute period even if the metric value consecutively exceeds the alert threshold several times. |
|AlertConfig.N.Webhook|String|No|http://www.aliyun.com|The callback URL. |
|AlertConfig.N.Statistics|String|No|Average|The statistical aggregation method that is used to calculate the metric values.

**Note:** Set the value to Average. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|3F6150F9-45C7-43F9-9578-A58B2E726C90|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Message|String|The Request is not authorization.|The returned message. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=CreateGroupMonitoringAgentProcess
&AlertConfig.1.ComparisonOperator=GreaterThanOrEqualToThreshold
&AlertConfig.1.EscalationsLevel=warn
&AlertConfig.1.Threshold=5
&AlertConfig.1.Times=3
&GroupId=123456
&ProcessName=test1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<CreateGroupMonitoringAgentProcessResponse>
          <RequestId>7985D471-3FA8-4EE9-8F4B-45C19DF3D36F</RequestId>
          <Success>true</Success>
          <Code>200</Code>
</CreateGroupMonitoringAgentProcessResponse>
```

`JSON` format

```
{
    "RequestId": "7985D471-3FA8-4EE9-8F4B-45C19DF3D36F",
    "Success": true,
    "Code": 200
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

