# DescribeMetricRuleCount

Queries the number of alert rules in each state.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeMetricRuleCount&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeMetricRuleCount|The operation that you want to perform. Set the value to DescribeMetricRuleCount. |
|Namespace|String|No|acs\_ecs\_dashboard|The namespace of the service. For more information, see [Appendix 1: Metrics](~~163515~~). |
|MetricName|String|No|cpu\_total|The name of the metric. For more information, see [Appendix 1: Metrics](~~163515~~). |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Message|String|The Request is not authorization.|The returned message. |
|MetricRuleCount|Struct|N/A|The number of alert rules in each state. |
|Alarm|Integer|5|The number of alert rules with active alerts. |
|Disable|Integer|0|The number of disabled alert rules. |
|Nodata|Integer|0|The number of alert rules without data. |
|Ok|Integer|40|The number of alert rules without active alerts. |
|Total|Integer|45|The total number of alert rules. |
|RequestId|String|FF38D33A-67C1-40EB-AB65-FAEE51EDB644|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeMetricRuleCount
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeMetricRuleCountResponse>
      <Success>true</Success>
      <Code>200</Code>
      <RequestId>FF38D33A-67C1-40EB-AB65-FAEE51EDB644</RequestId>
      <MetricRuleCount>
            <Ok>40</Ok>
            <Disable>0</Disable>
            <Total>45</Total>
            <Nodata>0</Nodata>
            <Alarm>5</Alarm>
      </MetricRuleCount>
</DescribeMetricRuleCountResponse>
```

`JSON` format

```
{
  "Success": true,
  "Code": "200",
  "RequestId":"FF38D33A-67C1-40EB-AB65-FAEE51EDB644",
  "MetricRuleCount": {
    "Ok": 40,
    "Disable": 0,
    "Total": 45,
    "Nodata": 0,
    "Alarm": 5
  }
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

