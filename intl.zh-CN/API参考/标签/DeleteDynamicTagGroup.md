# DeleteDynamicTagGroup

调用DeleteDynamicTagGroup接口删除智能标签规则。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DeleteDynamicTagGroup&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteDynamicTagGroup|要执行的操作，取值：DeleteDynamicTagGroup。 |
|DynamicTagRuleId|String|是|6b882d9a-5117-42e2-9d0c-4749a0c6\*\*\*\*|智能标签规则ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|RequestId|String|ACBDBB40-DFB6-4F4C-8957-51FFB233969C|请求ID。 |
|Message|String|The Request is not authorization.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DeleteDynamicTagGroup
&DynamicTagRuleId=6b882d9a-5117-42e2-9d0c-4749a0c6****
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DeleteDynamicTagGroupResponse>
	  <RequestId>08AAE67E-77B5-485B-9C79-D7C8C059150A</RequestId>
	  <Code>200</Code>
</DeleteDynamicTagGroupResponse>
```

`JSON` 格式

```
{
	"RequestId": "08AAE67E-77B5-485B-9C79-D7C8C059150A",
	"Code": 200,
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

