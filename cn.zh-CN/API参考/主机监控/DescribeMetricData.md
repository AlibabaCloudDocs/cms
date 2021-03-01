# DescribeMetricData

调用DescribeMetricData接口查询指定时间段内的云产品时序指标监控数据。

各云产品**Namespace**、**Project**、**Metric**、**Period**、**Dimensions**等参数的取值，请参见[DescribeMetricMetaList](~~98846~~)或[云产品监控项](~~163515~~)。

**说明：** 与**DescribeMetricList**不同，本接口具有统计功能，即Dimension=\{"userId:"xxxx"\}，将该用户下的所有数据进行聚合计算。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeMetricData&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeMetricData|要执行的操作，取值：DescribeMetricData。 |
|MetricName|String|是|cpu\_idle|监控项名称。 |
|Namespace|String|是|acs\_ecs\_dashboard|产品的数据命名空间，用于区分不同的产品。

 命名方式：acs\_产品名。 |
|Period|String|否|60|时间间隔。单位：秒。取值：60、300、900。

 请根据您的实际需求设置该参数。 |
|StartTime|String|否|2019-01-30 00:00:00|开始时间。支持的格式：

 -   Unix时间戳：从1970年1月1日开始所经过的毫秒数。
-   Format格式：YYYY-MM-DDThh:mm:ssZ。

 **说明：** 开始和结束时间执行的是左开右闭的模式，StartTime不能等于或大于EndTime。 |
|EndTime|String|否|2019-01-30 00:10:00|结束时间。支持的格式：

 -   Unix时间戳：从1970年1月1日开始所经过的毫秒数。
-   Format格式：YYYY-MM-DDThh:mm:ssZ。 |
|Dimensions|String|否|\[\{"instanceId": "i-abcdefgh12\*\*\*\*"\}\]|维度Map，用于查询指定资源的监控数据。

 格式为：key-value键值对形式的集合，常用的key-value集合为：`instanceId:XXXXXX`。

 Key和Value的长度为1~64个字节，超过64个字节时截取前64字节。

 Key和Value的取值可包含大小写字母、数字、点号（.）、短划线（-）、下划线（\_）、正斜线（/）和反斜线（\\）。

 **说明：** Dimensions传入时需要使用JSON字符串表示该Map对象，必须按顺序传入。 |
|Express|String|否|“\{"groupby":\["userId","instanceId"\]\}”|对查询出的现有结果进行实时计算的表达式。

 目前仅支持groupby，类似数据库的groupby语句。 |
|Length|String|否|1000|每页显示的记录条数，用于分页查询。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Datapoints|String|\[\{"timestamp":1548777660000,"userId":"123\*\*\*\*","instanceId":"i-abc\*\*\*\*","Minimum":9.92,"Average":9.92,"Maximum":9.92\}\]|监控数据列表。包括如下信息：

 -   timestamp：发生报警的时间戳。
-   userId：发生报警的用户ID。
-   instanceId：发生报警的实例ID。
-   Minimum、Average、Maximum：报警规则。 |
|Message|String|The Request is not authorization.|错误信息。 |
|Period|String|60|时间间隔。单位：秒。取值：60、300、900。 |
|RequestId|String|6A5F022D-AC7C-460E-94AE-B9E75083D027|请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeMetricData
&MetricName=cpu_idle
&Namespace=acs_ecs_dashboard
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeMetricData>
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
		  <Code>200</Code>
</DescribeMetricData>
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
    "Code": "200"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

