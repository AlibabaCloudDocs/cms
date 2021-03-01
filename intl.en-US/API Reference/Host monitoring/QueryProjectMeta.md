# QueryProjectMeta

Queries information about monitored services in Cloud Monitor.

## Debugging

Alibaba Cloud provides [OpenAPI Explorer](https://api.aliyun.com/#product=Cms&api=QueryProjectMeta) to simplify API usage. You can use OpenAPI Explorer to search for APIs, call APIs, and dynamically generate SDK example code.

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|No|QueryProjectMeta|The operation that you want to perform. Set the value to QueryProjectMeta. |
|Labels|String|No|\[\{\\"name\\":\\"product\\",\\"value\\":\\"MongoDB\\"\]|The tags of the service. You must specify the tags in the following format: `[{"name":"Tag key","value":"Tag value"},{"name":"Tag key","value":"Tag value"}]`.

The following tag keys are supported:

product: the cloud service. Set the value to a service name.

groupFlag: specifies whether the service supports application grouping. Set the value to true or false. |
|PageNumber|Integer|No|1|The number of the page to return. Default value: 1. |
|PageSize|Integer|No|30|The number of entries to return on each page. Default value: 30. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|ErrorCode|String|200|The HTTP status code. The status code 200 indicates that the call was successful. |
|ErrorMessage|String|Success|The returned message. |
|RequestId|String|D3DBF9F5-7C4D-4A67-B869-097C069C481D|The ID of the request. |
|Resources| | |The information about monitored services. |
|└Description|String|ApsaraDB for MongoDB|The description of the service. |
|└Labels|String|\[\{\\"name\\":\\"product\\",\\"value\\":\\"MongoDB\\"\]|`[{"name":"Tag key","value":"Tag value"},{"name":"Tag key","value":"Tag value"}]`The tags of the service. The following tag keys are supported:

product: the cloud service. The value of this tag is a service name.

groupFlag: indicates whether the service supports application grouping. The value of this tag is true or false. |
|└Project|String|acs\_mongodb|The project to which the service belongs. It is used to query monitoring data. |
|Success|Boolean|true|Indicates whether the call was successful. |

## Examples

Sample requests

```

http(s)://[Endpoint]/?Action=QueryProjectMeta
&<Common request parameters>

```

Sample success responses

`XML` format

```
<? xml version="1.0" encoding="UTF-8" ? >
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

`JSON` format

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

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.aliyun.com/status/product/Cms).

