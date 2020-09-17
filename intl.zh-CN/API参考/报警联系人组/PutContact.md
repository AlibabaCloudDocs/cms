# PutContact

调用PutContact接口创建或修改报警联系人信息。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=PutContact&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|PutContact|要执行的操作，取值：PutContact。 |
|ContactName|String|是|Alice|报警联系人姓名。 |
|Describe|String|是|ECS\_Instance|报警联系人描述详情。 |
|Channels.SMS|String|否|1333333\*\*\*\*|手机号码。手机号码会收到一个激活链接， 激活之后您才会被加入到联系人中。

 邮箱和钉钉机器人最少添加一种联系方式。 |
|Channels.Mail|String|否|test@aliyun.com|Email地址。Email会收到一个激活链接， 激活之后您才会被加入到联系人中。

 邮箱和钉钉机器人最少添加一种联系方式。 |
|Channels.DingWebHook|String|否|https://oapi.dingtalk.com/robot/send?access\_token=7d49515e8ebf21106a80a9cc4bb3d247771305d52fb15d6201234565\*\*\*\*|钉钉机器人。

 邮箱和钉钉机器人最少添加一种联系方式。 |
|Channels.AliIM|String|否|Jim|旺旺联系人。

 邮箱和钉钉机器人最少添加一种联系方式。 |
|Lang|String|否|zh-cn|报警的语言类型。取值：

 -   zh-cn：简体中文。
-   en：英文。

 **说明：** 如果不设置该参数，则自动按照账号归属地域自动识别。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The Request is not authorization.|错误信息。 |
|RequestId|String|181C406E-9DE4-484C-9C61-37AE9A1A12EE|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=PutContact
&ContactName=Alice
&Describe=ECS_Instance
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<PutContactResponse>
      <Code>200</Code>
      <RequestId>181C406E-9DE4-484C-9C61-37AE9A1A12EE</RequestId>
      <Success>true</Success>
</PutContactResponse>
```

`JSON` 格式

```
{
  "RequestId": "F7FA82F0-8627-441B-9B2B-8663617F36B9",
  "Success": true,
  "Code": "200"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

