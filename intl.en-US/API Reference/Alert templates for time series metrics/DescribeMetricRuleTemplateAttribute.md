# DescribeMetricRuleTemplateAttribute

Queries the details of an alert template.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Cms&api=DescribeMetricRuleTemplateAttribute&type=RPC&version=2019-01-01)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeMetricRuleTemplateAttribute|The operation that you want to perform. Set the value to DescribeMetricRuleTemplateAttribute. |
|Name|String|No|ECS\_Template1|The name of the alert template. You must specify at least one of the Name and TemplateId parameters. |
|TemplateId|String|No|12345|The ID of the alert template. You must specify at least one of the Name and TemplateId parameters. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Code|Integer|200|The HTTP status code.

**Note:** The status code 200 indicates that the call was successful. |
|RequestId|String|C14F2566-B4AC-4C3E-AC7D-0A1D16CF33DE|The ID of the request. |
|Message|String|The Request is not authorization.|The returned message. |
|Resource|Struct|N/A|The details of the alert template. |
|AlertTemplates|Array of AlertTemplate|N/A|The details of alert rules that are generated based on the alert template. |
|AlertTemplate|N/A|N/A|N/A|
|Category|String|ecs|The abbreviation of the service name. |
|Escalations|Struct|N/A|The information about the trigger condition based on the alert level. |
|Critical|Struct|N/A|The condition for triggering critical-level alerts. |
|ComparisonOperator|String|GreaterThanOrEqualToThreshold|The comparison operator of the threshold for critical-level alerts. Valid values:

-   GreaterThanOrEqualToThreshold: greater than or equal to the threshold
-   GreaterThanThreshold: greater than the threshold
-   LessThanOrEqualToThreshold: less than or equal to the threshold
-   LessThanThreshold: less than the threshold
-   NotEqualToThreshold: not equal to the threshold
-   GreaterThanYesterday: greater than the metric value at the same time yesterday
-   LessThanYesterday: less than the metric value at the same time yesterday
-   GreaterThanLastWeek: greater than the metric value at the same time last week
-   LessThanLastWeek: less than the metric value at the same time last week
-   GreaterThanLastPeriod: greater than the metric value in the last monitoring cycle
-   LessThanLastPeriod: less than the metric value in the last monitoring cycle |
|Statistics|String|Average|The statistical aggregation method for critical-level alerts.

The valid values of the Statistics parameter vary based on services. For more information about valid values, see [Appendix 1: Metrics](~~163515~~). |
|Threshold|String|90|The threshold for critical-level alerts. |
|Times|Integer|3|The consecutive number of times for which the metric value is measured before a critical-level alert is triggered. |
|Info|Struct|N/A|The condition for triggering info-level alerts. |
|ComparisonOperator|String|GreaterThanOrEqualToThreshold|The comparison operator of the threshold for info-level alerts. Valid values:

-   GreaterThanOrEqualToThreshold: greater than or equal to the threshold
-   GreaterThanThreshold: greater than the threshold
-   LessThanOrEqualToThreshold: less than or equal to the threshold
-   LessThanThreshold: less than the threshold
-   NotEqualToThreshold: not equal to the threshold
-   GreaterThanYesterday: greater than the metric value at the same time yesterday
-   LessThanYesterday: less than the metric value at the same time yesterday
-   GreaterThanLastWeek: greater than the metric value at the same time last week
-   LessThanLastWeek: less than the metric value at the same time last week
-   GreaterThanLastPeriod: greater than the metric value in the last monitoring cycle
-   LessThanLastPeriod: less than the metric value in the last monitoring cycle |
|Statistics|String|Average|The statistical aggregation method for info-level alerts.

The valid values of the Statistics parameter vary based on services. For more information about valid values, see [Appendix 1: Metrics](~~163515~~). |
|Threshold|String|90|The threshold for info-level alerts. |
|Times|Integer|3|The consecutive number of times for which the metric value is measured before an info-level alert is triggered. |
|Warn|Struct|N/A|The condition for triggering warn-level alerts. |
|ComparisonOperator|String|GreaterThanOrEqualToThreshold|The comparison operator of the threshold for warn-level alerts. Valid values:

-   GreaterThanOrEqualToThreshold: greater than or equal to the threshold
-   GreaterThanThreshold: greater than the threshold
-   LessThanOrEqualToThreshold: less than or equal to the threshold
-   LessThanThreshold: less than the threshold
-   NotEqualToThreshold: not equal to the threshold
-   GreaterThanYesterday: greater than the metric value at the same time yesterday
-   LessThanYesterday: less than the metric value at the same time yesterday
-   GreaterThanLastWeek: greater than the metric value at the same time last week
-   LessThanLastWeek: less than the metric value at the same time last week
-   GreaterThanLastPeriod: greater than the metric value in the last monitoring cycle
-   LessThanLastPeriod: less than the metric value in the last monitoring cycle |
|Statistics|String|Average|The statistical aggregation method for warn-level alerts.

