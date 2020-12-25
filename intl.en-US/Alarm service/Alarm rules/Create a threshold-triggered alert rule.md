# Create a threshold-triggered alert rule

You can create threshold-triggered alert rules to monitor the usage and operating status of cloud service resources. When a metric value reaches the specified threshold, Cloud Monitor sends an alert notification to you. This way, you can be informed of exceptions and handle them efficiently.

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, choose **Alerts** \> **Alert Rules**.

3.  On the **Threshold Value Alert** tab, click **Create Alert Rule**.

4.  On the Create Alert Rule page, set relevant parameters of the alert rule.

    ![Create an alert rule](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/7723688061/p102160.png)

    |Parameter|Description|
    |---------|-----------|
    |**Product**|The name of the service that can be monitored by Cloud Monitor. Example: ECS.|
    |**Resource Range**|The resources to which the alert rule is applied. Valid values:    -   **All Resources**: The alert rule is applied to all your instances of the specified service. Assume that you set the Resource Range parameter to All Resources and the alert threshold for CPU utilization to 80% for ApsaraDB for MongoDB. Cloud Monitor sends an alert notification when the CPU utilization of an ApsaraDB for MongoDB instance exceeds 80%. If you set the **Resource Range** parameter to **All Resources**, the alert rule is applied to up to 1,000 instances. If the specified service has more than 1,000 instances, you may not receive alert notifications when the value of the specified metric reaches the threshold. We recommend that you add resources to service-specific application groups before you create alert rules.
    -   **Instances**: The alert rule is applied to a specific instance. Assume that you set the Resource Range parameter to Instances and the alert threshold for the CPU utilization to 80% for an ECS instance. Cloud Monitor sends an alert notification when the CPU utilization of the ECS instance exceeds 80%. |
    |**Alert Rule**|The name of the alert rule.|
    |**Rule Description**|The content of the alert rule. This parameter defines the conditions that trigger an alert. For example, if you set the condition to that the average CPU utilization in 5 minutes is greater than or equal to 90% for three consecutive cycles, Cloud Monitor checks whether the condition is met every 5 minutes for only three times.|
    |**Mute for**|The interval of re-sending the notification for an alert before the alert is cleared.|
    |**Effective Period**|The time period during which the alert rule is effective. Cloud Monitor checks whether monitoring data meets the alert rule only during the effective period.|
    |**Notification Contact**|The alert groups to which alert notifications are sent.|
    |**Notification Methods**|Set the value to Email + DingTalk \(Info\). |
    |**Auto Scaling**|If you select **Auto Scaling**, the specified scaling rule is triggered if an alert is generated. You must set the **Region**, **ESS Group**, and **ESS Rule** parameters.    -   For more information about how to create a scaling group, see [Create a scaling group](/intl.en-US/Scaling Group/Scaling group/Create a scaling group.md).
    -   For more information about how to create a scaling rule, see [Create a scaling rule](/intl.en-US/Scaling Group/Scaling rule/Create a scaling rule.md). |
    |**Log Service**|If you select **Log Service**, the alert message is written to Log Service if an alert is generated. You must set the **Region**, **Project**, and **Logstore** parameters.For more information about how to create a project and a Logstore, see [Quick start](/intl.en-US/Quick Start/Quick start.md). |
    |**Email Remark**|The custom remarks that you want to include in the alert notification email.|
    |**HTTP CallBack**|The callback URL that can be accessed over the Internet. Cloud Monitor sends a POST request to push an alert message to the specified callback URL. Only HTTP requests are supported.|

5.  Click **Confirm**.


