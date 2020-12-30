# Manage alert rules

You can create alert rules for Container Service for Kubernetes \(ACK\) clusters, nodes, and pods. When an alert is triggered based on alert rules, Cloud Monitor sends an alert notification. This way, you are immediately notified of exceptions and can handle the exceptions at the earliest opportunity. This topic describes how to create, view, modify, delete, enable, and disable alert rules.

ACK is activated and a cluster is created. For more information, see [Use ACK for the first time](/intl.en-US/Quick Start/Use ACK for the first time.md).

## Create an alert rule

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Container Service Monitoring**.

3.  On the Container Service Monitoring page, find the cluster for which you want to create an alert rule and click **View Alert Rules** in the **Actions** column.

4.  On the Alert Rules page, click **Create Alert Rule**.

5.  In the Create Alert Rule panel, configure the parameters.

    |Parameter|Description|
    |---------|-----------|
    |**Resource Range**|The resources to which the alert rule is applied. Valid values:    -   **Cluster**: The alert rule is applied to the cluster.
    -   **Node**: The alert rule is applied to all nodes or specified nodes in the cluster.
    -   **Container Group \(pod\)**: The alert rule is applied to all pods or specified pods in the specified application under the specified namespace of the cluster. |
    |**Rule Description**|The content of the alert rule. The parameters in this section specify the conditions that trigger an alert.|
    |**Effective Time**|The interval at which new alert notifications are sent if the alert is not cleared.|
    |**Effective From**|The time period during which the alert rule is effective. Cloud Monitor checks whether monitoring data meets the alert rule only during the effective period.|
    |**HTTP Callback**|Cloud Monitor sends a POST request to push an alert to the specified callback URL. Only HTTP requests are supported.**Note:** We recommend that you specify a callback URL that can be accessed over the Internet. |
    |**Alert Contact Group**|The alert group that receives alert notifications.|

6.  Click **OK**.


## View an alert rule

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Container Service Monitoring**.

3.  On the Container Service Monitoring page, find the cluster whose alert rule you want to view and click **View Alert Rules** in the **Actions** column.

4.  On the Alert Rules page, find the alert rule that you want to view and click **Rule Details** or **Alert Logs** in the **Actions** column.

    View the details of the alert rule, alert logs, and faulty resources.


## Modify an alert rule

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Container Service Monitoring**.

3.  On the Container Service Monitoring page, find the cluster for which you want to modify an alert rule and click **View Alert Rules** in the **Actions** column.

4.  On the Alert Rules page, find the alert rule that you want to modify and click **Modify** in the **Actions** column.

5.  In the Modify Alert Rule panel, modify the parameters as required.

6.  Click **OK**.


## Delete an alert rule

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Container Service Monitoring**.

3.  On the Container Service Monitoring page, find the cluster for which you want to delete an alert rule and click **View Alert Rules** in the **Actions** column.

4.  On the Alert Rules page, find the alert rule that you want to delete and click **Delete** in the **Actions** column.

5.  In the Delete Alert message, click **Confirm**.


## Disable an alert rule

**Note:** After you create an alert rule, the alert rule is in the **Enabled** state.

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Container Service Monitoring**.

3.  On the Container Service Monitoring page, find the cluster for which you want to disable an alert rule and click **View Alert Rules** in the **Actions** column.

4.  On the Alert Rules page, find the alert rule that you want to disable and choose **More** \> **Disable** in the **Actions** column.

5.  In the Disable Alert Rule message, click **Confirm**.


## Enable an alert rule

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Container Service Monitoring**.

3.  On the Container Service Monitoring page, find the cluster for which you want to enable an alert rule and click **View Alert Rules** in the **Actions** column.

4.  On the Alert Rules page, find the alert rule that you want to enable and choose **More** \> **Enable** in the **Actions** column.

5.  In the Enable Alert Rule message, click **Confirm**.


