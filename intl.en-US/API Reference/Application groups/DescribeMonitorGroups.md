# DescribeMonitorGroups

Queries application groups.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeMonitorGroups&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeMonitorGroups|The operation that you want to perform. Set the value to DescribeMonitorGroups. |
|GroupName|String|No|demo|The name of the application group. |
|Keyword|String|No|test|The keyword to be matched. |
|PageSize|Integer|No|10|The number of entries to return on each page. Default value: 10. |
|PageNumber|Integer|No|1|The number of the page to return. Default value: 1. |
|InstanceId|String|No|i-abcdefgh12\*\*\*\*|The ID of the instance that belongs to the specified application group. You can search for the application group to which the specified instance belongs. |
|SelectContactGroups|Boolean|No|true|Specifies whether to include the alert groups that receive alert notifications for the application group in the returned data. Valid values:

-   true
-   false |
|IncludeTemplateHistory|Boolean|No|true|Specifies whether to include the alert templates that have been applied to the application group in the returned data. Valid values:

-   true
-   false |
|Tag.N.Key|String|No|testKey1|The key of the tag attached to the application group. Valid values of N: 1 to 5. |
|Tag.N.Value|String|No|testValue1|The value of the tag attached to the application group. Valid values of N: 1 to 5. |
|Type|String|No|custom|The type of the application group. Valid values:

-   custom: a user-created application group
-   ehpc\_cluster: an application group synchronized from an E-HPC cluster
-   kubernetes: an application group synchronized from a Kubernetes cluster |
|DynamicTagRuleId|String|No|055995c1-4625-4dc0-8338-\*\*\*\*\*\*376950|The ID of the tag rule. |
|GroupId|String|No|123\*\*\*\*|The ID of the application group. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|31BC7201-00F2-47B2-B7B9-6A173076ACE8|The ID of the request. |
|Message|String|The Request is not authorization.|The returned message. |
|PageNumber|Integer|1|The number of the returned page. |
|PageSize|Integer|10|The number of entries returned on each page. |
|Code|Integer|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Resources|Array of Resource|N/A|The information about the queried application group. |
|Resource|N/A|N/A|N/A|
|BindUrl|String|http://aliyun.com|The URL of the Kubernetes cluster from which the application group is synchronized. |
|ContactGroups|Array of ContactGroup|N/A|The alert groups that receive alert notifications for the application group. |
|ContactGroup|N/A|N/A|N/A|
|Name|String|ECS\_Group|The name of the alert group. |
|DynamicTagRuleId|String|055995c1-4625-4dc0-8338-\*\*\*\*\*\*376950|The ID of the tag rule. |
|GmtCreate|Long|1489043796000|The time when the application group was created.

This value is a UNIX timestamp that represents the number of milliseconds that have elapsed since January 1, 1970, 00:00:00 UTC. |
|GmtModified|Long|1525183537000|The time when the application group was modified.

This value is a UNIX timestamp that represents the number of milliseconds that have elapsed since January 1, 1970, 00:00:00 UTC. |
|GroupFounderTagKey|String|portalGroup|The key of the tag used to create the application group.

**Note:** If the application group is created based on a tag rule, the value of this parameter indicates the key of the tag used to create the application group. |
|GroupFounderTagValue|String|portalJP|The value of the tag used to create the application group.

**Note:** If the application group is created based on a tag rule, the value of this parameter indicates the value of the tag used to create the application group. |
|GroupId|Long|12345|The ID of the application group. |
|GroupName|String|demo|The name of the application group. |
|ServiceId|String|49\*\*\*\*|The ID of the Alibaba Cloud service. |
|Tags|Array of Tag|N/A|The tags attached to the application group. |
|Tag|N/A|N/A|N/A|
|Key|String|tagKey1|The key of the tag attached to the application group. |
|Value|String|tagValue1|The value of the tag attached to the application group. |
|TemplateIds|List|123|The alert templates applied to the application group.

**Note:** If the IncludeTemplateHistory parameter is set to true in the request, the returned results contain the alert templates. |
|Type|String|custom|The type of the application group. Valid values:

-   custom: a user-created application group
-   ehpc\_cluster: an application group synchronized from an E-HPC cluster
-   kubernetes: an application group synchronized from a Kubernetes cluster |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |
|Total|Integer|10|The total number of the returned entries. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeMonitorGroups
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeMonitorGroupsResponse>
          <PageNumber>1</PageNumber>
          <PageSize>10</PageSize>
          <RequestId>31BC7201-00F2-47B2-B7B9-6A173076ACE8</RequestId>
          <Success>true</Success>
          <Code>200</Code>
          <Total>1</Total>
          <Resources>
                <Resource>
                      <GroupName>demo</GroupName>
                      <Type>custom</Type>
                      <ContactGroups>
                            <ContactGroup>
                                  <Name>ECS_Group</Name>
                            </ContactGroup>
                      </ContactGroups>
                      <ServiceId>49****</ServiceId>
                      <GmtCreate>1489043796000</GmtCreate>
                      <GmtModified>1525183537000</GmtModified>
                      <GroupId>123****</GroupId>
                      <Tags>
                            <Tag>
                                  <Value>tagValue1</Value>
                                  <Key>tagKey1</Key>
                            </Tag>
                      </Tags>
                      <TemplateIds></TemplateIds>
                </Resource>
          </Resources>
</DescribeMonitorGroupsResponse>
```

`JSON` format

```
{
    "PageNumber": 1,
    "PageSize": 10,
    "RequestId": "31BC7201-00F2-47B2-B7B9-6A173076ACE8",
    "Success": true,
    "Code": 200,
    "Total": 1,
    "Resources": {
        "Resource": [
            {
                "GroupName": "demo",
                "Type": "custom",
                "ContactGroups": {
                    "ContactGroup": [
                        {
                            "Name": "ECS_Group"
                        }
                    ]
                },
                "ServiceId": "49****",
                "GmtCreate": "1489043796000",
                "GmtModified": "1525183537000",
                "GroupId": "123****",
                "Tags": {
                    "Tag": [
                        {
                            "Value": "tagValue1",
                            "Key": "tagKey1"
                        }
                    ]
                },
                "TemplateIds": {
                    "TemplateId": []
                }
            }
        ]
    }
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

