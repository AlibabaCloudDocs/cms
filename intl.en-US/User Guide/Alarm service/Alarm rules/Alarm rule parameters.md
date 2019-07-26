# Alarm rule parameters {#concept_270434 .concept}

This topic describes parameters of a threshold alarm rule.

## Parameters {#section_qw0_so5_x63 .section}

-   **Product**: the monitored service, such as ECS, ApsaraDB for RDS, and Object Storage Service \(OSS\).
-   **Resource Range**: the scope of the alarm rule. Valid values: **All Resources** and **Instances**.

    **Note:** If you set **Resource Range** to **All Resources**, the alarm rule is applicable to 1,000 instances or fewer. If the number of monitored resources is more than 1,000, you may not receive alarms when the specified metric reaches the threshold. We recommend that you add resources to service-specific application groups before creating the alarm rule. To create a threshold alarm rule for a group, go to the Group Instances page, and click **Threshold alarm**.

    -   **All Resources**: specifies that the alarm rule is applicable to all your instances of the specified service. The system sends alarm notifications if any metric of these instances reaches the specified threshold.
    -   **Instances**: specifies that the alarm rule is applicable to a specified instance. The system sends alarm notifications if any metric of the instance reaches the specified threshold.
-   **Alarm Rule**: the name of the alarm rule.
-   **Rule Description**: the content of the alarm rule. This parameter defines the metric conditions that cause alarms.

    **Alarm rule example**: in host monitoring, a data point on the metric of a single host is reported at a 15-second interval. Therefore, 20 data points are reported in 5 minutes.

    -   Average CPU usage in a 5-minute cycle greater than 90% in three consecutive cycles: specifies that the average value of the 20 data points on CPU usage reported in a 5-minute cycle is greater than 90% in three consecutive cycles. The system sends alarm notifications if the specified metric reaches the threshold.
    -   CPU usage in a 5-minute cycle always greater than 90% in three consecutive cycles: specifies that the values of the 20 data points on CPU usage reported in a 5-minute cycle are greater than 90% in three consecutive cycles. The system sends alarm notifications if the specified metric reaches the threshold.
    -   CPU usage in a 5-minute cycle greater than 90% for once in three consecutive cycles: specifies that the value of at least one of the 20 data points on CPU usage reported in a 5-minute cycle is greater than 90% in three consecutive cycles. The system sends alarm notifications if the specified metric reaches the threshold.
    -   Total public network outbound traffic in a 5-minute cycle greater than 50 MB/s in three consecutive cycles: specifies that the sum of the values of the 20 data points on public network outbound traffic reported in a 5-minute cycle is greater than 50 MB/s in three consecutive cycles. The system sends alarm notifications if the specified metric reaches the threshold.
-   **Mute For**: CloudMonitor sends an alarm notification only after detecting the specified exceptions consecutively for specified times. The minimum value is 5 minutes and the maximum value is 24 hours.
-   **Effective Period**: the period when an alarm rule is effective. The system only sends alarm notifications within the effective period according to the alarm rule. The system only records alarms if the alarms occur during a non-effective period.
-   **Notification Contact**: the contact group that CloudMonitor sends alarm notifications to.
-   **Alarm Levels**: specifies the alarm severity level that corresponds to a specified notification method. Valid values: CRITICAL, WARN, and INFO.
    -   INFO: sends alarm notifications by means of emails and DingTalk ChatBot.
-   **Auto Scaling**: an alarm triggers the corresponding scaling rule after you select Auto Scaling and configure the rule.
-   **Email Remark**: custom supplementary information of an alarm email. CloudMonitor sends the remarks along with the alarm email.
-   **HTTP CallBack**: CloudMonitor uses a POST request to push an alarm to the public URL address you provided. This callback supports HTTP-based requests.

