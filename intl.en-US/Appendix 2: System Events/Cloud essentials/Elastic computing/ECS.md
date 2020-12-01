# ECS

This topic describes the system events of Elastic Compute Service \(ECS\).

|Type|Event name|Description|State|Level|Description|
|----|----------|-----------|-----|-----|-----------|
|StatusNotification|Disk:ConvertToPostpaidCompleted|The billing method of the disk is changed to pay-as-you-go.|Normal|Info|None.|
|StatusNotification|Disk:DiskOperationCompleted|The operation on the disk is completed.|Normal|Info|None.|
|Exception|Disk:ErrorDetected:Executed|The alert about the damage to the local disk starts.|Executed|Critical|None.|
|Exception|Disk:ErrorDetected:Executing|The alert about the damage to the local disk ends.|Executing|Critical|None.|
|StatusNotification|Disk:OverduePaymentRelease|The disk is released due to overdue payments of the account.|Normal|Critical|None.|
|Exception|Disk:Stalled:Executed|The impact on the disk performance ends.|Executed|Critical|None.|
|Exception|Disk:Stalled:Executing|The impact on the disk performance starts.|Executing|Critical|None.|
|StatusNotification|Instance:BurstablePerformanceRestricted|The performance of the burstable instance is restricted.|Normal|Warn|None.|
|Exception|Instance:InstanceFailure.Reboot:Executed|The instance reboot that is caused by an instance error is completed.|Executed|Critical|None.|
|Exception|Instance:InstanceFailure.Reboot:Executing|The instance reboot that is caused by an instance error starts.|Executing|Critical|None.|
|StatusNotification|Instance:LiveMigrationAcrossDDH|An instance is hot migrated between dedicated hosts.|N/A|Info|None.|
|StatusNotification|Instance:PerformanceModeChange|The performance mode of the burstable instance is changed.|Normal|Info|None.|
|StatusNotification|Instance:PreemptibleInstanceInterruption|The preemptible instance is interrupted.|Normal|Warn|If the market price is higher than your bid or the resources are insufficient, your preemptible instance enters the To Be Released state. For more information, see [Overview](/intl.en-US/Instance/Instance purchasing options/Preemptible instances/Overview.md).|
|Exception|Instance:Security.TpmAlert:Executed|The Trusted Platform Module \(TPM\) security alert ends.|Executed|Warn|None.|
|Exception|Instance:Security.TpmAlert:Executing|The TPM security alert starts.|Executing|Warn|None.|
|StatusNotification|Instance:StateChange|The status of the instance is changed.|Normal|Info|The event details contain the status of the instance. An instance can be in one of the following states:-   Running.
-   Stopped: The instance enters the Stopped status if it is stopped, expired, about to expire, locked, and waiting for being released.
-   Deleted: The instance is released.

