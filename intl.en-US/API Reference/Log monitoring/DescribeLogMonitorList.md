# DescribeLogMonitorList

Queries log monitoring metrics.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeLogMonitorList&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeLogMonitorList|The operation that you want to perform. Set the value to DescribeLogMonitorList. |
|PageNumber|Integer|No|1|The number of the page to return. |
|PageSize|Integer|No|10|The number of entries to return on each page. Default value: 10 |
|SearchValue|String|No|test|The keyword that is used to search for log monitoring metrics. Fuzzy match is supported. |
|GroupId|Long|No|123456|The ID of the application group. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|LogMonitorList|Array of LogMonitor|N/A|The log monitoring metrics. |
|GmtCreate|Long|1577766395000|The time when the log monitoring metric was created.

This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|GroupId|Long|12345|The ID of the application group. |
|LogId|Long|12345|The ID returned by Log Service. |
|MetricName|String|cpu\_total|The name of the log monitoring metric. For more information, see [Appendix 1: Metrics](~~163515~~). |
|SlsLogstore|String|testSlS\*\*\*\*|The name of the Log Service Logstore. |
|SlsProject|String|sls-project-test\*\*\*\*|The name of the Log Service project. |
|SlsRegionId|String|cn-hangzhou|The ID of the region where the Log Service Logstore resides. |
|ValueFilter|Array of ValueFilterObject|N/A|The condition that is used to filter logs. The ValueFilter and ValueFilterRelation parameters are used in pair. The filter condition is equivalent to the WHERE clause in SQL statements.

If no filter condition is specified, all logs are processed. Assume that logs contain the Level field, which may be set to Error. If you need to calculate the number of times that logs of the Error level appear every minute, you can set the filter condition to Level=Error and count the number of logs that meet this condition. |
|Key|String|hostName|The name of the log field used for matching in the filter condition. |
|Operator|String|contain|The method that is used to match the field value. Valid values:

-   contain
-   notContain
-   `>`: greater than
-   `<`: less than
-   `>=`: greater than or equal to
-   `<=`: less than or equal to |
|Value|String|portal|The field value to be matched in the filter condition. |
|ValueFilterRelation|String|and|The logical operator that is used between log filter conditions. The ValueFilter and ValueFilterRelation parameters are used in pair. Valid values:

-   and
-   or |
|Message|String|successful|The returned message. |
|PageNumber|Integer|1|The number of the returned page. |
|PageSize|Integer|10|The number of entries returned on each page. |
|RequestId|String|01E90080-4300-4FAA-B9AE-161956BC350D|The ID of the request. |
|Total|Long|15|The total number of the returned entries. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DescribeLogMonitorList
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeLogMonitorListResponse>
          <Message>successful</Message>
          <RequestId>C085617E-7A64-402E-877D-410E86174B0C</RequestId>
          <PageSize>10</PageSize>
          <Total>2</Total>
          <LogMonitorList>
                <SlsProject>sls-project-test****</SlsProject>
                <MetricName>cpu_total</MetricName>
                <GmtCreate>1591175112000</GmtCreate>
                <ValueFilterRelation>and</ValueFilterRelation>
                <LogId>12345</LogId>
                <SlsRegionId>cn-hangzhou</SlsRegionId>
                <SlsLogstore>testSlS****</SlsLogstore>
                <GroupId>12345</GroupId>
          </LogMonitorList>
          <LogMonitorList>
                <SlsProject>sls-project-test****</SlsProject>
                <MetricName>cpu_total</MetricName>
                <GmtCreate>1586826787000</GmtCreate>
                <ValueFilterRelation>and</ValueFilterRelation>
                <ValueFilter>
                      <Operator>=</Operator>
                      <Value>1</Value>
                      <Key>lh_source</Key>
                </ValueFilter>
                <LogId>12345</LogId>
                <SlsRegionId>cn-hangzhou</SlsRegionId>
                <SlsLogstore>internal-alert-history</SlsLogstore>
                <GroupId>12345</GroupId>
          </LogMonitorList>
          <Code>200</Code>
          <Success>true</Success>
</DescribeLogMonitorListResponse>
```

`JSON` format

```
{
    "Message": "successful",
    "RequestId": "C085617E-7A64-402E-877D-410E86174B0C",
    "PageSize": 10,
    "Total": 2,
    "LogMonitorList": [
        {
            "SlsProject": "sls-project-test****",
            "MetricName": "cpu_total",
            "GmtCreate": 1591175112000,
            "ValueFilterRelation": "and",
            "ValueFilter": [],
            "LogId": 12345,
            "SlsRegionId": "cn-hangzhou",
            "SlsLogstore": "testSlS****",
            "GroupId": 12345
        },
        {
            "SlsProject": "sls-project-test****",
            "MetricName": "cpu_total",
            "GmtCreate": 1586826787000,
            "ValueFilterRelation": "and",
            "ValueFilter": [
                {
                    "Operator": "=",
                    "Value": "1",
                    "Key": "lh_source"
                }
            ],
            "LogId": 12345,
            "SlsRegionId": "cn-hangzhou",
            "SlsLogstore": "internal-alert-history",
            "GroupId": 12345
        }
    ],
    "Code": 200,
    "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

