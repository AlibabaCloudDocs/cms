# QueryProjectMeta

查询云监控支持的时序类监控项产品列表。

## 调试

前往【[API Explorer](https://api.aliyun.com/#product=Cms&api=QueryProjectMeta)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|否|QueryProjectMeta|系统规定参数，取值：QueryProjectMeta |
|Labels|String|否|\[\{\\"name\\":\\"product\\",\\"value\\":\\"MongoDB\\"\]|根据标签过滤，格式为`[{"name":"标签名","value":"标签值"},{"name":"标签名","value":"标签值"}]`​。

 支持的标签名包括product、groupFlag。

 product 标签值为产品英文名称。

 groupFlag含义为该产品是否支持应用分组，标签值为true或false​ 。 |
|PageNumber|Integer|否|1|分页参数，默认1。 |
|PageSize|Integer|否|30|每页最大数量，默认30。 |

## 返回参数

|名称|类型|示例值|描述|
|--|--|---|--|
|ErrorCode|String|200|错误码200成功。 |
|ErrorMessage|String|Success|错误码消息。 |
|RequestId|String|D3DBF9F5-7C4D-4A67-B869-097C069C481D|用于跟踪。 |
|Resources| | |ProjectMeta列表。 |
|└Description|String|ApsaraDB for MongoDB|监控项的描述。 |
|└Labels|String|\[\{\\"name\\":\\"product\\",\\"value\\":\\"MongoDB\\"\]|`[{"name":"标签名","value":"标签值"},{"name":"标签名","value":"标签值"}]` 支持的标签名包括product、groupFlag。

 product 标签值为产品英文名称。

 groupFlag含义为该产品是否支持应用分组，标签值为true或false。 |
|└Project|String|acs\_mongodb|监控项的Project，用于查询监控数据。 |
|Success|Boolean|true|用于标识本次调用是否成功。 |

## 示例

请求示例

```

http(s)://[Endpoint]/?Action=QueryProjectMeta
&<公共请求参数>

```

正常返回示例

`XML` 格式

```
<?xml version="1.0" encoding="UTF-8" ?>
	<RequestId>D3DBF9F5-7C4D-4A67-B869-097C069C481D</RequestId>
	<ErrorCode>200</ErrorCode>
	<Success>true</Success>
	<Resources>
		<Resource>
			<Description>AnalyticDB</Description>
			<Labels>[{&quot;name&quot;:&quot;product&quot;,&quot;value&quot;:&quot;ADS&quot;},{&quot;name&quot;:&quot;groupFlag&quot;,&quot;value&quot;:&quot;true&quot;}]</Labels>
			<Project>acs_ads</Project>
		</Resource>
		<Resource>
			<Description>API Gateway</Description>
			<Labels>[{&quot;name&quot;:&quot;product&quot;,&quot;value&quot;:&quot;APIGateway&quot;},{&quot;name&quot;:&quot;groupFlag&quot;,&quot;value&quot;:&quot;true&quot;}]</Labels>
			<Project>acs_apigateway_dashboard</Project>
		</Resource>
		<Resource>
			<Description>Internet Shared Bandwidth</Description>
			<Labels>[{&quot;name&quot;:&quot;product&quot;,&quot;value&quot;:&quot;InternetSharedBandwidth&quot;},{&quot;name&quot;:&quot;groupFlag&quot;,&quot;value&quot;:&quot;true&quot;}]</Labels>
			<Project>acs_bandwidth_package</Project>
		</Resource>
		<Resource>
			<Description>CDN</Description>
			<Labels>[{&quot;name&quot;:&quot;product&quot;,&quot;value&quot;:&quot;CDN&quot;},{&quot;name&quot;:&quot;groupFlag&quot;,&quot;value&quot;:&quot;true&quot;}]</Labels>
			<Project>acs_cdn</Project>
		</Resource>
		<Resource>
			<Description>Cloud Enterprise Network</Description>
			<Labels>[{&quot;name&quot;:&quot;product&quot;,&quot;value&quot;:&quot;CEN&quot;},{&quot;name&quot;:&quot;groupFlag&quot;,&quot;value&quot;:&quot;false&quot;}]</Labels>
			<Project>acs_cen</Project>
		</Resource>
	</Resources>
	

```

`JSON` 格式

```
{
	"RequestId":"D3DBF9F5-7C4D-4A67-B869-097C069C481D",
	"Success":true,
	"ErrorCode":200,
	"Resources":{
		"Resource":[
			{
				"Description":"AnalyticDB",
				"Labels":"[{\"name\":\"product\",\"value\":\"ADS\"},{\"name\":\"groupFlag\",\"value\":\"true\"}]",
				"Project":"acs_ads"
			},
			{
				"Description":"API Gateway",
				"Labels":"[{\"name\":\"product\",\"value\":\"APIGateway\"},{\"name\":\"groupFlag\",\"value\":\"true\"}]",
				"Project":"acs_apigateway_dashboard"
			},
			{
				"Description":"Internet Shared Bandwidth",
				"Labels":"[{\"name\":\"product\",\"value\":\"InternetSharedBandwidth\"},{\"name\":\"groupFlag\",\"value\":\"true\"}]",
				"Project":"acs_bandwidth_package"
			},
			{
				"Description":"CDN",
				"Labels":"[{\"name\":\"product\",\"value\":\"CDN\"},{\"name\":\"groupFlag\",\"value\":\"true\"}]",
				"Project":"acs_cdn"
			},
			{
				"Description":"Cloud Enterprise Network",
				"Labels":"[{\"name\":\"product\",\"value\":\"CEN\"},{\"name\":\"groupFlag\",\"value\":\"false\"}]",
				"Project":"acs_cen"
			}
		]
	}
}
```

## 错误码

[查看本产品错误码](https://error-center.aliyun.com/status/product/Cms)

