# DescribeMetricTop

Queries the sorted data of a time series metric that belongs to a cloud service.

**Note:** For information about how to assign values to the Namespace, Project, Metric, Period, and Dimensions parameters for cloud services, see [DescribeMetricMetaList](~~98846~~) or [Metrics](~~163515~~).

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeMetricTop&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeMetricTop|The operation that you want to perform. Set the value to DescribeMetricTop. |
|MetricName|String|Yes|cpu\_idle|The name of the metric. |
|Namespace|String|Yes|acs\_ecs\_dashboard|The namespace of the cloud service. Specify the value in the acs\_service name format. |
|Orderby|String|Yes|Average|The field by which the metric data is sorted. |
|Period|String|No|60|The time interval at which metric data is queried. Unit: seconds. Valid values: 60, 300, and 900.

 Set this parameter as needed. Examples:

 -   If you set this parameter to 60 and 1,440 metric data entries exist, only the first 1,000 entries are returned.
-   If you set this parameter to 300 and 288 metric data entries exist, all of the entries are returned.

 **Note:** The maximum number of returned metric data entries is 1,000. If the number exceeds 1,000, only the first 1,000 entries are returned. |
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
|OrderDesc|String|No|False|The method that is used to sort the metric data. Valid values:

 -   True: sorts values in ascending order.
-   False: sorts values in descending order. |
|Length|String|No|1000|The number of entries to return on each page. Default value: 1000. |
|Express|String|No|\{"groupby":\["userId","instanceId"\]\}|The expression for real-time computation on the query results.

 Only the `groupby` expression is supported. This expression is similar to the GROUP BY statement used in databases. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|3121AE7D-4AFF-4C25-8F1D-C8226EBB1F42|The ID of the request. |
|Code|String|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Datapoints|String|\[\{"timestamp":1548777660000,"userId":"123","instanceId":"i-abc","Minimum":9.92,"Average":9.92,"Maximum":9.92,"\_count":1\}\]|The data of the metric. |
|Period|String|60|The time interval at which metric data was queried. Unit: seconds. Valid values: 60, 300, and 900. |
|Message|String|The Request is not authorization.|The error message. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeMetricTop
&MetricName=cpu_idle
&Namespace=acs_ecs_dashboard
&Orderby=Average
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeMetricTopResponse>
	  <Period>60</Period>
	  <Datapoints>
		    <order>1</order>
		    <timestamp>1551687360000</timestamp>
		    <userId>12345****</userId>
		    <instanceId>i-2zeehst1****</instanceId>
		    <Maximum>16.41</Maximum>
		    <Minimum>4.66</Minimum>
		    <Average>7.74</Average>
		    <_count>1</_count>
	  </Datapoints>
	  <Datapoints>
		    <order>2</order>
		    <timestamp>1551687360000</timestamp>
		    <userId>12345****</userId>
		    <instanceId>i-2zefxdy2****</instanceId>
		    <Maximum>15.74</Maximum>
		    <Minimum>5.03</Minimum>
		    <Average>7.14</Average>
		    <_count>1</_count>
	  </Datapoints>
	  <RequestId>1F68A4E8-4488-48E7-9189-3E1F5165E64E</RequestId>
	  <Code>200</Code>
</DescribeMetricTopResponse>
```

`JSON` format

```
{
    "Period": "60",
    "Datapoints": [
        {
            "order": 1,
            "timestamp": 1551687360000,
            "userId": "12345****",
            "instanceId": "i-2zeehst1****",
            "Maximum": 16.41,
            "Minimum": 4.66,
            "Average": 7.74,
            "_count": 1
        },
        {
            "order": 2,
            "timestamp": 1551687360000,
            "userId": "12345****",
            "instanceId": "i-2zefxdy2****",
            "Maximum": 15.74,
            "Minimum": 5.03,
            "Average": 7.14,
            "_count": 1
        }
    ],
    "RequestId": "1F68A4E8-4488-48E7-9189-3E1F5165E64E",
    "Code": "200"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

