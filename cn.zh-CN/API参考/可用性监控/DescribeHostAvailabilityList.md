# DescribeHostAvailabilityList

调用DescribeHostAvailabilityList接口查询可用性监控任务列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeHostAvailabilityList&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeHostAvailabilityList|要执行的操作，取值：DescribeHostAvailabilityList。 |
|Id|Long|否|123456|可用性监控任务ID。 |
|TaskName|String|否|我的探测|可用性监控任务名称。 |
|PageNumber|Integer|否|1|页码。 |
|PageSize|Integer|否|10|每页记录条数。 |
|GroupId|Long|否|12345|应用分组ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|CE26797C-1094-47E6-B651-73AA888F5873|请求ID。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|TaskList|Array of NodeTaskConfig| |可用性监控任务列表。 |
|NodeTaskConfig| | | |
|AlertConfig|Struct| |报警规则配置。 |
|EndTime|Integer|23|报警生效的结束时间。取值范围：0~23。 |
|EscalationList|Array of escalationList| |报警触发条件。 |
|escalationList| | | |
|Aggregate|String|Value|报警统计方法。不同监控项的取值如下：

 -   HttpStatus：Value。
-   HttpLatency：Average。
-   TelnetStatus：Value。
-   TelnetLatency：Average。
-   PingLostRate：Average。 |
|MetricName|String|HttpStatus|报警监控项。取值：

 -   HttpStatus：HTTP状态码。
-   HttpLatency：HTTP等待时间。
-   TelnetStatus：TELNET状态码。
-   TelnetLatency：TELNET等待时间。
-   PingLostRate：PING丢包率。 |
|Operator|String|\>|报警规则比较符号。取值：

 -   `>`
-   `>=`
-   `<`
-   `<=`
-   `=` |
|Times|String|2|报警周期。即连续几个周期超过阈值。 |
|Value|String|99|报警阈值。 |
|NotifyType|Integer|1|报警通知类型。取值：

 -   2：电话+短信+邮件+钉钉机器人。
-   1：短信+邮件+钉钉机器人。
-   0：邮件+钉钉机器人。 |
|SilenceTime|Integer|86400|通道沉默时间。单位：秒。默认值：86400（1天）。 |
|StartTime|Integer|0|报警生效的起始时间。取值范围：0~23。 |
|WebHook|String|https://www.aliyun.com|URL回调地址。 |
|Disabled|Boolean|false|是否禁用。取值：

 -   true
-   false |
|GroupId|Long|12345|应用分组ID。 |
|GroupName|String|应用组名|应用分组名称。 |
|Id|Long|123|可用性监控任务ID。 |
|Instances|List|i-abcdefgh12\*\*\*\*|发起探测的ECS实例列表。 |
|TaskName|String|task1|可用性监控任务名称。 |
|TaskOption|Struct| |可用性监控任务的参数选项。 |
|HttpKeyword|String|ok|HTTP探测类型匹配响应内容。 |
|HttpMethod|String|GET|探测类型的方法。取值：

 -   GET
-   POST
-   HEAD |
|HttpNegative|Boolean|true|匹配HTTP响应内容的报警规则。取值：

 -   true：如果HTTP响应内容包含设置的报警规则，则报警。
-   false：如果HTTP响应内容不包含设置的报警规则，则报警。 |
|HttpPostContent|String|params1=paramsValue1|HTTP探测类型探测请求的Post内容。 |
|HttpResponseCharset|String|UTF-8|HTTP探测类型的响应字符集。 |
|HttpURI|String|https://www.aliyun.com|HTTP探测类型的探测URI地址。 |
|TelnetOrPingHost|String|ssh.aliyun.com|探测的域名或地址。 |
|TaskScope|String|GROUP|可用性监控任务的探测范围。取值：

 -   GROUP：表示当前应用分组内的所有ECS实例作为探测任务的探针。
-   GROUP\_SPEC\_INSTANCE：表示在应用分组内添加的实例作为探测任务的探针。设置该参数时，需要同时设置InstanceList（探测的ECS实例列表）。 |
|TaskType|String|HTTP|任务类型。取值：

 -   PING
-   TELNET
-   HTTP |
|Total|Integer|12|总记录条数。 |
|Message|String|The Request is not authorization.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeHostAvailabilityList
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeHostAvailabilityListResponse>
	  <RequestId>4A288E86-45C3-4858-9DB0-6D85B10BD92A</RequestId>
	  <Total>1</Total>
	  <TaskList>
		    <NodeTaskConfig>
			      <GroupName>Group_ECS</GroupName>
			      <TaskOption>
				        <HttpURI>https://aliyun.com</HttpURI>
				        <HttpMethod>HEAD</HttpMethod>
			      </TaskOption>
			      <AlertConfig>
				        <NotifyType>1</NotifyType>
				        <SilenceTime>86400</SilenceTime>
				        <EndTime>24</EndTime>
				        <StartTime>0</StartTime>
				        <EscalationList>
					          <escalationList>
						            <Operator>&gt;</Operator>
						            <MetricName>HttpStatus</MetricName>
						            <Times>3</Times>
						            <Value>400</Value>
						            <Aggregate>Value</Aggregate>
					          </escalationList>
					          <escalationList>
						            <Operator>&gt;</Operator>
						            <MetricName>HttpLatency</MetricName>
						            <Times>3</Times>
						            <Value>500</Value>
						            <Aggregate>Average</Aggregate>
					          </escalationList>
				        </EscalationList>
			      </AlertConfig>
			      <TaskName>ecs_instance</TaskName>
			      <TaskScope>GROUP</TaskScope>
			      <TaskType>HTTP</TaskType>
			      <Id>90****</Id>
			      <Disabled>false</Disabled>
			      <GroupId>7671****</GroupId>
		    </NodeTaskConfig>
	  </TaskList>
	  <Code>200</Code>
	  <Success>true</Success>
</DescribeHostAvailabilityListResponse>
```

`JSON` 格式

```
{
	"RequestId": "4A288E86-45C3-4858-9DB0-6D85B10BD92A",
	"Total": 1,
	"TaskList": {
		"NodeTaskConfig": [
			{
				"GroupName": "Group_ECS",
				"TaskOption": {
					"HttpURI": "https://aliyun.com",
					"HttpMethod": "HEAD"
				},
				"AlertConfig": {
					"NotifyType": 1,
					"SilenceTime": 86400,
					"EndTime": 24,
					"StartTime": 0,
					"EscalationList": {
						"escalationList": [
							{
								"Operator": ">",
								"MetricName": "HttpStatus",
								"Times": 3,
								"Value": "400",
								"Aggregate": "Value"
							},
							{
								"Operator": ">",
								"MetricName": "HttpLatency",
								"Times": 3,
								"Value": "500",
								"Aggregate": "Average"
							}
						]
					}
				},
				"TaskName": "ecs_instance",
				"TaskScope": "GROUP",
				"TaskType": "HTTP",
				"Id": "90****",
				"Disabled": false,
				"GroupId": "7671****"
			}
		]
	},
	"Code": 200,
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

