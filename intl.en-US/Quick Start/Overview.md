# Overview

Cloud Monitor providesan overview of alerts, key events, and resource usage.

This allows you to checkthe resource usage and alerts of each cloud service in real time.

![Overview](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2721987951/p102797.png)

## Alert overview

In the Alert Overview section, Cloud Monitor provides alert statistics, including the total number of alerts in the last seven days, the number of triggered alert rules, the number of alert rules with insufficient data, and the usage of text messages in this month.

You can view more information about alert rules by clicking the number of alert rules that are triggered or have insufficient data.

## Event overview

In the Event Overview section, Cloud Monitor summarizes all the exceptions and O&M events that occurred within the last 24 hours. The following table lists the key events that are supported.

|Alibaba Cloud service|Event Name|
|:--------------------|:---------|
|ECS or non-ECS hosts|Agent Stopped|
|ApsaraDB RDS|Master/Slave Instance Switch|
|ApsaraDB RDS|Instance Faults|
|ApsaraDB for MongoDB|Instance Faults|
|ApsaraDB for Redis|Master/Slave Instance Switch|
|ApsaraDB for Redis|Instance Faults|

## Resource usage overview

In the Resource Usage section, Cloud Monitor displays the overall resource usage of each cloud service within the Alibaba Cloud account. For Object Storage Service \(OSS\), Alibaba Cloud CDN, and Log Service, Cloud Monitor displays the cumulative resource usage in this month. For other cloud services, Cloud Monitor displays the resource usage in real time by using the 95th percentile.

Statistical method: the 95th percentile.

-   A percentile is a measure used in statistics. It indicates the value lower than which a given percentage of observations in a group of observations in ascending order falls.
-   The 95th percentile is the value lower than which 95% of observations in a group of observations in ascending order falls. For example, if the 95th percentile for the CPU usage of ECS instances is 34%, 95% of the ECS instances have a CPU usage of lower than 34%.

Cloud Monitor uses the 95th percentile to measure the resource usage of most cloud services.

## Resource metric description

|Alibaba Cloud service|Metric|Statistical method|Statistical period|Statistical range|
|:--------------------|:-----|:-----------------|:-----------------|:----------------|
|Hosts|CPU Usage|95th Percent|Real-time|All instances|
|Hosts|Memory Usage|95th Percent|Real-time|All instances|
|Hosts|Disk Usage|95th Percent|Real-time|All instances|
|Hosts|Public Network Outbound Traffic|95th Percent|Real-time|All instances|
|RDS-DB|CPU Usage|95th Percent|Real-time|All instances|
|RDS-DB|IOPS Usage|95th Percent|Real-time|All instances|
|RDS-DB|Connection Usage|95th Percent|Real-time|All instances|
|ApsaraDB RDS|Disk Usage|95th Percent|Real-time|All instances|
|Object Storage Service|Monthly Internet Outbound Traffic|Sum|The cumulative value since 00:00 on the first day of this month|All buckets|
|Object Storage Service|Monthly Put Requests|Sum|The cumulative value since 00:00 on the first day of this month|All buckets|
|Object Storage Service|Monthly Get Requests|Sum|The cumulative value since 00:00 on the first day of this month|All buckets|
|Object Storage Service|Size|Sum|The sum of the storage occupied by all OSS buckets|All buckets|
|CDN|Monthly Traffic|Sum|The cumulative value since 00:00 on the first day of this month|All domain names|
|CDN|Peak Bandwidth|95th Percent|Real-time|All domains|
|CDN|Visit QPS|95th Percent|Real-time|All domain names|
|ApsaraDB for MongoDB|CPU Usage|95th Percent|Real-time|All instances|
|ApsaraDB for MongoDB|Memory Usage|95th Percent|Real-time|All instances|
|ApsaraDB for MongoDB|IOPS Usage|95th Percent|Real-time|All instances|
|ApsaraDB for MongoDB|Connection Usage|95th Percent|Real-time|All instances|
|ApsaraDB for MongoDB|Disk Usage|95th Percent|Real-time|All instances|
|Earlier ApsaraDB for Memcache|Cache Hit Ratio|95th Percent|Real-time|All instances|
|Earlier ApsaraDB for Memcache|Cache Usage|95th Percent|Real-time|All instances|
|KVStore for Redis|Memory Usage|95th Percent|Real-time|All instances|
|KVStore for Redis|IOPS Usage|95th Percent|Real-time|All instances|
|KVStore for Redis|Connection Usage|95th Percent|Real-time|All instances|
|Elastic IP Address|Inbound Bandwidth|95th Percent|Real-time|All instances|
|Elastic IP Address|Outbound Bandwidth|95th Percent|Real-time|All instances|
|Container Service|CPU Usage|95th Percent|Real-time|All instances|
|Container Service|Memory Usage|95th Percent|Real-time|All instances|
|Container Service|Internet Outbound Traffic|95th Percent|Real-time|All instances|
|Log Service|Monthly Inbound Traffic|Sum|The cumulative value since 00:00 on the first day of this month|All projects|
|Log Service|Monthly Outbound Traffic|Sum|The cumulative value since 00:00 on the first day of this month|All projects|
|Log Service|Monthly Requests|Sum|The cumulative value since 00:00 on the first day of this month|All projects|
|AnalyticDB for PostgreSQL|CPU Usage|95th Percent|Real-time|All instances|
|AnalyticDB for PostgreSQL|Memory Usage|95th Percent|Real-time|All instances|
|AnalyticDB for PostgreSQL|I/O Throughput Usage|95th Percent|Real-time|All instances|
|AnalyticDB for PostgreSQL|Connection Usage|95th Percent|Real-time|All instances|
|AnalyticDB for PostgreSQL|Disk Usage|95th Percent|Real-time|All instances|

