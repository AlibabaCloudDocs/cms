# Redis Cluster

This topic describes the metrics for ApsaraDB for Redis of the cluster architecture.

**Note:** During the period from August 1, 2020 to September 30, 2020, Alibaba Cloud unpublished specific metrics for ApsaraDB for Redis. These metrics become unavailable after September 30, 2020. For more information, see [Deprecated alarm metrics in Cloud Monitor](/intl.en-US/Notices/Deprecated alarm metrics in Cloud Monitor.md).

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for ApsaraDB for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_kvstore**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Average Response Time|μs|ShardingAvgRt|userId, instanceId, and nodeId|Average and Maximum|
|Connection Usage|%|ShardingConnectionUsage|userId, instanceId, and nodeId|Average and Maximum|
|Cpu Usage|%|ShardingCpuUsage|userId, instanceId, and nodeId|Average and Maximum|
|EvictedKeys Execution Count|count|ShardingEvictedKeys|userId, instanceId, and nodeId|Average and Maximum|
|ExpiredKeys Execution Count|count|ShardingExpiredKeys|userId, instanceId, and nodeId|Average and Maximum|
|Expires Execution Count|count|ShardingExpires|userId, instanceId, and nodeId|Average and Maximum|
|Hit Rate|%|ShardingHitRate|userId, instanceId, and nodeId|Average and Maximum|
|Intranet In|KB/s|ShardingIntranetIn|userId, instanceId, and nodeId|Average and Maximum|
|Intranet In Ratio|%|ShardingIntranetInRatio|userId, instanceId, and nodeId|Average and Maximum|
|Intranet Out|KB/s|ShardingIntranetOut|userId, instanceId, and nodeId|Average and Maximum|
|Intranet Out Ratio|%|ShardingIntranetOutRatio|userId, instanceId, and nodeId|Average and Maximum|
|Keys Execution Count|count|ShardingKeys|userId, instanceId, and nodeId|Average and Maximum|
|Max Response Time|μs|ShardingMaxRt|userId, instanceId, and nodeId|Average and Maximum|
|Memory Usage|%|ShardingMemoryUsage|userId, instanceId, and nodeId|Average and Maximum|
|QPS Usage|%|ShardingQPSUsage|userId, instanceId, and nodeId|Average and Maximum|
|Used Connection|count|ShardingUsedConnection|userId, instanceId, and nodeId|Average and Maximum|
|Used Memory|byte|ShardingUsedMemory|userId, instanceId, and nodeId|Average, Maximum, and Sum|
|Used QPS|count|ShardingUsedQPS|userId, instanceId, and nodeId|Average and Maximum|
|Append Execution Frequency|count/s|Shardingappend|userId, instanceId, and nodeId|Average and Maximum|
|Bitcount Execution Frequency|count/s|Shardingbitcount|userId, instanceId, and nodeId|Average and Maximum|
|Bitop Execution Frequency|count/s|Shardingbitop|userId, instanceId, and nodeId|Average and Maximum|
|Blpop Execution Frequency|count/s|Shardingblpop|userId, instanceId, and nodeId|Average and Maximum|
|Shardingbrpop|count/s|Shardingbrpop|userId, instanceId, and nodeId|Average and Maximum|
|Brpoplpush Execution Frequency|count/s|Shardingbrpoplpush|userId, instanceId, and nodeId|Average and Maximum|
|Decr Execution Frequency|count/s|Shardingdecr|userId, instanceId, and nodeId|Average and Maximum|
|Decrby Execution Frequency|count/s|Shardingdecrby|userId, instanceId, and nodeId|Average and Maximum|
|Del Execution Frequency|count/s|Shardingdel|userId, instanceId, and nodeId|Average and Maximum|
|Discard Execution Frequency|count/s|Shardingdiscard|userId, instanceId, and nodeId|Average and Maximum|
|Dump Execution Frequency|count/s|Shardingdump|userId, instanceId, and nodeId|Average and Maximum|
|Exec Execution Frequency|count/s|Shardingexec|userId, instanceId, and nodeId|Average and Maximum|
|Exists Execution Frequency|count/s|Shardingexists|userId, instanceId, and nodeId|Average and Maximum|
|Expire Execution Frequency|count/s|Shardingexpire|userId, instanceId, and nodeId|Average and Maximum|
|Expireat Execution Frequency|count/s|Shardingexpireat|userId, instanceId, and nodeId|Average and Maximum|
|Get Execution Frequency|count/s|Shardingget|userId, instanceId, and nodeId|Average and Maximum|
|Getbit Execution Frequency|count/s|Shardinggetbit|userId, instanceId, and nodeId|Average and Maximum|
|Getrange Execution Frequency|count/s|Shardinggetrange|userId, instanceId, and nodeId|Average and Maximum|
|Getset Execution Frequency|count/s|Shardinggetset|userId, instanceId, and nodeId|Average and Maximum|
|Hdel Execution Frequency|count/s|Shardinghdel|userId, instanceId, and nodeId|Average and Maximum|
|Hexists Execution Frequency|count/s|Shardinghexists|userId, instanceId, and nodeId|Average and Maximum|
|Hget Execution Frequency|count/s|Shardinghget|userId, instanceId, and nodeId|Average and Maximum|
|Hgetall Execution Frequency|count/s|Shardinghgetall|userId, instanceId, and nodeId|Average and Maximum|
|Hincrby Execution Frequency|count/s|Shardinghincrby|userId, instanceId, and nodeId|Average and Maximum|
|Hincrbyfloat Execution Frequency|count/s|Shardinghincrbyfloat|userId, instanceId, and nodeId|Average and Maximum|
|Hkeys Execution Frequency|count/s|Shardinghkeys|userId, instanceId, and nodeId|Average and Maximum|
|Hlen Execution Frequency|count/s|Shardinghlen|userId, instanceId, and nodeId|Average and Maximum|
|Hmget Execution Frequency|count/s|Shardinghmget|userId, instanceId, and nodeId|Average and Maximum|
|Hmset Execution Frequency|count/s|Shardinghmset|userId, instanceId, and nodeId|Average and Maximum|
|Hscan Execution Frequency|count/s|Shardinghscan|userId, instanceId, and nodeId|Average and Maximum|
|Hset Execution Frequency|count/s|Shardinghset|userId, instanceId, and nodeId|Average and Maximum|
|Hsetnx Execution Frequency|count/s|Shardinghsetnx|userId, instanceId, and nodeId|Average and Maximum|
|Hvals Execution Frequency|count/s|Shardinghvals|userId, instanceId, and nodeId|Average and Maximum|
|Incr Execution Frequency|count/s|Shardingincr|userId, instanceId, and nodeId|Average and Maximum|
|Incrby Execution Frequency|count/s|Shardingincrby|userId, instanceId, and nodeId|Average and Maximum|
|Incrbyfloat Execution Frequency|count/s|Shardingincrbyfloat|userId, instanceId, and nodeId|Average and Maximum|
|Lindex Execution Frequency|count/s|Shardinglindex|userId, instanceId, and nodeId|Average and Maximum|
|Linsert Execution Frequency|count/s|Shardinglinsert|userId, instanceId, and nodeId|Average and Maximum|
|Llen Execution Frequency|count/s|Shardingllen|userId, instanceId, and nodeId|Average and Maximum|
|Lpop Execution Frequency|count/s|Shardinglpop|userId, instanceId, and nodeId|Average and Maximum|
|Lpush Execution Frequency|count/s|Shardinglpush|userId, instanceId, and nodeId|Average and Maximum|
|Lpushx Execution Frequency|count/s|Shardinglpushx|userId, instanceId, and nodeId|Average and Maximum|
|Lrange Execution Frequency|count/s|Shardinglrange|userId, instanceId, and nodeId|Average and Maximum|
|Lrem Execution Frequency|count/s|Shardinglrem|userId, instanceId, and nodeId|Average and Maximum|
|Lset Execution Frequency|count/s|Shardinglset|userId, instanceId, and nodeId|Average and Maximum|
|Ltrim Execution Frequency|count/s|Shardingltrim|userId, instanceId, and nodeId|Average and Maximum|
|Mget Execution Frequency|count/s|Shardingmget|userId, instanceId, and nodeId|Average and Maximum|
|Move Execution Frequency|count/s|Shardingmove|userId, instanceId, and nodeId|Average and Maximum|
|Mset Execution Frequency|count/s|Shardingmset|userId, instanceId, and nodeId|Average and Maximum|
|Msetnx Execution Frequency|count/s|Shardingmsetnx|userId, instanceId, and nodeId|Average and Maximum|
|Multi Execution Frequency|count/s|Shardingmulti|userId, instanceId, and nodeId|Average and Maximum|
|Persist Execution Frequency|count/s|Shardingpersist|userId, instanceId, and nodeId|Average and Maximum|
|Pexpire Execution Frequency|count/s|Shardingpexpire|userId, instanceId, and nodeId|Average and Maximum|
|Pexpireat Execution Frequency|count/s|Shardingpexpireat|userId, instanceId, and nodeId|Average and Maximum|
|Pfadd Execution Frequency|count/s|Shardingpfadd|userId, instanceId, and nodeId|Average and Maximum|
|Pfcount Execution Frequency|count/s|Shardingpfcount|userId, instanceId, and nodeId|Average and Maximum|
|Pfmerge Execution Frequency|count/s|Shardingpfmerge|userId, instanceId, and nodeId|Average and Maximum|
|Psetex Execution Frequency|count/s|Shardingpsetex|userId, instanceId, and nodeId|Average and Maximum|
|Psubscribe Execution Frequency|count/s|Shardingpsubscribe|userId, instanceId, and nodeId|Average and Maximum|
|Pttl Execution Frequency|count/s|Shardingpttl|userId, instanceId, and nodeId|Average and Maximum|
|Publish Execution Frequency|count/s|Shardingpublish|userId, instanceId, and nodeId|Average and Maximum|
|Pubsub Execution Frequency|count/s|Shardingpubsub|userId, instanceId, and nodeId|Average and Maximum|
|Punsubscribe Execution Frequency|count/s|Shardingpunsubscribe|userId, instanceId, and nodeId|Average and Maximum|
|Randomkey Execution Frequency|count/s|Shardingrandomkey|userId, instanceId, and nodeId|Average and Maximum|
|Rename Execution Frequency|count/s|Shardingrename|userId, instanceId, and nodeId|Average and Maximum|
|Renamenx Execution Frequency|count/s|Shardingrenamenx|userId, instanceId, and nodeId|Average and Maximum|
|Restore Execution Frequency|count/s|Shardingrestore|userId, instanceId, and nodeId|Average and Maximum|
|rpop Execution Frequency|count/s|Shardingrpop|userId, instanceId, and nodeId|Average and Maximum|
|Rpoplpush Execution Frequency|count/s|Shardingrpoplpush|userId, instanceId, and nodeId|Average and Maximum|
|Rpush Execution Frequency|count/s|Shardingrpush|userId, instanceId, and nodeId|Average and Maximum|
|Rpushx Execution Frequency|count/s|Shardingrpushx|userId, instanceId, and nodeId|Average and Maximum|
|Sadd Execution Frequency|count/s|Shardingsadd|userId, instanceId, and nodeId|Average and Maximum|
|Scan Execution Frequency|count/s|Shardingscan|userId, instanceId, and nodeId|Average and Maximum|
|Scard Execution Frequency|count/s|Shardingscard|userId, instanceId, and nodeId|Average and Maximum|
|Sdiff Execution Frequency|count/s|Shardingsdiff|userId, instanceId, and nodeId|Average and Maximum|
|Sdiffstore Execution Frequency|count/s|Shardingsdiffstore|userId, instanceId, and nodeId|Average and Maximum|
|Set Execution Frequency|count/s|Shardingset|userId, instanceId, and nodeId|Average and Maximum|
|Setbit Execution Frequency|count/s|Shardingsetbit|userId, instanceId, and nodeId|Average and Maximum|
|Setex Execution Frequency|count/s|Shardingsetex|userId, instanceId, and nodeId|Average and Maximum|
|Setnx Execution Frequency|count/s|Shardingsetnx|userId, instanceId, and nodeId|Average and Maximum|
|Setrange Execution Frequency|count/s|Shardingsetrange|userId, instanceId, and nodeId|Average and Maximum|
|Sinter Execution Frequency|count/s|Shardingsinter|userId, instanceId, and nodeId|Average and Maximum|
|Sinterstore Execution Frequency|count/s|Shardingsinterstore|userId, instanceId, and nodeId|Average and Maximum|
|Sismember Execution Frequency|count/s|Shardingsismember|userId, instanceId, and nodeId|Average and Maximum|
|Smembers Execution Frequency|count/s|Shardingsmembers|userId, instanceId, and nodeId|Average and Maximum|
|Smove Execution Frequency|count/s|Shardingsmove|userId, instanceId, and nodeId|Average and Maximum|
|Sort Execution Frequency|count/s|Shardingsort|userId, instanceId, and nodeId|Average and Maximum|
|Spop Execution Frequency|count/s|Shardingspop|userId, instanceId, and nodeId|Average and Maximum|
|Srandmember Execution Frequency|count/s|Shardingsrandmember|userId, instanceId, and nodeId|Average and Maximum|
|Srem Execution Frequency|count/s|Shardingsrem|userId, instanceId, and nodeId|Average and Maximum|
|Sscan Execution Frequency|count/s|Shardingsscan|userId, instanceId, and nodeId|Average and Maximum|
|Strlen Execution Frequency|count/s|Shardingstrlen|userId, instanceId, and nodeId|Average and Maximum|
|Subscribe Execution Frequency|count/s|Shardingsubscribe|userId, instanceId, and nodeId|Average and Maximum|
|Sunion Execution Frequency|count/s|Shardingsunion|userId, instanceId, and nodeId|Average and Maximum|
|Sunionstore Execution Frequency|count/s|Shardingsunionstore|userId, instanceId, and nodeId|Average and Maximum|
|Ttl Execution Frequency|count/s|Shardingttl|userId, instanceId, and nodeId|Average and Maximum|
|Type Execution Frequency|count/s|Shardingtype|userId, instanceId, and nodeId|Average and Maximum|
|Unsubscribe Execution Frequency|count/s|Shardingunsubscribe|userId, instanceId, and nodeId|Average and Maximum|
|Unwatch Execution Frequency|count/s|Shardingunwatch|userId, instanceId, and nodeId|Average and Maximum|
|Watch Execution Frequency|count/s|Shardingwatch|userId, instanceId, and nodeId|Average and Maximum|
|Zadd Execution Frequency|count/s|Shardingzadd|userId, instanceId, and nodeId|Average and Maximum|
|Zcard Execution Frequency|count/s|Shardingzcard|userId, instanceId, and nodeId|Average and Maximum|
|Zcount Execution Frequency|count/s|Shardingzcount|userId, instanceId, and nodeId|Average and Maximum|
|Zincrby Execution Frequency|count/s|Shardingzincrby|userId, instanceId, and nodeId|Average and Maximum|
|Zinterstore Execution Frequency|count/s|Shardingzinterstore|userId, instanceId, and nodeId|Average and Maximum|
|Zlexcount Execution Frequency|count/s|Shardingzlexcount|userId, instanceId, and nodeId|Average and Maximum|
|Zrange Execution Frequency|count/s|Shardingzrange|userId, instanceId, and nodeId|Average and Maximum|
|Zrangebylex Execution Frequency|count/s|Shardingzrangebylex|userId, instanceId, and nodeId|Average and Maximum|
|Zrangebyscore Execution Frequency|count/s|Shardingzrangebyscore|userId, instanceId, and nodeId|Average and Maximum|
|Zrank Execution Frequency|count/s|Shardingzrank|userId, instanceId, and nodeId|Average and Maximum|
|Zrem Execution Frequency|count/s|Shardingzrem|userId, instanceId, and nodeId|Average and Maximum|
|Zremrangebylex Execution Frequency|count/s|Shardingzremrangebylex|userId, instanceId, and nodeId|Average and Maximum|
|Zremrangebyrank Execution Frequency|count/s|Shardingzremrangebyrank|userId, instanceId, and nodeId|Average and Maximum|
|Zremrangebyscore Execution Frequency|count/s|Shardingzremrangebyscore|userId, instanceId, and nodeId|Average and Maximum|
|Zrevrange Execution Frequency|count/s|Shardingzrevrange|userId, instanceId, and nodeId|Average and Maximum|
|Zrevrangebyscore Execution Frequency|count/s|Shardingzrevrangebyscore|userId, instanceId, and nodeId|Average and Maximum|
|Zrevrank Execution Frequency|count/s|Shardingzrevrank|userId, instanceId, and nodeId|Average and Maximum|
|Zscan Execution Frequency|count/s|Shardingzscan|userId, instanceId, and nodeId|Average and Maximum|
|Zscore Execution Frequency|count/s|Shardingzscore|userId, instanceId, and nodeId|Average and Maximum|
|Zunionstore Execution Frequency|count/s|Shardingzunionstore|userId, instanceId, and nodeId|Average and Maximum|

