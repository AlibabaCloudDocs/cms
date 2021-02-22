# DescribeMonitorResourceQuotaAttribute

调用DescribeMonitorResourceQuotaAttribute接口查询云监控各个资源的配额。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeMonitorResourceQuotaAttribute&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeMonitorResourceQuotaAttribute|要执行的操作，取值：DescribeMonitorResourceQuotaAttribute。 |
|ShowUsed|Boolean|否|true|返回值是否包含已使用配额。取值：

 -   true（默认值）：包含。
-   false：不包含。 |

关于公共请求参数的详情，请参见[公共参数](~~199331~~)。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The specified resource is not found.|错误信息。 |
|RequestId|String|31BC7201-00F2-47B2-B7B9-6A173076ACE|请求ID。 |
|ResourceQuota|Struct| |云监控的配额详情。 |
|Api|Struct| |API配额。 |
|QuotaLimit|Integer|500|API总配额。单位：万次。 |
|QuotaPackage|Integer|500|套餐内API的配额。单位：万次。 |
|QuotaUsed|Integer|9987|套餐内API的配额用量。单位：次。 |
|CustomMonitor|Struct| |自定义监控配额。 |
|QuotaLimit|Integer|1200|自定义监控时间序列的总配额。单位：个。 |
|QuotaPackage|Integer|1000|套餐内自定义监控时间序列的配额。单位：个。 |
|QuotaUsed|Integer|8|套餐内自定义监控时间序列的配额用量。单位：个。 |
|EventMonitor|Struct| |事件监控配额。 |
|QuotaLimit|Integer|55|事件监控的总配额。单位：万。 |
|QuotaPackage|Integer|50|套餐包内事件监控的配额。单位：万。 |
|QuotaUsed|Integer|2|套餐包内事件监控的配额用量。单位：万。 |
|ExpireTime|String|2021-02-28|套餐到期时间。 |
|InstanceId|String|cms\_edition-cn-n6w20rn\*\*\*\*|预付费套餐ID。 |
|LogMonitor|Struct| |日志监控配额。 |
|QuotaLimit|Integer|150|日志监控的总配额。单位：MByte/Min。 |
|QuotaPackage|Integer|150|套餐包内日志监控的配额。单位：MByte/Min。 |
|QuotaUsed|Integer|80|套餐包内日志监控的配额使用量。单位：MByte/Min。 |
|Phone|Struct| |报警电话包配额。 |
|QuotaLimit|Integer|550|报警电话的总配额。单位：通。 |
|QuotaPackage|Integer|500|报警电话包的配额。单位：通。 |
|QuotaUsed|Integer|100|报警电话包的配额使用量。单位：通。 |
|SMS|Struct| |报警短信包配额。 |
|QuotaLimit|Integer|550|报警短信的总配额。单位：通。 |
|QuotaPackage|Integer|500|报警短信包的配额。单位：通。 |
|QuotaUsed|Integer|38|报警短信包的配额使用量。单位：通。 |
|SiteMonitorEcsProbe|Struct| |站点监控ECS探测点配额。 |
|QuotaLimit|Integer|5|站点监控ECS探测点的总配额。

 **说明：** 单个站点监控任务能够选择的最大ECS探测点的数量。 |
|QuotaPackage|Integer|5|套餐包内站点监控ECS探测点的配额。 |
|QuotaUsed|Integer|20|套餐包内站点监控ECS探测点的配额使用量。

 **说明：** 目前已创建的所有站点监控任务的总ECS探测点数量。 |
|SiteMonitorOperatorProbe|Struct| |站点监控运营商探测点配额。 |
|QuotaLimit|Integer|5|站点监控运营商探测点的总配额。 |
|QuotaPackage|Integer|5|套餐包内站点监控运营商探测点的配额。 |
|QuotaUsed|Integer|0|套餐包内站点监控运营商探测点的配额使用量。 |
|SiteMonitorTask|Struct| |站点监控任务配额。 |
|QuotaLimit|Integer|25|站点监控任务的总配额。单位：个。 |
|QuotaPackage|Integer|20|套餐包内站点监控任务的配额。单位：个。 |
|QuotaUsed|Integer|15|套餐包内站点监控任务的配额使用量。单位：个。 |
|SuitInfo|String|pro|云监控当前版本。取值：

 -   free：免费版。
