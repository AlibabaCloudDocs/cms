# CreateSiteMonitor

调用CreateSiteMonitor接口创建站点监控的监控任务。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=CreateSiteMonitor&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateSiteMonitor|要执行的操作，取值：CreateSiteMonitor。 |
|Address|String|是|https://www.aliyun.com|监控任务的URL或IP地址。 |
|TaskName|String|是|HanZhou\_ECS1|监控任务名称。长度4~100个字符，取值可包含英文字母、数字、下划线（\_）和汉字。 |
|TaskType|String|是|HTTP|监控任务类型。目前站点监控任务的类型包括：HTTP（s）、PING、TCP、UDP、DNS、SMTP、POP3、FTP。 |
|Interval|String|否|1|监控频率。取值：1、5、15。单位：分钟。默认值：1。 |
|IspCities|String|否|\[\{"city":"546","isp":"465"\},\{"city":"572","isp":"465"\},\{"city":"738","isp":"465"\}\]|探针信息。格式为JSONArray，例如：`[{"city":"546","isp":"465"},{"city":"572","isp":"465"},{"city":"738","isp":"465"}]`，分别对应北京、杭州、青岛。

 **说明：** 您可以通过DescribeSiteMonitorISPCityList接口获取探测点信息，请参见[DescribeSiteMonitorISPCityList](~~115045~~)。如果该参数取值为空，则系统随机选择3个探测点。 |
|OptionsJson|String|否|\{"time\_out":5000\}|监控任务对应协议类型的高级扩展选项。不同监控任务的协议类型对应不同的扩展选项。 |
|AlertIds|String|否|SystemDefault\_acs\_ecs\_dashboard\_InternetOutRate\_Percent|报警规则ID。云监控中已存在的报警规则ID，可通过DescribeMetricRuleList接口查询，请参见[DescribeMetricRuleList](~~114941~~)。 |

TaskType中HTTP（s）、PING、TCP、UDP、DNS、SMTP、POP3和FTP的高级参数的设置方法如下表所示。

-   HTTP

|参数名

|类型

|描述 |
|-----|----|----|
|http\_method

|String

|HTTP请求方式，支持三种：GET、POST、HEAD。默认值：GET。 |
|header

|String

|换行符（\\n）分隔的自定义HTTP header。

 每行header格式需符合HTTP协议（使用英文冒号分隔的键值）。 |
|cookie

|String

|cookie和HTTP请求标准的写法一致。 |
|request\_content

|String

|请求内容。支持两种格式：JSON和表单。不提供时，请求中不含正文。 |
|response\_content

|String

|期望的回应内容。探测时会在HTTP服务器返回的前64个字节进行检查。 |
|match\_rule

|String

|0：回应中不含response\_content时，探测成功。

 1：回应中含response\_content时，探测成功。 |
|username

|String

|如果提供username，则会在HTTP请求中携带BasicAuth header。 |
|password

|String

|HTTP请求验证密码。 |
|time\_out

|int

|超时时间。单位：毫秒。默认值：5 。 |
|max\_redirect

|int

|大跳转次数。ECS探针默认5次，运营商探针默认2次。

 如果需要禁止跳转，则将该参数设置为：0。

 取值范围：0~50 。 |

-   PING

|参数名

|类型

|描述 |
|-----|----|----|
|failure\_rate

|int

|当PING失败率超过该参数时，探测失败，返回610（PingAllFail）或615（PingPartialFail）。

 默认值：0.1。 |
|ping\_num

|int

|PING次数，默认值：20。

 取值范围：1~100。 |

-   DNS

|参数名

|类型

|描述 |
|-----|----|----|
|dns\_server

|string

|DNS服务器地址，可以为域名或IP地址。 |
|dns\_type

|string

|DNS查询类型。取值：A、NS、CNAME、MX、TXT、ANY。 |
|expect\_value

|string

|英文空白符分隔的期望值列表。 |
|match\_rule

|string

|期望值列表与DNS列表的关系，当不满足指定关系时，探测失败。

 空字符串或IN\_DNS：期望值列表是DNS列表的子集。

 DNS\_IN：DNS列表是期望值列表的子集。

 EQUAL：DNS列表与期望值列表相等。

 ANY：DNS列表与期望值列表有交集（交集不为空）。 |

-   FTP

|参数名

|类型

|描述 |
|-----|----|----|
|port

|int

|FTP服务器端口号。如果不提供，则使用默认值。FTP默认值：21，FTPs默认值：990。 |
|username

|string

|FTP用户名。 如果未提供，则匿名登录。 |
|password

|string

|FTP密码。 |

