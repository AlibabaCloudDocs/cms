# DescribeMetricRuleList

调用DescribeMetricRuleList接口查询报警规则列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeMetricRuleList&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeMetricRuleList|要执行的操作，取值：DescribeMetricRuleList。 |
|Namespace|String|否|acs\_ecs\_dashboard|服务的数据命名空间。

 **说明：** 详情请参见[DescribeSystemEventMetaList](~~114972~~)或[云服务监控项](~~163515~~)。 |
|MetricName|String|否|cpu\_total|监控项名称。

 **说明：** 详情请参见[DescribeSystemEventMetaList](~~114972~~)或[云服务监控项](~~163515~~)。 |
|EnableState|Boolean|否|true|启用状态。取值：

 -   true：启用。
-   false：禁用。

 默认为空，表示查询所有状态（包含启用和禁用）的规则。 |
|Page|String|否|1|分页码。默认值：1。 |
|PageSize|String|否|10|每页显示记录条数。默认值：10。 |
|AlertState|String|否|ALARM|报警规则状态。取值：

 -   OK：正常。
-   ALARM：报警。
-   INSUFFICIENT\_DATA：无数据。 |
|Dimensions|String|否|\{"instanceId":"i-xy123\*\*\*\*"\}|维度Map，用于查询指定资源的监控数据。

 格式为：key-value键值对形式的集合。常用的key-value集合为：`instanceId:XXXXXX`。

 Key和Value的长度为1~64个字节，超过64个字节时截取前64字节。

 Key和Value的取值可包含英文字母、数字、英文句点（.）、短划线（-）、下划线（\_）、正斜线（/）和反斜线（\\）。

 **说明：** Dimensions传入时需要使用JSON字符串表示该Map对象，必须按顺序传入。 |
|RuleName|String|否|rule1|报警规则名称。

 **说明：** 该参数支持模糊查询。 |
|GroupId|String|否|123456|应用分组ID。 |
|RuleIds|String|否|a151cd6023eacee2f0978e03863cc1697c8950812\*\*\*\*|报警规则ID。

 **说明：** 该参数支持一次查询多个，多个ID之间用英文逗号（,）分隔，一次最多可查询20条。 |

查询报警规则列表。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|0E657631-CD6C-4C24-9637-98D000B9272C|请求ID。 |
|Code|Integer|200|状态码。

 **说明：** 200表示成功。 |
|Total|String|21|总记录条数。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Alarms|Array of Alarm| |报警规则列表。 |
|Alarm| | | |
|AlertState|String|OK|报警规则状态。取值：

 -   OK：正常。
-   ALARM：报警。
-   INSUFFICIENT\_DATA：无数据。 |
|ContactGroups|String|Alice|报警联系人。 |
|Dimensions|String|\[\{\}\]|维度Map，用于查询指定资源的监控数据。

 格式为：key-value键值对形式的集合。常用的key-value集合为：`instanceId:XXXXXX`。

 Key和Value的长度为1~64个字节，超过64个字节时截取前64字节。

 Key和Value的取值可包含英文字母、数字、英文句点（.）、短划线（-）、下划线（\_）、正斜线（/）和反斜线（\\）。

 **说明：** Dimensions传入时需要使用JSON字符串表示该Map对象，必须按顺序传入。 |
|EffectiveInterval|String|00:00-23:59|报警规则的生效时间段。 |
|EnableState|Boolean|true|启用状态。取值：

 -   true：启用。
-   false：禁用。

 默认为空，表示查询所有状态（包含启用和禁用）的规则。 |
|Escalations|Struct| |报警分级别触发条件。 |
|Critical|Struct| |Critical级别报警触发条件。 |
|ComparisonOperator|String|GreaterThanOrEqualToThreshold|Critical级别阈值比较符。取值：

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
|PreCondition|String|$Average\>80|Critical级别报警的前置条件。当参数ComparisonOperator设置为同比或环比时，与该参数共同起作用。

 例如：该参数设置为$Average\>80，ComparisonOperator设置为GreaterThanYesterday，Threshold设置为10，表示当平均值大于80且环比昨天上涨10%时，触发报警。

 **说明：** $Average\>0中的$Average为一个占位符，为"$"+监控结果字段值，云监控会将其替换为对应的统计值或原始的监控值。 |
