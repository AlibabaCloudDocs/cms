# DeleteMonitorGroupNotifyPolicy

调用DeleteMonitorGroupNotifyPolicy接口删除暂停指定应用分组报警通知策略。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DeleteMonitorGroupNotifyPolicy&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteMonitorGroupNotifyPolicy|要执行的操作，取值：DeleteMonitorGroupNotifyPolicy。 |
|PolicyType|String|是|PauseNotify|暂停通知类型。目前仅支持PauseNotify。 |
|RegionId|String|是|华东1（杭州）|目前仅支持3个地域。取值：

 -   华东1（杭州）
-   新加坡
-   日本（东京） |
|GroupId|String|否|123456|应用分组ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The Request is not authorization.|错误信息。 |
|RequestId|String|B7AF834D-D38B-4A46-920B-FE974EB7E135|请求ID。 |
|Result|Integer|1|影响行数。 |
|Success|String|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DeleteMonitorGroupNotifyPolicy
&PolicyType=PauseNotify
&RegionId=华东1（杭州）
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DeleteMonitorGroupNotifyPolicyResponse>
      <Result>1</Result>
      <Success>true</Success>
      <Code>200</Code>
</DeleteMonitorGroupNotifyPolicyResponse>
```

`JSON` 格式

```
{
	"Result":1,
	"RequestId":"5D0D3910-5B01-4868-A2F2-A5DEA7F5150E",
	"Success":true,
	"Code":200
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

