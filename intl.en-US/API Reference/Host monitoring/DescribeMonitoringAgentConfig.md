# DescribeMonitoringAgentConfig

Queries the configuration of the Cloud Monitor agent.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeMonitoringAgentConfig&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeMonitoringAgentConfig|The operation that you want to perform. Set the value to DescribeMonitoringAgentConfig. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|E9F4FA2A-54BE-4EF9-9D1D-1A0B1DC86B8D|The ID of the request. |
|AutoInstall|Boolean|true|Indicates whether the Cloud Monitor agent is automatically installed on existing Elastic Compute Service \(ECS\) instances. Valid values:

 -   true
-   false |
|EnableInstallAgentNewECS|Boolean|true|Indicates whether the Cloud Monitor agent is automatically installed on new ECS instances. Valid values:

 -   true
-   false |
|Message|String|Successfully|The error message. |
|Code|String|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |
|EnableActiveAlert|String|redis,rds,ecs|The service for which one-click alert is enabled. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeMonitoringAgentConfig
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeMonitoringAgentConfigResponse>
	  <AutoInstall>true</AutoInstall>
	  <EnableActiveAlert></EnableActiveAlert>
	  <EnableInstallAgentNewECS>true</EnableInstallAgentNewECS>
	  <RequestId>B4EB0F95-3181-4E8F-B32E-8C3734E8F88E</RequestId>
	  <Code>200</Code>
	  <Success>true</Success>
</DescribeMonitoringAgentConfigResponse>
```

`JSON` format

```
{
  "AutoInstall": true,
  "EnableActiveAlert": "",
  "EnableInstallAgentNewECS": true,
  "RequestId": "B4EB0F95-3181-4E8F-B32E-8C3734E8F88E",
  "Code": 200,
  "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

