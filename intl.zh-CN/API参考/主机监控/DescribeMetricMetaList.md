# DescribeMetricMetaList

调用DescribeMetricMetaList接口查询云监控开放的时序类指标监控项描述。

通常配合查询监控数据接口DescribeMetricList和DescribeMetricLast一起使用，详情请参见[DescribeMetricList](~~51936~~)和[DescribeMetricLast](~~51939~~)。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeMetricMetaList&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeMetricMetaList|系统规定参数，取值：DescribeMetricMetaList。 |
|Namespace|String|否|acs\_kvstore|指标所属的Namespace，用于区分每个产品配置。

 详情请参见[云产品监控项](~~163515~~)。 |
|Labels|String|否|\[\{"name":"productCategory","value":"kvstore\_old"\}\]|根据标签过滤。是一个JSON的字符串。

 格式：`[{"name":"标签名","value":"标签值"},{"name":"标签名","value":"标签值"}]`。已有标签说明如下：

 -   metricCategory：监控项分类的描述。
-   alertEnable：是否需要报警。
-   alertUnit：建议的报警单位。
-   unitFactor：单位转换系数。
-   minAlertPeriod：最小报警周期。
-   productCategory：产品类型分类。 |
|MetricName|String|否|CPUUtilization|监控项名称。详情请参见[云产品监控项](~~163515~~)。 |
|PageNumber|Integer|否|1|分页参数。默认值：1。 |
|PageSize|Integer|否|30|每页最大数量。默认值：30。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Success|Boolean|true|操作是否成功。true表示成功，false表示失败。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|RequestId|String|0CCE0AF0-053C-4B13-A583-DC9A85785D49|请求ID。 |
|Message|String|The Request is not authorization.|错误信息。 |
|Resources|Array| |指定监控项的配置信息。 |
|Resource| | | |
|Description|String|CPUUtilization|监控项描述。 |
|Dimensions|String|instanceId|监控项的Dimensions。多个用英文逗号（,）分隔。 |
|Labels|String|\[\{\\"name\\":\\"alertUnit\\",\\"value\\":\\"Bytes\\"\},\{\\"name\\":\\"minAlertPeriod\\",\\"value\\":\\"60\\"\},\{\\"name\\":\\"metricCategory\\",\\"value\\":\\"instanceId\\"\},\{\\"name\\":\\"instanceType\\",\\"value\\":\\"disaster\\"\},\{\\"name\\":\\"is\_alarm\\",\\"value\\":\\"true\\"\},\{\\"name\\":\\"productCategory\\",\\"value\\":\\"kvstore\_old\\"\}\]|监控项的标签，是一个或多个JSON字符串。格式：`[{"name":"标签名","value":"标签的值"}]`，`name`可以重复，

 已有标签说明如下：

 -   metricCategory：监控项分类的描述。
