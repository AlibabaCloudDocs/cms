# PutCustomMetric

调用PutCustomMetric接口上报自定义监控数据。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=PutCustomMetric&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|PutCustomMetric|要执行的操作，取值：PutCustomMetric。 |
|MetricList.N.Dimensions|String|是|\{"sampleName1":"value1","sampleName2":"value2"\}|维度Map，用于查询指定资源的监控数据。N的取值范围：1~21。

 格式：key-value键值对形式的集合，常用的key-value集合为：`{"Key":"Value"}`。

 Key和Value的长度为1~64个字符，超过64个字符时截取前64个。

 Key和Value的取值可包含英文字母、数字、点号（.）、短划线（-）、下划线（\_）、正斜线（/）和反斜线（\\）。

 **说明：** Dimensions传入时需要使用JSON字符串表示该Map对象，必须按顺序传入。 |
|MetricList.N.GroupId|String|是|12345|应用分组ID。N的取值范围：1~21。

 **说明：** 如果监控项不属于任何应用分组， 则输入0。 |
|MetricList.N.MetricName|String|是|cpu\_total|监控项名称。N的取值范围：1~21。详情请参见[云服务监控项](~~163515~~)。 |
|MetricList.N.Type|String|是|0|上报数值类型。N的取值范围：1~21。取值：

 -   0：原始数据。
-   1：聚合数据。

 **说明：** 当上报聚合数据时，建议周期为60秒和300秒的数据均上报，否则无法正常查询跨度大于7天的监控数据。 |
|MetricList.N.Values|String|是|\{"value":10.5\}|指标值集合。N的取值范围：1~21。

 **说明：** 如果上报数值的类型为0，则上报的是原始值，云监控会按周期将原始值聚合为多个值，例如：最大、计数、求和等。 |
|MetricList.N.Time|String|否|1508136760000|指标发生的时间。N的取值范围：1~21。支持以下两种类型：

 -   UTC时间。格式：YYYY-MM-DDThh:mm:ssZ，例如：20171012T132456.888+0800。
-   Long型时间戳。例如：1508136760000。 |
|MetricList.N.Period|String|否|60|聚合周期。N的取值范围：1~21。单位：秒，取值：60或300。

 **说明：** 如果上报数值的类型为1，则需要设置该参数。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|05B36C2C-5F6E-48D5-8B41-CE36DD7EE8E0|请求ID。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The request has failed due to a temporary failure of the server.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=PutCustomMetric
&MetricList.1.Dimensions={"sampleName1":"value1","sampleName2":"value2"}
&MetricList.1.GroupId=12345
&MetricList.1.MetricName=cpu_total
&MetricList.1.Type=0
&MetricList.1.Values={"value":10.5}
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<PutCustomMetricResponse>
	  <RequestId>75D115CE-5DA8-4647-9073-8F72BB85B6F7</RequestId>
	  <Message>success</Message>
	  <Code>200</Code>
</PutCustomMetricResponse>
```

`JSON` 格式

```
{
  "RequestId": "75D115CE-5DA8-4647-9073-8F72BB85B6F7",
  "Message": "success",
  "Code": "200"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

