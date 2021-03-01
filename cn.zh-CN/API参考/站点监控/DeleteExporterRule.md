# DeleteExporterRule

调用DeleteExporterRule接口删除数据导出规则。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DeleteExporterRule&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteExporterRule|要执行的操作，取值：**DeleteExporterRule**。 |
|RuleName|String|是|myRuleName|导出规则名称。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 状态码为200表示成功，其余取值表示失败。 |
|Message|String|success|返回信息。 |
|RequestId|String|6A5F022D-AC7C-460E-94AE-B9E75083D023|请求ID。 |
|Success|Boolean|true|是否成功，取值：

 -   `true`：成功
-   `false`：失败 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DeleteExporterRule
&RuleName=myRuleName
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<Message>success</Message>
<RequestId>8B524AE2-FBB1-4202-AA17-B3DEAAC8D861</RequestId>
<Code>200</Code>
<Success>true</Success>
```

`JSON` 格式

```
{
	"Message": "success",
	"RequestId": "8B524AE2-FBB1-4202-AA17-B3DEAAC8D861",
	"Code": "200",
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

