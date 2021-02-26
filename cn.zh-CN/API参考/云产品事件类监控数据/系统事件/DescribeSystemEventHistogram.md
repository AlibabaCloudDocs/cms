# DescribeSystemEventHistogram

调用DescribeSystemEventHistogram接口查询系统事件的时段数量分布图（柱状图）。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeSystemEventHistogram&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeSystemEventHistogram|要执行的操作，取值：DescribeSystemEventHistogram。 |
|Product|String|否|OSS|产品的名称缩写。

 **说明：** 关于产品名称缩写的取值，请参见[DescribeSystemEventMetaList](~~114972~~)。 |
|EventType|String|否|Exception|事件类型。

 **说明：** 关于事件类型的取值，请参见[DescribeSystemEventMetaList](~~114972~~)。 |
|Name|String|否|BucketIngressBandwidth|事件名称。

 **说明：** 关于事件名称的取值，请参见[DescribeSystemEventMetaList](~~114972~~)。 |
|Level|String|否|CRITICAL|事件级别，取值：

 -   CRITICAL：严重
-   WARN：警告
-   INFO：信息 |
|Status|String|否|normal|事件状态。

 **说明：** 关于事件状态的取值，请参见[DescribeSystemEventMetaList](~~114972~~)。 |
|GroupId|String|否|12345|应用分组ID。 |
|SearchKeywords|String|否|cms|搜索事件内容包含的关键字。取值：

 -   如果您待搜索事件的内容中包括a和b，可以搜索`a and b`。
-   如果您待搜索事件的内容中包括a或b，可以搜索`a or b`。 |
|StartTime|String|否|1552209685596|开始时间。

 格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |
|EndTime|String|否|1552220485596|结束时间。

 格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|486029C9-53E1-44B4-85A8-16A571A043FD|请求ID。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Success|String|true|操作是否成功。true表示成功，false表示失败。 |
|SystemEventHistograms|Array| |事件分段统计详情。 |
|SystemEventHistogram| | | |
|Count|Long|2|事件发生数量。 |
|EndTime|Long|1552225753000|结束时间。

 格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |
|StartTime|Long|1552225770000|开始时间。

 格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |
|Message|String|The Request is not authorization.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeSystemEventHistogram
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeSystemEventHistogram>
		  <RequestId>E38CA81A-A012-4C59-B694-42AAFBE27ED2</RequestId>
		  <SystemEventHistograms>
			    <SystemEventHistogram>
				      <EndTime>1593671700000</EndTime>
				      <StartTime>1593671684000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593671730000</EndTime>
				      <StartTime>1593671700000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593671760000</EndTime>
				      <StartTime>1593671730000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593671790000</EndTime>
				      <StartTime>1593671760000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593671820000</EndTime>
				      <StartTime>1593671790000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593671850000</EndTime>
				      <StartTime>1593671820000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593671880000</EndTime>
				      <StartTime>1593671850000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593671910000</EndTime>
				      <StartTime>1593671880000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593671940000</EndTime>
				      <StartTime>1593671910000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593671970000</EndTime>
				      <StartTime>1593671940000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672000000</EndTime>
				      <StartTime>1593671970000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672030000</EndTime>
				      <StartTime>1593672000000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672060000</EndTime>
				      <StartTime>1593672030000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672090000</EndTime>
				      <StartTime>1593672060000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672120000</EndTime>
				      <StartTime>1593672090000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672150000</EndTime>
				      <StartTime>1593672120000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672180000</EndTime>
				      <StartTime>1593672150000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672210000</EndTime>
				      <StartTime>1593672180000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672240000</EndTime>
				      <StartTime>1593672210000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672270000</EndTime>
				      <StartTime>1593672240000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672300000</EndTime>
				      <StartTime>1593672270000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672330000</EndTime>
				      <StartTime>1593672300000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672360000</EndTime>
				      <StartTime>1593672330000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672390000</EndTime>
				      <StartTime>1593672360000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672420000</EndTime>
				      <StartTime>1593672390000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672450000</EndTime>
				      <StartTime>1593672420000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672480000</EndTime>
				      <StartTime>1593672450000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672510000</EndTime>
				      <StartTime>1593672480000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672540000</EndTime>
				      <StartTime>1593672510000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672570000</EndTime>
				      <StartTime>1593672540000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
			    <SystemEventHistogram>
				      <EndTime>1593672584000</EndTime>
				      <StartTime>1593672570000</StartTime>
				      <Count>0</Count>
			    </SystemEventHistogram>
		  </SystemEventHistograms>
		  <Code>200</Code>
		  <Success>true</Success>
