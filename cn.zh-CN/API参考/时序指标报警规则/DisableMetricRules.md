# DisableMetricRules

调用DisableMetricRules接口禁用报警规则。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DisableMetricRules&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DisableMetricRules|要执行的操作，取值：DisableMetricRules。 |
|RuleId.N|RepeatList|是|detect\_87\*\*\*\*\_HTTP\_HttpLatency|报警规则ID。N的取值范围：1~20。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|RuleId is mandatory for this action.|错误信息。 |
|RequestId|String|FF38D33A-67C1-40EB-AB65-FAEE51EDB644|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DisableMetricRules
&RuleId.1=detect_87****_HTTP_HttpLatency
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DisableMetricRulesResponse>
      <Code>200</Code>
      <RequestId>FF38D33A-67C1-40EB-AB65-FAEE51EDB644</RequestId>
      <Success>true</Success>
</DisableMetricRulesResponse>
```

`JSON` 格式

```
{
    "Code":"200",
    "RequestId":"FF38D33A-67C1-40EB-AB65-FAEE51EDB644",
    "Success":true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

