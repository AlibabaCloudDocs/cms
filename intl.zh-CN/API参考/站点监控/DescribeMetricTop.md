# DescribeMetricTop

调用DescribeMetricTop接口查询排序后的指定云服务时序指标的监控数据。

**说明：** 云服务Namespace、Orderby、Project、Metric、Period、Dimensions等参数的取值，请参见[DescribeMetricMetaList](~~98846~~)或[云服务监控项](~~163515~~)。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeMetricTop&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeMetricTop|要执行的操作，取值：DescribeMetricTop。 |
|MetricName|String|是|cpu\_idle|监控项名称。 |
|Namespace|String|是|acs\_ecs\_dashboard|云服务的数据命名空间。命名方式：acs\_产品名。 |
|Orderby|String|是|Average|排序字段，即按该排序字段进行排序。 |
|Period|String|否|60|时间间隔，单位：秒。取值：60、300、900。

 请根据您的实际需求设置该参数。例如：

 -   当Period设置为60时，如果实际存在1440条数据，则只返回1000条数据。
-   当Period设置为300时，如果实际存在288条数据，则返回288条数据。

 **说明：** 由于最大返回值不超过1000条数据，因此当其超过1000条数据时，只返回前1000条。 |
|StartTime|String|否|2019-01-30 00:00:00|开始时间。支持的格式：

 -   Unix时间戳：从1970年1月1日开始所经过的毫秒数。
-   Format格式：YYYY-MM-DDThh:mm:ssZ。

 **说明：** 开始和结束时间执行的是左开右闭的模式，StartTime不能等于或大于EndTime。 |
|EndTime|String|否|2019-01-30 00:10:00|结束时间。支持的格式：

 -   Unix时间戳：从1970年1月1日开始所经过的毫秒数。
-   Format格式：YYYY-MM-DDThh:mm:ssZ。 |
|Dimensions|String|否|\[\{"instanceId": "i-abcdefgh12\*\*\*\*"\}\]|维度Map，用于查询指定资源的监控数据。

 格式：key-value键值对形式的集合，常用的key-value集合为`instanceId:i-2ze2d6j5uhg20x47****`。

 **说明：** Dimensions传入时需要使用JSON字符串表示该Map对象，必须按顺序传入。 |
|OrderDesc|String|否|False|排序方式。取值：

 -   True：由小到大排序。
-   False：由大到小排序。 |
|Length|String|否|1000|每页显示的记录条数。用于分页查询，默认值：1000。 |
|Express|String|否|\{"groupby":\["userId","instanceId"\]\}|对查询出的现有结果进行实时计算的表达式。

 目前仅支持`groupby`（类似数据库的groupby语句）。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|3121AE7D-4AFF-4C25-8F1D-C8226EBB1F42|请求ID。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Datapoints|String|\[\{"timestamp":1548777660000,"userId":"123","instanceId":"i-abc","Minimum":9.92,"Average":9.92,"Maximum":9.92,"\_count":1\}\]|监控数据列表。 |
|Period|String|60|时间间隔。单位：秒。取值：60、300、900。 |
|Message|String|The Request is not authorization.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeMetricTop
&MetricName=cpu_idle
&Namespace=acs_ecs_dashboard
&Orderby=Average
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeMetricTopResponse>
	  <Period>60</Period>
	  <Datapoints>
		    <order>1</order>
		    <timestamp>1551687360000</timestamp>
		    <userId>12345****</userId>
		    <instanceId>i-2zeehst1****</instanceId>
		    <Maximum>16.41</Maximum>
		    <Minimum>4.66</Minimum>
		    <Average>7.74</Average>
		    <_count>1</_count>
	  </Datapoints>
	  <Datapoints>
		    <order>2</order>
		    <timestamp>1551687360000</timestamp>
		    <userId>12345****</userId>
		    <instanceId>i-2zefxdy2****</instanceId>
		    <Maximum>15.74</Maximum>
		    <Minimum>5.03</Minimum>
		    <Average>7.14</Average>
		    <_count>1</_count>
	  </Datapoints>
	  <RequestId>1F68A4E8-4488-48E7-9189-3E1F5165E64E</RequestId>
	  <Code>200</Code>
</DescribeMetricTopResponse>
```

`JSON` 格式

```
{
    "Period": "60",
    "Datapoints": [
        {
            "order": 1,
            "timestamp": 1551687360000,
            "userId": "12345****",
            "instanceId": "i-2zeehst1****",
            "Maximum": 16.41,
            "Minimum": 4.66,
            "Average": 7.74,
            "_count": 1
        },
        {
            "order": 2,
            "timestamp": 1551687360000,
            "userId": "12345****",
            "instanceId": "i-2zefxdy2****",
            "Maximum": 15.74,
            "Minimum": 5.03,
            "Average": 7.14,
            "_count": 1
        }
    ],
    "RequestId": "1F68A4E8-4488-48E7-9189-3E1F5165E64E",
    "Code": "200"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

