# DescribeMonitoringAgentConfig

调用DescribeMonitoringAgentConfig接口查询云监控插件的配置信息。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeMonitoringAgentConfig&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeMonitoringAgentConfig|要执行的操作，取值：DescribeMonitoringAgentConfig。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|E9F4FA2A-54BE-4EF9-9D1D-1A0B1DC86B8D|请求ID。 |
|AutoInstall|Boolean|true|现有ECS主机是否自动安装云监控插件。取值：

 -   true
-   false |
|EnableInstallAgentNewECS|Boolean|true|新购ECS主机是否自动安装云监控插件。取值：

 -   true
-   false |
|Message|String|The Request is not authorization.|错误信息。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|EnableActiveAlert|String|redis,rds,ecs|开通一键告警的云服务。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeMonitoringAgentConfig
&<公共请求参数>
```

正常返回示例

`XML` 格式

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

`JSON` 格式

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

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