For more information, see [ECS instance lifecycle](/intl.en-US/Instance/ECS instance lifecycle.md). |
|Exception|Instance:SystemFailure.Delete:Avoided|The automatic instance release that is caused by an instance creation failure is bypassed.|Avoided|Critical|None.|
|Exception|Instance:SystemFailure.Delete:Executed|The automatic instance release that is caused by an instance creation failure is completed.|Executed|Critical|None.|
|Exception|Instance:SystemFailure.Delete:Executing|The automatic instance release that is caused by an instance creation failure is being executed.|Executing|Critical|None.|
|Exception|Instance:SystemFailure.Reboot:Executed|The instance reboot that is caused by a system error is completed.|Executed|Critical|None.|
|Exception|Instance:SystemFailure.Reboot:Executing|The instance reboot that is caused by a system error starts.|Executing|Critical|None.|
|Exception|Instance:SystemFailure.Reboot:Failed|The instance reboot that is caused by a system error fails.|Failed|Critical|None.|
|Exception|Instance:SystemFailure.Redeploy:Avoided|The instance redeployment that is caused by a system error is bypassed.|Avoided|Critical|None.|
|Exception|Instance:SystemFailure.Redeploy:Canceled|The instance redeployment that is caused by a system error is canceled.|Canceled|Critical|None.|
|Exception|Instance:SystemFailure.Redeploy:Executed|The instance redeployment that is caused by a system error is completed.|Executed|Critical|None.|
|Exception|Instance:SystemFailure.Redeploy:Executing|The instance redeployment that is caused by a system error is being executed.|Executing|Critical|None.|
|Exception|Instance:SystemFailure.Redeploy:Scheduled|The instance redeployment that is caused by a system error is scheduled.|Scheduled|Critical|None.|
|Maintenance|Instance:SystemMaintenance.IsolateErrorDisk:Avoided|The damaged-disk isolation that is caused by system maintenance is bypassed.|Avoided|Critical|None.|
|Maintenance|Instance:SystemMaintenance.IsolateErrorDisk:Canceled|The damaged-disk isolation that is caused by system maintenance is canceled.|Canceled|Critical|None.|
|Maintenance|Instance:SystemMaintenance.IsolateErrorDisk:Executed|The damaged-disk isolation that is caused by system maintenance is completed.|Executed|Critical|None.|
|Maintenance|Instance:SystemMaintenance.IsolateErrorDisk:Executing|The damaged-disk isolation that is caused by system maintenance is being executed.|Executing|Critical|None.|
|Maintenance|Instance:SystemMaintenance.IsolateErrorDisk:Failed|The damaged-disk isolation that is caused by system maintenance fails.|Failed|Critical|None.|
|Maintenance|Instance:SystemMaintenance.IsolateErrorDisk:Inquiring|The damaged-disk isolation that is caused by system maintenance is waiting for your confirmation.|Inquiring|Critical|None.|
|Maintenance|Instance:SystemMaintenance.PerformanceImpact:Executed|The potential impact of system maintenance on the instance performance ends.|Executed|Warn|None.|
|Maintenance|Instance:SystemMaintenance.PerformanceImpact:Executing|The potential impact of system maintenance on the instance performance starts.|Executing|Warn|None.|
|Maintenance|Instance:SystemMaintenance.ReInitErrorDisk:Avoided|The damaged-disk reinitialization that is caused by system maintenance is bypassed.|Avoided|Critical|None.|
|Maintenance|Instance:SystemMaintenance.ReInitErrorDisk:Canceled|The damaged-disk reinitialization that is caused by system maintenance is canceled.|Canceled|Critical|None.|
|Maintenance|Instance:SystemMaintenance.ReInitErrorDisk:Executed|The damaged-disk reinitialization that is caused by system maintenance is completed.|Executed|Critical|None.|
|Maintenance|Instance:SystemMaintenance.ReInitErrorDisk:Executing|The damaged-disk reinitialization that is caused by system maintenance is being executed.|Executing|Critical|None.|
|Maintenance|Instance:SystemMaintenance.ReInitErrorDisk:Failed|The damaged-disk reinitialization that is caused by system maintenance fails.|Failed|Critical|None.|
|Maintenance|Instance:SystemMaintenance.ReInitErrorDisk:Inquiring|The damaged-disk reinitialization that is caused by system maintenance is waiting for your confirmation.|Inquiring|Critical|None.|
|Maintenance|Instance:SystemMaintenance.Reboot:Avoided|The scheduled instance reboot that is caused by system maintenance is bypassed.|Avoided|Critical|None.|
|Maintenance|Instance:SystemMaintenance.Reboot:Canceled|The scheduled instance reboot that is caused by system maintenance is canceled.|Canceled|Critical|None.|
|Maintenance|Instance:SystemMaintenance.Reboot:Executed|The scheduled instance reboot that is caused by system maintenance is completed.|Executed|Critical|None.|
|Maintenance|Instance:SystemMaintenance.Reboot:Executing|The scheduled instance reboot that is caused by system maintenance is being executed.|Executing|Critical|None.|
|Maintenance|Instance:SystemMaintenance.Reboot:Failed|The scheduled instance reboot that is caused by system maintenance fails.|Failed|Critical|None.|
|Maintenance|Instance:SystemMaintenance.Reboot:Inquiring|The scheduled instance reboot that is caused by system maintenance is waiting for your confirmation.|Inquiring|Critical|None.|
|Maintenance|Instance:SystemMaintenance.Reboot:Scheduled|The instance reboot that is caused by system maintenance is scheduled.|Scheduled|Critical|None.|
|Maintenance|Instance:SystemMaintenance.RebootAndIsolateErrorDisk:Avoided|The instance reboot and damaged-disk isolation that are caused by system maintenance are bypassed.|Avoided|Critical|None.|
|Maintenance|Instance:SystemMaintenance.RebootAndIsolateErrorDisk:Canceled|The instance reboot and damaged-disk isolation that are caused by system maintenance are canceled.|Canceled|Critical|None.|
|Maintenance|Instance:SystemMaintenance.RebootAndIsolateErrorDisk:Executed|The instance reboot and damaged-disk isolation that are caused by system maintenance are complete.|Executed|Critical|None.|
|Maintenance|Instance:SystemMaintenance.RebootAndIsolateErrorDisk:Executing|The instance reboot and damaged-disk isolation that are caused by system maintenance are being executed.|Executing|Critical|None.|
|Maintenance|Instance:SystemMaintenance.RebootAndIsolateErrorDisk:Inquiring|The instance reboot and damaged-disk isolation that are caused by system maintenance are waiting for your confirmation.|Inquiring|Critical|None.|
|Maintenance|Instance:SystemMaintenance.RebootAndReInitErrorDisk:Avoided|The instance reboot and damaged-disk reinitialization that are caused by system maintenance are bypassed.|Avoided|Critical|None.|
|Maintenance|Instance:SystemMaintenance.RebootAndReInitErrorDisk:Canceled|The instance reboot and damaged-disk reinitialization that are caused by system maintenance are canceled.|Canceled|Critical|None.|
|Maintenance|Instance:SystemMaintenance.RebootAndReInitErrorDisk:Executed|The instance reboot and damaged-disk reinitialization that are caused by system maintenance are completed.|Executed|Critical|None.|
|Maintenance|Instance:SystemMaintenance.RebootAndReInitErrorDisk:Executing|The instance reboot and damaged-disk reinitialization that are caused by system maintenance are being executed.|Executing|Critical|None.|
|Maintenance|Instance:SystemMaintenance.RebootAndReInitErrorDisk:Inquiring|The instance reboot and damaged-disk reinitialization that are caused by system maintenance are waiting for your confirmation.|Inquiring|Critical|None.|
|Maintenance|Instance:SystemMaintenance.Redeploy:Avoided|The scheduled instance redeployment that is caused by system maintenance is bypassed.|Avoided|Critical|None.|
|Maintenance|Instance:SystemMaintenance.Redeploy:Canceled|The scheduled instance redeployment that is caused by system maintenance is canceled.|Canceled|Critical|None.|
|Maintenance|Instance:SystemMaintenance.Redeploy:Executed|The scheduled instance redeployment that is caused by system maintenance is completed.|Executed|Critical|None.|
|Maintenance|Instance:SystemMaintenance.Redeploy:Executing|The scheduled instance redeployment that is caused by system maintenance is being executed.|Executing|Critical|None.|
|Maintenance|Instance:SystemMaintenance.Redeploy:Inquiring|The scheduled instance redeployment that is caused by system maintenance is waiting for your confirmation.|Inquiring|Critical|None.|
|Maintenance|Instance:SystemMaintenance.Redeploy:Scheduled|The instance redeployment that is caused by system maintenance is scheduled.|Scheduled|Critical|None.|
|StatusNotification|Snapshot:CreateSnapshotCompleted|The disk snapshot is created.|Normal|Info|None.|
|Maintenance|Instance:SystemMaintenance.Stop:Avoided|The scheduled instance stop that is caused by system maintenance is bypassed.|Avoided|Critical|None.|
|Maintenance|Instance:SystemMaintenance.Stop:Canceled|The scheduled instance stop that is caused by system maintenance is canceled.|Canceled|Critical|None.|
|Maintenance|Instance:SystemMaintenance.Stop:Executed|The scheduled instance stop that is caused by system maintenance is completed.|Executed|Critical|None.|
|Maintenance|Instance:SystemMaintenance.Stop:Executing|The scheduled instance stop that is caused by system maintenance is being executed.|Executing|Critical|None.|
|Maintenance|Instance:SystemMaintenance.Stop:Failed|The scheduled instance stop that is caused by system maintenance fails.|Failed|Critical|None.|
|Maintenance|Instance:SystemMaintenance.Stop:Scheduled|The instance stop that is caused by system maintenance is scheduled.|Scheduled|Critical|None.|
|Exception|Instance:SystemFailure.Stop:Executed|The instance stop that is caused by a system error is completed.|Executed|Critical|None.|
|Exception|Instance:SystemFailure.Stop:Executing|The instance stop that is caused by a system error starts.|Executing|Critical|None.|

