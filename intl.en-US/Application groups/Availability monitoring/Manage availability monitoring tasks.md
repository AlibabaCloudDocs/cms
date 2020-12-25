# Manage availability monitoring tasks

You can configure availability monitoring to periodically check whether a specified local or remote path or port responds. Cloud Monitor sends an alert notification if the response times out or an error status code is received. This way, you are immediately notified when a local or remote service stops responding.

A site monitoring task is created. For more information, see [Create a site monitoring task](/intl.en-US/Site Monitoring/Create a site monitoring task.md).

## View availability monitoring results

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Application Groups**.

3.  On the **Application grouping** tab, click the name or ID of the application group that you want to manage.

4.  In the left-side navigation pane of the page that appears, click **Availability Monitoring**.

5.  View availability monitoring results.

    -   If no alerts are generated for a monitoring task, the number of unhealthy hosts is 0 in the task list.
    -   If an alert is generated for a task, the number of unhealthy hosts or agents is displayed in the task list. You can click the number to view details about unhealthy hosts.

## View availability monitoring charts

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Application Groups**.

3.  On the **Application grouping** tab, click the name or ID of the application group that you want to manage.

4.  In the left-side navigation pane of the page that appears, click **Availability Monitoring**.

5.  Find the monitoring task that you want to view and click **Monitoring Charts** in the **Actions** column.

6.  View the monitoring charts of the monitoring task.


## Modify an availability monitoring task

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Application Groups**.

3.  On the **Application grouping** tab, click the name or ID of the application group that you want to manage.

4.  In the left-side navigation pane of the page that appears, click **Availability Monitoring**.

5.  Find the monitoring task that you want to modify and click **Modify** in the **Actions** column.

6.  In the ModifyAvailability Monitoring dialog box, set relevant parameters of the availability monitoring task.

7.  Click **OK**.


## Delete an availability monitoring task

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Application Groups**.

3.  On the **Application grouping** tab, click the name or ID of the application group that you want to manage.

4.  In the left-side navigation pane of the page that appears, click **Availability Monitoring**.

5.  Find the monitoring task that you want to delete and click **Delete** in the **Actions** column.

6.  In the BatchDelete message, click **OK**.


## Disable an availability monitoring task

**Note:** You can disable only availability monitoring tasks that are in the Enable state.

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Application Groups**.

3.  On the **Application grouping** tab, click the name or ID of the application group that you want to manage.

4.  In the left-side navigation pane of the page that appears, click **Availability Monitoring**.

5.  Find the monitoring task that you want to disable and click **Disable** in the **Actions** column.

6.  In the BatchDisable message, click **OK**.


## Enable an availability monitoring task

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Application Groups**.

3.  On the **Application grouping** tab, click the name or ID of the application group that you want to manage.

4.  In the left-side navigation pane of the page that appears, click **Availability Monitoring**.

5.  Find the monitoring task that you want to enable and click **Enable** in the **Actions** column.

6.  In the BatchEnable message, click **OK**.


## Related operations

In the list of the availability monitoring tasks for an application group, select the monitoring tasks that you want to manage. Then, click **BatchDelete**, **BatchEnable**, or **BatchDisable** to delete, enable, or disable the monitoring tasks at a time.

