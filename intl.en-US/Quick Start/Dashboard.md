# Dashboard

Cloud Monitor provides the dashboard feature. You can customize the monitoring data that a dashboard displays and view the monitoring data on the dashboard.

## Scenario

On a dashboard, you can aggregate monitoring data of different instances that run the same workloads. These instances can belong to different services.

## View monitoring data on a dashboard

You can use a dashboard to display the resource usage of Alibaba Cloud services.

**Note:**

-   Cloud Monitor provides a default dashboard that displays specific monitoring data for Elastic Compute Service \(ECS\).
-   You can add monitoring data of other Alibaba Cloud services to the dashboard.

**Procedure**

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).
2.  In the left-side navigation pane, choose **Dashboard** \> **Custom Dashboard**.
3.  On the **Dashboards** page, select the dashboard that you want to view from the drop-down list. You can switch to another dashboard by selecting the dashboard from the drop-down list.

## Create a dashboard

If the default dashboard for ECS cannot meet your requirements on service monitoring, you can create dashboards and add monitoring charts as needed.

**Procedure**

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).
2.  In the left-side navigation pane, choose **Dashboard** \> **Custom Dashboard**.
3.  On the Dashboards page, click **Create Dashboard** in the upper-right corner.
4.  In the Create Dashboard dialog box, enter a name for the dashboard and click **Create**. The Dashboards page displays the created dashboard. You can add monitoring charts to the dashboard as needed.

## Add a monitoring chart

You can add monitoring charts for metrics of your Alibaba Cloud services and custom metrics.

If you use multiple Alibaba Cloud services, you can add monitoring charts for metrics of these services to a dashboard. Then, you can view the monitoring data of the services on the dashboard.

After you report custom monitoring data to Cloud Monitor by using the Cloud Monitor API, you can add monitoring charts for the custom metrics to a dashboard to display the monitoring data.

**Procedure**

For more information, see [Add a monitoring chart](/intl.en-US/Dashboard/Use dashboards/Add charts.md).

## Delete a dashboard

**Note:**

-   If you delete a dashboard, all monitoring charts that are added to the dashboard are deleted.
-   You cannot restore a dashboard after you delete it.
-   Exercise caution when you delete a dashboard.

**Procedure**

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).
2.  In the left-side navigation pane, choose **Dashboard** \> **Custom Dashboard**.
3.  On the Dashboards page, click **Delete Dashboard** in the upper-right corner to delete the current dashboard.

## Change the name of a dashboard

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).
2.  In the left-side navigation pane, choose **Dashboard** \> **Custom Dashboard**.
3.  On the **Dashboards** page, move the pointer over the dashboard name and click **Edit** that appears. Enter a new name and click **OK**.

