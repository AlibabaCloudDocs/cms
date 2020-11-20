# DisableHostAvailability

调用DisableHostAvailability接口禁用指定可用性监控任务。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DisableHostAvailability&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DisableHostAvailability|要执行的操作，取值：DisableHostAvailability。 |
|Id.N|RepeatList|是|12345|可用性监控任务ID。N的取值范围：1~20。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|User not authorized to operate on the specified resource.|错误信息。 |
|RequestId|String|ACBDBB40-DFB6-4F4C-8957-51FFB233969C|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DisableHostAvailability
&Id.1=12345
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DisableHostAvailabilityResponse>
      <RequestId>ACBDBB40-DFB6-4F4C-8957-51FFB233969C</RequestId>
      <Success>true</Success>
      <Code>200</Code>
</DisableHostAvailabilityResponse>
```

`JSON` 格式

```
{
  "RequestId": "ACBDBB40-DFB6-4F4C-8957-51FFB233969C",
  "Success": true,
  "Code": 200
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

