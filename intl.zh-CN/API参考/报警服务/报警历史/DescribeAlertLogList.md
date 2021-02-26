# DescribeAlertLogList

调用DescribeAlertLogList接口查询报警历史。

本文将提供一个示例，从云服务`product`维度查询ECS的报警历史。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeAlertLogList&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAlertLogList|要执行的操作，取值：DescribeAlertLogList。 |
|StartTime|Long|否|1609988009694|查询报警历史的开始时间戳。单位：毫秒。 |
|EndTime|Long|否|1610074409694|查询报警历史的结束时间戳。单位：毫秒。 |
|PageNumber|Integer|否|1|页码。默认值：1。 |
|PageSize|Integer|否|10|分页大小。默认值：10。 |
|SearchKey|String|否|alert|查询报警历史的搜索关键字。 |
|GroupId|String|否|7301\*\*\*\*|应用分组ID。 |
|Namespace|String|否|acs\_ecs\_dashboard|云服务的命名空间。

 **说明：** 关于云服务的命名空间，请参见[云服务监控项](~~163515~~)。 |
|Product|String|否|ECS|云服务名称缩写。 |
|Level|String|否|P4|报警的级别和通知方式。取值：

 -   P4：邮件+钉钉机器人。
-   OK：无报警。 |
|SendStatus|String|否|0|报警状态。取值：

 -   0：发生报警或报警恢复正常。
-   1：非生效期。
-   2：通道沉默周期。
-   3：主机重启中。
-   4：不发送报警。

 当报警状态为0时，如果Level的取值为P4，则发生告警；如果Level的取值为OK，则报警恢复正常。 |
|ContactGroup|String|否|ECS\_Group|报警联系人组。 |
|RuleName|String|否|test123|报警规则名称。 |
|MetricName|String|否|IntranetInRate|监控项名称。

 **说明：** 关于云服务的监控项，请参见[云服务监控项](~~163515~~)。 |
|LastMin|String|否|360|获取日志的周期。单位：分钟。 |
|GroupBy|String|否|product|对数据进行空间维度聚合，相当于SQL中的Group By。取值：

 -   `product`：按照云服务统计。
-   `level`：按照报警级别统计。
-   `groupId`：按照应用分组统计。
-   `contactGroup`：按照报警联系人组统计。
-   `product,metricName`：按照云服务和监控项统计。 |

关于公共请求参数的详情，请参见[公共参数](~~199331~~)。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|AlertLogList|Array of Alarm| |报警历史列表。 |
|AlertTime|String|1610043776621|发生报警的时间戳。单位：毫秒。 |
|ContactALIIWWList|List|Alice|报警联系人的旺旺列表。

 **说明：** 该参数仅适用于中国站。 |
|ContactDingList|List|CloudMonitor|报警联系人的钉钉列表。 |
|ContactGroups|List|ECS\_Group|报警联系人组。 |
|ContactMailList|List|alice@example.com|报警联系人的邮件列表。 |
|ContactOnCallList|List|1368888\*\*\*\*|报警联系人的电话通知列表。

 **说明：** 该参数仅适用于中国站。 |
|ContactSMSList|List|1368888\*\*\*\*|报警联系人的短信通知列表。

 **说明：** 该参数仅适用于中国站。 |
|Dimensions|Array of Dimensions| |报警资源的维度。 |
|Key|String|instanceId|报警资源的Key。 |
|Value|String|i-m5e1qg6uo38rztr4\*\*\*\*|报警资源的Value。 |
|DingdingWebhookList|List|https://oapi.dingtalk.com/robot/send?access\_token=b7ff24032da1a5f86659ecda46797e13cc1d4e4da6903d7b014ea1d1488b\*\*\*\*|报警联系人的Webhook地址列表。 |
|Escalation|Struct| |触发报警的规则。 |
|Expression|String|$Average<90|触发报警的规则描述。

 **说明：** 报警规则的主体，当监控数据满足报警条件时，触发报警规则。 |
|Level|String|P4|报警的级别和通知方式。取值：

 -   P4：邮件+钉钉机器人。
-   OK：无报警。 |
|Times|Integer|1|报警重试次数。 |
|EventName|String|IOHang|事件名称。 |
|ExtendedInfo|Array of ExtInfo| |报警的扩展信息。 |
|Name|String|userId|扩展字段名称。 |
|Value|String|12706\*\*\*\*|扩展字段值。 |
|GroupId|String|7301\*\*\*\*|应用分组ID。 |
|GroupName|String|ECS\_Instances|应用分组名称。 |
|InstanceId|String|i-m5e1qg6uo38rztr4\*\*\*\*|资源ID。 |
|InstanceName|String|portalHost|资源名称。 |
|Level|String|P4|报警的级别和通知方式。取值：

 -   P4：邮件+钉钉机器人。
-   OK：无报警。 |
|LevelChange|String|P4-\>OK|报警级别的变更。取值：

 -   `P4->OK`：由P4级别报警到报警恢复。
-   `P4->P4`：P4级别报警。 |
|Message|String|\{"alertName":"e47aa0ac-4076-44db-a47d-d1083968\*\*\*\*\_Availability"\}|报警相关信息，为一个JSON串。 |
|MetricName|String|cpu\_total|监控项名称。 |
|Namespace|String|acs\_ecs\_dashboard|云服务的命名空间。 |
|Product|String|ECS|云服务标识。取值：

 -   如果是阿里云服务，则为云服务名称缩写，例如：ECS。
