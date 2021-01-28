# ECS

This topic describes the metrics of Elastic Compute Service \(ECS\).

-   Basic metrics

    When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

    -   Set the **Namespace** parameter to **acs\_ecs\_dashboard**.
    -   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.
    The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

    |Metric|Unit|MetricName|Dimensions|Statistics|
    |------|----|----------|----------|----------|
    |AdvanceCredit|count|AdvanceCredit|userId and instanceId|Maximum, Minimum, and Average|
    |Burst Credit|count|BurstCredit|userId and instanceId|Maximum, Minimum, and Average|
    |\(ECS\) ECS.CPUUtilization\(Not recommend\)|%|CPUUtilization|userId and instanceId|Maximum, Minimum, and Average|
    |\(ECS\) Disk Read BPS|byte/s|DiskReadBPS|userId and instanceId|Maximum, Minimum, and Average|
    |\(ECS\) ECS.SystemDiskReadOps|count/s|DiskReadIOPS|userId and instanceId|Maximum, Minimum, and Average|
    |\(ECS\) Disk Write BPS|byte/s|DiskWriteBPS|userId and instanceId|Maximum, Minimum, and Average|
    |\(ECS\) Disk Write IOPS|count/s|DiskWriteIOPS|userId and instanceId|Maximum, Minimum, and Average|
    |\(ECS\) Public Network In Band Width|bit/s|InternetInRate|userId and instanceId|Maximum, Minimum, and Average|
    |\(ECS\) Public Network Outbound Bandwidth|bit/s|InternetOutRate|userId and instanceId|Maximum, Minimum, and Average|
    |\(ECS\) Internet Outbound Bandwidth Usage|%|InternetOutRate\_Percent|userId and instanceId|Average|
    |\(ECS\) Intranet Inbound Traffic|bit/s|IntranetInRate|userId and instanceId|Maximum, Minimum, and Average|
    |\(ECS\) Intranet Outbound Bandwidth|bit/s|IntranetOutRate|userId and instanceId|Maximum, Minimum, and Average|
    |Notpaid Surplus Credit|count|NotpaidSurplusCredit|userId and instanceId|Maximum, Minimum, and Average|
    |Total Credit|count|TotlCredit|userId and instanceId|Maximum, Minimum, and Average|
    |\(ECS\) VPC-Internet Inbound Bandwidth|bit/s|VPC\_PublicIP\_InternetInRate|userId, instanceId, and ip|Maximum, Minimum, and Average|
    |\(ECS\) VPC-Internet Outbound Bandwidth|bit/s|VPC\_PublicIP\_InternetOutRate|userId, instanceId, and ip|Maximum, Minimum, and Average|
    |\(ECS\) VPC-Internet Outbound Bandwidth Usage|%|VPC\_PublicIP\_InternetOutRate\_Percent|userId, instanceId, and ip|Average|
    |concurrentConnections|count|concurrentConnections|userId and instanceId|Maximum|
    |packetInDropRates|%|packetInDropRates|userId and instanceId|Maximum|
    |packetOutDropRates|%|packetOutDropRates|userId and instanceId|Maximum|

