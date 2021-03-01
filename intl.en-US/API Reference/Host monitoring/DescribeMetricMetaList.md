# DescribeMetricMetaList

Queries the descriptions of time series metrics that are supported in Cloud Monitor.

This operation is usually used with DescribeMetricList and DescribeMetricLast. For more information, see [DescribeMetricList](~~51936~~) and [DescribeMetricLast](~~51939~~).

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeMetricMetaList&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeMetricMetaList|The operation that you want to perform. Set the value to DescribeMetricMetaList. |
|Namespace|String|No|acs\_kvstore|The namespace of the service.

For more information, see [Appendix 1: Metrics](~~163515~~). |
|Labels|String|No|\[\{"name":"productCategory","value":"kvstore\_old"\}\]|The tags for filtering metrics. Specify a JSON string.

Format:`[{"name":"tag name","value":"tag value"},{"name":"tag name","value":"tag value"}]`. The following tags are available:

-   metricCategory: the category of the metric.
-   alertEnable: specifies whether to report alerts for the metric.
-   alertUnit: the suggested unit of the metric value in alerts.
-   unitFactor: the factor for metric unit conversion.
-   minAlertPeriod: the minimum time interval to report a new alert.
-   productCategory: the category of the service. |
|MetricName|String|No|CPUUtilization|The name of the metric. For more information, see [Appendix 1: Metrics](~~163515~~). |
|PageNumber|Integer|No|1|The page to return. Default value: 1 |
|PageSize|Integer|No|30|The number of entries to return on each page. Default value: 30. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Success|Boolean|true|Indicates whether the request was successful. The value true indicates success. The value false indicates failure. |
|Code|String|200|The response code.

**Note:** The HTTP 200 code indicates that the request was successful. |
|RequestId|String|0CCE0AF0-053C-4B13-A583-DC9A85785D49|The ID of the request. |
|Message|String|The Request is not authorization.|The error message. |
|Resources|Array| |The configuration of the metric. |
|Resource| | | |
|Description|String|CPUUtilization|The description of the metric. |
|Dimensions|String|instanceId|The dimensions of the metric. Multiple dimensions are separated with commas \(,\). |
|Labels|String|\[\{\\"name\\":\\"alertUnit\\",\\"value\\":\\"Bytes\\"\},\{\\"name\\":\\"minAlertPeriod\\",\\"value\\":\\"60\\"\},\{\\"name\\":\\"metricCategory\\",\\"value\\":\\"instanceId\\"\},\{\\"name\\":\\"instanceType\\",\\"value\\":\\"disaster\\"\},\{\\"name\\":\\"is\_alarm\\",\\"value\\":\\"true\\"\},\{\\"name\\":\\"productCategory\\",\\"value\\":\\"kvstore\_old\\"\}\]|The tags of the metric, including one or more JSON strings. Format: `[{"name":"tag name","value":"tag value"}]`. The `name` can be repeated.

The following tags are available:

