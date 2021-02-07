# 云数据库ClickHouse

通过本文您可以了解云数据库ClickHouse的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_clickhouse**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|连接数使用比例|%|conn\_usage|uid、logic\_name|Average|
|连接数|count|conn\_usage\_count|uid、logic\_name|Average|
|CPU使用率|%|cpu\_usage|uid、logic\_name|Average|
|磁盘空间已用比例|%|disk\_usage|uid、logic\_name|Average|
|磁盘总使用空间|MB|disk\_usage\_size|uid、logic\_name|Average|
|每秒插入数据量|MB|insert\_mb\_ps|uid、logic\_name|Average|
|每秒插入行数|line|insert\_rows\_ps|uid、logic\_name|Average|
|内存使用比例|%|mem\_usage|uid、logic\_name|Average|
|内存使用量|MB|mem\_usage\_size|uid、logic\_name|Average|
|每秒查询次数|frequency|qps|uid、logic\_name|Average|

