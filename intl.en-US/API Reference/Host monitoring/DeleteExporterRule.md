# DeleteExporterRule

Deletes a data export rule.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DeleteExporterRule&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DeleteExporterRule|The operation that you want to perform. Set the value to **DeleteExporterRule**. |
|RuleName|String|Yes|myRuleName|The name of the data export rule. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. Other status codes indicate that the call failed. |
|Message|String|success|The returned message. |
|RequestId|String|6A5F022D-AC7C-460E-94AE-B9E75083D023|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   `true`: indicates a success.
-   `false`: indicates a failure. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DeleteExporterRule
&RuleName=myRuleName
&<Common request parameters>
```

Sample success responses

`XML` format

```
<Message>success</Message>
<RequestId>8B524AE2-FBB1-4202-AA17-B3DEAAC8D861</RequestId>
<Code>200</Code>
<Success>true</Success>
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

