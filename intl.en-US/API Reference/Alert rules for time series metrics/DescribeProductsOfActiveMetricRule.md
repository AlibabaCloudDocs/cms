# DescribeProductsOfActiveMetricRule

Queries the services for which one-click alert is enabled.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeProductsOfActiveMetricRule&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeProductsOfActiveMetricRule|The operation that you want to perform. Set the value to DescribeProductsOfActiveMetricRule. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|AllProductInitMetricRuleList|Array of AllProductInitMetricRule|N/A|The information about the services for which one-click alert is enabled. |
|AllProductInitMetricRule|N/A|N/A|N/A|
|AlertInitConfigList|Array of AlertInitConfig|N/A|The initial alert rules that are generated after one-click alert is enabled for a service. |
|AlertInitConfig|N/A|N/A|N/A|
|EvaluationCount|String|3|The consecutive number of times for which the metric value is measured before an alert is triggered. |
|MetricName|String|cpu\_total|The name of the metric. For more information, see [Appendix 1: Metrics](~~163515~~). |
|Namespace|String|acs\_rds\_dashboard|The namespace of the service. For more information, see [Appendix 1: Metrics](~~163515~~). |
|Period|String|1m|The aggregation period of the monitoring data. Unit: minutes. For more information, see [Appendix 1: Metrics](~~163515~~). |
|Statistics|String|Average|The statistical aggregation method that is used to calculate metric values that trigger alerts. For more information, see [Appendix 1: Metrics](~~163515~~). |
|Threshold|String|90|The threshold of the metric value. |
|Product|String|ecs|The abbreviation of the service name. |
|Code|Integer|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|Datapoints|String|ecs,rds|The information about the services for which one-click alert is enabled. Services are separated with commas \(,\). Valid values:

