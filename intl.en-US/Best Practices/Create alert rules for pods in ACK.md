# Create alert rules for pods in ACK

Cloud Monitor provides multiple metrics, such as the CPU utilization, memory usage, and network conditions, to help you monitor the status of Container Service for Kubernetes \(ACK\) clusters. After you create an ACK cluster, Cloud Monitor automatically monitors the cluster. You can log on to the Cloud Monitor console to view the detailed monitoring data. You can configure alert rules for the metrics. If a metric value exceeds the specified threshold, Cloud Monitor sends an alert notification.

-   An ACK cluster is created. For more information, see [Create a managed Kubernetes cluster](/intl.en-US/Quick Start/Basic operations/Create a managed Kubernetes cluster.md).
-   An application group is created for the ACK cluster. For more information, see [Create an application group](/intl.en-US/Application groups/Create an application group.md).
-   An alert contact or alert group is created for the ACK cluster. For more information, see [Create an alert contact or alert group](/intl.en-US/Alarm service/Alert contacts/Create an alert contact or alert group.md).

-   Monitoring data is retained for up to 31 days.
-   You can view the monitoring data for up to 14 consecutive days.

1.  Create an alert template for ACK.

    1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

    2.  In the left-side navigation pane, choose **Alerts** \> **Alert Templates**.

    3.  On the Alert Templates page, click **Create Alert Template** in the upper-right corner.

    4.  In the Create/modify alert templates panel, enter the template name, select **Kubernetes** as the service, and configure alert rules.

    5.  Click **OK**.

2.  Apply the alert template to the application group that is created for your ACK cluster.

    1.  In the Create/modify alert template complete message, click **OK**.

    2.  In the Apply Template to Group dialog box, select the application group and set the Muted, Effective Period, HTTP CallBack, and Option parameters.

    3.  Click **OK**.

    4.  In the Apply Template to Group message, click **OK**.


-   If you need to send alert notifications for different ACK clusters to different alert groups, you must modify the alert group associated with each application group.

    For more information, see [Modify an application group](/intl.en-US/Application groups/Modify an application group.md).

-   You can call an API operation to modify alert groups for multiple application groups at a time.

    Log on to [OpenAPI Explorer](https://api.aliyun.com) and call the PutContactGroup operation to modify the alert groups.

    For more information about how to set the parameters of the PutContactGroup operation, see [PutContactGroup](/intl.en-US/API Reference/Alert groups/PutContactGroup.md).


