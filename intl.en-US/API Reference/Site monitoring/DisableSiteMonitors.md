# DisableSiteMonitors

Disables one or more site monitoring tasks.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DisableSiteMonitors&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DisableSiteMonitors|The operation that you want to perform. Set the value to DisableSiteMonitors. |
|TaskIds|String|Yes|49f7b317-7645-4cc9-94fd-ea42e522\*\*\*\*,49f7b317-7645-4cc9-94fd-ea42e522\*\*\*\*|The IDs of the site monitoring tasks. Separate multiple IDs with commas \(,\). |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The status code.

 **Note:** The status code 200 indicates a success. |
|Data|Struct| |The number of detection points that were monitored by the site monitoring tasks. |
|count|Integer|0|The number of detection points. |
|Message|String|successful|The returned message. |
|RequestId|String|3fcd12e7-d387-42ee-b77e-661c775bb17f|The ID of the request. |
|Success|String|true|Indicates whether the operation was successful. Valid values:

 -   true: successful.
-   false: failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DisableSiteMonitors
&TaskIds=49f7b317-7645-4cc9-94fd-ea42e522****,49f7b317-7645-4cc9-94fd-ea42e522****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DisableSiteMonitorsResponse>
	  <Message>successful</Message>
	  <RequestId>EC3F33C8-9149-493C-92A8-9B33A9DA951C</RequestId>
	  <Data>
		    <count>0</count>
	  </Data>
	  <Code>200</Code>
	  <Success>true</Success>
</DisableSiteMonitorsResponse>
```

`JSON` format

```
{
	"Message": "successful",
	"RequestId": "EC3F33C8-9149-493C-92A8-9B33A9DA951C",
	"Data": {
		"count": 0
	},
	"Code": "200",
	"Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

