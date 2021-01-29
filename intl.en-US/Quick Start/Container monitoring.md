# Container monitoring

Cloud Monitor provides the container monitoring feature. This feature provides an overview of Container Service for Kubernetes \(ACK\) clusters and monitoring data of nodes, namespaces, and workloads of ACK clusters. This feature allows you to track the status of ACK clusters. This feature also allows you to configure alert rules for ACK clusters, nodes, and pods. When an alert is triggered, Cloud Monitor sends an alert notification. This way, you are immediately notified of exceptions and can handle the exceptions as early as possible.

ACK is activated and a cluster is created. For more information, see [Use ACK for the first time](/intl.en-US/Quick Start/Use ACK for the first time.md).

Before Cloud Monitor can monitor ACK clusters, you must update the metrics-server component of the clusters to V0.3.8 or later. For more information, see [Install the metrics-server component](/intl.en-US/User Guide for Kubernetes Clusters/Cluster management/Upgrade cluster/Install the metrics-server component.md).

## Cluster overview

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Container Service Monitoring**.

3.  On the Container Service Monitoring page, find the cluster that you want to view and click the cluster name or **View the Detail**.

4.  The Cluster overview page appears. You can view the basic information and monitoring data of the cluster.

    -   On the Overview tab, you can view the running status of pods and nodes. You can also view the CPU utilization and memory usage of top pods and nodes.
    -   On the Cluster Monitoring Chart tab, you can view the monitoring charts of all metrics of the cluster in the specified time range.

## Node monitoring data

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Container Service Monitoring**.

3.  On the Container Service Monitoring page, find the cluster that you want to view and click the cluster name or **View the Detail**.

4.  In the left-side navigation pane, click **Node**.

5.  On the Node page, find the node that you want to view and click the node ID or **View the Detail**.

6.  On the Monitoring Charts tab, you can view the monitoring charts of all metrics of the node in the specified time range.


## Namespace monitoring data

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Container Service Monitoring**.

3.  On the Container Service Monitoring page, find the cluster that you want to view and click the cluster name or **View the Detail**.

4.  In the left-side navigation pane, click **Namespace**.

5.  On the Namespace page, find the namespace that you want to view and click the namespace name or **View the Detail**.

6.  On the Monitoring Charts tab, you can view the running status of pods and the monitoring charts of CPU utilization and memory usage of top pods in the specified time range.


## Workload monitoring data

1.  Log on to the [Cloud Monitor console](https://cms-intl.console.aliyun.com).

2.  In the left-side navigation pane, click **Container Service Monitoring**.

3.  On the Container Service Monitoring page, find the cluster that you want to view and click the cluster name or **View the Detail**.

4.  In the left-side navigation pane, click **Workload**.

5.  On the Workload page, you can view the monitoring charts of applications and pods. You can also view the CPU utilization and memory usage of top pods.

    -   On the **Stateless**, **Stateful**, **Daemon set**, **Scheduled Tasks**, or **Task** tab, find the application that you want to view. Then, click the application name or click **View the Detail** in the **Actions** column. On the page that appears, you can view the monitoring chart, the list of pods, and the hot spots of pods of the application.
    -   On the **Container Group** tab, find the pod that you want to view. Then, click the pod name or click **View the Detail** in the **Actions** column. On the page that appears, you can view the monitoring charts of all pods in the workload.
6.  On the Stateless tab of the Workload page, find the workload that you want to view and click the workload name or **View the Detail**.

    You can view the CPU utilization and memory usage of workloads on the **Stateless**, **Stateful**, **Daemon set**, **Scheduled Tasks**, **Task**, and **Container Group** tabs.

7.  On the **Deployment Application**, **Container group list**, and **Container group hotspot** tabs, you can view the basic information and monitoring charts of the workload.


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