</DescribeSystemEventHistogram>
```

`JSON` 格式

```
{
	"RequestId": "E38CA81A-A012-4C59-B694-42AAFBE27ED2",
	"SystemEventHistograms": {
		"SystemEventHistogram": [
			{
				"EndTime": 1593671700000,
				"StartTime": 1593671684000,
				"Count": 0
			},
			{
				"EndTime": 1593671730000,
				"StartTime": 1593671700000,
				"Count": 0
			},
			{
				"EndTime": 1593671760000,
				"StartTime": 1593671730000,
				"Count": 0
			},
			{
				"EndTime": 1593671790000,
				"StartTime": 1593671760000,
				"Count": 0
			},
			{
				"EndTime": 1593671820000,
				"StartTime": 1593671790000,
				"Count": 0
			},
			{
				"EndTime": 1593671850000,
				"StartTime": 1593671820000,
				"Count": 0
			},
			{
				"EndTime": 1593671880000,
				"StartTime": 1593671850000,
				"Count": 0
			},
			{
				"EndTime": 1593671910000,
				"StartTime": 1593671880000,
				"Count": 0
			},
			{
				"EndTime": 1593671940000,
				"StartTime": 1593671910000,
				"Count": 0
			},
			{
				"EndTime": 1593671970000,
				"StartTime": 1593671940000,
				"Count": 0
			},
			{
				"EndTime": 1593672000000,
				"StartTime": 1593671970000,
				"Count": 0
			},
			{
				"EndTime": 1593672030000,
				"StartTime": 1593672000000,
				"Count": 0
			},
			{
				"EndTime": 1593672060000,
				"StartTime": 1593672030000,
				"Count": 0
			},
			{
				"EndTime": 1593672090000,
				"StartTime": 1593672060000,
				"Count": 0
			},
			{
				"EndTime": 1593672120000,
				"StartTime": 1593672090000,
				"Count": 0
			},
			{
				"EndTime": 1593672150000,
				"StartTime": 1593672120000,
				"Count": 0
			},
			{
				"EndTime": 1593672180000,
				"StartTime": 1593672150000,
				"Count": 0
			},
			{
				"EndTime": 1593672210000,
				"StartTime": 1593672180000,
				"Count": 0
			},
			{
				"EndTime": 1593672240000,
				"StartTime": 1593672210000,
				"Count": 0
			},
			{
				"EndTime": 1593672270000,
				"StartTime": 1593672240000,
				"Count": 0
			},
			{
				"EndTime": 1593672300000,
				"StartTime": 1593672270000,
				"Count": 0
			},
			{
				"EndTime": 1593672330000,
				"StartTime": 1593672300000,
				"Count": 0
			},
			{
				"EndTime": 1593672360000,
				"StartTime": 1593672330000,
				"Count": 0
			},
			{
				"EndTime": 1593672390000,
				"StartTime": 1593672360000,
				"Count": 0
			},
			{
				"EndTime": 1593672420000,
				"StartTime": 1593672390000,
				"Count": 0
			},
			{
				"EndTime": 1593672450000,
				"StartTime": 1593672420000,
				"Count": 0
			},
			{
				"EndTime": 1593672480000,
				"StartTime": 1593672450000,
				"Count": 0
			},
			{
				"EndTime": 1593672510000,
				"StartTime": 1593672480000,
				"Count": 0
			},
			{
				"EndTime": 1593672540000,
				"StartTime": 1593672510000,
				"Count": 0
			},
			{
				"EndTime": 1593672570000,
				"StartTime": 1593672540000,
				"Count": 0
			},
			{
				"EndTime": 1593672584000,
				"StartTime": 1593672570000,
				"Count": 0
			}
		]
	},
	"Code": "200",
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

