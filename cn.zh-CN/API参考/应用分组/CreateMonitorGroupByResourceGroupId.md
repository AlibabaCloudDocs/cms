# CreateMonitorGroupByResourceGroupId

调用CreateMonitorGroupByResourceGroupId接口通过资源组创建应用分组。

调用本接口之前，请确保您已在资源管理中创建资源组。具体操作，请参见 [创建资源组](~~94485~~)。

本接口支持的云服务包括：云服务器ECS、云数据库RDS、版负载均衡SLB、弹性公网IP、DDos防护包、内容分发网络CDN、共享带宽CBWP、云数据库PolarDB和云数据库Redis版。

本文将提供一个示例，为地域`cn-hangzhou`的资源组`CloudMonitor`创建一个应用分组，应用分组的报警联系人组为`ECS_Group`。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=CreateMonitorGroupByResourceGroupId&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateMonitorGroupByResourceGroupId|要执行的操作，取值：CreateMonitorGroupByResourceGroupId。 |
|ContactGroupList.N|RepeatList|是|ECS\_Group|报警联系人组。

 关于如何获取报警联系人组，请参见[DescribeContactGroupList](~~114922~~)。 |
|RegionId|String|是|cn-hangzhou|资源组对应的地域ID。 |
|ResourceGroupId|String|是|rg-acfmw3ty5y7\*\*\*\*|资源组ID。

 关于如何获取资源组ID，请参见[ListResourceGroups](~~158855~~)。

 **说明：** ResourceGroupId和ResourceGroupName至少设置一个。 |
|ResourceGroupName|String|是|CloudMonitor|资源组名称。

 关于如何获取资源组名称，请参见[ListResourceGroups](~~158855~~)。

 **说明：** ResourceGroupId和ResourceGroupName至少设置一个。 |
|EnableSubscribeEvent|Boolean|否|true|应用分组是否自动订阅事件通知。取值：

 -   true
-   false |
|EnableInstallAgent|Boolean|否|true|应用分组是否自动安装云监控插件。取值：

 -   true
-   false |

关于公共请求参数的详情，请参见[公共参数](~~199331~~)。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The specified resource is not found.|错误信息。 |
|RequestId|String|3D373A32-9EF5-409D-B6D7-DDDB714FFE94|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=CreateMonitorGroupByResourceGroupId
&ContactGroupList.1=ECS_Group
&RegionId=cn-hangzhou
&ResourceGroupId=rg-acfmw3ty5y7****
&ResourceGroupName=CloudMonitor
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<CreateMonitorGroupByResourceGroupIdResponse>
	  <RequestId>EBB5215C-44AB-4000-A2D7-48634FDC4F04</RequestId>
	  <Success>true</Success>
	  <Code>200</Code>
</CreateMonitorGroupByResourceGroupIdResponse>
```

`JSON`格式

```
{
    "RequestId": "EBB5215C-44AB-4000-A2D7-48634FDC4F04",
    "Success": "true",
    "Code": "200"
}
```

## 错误码

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|404|ResourceNotFound|The specified resource is not found.|未找到指定资源。|

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

