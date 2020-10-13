# Redis Standard

This topic describes the metrics for ApsaraDB for Redis of the standard architecture.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for ApsaraDB for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_kvstore**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Average Response Time|μs|StandardAvgRt|userId and instanceId|Average and Maximum|
|Connection Usage|%|StandardConnectionUsage|userId and instanceId|Average and Maximum|
|Cpu Usage|%|StandardCpuUsage|userId and instanceId|Average and Maximum|
|EvictedKeys Execution Count|count|StandardEvictedKeys|userId and instanceId|Average and Maximum|
|ExpiredKeys Execution Count|count|StandardExpiredKeys|userId and instanceId|Average and Maximum|
|Expires Execution Count|count|StandardExpires|userId and instanceId|Average and Maximum|
|Command Failed Count|count/s|StandardFailedCount|userId and instanceId|Average and Maximum|
|Hit Rate|%|StandardHitRate|userId and instanceId|Average and Maximum|
|Intranet In|KB/s|StandardIntranetIn|userId and instanceId|Average and Maximum|
|Intranet In Ratio|%|StandardIntranetInRatio|userId and instanceId|Average and Maximum|
|Intranet Out|KB/s|StandardIntranetOut|userId and instanceId|Average and Maximum|
|Intranet Out Ratio|%|StandardIntranetOutRatio|userId and instanceId|Average and Maximum|
|Keys Execution Count|count|StandardKeys|userId and instanceId|Average and Maximum|
|Max Response Time|μs|StandardMaxRt|userId and instanceId|Average and Maximum|
|Memory Usage|%|StandardMemoryUsage|userId and instanceId|Average and Maximum|
|QPS Usage|%|StandardQPSUsage|userId and instanceId|Average and Maximum|
|Used Connection|count|StandardUsedConnection|userId and instanceId|Average and Maximum|
|Used Memory|byte|StandardUsedMemory|userId and instanceId|Average and Maximum|
|Used QPS|count|StandardUsedQPS|userId and instanceId|Average and Maximum|
|Append Execution Frequency|count/s|Standardappend|userId and instanceId|Average and Maximum|
|Bitcount Execution Frequency|count/s|Standardbitcount|userId and instanceId|Average and Maximum|
|Bitop Execution Frequency|count/s|Standardbitop|userId and instanceId|Average and Maximum|
|Blpop Execution Frequency|count/s|Standardblpop|userId and instanceId|Average and Maximum|
|Standardbrpop|count/s|Standardbrpop|userId and instanceId|Average and Maximum|
|Brpoplpush Execution Frequency|count/s|Standardbrpoplpush|userId and instanceId|Average and Maximum|
|Decr Execution Frequency|count/s|Standarddecr|userId and instanceId|Average and Maximum|
|Decrby Execution Frequency|count/s|Standarddecrby|userId and instanceId|Average and Maximum|
|Del Execution Frequency|count/s|Standarddel|userId and instanceId|Average and Maximum|
|Discard Execution Frequency|count/s|Standarddiscard|userId and instanceId|Average and Maximum|
|Dump Execution Frequency|count/s|Standarddump|userId and instanceId|Average and Maximum|
|Exec Execution Frequency|count/s|Standardexec|userId and instanceId|Average and Maximum|
|Exists Execution Frequency|count/s|Standardexists|userId and instanceId|Average and Maximum|
|Expire Execution Frequency|count/s|Standardexpire|userId and instanceId|Average and Maximum|
|Expireat Execution Frequency|count/s|Standardexpireat|userId and instanceId|Average and Maximum|
|Get Execution Frequency|count/s|Standardget|userId and instanceId|Average and Maximum|
|Getbit Execution Frequency|count/s|Standardgetbit|userId and instanceId|Average and Maximum|
|Getrange Execution Frequency|count/s|Standardgetrange|userId and instanceId|Average and Maximum|
|Getset Execution Frequency|count/s|Standardgetset|userId and instanceId|Average and Maximum|
|Hdel Execution Frequency|count/s|Standardhdel|userId and instanceId|Average and Maximum|
|Hexists Execution Frequency|count/s|Standardhexists|userId and instanceId|Average and Maximum|
|Hget Execution Frequency|count/s|Standardhget|userId and instanceId|Average and Maximum|
|Hgetall Execution Frequency|count/s|Standardhgetall|userId and instanceId|Average and Maximum|
|Hincrby Execution Frequency|count/s|Standardhincrby|userId and instanceId|Average and Maximum|
|Hincrbyfloat Execution Frequency|count/s|Standardhincrbyfloat|userId and instanceId|Average and Maximum|
|Hkeys Execution Frequency|count/s|Standardhkeys|userId and instanceId|Average and Maximum|
|Hlen Execution Frequency|count/s|Standardhlen|userId and instanceId|Average and Maximum|
|Hmget Execution Frequency|count/s|Standardhmget|userId and instanceId|Average and Maximum|
|Hmset Execution Frequency|count/s|Standardhmset|userId and instanceId|Average and Maximum|
|Hscan Execution Frequency|count/s|Standardhscan|userId and instanceId|Average and Maximum|
|Hset Execution Frequency|count/s|Standardhset|userId and instanceId|Average and Maximum|
|Hsetnx Execution Frequency|count/s|Standardhsetnx|userId and instanceId|Average and Maximum|
|Hvals Execution Frequency|count/s|Standardhvals|userId and instanceId|Average and Maximum|
|Incr Execution Frequency|count/s|Standardincr|userId and instanceId|Average and Maximum|
|Incrby Execution Frequency|count/s|Standardincrby|userId and instanceId|Average and Maximum|
|Incrbyfloat Execution Frequency|count/s|Standardincrbyfloat|userId and instanceId|Average and Maximum|
|Lindex Execution Frequency|count/s|Standardlindex|userId and instanceId|Average and Maximum|
|Linsert Execution Frequency|count/s|Standardlinsert|userId and instanceId|Average and Maximum|
|Llen Execution Frequency|count/s|Standardllen|userId and instanceId|Average and Maximum|
|Lpop Execution Frequency|count/s|Standardlpop|userId and instanceId|Average and Maximum|
|Lpush Execution Frequency|count/s|Standardlpush|userId and instanceId|Average and Maximum|
|Lpushx Execution Frequency|count/s|Standardlpushx|userId and instanceId|Average and Maximum|
|Lrange Execution Frequency|count/s|Standardlrange|userId and instanceId|Average and Maximum|
|Lrem Execution Frequency|count/s|Standardlrem|userId and instanceId|Average and Maximum|
|Lset Execution Frequency|count/s|Standardlset|userId and instanceId|Average and Maximum|
|Ltrim Execution Frequency|count/s|Standardltrim|userId and instanceId|Average and Maximum|
|Mget Execution Frequency|count/s|Standardmget|userId and instanceId|Average and Maximum|
|Move Execution Frequency|count/s|Standardmove|userId and instanceId|Average and Maximum|
|Mset Execution Frequency|count/s|Standardmset|userId and instanceId|Average and Maximum|
|Msetnx Execution Frequency|count/s|Standardmsetnx|userId and instanceId|Average and Maximum|
|Multi Execution Frequency|count/s|Standardmulti|userId and instanceId|Average and Maximum|
|Persist Execution Frequency|count/s|Standardpersist|userId and instanceId|Average and Maximum|
|Pexpire Execution Frequency|count/s|Standardpexpire|userId and instanceId|Average and Maximum|
|Pexpireat Execution Frequency|count/s|Standardpexpireat|userId and instanceId|Average and Maximum|
|Pfadd Execution Frequency|count/s|Standardpfadd|userId and instanceId|Average and Maximum|
|Pfcount Execution Frequency|count/s|Standardpfcount|userId and instanceId|Average and Maximum|
|Pfmerge Execution Frequency|count/s|Standardpfmerge|userId and instanceId|Average and Maximum|
|Psetex Execution Frequency|count/s|Standardpsetex|userId and instanceId|Average and Maximum|
|Psubscribe Execution Frequency|count/s|Standardpsubscribe|userId and instanceId|Average and Maximum|
|Pttl Execution Frequency|count/s|Standardpttl|userId and instanceId|Average and Maximum|
|Publish Execution Frequency|count/s|Standardpublish|userId and instanceId|Average and Maximum|
|Pubsub Execution Frequency|count/s|Standardpubsub|userId and instanceId|Average and Maximum|
|Punsubscribe Execution Frequency|count/s|Standardpunsubscribe|userId and instanceId|Average and Maximum|
|Randomkey Execution Frequency|count/s|Standardrandomkey|userId and instanceId|Average and Maximum|
|Rename Execution Frequency|count/s|Standardrename|userId and instanceId|Average and Maximum|
|Renamenx Execution Frequency|count/s|Standardrenamenx|userId and instanceId|Average and Maximum|
|Restore Execution Frequency|count/s|Standardrestore|userId and instanceId|Average and Maximum|
|rpop Execution Frequency|count/s|Standardrpop|userId and instanceId|Average and Maximum|
|Rpoplpush Execution Frequency|count/s|Standardrpoplpush|userId and instanceId|Average and Maximum|
|Rpush Execution Frequency|count/s|Standardrpush|userId and instanceId|Average and Maximum|
|Rpushx Execution Frequency|count/s|Standardrpushx|userId and instanceId|Average and Maximum|
|Sadd Execution Frequency|count/s|Standardsadd|userId and instanceId|Average and Maximum|
|Scan Execution Frequency|count/s|Standardscan|userId and instanceId|Average and Maximum|
|Scard Execution Frequency|count/s|Standardscard|userId and instanceId|Average and Maximum|
|Sdiff Execution Frequency|count/s|Standardsdiff|userId and instanceId|Average and Maximum|
|Sdiffstore Execution Frequency|count/s|Standardsdiffstore|userId and instanceId|Average and Maximum|
|Set Execution Frequency|count/s|Standardset|userId and instanceId|Average and Maximum|
|Setbit Execution Frequency|count/s|Standardsetbit|userId and instanceId|Average and Maximum|
|Setex Execution Frequency|count/s|Standardsetex|userId and instanceId|Average and Maximum|
|Setnx Execution Frequency|count/s|Standardsetnx|userId and instanceId|Average and Maximum|
|Setrange Execution Frequency|count/s|Standardsetrange|userId and instanceId|Average and Maximum|
|Sinter Execution Frequency|count/s|Standardsinter|userId and instanceId|Average and Maximum|
|Sinterstore Execution Frequency|count/s|Standardsinterstore|userId and instanceId|Average and Maximum|
|Sismember Execution Frequency|count/s|Standardsismember|userId and instanceId|Average and Maximum|
|Smembers Execution Frequency|count/s|Standardsmembers|userId and instanceId|Average and Maximum|
|Smove Execution Frequency|count/s|Standardsmove|userId and instanceId|Average and Maximum|
|Sort Execution Frequency|count/s|Standardsort|userId and instanceId|Average and Maximum|
|Spop Execution Frequency|count/s|Standardspop|userId and instanceId|Average and Maximum|
|Srandmember Execution Frequency|count/s|Standardsrandmember|userId and instanceId|Average and Maximum|
|Srem Execution Frequency|count/s|Standardsrem|userId and instanceId|Average and Maximum|
|Sscan Execution Frequency|count/s|Standardsscan|userId and instanceId|Average and Maximum|
|Strlen Execution Frequency|count/s|Standardstrlen|userId and instanceId|Average and Maximum|
|Subscribe Execution Frequency|count/s|Standardsubscribe|userId and instanceId|Average and Maximum|
|Sunion Execution Frequency|count/s|Standardsunion|userId and instanceId|Average and Maximum|
|Sunionstore Execution Frequency|count/s|Standardsunionstore|userId and instanceId|Average and Maximum|
|Ttl Execution Frequency|count/s|Standardttl|userId and instanceId|Average and Maximum|
|Type Execution Frequency|count/s|Standardtype|userId and instanceId|Average and Maximum|
|Unsubscribe Execution Frequency|count/s|Standardunsubscribe|userId and instanceId|Average and Maximum|
|Unwatch Execution Frequency|count/s|Standardunwatch|userId and instanceId|Average and Maximum|
|Watch Execution Frequency|count/s|Standardwatch|userId and instanceId|Average and Maximum|
|Zadd Execution Frequency|count/s|Standardzadd|userId and instanceId|Average and Maximum|
|Zcard Execution Frequency|count/s|Standardzcard|userId and instanceId|Average and Maximum|
|Zcount Execution Frequency|count/s|Standardzcount|userId and instanceId|Average and Maximum|
|Zincrby Execution Frequency|count/s|Standardzincrby|userId and instanceId|Average and Maximum|
|Zinterstore Execution Frequency|count/s|Standardzinterstore|userId and instanceId|Average and Maximum|
|Zlexcount Execution Frequency|count/s|Standardzlexcount|userId and instanceId|Average and Maximum|
|Zrange Execution Frequency|count/s|Standardzrange|userId and instanceId|Average and Maximum|
|Zrangebylex Execution Frequency|count/s|Standardzrangebylex|userId and instanceId|Average and Maximum|
|Zrangebyscore Execution Frequency|count/s|Standardzrangebyscore|userId and instanceId|Average and Maximum|
|Zrank Execution Frequency|count/s|Standardzrank|userId and instanceId|Average and Maximum|
|Zrem Execution Frequency|count/s|Standardzrem|userId and instanceId|Average and Maximum|
|Zremrangebylex Execution Frequency|count/s|Standardzremrangebylex|userId and instanceId|Average and Maximum|
|Zremrangebyrank Execution Frequency|count/s|Standardzremrangebyrank|userId and instanceId|Average and Maximum|
|Zremrangebyscore Execution Frequency|count/s|Standardzremrangebyscore|userId and instanceId|Average and Maximum|
|Zrevrange Execution Frequency|count/s|Standardzrevrange|userId and instanceId|Average and Maximum|
|Zrevrangebyscore Execution Frequency|count/s|Standardzrevrangebyscore|userId and instanceId|Average and Maximum|
|Zrevrank Execution Frequency|count/s|Standardzrevrank|userId and instanceId|Average and Maximum|
|Zscan Execution Frequency|count/s|Standardzscan|userId and instanceId|Average and Maximum|
|Zscore Execution Frequency|count/s|Standardzscore|userId and instanceId|Average and Maximum|
|Zunionstore Execution Frequency|count/s|Standardzunionstore|userId and instanceId|Average and Maximum|

