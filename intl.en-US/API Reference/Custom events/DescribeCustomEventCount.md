# DescribeCustomEventCount

Queries the number of times that a custom event occurred in a specified time period.

**Note:** This operation counts the number of times that a custom event occurred for each service.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeCustomEventCount&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeCustomEventCount|The operation that you want to perform. Set the value to DescribeCustomEventCount. |
|Name|String|No|BABEL\_BUY|The name of the custom event. |
|EventId|String|No|123|The ID of the custom event. |
|GroupId|String|No|12345|The ID of the application group. |
|SearchKeywords|String|No|cms|The keywords that are contained in the content of the custom event to query. You can use a logical operator between keywords.

-   If you need to query the custom event whose content contains a and b, set the value to a and b.
-   If you need to query the custom event whose content contains a or b, set the value to a or b. |
|StartTime|String|No|1552209685596|The beginning of the time range to query.

This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|EndTime|String|No|1552220485596|The end of the time range to query.

This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|60912C8D-B340-4253-ADE7-61ACDFD25CFC|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. The value true indicates a success. The value false indicates a failure. |
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|CustomEventCounts|Array|N/A|The details of the custom event. |
|CustomEventCount|N/A|N/A|N/A|
|Name|String|BABEL\_BUY|The name of the custom event. |
|Num|Integer|20|The number of times that the custom event occurred in the specified time period. |
|Time|Long|1552267615000|The time when the custom event occurred.

This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|Message|String|success|The returned message. If the call was successful, the value success is returned. If the call failed, an error message is returned. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DescribeCustomEventCount
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeCustomEventCount>
          <CustomEventCounts>
                <CustomEventCount>
                      <Name>BABEL_BUY</Name>
                      <Time>1552267615000</Time>
                      <Num>20</Num>
                </CustomEventCount>
          </CustomEventCounts>
          <Message>success</Message>
          <RequestId>38D3C270-6799-4461-AA55-7975352140C1</RequestId>
          <Code>200</Code>
          <Success>true</Success>
</DescribeCustomEventCount>
```

`JSON` format

```
{
    "CustomEventCounts": {
        "CustomEventCount": 
        {
            "Name":"BABEL_BUY",
            "Time":1552267615000,
            "Num":"20"
        }
    },
    "Message": "success",
    "RequestId": "38D3C270-6799-4461-AA55-7975352140C1",
    "Code": "200",
    "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

