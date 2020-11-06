# DescribeMonitorGroupCategories

调用DescribeMonitorGroupCategories接口查询指定应用分组的资源列表和每个云服务的资源数量。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeMonitorGroupCategories&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeMonitorGroupCategories|要执行的操作，取值：DescribeMonitorGroupCategories。 |
|GroupId|Long|是|123456|应用分组ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|Integer|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The specified resource is not found.|错误信息。 |
|MonitorGroupCategories|Struct| |应用分组中资源的云服务类型。 |
|GroupId|Long|123456|应用分组ID。 |
|MonitorGroupCategory|Array of CategoryItem| |应用分组的云服务类型。 |
|CategoryItem| | | |
|Category|String|ECS|云服务名称。取值：

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
|Count|Integer|1|云服务的资源数量。 |
|RequestId|String|9E0347B0-EBC3-4769-A78D-D96F21C6BB52|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeMonitorGroupCategories
&GroupId=123456
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeMonitorGroupCategoriesResponse>
	  <RequestId>B7C9F725-E743-4F2E-81A2-4CC19783DC42</RequestId>
	  <MonitorGroupCategories>
		    <MonitorGroupCategory>
			      <CategoryItem>
				        <Category>ECS</Category>
				        <Count>39</Count>
			      </CategoryItem>
		    </MonitorGroupCategory>
		    <GroupId>123456</GroupId>
	  </MonitorGroupCategories>
	  <Code>200</Code>
	  <Success>true</Success>
</DescribeMonitorGroupCategoriesResponse>
```

`JSON` 格式

```
{
	"RequestId": "B7C9F725-E743-4F2E-81A2-4CC19783DC42",
	"MonitorGroupCategories": {
		"MonitorGroupCategory": {
			"CategoryItem": [
				{
					"Category": "ECS",
					"Count": 39
				}
			]
		},
		"GroupId": 123456
	},
	"Code": 200,
	"Success": true
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

