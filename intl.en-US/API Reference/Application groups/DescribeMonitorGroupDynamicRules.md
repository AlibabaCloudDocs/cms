# DescribeMonitorGroupDynamicRules

Queries dynamic rules of an application group.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeMonitorGroupDynamicRules&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeMonitorGroupDynamicRules|The operation that you want to perform. Set the value to DescribeMonitorGroupDynamicRules. |
|GroupId|Long|Yes|123456|The ID of application group. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|Integer|200|The HTTP status code.

 **Note:** The value 200 indicates that the call was successful. |
|Message|String|The specified resource is not found.|The error message. |
|RequestId|String|2170B94A-1576-4D65-900E-2093037CDAF3|The ID of the request. |
|Resource|Array of Resource| |The resources that is associated with the application group. |
|Resource| | | |
|Category|String|ecs|The type of the cloud service to which the dynamic rule belongs. Valid values:

 -   ecs: Elastic Compute Service \(ECS\)
-   rds: ApsaraDB RDS
-   slb: Server Load Balancer \(SLB\) |
|FilterRelation|String|and|The filtering condition. Valid values:

 -   and: queries the instances that meet all alert rules
-   or: queries the instances that meet any alert rule |
|Filters|Array of Filter| |The dynamic rules of the application group. |
|Filter| | | |
|Function|String|contains|The method that is used to filter the instances. Valid values:

 -   contains: includes a specified element
-   startWith: specifies a prefix
-   endWith: specifies a suffix |
|Name|String|hostName|The name of the instance. |
|Value|String|1|The value of the dynamic rule. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |

## Examples

Sample request

```
http(s)://[Endpoint]/? Action=DescribeMonitorGroupDynamicRules
&GroupId=123456
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeMonitorGroupDynamicRulesResponse>
	  <RequestId>38D0A8B4-7231-4E3E-A39F-D8CE3E242AC7</RequestId>
	  <Resource>
		    <Resource>
			      <FilterRelation>and</FilterRelation>
			      <Filters>
				        <Filter>
					          <Function>contains</Function>
					          <Value>1</Value>
					          <Name>hostName</Name>
				        </Filter>
			      </Filters>
			      <Category>ecs</Category>
		    </Resource>
	  </Resource>
	  <Code>200</Code>
	  <Success>true</Success>
</DescribeMonitorGroupDynamicRulesResponse>
```

`JSON` format

```
{
	"RequestId": "38D0A8B4-7231-4E3E-A39F-D8CE3E242AC7",
	"Resource": {
		"Resource": [
			{
				"FilterRelation": "and",
				"Filters": {
					"Filter": [
						{
							"Function": "contains",
							"Value": "1",
							"Name": "hostName"
						}
					]
				},
				"Category": "ecs"
			}
		]
	},
	"Code": 200,
	"Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

