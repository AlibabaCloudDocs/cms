# DescribeActiveMetricRuleList

调用DescribeActiveMetricRuleList接口查询一键报警规则的列表详情。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeActiveMetricRuleList&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeActiveMetricRuleList|要执行的操作，取值：DescribeActiveMetricRuleList。 |
|Product|String|是|ecs|云服务名称缩写。目前支持的云服务如下：

 -   ecs：云服务器ECS。
-   rds：云数据库RDS版。
-   slb：负载均衡。
-   redis\_standard：云数据库Redis标准版。
-   redis\_sharding：云数据库Redis集群版。
-   redis\_splitrw：云数据库Redis读写分离版。
-   mongodb：云数据库MongoDB版（副本集）。
-   mongodb\_sharding：云数据库MongoDB版（分片集群）。
-   hbase：云数据库HBase版。
-   elasticsearch：Elasticsearch。
-   opensearch：OpenSearch。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|AlertList|Array of Alert| |报警规则列表。该列表的结构和获取报警规则列表保持统一。 |
|Alert| | | |
|AlertState|String|OK|报警规则状态。取值：

 -   OK：正常。
-   ALARM：报警。
-   INSUFFICIENT\_DATA：无数据。 |
|ContactGroups|String|ECS\_Group|报警联系人组。 |
|Dimensions|String|""|维度Map，用于查询指定资源的监控数据。

 格式为：key-value键值对形式的集合。常用的key-value集合为：`instanceId:XXXXXX`。

 Key和Value的长度为1~64个字节，超过64个字节时截取前64字节。

 Key和Value的取值可包含英文字母、数字、英文句点（.）、短划线（-）、下划线（\_）、正斜线（/）和反斜线（\\）。

 **说明：** Dimensions传入时需要使用JSON字符串表示该Map对象，必须按顺序传入。 |
|EffectiveInterval|String|00:00-23:59|报警规则的生效时间段。 |
|EnableState|Boolean|true|报警规则的启用状态。取值：

 -   true：启用。
-   false：禁用。 |
|Escalations|Struct| |报警分级别触发条件。 |
|Critical|Struct| |Critical级别报警触发条件。 |
|ComparisonOperator|String|GreaterThanThreshold|Critical级别阈值比较符。取值：

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
|Statistics|String|Average|Critical级别报警统计方法。 |
|Threshold|String|99|Critical级别阈值。 |
|Times|String|3|Critical级别连续出现次数。Critical级别连续出现达到该值且超过阈值才会触发报警。 |
|Info|Struct| |Info级别报警触发条件。 |
|ComparisonOperator|String|GreaterThanThreshold|Info级别阈值比较符。取值：

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
|Statistics|String|Average|Info级别报警统计方法。 |
|Threshold|String|95|Info级别阈值。 |
|Times|String|3|Info级别连续出现次数。Info级别连续出现达到该值且超过阈值才会触发报警。 |
|Warn|Struct| |Wan级别报警触发条件。 |
|ComparisonOperator|String|GreaterThanThreshold|Critical级别阈值比较符。取值：

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
|Statistics|String|Average|Warn级别报警统计方法。 |
|Threshold|String|80|Warn级别阈值。 |
|Times|String|3|Wan级别连续出现次数。Wan级别连续出现达到该值且超过阈值才会触发报警。 |
|MailSubject|String|ECS\_Bucket|发送邮件的主题。 |
|MetricName|String|cpu\_total|监控项的名称。 |
|Namespace|String|acs\_ecs\_dashboard|云服务的命名空间。请参考[云服务主要监控项](~~163515~~)。 |
|NoEffectiveInterval|String|00:00-06:00|报警不生效的时间段。 |
|Period|String|60|监控数据的聚合周期。单位：秒。默认取值为监控项对应的最小频率，通常不需要指定。 |
|Resources|String|\[\{"resource":"\_ALL"\}\]|报警规则关联的资源。 一键报警关联所有的资源，该结果目前是固定取值。 |
|RuleId|String|ruleIdxxxx|报警规则ID。 |
|RuleName|String|myAlert|报警规则名称。 |
|SilenceTime|String|86400|通道沉默时间。单位：秒， 默认：86400。 |
|Webhook|String|http://www.aliyun.com|URL回调地址。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Datapoints|Array of Alarm| |报警规则列表。 |
|Alarm| | | |
|ComparisonOperator|String|\>|报警规则比较符。取值：

 -   `>`
-   `<`
-   `>=`
-   `<=`
-   `=`
-   `=` |
|ContactGroups|String|ECS\_Group|报警联系人组。 |
|Enable|String|true|报警规则的启用状态。取值：

 -   true：启用。
