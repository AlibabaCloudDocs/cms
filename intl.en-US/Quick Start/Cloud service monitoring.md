# Cloud service monitoring

Cloud Monitor automatically retrieves cloud service resources under the current Alibaba Cloud account. You can view the monitoring chart of cloud services to check the running status of resources. You can also configure alert rules to monitor the running status of resources. When an alert is triggered, Cloud Monitor automatically sends an alert notification. This allows you to obtain the running status of your resources in a timely manner.

The monitoring data that is displayed on the monitoring page varies with cloud services. For example, on the monitoring page of Server Load Balancer \(SLB\), you can view the instance list and monitoring chart. You can also configure alert rules.

## View monitoring data

On the monitoring page of a cloud service, you can view the status of resources and the usage of metrics.

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Cloud products**.

3.  On the Cloud products page, click the required cloud service.

4.  On the monitoring page of the cloud service, find the resource that you want to manage. Click **Monitoring Chart** in the **Actions** column.

    You can view the monitoring chart of the resource.

    **Note:**

    -   Monitoring data is retained for up to 31 days.
    -   You can view the monitoring data for up to 14 consecutive days.

## Configure alert rules

On the monitoring page of a cloud service, you can configure alert rules for resources. When an alert is triggered, Cloud Monitor automatically sends an alert notification.

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Cloud products**.

3.  On the Cloud products page, click the required cloud service.

4.  Create an alert rule for the cloud service.

    -   Create an alert rule on the **Alert Rules** page.
        1.  On the monitoring page of the cloud service, find the resource that you want to manage. Click **Alert Rule** in the **Actions** column.
        2.  On the Alert Rules page, click **Create Alert Rule**.
        3.  On the Create Alert Rule page, configure the alert rule.
        4.  Click **Confirm**.
    -   Create an alert rule on the monitoring page of the cloud service.
        1.  On the monitoring page of the cloud service, click **Create Alert Rule** in the upper-right corner.
        2.  On the Create Alert Rule page, configure the alert rule.
        3.  Click **Confirm**.
    **Note:** For more information about the parameters of an alert rule, see [t111649.md\#](/intl.en-US/Alarm service/Alarm rules/Create a threshold-triggered alert rule.md).


## View alert rules

On the monitoring page of a cloud service, you can view all alert rules for resources.

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Cloud products**.

3.  On the Cloud products page, click the required cloud service.

4.  On the monitoring page of the cloud service, click **Alert Rules** in the upper-right corner.


## References

[Monitoring metrics of cloud services](/intl.en-US/Appendix 1: Metrics/Overview.md)

