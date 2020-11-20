# View an application group

You can view the resources, dashboards, fault list, alert history, and alert rules of an application group. You can also perform operations based on the monitoring data. The application group provides centralized resource management that allows you to receive alert notifications and handle faults at the earliest opportunity if a resource fault occurs.

An application group is created. For more information, see [Create an application group](/intl.en-US/Application groups/Create an application group.md).

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Application Groups**.

3.  On the Application grouping tab of the **Application Groups** page, click the group name or ID in the **Group Name / Group ID** column.

    On the **group resource** page, you can view the basic information of the group and the health status of the instances in the group.

4.  In the left-side navigation pane, click **Dashboards**, **Fault List**, **Event Monitor**, **Availability Monitoring**, **Group Process**, **Log Monitoring**, **Custom Monitoring**, **Alert Logs**, or **Alert Rule** to view the monitoring data based on your business requirements.

    -   **Dashboards**

        On this page, you can view the monitoring details of resources in the application group. By default, the page displays the monitoring data of the metrics that are frequently used in Cloud Monitor. If you need to view more monitoring data or change the display mode of charts, you can change the chart type or customize charts.

        To view more monitoring data, you can click **Add Monitoring Chart** on the CustomChart tab to add more charts.

        **Note:** If you need to monitor the metrics for Elastic Compute Service \(ECS\) instances, install the Cloud Monitor agent on the ECS instances. For more information, see [Install and uninstall the Cloud Monitor agent](/intl.en-US/Host monitoring/Cloud Monitor agent/Install and uninstall the Cloud Monitor agent.md).

    -   **Fault List**

        On this page, you can view all the resources with active alerts in the application group. This allows you to get an overview of all unhealthy instances and handle faults at the earliest opportunity.

        **Note:**

        -   If multiple metrics of a resource trigger alerts, the Fault List page displays multiple entries for the resource. Each entry in the list indicates a metric of a resource that triggers alerts.
        -   If you disable an alert rule with active alerts, the entries for the resources to which the alert rule is applied are no longer displayed on the page.
    -   **Event Monitor**

        On this page, you can view system events and custom events in the application group, and create, delete, or modify alert rules for events. You can view the events that are reported in the last 90 days.

    -   **Availability Monitoring**

        On this page, you can view, create, modify, delete, enable, and disable availability monitoring tasks in the application group.

    -   **Group Process**

        On this page, you can view, create, modify, and delete processes in the application group.

    -   **Log Monitoring**

        On this page, you can view, create, modify, or delete log monitoring metrics in the application group.

    -   **Custom Monitoring**

        On this page, you can view all custom monitoring records in the application group and create or delete alert rules.

    -   **Alert Logs**

        On this page, you can view all alerts triggered based on alert rules of the application group.

    -   **Alert Rule**

        On this page, you can view, disable, enable, and modify alert rules of the application group.


