# ApplyMetricRuleTemplate

调用ApplyMetricRuleTemplate接口将报警模板应用到应用分组并生成报警规则。

本文将提供一个示例，将报警模板`700****`应用到应用分组`123456`，生成报警规则的ID为`applyTemplate8ab74c6b-9f27-47ab-8841-de01dc08****`，名称为`test123`。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=ApplyMetricRuleTemplate&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ApplyMetricRuleTemplate|要执行的操作，取值：ApplyMetricRuleTemplate。 |
|GroupId|Long|是|123456|应用分组ID。 |
|TemplateIds|String|是|700\*\*\*\*|报警模板ID。 |
|SilenceTime|Long|否|86400|通道沉默周期。单位：秒。默认值：86400。

 **说明：** 当监控数据持续超过报警规则阈值时，每个沉默周期内只发送一次报警通知。 |
|EnableStartTime|Long|否|00|报警生效的开始时间。取值范围：00~23，表示00:00到23:00。 |
|EnableEndTime|Long|否|23|报警生效的结束时间。取值范围：00~23，表示00:59到23:59。 |
|NotifyLevel|Long|否|4|报警通知方式。取值：

 -   2：电话+短信+邮箱+旺旺+钉钉机器人。
-   3：短信+邮箱+旺旺+钉钉机器人。
-   4：旺旺+钉钉机器人。 |
|ApplyMode|String|否|GROUP\_INSTANCE\_FIRST|模板应用方式。取值：

 -   GROUP\_INSTANCE\_FIRST：应用分组实例优先。应用报警模板时，以应用分组实例优先，如果应用分组中不存在该实例，则忽略模板中的规则。
-   ALARM\_TEMPLATE\_FIRST：报警模板实例优先。应用报警模板时，不管应用分组中是否存在该实例，都创建报警规则。 |
|Webhook|String|否|https://www.aliyun.com|报警发生时会回调指定的URL地址并发送POST请求。 |

关于公共请求参数的详情，请参见[公共参数](~~199331~~)。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|Integer|200|状态码。

 **说明：** 200表示成功。 |
|RequestId|String|3F897F3C-020A-4993-95B4-63ABB84F83E6|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Resource|Struct| |报警规则影响的资源。 |
|AlertResults|Array of Result| |生成报警规则的详细结果。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|alert rule is creating, please wait a few minutes.|返回信息。 |
|RuleId|String|applyTemplate8ab74c6b-9f27-47ab-8841-de01dc08\*\*\*\*|报警规则ID。 |
|RuleName|String|test123|报警规则名称。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|GroupId|Long|123456|应用分组ID。 |
|Message|String|The specified resource is not found.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ApplyMetricRuleTemplate
&GroupId=123456
&TemplateIds=700****
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<ApplyMetricRuleTemplateResponse>
	  <RequestId>37D4037E-827E-4E66-87DF-F56A22F2884D</RequestId>
	  <Resource>
		    <GroupId>7756****</GroupId>
		    <AlertResults>
			      <Message>alert rule is creating, please wait a few minutes.</Message>
			      <RuleId>applyTemplate8ab74c6b-9f27-47ab-8841-de01dc08****</RuleId>
			      <Code>202</Code>
			      <RuleName>test123</RuleName>
			      <Success>true</Success>
		    </AlertResults>
	  </Resource>
	  <Code>200</Code>
	  <Success>true</Success>
</ApplyMetricRuleTemplateResponse>
```

`JSON`格式

```
{
	"RequestId": "37D4037E-827E-4E66-87DF-F56A22F2884D",
	"Resource": {
		"GroupId": "7756****",
		"AlertResults": [
			{
				"Message": "alert rule is creating, please wait a few minutes.",
				"RuleId": "applyTemplate8ab74c6b-9f27-47ab-8841-de01dc08****",
				"Code": 202,
				"RuleName": "test123",
				"Success": true
			}
		]
	},
	"Code": 200,
	"Success": true
}
```

## 错误码

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|ResourceNotFound|The specified resource is not found.|未找到指定资源。|

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

