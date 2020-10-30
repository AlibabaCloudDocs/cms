# Configure the data export service

You can define a data export rule to export real-time monitoring data of a time series metric about which you are concerned to a data storage service. This topic describes how to define a data export rule.

1.  Activate a data storage service.

    Take Log Service as an example. When you log on to the Log Service console for the first time, activate Log Service as prompted.

2.  Configure data storage service.

    After you activate the data storage service, you can call an API operation to configure the service as a container for storing exported data. For more information, see [PutExporterOutput](/intl.en-US/API Reference/Monitoring data on time series metrics of cloud services/PutExporterOutput.md).

3.  Define a data export rule.

    After you configure the data storage service for storing exported data, you can call an API operation to subscribe to the data that you want to obtain. For more information, see [PutExporterRule](/intl.en-US/API Reference/Monitoring data on time series metrics of cloud services/PutExporterRule.md).

    The exported data includes monitoring data and data export information. The monitoring data is determined by the metric to which you subscribe and the data export rule. The following table describes the data export information.

    |Parameter|Description|
    |---------|-----------|
    |cms\_namespace|The namespace of the metric.|
    |cms\_metric|The name of the metric.|
    |cms\_platform|The name of the platform for processing CloudMonitor data.|
    |cms\_data\_filter\_rule|The information about the data filter.|
    |cms\_data\_filter\_user\_id|The ID of the user who filters data.|
    |cms\_exporter\_dispatch\_ts|The timestamp when the data was distributed.|
    |cms\_tumbling\_window|The time window for collecting metric data.|

    For example, the data storage service is configured as the following code:

    ```
    DestName:DemoDest
    ConfigJson:
    {
        "logstore": "sls_logstore_name",
        "ak": "access_key",
        "project": "sls_project_name",
        "as": "access_secret",
        "endpoint": "http://sls-endpoint.log.aliyuncs.com"
    }
    DestType:sls
    Desc:Demo
    ```

    The following code shows the subscribed metric:

    ```
    Project (Namespace): acs_ecs_dashboard
    Metric: CPUUtilization
    Description: The CPU usage.
    Unit: percent
    Dimensions: instanceId
    Statistics: Average, Minimum, Maximum
    ```

    For more information about the key metrics of cloud services, see [Overview](/intl.en-US/Appendix 1: Metrics/Overview.md).

    The following code shows the data export rule:

    ```
    RuleName:DemoExporterRule
    DstNames:DemoDest
    Namespace:acs_ecs_dashboard
    MetricName:CPUUtilization
    TargetWindows:60
    Describe:demo
    ```

    The following code shows the exported data:

    ```
    cms_data_filter_rule:DemoExporterRule
    cms_data_filter_ts:158434268****
    cms_data_filter_user_id:127067667954****
    cms_exporter_dispatch_ts:158434268****
    cms_metric:CPUUtilization
    cms_namespace:acs_ecs_dashboard
    cms_platform:blink
    cms_tumbling_window:60
    instanceId:i-2zefuqggczshldq*****
    Maximum:4.47388452258
    Minimum:4.47388452258
    Average:4.47388452258
    userId:12706766795*****
    ```


Modify or delete a data export rule.

You cannot directly call an API operation to modify a data export rule that has been configured. However, you can call relevant API operations to delete the rule and then configure the required data export rule. For more information, see [DeleteExporterRule](/intl.en-US/API Reference/Monitoring data on time series metrics of cloud services/DeleteExporterRule.md).

