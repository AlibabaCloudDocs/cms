# DeleteMonitorGroupNotifyPolicy

Deletes a policy that is used to pause alert notifications for a specified application group.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DeleteMonitorGroupNotifyPolicy&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DeleteMonitorGroupNotifyPolicy|The operation that you want to perform. Set the value to DeleteMonitorGroupNotifyPolicy. |
|PolicyType|String|Yes|PauseNotify|The type of the policy. Set the value to PauseNotify. |
|RegionId|String|Yes|China \(Hangzhou\)|The region where the policy to delete was created. Valid values:

-   China \(Hangzhou\)
-   Singapore
-   Japan \(Tokyo\) |
|GroupId|String|No|123456|The ID of the application group. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Message|String|The Request is not authorization.|The returned message. |
|RequestId|String|B7AF834D-D38B-4A46-920B-FE974EB7E135|The ID of the request. |
|Result|Integer|1|The number of policies that were deleted. |
|Success|String|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DeleteMonitorGroupNotifyPolicy
&PolicyType=PauseNotify
&RegionId=China (Hangzhou)
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DeleteMonitorGroupNotifyPolicyResponse>
      <Result>1</Result>
      <Success>true</Success>
      <Code>200</Code>
</DeleteMonitorGroupNotifyPolicyResponse>
```

`JSON` format

```
{
    "Result":1,
    "RequestId":"5D0D3910-5B01-4868-A2F2-A5DEA7F5150E",
    "Success":true,
    "Code":200
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

