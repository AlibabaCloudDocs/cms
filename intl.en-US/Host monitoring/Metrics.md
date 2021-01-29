# Metrics

Metrics that the host monitoring feature supports include operating system metrics, of which data is collected by the Cloud Monitor agent, and Elastic Compute Service \(ECS\) basic metrics. The Cloud Monitor agent collects data of operating system metrics every 15 seconds. Cloud Monitor collects data of ECS basic metrics every minute.

**Note:** The data of operating system metrics may be inconsistent with the data of ECS basic metrics due to the following causes:

-   Different monitoring frequencies: The monitoring data displayed on a monitoring chart is the average value of metric data collected in a statistical period. The statistical period is 15 seconds for operating system metrics and 1 minute for ECS basic metrics. If metric data fluctuates sharply, the values of ECS basic metrics are smaller than those of operating system metrics.
-   Different monitored objects: The network traffic data collected based on ECS basic metrics is used for billing. The data does not include the free traffic between ECS instances and Server Load Balancer \(SLB\) instances. The network traffic data collected by the Cloud Monitor agent is the actual network traffic of each network interface card \(NIC\). Therefore, the network traffic data collected by the Cloud Monitor agent is greater than that collected based on ECS basic metrics. In this case, the data that the Cloud Monitor agent collects is greater than the purchased bandwidth or traffic quota.

## Operating system metrics

-   CPU metrics

    -   Linux

        You can check the output of the top command to understand the metrics described in the following table.

    -   Windows

        Call the NtQuerySystemInformation function in ntdll.dll to obtain the CPU time consumed by each process or thread. Call this function again after a duration to obtain the CPU time and calculate the CPU utilization of each process or thread in this duration.

    |Metric|Description|Unit|Remarks for Linux|
    |:-----|:----------|:---|:----------------|
    |Host.cpu.idle|The percentage of the CPU that is idle.|%|Measures the CPU that is in the idle status.|
    |Host.cpu.system|The percentage of the CPU that is occupied by the kernel.|%|Measures the CPU consumed by a system context switch. A high value indicates that excessive processes or threads run on the host.|
    |Host.cpu.user|The percentage of the CPU that is occupied by user processes.|%|Measures the CPU occupied by user processes.|
    |Host.cpu.iowait|The percentage of the CPU that waits for I/O operations to complete.|%|A high value indicates frequent I/O operations.|
    |Host.cpu.other|The percentage of the CPU that is occupied by other operations.|%|Calculation method: CPU utilization of Nice + CPU utilization of SoftIrq + CPU utilization of Irq + CPU utilization of Stolen.|
    |Host.cpu.total|The percentage of the CPU that is occupied.|%|The sum of the preceding CPU consumption. This metric is typically used for alerting.|

-   Memory metrics

    -   Linux

        You can check the output of the free command to understand the metrics described in the following table. The free command obtains memory information from the /proc/meminfo file.

    -   Windows

        Call the GlobalMemoryStatusEx function in kernel32.dll to obtain the current physical and virtual memory usage in a 32-bit Windows operating system.

    |Metric|Description|Unit|Remarks for Linux|
    |:-----|:----------|:---|:----------------|
    |Host.mem.total|The total memory.|byte|The total memory size of the host.

Data source: the value of MemTotal in the /proc/meminfo file. |
    |Host.mem.free|The amount of available memory.|byte|The amount of available memory in the system.

Data source: the value of MemFree in the /proc/meminfo file. |
    |Host.mem.used|The amount of memory in use.|byte|The amount of used memory in the system.

Calculation method: total - free. |
    |Host.mem.actualused|The memory used by users.|byte|Calculation method:     -   When MemAvailable exists in the /proc/meminfo file: total - MemAvailable.
    -   When MemAvailable does not exist in the /proc/meminfo file: used - buffers - cached.
**Note:** The calculation result is more accurate in CentOS 7.2, Ubuntu 16.04, or their later versions that use the new Linux kernel. For more information about MemAvailable, visit [commit](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=34e431b0ae398fc54ea69ff85ec700722c9da773). |
    |Host.mem.freeutilization|The percentage of available memory.|%|Calculation method:     -   When MemAvailable exists in the /proc/meminfo file: MemAvailable/total × 100%.
    -   When MemAvailable does not exist in the /proc/meminfo file: \(total - actualused\)/total × 100%. |
    |Host.mem.usedutilization|The memory usage.|%|Calculation method:     -   When MemAvailable exists in the /proc/meminfo file: \(total - MemAvailable\)/total × 100%.
    -   When MemAvailable does not exist in the /proc/meminfo file: \(total - free - buffers - cached\)/total × 100%. |