-   ecs: Elastic Compute Service \(ECS\)
-   rds: ApsaraDB for RDS
-   slb: Server Load Balancer \(SLB\)
-   redis\_standard: ApsaraDB for Redis of the standard architecture
-   redis\_sharding: ApsaraDB for Redis of the cluster architecture
-   redis\_splitrw: ApsaraDB for Redis of the read/write splitting architecture
-   mongodb: ApsaraDB for MongoDB of the replica set architecture
-   mongodb\_sharding: ApsaraDB for MongoDB of the sharded cluster architecture
-   hbase: ApsaraDB for HBase
-   elasticsearch: Elasticsearch
-   opensearch: Open Search |
|Message|String|The Request is not authorization.|The returned message. |
|RequestId|String|F82E6667-7811-4BA0-842F-5B2DC42BBAAD|The ID of the request. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=DescribeProductsOfActiveMetricRule
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeProductsOfActiveMetricRuleResponse>
          <RequestId>A4FFAEFF-4225-4EF6-8F63-FAAA8F58289D</RequestId>
          <AllProductInitMetricRuleList>
                <AllProductInitMetricRule>
                      <AlertInitConfigList>
                            <AlertInitConfig>
                                  <MetricName>CPUUtilization</MetricName>
                                  <EvaluationCount>5</EvaluationCount>
                                  <Period>1m</Period>
                                  <Statistics>Average</Statistics>
                                  <Namespace>acs_ecs_dashboard</Namespace>
                                  <Threshold>95</Threshold>
                            </AlertInitConfig>
                            <AlertInitConfig>
                                  <MetricName>vm.DiskUtilization</MetricName>
                                  <EvaluationCount>5</EvaluationCount>
                                  <Period>1m</Period>
                                  <Statistics>Average</Statistics>
                                  <Namespace>acs_ecs_dashboard</Namespace>
                                  <Threshold>95</Threshold>
                            </AlertInitConfig>
                            <AlertInitConfig>
                                  <MetricName>vm.MemoryUtilization</MetricName>
                                  <EvaluationCount>5</EvaluationCount>
                                  <Period>1m</Period>
                                  <Statistics>Average</Statistics>
                                  <Namespace>acs_ecs_dashboard</Namespace>
                                  <Threshold>95</Threshold>
                            </AlertInitConfig>
                            <AlertInitConfig>
                                  <MetricName>InternetOutRate_Percent</MetricName>
                                  <EvaluationCount>5</EvaluationCount>
                                  <Period>1m</Period>
                                  <Statistics>Average</Statistics>
                                  <Namespace>acs_ecs_dashboard</Namespace>
                                  <Threshold>95</Threshold>
                            </AlertInitConfig>
                      </AlertInitConfigList>
                      <Product>ecs</Product>
                </AllProductInitMetricRule>
                <AllProductInitMetricRule>
                      <AlertInitConfigList>
                            <AlertInitConfig>
                                  <MetricName>CpuUsage</MetricName>
                                  <EvaluationCount>5</EvaluationCount>
                                  <Period>5m</Period>
                                  <Statistics>Average</Statistics>
                                  <Namespace>acs_rds_dashboard</Namespace>
                                  <Threshold>80</Threshold>
                            </AlertInitConfig>
                            <AlertInitConfig>
                                  <MetricName>DiskUsage</MetricName>
                                  <EvaluationCount>5</EvaluationCount>
                                  <Period>5m</Period>
                                  <Statistics>Average</Statistics>
                                  <Namespace>acs_rds_dashboard</Namespace>
                                  <Threshold>80</Threshold>
                            </AlertInitConfig>
                            <AlertInitConfig>
                                  <MetricName>IOPSUsage</MetricName>
                                  <EvaluationCount>5</EvaluationCount>
                                  <Period>5m</Period>
                                  <Statistics>Average</Statistics>
                                  <Namespace>acs_rds_dashboard</Namespace>
                                  <Threshold>80</Threshold>
                            </AlertInitConfig>
                            <AlertInitConfig>
                                  <MetricName>ConnectionUsage</MetricName>
                                  <EvaluationCount>5</EvaluationCount>
                                  <Period>5m</Period>
                                  <Statistics>Average</Statistics>
                                  <Namespace>acs_rds_dashboard</Namespace>
                                  <Threshold>80</Threshold>
                            </AlertInitConfig>
                            <AlertInitConfig>
                                  <MetricName>DataDelay</MetricName>
                                  <EvaluationCount>5</EvaluationCount>
                                  <Period>5m</Period>
                                  <Statistics>Average</Statistics>
                                  <Namespace>acs_rds_dashboard</Namespace>
                                  <Threshold>5</Threshold>
                            </AlertInitConfig>
                      </AlertInitConfigList>
                      <Product>rds</Product>
                </AllProductInitMetricRule>
                <AllProductInitMetricRule>
                      <AlertInitConfigList>
                            <AlertInitConfig>
                                  <MetricName>DocSizeRatiobyApp</MetricName>
                                  <EvaluationCount>1</EvaluationCount>
                                  <Period>10m</Period>
                                  <Statistics>Maximum</Statistics>
                                  <Namespace>acs_opensearch</Namespace>
                                  <Threshold>85</Threshold>
                            </AlertInitConfig>
                            <AlertInitConfig>
                                  <MetricName>lossqpsbyapp</MetricName>
                                  <EvaluationCount>1</EvaluationCount>
                                  <Period>10m</Period>
                                  <Statistics>Maximum</Statistics>
                                  <Namespace>acs_opensearch</Namespace>
                                  <Threshold>0</Threshold>
                            </AlertInitConfig>
                            <AlertInitConfig>
                                  <MetricName>ComputeResourceRatiobyApp</MetricName>
                                  <EvaluationCount>1</EvaluationCount>
                                  <Period>10m</Period>
                                  <Statistics>Maximum</Statistics>
                                  <Namespace>acs_opensearch</Namespace>
                                  <Threshold>85</Threshold>
                            </AlertInitConfig>
                            <AlertInitConfig>
                                  <MetricName>app_realtime_write_latency</MetricName>
                                  <EvaluationCount>1</EvaluationCount>
                                  <Period>20m</Period>
                                  <Statistics>Maximum</Statistics>
                                  <Namespace>acs_opensearch</Namespace>
                                  <Threshold>1800000</Threshold>
                            </AlertInitConfig>
                      </AlertInitConfigList>
                      <Product>opensearch</Product>
                </AllProductInitMetricRule>
          </AllProductInitMetricRuleList>
          <Datapoints>rds,redis_standard</Datapoints>
          <Code>200</Code>
          <Success>true</Success>
