# CreateMonitorGroupNotifyPolicy

Creates a policy to pause alert notifications for an application group.

No alert notifications are sent for the application group during the effective period of the policy.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=CreateMonitorGroupNotifyPolicy&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CreateMonitorGroupNotifyPolicy|The operation that you want to perform. Set the value to CreateMonitorGroupNotifyPolicy. |
|GroupId|String|Yes|12345|The ID of the application group. |
|PolicyType|String|Yes|PauseNotify|The type of the policy. Set the value to PauseNotify. |
|StartTime|Long|Yes|1551756547863|The time when the policy takes effect.

This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|EndTime|Long|Yes|1551757147863|The time when the policy expires.

This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|RegionId|String|Yes|China \(Hangzhou\)|The region where you want to create the policy. Valid values:

-   China \(Hangzhou\)
-   Singapore
-   Japan \(Tokyo\) |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|13356BCA-3EC3-4748-A771-2064DA69AEF1|The ID of the request. |
|Success|String|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Result|Integer|1|The number of policies that were created. |
|Message|String|The Request is not authorization.|The returned message. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=CreateMonitorGroupNotifyPolicy
&GroupId=12345
&PolicyType=PauseNotify
&StartTime=1551756547863
&EndTime=1551757147863
&RegionId=China (Hangzhou)
&<Common request parameters>
```

Sample success responses

`XML` format

```
<CreateMonitorGroupNotifyPolicyResponse>
          <RequestId>13356BCA-3EC3-4748-A771-2064DA69AEF1</RequestId>
          <Result>1</Result>
          <Success>true</Success>
          <Code>200</Code>
</CreateMonitorGroupNotifyPolicyResponse>
```

`JSON` format

```
{
  "RequestId":"13356BCA-3EC3-4748-A771-2064DA69AEF1",
  "Result": 1,
  "Success": true,
  "Code": "200"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