-   pro：专业版。
-   cms\_post：后付费。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeMonitorResourceQuotaAttribute
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<DescribeMonitorResourceQuotaAttributeResponse>
	  <RequestId>1E1961C4-B340-45D7-8CC3-F7D0BF19F2E0</RequestId>
	  <ResourceQuota>
		    <SiteMonitorOperatorProbe>
			      <QuotaUsed>0</QuotaUsed>
			      <QuotaPackage>5</QuotaPackage>
			      <QuotaLimit>5</QuotaLimit>
		    </SiteMonitorOperatorProbe>
		    <InstanceId>cms_edition-cn-n6w20rn****</InstanceId>
		    <Phone>
			      <QuotaUsed>100</QuotaUsed>
			      <QuotaPackage>500</QuotaPackage>
			      <QuotaLimit>550</QuotaLimit>
		    </Phone>
		    <SuitInfo>pro</SuitInfo>
		    <SiteMonitorTask>
			      <QuotaUsed>7</QuotaUsed>
			      <QuotaPackage>20</QuotaPackage>
			      <QuotaLimit>20</QuotaLimit>
		    </SiteMonitorTask>
		    <SMS>
			      <QuotaUsed>38</QuotaUsed>
			      <QuotaPackage>500</QuotaPackage>
			      <QuotaLimit>550</QuotaLimit>
		    </SMS>
		    <LogMonitor>
			      <QuotaUsed>0</QuotaUsed>
			      <QuotaPackage>50</QuotaPackage>
			      <QuotaLimit>50</QuotaLimit>
		    </LogMonitor>
		    <Api>
			      <QuotaUsed>9987</QuotaUsed>
			      <QuotaPackage>500</QuotaPackage>
			      <QuotaLimit>500</QuotaLimit>
		    </Api>
		    <ExpireTime>2021-02-28</ExpireTime>
		    <SiteMonitorEcsProbe>
			      <QuotaUsed>20</QuotaUsed>
			      <QuotaPackage>5</QuotaPackage>
			      <QuotaLimit>5</QuotaLimit>
		    </SiteMonitorEcsProbe>
		    <CustomMonitor>
			      <QuotaUsed>8</QuotaUsed>
			      <QuotaPackage>1000</QuotaPackage>
			      <QuotaLimit>1200</QuotaLimit>
		    </CustomMonitor>
		    <EventMonitor>
			      <QuotaUsed>2</QuotaUsed>
			      <QuotaPackage>50</QuotaPackage>
			      <QuotaLimit>55</QuotaLimit>
		    </EventMonitor>
	  </ResourceQuota>
	  <Code>200</Code>
</DescribeMonitorResourceQuotaAttributeResponse>
```

`JSON`格式

```
{
	"RequestId": "1E1961C4-B340-45D7-8CC3-F7D0BF19F2E0",
	"ResourceQuota": {
		"SiteMonitorOperatorProbe": {
			"QuotaUsed": 0,
			"QuotaPackage": 5,
			"QuotaLimit": 5
		},
		"InstanceId": "cms_edition-cn-n6w20rn****",
		"Phone": {
			"QuotaUsed": 100,
			"QuotaPackage": 500,
			"QuotaLimit": 550
		},
		"SuitInfo": "pro",
		"SiteMonitorTask": {
			"QuotaUsed": 7,
			"QuotaPackage": 20,
			"QuotaLimit": 20
		},
		"SMS": {
			"QuotaUsed": 38,
			"QuotaPackage": 500,
			"QuotaLimit": 550
		},
		"LogMonitor": {
			"QuotaUsed": 0,
			"QuotaPackage": 50,
			"QuotaLimit": 50
		},
		"Api": {
			"QuotaUsed": 9987,
			"QuotaPackage": 500,
			"QuotaLimit": 500
		},
		"ExpireTime": "2021-02-28",
		"SiteMonitorEcsProbe": {
			"QuotaUsed": 20,
			"QuotaPackage": 5,
			"QuotaLimit": 5
		},
		"CustomMonitor": {
			"QuotaUsed": 8,
			"QuotaPackage": 1000,
			"QuotaLimit": 1200
		},
		"EventMonitor": {
			"QuotaUsed": 2,
			"QuotaPackage": 50,
			"QuotaLimit": 55
		}
	},
	"Code": 200
}
```

## 错误码

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|ResourceNotFound|The specified resource is not found.|未找到指定资源。|

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

