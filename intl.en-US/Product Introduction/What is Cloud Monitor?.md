# What is Cloud Monitor?

Cloud Monitor is a service that monitors Alibaba Cloud resources and Internet applications.

Cloud Monitor provides a one-stop, out-of-the-box, and enterprise-class monitoring solution. Cloud Monitor supports IT infrastructure monitoring and dial testing-based Internet quality monitoring by using events and custom metrics. The monitoring services provided by Cloud Monitor are efficient, comprehensive, and cost-effective. Cloud Monitor helps you improve system service availability and reduce the operations and maintenance \(O&M\) costs of IT infrastructure.

Cloud Monitor provides application groups and alert templates to monitor tens of thousands of instances from dozens of services. You can add resources from different services and regions to the same application group to simplify resource management.

Cloud Monitor allows you to monitor the metrics of Alibaba Cloud services, detect the availability of websites hosted on Elastic Compute Service \(ECS\) instances or carrier servers, and configure alert rules for specified metrics. This way, you can monitor the usage of your Alibaba Cloud services and the status of your applications. You can also resolve alerts as early as possible to ensure the availability of your applications.

## Architecture

![Architecture](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/8590987951/p6442.png)

## Features

The following table describes the features that are supported by Cloud Monitor.

|Feature|Description|
|-------|-----------|
|[Dashboard](/intl.en-US/Dashboard/Overview.md)|Allows you to view monitoring data as needed. You can view monitoring data of different instances from different services by using a dashboard.|
|[Application group](/intl.en-US/Application groups/Overview.md)|Allows you to manage resources from different services and regions by group. You can use application groups to manage resources, such as servers, databases, load balancers, and storage resources, of your business in a centralized manner. For example, you can manage alert rules and view monitoring data by application group. This improves O&M efficiency.|
|[Host monitoring](/intl.en-US/Host monitoring/Overview.md)|Allows you to install Cloud Monitor agents on servers to collect monitoring data of metrics such as CPU, memory, disk, and network usage. Host monitoring allows you to configure alert rules for all metrics.|
|[Event monitoring](/intl.en-US/Event monitoring/Overview.md)|Allows you to report events, query events, and receive alerts about events. Event monitoring allows you to report exceptions or important changes in your business to Cloud Monitor and receive alerts when exceptions occur.|
|[Custom monitoring](/intl.en-US/Custom monitoring/Overview.md)|Allows you to report business metrics about which you are concerned to Cloud Monitor. Cloud Monitor processes the collected monitoring data and generates alerts based on the processing result.|
|[Site monitoring](/intl.en-US/Site Monitoring/Overview.md)|Allows you to test network connectivity. Site monitoring sends detection requests that simulate real user access from Alibaba Cloud data centers to your site.|
|[Cloud service monitoring](/intl.en-US/.md)|Allows you to monitor the metrics of the Alibaba Cloud services that are activated for your Alibaba Cloud account. You can view the monitoring data about resources of each Alibaba Cloud service in monitoring charts. You can also configure alert rules to monitor resources. If an alert is triggered based on the alert rules, Cloud Monitor sends an alert notification to you. This way, you are notified of the status of your cloud resources as early as possible.|
|[Alert service](/intl.en-US/Alarm service/Overview.md)|Allows you to configure alert rules based on monitoring data. You can configure alert rules to specify how Cloud Monitor checks the monitoring data and when Cloud Monitor sends alert notifications. After you configure alert rules for important metrics, you can receive alert notifications when exceptions occur and handle the exceptions as early as possible.|
|[Container monitoring](/intl.en-US/Container Service Monitoring/Overview.md)|Allows you to monitor Container Service for Kubernetes \(ACK\) clusters across regions in a centralized and global way.|

