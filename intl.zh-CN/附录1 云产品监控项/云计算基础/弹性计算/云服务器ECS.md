# 云服务器ECS

通过本文您可以了解云服务器ECS的监控项。

-   基础监控项

    当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

    -   **Namespace**为**acs\_ecs\_dashboard**。
    -   **Period**默认为60秒，也可以为60的整数倍。
    当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

    |监控项|单位|MetricName|Dimensions|Statistics|
    |---|--|----------|----------|----------|
    |突发性能实例-预支CPU积分|Count|AdvanceCredit|userId、instanceId|Maximum、Minimum、Average|
    |突发性能实例-已消耗CPU积分|Count|BurstCredit|userId、instanceId|Maximum、Minimum、Average|
    |（ECS）CPU使用率（不推荐）|%|CPUUtilization|userId、instanceId|Maximum、Minimum、Average|
    |（ECS）系统盘总读BPS|Byte/s|DiskReadBPS|userId、instanceId|Maximum、Minimum、Average|
    |（ECS）ECS.SystemDiskReadOps|Count/Second|DiskReadIOPS|userId、instanceId|Maximum、Minimum、Average|
    |（ECS）系统盘总写BPS|Byte/s|DiskWriteBPS|userId、instanceId|Maximum、Minimum、Average|
    |（ECS）系统写IOPS|Count/Second|DiskWriteIOPS|userId、instanceId|Maximum、Minimum、Average|
    |（ECS）经典网络-公网网络入流量|Byte|InternetIn|userId、instanceId|Maximum、Minimum、Average、Sum|
    |（ECS）经典网络-公网流入带宽|bit/s|InternetInRate|userId、instanceId|Maximum、Minimum、Average|
    |（ECS）下行流量|Byte|InternetOut|userId、instanceId|Maximum、Minimum、Average、Sum|
    |（ECS）经典网络-公网流出带宽|bit/s|InternetOutRate|userId、instanceId|Maximum、Minimum、Average|
    |（ECS）经典网络-公网流出带宽使用率|%|InternetOutRate\_Percent|userId、instanceId|Average|
    |（ECS）内网流入流量|Byte|IntranetIn|userId、instanceId|Maximum、Minimum、Average、Sum|
    |（ECS）内网流入带宽|bit/s|IntranetInRate|userId、instanceId|Maximum、Minimum、Average|
    |（ECS）内网流出流量|Byte|IntranetOut|userId、instanceId|Maximum、Minimum、Average、Sum|
    |（ECS）内网流出带宽|bit/s|IntranetOutRate|userId、instanceId|Maximum、Minimum、Average|
    |突发性能实例-超额CPU积分|Count|NotpaidSurplusCredit|userId、instanceId|Maximum、Minimum、Average|
    |突发性能实例-累积CPU积分|Count|TotlCredit|userId、instanceId|Maximum、Minimum、Average|
    |（ECS）专有网络-公网流入带宽|bit/s|VPC\_PublicIP\_InternetInRate|userId、instanceId、ip|Maximum、Minimum、Average|
    |（ECS）专有网络-公网流出带宽|bit/s|VPC\_PublicIP\_InternetOutRate|userId、instanceId、ip|Maximum、Minimum、Average|
    |（ECS）专有网络-公网流出带宽使用率|%|VPC\_PublicIP\_InternetOutRate\_Percent|userId、instanceId、ip|Average|
    |ECS同时连接数|Count|concurrentConnections|userId、instanceId|Maximum|
    |EIP-网络流入带宽|bit/s|eip\_InternetInRate|userId、instanceId|Value|
    |EIP-网络流出带宽|bit/s|eip\_InternetOutRate|userId、instanceId|Value|
    |入方向前后端丢包率|%|packetInDropRates|userId、instanceId|Maximum|
    |出方向前后端丢包率|%|packetOutDropRates|userId、instanceId|Maximum|

