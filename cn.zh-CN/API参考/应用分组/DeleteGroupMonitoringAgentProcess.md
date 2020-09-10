# DeleteGroupMonitoringAgentProcess

调用DeleteGroupMonitoringAgentProcess接口删除组进程监控任务。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DeleteGroupMonitoringAgentProcess&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteGroupMonitoringAgentProcess|要执行的操作，取值：DeleteGroupMonitoringAgentProcess。 |
|GroupId|String|是|123456|应用分组ID。 |
|Id|String|是|48F83746-C817-478C-9B06-7158F56B\*\*\*\*|组进程ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|3F6150F9-45C7-43F9-9578-A58B2E726C90|请求ID。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Message|String|The Request is not authorization.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DeleteGroupMonitoringAgentProcess
&GroupId=123456
&Id=48F83746-C817-478C-9B06-7158F56B****
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DeleteGroupMonitoringAgentProcessResponse>
		  <RequestId>7985D471-3FA8-4EE9-8F4B-45C19DF3D36F</RequestId>
		  <Success>true</Success>
		  <Code>200</Code>
</DeleteGroupMonitoringAgentProcessResponse>
```

`JSON` 格式

```
{
	"RequestId": "7985D471-3FA8-4EE9-8F4B-45C19DF3D36F",
	"Success": true,
	"Code": 200
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

