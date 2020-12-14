# PutCustomEventRule

调用PutCustomEventRule接口创建自定义事件报警规则。

调用本接口前，请先调用PutCustomEvent接口上报自定义事件的监控数据，详情请参见[PutCustomEvent](~~115012~~)。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=PutCustomEventRule&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|PutCustomEventRule|要执行的操作，取值：PutCustomEventRule。 |
|ContactGroups|String|是|ECS\_Group|报警联系人组。多个联系人组之间用英文逗号（,）分隔。 |
|EventName|String|是|HostDown|自定义事件名称。获取方法请参见[DescribeCustomEventAttribute](~~115262~~)。 |
|GroupId|String|是|7378\*\*\*\*|应用分组ID。获取方法请参见[DescribeCustomEventAttribute](~~115262~~)。

 **说明：** 0表示上报的自定义事件不属于任何一个应用分组。 |
|Level|String|是|CRITICAL|报警级别。取值：

 -   CRITICAL：严重。
-   WARN：警告。
-   INFO：信息。 |
|RuleId|String|是|CustomRuleId1|报警规则ID。

 **说明：** 如果报警规则ID已存在，则表示修改报警规则；如果报警规则ID不存在，则表示创建报警规则。 |
|RuleName|String|是|CustomeRule|报警规则名称。 |
|Threshold|String|是|99|报警阈值。 |
|Webhook|String|否|https://www.aliyun.com|报警发生回调时指定的URL地址，向URL发送POST请求。 |
|EffectiveInterval|String|否|00:00-23:59|报警规则生效的时间范围。取值范围：00:00-23:59。 |
|Period|String|否|60|自定义事件监控数据的聚合周期。单位：秒。取值为60或60的整数倍。默认值：300。 |
|EmailSubject|String|否|ECS实例|报警邮件主题。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The request has failed due to a temporary failure of the server.|错误信息。 |
|RequestId|String|AD5DCD82-BD1C-405F-BAED-32302DE9F498|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=PutCustomEventRule
&ContactGroups=ECS_Group
&EventName=HostDown
&GroupId=7378****
&Level=CRITICAL
&RuleId=CustomRuleId1
&RuleName=CustomeRule
&Threshold=99
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<PutCustomEventRuleResponse>
	  <RequestId>AD5DCD82-BD1C-405F-BAED-32302DE9F498</RequestId>
	  <Code>200</Code>
	  <Success>true</Success>
</PutCustomEventRuleResponse>
```

`JSON` 格式

```
{
	"RequestId": "AD5DCD82-BD1C-405F-BAED-32302DE9F498",
	"Code": "200",
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

