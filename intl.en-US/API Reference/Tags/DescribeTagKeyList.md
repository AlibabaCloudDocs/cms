# DescribeTagKeyList

Queries tag keys.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeTagKeyList&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeTagKeyList|The operation that you want to perform. Set the value to DescribeTagKeyList. |
|PageNumber|Integer|No|1|The number of the page to return.

 Pages start from page 1. Default value: 1. |
|PageSize|Integer|No|10|The number of entries to return on each page.

 Maximum value: 100. Default value: 50. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|B04B8CF3-4489-432D-83BA-6F128E5F2293|The ID of the request. |
|Message|String|Specified parameter PageSize is not valid.|The error message. |
|Code|String|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |
|TagKeys|List|tagKey1|The tag keys returned. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeTagKeyList
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeTagKeyListResponse>
	  <TagKeys>
		    <TagKey>tagKey1</TagKey>
		    <TagKey>tagKey2</TagKey>
	  </TagKeys>
	  <RequestId>FA9A8612-C770-4264-8A9C-C90F0081B4F5</RequestId>
	  <Success>true</Success>
	  <Code>200</Code>
</DescribeTagKeyListResponse>
```

`JSON` format

```
{
	"TagKeys": {
		"TagKey": [
			"tagKey1",
			"tagKey2"
		]
	},
	"RequestId": "FA9A8612-C770-4264-8A9C-C90F0081B4F5",
	"Success": true,
	"Code": 200
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

