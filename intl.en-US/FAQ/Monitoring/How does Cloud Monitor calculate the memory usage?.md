# How does Cloud Monitor calculate the memory usage?

This topic describes how Cloud Monitor calculates the memory usage.

Cloud Monitor uses the following formula to calculate the memory usage:

\(mem\_total - \(mem\_free + mem\_buffer + mem\_cache\)\)/mem\_total

You can run the `cat/proc/meminfo` command to view the values of mem\_free, mem\_buffer, and mem\_cache. Example:

```
[root@localhost ~]# cat /proc/meminfo MemTotal: 8011936 kBMemFree: 227336 kBBuffers: 277872 kBCached: 1451828 kB
```

Calculation process: \(8,011,936 - \(227,336 + 277,872 + 1,451,828\)\)/8,011,936

Calculation result: The memory usage is about 75%.

