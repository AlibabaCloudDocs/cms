# DescribeSiteMonitorQuota

调用DescribeSiteMonitorQuota接口查询站点监控的配额以及版本。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeSiteMonitorQuota&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeSiteMonitorQuota|要执行的操作，取值：DescribeSiteMonitorQuota。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Data|Struct| |配额。 |
|SecondMonitor|Boolean|false|是否开启秒级监控。取值：

 -   true：开启。
-   false：关闭。 |
|SiteMonitorIdcQuota|Integer|5|阿里巴巴探测点配额。免费配额5个。 |
|SiteMonitorOperatorQuotaQuota|Integer|0|非阿里巴巴探测点配额。默认值：0。 |
|SiteMonitorQuotaTaskUsed|Integer|6|站点监控探测任务配额使用数。 |
|SiteMonitorTaskQuota|Integer|10|站点监控探测任务配额。 |
|SiteMonitorVersion|String|V1|站点监控版本。取值：

 -   V1：老版本。
-   V2：新版本。 |
|Message|String|请求成功|返回信息。 |
|RequestId|String|26860260-76C6-404E-AB7A-EB98D36A6885|请求ID。 |
|Success|String|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeSiteMonitorQuota
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeSiteMonitorQuotaResponse>
		  <Message>请求成功</Message>
		  <RequestId>C1359088-B0D3-4344-BA51-FB920425D836</RequestId>
		  <Data>
			    <SiteMonitorVersion>V2</SiteMonitorVersion>
			    <SiteMonitorQuotaTaskUsed>2</SiteMonitorQuotaTaskUsed>
			    <SecondMonitor>false</SecondMonitor>
			    <SiteMonitorOperatorQuotaQuota>0</SiteMonitorOperatorQuotaQuota>
			    <SiteMonitorTaskQuota>100</SiteMonitorTaskQuota>
			    <SiteMonitorIdcQuota>5</SiteMonitorIdcQuota>
		  </Data>
		  <Code>200</Code>
		  <Success>true</Success>
</DescribeSiteMonitorQuotaResponse>
```

`JSON` 格式

```
{
	"Message": "请求成功",
	"RequestId": "C1359088-B0D3-4344-BA51-FB920425D836",
	"Data": {
		"SiteMonitorVersion": "V2",
		"SiteMonitorQuotaTaskUsed": 2,
		"SecondMonitor": false,
		"SiteMonitorOperatorQuotaQuota": 0,
		"SiteMonitorTaskQuota": 100,
		"SiteMonitorIdcQuota": 5
	},
	"Code": "200",
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

