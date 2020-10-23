# DescribeAlertingMetricRuleResources

调用DescribeAlertingMetricRuleResources接口查询指定报警规则下报警的资源。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeAlertingMetricRuleResources&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAlertingMetricRuleResources|要执行的操作，取值：DescribeAlertingMetricRuleResources。 |
|RuleId|String|否|alerRuleId\*\*\*\*|报警规则ID。

 **说明：** GroupId和RuleId至少需要填写一个。如果两个参数都填写，则查询时需同时满足。 |
|GroupId|String|否|123456|应用分组ID。 |
|Page|Integer|否|1|分页页码。 默认值：1 。 |
|PageSize|Integer|否|10|分页大小。默认值：10。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|9B868619-77B4-4623-AD64-6181EA7CF8FA|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Code|Integer|200|状态码。

 **说明：** 200表示成功。 |
|Total|Integer|1|总记录条数。 |
|Resources|Array of Resource| |报警规则的资源列表。 |
|Resource| | | |
|Enable|String|true|报警规则是否启用。取值：

 -   true：是。
-   false：否。 |
|GroupId|String|123456|应用分组ID。

 **说明：** 如果报警规则与指定应用分组关联，则显示该应用分组ID。 |
|LastAlertTime|String|1603159271000|最后一次触发报警的时间。

 格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |
|LastModifyTime|String|1603159271000|最后一次修改报警规则的时间。

 格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |
|MetricValues|String|\{\\"Maximum\\":3000.25,\\"Average\\":3000.25,\\"timestamp\\":1603159200000,\\"userId\\":\\"120886317861\*\*\*\*\\",\\"taskId\\":\\"87\*\*\*\*\\",\\"instanceId\\":\\"i-hp3aazrjdvrl41ar\*\*\*\*\\"\}|触发报警时监控项的值。格式为一个JSON字符串。 |
|Resource|String|userId=120886317861\*\*\*\*,taskId=87\*\*\*\*,instanceId=i-hp3aazrjdvrl41ar\*\*\*\*|报警的资源。 |
|RetryTimes|String|3|重试次数。 |
|RuleId|String|detect\_87\*\*\*\*\_HTTP\_HttpLatency|报警规则ID。 |
|RuleName|String|test123-HttpLatency.Average|报警规则名称。 |
|StartTime|String|1603159211000|资源被关联到报警规则的时间。

 格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |
|Threshold|String|500|报警阈值。 |
|Message|String|The Request is not authorization.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAlertingMetricRuleResources
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeAlertingMetricRuleResourcesResponse>
	  <RequestId>382001F9-A2E7-4511-8B79-75352ABA42F5</RequestId>
	  <Total>2</Total>
	  <Resources>
		    <Resource>
			      <LastAlertTime>1603159271000</LastAlertTime>
			      <RuleId>detect_87****_HTTP_HttpLatency</RuleId>
			      <Resource>userId=120886317861****,taskId=87****,instanceId=i-hp3aazrjdvrl41ar****</Resource>
			      <StartTime>1603159211000</StartTime>
			      <Enable>true</Enable>
			      <MetricValues>{\"Maximum\":3000.25,\"Average\":3000.25,\"timestamp\":1603159200000,\"userId\":\"120886317861****\",\"taskId\":\"87****\",\"instanceId\":\"i-hp3aazrjdvrl41ar****\"}</MetricValues>
			      <LastModifyTime>1603159271000</LastModifyTime>
			      <RuleName>test123-HttpLatency.Average</RuleName>
			      <RetryTimes>3</RetryTimes>
			      <GroupId>6745****</GroupId>
			      <Threshold>500</Threshold>
		    </Resource>
		    <Resource>
			      <LastAlertTime>1603159271000</LastAlertTime>
			      <RuleId>detect_87****_HTTP_HttpLatency</RuleId>
			      <Resource>userId=120886317861****,taskId=87****,instanceId=i-m5e1qg6uo38rztr4****</Resource>
			      <StartTime>1603159211000</StartTime>
			      <Enable>true</Enable>
			      <MetricValues>{\"Maximum\":3000.99,\"Average\":3000.99,\"timestamp\":1603159200000,\"userId\":\"120886317861****\",\"taskId\":\"87****\",\"instanceId\":\"i-m5e1qg6uo38rztr4****\"}</MetricValues>
			      <LastModifyTime>1603159271000</LastModifyTime>
			      <RuleName>test123-HttpLatency.Average</RuleName>
			      <RetryTimes>3</RetryTimes>
			      <GroupId>6745****</GroupId>
			      <Threshold>500</Threshold>
		    </Resource>
	  </Resources>
	  <Success>true</Success>
</DescribeAlertingMetricRuleResourcesResponse>
```

`JSON` 格式

```
{
	"RequestId": "382001F9-A2E7-4511-8B79-75352ABA42F5",
	"Total": 2,
	"Resources": {
		"Resource": [
			{
				"LastAlertTime": 1603159271000,
				"RuleId": "detect_87****_HTTP_HttpLatency",
				"Resource": "userId=120886317861****,taskId=87****,instanceId=i-hp3aazrjdvrl41ar****",
				"StartTime": 1603159211000,
				"Enable": true,
				"MetricValues": "{\"Maximum\":3000.25,\"Average\":3000.25,\"timestamp\":1603159200000,\"userId\":\"120886317861****\",\"taskId\":\"87****\",\"instanceId\":\"i-hp3aazrjdvrl41ar****\"}",
				"LastModifyTime": 1603159271000,
				"RuleName": "test123-HttpLatency.Average",
				"RetryTimes": 3,
				"GroupId": "6745****",
				"Threshold": "500"
			},
			{
				"LastAlertTime": 1603159271000,
				"RuleId": "detect_87****_HTTP_HttpLatency",
				"Resource": "userId=120886317861****,taskId=87****,instanceId=i-m5e1qg6uo38rztr4****",
				"StartTime": 1603159211000,
				"Enable": true,
				"MetricValues": "{\"Maximum\":3000.99,\"Average\":3000.99,\"timestamp\":1603159200000,\"userId\":\"120886317861****\",\"taskId\":\"87****\",\"instanceId\":\"i-m5e1qg6uo38rztr4****\"}",
				"LastModifyTime": 1603159271000,
				"RuleName": "test123-HttpLatency.Average",
				"RetryTimes": 3,
				"GroupId": "6745****",
				"Threshold": "500"
			}
		]
	},
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

