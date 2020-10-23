# Manage dashboards

You can create, modify, and delete a dashboard, and view monitoring data on a dashboard.

## View monitoring data on a dashboard

You can customize the monitoring data that a dashboard displays and view the monitoring data on the dashboard. On a dashboard, you can aggregate monitoring data of different instances that run the same workloads. These instances can belong to different services.

**Note:**

-   Cloud Monitor provides a default dashboard that displays specific monitoring data for Elastic Compute Service \(ECS\).
-   Cloud Monitor can automatically refresh the monitoring data that is generated in the last 1 hour, 3 hours, or 6 hours. You must manually refresh the monitoring data for a time range that exceeds 6 hours.

**Procedure**

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).
2.  In the left-side navigation pane, choose **Dashboard** \> **Custom Dashboard**.
3.  On the Dashboards page, select the dashboard that you want to view from the drop-down list. The Dashboards page displays the dashboard for ECS by default.
4.  Click **Full Screen** in the upper-right corner to view the dashboard in full screen.
5.  In the top bar, select or specify the time range of the monitoring data that you want to view on the dashboard. You can click 1 h, 3 h, 6 h, 12 h, 1days, 3days, 7days, or 14days. Alternatively, you can click the time selection icon to specify the time range. After you select or specify a time range, all monitoring charts on the dashboard display the monitoring data that are generated within the time range.
6.  Turn on or off Auto Refresh as needed. If you click **1 h**, **3 h** or **6 h** and turn on Auto Refresh, Cloud Monitor automatically refreshes monitoring data every minute.
7.  View the monitoring charts on the dashboard. The unit of the metric displayed in a monitoring chart is enclosed in parentheses \(\) next to the title of the chart.
8.  Move the pointer over a point in a monitoring chart. You can view the metric value at the specified time point in each monitoring chart.

## Create a dashboard

If the default dashboard for ECS cannot meet your requirements on service monitoring, you can create dashboards and add monitoring charts as needed.

**Note:** You can add a maximum of 20 monitoring charts to a dashboard.

**Procedure**

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).
2.  In the left-side navigation pane, choose **Dashboard** \> **Custom Dashboard**.
3.  On the Dashboards page, click **Create Dashboard** in the upper-right corner.
4.  In the Create Dashboard dialog box, enter a name for the dashboard and click **Create**. The Dashboards page displays the created dashboard. You can add monitoring charts to the dashboard as needed.
5.  Move the pointer over the dashboard name and click **Edit** to change the dashboard name.

## Delete a dashboard

You can delete a dashboard that you do not want.

**Note:** If you delete a dashboard, all monitoring chart that are added to the dashboard are deleted.

**Procedure**

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).
2.  In the left-side navigation pane, choose **Dashboard** \> **Custom Dashboard**.
3.  On the Dashboards page, select the dashboard that you want to delete from the Dashboards drop-down list. After the dashboard is displayed, click **Delete Dashboard** in the upper-right corner.