-   alertEnable：是否需要报警。
-   alertUnit：建议的报警单位。
-   unitFactor：单位转换系数。
-   minAlertPeriod：最小报警周期。
-   productCategory：产品类型分类。 |
|MetricName|String|CPUUtilization|监控项名称。 |
|Namespace|String|acs\_kvstore|用于区分产品类型。通常的命名方式为acs\_产品名。 |
|Periods|String|60,300|监控项的所有统计周期。多个用英文逗号（,）分隔。 |
|Statistics|String|Average,Minimum,Maximum|统计方法。多个用英文逗号（,）分隔。 |
|Unit|String|%|监控项的单位。 |
|TotalCount|String|12|总记录条数。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeMetricMetaList
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeMetricMetaListResponse>
		  <TotalCount>1853</TotalCount>
		  <RequestId>CDE9EAFF-D54E-4024-BBFC-B0AAC883143B</RequestId>
		  <Success>true</Success>
		  <Code>200</Code>
		  <Resources>
			    <Resource>
				      <Description>磁盘额定容量</Description>
				      <Statistics>Average,Minimum,Maximum</Statistics>
				      <MetricName>ads.diskSize</MetricName>
				      <Labels>[{\"name\":\"minAlertPeriod\",\"value\":\"300\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"name\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"Mbytes\"},{\"name\":\"productCategory\",\"value\":\"ads\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"workerId\"}]</Labels>
				      <Dimensions>userId,instanceId,tableSchema,workerId</Dimensions>
				      <Namespace>acs_ads</Namespace>
				      <Periods>300</Periods>
				      <Unit>MB</Unit>
			    </Resource>
			    <Resource>
				      <Description>磁盘已用容量</Description>
				      <Statistics>Average,Minimum,Maximum</Statistics>
				      <MetricName>ads.diskUsed</MetricName>
				      <Labels>[{\"name\":\"alertUnit\",\"value\":\"Mbytes\"},{\"name\":\"minAlertPeriod\",\"value\":\"300\"},{\"name\":\"metricCategory\",\"value\":\"workerId\"},{\"name\":\"is_alarm\",\"value\":\"true\"}]</Labels>
				      <Dimensions>userId,instanceId,tableSchema,workerId</Dimensions>
				      <Namespace>acs_ads</Namespace>
				      <Periods>300</Periods>
				      <Unit>MB</Unit>
			    </Resource>
			    <Resource>
				      <Description>磁盘使用率</Description>
				      <Statistics>Average,Minimum,Maximum</Statistics>
				      <MetricName>ads.diskUsedPercent</MetricName>
				      <Labels>[{\"name\":\"alertUnit\",\"value\":\"%\"},{\"name\":\"minAlertPeriod\",\"value\":\"300\"},{\"name\":\"metricCategory\",\"value\":\"workerId\"},{\"name\":\"is_alarm\",\"value\":\"true\"}]</Labels>
				      <Dimensions>userId,instanceId,tableSchema,workerId</Dimensions>
				      <Namespace>acs_ads</Namespace>
				      <Periods>300</Periods>
				      <Unit>%</Unit>
			    </Resource>
			    <Resource>
				      <Description>queue的未消费的消息数目</Description>
				      <Statistics>Maximum</Statistics>
				      <MetricName>QueueMessageAccumulation</MetricName>
				      <Labels>[{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"name\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"count/min\"},{\"name\":\"productCategory\",\"value\":\"amqp\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"queue\"}]</Labels>
				      <Dimensions>userId,regionId,vhostName,queueName</Dimensions>
				      <Namespace>acs_amqp</Namespace>
				      <Periods>60,300</Periods>
				      <Unit>count/min</Unit>
			    </Resource>
			    <Resource>
				      <Description>queue每分钟消息生产量</Description>
				      <Statistics>Value</Statistics>
				      <MetricName>QueueMessageInput</MetricName>
				      <Labels>[{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"n ame\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"count/min\"},{\"name\":\"productCategory\",\"value\":\"amqp\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"queue\"}]</Labels>
				      <Dimensions>userId,regionId,vhostName,queueName</Dimensions>
				      <Namespace>acs_amqp</Namespace>
				      <Periods>60,300</Periods>
				      <Unit>count/min</Unit>
			    </Resource>
			    <Resource>
				      <Description>queue的未消费的消息数目</Description>
				      <Statistics>Value</Statistics>
				      <MetricName>QueueMessageOutput</MetricName>
				      <Labels>[{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"name\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"count/min\"},{\"name\":\"productCategory\",\"value\":\"amqp\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"queue\"}]</Labels>
				      <Dimensions>userId,regionId,vhostName,queueName</Dimensions>
				      <Namespace>acs_amqp</Namespace>
				      <Periods>60,300</Periods>
				      <Unit>count/min</Unit>
			    </Resource>
			    <Resource>
				      <Description>实例每分钟产生的消息数量</Description>
				      <Statistics>Value</Statistics>
				      <MetricName>VhostMessageInput</MetricName>
				      <Labels>[{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"name\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"count/min\"},{\"name\":\"productCategory\",\"value\":\"amqp\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"vhost\"}]</Labels>
				      <Dimensions>userId,regionId,vhostName</Dimensions>
				      <Namespace>acs_amqp</Namespace>
				      <Periods>60,300</Periods>
				      <Unit>count/min</Unit>
			    </Resource>
			    <Resource>
				      <Description>实例每分钟消费的消息数量</Description>
				      <Statistics>Value</Statistics>
				      <MetricName>VhostMessageOutput</MetricName>
				      <Labels>[{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"name\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"count/min\"},{\"name\":\"productCategory\",\"value\":\"amqp\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"vhost\"}]</Labels>
				      <Dimensions>userId,regionId,vhostName</Dimensions>
				      <Namespace>acs_amqp</Namespace>
				      <Periods>60,300</Periods>
				      <Unit>count/min</Unit>
			    </Resource>
			    <Resource>
				      <Description></Description>
				      <Statistics>Average</Statistics>
				      <MetricName>Latency</MetricName>
				      <Labels>[{\"name\":\"alertUnit\",\"value\":\"ms\"},{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"metricCategory\",\"value\":\"instanceId\"},{\"name\":\"is_alarm\",\"value\":\"true\"}]</Labels>
				      <Dimensions>userId,region,apiUid</Dimensions>
				      <Namespace>acs_apigateway_dashboard</Namespace>
				      <Periods>60,300,900</Periods>
				      <Unit>ms</Unit>
			    </Resource>
			    <Resource>
				      <Description>时间粒度内http返回码4XX占全部返回码的百分比</Description>
				      <Statistics>Average,Minimum,Maximum</Statistics>
				      <MetricName>code4xx</MetricName>
				      <Labels>[{\"name\":\"alertUnit\",\"value\":\"%\"},{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"metricCategory\",\"value\":\"instanceId\"},{\"name\":\"is_alarm\",\"value\":\"true\"}]</Labels>
				      <Dimensions>userId,instanceId</Dimensions>
				      <Namespace>acs_cdn</Namespace>
				      <Periods>60,300</Periods>
				      <Unit>%</Unit>
			    </Resource>
		  </Resources>
</DescribeMetricMetaListResponse>
```

`JSON` 格式

```
{
        "TotalCount":  1853,
        "RequestId":  "CDE9EAFF-D54E-4024-BBFC-B0AAC883143B",
        "Success":  true,
        "Code":  200,
        "Resources":  {
                "Resource":  [
                        {
                                "Description":  "磁盘额定容量",
                                "Statistics":  "Average,Minimum,Maximum",
                                "MetricName":  "ads.diskSize",
                                "Labels":  "[{\"name\":\"minAlertPeriod\",\"value\":\"300\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"name\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"Mbytes\"},{\"name\":\"productCategory\",\"value\":\"ads\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"workerId\"}]",
                                "Dimensions":  "userId,instanceId,tableSchema,workerId",
                                "Namespace":  "acs_ads",
                                "Periods":  "300",
                                "Unit":  "MB"
                        },
                        {
                                "Description":  "磁盘已用容量",
                                "Statistics":  "Average,Minimum,Maximum",
                                "MetricName":  "ads.diskUsed",
                                "Labels":  "[{\"name\":\"alertUnit\",\"value\":\"Mbytes\"},{\"name\":\"minAlertPeriod\",\"value\":\"300\"},{\"name\":\"metricCategory\",\"value\":\"workerId\"},{\"name\":\"is_alarm\",\"value\":\"true\"}]",
                                "Dimensions":  "userId,instanceId,tableSchema,workerId",
                                "Namespace":  "acs_ads",
                                "Periods":  "300",
                                "Unit":  "MB"
                        },
                        {
                                "Description":  "磁盘使用率",
                                "Statistics":  "Average,Minimum,Maximum",
                                "MetricName":  "ads.diskUsedPercent",
                                "Labels":  "[{\"name\":\"alertUnit\",\"value\":\"%\"},{\"name\":\"minAlertPeriod\",\"value\":\"300\"},{\"name\":\"metricCategory\",\"value\":\"workerId\"},{\"name\":\"is_alarm\",\"value\":\"true\"}]",
                                "Dimensions":  "userId,instanceId,tableSchema,workerId",
                                "Namespace":  "acs_ads",
                                "Periods":  "300",
                                "Unit":  "%"
                        },
                        {
                                "Description":  "queue的未消费的消息数目",
                                "Statistics":  "Maximum",
                                "MetricName":  "QueueMessageAccumulation",
                                "Labels":  "[{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"name\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"count/min\"},{\"name\":\"productCategory\",\"value\":\"amqp\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"queue\"}]",
                                "Dimensions":  "userId,regionId,vhostName,queueName",
                                "Namespace":  "acs_amqp",
                                "Periods":  "60,300",
                                "Unit":  "count/min"
                        },
                        {
                                "Description":  "queue每分钟消息生产量",
                                "Statistics":  "Value",
                                "MetricName":  "QueueMessageInput",
                                "Labels":  "[{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"n ame\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"count/min\"},{\"name\":\"productCategory\",\"value\":\"amqp\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"queue\"}]",
                "Dimensions": "userId,regionId,vhostName,queueName",
                "Namespace": "acs_amqp",
                "Periods": "60,300",
                "Unit": "count/min"
            },
            {
                "Description": "queue的未消费的消息数目",
                "Statistics": "Value",
                "MetricName": "QueueMessageOutput",
                "Labels": "[{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"name\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"count/min\"},{\"name\":\"productCategory\",\"value\":\"amqp\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"queue\"}]",
                "Dimensions": "userId,regionId,vhostName,queueName",
                "Namespace": "acs_amqp",
                "Periods": "60,300",
                "Unit": "count/min"
            },
            {
                "Description": "实例每分钟产生的消息数量",
                "Statistics": "Value",
                "MetricName": "VhostMessageInput",
                "Labels": "[{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"name\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"count/min\"},{\"name\":\"productCategory\",\"value\":\"amqp\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"vhost\"}]",
                "Dimensions": "userId,regionId,vhostName",
                "Namespace": "acs_amqp",
                "Periods": "60,300",
                "Unit": "count/min"
            },
            {
                "Description": "实例每分钟消费的消息数量",
                "Statistics": "Value",
                "MetricName": "VhostMessageOutput",
                "Labels": "[{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"name\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"count/min\"},{\"name\":\"productCategory\",\"value\":\"amqp\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"vhost\"}]",
                "Dimensions": "userId,regionId,vhostName",
                "Namespace": "acs_amqp",
                "Periods": "60,300",
                "Unit": "count/min"
            },
            {
                "Description": "",
                "Statistics": "Average",
                "MetricName": "Latency",
                "Labels": "[{\"name\":\"alertUnit\",\"value\":\"ms\"},{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"metricCategory\",\"value\":\"instanceId\"},{\"name\":\"is_alarm\",\"value\":\"true\"}]",
                "Dimensions": "userId,region,apiUid",
                "Namespace": "acs_apigateway_dashboard",
                "Periods": "60,300,900",
                "Unit": "ms"
            },
            {
                "Description": "时间粒度内http返回码4XX占全部返回码的百分比",
                "Statistics": "Average,Minimum,Maximum",
                "MetricName": "code4xx",
                "Labels": "[{\"name\":\"alertUnit\",\"value\":\"%\"},{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"metricCategory\",\"value\":\"instanceId\"},{\"name\":\"is_alarm\",\"value\":\"true\"}]",
                "Dimensions": "userId,instanceId",
                "Namespace": "acs_cdn",
                "Periods": "60,300",
                "Unit": "%"
            }
        ]
    }
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

