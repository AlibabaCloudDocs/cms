# DescribeExporterRuleList

调用DescribeExporterRuleList接口查询数据导出规则列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeExporterRuleList&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeExporterRuleList|要执行的操作，取值：**DescribeExporterRuleList**。 |
|PageNumber|Integer|否|1|分页码，默认为1。 |
|PageSize|Integer|否|1000|每页显示记录条数，默认为1000。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Total|Integer|1000|总记录条数。 |
|Code|String|200|状态码。

 **说明：** 状态码为200表示成功，其余取值表示失败。 |
|Success|Boolean|true|是否成功，取值：

 -   `true`：成功
-   `false`：失败 |
|RequestId|String|6BA047CA-8BC6-40BC-BC8F-FBECF35F1993|请求ID。 |
|Message|String|susscess|返回信息。 |
|Datapoints|Array| |输出的规则列表。 |
|Datapoint| | | |
|CreateTime|Long|1584024616228|创建的时间， 为unix时间戳。 |
|Describe|String|监控数据导出|规则描述信息。 |
|Dimension|String|\{"instanceId":"xxxxx"\}|关联的维度。 |
|DstName|List|exporter1|导出目的地。 |
|Enabled|Boolean|true|是否启用。 |
|MetricName|String|cpu\_total|监控项名称。

 **说明：** 详情请参见[DescribeMetricMetaList](~~98846~~)或[预设监控项参考](~~28619~~)。 |
|Namespace|String|acs\_ecs\_dashboard|产品的数据命名空间。

 **说明：** 详情请参见[DescribeMetricMetaList](~~98846~~)或[预设监控项参考](~~28619~~)。 |
|RuleName|String|myRuleName|导出规则名。 |
|TargetWindows|String|60,300|导出数据的时间窗口。

 如果要导出多个窗口，使用逗号分隔。

 **说明：** 不支持小于60秒数据的导出。 |
|PageNumber|Integer|1|当前页码。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeExporterRuleList
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>6BA047CA-8BC6-40BC-BC8F-FBECF35F1993</RequestId>
<PageNumber>1</PageNumber>
<Total>1</Total>
<Datapoints>
    <Datapoint>
        <TargetWindows>60,300</TargetWindows>
        <Describe/>
        <MetricName>cpu_total</MetricName>
        <CreateTime>1584024616228</CreateTime>
        <Enabled>false</Enabled>
        <Dimension>{'userId': '177******'}</Dimension>
        <DstName>
            <DstName>exporter1</DstName>
        </DstName>
        <RuleName>exporterRule1</RuleName>
        <Namespace>acs_ecs_dashboard</Namespace>
        <dstNames/>
    </Datapoint>
</Datapoints>
<Code>200</Code>
<Success>true</Success>
```

`JSON` 格式

```
{
	"RequestId": "6BA047CA-8BC6-40BC-BC8F-FBECF35F1993",
	"PageNumber": 1,
	"Total": 1,
	"Datapoints": {
		"Datapoint": [
			{
				"TargetWindows": "60,300",
				"Describe": "",
				"MetricName": "cpu_total",
				"CreateTime": 1584024616228,
				"Enabled": false,
				"Dimension": "{'userId': '177******'}",
				"DstName": {
					"DstName": [
						"exporter1"
					]
				},
				"RuleName": "exporterRule1",
				"Namespace": "acs_ecs_dashboard",
				"dstNames": ""
			}
		]
	},
	"Code": "200",
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

