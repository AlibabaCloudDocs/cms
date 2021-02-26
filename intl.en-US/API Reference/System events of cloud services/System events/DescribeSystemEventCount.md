# DescribeSystemEventCount

Queries the number of times that a system event occurred in a specified time period.

**Note:** This operation counts the number of times that a system event occurred for each service.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeSystemEventCount&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeSystemEventCount|The operation that you want to perform. Set the value to DescribeSystemEventCount. |
|Product|String|No|oss|The abbreviation of the service name.

**Note:** You can call the [DescribeSystemEventMetaList](~~114972~~) operation to query the abbreviations of service names. |
|EventType|String|No|Exception|The type of the system event.

**Note:** You can call the [DescribeSystemEventMetaList](~~114972~~) operation to query the types of system events. |
|Name|String|No|BucketIngressBandwidth|The name of the system event.

**Note:** You can call the [DescribeSystemEventMetaList](~~114972~~) operation to query the names of system events. |
|Level|String|No|WARN|The level of the system event. Valid values:

-   CRITICAL
-   WARN
-   INFO |
|Status|String|No|normal|The status of the system event.

**Note:** You can call the [DescribeSystemEventMetaList](~~114972~~) operation to query the statuses of system events. |
|GroupId|String|No|12345|The ID of the application group. |
|SearchKeywords|String|No|cms|The keywords that are contained in the content of the system event to query. You can use a logical operator between keywords. Valid values:

-   If you need to query the system event whose content contains a and b, set the value to `a and b`.
-   If you need to query the system event whose content contains a or b, set the value to `a or b`. |
|StartTime|String|No|1552209685596|The beginning of the time range to query.

This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|EndTime|String|No|1552220485596|The end of the time range to query.

This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |

You can call the [DescribeSystemEventMetaList](~~114972~~) operation to obtain information about the services for which system event monitoring is enabled. The returned information includes the abbreviation of the service name, event name, event level, and event status.

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|60912C8D-B340-4253-ADE7-61ACDFD25CFC|The ID of the request. |
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Success|String|true|Indicates whether the call was successful. The value true indicates a success. The value false indicates a failure. |
|SystemEventCounts|Array|N/A|The details of the system event occurred in the specified time period. |
|SystemEventCount|N/A|N/A|N/A|
|Content|String|xxxx|The content of the system event. |
|GroupId|String|123456|The ID of the application group. |
|InstanceName|String|instanceId1|The name of the instance on which the system event occurred. |
|Level|String|WARN|The level of the system event. Valid values:

-   CRITICAL
-   WARN
-   INFO |
|Name|String|Agent\_Status\_Stopped|The name of the system event. |
|Num|Long|2|The number of times that the system event occurred in the specified time period. |
|Product|String|ECS|The abbreviation of the service name. |
|RegionId|String|cn-hangzhou|The ID of the region where the instance resides. |
|ResourceId|String|xxxxx-1|The ID of the resource related to the system event. |
|Status|String|normal|The status of the system event. |
|Time|Long|1552199984000|The time when the system event occurred.

This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|Message|String|success|The returned message. If the call was successful, the value success is returned. If the call failed, an error message is returned. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DescribeSystemEventCount
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeSystemEventCount>
          <Message>success</Message>
          <RequestId>60912C8D-B340-4253-ADE7-61ACDFD25CFC</RequestId>
          <SystemEventCounts>
                <SystemEventCount>
                      <Status>normal</Status>
                      <InstanceName>instanceId1</InstanceName>
                      <ResourceId>xxxxx-1</ResourceId>
                      <Content>xxxx</Content>
                      <Num>2</Num>
                      <Product>ECS</Product>
                      <Level>WARN</Level>
                      <Time>1552199984000</Time>
                      <RegionId>cn-hangzhou</RegionId>
                      <Name>Agent_Status_Stopped</Name>
                      <GroupId>123456</GroupId>
                </SystemEventCount>
          </SystemEventCounts>
          <Code>200</Code>
          <Success>true</Success>
</DescribeSystemEventCount>
```

`JSON` format

```
{
    "Message":"success",
    "RequestId":"60912C8D-B340-4253-ADE7-61ACDFD25CFC",
    "SystemEventCounts":{
        "SystemEventCount":[
            {
                "Status":"normal",
                "InstanceName":"instanceId1",
                "ResourceId":"xxxxx-1",
                "Content":"xxxx",
                "Num":"2",
                "Product":"ECS",
                "Level":"WARN",
                "Time":"1552199984000",
                "RegionId":"cn-hangzhou",
                "Name":"Agent_Status_Stopped",
                "GroupId":"123456"
            }]
    },
    "Code":"200",
    "Success":"true"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