-   metricCategory: the category of the metric.
-   alertEnable: specifies whether to report alerts for the metric.
-   alertUnit: the suggested unit of the metric value in alerts.
-   unitFactor: the factor for metric unit conversion.
-   minAlertPeriod: the minimum time interval to report a new alert.
-   productCategory: the category of the service. |
|MetricName|String|CPUUtilization|The name of the metric. |
|Namespace|String|acs\_kvstore|The namespace of the service. The value is usually in the format of acs\_Service. |
|Periods|String|60,300|The statistical period of the metric. Multiple statistical periods are separated with commas \(,\). |
|Statistics|String|Average,Minimum,Maximum|The statistical method. Multiple statistic methods are separated with commas \(,\). |
|Unit|String|%|The unit of the metric. |
|TotalCount|String|12|The total number of returned records. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeMetricMetaList
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeMetricMetaListResponse>
          <TotalCount>1853</TotalCount>
          <RequestId>CDE9EAFF-D54E-4024-BBFC-B0AAC883143B</RequestId>
          <Success>true</Success>
          <Code>200</Code>
          <Resources>
                <Resource>
                      <Description>The rated disk capacity</Description>
                      <Statistics>Average,Minimum,Maximum</Statistics>
                      <MetricName>ads.diskSize</MetricName>
                      <Labels>[{\"name\":\"minAlertPeriod\",\"value\":\"300\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"name\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"Mbytes\"},{\"name\":\"productCategory\",\"value\":\"ads\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"workerId\"}]</Labels>
                      <Dimensions>userId,instanceId,tableSchema,workerId</Dimensions>
                      <Namespace>acs_ads</Namespace>
                      <Periods>300</Periods>
                      <Unit>MB</Unit>
                </Resource>
                <Resource>
                      <Description>The used disk space</Description>
                      <Statistics>Average,Minimum,Maximum</Statistics>
                      <MetricName>ads.diskUsed</MetricName>
                      <Labels>[{\"name\":\"alertUnit\",\"value\":\"Mbytes\"},{\"name\":\"minAlertPeriod\",\"value\":\"300\"},{\"name\":\"metricCategory\",\"value\":\"workerId\"},{\"name\":\"is_alarm\",\"value\":\"true\"}]</Labels>
                      <Dimensions>userId,instanceId,tableSchema,workerId</Dimensions>
                      <Namespace>acs_ads</Namespace>
                      <Periods>300</Periods>
                      <Unit>MB</Unit>
                </Resource>
                <Resource>
                      <Description>The disk usage</Description>
                      <Statistics>Average,Minimum,Maximum</Statistics>
                      <MetricName>ads.diskUsedPercent</MetricName>
                      <Labels>[{\"name\":\"alertUnit\",\"value\":\"%\"},{\"name\":\"minAlertPeriod\",\"value\":\"300\"},{\"name\":\"metricCategory\",\"value\":\"workerId\"},{\"name\":\"is_alarm\",\"value\":\"true\"}]</Labels>
                      <Dimensions>userId,instanceId,tableSchema,workerId</Dimensions>
                      <Namespace>acs_ads</Namespace>
                      <Periods>300</Periods>
                      <Unit>%</Unit>
                </Resource>
                <Resource>
                      <Description>The number of unconsumed messages in the queue</Description>
                      <Statistics>Maximum</Statistics>
                      <MetricName>QueueMessageAccumulation</MetricName>
                      <Labels>[{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"name\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"count/min\"},{\"name\":\"productCategory\",\"value\":\"amqp\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"queue\"}]</Labels>
                      <Dimensions>userId,regionId,vhostName,queueName</Dimensions>
                      <Namespace>acs_amqp</Namespace>
                      <Periods>60,300</Periods>
                      <Unit>count/min</Unit>
                </Resource>
                <Resource>
                      <Description>The number of new messages in the queue per minute</Description>
                      <Statistics>Value</Statistics>
                      <MetricName>QueueMessageInput</MetricName>
                      <Labels>[{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"n ame\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"count/min\"},{\"name\":\"productCategory\",\"value\":\"amqp\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"queue\"}]</Labels>
                      <Dimensions>userId,regionId,vhostName,queueName</Dimensions>
                      <Namespace>acs_amqp</Namespace>
                      <Periods>60,300</Periods>
                      <Unit>count/min</Unit>
                </Resource>
                <Resource>
                      <Description>The number of unconsumed messages in the queue</Description>
                      <Statistics>Value</Statistics>
                      <MetricName>QueueMessageOutput</MetricName>
                      <Labels>[{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"name\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"count/min\"},{\"name\":\"productCategory\",\"value\":\"amqp\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"queue\"}]</Labels>
                      <Dimensions>userId,regionId,vhostName,queueName</Dimensions>
                      <Namespace>acs_amqp</Namespace>
                      <Periods>60,300</Periods>
                      <Unit>count/min</Unit>
                </Resource>
                <Resource>
                      <Description>The number of messages generated by the instance per minute</Description>
                      <Statistics>Value</Statistics>
                      <MetricName>VhostMessageInput</MetricName>
                      <Labels>[{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"name\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"count/min\"},{\"name\":\"productCategory\",\"value\":\"amqp\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"vhost\"}]</Labels>
                      <Dimensions>userId,regionId,vhostName</Dimensions>
                      <Namespace>acs_amqp</Namespace>
                      <Periods>60,300</Periods>
                      <Unit>count/min</Unit>
                </Resource>
                <Resource>
                      <Description>The number of messages consumed by the instance per minute</Description>
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
                      <Description>The percentage of HTTP 4xx status codes in a specified time range</Description>
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

`JSON` format

```
{
        "TotalCount":  1853,
        "RequestId":  "CDE9EAFF-D54E-4024-BBFC-B0AAC883143B",
        "Success":  true,
        "Code":  200,
        "Resources":  {
                "Resource":  [
                        {
                                "Description":  "The rated disk capacity",
                                "Statistics":  "Average,Minimum,Maximum",
                                "MetricName":  "ads.diskSize",
                                "Labels":  "[{\"name\":\"minAlertPeriod\",\"value\":\"300\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"name\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"Mbytes\"},{\"name\":\"productCategory\",\"value\":\"ads\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"workerId\"}]",
                                "Dimensions":  "userId,instanceId,tableSchema,workerId",
                                "Namespace":  "acs_ads",
                                "Periods":  "300",
                                "Unit":  "MB"
                        },
                        {
                                "Description":  "The used disk space",
                                "Statistics":  "Average,Minimum,Maximum",
                                "MetricName":  "ads.diskUsed",
                                "Labels":  "[{\"name\":\"alertUnit\",\"value\":\"Mbytes\"},{\"name\":\"minAlertPeriod\",\"value\":\"300\"},{\"name\":\"metricCategory\",\"value\":\"workerId\"},{\"name\":\"is_alarm\",\"value\":\"true\"}]",
                                "Dimensions":  "userId,instanceId,tableSchema,workerId",
                                "Namespace":  "acs_ads",
                                "Periods":  "300",
                                "Unit":  "MB"
                        },
                        {
                                "Description":  "The disk usage",
                                "Statistics":  "Average,Minimum,Maximum",
                                "MetricName":  "ads.diskUsedPercent",
                                "Labels":  "[{\"name\":\"alertUnit\",\"value\":\"%\"},{\"name\":\"minAlertPeriod\",\"value\":\"300\"},{\"name\":\"metricCategory\",\"value\":\"workerId\"},{\"name\":\"is_alarm\",\"value\":\"true\"}]",
                                "Dimensions":  "userId,instanceId,tableSchema,workerId",
                                "Namespace":  "acs_ads",
                                "Periods":  "300",
                                "Unit":  "%"
                        },
                        {
                                "Description": "The number of unconsumed messages in the queue",
                                "Statistics":  "Maximum",
                                "MetricName":  "QueueMessageAccumulation",
                                "Labels":  "[{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"name\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"count/min\"},{\"name\":\"productCategory\",\"value\":\"amqp\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"queue\"}]",
                                "Dimensions":  "userId,regionId,vhostName,queueName",
                                "Namespace":  "acs_amqp",
                                "Periods":  "60,300",
                                "Unit":  "count/min"
                        },
                        {
                                "Description":  "The number of new messages in the queue per minute",
                                "Statistics":  "Value",
                                "MetricName":  "QueueMessageInput",
                                "Labels":  "[{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"n ame\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"count/min\"},{\"name\":\"productCategory\",\"value\":\"amqp\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"queue\"}]",
                "Dimensions": "userId,regionId,vhostName,queueName",
                "Namespace": "acs_amqp",
                "Periods": "60,300",
                "Unit": "count/min"
            },
            {
                "Description": "The number of unconsumed messages in the queue",
                "Statistics": "Value",
                "MetricName": "QueueMessageOutput",
                "Labels": "[{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"name\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"count/min\"},{\"name\":\"productCategory\",\"value\":\"amqp\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"queue\"}]",
                "Dimensions": "userId,regionId,vhostName,queueName",
                "Namespace": "acs_amqp",
                "Periods": "60,300",
                "Unit": "count/min"
            },
            {
                "Description":"The number of messages generated by the instance per minute",
                "Statistics": "Value",
                "MetricName": "VhostMessageInput",
                "Labels": "[{\"name\":\"minAlertPeriod\",\"value\":\"60\"},{\"name\":\"alertDefault\",\"value\":\"\"},{\"name\":\"unitFactor\",\"value\":\"1\"},{\"name\":\"alertUnit\",\"value\":\"count/min\"},{\"name\":\"productCategory\",\"value\":\"amqp\"},{\"name\":\"is_alarm\",\"value\":\"true\"},{\"name\":\"metricCategory\",\"value\":\"vhost\"}]",
                "Dimensions": "userId,regionId,vhostName",
                "Namespace": "acs_amqp",
                "Periods": "60,300",
                "Unit": "count/min"
            },
            {
                "Description":"The number of messages consumed by the instance per minute",
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
                "Description": "The percentage of HTTP 4xx status codes in a specified time range",
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

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

