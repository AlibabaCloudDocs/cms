# EnableActiveMetricRule

Enables one-click alert for a service.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=EnableActiveMetricRule&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|EnableActiveMetricRule|The operation that you want to perform. Set the value to EnableActiveMetricRule. |
|Product|String|Yes|ecs|The service for which you want to enable one-click alert. Valid values:

 -   ecs: Elastic Compute Service \(ECS\)
-   rds: ApsaraDB RDS
-   slb: Server Load Balancer \(SLB\)
-   redis\_standard: ApsaraDB for Redis of the standard architecture
-   redis\_sharding: ApsaraDB for Redis of the cluster architecture
-   redis\_splitrw: ApsaraDB for Redis of the read/write splitting architecture
-   mongodb: ApsaraDB for MongoDB of the replica set architecture
-   mongodb\_sharding: ApsaraDB for MongoDB of the sharded cluster architecture
-   hbase: ApsaraDB for HBase
-   elasticsearch: Elasticsearch
-   opensearch: Open Search |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The HTTP status code.

 **Note:** The status code 200 indicates that the call was successful. |
|Message|String|The Request is not authorization.|The returned message. |
|RequestId|String|F82E6667-7811-4BA0-842F-5B2DC42BBAAD|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

 -   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=EnableActiveMetricRule
&Product=ecs
&<Common request parameters>
```

Sample success responses

`XML` format

```
<EnableActiveMetricRuleResponse>
      <Code>200</Code>
      <Success>true</Success>
      <RequestId>55850888-9CCE-4FD5-B949-5F8947D63929</RequestId>
</EnableActiveMetricRuleResponse>
```

`JSON` format

```
{
  "Code": "200",
  "Success": true,
  "RequestId": "55850888-9CCE-4FD5-B949-5F8947D63929"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

