# PutGroupMetricRule

调用PutGroupMetricRule接口创建或修改应用分组的报警规则。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=PutGroupMetricRule&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|PutGroupMetricRule|要执行的操作，取值：PutGroupMetricRule。 |
|Category|String|是|ecs|云服务名称缩写。N的取值范围：1~200。取值：

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
|GroupId|String|是|123456|应用分组ID。 |
|MetricName|String|是|cpu\_total|监控项名称。详情请参见[云服务监控项](~~163515~~)。 |
|Namespace|String|是|acs\_ecs\_dashboard|产品的数据命名空间。详情请参见[云服务监控项](~~163515~~)。 |
|RuleId|String|是|bfae2ca5b4e07d2c7278772eccda169808c7b\*\*\*\*|报警规则ID。 |
|RuleName|String|否|rule1|报警规则名称。 |
|Dimensions|String|否|\[\{"instanceId":"xxxxxx"\}\]|维度Map，用于查询指定资源的监控数据。

 格式为：key-value键值对形式的集合，常用的key-value集合为：`instanceId:XXXXXX`。

 Key和Value的长度为1~64个字节，超过64个字节时截取前64字节。

 Key和Value的取值可包含英文字母、数字、英文句点（.）、短划线（-）、下划线（\_）、正斜线（/）和反斜线（\\）。

 **说明：** Dimensions传入时需要使用JSON字符串表示该Map对象，必须按顺序传入。 |
|EffectiveInterval|String|否|00:00-23:59|报警规则的生效时间范围。 |
|NoEffectiveInterval|String|否|00:00-05:30|报警规则的非生效时间范围。 |
|SilenceTime|Integer|否|86400|通道沉默周期，单位：秒，默认值：86400秒（1天）。 |
|Period|String|否|60|监控数据的聚合周期。单位：秒。取值为60或60的整数倍。默认值：300秒。 |
|Interval|String|否|60|报警规则的探测周期。单位：秒。

 **说明：** 建议报警的探测周期和数据上报周期保持一致。如果报警规则的探测周期小于数据上报周期，会因为数据不足而不能触发报警。 |
|Webhook|String|否|http://www.aliyun.com|报警发生回调时指定的URL地址。 |
|EmailSubject|String|否|ECS实例|报警邮件主题。 |
|Escalations.Critical.Statistics|String|否|Average|Critical级别报警统计方法。

 **说明：** 详情请参见[DescribeMetricMetaList](~~98846~~)。 |
|Escalations.Critical.ComparisonOperator|String|否|GreaterThanOrEqualToThreshold|Critical级别阈值比较符。取值：

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
|Escalations.Critical.Threshold|String|否|90|Critical级别报警阈值。 |
|Escalations.Critical.Times|Integer|否|3|Critical级别报警重试次数。 |
|Escalations.Warn.Statistics|String|否|Average|Warn级别报警统计方法。

 **说明：** 详情请参见[DescribeMetricMetaList](~~98846~~)。 |
|Escalations.Warn.ComparisonOperator|String|否|GreaterThanOrEqualToThreshold|Warn级别阈值比较符。取值：

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
|Escalations.Warn.Threshold|String|否|90|Warn级别报警阈值。 |
|Escalations.Warn.Times|Integer|否|3|Warn级别报警重试次数。 |
|Escalations.Info.Statistics|String|否|Average|Info级别报警统计方法。

 **说明：** 详情请参见[DescribeMetricMetaList](~~98846~~)。 |
|Escalations.Info.ComparisonOperator|String|否|GreaterThanOrEqualToThreshold|Info级别阈值比较符。取值：

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
|Escalations.Info.Threshold|String|否|90|Info级别报警阈值。 |
|Escalations.Info.Times|Integer|否|3|Info级别报警重试次数。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|461CF2CD-2FC3-4B26-8645-7BD27E7D0F1D|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The Request is not authorization.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=PutGroupMetricRule
&Category=ecs
&GroupId=123456
&MetricName=cpu_total
&Namespace=acs_ecs_dashboard
&RuleId=bfae2ca5b4e07d2c7278772eccda169808c7b****
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<PutGroupMetricRuleResponse>
	  <RequestId>26C766DE-E759-4B38-8B23-28589C491CEF</RequestId>
	  <Code>200</Code>
	  <Success>true</Success>
</PutGroupMetricRuleResponse>
```

`JSON` 格式

```
{
    "RequestId":"26C766DE-E759-4B38-8B23-28589C491CEF",
    "Code":200,
    "Success":true
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

