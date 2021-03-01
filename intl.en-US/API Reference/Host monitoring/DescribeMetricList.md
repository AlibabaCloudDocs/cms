# DescribeMetricList

Queries the data of a time series metric of a specified cloud service.

**Note:** For information about how to assign values to the Namespace, Project, Metric, Period, and Dimensions parameters for cloud services, see [DescribeMetricMetaList](~~98846~~) or [Metrics](~~163515~~).

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeMetricList&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeMetricList|The operation that you want to perform. Set the value to DescribeMetricList. |
|MetricName|String|Yes|cpu\_idle|The name of the metric. |
|Namespace|String|Yes|acs\_ecs\_dashboard|The namespace of the cloud service.

 Specify the value in the acs\_service name format. |
|Period|String|No|60|The time interval at which metric data is queried. Unit: seconds. Valid values: 60, 300, and 900.

 **Note:** Set this parameter as needed. |
|StartTime|String|No|2019-01-30 00:00:00|The start of the time range to query. Supported formats:

 -   UNIX timestamp: the number of milliseconds that have elapsed since 00:00:00 Thursday, January 1, 1970.
-   Time format: YYYY-MM-DDThh:mm:ssZ.

 **Note:** The period specified by StartTime and EndTime includes the time specified by EndTime and excludes the time specified by StartTime. StartTime must be earlier than EndTime. |
|EndTime|String|No|2019-01-30 00:10:00|The end of the time range to query. Supported formats:

 -   UNIX timestamp: the number of milliseconds that have elapsed since 00:00:00 Thursday, January 1, 1970.
-   Time format: YYYY-MM-DDThh:mm:ssZ. |
|Dimensions|String|No|\[\{"instanceId": "i-abcdefgh12\*\*\*\*"\}\]|The dimensions that specify the resources for which you want to query metric data.

 Set the value to a set of key-value pairs. A typical pair is `instanceId:i-2ze2d6j5uhg20x47****`.

 **Note:** Dimensions must be formatted as a JSON string in a specified order. |
|NextToken|String|No|15761485350009dd70bb64cff1f0fff750b08ffff073be5fb1e785e2b020f1a949d5ea14aea7fed82f01dd8\*\*\*\*|The pagination cursor.

 **Note:** If this parameter is not specified, the data on the first page is returned. The returned value indicates that not all entries have been returned. You can use this value as an input parameter to obtain entries on the next page. If a response is empty, all query results have been returned. |
|Length|String|No|1000|The number of entries to return on each page. |
|Express|String|No|\{"groupby":\["userId","instanceId"\]\}|The expression for real-time computation on the query results.

 Only the groupby expression is supported. This expression is similar to the GROUP BY statement used in databases. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|3121AE7D-4AFF-4C25-8F1D-C8226EBB1F42|The ID of the request. |
|Code|String|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |
|NextToken|String|15761441850009dd70bb64cff1f0fff6d0b08ffff073be5fb1e785e2b020f7fed9b5e137bd810a6d6cff5ae\*\*\*\*|The pagination cursor. |
|Period|String|60|The time interval at which metric data was queried. Unit: seconds. Valid values: 60, 300, and 900. |
|Datapoints|String|\[\{"timestamp":1548777660000,"userId":"123","instanceId":"i-abc","Minimum":9.92,"Average":9.92,"Maximum":9.92\}\]|The data of the metric. |
|Message|String|The Request is not authorization.|The error message. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeMetricList
&MetricName=cpu_idle
&Namespace=acs_ecs_dashboard
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeMetricListResponse>
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
		  <Success>true</Success>
		  <Code>200</Code>
</DescribeMetricListResponse>
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

