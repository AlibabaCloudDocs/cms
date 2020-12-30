# View monitoring data

Cloud Monitor provides the Container Service Monitoring feature. This feature provides an overview of Container Service for Kubernetes \(ACK\) clusters and monitoring data of nodes, namespaces, and workloads of ACK clusters. This feature allows you to track the running status of ACK clusters.

ACK is activated and a cluster is created. For more information, see [Use ACK for the first time](/intl.en-US/Quick Start/Use ACK for the first time.md).

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


