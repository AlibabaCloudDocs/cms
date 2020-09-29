# DescribeMonitorGroupNotifyPolicyList

Queries policies that are used to pause alert notifications for an application group.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeMonitorGroupNotifyPolicyList&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeMonitorGroupNotifyPolicyList|The operation that you want to perform. Set the value to DescribeMonitorGroupNotifyPolicyList. |
|PolicyType|String|Yes|PauseNotify|The type of the policy. Set the value to PauseNotify. |
|RegionId|String|Yes|China \(Hangzhou\)|The region where the policy to query was created. Valid values:

-   China \(Hangzhou\)
-   Singapore
-   Japan \(Tokyo\) |
|PageNumber|Integer|No|1|The number of the page to return. Default value: 1 |
|PageSize|Integer|No|100|The number of entries to return on each page. Default value: 10. |
|GroupId|String|No|123\*\*\*\*|The ID of the application group. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Message|String|The Request is not authorization.|The returned message. |
|NotifyPolicyList|Array of NotifyPolicy|N/A|The policies that were returned. |
|NotifyPolicy|N/A|N/A|N/A|
|EndTime|Long|1551761781273|The time when the policy expires. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|GroupId|String|123\*\*\*\*|The ID of the application group. |
|Id|String|123\*\*\*\*|The ID of the policy. |
|StartTime|Long|1551761781273|The time when the policy takes effect. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|Type|String|PauseNotify|The type of the policy. Default value: PauseNotify. |
|RequestId|String|6072F026-C441-41A6-B114-35A1E8F8FDD3|The ID of the request. |
|Success|String|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |
|Total|Integer|11|The total number of the returned entries. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DescribeMonitorGroupNotifyPolicyList
&PolicyType=PauseNotify
&RegionId=China (Hangzhou)
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeMonitorGroupNotifyPolicyListResponse>
    <NotifyPolicyList>
            <NotifyPolicy>
                  <Type>PauseNotify</Type>
                  <EndTime>1551763581273</EndTime>
                  <Id>123****</Id>
                  <StartTime>1551761781273</StartTime>
                  <GroupId>123****</GroupId>
            </NotifyPolicy>
      </NotifyPolicyList>
      <Success>true</Success>
      <Code>200</Code>
      <Total>1</Total>
</DescribeMonitorGroupNotifyPolicyListResponse>
```

`JSON` format

```
{
    "NotifyPolicyList": {
    "NotifyPolicy": [
      {
        "Type": "PauseNotify",
        "EndTime": 1551763581273,
        "Id": "123****",
        "StartTime": 1551761781273,
        "GroupId": "123****"
      }
    ]
  },
  "Success": true,
  "Code": "200",
  "Total": 1
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

