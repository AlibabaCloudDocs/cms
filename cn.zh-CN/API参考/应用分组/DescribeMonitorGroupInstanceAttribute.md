# DescribeMonitorGroupInstanceAttribute

调用DescribeMonitorGroupInstanceAttribute接口查询应用分组的资源详情。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeMonitorGroupInstanceAttribute&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeMonitorGroupInstanceAttribute|要执行的操作，取值：DescribeMonitorGroupInstanceAttribute。 |
|GroupId|Long|是|123456|应用分组ID。 |
|PageNumber|Integer|否|1|分页页码。默认值：1。 |
|PageSize|Integer|否|10|每页显示记录条数。 |
|Total|Boolean|否|true|总记录条数。 |
|Category|String|否|ecs|资源所属的云服务。取值：

 -   ecs：包括阿里云和非阿里云主机。
-   rds：云数据库RDS版。
-   ads：分析型数据库。
-   slb：负载均衡。
-   vpc：专有网络。
-   apigateway：API网关。
-   cdn：内容分发网络。
-   cs：容器服务Swarm版。
-   dcdn：全站加速。
-   ddos：DDoS防护。
-   eip：弹性公网IP。
-   elasticsearch：阿里云Elasticsearch。
-   emr：E-MapReduce。
-   ess：弹性伸缩。
-   hbase：云数据库 HBase。
-   iot\_edge：IoT边缘计算。
-   k8s\_pod：k8s pod。
-   kvstore\_sharding：Redis集群版。
-   kvstore\_splitrw：Redis读写分离版。
-   kvstore\_standard：Redis标准版。
-   memcache：云数据库Memcache。
-   mns：消息服务。
-   mongodb：MongoDB副本实例。
-   mongodb\_cluster：MongoDB集群版本。
-   mongodb\_sharding：MongoDB分片集群。
-   mq\_topic：消息服务Topic。
-   ocs：旧版云数据库Memcache。
-   opensearch：开放搜索。
-   oss：对象存储OSS。
-   polardb：云数据库PolarDB。
-   petadata：HybridDB for MySQL。
-   scdn：安全加速。
-   sharebandwidthpackages：共享带宽包。
-   sls：日志服务。
-   vpn：VPN网关。 |
|Keyword|String|否|portal|资源的关键字。可以按照资源ID模糊搜索。 |
|InstanceIds|String|否|i-m5e0k0bexac8tykr\*\*\*\*|资源ID。多个资源ID之间用英文逗号（,）分隔，最多支持20个资源。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|9FB8EA79-7279-4482-8D6D-3D28EEDD871A|请求ID。 |
|Code|Integer|200|状态码。

 **说明：** 200表示成功。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |
|PageNumber|Integer|1|页码。 |
|PageSize|Integer|2|总页数。 |
|Total|Integer|12|总记录条数。 |
|Resources|Array of Resource| |应用分组关联的资源。 |
|Resource| | | |
|Category|String|ecs|云服务名称。 |
|Desc|String|desc\_test|资源描述信息。 |
|Dimension|String|\{"instanceId":"i-m5e0k0bexac8tykr\*\*\*\*"\}|应用分组关联资源的维度信息。 |
|InstanceId|String|i-m5e0k0bexac8tykr\*\*\*\*|实例ID。 |
|InstanceName|String|hostName|实例名称。 |
|NetworkType|String|vpc|网络类型。 |
|Region|Struct| |地域。 |
|AvailabilityZone|String|cn-hangzhou-f|可用区。 |
|RegionId|String|cn-hangzhou|地域ID。 |
|Tags|Array of Tag| |资源的标签。 |
|Tag| | | |
|Key|String|instanceNetworkType|标签键。 |
|Value|String|VPC|标签值。 |
|Vpc|Struct| |VPC实例的描述信息。 |
|VpcInstanceId|String|vpc-2zew7etgiceg21\*\*\*\*|VPC实例ID。 |
|VswitchInstanceId|String|vsw-2ze36seq79n992\*\*\*\*|Vswitch实例ID。 |
|Message|String|The specified resource is not found.|错误信息。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeMonitorGroupInstanceAttribute
&GroupId=123456
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeMonitorGroupInstanceAttributeResponse>
	  <PageNumber>1</PageNumber>
	  <PageSize>30</PageSize>
	  <RequestId>7DB8DA3D-EDA6-46F8-9222-70C52416AE7D</RequestId>
	  <Success>true</Success>
	  <Code>200</Code>
	  <Total>1</Total>
	  <Resources>
		    <Resource>
			      <Vpc>
				        <VswitchInstanceId>vsw-2ze36seq79n992****</VswitchInstanceId>
				        <VpcInstanceId>vpc-2zew7etgiceg21****</VpcInstanceId>
			      </Vpc>
			      <Tags>
				        <Tag>
					          <Value>12345</Value>
					          <Key>aliUid</Key>
				        </Tag>
				        <Tag>
					          <Value>26842</Value>
					          <Key>bid</Key>
				        </Tag>
			      </Tags>
			      <NetworkType>VPC</NetworkType>
			      <Category>RDS</Category>
			      <Region>
				        <RegionId>cn-hangzhou</RegionId>
				        <AvailabilityZone>cn-hangzhou-MAZ8(f,g)</AvailabilityZone>
			      </Region>
			      <AliUid>127067667954****</AliUid>
			      <InstanceId>i-m5e0k0bexac8tykr****</InstanceId>
			      <Dimension>{\"userId\":\"127067667954****\",\"instanceId\":\"rm-bp179a8xfaz4i****\"}</Dimension>
			      <Desc>test_name</Desc>
			      <InstanceName>test_name</InstanceName>
		    </Resource>
	  </Resources>
</DescribeMonitorGroupInstanceAttributeResponse>
```

`JSON` 格式

```
{
    "PageNumber": 1,
    "PageSize": 30,
    "RequestId": "7DB8DA3D-EDA6-46F8-9222-70C52416AE7D",
    "Success": true,
    "Code": 200,
    "Total": 1,
    "Resources": {
        "Resource": [
            {
                "Vpc": {
                    "VswitchInstanceId": "vsw-2ze36seq79n992****",
                    "VpcInstanceId": "vpc-2zew7etgiceg21****"
                },
                "Tags": {
                    "Tag": [
                        {
                            "Value": "12345",
                            "Key": "aliUid"
                        },
                        {
                            "Value": "26842",
                            "Key": "bid"
                        }
                    ]
                },
                "NetworkType": "VPC",
                "Category": "RDS",
                "Region": {
                    "RegionId": "cn-hangzhou",
                    "AvailabilityZone": "cn-hangzhou-MAZ8(f,g)"
                },
                "AliUid": "127067667954****",
                "InstanceId": "i-m5e0k0bexac8tykr****",
                "Dimension": "{\"userId\":\"127067667954****\",\"instanceId\":\"rm-bp179a8xfaz4i****\"}",
                "Desc": "test_name",
                "InstanceName": "test_name"
            }
        ]
    }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Cms)查看更多错误码。

