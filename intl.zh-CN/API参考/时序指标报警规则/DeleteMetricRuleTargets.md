# DeleteMetricRuleTargets

调用DeleteMetricRuleTargets接口删除一个报警规则的目标。目前仅支持消息服务MNS。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DeleteMetricRuleTargets&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteMetricRuleTargets|要执行的操作，取值：DeleteMetricRuleTargets。 |
|RuleId|String|是|ruleId-xxxxxx|报警规则ID。 |
|TargetIds.N|RepeatList|是|12345|目标ID。N的取值范围：1~5。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|FailIds|Struct| |删除失败的目标ID列表。 |
|TargetIds|List|1|删除失败的目标ID。 |
|Message|String|The Request is not authorization.|错误信息。 |
|RequestId|String|786E92D2-AC66-4250-B76F-F1E2FCDDBA1C|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DeleteMetricRuleTargets
&RuleId=ruleId-xxxxxx
&TargetIds.1=12345
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DeleteMetricRuleTargetsResponse>
		  <RequestId>786E92D2-AC66-4250-B76F-F1E2FCDDBA1C</RequestId>
		  <Code>200</Code>
		  <Success>true</Success>
		  <FailIds>
			    <TargetIds>1</TargetIds>
		  </FailIds>
</DeleteMetricRuleTargetsResponse>
```

`JSON` 格式

```
{
    "RequestId":"786E92D2-AC66-4250-B76F-F1E2FCDDBA1C",
    "Code":"200",
    "Success":"true",
    "FailIds":{
        "TargetIds":"1"
    }
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

