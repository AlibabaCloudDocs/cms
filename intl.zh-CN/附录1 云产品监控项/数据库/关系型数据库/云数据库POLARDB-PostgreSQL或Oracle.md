# 云数据库POLARDB-PostgreSQL或Oracle

通过本文您可以了解云数据库POLARDB的PostgreSQL或Oracle版的监控项。

-   **Namespace**为**acs\_polardb**。
-   **Period**默认为60秒，也可以为60的整数倍。

|监控项|单位|Metric|Dimensions|Statistics|
|---|--|------|----------|----------|
|活跃连接数|Count|active\_connections|userId、clusterId、instanceId|Average|
|数据块读取数|Count|blks\_read\_delta|userId、clusterId、instanceId|Value|
|连接使用率|%|conn\_usage|userId、clusterId、instanceId|Average|
|CPU使用率|%|cpu\_total|userId、clusterId、instanceId|Average|
|数据库最大年龄|xids|db\_age|userId、clusterId、instanceId|Value|
|内存使用率|%|mem\_usage|userId、clusterId、instanceId|Average|
|数据盘大小|Mbyte|pls\_data\_size|userId、clusterId、instanceId|Value|
|IOPS|Frequency|pls\_iops|userId、clusterId、instanceId|Average|
|读IOPS|Frequency|pls\_iops\_read|userId、clusterId、instanceId|Average|
|写IOPS|Frequency|pls\_iops\_write|userId、clusterId、instanceId|Average|
|WAL日志大小|Mbyte|pls\_pg\_wal\_dir\_size|userId、clusterId、instanceId|Value|
|IO吞吐|Mbyte/s|pls\_throughput|userId、clusterId、instanceId|Average|
|读IO吞吐|Mbyte/s|pls\_throughput\_read|userId、clusterId、instanceId|Average|
|写IO吞吐|Mbyte/s|pls\_throughput\_write|userId、clusterId、instanceId|Average|
|膨胀点|s|swell\_time|userId、clusterId、instanceId|Average|
|TPS|Frequency|tps|userId、clusterId、instanceId|Average|

