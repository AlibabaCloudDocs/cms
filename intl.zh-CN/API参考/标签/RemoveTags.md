# RemoveTags

调用RemoveTags接口删除标签。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=RemoveTags&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|RemoveTags|要执行的操作，取值：RemoveTags。 |
|GroupIds.N|RepeatList|是|12345|应用分组ID。 |
|Tag.N.Key|String|是|Key1|标签键。

 **说明：** 标签键（`Tag.N.Key`）和标签值（`Tag.N.Value`）需要同时设置。 |
|Tag.N.Value|String|是|Value1|标签值。

 **说明：** 标签键（`Tag.N.Key`）和标签值（`Tag.N.Value`）需要同时设置。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|195390D2-69D0-4D9E-81AA-A7F5BC1B91EB|请求ID。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Tag|List|tag1|被删除的标签列表。 |
|Message|String|Illegal parameters.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=RemoveTags
&GroupIds.1=12345
&Tag.1.Key=Key1
&Tag.1.Value=Value1
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RemoveTagsResponse>
		  <RequestId>E15C718E-067E-49D0-86F7-BC7242230091</RequestId>
		  <Code>200</Code>
		  <Success>true</Success>
</RemoveTagsResponse>
```

`JSON` 格式

```
{
	"RequestId": "E15C718E-067E-49D0-86F7-BC7242230091",
	"Code": 200,
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

