# DescribeMetricLast

Queries the latest monitoring data of a metric.

**Note:** For information about how to specify the Namespace, Project, Metric, Period, and Dimensions parameters for cloud services, see [DescribeMetricMetaList](~~98846~~) or [Metrics](~~163515~~).

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeMetricLast&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeMetricLast|The operation that you want to perform. Set the value to DescribeMetricLast. |
|MetricName|String|Yes|CPUUtilization|The name of the metric. |
|Namespace|String|Yes|acs\_ecs\_dashboard|The namespace of the cloud service. Specify the value in the format of acs\_Service name. |
|Period|String|No|60|The statistical period of the metric. Unit: seconds.

 **Note:** If this parameter is not specified in the alert rule, raw data is queried at the interval at which the metric data is reported. If this parameter is specified in the alert rule, metric data is queried at the specified interval. |
|StartTime|String|No|2019-01-31 10:00:00|The beginning of the time range to query.

 **Note:** To avoid unpredictable results, we recommend that you do not use this parameter. |
|EndTime|String|No|2019-01-31 10:10:00|The end of the time range to query.

 -   For second-level data, the start time is obtained by comparing the time that is specified by the startTime parameter and 20 minutes earlier of the time that is specified by the EndTime parameter. The earlier one of the preceding time points is used as the start time.
-   For minute-level data, the start time is obtained by comparing the time that is specified by the startTime parameter and 2 hours earlier of the time that is specified by the EndTime parameter. The earlier one of the preceding time points is used as the start time.
-   For hour-level data, the start time is obtained by comparing the time that is specified by the startTime parameter and two days earlier of the time that is specified by the EndTime parameter. The earlier one of the preceding time points is used as the start time. |
|Dimensions|String|No|\[\{"instanceId":"i-abcdefgh12\*\*\*\*"\}\]|The dimensions. This parameter is used to specify the resources that you want to query.

 Set the value to a collection of key-value pairs. A typical example is `instanceId:i-2ze2d6j5uhg20x47****`.

 **Note:** Dimensions must be formatted as a JSON string in a specified order. |
|NextToken|String|No|15761432850009dd70bb64cff1f0fff6c0b08ffff073be5fb1e785e2b020f7fed9b5e137bd810a6d6cff5ae\*\*\*\*|The paging token.

 -   If the number of results exceeds the maximum number of entries on a single page, a paging token is returned.
-   This token can be used as an input parameter to retrieve the next page of results. If all results are retrieved, no token is returned. |
|Length|String|No|1000|The number of entries to return on each page.

 Default value: 1000. This value indicates that 1,000 entries of metric data are returned on each page. |
|Express|String|No|\{"groupby":\["userId","instanceId"\]\}|The expression that is used to compute the query results in real time. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|021472A6-25E3-4094-8D00-BA4B6A5486C3|The ID of the request. |
|Code|String|200|The HTTP status code.

 **Note:** The value 200 indicates that the call was successful. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |
|Period|String|60|The time interval at which metric data was queried. Unit: seconds. |
|NextToken|String|xxxxxx|The paging token. |
|Datapoints|String|\[\{"timestamp":1548777660000,"userId":"123456789876\*\*\*\*","instanceId":"i-abcdefgh12\*\*\*\*","Minimum":9.92,"Average":9.92,"Maximum":9.92\}\]|The monitoring data. |
|Message|String|The Request is not authorization.|The returned message. |

## Examples

Sample request

```
http(s)://[Endpoint]/? Action=DescribeMetricLast
&MetricName=CPUUtilization
&Namespace=acs_ecs_dashboard
&<Common request parameters>
```

Sample success responses

`XML` format

