# CreateMonitorGroupNotifyPolicy

调用CreateMonitorGroupNotifyPolicy接口创建暂停应用分组报警通知的策略。

在策略的生效期间内，应用分组内发生的所有报警都不再发送通知。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=CreateMonitorGroupNotifyPolicy&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateMonitorGroupNotifyPolicy|要执行的操作，取值：CreateMonitorGroupNotifyPolicy。 |
|GroupId|String|是|12345|应用分组ID。 |
|PolicyType|String|是|PauseNotify|暂停通知类型。目前仅支持PauseNotify。 |
|StartTime|Long|是|1551756547863|暂停通知的开始时间。

 格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |
|EndTime|Long|是|1551757147863|暂停通知的结束时间。

 格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |
|RegionId|String|是|华东1（杭州）|目前仅支持3个地域。取值：

 -   华东1（杭州）
-   新加坡
-   日本（东京） |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|13356BCA-3EC3-4748-A771-2064DA69AEF1|请求ID。 |
|Success|String|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Result|Integer|1|返回创建的结果数。 |
|Message|String|The Request is not authorization.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=CreateMonitorGroupNotifyPolicy
&GroupId=12345
&PolicyType=PauseNotify
&StartTime=1551756547863
&EndTime=1551757147863
&RegionId=华东1（杭州）
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<CreateMonitorGroupNotifyPolicyResponse>
		  <RequestId>13356BCA-3EC3-4748-A771-2064DA69AEF1</RequestId>
		  <Result>1</Result>
		  <Success>true</Success>
		  <Code>200</Code>
</CreateMonitorGroupNotifyPolicyResponse>
```

`JSON` 格式

```
{
  "RequestId":"13356BCA-3EC3-4748-A771-2064DA69AEF1",
  "Result": 1,
  "Success": true,
  "Code": "200"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

