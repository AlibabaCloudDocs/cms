# DescribeAlertLogCount

调用DescribeAlertLogCount接口统计报警历史。

本文将提供一个示例，从云服务`product`维度查询ECS的报警统计历史。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeAlertLogCount&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAlertLogCount|要执行的操作，取值：DescribeAlertLogCount。 |
|GroupBy|String|是|product|对数据进行空间维度聚合，相当于SQL中的Group By。取值：

 -   `product`：按照云服务统计。
-   `level`：按照报警级别统计。
-   `groupId`：按照应用分组统计。
-   `contactGroup`：按照报警联系人组统计。
-   `product,metricName`：按照云服务和监控项统计。 |
|StartTime|Long|否|1609988009694|统计报警历史的开始时间戳。单位：毫秒。 |
|EndTime|Long|否|1610074409694|统计报警历史的结束时间戳。单位：毫秒。 |
|PageNumber|Integer|否|1|页码。默认值：1。 |
|PageSize|Integer|否|10|每页显示记录条数。默认值：10。 |
|SearchKey|String|否|test|统计报警历史的搜索关键字。 |
|Namespace|String|否|acs\_ecs\_dashboard|云服务的命名空间。

 **说明：** 关于云服务的命名空间，请参见[云服务监控项](~~163515~~)。 |
|GroupId|String|否|7301\*\*\*\*|应用分组ID。 |
|Product|String|否|ECS|云服务名称缩写。 |
|Level|String|否|P4|报警的级别和通知方式。取值：

 -   P2：电话+短信+邮件+钉钉机器人。
-   P3：短信+邮件+钉钉机器人。
-   P4：邮件+钉钉机器人。
-   OK：无报警。 |
|SendStatus|String|否|0|报警状态。取值：

 -   0：发生报警或报警恢复正常。
-   1：非生效期。
-   2：通道沉默周期。
-   3：主机重启中。
-   4：不发送报警。

 当报警状态为0时，如果Level的取值为P2、P3或P4，则发生告警；如果Level的取值为OK，则报警恢复正常。 |
|ContactGroup|String|否|ECS\_Group|报警联系人组。 |
|RuleName|String|否|test123|报警规则名称。 |
|MetricName|String|否|cpu\_total|监控项名称。

 **说明：** 关于云服务的监控项，请参见[云服务监控项](~~163515~~)。 |
|LastMin|String|否|360|获取日志的周期。单位：分钟。 |

关于公共请求参数的详情，请参见[公共参数](~~199331~~)。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|AlertLogCount|Array of AlertLogCount| |报警历史数量统计。 |
|Count|Integer|1|报警历史统计的数量。 |
|Logs|Array of Logs| |报警历史统计的数量详情。 |
|Name|String|product|报警历史统计的字段名称。 |
|Value|String|ECS|报警历史统计的字段值。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The specified resource is not found.|错误信息。 |
|RequestId|String|1C4A3709-BF52-42EE-87B5-7435F0929585|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeAlertLogCount
&GroupBy=product
&Product=ECS
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<DescribeAlertLogCountResponse>
	  <RequestId>0BA67F6D-B699-4E3F-B205-93A5C38A0A2E</RequestId>
	  <AlertLogCount>
		    <Count>1</Count>
		    <Logs>
			      <Value>ECS</Value>
			      <Name>product</Name>
		    </Logs>
	  </AlertLogCount>
	  <Code>200</Code>
	  <Success>true</Success>
</DescribeAlertLogCountResponse>
```

`JSON`格式

```
{
	"RequestId": "0BA67F6D-B699-4E3F-B205-93A5C38A0A2E",
	"AlertLogCount": [
		{
			"Count": 1,
			"Logs": [
				{
					"Value": "ECS",
					"Name": "product"
				}
			]
		}
	],
	"Code": 200,
	"Success": true
}
```

## 错误码

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|ResourceNotFound|The specified resource is not found.|未找到指定资源。|

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