```
<QueryMetricListResponse>
    <Period>60</Period>
    <Datapoints>
        <Datapoints>
            <timestamp>1490152860000</timestamp>
            <Maximum>100</Maximum>
            <userId> 123456789876****</userId>
            <Minimum>93.1</Minimum>
            <instanceId>i-abcdefgh12****</instanceId>
            <Average>99.52</Average>
        </Datapoints>
        <Datapoints>
            <timestamp>1490152920000</timestamp>
            <Maximum>100</Maximum>
            <userId> 123456789876**** </userId>
            <Minimum>92.59</Minimum>
            <instanceId>i-abcdefgh12****</instanceId>
            <Average>99.49</Average>
        </Datapoints>
        <Datapoints>
            <timestamp>1490152980000</timestamp>
            <Maximum>100</Maximum>
            <userId>123456789876****</userId>
            <Minimum>92.86</Minimum>
            <instanceId>i-abcdefgh12****</instanceId>
            <Average>99.44</Average>
        </Datapoints>
        <Datapoints>
            <timestamp>1490153040000</timestamp>
            <Maximum>100</Maximum>
            <userId>123456789876****</userId>
            <Minimum>91.43</Minimum>
            <instanceId>i-abcdefgh12****</instanceId>
            <Average>99.36</Average>
        </Datapoints>
        <Datapoints>
            <timestamp>1490153100000</timestamp>
            <Maximum>100</Maximum>
            <userId>123456789876****</userId>
            <Minimum>93.55</Minimum>
            <instanceId>i-abcdefgh12****</instanceId>
            <Average>99.51</Average>
        </Datapoints>
        <Datapoints>
            <timestamp>1490153160000</timestamp>
            <Maximum>100</Maximum>
            <userId>123456789876****</userId>
            <Minimum>93.1</Minimum>
            <instanceId>i-abcdefgh12****</instanceId>
            <Average>99.52</Average>
        </Datapoints>
        <Datapoints>
            <timestamp>1490153220000</timestamp>
            <Maximum>100</Maximum>
            <userId>123456789876****</userId>
            <Minimum>92.59</Minimum>
            <instanceId>i-abcdefgh12****</instanceId>
            <Average>99.42</Average>
        </Datapoints>
        <Datapoints>
            <timestamp>1490153280000</timestamp>
            <Maximum>100</Maximum>
            <userId>123456789876****</userId>
            <Minimum>91.18</Minimum>
            <instanceId>i-abcdefgh12****</instanceId>
            <Average>99.34</Average>
        </Datapoints>
        <Datapoints>
            <timestamp>1490153340000</timestamp>
            <Maximum>100</Maximum>
            <userId>123456789876****</userId>
            <Minimum>92.86</Minimum>
            <instanceId>i-abcdefgh12****</instanceId>
            <Average>99.46</Average>
        </Datapoints>
        <Datapoints>
            <timestamp>1490153400000</timestamp>
            <Maximum>100</Maximum>
            <userId>123456789876****</userId>
            <Minimum>91.18</Minimum>
            <instanceId>i-abcdefgh12****</instanceId>
            <Average>99.35</Average>
        </Datapoints>
    </Datapoints>
    <RequestId>6661EC50-8625-4161-B349-E0DD59002AB7</RequestId>
    <Success>true</Success>
    <Code>200</Code>
</QueryMetricListResponse>
```

`JSON` format

```
{
    "Period": "60",
    "Datapoints": [
        {
            "timestamp": 1490152860000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 93.1,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.52
        },
        {
            "timestamp": 1490152920000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 92.59,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.49
        },
        {
            "timestamp": 1490152980000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 92.86,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.44
        },
        {
            "timestamp": 1490153040000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 91.43,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.36
        },
        {
            "timestamp": 1490153100000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 93.55,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.51
        },
        {
            "timestamp": 1490153160000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 93.1,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.52
        },
        {
            "timestamp": 1490153220000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 92.59,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.42
        },
        {
            "timestamp": 1490153280000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 91.18,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.34
        },
        {
            "timestamp": 1490153340000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 92.86,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.46
        },
        {
            "timestamp": 1490153400000,
            "Maximum": 100,
            "userId": "123456789876****",
            "Minimum": 91.18,
            "instanceId": "i-abcdefgh12****",
            "Average": 99.35
        }
    ],
    "RequestId": "6A5F022D-AC7C-460E-94AE-B9E75083D027",
    "Success": true,
    "Code": "200"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

