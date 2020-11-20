# Serverless App Engine

This topic describes the metrics of Serverless App Engine.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_serverless**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|CPU|%|cpu|userId and appId|Average, Maximum, and Minimum|
|instanceId\_memoryUsed|MB|instanceId\_memoryUsed|userId, appId, and instanceId|Average|
|CPU|%|instance\_cpu|userId, appId, and instanceId|Average|
|instance\_load|1min|instance\_load|userId, appId, and instanceId|Average|
|instance\_memoryTotal|MB|instance\_memoryTotal|userId, appId, and instanceId|Average|
|instance\_netRecv|Bytes/Second|instance\_netRecv|userId, appId, and instanceId|Average|
|instance\_netTran|Bytes/Second|instance\_netTran|userId, appId, and instanceId|Average|
|Average Load|min|load|userId and appId|Average, Maximum, and Minimum|
|memoryTotal|MB|memoryTotal|userId and appId|Average|
|memoryUsed|MB|memoryUsed|userId and appId|Average, Maximum, and Minimum|
|netRecv|Bytes/Second|netRecv|userId and appId|Average, Maximum, and Minimum|
|netTran|Bytes/Second|netTran|userId and appId|Average, Maximum, and Minimum|

