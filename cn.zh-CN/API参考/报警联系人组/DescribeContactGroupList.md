# DescribeContactGroupList

调用DescribeContactGroupList接口查询报警联系组列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeContactGroupList&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeContactGroupList|要执行的操作，取值：DescribeContactGroupList。 |
|PageSize|Integer|否|1|每页显示记录条数。 |
|PageNumber|Integer|否|10|页码。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|ContactGroupList|Array of ContactGroup| |报警联系组详情列表。 |
|ContactGroup| | | |
|Contacts|List|Jimmy|报警联系人列表。 |
|CreateTime|Long|1507070598000|创建时间。Unix时间戳：从1970年1月1日开始所经过的毫秒数。 |
|Describe|String|PE报警组|报警联系组描述信息。 |
|EnableSubscribed|Boolean|true|是否开启周报订阅。

 -   true：开启。
-   false：关闭。 |
|EnabledWeeklyReport|Boolean|true|是否支持周报订阅。取值：

 -   true：支持。
-   false：不支持。

 **说明：** 目前仅ECS实例数量大于5的阿里云账号支持周报订阅。 |
|Name|String|Contact1|报警联系组的名称。 |
|UpdateTime|Long|1589447759000|修改时间。Unix时间戳：从1970年1月1日开始所经过的毫秒数。 |
|ContactGroups|List|\{ "ContactGroup": \[ "ECS\_Group", "Jim" \] \}|报警联系组列表。 |
|Message|String|The Request is not authorization.|错误信息。 |
|RequestId|String|916EE694-03C2-47B6-85EE-5054E3C168D3|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Total|Integer|22|总记录条数。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeContactGroupList
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeContactGroupListResponse>
		  <ContactGroupList>
			    <ContactGroup>
				      <Describe></Describe>
				      <Contacts>
					        <Contact>Jimmy</Contact>
				      </Contacts>
				      <CreateTime>1507070598000</CreateTime>
				      <UpdateTime>1589447759000</UpdateTime>
				      <EnabledWeeklyReport>true</EnabledWeeklyReport>
				      <EnableSubscribed>false</EnableSubscribed>
				      <Name>Contact1</Name>
			    </ContactGroup>
		  </ContactGroupList>
		  <ContactGroups>
			    <ContactGroup>MyContactGroup1</ContactGroup>
		  </ContactGroups>
		  <RequestId>38516F54-0364-479E-AFCB-E856A4FFB67E</RequestId>
		  <Total>1</Total>
		  <Code>200</Code>
		  <Success>true</Success>
</DescribeContactGroupListResponse>
```

`JSON` 格式

```
{
	"ContactGroupList": {
		"ContactGroup": [
			{
				"Describe": "",
				"Contacts": {
					"Contact": [
						"Jimmy"
					]
				},
				"CreateTime": 1507070598000,
				"UpdateTime": 1589447759000,
				"EnabledWeeklyReport": true,
				"EnableSubscribed": false,
				"Name": "Contact1"
			}
		]
	},
	"ContactGroups": {
		"ContactGroup": [
			"MyContactGroup1"
		]
	},
	"RequestId": "38516F54-0364-479E-AFCB-E856A4FFB67E",
	"Total": 1,
	"Code": "200",
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

