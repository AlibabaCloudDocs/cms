# DescribeMetricLast

调用DescribeMetricLast接口查询指定监控项的最新监控数据。

本文将提供一个示例，查询云服务`acs_ecs_dashboard`监控项`CPUUtilization`的最新监控数据。返回结果显示，当前账号`123456789876****`下实例`i-abcdefgh12****`的监控项`CPUUtilization`间隔60秒的最大值为100、最小值为93.1、平均值为99.52。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeMetricLast&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeMetricLast|要执行的操作，取值：DescribeMetricLast。 |
|MetricName|String|是|CPUUtilization|云服务的监控项名称。

 **说明：** 关于监控项名称，请参见[云服务监控项](~~163515~~)。 |
|Namespace|String|是|acs\_ecs\_dashboard|云服务的命名空间。命名方式：acs\_云服务名称。

 **说明：** 关于命名空间，请参见[云服务监控项](~~163515~~)。 |
|Period|String|否|60|监控项的统计周期。单位：秒。

 如果不设置统计周期，则按照注册监控项时申请的上报周期来查询原始数据；如果设置报警规则时设置了统计周期，则按照该周期查询对应的统计数据。

 **说明：** 关于监控项的统计周期，请参见[云服务监控项](~~163515~~)。 |
|StartTime|String|否|2019-01-31 10:00:00|查询监控项的开始时间。 |
|EndTime|String|否|2019-01-31 10:10:00|查询监控项的结束时间。

 -   对于秒级数据，查询数据的起始时间是EndTime往前倒推20分钟后与startTime对比的最大值。
-   对于分钟级数据，查询数据的起始时间是EndTime往前倒推2小时后与startTime对比的最大值。
-   对于小时级数据，查询数据的起始时间是EndTime往前倒推2天后与startTime对比的最大值。 |
|Dimensions|String|否|\[\{"instanceId":"i-abcdefgh12\*\*\*\*"\}\]|维度Map，用于查询指定资源的监控数据。

 格式：key-value键值对形式的集合，常用的key-value集合为`instanceId:i-2ze2d6j5uhg20x47****`。

 **说明：** 关于监控项的维度，请参见[云服务监控项](~~163515~~)。 |
|NextToken|String|否|15761432850009dd70bb64cff1f0fff6c0b08ffff073be5fb1e785e2b020f7fed9b5e137bd810a6d6cff5ae\*\*\*\*|分页游标的标识。

 -   如果匹配查询条件的返回结果超过了分页大小，则会返回这个分页游标。
-   如果需要获取下一页数据，将返回的游标值作为请求参数即可，直到无游标值返回，表示已经获取了全部数据。 |
|Length|String|否|1000|返回监控数据的每页大小，用于分页查询。

 默认值：1000，即每页1000条监控数据。 |
|Express|String|否|\{"groupby":\["userId","instanceId"\]\}|对现有查询结果进行实时计算的表达式。 |

关于公共请求参数的详情，请参见[公共参数](~~199331~~)。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|021472A6-25E3-4094-8D00-BA4B6A5486C3|请求ID。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Period|String|60|时间间隔。单位：秒。 |
|NextToken|String|xxxxxx|分页游标标识。 |
|Datapoints|String|\[\{"timestamp":1548777660000,"userId":"123456789876\*\*\*\*","instanceId":"i-abcdefgh12\*\*\*\*","Minimum":93.1,"Average":99.52,"Maximum":100\}\]|监控数据列表。 |
|Message|String|The specified resource is not found.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeMetricLast
&MetricName=CPUUtilization
&Namespace=acs_ecs_dashboard
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<QueryMetricListResponse>
	  <Period>60</Period>
	  <Datapoints>
		    <timestamp>1548777660000</timestamp>
		    <Maximum>100</Maximum>
		    <userId>123456789876****</userId>
		    <Minimum>93.1</Minimum>
		    <instanceId>i-abcdefgh12****</instanceId>
		    <Average>99.52</Average>
	  </Datapoints>
	  <RequestId>6A5F022D-AC7C-460E-94AE-B9E75083D027</RequestId>
	  <Success>true</Success>
	  <Code>200</Code>
</QueryMetricListResponse>
```

`JSON`格式

```
{
    "Period": "60",
    "Datapoints": [
        {
            "timestamp": 1548777660000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 93.1,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.52
        }
    ],
    "RequestId": "6A5F022D-AC7C-460E-94AE-B9E75083D027",
    "Success": true,
    "Code": "200"
}
```

## 错误码

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|ResourceNotFound|The specified resource is not found.|未找到指定资源。|

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

