# EnableSiteMonitors

调用EnableSiteMonitors接口启用一个或多个站点监控任务。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=EnableSiteMonitors&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|EnableSiteMonitors|要执行的操作，取值：EnableSiteMonitors。 |
|TaskIds|String|是|49f7b317-7645-4cc9-94fd-ea42e522\*\*\*\*,49f7b317-7645-4cc9-94fd-ea42e522\*\*\*\*|站点监控任务ID。多个ID之间用英文逗号（,）分隔。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Data|Struct| |站点监控任务影响探测点的记录数。 |
|count|Integer|0|探测点的记录条数。 |
|Message|String|successful|返回信息。 |
|RequestId|String|3fcd12e7-d387-42ee-b77e-661c775bb17f|请求ID。 |
|Success|String|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=EnableSiteMonitors
&TaskIds=49f7b317-7645-4cc9-94fd-ea42e522****,49f7b317-7645-4cc9-94fd-ea42e522****
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DisableSiteMonitorsResponse>
	  <Message>successful</Message>
	  <RequestId>7AB49ADD-3276-4161-B9F9-8662CAA800D6</RequestId>
	  <Data>
		    <count>0</count>
	  </Data>
	  <Code>200</Code>
	  <Success>true</Success>
</DisableSiteMonitorsResponse>
```

`JSON` 格式

```
{
	"Message": "successful",
	"RequestId": "7AB49ADD-3276-4161-B9F9-8662CAA800D6",
	"Data": {
		"count": 0
	},
	"Code": "200",
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