-   操作系统级别监控项

    当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

    -   **Namespace**为**acs\_ecs\_dashboard**。
    -   **Period**默认为15秒，也可以为15的整数倍。
    当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

    |监控项|单位|MetricName|Dimensions|Statistics|
    |---|--|----------|----------|----------|
    |（Agent）Host.cpu\_total（推荐）|%|cpu\_total|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）Host.cpu.idle|%|cpu\_idle|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）Host.cpu.other|%|cpu\_other|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）Host.cpu.system|%|cpu\_system|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）Host.cpu.user|%|cpu\_user|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）Host.cpu.iowait|%|cpu\_wait|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）Host.disk.readbytes|Byte/s|disk\_readbytes|userId、instanceId、device|Maximum、Minimum、Average|
    |（Agent）Host.disk.readiops|Count/s|disk\_readiops|userId、instanceId、device|Maximum、Minimum、Average|
    |（Agent）Host.disk.writebytes|Byte/s|disk\_writebytes|userId、instanceId、device|Maximum、Minimum、Average|
    |（Agent）Host.disk.writeiops|Count/s|disk\_writeiops|userId、instanceId、device|Maximum、Minimum、Average|
    |（Agent）Host.diskusage.free|Byte|diskusage\_free|userId、instanceId、device|Maximum、Minimum、Average|
    |（Agent）Host.diskusage.avail|Byte|diskusage\_avail|userId、instanceId、device|Maximum、Minimum、Average|
    |（Agent）Host.diskusage.total|Byte|diskusage\_total|userId、instanceId、device|Maximum、Minimum、Average|
    |（Agent）Host.diskusage.used|Byte|diskusage\_used|userId、instanceId、device|Maximum、Minimum、Average|
    |（Agent）Host.disk.utilization|%|diskusage\_utilization|userId、instanceId、device|Maximum、Minimum、Average|
    |（Agent）Host.fs.inode|%|fs\_inodeutilization|userId、instanceId、device|Maximum、Minimum、Average|
    |（Agent）GPU维度解码器使用率|%|gpu\_decoder\_utilization|userId、instanceId、gpuId|Maximum、Minimum、Average|
    |（Agent）GPU维度编码器使用率|%|gpu\_encoder\_utilization|userId、instanceId、gpuId|Maximum、Minimum、Average|
    |（Agent）GPU维度GPU温度|℃|gpu\_gpu\_temperature|userId、instanceId、gpuId|Maximum、Minimum、Average|
    |（Agent）GPU维度GPU使用率|%|gpu\_memory\_userdutilization|userId、instanceId、gpuId|Maximum、Minimum、Average|
    |（Agent）GPU维度显存空闲量|Byte|gpu\_memory\_freespace|userId、instanceId、gpuId|Maximum、Minimum、Average|
    |（Agent）GPU维度显存空闲率|%|gpu\_memory\_freeutilization|userId、instanceId、gpuId|Maximum、Minimum、Average|
    |（Agent）GPU维度显存使用量|Byte|gpu\_memory\_userdspace|userId、instanceId、gpuId|Maximum、Minimum、Average|
    |（Agent）GPU维度显存使用率|%|gpu\_memory\_usedutilization|userId、instanceId、gpuId|Maximum、Minimum、Average|
    |（Agent）GPU维度GPU功率|W|gpu\_power\_readings\_power\_draw|userId、instanceId、gpuId|Maximum、Minimum、Average|
    |（Agent）分组维度解码器使用率|%|group\_gpu\_decoder\_utilization|userId、groupId|Maximum、Minimum、Average|
    |（Agent）分组维度编码器使用率|%|group\_gpu\_encoder\_utilization|userId、groupId|Maximum、Minimum、Average|
    |（Agent）分组维度GPU温度|℃|group\_gpu\_gpu\_temperature|userId、groupId|Maximum、Minimum、Average|
    |（Agent）分组维度GPU使用率|%|group\_gpu\_gpu\_usedutilization|userId、groupId|Maximum、Minimum、Average|
    |（Agent）分组维度显存空闲量|Byte|group\_gpu\_memory\_freespace|userId、groupId|Maximum、Minimum、Average|
    |（Agent）分组维度显存空闲率|%|group\_gpu\_memory\_freeutilization|userId、groupId|Maximum、Minimum、Average|
    |（Agent）分组维度显存使用量|Byte|group\_gpu\_memory\_usedspace|userId、groupId|Maximum、Minimum、Average|
    |（Agent）分组维度显存使用率|%|group\_gpu\_memory\_usedutilization|userId、groupId|Maximum、Minimum、Average|
    |（Agent）分组维度GPU功率|W|group\_gpu\_power\_readings\_power\_draw|userId、groupId|Maximum、Minimum、Average|
    |（Agent）实例维度解码器使用率|%|instance\_gpu\_decoder\_utilization|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）实例维度编码器使用率|%|instance\_gpu\_encoder\_utilization|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）实例维度GPU温度|℃|instance\_gpu\_temperature|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）实例维度GPU使用率|%|instance\_gpu\_usedutilization|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）实例维度显存空闲量|Byte|instance\_gpu\_memory\_freespace|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）实例维度显存空闲率|%|instance\_gpu\_memory\_freeutlization|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）实例维度显存使用量|Byte|instance\_gpu\_memory\_usedspace|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）实例维度显存使用率|%|instance\_gpu\_memory\_usedutilizatioin|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）实例维度GPU功率|W|instance\_gpu\_power\_readings\_power\_draw|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）Host.load15|无|load\_15m|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）Host.load1|无|load\_1m|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）Host.load5|无|load\_5m|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）Host.mem.actualUsedSpace|Byte|memory\_actualusedspace|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）Host.mem.free|Byte|memory\_freespace|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）Host.mem.freeutilization|%|memory\_freeutilization|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）Host.mem.total|Byte|memory\_totalspace|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）Host.mem.used|Byte|memory\_usedspace|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）Host.mem.usedutilization|%|memory\_usedutilization|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）Host.tcpconnection|Count|net\_tcpconnection|userId、instanceId、state|Maximum、Minimum、Average|
    |（Agent）Host.netin.errorpackage|Count/s|networkin\_errorpackages|userId、instanceId、device|Maximum、Minimum、Average|
    |（Agent）Host.netin.packages|Count/s|networkin\_packages|userId、instanceId、device|Maximum、Minimum、Average|
    |（Agent）Host.netin.rate|bit/s|networkin\_rate|userId、instanceId、device|Maximum、Minimum、Average|
    |（Agent）Host.netout.errorpackages|Count/s|networkout\_errorpackages|userId、instanceId、device|Maximum、Minimum、Average|
    |（Agent）Host.netout.packages|Count/s|networkout\_packages|userId、instanceId、device|Maximum、Minimum、Average|
    |（Agent）Host.netout.rate|bit/s|networkout\_rate|userId、instanceId、device|Maximum、Minimum、Average|
    |进程数|Count/Min|process.number|userId、instanceId、processName|Average|
    |（旧版Agent）CPU使用率|%|vm.CPUUtilization|userId、instanceId|Maximum、Minimum、Average|
    |（旧版Agent）磁盘IO读|Byte/s|vm.DiskIORead|userId、instanceId、diskname|Maximum、Minimum、Average|
    |（旧版Agent）磁盘IO写|Byte/s|vm.DiskIOWrite|userId、instanceId、diskname|Maximum、Minimum、Average|
    |（旧版Agent）inode使用率|%|vm.DiskIusedUtilization|userId、instanceId、mountpoint|Maximum、Minimum、Average|
    |（旧版Agent）磁盘使用率|%|vm.DiskUtilization|userId、instanceId、mountpoint|Maximum、Minimum、Average|
    |（旧版Agent）平均负载|无|vm.LoadAverage|userId、instanceId、period|Maximum、Minimum、Average|
    |（旧版Agent）内存使用率|%|vm.MemoryUtilization|userId、instanceId|Maximum、Minimum、Average|
    |（旧版Agent）进程数|Count/Min|vm.Process.number|userId、instanceId、processName|Maximum、Minimum、Average|
    |（旧版Agent）进程总数|Count/Min|vm.ProcessCount|userId、instanceId|Maximum、Minimum、Average|
    |（旧版Agent）TCP连接数|Count/Min|vm.TcpCount|userId、instanceId、state|Maximum、Minimum、Average|
    |（Agent）Host.loadpercore15|无|load\_per\_core\_15m|userId、instanceId|Maximum、Minimum、Average|
    |（Agent） Host.loadpercore1|无|load\_per\_core\_1m|userId、instanceId|Maximum、Minimum、Average|
    |（Agent）Host.loadpercore5|无|load\_per\_core\_5m|userId、instanceId|Maximum、Minimum、Average|


