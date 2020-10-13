# 云原生分布式数据库PolarDB-X 1.0

通过本文您可以了解云原生分布式数据库PolarDB-X 1.0的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_drds**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|CPU利用率|%|CPUUtilization|userId、instanceId|Average|
|连接数|Count|ConnectionCount|userId、instanceId|Average|
|逻辑QPS|Count|LogicQPS|userId、instanceId|Average|
|逻辑RT|ms|LogicRT|userId、instanceId|Average|
|内存利用率|%|MemoryUtilization|userId、instanceId|Average|
|网络输入带宽|bit/s|NetworkInputTraffic|userId、instanceId|Average|
|网络输出带宽|bit/s|NetworkOutputTraffic|userId、instanceId|Average|
|物理QPS|Count|PhysicsQPS|userId、instanceId|Average|
|物理RT|ms|PhysicsRT|userId、instanceId|Average|
|活跃线程数|Count|ThreadCount|userId、instanceId|Average|
|私有RDS\_MySQL每秒InsertSelect量|Count|com\_insert\_select|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL每秒Replace量|Count|com\_replace|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL每秒ReplaceSelect量|Count|com\_replace\_select|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL每秒Select量|Count|com\_select|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL每秒Update量|Count|com\_update|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL连接数利用率|%|conn\_usage|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL CPU利用率|%|cpu\_usage|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL磁盘使用率|%|disk\_usage|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL\_BP脏页百分率|%|ibuf\_dirty\_ratio|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL每秒物理读次数|Count|ibuf\_pool\_reads|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL\_BP读命中率|%|ibuf\_read\_hit|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL每秒逻辑读次数|Count|ibuf\_request\_r|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL每秒逻辑写次数|Count|ibuf\_request\_w|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL\_BP利用率|%|ibuf\_use\_ratio|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL\_InnoDB每秒读取数据量|Kbyte|inno\_data\_read|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL\_InnoDB每秒写入数据量|Kbyte|inno\_data\_written|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL\_InnoDB每秒删除行数|Count|inno\_row\_delete|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL\_InnoDB每秒插入行数|Count|inno\_row\_insert|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL\_InnoDB每秒读取行数|Count|inno\_row\_readed|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL\_InnoDB每秒更新行数|Count|inno\_row\_update|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL\_InnoDB每秒日志写请求次数|Count|innodb\_log\_write\_requests|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL\_InnoDB每秒日志物理写次数|Count|innodb\_log\_writes|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL\_InnoDB每秒日志fsync量|Count|innodb\_os\_log\_fsyncs|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL网络流入带宽|bits/s|input\_traffic\_ps|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL IOPS利用率|%|iops\_usage|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL内存利用率|%|mem\_usage|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL网络流出带宽|bits/s|output\_traffic\_ps|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL每秒查询量|Count|qps|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL只读实例延迟|seconds|slave\_lag|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL每秒慢查询量|Count|slow\_queries|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL每秒创建临时表数量|Count|tb\_tmp\_disk|userId、instanceId、rdsInstId|Average|
|私有RDS\_MySQL每秒事务数|Count|tps|userId、instanceId、rdsInstId|Average|
|DRDS\_CPU利用率|%|CPUUtilization|userId、instanceId|Average|
|DRDS\_网络输入带宽|bit/s|NetworkInputTraffic|userId、instanceId|Average|
|DRDS\_网络输出带宽|bit/s|NetworkOutputTraffic|userId、instanceId|Average|

