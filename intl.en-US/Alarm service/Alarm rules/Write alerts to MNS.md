# Write alerts to MNS

This topic describes how to write alerts from Cloud Monitor to Message Service \(MNS\).

## Procedure

1.  Authorize Cloud Monitor to write alerts to MNS.

    1.  Click [Cloud Resource Access Authorization](https://ram.console.aliyun.com/#/role/authorize?request=%7B%22Requests%22:%20%7B%22request1%22:%20%7B%22RoleName%22:%20%22AliyunCloudMonitorDefaultRole%22,%20%22TemplateId%22:%20%22DefaultRole%22%7D%7D,%20%22ReturnUrl%22:%20%22http:%2F%2Fcms.console.aliyun.com%2F%23%2Feventsubscription%2Ffault%22,%20%22Service%22:%20%22CloudMonitor%22%7D) to allow Cloud Monitor to assume AliyunCloudMonitorDefaultRole.

    2.  Click **Confirm Authorization Policy**.

2.  Call the PutResourceMetricRule operation to create an alert rule.

    For more information, see [PutResourceMetricRule](/intl.en-US/API Reference/Alert rules for time series metrics/PutResourceMetricRule.md).

3.  Call the PutMetricRuleTargets operation to specify a MNS queue or topic to receive the alert notifications of the specified alert rule.

    For more information, see [PutMetricRuleTargets](/intl.en-US/API Reference/Alert rules for time series metrics/PutMetricRuleTargets.md).

    Set the Arn element to the Alibaba Cloud Resource Name \(ARN\) of an MNS queue or topic to which the alerts are written.

    -   The ARN of an MNS queue is in the format of `"acs:mns:{$RegionId}:{$UserId}:/queues/{$queueName}/messages"`.
    -   The ARN of an MNS topic is in the format of `"acs:mns:{$RegionId}:{$UserId}:/topics/{$queueName}/messages"`.
    The following code shows an example of the PutMetricRuleTargets operation:

    ```
    RuleId:"db17-4afc-b11a-568512d5a1f9",
    Targets:[{
        Id: 1,
        Arn:"acs:mns:{$RegionId}:{$UserId}:/queues/{$queueName}/messages",
        Level: ["INFO", "WARN", "CRITICAL"],
    }]
    ```


## Message body written to MNS

Cloud Monitor writes a message body to MNS in the JSON format. The following code shows an example of a message body in the JSON format:

```
{
  "ruleId": "putNewAlarm_group_778af9ba-a291-46ab-ac53-3983bcee****",
  "ruleName": "test",
  // Current level.
  "curLevel": "WARN",
  // Previous level.
  "preLevel": "OK",
  // The instance that triggers the alert.
  "resources": "{\"instanceId\": \"i-uf61rfofjd2iku7e****\"}",
  // The condition that triggers the alert.
  "escalation": {
    "comparisonOperator": "GreaterThanYesterday",
    "level": 3,
    "statistics": "Average",
    "tag": "WARN",
    "threshold": "0",
    "times": 1
  },
  "metricData": {
    "timestamp": 1534736160000,
    "userId": "127067667954****",
    "instanceId": "i-uf61rfofjd2iku7e****",
    "Average": 470687744,
    "Maximum": 470794240,
    "Minimum": 470556672,
    // Start the comparison of metrics.
    "AliyunCmsPrevValues": { // Compared values.
      "timestamp": 1534649760000,
      "userId": "127067667954****",
      "instanceId": "i-uf61rfofjd2iku7e****",
      "Average": 468463616,
      "Maximum": 468549632,
      "Minimum": 468258816
    },
    // Comparison formula.
    "AliyunCmsComplexExpression": "100.0 * ($Average-$$prevAverage)/$$prevAverage",
    // Conversion formula.
    "AliyunCmsComplexMath": "100.0 * (470687744-468463616)/468463616",
    // Calculation result.
    "AliyunCmsComplexValue": 0.47477070236336133
    // End the comparison of metrics.
  },
  // Metric parameters.
  "metricName": "memory_actualusedspace#60",
  "namespace": "acs_ecs_dashboard",
  "period": "60",

  // Application group parameters.
  "groupBy": "group",
  "productGroupName": "RDS instance group",
  "groupId":"12345",

  // Alert time.
  "lastTime": 327362743, // The duration of the alert.
  "time": 1534736160000, // The time when the alert occurred.

  "userId": "173651113438****",
  "eventName": "AlertOk",
  "eventType": "Alert",
  // Use the following parameters to trace the alert.
  "batchId": "4272653-152082****-0",
  "version": "1.0"
}
```

