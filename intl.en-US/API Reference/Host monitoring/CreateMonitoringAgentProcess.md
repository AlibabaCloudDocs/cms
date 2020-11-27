# CreateMonitoringAgentProcess

Creates a task to monitor a specified process.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=CreateMonitoringAgentProcess&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CreateMonitoringAgentProcess|The operation that you want to perform. Set the value to CreateMonitoringAgentProcess. |
|InstanceId|String|Yes|i-2ze51wjtwox01r8g\*\*\*\*|The ID of the instance. |
|ProcessName|String|No|java|The name of the process. |
|ProcessUser|String|No|admin|The user who launches the process. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Id|Long|12345|The ID of the process. |
|Message|String|User not authorized to operate on the specified resource.|The error message. |
|RequestId|String|0DFCB47D-E7E1-4CBE-A381-8339F7B300EF|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=CreateMonitoringAgentProcess
&InstanceId= i-2ze51wjtwox01r8g****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<CreateMonitoringAgentProcessResponse>
      <RequestId>0DFCB47D-E7E1-4CBE-A381-8339F7B300EF</RequestId>
      <Id>171894</Id>
      <Success>true</Success>
      <Code>200</Code>
</CreateMonitoringAgentProcessResponse>
```

`JSON` format

```
{
  "RequestId": "0DFCB47D-E7E1-4CBE-A381-8339F7B300EF",
  "Id": 489492,
  "Code": 200,
  "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

