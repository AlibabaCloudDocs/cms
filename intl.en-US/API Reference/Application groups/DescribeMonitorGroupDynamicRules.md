# DescribeMonitorGroupDynamicRules

Queries the rules that are used to dynamically add instances of services that meet the rules to an application group.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeMonitorGroupDynamicRules&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeMonitorGroupDynamicRules|The operation that you want to perform. Set the value to DescribeMonitorGroupDynamicRules. |
|GroupId|Long|Yes|123456|The ID of the application group. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|Integer|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Message|String|The Request is not authorization.|The returned message. |
|RequestId|String|2170B94A-1576-4D65-900E-2093037CDAF3|The ID of the request. |
|Resource|Array of Resource|N/A|The information about the queried matching rules. |
|Resource|N/A|N/A|N/A|
|Category|String|ecs|The service to which the instances to be added based on the matching rule belong. |
|FilterRelation|String|and|The logical operator used between conditional expressions. |
|Filters|Array of Filter|N/A|The conditional expression used to match instances. |
|Filter|N/A|N/A|N/A|
|Function|String|contains|The method that is used to match the instances. Valid values:

-   contains
-   startWith
-   endWith |
|Name|String|hostName|The name of the field to be matched with. |
|Value|String|aaa|The value to be matched with the value of the hostName field. |
|GroupId|Long|12345|The ID of the application group. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DescribeMonitorGroupDynamicRules
&GroupId=123456
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeMonitorGroupDynamicRulesResponse>
      <Resource>
            <Resource>
                  <Filters>
                        <Filter>
                              <Name>hostName</Name>
                              <Value>aaa</Value>
                              <Function>contains</Function>
                        </Filter>
                  </Filters>
                  <Category>ecs</Category>
                  <FilterRelation>and</FilterRelation>
            </Resource>
      </Resource>
      <RequestId>2170B94A-1576-4D65-900E-2093037CDAF3</RequestId>
      <Success>true</Success>
      <Code>200</Code>
</DescribeMonitorGroupDynamicRulesResponse>
```

`JSON` format

```
{
  "Resource": {
    "Resource": [
      {
        "Filters": {
          "Filter": [
            {
              "Name": "hostName",
              "Value": "aaa",
              "Function": "contains"
            }
          ]
        },
        "Category": "ecs",
        "FilterRelation": "and"
      }
    ]
  },
  "RequestId": "2170B94A-1576-4D65-900E-2093037CDAF3",
  "Success": true,
  "Code": 200
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

