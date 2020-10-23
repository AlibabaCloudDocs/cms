# Add a monitoring chart

This topic describes how to add a monitoring chart to a dashboard to display more monitoring data.

## Background information

Cloud Monitor provides a default dashboard that displays specific monitoring data for Elastic Compute Service \(ECS\). To view more monitoring data related to your ECS instances, you can add monitoring charts to the dashboard.

If the default dashboard for ECS cannot meet your requirements on service monitoring, you can create dashboards and add monitoring charts as needed.

## Before you begin

To add a monitoring chart to a custom dashboard, you must first create the custom dashboard.

Cloud Monitor allows you to add the following monitoring charts to a dashboard:

-   **Line chart**: displays monitoring data of the time series type. You can add multiple metrics to a line chart.
-   **Area chart**: displays monitoring data of the time series type. You can add multiple metrics to an area chart.
-   **Table**: displays the latest monitoring data in the last 3 hours in ascending or descending order. A table can display up to 1,000 data records. For example, you can use a table to display the CPU utilization of all ECS instances in an application group in descending order. You can add only one metric to a table.
-   **Heat map**: displays the real-time monitoring data of a specific metric. A heat map is used to show the distribution and comparison of real-time monitoring data of a specific metric for multiple instances. For example, you can use a heat map to display the distribution of the CPU utilization for multiple instances. You can add only one metric to a heat map.
-   **Pie chart**: displays real-time monitoring data of a specific metric. A pie chart is often used for data comparison. You can add only one metric to a pie chart.

## Add a monitoring chart

**Usage notes**

**Note:**

-   The default dashboard for ECS displays the following monitoring charts: CPU Usage, Network Inbound Bandwidth, Network Outbound Bandwidth, Disk BPS, Disk IOPS, Network Inbound Traffic, and Network Outbound Traffic.
-   You can add up to 20 charts to a dashboard.
-   A line chart can display up to 10 lines.
-   An area chart can display up to 10 areas.
-   A table can display up to 1,000 data records.
-   A heat map can display up to 1,000 color blocks.

**Procedure**

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).
2.  In the left-side navigation pane, choose **Dashboard** \> **Custom Dashboard**.
3.  On the page that appears, select the dashboard to which you want to add monitoring charts from the **Dashboards** drop-down list. On the dashboard, click **Add View** in the upper-right corner. The Add View panel appears.
4.  In the **Chart Type** section, select Line, Area, Table, Heat Map, or Pie Chart.
5.  In the **Select Metrics** section, select metrics. You can select cloud service metrics, log monitoring metrics, or custom metrics. For example, click the Dashboards tab, select an Alibaba Cloud service, enter a name for the chart, and then select the metrics and statistical methods as needed.

    -   Select the metric that you want to view.
    -   Select the statistical method used to aggregate the metric data. Valid values: Maximum Value, Minimum Value, or Average.
    To add more metrics, click **AddMetrics**.

6.  Click **Save**. The monitoring chart is displayed on the dashboard.
7.  Optional. Drag the right border, lower border, or lower-right corner of the monitoring chart to resize the chart.

**GUI elements in the Select Metrics section**

-   **Dashboards**: the metrics of Alibaba Cloud services.
-   **Log Monitoring**: the metrics that you add by using the log monitoring feature.
-   **Custom**: the metrics that you add by using the custom monitoring feature.
-   **Metrics**: the name of the metric, such as CPU utilization and memory usage.
-   Statistical method: the method used to aggregate metric data in a statistical period. Valid values: Maximum Value, Minimum Value, or Average.
-   **Resource**: the application group or instance for which you want to display monitoring data.

