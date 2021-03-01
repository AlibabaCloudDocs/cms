# PutExporterOutput

调用PutExporterOutput接口创建或者修改一个监控数据导出配置。

**说明：** 目前仅支持日志服务（SLS），后续将支持导出更多的产品。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=PutExporterOutput&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|PutExporterOutput|要执行的操作，取值：PutExporterOutput。 |
|ConfigJson|String|是|\{ "endpoint": "http://cn-qingdao-share.log.aliyuncs.com", "project": "exporter", "logstore": "exporter","ak": "LTAIp\*\*\*\*\*\*\*", "userId": "17754\*\*\*\*\*\*\*\*", "as": "TxHwuJ8yAb3AU\*\*\*\*\*\*"\}|数据导出的配置。是一个JSONObject字符串。必须要包含如下字段：

 -   endpoint：日志服务（SLS）数据对应的域名。
-   project：项目。
-   logstore：日志库。
-   ak：AccessKey ID。
-   as：AccessKey Secret。 |
|DestName|String|是|exporterConfig|配置的名称。 |
|DestType|String|是|sls|导出的产品。 |
|Desc|String|否|CPU指标导出|配置的描述信息。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The Request is not authorization.|返回信息。 |
|RequestId|String|6A5F022D-AC7C-460E-94AE-B9E75083D027|请求ID。 |
|Success|Boolean|true|操作是否成功。true表示成功，false表示失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=PutExporterOutput
&ConfigJson={ "endpoint": "http://cn-qingdao-share.log.aliyuncs.com", "project": "exporter", "logstore": "exporter","ak": "LTAIp*******", "userId": "17754********", "as": "TxHwuJ8yAb3AU******"}
&DestName=exporterConfig
&DestType=sls
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<PutExporterOutput>
		  <RequestId>E5DC60DD-2FDE-488F-942C-424FA3E18BF8</RequestId>
		  <Code>200</Code>
		  <Success>true</Success>
</PutExporterOutput>
```

`JSON` 格式

```
{
	"RequestId": "E5DC60DD-2FDE-488F-942C-424FA3E18BF8",
	"Code": "200",
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

