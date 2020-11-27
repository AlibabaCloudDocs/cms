# DescribeTagValueList

Queries tag values.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeTagValueList&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeTagValueList|The operation that you want to perform. Set the value to DescribeTagValueList. |
|TagKey|String|Yes|tagKey1|The key of the tag whose value you want to query. |
|PageNumber|Integer|No|1|The number of the page to return.

 Pages start from page 1. Default value: 1. |
|PageSize|Integer|No|10|The number of entries to return on each page.

 Maximum value: 100. Default value: 10. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|B04B8CF3-4489-432D-83BA-6F128E4F2295|The ID of the request. |
|Message|String|Specified parameter PageNumber is not valid.|The error message. |
|Code|String|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |
|TagValues|List|tagValue1|The tag values returned. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeTagValueList
&TagKey=tagKey1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeTagValueListResponse>
	  <RequestId>9AF637BA-6617-41FE-A0FA-3301521377A4</RequestId>
	  <TagValues>
		    <TagValue>tagValue1</TagValue>
		    <TagValue>tagValue2</TagValue>
	  </TagValues>
	  <Success>true</Success>
	  <Code>200</Code>
</DescribeTagValueListResponse>
```

`JSON` format

```
{
	"RequestId": "9AF637BA-6617-41FE-A0FA-3301521377A4",
	"TagValues": {
		"TagValue": [
			"tagValue1",
			"tagValue2"
		]
	},
	"Success": true,
	"Code": 200
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

