# Manage availability monitoring tasks

Based on the availability monitoring task that you configure, Cloud Monitor periodically checks whether the path or port of a local or remote service responds. Cloud Monitor sends an alert notification if the connection times out or an error status code is received. This way, you can monitor the availability of a local or remote service. You are notified immediately when the service becomes unavailable.

## View availability monitoring tasks

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).
2.  In the left-side navigation pane, click **Application Groups**.
3.  On the **Application grouping** tab of the Application Groups page, click the name or ID of the application group for which you want to view availability monitoring tasks. The details page of the application group appears.
4.  In the left-side navigation pane, click **Availability Monitoring**. On the page that appears, you can view all availability monitoring tasks of the application group.

## View availability monitoring results

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).
2.  In the left-side navigation pane, click **Application Groups**.
3.  On the **Application grouping** tab of the Application Groups page, click the name or ID of the application group for which you want to view availability monitoring results. The details page of the application group appears.
4.  In the left-side navigation pane, click **Availability Monitoring**.
5.  On the page that appears, view the monitoring results in the task list.
    -   If no alerts are generated for a task, the number of unhealthy hosts or agents is 0.
    -   If an alert is generated for a task, the number of unhealthy hosts or agents is displayed. You can click the number to view the details about unhealthy hosts and agents.
    -   The following figure shows an example of the details about unhealthy hosts and agents.

## Modify an availability monitoring task

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).
2.  In the left-side navigation pane, click **Application Groups**.
3.  On the **Application grouping** tab of the Application Groups page, click the name or ID of the application group for which you want to modify an availability monitoring task. The details page of the application group appears.
4.  In the left-side navigation pane, click **Availability Monitoring**.
5.  On the page that appears, find the task that you want to modify and click **Modify** in the Actions column. The ModifyAvailability Monitoring dialog box appears.
6.  Modify the task and click **OK**.

## View alert logs

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).
2.  In the left-side navigation pane, click **Application Groups**.
3.  On the **Application grouping** tab of the Application Groups page, click the name or ID of the application group for which you want to view alert logs. The details page of the application group appears.
4.  In the left-side navigation pane, click **Alert Logs**. On the page that appears, you can view the alert logs of the application group.

## Enable or disable an availability monitoring task

You can enable or disable an availability monitoring task for an application group. After you disable a task, Cloud Monitor stops monitoring the application group or reporting alerts based on the task. After you enable the task again, Cloud Monitor resumes the monitoring and reports alerts if an alert rule is met.

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).
2.  In the left-side navigation pane, click **Application Groups**.
3.  On the **Application grouping** tab of the Application Groups page, click the name or ID of the application group for which you want to enable or disable an availability monitoring task. The details page of the application group appears.
4.  In the left-side navigation pane, click **Availability Monitoring**.
5.  On the page that appears, find the task that you want to enable or disable and click **Enable** or **Disable** in the Actions column.

