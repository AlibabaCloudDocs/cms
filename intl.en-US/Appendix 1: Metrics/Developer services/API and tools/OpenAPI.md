# OpenAPI

This topic describes the metrics for OpenAPI Explorer.

-   Set the **Namespace** parameter to **acs\_openAPI**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|TotalNumber|Count|TotalNumber|userId, productName, and API|Value|
|code4XXNumber|Count|code4XXNumber|userId, productName, and API|Value|
|code4XXRate|%|code4XXRate|userId, productName, and API|Value|

