# DescribeProjectMeta

Queries information about monitored services in Cloud Monitor.

The information that can be obtained by this operation includes the service description, namespace, and tags.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeProjectMeta&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeProjectMeta|The operation that you want to perform. Set the value to DescribeProjectMeta. |
|Labels|String|No|\[\{"name":"product","value":"ECS"\}\]|The tags of the service. Tags are used to filter services.

 You can filter services only by the tag whose `name` is `product`. Example: \{"name":"product","value":"ECS"\}.

 **Note:** We recommend that you do not use the special tags in the Cloud Monitor console. |
|PageNumber|Integer|No|1|The page to return. Default value: 1 |
|PageSize|Integer|No|30|The number of entries to return on each page. Default value: 30.

 **Note:** The value of this parameter is not limited. You can view a large number of entries per page. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|String|200|The response code.

 **Note:** The HTTP 200 code indicates that the request was successful. |
|Message|String|The Request is not authorization.|The error message. |
|PageNumber|String|1|The page that is returned. |
|PageSize|String|5|The number of entries returned on each page. |
|RequestId|String|4C2061B2-3B1B-43BF-A4A4-C53426F479C0|The ID of the request. |
|Resources|Array| |The details of the service. |
|Resource| | | |
|Description|String|CDN|The description of the service. |
|Labels|String|\[\{"groupFlag":true\}\]|The tags of the service. Tags are used to filter services.

 Tags are returned in the following format: `[{"name":"Tag key","value":"Tag value"}, {"name":"Tag key","value":"Tag value"}]`. The following tags are commonly used:

 -   alertUnit: the unit of the metric value in alerts.

If the unit is small, the original metric value may be too large. In this case, you can use the `alertUnit` tag to specify an appropriate unit. This tag is used in Cloud Monitor.

-   minAlertPeriod: the minimum time interval to report a new alert. The interval is usually set to 1 minute.
-   metricCategory: the specification of the service. Example: kvstore\_sharding.

An Alibaba Cloud service may have different specifications that are defined in the same namespace. You can use this parameter to distinguish between service specifications.

-   is\_alarm: specifies whether an alert rule can be set.

We recommend that you do not use the special tags in the Cloud Monitor console. |
|Namespace|String|acs\_cdn|The namespace of the service. Format: `acs_Service name abbreviation`. For more information about namespaces, see [Appendix 1: Metrics](~~163515~~). |
|Success|Boolean|true|Indicates whether the request was successful. The value true indicates success. The value false indicates failure. |
|Total|String|12|The total number of records. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeProjectMeta
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeProjectMeta>
		  <PageNumber>1</PageNumber>
		  <PageSize>5</PageSize>
		  <RequestId>4C2061B2-3B1B-43BF-A4A4-C53426F479C0</RequestId>
		  <Success>true</Success>
		  <Code>200</Code>
		  <Total>12</Total>
		  <Resources>
			    <Resource>
				      <Description>AnalyticDB</Description>
				      <Labels>[{"name":"product","value":"ADS"},{"name":"productCategory","value":"ads"},{"name":"groupFlag","value":"true"}]</Labels>
				      <Namespace>acs_ads</Namespace>
			    </Resource>
			    <Resource>
				      <Description>Artificial Intelligence Recommendation</Description>
				      <Labels>[{"name":"product","value":"AIRec"},{"name":"productCategory","value":"airec"},{"name":"groupFlag","value":"true"}]</Labels>
				      <Namespace>acs_airec</Namespace>
			    </Resource>
			    <Resource>
				      <Description>API Gateway</Description>
				      <Labels>[{"name":"product","value":"APIGateway"},{"name":"productCategory","value":"apigateway"},{"name":"groupFlag","value":"true"}]</Labels>
				      <Namespace>acs_apigateway_dashboard</Namespace>
			    </Resource>
			    <Resource>
				      <Description>CDN</Description>
				      <Labels>[{"name":"product","value":"CDN"},{"name":"productCategory","value":"cdn"},{"name":"groupFlag","value":"true"}]</Labels>
				      <Namespace>acs_cdn</Namespace>
			    </Resource>
			    <Resource>
				      <Description>Cloud Enterprise Network</Description>
				      <Labels>[{"name":"product","value":"CEN"},{"name":"productCategory","value":"cen,cen_flow,cen_vbr"},{"name":"groupFlag","value":"true"}]</Labels>
				      <Namespace>acs_cen</Namespace>
			    </Resource>
		  </Resources>
</DescribeProjectMeta>
```

`JSON` format

```
{
  "PageNumber": 1,
  "PageSize": 5,
  "RequestId": "4C2061B2-3B1B-43BF-A4A4-C53426F479C0",
  "Success": true,
  "Code": 200,
  "Total": 12,
  "Resources": {
    "Resource": [
      {
        "Description": "AnalyticDB",
        "Labels": "[{\"name\":\"product\",\"value\":\"ADS\"},{\"name\":\"productCategory\",\"value\":\"ads\"},{\"name\":\"groupFlag\",\"value\":\"true\"}]",
        "Namespace": "acs_ads"
      },
      {
        "Description": "Artificial Intelligence Recommendation",
        "Labels": "[{\"name\":\"product\",\"value\":\"AIRec\"},{\"name\":\"productCategory\",\"value\":\"airec\"},{\"name\":\"groupFlag\",\"value\":\"true\"}]",
        "Namespace": "acs_airec"
      },
      {
        "Description": "API Gateway",
        "Labels": "[{\"name\":\"product\",\"value\":\"APIGateway\"},{\"name\":\"productCategory\",\"value\":\"apigateway\"},{\"name\":\"groupFlag\",\"value\":\"true\"}]",
        "Namespace": "acs_apigateway_dashboard"
      },
      {
        "Description": "CDN",
        "Labels": "[{\"name\":\"product\",\"value\":\"CDN\"},{\"name\":\"productCategory\",\"value\":\"cdn\"},{\"name\":\"groupFlag\",\"value\":\"true\"}]",
        "Namespace": "acs_cdn"
      },
      {
        "Description": "Cloud Enterprise Network",
        "Labels": "[{\"name\":\"product\",\"value\":\"CEN\"},{\"name\":\"productCategory\",\"value\":\"cen,cen_flow,cen_vbr\"},{\"name\":\"groupFlag\",\"value\":\"true\"}]",
        "Namespace": "acs_cen"
      }
    ]
  }
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

