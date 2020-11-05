# CreateMonitoringAgentProcess

调用CreateMonitoringAgentProcess接口创建进程监控。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=CreateMonitoringAgentProcess&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateMonitoringAgentProcess|要执行的操作，取值：CreateMonitoringAgentProcess。 |
|InstanceId|String|是|i-2ze51wjtwox01r8g\*\*\*\*|实例ID。 |
|ProcessName|String|否|java|进程名称。 |
|ProcessUser|String|否|admin|执行进程的用户。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Id|Long|12345|进程ID。 |
|Message|String|User not authorized to operate on the specified resource.|错误消息。 |
|RequestId|String|0DFCB47D-E7E1-4CBE-A381-8339F7B300EF|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=CreateMonitoringAgentProcess
&InstanceId= i-2ze51wjtwox01r8g****
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<CreateMonitoringAgentProcessResponse>
      <RequestId>0DFCB47D-E7E1-4CBE-A381-8339F7B300EF</RequestId>
      <Id>171894</Id>
      <Success>true</Success>
      <Code>200</Code>
</CreateMonitoringAgentProcessResponse>
```

`JSON` 格式

```
{
  "RequestId": "0DFCB47D-E7E1-4CBE-A381-8339F7B300EF",
  "Id": 489492,
  "Code": 200,
  "Success": true
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

