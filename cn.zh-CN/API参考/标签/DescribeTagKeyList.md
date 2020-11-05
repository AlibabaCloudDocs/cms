# DescribeTagKeyList

调用DescribeTagKeyList接口查询标签键列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeTagKeyList&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeTagKeyList|要执行的操作，取值：DescribeTagKeyList。 |
|PageNumber|Integer|否|1|标签列表的页码。

 起始值：1，默认值：1。 |
|PageSize|Integer|否|10|分页查询时设置的每页行数。

 最大值：100，默认值：50。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|B04B8CF3-4489-432D-83BA-6F128E5F2293|请求ID。 |
|Message|String|Specified parameter PageSize is not valid.|错误信息。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|TagKeys|List|tagKey1|符合条件的标签键列表。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeTagKeyList
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeTagKeyListResponse>
	  <TagKeys>
		    <TagKey>tagKey1</TagKey>
		    <TagKey>tagKey2</TagKey>
	  </TagKeys>
	  <RequestId>FA9A8612-C770-4264-8A9C-C90F0081B4F5</RequestId>
	  <Success>true</Success>
	  <Code>200</Code>
</DescribeTagKeyListResponse>
```

`JSON` 格式

```
{
	"TagKeys": {
		"TagKey": [
			"tagKey1",
			"tagKey2"
		]
	},
	"RequestId": "FA9A8612-C770-4264-8A9C-C90F0081B4F5",
	"Success": true,
	"Code": 200
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

