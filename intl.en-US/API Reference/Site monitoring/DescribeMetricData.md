# DescribeMetricData

Queries the monitoring data on a time series metric of a cloud service in a specified period.

For more information about how to assign values to the **Namespace**, **Project**, **Metric**, **Period**, and **Dimensions** parameters for cloud services, see [DescribeMetricMetaList](~~98846~~) or [Appendix 1: Metrics](~~163515~~).

**Note:** Different from **DescribeMetricList**, this operation provides statistical features. You can set the Dimension parameter to \{"userId:"xxxx"\} to aggregate all data of the specified user.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeMetricData&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description |
|---------|----|--------|-------|------------|
|Action|String|Yes|DescribeMetricData|The operation that you want to perform. Set the value to DescribeMetricData. |
|MetricName|String|Yes|cpu\_idle|The name of the metric that you want to query. |
|Namespace|String|Yes|acs\_ecs\_dashboard|The namespace of the service.

 Specify the value in the format of acs\_Service. |
|Period|String|No|60|The time interval to query monitoring data. Unit: seconds. Valid values: 60, 300, and 900.

 Set this parameter as needed. |
|StartTime|String|No|2019-01-30 00:00:00|The beginning of the time range to query. Supported formats:

 -   UNIX timestamp: the number of milliseconds that have elapsed since January 1, 1970, 00:00:00 UTC.
-   Time format: YYYY-MM-DDThh:mm:ssZ.

 **Note:** The period specified by StartTime and EndTime includes the time point specified by EndTime but does not include the time point specified by StartTime. StartTime must be earlier than EndTime. |
|EndTime|String|No|2019-01-30 00:10:00|The end of the time range to query. Supported formats:

 -   UNIX timestamp: the number of milliseconds that have elapsed since January 1, 1970, 00:00:00 UTC.
-   Time format: YYYY-MM-DDThh:mm:ssZ. |
|Dimensions|String|No|\[\{"instanceId": "i-abcdefgh12\*\*\*\*"\}\]|The dimensions that specify the resources for which you want to query monitoring data.

 Set the value to a collection of key-value pairs. A typical key-value pair is `instanceId:XXXXXX`.

 The key and value can each be 1 to 64 bytes in length. Values that contain more than 64 characters will be truncated.

 The key and value can contain letters, digits, periods \(.\), hyphens \(-\), underscores \(\_\), forward slashes \(/\), and backslashes \(\\\).

 **Note:** Dimensions must be organized in a JSON string and follow the required order. |
|Express|String|No|"\{"groupby":\["userId","instanceId"\]\}"|The expression for real-time computation on the query results.

 Only the groupby expression is supported. This expression is similar to the GROUP BY statement used in databases. |
|Length|String|No|1000|The number of entries to return on each page. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The response code.

 **Note:** The HTTP 200 code indicates that the request was successful. |
|Datapoints|String|\[\{"timestamp":1548777660000,"userId":"123\*\*\*\*","instanceId":"i-abc\*\*\*\*","Minimum":9.92,"Average":9.92,"Maximum":9.92\}\]|The monitoring data of the metric. The value includes the following fields:

 -   timestamp: the timestamp when the alert was triggered.
-   userId: the ID of the user for which the alert was triggered.
-   instanceId: the ID of the instance for which the alert was triggered.
-   Minimum, Average, and Maximum: the aggregation methods. |
|Message|String|The Request is not authorization.|The error message. |
|Period|String|60|The time interval at which monitoring data was queried. Unit: seconds. Valid values: 60, 300, and 900. |
|RequestId|String|6A5F022D-AC7C-460E-94AE-B9E75083D027|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeMetricData
&MetricName=cpu_idle
&Namespace=acs_ecs_dashboard
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeMetricData>
		  <Period>60</Period>
		  <Datapoints>
			    <timestamp>1490152860000</timestamp>
			    <Maximum>100</Maximum>
			    <userId>123456789876****</userId>
			    <Minimum>93.1</Minimum>
			    <instanceId>i-abcdefgh12****</instanceId>
			    <Average>99.52</Average>
		  </Datapoints>
		  <Datapoints>
			    <timestamp>1490152920000</timestamp>
			    <Maximum>100</Maximum>
			    <userId>123456789876****</userId>
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
		  <RequestId>6A5F022D-AC7C-460E-94AE-B9E75083D027</RequestId>
		  <Code>200</Code>
</DescribeMetricData>
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
    "Code": "200"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

