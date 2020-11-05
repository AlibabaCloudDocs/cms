# DescribeContactListByContactGroup

调用DescribeContactListByContactGroup接口查询报警联系组中的报警联系人列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeContactListByContactGroup&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeContactListByContactGroup|要执行的操作，取值：DescribeContactListByContactGroup。 |
|ContactGroupName|String|是|CloudMonitor|报警联系组名称。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Contacts|Array of Contact| |报警联系人。 |
|Contact| | | |
|Channels|Struct| |报警通道。 |
|AliIM|String|Alice|报警联系人的旺旺名称。

 **说明：** 该参数仅适用于中国站。 |
|DingWebHook|String|https://oapi.dingtalk.com/robot/send?access\_token=9bf44f8189597d07dfdd7a123455ffc112\*\*\*\*|报警联系人的钉钉机器人地址。 |
|Mail|String|alice@example.com|报警联系人的Email地址。 |
|SMS|String|1333333\*\*\*\*|报警联系人的手机号码。

 **说明：** 该参数仅适用于中国站。 |
|CreateTime|Long|1552314252000|创建报警联系人的时间戳。 |
|Desc|String|ECS|报警联系组的描述。 |
|Name|String|Alice|报警联系人的姓名。 |
|UpdateTime|Long|1552314252000|报警联系人的更新时间。 |
|Message|String|The group is not exists.|错误信息。 |
|RequestId|String|06D5ECC2-B9BE-42A4-8FA3-1A610FB08B83|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeContactListByContactGroup
&ContactGroupName=CloudMonitor
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeContactListByContactGroupResponse>
	  <RequestId>96B41DE5-6DC9-4FAF-A790-3D4AA17C1F09</RequestId>
	  <Contacts>
		    <Contact>
			      <Desc></Desc>
			      <CreateTime>1604024233000</CreateTime>
			      <UpdateTime>1604024233000</UpdateTime>
			      <Channels>
				        <SMS></SMS>
			      </Channels>
			      <Name>Alice</Name>
		    </Contact>
	  </Contacts>
	  <Code>200</Code>
	  <Success>true</Success>
</DescribeContactListByContactGroupResponse>
```

`JSON` 格式

```
{
  "RequestId": "96B41DE5-6DC9-4FAF-A790-3D4AA17C1F09",
  "Contacts": {
    "Contact": [
      {
        "Desc": "",
        "CreateTime": 1604024233000,
        "UpdateTime": 1604024233000,
        "Channels": {
          "SMS": ""
        },
        "Name": "Alice"
      }
    ]
  },
  "Code": "200",
  "Success": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

