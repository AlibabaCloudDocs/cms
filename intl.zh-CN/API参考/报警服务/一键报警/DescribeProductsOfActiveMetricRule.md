# DescribeProductsOfActiveMetricRule

调用DescribeProductsOfActiveMetricRule接口查询开通一键报警规则的云服务列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cms&api=DescribeProductsOfActiveMetricRule&type=RPC&version=2019-01-01)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeProductsOfActiveMetricRule|要执行的操作，取值：DescribeProductsOfActiveMetricRule。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|AllProductInitMetricRuleList|Array of AllProductInitMetricRule| |开通一键报警的云服务列表。 |
|AllProductInitMetricRule| | | |
|AlertInitConfigList|Array of AlertInitConfig| |初始化开通一键报警云服务的规则列表。 |
|AlertInitConfig| | | |
|EvaluationCount|String|3|报警重试次数。 |
|MetricName|String|cpu\_total|监控项名称。详情请参见[云服务监控项](~~163515~~)。 |
|Namespace|String|acs\_rds\_dashboard|指标所属空间。用于区分每个云服务配置。详情请参见[云服务监控项](~~163515~~)。 |
|Period|String|1m|监控数据的聚合周期。单位：分钟。详情请参见[云服务监控项](~~163515~~)。 |
|Statistics|String|Average|报警统计方法。详情请参见[云服务监控项](~~163515~~)。 |
|Threshold|String|90|报警阈值。 |
|Product|String|ecs|阿里云服务缩写。 |
|Code|Integer|200|状态码。

 **说明：** 200表示成功。 |
|Datapoints|String|ecs,rds|开通一键报警的云服务列表。云服务之间用英文逗号（,）分隔。取值：

 -   ecs：云服务器ECS。
-   rds：云数据库RDS版。
-   slb：负载均衡。
-   redis\_standard：云数据库Redis标准版。
-   redis\_sharding：云数据库Redis集群版。
-   redis\_splitrw：云数据库Redis读写分离版。
-   mongodb：云数据库MongoDB版（副本集）。
-   mongodb\_sharding：云数据库MongoDB版（分片集群）。
-   hbase：云数据库HBase版。
-   elasticsearch：Elasticsearch。
-   opensearch：OpenSearch。 |
|Message|String|The Request is not authorization.|错误信息。 |
|RequestId|String|F82E6667-7811-4BA0-842F-5B2DC42BBAAD|请求ID。 |
|Success|Boolean|true|操作是否成功。取值：

 -   true：成功。
-   false：失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeProductsOfActiveMetricRule
&<公共请求参数>
```

正常返回示例

`XML` 格式

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

`JSON` 格式

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

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Cms)查看更多错误码。

