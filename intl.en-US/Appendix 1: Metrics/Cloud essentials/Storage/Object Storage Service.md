# Object Storage Service

This topic describes the metrics for Object Storage Service \(OSS\).

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for ApsaraDB for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_oss\_dashboard**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Number of Successful AppendObject Requests|count|AppendObjectCount|userId and BucketName|Value|
|AppendObject Request Average E2E Latency|ms|AppendObjectE2eLatency|userId and BucketName|Value|
|AppendObject Request Average Server Latency|ms|AppendObjectServerLatency|userId and BucketName|Value|
|Number of Incorrect Authorization Requests|count|AuthorizationErrorCount|userId and BucketName|Value|
|Number of Authorization Error Requests|%|AuthorizationErrorRate|userId and BucketName|Value|
|CDN Inbound Traffic|byte|CdnRecv|userId and BucketName|Value|
|CND Outbound Traffic|byte|CdnSend|userId and BucketName|Value|
|Number of Client Other Error Requests|count|ClientOtherErrorCount|userId and BucketName|Value|
|Client Other Error Request Proportion|N/A|ClientOtherErrorRate|userId and BucketName|Value|
|Number of Client Timeout Error Requests|count|ClientTimeoutErrorCount|userId and BucketName|Value|
|Client Timeout Error Request Proportion|%|ClientTimeoutErrorRate|userId and BucketName|Value|
|Number of Successful CopyObject Requests|count|CopyObjectCount|userId and BucketName|Value|
|CopyObject Request Average E2E Latency|ms|CopyObjectE2eLatency|userId and BucketName|Value|
|CopyObject Request Average Server Latency|ms|CopyObjectServerLatency|userId and BucketName|Value|
|Number of Successful DeleteObject Requests|count|DeleteObjectCount|userId and BucketName|Value|
|Number of Successful DeleteObjects Requests|count|DeleteObjectsCount|userId and BucketName|Value|
|Number of Successful GetObject Requests|frequency|GetObjectCount|userId and BucketName|Value|
|Getobject Request Average E2E Latency|ms|GetObjectE2eLatency|userId and BucketName|Value|
|Getobject Request Average Server Latency|ms|GetObjectServerLatency|userId and BucketName|Value|
|Number of Successful HeadObject Requests|count|HeadObjectCount|userId and BucketName|Value|
|HeadObject Request Average E2E Latency|ms|HeadObjectE2eLatency|userId and BucketName|Value|
|HeadObject Request Average Server Latency|ms|HeadObjectServerLatency|userId and BucketName|Value|
|Internet Inbound Traffic|byte|InternetRecv|userId and BucketName|Value|
|Internet Outbound Traffic|byte|InternetSend|userId and BucketName|Value|
|Intranet Inbound Traffic|byte|IntranetRecv|userId and BucketName|Value|
|Intranet Outbound Traffic|byte|IntranetSend|userId and BucketName|Value|
|AppendObject Request Maximum E2E Latency|ms|MaxAppendObjectE2eLatency|userId and BucketName|Value|
|AppendObject Request Maximum Server Latency|ms|MaxAppendObjectServerLatency|userId and BucketName|Value|
|CopyObject requests the maximum E2E latency|ms|MaxCopyObjectE2eLatency|userId and BucketName|Value|
|CopyObject Request Maximum Server Latency|ms|MaxCopyObjectServerLatency|userId and BucketName|Value|
|Maximum E2E Latency for GetObject Requests|ms|MaxGetObjectE2eLatency|userId and BucketName|Value|
|Getobject Request Maximum Server Latency|ms|MaxGetObjectServerLatency|userId and BucketName|Value|
|HeadObject Request Maximum E2E Latency|ms|MaxHeadObjectE2eLatency|userId and BucketName|Value|
|HeadObject Request Maximum Server Latency|ms|MaxHeadObjectServerLatency|userId and BucketName|Value|
|PostObject Request Maximum E2E Latency|ms|MaxPostObjectE2eLatency|userId and BucketName|Value|
|PostObject Request Maximum Server Latency|ms|MaxPostObjectServerLatency|userId and BucketName|Value|
|PutObject Request Maximum E2E Latency|ms|MaxPutObjectE2eLatency|userId and BucketName|Value|
|PutObject Request Maximum Server Latency|ms|MaxPutObjectServerLatency|userId and BucketName|Value|
|UploadPart Request Maximum E2E Latency|ms|MaxUploadPartCopyE2eLatency|userId and BucketName|Value|
|UploadPart Request Maximum Server Latency|ms|MaxUploadPartCopyServerLatency|userId and BucketName|Value|
|UploadPart Request Maximum E2E Latency|ms|MaxUploadPartE2eLatency|userId and BucketName|Value|
|UploadPart Request Maximum Server Latency|ms|MaxUploadPartServerLatency|userId and BucketName|Value|
|CDN inflow metering flow|byte|MeteringCdnRX|userId, BucketName, region, and storageType|Value|
|CDN Outbound Traffic|byte|MeteringCdnTX|userId, BucketName, region, and storageType|Value|
|Number of GET Requests|count|MeteringGetRequest|userId, BucketName, region, and storageType|Value|
|MeteringInternetRX|byte|MeteringInternetRX|userId, BucketName, region, and storageType|Value|
|Internet Outbound Traffic|byte|MeteringInternetTX|userId, BucketName, region, and storageType|Value|
|MeteringIntranetRX|byte|MeteringIntranetRX|userId, BucketName, region, and storageType|Value|
|MeteringIntranetTX|byte|MeteringIntranetTX|userId, BucketName, region, and storageType|Value|
|Number of PUT Requests|count|MeteringPutRequest|userId, BucketName, region, and storageType|Value|
|Storage Size|byte|MeteringStorageUtilization|userId, BucketName, region, and storageType|Value|
|Cross-region Replication Inbound Traffic|byte|MeteringSyncRX|userId, BucketName, region, and storageType|Value|
|MeteringSyncTX|byte|MeteringSyncTX|userId, BucketName, region, and storageType|Value|
|MirrorAverageLatency|N/A|MirrorAverageLatency|userId, BucketName, and Host|Value|
|MirrorAverageLatencyByStatus|N/A|MirrorAverageLatencyByStatus|userId, BucketName, Host, and Status|Value|
|MirrorRequestCount|N/A|MirrorRequestCount|userId, BucketName, and Host|Value|
|MirrorRequestCountByStatus|N/A|MirrorRequestCountByStatus|userId, BucketName, Host, and Status|Value|
|MirrorRequestTransferSpeed|N/A|MirrorRequestTransferSpeed|userId, BucketName, and Host|Value|
|MirrorRequestTransferSpeedByStatus|N/A|MirrorRequestTransferSpeedByStatus|userId, BucketName, Host, and Status|Value|
|MirrorTraffic|N/A|MirrorTraffic|userId, BucketName, and Host|Value|
|MirrorTrafficByStatus|N/A|MirrorTrafficByStatus|userId, BucketName, Host, and Status|Value|
|Number of Network Error Requests|count|NetworkErrorCount|userId and BucketName|Value|
|Network Error Request Proportion|%|NetworkErrorRate|userId and BucketName|Value|
|Number of Successful PostObject Requests|count|PostObjectCount|userId and BucketName|Value|
|PostObject Request Average E2E Latency|ms|PostObjectE2eLatency|userId and BucketName|Value|
|PostObject Request Average Server Latency|ms|PostObjectServerLatency|userId and BucketName|Value|
|Number of Successful PutObject Requests|count|PutObjectCount|userId and BucketName|Value|
|PutObject Request Average E2E Latency|ms|PutObjectE2eLatency|userId and BucketName|Value|
|PutObject Request Average Server Latency|ms|PutObjectServerLatency|userId and BucketName|Value|
|Number of Redirected Requests|count|RedirectCount|userId and BucketName|Value|
|Redirected Request Proportion|%|RedirectRate|userId and BucketName|Value|
|Valid Request Proportion|%|RequestValidRate|userId and BucketName|Value|
|Number of Resource Not Found Error Requests|count|ResourceNotFoundErrorCount|userId and BucketName|Value|
|Resource Not Found Error Request Proportion|%|ResourceNotFoundErrorRate|userId and BucketName|Value|
|Number of Server Error Requests|count|ServerErrorCount|userId and BucketName|Value|
|Server Error Request Proportion|%|ServerErrorRate|userId and BucketName|Value|
|Number of Successful Requests|count|SuccessCount|userId and BucketName|Value|
|Successful Request Proportion|%|SuccessRate|userId and BucketName|Value|
|Cross-region Sync Inbound Traffic|byte|SyncRecv|userId and BucketName|Value|
|Cross-region Sync Outbound Traffic|byte|SyncSend|userId and BucketName|Value|
|Total Number of Requests|count|TotalRequestCount|userId and BucketName|Value|
|Number of Successful UploadPartCopy Requests|count|UploadPartCopyCount|userId and BucketName|Value|
|UploadPartCopy Request Average E2E Latency|ms|UploadPartCopyE2eLatency|userId and BucketName|Value|
|UploadPartCopy Request Average Server Latency|ms|UploadPartCopyServerLatency|userId and BucketName|Value|
|Number of Successful UploadPart Requests|count|UploadPartCount|userId and BucketName|Value|
|UploadPart Request Average E2E Latency|ms|UploadPartE2eLatency|userId and BucketName|Value|
|UploadPart Request Average Server Latency|ms|UploadPartServerLatency|userId and BucketName|Value|
|Number of Authorization Error Requests by User|count|UserAuthorizationErrorCount|userId|Value|
|Authorization Error Request Proportion by User|%|UserAuthorizationErrorRate|userId|Value|
|Availability by User|%|UserAvailability|userId|Value|
|CDN Inbound Traffic by User|byte|UserCdnRecv|userId|Value|
|CDN Outbound Traffic by User|byte|UserCdnSend|userId|Value|
|Number of Client Other Error Requests by User|count|UserClientOtherErrorCount|userId|Value|
|Client Other Error Request Proportion by User|N/A|UserClientOtherErrorRate|userId|Value|
|Number of Client Timeout Error Requests by User|count|UserClientTimeoutErrorCount|userId|Value|
|Client Timeout Error Request Proportion by User|%|UserClientTimeoutErrorRate|userId|Value|
|Internet Inbound Traffic by User|byte|UserInternetRecv|userId|Value|
|Internet Outbound Traffic by User|byte|UserInternetSend|userId|Value|
|Intranet Inbound Traffic by User|byte|UserIntranetRecv|userId|Value|
|Intranet Outbound Traffic by User|byte|UserIntranetSend|userId|Value|
|Number of Network Error Requests by User|count|UserNetworkErrorCount|userId|Value|
|Network Error Request Proportion by User|%|UserNetworkErrorRate|userId|Value|
|Number of Redirected Requests by User|count|UserRedirectCount|userId|Value|
|Redirected Request Proportion by User|%|UserRedirectRate|userId|Value|
|Valid Request Proportion by User|%|UserRequestValidRate|userId|Value|
|Number of Resource Not Found Error Requests by User|count|UserResourceNotFoundErrorCount|userId|Value|
|Resource Not Found Error Request Proportion by User|%|UserResourceNotFoundErrorRate|userId|Value|
|Number of Server Error Requests by User|count|UserServerErrorCount|userId|Value|
|Server Error Request Proportion by User|%|UserServerErrorRate|userId|Value|
|Number of Successful Requests by User|count|UserSuccessCount|userId|Value|
|Successful Request Proportion by User|%|UserSuccessRate|userId|Value|
|Cross-region Sync Inbound Traffic by User|byte|UserSyncRecv|userId|Value|
|Cross-region Sync Outbound Traffic by User|byte|UserSyncSend|userId|Value|
|Total Number of Requests by User|count|UserTotalRequestCount|userId|Value|
|Number of Valid Requests by User|count|UserValidRequestCount|userId|Value|
|Number of Valid Requests|count|ValidRequestCount|userId and BucketName|Value|
|Availability by User|%|Availability|userId and BucketName|Value|

