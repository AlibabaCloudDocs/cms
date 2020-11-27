# DescribeContactListByContactGroup

Queries the alert contacts in an alert group.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeContactListByContactGroup&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeContactListByContactGroup|The operation that you want to perform. Set the value to DescribeContactListByContactGroup. |
|ContactGroupName|String|Yes|CloudMonitor|The name of the alert group. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Contacts|Array of Contact| |The alert group. |
|Contact| | | |
|Channels|Struct| |The alert notification targets. |
|AliIM|String|Alice|The TradeManager ID of the alert contact.

 **Note:** This parameter can be returned only on the China site \(aliyun.com\). |
|DingWebHook|String|https://oapi.dingtalk.com/robot/send?access\_token=9bf44f8189597d07dfdd7a123455ffc112\*\*\*\*|The webhook URL of the DingTalk chatbot. |
|Mail|String|alice@example.com|The email address of the alert contact. |
|SMS|String|1333333\*\*\*\*|The phone number of the alert contact.

 **Note:** This parameter can be returned only on the China site \(aliyun.com\). |
|CreateTime|Long|1552314252000|The time when the alert contact was created. |
|Desc|String|ECS|The description of the alert contact. |
|Name|String|Alice|The name of the alert contact. |
|UpdateTime|Long|1552314252000|The time when the alert contact was modified. |
|Message|String|The group is not exists.|The error message. |
|RequestId|String|06D5ECC2-B9BE-42A4-8FA3-1A610FB08B83|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeContactListByContactGroup
&ContactGroupName=CloudMonitor
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeContactListByContactGroupResponse>
	  <RequestId>96B41DE5-6DC9-4FAF-A790-3D4AA17C1F09</RequestId>
	  <Contacts>
		    <Contact>
			      <Desc></Desc>
			      <CreateTime>1604024233000</CreateTime>
			      <UpdateTime>1604024233000</UpdateTime>
			      <Channels>
				        <SMS></SMS>
			      </Channels>
			      <Name>Alice</Name>
		    </Contact>
	  </Contacts>
	  <Code>200</Code>
	  <Success>true</Success>
</DescribeContactListByContactGroupResponse>
```

`JSON` format

```
{
  "RequestId": "96B41DE5-6DC9-4FAF-A790-3D4AA17C1F09",
  "Contacts": {
    "Contact": [
      {
        "Desc": "",
        "CreateTime": 1604024233000,
        "UpdateTime": 1604024233000,
        "Channels": {
          "SMS": ""
        },
        "Name": "Alice"
      }
    ]
  },
  "Code": "200",
  "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

