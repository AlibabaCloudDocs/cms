# 对象存储OSS监控

通过本文您可以了解对象存储OSS的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_oss\_dashboard**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|AppendObject成功请求数|Count|AppendObjectCount|userId、BucketName|Value|
|AppendObject请求平均E2E延时|Milliseconds|AppendObjectE2eLatency|userId、BucketName|Value|
|AppendObject请求平均服务器延时|Milliseconds|AppendObjectServerLatency|userId、BucketName|Value|
|授权错误请求数|Count|AuthorizationErrorCount|userId、BucketName|Value|
|授权错误请求占比|%|AuthorizationErrorRate|userId、BucketName|Value|
|CDN流入流量|Byte|CdnRecv|userId、BucketName|Value|
|CDN流出流量|Byte|CdnSend|userId、BucketName|Value|
|客户端其他错误请求数|Count|ClientOtherErrorCount|userId、BucketName|Value|
|客户端其他错误请求占比|无|ClientOtherErrorRate|userId、BucketName|Value|
|客户端超时错误请求数|Count|ClientTimeoutErrorCount|userId、BucketName|Value|
|客户端超时错误请求占比|%|ClientTimeoutErrorRate|userId、BucketName|Value|
|CopyObject成功请求数|Count|CopyObjectCount|userId、BucketName|Value|
|CopyObject请求平均E2E延时|ms|CopyObjectE2eLatency|userId、BucketName|Value|
|CopyObject请求平均服务器延时|ms|CopyObjectServerLatency|userId、BucketName|Value|
|DeleteObject成功请求数|Count|DeleteObjectCount|userId、BucketName|Value|
|DeleteObjects成功请求数|Count|DeleteObjectsCount|userId、BucketName|Value|
|GetObject成功请求数|Frequency|GetObjectCount|userId、BucketName|Value|
|GetObject请求平均E2E延时|Milliseconds|GetObjectE2eLatency|userId、BucketName|Value|
|GetObject请求平均服务器延时|Milliseconds|GetObjectServerLatency|userId、BucketName|Value|
|HeadObject成功请求数|Count|HeadObjectCount|userId、BucketName|Value|
|HeadObject请求成功E2E延时|Milliseconds|HeadObjectE2eLatency|userId、BucketName|Value|
|HeadObject请求平均服务器延时|Milliseconds|HeadObjectServerLatency|userId、BucketName|Value|
|公网流入流量|Byte|InternetRecv|userId、BucketName|Value|
|公网流出流量|Byte|InternetSend|userId、BucketName|Value|
|内网流入流量|Byte|IntranetRecv|userId、BucketName|Value|
|内网流出流量|Byte|IntranetSend|userId、BucketName|Value|
|AppendObject请求最大E2E延时|Milliseconds|MaxAppendObjectE2eLatency|userId、BucketName|Value|
|AppendObject请求最大服务器延时|Milliseconds|MaxAppendObjectServerLatency|userId、BucketName|Value|
|CopyObject请求最大E2E延迟|ms|MaxCopyObjectE2eLatency|userId、BucketName|Value|
|CopyObject请求最大服务器延时|ms|MaxCopyObjectServerLatency|userId、BucketName|Value|
|GetObject请求最大E2E延时|Milliseconds|MaxGetObjectE2eLatency|userId、BucketName|Value|
|GetObject请求最大服务器延时|Milliseconds|MaxGetObjectServerLatency|userId、BucketName|Value|
|HeadObject请求最大E2E延时|Milliseconds|MaxHeadObjectE2eLatency|userId、BucketName|Value|
|HeadObject请求最大服务器延时|Milliseconds|MaxHeadObjectServerLatency|userId、BucketName|Value|
|PostObject请求最大E2E延时|Milliseconds|MaxPostObjectE2eLatency|userId、BucketName|Value|
|PostObject请求最大服务器延时|Milliseconds|MaxPostObjectServerLatency|userId、BucketName|Value|
|PutObject请求最大E2E延时|Milliseconds|MaxPutObjectE2eLatency|userId、BucketName|Value|
|PutObject请求最大服务器延时|Milliseconds|MaxPutObjectServerLatency|userId、BucketName|Value|
|UploadPartCopy请求最大E2E延时|Milliseconds|MaxUploadPartCopyE2eLatency|userId、BucketName|Value|
|UploadPartCopy请求最大服务器延时|Milliseconds|MaxUploadPartCopyServerLatency|userId、BucketName|Value|
|UploadPart请求最大E2E延时|Milliseconds|MaxUploadPartE2eLatency|userId、BucketName|Value|
|UploadPart请求最大服务器延时|Milliseconds|MaxUploadPartServerLatency|userId、BucketName|Value|
|CDN流入计量流量|Byte|MeteringCdnRX|userId、BucketName、region、storageType|Value|
|CDN流出计量流量|Byte|MeteringCdnTX|userId、BucketName、region、storageType|Value|
|Get类请求数|Count|MeteringGetRequest|userId、BucketName、region、storageType|Value|
|MeteringInternetRX|Byte|MeteringInternetRX|userId、BucketName、region、storageType|Value|
|公网流出计量流量|Byte|MeteringInternetTX|userId、BucketName、region、storageType|Value|
|MeteringIntranetRX|Byte|MeteringIntranetRX|userId、BucketName、region、storageType|Value|
|MeteringIntranetTX|Byte|MeteringIntranetTX|userId、BucketName、region、storageType|Value|
|Put类请求数|Count|MeteringPutRequest|userId、BucketName、region、storageType|Value|
|存储大小|Byte|MeteringStorageUtilization|userId、BucketName、region、storageType|Value|
|跨区域复制流入计量流量|Byte|MeteringSyncRX|userId、BucketName、region、storageType|Value|
|MeteringSyncTX|Byte|MeteringSyncTX|userId、BucketName、region、storageType|Value|
|MirrorAverageLatency|无|MirrorAverageLatency|userId、BucketName、Host|Value|
|MirrorAverageLatencyByStatus|无|MirrorAverageLatencyByStatus|userId、BucketName、Host、Status|Value|
|MirrorRequestCount|无|MirrorRequestCount|userId、BucketName、Host|Value|
|MirrorRequestCountByStatus|无|MirrorRequestCountByStatus|userId、BucketName、Host、Status|Value|
|MirrorRequestTransferSpeed|无|MirrorRequestTransferSpeed|userId、BucketName、Host|Value|
|MirrorRequestTransferSpeedByStatus|无|MirrorRequestTransferSpeedByStatus|userId、BucketName、Host、Status|Value|
|MirrorTraffic|无|MirrorTraffic|userId、BucketName、Host|Value|
|MirrorTrafficByStatus|无|MirrorTrafficByStatus|userId、BucketName、Host、Status|Value|
|网络错误请求数|Count|NetworkErrorCount|userId、BucketName|Value|
|网络错误请求占比|%|NetworkErrorRate|userId、BucketName|Value|
|PostObject成功请求数|Count|PostObjectCount|userId、BucketName|Value|
|PostObject请求平均E2E延时|Milliseconds|PostObjectE2eLatency|userId、BucketName|Value|
|PostObject请求平均服务器延时|Milliseconds|PostObjectServerLatency|userId、BucketName|Value|
|PutObject成功请求数|Count|PutObjectCount|userId、BucketName|Value|
|PutObject请求平均E2E延时|Milliseconds|PutObjectE2eLatency|userId、BucketName|Value|
|PutObject请求平均服务器延时|Milliseconds|PutObjectServerLatency|userId、BucketName|Value|
|重定向请求数|Count|RedirectCount|userId、BucketName|Value|
|重定向请求占比|%|RedirectRate|userId、BucketName|Value|
|有效请求率|%|RequestValidRate|userId、BucketName|Value|
|资源不存在错误请求数|Count|ResourceNotFoundErrorCount|userId、BucketName|Value|
|资源不存在错误请求占比|%|ResourceNotFoundErrorRate|userId、BucketName|Value|
|服务端错误请求数|Count|ServerErrorCount|userId、BucketName|Value|
|服务端错误请求占比|%|ServerErrorRate|userId、BucketName|Value|
|成功请求数|Count|SuccessCount|userId、BucketName|Value|
|成功请求占比|%|SuccessRate|userId、BucketName|Value|
|跨区域复制流入流量|Byte|SyncRecv|userId、BucketName|Value|
|跨区域复制流出流量|Byte|SyncSend|userId、BucketName|Value|
|总请求数|Count|TotalRequestCount|userId、BucketName|Value|
|UploadPartCopy成功请求数|Count|UploadPartCopyCount|userId、BucketName|Value|
|UploadPartCopy请求平均E2E延时|Milliseconds|UploadPartCopyE2eLatency|userId、BucketName|Value|
|UploadPartCopy请求平均服务器延时|Milliseconds|UploadPartCopyServerLatency|userId、BucketName|Value|
|UploadPart成功请求数|Count|UploadPartCount|userId、BucketName|Value|
|UploadPart请求平均E2E延时|Milliseconds|UploadPartE2eLatency|userId、BucketName|Value|
|UploadPart请求平均服务器延时|Milliseconds|UploadPartServerLatency|userId、BucketName|Value|
|用户层级授权错误请求数|Count|UserAuthorizationErrorCount|userId|Value|
|用户层级授权错误请求占比|%|UserAuthorizationErrorRate|userId|Value|
|用户层级可用性|%|UserAvailability|userId|Value|
|用户层级CDN流入流量|Byte|UserCdnRecv|userId|Value|
|用户层级CDN流出流量|Byte|UserCdnSend|userId|Value|
|用户层级客户端其他错误请求数|Count|UserClientOtherErrorCount|userId|Value|
|用户层级客户端其他错误请求占比|无|UserClientOtherErrorRate|userId|Value|
|用户层级客户端超时错误请求数|Count|UserClientTimeoutErrorCount|userId|Value|
|用户层级客户端超时错误请求占比|%|UserClientTimeoutErrorRate|userId|Value|
|用户层级公网流入流量|Byte|UserInternetRecv|userId|Value|
|用户层级公网流出流量|Byte|UserInternetSend|userId|Value|
|用户层级内网流入流量|Byte|UserIntranetRecv|userId|Value|
|用户层级内网流出流量|Byte|UserIntranetSend|userId|Value|
|用户层级网络错误请求数|Count|UserNetworkErrorCount|userId|Value|
|用户层级网络错误请求占比|%|UserNetworkErrorRate|userId|Value|
|用户层级重定向请求数|Count|UserRedirectCount|userId|Value|
|用户层级重定向请求占比|%|UserRedirectRate|userId|Value|
|用户层级有效请求率|%|UserRequestValidRate|userId|Value|
|用户层级资源不存在错误请求数|Count|UserResourceNotFoundErrorCount|userId|Value|
|用户层级不存在错误请求占比|%|UserResourceNotFoundErrorRate|userId|Value|
|用户层级服务端错误请求数|Count|UserServerErrorCount|userId|Value|
|用户层级服务端错误请求占比|%|UserServerErrorRate|userId|Value|
|用户层级成功请求数|Count|UserSuccessCount|userId|Value|
|用户层级成功请求占比|%|UserSuccessRate|userId|Value|
|用户层级跨区域复制流入流量|Byte|UserSyncRecv|userId|Value|
|用户层级跨区域复制流出流量|Byte|UserSyncSend|userId|Value|
|用户层级总请求数|Count|UserTotalRequestCount|userId|Value|
|用户层级有效请求数|Count|UserValidRequestCount|userId|Value|
|有效请求数|Count|ValidRequestCount|userId、BucketName|Value|
|可用性|%|Availability|userId、BucketName|Value|

