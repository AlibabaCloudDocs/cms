# PutExporterRule

Creates or modifies a data export rule.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=PutExporterRule&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|PutExporterRule|The operation that you want to perform. Set the value to PutExporterRule. |
|RuleName|String|Yes|MyRuleName|The name of the data export rule.

**Note:** If you set the value to the name of an existing rule, the rule is to be modified. Otherwise, a rule is to be created. |
|Namespace|String|Yes|acs\_ecs\_dashboard|The namespace of the service.

**Note:** For more information, see [DescribeMetricMetaList](~~98846~~) or [Appendix 1: Metrics](~~163515~~). |
|MetricName|String|Yes|cpu\_total|The name of the metric.

**Note:** For more information, see [DescribeMetricMetaList](~~98846~~) or [Appendix 1: Metrics](~~163515~~). |
|TargetWindows|String|Yes|60,300|The time window of the data to be exported.

**Note:**

-   Separate multiple time windows with commas \(,\).
-   Data in a time window of less than 60 seconds cannot be exported. |
|DstNames.N|RepeatList|Yes|distName1|The destination to which the data is exported. Valid values of N: 1 to 20. |
|Describe|String|No|Export CPU metrics|The description of the data export rule. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Message|String|success|The returned message. If the call was successful, the value success is returned. If the call failed, an error message is returned. |
|RequestId|String|461CF2CD-2FC3-4B26-8645-7BD27E7D0F1D|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=PutExporterRule
&RuleName=MyRuleName
&Namespace=acs_ecs_dashboard
&MetricName=cpu_total
&TargetWindows=60,300
&DstNames.1=distName1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<PutExporterRuleResponse>
          <Message>success</Message>
          <RequestId>8B524AE2-FBB1-4202-AA17-B3DEAAC8D861</RequestId>
          <Code>200</Code>
          <Success>true</Success>
</PutExporterRuleResponse>
```

`JSON` format

```
{
    "Message": "success",
    "RequestId": "8B524AE2-FBB1-4202-AA17-B3DEAAC8D861",
    "Code": "200",
    "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

