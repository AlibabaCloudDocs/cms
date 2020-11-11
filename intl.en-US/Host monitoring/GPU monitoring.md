# GPU monitoring

This topic describes how to view monitoring data of graphics processing units \(GPUs\) in the CloudMonitor console and query the data by calling an API operation.

## Metrics

The metrics for GPU monitoring are based on three dimensions: GPU, instance, and group.

-   **GPU-dimension metrics**

    GPU-dimension metrics collect monitoring data of a single GPU. The following table lists the GPU-dimension metrics.

    |Metric|Unit|Description|Dimension|
    |:-----|:---|:----------|:--------|
    |gpu\_memory\_freespace|Byte|The idle memory of a GPU|instanceId and gpuId|
    |gpu\_memory\_totalspace|Byte|The total memory of a GPU|instanceId and gpuId|
    |gpu\_memory\_usedspace|Byte|The used memory of a GPU|instanceId and gpuId|
    |gpu\_gpu\_usedutilization|%|The usage of a GPU|instanceId and gpuId|
    |gpu\_encoder\_utilization|%|The encoder usage of a GPU|instanceId and gpuId|
    |gpu\_decoder\_utilization|%|The decoder usage of a GPU|instanceId and gpuId|
    |gpu\_gpu\_temperature|°C|The temperature of a GPU|instanceId and gpuId|
    |gpu\_power\_readings\_power\_draw|W|The power of a GPU|instanceId and gpuId|
    |gpu\_memory\_freeutilization|%|The memory idle rate of a GPU|instanceId and gpuId|
    |gpu\_memory\_useutilization|%|The memory usage of a GPU|instanceId and gpuId|

-   **Instance-dimension metrics**

    Instance-dimension metrics collect monitoring data of all GPUs on a single Elastic Compute Service \(ECS\) instance, and calculate the maximum, minimum, and average values. In this way, you can view the overall GPU resource usage on the instance. The following table lists the instance-dimension metrics.

    |Metric|Unit|Description|Dimension|
    |:-----|:---|:----------|:--------|
    |instance\_gpu\_decoder\_utilization|%|The decoder usage of GPUs on an instance|instanceId|
    |instance\_gpu\_encoder\_utilization|%|The encoder usage of GPUs on an instance|instanceId|
    |instance\_gpu\_gpu\_temperature|°C|The temperature of GPUs on an instance|instanceId|
    |instance\_gpu\_gpu\_usedutilization|%|The usage of GPUs on an instance|instanceId|
    |instance\_gpu\_memory\_freespace|Byte|The idle memory of GPUs on an instance|instanceId|
    |instance\_gpu\_memory\_freeutilization|%|The memory idle rate of GPUs on an instance|instanceId|
    |instance\_gpu\_memory\_totalspace|Byte|The total memory of GPUs on an instance|instanceId|
    |instance\_gpu\_memory\_usedspace|Byte|The used memory of GPUs on an instance|instanceId|
    |instance\_gpu\_memory\_usedutilization|%|The memory usage of GPUs on an instance|instanceId|
    |instance\_gpu\_power\_readings\_power\_draw|W|The power of GPUs on an instance|instanceId|

-   **Group-dimension metrics**

    Group-dimension metrics collect monitoring data of all GPUs on all ECS instances in an application group, and calculate the maximum, minimum, and average values. In this way, you can view the overall GPU resource usage in the application group. The following table lists the group-dimension metrics.

    |Metric|Unit|Description|Dimension|
    |:-----|:---|:----------|:--------|
    |group\_gpu\_decoder\_utilization|%|The decoder usage of GPUs in an application group|groupId|
    |group\_gpu\_encoder\_utilization|%|The encoder usage of GPUs in an application group|groupId|
    |group\_gpu\_gpu\_temperature|°C|The temperature of GPUs in an application group|groupId|
    |group\_gpu\_gpu\_usedutilization|%|The usage of GPUs in an application group|groupId|
    |group\_gpu\_memory\_freespace|Byte|The idle memory of GPUs in an application group|groupId|
    |group\_gpu\_memory\_freeutilization|%|The memory idle rate of GPUs in an application group|groupId|
    |group\_gpu\_memory\_totalspace|Byte|The total memory of GPUs in an application group|groupId|
    |group\_gpu\_memory\_usedspace|Byte|The used memory of GPUs in an application group|groupId|
    |group\_gpu\_memory\_usedutilization|%|The memory usage of GPUs in an application group|groupId|
    |group\_gpu\_power\_readings\_power\_draw|W|The power of GPUs in an application group|groupId|


## View GPU monitoring data in the CloudMonitor console

After purchasing an ECS compute optimized instance with GPU, you need to install the GPU driver and the CloudMonitor agent on the instance. Then, you can view and configure GPU monitoring charts and set alert rules for the instance in the CloudMonitor console.

**View monitoring charts**

1.  Log on to the [CloudMonitor console](https://cms-intl.console.aliyun.com).
2.  In the left-side navigation pane, click **Host Monitoring**. The Host Monitoring page appears.
3.  On the Instances tab, click the name of an instance to go to the Instance Info page. Click the **GPUMonitor** tab to view the GPU monitoring charts of the instance.

**Configure monitoring charts**

1.  Log on to the [CloudMonitor console](https://cms-intl.console.aliyun.com).
2.  In the left-side navigation pane, choose **Dashboard** \> **Custom Dashboard**. The **Dashboards** page appears.
3.  In the upper-right corner, click **Create Dashboard**. In the **Create Dashboard** dialog box that appears, enter the dashboard name, and click **Create**.
4.  On the page that appears, click **Add View** in the upper-right corner. The Add View page appears.
5.  In the **Chart Type** section, select a chart type from the line chart, area chart, TopN table, heat map, and pie chart.
6.  In the **Select Metrics** section, select a GPU-related metric from the Metrics drop-down list. Then, click **Save**.

**Set alert rules**

You can set alert rules for GPU-related metrics. We recommend that you create an alert template and apply the template to an application group to set alert rules for multiple instances at a time. For more information, see [Create an alarm template](/intl.en-US/Best Practices/Create an alarm template.md).

## Query GPU monitoring data by calling an API operation

-   You can query GPU monitoring data by calling the [DescribeMetricList](/intl.en-US/API Reference/Monitoring data on time series metrics of cloud services/DescribeMetricList.md) operation.
-   Parameter description: Set the Namespace parameter to acs\_ecs\_dashboard. Set the MetricName and Dimensions parameters as required based on the preceding tables.

