# DescribeContactList

Queries alert contacts.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeContactList&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeContactList|The operation that you want to perform. Set the value to DescribeContactList. |
|PageSize|Integer|No|10|The number of entries to return on each page. Default value: 100. |
|PageNumber|Integer|No|1|The number of the page to return. Default value: 1 |
|ContactName|String|No|Alice|The name of the alert contact. |
|ChanelType|String|No|Email|The alert notification method.

Alert notifications can be sent by using emails or DingTalk chatbots. |
|ChanelValue|String|No|testxx\*\*\*\*@aliyun.com|The alert notification target.

If you set the ChanelType parameter to Email, set the value of the ChanelValue parameter to an email address of the alert contact that you want to query. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|06D5ECC2-B9BE-42A4-8FA3-1A610FB08B83|The ID of the request. |
|Message|String|The Request is not authorization.|The returned message. |
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |
|Contacts|Array of Contact|N/A|The alert contact information. |
|Contact|N/A|N/A|N/A|
|Channels|Struct|N/A|The alert notification targets. |
|AliIM|String|Alice|The TradeManager ID of the alert contact. |
|DingWebHook|String|https://oapi.dingtalk.com/robot/send?access\_token=9bf44f8189597d07dfdd7a123455ffc112\*\*\*\*|The webhook URL of the DingTalk chatbot. |
|Mail|String|someone@example.com|The email address of the alert contact. |
|SMS|String|1333333\*\*\*\*|The phone number of the alert contact. |
|ChannelsState|Struct|N/A|The status of the alert notification target. Valid values: PENDING and OK.

The email address must be activated after it is added as an alert notification target. The value PENDING indicates that the email address is not activated. The value OK indicates that the email address is activated. |
|AliIM|String|OK|The status of the TradeManager ID.

The value is fixed to OK. The value OK indicates that the TradeManager ID is valid and can receive alert notifications. |
|DingWebHook|String|OK|The status of the DingTalk chatbot.

The value is fixed to OK. The value OK indicates that the DingTalk chatbot is normal and alert notifications can be received in a DingTalk group. |
|Mail|String|PENDING|The status of the email address. Valid values:

-   PENDING: The email address is not activated. Alert notifications can be sent to the email address only after the email address is activated.
-   OK: The email address is activated and can receive alert notifications. |
|SMS|String|OK|The status of the phone number. Valid values:

-   PENDING: The phone number is not activated. Alert notifications can be sent to the phone number by using text messages only after the phone number is activated.
-   OK: The phone number is activated and can receive alert notifications. |
|ContactGroups|List|\{ "ContactGroup": \[ "ECS\_Group", "Jim" \] \}|The alert groups to which the alert contact is added. |
|CreateTime|Long|1552356159000|The time when the alert contact was created. |
|Desc|String|My alert notification method|The description of the alert contact. |
|Lang|String|zh-cn|The language in which the alert information is displayed. Valid values:

-   zh-cn: simplified Chinese
-   en: English |
|Name|String|Alice|The name of the alert contact. |
|UpdateTime|Long|1552356159000|The time when the alert contact was modified. |
|Total|Integer|15|The total number of the returned entries. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DescribeContactList
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeContactListResponse>
          <RequestId>A1267F27-942F-40EE-9254-57FE16E3C9AB</RequestId>
          <Contacts>
                <Contact>
                      <Desc>Contact Desc</Desc>
                      <ContactGroups>
                            <ContactGroup>ECS_Group</ContactGroup>
                            <ContactGroup>Jim</ContactGroup>
                      </ContactGroups>
                      <ChannelsState>
                            <SMS>PENDING</SMS>
                            <Mail>OK</Mail>
                      </ChannelsState>
                      <CreateTime>1583307692000</CreateTime>
                      <UpdateTime>1589441072000</UpdateTime>
                      <Channels>
                            <Mail>someone@example.com</Mail>
                            <SMS>155*******</SMS>
                      </Channels>
                      <Name>Alice</Name>
                      <Lang>zh-cn</Lang>
                </Contact>
          </Contacts>
          <Total>25</Total>
          <Code>200</Code>
          <Success>true</Success>
</DescribeContactListResponse>
```

`JSON` format

```
{
    "RequestId": "A1267F27-942F-40EE-9254-57FE16E3C9AB",
    "Contacts": {
        "Contact": [
            {
                "Desc": "Contact Desc",
                "ContactGroups": {
                    "ContactGroup": [
                        "ECS_Group",
                        "Jim"
                    ]
                },
                "ChannelsState":{
                    "SMS":"PENDING",
                    "Mail":"OK"
                },
                "CreateTime": 1583307692000,
                "UpdateTime": 1589441072000,
                "Channels": {
                    "Mail": "someone@example.com",
                    "SMS": "155*******"
                },
                "Name": "Alice",
                "Lang":"zh-cn"
            }
        ]
    },
    "Total": 25,
    "Code": "200",
    "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

