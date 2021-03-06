# DisableHostAvailability

Disables the specified availability monitoring tasks.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DisableHostAvailability&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DisableHostAvailability|The operation that you want to perform. Set the value to DisableHostAvailability. |
|Id.N|RepeatList|Yes|12345|The ID of the availability monitoring task. Valid values of N: 1 to 20. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The status code.

 **Note:** The status code 200 indicates a success. |
|Message|String|User not authorized to operate on the specified resource.|The error message. |
|RequestId|String|ACBDBB40-DFB6-4F4C-8957-51FFB233969C|The ID of the request. |
|Success|Boolean|true|Indicates whether the operation was successful. Valid values:

 -   true: successful.
-   false: failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DisableHostAvailability
&Id.1=12345
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DisableHostAvailabilityResponse>
      <RequestId>ACBDBB40-DFB6-4F4C-8957-51FFB233969C</RequestId>
      <Success>true</Success>
      <Code>200</Code>
</DisableHostAvailabilityResponse>
```

`JSON` format

```
{
  "RequestId": "ACBDBB40-DFB6-4F4C-8957-51FFB233969C",
  "Success": true,
  "Code": 200
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

