# CreateGroupMetricRules

调用CreateGroupMetricRules接口批量为应用分组创建报警规则。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=CreateGroupMetricRules&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateGroupMetricRules|要执行的操作，取值：CreateGroupMetricRules。 |
|GroupId|Long|是|123456|应用分组ID。 |
|GroupMetricRules.N.Category|String|是|ecs|云服务名称。N的取值范围：1~200。取值：

 -   ecs：包括阿里云和非阿里云主机。
-   rds：云数据库RDS版。
-   ads：分析型数据库。
-   slb：负载均衡。
-   vpc：专有网络。
-   apigateway：API网关。
-   cdn：内容分发网络。
-   cs：容器服务Swarm版。
-   dcdn：全站加速。
-   ddos：DDoS防护。
-   eip：弹性公网IP。
-   elasticsearch：阿里云Elasticsearch。
-   emr：E-MapReduce。
-   ess：弹性伸缩。
-   hbase：云数据库 HBase。
-   iot\_edge：IoT边缘计算。
-   k8s\_pod：k8s pod。
-   kvstore\_sharding：Redis集群版。
-   kvstore\_splitrw：Redis读写分离版。
-   kvstore\_standard：Redis标准版。
-   memcache：云数据库 Memcache。
-   mns：消息服务。
-   mongodb：MongoDB副本实例。
-   mongodb\_cluster：MongoDB集群版本。
-   mongodb\_sharding：MongoDB分片集群。
-   mq\_topic：消息服务Topic。
-   ocs：旧版云数据库Memcache。
-   opensearch：开放搜索。
-   oss：对象存储OSS。
-   polardb：云数据库PolarDB。
-   petadata：HybridDB for MySQL。
-   scdn：安全加速。
-   sharebandwidthpackages：共享带宽包。
-   sls：日志服务。
-   vpn：VPN网关。 |
|GroupMetricRules.N.MetricName|String|是|cpu\_total|监控项名称。N的取值范围：1~200。

 **说明：** 详细信息请参见[DescribeMetricMetaList](~~98846~~)或[云服务监控项](~~163515~~)。 |
|GroupMetricRules.N.Namespace|String|是|acs\_ecs\_dashboard|云服务的数据命名空间。N的取值范围：1~200。

 **说明：** 详细信息请参见[DescribeMetricMetaList](~~98846~~)或[云服务监控项](~~163515~~)。 |
|GroupMetricRules.N.RuleId|String|是|bfae2ca5b4e07d2c7278772eccda169808c7b\*\*\*\*|报警规则ID。N的取值范围：1~200。 |
|GroupMetricRules.N.RuleName|String|是|ECS\_Rule1|报警规则名称。N的取值范围：1~200。 |
|GroupMetricRules.N.Dimensions|String|否|\[\{"instanceId":"i-m5e1qg6uo38rztr4\*\*\*\*"\}\]|扩展资源维度。N的取值范围：1~200。

 **说明：** 当您为应用分组设置报警规则时，会将该应用分组中的所有资源与该报警规则关联。该参数既可以设置实例，也可以设置更深一级的资源，例如，您需要在应用分组下设置所有实例根分区的磁盘使用率，可以设置为`[ {"dskName":"/"} ]`。 |
|GroupMetricRules.N.EffectiveInterval|String|否|00:00-23:59|报警规则的生效时间范围。N的取值范围：1~200。 |
|GroupMetricRules.N.NoEffectiveInterval|String|否|00:00-05:30|报警规则的非生效时间范围。N的取值范围：1~200。 |
|GroupMetricRules.N.SilenceTime|Integer|否|86400|报警通知的沉默周期。单位：秒，最小值：3600，默认值：86400。

 N的取值范围：1~200。 |
|GroupMetricRules.N.Period|String|否|60|监控数据的聚合周期。单位：秒，取值：60或60的整数倍。默认值：300。

 N的取值范围：1~200。

 **说明：** 该参数设置为300秒，表示将原始上报的5分钟内的监控数据的平均值作为报警参考点。 |
|GroupMetricRules.N.Interval|String|否|60|报警规则的探测周期。单位：秒，默认为监控项的最小频率。

 N的取值范围：1~200。

 **说明：** 建议报警的探测周期和数据上报周期保持一致。如果报警规则的探测周期小于数据上报周期，会因为数据不足而不能触发报警。 |
|GroupMetricRules.N.Webhook|String|否|https://www.aliyun.com|报警发生回调时指定的URL地址。N的取值范围：1~200。 |
|GroupMetricRules.N.EmailSubject|String|否|ECS\_Instance1|邮件主题。N的取值范围：1~200。 |
|GroupMetricRules.N.Escalations.Critical.Statistics|String|否|Average|Critical级别报警统计方法。N的取值范围：1~200。

 **说明：** 详细信息请参见[DescribeSystemEventMetaList](~~114972~~)。 |
