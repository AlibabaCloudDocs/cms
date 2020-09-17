# AddTags

调用AddTags接口为资源创建标签。

**说明：** 目前仅支持为应用分组创建标签。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=AddTags&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|AddTags|要执行的操作，取值：AddTags。 |
|GroupIds.N|RepeatList|是|12345|应用分组ID。 |
|Tag.N.Key|String|是|key1|标签键。

 N的取值范围：1~3。Key的取值范围：1~64个字符。

 **说明：** N的取值不允许为空字符串，不能以`aliyun`和`acs:`开头。标签键（`Tag.N.Key`）和标签值（`Tag.N.Value`）需要同时设置。 |
|Tag.N.Value|String|是|value1|标签值。N的取值范围：1~3。Value的取值范围：1~64个字符。

 **说明：** N的取值不允许为空字符串，不能以`aliyun`和`acs:`开头。 标签键（`Tag.N.Key`）和标签值（`Tag.N.Value`）需要同时设置。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|B04B8CF3-4489-432D-83BA-6F128E4F2295|请求ID。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Message|String|The Request is not authorization.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=AddTags
&GroupIds.1=12345
&Tag.1.Key=key1
&Tag.1.Value=value1
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<AddTagsResponse>
		  <Code>200</Code>
		  <RequestId>B04B8CF3-4489-432D-83BA-6F128E4F2295</RequestId>
		  <Success>true</Success>
</AddTagsResponse>
```

`JSON` 格式

```
{
    "Code":"200",
    "RequestId":"B04B8CF3-4489-432D-83BA-6F128E4F2295",
    "Success":true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

