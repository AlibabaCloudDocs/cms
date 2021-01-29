# Manage monitoring charts on a custom dashboard

If you use multiple Alibaba Cloud services, you can add monitoring charts for the metrics of these services to a dashboard. Then, you can view the monitoring data of the services on the dashboard.

A dashboard is created. For more information, see [Create a dashboard](/intl.en-US/Dashboard/Manage a custom dashboard.md).

Cloud Monitor provides a default dashboard that displays monitoring data for Elastic Compute Service \(ECS\). To view the metrics of other Alibaba Cloud services, you can add monitoring charts to the dashboard. You can add a maximum of 20 monitoring charts to a dashboard.

The following table describes the types of monitoring charts that are supported by Cloud Monitor and the limits of each type.

|Type|Description|Limits|
|----|-----------|------|
|Line chart|Displays monitoring data in time series. You can add multiple metrics to a line chart.|Each line chart can display a maximum of 10 lines.|
|Area chart|Displays monitoring data in time series. You can add multiple metrics to an area chart.|Each area chart can display a maximum of 10 areas.|
|Table|Displays the monitoring data of the last 3 hours in ascending or descending order. Each table can display a maximum of 1,000 data records. For example, you can use a table to display the CPU utilization of all ECS instances in descending order. You can add only one metric to a table.|Each table can display a maximum of 1,000 data records.|
|Heat map|Displays the real-time monitoring data of a specific metric. A heat map is used to display the distribution and comparison of real-time monitoring data that is collected for a specific metric of multiple instances. For example, you can use a heat map to display the distribution of the CPU utilization for multiple instances. You can add only one metric to a heat map.|Each heat map can display a maximum of 1,000 color blocks.|
|Pie chart|Displays the real-time monitoring data of a specific metric. A pie chart is used for data comparison. You can add only one metric to a pie chart.|N/A|

## Add a monitoring chart

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, choose **Dashboard** \> **Custom Dashboard**.

3.  Select a dashboard from the **Dashboards** drop-down list.

4.  In the upper-right corner, click **Add View**.

5.  In the Add View panel, select a chart type and metrics.

    |Parameter|Description|
    |---------|-----------|
    |**Chart Type**|Supported types include line charts, area charts, tables, heat maps, and pie charts.|
    |**Select Metrics**|You can select cloud service metrics, log monitoring metrics, or custom metrics.

    -   Dashboards: the metrics of Alibaba Cloud services. For more information, see [Cloud service monitoring](/intl.en-US/.md).
    -   Custom: the metrics that you add by using the custom monitoring feature. For more information, see [Report monitoring data](/intl.en-US/Custom monitoring/Report monitoring data/Overview.md). |

6.  Click **Save**.


## Modify a monitoring chart

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, choose **Dashboard** \> **Custom Dashboard**.

3.  Select a dashboard from the **Dashboards** drop-down list.

4.  Move the pointer over the monitoring chart that you want to modify. Click the ![Settings](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/4407407061/p175261.png) icon in the upper-right corner and then click the ![Edit](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/4407407061/p175262.png) icon.

5.  In the Add View panel, modify the type and metrics of the chart.

6.  Click **Save**.


## Delete a monitoring chart

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, choose **Dashboard** \> **Custom Dashboard**.

3.  Select a dashboard from the **Dashboards** drop-down list.

4.  Move the pointer over the monitoring chart that you want to delete. Click the ![Settings](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/4407407061/p175261.png) icon in the upper-right corner and then click the ![Delete](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/5407407061/p175266.png) icon.

5.  In the Confirm message, click **Confirm**.


## View monitoring charts

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, choose **Dashboard** \> **Custom Dashboard**.

3.  Select a dashboard from the **Dashboards** drop-down list.

4.  Select the time range to display monitoring data on the monitoring charts.

    **Note:** You can query only the monitoring data of the last 30 days.

5.  View the monitoring charts.

    -   Click **Full Screen** in the upper-right corner. You can view all the monitoring charts on the dashboard in full-screen mode.
    -   Click **Refresh** in the upper-right corner. You can refresh all monitoring charts on the dashboard in real time.

