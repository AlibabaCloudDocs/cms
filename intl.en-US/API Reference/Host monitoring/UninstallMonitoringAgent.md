# UninstallMonitoringAgent

Uninstalls the Cloud Monitor agent from a host that is not provided by Alibaba Cloud.

**Note:** This API operation is not applicable to ECS instances. To uninstall the agent from an ECS instance, see [Install and uninstall the Cloud Monitor agent](~~183482~~).

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer automatically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=UninstallMonitoringAgent&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|UninstallMonitoringAgent|The operation that you want to perform. Set the value to UninstallMonitoringAgent. |
|InstanceId|String|Yes|host-\*\*\*\*|The ID of the host. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

 **Note:** The HTTP status code 200 indicates that the call was successful. |
|Message|String|Successfully|The returned message. |
|RequestId|String|466902B9-2842-40B0-B796-00FE772B6EF3|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=UninstallMonitoringAgent
&InstanceId=host-****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<UninstallMonitoringAgentResponse>
    <RequestId>466902B9-2842-40B0-B796-00FE772B6EF3</RequestId>
    <Code>200</Code>
    <Message>Successfully</Message>
</UninstallMonitoringAgentResponse>
```

`JSON` format

```
{
    "RequestId": "466902B9-2842-40B0-B796-00FE772B6EF3",
    "Code": "200",
    "Message": "Successfully"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

