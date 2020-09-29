# DeleteMetricRuleTargets

Deletes the message resources of an alert rule. This operation supports only Message Service \(MNS\) resources.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DeleteMetricRuleTargets&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DeleteMetricRuleTargets|The operation that you want to perform. Set the value to DeleteMetricRuleTargets. |
|RuleId|String|Yes|ruleId-xxxxxx|The ID of the alert rule. |
|TargetIds.N|RepeatList|Yes|12345|The ID of the message resource. Valid values of N: 1 to 5. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|FailIds|Struct|N/A|The message resources that failed to be deleted. |
|TargetIds|List|1|The ID of the message resource that failed to be deleted. |
|Message|String|The Request is not authorization.|The returned message. |
|RequestId|String|786E92D2-AC66-4250-B76F-F1E2FCDDBA1C|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DeleteMetricRuleTargets
&RuleId=ruleId-xxxxxx
&TargetIds.1=12345
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DeleteMetricRuleTargetsResponse>
          <RequestId>786E92D2-AC66-4250-B76F-F1E2FCDDBA1C</RequestId>
          <Code>200</Code>
          <Success>true</Success>
          <FailIds>
                <TargetIds>1</TargetIds>
          </FailIds>
</DeleteMetricRuleTargetsResponse>
```

`JSON` format

```
{
    "RequestId":"786E92D2-AC66-4250-B76F-F1E2FCDDBA1C",
    "Code":"200",
    "Success":"true",
    "FailIds":{
        "TargetIds":"1"
    }
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

