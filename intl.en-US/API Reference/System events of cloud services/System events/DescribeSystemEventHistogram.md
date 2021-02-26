# DescribeSystemEventHistogram

Queries the number of times that a system event occurred during each interval of a time period.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeSystemEventHistogram&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeSystemEventHistogram|The operation that you want to perform. Set the value to DescribeSystemEventHistogram. |
|Product|String|No|OSS|The abbreviation of the service name.

**Note:** You can call the [DescribeSystemEventMetaList](~~114972~~) operation to view the abbreviations of service names. |
|EventType|String|No|Exception|The type of the system event.

**Note:** You can call the [DescribeSystemEventMetaList](~~114972~~) operation to view the types of system events. |
|Name|String|No|BucketIngressBandwidth|The name of the system event.

**Note:** You can call the [DescribeSystemEventMetaList](~~114972~~) operation to view the names of system events. |
|Level|String|No|CRITICAL|The level of the system event. Valid values:

-   CRITICAL
-   WARN
-   INFO |
|Status|String|No|normal|The status of the system event.

**Note:** You can call the [DescribeSystemEventMetaList](~~114972~~) operation to view the statuses of system events. |
|GroupId|String|No|12345|The ID of the application group. |
|SearchKeywords|String|No|cms|The keywords contained in the content of the system event to query. You can use a logical operator between keywords. Examples:

-   If you need to query the system event whose content contains a and b, set the value to `a and b`.
-   If you need to query the system event whose content contains a or b, set the value to `a or b`. |
|StartTime|String|No|1552209685596|The beginning of the time range to query.

This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|EndTime|String|No|1552220485596|The end of the time range to query.

This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|486029C9-53E1-44B4-85A8-16A571A043FD|The ID of the request. |
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Success|String|true|Indicates whether the call was successful. The value true indicates a success. The value false indicates a failure. |
|SystemEventHistograms|Array|N/A|The information about the number of times that the system event occurred during each interval of a time period. |
|SystemEventHistogram|N/A|N/A|N/A|
|Count|Long|2|The number of times that the system event occurred. |
|EndTime|Long|1552225753000|The end of an interval.

This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|StartTime|Long|1552225770000|The beginning of an interval.

This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|Message|String|The Request is not authorization.|The returned message. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeSystemEventHistogram
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeSystemEventHistogram>
          <RequestId>E38CA81A-A012-4C59-B694-42AAFBE27ED2</RequestId>
          <SystemEventHistograms>
                <SystemEventHistogram>
                      <EndTime>1593671700000</EndTime>
                      <StartTime>1593671684000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593671730000</EndTime>
                      <StartTime>1593671700000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593671760000</EndTime>
                      <StartTime>1593671730000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593671790000</EndTime>
                      <StartTime>1593671760000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593671820000</EndTime>
                      <StartTime>1593671790000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593671850000</EndTime>
                      <StartTime>1593671820000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593671880000</EndTime>
                      <StartTime>1593671850000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593671910000</EndTime>
                      <StartTime>1593671880000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593671940000</EndTime>
                      <StartTime>1593671910000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593671970000</EndTime>
                      <StartTime>1593671940000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672000000</EndTime>
                      <StartTime>1593671970000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672030000</EndTime>
                      <StartTime>1593672000000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672060000</EndTime>
                      <StartTime>1593672030000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672090000</EndTime>
                      <StartTime>1593672060000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672120000</EndTime>
                      <StartTime>1593672090000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672150000</EndTime>
                      <StartTime>1593672120000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672180000</EndTime>
                      <StartTime>1593672150000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672210000</EndTime>
                      <StartTime>1593672180000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672240000</EndTime>
                      <StartTime>1593672210000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672270000</EndTime>
                      <StartTime>1593672240000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672300000</EndTime>
                      <StartTime>1593672270000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672330000</EndTime>
                      <StartTime>1593672300000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672360000</EndTime>
                      <StartTime>1593672330000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672390000</EndTime>
                      <StartTime>1593672360000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672420000</EndTime>
                      <StartTime>1593672390000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672450000</EndTime>
                      <StartTime>1593672420000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672480000</EndTime>
                      <StartTime>1593672450000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672510000</EndTime>
                      <StartTime>1593672480000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672540000</EndTime>
                      <StartTime>1593672510000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672570000</EndTime>
                      <StartTime>1593672540000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
                <SystemEventHistogram>
                      <EndTime>1593672584000</EndTime>
                      <StartTime>1593672570000</StartTime>
                      <Count>0</Count>
                </SystemEventHistogram>
          </SystemEventHistograms>
          <Code>200</Code>
          <Success>true</Success>
