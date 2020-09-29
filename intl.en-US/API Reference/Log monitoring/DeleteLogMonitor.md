# DeleteLogMonitor

Deletes a log monitoring metric.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DeleteLogMonitor&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DeleteLogMonitor|The operation that you want to perform. Set the value to DeleteLogMonitor. |
|LogId|Long|Yes|12345|The ID returned by Log Service. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Message|String|metric not exist.|The returned message. |
|RequestId|String|42BFFC2B-5E4D-4FDE-BCC6-E91EE33C5967|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DeleteLogMonitor
&LogId=12345
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DeleteLogMonitorResponse>
          <RequestId>EBB5215C-44AB-4000-A2D7-48634FDC4F04</RequestId>
          <Success>true</Success>
          <Code>200</Code>
</DeleteLogMonitorResponse>
```

`JSON` format

```
{
    "RequestId": "EBB5215C-44AB-4000-A2D7-48634FDC4F04",
    "Success": "true",
    "Code": "200"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

