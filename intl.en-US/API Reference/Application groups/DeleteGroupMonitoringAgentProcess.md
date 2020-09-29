# DeleteGroupMonitoringAgentProcess

Deletes a process monitoring task for an application group.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DeleteGroupMonitoringAgentProcess&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DeleteGroupMonitoringAgentProcess|The operation that you want to perform. Set the value to DeleteGroupMonitoringAgentProcess. |
|GroupId|String|Yes|123456|The ID of the application group. |
|Id|String|Yes|48F83746-C817-478C-9B06-7158F56B\*\*\*\*|The ID of the process monitoring task. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|3F6150F9-45C7-43F9-9578-A58B2E726C90|The ID of the request. |
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |
|Message|String|The Request is not authorization.|The returned message. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DeleteGroupMonitoringAgentProcess
&GroupId=123456
&Id=48F83746-C817-478C-9B06-7158F56B****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DeleteGroupMonitoringAgentProcessResponse>
          <RequestId>7985D471-3FA8-4EE9-8F4B-45C19DF3D36F</RequestId>
          <Success>true</Success>
          <Code>200</Code>
</DeleteGroupMonitoringAgentProcessResponse>
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

