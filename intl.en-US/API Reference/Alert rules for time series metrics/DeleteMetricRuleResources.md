# DeleteMetricRuleResources

Disassociates resources from an alert rule.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DeleteMetricRuleResources&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DeleteMetricRuleResources|The operation that you want to perform. Set the value to DeleteMetricRuleResources. |
|Resources|String|Yes|\[\{"instanceId":"i-uf6hm9lnlzsarrc7\*\*\*\*"\}\]|The resources to be disassociated from the alert rule. |
|RuleId|String|Yes|rr-bp18017n6iolv\*\*\*\*|The ID of the alert rule. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|D8A35882-90C6-4F03-BBEB-153C180398EA|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |
|Code|String|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Message|String|The alert does not exist.|The returned message. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DeleteMetricRuleResources
&Resources=[{"instanceId":"i-uf6hm9lnlzsarrc7****"}]
&RuleId=rr-bp18017n6iolv****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DeleteMetricRuleResourcesResponse>
		  <RequestId>0671A721-0D7A-4F11-BB77-2416325D65AB</RequestId>
		  <Success>true</Success>
		  <Code>200</Code>
</DeleteMetricRuleResourcesResponse>
```

`JSON` format

```
{
    "RequestId": "0671A721-0D7A-4F11-BB77-2416325D65AB",
    "Success": true,
    "Code": "200"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

