# CreateMonitorGroupInstances

调用CreateMonitorGroupInstances接口添加资源到应用分组。

一个应用分组中，一个云服务最多添加3000个资源，单次最多添加1000个资源，应用分组中的总资源数无限制。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=CreateMonitorGroupInstances&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateMonitorGroupInstances|要执行的操作，取值：CreateMonitorGroupInstances。 |
|GroupId|Long|是|12345|应用分组ID。 |
|Instances.N.Category|String|是|ECS|云服务名称缩写。取值：

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
-   hbase：云数据库HBase。
-   iot\_edge：IoT边缘计算。
-   k8s\_pod：容器服务Kubernetes版的容器组（pod）。
-   kvstore\_sharding：Redis集群版。
-   kvstore\_splitrw：Redis读写分离版。
-   kvstore\_standard：Redis标准版。
-   memcache：云数据库Memcache。
-   mns：消息服务。
-   mongodb：云数据库MongoDB版副本集实例。
-   mongodb\_cluster：云数据库MongoDB版单节点实例。
-   mongodb\_sharding：云数据库MongoDB版分片集群实例。
-   mq\_topic：消息服务主题。
-   ocs：旧版云数据库Memcache。
-   opensearch：开放搜索。
-   oss：对象存储OSS。
-   polardb：云数据库PolarDB。
-   petadata：HybridDB for MySQL。
-   scdn：安全加速。
-   sharebandwidthpackages：共享带宽包。
-   sls：日志服务。
-   vpn：VPN网关。 |
|Instances.N.InstanceId|String|是|i-2ze26xj5wwy12\*\*\*\*|实例ID。 |
|Instances.N.InstanceName|String|是|test-instance-ecs|实例名称。 |
|Instances.N.RegionId|String|是|cn-hangzhou|实例所在地域。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|Integer|200|状态码。

 **说明：** 200表示成功。 |
|Message|String|The Request is not authorization.|错误信息。 |
|RequestId|String|1BC69FEB-56CD-4555-A0E2-02536A24A946|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=CreateMonitorGroupInstances
&GroupId=12345
&Instances.1.Category=ECS
&Instances.1.InstanceId=i-2ze26xj5wwy12****
&Instances.1.InstanceName=test-instance-ecs
&Instances.1.RegionId= cn-hangzhou
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<CreateMonitorGroupInstancesResponse>
      <RequestId>1BC69FEB-56CD-4555-A0E2-02536A24A946</RequestId>
      <Success>true</Success>
      <Code>200</Code>
</CreateMonitorGroupInstancesResponse>
```

`JSON` 格式

```
{
  "RequestId": "1BC69FEB-56CD-4555-A0E2-02536A24A946",
  "Success": true,
  "Code": 200
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

