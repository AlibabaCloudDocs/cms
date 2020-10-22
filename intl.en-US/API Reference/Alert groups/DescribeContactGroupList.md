# DescribeContactGroupList

Queries alert groups.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeContactGroupList&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeContactGroupList|The operation that you want to perform. Set the value to DescribeContactGroupList. |
|PageSize|Integer|No|1|The number of entries to return on each page. |
|PageNumber|Integer|No|10|The number of the page to return. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|ContactGroupList|Array|N/A|The information about alert groups that were queried. |
|ContactGroup|N/A|N/A|N/A|
|Contacts|List|Jimmy|The alert contacts in the alert group. |
|CreateTime|Long|1507070598000|The time when the alert group was created. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|Describe|String|PE alert group|The description of the alert group. |
|EnableSubscribed|Boolean|true|Indicates whether the alert group subscribes to weekly reports. The value true indicates that the alert group subscribes to weekly reports. The value false indicates that the alert group does not subscribe to weekly reports. |
|EnabledWeeklyReport|Boolean|true|Indicates whether the alert group can subscribe to weekly reports. The weekly report subscription feature is only available for Alibaba Cloud accounts with more than five Elastic Compute Service \(ECS\) instances. The value true indicates that the alert group can subscribe to weekly reports. The value false indicates that the alert group cannot subscribe to weekly reports. |
|Name|String|Contact1|The name of the alert group. |
|UpdateTime|Long|1589447759000|The time when the alert group was modified. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|ContactGroups|List|Alert group list|The names of alert groups. |
|Message|String|The Request is not authorization.|The returned message. |
|RequestId|String|916EE694-03C2-47B6-85EE-5054E3C168D3|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. The value true indicates a success. The value false indicates a failure. |
|Total|Integer|22|The total number of entries returned. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeContactGroupList
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeContactGroupList>
          <ContactGroupList>
                <ContactGroup>
                      <Describe></Describe>
                      <Contacts>
                            <Contact>Jimmy</Contact>
                      </Contacts>
                      <CreateTime>1507070598000</CreateTime>
                      <UpdateTime>1589447759000</UpdateTime>
                      <EnabledWeeklyReport>true</EnabledWeeklyReport>
                      <EnableSubscribed>false</EnableSubscribed>
                      <Name>Contact1</Name>
                </ContactGroup>
          </ContactGroupList>
          <ContactGroups>
                <ContactGroup>MyContactGroup1</ContactGroup>
          </ContactGroups>
          <RequestId>38516F54-0364-479E-AFCB-E856A4FFB67E</RequestId>
          <Total>1</Total>
          <Code>200</Code>
          <Success>true</Success>
</DescribeContactGroupList>
```

`JSON` format

```
{
    "ContactGroupList": {
        "ContactGroup": [
            {
                "Describe": "",
                "Contacts": {
                    "Contact": [
                        "Jimmy"
                    ]
                },
                "CreateTime": 1507070598000,
                "UpdateTime": 1589447759000,
                "EnabledWeeklyReport": true,
                "EnableSubscribed": false,
                "Name": "Contact1"
            }
        ]
    },
    "ContactGroups": {
        "ContactGroup": [
            "MyContactGroup1"
        ]
    },
    "RequestId": "38516F54-0364-479E-AFCB-E856A4FFB67E",
    "Total": 1,
    "Code": "200",
    "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