-   Metrics of average system loads

    -   Linux

        You can check the output of the top command to understand the metrics described in the following table. A higher value of a metric indicates a busier system.

    -   Windows

        The metrics of average system loads are unavailable for hosts that run Windows.

    |Metric|Description|Unit|
    |:-----|:----------|:---|
    |Host.load1|The average system load in the last minute.|N/A|
    |Host.load5|The average system load in the last 5 minutes.|N/A|
    |Host.load15|The average system load in the last 15 minutes.|N/A|
    |host.loadpercore1|The average system load per CPU core in the last minute.|N/A|
    |host.loadpercore5|The average system load per CPU core in the last 5 minutes.|N/A|
    |host.loadpercore15|The average system load per CPU core in the last 15 minutes.|N/A|

-   Disk metrics

    -   Linux

        You can check the output of the df command to understand the metrics about disk and inode usage. You can check the output of the iostat command to understand metrics about disk reads and writes.

    -   Windows

        Call the GetDiskFreeSpaceExA function in Kernel32.dll to obtain the used disk space, disk usage, free disk space, and total disk space. Call the RegConnectRegistryA function to connect to the HKEY\_PERFORMANCE\_DATA entry in the registry. Then, call the RegQueryValueExA function to query the disk information in HKEY\_PERFORMANCE\_DATA, including the read count, write count, read bytes, written bytes, read time, write time, and disk active time.

    |Metric|Description|Unit|
    |:-----|:----------|:---|
    |Host.diskusage.used|The disk space in use.|byte|
    |Host.disk.utilization|The disk usage.|%|
    |Host.diskusage.free|The available disk space for regular users and superusers.|byte|
    |Host.diskusage.avail|The available disk space for regular users.|byte|
    |Host.diskusage.total|The total disk space.|byte|
    |Host.disk.readbytes|The number of bytes read from the disk per second.|byte/s|
    |Host.disk.writebytes|The number of bytes written to the disk per second.|byte/s|
    |Host.disk.readiops|The number of read requests that the disk receives per second.|count/s|
    |Host.disk.writeiops|The number of write requests that the disk receives per second.|count/s|

-   File system metric

    -   Linux

        You can check the output of the df command to understand the metric described in the following table.

    -   Windows

        The file system metric is unavailable for hosts that run Windows.

    |Metric|Description|Unit|Remarks for Linux|
    |:-----|:----------|:---|:----------------|
    |Host.fs.inode|The inode usage.|%|Linux operating systems use inode numbers rather than file names to identify files. When you have used up inode numbers, you cannot create new files even if disk space is available. Therefore, Cloud Monitor must monitor the inode usage. The number of inodes indicates the number of files. A large number of small files can cause a high inode usage.|

-   Network metrics

    -   Linux
        -   You can check the output of the ss command to understand the TCP connection metric.

            The Cloud Monitor agent collects the following TCP connection data by default: TCP\_TOTAL, ESTABLISHED, and NON\_ESTABLISHED. TCP\_TOTAL indicates the total number of connections. ESTABLISHED indicates the number of established connections. NON\_ESTABLISHED indicates the number of connections not in the established state. To allow the Cloud Monitor to collect TCP connection data, perform the following steps:

            1.  Log on to the host where the Cloud Monitor agent resides as the root user.
            2.  Change the value of `netstat.tcp.disable` to `false` in the cloudmonitor/config/conf.properties configuration file.
            3.  Restart the Cloud Monitor agent.

                For more information, see [How do I restart the Cloud Monitor agent?](/intl.en-US/FAQ/Troubleshooting/How do I restart the Cloud Monitor agent?.md)

        -   You can check the output of the iftop command to understand the network metrics.
    -   Windows

        Call the GetAdaptersAddresses function in Iphlpapi.dll to obtain the addresses of NICs on the host. Call the GetIfTable function to obtain the data of metrics for each interface, including the number of bits that an interface receives and sends per second, number of packets that an interface receives and sends per second, and number of error packets that an interface receives and sends.

    |Metric|Description|Unit|
    |:-----|:----------|:---|
    |Host.netin.rate|The number of bits that the NIC receives per second, namely, the upstream bandwidth of the NIC.|bit/s|
    |Host.netout.rate|The number of bits that the NIC sends per second, namely, the downstream bandwidth of the NIC.|bit/s|
    |Host.netin.packages|The number of packets that the NIC receives per second.|count/s|
    |Host.netout.packages|The number of packets that the NIC sends per second.|count/s|
    |Host.netin.errorpackage|The number of inbound error packets that the drive detects.|count/s|
    |Host.netout.errorpackages|The number of outbound error packets that the drive detects.|count/s|
    |Host.tcpconnection|The number of TCP connections in various states, including LISTEN, SYN\_SENT, ESTABLISHED, SYN\_RECV, FIN\_WAIT1, CLOSE\_WAIT, FIN\_WAIT2, LAST\_ACK, TIME\_WAIT, CLOSING, and CLOSED.|N/A|