-   Operating system metrics

    When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

    -   Set the **Namespace** parameter to **acs\_ecs\_dashboard**.
    -   Set the **Period** parameter to an integral multiple of 15s. The default value is 15s.
    The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

    |Metric|Unit|MetricName|Dimensions|Statistics|
    |------|----|----------|----------|----------|
    |\(Agent\) Host.cpu.total\(Recommend\)|%|cpu\_total|userId and instanceId|Maximum, Minimum, and Average|
    |CPU idle rate|%|cpu\_idle|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) Host.cpu.other|%|cpu\_other|userId and instanceId|Maximum, Minimum, and Average|
    |System state CPU Usage|%|cpu\_system|userId and instanceId|Maximum, Minimum, and Average|
    |User CPU Usage|%|cpu\_user|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) Host.cpu.iowait|%|cpu\_wait|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) Host.disk.readbytes|byte/s|disk\_readbytes|userId, instanceId, and device|Maximum, Minimum, and Average|
    |\(Agent\) Host.disk.readiops|count/s|disk\_readiops|userId, instanceId, and device|Maximum, Minimum, and Average|
    |\(Agent\) Host.disk.writebytes|byte/s|disk\_writebytes|userId, instanceId, and device|Maximum, Minimum, and Average|
    |\(Agent\) Host.disk.writeiops|count/s|disk\_writeiops|userId, instanceId, and device|Maximum, Minimum, and Average|
    |\(Agent\) Host.diskusage.free|byte|diskusage\_free|userId, instanceId, and device|Maximum, Minimum, and Average|
    |\(Agent\) Host.diskusage.avail|byte|diskusage\_avail|userId, instanceId, and device|Maximum, Minimum, and Average|
    |\(Agent\) Host.diskusage.total|byte|diskusage\_total|userId, instanceId, and device|Maximum, Minimum, and Average|
    |\(Agent\) Host.diskusage.used|byte|diskusage\_used|userId, instanceId, and device|Maximum, Minimum, and Average|
    |\(Agent\) Host.disk.utilization|%|diskusage\_utilization|userId, instanceId, and device|Maximum, Minimum, and Average|
    |\(Agent\) Host.FS.Inode|%|fs\_inodeutilization|userId, instanceId, and device|Maximum, Minimum, and Average|
    |\(Agent\) gpu decoder utilization|%|gpu\_decoder\_utilization|userId, instanceId, and gpuId|Maximum, Minimum, and Average|
    |\(Agent\) gpu encoder utilization|%|gpu\_encoder\_utilization|userId, instanceId, and gpuId|Maximum, Minimum, and Average|
    |\(Agent\) gpu gpu temperature|°C|gpu\_gpu\_temperature|userId, instanceId, and gpuId|Maximum, Minimum, and Average|
    |\(Agent\) gpu gpu usedutilization|%|gpu\_memory\_userdutilization|userId, instanceId, and gpuId|Maximum, Minimum, and Average|
    |\(Agent\) gpu memory freespace|byte|gpu\_memory\_freespace|userId, instanceId, and gpuId|Maximum, Minimum, and Average|
    |\(Agent\) gpu memory freeutilization|%|gpu\_memory\_freeutilization|userId, instanceId, and gpuId|Maximum, Minimum, and Average|
    |\(Agent\) gpu memory usedspace|byte|gpu\_memory\_userdspace|userId, instanceId, and gpuId|Maximum, Minimum, and Average|
    |\(Agent\) gpu memory usedutilization|%|gpu\_memory\_usedutilization|userId, instanceId, and gpuId|Maximum, Minimum, and Average|
    |\(Agent\) gpu power readings power draw|W|gpu\_power\_readings\_power\_draw|userId, instanceId, and gpuId|Maximum, Minimum, and Average|
    |\(Agent\) group gpu decoder utilization|%|group\_gpu\_decoder\_utilization|userId and groupId|Maximum, Minimum, and Average|
    |\(Agent\) group gpu encoder utilization|%|group\_gpu\_encoder\_utilization|userId and groupId|Maximum, Minimum, and Average|
    |\(Agent\) group\_gpu\_gpu\_temperature|°C|group\_gpu\_gpu\_temperature|userId and groupId|Maximum, Minimum, and Average|
    |\(Agent\) group gpu gpu usedutilization|%|group\_gpu\_gpu\_usedutilization|userId and groupId|Maximum, Minimum, and Average|
    |\(Agent\) group gpu memory freespace|byte|group\_gpu\_memory\_freespace|userId and groupId|Maximum, Minimum, and Average|
    |\(Agent\) group gpu memory freeutilization|%|group\_gpu\_memory\_freeutilization|userId and groupId|Maximum, Minimum, and Average|
    |\(Agent\) group gpu memory usedspace|byte|group\_gpu\_memory\_usedspace|userId and groupId|Maximum, Minimum, and Average|
    |\(Agent\) group gpu memory usedutilization|%|group\_gpu\_memory\_usedutilization|userId and groupId|Maximum, Minimum, and Average|
    |\(Agent\) group gpu power readings power draw|W|group\_gpu\_power\_readings\_power\_draw|userId and groupId|Maximum, Minimum, and Average|
    |\(Agent\) instance gpu decoder utilization|%|instance\_gpu\_decoder\_utilization|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) instance gpu encoder utilization|%|instance\_gpu\_encoder\_utilization|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) instance gpu gpu temperature|°C|instance\_gpu\_temperature|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) instance gpu gpu usedutilization|%|instance\_gpu\_usedutilization|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) instance gpu memory freespace|byte|instance\_gpu\_memory\_freespace|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) instance gpu memory freeutilization|%|instance\_gpu\_memory\_freeutlization|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) instance gpu memory usedspace|byte|instance\_gpu\_memory\_usedspace|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) instance gpu memory usedutilization|%|instance\_gpu\_memory\_usedutilizatioin|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) instance gpu power readings power draw|W|instance\_gpu\_power\_readings\_power\_draw|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) Host.load15|N/A|load\_15m|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) Host.load1|N/A|load\_1m|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) Host.load5|N/A|load\_5m|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) Host.mem.actualUsedSpace|byte|memory\_actualusedspace|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) Host.mem.free|byte|memory\_freespace|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) Host.mem.freeutilization|%|memory\_freeutilization|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) Host.mem.total|byte|memory\_totalspace|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) Host.mem.used|byte|memory\_usedspace|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) Host.Memory.Usedutilization|%|memory\_usedutilization|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) Host.tcpconnection|count|net\_tcpconnection|userId, instanceId, and state|Maximum, Minimum, and Average|
    |\(Agent\) Host.netin.errorpackages|count/s|networkin\_errorpackages|userId, instanceId, and device|Maximum, Minimum, and Average|
    |\(Agent\) Host.netin.packages|count/s|networkin\_packages|userId, instanceId, and device|Maximum, Minimum, and Average|
    |\(Agent\) Host.netin.rate|bit/s|networkin\_rate|userId, instanceId, and device|Maximum, Minimum, and Average|
    |\(Agent\) Host.netout.errorpackages|count/s|networkout\_errorpackages|userId, instanceId, and device|Maximum, Minimum, and Average|
    |\(Agent\) Host.netout.packages|count/s|networkout\_packages|userId, instanceId, and device|Maximum, Minimum, and Average|
    |\(Agent\) Host.netout.rate|bit/s|networkout\_rate|userId, instanceId, and device|Maximum, Minimum, and Average|
    |Host Process Number|count/min|process.number|userId, instanceId, and processName|Average|
    |\(OldAgent\)CPU Usage|%|vm.CPUUtilization|userId and instanceId|Maximum, Minimum, and Average|
    |\(OldAgent\)Disk I/O Read|byte/s|vm.DiskIORead|userId, instanceId, and diskname|Maximum, Minimum, and Average|
    |\(OldAgent\)Disk I/O Write|byte/s|vm.DiskIOWrite|userId, instanceId, and diskname|Maximum, Minimum, and Average|
    |\(OldAgent\)inode Usage|%|vm.DiskIusedUtilization|userId, instanceId, and mountpoint|Maximum, Minimum, and Average|
    |\(OldAgent\)Disk Usage|%|vm.DiskUtilization|userId, instanceId, and mountpoint|Maximum, Minimum, and Average|
    |\(OldAgent\)Average Load|N/A|vm.LoadAverage|userId, instanceId, and period|Maximum, Minimum, and Average|
    |\(OldAgent\)MemaryUtilization|%|vm.MemoryUtilization|userId and instanceId|Maximum, Minimum, and Average|
    |\(OldAgent\)Number of TCP Connections|count/min|vm.TcpCount|userId, instanceId, and state|Maximum, Minimum, and Average|
    |\(Agent\) Host.loadpercore15|N/A|load\_per\_core\_15m|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) Host.loadpercore1|N/A|load\_per\_core\_1m|userId and instanceId|Maximum, Minimum, and Average|
    |\(Agent\) Host.loadpercore5|N/A|load\_per\_core\_5m|userId and instanceId|Maximum, Minimum, and Average|


