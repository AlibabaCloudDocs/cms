# DescribeHostAvailabilityList

Queries availability monitoring tasks.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeHostAvailabilityList&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeHostAvailabilityList|The operation that you want to perform. Set the value to DescribeHostAvailabilityList. |
|Id|Long|No|123456|The ID of the availability monitoring task. |
|TaskName|String|No|My availability monitoring task|The name of the availability monitoring task. |
|PageNumber|Integer|No|1|The number of the page to return. |
|PageSize|Integer|No|10|The number of entries to return on each page. |
|GroupId|Long|No|12345|The ID of the application group. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|CE26797C-1094-47E6-B651-73AA888F5873|The ID of the request. |
|Code|String|200|The HTTP status code.

 **Note:** The value 200 indicates that the call was successful. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |
|TaskList|Array of NodeTaskConfig| |The list of availability monitoring tasks. |
|NodeTaskConfig| | | |
|AlertConfig|Struct| |The configurations of the alert rule. |
|EndTime|Integer|23|The end of the time period during which the alert rule is effective. Valid values: 0 to 23. |
|EscalationList|Array of escalationList| |The trigger condition of the alert rule. |
|escalationList| | | |
|Aggregate|String|Value|The method used to calculate metric values that trigger alerts. The following points describe the correspondence between metrics and calculation methods:

 -   HttpStatus: Value
-   HttpLatency: Average
-   TelnetStatus: Value
-   TelnetLatency: Average
-   PingLostRate: Average |
|MetricName|String|HttpStatus|The monitoring metrics. Valid values:

 -   HttpStatus: HTTP status code
-   HttpLatency: HTTP response time
-   TelnetStatus: TELNET status code
-   TelnetLatency: TELNET response time
-   PingLostRate: PING packet loss rate |
|Operator|String|\>|The comparison operator that is used in the alert rule. Valid values:

 -   `>`
-   `>=`
-   `<`
-   `<=`
-   `=` |
|Times|String|2|The consecutive times for which the metric value is measured before an alert is triggered. |
|Value|String|99|The alert threshold. |
|NotifyType|Integer|1|The alert notification method.

 
 Set the value to 0. The value 0 indicates that alert notifications are sent by using emails and DingTalk chatbots. |
|SilenceTime|Integer|86400|The mute period during which notifications are not repeatedly sent for an alert. Unit: seconds. Default value: 86400. The default value indicates one day. |
|StartTime|Integer|0|The beginning of the time period during which the alert rule is effective. Valid values: 0 to 23. |
|WebHook|String|https://www.aliyun.com|The callback URL. |
|Disabled|Boolean|false|Specifies whether to disable the availability monitoring task. Valid values:

 -   true
-   false |
|GroupId|Long|12345|The ID of the application group. |
|GroupName|String|Application group name|The name of the application group. |
|Id|Long|123|The ID of the availability monitoring task. |
|Instances|List|i-abcdefgh12\*\*\*\*|The ECS instances to be monitored. |
|TaskName|String|task1|The name of the availability monitoring task. |
|TaskOption|Struct| |The options of the availability monitoring task. |
|HttpKeyword|String|ok|The response to the HTTP request. |
|HttpMethod|String|GET|The HTTP request method. Valid values:

 -   GET
-   POST
-   HEAD |
|HttpNegative|Boolean|true|The method to trigger an alert. The alert can be triggered based on whether the specified alert rule is included in the response body. Valid values:

 -   true: If the HTTP response body includes the alert rule, an alert is triggered.
-   false: If the HTTP response does not include the alert rule, an alert is triggered. |
|HttpPostContent|String|params1=paramsValue1|The post body in the HTTP request. |
|HttpResponseCharset|String|UTF-8|The character set that is used in the HTTP response. |
|HttpURI|String|https://www.aliyun.com|The URI that is monitored. This parameter is returned if the TaskType parameter is set to HTTP. |
|TelnetOrPingHost|String|ssh.aliyun.com|The domain name or IP address to be monitored. |
|TaskScope|String|GROUP|The monitoring range of the availability monitoring task. Valid values:

 -   GROUP: monitors all Elastic Compute Service \(ECS\) instances in the application group
-   GROUP\_SPEC\_INSTANCE: monitors specific ECS instances in the application group The TaskScope and InstanceList.N parameters must be used in pairs. |
|TaskType|String|HTTP|The type of the task. Valid values:

 -   PING
-   TELNET
-   HTTP |
|Total|Integer|12|The total number of returned entries. |
|Message|String|The Request is not authorization.|The error message. |

## Examples

Sample request

```
http(s)://[Endpoint]/? Action=DescribeHostAvailabilityList
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeHostAvailabilityListResponse>
	  <RequestId>4A288E86-45C3-4858-9DB0-6D85B10BD92A</RequestId>
	  <Total>1</Total>
	  <TaskList>
		    <NodeTaskConfig>
			      <GroupName>Group_ECS</GroupName>
			      <TaskOption>
				        <HttpURI>https://aliyun.com</HttpURI>
				        <HttpMethod>HEAD</HttpMethod>
			      </TaskOption>
			      <AlertConfig>
				        <NotifyType>1</NotifyType>
				        <SilenceTime>86400</SilenceTime>
				        <EndTime>24</EndTime>
				        <StartTime>0</StartTime>
				        <EscalationList>
					          <escalationList>
						            <Operator>&gt;</Operator>
						            <MetricName>HttpStatus</MetricName>
						            <Times>3</Times>
						            <Value>400</Value>
						            <Aggregate>Value</Aggregate>
					          </escalationList>
					          <escalationList>
						            <Operator>&gt;</Operator>
						            <MetricName>HttpLatency</MetricName>
						            <Times>3</Times>
						            <Value>500</Value>
						            <Aggregate>Average</Aggregate>
					          </escalationList>
				        </EscalationList>
			      </AlertConfig>
			      <TaskName>ecs_instance</TaskName>
			      <TaskScope>GROUP</TaskScope>
			      <TaskType>HTTP</TaskType>
			      <Id>90****</Id>
			      <Disabled>false</Disabled>
			      <GroupId>7671****</GroupId>
		    </NodeTaskConfig>
	  </TaskList>
	  <Code>200</Code>
	  <Success>true</Success>
</DescribeHostAvailabilityListResponse>
```

`JSON` format

```
{
	"RequestId": "4A288E86-45C3-4858-9DB0-6D85B10BD92A",
	"Total": 1,
	"TaskList": {
		"NodeTaskConfig": [
			{
				"GroupName": "Group_ECS",
				"TaskOption": {
					"HttpURI": "https://aliyun.com",
					"HttpMethod": "HEAD"
				},
				"AlertConfig": {
					"NotifyType": 1,
					"SilenceTime": 86400,
					"EndTime": 24,
					"StartTime": 0,
					"EscalationList": {
						"escalationList": [
							{
								"Operator": ">",
								"MetricName": "HttpStatus",
								"Times": 3,
								"Value": "400",
								"Aggregate": "Value"
							},
							{
								"Operator": ">",
								"MetricName": "HttpLatency",
								"Times": 3,
								"Value": "500",
								"Aggregate": "Average"
							}
						]
					}
				},
				"TaskName": "ecs_instance",
				"TaskScope": "GROUP",
				"TaskType": "HTTP",
				"Id": "90****",
				"Disabled": false,
				"GroupId": "7671****"
			}
		]
	},
	"Code": 200,
	"Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

