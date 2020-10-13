# OpenAPI

通过本文您可以了解OpenAPI的监控项。

-   **Namespace**为**acs\_openAPI**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|调用次数|Count|TotalNumber|userId、productName、API|Value|
|错误次数|Count|code4XXNumber|userId、productName、API|Value|
|错误率|%|code4XXRate|userId、productName、API|Value|

