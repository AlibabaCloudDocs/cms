# DeleteDynamicTagGroup

Deletes a tag rule.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DeleteDynamicTagGroup&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DeleteDynamicTagGroup|The operation that you want to perform. Set the value to DeleteDynamicTagGroup. |
|DynamicTagRuleId|String|Yes|6b882d9a-5117-42e2-9d0c-4749a0c6\*\*\*\*|The ID of the tag rule. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |
|RequestId|String|ACBDBB40-DFB6-4F4C-8957-51FFB233969C|The ID of the request. |
|Message|String|The Request is not authorization.|The returned message. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DeleteDynamicTagGroup
&DynamicTagRuleId=6b882d9a-5117-42e2-9d0c-4749a0c6****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DeleteDynamicTagGroupResponse>
	  <RequestId>08AAE67E-77B5-485B-9C79-D7C8C059150A</RequestId>
	  <Code>200</Code>
</DeleteDynamicTagGroupResponse>
```

`JSON` format

```
{
	"RequestId": "08AAE67E-77B5-485B-9C79-D7C8C059150A",
	"Code": 200,
	"Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