</DescribeSystemEventHistogram>
```

`JSON` format

```
{
    "RequestId": "E38CA81A-A012-4C59-B694-42AAFBE27ED2",
    "SystemEventHistograms": {
        "SystemEventHistogram": [
            {
                "EndTime": 1593671700000,
                "StartTime": 1593671684000,
                "Count": 0
            },
            {
                "EndTime": 1593671730000,
                "StartTime": 1593671700000,
                "Count": 0
            },
            {
                "EndTime": 1593671760000,
                "StartTime": 1593671730000,
                "Count": 0
            },
            {
                "EndTime": 1593671790000,
                "StartTime": 1593671760000,
                "Count": 0
            },
            {
                "EndTime": 1593671820000,
                "StartTime": 1593671790000,
                "Count": 0
            },
            {
                "EndTime": 1593671850000,
                "StartTime": 1593671820000,
                "Count": 0
            },
            {
                "EndTime": 1593671880000,
                "StartTime": 1593671850000,
                "Count": 0
            },
            {
                "EndTime": 1593671910000,
                "StartTime": 1593671880000,
                "Count": 0
            },
            {
                "EndTime": 1593671940000,
                "StartTime": 1593671910000,
                "Count": 0
            },
            {
                "EndTime": 1593671970000,
                "StartTime": 1593671940000,
                "Count": 0
            },
            {
                "EndTime": 1593672000000,
                "StartTime": 1593671970000,
                "Count": 0
            },
            {
                "EndTime": 1593672030000,
                "StartTime": 1593672000000,
                "Count": 0
            },
            {
                "EndTime": 1593672060000,
                "StartTime": 1593672030000,
                "Count": 0
            },
            {
                "EndTime": 1593672090000,
                "StartTime": 1593672060000,
                "Count": 0
            },
            {
                "EndTime": 1593672120000,
                "StartTime": 1593672090000,
                "Count": 0
            },
            {
                "EndTime": 1593672150000,
                "StartTime": 1593672120000,
                "Count": 0
            },
            {
                "EndTime": 1593672180000,
                "StartTime": 1593672150000,
                "Count": 0
            },
            {
                "EndTime": 1593672210000,
                "StartTime": 1593672180000,
                "Count": 0
            },
            {
                "EndTime": 1593672240000,
                "StartTime": 1593672210000,
                "Count": 0
            },
            {
                "EndTime": 1593672270000,
                "StartTime": 1593672240000,
                "Count": 0
            },
            {
                "EndTime": 1593672300000,
                "StartTime": 1593672270000,
                "Count": 0
            },
            {
                "EndTime": 1593672330000,
                "StartTime": 1593672300000,
                "Count": 0
            },
            {
                "EndTime": 1593672360000,
                "StartTime": 1593672330000,
                "Count": 0
            },
            {
                "EndTime": 1593672390000,
                "StartTime": 1593672360000,
                "Count": 0
            },
            {
                "EndTime": 1593672420000,
                "StartTime": 1593672390000,
                "Count": 0
            },
            {
                "EndTime": 1593672450000,
                "StartTime": 1593672420000,
                "Count": 0
            },
            {
                "EndTime": 1593672480000,
                "StartTime": 1593672450000,
                "Count": 0
            },
            {
                "EndTime": 1593672510000,
                "StartTime": 1593672480000,
                "Count": 0
            },
            {
                "EndTime": 1593672540000,
                "StartTime": 1593672510000,
                "Count": 0
            },
            {
                "EndTime": 1593672570000,
                "StartTime": 1593672540000,
                "Count": 0
            },
            {
                "EndTime": 1593672584000,
                "StartTime": 1593672570000,
                "Count": 0
            }
        ]
    },
    "Code": "200",
    "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

