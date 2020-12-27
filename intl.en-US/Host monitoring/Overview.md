# Overview

Cloud Monitor provides the host monitoring feature to monitor your hosts by using the Cloud Monitor agents that are installed on the hosts. The host monitoring feature allows you to monitor the Elastic Compute Service \(ECS\) instances of Alibaba Cloud. You can also use the host monitoring feature to monitor virtual machines \(VMs\) or physical machines from another vendor. The host monitoring feature supports hosts that run the Linux and Windows operating systems.

## Scenarios

You can use the host monitoring feature to monitor the resource usage of hosts and receive alert notifications if exceptions occur on hosts. Scenarios

-   Monitor hosts in a hybrid cloud

    Host monitoring uses Cloud Monitor agents to collect monitoring data of metrics from your host. You can install the Cloud Monitor agent on both ECS instances and non-ECS hosts. This way, you can collect monitoring data of metrics from the hosts in a hybrid cloud.

-   Monitor hosts of an enterprise

    Host monitoring allows you to group hosts in different regions to an application group for business-based host management. In addition, host monitoring allows you to manage alert rules by application group. After you apply an alert rule to an application group, the alert rule is applied to all hosts in the application group. This improves the O&M efficiency.


## Features

|Feature|Description|
|-------|-----------|
|Easy installation of agents|Collects multiple monitoring data of operating system metrics from your hosts by using the Cloud Monitor agents installed on your hosts. For more information, see [Install and uninstall the Cloud Monitor agent](/intl.en-US/Host monitoring/Cloud Monitor agent/Install and uninstall the Cloud Monitor agent.md).|
|Multiple monitoring metrics|Allows you to monitor metrics of CPU, memory, disk, and network to meet your basic O&M requirements of hosts. For more information, see [Metrics](/intl.en-US/Host monitoring/Metrics.md).|
|Business-level process monitoring|Collects the CPU usage, memory usage, and the number of files that are opened for the active processes. This enables you to monitor the resource usage of your host. For more information, see [Process monitoring](/intl.en-US/Host monitoring/Process monitoring.md).|
|GPU monitoring|Allows you to view monitoring data of metrics by graphics processing unit \(GPU\), instance, and group. For more information, see [GPU monitoring](/intl.en-US/Host monitoring/GPU monitoring.md).|
|Flexible alerting|Allows you to manage hosts from different regions and configure alert rules by application group. This reduces the cost of monitoring management. For more information, see [Alert service](/intl.en-US/Host monitoring/Alert service.md).|

