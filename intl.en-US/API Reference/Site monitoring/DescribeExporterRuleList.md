# DescribeExporterRuleList

Queries data export rules.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeExporterRuleList&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeExporterRuleList|The operation that you want to perform. Set the value to **DescribeExporterRuleList**. |
|PageNumber|Integer|No|1|The number of the page to return. Default value: 1. |
|PageSize|Integer|No|1000|The number of entries to return on each page. Default value: 1000. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Total|Integer|1000|The total number of entries returned. |
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. Other status codes indicate that the call failed. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   `true`: indicates a success.
-   `false`: indicates a failure. |
|RequestId|String|6BA047CA-8BC6-40BC-BC8F-FBECF35F1993|The ID of the request. |
|Message|String|success|The returned message. |
|Datapoints|Array| |The details of the data export rules. |
|Datapoint| | | |
|CreateTime|Long|1584024616228|The UNIX timestamp when the rule was created. |
|Describe|String|Export monitoring data|The description of the rule. |
|Dimension|String|\{"instanceId":"xxxxx"\}|The associated resources. |
|DstName|List|exporter1|The name of the destination to which the data is exported. |
|Enabled|Boolean|true|Indicates whether the rule is enabled. |
|MetricName|String|cpu\_total|The name of the metric.

**Note:** For more information, see [DescribeMetricMetaList](~~98846~~) or [Appendix 1: Metrics](~~28619~~). |
|Namespace|String|acs\_ecs\_dashboard|The namespace of the service.

**Note:** For more information, see [DescribeMetricMetaList](~~98846~~) or [Appendix 1: Metrics](~~28619~~). |
|RuleName|String|myRuleName|The name of the data export rule. |
|TargetWindows|String|60,300|The time window of the exported data.

Multiple windows are separated with commas \(,\).

**Note:** Data in a time window of less than 60 seconds cannot be exported. |
|PageNumber|Integer|1|The page number of the returned page. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DescribeExporterRuleList
&<Common request parameters>
```

Sample success responses

`XML` format

```
<RequestId>6BA047CA-8BC6-40BC-BC8F-FBECF35F1993</RequestId>
<PageNumber>1</PageNumber>
<Total>1</Total>
<Datapoints>
    <Datapoint>
        <TargetWindows>60,300</TargetWindows>
        <Describe/>
        <MetricName>cpu_total</MetricName>
        <CreateTime>1584024616228</CreateTime>
        <Enabled>false</Enabled>
        <Dimension>{'userId': '177******'}</Dimension>
        <DstName>
            <DstName>exporter1</DstName>
        </DstName>
        <RuleName>exporterRule1</RuleName>
        <Namespace>acs_ecs_dashboard</Namespace>
        <dstNames/>
    </Datapoint>
</Datapoints>
<Code>200</Code>
<Success>true</Success>
```

`JSON` format

```
{
    "RequestId": "6BA047CA-8BC6-40BC-BC8F-FBECF35F1993",
    "PageNumber": 1,
    "Total": 1,
    "Datapoints": {
        "Datapoint": [
            {
                "TargetWindows": "60,300",
                "Describe": "",
                "MetricName": "cpu_total",
                "CreateTime": 1584024616228,
                "Enabled": false,
                "Dimension": "{'userId': '177******'}",
                "DstName": {
                    "DstName": [
                        "exporter1"
                    ]
                },
                "RuleName": "exporterRule1",
                "Namespace": "acs_ecs_dashboard",
                "dstNames": ""
            }
        ]
    },
    "Code": "200",
    "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

