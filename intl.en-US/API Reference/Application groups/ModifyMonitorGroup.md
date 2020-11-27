# ModifyMonitorGroup

Modifies an application group.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=ModifyMonitorGroup&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ModifyMonitorGroup|The operation that you want to perform. Set the value to ModifyMonitorGroup. |
|GroupId|String|Yes|123456|The ID of the application group. |
|GroupName|String|No|ecs\_group|The name of the application group. |
|ContactGroups|String|No|alarm\_ecs\_group|The alert groups that can receive alert notifications for the application group. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|Integer|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Message|String|The specified resource is not found.|The error message. |
|RequestId|String|C85A2870-5DF4-4269-BC50-ECB5E4591A80|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=ModifyMonitorGroup
&GroupId=123456
&GroupName=ecs_group
&<Common request parameters>
```

Sample success responses

`XML` format

```
<ModifyMonitorGroupResponse>
      <RequestId>36FE4D3A-A907-4F2A-921C-89612FFA977B</RequestId>
      <Success>true</Success>
      <Code>200</Code>
</ModifyMonitorGroupResponse>
```

`JSON` format

```
{
  "RequestId": "36FE4D3A-A907-4F2A-921C-89612FFA977B",
  "Success": true,
  "Code": 200
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

