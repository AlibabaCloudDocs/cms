# DescribeUnhealthyHostAvailability

Queries unhealthy instances.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeUnhealthyHostAvailability&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeUnhealthyHostAvailability|The operation that you want to perform. Set the value to DescribeUnhealthyHostAvailability. |
|Id.N|RepeatList|Yes|123456|The ID of the availability monitoring task. Valid values of N: 1 to 20. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Message|String|User not authorized to operate on the specified resource.|The returned message. |
|RequestId|String|ACBDBB40-DFB6-4F4C-8957-51FFB233969C|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |
|UnhealthyList|Array of NodeTaskInstance|N/A|The unhealthy instances that are detected by the specified availability monitoring tasks. |
|NodeTaskInstance|N/A|N/A|N/A|
|Id|Long|123456|The ID of the availability monitoring task. |
|InstanceList|List|i-a34b581\*\*\*\*|The unhealthy instances that are detected by the availability monitoring task. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DescribeUnhealthyHostAvailability
&Id.1=123456
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeUnhealthyHostAvailabilityResponse>
          <RequestId>8C2F25CB-F9E7-4693-95C7-A095417B2948</RequestId>
          <Code>200</Code>
          <Success>true</Success>
          <UnhealthyList>
                <NodeTaskInstance>
                      <Id>123456</Id>
                      <InstanceList>
                            <String>i-a34b581****</String>
                      </InstanceList>
                </NodeTaskInstance>
          </UnhealthyList>
</DescribeUnhealthyHostAvailabilityResponse>
```

`JSON` format

```
{
    "RequestId": "8C2F25CB-F9E7-4693-95C7-A095417B2948",
    "Code": 200,
    "Success": true,
    "UnhealthyList": {
        "NodeTaskInstance": [
            {
                "Id": 123456,
                "InstanceList": {
                    "String": ["i-a34b581****"]
                }
            } 
        ]
    }
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