|GroupMetricRules.N.Escalations.Critical.ComparisonOperator|String|否|GreaterThanOrEqualToThreshold|Critical级别阈值比较符。N的取值范围：1~200。取值：

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
|GroupMetricRules.N.Escalations.Critical.Threshold|String|否|90|Critical级别报警阈值。N的取值范围：1~200。 |
|GroupMetricRules.N.Escalations.Critical.Times|Integer|否|3|Critical级别报警重试次数。N的取值范围：1~200。 |
|GroupMetricRules.N.Escalations.Warn.Statistics|String|否|Average|Warn级别报警统计方法。N的取值范围：1~200。

 **说明：** 详细信息请参见[DescribeSystemEventMetaList](~~114972~~)。 |
|GroupMetricRules.N.Escalations.Warn.ComparisonOperator|String|否|GreaterThanOrEqualToThreshold|Warn级别阈值比较符。N的取值范围：1~200。取值：

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
|GroupMetricRules.N.Escalations.Warn.Threshold|String|否|90|Warn级别报警阈值。N的取值范围：1~200。 |
|GroupMetricRules.N.Escalations.Warn.Times|Integer|否|3|Warn级别报警重试次数。N的取值范围：1~200。 |
|GroupMetricRules.N.Escalations.Info.Statistics|String|否|Average|Info级别报警统计方法。N的取值范围：1~200。

 **说明：** 详细信息请参见[DescribeSystemEventMetaList](~~114972~~)。 |
|GroupMetricRules.N.Escalations.Info.ComparisonOperator|String|否|GreaterThanOrEqualToThreshold|Info级别阈值比较符。N的取值范围：1~200。取值：

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
|GroupMetricRules.N.Escalations.Info.Threshold|String|否|90|Info级别报警阈值。N的取值范围：1~200。 |
|GroupMetricRules.N.Escalations.Info.Times|Integer|否|3|Info级别报警重试次数。N的取值范围：1~200。 |

报警级别Critical、Warn和Info至少设置一种，否则创建报警规则失败。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|Integer|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The Request is not authorization.|错误信息。 |
|RequestId|String|461CF2CD-2FC3-4B26-8645-7BD27E7D0F1D|请求ID。 |
|Resources|Array of AlertResult| |创建资源列表。 |
|AlertResult| | | |
|Code|Integer|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|Metric not found.|错误信息。 |
|RuleId|String|a151cd6023eacee2f0978e03863cc1697c89508\*\*\*\*|报警规则ID。 |
|RuleName|String|ECS\_Rule1|报警规则名称。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=CreateGroupMetricRules
&GroupId=123456
&GroupMetricRules.1.Category=ecs
&GroupMetricRules.1.MetricName=cpu_total
&GroupMetricRules.1.1amespace=acs_ecs_dashboard
&GroupMetricRules.1.RuleId=bfae2ca5b4e07d2c7278772eccda169808c7b****
&GroupMetricRules.1.RuleName=ECS_Rule1
&GroupMetricRules.1.Escalations.Critical.Statistics=Average
&GroupMetricRules.1.Escalations.Critical.ComparisonOperator=GreaterThanOrEqualToThreshold
&GroupMetricRules.1.Escalations.Critical.Threshold=90
&GroupMetricRules.1.Escalations.Critical.Times=3
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<CreateGroupMetricRulesResponse>
	  <RequestId>65D50468-ECEF-48F1-A6E1-D952E89D9436</RequestId>
	  <Success>true</Success>
	  <Code>200</Code>
	  <Resources>
		    <AlertResult>
			      <RuleId>a151cd6023eacee2f0978e03863cc1697c89508****</RuleId>
			      <Success>true</Success>
			      <RuleName>ECS_Rule1</RuleName>
			      <Code>200</Code>
		    </AlertResult>
		    <AlertResult>
			      <Message>Metric not found.</Message>
			      <RuleId>hyu91929****</RuleId>
			      <Success>false</Success>
			      <RuleName>ECS_Rule2</RuleName>
			      <Code>404</Code>
		    </AlertResult>
	  </Resources>
</CreateGroupMetricRulesResponse>
```

`JSON` 格式

```
{
    "RequestId": "65D50468-ECEF-48F1-A6E1-D952E89D9436",
    "Success": "true",
    "Code": "200",
    "Resources": {
        "AlertResult": [
            {
                "RuleId": "a151cd6023eacee2f0978e03863cc1697c89508****",
                "Success": "true",
                "RuleName": "ECS_Rule1",
                "Code": "200"
            },
            {
                "Message": "Metric not found.",
                "RuleId": "hyu91929****",
                "Success": "false",
                "RuleName": "ECS_Rule2",
                "Code": "404"
            }
        ]
    }
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

