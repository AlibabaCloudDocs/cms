# Redis Standard

This topic describes the metrics for ApsaraDB for Redis instances of the standard edition.

-   Set the **Namespace** parameter to **acs\_kvstore**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|Metric|Dimensions|Statistics|
|------|----|------|----------|----------|
|Average Response Time|us|StandardAvgRt|userId and instanceId|Average and Maximum|
|Connection Usage|%|StandardConnectionUsage|userId and instanceId|Average and Maximum|
|Cpu Usage|%|StandardCpuUsage|userId and instanceId|Average and Maximum|
|EvictedKeys Execution Count|Count|StandardEvictedKeys|userId and instanceId|Average and Maximum|
|ExpiredKeys Execution Count|Count|StandardExpiredKeys|userId and instanceId|Average and Maximum|
|Expires Execution Count|Count|StandardExpires|userId and instanceId|Average and Maximum|
|Command Failed Count|Count/second|StandardFailedCount|userId and instanceId|Average and Maximum|
|Hit Rate|%|StandardHitRate|userId and instanceId|Average and Maximum|
|Intranet In|KByte/s|StandardIntranetIn|userId and instanceId|Average and Maximum|
|Intranet In Ratio|%|StandardIntranetInRatio|userId and instanceId|Average and Maximum|
|Intranet Out|KByte/s|StandardIntranetOut|userId and instanceId|Average and Maximum|
|Intranet Out Ratio|%|StandardIntranetOutRatio|userId and instanceId|Average and Maximum|
|Keys Execution Count|Count|StandardKeys|userId and instanceId|Average and Maximum|
|Max Response Time|us|StandardMaxRt|userId and instanceId|Average and Maximum|
|Memory Usage|%|StandardMemoryUsage|userId and instanceId|Average and Maximum|
|QPS Usage|%|StandardQPSUsage|userId and instanceId|Average and Maximum|
|Used Connection|Count|StandardUsedConnection|userId and instanceId|Average and Maximum|
|Used Memory|Bytes|StandardUsedMemory|userId and instanceId|Average and Maximum|
|Used QPS|Count|StandardUsedQPS|userId and instanceId|Average and Maximum|
|Append Execution Frequency|Count/Second|Standardappend|userId and instanceId|Average and Maximum|
|Bitcount Execution Frequency|Count/Second|Standardbitcount|userId and instanceId|Average and Maximum|
|Bitop Execution Frequency|Count/Second|Standardbitop|userId and instanceId|Average and Maximum|
|Blpop Execution Frequency|Count/Second|Standardblpop|userId and instanceId|Average and Maximum|
|Standardbrpop|Count/Second|Standardbrpop|userId and instanceId|Average and Maximum|
|Brpoplpush Execution Frequency|Count/Second|Standardbrpoplpush|userId and instanceId|Average and Maximum|
|Decr Execution Frequency|Count/Second|Standarddecr|userId and instanceId|Average and Maximum|
|Decrby Execution Frequency|Count/Second|Standarddecrby|userId and instanceId|Average and Maximum|
|Del Execution Frequency|Count/Second|Standarddel|userId and instanceId|Average and Maximum|
|Discard Execution Frequency|Count/Second|Standarddiscard|userId and instanceId|Average and Maximum|
|Dump Execution Frequency|Count/Second|Standarddump|userId and instanceId|Average and Maximum|
|Exec Execution Frequency|Count/Second|Standardexec|userId and instanceId|Average and Maximum|
|Exists Execution Frequency|Count/Second|Standardexists|userId and instanceId|Average and Maximum|
|Expire Execution Frequency|Count/Second|Standardexpire|userId and instanceId|Average and Maximum|
|Expireat Execution Frequency|Count/Second|Standardexpireat|userId and instanceId|Average and Maximum|
|Get Execution Frequency|Count/Second|Standardget|userId and instanceId|Average and Maximum|
|Getbit Execution Frequency|Count/Second|Standardgetbit|userId and instanceId|Average and Maximum|
|Getrange Execution Frequency|Count/Second|Standardgetrange|userId and instanceId|Average and Maximum|
|Getset Execution Frequency|Count/Second|Standardgetset|userId and instanceId|Average and Maximum|
|Hdel Execution Frequency|Count/Second|Standardhdel|userId and instanceId|Average and Maximum|
|Hexists Execution Frequency|Count/Second|Standardhexists|userId and instanceId|Average and Maximum|
|Hget Execution Frequency|Count/Second|Standardhget|userId and instanceId|Average and Maximum|
|Hgetall Execution Frequency|Count/Second|Standardhgetall|userId and instanceId|Average and Maximum|
|Hincrby Execution Frequency|Count/Second|Standardhincrby|userId and instanceId|Average and Maximum|
|Hincrbyfloat Execution Frequency|Count/Second|Standardhincrbyfloat|userId and instanceId|Average and Maximum|
|Hkeys Execution Frequency|Count/Second|Standardhkeys|userId and instanceId|Average and Maximum|
|Hlen Execution Frequency|Count/Second|Standardhlen|userId and instanceId|Average and Maximum|
|Hmget Execution Frequency|Count/Second|Standardhmget|userId and instanceId|Average and Maximum|
|Hmset Execution Frequency|Count/Second|Standardhmset|userId and instanceId|Average and Maximum|
|Hscan Execution Frequency|Count/Second|Standardhscan|userId and instanceId|Average and Maximum|
|Hset Execution Frequency|Count/Second|Standardhset|userId and instanceId|Average and Maximum|
|Hsetnx Execution Frequency|Count/Second|Standardhsetnx|userId and instanceId|Average and Maximum|
|Hvals Execution Frequency|Count/Second|Standardhvals|userId and instanceId|Average and Maximum|
|Incr Execution Frequency|Count/Second|Standardincr|userId and instanceId|Average and Maximum|
|Incrby Execution Frequency|Count/Second|Standardincrby|userId and instanceId|Average and Maximum|
|Incrbyfloat Execution Frequency|Count/Second|Standardincrbyfloat|userId and instanceId|Average and Maximum|
|Lindex Execution Frequency|Count/Second|Standardlindex|userId and instanceId|Average and Maximum|
|Linsert Execution Frequency|Count/Second|Standardlinsert|userId and instanceId|Average and Maximum|
|Llen Execution Frequency|Count/Second|Standardllen|userId and instanceId|Average and Maximum|
|Lpop Execution Frequency|Count/Second|Standardlpop|userId and instanceId|Average and Maximum|
|Lpush Execution Frequency|Count/Second|Standardlpush|userId and instanceId|Average and Maximum|
|Lpushx Execution Frequency|Count/Second|Standardlpushx|userId and instanceId|Average and Maximum|
|Lrange Execution Frequency|Count/Second|Standardlrange|userId and instanceId|Average and Maximum|
|Lrem Execution Frequency|Count/Second|Standardlrem|userId and instanceId|Average and Maximum|
|Lset Execution Frequency|Count/Second|Standardlset|userId and instanceId|Average and Maximum|
|Ltrim Execution Frequency|Count/Second|Standardltrim|userId and instanceId|Average and Maximum|
|Mget Execution Frequency|Count/Second|Standardmget|userId and instanceId|Average and Maximum|
|Move Execution Frequency|Count/Second|Standardmove|userId and instanceId|Average and Maximum|
|Mset Execution Frequency|Count/Second|Standardmset|userId and instanceId|Average and Maximum|
|Msetnx Execution Frequency|Count/Second|Standardmsetnx|userId and instanceId|Average and Maximum|
|Multi Execution Frequency|Count/Second|Standardmulti|userId and instanceId|Average and Maximum|
|Persist Execution Frequency|Count/Second|Standardpersist|userId and instanceId|Average and Maximum|
|Pexpire Execution Frequency|Count/Second|Standardpexpire|userId and instanceId|Average and Maximum|
|Pexpireat Execution Frequency|Count/Second|Standardpexpireat|userId and instanceId|Average and Maximum|
|Pfadd Execution Frequency|Count/Second|Standardpfadd|userId and instanceId|Average and Maximum|
|Pfcount Execution Frequency|Count/Second|Standardpfcount|userId and instanceId|Average and Maximum|
|Pfmerge Execution Frequency|Count/Second|Standardpfmerge|userId and instanceId|Average and Maximum|
|Psetex Execution Frequency|Count/Second|Standardpsetex|userId and instanceId|Average and Maximum|
|Psubscribe Execution Frequency|Count/Second|Standardpsubscribe|userId and instanceId|Average and Maximum|
|Pttl Execution Frequency|Count/Second|Standardpttl|userId and instanceId|Average and Maximum|
|Publish Execution Frequency|Count/Second|Standardpublish|userId and instanceId|Average and Maximum|
|Pubsub Execution Frequency|Count/Second|Standardpubsub|userId and instanceId|Average and Maximum|
|Punsubscribe Execution Frequency|Count/Second|Standardpunsubscribe|userId and instanceId|Average and Maximum|
|Randomkey Execution Frequency|Count/Second|Standardrandomkey|userId and instanceId|Average and Maximum|
|Rename Execution Frequency|Count/Second|Standardrename|userId and instanceId|Average and Maximum|
|Renamenx Execution Frequency|Count/Second|Standardrenamenx|userId and instanceId|Average and Maximum|
|Restore Execution Frequency|Count/Second|Standardrestore|userId and instanceId|Average and Maximum|
|rpop Execution Frequency|Count/Second|Standardrpop|userId and instanceId|Average and Maximum|
|Rpoplpush Execution Frequency|Count/Second|Standardrpoplpush|userId and instanceId|Average and Maximum|
|Rpush Execution Frequency|Count/Second|Standardrpush|userId and instanceId|Average and Maximum|
|Rpushx Execution Frequency|Count/Second|Standardrpushx|userId and instanceId|Average and Maximum|
|Sadd Execution Frequency|Count/Second|Standardsadd|userId and instanceId|Average and Maximum|
|Scan Execution Frequency|Count/Second|Standardscan|userId and instanceId|Average and Maximum|
|Scard Execution Frequency|Count/Second|Standardscard|userId and instanceId|Average and Maximum|
|Sdiff Execution Frequency|Count/Second|Standardsdiff|userId and instanceId|Average and Maximum|
|Sdiffstore Execution Frequency|Count/Second|Standardsdiffstore|userId and instanceId|Average and Maximum|
|Set Execution Frequency|Count/Second|Standardset|userId and instanceId|Average and Maximum|
|Setbit Execution Frequency|Count/Second|Standardsetbit|userId and instanceId|Average and Maximum|
|Setex Execution Frequency|Count/Second|Standardsetex|userId and instanceId|Average and Maximum|
|Setnx Execution Frequency|Count/Second|Standardsetnx|userId and instanceId|Average and Maximum|
|Setrange Execution Frequency|Count/Second|Standardsetrange|userId and instanceId|Average and Maximum|
|Sinter Execution Frequency|Count/Second|Standardsinter|userId and instanceId|Average and Maximum|
|Sinterstore Execution Frequency|Count/Second|Standardsinterstore|userId and instanceId|Average and Maximum|
|Sismember Execution Frequency|Count/Second|Standardsismember|userId and instanceId|Average and Maximum|
|Smembers Execution Frequency|Count/Second|Standardsmembers|userId and instanceId|Average and Maximum|
|Smove Execution Frequency|Count/Second|Standardsmove|userId and instanceId|Average and Maximum|
|Sort Execution Frequency|Count/Second|Standardsort|userId and instanceId|Average and Maximum|
|Spop Execution Frequency|Count/Second|Standardspop|userId and instanceId|Average and Maximum|
|Srandmember Execution Frequency|Count/Second|Standardsrandmember|userId and instanceId|Average and Maximum|
|Srem Execution Frequency|Count/Second|Standardsrem|userId and instanceId|Average and Maximum|
|Sscan Execution Frequency|Count/Second|Standardsscan|userId and instanceId|Average and Maximum|
|Strlen Execution Frequency|Count/Second|Standardstrlen|userId and instanceId|Average and Maximum|
|Subscribe Execution Frequency|Count/Second|Standardsubscribe|userId and instanceId|Average and Maximum|
|Sunion Execution Frequency|Count/Second|Standardsunion|userId and instanceId|Average and Maximum|
|Sunionstore Execution Frequency|Count/Second|Standardsunionstore|userId and instanceId|Average and Maximum|
|Ttl Execution Frequency|Count/Second|Standardttl|userId and instanceId|Average and Maximum|
|Type Execution Frequency|Count/Second|Standardtype|userId and instanceId|Average and Maximum|
|Unsubscribe Execution Frequency|Count/Second|Standardunsubscribe|userId and instanceId|Average and Maximum|
|Unwatch Execution Frequency|Count/Second|Standardunwatch|userId and instanceId|Average and Maximum|
|Watch Execution Frequency|Count/Second|Standardwatch|userId and instanceId|Average and Maximum|
|Zadd Execution Frequency|Count/Second|Standardzadd|userId and instanceId|Average and Maximum|
|Zcard Execution Frequency|Count/Second|Standardzcard|userId and instanceId|Average and Maximum|
|Zcount Execution Frequency|Count/Second|Standardzcount|userId and instanceId|Average and Maximum|
|Zincrby Execution Frequency|Count/Second|Standardzincrby|userId and instanceId|Average and Maximum|
|Zinterstore Execution Frequency|Count/Second|Standardzinterstore|userId and instanceId|Average and Maximum|
|Zlexcount Execution Frequency|Count/Second|Standardzlexcount|userId and instanceId|Average and Maximum|
|Zrange Execution Frequency|Count/Second|Standardzrange|userId and instanceId|Average and Maximum|
|Zrangebylex Execution Frequency|Count/Second|Standardzrangebylex|userId and instanceId|Average and Maximum|
|Zrangebyscore Execution Frequency|Count/Second|Standardzrangebyscore|userId and instanceId|Average and Maximum|
|Zrank Execution Frequency|Count/Second|Standardzrank|userId and instanceId|Average and Maximum|
|Zrem Execution Frequency|Count/Second|Standardzrem|userId and instanceId|Average and Maximum|
|Zremrangebylex Execution Frequency|Count/Second|Standardzremrangebylex|userId and instanceId|Average and Maximum|
|Zremrangebyrank Execution Frequency|Count/Second|Standardzremrangebyrank|userId and instanceId|Average and Maximum|
|Zremrangebyscore Execution Frequency|Count/Second|Standardzremrangebyscore|userId and instanceId|Average and Maximum|
|Zrevrange Execution Frequency|Count/Second|Standardzrevrange|userId and instanceId|Average and Maximum|
|Zrevrangebyscore Execution Frequency|Count/Second|Standardzrevrangebyscore|userId and instanceId|Average and Maximum|
|Zrevrank Execution Frequency|Count/Second|Standardzrevrank|userId and instanceId|Average and Maximum|
|Zscan Execution Frequency|Count/Second|Standardzscan|userId and instanceId|Average and Maximum|
|Zscore Execution Frequency|Count/Second|Standardzscore|userId and instanceId|Average and Maximum|
|Zunionstore Execution Frequency|Count/Second|Standardzunionstore|userId and instanceId|Average and Maximum|

