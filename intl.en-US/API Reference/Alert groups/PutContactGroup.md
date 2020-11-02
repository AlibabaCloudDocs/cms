# PutContactGroup

Creates or modifies an alert group.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=PutContactGroup&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|PutContactGroup|The operation that you want to perform. Set the value to PutContactGroup. |
|ContactGroupName|String|Yes|ECS\_Group|The name of the alert group. |
|Describe|String|No|ECS alert group|The description of the alert group. |
|ContactNames.N|RepeatList|No|Alice|The name of the alert contact. Valid values of N: 1 to 100. |
|EnableSubscribed|Boolean|No|true|Specifies whether to enable the weekly report subscription feature. Valid values:

 -   true
-   false

 **Note:** The weekly report subscription feature can be used only by Alibaba Cloud accounts with more than five Elastic Compute Service \(ECS\) instances. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Message|String|success|The returned message. |
|RequestId|String|06D5ECC2-B9BE-42A4-8FA3-1A610FB08B83|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=PutContactGroup
&ContactGroupName=group1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<PutContactGroupResponse>
      <Code>200</Code>
      <Message>success</Message>
      <RequestId>181C406E-9DE4-484C-9C61-37AE9A1A12EE</RequestId>
      <Success>true</Success>
</PutContactGroupResponse>
```

`JSON` format

```
{
    "Code":"200",
    "Message":"success",
    "RequestId":"06D5ECC2-B9BE-42A4-8FA3-1A610FB08B83",
    "Success":true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

