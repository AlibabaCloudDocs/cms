# CreateHostAvailability

调用CreateHostAvailability接口创建可用性监控任务。

本文将提供一个示例，在应用分组`123456`中创建探测类型`HTTP`的可用性监控任务`task1`，HTTP状态码`HttpStatus`通过邮件和钉钉机器人给您发送报警。返回结果显示可用性监控任务ID`12345`，说明创建成功。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=CreateHostAvailability&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateHostAvailability|要执行的操作，取值：CreateHostAvailability。 |
|AlertConfig.NotifyType|Integer|是|0|报警通知类型。取值：

 
 0：邮件+钉钉机器人。 |
|AlertConfigEscalationList.N.MetricName|String|是|HttpStatus|报警的监控项。N的取值范围：1~21。取值：

 -   HttpStatus：HTTP状态码。
-   HttpLatency：HTTP等待时间。
-   TelnetStatus：Telnet状态码。
-   TelnetLatency：Telnet等待时间。
-   PingLostRate：Ping丢包率。 |
|GroupId|Long|是|123456|应用分组ID。 |
|TaskName|String|是|task1|可用性监控任务名称。取值范围：4~100个字符，支持英文字母、数字、下划线（\_）和汉字。 |
|TaskType|String|是|HTTP|可用性监控任务的探测类型。取值：

 -   PING
-   TELNET
-   HTTP |
|TaskScope|String|否|GROUP|可用性监控任务的探测范围。取值：

 -   GROUP：表示当前应用分组内的所有ECS实例作为探测任务的探针。
-   GROUP\_SPEC\_INSTANCE：表示在应用分组内添加的实例作为探测任务的探针。设置该参数时，需要同时设置InstanceList（探测的ECS实例列表）。 |
|TaskOption.HttpURI|String|否|https://www.aliyun.com|HTTP探测类型的探测URI地址。 |
|TaskOption.TelnetOrPingHost|String|否|www.aliyun.com|探测的域名或地址。

 **说明：** 如果探测任务类型为PING或TELNET，则需要设置该参数。 |
|TaskOption.HttpResponseCharset|String|否|UTF-8|HTTP探测类型响应字符集。 |
|TaskOption.HttpPostContent|String|否|params1=paramsValue1|HTTP探测类型探测请求的Post内容。 |
|TaskOption.HttpResponseMatchContent|String|否|ok|匹配响应的内容。 |
|TaskOption.HttpMethod|String|否|GET|探测类型的方法。取值：

 -   GET
-   POST
-   HEAD

 **说明：** 如果任务的探测类型为HTTP，则需要设置该参数。 |
|TaskOption.HttpNegative|Boolean|否|true|匹配HTTP响应内容的报警规则。取值：

 -   true：如果HTTP响应内容包含设置的报警规则，则报警。
-   false：如果HTTP响应内容不包含设置的报警规则，则报警。

 **说明：** 如果任务的探测类型为HTTP，则该参数生效。 |
|TaskOption.HttpHeader|String|否|token:testTokenValue|HTTP请求的Header。格式为`参数名:参数`，多个参数之间用回车换行分隔，例如：

 ```

params1:value1
params2:value2

``` |
|AlertConfig.StartTime|Integer|否|0|报警生效的起始时间，取值范围：0~23。

 **说明：** 如果报警不在生效时间内，则超过阈值也不会发送报警通知。 |
|AlertConfig.EndTime|Integer|否|23|报警生效的结束时间，取值范围：0~23。

 **说明：** 如果报警不在生效时间内，则超过阈值也不会发送报警通知。 |
|AlertConfig.SilenceTime|Integer|否|86400|通道沉默时间。单位：秒，默认值：86400（1天）。 |
|AlertConfig.WebHook|String|否|https://www.aliyun.com/webhook.json|URL回调地址。 |
|AlertConfigEscalationList.N.Aggregate|String|否|Value|报警统计方法。N的取值范围：1~21。不同监控项的取值如下：

 -   HttpStatus：Value。
-   HttpLatency：Average。
-   TelnetStatus：Value。
-   TelnetLatency：Average。
-   PingLostRate：Average。

 **说明：** 状态码类的统计方法为原始值（Value），延时时间或丢包率的统计方法为平均值（Average）。 |
|AlertConfigEscalationList.N.Times|Integer|否|3|报警重试次数。N的取值范围：1~21。 |
|AlertConfigEscalationList.N.Operator|String|否|\>|报警规则比较符号。N的取值范围：1~21。取值：

 -   `>`
-   `>=`
-   `<`
-   `<=`
-   `=` |
|AlertConfigEscalationList.N.Value|String|否|90|报警阈值。N的取值范围：1~21。 |
|InstanceList.N|RepeatList|否|i-absdfkwl321\*\*\*\*|发起探测的ECS实例列表。N的取值范围：1~21。

 **说明：** 该参数为空，表示该应用分组下所有的实例。 |

关于公共请求参数的详情，请参见[公共参数](~~199331~~)。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|ACBDBB40-DFB6-4F4C-8957-51FFB233969C|请求ID。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|TaskId|Long|12345|可用性监控任务ID。 |
|Message|String|The specified resource is not found.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=CreateHostAvailability
&AlertConfig.1otifyType=0
&AlertConfigEscalationList.1.MetricName=HttpStatus
&GroupId=123456
&TaskName=task1
&TaskType=HTTP
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<CreateHostAvailabilityResponse>
	  <TaskId>12345</TaskId>
	  <RequestId>CDA78493-F10F-485F-98AD-B4C0B40AB225</RequestId>
	  <Code>200</Code>
	  <Success>true</Success>
</CreateHostAvailabilityResponse>
```

`JSON`格式

```
{
	"TaskId": "12345",
	"RequestId": "CDA78493-F10F-485F-98AD-B4C0B40AB225",
	"Code": 200,
	"Success": true
}
```

## 错误码

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|ResourceNotFound|The specified resource is not found.|未找到指定资源。|

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

