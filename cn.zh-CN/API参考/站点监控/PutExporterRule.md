# PutExporterRule

调用PutExporterRule接口创建或修改数据导出规则。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=PutExporterRule&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|PutExporterRule|要执行的操作，取值：PutExporterRule。 |
|RuleName|String|是|MyRuleName|规则名称。

 **说明：** 如果该规则名称与现有的名称重复，则表示修改，否则表示创建。 |
|Namespace|String|是|acs\_ecs\_dashboard|产品的数据命名空间。

 **说明：** 详情请参见[DescribeMetricMetaList](~~98846~~)或[云产品监控项](~~163515~~)。 |
|MetricName|String|是|cpu\_total|监控项名称。

 **说明：** 详情请参见[DescribeMetricMetaList](~~98846~~)或[云产品监控项](~~163515~~)。 |
|TargetWindows|String|是|60,300|导出数据的时间窗口。

 **说明：**

-   如果需要导出多个窗口，则使用英文逗号（,）分隔。
-   不支持导出小于60秒的数据。 |
|DstNames.N|RepeatList|是|distName1|数据导出的目的地。N的取值范围：1~20。 |
|Describe|String|否|导出CPU指标|导出规则描述。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|success|返回信息。当请求成功时，返回成功信息；当请求失败时，返回失败原因。 |
|RequestId|String|461CF2CD-2FC3-4B26-8645-7BD27E7D0F1D|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=PutExporterRule
&RuleName=MyRuleName
&Namespace=acs_ecs_dashboard
&MetricName=cpu_total
&TargetWindows=60,300
&DstNames.1=distName1
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<PutExporterRuleResponse>
		  <Message>success</Message>
		  <RequestId>8B524AE2-FBB1-4202-AA17-B3DEAAC8D861</RequestId>
		  <Code>200</Code>
		  <Success>true</Success>
</PutExporterRuleResponse>
```

`JSON` 格式

```
{
	"Message": "success",
	"RequestId": "8B524AE2-FBB1-4202-AA17-B3DEAAC8D861",
	"Code": "200",
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

