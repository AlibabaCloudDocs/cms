# 云数据库RDS版（RDS）

通过本文您可以了解云数据库RDS版的系统事件。

|事件类型|事件名称|事件含义|事件状态|事件等级|
|----|----|----|----|----|
|Maintenance|Instance\_Failover|实例主备切换|Executed|Warn|
|Exception|Instance\_Failure\_End|实例故障结束|Executed|Critical|
|Exception|Instance\_Failure\_Start|实例故障开始|Executing|Critical|
|Maintenance|Instance:SystemMaintenance.Transfer:Scheduled|实例迁移（计划中）|Scheduled|Warn|
|Maintenance|Instance:SystemMaintenance.Transfer:Executing|实例迁移（开始执行）|Executing|Warn|
|Maintenance|Instance:SystemMaintenance.Transfer:Executed|实例迁移（执行完成）|Executed|Warn|
|Maintenance|Instance:SystemMaintenance.Transfer:Canceled|实例迁移（已取消）|Canceled|Warn|
|Maintenance|Instance:SystemMaintenance.MinorVersionUpgrade:Scheduled|实例小版本升级（计划中）|Scheduled|Warn|
|Maintenance|Instance:SystemMaintenance.MinorVersionUpgrade:Executing|实例小版本升级（开始执行）|Executing|Warn|
|Maintenance|Instance:SystemMaintenance.MinorVersionUpgrade:Executed|实例小版本升级（执行完成）|Executed|Warn|
|Maintenance|Instance:SystemMaintenance.MinorVersionUpgrade:Canceled|实例小版本升级（已取消）|Canceled|Warn|

