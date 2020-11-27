# DisableMetricRules

Disables alert rules.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DisableMetricRules&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DisableMetricRules|The operation that you want to perform. Set the value to DisableMetricRules. |
|RuleId.N|RepeatList|Yes|detect\_87\*\*\*\*\_HTTP\_HttpLatency|The ID of the alert rule. Valid values of N: 1 to 20. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Message|String|RuleId is mandatory for this action.|The error message. |
|RequestId|String|FF38D33A-67C1-40EB-AB65-FAEE51EDB644|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DisableMetricRules
&RuleId.1=detect_87****_HTTP_HttpLatency
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DisableMetricRulesResponse>
      <Code>200</Code>
      <RequestId>FF38D33A-67C1-40EB-AB65-FAEE51EDB644</RequestId>
      <Success>true</Success>
</DisableMetricRulesResponse>
```

`JSON` format

```
{
    "Code":"200",
    "RequestId":"FF38D33A-67C1-40EB-AB65-FAEE51EDB644",
    "Success":true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

