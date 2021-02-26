# PutMonitoringConfig

Configures global settings for the Cloud Monitor agent.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=PutMonitoringConfig&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|PutMonitoringConfig|The operation that you want to perform. Set the value to PutMonitoringConfig. |
|AutoInstall|Boolean|No|true|Specifies whether to automatically install the Cloud Monitor agent on existing Elastic Compute Service \(ECS\) instances. Valid values:

 -   true
-   false |
|EnableInstallAgentNewECS|Boolean|No|true|Specifies whether to automatically install the Cloud Monitor agent on new ECS instances. Valid values:

 -   true
-   false |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|Integer|200|The HTTP status code.

 **Note:** The value 200 indicates that the call was successful. |
|Message|String|Specified parameter EnableInstallAgentNewECS is not valid.|The error message. |
|RequestId|String|109C8095-6FAD-4DBB-B013-6ED18CE4C0B1|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |

## Examples

Sample request

```
http(s)://[Endpoint]/? Action=PutMonitoringConfig
&<Common request parameters>
```

Sample success responses

`XML` format

```
<PutMonitoringConfigResponse>
      <RequestId>109C8095-6FAD-4DBB-B013-6ED18CE4C0B1</RequestId>
      <Success>true</Success>
      <Code>200</Code>
</PutMonitoringConfigResponse>
```

`JSON` format

```
{
  "RequestId": "109C8095-6FAD-4DBB-B013-6ED18CE4C0B1",
  "Code": 200,
  "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