</DescribeProductsOfActiveMetricRuleResponse>
```

`JSON` format

```
{
    "RequestId": "A4FFAEFF-4225-4EF6-8F63-FAAA8F58289D",
    "AllProductInitMetricRuleList": {
        "AllProductInitMetricRule": [
            {
                "AlertInitConfigList": {
                    "AlertInitConfig": [
                        {
                            "MetricName": "CPUUtilization",
                            "EvaluationCount": "5",
                            "Period": "1m",
                            "Statistics": "Average",
                            "Namespace": "acs_ecs_dashboard",
                            "Threshold": "95"
                        },
                        {
                            "MetricName": "vm.DiskUtilization",
                            "EvaluationCount": "5",
                            "Period": "1m",
                            "Statistics": "Average",
                            "Namespace": "acs_ecs_dashboard",
                            "Threshold": "95"
                        },
                        {
                            "MetricName": "vm.MemoryUtilization",
                            "EvaluationCount": "5",
                            "Period": "1m",
                            "Statistics": "Average",
                            "Namespace": "acs_ecs_dashboard",
                            "Threshold": "95"
                        },
                        {
                            "MetricName": "InternetOutRate_Percent",
                            "EvaluationCount": "5",
                            "Period": "1m",
                            "Statistics": "Average",
                            "Namespace": "acs_ecs_dashboard",
                            "Threshold": "95"
                        }
                    ]
                },
                "Product": "ecs"
            },
            {
                "AlertInitConfigList": {
                    "AlertInitConfig": [
                        {
                            "MetricName": "CpuUsage",
                            "EvaluationCount": "5",
                            "Period": "5m",
                            "Statistics": "Average",
                            "Namespace": "acs_rds_dashboard",
                            "Threshold": "80"
                        },
                        {
                            "MetricName": "DiskUsage",
                            "EvaluationCount": "5",
                            "Period": "5m",
                            "Statistics": "Average",
                            "Namespace": "acs_rds_dashboard",
                            "Threshold": "80"
                        },
                        {
                            "MetricName": "IOPSUsage",
                            "EvaluationCount": "5",
                            "Period": "5m",
                            "Statistics": "Average",
                            "Namespace": "acs_rds_dashboard",
                            "Threshold": "80"
                        },
                        {
                            "MetricName": "ConnectionUsage",
                            "EvaluationCount": "5",
                            "Period": "5m",
                            "Statistics": "Average",
                            "Namespace": "acs_rds_dashboard",
                            "Threshold": "80"
                        },
                        {
                            "MetricName": "DataDelay",
                            "EvaluationCount": "5",
                            "Period": "5m",
                            "Statistics": "Average",
                            "Namespace": "acs_rds_dashboard",
                            "Threshold": "5"
                        }
                    ]
                },
                "Product": "rds"
            },
            {
                "AlertInitConfigList": {
                    "AlertInitConfig": [
                        {
                            "MetricName": "DocSizeRatiobyApp",
                            "EvaluationCount": "1",
                            "Period": "10m",
                            "Statistics": "Maximum",
                            "Namespace": "acs_opensearch",
                            "Threshold": "85"
                        },
                        {
                            "MetricName": "lossqpsbyapp",
                            "EvaluationCount": "1",
                            "Period": "10m",
                            "Statistics": "Maximum",
                            "Namespace": "acs_opensearch",
                            "Threshold": "0"
                        },
                        {
                            "MetricName": "ComputeResourceRatiobyApp",
                            "EvaluationCount": "1",
                            "Period": "10m",
                            "Statistics": "Maximum",
                            "Namespace": "acs_opensearch",
                            "Threshold": "85"
                        },
                        {
                            "MetricName": "app_realtime_write_latency",
                            "EvaluationCount": "1",
                            "Period": "20m",
                            "Statistics": "Maximum",
                            "Namespace": "acs_opensearch",
                            "Threshold": "1800000"
                        }
                    ]
                },
                "Product": "opensearch"
            }
        ]
    },
    "Datapoints": "rds,redis_standard",
    "Code": 200,
    "Success": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

