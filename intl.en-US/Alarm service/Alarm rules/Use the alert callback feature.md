# Use the alert callback feature

This topic describes how to use the alert callback feature to send alert notifications to your existing operations and maintenance \(O&M\) or notification system.

-   The callback URL that can be accessed over the Internet is prepared.
-   The URL callback feature is enabled as an alert notification method in your existing O&M or notification system.

**Note:**

-   If an alert callback fails, three retries are performed. Each callback request times out after 5 seconds.
-   Only HTTP callbacks are supported.

Cloud Monitor allows you to report alerts by using emails and DingTalk chatbots. Cloud Monitor also allows you to report alerts by using the alert callback feature. After you enable the alert callback feature, Cloud Monitor can push alert notifications to the specified Internet URL by sending HTTP POST requests. You can take actions based on the received notifications.

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, choose **Alerts** \> **Alert Rules**.

3.  On the **Threshold Value Alert** tab of the Alert Rule page, find the alert rule that you want to modify and click **Modify** in the **Actions** column.

    **Note:** You can also create an alert rule.

4.  Enter the prepared callback URL in the HTTP Callback field.

5.  Click **Confirm**.


If an alert is triggered based on the alert rule, Cloud Monitor sends an HTTP POST request that contains the alert information to the callback URL. The following table describes the parameters of the HTTP POST request.

**Note:** Event alerts do not support the alert callback feature.

|Parameter|Date type|Description|
|---------|---------|-----------|
|alertName|String|The name of the alert.|
|alertState|String|The status of the alert. Valid values: -   OK
-   ALERT
-   INSUFFICIENT\_DATA |
|curValue|String|The value of the metric when the alert was triggered or cleared.|
|dimensions|String|The object for which the alert was triggered. Example: `{userId=12****, instanceId=i-12****}`.|
|expression|String|The conditions that triggered the alert.|
|instanceName|String|The name of the instance.|
|metricName|String|The name of the metric.|
|metricProject|String|The name of the service. For more information about metrics for different services, see [Overview](/intl.en-US/Appendix 1: Metrics/Overview.md).|
|namespace|String|The namespace of the service. The value of this parameter is the same as that of the metricProject parameter.|
|preTriggerLevel|String|The level of the alert that was triggered last time.|
|ruleId|String|The ID of the alert rule based on which the alert was triggered.|
|timestamp|String|The timestamp when the alert was triggered.|
|triggerLevel|String|The level of the alert that was triggered this time.|
|userId|String|The ID of the user.|

Sample POST request

```
Content-Type: application/x-www-form-urlencoded; charset=UTF-8

expression=$Average>=95&metricName=Host.mem.usedutilization&instanceName=instance-name-****&signature=eEq1zHuCUp0XSmLD8p8VtTKF****&metricProject=acs_ecs&userId=12****&curValue=97.39&alertName=Basic monitoring-ECS-memory usage&namespace=acs_ecs&triggerLevel=WARN&alertState=ALERT&preTriggerLevel=WARN&ruleId=applyTemplateee147e59-664f-4033-a1be-e9595746****&dimensions={userId=12****), instanceId=i-12****}&timestamp=1508136760
```

