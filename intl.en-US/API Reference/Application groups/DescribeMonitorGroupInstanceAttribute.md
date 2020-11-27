# DescribeMonitorGroupInstanceAttribute

Queries the details of the instances in an application group.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeMonitorGroupInstanceAttribute&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeMonitorGroupInstanceAttribute|The operation that you want to perform. Set the value to DescribeMonitorGroupInstanceAttribute. |
|GroupId|Long|Yes|123456|The ID of the application group. |
|PageNumber|Integer|No|1|The number of the page to return. Default value: 1. |
|PageSize|Integer|No|10|The number of entries to return on each page. |
|Total|Boolean|No|true|The total number of entries to return. |
|Category|String|No|ecs|The name and specifications of the cloud service to which the instance belongs. Valid values:

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
|Keyword|String|No|portal|The keyword used to search for instances. You can perform a fuzzy search based on the instance ID. |
|InstanceIds|String|No|i-m5e0k0bexac8tykr\*\*\*\*|The ID of the instance. Separate multiple instance IDs with commas \(,\). You can query the details about a maximum of 20 instances at a time. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|9FB8EA79-7279-4482-8D6D-3D28EEDD871A|The ID of the request. |
|Code|Integer|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |
|PageNumber|Integer|1|The page number of the returned page. |
|PageSize|Integer|2|The total number of returned pages. |
|Total|Integer|12|The total number of returned entries. |
|Resources|Array of Resource| |The instances associated with the application group. |
|Resource| | | |
|Category|String|ecs|The name of the cloud service. |
|Desc|String|desc\_test|The description of the instance. |
|Dimension|String|\{"instanceId":"i-m5e0k0bexac8tykr\*\*\*\*"\}|The dimensions of the instance that is associated with the application group. |
|InstanceId|String|i-m5e0k0bexac8tykr\*\*\*\*|The ID of the instance. |
|InstanceName|String|hostName|The name of the instance. |
|NetworkType|String|vpc|The type of the network. |
|Region|Struct| |The region where the instance resides. |
|AvailabilityZone|String|cn-hangzhou-f|The available zone where the instance resides. |
|RegionId|String|cn-hangzhou|The ID of the region where the instance resides. |
|Tags|Array of Tag| |The tags of the instance. |
|Tag| | | |
|Key|String|instanceNetworkType|The key of the tag. |
|Value|String|VPC|The value of the tag. |
|Vpc|Struct| |The information about the VPC. |
|VpcInstanceId|String|vpc-2zew7etgiceg21\*\*\*\*|The ID of the VPC where the instance resides. |
|VswitchInstanceId|String|vsw-2ze36seq79n992\*\*\*\*|The ID of the vSwitch to which the instance belongs. |
|Message|String|The specified resource is not found.|The error message. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeMonitorGroupInstanceAttribute
&GroupId=123456
&<Common request parameters>
```

Sample success responses

`XML` format

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

`JSON` format

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

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

