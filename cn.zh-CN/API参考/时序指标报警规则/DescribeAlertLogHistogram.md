# DescribeAlertLogHistogram

调用DescribeAlertLogHistogram接口查询报警历史的直方图列表。

本文将提供一个示例，从云服务`product`维度查询ECS报警历史的直方图列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeAlertLogHistogram&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAlertLogHistogram|要执行的操作，取值：DescribeAlertLogHistogram。 |
|StartTime|Long|否|1609988009694|查询报警历史的开始时间戳。单位：毫秒。 |
|EndTime|Long|否|1609989009694|查询报警历史的结束时间戳。单位：毫秒。 |
|PageNumber|Integer|否|1|页码。默认值：1。 |
|PageSize|Integer|否|10|每页显示记录条数。默认值：10。 |
|SearchKey|String|否|alert|查询报警历史的搜索关键字。 |
|GroupId|String|否|7301\*\*\*\*|应用分组ID。 |
|Product|String|否|ECS|云服务名称缩写。 |
|Namespace|String|否|acs\_ecs\_dashboard|云服务的命名空间。

 **说明：** 关于云服务的命名空间，请参见[云服务监控项](~~163515~~)。 |
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
|AlertLogHistogramList|Array of AlertLogHistogramList| |查询报警历史的直方图列表。 |
|Count|Integer|20|报警历史的数量。 |
|From|Long|1610074791|查询报警历史的开始时间戳。单位：秒。 |
|To|Long|1610074800|查询报警历史的结束时间戳。单位：秒。 |
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
http(s)://[Endpoint]/?Action=DescribeAlertLogHistogram
&Product=ECS
&GroupBy=product
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<DescribeAlertLogHistogramResponse>
	  <RequestId>6DCB654A-4002-4977-A2E1-F58F85E7143D</RequestId>
	  <AlertLogHistogramList>
		    <Count>0</Count>
		    <From>1610074791</From>
		    <To>1610074800</To>
	  </AlertLogHistogramList>
	  <AlertLogHistogramList>
		    <Count>0</Count>
		    <From>1610074800</From>
		    <To>1610074830</To>
	  </AlertLogHistogramList>
	  <AlertLogHistogramList>
		    <Count>1</Count>
		    <From>1610074830</From>
		    <To>1610074860</To>
	  </AlertLogHistogramList>
	  <AlertLogHistogramList>
		    <Count>0</Count>
		    <From>1610074860</From>
		    <To>1610074890</To>
	  </AlertLogHistogramList>
	  <AlertLogHistogramList>
		    <Count>0</Count>
		    <From>1610074890</From>
		    <To>1610074920</To>
	  </AlertLogHistogramList>
	  <AlertLogHistogramList>
		    <Count>1</Count>
		    <From>1610074920</From>
		    <To>1610074950</To>
	  </AlertLogHistogramList>
	  <AlertLogHistogramList>
		    <Count>0</Count>
		    <From>1610074950</From>
		    <To>1610074980</To>
	  </AlertLogHistogramList>
	  <AlertLogHistogramList>
		    <Count>0</Count>
		    <From>1610074980</From>
		    <To>1610075010</To>
	  </AlertLogHistogramList>
	  <AlertLogHistogramList>
		    <Count>0</Count>
		    <From>1610075010</From>
		    <To>1610075040</To>
	  </AlertLogHistogramList>
	  <Code>200</Code>
	  <Success>true</Success>
</DescribeAlertLogHistogramResponse>
```

`JSON`格式

```
{
	"RequestId": "6DCB654A-4002-4977-A2E1-F58F85E7143D",
	"AlertLogHistogramList": [
		{
			"Count": 0,
			"From": 1610074791,
			"To": 1610074800
		},
		{
			"Count": 0,
			"From": 1610074800,
			"To": 1610074830
		},
		{
			"Count": 1,
			"From": 1610074830,
			"To": 1610074860
		},
		{
			"Count": 0,
			"From": 1610074860,
			"To": 1610074890
		},
		{
			"Count": 0,
			"From": 1610074890,
			"To": 1610074920
		},
		{
			"Count": 1,
			"From": 1610074920,
			"To": 1610074950
		},
		{
			"Count": 0,
			"From": 1610074950,
			"To": 1610074980
		},
		{
			"Count": 0,
			"From": 1610074980,
			"To": 1610075010
		},
		{
			"Count": 0,
			"From": 1610075010,
			"To": 1610075040
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

