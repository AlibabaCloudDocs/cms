# CreateMonitorGroupByResourceGroupId

Creates an application group by using a resource group.

Before you call this operation, make sure that you have created a resource group in the Resource Management console. For more information, see [Create a resource group](~~94485~~).

This operation supports the following cloud services: Elastic Compute Service \(ECS\), ApsaraDB RDS, Server Load Balancer \(SLB\), Elastic IP Address \(EIP\), Anti-DDoS, Alibaba Cloud CDN, EIP Bandwidth Plan, PolarDB, and ApsaraDB for Redis.

This topic provides an example on how to create an application group by using the resource group `CloudMonitor` and alert group `ECS_Group`. The region ID of the resource group is `cn-hangzhou`.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=CreateMonitorGroupByResourceGroupId&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CreateMonitorGroupByResourceGroupId|The operation that you want to perform. Set the value to CreateMonitorGroupByResourceGroupId. |
|ContactGroupList.N|RepeatList|Yes|ECS\_Group|The alert group.

For more information about how to query the alert group, see [DescribeContactGroupList](~~114922~~). |
|RegionId|String|Yes|cn-hangzhou|The ID of the region where the resource group resides. |
|ResourceGroupId|String|Yes|rg-acfmw3ty5y7\*\*\*\*|The ID of the resource group.

For more information about how to query the resource group ID, see [ListResourceGroups](~~158855~~).

**Note:** Set at least one of the ResourceGroupId and ResourceGroupName parameters. |
|ResourceGroupName|String|Yes|CloudMonitor|The name of the resource group.

For more information about how to query the resource group name, see [ListResourceGroups](~~158855~~).

**Note:** Set at least one of the ResourceGroupId and ResourceGroupName parameters. |
|EnableSubscribeEvent|Boolean|No|true|Specifies whether the application group automatically subscribes to event notifications. Valid values:

-   true
-   false |
|EnableInstallAgent|Boolean|No|true|Specifies whether the Cloud Monitor agent is automatically installed for the application group. Valid values:

-   true
-   false |

For more information about common request parameters, see [Common parameters](~~199331~~).

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

**Note:** The HTTP status code 200 indicates a success. |
|Message|String|The specified resource is not found.|The error message. |
|RequestId|String|3D373A32-9EF5-409D-B6D7-DDDB714FFE94|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=CreateMonitorGroupByResourceGroupId
&ContactGroupList.1=ECS_Group
&RegionId=cn-hangzhou
&ResourceGroupId=rg-acfmw3ty5y7****
&ResourceGroupName=CloudMonitor
&<Common request parameters>
```

Sample success responses

`XML` format

```
<CreateMonitorGroupByResourceGroupIdResponse>
      <RequestId>EBB5215C-44AB-4000-A2D7-48634FDC4F04</RequestId>
      <Success>true</Success>
      <Code>200</Code>
</CreateMonitorGroupByResourceGroupIdResponse>
```

`JSON` format

```
{
    "RequestId": "EBB5215C-44AB-4000-A2D7-48634FDC4F04",
    "Success": "true",
    "Code": "200"
}
```

## Error codes

|HTTP status code|Error code|Error message|Description|
|----------------|----------|-------------|-----------|
|404|ResourceNotFound|The specified resource is not found.|The error message returned because the specified resource is not found.|

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

