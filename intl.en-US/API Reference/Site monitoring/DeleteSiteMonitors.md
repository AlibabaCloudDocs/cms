# DeleteSiteMonitors

Deletes one or more site monitoring tasks.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DeleteSiteMonitors&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DeleteSiteMonitors|The operation that you want to perform. Set the value to DeleteSiteMonitors. |
|TaskIds|String|Yes|01adacc2-ece5-41b6-afa2-3143ab5d\*\*\*\*,43bd1ead-514f-4524-813e-228ce091\*\*\*\*|The IDs of the site monitoring tasks to delete. Separate multiple task IDs with commas \(,\). |
|IsDeleteAlarms|Boolean|No|true|Specifies whether to delete the alert rules configured for the site monitoring tasks to delete. Default value: true. Valid values:

-   true
-   false |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Data|Struct|N/A|The information about the site monitoring tasks that were deleted. |
|count|Integer|0|The number of the site monitoring tasks that were deleted. |
|Message|String|success|The returned message. If the call was successful, the value success is returned. If the call failed, an error message such as `TaskId not found` is returned. |
|RequestId|String|123BCC5D-8B63-48EA-B747-9A8995BE7AA6|The ID of the request. |
|Success|String|true|Indicates whether the call was successful. The value true indicates a success. The value false indicates a failure. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DeleteSiteMonitors
&TaskIds=01adacc2-ece5-41b6-afa2-3143ab5d****,43bd1ead-514f-4524-813e-228ce091****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DeleteSiteMonitorsResponse>
        <Data>
            <count>0</count>
        </Data>
        <Message>success</Message>
        <RequestId>123BCC5D-8B63-48EA-B747-9A8995BE7AA6</RequestId>
        <Success>true</Success>
        <Code>200</Code>
<DeleteSiteMonitorsResponse>
```

`JSON` format

```
{
  "Data": {
    "count": 0
  },
  "Message":"success",
  "RequestId": "123BCC5D-8B63-48EA-B747-9A8995BE7AA6",
  "Success": true,
  "Code": "200"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

