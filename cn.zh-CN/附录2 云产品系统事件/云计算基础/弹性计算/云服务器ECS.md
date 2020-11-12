# 云服务器ECS

通过本文您可以了解云服务器ECS的系统事件。

|事件类型|事件名称|事件含义|事件状态|事件等级|说明|
|----|----|----|----|----|--|
|StatusNotification|Disk:ConvertToPostpaidCompleted|转换磁盘到按量付费完成|Normal|Info|无|
|StatusNotification|Disk:DiskOperationCompleted|磁盘操作完成|Normal|Info|无|
|Exception|Disk:ErrorDetected:Executed|本地磁盘出现损坏告警结束|Executed|Critical|无|
|Exception|Disk:ErrorDetected:Executing|本地磁盘出现损坏告警开始|Executing|Critical|无|
|StatusNotification|Disk:OverduePaymentRelease|磁盘释放（账号欠费）|Normal|Critical|无|
|Exception|Disk:Stalled:Executed|磁盘性能受到严重影响结束|Executed|Critical|无|
|Exception|Disk:Stalled:Executing|磁盘性能受到严重影响开始|Executing|Critical|无|
|StatusNotification|Instance:BurstablePerformanceRestricted|突发性能实例性能受限|Normal|Warn|无|
|Exception|Instance:InstanceFailure.Reboot:Executed|实例重启结束（实例错误）|Executed|Critical|无|
|Exception|Instance:InstanceFailure.Reboot:Executing|实例重启开始（实例错误）|Executing|Critical|无|
|StatusNotification|Instance:LiveMigrationAcrossDDH|实例在专有宿主机间热迁移|无|Info|无|
|StatusNotification|Instance:PerformanceModeChange|突发性能实例性能模式切换|Normal|Info|无|
|StatusNotification|Instance:PreemptibleInstanceInterruption|抢占式实例中断通知|Normal|Warn|如果市场价格高于您的出价或资源供需关系发生变化等，则会导致抢占式实例进入待回收状态，请参见[抢占式实例概述](/cn.zh-CN/实例/选择实例购买方式/抢占式实例/抢占式实例概述.md)。|
|Exception|Instance:Security.TpmAlert:Executed|TPM安全警告结束|Executed|Warn|无|
|Exception|Instance:Security.TpmAlert:Executing|TPM安全警告开始|Executing|Warn|无|
|StatusNotification|Instance:StateChange|实例状态改变通知|Normal|Info|事件详情中会展示实例的具体状态。状态如下：-   Running：运行中
-   Stopped：已停止、已过期、即将过期、已锁定、欠费回收中、等待释放
-   Deleted：实例已释放

