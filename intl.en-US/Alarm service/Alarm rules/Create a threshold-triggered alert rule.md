# Create a threshold-triggered alert rule

You can create threshold-triggered alert rules to monitor the usage and operation of cloud service resources. When a metric value reaches the specified threshold, Cloud Monitor sends an alert notification to you. In this way, you can be informed of exceptions and handle them efficiently.

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, choose **Alerts** \> **Alert Rules**.

3.  On the **Threshold Value Alert** tab of the Alert Rules page, click **Create Alert Rule**.

4.  On the Create Alert Rule page, set relevant parameters.

    |Parameter|Description|
    |---------|-----------|
    |**Product**|The name of the service monitored by Cloud Monitor. Example: ECS.|
    |**Resource Range**|The resources to which the alert rule is applied. Valid values:    -   **All Resources**: The alert rule is applied to all your instances of the specified service. Assume that you set the Resource Range parameter to All Resources and the alert threshold for CPU usage of ApsaraDB for MongoDB to 80%. Cloud Monitor sends an alert notification when the CPU usage of an ApsaraDB for MongoDB instance exceeds 80%. If you set the **Resource Range** parameter to **All Resources**, the alert rule is applied to up to 1,000 instances. If the specified service has more than 1,000 instances, you may not receive alert notifications when the value of the specified metric reaches the threshold. We recommend that you add resources to service-specific application groups before you create alert rules.
    -   **Instances**: The alert rule is applied to a specific instance. Assume that you set the Resource Range parameter to Instances and the alert threshold for the CPU usage of an ECS instance to 80%. Cloud Monitor sends an alert notification when the CPU usage of the ECS instance exceeds 80%. |
    |**Alert Rule**|The name of the alert rule.|
    |**Rule Description**|The content of the alert rule. This parameter defines the conditions that trigger an alert. For example, if you set the condition to that the average CPU usage in 5 minutes is greater than or equal to 90%, Cloud Monitor checks whether the condition is met every 5 minutes. Take host monitoring as an example. A data point on the metric of a single host is reported at a 15-second interval. Therefore, 20 data points are reported in 5 minutes. Cloud Monitor checks whether conditions are met based on the following rules:

    -   If the average value of the 20 data points on CPU usage reported in 5 minutes is greater than 90%, the average CPU usage in 5 minutes is greater than 90%.
    -   If the values of all the 20 data points on CPU usage reported in 5 minutes are greater than 90%, the CPU usage in 5 minutes is always greater than 90%.
    -   If the value of at least one of the 20 data points on CPU usage reported in 5 minutes is greater than 90%, the CPU usage in 5 minutes is greater than 90% for once.
    -   If the sum of the values of the 20 data points on outbound traffic over Internet reported in 5 minutes is greater than 50 MB, the total outbound traffic over Internet in 5 minutes is greater than 50 MB. |
    |**Mute for**|The interval of re-sending the notification for an alert before the alert is cleared.|
    |**Effective Period**|The time period during which the alert rule is effective. Cloud Monitor checks whether monitoring data meets the alert rule only during the effective period.|
    |**Notification Contact**|The alert groups to which alert notifications are sent.|
    |**Notification Methods**|Email + DingTalk \(Info\) |
    |**Auto Scaling**|If you set the **Product** parameter to **Auto Scaling**, you must set the **Region**, **ESS Group**, and **ESS Rule** parameters.|
    |**Log Service**|If you set the **Product** parameter to **Log Service**, you must set the **Region**, **Project**, and **Logstore** parameters.|
    |**Email Remark**|Optional. The custom remarks that you want to include in the alert notification email.|
    |**HTTP CallBack**|The callback URL that can be accessed by using the Internet. Cloud Monitor pushes an alert notification to the specified callback URL by sending an HTTP POST request. Only the HTTP protocol is supported.|

5.  Click **OK**.


