# CreateMonitorAgentProcess

Creates a task to monitor a process.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=CreateMonitorAgentProcess&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CreateMonitorAgentProcess|The operation that you want to perform. Set the value to CreateMonitorAgentProcess. |
|InstanceId|String|Yes|i-2ze2d6j5uhg20x47\*\*\*\*|The ID of the instance. |
|ProcessName|String|Yes|AliYunDun|The name of the process. |
|ProcessUser|String|No|admin|The user who launches the process. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Id|Long|123456|The ID of the process. |
|Message|String|User not authorized to operate on the specified resource.|The error message. |
|RequestId|String|971CC023-5A96-452A-BB7C-2483F948BCFD|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=CreateMonitorAgentProcess
&InstanceId=i-2ze2d6j5uhg20x47****
&ProcessName=AliYunDun
&<Common request parameters>
```

Sample success responses

`XML` format

```
<CreateMonitorAgentProcessResponse>
      <RequestId>971CC023-5A96-452A-BB7C-2483F948BCFD</RequestId>
      <Id>123456</Id>
      <Success>true</Success>
      <Code>200</Code>
</CreateMonitorAgentProcessResponse>
```

`JSON` format

```
{
  "RequestId": "CA9CE1FD-E546-4D44-B1DE-5D22496553E1",
  "Id": 123456,
  "Code": 200,
  "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

