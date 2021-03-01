# DescribeMetricList

调用DescribeMetricList接口查询指定云服务时序指标的监控数据。

**说明：** 云服务Namespace、Project、Metric、Period、Dimensions等参数的取值，请参见[DescribeMetricMetaList](~~98846~~)或[云服务监控项](~~163515~~)。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeMetricList&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeMetricList|要执行的操作，取值：DescribeMetricList。 |
|MetricName|String|是|cpu\_idle|监控项名称。 |
|Namespace|String|是|acs\_ecs\_dashboard|云服务的数据命名空间。

 命名方式：acs\_产品名。 |
|Period|String|否|60|时间间隔。单位：秒。取值：60、300、900。

 **说明：** 请根据您的实际需求设置该参数。 |
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
|NextToken|String|否|15761485350009dd70bb64cff1f0fff750b08ffff073be5fb1e785e2b020f1a949d5ea14aea7fed82f01dd8\*\*\*\*|分页游标标识。

 **说明：** 如果不设置该参数，则表示获取第一页的数据。当该参数有返回值时，说明还有下一页，您可以将返回的NextToken作为参数再次请求获得下一页的数据，直到返回为Null为止，表示获取到了所有的数据。 |
|Length|String|否|1000|每页显示的记录条数，用于分页查询。 |
|Express|String|否|\{"groupby":\["userId","instanceId"\]\}|查询出的现有结果进行实时计算的表达式。

 目前仅支持groupby，类似数据库的groupby语句。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|3121AE7D-4AFF-4C25-8F1D-C8226EBB1F42|请求ID。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|NextToken|String|15761441850009dd70bb64cff1f0fff6d0b08ffff073be5fb1e785e2b020f7fed9b5e137bd810a6d6cff5ae\*\*\*\*|分页游标标识。 |
|Period|String|60|时间间隔。单位：秒。取值：60、300、900。 |
|Datapoints|String|\[\{"timestamp":1548777660000,"userId":"123","instanceId":"i-abc","Minimum":9.92,"Average":9.92,"Maximum":9.92\}\]|监控数据列表。 |
|Message|String|The Request is not authorization.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeMetricList
&MetricName=cpu_idle
&Namespace=acs_ecs_dashboard
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeMetricListResponse>
		  <Period>60</Period>
		  <Datapoints>
			    <timestamp>1490152860000</timestamp>
			    <Maximum>100</Maximum>
			    <userId>123456789876****</userId>
			    <Minimum>93.1</Minimum>
			    <instanceId>i-abcdefgh12****</instanceId>
			    <Average>99.52</Average>
		  </Datapoints>
		  <Datapoints>
			    <timestamp>1490152920000</timestamp>
			    <Maximum>100</Maximum>
			    <userId>123456789876****</userId>
			    <Minimum>92.59</Minimum>
			    <instanceId>i-abcdefgh12****</instanceId>
			    <Average>99.49</Average>
		  </Datapoints>
		  <Datapoints>
			    <timestamp>1490152980000</timestamp>
			    <Maximum>100</Maximum>
			    <userId>123456789876****</userId>
			    <Minimum>92.86</Minimum>
			    <instanceId>i-abcdefgh12****</instanceId>
			    <Average>99.44</Average>
		  </Datapoints>
		  <Datapoints>
			    <timestamp>1490153040000</timestamp>
			    <Maximum>100</Maximum>
			    <userId>123456789876****</userId>
			    <Minimum>91.43</Minimum>
			    <instanceId>i-abcdefgh12****</instanceId>
			    <Average>99.36</Average>
		  </Datapoints>
		  <Datapoints>
			    <timestamp>1490153100000</timestamp>
			    <Maximum>100</Maximum>
			    <userId>123456789876****</userId>
			    <Minimum>93.55</Minimum>
			    <instanceId>i-abcdefgh12****</instanceId>
			    <Average>99.51</Average>
		  </Datapoints>
		  <Datapoints>
			    <timestamp>1490153160000</timestamp>
			    <Maximum>100</Maximum>
			    <userId>123456789876****</userId>
			    <Minimum>93.1</Minimum>
			    <instanceId>i-abcdefgh12****</instanceId>
			    <Average>99.52</Average>
		  </Datapoints>
		  <Datapoints>
			    <timestamp>1490153220000</timestamp>
			    <Maximum>100</Maximum>
			    <userId>123456789876****</userId>
			    <Minimum>92.59</Minimum>
			    <instanceId>i-abcdefgh12****</instanceId>
			    <Average>99.42</Average>
		  </Datapoints>
		  <Datapoints>
			    <timestamp>1490153280000</timestamp>
			    <Maximum>100</Maximum>
			    <userId>123456789876****</userId>
			    <Minimum>91.18</Minimum>
			    <instanceId>i-abcdefgh12****</instanceId>
			    <Average>99.34</Average>
		  </Datapoints>
		  <Datapoints>
			    <timestamp>1490153340000</timestamp>
			    <Maximum>100</Maximum>
			    <userId>123456789876****</userId>
			    <Minimum>92.86</Minimum>
			    <instanceId>i-abcdefgh12****</instanceId>
			    <Average>99.46</Average>
		  </Datapoints>
		  <Datapoints>
			    <timestamp>1490153400000</timestamp>
			    <Maximum>100</Maximum>
			    <userId>123456789876****</userId>
			    <Minimum>91.18</Minimum>
			    <instanceId>i-abcdefgh12****</instanceId>
			    <Average>99.35</Average>
		  </Datapoints>
		  <RequestId>6A5F022D-AC7C-460E-94AE-B9E75083D027</RequestId>
		  <Success>true</Success>
		  <Code>200</Code>
</DescribeMetricListResponse>
```

`JSON` 格式

```
{
    "Period": "60",
    "Datapoints": [
        {
            "timestamp": 1490152860000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 93.1,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.52
        },
        {
            "timestamp": 1490152920000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 92.59,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.49
        },
        {
            "timestamp": 1490152980000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 92.86,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.44
        },
        {
            "timestamp": 1490153040000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 91.43,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.36
        },
        {
            "timestamp": 1490153100000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 93.55,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.51
        },
        {
            "timestamp": 1490153160000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 93.1,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.52
        },
        {
            "timestamp": 1490153220000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 92.59,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.42
        },
        {
            "timestamp": 1490153280000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 91.18,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.34
        },
        {
            "timestamp": 1490153340000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 92.86,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.46
        },
        {
            "timestamp": 1490153400000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 91.18,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.35
        }
    ],
    "RequestId": "6A5F022D-AC7C-460E-94AE-B9E75083D027",
    "Success": true,
    "Code": "200"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

