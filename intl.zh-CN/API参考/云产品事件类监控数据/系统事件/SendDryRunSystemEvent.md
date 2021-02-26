# SendDryRunSystemEvent

调用SendDryRunSystemEvent接口调试云资源的系统事件。

本接口用于调试资源配置的触发逻辑是否符合预期，即通过调用该接口发送一条测试事件，帮助您验证对应的事件触发报警后返回的内容是否符合预期。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=SendDryRunSystemEvent&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SendDryRunSystemEvent|要执行的操作，取值：SendDryRunSystemEvent。 |
|EventName|String|是|Agent\_Status\_Stopped|事件名称。

 **说明：** 详细信息请参见[DescribeSystemEventMetaList](~~114972~~)。 |
|Product|String|是|ecs|云服务名称。

 **说明：** 事件支持的云服务，详细信息请参见[云服务系统事件](~~167388~~)。 |
|GroupId|String|否|123456|应用分组ID。 |
|EventContent|String|否|\{"product":"CloudMonitor","resourceId":"acs:ecs:cn-hongkong:173651113438\*\*\*\*:instance/\{instanceId\}","level":"CRITICAL","instanceName":"instanceName","regionId":"cn-hangzhou","name":"Agent\_Status\_Stopped","content":\{"ipGroup":"0.0.0.0,0.0.0.1","tianjimonVersion":"1.2.11"\},"status":"stopped"\}|事件内容。

 **说明：** 该参数的取值可以为任意一个合法的JSON，建议JSON中包含关键字值`product`、`resourceId`和`regionId`。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|486029C9-53E1-44B4-85A8-16A571A043FD|请求ID。 |
|Success|String|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|success|返回信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=SendDryRunSystemEvent
&EventName=Agent_Status_Stopped
&Product=ecs
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<SendDryRunSystemEventResponse>
	  <Message>success</Message>
	  <RequestId>590FB642-5FFE-4AE0-883B-E1323DD20541</RequestId>
	  <Code>200</Code>
	  <Success>true</Success>
</SendDryRunSystemEventResponse>
```

`JSON` 格式

```
{
  "Message": "success",
  "RequestId": "590FB642-5FFE-4AE0-883B-E1323DD20541",
  "Code": "200",
  "Success": true
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

