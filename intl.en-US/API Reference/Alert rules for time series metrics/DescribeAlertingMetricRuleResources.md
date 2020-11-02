# DescribeAlertingMetricRuleResources

Queries the resources with active alerts that are triggered based on an alert rule.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeAlertingMetricRuleResources&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeAlertingMetricRuleResources|The operation that you want to perform. Set the value to DescribeAlertingMetricRuleResources. |
|RuleId|String|No|alerRuleId\*\*\*\*|The ID of the alert rule.

**Note:** You must specify at least one of the GroupId and RuleId parameters. If you specify both the parameters, only entries that meet both conditions are returned. |
|GroupId|String|No|123456|The ID of the application group. |
|Page|Integer|No|1|The number of the page to return. Default value: 1. |
|PageSize|Integer|No|10|The number of entries to return on each page. Default value: 10. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|9B868619-77B4-4623-AD64-6181EA7CF8FA|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |
|Code|Integer|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Total|Integer|1|The total number of the returned entries. |
|Resources|Array of Resource|N/A|The resources to which the alert rule is applied. |
|Resource|N/A|N/A|N/A|
|Enable|String|true|Indicates whether the alert rule is enabled for the resource. Valid values:

-   true
-   false |
|GroupId|String|123456|The ID of the application group.

**Note:** If the alert rule is associated with an application group, the ID of the application group is returned in this parameter. |
|LastAlertTime|String|1603159271000|The time when the last alert was triggered for the resource based on the alert rule.

This value is a UNIX timestamp that represents the number of milliseconds that have elapsed since January 1, 1970, 00:00:00 UTC. |
|LastModifyTime|String|1603159271000|The time when the resource was last modified.

This value is a UNIX timestamp that represents the number of milliseconds that have elapsed since January 1, 1970, 00:00:00 UTC. |
|MetricValues|String|\{\\"Maximum\\":3000.25,\\"Average\\":3000.25,\\"timestamp\\":1603159200000,\\"userId\\":\\"120886317861\*\*\*\*\\",\\"taskId\\":\\"87\*\*\*\*\\",\\"instanceId\\":\\"i-hp3aazrjdvrl41ar\*\*\*\*\\"\}|The metric value that triggered the alert based on the alert rule. The value is a JSON string. |
|Resource|String|userId=120886317861\*\*\*\*,taskId=87\*\*\*\*,instanceId=i-hp3aazrjdvrl41ar\*\*\*\*|The resource to which the alert rule is applied. |
|RetryTimes|String|3|The consecutive number of times for which the metric value is measured before an alert is triggered. |
|RuleId|String|detect\_87\*\*\*\*\_HTTP\_HttpLatency|The ID of the alert rule. |
|RuleName|String|test123-HttpLatency.Average|The name of the alert rule. |
|StartTime|String|1603159211000|The time when the resource was associated with the alert rule.

This value is a UNIX timestamp that represents the number of milliseconds that have elapsed since January 1, 1970, 00:00:00 UTC. |
|Threshold|String|500|The alert threshold. |
|Message|String|The Request is not authorization.|The returned message. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeAlertingMetricRuleResources
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeAlertingMetricRuleResourcesResponse>
      <RequestId>382001F9-A2E7-4511-8B79-75352ABA42F5</RequestId>
      <Total>2</Total>
      <Resources>
            <Resource>
                  <LastAlertTime>1603159271000</LastAlertTime>
                  <RuleId>detect_87****_HTTP_HttpLatency</RuleId>
                  <Resource>userId=120886317861****,taskId=87****,instanceId=i-hp3aazrjdvrl41ar****</Resource>
                  <StartTime>1603159211000</StartTime>
                  <Enable>true</Enable>
                  <MetricValues>{\"Maximum\":3000.25,\"Average\":3000.25,\"timestamp\":1603159200000,\"userId\":\"120886317861****\",\"taskId\":\"87****\",\"instanceId\":\"i-hp3aazrjdvrl41ar****\"}</MetricValues>
                  <LastModifyTime>1603159271000</LastModifyTime>
                  <RuleName>test123-HttpLatency.Average</RuleName>
                  <RetryTimes>3</RetryTimes>
                  <GroupId>6745****</GroupId>
                  <Threshold>500</Threshold>
            </Resource>
            <Resource>
                  <LastAlertTime>1603159271000</LastAlertTime>
                  <RuleId>detect_87****_HTTP_HttpLatency</RuleId>
                  <Resource>userId=120886317861****,taskId=87****,instanceId=i-m5e1qg6uo38rztr4****</Resource>
                  <StartTime>1603159211000</StartTime>
                  <Enable>true</Enable>
                  <MetricValues>{\"Maximum\":3000.99,\"Average\":3000.99,\"timestamp\":1603159200000,\"userId\":\"120886317861****\",\"taskId\":\"87****\",\"instanceId\":\"i-m5e1qg6uo38rztr4****\"}</MetricValues>
                  <LastModifyTime>1603159271000</LastModifyTime>
                  <RuleName>test123-HttpLatency.Average</RuleName>
                  <RetryTimes>3</RetryTimes>
                  <GroupId>6745****</GroupId>
                  <Threshold>500</Threshold>
            </Resource>
      </Resources>
      <Success>true</Success>
</DescribeAlertingMetricRuleResourcesResponse>
```

`JSON` format

```
{
    "RequestId": "382001F9-A2E7-4511-8B79-75352ABA42F5",
    "Total": 2,
    "Resources": {
        "Resource": [
            {
                "LastAlertTime": 1603159271000,
                "RuleId": "detect_87****_HTTP_HttpLatency",
                "Resource": "userId=120886317861****,taskId=87****,instanceId=i-hp3aazrjdvrl41ar****",
                "StartTime": 1603159211000,
                "Enable": true,
                "MetricValues": "{\"Maximum\":3000.25,\"Average\":3000.25,\"timestamp\":1603159200000,\"userId\":\"120886317861****\",\"taskId\":\"87****\",\"instanceId\":\"i-hp3aazrjdvrl41ar****\"}",
                "LastModifyTime": 1603159271000,
                "RuleName": "test123-HttpLatency.Average",
                "RetryTimes": 3,
                "GroupId": "6745****",
                "Threshold": "500"
            },
            {
                "LastAlertTime": 1603159271000,
                "RuleId": "detect_87****_HTTP_HttpLatency",
                "Resource": "userId=120886317861****,taskId=87****,instanceId=i-m5e1qg6uo38rztr4****",
                "StartTime": 1603159211000,
                "Enable": true,
                "MetricValues": "{\"Maximum\":3000.99,\"Average\":3000.99,\"timestamp\":1603159200000,\"userId\":\"120886317861****\",\"taskId\":\"87****\",\"instanceId\":\"i-m5e1qg6uo38rztr4****\"}",
                "LastModifyTime": 1603159271000,
                "RuleName": "test123-HttpLatency.Average",
                "RetryTimes": 3,
                "GroupId": "6745****",
                "Threshold": "500"
            }
        ]
    },
    "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

