# DescribeExporterOutputList

调用DescribeExporterOutputList接口查询监控数据导出列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeExporterOutputList&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeExporterOutputList|要执行的操作，取值：**DescribeExporterOutputList**。 |
|PageNumber|Integer|否|1|分页码，默认为1。 |
|PageSize|Integer|否|10|每页显示记录条数，默认为10。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 状态码为200表示成功，其余取值表示失败。 |
|Datapoints|Array| |输出的配置列表。 |
|Datapoint| | | |
|ConfigJson|Struct| |监控输出配置。 |
|ak|String|LTAIpY33\*\*\*\*\*\*\*\*|AccessKeyId。 |
|as|String|TxHwuJ8yAb3AULcnny\*\*\*\*\*\*|AccessKeySecret。 |
|endpoint|String|http://cn-qingdao-share.log.aliyuncs.com|SLS的数据对应的域名。 |
|logstore|String|monitorlogstore|日志库。 |
|project|String|exporter|SLS项目。 |
|CreateTime|Long|1584016495498|创建的uninx时间戳。 |
|DestName|String|exporterOut|配置的名称。 |
|DestType|String|SLS|数据导出的类型。

 **说明：** 目前仅支持SLS，后续将支持导出更多的产品。 |
|Message|String|sucess|错误信息。 |
|PageNumber|Integer|1|当前页码。 |
|RequestId|String|0E657631-CD6C-4C24-9637-98D000B9272C|请求ID。 |
|Success|Boolean|true|是否成功，取值：

 -   `true`：成功
-   `false`：失败 |
|Total|Integer|25|总记录条数。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeExporterOutputList
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>BB30C6D9-8D0D-442E-9484-C15BADE76A21</RequestId>
<PageNumber>1</PageNumber>
<Total>1</Total>
<Datapoints>
    <Datapoint>
        <DestType>SLS</DestType>
        <DestName>desctName1</DestName>
        <CreateTime>1584016495498</CreateTime>
        <ConfigJson>
            <endpoint>http://cn-qingdao-share.log.aliyuncs.com</endpoint>
            <as>TxHwuJ8yAb3AULcnny******</as>
            <project>exporter</project>
            <ak>LTAIpY33********</ak>
            <logstore>exporter</logstore>
        </ConfigJson>
    </Datapoint>
</Datapoints>
<Code>200</Code>
<Success>true</Success>
```

`JSON` 格式

```
{
	"RequestId": "BB30C6D9-8D0D-442E-9484-C15BADE76A21",
	"PageNumber": 1,
	"Total": 1,
	"Datapoints": {
		"Datapoint": [
			{
				"DestType": "SLS",
				"DestName": "desctName1",
				"CreateTime": 1584016495498,
				"ConfigJson": {
					"endpoint": "http://cn-qingdao-share.log.aliyuncs.com",
					"as": "TxHwuJ8yAb3AULcnny******",
					"project": "exporter",
					"ak": "LTAIpY33********",
					"logstore": "exporter"
				}
			}
		]
	},
	"Code": "200",
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

