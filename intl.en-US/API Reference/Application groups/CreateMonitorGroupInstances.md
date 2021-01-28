# CreateMonitorGroupInstances

Adds resources to an application group.

You can add a maximum of 1,000 instances to an application group at a time. You can add a maximum of 3,000 instances of an Alibaba Cloud service to an application group. The total number of instances that you can add to an application group is unlimited.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=CreateMonitorGroupInstances&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CreateMonitorGroupInstances|The operation that you want to perform. Set the value to CreateMonitorGroupInstances. |
|GroupId|Long|Yes|12345|The ID of the application group. |
|Instances.N.Category|String|Yes|ECS|The abbreviation of the service name. Valid values:

 -   ecs: Elastic Compute Service \(ECS\) instances that are provided by Alibaba Cloud and hosts that are not provided by Alibaba Cloud
-   rds: ApsaraDB RDS
-   ads: AnalyticDB
-   slb: Server Load Balancer \(SLB\)
-   vpc: Virtual Private Cloud \(VPC\)
-   apigateway: API Gateway
-   cdn: Alibaba Cloud CDN
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
-   mongodb\_cluster: ApsaraDB for MongoDB of the standalone architecture
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
|Instances.N.InstanceId|String|Yes|i-2ze26xj5wwy12\*\*\*\*|The ID of the instance. |
|Instances.N.InstanceName|String|Yes|test-instance-ecs|The name of the instance. |
|Instances.N.RegionId|String|Yes|cn-hangzhou|The ID of the region where the instance resides. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|Integer|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Message|String|The Request is not authorization.|The returned message. |
|RequestId|String|1BC69FEB-56CD-4555-A0E2-02536A24A946|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=CreateMonitorGroupInstances
&GroupId=12345
&Instances.1.Category=ECS
&Instances.1.InstanceId=i-2ze26xj5wwy12****
&Instances.1.InstanceName=test-instance-ecs
&Instances.1.RegionId= cn-hangzhou
&<Common request parameters>
```

Sample success responses

`XML` format

```
<CreateMonitorGroupInstancesResponse>
      <RequestId>1BC69FEB-56CD-4555-A0E2-02536A24A946</RequestId>
      <Success>true</Success>
      <Code>200</Code>
</CreateMonitorGroupInstancesResponse>
```

`JSON` format

```
{
  "RequestId": "1BC69FEB-56CD-4555-A0E2-02536A24A946",
  "Success": true,
  "Code": 200
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

