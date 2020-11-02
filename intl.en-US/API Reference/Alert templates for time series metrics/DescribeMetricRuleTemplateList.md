# DescribeMetricRuleTemplateList

Queries alert templates.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeMetricRuleTemplateList&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeMetricRuleTemplateList|The operation that you want to perform. Set the value to DescribeMetricRuleTemplateList. |
|Name|String|No|ECS\_Template1|The name of the alert template. |
|Keyword|String|No|ECS|The name of the alert template. You can perform fuzzy search based on the template name. |
|TemplateId|Long|No|12345|The ID of the alert template. |
|PageNumber|Long|No|1|The number of the page to return. Default value: 1. |
|PageSize|Long|No|10|The number of entries to return on each page. |
|History|Boolean|No|false|Specifies whether to display the history of applying the alert templates to application groups. Default value: false. Valid values:

-   true
-   false |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|Integer|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |
|Message|String|The Request is not authorization.|The returned message. |
|Total|Long|11|The total number of the returned entries. |
|RequestId|String|1A1B405A-B877-4A27-9922-471F080E4985|The ID of the request. |
|Templates|Array of Template|N/A|The alert templates. |
|Template|N/A|N/A|N/A|
|ApplyHistories|Array of ApplyHistory|N/A|The application history of the alert template. |
|ApplyHistory|N/A|N/A|N/A|
|ApplyTime|Long|1543459583000|The time when the alert template was applied. |
|GroupId|Long|12345|The ID of the application group. |
|GroupName|String|ECS\_Group|The name of the application group. |
|Description|String|ECS CPU utilization|The description of the alert template. |
|GmtCreate|Long|1543302440000|The time when the alert template was created. |
|GmtModified|Long|1543302440000|The time when the alert template was modified. |
|Name|String|ECS\_Template1|The name of the alert template. |
|RestVersion|Long|0|The version of the alert template. Default value: 0. |
|TemplateId|Long|12345|The ID of the alert template. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeMetricRuleTemplateList
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeMetricRuleTemplateListResponse>
      <RequestId>03AE5FA9-8CB2-4B5B-8306-1BBBF012A1A7</RequestId>
      <Templates>
            <Template>
                  <RestVersion>0</RestVersion>
                  <Name>newtemplate_1</Name>
                  <Description>ECS CPU utilization</Description>
                  <GmtCreate>1543302440000</GmtCreate>
                  <GmtModified>1543302440000</GmtModified>
                  <TemplateId>32</TemplateId>
            </Template>
            <Template>
                  <RestVersion>0</RestVersion>
                  <Name>newtemplate_2</Name>
                  <Description></Description>
                  <GmtCreate>1543307344000</GmtCreate>
                  <GmtModified>1543307344000</GmtModified>
                  <TemplateId>42</TemplateId>
            </Template>
      </Templates>
      <Success>true</Success>
      <Code>200</Code>
      <Total>65</Total>
</DescribeMetricRuleTemplateListResponse>
```

`JSON` format

```
{
  "RequestId": "03AE5FA9-8CB2-4B5B-8306-1BBBF012A1A7",
  "Templates": {
    "Template": [
      {
        "RestVersion": 0,
        "Name": "newtemplate_1",
        "Description":"ECS CPU utilization",
        "GmtCreate": 1543302440000,
        "GmtModified": 1543302440000,
        "TemplateId": 32
      },
      {
        "RestVersion": 0,
        "Name": "newtemplate_2",
        "Description": "",
        "GmtCreate": 1543307344000,
        "GmtModified": 1543307344000,
        "TemplateId": 42
      }
    ]
  },
  "Success": true,
  "Code": 200,
  "Total": 65
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

