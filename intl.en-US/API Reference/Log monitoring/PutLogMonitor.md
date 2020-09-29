# PutLogMonitor

Creates or modifies a log monitoring metric.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=PutLogMonitor&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|PutLogMonitor|The operation that you want to perform. Set the value to PutLogMonitor. |
|Aggregates.N.Alias|String|Yes|Count|The alias of the aggregate function. Valid values of N: 1 to 10. |
|Aggregates.N.FieldName|String|Yes|sourceCount|The name of the field to be aggregated. Valid values of N: 1 to 10. |
|Aggregates.N.Function|String|Yes|count|The function that is used to aggregate the monitoring data of logs within an aggregation period. Valid values of N: 1 to 10. Valid values:

-   count: counts the number.
-   sum: calculates the total value.
-   avg: calculates the average value.
-   max: selects the maximum value.
-   min: selects the minimum value.
-   countps: calculates the counted number of the specified field divided by the total number of seconds of the aggregation period.
-   sumps: calculates the total value of the specified field divided by the total number of seconds of the aggregation period.
-   distinct: counts the number of logs where the specified field appears within the aggregation period. |
|SlsLogstore|String|Yes|test-logstore|The name of the Log Service Logstore. |
|SlsProject|String|Yes|test-project|The name of the Log Service project. |
|SlsRegionId|String|Yes|cn-hangzhou|The ID of the region where the Log Service Logstore resides. |
|LogId|String|No|12345|The ID returned by Log Service. |
|MetricName|String|No|cpu\_total|The name of the log monitoring metric. For more information, see [Appendix 1: Metrics](~~163515~~). |
|MetricExpress|String|No|\{"extend":\{"errorPercent":"5XXNumber/TotalNumber\*100"\}\}|The extended field. The extended field allows you to perform basic operations on the aggregation results.

Assume that you have calculated TotalNumber and 5XXNumber by aggregating the data. TotalNumber indicates the total number of HTTP requests, and 5XXNumber indicates the number of HTTP requests whose status code is greater than 499. You can calculate the server error rate by adding the following formula to the extended field: 5XXNumber/TotalNumber\*100.

JSON format: \{"extend":\{"errorPercent":"5XXNumber/TotalNumber\*100"\}\}. Description:

-   extend: required.
-   errorPercent: the alias of the field generated in the calculation result. You can specify the alias as needed.
-   5XXNumber/TotalNumber\*100: the calculation expression. |
|GroupId|String|No|12345|The ID of the application group. |
|Groupbys.N.Alias|String|No|CPUUtilization|The alias of the dimension based on which the data is grouped. Valid values of N: 1 to 10. |
|Groupbys.N.FieldName|String|No|cpu|The name of the field specified as the dimension. Valid values of N: 1 to 10. |
|ValueFilterRelation|String|No|and|The logical operator that is used between log filter conditions. The ValueFilter and ValueFilterRelation parameters must be used in pair. Valid values:

-   and
-   or |
|ValueFilter.N.Key|String|No|lh\_source|The name of the log field used for matching in the filter condition. Valid values of N: 1 to 10. |
|ValueFilter.N.Operator|String|No|Operator|The method that is used to match the field value. Valid values of N: 1 to 10. Valid values:

-   `contain`
-   `notContain`
-   `>`: greater than
-   `<`: less than
-   `>=`: greater than or equal to
-   `<=`: less than or equal to |
|ValueFilter.N.Value|String|No|test|The field value to be matched in the filter condition. Valid values of N: 1 to 10. |
|Tumblingwindows|String|No|60,300|The size of the tumbling window for calculation. Unit: seconds. The system performs an aggregation for each tumbling window. |
|Unit|String|No|Percent|The unit. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code. |
|LogId|String|12345|The ID returned by Log Service. If the log monitoring metric is created or modified, the ID is returned. |
|Message|String|successful|The returned message. Valid values:

-   If the call is successful, the value of `successful` is returned.
-   If the call fails, an error message is returned. Example: `alias of aggreate must be set value.` |
|RequestId|String|BBD7B294-1325-46D1-BD08-848D6A6B9AC6|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=PutLogMonitor
&Aggregates.1.Alias=Count
&Aggregates.1.FieldName=sourceCount
&Aggregates.1.Function=count
&SlsLogstore=test-logstore
&SlsProject=test-project
&SlsRegionId=cn-hangzhou
&<Common request parameters>
```

Sample success responses

`XML` format

```
<PutLogMonitorResponse>
          <Message>successful</Message>
          <RequestId>BA75EC4B-9363-4F96-9CD4-59F7CDFC2293</RequestId>
          <Code>200</Code>
          <LogId>12345</LogId>
          <Success>true</Success>
</PutLogMonitorResponse>
```

`JSON` format

```
{
    "Message": "successful",
    "RequestId": "BA75EC4B-9363-4F96-9CD4-59F7CDFC2293",
    "Code": 200,
    "LogId": 12345,
    "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

