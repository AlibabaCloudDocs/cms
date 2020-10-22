# DescribeMetricRuleTemplateAttribute

调用DescribeMetricRuleTemplateAttribute接口查询报警模板详情。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeMetricRuleTemplateAttribute&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeMetricRuleTemplateAttribute|要执行的操作，取值：DescribeMetricRuleTemplateAttribute。 |
|Name|String|否|ECS\_Template1|报警模板名称。Name和TemplateId必须设置一个。 |
|TemplateId|String|否|12345|报警模板ID。Name和TemplateId必须设置一个。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|Integer|200|状态码。

 **说明：** 200表示成功。 |
|RequestId|String|C14F2566-B4AC-4C3E-AC7D-0A1D16CF33DE|请求ID。 |
|Message|String|The Request is not authorization.|错误信息。 |
|Resource|Struct| |报警模板详情。 |
|AlertTemplates|Array of AlertTemplate| |报警模板。 |
|AlertTemplate| | | |
|Category|String|ecs|云服务名称缩写。 |
|Escalations|Struct| |阈值及报警级别。 |
|Critical|Struct| |Critical报警级别。 |
|ComparisonOperator|String|GreaterThanOrEqualToThreshold|Critical级别的阈值比较符。取值：

 -   GreaterThanOrEqualToThreshold：大于等于。
-   GreaterThanThreshold：大于。
-   LessThanOrEqualToThreshold：小于等于。
-   LessThanThreshold：小于。
-   NotEqualToThreshold：不等。
-   GreaterThanYesterday：同比昨天时间上涨。
-   LessThanYesterday：同比昨天时间下降。
-   GreaterThanLastWeek：同比上周同一时间上涨。
-   LessThanLastWeek：同比上周同一时间下降。
-   GreaterThanLastPeriod：环比上周期上涨。
-   LessThanLastPeriod：环比上周期下降。 |
|Statistics|String|Average|Critical级别的统计方法。

 每个云服务的Statistics取值不同，请您根据云服务链接查找，详情请参见[云服务监控项](~~163515~~)。 |
|Threshold|String|90|Critical级别的阈值。 |
|Times|Integer|3|Critical级别的重试次数。 |
|Info|Struct| |Info报警级别。 |
|ComparisonOperator|String|GreaterThanOrEqualToThreshold|Info级别的阈值比较符。取值：

 -   GreaterThanOrEqualToThreshold：大于等于。
-   GreaterThanThreshold：大于。
-   LessThanOrEqualToThreshold：小于等于。
-   LessThanThreshold：小于。
-   NotEqualToThreshold：不等。
-   GreaterThanYesterday：同比昨天时间上涨。
-   LessThanYesterday：同比昨天时间下降。
-   GreaterThanLastWeek：同比上周同一时间上涨。
-   LessThanLastWeek：同比上周同一时间下降。
-   GreaterThanLastPeriod：环比上周期上涨。
-   LessThanLastPeriod：环比上周期下降。 |
|Statistics|String|Average|Info级别的统计方法。

 每个云服务的Statistics取值不同，请您根据云服务链接查找，详情请参见[云服务监控项](~~163515~~)。 |
|Threshold|String|90|Info级别的阈值。 |
|Times|Integer|3|Info级别的重试次数。 |
|Warn|Struct| |Warn报警级别。 |
|ComparisonOperator|String|GreaterThanOrEqualToThreshold|Warn级别阈值的比较符。取值：

 -   GreaterThanOrEqualToThreshold：大于等于。
-   GreaterThanThreshold：大于。
-   LessThanOrEqualToThreshold：小于等于。
-   LessThanThreshold：小于。
-   NotEqualToThreshold：不等。
-   GreaterThanYesterday：同比昨天时间上涨。
-   LessThanYesterday：同比昨天时间下降。
-   GreaterThanLastWeek：同比上周同一时间上涨。
-   LessThanLastWeek：同比上周同一时间下降。
-   GreaterThanLastPeriod：环比上周期上涨。
-   LessThanLastPeriod：环比上周期下降。 |
|Statistics|String|Average|Warn级别的统计方法。

 每个云服务的Statistics取值不同，请您根据云服务链接查找，详情请参见[云服务监控项](~~163515~~)。 |