-   false：禁用。 |
|EndTime|String|24|报警规则失效时间。单位：小时。例如：23表示`23:59:59`。 |
|EvaluationCount|String|3|重试次数。 |
|MetricName|String|cpu\_total|监控项名称。 |
|Namespace|String|acs\_ecs\_dashboard|云服务的命名空间。请参考[云服务主要监控项](~~163515~~)。 |
|Period|String|60|监控数据的聚合周期。单位：秒。默认取值为监控项对应的最小频率，通常不需要指定。 |
|RuleId|String|a151cd6023eacee2f0978e03863cc1697c89508\*\*\*\*|报警规则ID。 |
|RuleName|String|SystemDefault\_acs\_rds\_dashboard\_CpuUsage|报警规则名称。 |
|SilenceTime|String|86400|通道沉默时间。单位：秒， 默认：86400。 |
|StartTime|String|00|报警规则生效起始时间。单位：小时。例如：00表示`00：00：00`。 |
|State|String|Enable|报警规则的启用状态。 |
|Statistics|String|Average|统计方法。 |
|Threshold|String|90|报警阈值。 |
|Webhook|String|http://www.aliyun.com|URL回调地址。 |
|Message|String|The Request is not authorization.|错误信息。 |
|RequestId|String|F82E6667-7811-4BA0-842F-5B2DC42BBAAD|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeActiveMetricRuleList
&Product=ecs
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeActiveMetricRuleListResponse>
		  <AlertList>
			    <Alert>
				      <SilenceTime>86400</SilenceTime>
				      <ContactGroups>ECS_Group</ContactGroups>
				      <NoEffectiveInterval></NoEffectiveInterval>
				      <MailSubject>${serviceType}-${metricName}-${levelDescription}</MailSubject>
				      <RuleId>SystemDefault_acs_rds_dashboard_IOPSUsage</RuleId>
				      <Period>300</Period>
				      <Dimensions></Dimensions>
				      <EffectiveInterval></EffectiveInterval>
				      <Namespace>acs_rds_dashboard</Namespace>
				      <AlertState>INSUFFICIENT_DATA</AlertState>
				      <MetricName>IOPSUsage</MetricName>
				      <EnableState>true</EnableState>
				      <Escalations>
					        <Critical></Critical>
					        <Info>
						          <ComparisonOperator>GreaterThanThreshold</ComparisonOperator>
						          <Times>5</Times>
						          <Statistics>Average</Statistics>
						          <Threshold>80</Threshold>
					        </Info>
					        <Warn></Warn>
				      </Escalations>
				      <Webhook></Webhook>
				      <Resources>[{\"resource\":\"_ALL\"}]</Resources>
				      <RuleName>SystemDefault_acs_rds_dashboard_IOPSUsage</RuleName>
			    </Alert>
			    <Alert>
				      <SilenceTime>86400</SilenceTime>
				      <ContactGroups>ECS_Group</ContactGroups>
				      <NoEffectiveInterval></NoEffectiveInterval>
				      <MailSubject>${serviceType}-${metricName}-${levelDescription}</MailSubject>
				      <RuleId>SystemDefault_acs_rds_dashboard_CpuUsage</RuleId>
				      <Period>300</Period>
				      <Dimensions></Dimensions>
				      <EffectiveInterval></EffectiveInterval>
				      <Namespace>acs_rds_dashboard</Namespace>
				      <AlertState>INSUFFICIENT_DATA</AlertState>
				      <MetricName>CpuUsage</MetricName>
				      <EnableState>true</EnableState>
				      <Escalations>
					        <Critical></Critical>
					        <Info>
						          <ComparisonOperator>GreaterThanThreshold</ComparisonOperator>
						          <Times>5</Times>
						          <Statistics>Average</Statistics>
						          <Threshold>80</Threshold>
					        </Info>
					        <Warn></Warn>
				      </Escalations>
				      <Webhook></Webhook>
				      <Resources>[{\"resource\":\"_ALL\"}]</Resources>
				      <RuleName>SystemDefault_acs_rds_dashboard_CpuUsage</RuleName>
			    </Alert>
		  </AlertList>
		  <Datapoints>
			    <Alarm>
				      <SilenceTime>86400</SilenceTime>
				      <ContactGroups>[\"Alice\"]</ContactGroups>
				      <ComparisonOperator>GreaterThanThreshold</ComparisonOperator>
				      <EndTime></EndTime>
				      <RuleId>SystemDefault_acs_rds_dashboard_IOPSUsage</RuleId>
				      <StartTime></StartTime>
				      <Period>300</Period>
				      <EvaluationCount>5</EvaluationCount>
				      <Statistics>Average</Statistics>
				      <Namespace>acs_rds_dashboard</Namespace>
				      <MetricName>IOPSUsage</MetricName>
				      <State>INSUFFICIENT_DATA</State>
				      <Enable>true</Enable>
				      <Webhook></Webhook>
				      <RuleName>SystemDefault_acs_rds_dashboard_IOPSUsage</RuleName>
				      <Threshold>80</Threshold>
			    </Alarm>
			    <Alarm>
				      <SilenceTime>86400</SilenceTime>
				      <ContactGroups>[\"Jim\"]</ContactGroups>
				      <ComparisonOperator>GreaterThanThreshold</ComparisonOperator>
				      <EndTime></EndTime>
				      <RuleId>SystemDefault_acs_rds_dashboard_CpuUsage</RuleId>
				      <StartTime></StartTime>
				      <Period>300</Period>
				      <EvaluationCount>5</EvaluationCount>
				      <Statistics>Average</Statistics>
				      <Namespace>acs_rds_dashboard</Namespace>
				      <MetricName>CpuUsage</MetricName>
				      <State>INSUFFICIENT_DATA</State>
				      <Enable>true</Enable>
				      <Webhook></Webhook>
				      <RuleName>SystemDefault_acs_rds_dashboard_CpuUsage</RuleName>
				      <Threshold>80</Threshold>
			    </Alarm>
		  </Datapoints>
		  <Code>200</Code>
		  <Success>true</Success>
</DescribeActiveMetricRuleListResponse>
```

`JSON` 格式

```
{
    "AlertList": {
        "Alert": [
            {
                "SilenceTime": 86400,
                "ContactGroups": "ECS_Group",
                "NoEffectiveInterval": "",
                "MailSubject": "${serviceType}-${metricName}-${levelDescription}",
                "RuleId": "SystemDefault_acs_rds_dashboard_IOPSUsage",
                "Period": 300,
                "Dimensions": "",
                "EffectiveInterval": "",
                "Namespace": "acs_rds_dashboard",
                "AlertState": "INSUFFICIENT_DATA",
                "MetricName": "IOPSUsage",
                "EnableState": true,
                "Escalations": {
                    "Critical": {},
                    "Info": {
                        "ComparisonOperator": "GreaterThanThreshold",
                        "Times": 5,
                        "Statistics": "Average",
                        "Threshold": "80"
                    },
                    "Warn": {}
                },
                "Webhook": "",
                "Resources": "[{\"resource\":\"_ALL\"}]",
                "RuleName": "SystemDefault_acs_rds_dashboard_IOPSUsage"
            },
            {
                "SilenceTime": 86400,
                "ContactGroups": "ECS_Group",
                "NoEffectiveInterval": "",
                "MailSubject": "${serviceType}-${metricName}-${levelDescription}",
                "RuleId": "SystemDefault_acs_rds_dashboard_CpuUsage",
                "Period": 300,
                "Dimensions": "",
                "EffectiveInterval": "",
                "Namespace": "acs_rds_dashboard",
                "AlertState": "INSUFFICIENT_DATA",
                "MetricName": "CpuUsage",
                "EnableState": true,
                "Escalations": {
                    "Critical": {},
                    "Info": {
                        "ComparisonOperator": "GreaterThanThreshold",
                        "Times": 5,
                        "Statistics": "Average",
                        "Threshold": "80"
                    },
                    "Warn": {}
                },
                "Webhook": "",
                "Resources": "[{\"resource\":\"_ALL\"}]",
                "RuleName": "SystemDefault_acs_rds_dashboard_CpuUsage"
            } 
        ]
    },
    "Datapoints": {
        "Alarm": [
            {
                "SilenceTime": 86400,
                "ContactGroups": "[\"Alice\"]",
                "ComparisonOperator": "GreaterThanThreshold",
                "EndTime": "",
                "RuleId": "SystemDefault_acs_rds_dashboard_IOPSUsage",
                "StartTime": "",
                "Period": 300,
                "EvaluationCount": 5,
                "Statistics": "Average",
                "Namespace": "acs_rds_dashboard",
                "MetricName": "IOPSUsage",
                "State": "INSUFFICIENT_DATA",
                "Enable": true,
                "Webhook": "",
                "RuleName": "SystemDefault_acs_rds_dashboard_IOPSUsage",
                "Threshold": "80"
            },
            {
                "SilenceTime": 86400,
                "ContactGroups": "[\"Jim\"]",
                "ComparisonOperator": "GreaterThanThreshold",
                "EndTime": "",
                "RuleId": "SystemDefault_acs_rds_dashboard_CpuUsage",
                "StartTime": "",
                "Period": 300,
                "EvaluationCount": 5,
                "Statistics": "Average",
                "Namespace": "acs_rds_dashboard",
                "MetricName": "CpuUsage",
                "State": "INSUFFICIENT_DATA",
                "Enable": true,
                "Webhook": "",
                "RuleName": "SystemDefault_acs_rds_dashboard_CpuUsage",
                "Threshold": "80"
            } 
        ]
    },
    "Code": "200",
    "Success": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