-   Process metrics

    -   Linux
        -   You can check the output of the top command to understand the CPU utilization and memory usage of processes. The CPU utilization indicates the consumption of multi-core CPUs.
        -   You can check the output of the lsof command to understand the Host.process.openfile metric.
        -   You can check the output of the ps aux \| grep '<Keyword\>' command to understand the Host.process.number metric.
    -   Windows
        -   Query process information

            Call the OpenProcess function in Kernel32.dll to obtain the handle of a process. Call the GetProcessTimes function twice to obtain the CPU time consumed by the process and then calculate the CPU utilization of the process in the interval between the two executions of the command. Call the RegConnectRegistryA function to connect to the HKEY\_PERFORMANCE\_DATA entry in the registry. Then, call the RegQueryValueExA function to query the process information in HKEY\_PERFORMANCE\_DATA, including the process ID, parent process ID, priority, virtual memory, resident memory, shared memory, number of files that the process opens, thread count, page errors, read bytes, and written bytes.

        -   Count the number of processes that match the specified keyword
            -   Call the OpenProcess function to obtain the handle of a process. Call the NtQueryInformationProcess function in ntdll.dll to obtain RTL\_USER\_PROCESS\_PARAMETERS of the process. Call the ReadProcessMemory function to obtain the arguments and root path of the process from the command line information. This way, you can obtain the directory of the process.
            -   Call the OpenProcessToken function to obtain the handle of a token. Call the GetTokenInformation function to obtain the token information. Call the LookupAccountSid function to obtain the username and user group of the process.
            -   Match the directory, username, and user group of the process with the keyword. If the process information matches the keyword, increase the value of Host.process.number by 1.
    |Metric|Description|Unit|Remarks|
    |:-----|:----------|:---|:------|
    |Host.process.cpu|The CPU utilization of the process.|%|You cannot configure alert rules for this metric.|
    |Host.process.memory|The memory usage of the process.|%|You cannot configure alert rules for this metric.|
    |Host.process.openfile|The number of files that the process opens.|count|You cannot configure alert rules for this metric.|
    |Host.process.number|The number of processes that match the specific keyword.|count|You cannot configure alert rules for this metric.|


## ECS basic metrics

Cloud Monitor collects data of the metrics described in the following table from ECS instances without the need to use the Cloud Monitor agent. Cloud Monitor collects data of these metrics every minute.

|Metric|Description|Unit|
|:-----|:----------|:---|
|ECS.CPUUtilization|The CPU utilization.|%|
|ECS.InternetInRate|The average rate of inbound Internet traffic.|bit/s|
|ECS.IntranetInRate|The average rate of inbound internal network traffic.|bit/s|
|ECS.InternetOutRate|The average rate of outbound Internet traffic.|bit/s|
|ECS.IntranetOutRate|The average rate of outbound internal network traffic.|bit/s|
|ECS.SystemDiskReadbps|The number of bytes read from the system disk per second.|byte/s|
|ECS.SystemDiskWritebps|The number of bytes written to the system disk per second.|byte/s|
|ECS.SystemDiskReadOps|The number of reads from the system disk per second.|count/s|
|ECS.SystemDiskWriteOps|The number of writes to the system disk per second.|count/s|
|ECS.InternetIn|The inbound Internet traffic.|byte|
|ECS.InternetOut|The outbound Internet traffic.|byte|
|ECS.IntranetIn|The inbound traffic of the internal network.|byte|
|ECS.IntranetOut|The outbound traffic of the internal network.|byte|

