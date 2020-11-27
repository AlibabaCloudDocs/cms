# DescribeMonitorGroupCategories

Queries the cloud services to which the resources in an application group belong and the number of resources that belong to each cloud service in the application group.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeMonitorGroupCategories&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeMonitorGroupCategories|The operation that you want to perform. Set the value to DescribeMonitorGroupCategories. |
|GroupId|Long|Yes|123456|The ID of the application group. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|Integer|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Message|String|The specified resource is not found.|The error message. |
|MonitorGroupCategories|Struct| |The cloud services to which the resources in the application group belong and the number of resources that belong to the cloud service. |
|GroupId|Long|123456|The ID of the application group. |
|MonitorGroupCategory|Array of CategoryItem| |One of the cloud services to which the resources in the application group belong and the number of resources that belong to the cloud service. |
|CategoryItem| | | |
|Category|String|ECS|The name of the cloud service. Valid values:

 -   ecs: Elastic Compute Service \(ECS\) instances that are provided by Alibaba Cloud and hosts that are not provided by Alibaba Cloud
-   rds: ApsaraDB RDS
-   ads: AnalyticDB
-   slb: Server Load Balancer \(SLB\)
-   vpc: Virtual Private Cloud \(VPC\)
-   apigateway: API Gateway
-   cdn: Alibaba Cloud Content Delivery Network \(CDN\)
-   cs: Container Service for Swarm
-   dcdn: Dynamic Route for CDN \(DCDN\)
-   ddos: Anti-DDoS
-   eip: Elastic IP Address \(EIP\)
-   elasticsearch: Elasticsearch
-   emr: E-MapReduce
-   ess: Auto Scaling
-   hbase: ApsaraDB for HBase
-   iot\_edge: IoT Edge
-   k8s\_pod: pods in Container Service for Kubernetes \(ACK\)
-   kvstore\_sharding: ApsaraDB for Redis of the cluster master-replica architecture
-   kvstore\_splitrw: ApsaraDB for Redis of the read/write splitting architecture
-   kvstore\_standard: ApsaraDB for Redis of the standard master-replica architecture
-   memcache: ApsaraDB for Memcache
-   mns: Message Service \(MNS\)
-   mongodb: ApsaraDB for MongoDB of the replica set architecture
-   mongodb\_cluster: ApsaraDB for MongoDB of the cluster architecture
-   mongodb\_sharding: ApsaraDB for MongoDB of the sharded cluster architecture
-   mq\_topic: MNS topics
-   ocs: ApsaraDB for Memcache of earlier versions
-   opensearch: Open Search
-   oss: Object Storage Service \(OSS\)
-   polardb: PolarDB
-   petadata: HybridDB for MySQL
-   scdn: Secure CDN \(SCDN\)
-   sharebandwidthpackages: EIP Bandwidth Plan
-   sls: Log Service
-   vpn: VPN Gateway |
|Count|Integer|1|The number of resources that belong to the cloud service. |
|RequestId|String|9E0347B0-EBC3-4769-A78D-D96F21C6BB52|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeMonitorGroupCategories
&GroupId=123456
&<Common request parameters>
```

Sample success responses

`XML` format

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

`JSON` format

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

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

