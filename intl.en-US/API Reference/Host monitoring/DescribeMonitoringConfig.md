# DescribeMonitoringConfig

Queries the global configurations of the Cloud Monitor agent.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeMonitoringConfig&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeMonitoringConfig|The operation that you want to perform. Set the value to DescribeMonitoringConfig. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |
|Code|String|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|RequestId|String|F35654DB-0C9D-4FB3-903F-479BA7663061|The ID of the request. |
|Message|String|The Request is not authorization.|The error message. |
|EnableInstallAgentNewECS|Boolean|true|Indicates whether the Cloud Monitor agent is automatically installed on new Elastic Compute Service \(ECS\) instances. Valid values:

 -   true
-   false |
|AutoInstall|Boolean|false|Indicates whether the Cloud Monitor agent is automatically installed on existing ECS instances. Valid values:

 -   true
-   false |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeMonitoringConfig
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeMonitoringConfigResponse>
	  <AutoInstall>false</AutoInstall>
	  <EnableInstallAgentNewECS>true</EnableInstallAgentNewECS>
	  <RequestId>BA76F154-DE3F-442C-94D3-895E7ABC1BDE</RequestId>
	  <Code>200</Code>
	  <Success>true</Success>
</DescribeMonitoringConfigResponse>
```

`JSON` format

```
{
  "AutoInstall": false,
  "EnableInstallAgentNewECS": true,
  "RequestId": "BA76F154-DE3F-442C-94D3-895E7ABC1BDE",
  "Code": 200,
  "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

