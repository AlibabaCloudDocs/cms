# DescribeTagValueList

调用DescribeTagValueList接口查询标签值列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeTagValueList&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeTagValueList|要执行的操作，取值：DescribeTagValueList。 |
|TagKey|String|是|tagKey1|标签键名称。 |
|PageNumber|Integer|否|1|标签列表的页码。

 起始值：1，默认值：1。 |
|PageSize|Integer|否|10|分页查询时设置的每页行数。

 最大值：100，默认值：50。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|B04B8CF3-4489-432D-83BA-6F128E4F2295|请求ID。 |
|Message|String|Specified parameter PageNumber is not valid.|错误信息。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|TagValues|List|tagValue1|符合条件的标签值列表。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeTagValueList
&TagKey=tagKey1
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeTagValueListResponse>
	  <RequestId>9AF637BA-6617-41FE-A0FA-3301521377A4</RequestId>
	  <TagValues>
		    <TagValue>tagValue1</TagValue>
		    <TagValue>tagValue2</TagValue>
	  </TagValues>
	  <Success>true</Success>
	  <Code>200</Code>
</DescribeTagValueListResponse>
```

`JSON` 格式

```
{
	"RequestId": "9AF637BA-6617-41FE-A0FA-3301521377A4",
	"TagValues": {
		"TagValue": [
			"tagValue1",
			"tagValue2"
		]
	},
	"Success": true,
	"Code": 200
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

