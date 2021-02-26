# DescribeMonitoringConfig

调用DescribeMonitoringConfig接口查询云监控插件的全局配置。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeMonitoringConfig&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeMonitoringConfig|要执行的操作，取值：DescribeMonitoringConfig。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|RequestId|String|F35654DB-0C9D-4FB3-903F-479BA7663061|请求ID。 |
|Message|String|The Request is not authorization.|错误信息。 |
|EnableInstallAgentNewECS|Boolean|true|新购ECS主机是否自动安装云监控插件。取值：

 -   true
-   false |
|AutoInstall|Boolean|false|现有ECS主机是否自动安装云监控插件。取值：

 -   true
-   false |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeMonitoringConfig
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeMonitoringConfigResponse>
	  <AutoInstall>false</AutoInstall>
	  <EnableInstallAgentNewECS>true</EnableInstallAgentNewECS>
	  <RequestId>BA76F154-DE3F-442C-94D3-895E7ABC1BDE</RequestId>
	  <Code>200</Code>
	  <Success>true</Success>
</DescribeMonitoringConfigResponse>
```

`JSON` 格式

```
{
  "AutoInstall": false,
  "EnableInstallAgentNewECS": true,
  "RequestId": "BA76F154-DE3F-442C-94D3-895E7ABC1BDE",
  "Code": 200,
  "Success": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

