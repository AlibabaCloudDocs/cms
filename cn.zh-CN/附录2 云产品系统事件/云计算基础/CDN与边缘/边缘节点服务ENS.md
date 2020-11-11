# 边缘节点服务ENS

通过本文您可以了解边缘节点服务ENS的系统事件。

|事件类型|事件名称|事件含义|事件状态|事件等级|
|----|----|----|----|----|
|Exception|Disk:Stalled:Executed|磁盘性能受限结束|Executed|Critical|
|Exception|Disk:Stalled:Executing|磁盘性能受限开始|Executing|Critical|
|Notice|EnsInstance:Create:Executed|实例创建完成|Executed|Critical|
|Notice|EnsInstance:Delete:Executed|实例删除完成|Executed|Critical|
|Exception|EnsRegion:NetworkDown:Executed|节点网络恢复|Executed|Critical|
|Exception|EnsRegion:NetworkDown:Executing|节点网络失联|Executing|Critical|
|Maintenance|EnsRegion:NetworkMigration:Canceled|边缘节点网络割接取消|Canceled|Info|
|Maintenance|EnsRegion:NetworkMigration:Executed|边缘节点网络割接完成|Executed|Info|
|Maintenance|EnsRegion:NetworkMigration:Executing|边缘节点网络割接执行|Executing|Critical|
|Maintenance|EnsRegion:NetworkMigration:Scheduled|边缘节点网络割接计划|Scheduled|Warn|
|Executed|EnsRegion:NetworkWaterLevel:Executed|ENS节点带宽水位恢复|Executed|Warn|
|Executing|EnsRegion:NetworkWaterLevel:Executing|ENS节点带宽水位异常|Executing|Warn|
|Exception|EnsRegion:PortError:Executed|节点端口恢复|Executed|Critical|
|Exception|EnsRegion:PortError:Executing|节点端口异常|Executing|Critical|
|Exception|Instance:SystemFailure.Reboot:Executed|实例重启完成（系统问题导致）|Executed|Critical|
|Exception|Instance:SystemFailure.Reboot:Executing|实例重启执行中（系统问题导致）|Executing|Critical|