-   如果非阿里云服务，则为`acs_服务关键字`，例如：acs\_networkmonitor。 |
|RuleId|String|d582b9e9-b1c1-4f17-9279-0fe7333a\*\*\*\*\_ResponseTime|报警规则ID。 |
|RuleName|String|CPU使用率|报警规则名称。 |
|SendStatus|String|0|报警状态。取值：

 -   0：发生报警或报警恢复正常。
-   1：非生效期。
-   2：通道沉默周期。
-   3：主机重启中。
-   4：不发送报警。

 当报警状态为0时，如果Level的取值为P4，则发生告警；如果Level的取值为OK，则报警恢复正常。 |
|WebhookList|List|https://www.aliyun.com|报警触发的URL回调地址列表。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The specified resource is not found.|错误信息。 |
|PageNumber|Integer|1|页码。 |
|PageSize|Integer|10|每页显示记录条数。 |
|RequestId|String|1C4A3709-BF52-42EE-87B5-7435F0929585|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Total|Integer|88|总记录条数。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAlertLogList
&Product=ECS
&GroupBy=product
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<DescribeAlertLogListResponse>
	  <AlertLogList>
		    <GroupName></GroupName>
		    <Message>{\"alertName\":\"d582b9e9-b1c1-4f17-9279-0fe7333a****_ResponseTime\",\"curLevel\":\"OK\",\"dimensions\":{\"taskId\":\"d582b9e9-b1c1-4f17-9279-0fe7333a****\",\"userId\":\"127067667954****\"},\"escalation\":{\"expression\":\"$Average&gt;=800\",\"level\":P4,\"tag\":\"P4\",\"times\":1}</Message>
		    <RuleId>d582b9e9-b1c1-4f17-9279-0fe7****_ResponseTime</RuleId>
		    <Escalation>
			      <Expression>$Average&gt;=800</Expression>
			      <Times>1</Times>
			      <Level>P4</Level>
		    </Escalation>
		    <SendStatus>0</SendStatus>
		    <Product>acs_ecs_dashboard</Product>
		    <MetricName>cpu_total</MetricName>
		    <RuleName>CPU使用率</RuleName>
		    <ContactGroups>ECS_Group</ContactGroups>
		    <InstanceId></InstanceId>
		    <LevelChange>P4-&gt;OK</LevelChange>
		    <Dimensions>
			      <Value>127067667954****</Value>
			      <Key>userId</Key>
		    </Dimensions>
		    <Dimensions>
			      <Value>i-abcdefgh12****</Value>
			      <Key>instanceId</Key>
		    </Dimensions>
		    <EventName>AlertOk</EventName>
		    <ExtendedInfo>
			      <Value>i-hp34y1eiszazu49y****</Value>
			      <Name>instanceId</Name>
		    </ExtendedInfo>
		    <ExtendedInfo>
			      <Value>12706****</Value>
			      <Name>userId</Name>
		    </ExtendedInfo>
		    <Namespace>acs_ecs_dashboard</Namespace>
		    <AlertTime>1610085521564</AlertTime>
		    <GroupId>7301****</GroupId>
		    <InstanceName>portalHost</InstanceName>
		    <Level>OK</Level>
	  </AlertLogList>
	  <RequestId>6FCB1AB7-57F7-4DDA-B14E-6468FAFE79D9</RequestId>
	  <PageSize>10</PageSize>
	  <PageNumber>1</PageNumber>
	  <Code>200</Code>
	  <Success>true</Success>
</DescribeAlertLogListResponse>
```

`JSON`格式

```
{
	"AlertLogList": [
		{
			"GroupName": "",
			"ContactALIIWWList": [],
			"Message": "{\"alertName\":\"d582b9e9-b1c1-4f17-9279-0fe7333a****_ResponseTime\",\"curLevel\":\"OK\",\"dimensions\":{\"taskId\":\"d582b9e9-b1c1-4f17-9279-0fe7333a****\",\"userId\":\"127067667954****\"},\"escalation\":{\"expression\":\"$Average>=800\",\"level\":P4,\"tag\":\"P4\",\"times\":1}",
			"RuleId": "d582b9e9-b1c1-4f17-9279-0f****_ResponseTime",
			"Escalation": {
				"Expression": "$Average>=800",
				"Times": 1,
				"Level": "P4"
			},
			"SendStatus": "0",
			"Product": "acs_ecs_dashboard",
			"MetricName": "cpu_total",
			"ContactSMSList": [],
			"RuleName": "CPU使用率",
			"ContactGroups": [
				"ECS_Group"
			],
			"DingdingWebhookList": [],
			"InstanceId": "",
			"LevelChange": "P4->OK",
			"Dimensions": [
				{
					"Value": "127067667954****",
					"Key": "userId"
				},
				{
					"Value": "i-abcdefgh12****",
					"Key": "instanceId"
				}
			],
			"ContactOnCallList": [],
			"ContactDingList": [],
			"EventName": "AlertOk",
			"ExtendedInfo": [
				{
					"Value": "i-hp34y1eiszazu49y****",
					"Name": "instanceId"
				},
				{
					"Value": "12706****",
					"Name": "userId"
				}
			],
			"Namespace": "acs_ecs_dashboard",
			"AlertTime": 1610085521564,
			"GroupId": "7301****",
			"InstanceName": "portalHost",
			"WebhookList": [],
			"ContactMailList": [],
			"Level": "OK"
		}
	],
	"RequestId": "6FCB1AB7-57F7-4DDA-B14E-6468FAFE79D9",
	"PageSize": 10,
	"PageNumber": 1,
	"Code": 200,
	"Success": true
}
```

## 错误码

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|ResourceNotFound|The specified resource is not found.|未找到指定资源。|

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

