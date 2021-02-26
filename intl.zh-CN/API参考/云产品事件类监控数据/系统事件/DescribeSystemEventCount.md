# DescribeSystemEventCount

调用DescribeSystemEventCount接口查询各个产品指定时间段内事件的数量。

**说明：** 此API以产品为维度返回每个产品事件的数量。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeSystemEventCount&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeSystemEventCount|要执行的操作，取值：DescribeSystemEventCount。 |
|Product|String|否|oss|产品名称缩写。

 **说明：** 关于产品名称缩写的取值，请参见[DescribeSystemEventMetaList](~~114972~~)。 |
|EventType|String|否|Exception|事件类型。

 **说明：** 关于事件类型的取值，请参见[DescribeSystemEventMetaList](~~114972~~)。 |
|Name|String|否|BucketIngressBandwidth|事件名称。

 **说明：** 关于事件名称的取值，请参见[DescribeSystemEventMetaList](~~114972~~)。 |
|Level|String|否|WARN|事件级别。取值：

 -   CRITICAL：严重。
-   WARN：警告。
-   INFO：信息。 |
|Status|String|否|normal|事件状态。

 **说明：** 关于事件状态的取值，请参见[DescribeSystemEventMetaList](~~114972~~)。 |
|GroupId|String|否|12345|应用分组ID。 |
|SearchKeywords|String|否|cms|搜索事件内容包含的关键字。取值：

 -   如果您需要搜索事件的内容中包括a和b，则可以搜索`a and b`。
-   如果您需要搜索事件的内容中包括a或b，可以搜索`a or b`。 |
|StartTime|String|否|1552209685596|开始时间。

 格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |
|EndTime|String|否|1552220485596|结束时间。

 格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |

接入系统事件的产品，以及对应的事件名称、事件级别、状态等信息，请参考[DescribeSystemEventMetaList](~~114972~~)。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|60912C8D-B340-4253-ADE7-61ACDFD25CFC|请求ID。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Success|String|true|操作是否成功。true表示成功，false表示失败。 |
|SystemEventCounts|Array| |事件数量详情。 |
|SystemEventCount| | | |
|Content|String|xxxx|事件的具体内容。 |
|GroupId|String|123456|应用分组ID。 |
|InstanceName|String|instanceId1|实例名称。 |
|Level|String|WARN|事件级别。取值：

 -   CRITICAL：严重。
-   WARN：警告。
-   INFO：信息。 |
|Name|String|Agent\_Status\_Stopped|事件名称。 |
|Num|Long|2|发生事件的数量。 |
|Product|String|ECS|产品名称缩写。 |
|RegionId|String|cn-hangzhou|地域ID。 |
|ResourceId|String|xxxxx-1|资源ID。 |
|Status|String|normal|事件状态。 |
|Time|Long|1552199984000|事件发生时间。

 格式为Unix时间戳，即从1970年1月1日开始所经过的毫秒数。 |
|Message|String|success|返回信息。当请求成功时，返回成功信息；当请求失败时，返回失败原因。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeSystemEventCount
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeSystemEventCount>
		  <Message>success</Message>
		  <RequestId>60912C8D-B340-4253-ADE7-61ACDFD25CFC</RequestId>
		  <SystemEventCounts>
			    <SystemEventCount>
				      <Status>normal</Status>
				      <InstanceName>instanceId1</InstanceName>
				      <ResourceId>xxxxx-1</ResourceId>
				      <Content>xxxx</Content>
				      <Num>2</Num>
				      <Product>ECS</Product>
				      <Level>WARN</Level>
				      <Time>1552199984000</Time>
				      <RegionId>cn-hangzhou</RegionId>
				      <Name>Agent_Status_Stopped</Name>
				      <GroupId>123456</GroupId>
			    </SystemEventCount>
		  </SystemEventCounts>
		  <Code>200</Code>
		  <Success>true</Success>
</DescribeSystemEventCount>
```

`JSON` 格式

```
{
    "Message":"success",
    "RequestId":"60912C8D-B340-4253-ADE7-61ACDFD25CFC",
    "SystemEventCounts":{
        "SystemEventCount":[
            {
                "Status":"normal",
                "InstanceName":"instanceId1",
                "ResourceId":"xxxxx-1",
                "Content":"xxxx",
                "Num":"2",
                "Product":"ECS",
                "Level":"WARN",
                "Time":"1552199984000",
                "RegionId":"cn-hangzhou",
                "Name":"Agent_Status_Stopped",
                "GroupId":"123456"
            }]
    },
    "Code":"200",
    "Success":"true"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

