# PutMonitoringConfig

调用PutMonitoringConfig接口设置云监控插件的全局配置。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=PutMonitoringConfig&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|PutMonitoringConfig|要执行的操作，取值：PutMonitoringConfig。 |
|AutoInstall|Boolean|否|true|现有ECS主机是否自动安装云监控插件。取值：

 -   true
-   false |
|EnableInstallAgentNewECS|Boolean|否|true|新购ECS主机是否自动安装云监控插件。取值：

 -   true
-   false |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|Integer|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|Specified parameter EnableInstallAgentNewECS is not valid.|错误信息。 |
|RequestId|String|109C8095-6FAD-4DBB-B013-6ED18CE4C0B1|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=PutMonitoringConfig
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<PutMonitoringConfigResponse>
      <RequestId>109C8095-6FAD-4DBB-B013-6ED18CE4C0B1</RequestId>
      <Success>true</Success>
      <Code>200</Code>
</PutMonitoringConfigResponse>
```

`JSON` 格式

```
{
  "RequestId": "109C8095-6FAD-4DBB-B013-6ED18CE4C0B1",
  "Code": 200,
  "Success": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

