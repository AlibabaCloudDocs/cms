# CreateGroupMonitoringAgentProcess

调用CreateGroupMonitoringAgentProcess接口创建组进程监控。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=CreateGroupMonitoringAgentProcess&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateGroupMonitoringAgentProcess|要执行的操作，取值：CreateGroupMonitoringAgentProcess。 |
|AlertConfig.N.ComparisonOperator|String|是|GreaterThanOrEqualToThreshold|阈值比较符。取值：

 -   GreaterThanOrEqualToThreshold：大于等于。
-   GreaterThanThreshold：大于。
-   LessThanOrEqualToThreshold：小于等于。
-   LessThanThreshold：小于。
-   NotEqualToThreshold：不等。
-   GreaterThanYesterday：同比昨天时间上涨。
-   LessThanYesterday：同比昨天时间下降。
-   GreaterThanLastWeek：同比上周同一时间上涨。
-   LessThanLastWeek：同比上周同一时间下降。
-   GreaterThanLastPeriod：环比上周期上涨。
-   LessThanLastPeriod：环比上周期下降。 |
|AlertConfig.N.EscalationsLevel|String|是|warn|报警级别。取值：

 -   critical（默认值）：故障。
-   warn：警告。
-   info：信息。 |
|AlertConfig.N.Threshold|String|是|5|报警阈值。 |
|AlertConfig.N.Times|String|是|3|报警级别连续出现次数。默认：3次。

 **说明：** 只有当报警级别连续出现设定的次数且达到报警阈值才会触发报警。 |
|GroupId|String|是|123456|应用分组ID。 |
|ProcessName|String|是|test1|进程名称。 |
|MatchExpressFilterRelation|String|否|and|匹配实例的条件。取值：

 -   all：全部。
-   and：与。
-   or：或。 |
|MatchExpress.N.Name|String|否|name1|匹配条件的类型。

 **说明：** 目前仅支持name，即实例名称。 |
|MatchExpress.N.Function|String|否|startWith|匹配条件。取值：

 -   all（默认值）：全部。
-   startWith：前缀。
-   endWith：后缀。
-   contains：包含。
-   notContains：不包含。
-   equals：相等。 |
|MatchExpress.N.Value|String|否|portalHost|匹配实例名。 |
|AlertConfig.N.EffectiveInterval|String|否|00:00-23:59|报警规则的生效时间段。 |
|AlertConfig.N.NoEffectiveInterval|String|否|00:00-23:59|报警规则不生效时间段。 |
|AlertConfig.N.SilenceTime|String|否|86400|通道沉默周期。单位：秒。最小值：3600秒（1小时），默认值：86400秒（1天）。

 **说明：** 当监控数据持续超过报警规则阈值时，每个沉默周期内只发送一次报警通知。 |
|AlertConfig.N.Webhook|String|否|http://www.aliyun.com|报警回调URL地址。 |
|AlertConfig.N.Statistics|String|否|Average|报警统计方式。

 **说明：** 目前仅支持Average。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|3F6150F9-45C7-43F9-9578-A58B2E726C90|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The Request is not authorization.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=CreateGroupMonitoringAgentProcess
&AlertConfig.1.ComparisonOperator=GreaterThanOrEqualToThreshold
&AlertConfig.1.EscalationsLevel=warn
&AlertConfig.1.Threshold=5
&AlertConfig.1.Times=3
&GroupId=123456
&ProcessName=test1
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<CreateGroupMonitoringAgentProcessResponse>
		  <RequestId>7985D471-3FA8-4EE9-8F4B-45C19DF3D36F</RequestId>
		  <Success>true</Success>
		  <Code>200</Code>
</CreateGroupMonitoringAgentProcessResponse>
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

