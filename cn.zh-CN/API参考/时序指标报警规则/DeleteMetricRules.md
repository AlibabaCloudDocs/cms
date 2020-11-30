# DeleteMetricRules

调用DeleteMetricRules接口删除一个或多个报警规则。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DeleteMetricRules&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteMetricRules|要执行的操作，取值：DeleteMetricRules。 |
|Id.N|RepeatList|是|ab05733c97b7ce239fb1b53393dc1697c7e12\*\*\*\*|报警规则ID。N的取值范围：1~100。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The specified resource is not found.|返回信息。 |
|RequestId|String|E5599964-8D0D-40DC-8E90-27A619384B81|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DeleteMetricRules
&Id.1=ab05733c97b7ce239fb1b53393dc1697c7e12****
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DeleteMetricRulesResponse>
      <RequestId>AE2ACE17-BD92-4FB0-83DB-AC969C677CE7</RequestId>
      <Code>200</Code>
      <Success>true</Success>
</DeleteMetricRulesResponse>
```

`JSON` 格式

```
{
	"RequestId": "AE2ACE17-BD92-4FB0-83DB-AC969C677CE7",
	"Code": "200",
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

