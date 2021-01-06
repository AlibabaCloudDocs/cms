# PutCustomMetric

Reports monitoring data.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=PutCustomMetric&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|PutCustomMetric|The operation that you want to perform. Set the value to PutCustomMetric. |
|MetricList.N.Dimensions|String|Yes|\{"sampleName1":"value1","sampleName2":"value2"\}|The dimensions. This parameter is used to specify the resources that you want to query. Valid values of N: 1 to 21.

 Set the value to a collection of key-value pairs. Format: `{"Key":"Value"}`.

 The key or value must be 1 to 64 bytes in length. Excessive characters are truncated.

 The key or value can contain letters, digits, periods \(.\), hyphens \(-\), underscores \(\_\), forward slashes \(/\), and backslashes \(\\\).

 **Note:** Dimensions must be formatted as a JSON string in a specified order. |
|MetricList.N.GroupId|String|Yes|12345|The ID of the application group. Valid values of N: 1 to 21.

 **Note:** If the metric does not belong to any application group, enter 0. |
|MetricList.N.MetricName|String|Yes|cpu\_total|The name of the metric. Valid values of N: 1 to 21. For more information, see [Cloud service metrics](~~163515~~). |
|MetricList.N.Type|String|Yes|0|The type of the reported data. Valid values of N: 1 to 21. Valid values of the MetricList.N.Type parameter:

 -   0: reports raw data
-   1: reports aggregate data

 **Note:** We recommend that you report aggregate data in both the aggregation periods of 60s and 300s. Otherwise, you cannot query monitoring data in a time span that is more than seven days. |
|MetricList.N.Values|String|Yes|\{"value":10.5\}|The collection of metric values. Valid values of N: 1 to 21.

 **Note:** If the MetricList.N.Type parameter is set to 0, the keys in this parameter must be set to the specified value. Cloud Monitor aggregates raw data in each aggregation period to generate multiple statistical values, such as the maximum value, the count, and the total value. |
|MetricList.N.Time|String|No|1508136760000|The timestamp when the metric data is generated. Valid values of N: 1 to 21. The timestamp can be in one of the following formats:

 -   The UTC timestamp, in the YYYY-MM-DDThh:mm:ssZ format. Example: 20171012T132456.888+0800.
-   The UNIX timestamp of the LONG type. Example: 1508136760000. |
|MetricList.N.Period|String|No|60|The aggregation period. Valid values of N: 1 to 21. Unit: seconds. Valid values: 60 and 300.

 **Note:** If the MetricList.N.Type parameter is set to 1, the MetricList.N.Period parameter is required. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|05B36C2C-5F6E-48D5-8B41-CE36DD7EE8E0|The ID of the request. |
|Code|String|200|The HTTP status code.

 **Note:** The value 200 indicates that the call was successful. |
|Message|String|The request has failed due to a temporary failure of the server.|The error message. |

## Examples

Sample request

```
http(s)://[Endpoint]/? Action=PutCustomMetric
&MetricList.1.Dimensions={"sampleName1":"value1","sampleName2":"value2"}
&MetricList.1.GroupId=12345
&MetricList.1.MetricName=cpu_total
&MetricList.1.Type=0
&MetricList.1.Values={"value":10.5}
&<Common request parameters>
```

Sample success responses

`XML` format

```
<PutCustomMetricResponse>
	  <RequestId>75D115CE-5DA8-4647-9073-8F72BB85B6F7</RequestId>
	  <Message>success</Message>
	  <Code>200</Code>
</PutCustomMetricResponse>
```

`JSON` format

```
{
  "RequestId": "75D115CE-5DA8-4647-9073-8F72BB85B6F7",
  "Message": "success",
  "Code": "200"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