|Statistics|String|Average|Critical级别报警统计方法。 |
|Threshold|String|90|Critical级别阈值。 |
|Times|String|3|Critical级别连续出现次数。连续出现这个次数并且超过阈值才会触发报警。 |
|Info|Struct| |Info级别报警触发条件。 |
|ComparisonOperator|String|GreaterThanOrEqualToThreshold|Info级别阈值比较符。取值：

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
|PreCondition|String|$Average\>80|Info级别报警的前置条件。当参数ComparisonOperator设置为同比或环比时，与该参数共同起作用。

 例如：该参数设置为$Average\>80，ComparisonOperator设置为GreaterThanYesterday，Threshold设置为10，表示当平均值大于80且环比昨天上涨10%时，触发报警。

 **说明：** $Average\>0中的$Average为一个占位符，为"$"+监控结果字段值，云监控会将其替换为对应的统计值或原始的监控值。 |
|Statistics|String|Average|Info级别报警统计方法。 |
|Threshold|String|90|Info级别阈值。 |
|Times|String|1|Info级别连续出现次数。连续出现这个次数并且超过阈值才会触发报警。 |
|Warn|Struct| |Warn级别报警触发条件。 |
|ComparisonOperator|String|GreaterThanOrEqualToThreshold|Warn级别阈值比较符。取值：

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
|PreCondition|String|$Average\>80|Warn级别报警的前置条件。当参数ComparisonOperator设置为同比或环比时，与该参数共同起作用。

 例如：该参数设置为$Average\>80，ComparisonOperator设置为GreaterThanYesterday，Threshold设置为10，表示当平均值大于80且环比昨天上涨10%时，触发报警。

 **说明：** $Average\>0中的$Average为一个占位符，为"$"+监控结果字段值，云监控会将其替换为对应的统计值或原始的监控值。 |
|Statistics|String|Average|Warn级别报警统计方法。 |
|Threshold|String|90|Warn级别阈值。 |
|Times|String|3|Warn级别连续出现次数。连续出现这个次数并且超过阈值才会触发报警。 |
|GroupId|String|123456|应用分组ID。 |
|GroupName|String|ECS\_Group|应用分组名称。

 **说明：** 如果报警规则是关联到应用分组上的，则此处显示该参数。 |
|MailSubject|String|ECS\_Bucket|报警邮件主题定义。 |
|MetricName|String|cpu\_total|监控项名称。 |
|Namespace|String|acs\_ecs\_dashboard|服务的数据命名空间，用于区分不同的产品。

 **说明：** 详情请参见[云服务监控项](~~163515~~)。 |
