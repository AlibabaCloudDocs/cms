# 对象存储OSS

通过本文您可以了解对象存储OSS的系统事件。

|事件名称|事件含义|事件状态|事件等级|说明|
|----|----|----|----|--|
|BucketEgressBandwidth|Bucket下行带宽超过汇报阈值|Normal|Info|阿里云账号中所有Bucket下行带宽之和超过128Mbps汇报阈值即触发该事件。|
|BucketEgressBandwidthThresholdExceeded|Bucket下行带宽超过流控阈值|Normal|Warn|Bucket受到区域流控限流影响。 如果指定区域内所有Bucket的下行带宽之和超过流控设置，则触发流控。

-   中国内地公共云默认每个区域是10Gbps。
-   中国香港和海外默认是5Gbps。

 Bucket级别不设置默认流控。 |
|BucketIngressBandwidth|Bucket上行带宽超过汇报阈值|Normal|Info|阿里云账号中所有Bucket上行带宽之和超过128Mbps汇报阈值即触发该事件。|
|BucketIngressBandwidthThresholdExceeded|Bucket上行带宽超过流控阈值|Normal|Warn|Bucket受到区域流控限流影响。 如果指定区域内所有Bucket的下行带宽之和超过流控设置，则触发流控。

-   中国内地公共云默认每个区域是10Gbps。
-   中国香港和海外默认是5Gbps。

 Bucket级别不设置默认流控。 |
|UserEgressBandwidth|User下行带宽超过汇报阈值|Normal|Info|阿里云账号中所有Bucket下行带宽之和超过128Mbps汇报阈值即触该发事件。|
|UserEgressBandwidthThresholdExceeded|User下行带宽超过流控阈值|Normal|Warn|如果指定区域内所有Bucket的下行带宽之和超过流控设置，则会触发该事件。 -   中国内地公共云默认每个区域是10Gbps。
-   中国香港和海外默认是5Gbps。

 Bucket级别不设置默认流控。 |
|UserIngressBandwidth|User上行带宽超过汇报阈值|Normal|Info|阿里云账号中所有Bucket上行带宽之和超过128Mbps汇报阈值即触发该事件。|
|UserIngressBandwidthThresholdExceeded|User上行带宽超过流控阈值|Normal|Warn|如果指定区域内所有Bucket的上行带宽之和超过流控设置，则会触发该事件。 -   中国内地公共云默认每个区域是10Gbps。
-   中国香港和海外默认是5Gbps。

 Bucket级别不设置默认流控。 |

