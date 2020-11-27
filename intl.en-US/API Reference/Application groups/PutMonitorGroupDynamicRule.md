# PutMonitorGroupDynamicRule

Creates or modifies an alert rule to dynamically add instances that meet the rule to an application group.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=PutMonitorGroupDynamicRule&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|PutMonitorGroupDynamicRule|The operation that you want to perform. Set the value to PutMonitorGroupDynamicRule. |
|GroupId|Long|Yes|123456|The ID of the application group. |
|GroupRules.N.Category|String|Yes|ecs|The cloud service to which the alert rule is applied. Valid values of N: 1 to 3. Valid values:

 -   ecs: Elastic Compute Service \(ECS\)
-   rds: ApsaraDB RDS
-   slb: Server Load Balancer \(SLB\) |
|GroupRules.N.FilterRelation|String|Yes|and|The logical operator used between conditional expressions in the alert rule. Valid values of N: 1 to 3. Valid values:

 -   and: The instances that meet all the conditional expressions are automatically added to the application group.
-   or: The instances that meet one of the conditional expressions are automatically added to the application group. |
|GroupRules.N.Filters.N.Function|String|Yes|contains|The method used to filter instances. Valid values of N: 1 to 3. Valid values:

 -   contains: containment relationship
-   startWith: prefix
-   endWith: suffix |
|GroupRules.N.Filters.N.Name|String|Yes|hostName|The name of the instance. Valid values of N: 1 to 3.

 The name of the field based on which instances are filtered. Set the value to hostName. |
|GroupRules.N.Filters.N.Value|String|Yes|nginx|The value to be matched with the value of the hostName field. Valid values of N: 1 to 3. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|3E73F1AB-D195-438A-BCA7-2F4355789C58|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |
|Code|Integer|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Message|String|The X.509 certificate or cms access key ID provided does not exist in our records.|The error message. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=PutMonitorGroupDynamicRule
&GroupId=123456
&GroupRules.1.Category=ecs
&GroupRules.1.FilterRelation=and
&GroupRules.1.Filters.1.Function=contains
&GroupRules.1.Filters.1.1ame=hostName
&GroupRules.1.Filters.1.Value=nginx
&<Common request parameters>
```

Sample success responses

`XML` format

```
<PutMonitorGroupDynamicRuleResponse>
	  <RequestId>3E73F1AB-D195-438A-BCA7-2F4355789C58</RequestId>
	  <Success>true</Success>
	  <Code>200</Code>
</PutMonitorGroupDynamicRuleResponse>
```

`JSON` format

```
{
  "RequestId": "3E73F1AB-D195-438A-BCA7-2F4355789C58",
  "Success": true,
  "Code": 200
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

