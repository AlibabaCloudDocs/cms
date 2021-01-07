# Terms

This topic describes the terms of Cloud Monitor.

|Term|Description|
|:---|:----------|
|site monitoring|This feature allows you to monitor the availability of URLs and IP addresses. You can use detection points to send requests over the HTTP, HTTPS, ICMP, TCP, UDP, DNS, POP3, SMTP, or FTP protocol to the monitored URLs or IP addresses. You can then receive the status codes and response time.|
|cloud service monitoring|This feature allows you to monitor the metrics of different cloud services. You can monitor the metrics of ApsaraDB RDS, Server Load Balancer \(SLB\), and Object Storage Service \(OSS\).|
|custom monitoring|This feature allows you to customize metrics. You can add monitoring charts and configure alert rules for the custom metrics.|
|alert|You can configure alert rules for metrics in host monitoring, detection points in site monitoring, instances in cloud service monitoring, and metrics in custom monitoring. If a metric meets the conditions specified in the alert rule, an alert notification is sent.|
|metric|The type of the monitoring data. Cloud Monitor provides system metrics and allows you to customize metrics. For example, the CPU usage, memory usage, and disk usage of an ECS instance.|
|dimension|The identifier that is used to locate monitoring data of a metric. For example, to monitor the CPU usage of an ECS instance, you can use the ID of the Alibaba Cloud account and the ID of the instance to identify the monitoring data.|
|alert rule|The condition that triggers an alert. If a metric meets an alert condition, you will receive an alert notification.|
|mute period|The interval during which alert notifications are not sent for a metric. If a metric continuously exceeds the threshold within the specified mute period after an alert notification was sent, no more alert notifications will be sent for the metric.|
|alert contact|The recipient of alert notifications.|
|alert group|The alert group that receives alert notifications. The group can consist of one or more alert contacts. If you specify an alert group for an alert rule of an application group, alert notifications are sent to the contacts in the alert group by using the specified notification method.|
|notification method|The method used to send alert notifications. Supported methods includeemails and DingTalk robots.|

