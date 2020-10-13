# Redis Read-Write

This topic describes the metrics for ApsaraDB for Redis of the read/write splitting architecture.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for ApsaraDB for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_kvstore**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Average Response Time|μs|SplitrwAvgRt|userId, instanceId, and nodeId|Average and Maximum|
|Connection Usage|%|SplitrwConnectionUsage|userId, instanceId, and nodeId|Average and Maximum|
|Cpu Usage|%|SplitrwCpuUsage|userId, instanceId, and nodeId|Average and Maximum|
|EvictedKeys Execution Count|count|SplitrwEvictedKeys|userId, instanceId, and nodeId|Average and Maximum|
|ExpiredKeys Execution Count|count|SplitrwExpiredKeys|userId, instanceId, and nodeId|Average and Maximum|
|Expires Execution Count|count|SplitrwExpires|userId, instanceId, and nodeId|Average and Maximum|
|Command Failed Count|count/s|SplitrwFailedCount|userId, instanceId, and nodeId|Average and Maximum|
|Hit Rate|%|SplitrwHitRate|userId, instanceId, and nodeId|Average and Maximum|
|Intranet In|KB/s|SplitrwIntranetIn|userId, instanceId, and nodeId|Average and Maximum|
|Intranet In Ratio|%|SplitrwIntranetInRatio|userId, instanceId, and nodeId|Average and Maximum|
|Intranet Out|KB/s|SplitrwIntranetOut|userId, instanceId, and nodeId|Average and Maximum|
|Intranet Out Ratio|%|SplitrwIntranetOutRatio|userId, instanceId, and nodeId|Average and Maximum|
|Keys Execution Count|count|SplitrwKeys|userId, instanceId, and nodeId|Average and Maximum|
|Max Response Time|μs|SplitrwMaxRt|userId, instanceId, and nodeId|Average and Maximum|
|Memory Usage|%|SplitrwMemoryUsage|userId, instanceId, and nodeId|Average and Maximum|
|QPS Usage|%|SplitrwQPSUsage|userId, instanceId, and nodeId|Average and Maximum|
|Used Connection|count|SplitrwUsedConnection|userId, instanceId, and nodeId|Average and Maximum|
|Used Memory|byte|SplitrwUsedMemory|userId, instanceId, and nodeId|Average, Maximum, and Sum|
|Used QPS|count|SplitrwUsedQPS|userId, instanceId, and nodeId|Average and Maximum|
|Append Execution Frequency|count/s|Splitrwappend|userId, instanceId, and nodeId|Average and Maximum|
|Bitcount Execution Frequency|count/s|Splitrwbitcount|userId, instanceId, and nodeId|Average and Maximum|
|Bitop Execution Frequency|count/s|Splitrwbitop|userId, instanceId, and nodeId|Average and Maximum|
|Blpop Execution Frequency|count/s|Splitrwblpop|userId, instanceId, and nodeId|Average and Maximum|
|Brpoplpush Execution Frequency|count/s|Splitrwbrpoplpush|userId, instanceId, and nodeId|Average and Maximum|
|Decr Execution Frequency|count/s|Splitrwdecr|userId, instanceId, and nodeId|Average and Maximum|
|Decrby Execution Frequency|count/s|Splitrwdecrby|userId, instanceId, and nodeId|Average and Maximum|
|Del Execution Frequency|count/s|Splitrwdel|userId, instanceId, and nodeId|Average and Maximum|
|Discard Execution Frequency|count/s|Splitrwdiscard|userId, instanceId, and nodeId|Average and Maximum|
|Dump Execution Frequency|count/s|Splitrwdump|userId, instanceId, and nodeId|Average and Maximum|
|Exec Execution Frequency|count/s|Splitrwexec|userId, instanceId, and nodeId|Average and Maximum|
|Exists Execution Frequency|count/s|Splitrwexists|userId, instanceId, and nodeId|Average and Maximum|
|Expire Execution Frequency|count/s|Splitrwexpire|userId, instanceId, and nodeId|Average and Maximum|
|Expireat Execution Frequency|count/s|Splitrwexpireat|userId, instanceId, and nodeId|Average and Maximum|
|Get Execution Frequency|count/s|Splitrwget|userId, instanceId, and nodeId|Average and Maximum|
|Getbit Execution Frequency|count/s|Splitrwgetbit|userId, instanceId, and nodeId|Average and Maximum|
|Getrange Execution Frequency|count/s|Splitrwgetrange|userId, instanceId, and nodeId|Average and Maximum|
|Getset Execution Frequency|count/s|Splitrwgetset|userId, instanceId, and nodeId|Average and Maximum|
|Hdel Execution Frequency|count/s|Splitrwhdel|userId, instanceId, and nodeId|Average and Maximum|
|Hexists Execution Frequency|count/s|Splitrwhexists|userId, instanceId, and nodeId|Average and Maximum|
|Hget Execution Frequency|count/s|Splitrwhget|userId, instanceId, and nodeId|Average and Maximum|
|Hgetall Execution Frequency|count/s|Splitrwhgetall|userId, instanceId, and nodeId|Average and Maximum|
|Hincrby Execution Frequency|count/s|Splitrwhincrby|userId, instanceId, and nodeId|Average and Maximum|
|Hincrbyfloat Execution Frequency|count/s|Splitrwhincrbyfloat|userId, instanceId, and nodeId|Average and Maximum|
|Hkeys Execution Frequency|count/s|Splitrwhkeys|userId, instanceId, and nodeId|Average and Maximum|
|Hlen Execution Frequency|count/s|Splitrwhlen|userId, instanceId, and nodeId|Average and Maximum|
|Hmget Execution Frequency|count/s|Splitrwhmget|userId, instanceId, and nodeId|Average and Maximum|
|Hmset Execution Frequency|count/s|Splitrwhmset|userId, instanceId, and nodeId|Average and Maximum|
|Hscan Execution Frequency|count/s|Splitrwhscan|userId, instanceId, and nodeId|Average and Maximum|
|Hset Execution Frequency|count/s|Splitrwhset|userId, instanceId, and nodeId|Average and Maximum|
|Hsetnx Execution Frequency|count/s|Splitrwhsetnx|userId, instanceId, and nodeId|Average and Maximum|
|Hvals Execution Frequency|count/s|Splitrwhvals|userId, instanceId, and nodeId|Average and Maximum|
|Incr Execution Frequency|count/s|Splitrwincr|userId, instanceId, and nodeId|Average and Maximum|
|Incrby Execution Frequency|count/s|Splitrwincrby|userId, instanceId, and nodeId|Average and Maximum|
|Incrbyfloat Execution Frequency|count/s|Splitrwincrbyfloat|userId, instanceId, and nodeId|Average and Maximum|
|Lindex Execution Frequency|count/s|Splitrwlindex|userId, instanceId, and nodeId|Average and Maximum|
|Linsert Execution Frequency|count/s|Splitrwlinsert|userId, instanceId, and nodeId|Average and Maximum|
|Llen Execution Frequency|count/s|Splitrwllen|userId, instanceId, and nodeId|Average and Maximum|
|Lpop Execution Frequency|count/s|Splitrwlpop|userId, instanceId, and nodeId|Average and Maximum|
|Lpush Execution Frequency|count/s|Splitrwlpush|userId, instanceId, and nodeId|Average and Maximum|
|Lpushx Execution Frequency|count/s|Splitrwlpushx|userId, instanceId, and nodeId|Average and Maximum|
|Lrange Execution Frequency|count/s|Splitrwlrange|userId, instanceId, and nodeId|Average and Maximum|
|Lrem Execution Frequency|count/s|Splitrwlrem|userId, instanceId, and nodeId|Average and Maximum|
|Lset Execution Frequency|count/s|Splitrwlset|userId, instanceId, and nodeId|Average and Maximum|
|Ltrim Execution Frequency|count/s|Splitrwltrim|userId, instanceId, and nodeId|Average and Maximum|
|Mget Execution Frequency|count/s|Splitrwmget|userId, instanceId, and nodeId|Average and Maximum|
|Move Execution Frequency|count/s|Splitrwmove|userId, instanceId, and nodeId|Average and Maximum|
|Mset Execution Frequency|count/s|Splitrwmset|userId, instanceId, and nodeId|Average and Maximum|
|Msetnx Execution Frequency|count/s|Splitrwmsetnx|userId, instanceId, and nodeId|Average and Maximum|
|Multi Execution Frequency|count/s|Splitrwmulti|userId, instanceId, and nodeId|Average and Maximum|
|Persist Execution Frequency|count/s|Splitrwpersist|userId, instanceId, and nodeId|Average and Maximum|
|Pexpire Execution Frequency|count/s|Splitrwpexpire|userId, instanceId, and nodeId|Average and Maximum|
|Pexpireat Execution Frequency|count/s|Splitrwpexpireat|userId, instanceId, and nodeId|Average and Maximum|
|Pfadd Execution Frequency|count/s|Splitrwpfadd|userId, instanceId, and nodeId|Average and Maximum|
|Pfcount Execution Frequency|count/s|Splitrwpfcount|userId, instanceId, and nodeId|Average and Maximum|
|Pfmerge Execution Frequency|count/s|Splitrwpfmerge|userId, instanceId, and nodeId|Average and Maximum|
|Psetex Execution Frequency|count/s|Splitrwpsetex|userId, instanceId, and nodeId|Average and Maximum|
|Psubscribe Execution Frequency|count/s|Splitrwpsubscribe|userId, instanceId, and nodeId|Average and Maximum|
|Pttl Execution Frequency|count/s|Splitrwpttl|userId, instanceId, and nodeId|Average and Maximum|
|Publish Execution Frequency|count/s|Splitrwpublish|userId, instanceId, and nodeId|Average and Maximum|
|Pubsub Execution Frequency|count/s|Splitrwpubsub|userId, instanceId, and nodeId|Average and Maximum|
|Punsubscribe Execution Frequency|count/s|Splitrwpunsubscribe|userId, instanceId, and nodeId|Average and Maximum|
|Randomkey Execution Frequency|count/s|Splitrwrandomkey|userId, instanceId, and nodeId|Average and Maximum|
|Rename Execution Frequency|count/s|Splitrwrename|userId, instanceId, and nodeId|Average and Maximum|
|Renamenx Execution Frequency|count/s|Splitrwrenamenx|userId, instanceId, and nodeId|Average and Maximum|
|Restore Execution Frequency|count/s|Splitrwrestore|userId, instanceId, and nodeId|Average and Maximum|
|rpop Execution Frequency|count/s|Splitrwrpop|userId, instanceId, and nodeId|Average and Maximum|
|Rpoplpush Execution Frequency|count/s|Splitrwrpoplpush|userId, instanceId, and nodeId|Average and Maximum|
|Rpush Execution Frequency|count/s|Splitrwrpush|userId, instanceId, and nodeId|Average and Maximum|
|Rpushx Execution Frequency|count/s|Splitrwrpushx|userId, instanceId, and nodeId|Average and Maximum|
|Sadd Execution Frequency|count/s|Splitrwsadd|userId, instanceId, and nodeId|Average and Maximum|
|Scan Execution Frequency|count/s|Splitrwscan|userId, instanceId, and nodeId|Average and Maximum|
|Scard Execution Frequency|count/s|Splitrwscard|userId, instanceId, and nodeId|Average and Maximum|
|Sdiff Execution Frequency|count/s|Splitrwsdiff|userId, instanceId, and nodeId|Average and Maximum|
|Sdiffstore Execution Frequency|count/s|Splitrwsdiffstore|userId, instanceId, and nodeId|Average and Maximum|
|Set Execution Frequency|count/s|Splitrwset|userId, instanceId, and nodeId|Average and Maximum|
|Setbit Execution Frequency|count/s|Splitrwsetbit|userId, instanceId, and nodeId|Average and Maximum|
|Setex Execution Frequency|count/s|Splitrwsetex|userId, instanceId, and nodeId|Average and Maximum|
|Setnx Execution Frequency|count/s|Splitrwsetnx|userId, instanceId, and nodeId|Average and Maximum|
|Setrange Execution Frequency|count/s|Splitrwsetrange|userId, instanceId, and nodeId|Average and Maximum|
|Sinter Execution Frequency|count/s|Splitrwsinter|userId, instanceId, and nodeId|Average and Maximum|
|Sinterstore Execution Frequency|count/s|Splitrwsinterstore|userId, instanceId, and nodeId|Average and Maximum|
|Sismember Execution Frequency|count/s|Splitrwsismember|userId, instanceId, and nodeId|Average and Maximum|
|Smembers Execution Frequency|count/s|Splitrwsmembers|userId, instanceId, and nodeId|Average and Maximum|
|Smove Execution Frequency|count/s|Splitrwsmove|userId, instanceId, and nodeId|Average and Maximum|
|Sort Execution Frequency|count/s|Splitrwsort|userId, instanceId, and nodeId|Average and Maximum|
|Spop Execution Frequency|count/s|Splitrwspop|userId, instanceId, and nodeId|Average and Maximum|
|Srandmember Execution Frequency|count/s|Splitrwsrandmember|userId, instanceId, and nodeId|Average and Maximum|
|Srem Execution Frequency|count/s|Splitrwsrem|userId, instanceId, and nodeId|Average and Maximum|
|Sscan Execution Frequency|count/s|Splitrwsscan|userId, instanceId, and nodeId|Average and Maximum|
|Strlen Execution Frequency|count/s|Splitrwstrlen|userId, instanceId, and nodeId|Average and Maximum|
|Subscribe Execution Frequency|count/s|Splitrwsubscribe|userId, instanceId, and nodeId|Average and Maximum|
|Sunion Execution Frequency|count/s|Splitrwsunion|userId, instanceId, and nodeId|Average and Maximum|
|Sunionstore Execution Frequency|count/s|Splitrwsunionstore|userId, instanceId, and nodeId|Average and Maximum|
|Ttl Execution Frequency|count/s|Splitrwttl|userId, instanceId, and nodeId|Average and Maximum|
|Type Execution Frequency|count/s|Splitrwtype|userId, instanceId, and nodeId|Average and Maximum|
|Unsubscribe Execution Frequency|count/s|Splitrwunsubscribe|userId, instanceId, and nodeId|Average and Maximum|
|Unwatch Execution Frequency|count/s|Splitrwunwatch|userId, instanceId, and nodeId|Average and Maximum|
|Watch Execution Frequency|count/s|Splitrwwatch|userId, instanceId, and nodeId|Average and Maximum|
|Zadd Execution Frequency|count/s|Splitrwzadd|userId, instanceId, and nodeId|Average and Maximum|
|Zcard Execution Frequency|count/s|Splitrwzcard|userId, instanceId, and nodeId|Average and Maximum|
|Zcount Execution Frequency|count/s|Splitrwzcount|userId, instanceId, and nodeId|Average and Maximum|
|Zincrby Execution Frequency|count/s|Splitrwzincrby|userId, instanceId, and nodeId|Average and Maximum|
|Zinterstore Execution Frequency|count/s|Splitrwzinterstore|userId, instanceId, and nodeId|Average and Maximum|
|Zlexcount Execution Frequency|count/s|Splitrwzlexcount|userId, instanceId, and nodeId|Average and Maximum|
|Zrange Execution Frequency|count/s|Splitrwzrange|userId, instanceId, and nodeId|Average and Maximum|
|Zrangebylex Execution Frequency|count/s|Splitrwzrangebylex|userId, instanceId, and nodeId|Average and Maximum|
|Zrangebyscore Execution Frequency|count/s|Splitrwzrangebyscore|userId, instanceId, and nodeId|Average and Maximum|
|Zrank Execution Frequency|count/s|Splitrwzrank|userId, instanceId, and nodeId|Average and Maximum|
|Zrem Execution Frequency|count/s|Splitrwzrem|userId, instanceId, and nodeId|Average and Maximum|
|Zremrangebylex Execution Frequency|count/s|Splitrwzremrangebylex|userId, instanceId, and nodeId|Average and Maximum|
|Zremrangebyrank Execution Frequency|count/s|Splitrwzremrangebyrank|userId, instanceId, and nodeId|Average and Maximum|
|Zremrangebyscore Execution Frequency|count/s|Splitrwzremrangebyscore|userId, instanceId, and nodeId|Average and Maximum|
|Zrevrange Execution Frequency|count/s|Splitrwzrevrange|userId, instanceId, and nodeId|Average and Maximum|
|Zrevrangebyscore Execution Frequency|count/s|Splitrwzrevrangebyscore|userId, instanceId, and nodeId|Average and Maximum|
|Zrevrank Execution Frequency|count/s|Splitrwzrevrank|userId, instanceId, and nodeId|Average and Maximum|
|Zscan Execution Frequency|count/s|Splitrwzscan|userId, instanceId, and nodeId|Average and Maximum|
|Zscore Execution Frequency|count/s|Splitrwzscore|userId, instanceId, and nodeId|Average and Maximum|
|Zunionstore Execution Frequency|count/s|Splitrwzunionstore|userId, instanceId, and nodeId|Average and Maximum|

