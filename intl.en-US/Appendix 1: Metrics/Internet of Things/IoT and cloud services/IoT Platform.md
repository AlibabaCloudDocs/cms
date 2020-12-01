# IoT Platform

This topic describes the metrics of IoT Platform.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_iot**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|DeviceEventReportError|Frequency|DeviceEventReportError|userId, regionId, instanceId, and productKey|Count|
|DevicePropertyReportError|Frequency|DevicePropertyReportError|userId, regionId, instanceId, and productKey|Count|
|DevicePropertySettingError|Frequency|DevicePropertySettingError|userId, regionId, instanceId, and productKey|Count|
|DeviceServiceCallError|Frequency|DeviceServiceCallError|userId, regionId, instanceId, and productKey|Count|
|MessageCountForwardedThroughRuleEngine\_DATAHUB|Frequency|MessageCountForwardedThroughRuleEngine\_DATAHUB|userId, regionId, instanceId, and productKey|Count|
|MessageCountForwardedThroughRuleEngine\_FC|Frequency|MessageCountForwardedThroughRuleEngine\_FC|userId, regionId, instanceId, and productKey|Count|
|MessageCountForwardedThroughRuleEngine\_MNS|Frequency|MessageCountForwardedThroughRuleEngine\_MNS|userId, regionId, instanceId, and productKey|Count|
|MessageCountForwardedThroughRuleEngine\_MQ|Frequency|MessageCountForwardedThroughRuleEngine\_MQ|userId, regionId, instanceId, and productKey|Count|
|MessageCountForwardedThroughRuleEngine\_OTS|Frequency|MessageCountForwardedThroughRuleEngine\_OTS|userId, regionId, instanceId, and productKey|Count|
|MessageCountForwardedThroughRuleEngine\_RDS|Frequency|MessageCountForwardedThroughRuleEngine\_RDS|userId, regionId, instanceId, and productKey|Count|
|MessageCountForwardedThroughRuleEngine\_REPUBLISH|Frequency|MessageCountForwardedThroughRuleEngine\_REPUBLISH|userId, regionId, instanceId, and productKey|Count|
|MessageCountForwardedThroughRuleEngine\_TSDB|Frequency|MessageCountForwardedThroughRuleEngine\_TSDB|userId, regionId, instanceId, and productKey|Count|
|MessageCountSentFromIoT\_HTTP\_2|Frequency|MessageCountSentFromIoT\_HTTP\_2|userId, regionId, instanceId, and productKey|Count|
|MessageCountSentFromIoT\_LoRa|Frequency|MessageCountSentFromIoT\_LoRa|userId, regionId, instanceId, and productKey|Count|
|MessageCountSentFromIoT\_MQTT|Frequency|MessageCountSentFromIoT\_MQTT|userId, regionId, instanceId, and productKey|Count|
|MessageCountSentToIoT\_CoAP|Frequency|MessageCountSentToloT\_CoAP|userId, regionId, instanceId, and productKey|Count|
|MessageCountSentToIoT\_HTTP|Frequency|MessageCountSentToloT\_HTTP|userId, regionId, instanceId, and productKey|Count|
|MessageCountSentToIoT\_HTTP/2|Count|MessageCountSentToloT\_HTTP\_2|userId, regionId, instanceId, and productKey|Count|
|MessageCountSentToIoT\_LoRa|Frequency|MessageCountSentToloT\_Lora|userId, regionId, instanceId, and productKey|Count|
|MessageCountSentToIoT\_MQTT|Frequency|MessageCountSentToloT\_MQTT|userId, regionId, instanceId, and productKey|Count|
|OnlineDevicesCount\_MQTT|Frequency|OnlineDevicesCount\_MQTT|userId, regionId, instanceId, and productKey|DeviceNum|
|MessageCountPerMinute|Count|MessageCountPerMinute|userId, regionId, instanceId, and productKey|Count|
|RuleEningeTransmitCountPerMinute|Count|RuleEningeTransmitCountPerMinute|userId, regionId, instanceId, and productKey|Count|
|DeviceCount\_Product|Count|device\_count\_of\_product|userId, regionId, instanceId, and productKey|Count|

