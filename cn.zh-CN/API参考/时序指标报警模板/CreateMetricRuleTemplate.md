# CreateMetricRuleTemplate

调用CreateMetricRuleTemplate接口创建报警模板。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=CreateMetricRuleTemplate&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateMetricRuleTemplate|要执行的操作，取值：CreateMetricRuleTemplate。 |
|Name|String|是|Template1|报警模板名称。 |
|AlertTemplates.N.MetricName|String|是|cpu\_total|监控项名称。N的取值范围：1~200。

 **说明：** 详情请参见[DescribeMetricMetaList](~~98846~~)或[云服务监控项](~~28619~~)。 |
|AlertTemplates.N.RuleName|String|是|我的CPU监控|报警规则名称。N的取值范围：1~200。 |
|AlertTemplates.N.Category|String|是|ecs|阿里云服务名称或产品规格缩写。N的取值范围：1~200。取值：

 -   ecs：阿里云主机和非阿里云主机。
-   rds：云数据库RDS版。
-   ads：分析型数据库。
-   slb：负载均衡。
-   vpc：弹性IP。
-   apigateway：API网关。
-   cdn：内容分发网络。
-   cs：容器服务Swarm版。
-   dcdn：全站加速。
-   ddos：DDoS防护。
-   eip：弹性公网IP。
-   elasticsearch：elasticsearch。
-   emr：E-MapReduce。
-   ess：弹性伸缩。
-   hbase：云数据库HBase。
-   iot\_edge：IoT边缘计算。
-   k8s\_pod：k8s pod。
-   kvstore\_sharding：Redis集群版。
-   kvstore\_splitrw：Redis读写分离版。
-   kvstore\_standard：Redis标准版。
-   memcache：云数据库Memcache。
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
|AlertTemplates.N.Namespace|String|是|acs\_ecs\_dashboard|阿里云服务的数据命名空间。N的取值范围：1~200。

 **说明：** 详情请参见[DescribeMetricMetaList](~~98846~~)或[云服务监控项](~~28619~~)。 |
|Description|String|否|ECS\_Template1|报警模板描述信息。 |
|AlertTemplates.N.Period|Integer|否|60|监控数据的聚合周期。单位：秒。

 默认为监控项对应的最小周期，通常不需要指定。

 N的取值范围：1~200。 |
|AlertTemplates.N.Selector|String|否|\{"disk":"/"\}|扩展字段选项。N的取值范围：1~200。 |
|AlertTemplates.N.Escalations.Critical.Statistics|String|否|Average|Critical级别统计方法。N的取值范围：1~200。 |
|AlertTemplates.N.Escalations.Critical.ComparisonOperator|String|否|GreaterThanOrEqualToThreshold|Critical级别阈值比较符。N的取值范围：1~200。取值：

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
|AlertTemplates.N.Escalations.Critical.Threshold|String|否|90|Critical级别报警阈值。N的取值范围：1~200。 |
|AlertTemplates.N.Escalations.Critical.Times|Integer|否|3|Critical级别报警重试次数。N的取值范围：1~200。 |
|AlertTemplates.N.Escalations.Warn.Statistics|String|否|Average|Warn级别报警统计方法。N的取值范围：1~200。 |
|AlertTemplates.N.Escalations.Warn.ComparisonOperator|String|否|GreaterThanOrEqualToThreshold|Wran级别阈值比较符。N的取值范围：1~200。取值：

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
|AlertTemplates.N.Escalations.Warn.Threshold|String|否|90|Warn级别报警阈值。N的取值范围：1~200。 |
|AlertTemplates.N.Escalations.Warn.Times|Integer|否|3|Warn级别报警重试次数。N的取值范围：1~200。 |
|AlertTemplates.N.Escalations.Info.Statistics|String|否|Average|Info级别报警统计方法。N的取值范围：1~200。 |
|AlertTemplates.N.Escalations.Info.ComparisonOperator|String|否|GreaterThanOrEqualToThreshold|Info级别阈值比较符。N的取值范围：1~200。取值：

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
|AlertTemplates.N.Escalations.Info.Threshold|String|否|90|Info级别报警阈值。N的取值范围：1~200。 |
|AlertTemplates.N.Escalations.Info.Times|Integer|否|3|Info级别报警重试次数。N的取值范围：1~200。 |
|AlertTemplates.N.Webhook|String|否|http://ww.aliyun.com|报警发生时回调指定的URL地址。向URL发送POST请求。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|9763ED1A-4D09-41BF-851E-310421750204|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Code|Integer|200|状态码。

 **说明：** 200表示成功。 |
|Id|Long|12345|报警模板ID。 |
|Message|String|The Request is not authorization.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=CreateMetricRuleTemplate
&Name=Template1
&AlertTemplates.1.MetricName=cpu_total
&AlertTemplates.1.RuleName=我的CPU监控
&AlertTemplates.1.Category=ecs
&AlertTemplates.1.1amespace=acs_ecs_dashboard
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<CreateMetricRuleTemplateResponse>
		  <RequestId>9763ED1A-4D09-41BF-851E-310421750204</RequestId>
		  <Id>12345</Id>
		  <Success>true</Success>
		  <Code>200</Code>
</CreateMetricRuleTemplateResponse>
```

`JSON` 格式

```
{
    "RequestId": "9763ED1A-4D09-41BF-851E-310421750204",
    "Id": 12345,
    "Success": true,
    "Code": 200
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

