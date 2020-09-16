# DescribeSystemEventMetaList

调用DescribeSystemEventMetaList接口查询系统事件的Meta信息。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeSystemEventMetaList&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeSystemEventMetaList|要执行的操作，取值：DescribeSystemEventMetaList。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|Integer|200|状态码。

 **说明：** 200表示成功。 |
|Data|Array of Resource| |Meta返回信息。 |
|Resource| | | |
|EventType|String|Exception|事件类型。取值：

 -   StatusNotification：故障通知。
-   Exception：异常。
-   Maintenance：运维。 |
|Level|String|INFO|报警级别。取值：

 -   CRITICAL：紧急。
-   WARN：警告。
-   INFO：信息。 |
|Name|String|SelectFailureRate|事件名称。 |
|NameDesc|String|查询失败率高|事件名称的描述信息。 |
|NameDesc.En|String|High query failure rate.|英文事件名称的描述信息。 |
|Product|String|ADS|产品名称缩写。 |
|Status|String|failed|事件状态。 |
|StatusDesc|String|Operation Failed|事件状态描述。 |
|Message|String|success|返回信息。 |
|RequestId|String|A6582C8B-E67C-4A19-BC15-EAEFEBDC7995|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeSystemEventMetaList
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeSystemEventMetaListResponse>
		  <RequestId>46350DCE-3399-473B-875F-1340DC97186C</RequestId>
		  <Message>success</Message>
		  <Data>
			    <Resource>
				      <Status>Failed</Status>
				      <StatusDesc>OperationFailed</StatusDesc>
				      <NameDesc>插入失败率10%</NameDesc>
				      <NameDesc.En>InsertFailureRate</NameDesc.En>
				      <EventType>Exception</EventType>
				      <Product>ADS</Product>
				      <Level>CRITICAL</Level>
				      <Name>InsertFailureRate</Name>
			    </Resource>
			    <Resource>
				      <Status>Failed</Status>
				      <StatusDesc>OptionFailed</StatusDesc>
				      <NameDesc>查询失败率10%</NameDesc>
				      <NameDesc.En>SelectFailureRate</NameDesc.En>
				      <EventType>Exception</EventType>
				      <Product>ADS</Product>
				      <Level>CRITICAL</Level>
				      <Name>SelectFailureRate</Name>
			    </Resource>
			    <Resource>
				      <Status>Failed</Status>
				      <StatusDesc>Operation Failed</StatusDesc>
				      <NameDesc>磁盘使用率80%</NameDesc>
				      <NameDesc.En>StorageUsage</NameDesc.En>
				      <EventType>Maintenance</EventType>
				      <Product>ADS</Product>
				      <Level>CRITICAL</Level>
				      <Name>StorageUsage</Name>
			    </Resource>
			    <Resource>
				      <Status>EightyPercentQuotaExceeded</Status>
				      <StatusDesc>超过Quota 80%事件</StatusDesc>
				      <NameDesc>超过Quota 80%事件</NameDesc>
				      <NameDesc.En>EightyPercentQuotaExceeded:Route</NameDesc.En>
				      <EventType>80%QuotaExceeded</EventType>
				      <Product>CEN</Product>
				      <Level>WARN</Level>
				      <Name>EightyPercentQuotaExceeded:Route</Name>
			    </Resource>
			    <Resource>
				      <Status>NinetyEightPercentQuotaExceeded</Status>
				      <StatusDesc>超过Quota 98%事件</StatusDesc>
				      <NameDesc>超过Quota 98%事件</NameDesc>
				      <NameDesc.En>NinetyEightPercentQuotaExceeded:Route</NameDesc.En>
				      <EventType>98%QuotaExceeded</EventType>
				      <Product>CEN</Product>
				      <Level>WARN</Level>
				      <Name>NinetyEightPercentQuotaExceeded:Route</Name>
			    </Resource>
		  </Data>
		  <Code>200</Code>
		  <Success>true</Success>
</DescribeSystemEventMetaListResponse>
```

`JSON` 格式

```
{
    "RequestId": "46350DCE-3399-473B-875F-1340DC97186C",
	"Message": "success",
    "Data": {
        "Resource": [
         {
				"Status": "Failed",
				"StatusDesc": "OperationFailed",
				"NameDesc": "插入失败率10%",
				"NameDesc.En": "InsertFailureRate",
				"EventType": "Exception",
				"Product": "ADS",
				"Level": "CRITICAL",
				"Name": "InsertFailureRate"
			},
			{
				"Status": "Failed",
				"StatusDesc": "OptionFailed",
				"NameDesc": "查询失败率10%",
				"NameDesc.En": "SelectFailureRate",
				"EventType": "Exception",
				"Product": "ADS",
				"Level": "CRITICAL",
				"Name": "SelectFailureRate"
			},
			{
				"Status": "Failed",
				"StatusDesc": "Operation Failed",
				"NameDesc": "磁盘使用率80%",
				"NameDesc.En": "StorageUsage",
				"EventType": "Maintenance",
				"Product": "ADS",
				"Level": "CRITICAL",
				"Name": "StorageUsage"
			},
			{
				"Status": "EightyPercentQuotaExceeded",
				"StatusDesc": "超过Quota 80%事件",
				"NameDesc": "超过Quota 80%事件",
				"NameDesc.En": "EightyPercentQuotaExceeded:Route",
				"EventType": "80%QuotaExceeded",
				"Product": "CEN",
				"Level": "WARN",
				"Name": "EightyPercentQuotaExceeded:Route"
			},
			{
				"Status": "NinetyEightPercentQuotaExceeded",
				"StatusDesc": "超过Quota 98%事件",
				"NameDesc": "超过Quota 98%事件",
				"NameDesc.En": "NinetyEightPercentQuotaExceeded:Route",
				"EventType": "98%QuotaExceeded",
				"Product": "CEN",
				"Level": "WARN",
				"Name": "NinetyEightPercentQuotaExceeded:Route"
			}
        ]
    },
    "Code": "200",
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

