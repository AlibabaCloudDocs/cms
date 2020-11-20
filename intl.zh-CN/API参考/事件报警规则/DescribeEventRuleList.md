# DescribeEventRuleList

调用DescribeEventRuleList接口查询事件报警规则列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeEventRuleList&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeEventRuleList|要执行的操作，取值：DescribeEventRuleList。 |
|NamePrefix|String|否|test|事件报警规则前缀。 |
|PageNumber|String|否|1|当前页码。默认值：1。 |
|PageSize|String|否|10|每页显示记录条数。 |
|GroupId|String|否|12345|应用分组ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|EventRules|Array of EventRule| |事件报警规则。 |
|EventRule| | | |
|Description|String|Default group event rule.|事件报警规则的描述信息。 |
|EventPattern|Array of EventPattern| |事件报警规则的模式。 |
|EventPattern| | | |
|EventTypeList|List|\*|事件报警规则的类型。不限制类型用\*表示。 |
|LevelList|List|CRITICAL|事件的等级。取值：

 -   CRITICAL：严重。
-   WARN：警告。
-   INFO：信息。 |
|NameList|List|\["Agent\_Status\_Stopped"\]|事件名称列表。 |
|Product|String|CloudMonitor|云服务名称的缩写。 |
|EventType|String|SYSTEM|事件报警类型。取值：

 -   SYSTEM：系统事件。
-   CUSTOM：自定义事件。 |
|GroupId|String|7378\*\*\*\*|应用分组ID。 |
|Name|String|test\_DefaultEventRule\_7378\*\*\*\*|事件报警规则名称。 |
|State|String|ENABLED|事件报警规则状态。取值：

 -   ENABLED：启用。
-   DISABLED：禁用。 |
|Message|String|User not authorized to operate on the specified resource.|错误信息。 |
|RequestId|String|D0E6D82B-16B5-422A-8136-EE5BDC01E415|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Total|Integer|21|总记录条数。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeEventRuleList
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeEventRuleListResponse>
	  <RequestId>C8308712-6E7A-4FA0-82AC-80D018DAD168</RequestId>
	  <Total>3</Total>
	  <EventRules>
		    <EventRule>
			      <EventPattern>
				        <NameList>
					          <NameList>*</NameList>
				        </NameList>
				        <LevelList>
					          <LevelList>CRITICAL</LevelList>
				        </LevelList>
				        <EventTypeList>
					          <EventTypeList>*</EventTypeList>
				        </EventTypeList>
				        <Product>CloudMonitor</Product>
			      </EventPattern>
			      <EventType>SYSTEM</EventType>
			      <State>ENABLED</State>
			      <Name>test123</Name>
		    </EventRule>
		    <EventRule>
			      <EventPattern>
				        <NameList>
					          <NameList>*</NameList>
				        </NameList>
				        <LevelList>
					          <LevelList>CRITICAL</LevelList>
					          <LevelList>WARN</LevelList>
				        </LevelList>
				        <Product>*</Product>
			      </EventPattern>
			      <Description>Default group event rule.</Description>
			      <EventType>SYSTEM</EventType>
			      <State>ENABLED</State>
			      <Name>test_DefaultEventRule_7378****</Name>
			      <GroupId>7378****</GroupId>
		    </EventRule>
		    <EventRule>
			      <EventPattern>
				        <NameList>
					          <NameList>*</NameList>
				        </NameList>
				        <LevelList>
					          <LevelList>CRITICAL</LevelList>
					          <LevelList>WARN</LevelList>
				        </LevelList>
				        <Product>*</Product>
			      </EventPattern>
			      <Description>Default group event rule.</Description>
			      <EventType>SYSTEM</EventType>
			      <State>ENABLED</State>
			      <Name>test123_DefaultEventRule_7301****</Name>
			      <GroupId>7301****</GroupId>
		    </EventRule>
	  </EventRules>
	  <Code>200</Code>
	  <Success>true</Success>
</DescribeEventRuleListResponse>
```

`JSON` 格式

```
{
	"RequestId": "C8308712-6E7A-4FA0-82AC-80D018DAD168",
	"Total": 3,
	"EventRules": {
		"EventRule": [
			{
				"EventPattern": {
					"NameList": {
						"NameList": [
							"*"
						]
					},
					"LevelList": {
						"LevelList": [
							"CRITICAL"
						]
					},
					"EventTypeList": {
						"EventTypeList": [
							"*"
						]
					},
					"Product": "CloudMonitor"
				},
				"EventType": "SYSTEM",
				"State": "ENABLED",
				"Name": "test123"
			},
			{
				"EventPattern": {
					"NameList": {
						"NameList": [
							"*"
						]
					},
					"LevelList": {
						"LevelList": [
							"CRITICAL",
							"WARN"
						]
					},
					"Product": "*"
				},
				"Description": "Default group event rule.",
				"EventType": "SYSTEM",
				"State": "ENABLED",
				"Name": "test_DefaultEventRule_7378****",
				"GroupId": "7378****"
			},
			{
				"EventPattern": {
					"NameList": {
						"NameList": [
							"*"
						]
					},
					"LevelList": {
						"LevelList": [
							"CRITICAL",
							"WARN"
						]
					},
					"Product": "*"
				},
				"Description": "Default group event rule.",
				"EventType": "SYSTEM",
				"State": "ENABLED",
				"Name": "test123_DefaultEventRule_7301****",
				"GroupId": "7301****"
			}
		]
	},
	"Code": "200",
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

