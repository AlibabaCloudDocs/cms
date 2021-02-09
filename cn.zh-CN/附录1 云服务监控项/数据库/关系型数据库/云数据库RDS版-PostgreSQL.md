# 云数据库RDS版-PostgreSQL

通过本文您可以了解云数据库RDS版的PostgreSQL数据库云盘版的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_rds\_dashboard**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|PG\_数据库年龄|xids|PG\_DBAge|userId、instanceId|Average、Maximum、Minimum|
|PG\_每CPU平均活跃连接数|Count|active\_connections\_per\_cpu|userId、instanceId|Average|
|PG\_连接数使用率|%|conn\_usgae|userId、instanceId|Average|
|PG\_CPU使用率|%|cpu\_usage|userId、instanceId|Average|
|PG\_IOPS使用率|%|iops\_usage|userId、instanceId|Average|
|PG\_INODE使用率|%|local\_fs\_inode\_usage|userId、instanceId|Average|
|PG\_磁盘空间使用率|%|local\_fs\_size\_usage|userId、instanceId|Average|
|PG\_内存使用率|%|mem\_usage|userId、instanceId|Average|
|PG\_只读同步延迟|Second|PG\_RO\_ReadLag|userId、instanceId|Average|
|PG\_只读流复制状态|Value|PG\_RO\_StreamingStatus|userId、instanceId|Average|

