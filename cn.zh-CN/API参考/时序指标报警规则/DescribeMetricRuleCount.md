# DescribeMetricRuleCount

调用DescribeMetricRuleCount接口获取各种状态报警规则的数量。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeMetricRuleCount&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeMetricRuleCount|要执行的操作，取值：DescribeMetricRuleCount。 |
|Namespace|String|否|acs\_ecs\_dashboard|云服务的命名空间。详情请参见[云产品监控项](~~163515~~)。 |
|MetricName|String|否|cpu\_total|监控项名称。详情请参见[云产品监控项](~~163515~~)。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The Request is not authorization.|错误信息。 |
|MetricRuleCount|Struct| |各类状态报警规则的数量。 |
|Alarm|Integer|5|报警状态报警规则的数量。 |
|Disable|Integer|0|禁用状态报警规则的数量。 |
|Nodata|Integer|0|无数据状态报警规则的数量。 |
|Ok|Integer|40|正常状态报警规则的数量。 |
|Total|Integer|45|报警规则总数量。 |
|RequestId|String|FF38D33A-67C1-40EB-AB65-FAEE51EDB644|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeMetricRuleCount
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeMetricRuleCountResponse>
      <Success>true</Success>
      <Code>200</Code>
      <RequestId>FF38D33A-67C1-40EB-AB65-FAEE51EDB644</RequestId>
      <MetricRuleCount>
            <Ok>40</Ok>
            <Disable>0</Disable>
            <Total>45</Total>
            <Nodata>0</Nodata>
            <Alarm>5</Alarm>
      </MetricRuleCount>
</DescribeMetricRuleCountResponse>
```

`JSON` 格式

```
{
  "Success": true,
  "Code": "200",
  "RequestId":"FF38D33A-67C1-40EB-AB65-FAEE51EDB644",
  "MetricRuleCount": {
    "Ok": 40,
    "Disable": 0,
    "Total": 45,
    "Nodata": 0,
    "Alarm": 5
  }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

