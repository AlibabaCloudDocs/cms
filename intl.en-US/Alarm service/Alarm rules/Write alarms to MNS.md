# Write alarms to MNS

This topic describes how to write a threshold alarm to Message Service \(MNS\).

## Procedure

1.  To authorize CloudMonitor to write an alarm to MNS, click [Cloud Resource Access Authorization](https://ram.console.aliyun.com/#/role/authorize?request=%7B%22Requests%22:%20%7B%22request1%22:%20%7B%22RoleName%22:%20%22AliyunCloudMonitorDefaultRole%22,%20%22TemplateId%22:%20%22DefaultRole%22%7D%7D,%20%22ReturnUrl%22:%20%22http:%2F%2Fcms.console.aliyun.com%2F%23%2Feventsubscription%2Ffault%22,%20%22Service%22:%20%22CloudMonitor%22%7D).
2.  Start the OpenAPI Explorer service, and call the [PutResourceMetricRule](https://api.aliyun.com/#/?product=Cms&api=PutResourceMetricRule) operation to create an alarm rule.
3.  Call the [PutMetricRuleTargets](https://api.aliyun.com/#/?product=Cms&api=PutMetricRuleTargets) operation to create an alarm for the specified alarm rule, and set corresponding MNS parameters.

    ARN: specifies the target MNS queue in the format of `"acs:mns:{$RegionId}:{$UserId}:/queues/{$queueName}/messages"`, or specifies the target MNS topic in the format of `"acs:mns:{$RegionId}:{$UserId}:/topics/{$queueName}/messages"`.


The following example shows parameters of PutMetricRuleTargets:

```
RuleId:"db17-4afc-b11a-568512d5a1f9",
Targets:[{
    Id: 1,
    Arn:"acs:mns:{$RegionId}:{$UserId}:/queues/{$queueName}/messages",
    Level: ["INFO", "WARN", "CRITICAL"],
}]
```

## Message body written to MNS

CloudMonitor writes a message body to MNS in the JSON string format. When MNS consumes the message body, your client parses the message structure as a JSON string as follows:

```
{
  "ruleId": "putNewAlarm_group_778af9ba-a291-46ab-ac53-3983bcee****",
  "ruleName": "test",
  //Current level.
  "curLevel": "WARN",
  //Previous level.
  "preLevel": "OK",
  //The instance that triggers the alarm.
  "resources": "{\"instanceId\": \"i-uf61rfofjd2iku7e****\"}",
  //The condition that triggers the alarm.
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
    //Compare some metrics with those in the previous month and those in the same period of the previous year.--Start.
    "AliyunCmsPrevValues": { //Compared values.
      "timestamp": 1534649760000,
      "userId": "127067667954****",
      "instanceId": "i-uf61rfofjd2iku7e****",
      "Average": 468463616,
      "Maximum": 468549632,
      "Minimum": 468258816
    },
    //Comparison formula.
    "AliyunCmsComplexExpression": "100.0 * ($Average-$$prevAverage)/$$prevAverage",
    //Conversion formula.
    "AliyunCmsComplexMath": "100.0 * (470687744-468463616)/468463616",
    //Calculation result.
    "AliyunCmsComplexValue": 0.47477070236336133
    //Compare some metrics with those in the previous month and those in the same period last year.--End.
  },
  //Metric parameters.
  "metricName": "memory_actualusedspace#60",
  "namespace": "acs_ecs_dashboard",
  "period": "60",

  //Application group parameters.
  "groupBy": "group",
  "productGroupName": "RDS instance group",
  "groupId":"123456",

  //Alarm time
  "lastTime": 327362743, //The duration of the alarm.
  "time": 1534736160000, //The time when the data occurred.

  "userId": "173651113438****",
  "eventName": "AlertOk",
  "eventType": "Alert",
  //Use the following parameters to trace the alarm.
  "batchId": "4272653-152082****-0",
  "version": "1.0"
}
```

