# Overview

Cloud Monitor provides an overview of alerts, key events, and resource usage.

This allows you to check the resource usage and alerts of each Alibaba Cloud service in real time. The following figure shows the overview of Cloud Monitor.

![Overview](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2721987951/p102797.png)

## Alert overview

In the Alert Overview section, Cloud Monitor provides alert statistics, including the total number of alerts in the last seven days, the number of triggered alert rules, the number of alert rules with insufficient data, and the usage of text messages in this month.

-   You can click Total Alarms in 7 Days to view the alert trend chart and alert history in the last seven days.
-   You can click Alarms to view the details of alert rules in the **Alert** state.
-   You can click Insufficient Data to view the details of alert rules in the **Insufficient Data** state.

## Event overview

In the Event Overview section, Cloud Monitor summarizes all the exceptions and O&M events that occurred within the last 24 hours. The following table describes the key events that are supported.

|Alibaba Cloud service|Event|
|:--------------------|:----|
|ECS or non-ECS hosts|Agent Stopped|
|ApsaraDB RDS|Master/Slave Instance Switch|
|ApsaraDB RDS|Instance Faults|
|ApsaraDB for MongoDB|Instance Faults|
|ApsaraDB for Redis|Master/Slave Instance Switch|
|ApsaraDB for Redis|Instance Faults|

## Resource usage overview

In the Resource Usage section, Cloud Monitor displays the overall resource usage of each Alibaba Cloud service within your account. Cloud Monitor uses the 95th percentile to measure the resource usage of most Alibaba Cloud services.

The following table describes the statistical metrics of Alibaba Cloud services.

|Alibaba Cloud service|Metric|Statistical method|Statistical period|Statistical range|
|:--------------------|:-----|:-----------------|:-----------------|:----------------|
|ECS or non-ECS hosts|CPU utilization|95th percentile|Real-time|All instances|
|ECS or non-ECS hosts|Memory usage|95th percentile|Real-time|All instances|
|ECS or non-ECS hosts|Disk usage|95th percentile|Real-time|All instances|
|ECS or non-ECS hosts|Outbound bandwidth over Internet|95th percentile|Real-time|All instances|
|ApsaraDB RDS|CPU utilization|95th percentile|Real-time|All instances|
|ApsaraDB RDS|Input/Output operations per second \(IOPS\) usage|95th percentile|Real-time|All instances|
|ApsaraDB RDS|Connection usage|95th percentile|Real-time|All instances|
|ApsaraDB RDS|Disk usage|95th percentile|Real-time|All instances|
|OSS|Total outbound traffic over Internet in the current month|Sum|The cumulative value from 00:00 on the first day of the month to the current time|All buckets|
|OSS|Total number of PUT requests in the current month|Sum|The cumulative value from 00:00 on the first day of the month to the current time|All buckets|
|OSS|Total number of GET requests in the current month|Sum|The cumulative value from 00:00 on the first day of the month to the current time|All buckets|
|OSS|Storage size|Sum|The sum of the storage occupied by all OSS buckets|All buckets|
|CDN|Total traffic in the current month|Sum|The cumulative value from 00:00 on the first day of the month to the current time|All domains|
|CDN|Peak network bandwidth|95th percentile|Real-time|All domains|
|CDN|Queries per second \(QPS\)|95th percentile|Real-time|All domains|
|ApsaraDB for MongoDB|CPU utilization|95th percentile|Real-time|All instances|
|ApsaraDB for MongoDB|Memory usage|95th percentile|Real-time|All instances|
|ApsaraDB for MongoDB|IOPS usage|95th percentile|Real-time|All instances|
|ApsaraDB for MongoDB|Connection usage|95th percentile|Real-time|All instances|
|ApsaraDB for MongoDB|Disk usage|95th percentile|Real-time|All instances|
|ApsaraDB for Memcache|Cache hit ratio|95th percentile|Real-time|All instances|
|ApsaraDB for Memcache|Cache usage|95th percentile|Real-time|All instances|
|ApsaraDB for Redis|Memory usage|95th percentile|Real-time|All instances|
|ApsaraDB for Redis|IOPS usage|95th percentile|Real-time|All instances|
|ApsaraDB for Redis|Connection usage|95th percentile|Real-time|All instances|
|EIP|Inbound bandwidth|95th percentile|Real-time|All instances|
|EIP|Outbound bandwidth|95th percentile|Real-time|All instances|
|Container Service|CPU utilization|95th percentile|Real-time|All instances|
|Container Service|Memory usage|95th percentile|Real-time|All instances|
|Container Service|Outbound traffic over Internet|95th percentile|Real-time|All instances|
|Log Service|Total inbound traffic in the current month|Sum|The cumulative value from 00:00 on the first day of the month to the current time|All projects|
|Log Service|Total outbound traffic in the current month|Sum|The cumulative value from 00:00 on the first day of the month to the current time|All projects|
|Log Service|Total number of requests in the current month|Sum|The cumulative value from 00:00 on the first day of the month to the current time|All projects|
|HybridDB for MySQL|CPU utilization|95th percentile|Real-time|All instances|
|HybridDB for MySQL|Memory usage|95th percentile|Real-time|All instances|
|HybridDB for MySQL|IOPS usage|95th percentile|Real-time|All instances|
|HybridDB for MySQL|Connection usage|95th percentile|Real-time|All instances|
|HybridDB for MySQL|Disk usage|95th percentile|Real-time|All instances|

Statistical method: the 95th percentile.

-   A percentile is a measure used in statistics. It indicates the value lower than which a given percentage of observations in a group of observations in ascending order falls.
-   The 95th percentile is the value lower than which 95% of observations in a group of observations in ascending order falls. For example, if the 95th percentile for the CPU usage of ECS instances is 34%, 95% of the ECS instances have a CPU usage of lower than 34%.