-   POP3/SMTP

|参数名

|类型

|描述 |
|-----|----|----|
|port

|int

|POP3服务器端口号。POP3默认值：110，POP3s默认值：995。 |
|username

|string

|POP3/SMTP的用户名。 |
|password

|string

|POP3/SMTP的密码 。 |

-   TCP/UDP

|参数名

|类型

|描述 |
|-----|----|----|
|port

|int

|TCP/UDP服务器的端口。 |
|request\_content

|string

|请求内容。当request\_format为hex时，request\_content内容为十六进制紧凑格式。 |
|request\_format

|string

|当request\_format为其他值时，request\_content作为普通字符串发送给POP3/SMTP服务器。 |
|response\_content

|string

|回应内容。当POP3/SMTP服务器返回的内容中不含response\_content时，探测失败。

 当response\_format为hex时，response\_content中的内容为十六进制紧凑格式。

 当response\_content为其他值时，response\_content为普通字符串。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|AlertRule|String|\[\{"alarmActions":\["默认报警联系人组"\],"metricName":"Availability","expression":"$Availability<96"\}\]|创建或修改监控任务时设置报警规则，为一个JSONArray。

 格式：`[{"alarmActions":["xxx"],"metricName":"Availability","expression":"$Availability<96"}]`。

 -   alarmActions：对应报警联系组。
-   metricName：对应监控项。取值：
    -   Availability：可用探测点百分比。
    -   AvailableNumber：可用探测点数。 |
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|CreateResultList|Array of CreateResultList| |创建任务的返回结果。当创建任务成功时，会有返回结果。 |
|CreateResultList| | | |
|TaskId|String|df1f48e3-f814-491a-ad5f-\*\*\*\*|任务ID。 |
|TaskName|String|HanZhou\_ECS1|监控任务名称。 |
|Data|Struct| |创建监控任务结果详情。 |
|AttachAlertResult|Array of Contact| |关联已有报警规则的状态。 |
|Contact| | | |
|Code|String|200|关联已有报警规则的状态码。

 **说明：** 200表示成功。 |
|Message|String|successful|关联已存在报警规则的返回信息。 |
|RequestId|String|32565d-233-1b98-2231-892813f86c71|关联已存在报警规则的请求ID。 |
|RuleId|String|SystemDefault\_acs\_ecs\_dashboard\_InternetOutRate\_Percent|关联已存在报警规则ID。 |
|Success|String|true|关联已存在报警规则是否成功。取值：

 -   true：成功。
-   false：失败。 |
|Message|String|Successful|返回信息。 |
|RequestId|String|68192f5d-0d45-4b98-9724-892813f86c71|请求ID。 |
|Success|String|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=CreateSiteMonitor
&Address=https://www.aliyun.com
&TaskName=HanZhou_ECS1
&TaskType=HTTP
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<CreateSiteMonitorResponse>
	  <Message>successful</Message>
	  <RequestId>AB22040B-D13E-4693-9FE8-741615F5CBFC</RequestId>
	  <Data>
		    <AttachAlertResult>
			      <Contact>
				        <Message>successful</Message>
				        <RequestId>5dd33455-4f65-4b0c-9200-33d66f3f340b</RequestId>
				        <RuleId>SystemDefault_acs_ecs_dashboard_InternetOutRate_Percent</RuleId>
				        <Code>200</Code>
				        <Success>true</Success>
			      </Contact>
		    </AttachAlertResult>
	  </Data>
	  <Code>200</Code>
	  <CreateResultList>
		    <CreateResultList>
			      <TaskId>2c8dbdf9-a3ab-46a1-85a4-f094965ebef9</TaskId>
			      <TaskName>HanZhou_ECS1</TaskName>
		    </CreateResultList>
	  </CreateResultList>
	  <Success>true</Success>
</CreateSiteMonitorResponse>
```

`JSON` 格式

```
{
	"Message": "successful",
	"RequestId": "AB22040B-D13E-4693-9FE8-741615F5CBFC",
	"Data": {
		"AttachAlertResult": {
			"Contact": [
				{
					"Message": "successful",
					"RequestId": "5dd33455-4f65-4b0c-9200-33d66f3f340b",
					"RuleId": "SystemDefault_acs_ecs_dashboard_InternetOutRate_Percent",
					"Code": "200",
					"Success": true
				}
			]
		}
	},
	"Code": "200",
	"CreateResultList": {
		"CreateResultList": [
			{
				"TaskId": "2c8dbdf9-a3ab-46a1-85a4-f094965ebef9",
				"TaskName": "HanZhou_ECS1"
			}
		]
	},
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