|Threshold|String|90|Warn级别的阈值。 |
|Times|Integer|3|Warn级别的重试次数。 |
|MetricName|String|cpu\_total|监控项名称。

 请您根据云服务链接查找，详情请参见[云服务监控项](~~163515~~)。 |
|Namespace|String|acs\_ecs\_dashboard|阿里云服务的Namespace。

 请您根据云服务链接查找，详情请参见[云服务监控项](~~163515~~)。 |
|RuleName|String|ECS\_Rule1|报警规则名称。 |
|Selector|String|\{"disk":"/"\}|报警维度扩展选项。 |
|Webhook|String|https://api.aliyun.com/test.json|触发报警回调的URL地址。 |
|Description|String|ECS模板|报警模板描述信息。 |
|Name|String|ECS\_Template1|报警模板名称。 |
|RestVersion|String|0|报警模板版本。 |
|TemplateId|String|12345|报警模板ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeMetricRuleTemplateAttribute
&TemplateId=12345
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeMetricRuleTemplateAttributeResponse>
		  <Resource>
			    <RestVersion>0</RestVersion>
			    <Name>nametest</Name>
			    <Description>nametestDesc</Description>
			    <AlertTemplates>
				      <AlertTemplate>
					        <Category>ecs</Category>
					        <MetricName>cpu_total</MetricName>
					        <Namespace>acs_ecs_dashboard</Namespace>
					        <RuleName>cpu_total</RuleName>
					        <Webhook>https://api.aliyun.com/test.json</Webhook>
					        <Escalations>
						          <Critical></Critical>
						          <Info></Info>
						          <Warn>
							            <Statistics>Average</Statistics>
							            <Threshold>90.0</Threshold>
							            <Times>1</Times>
							            <ComparisonOperator>GreaterThanOrEqualToThreshold</ComparisonOperator>
						          </Warn>
					        </Escalations>
				      </AlertTemplate>
				      <AlertTemplate>
					        <Category>rds</Category>
					        <MetricName>AvgLogSize</MetricName>
					        <Namespace>acs_rds_dashboard</Namespace>
					        <RuleName>AvgLogSize</RuleName>
					        <Webhook></Webhook>
					        <Escalations>
						          <Critical></Critical>
						          <Info></Info>
						          <Warn>
							            <Statistics>Average</Statistics>
							            <Threshold>12.0</Threshold>
							            <Times>1</Times>
							            <ComparisonOperator>GreaterThanOrEqualToThreshold</ComparisonOperator>
						          </Warn>
					        </Escalations>
				      </AlertTemplate>
			    </AlertTemplates>
			    <TemplateId>12345</TemplateId>
		  </Resource>
		  <RequestId>C14F2566-B4AC-4C3E-AC7D-0A1D16CF33DE</RequestId>
		  <Success>true</Success>
		  <Code>200</Code>
</DescribeMetricRuleTemplateAttributeResponse>
```

`JSON` 格式

```
{
  "Resource": {
    "RestVersion": 0,
    "Name": "nametest",
    "Description": "nametestDesc",
    "AlertTemplates": {
      "AlertTemplate": [
        {
          "Category": "ecs",
          "MetricName": "cpu_total",
          "Namespace": "acs_ecs_dashboard",
          "RuleName": "cpu_total",
          "Webhook": "https://api.aliyun.com/test.json",
          "Escalations": {
            "Critical": {},
            "Info": {},
            "Warn": {
              "Statistics": "Average",
              "Threshold": "90.0",
              "Times": 1,
              "ComparisonOperator": "GreaterThanOrEqualToThreshold"
            }
          }
        },
        {
          "Category": "rds",
          "MetricName": "AvgLogSize",
          "Namespace": "acs_rds_dashboard",
          "RuleName": "AvgLogSize",
          "Webhook": "",
          "Escalations": {
            "Critical": {},
            "Info": {},
            "Warn": {
              "Statistics": "Average",
              "Threshold": "12.0",
              "Times": 1,
              "ComparisonOperator": "GreaterThanOrEqualToThreshold"
            }
          }
        }
      ]
    },
    "TemplateId": 12345
  },
  "RequestId": "C14F2566-B4AC-4C3E-AC7D-0A1D16CF33DE",
  "Success": true,
  "Code": 200
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

