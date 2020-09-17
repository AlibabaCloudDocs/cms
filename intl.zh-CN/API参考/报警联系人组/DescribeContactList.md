# DescribeContactList

调用DescribeContactList接口查询报警联系人列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeContactList&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeContactList|要执行的操作，取值：DescribeContactList。 |
|PageSize|Integer|否|10|每页显示的记录条数。默认值：100。 |
|PageNumber|Integer|否|1|当前页码。默认值：1。 |
|ContactName|String|否|Alice|报警联系人姓名。 |
|ChanelType|String|否|Email|报警类型。

 目前只支持Email（电子邮件）和DingWebHook（钉钉机器人）。 |
|ChanelValue|String|否|testxx\*\*\*\*@aliyun.com|报警类型的值。

 当ChanelType设置为Email时，需要设置搜索的Email地址。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|06D5ECC2-B9BE-42A4-8FA3-1A610FB08B83|请求ID。 |
|Message|String|The Request is not authorization.|错误信息。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Contacts|Array of Contact| |报警联系方式。 |
|Contact| | | |
|Channels|Struct| |报警通知方式。 |
|AliIM|String|Alice|旺旺名称。 |
|DingWebHook|String|https://oapi.dingtalk.com/robot/send?access\_token=9bf44f8189597d07dfdd7a123455ffc112\*\*\*\*|钉钉机器人的地址。 |
|Mail|String|someone@example.com|邮件地址。 |
|SMS|String|1333333\*\*\*\*|手机号码。 |
|ChannelsState|Struct| |报警通道的状态。

 因为Email需要激活以后才能使用，所以当添加或修改报警通道时，如果处于未激活状态，则为PENDING；如果处于激活状态，则为OK。 |
|AliIM|String|OK|旺旺名称的状态正常。

 目前取值只支持：OK。OK表示旺旺名状态正常，对应的报警通道正常，可正常报警。 |
|DingWebHook|String|OK|钉钉机器人的状态正常。

 目前取值只支持：OK。OK表示钉钉机器人状态正常，对应的报警通道正常，可正常报警。 |
|Mail|String|PENDING|Email的状态。取值：

 -   PENDING：对应报警通道未激活，激活后才能使用。
-   OK：对应报警通道正常，可正常报警。 |
|SMS|String|OK|短信的状态。取值：

 -   PENDING：对应报警通道未激活，激活后才能使用。
-   OK：对应报警通道正常，可正常报警。 |
|ContactGroups|List|\{ "ContactGroup": \[ "ECS\_Group", "Jim" \] \}|报警联系组列表。 |
|CreateTime|Long|1552356159000|创建时间戳。 |
|Desc|String|我的联系方式|描述信息。 |
|Lang|String|zh-cn|报警的语言类型。取值：

 -   zh-cn：简体中文。
-   en：英文。 |
|Name|String|Alice|联系人姓名。 |
|UpdateTime|Long|1552356159000|更新时间戳。 |
|Total|Integer|15|总记录条数。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeContactList
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeContactListResponse>
		  <RequestId>A1267F27-942F-40EE-9254-57FE16E3C9AB</RequestId>
		  <Contacts>
			    <Contact>
				      <Desc>Contact Desc</Desc>
				      <ContactGroups>
					        <ContactGroup>ECS_Group</ContactGroup>
					        <ContactGroup>Jim</ContactGroup>
				      </ContactGroups>
				      <ChannelsState>
					        <SMS>PENDING</SMS>
					        <Mail>OK</Mail>
				      </ChannelsState>
				      <CreateTime>1583307692000</CreateTime>
				      <UpdateTime>1589441072000</UpdateTime>
				      <Channels>
					        <Mail>someone@example.com</Mail>
					        <SMS>155*******</SMS>
				      </Channels>
				      <Name>Alice</Name>
				      <Lang>zh-cn</Lang>
			    </Contact>
		  </Contacts>
		  <Total>25</Total>
		  <Code>200</Code>
		  <Success>true</Success>
</DescribeContactListResponse>
```

`JSON` 格式

```
{
	"RequestId": "A1267F27-942F-40EE-9254-57FE16E3C9AB",
	"Contacts": {
		"Contact": [
			{
				"Desc": "Contact Desc",
				"ContactGroups": {
					"ContactGroup": [
						"ECS_Group",
						"Jim"
					]
				},
                "ChannelsState":{
                    "SMS":"PENDING",
                    "Mail":"OK"
                },
				"CreateTime": 1583307692000,
				"UpdateTime": 1589441072000,
				"Channels": {
					"Mail": "someone@example.com",
					"SMS": "155*******"
				},
				"Name": "Alice",
				"Lang":"zh-cn"
			}
		]
	},
	"Total": 25,
	"Code": "200",
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

