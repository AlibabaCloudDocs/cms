# DescribeSystemEventAttribute

调用DescribeSystemEventAttribute接口查询系统事件详情。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeSystemEventAttribute&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeSystemEventAttribute|要执行的操作，取值：DescribeSystemEventAttribute。 |
|Product|String|否|oss|产品名称缩写。

 **说明：** 关于产品名称缩写的取值，请参见[DescribeSystemEventMetaList](~~114972~~)。 |
|EventType|String|否|Exception|事件类型。

 **说明：** 关于事件类型的取值，请参见[DescribeSystemEventMetaList](~~114972~~)。 |
|Name|String|否|BucketIngressBandwidth|事件名称。

 **说明：** 关于事件名称的取值，请参见[DescribeSystemEventMetaList](~~114972~~)。 |
|Level|String|否|CRITICAL|事件级别。取值：

 -   CRITICAL：严重。
-   WARN：警告。
-   INFO：信息。 |
|Status|String|否|normal|事件状态。

 **说明：** 关于事件状态的取值，请参见[DescribeSystemEventMetaList](~~114972~~)。 |
|GroupId|String|否|12346|应用分组ID。 |
|SearchKeywords|String|否|cms|搜索事件内容包含的关键字。取值：

 -   如果您待搜索事件的内容中包括a和b，可以搜索`a and b`。
-   如果您待搜索事件的内容中包括a或b，可以搜索`a or b`。 |
|StartTime|String|否|1552199984949|开始时间。

 格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |
|EndTime|String|否|1552221584949|结束时间。

 格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |
|PageNumber|Integer|否|1|页码。默认值：1。 |
|PageSize|Integer|否|10|每页显示记录条数。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|60912C8D-B340-4253-ADE7-61ACDFD25CFC|请求ID。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Success|String|true|操作是否成功。true表示成功，false表示失败。 |
|SystemEvents|Array| |事件内容详情。 |
|SystemEvent| | | |
|Content|String|\[\{"product":"CloudMonitor","content":"\{\\"ipGroup\\":\\"112.126.XX.XX,10.163.XX.XX\\",\\"tianjimonVersion\\":\\"1.2.22\\"\}","groupId":"176,177,178,179,180,692,120812,1663836,96,2028302","time":"1552209568000","resourceId":"acs:ecs:cn-beijing:173651113438\*\*\*\*:instance/i-25k35\*\*\*\*","level":"CRITICAL","status":"stopped","instanceName":"cmssiteprobebj-6","name":"Agent\_Status\_Stopped","regionId":"cn-beijing"\}\]|事件内容详情。 |
|GroupId|String|12345|应用分组ID。 |
|InstanceName|String|instanceId1|实例名称。 |
|Level|String|WARN|事件级别。取值：

 -   CRITICAL：严重。
-   WARN：警告。
-   INFO：信息。 |
|Name|String|Agent\_Status\_Stopped|事件名称。 |
|Product|String|CloudMonitor|产品名称缩写。 |
|RegionId|String|cn-hangzhou|地域ID。 |
|ResourceId|String|xxxxx-1|资源ID。 |
|Status|String|normal|事件状态。 |
|Time|Long|1552199984000|事件发生的时间。

 格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |
|Message|String|success|返回信息。当操作成功时，返回`success`；当操作失败时，返回错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeSystemEventAttribute
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeSystemEventAttribute>
		  <SystemEvents>
			    <SystemEvent>
				      <Status>normal</Status>
				      <InstanceName>instanceId1</InstanceName>
				      <ResourceId>xxxxx-1</ResourceId>
				      <Content>[{\"product\":\"CloudMonitor\",\"content\":\"{\\\"ipGroup\\\":\\\"112.126.XX.XX,10.163.XX.XX\\\",\\\"tianjimonVersion\\\":\\\"1.2.22\\\"}\",\"groupId\":\"176,177,178,179,180,692,120812,1663836,96,2028302\",\"time\":\"1552209568000\",\"resourceId\":\"acs:ecs:cn-beijing:173651113438****:instance/i-25k35****\",\"level\":\"CRITICAL\",\"status\":\"stopped\",\"instanceName\":\"cmssiteprobebj-6\",\"name\":\"Agent_Status_Stopped\",\"regionId\":\"cn-beijing\"}]</Content>
				      <Product>CloudMonitor</Product>
				      <Level>WARN</Level>
				      <Time>1552199984000</Time>
				      <RegionId>cn-hangzhou</RegionId>
				      <Name>Agent_Status_Stopped</Name>
				      <GroupId>12345</GroupId>
			    </SystemEvent>
		  </SystemEvents>
		  <Message>success</Message>
		  <RequestId>60912C8D-B340-4253-ADE7-61ACDFD25CFC</RequestId>
		  <Code>200</Code>
		  <Success>true</Success>
</DescribeSystemEventAttribute>
```

`JSON` 格式

```
{
    "SystemEvents":{
        "SystemEvent":[
            {
                "Status":"normal",
                "InstanceName":"instanceId1",
                "ResourceId":"xxxxx-1",
                "Content":"[{\"product\":\"CloudMonitor\",\"content\":\"{\\\"ipGroup\\\":\\\"112.126.XX.XX,10.163.XX.XX\\\",\\\"tianjimonVersion\\\":\\\"1.2.22\\\"}\",\"groupId\":\"176,177,178,179,180,692,120812,1663836,96,2028302\",\"time\":\"1552209568000\",\"resourceId\":\"acs:ecs:cn-beijing:173651113438****:instance/i-25k35****\",\"level\":\"CRITICAL\",\"status\":\"stopped\",\"instanceName\":\"cmssiteprobebj-6\",\"name\":\"Agent_Status_Stopped\",\"regionId\":\"cn-beijing\"}]",
                "Product":"CloudMonitor",
                "Level":"WARN",
                "Time":"1552199984000",
                "RegionId":"cn-hangzhou",
                "Name":"Agent_Status_Stopped",
                "GroupId":"12345"
            }]
    },
    "Message":"success",
    "RequestId":"60912C8D-B340-4253-ADE7-61ACDFD25CFC",
    "Code":"200",
    "Success":"true"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

