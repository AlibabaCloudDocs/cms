# DescribeSystemEventAttribute

Queries the details of a system event occurred in a specified time period.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeSystemEventAttribute&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeSystemEventAttribute|The operation that you want to perform. Set the value to DescribeSystemEventAttribute. |
|Product|String|No|oss|The abbreviation of the service name.

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
|GroupId|String|No|12346|The ID of the application group. |
|SearchKeywords|String|No|cms|The keywords contained in the content of the system event to query. You can use a logical operator between keywords. Valid values:

-   If you need to query the system event whose content contains a and b, set the value to `a and b`.
-   If you need to query the system event whose content contains a or b, set the value to `a or b`. |
|StartTime|String|No|1552199984949|The beginning of the time range to query.

This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|EndTime|String|No|1552221584949|The end of the time range to query.

This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|PageNumber|Integer|No|1|The number of the page to return. Default value: 1 |
|PageSize|Integer|No|10|The number of entries to return on each page. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|60912C8D-B340-4253-ADE7-61ACDFD25CFC|The ID of the request. |
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Success|String|true|Indicates whether the call was successful. The value true indicates a success. The value false indicates a failure. |
|SystemEvents|Array|N/A|The details of the system event. |
|SystemEvent|N/A|N/A|N/A|
|Content|String|\[\{"product":"CloudMonitor","content":"\{\\"ipGroup\\":\\"112.126.XX.XX,10.163.XX.XX\\",\\"tianjimonVersion\\":\\"1.2.22\\"\}","groupId":"176,177,178,179,180,692,120812,1663836,96,2028302","time":"1552209568000","resourceId":"acs:ecs:cn-beijing:173651113438\*\*\*\*:instance/i-25k35\*\*\*\*","level":"CRITICAL","status":"stopped","instanceName":"cmssiteprobebj-6","name":"Agent\_Status\_Stopped","regionId":"cn-beijing"\}\]|The content of the system event. |
|GroupId|String|12345|The ID of the application group. |
|InstanceName|String|instanceId1|The name of the instance on which the system event occurred. |
|Level|String|WARN|The level of the system event. Valid values:

-   CRITICAL
-   WARN
-   INFO |
|Name|String|Agent\_Status\_Stopped|The name of the system event. |
|Product|String|CloudMonitor|The abbreviation of the service name. |
|RegionId|String|cn-hangzhou|The ID of the region where the instance resides. |
|ResourceId|String|xxxxx-1|The ID of the resource related to the system event. |
|Status|String|normal|The status of the system event. |
|Time|Long|1552199984000|The time when the system event occurred.

This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|Message|String|success|The returned message. If the call was successful, `success` is returned. If the call failed, an error message is returned. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeSystemEventAttribute
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeSystemEventAttribute>
          <SystemEvents>
                <SystemEvent>
                      <Status>normal</Status>
                      <InstanceName>instanceId1</InstanceName>
                      <ResourceId>xxxxx-1</ResourceId>
                      <Content>[{\"product\":\"CloudMonitor\",\"content\":\"{\\\"ipGroup\\\":\\\"112.126.XX.XX,10.163.XX.XX\\\",\\\"tianjimonVersion\\\":\\\"1.2.22\\\"}\",\"groupId\":\"176,177,178,179,180,692,120812,1663836,96,2028302\",\"time\":\"1552209568000\",\"resourceId\":\"acs:ecs:cn-beijing:173651113438****:instance/i-25k35****\",\"level\":\"CRITICAL\",\"status\":\"stopped\",\"instanceName\":\"cmssiteprobebj-6\",\"name\":\"Agent_Status_Stopped\",\"regionId\":\"cn-beijing\"}]</Content>
                      <Product>CloudMonitor</Product>
                      <Level>WARN</Level>
                      <Time>1552199984000</Time>
                      <RegionId>cn-hangzhou</RegionId>
                      <Name>Agent_Status_Stopped</Name>
                      <GroupId>12345</GroupId>
                </SystemEvent>
          </SystemEvents>
          <Message>success</Message>
          <RequestId>60912C8D-B340-4253-ADE7-61ACDFD25CFC</RequestId>
          <Code>200</Code>
          <Success>true</Success>
</DescribeSystemEventAttribute>
```

`JSON` format

```
{
    "SystemEvents":{
        "SystemEvent":[
            {
                "Status":"normal",
                "InstanceName":"instanceId1",
                "ResourceId":"xxxxx-1",
                "Content":"[{\"product\":\"CloudMonitor\",\"content\":\"{\\\"ipGroup\\\":\\\"112.126.XX.XX,10.163.XX.XX\\\",\\\"tianjimonVersion\\\":\\\"1.2.22\\\"}\",\"groupId\":\"176,177,178,179,180,692,120812,1663836,96,2028302\",\"time\":\"1552209568000\",\"resourceId\":\"acs:ecs:cn-beijing:173651113438****:instance/i-25k35****\",\"level\":\"CRITICAL\",\"status\":\"stopped\",\"instanceName\":\"cmssiteprobebj-6\",\"name\":\"Agent_Status_Stopped\",\"regionId\":\"cn-beijing\"}]",
                "Product":"CloudMonitor",
                "Level":"WARN",
                "Time":"1552199984000",
                "RegionId":"cn-hangzhou",
                "Name":"Agent_Status_Stopped",
                "GroupId":"12345"
            }]
    },
    "Message":"success",
    "RequestId":"60912C8D-B340-4253-ADE7-61ACDFD25CFC",
    "Code":"200",
    "Success":"true"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

