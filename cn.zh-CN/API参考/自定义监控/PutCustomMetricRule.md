# PutCustomMetricRule

调用PutCustomMetricRule接口创建自定义监控报警规则。

调用本接口前，请先调用PutCustomMetric接口上报自定义监控数据，详情请参见 [PutCustomMetric](~~115004~~)。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=PutCustomMetricRule&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|PutCustomMetricRule|要执行的操作，取值：PutCustomMetricRule。 |
|ComparisonOperator|String|是|\>=|阈值比较符号。取值：

 -   `>=`
-   =
-   `<=`
-   `>`
-   `<`
-   `!=` |
|ContactGroups|String|是|ECS\_Group|报警联系人组。多个联系人组之间用英文逗号（,）分隔。 |
|EvaluationCount|Integer|是|3|报警重试次数。 |
|Level|String|是|CRITICAL|报警级别。取值：

 -   CRITICAL：严重。
-   WARN：警告。
-   INFO：信息。 |
|MetricName|String|是|cpu\_total|监控项名称。

 **说明：** 获取方法请参见[DescribeCustomMetricList](~~115005~~)。 |
|Resources|String|是|\[\{"groupId":7378\*\*\*\*,"dimension":"instanceId=i-hp3543t5e4sudb3s\*\*\*\*"\}\]|报警规则作用的自定义监控数据。由自定义监控数据所属应用分组ID和监控项所属维度组成。 |
|RuleId|String|是|MyRuleId1|报警规则ID。

 **说明：** 如果报警规则ID已存在，则表示修改报警规则；如果报警规则ID不存在，则表示创建报警规则。 |
|Statistics|String|是|Average|报警统计方法。 |
|Threshold|String|是|90|报警阈值。 |
|GroupId|String|否|7378\*\*\*\*|自定义监控数据所属应用分组ID。

 **说明：** 0表示上报的自定义监控数据不属于任何一个应用分组。 |
|RuleName|String|否|CpuUsage|报警规则名称。 |
|Webhook|String|否|https://www.aliyun.com|报警发生回调时指定的URL地址，向URL发送POST请求。 |
|EffectiveInterval|String|否|00:00-23:59|报警规则生效的时间范围。取值范围：00:00-23:59。 |
|SilenceTime|Integer|否|86400|通道沉默周期。单位：秒，默认值：86400（1天）。

 **说明：** 当监控数据持续超过报警规则阈值时，每个沉默周期内只发送一次报警通知。 |
|Period|String|否|300|自定义监控数据的聚合周期。单位：秒。取值为60或60的整数倍。默认为自定义监控数据的原始上报周期。 |
|EmailSubject|String|否|ECS实例|报警邮件主题。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|ComparisonOperator is mandatory for this action.|返回信息。接口调用成功时，返回为空；接口调用失败时，返回失败原因。 |
|RequestId|String|65D50468-ECEF-48F1-A6E1-D952E89D9432|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=PutCustomMetricRule
&ComparisonOperator=>=
&ContactGroups=ECS_Group
&EvaluationCount=3
&Level=CRITICAL
&MetricName=cpu_total
&Resources=[{"groupId":7378****,"dimension":"instanceId=i-hp3543t5e4sudb3s****"}]
&RuleId=MyRuleId1
&Statistics=Average
&Threshold=90
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<PutCustomMetricRuleResponse>
	  <Message></Message>
	  <Code>200</Code>
	  <Success>true</Success>
</PutCustomMetricRuleResponse>
```

`JSON` 格式

```
{
	"Message": "",
	"Code": "200",
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