具体的实例生命周期说明，请参见[实例生命周期介绍](/cn.zh-CN/实例/实例生命周期介绍.md)。 |
|Exception|Instance:SystemFailure.Delete:Avoided|实例自动释放已规避（实例创建失败）|Avoided|Critical|无|
|Exception|Instance:SystemFailure.Delete:Executed|实例自动释放已完成（实例创建失败）|Executed|Critical|无|
|Exception|Instance:SystemFailure.Delete:Executing|实例自动释放执行中（实例创建失败）|Executing|Critical|无|
|Exception|Instance:SystemFailure.Reboot:Executed|实例重启结束（系统错误）|Executed|Critical|无|
|Exception|Instance:SystemFailure.Reboot:Executing|实例重启开始（系统错误）|Executing|Critical|无|
|Exception|Instance:SystemFailure.Reboot:Failed|实例重启失败（系统错误）|Failed|Critical|无|
|Exception|Instance:SystemFailure.Redeploy:Avoided|实例重新部署已规避（系统错误）|Avoided|Critical|无|
|Exception|Instance:SystemFailure.Redeploy:Canceled|实例重新部署已取消（系统错误）|Canceled|Critical|无|
|Exception|Instance:SystemFailure.Redeploy:Executed|实例重新部署已完成（系统错误）|Executed|Critical|无|
|Exception|Instance:SystemFailure.Redeploy:Executing|实例重新部署执行中（系统错误）|Executing|Critical|无|
|Exception|Instance:SystemFailure.Redeploy:Scheduled|实例计划重新部署通知（系统错误）|Scheduled|Critical|无|
|Maintenance|Instance:SystemMaintenance.IsolateErrorDisk:Avoided|因系统维护隔离坏盘已规避|Avoided|Critical|无|
|Maintenance|Instance:SystemMaintenance.IsolateErrorDisk:Canceled|因系统维护隔离坏盘已取消|Canceled|Critical|无|
|Maintenance|Instance:SystemMaintenance.IsolateErrorDisk:Executed|因系统维护隔离坏盘已完成|Executed|Critical|无|
|Maintenance|Instance:SystemMaintenance.IsolateErrorDisk:Executing|因系统维护隔离坏盘执行中|Executing|Critical|无|
|Maintenance|Instance:SystemMaintenance.IsolateErrorDisk:Failed|因系统维护隔离坏盘已失败|Failed|Critical|无|
|Maintenance|Instance:SystemMaintenance.IsolateErrorDisk:Inquiring|因系统维护隔离坏盘问询中|Inquiring|Critical|无|
|Maintenance|Instance:SystemMaintenance.PerformanceImpact:Executed|实例性能潜在影响结束（系统维护）|Executed|Warn|无|
|Maintenance|Instance:SystemMaintenance.PerformanceImpact:Executing|实例性能潜在影响开始（系统维护）|Executing|Warn|无|
|Maintenance|Instance:SystemMaintenance.ReInitErrorDisk:Avoided|因系统维护重新初始化坏盘已规避|Avoided|Critical|无|
|Maintenance|Instance:SystemMaintenance.ReInitErrorDisk:Canceled|因系统维护重新初始化坏盘已取消|Canceled|Critical|无|
|Maintenance|Instance:SystemMaintenance.ReInitErrorDisk:Executed|因系统维护重新初始化坏盘已完成|Executed|Critical|无|
|Maintenance|Instance:SystemMaintenance.ReInitErrorDisk:Executing|因系统维护重新初始化坏盘执行中|Executing|Critical|无|
|Maintenance|Instance:SystemMaintenance.ReInitErrorDisk:Failed|因系统维护重新初始化坏盘已失败|Failed|Critical|无|
|Maintenance|Instance:SystemMaintenance.ReInitErrorDisk:Inquiring|因系统维护重新初始化坏盘问询中|Inquiring|Critical|无|
|Maintenance|Instance:SystemMaintenance.Reboot:Avoided|实例计划重启规避（系统维护）|Avoided|Critical|无|
|Maintenance|Instance:SystemMaintenance.Reboot:Canceled|实例计划重启取消（系统维护）|Canceled|Critical|无|
|Maintenance|Instance:SystemMaintenance.Reboot:Executed|实例计划重启已完成（系统维护）|Executed|Critical|无|
|Maintenance|Instance:SystemMaintenance.Reboot:Executing|实例计划重启执行中（系统维护）|Executing|Critical|无|
|Maintenance|Instance:SystemMaintenance.Reboot:Failed|实例计划重启失败（系统维护）|Failed|Critical|无|
|Maintenance|Instance:SystemMaintenance.Reboot:Inquiring|实例计划重启问询中（系统维护）|Inquiring|Critical|无|
|Maintenance|Instance:SystemMaintenance.Reboot:Scheduled|实例计划重启通知（系统维护）|Scheduled|Critical|无|
|Maintenance|Instance:SystemMaintenance.RebootAndIsolateErrorDisk:Avoided|因系统维护重启实例并隔离坏盘已规避|Avoided|Critical|无|
|Maintenance|Instance:SystemMaintenance.RebootAndIsolateErrorDisk:Canceled|因系统维护重启实例并隔离坏盘已取消|Canceled|Critical|无|
|Maintenance|Instance:SystemMaintenance.RebootAndIsolateErrorDisk:Executed|因系统维护重启实例并隔离坏盘已完成|Executed|Critical|无|
|Maintenance|Instance:SystemMaintenance.RebootAndIsolateErrorDisk:Executing|因系统维护重启实例并隔离坏盘执行中|Executing|Critical|无|
|Maintenance|Instance:SystemMaintenance.RebootAndIsolateErrorDisk:Inquiring|因系统维护重启实例并隔离坏盘问询中|Inquiring|Critical|无|
|Maintenance|Instance:SystemMaintenance.RebootAndReInitErrorDisk:Avoided|因系统维护重启实例并重新初始化坏盘已规避|Avoided|Critical|无|
|Maintenance|Instance:SystemMaintenance.RebootAndReInitErrorDisk:Canceled|因系统维护重启实例并重新初始化坏盘已取消|Canceled|Critical|无|
|Maintenance|Instance:SystemMaintenance.RebootAndReInitErrorDisk:Executed|因系统维护重启实例并重新初始化坏盘已完成|Executed|Critical|无|
|Maintenance|Instance:SystemMaintenance.RebootAndReInitErrorDisk:Executing|因系统维护重启实例并重新初始化坏盘执行中|Executing|Critical|无|
|Maintenance|Instance:SystemMaintenance.RebootAndReInitErrorDisk:Inquiring|因系统维护重启实例并重新初始化坏盘问询中|Inquiring|Critical|无|
|Maintenance|Instance:SystemMaintenance.Redeploy:Avoided|实例计划重新部署已规避（系统维护）|Avoided|Critical|无|
|Maintenance|Instance:SystemMaintenance.Redeploy:Canceled|实例计划重新部署已取消（系统维护）|Canceled|Critical|无|
|Maintenance|Instance:SystemMaintenance.Redeploy:Executed|实例计划重新部署已完成（系统维护）|Executed|Critical|无|
|Maintenance|Instance:SystemMaintenance.Redeploy:Executing|实例计划重新部署执行中（系统维护）|Executing|Critical|无|
|Maintenance|Instance:SystemMaintenance.Redeploy:Inquiring|实例计划重新部署问询中（系统维护）|Inquiring|Critical|无|
|Maintenance|Instance:SystemMaintenance.Redeploy:Scheduled|实例计划重新部署通知（系统维护）|Scheduled|Critical|无|
|StatusNotification|Snapshot:CreateSnapshotCompleted|磁盘快照创建完成|Normal|Info|无|
|Maintenance|Instance:SystemMaintenance.Stop:Avoided|实例计划停止规避（系统维护）|Avoided|Critical|无|
|Maintenance|Instance:SystemMaintenance.Stop:Canceled|实例计划停止取消（系统维护）|Canceled|Critical|无|
|Maintenance|Instance:SystemMaintenance.Stop:Executed|实例计划停止已完成（系统维护）|Executed|Critical|无|
|Maintenance|Instance:SystemMaintenance.Stop:Executing|实例计划停止执行中（系统维护）|Executing|Critical|无|
|Maintenance|Instance:SystemMaintenance.Stop:Failed|实例计划停止失败（系统维护）|Failed|Critical|无|
|Maintenance|Instance:SystemMaintenance.Stop:Scheduled|实例计划停止通知（系统维护）|Scheduled|Critical|无|
|Exception|Instance:SystemFailure.Stop:Executed|实例停止已完成（系统错误）|Executed|Critical|无|
|Exception|Instance:SystemFailure.Stop:Executing|实例停止开始（系统错误）|Executing|Critical|无|

