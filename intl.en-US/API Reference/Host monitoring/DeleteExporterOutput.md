# DeleteExporterOutput

Deletes a configuration set for exporting monitoring data.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DeleteExporterOutput&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DeleteExporterOutput|The operation that you want to perform. Set the value to **DeleteExporterOutput**. |
|DestName|String|Yes|testName|The name of the configuration set. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. Other status codes indicate that the call failed. |
|Message|String|Success|The returned message. |
|RequestId|String|2DECF751-7AFA-43BB-8C63-2B6B07E51AE1|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   `true`: indicates a success.
-   `false`: indicates a failure. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DeleteExporterOutput
&DestName=testName
&<Common request parameters>
```

Sample success responses

`XML` format

```
<Message>success</Message>
<RequestId>296AE90D-153C-4612-AF24-75D0F5921976</RequestId>
<Code>200</Code>
<Success>true</Success>
```

`JSON` format

```
{
    "Message": "success",
    "RequestId": "296AE90D-153C-4612-AF24-75D0F5921976",
    "Code": "200",
    "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