|NoEffectiveInterval|String|00:00-23:59|报警规则不生效的时间段。 |
|Period|String|60|统计周期。 |
|Resources|String|\[\{\\"instanceId\\":\\"i-a2d5q7pm3f9yr29e\*\*\*\*\\"\},\{\\"instanceId\\":\\"i-a2d5q7pm3f9yr29e\*\*\*\*\\"\}|报警规则关联的资源。 |
|RuleId|String|a151cd6023eacee2f0978e03863cc1697c895012\*\*\*\*|报警规则ID。 |
|RuleName|String|ECS\_CPU|报警规则名称。 |
|SilenceTime|String|86400|通道沉默周期。单位：秒。默认值：86400秒，最小值：3600秒。

 监控数据持续超过报警规则阈值时，每个沉默周期内只发送一次报警通知。 |
|SourceType|String|METRIC|报警规则类型。取值：METRIC，表示时序指标报警规则。 |
|Webhook|String|http://www.aliyun.com|URL回调地址。 |
|Message|String|The Request is not authorization.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeMetricRuleList
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeMetricRuleListResponse>
		  <RequestId>0E657631-CD6C-4C24-9637-98D000B9272C</RequestId>
		  <Total>21</Total>
		  <Alarms>
			    <Alarm>
				      <GroupName>ECS_Group</GroupName>
				      <NoEffectiveInterval>00:00-23:59</NoEffectiveInterval>
				      <SilenceTime>86400</SilenceTime>
				      <ContactGroups>Alice</ContactGroups>
				      <MailSubject>ECS_Bucket</MailSubject>
				      <RuleId>a151cd6023eacee2f0978e03863cc1697c895012****</RuleId>
				      <SourceType>METRIC</SourceType>
				      <Period>60</Period>
				      <Dimensions>[{}]</Dimensions>
				      <EffectiveInterval>00:00-23:59</EffectiveInterval>
				      <Namespace>acs_ecs_dashboard</Namespace>
				      <AlertState>OK</AlertState>
				      <GroupId>123456</GroupId>
				      <MetricName>cpu_total</MetricName>
				      <EnableState>true</EnableState>
				      <Webhook>http://www.aliyun.com</Webhook>
				      <Resources>[{\\\"instanceId\\\":\\\"i-a2d5q7pm3f9yr29e****\\\"},{\\\"instanceId\\\":\\\"i-a2d5q7pm3f9yr29e****\\\"}</Resources>
				      <RuleName>ECS_CPU</RuleName>
			    </Alarm>
			    <Alarm>
				      <Escalations>
					        <Critical>
						          <ComparisonOperator>GreaterThanOrEqualToThreshold</ComparisonOperator>
						          <Times>3</Times>
						          <Statistics>Average</Statistics>
						          <Threshold>90</Threshold>
					        </Critical>
					        <Info>
						          <ComparisonOperator>GreaterThanOrEqualToThreshold</ComparisonOperator>
						          <Times>3</Times>
						          <Statistics>Average</Statistics>
						          <Threshold>90</Threshold>
					        </Info>
					        <Warn>
						          <ComparisonOperator>GreaterThanOrEqualToThreshold</ComparisonOperator>
						          <Times>3</Times>
						          <Statistics>Average</Statistics>
						          <Threshold>90</Threshold>
					        </Warn>
				      </Escalations>
			    </Alarm>
		  </Alarms>
		  <Code>200</Code>
		  <Success>true</Success>
</DescribeMetricRuleListResponse>
```

`JSON` 格式

```
{
    "RequestId":"0E657631-CD6C-4C24-9637-98D000B9272C",
    "Total":"21",
    "Alarms":{
        "Alarm":[
            {
                "GroupName":"ECS_Group",
                "NoEffectiveInterval":"00:00-23:59",
                "SilenceTime":"86400",
                "ContactGroups":"Alice",
                "MailSubject":"ECS_Bucket",
                "RuleId":"a151cd6023eacee2f0978e03863cc1697c895012****",
                "SourceType":"METRIC",
                "Period":"60",
                "Dimensions":"[{}]",
                "EffectiveInterval":"00:00-23:59",
                "Namespace":"acs_ecs_dashboard",
                "AlertState":"OK",
                "GroupId":"123456",
                "MetricName":"cpu_total",
                "EnableState":"true",
                "Webhook":"http://www.aliyun.com",
                "Resources":"[{\\\"instanceId\\\":\\\"i-a2d5q7pm3f9yr29e****\\\"},{\\\"instanceId\\\":\\\"i-a2d5q7pm3f9yr29e****\\\"}",
                "RuleName":"ECS_CPU"
            },
            {
                "Escalations":{
                    "Critical":{
                        "ComparisonOperator":"GreaterThanOrEqualToThreshold",
                        "Times":"3",
                        "Statistics":"Average",
                        "Threshold":"90"
                    },
                    "Info":{
                        "ComparisonOperator":"GreaterThanOrEqualToThreshold",
                        "Times":"3",
                        "Statistics":"Average",
                        "Threshold":"90"
                    },
                    "Warn":{
                        "ComparisonOperator":"GreaterThanOrEqualToThreshold",
                        "Times":"3",
                        "Statistics":"Average",
                        "Threshold":"90"
                    }
                }
            }]
    },
    "Code":"200",
    "Success":"true"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

