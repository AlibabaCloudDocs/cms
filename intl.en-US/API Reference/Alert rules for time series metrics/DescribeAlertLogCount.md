# DescribeAlertLogCount

Queries the statistics of alert logs.

This topic provides an example on how to query the statistics about alert logs of Elastic Compute Service \(ECS\) from the cloud service dimension.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeAlertLogCount&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeAlertLogCount|The operation that you want to perform. Set the value to DescribeAlertLogCount. |
|GroupBy|String|Yes|product|The dimension based on which data is aggregated. This parameter is similar to the Group By clause of SQL statements. Valid values:

-   `product`: aggregates data by cloud service.
-   `level`: aggregates data by alert level.
-   `groupId`: aggregates data by application group.
-   `contactGroup`: aggregates data by alert group.
-   `product,metricName`: aggregates data both by cloud service and by metric. |
|StartTime|Long|No|1609988009694|The start timestamp of the alert logs to be counted. Unit: milliseconds. |
|EndTime|Long|No|1610074409694|The end timestamp of the alert logs to be counted. Unit: milliseconds. |
|PageNumber|Integer|No|1|The number of the page to return. Default value: 1 |
|PageSize|Integer|No|10|The number of entries to return on each page. Default value: 10. |
|SearchKey|String|No|test|The keyword based on which the alert logs to be counted are searched. |
|Namespace|String|No|acs\_ecs\_dashboard|The namespace of the cloud service.

**Note:** For more information about the namespaces of cloud services, see [Appendix 1: Metrics](~~163515~~). |
|GroupId|String|No|7301\*\*\*\*|The ID of the application group. |
|Product|String|No|ECS|The abbreviation of the service name. |
|Level|String|No|P4|The level and notification method of the alert. Valid values:

-   P4: Alert notifications are sent by using emails and DingTalk chatbots.
-   OK: No alert is generated. |
|SendStatus|String|No|0|The status of the alert. Valid values:

-   0: The alert is triggered or cleared.
-   1: The alert is generated not during the effective period.
-   2: The alert is muted and not triggered in a specified period.
-   3: The host is restarting.
-   4: Notifications are not sent for the alert.

When the value of the SendStatus parameter is 0, the value P4 of the Level parameter indicates a triggered alert and the value OK indicates a cleared alert. |
|ContactGroup|String|No|ECS\_Group|The alert group. |
|RuleName|String|No|test123|The name of the alert rule. |
|MetricName|String|No|cpu\_total|The name of the metric.

**Note:** For more information about the metrics of different cloud services, see [Appendix 1: Metrics](~~163515~~). |
|LastMin|String|No|360|The statistical period of alert logs. Unit: minutes. |

For more information about common request parameters, see [Common parameters](~~199331~~).

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|AlertLogCount|Array of AlertLogCount|N/A|The statistics of alert logs. |
|Count|Integer|1|The number of alert logs. |
|Logs|Array of Logs|N/A|The details about alert logs. |
|Name|String|product|The name of the dimension field based on which alert logs are aggregated. |
|Value|String|ECS|The value of the dimension field based on which alert logs are aggregated. |
|Code|String|200|The HTTP status code.

**Note:** The HTTP status code 200 indicates a success. |
|Message|String|The specified resource is not found.|The error message. |
|RequestId|String|1C4A3709-BF52-42EE-87B5-7435F0929585|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeAlertLogCount
&GroupBy=product
&Product=ECS
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeAlertLogCountResponse>
      <RequestId>0BA67F6D-B699-4E3F-B205-93A5C38A0A2E</RequestId>
      <AlertLogCount>
            <Count>1</Count>
            <Logs>
                  <Value>ECS</Value>
                  <Name>product</Name>
            </Logs>
      </AlertLogCount>
      <Code>200</Code>
      <Success>true</Success>
</DescribeAlertLogCountResponse>
```

`JSON` format

```
{
    "RequestId": "0BA67F6D-B699-4E3F-B205-93A5C38A0A2E",
    "AlertLogCount": [
        {
            "Count": 1,
            "Logs": [
                {
                    "Value": "ECS",
                    "Name": "product"
                }
            ]
        }
    ],
    "Code": 200,
    "Success": true
}
```

## Error codes

|HTTP status code|Error code|Error message|Description|
|----------------|----------|-------------|-----------|
|404|ResourceNotFound|The specified resource is not found.|The error message returned because the specified resource is not found.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

