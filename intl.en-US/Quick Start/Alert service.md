# Alert service

You can customize alert rules to specify how the alert system checks the monitoring data and when the alert system sends alert notifications. After you set alert rules for important metrics, you can receive alert notifications immediately after exceptions occur and handle the exceptions as early as possible.

-   Alert rules have a 24-hour mute period. During the 24-hour period, the notification is not re-sent for an alert. This prevents the system from sending a large number of repeated alert notifications to you.
-   By default, Cloud Monitor adds your Alibaba Cloud account as an alert contact and automatically creates an alert group for the alert contact.

## Step 1: Create an alert contact

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, choose **Alerts** \> **Alert Contacts**.

3.  On the Alert Contacts tab, click **Create Alert Contact**.

4.  In the Set Alert Contact panel,enter the name, email address, and DingTalk chatbot of the alert contact, and retain the default value **Automatic** for the **Alert Notification Information Language** parameter.

    **Note:** **Automatic** indicates that Cloud Monitor automatically selects the language of alert notifications based on the language that you use to create your Alibaba Cloud account.

5.  Verify the parameters and then click **OK**.

6.  Optional. Activate the email address and phone number of the alert contact.

    By default, the email address and phone number of the alert contact are in the **Pending Activation** state. After the alert contact receives an email and text message that contain the activation links, the alert contact must activate the email address and phone number within 24 hours. Otherwise, the alert contact cannot receive alert notifications. After the email address and phone number are activated, they are displayed in the alert contact list.


## Step 2: Create an alert group

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, choose **Alerts** \> **Alert Contacts**.

3.  Click the **Alert Contact Group** tab.

4.  On the Alert Contact Group tab, click **Create Alert Contact Group**.

5.  In the Create Alert Contact Group panel, specify the alert group name and add alert contacts to the alert group.

6.  Click **Confirm**.


## Step 3: Create an alert rule

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
    |**Log Service**|If you select **Log Service**, the alert message is written to Log Service if an alert is generated. You must set the **Region**, **Project**, and **Logstore** parameters.For more information about how to create a project and a Logstore, see [Quick Start](/intl.en-US/Quick Start/Quick Start.md). |
    |**Email Remark**|The custom remarks that you want to include in the alert notification email.|
    |**HTTP CallBack**|The callback URL that can be accessed over the Internet. Cloud Monitor sends a POST request to push an alert message to the specified callback URL. Only HTTP requests are supported.|

5.  Click **Confirm**.