The valid values of the Statistics parameter vary based on services. For more information about valid values, see [Appendix 1: Metrics](~~163515~~). |
|Threshold|String|90|The threshold for warn-level alerts. |
|Times|Integer|3|The consecutive number of times for which the metric value is measured before a warn-level alert is triggered. |
|MetricName|String|cpu\_total|The name of the metric.

The valid values of the MetricName parameter vary based on services. For more information about valid values, see [Appendix 1: Metrics](~~163515~~). |
|Namespace|String|acs\_ecs\_dashboard|The namespace of the service.

The valid values of the Namespace parameter vary based on services. For more information about valid values, see [Appendix 1: Metrics](~~163515~~). |
|RuleName|String|ECS\_Rule1|The name of the alert rule. |
|Selector|String|\{"disk":"/"\}|The dimension of the alert. It is an extended field. |
|Webhook|String|https://api.aliyun.com/test.json|The callback URL to which a request is sent when an alert is triggered. |
|Description|String|ECS alert template|The description of the alert template. |
|Name|String|ECS\_Template1|The name of the alert template. |
|RestVersion|String|0|The version of the alert template. |
|TemplateId|String|12345|The ID of the alert template. |
|Success|Boolean|true|Indicates whether the call was successful. Valid values:

-   true: The call was successful.
-   false: The call failed. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=DescribeMetricRuleTemplateAttribute
&TemplateId=12345
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DescribeMetricRuleTemplateAttributeResponse>
          <Resource>
                <RestVersion>0</RestVersion>
                <Name>nametest</Name>
                <Description>nametestDesc</Description>
                <AlertTemplates>
                      <AlertTemplate>
                            <Category>ecs</Category>
                            <MetricName>cpu_total</MetricName>
                            <Namespace>acs_ecs_dashboard</Namespace>
                            <RuleName>cpu_total</RuleName>
                            <Webhook>https://api.aliyun.com/test.json</Webhook>
                            <Escalations>
                                  <Critical></Critical>
                                  <Info></Info>
                                  <Warn>
                                        <Statistics>Average</Statistics>
                                        <Threshold>90.0</Threshold>
                                        <Times>1</Times>
                                        <ComparisonOperator>GreaterThanOrEqualToThreshold</ComparisonOperator>
                                  </Warn>
                            </Escalations>
                      </AlertTemplate>
                      <AlertTemplate>
                            <Category>rds</Category>
                            <MetricName>AvgLogSize</MetricName>
                            <Namespace>acs_rds_dashboard</Namespace>
                            <RuleName>AvgLogSize</RuleName>
                            <Webhook></Webhook>
                            <Escalations>
                                  <Critical></Critical>
                                  <Info></Info>
                                  <Warn>
                                        <Statistics>Average</Statistics>
                                        <Threshold>12.0</Threshold>
                                        <Times>1</Times>
                                        <ComparisonOperator>GreaterThanOrEqualToThreshold</ComparisonOperator>
                                  </Warn>
                            </Escalations>
                      </AlertTemplate>
                </AlertTemplates>
                <TemplateId>12345</TemplateId>
          </Resource>
          <RequestId>C14F2566-B4AC-4C3E-AC7D-0A1D16CF33DE</RequestId>
          <Success>true</Success>
          <Code>200</Code>
</DescribeMetricRuleTemplateAttributeResponse>
```

`JSON` format

```
{
  "Resource": {
    "RestVersion": 0,
    "Name": "nametest",
    "Description": "nametestDesc",
    "AlertTemplates": {
      "AlertTemplate": [
        {
          "Category": "ecs",
          "MetricName": "cpu_total",
          "Namespace": "acs_ecs_dashboard",
          "RuleName": "cpu_total",
          "Webhook": "https://api.aliyun.com/test.json",
          "Escalations": {
            "Critical": {},
            "Info": {},
            "Warn": {
              "Statistics": "Average",
              "Threshold": "90.0",
              "Times": 1,
              "ComparisonOperator": "GreaterThanOrEqualToThreshold"
            }
          }
        },
        {
          "Category": "rds",
          "MetricName": "AvgLogSize",
          "Namespace": "acs_rds_dashboard",
          "RuleName": "AvgLogSize",
          "Webhook": "",
          "Escalations": {
            "Critical": {},
            "Info": {},
            "Warn": {
              "Statistics": "Average",
              "Threshold": "12.0",
              "Times": 1,
              "ComparisonOperator": "GreaterThanOrEqualToThreshold"
            }
          }
        }
      ]
    },
    "TemplateId": 12345
  },
  "RequestId": "C14F2566-B4AC-4C3E-AC7D-0A1D16CF33DE",
  "Success": true,
  "Code": 200
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Cms).

