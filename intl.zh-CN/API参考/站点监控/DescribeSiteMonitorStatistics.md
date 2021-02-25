# DescribeSiteMonitorStatistics

调用DescribeSiteMonitorStatistics接口查询指定站点监控任务的平均统计数据。

本文将提供一个示例，查询站点监控任务`49f7b317-7645-4cc9-94fd-ea42e522****`的可用率`Availability`。返回结果显示站点监控的可用率为100。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeSiteMonitorStatistics&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeSiteMonitorStatistics|要执行的操作，取值：DescribeSiteMonitorStatistics。 |
|MetricName|String|是|Availability|监控项名称。取值：

 -   Availability：可用率。
-   ErrorRate：错误率。
-   ResponseTime：响应时间。 |
|TaskId|String|是|ef4cdc8b-9dc7-43e7-810e-f950e56c\*\*\*\*|站点监控任务ID。 |
|TimeRange|String|否|60|统计周期。单位：分钟，最大值：1440。 |
|StartTime|String|否|1576142850527|开始时间戳。单位：毫秒。 |

关于公共请求参数的详情，请参见[公共参数](~~199331~~)。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|3AD2724D-E317-4BFB-B422-D6691D071BE1|请求ID。 |
|Success|String|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Data|String|100|统计结果。 |
|Message|String|Succcessful|返回信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeSiteMonitorStatistics
&MetricName=Availability
&TaskId=ef4cdc8b-9dc7-43e7-810e-f950e56c****
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<DescribeSiteMonitorStatisticsResponse>
	  <Message>successful</Message>
	  <RequestId>3AD2724D-E317-4BFB-B422-D6691D071BE1</RequestId>
	  <Data>100</Data>
	  <Code>200</Code>
	  <Success>true</Success>
</DescribeSiteMonitorStatisticsResponse>
```

`JSON`格式

```
{
	"Message": "successful",
	"RequestId": "3AD2724D-E317-4BFB-B422-D6691D071BE1",
	"Data": 100,
	"Code": "200",
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

