# Cloud-native multi-mode database Lindorm

This topic describes the metrics of ApsaraDB for Lindorm.

When you call an API operation provided by Cloud Monitor, you may need to set the **Namespace** and **Period** parameters. Set the parameters for the current service in the following way:

-   Set the **Namespace** parameter to **acs\_lindorm**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

The following table describes the valid values of the **MetricName** and **Dimensions** parameters for the current service.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Above memstore|Frequency|above\_memstore\_count|userId, instanceId, and host|Average, Maximum, and Minimum|
|bytes\_in|Bytes/s|bytes\_in|userId, instanceId, and host|Average, Maximum, and Minimum|
|bytes\_out|Bytes/s|bytes\_out|userId, instanceId, and host|Average, Maximum, and Minimum|
|cold\_storage\_total\_bytes|Bytes|cold\_storage\_total\_bytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|cold\_storage\_used\_bytes|Bytes|cold\_storage\_used\_bytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|cold\_storage\_used\_percent|%|cold\_storage\_used\_percent|userId, instanceId, and host|Average, Maximum, and Minimum|
|compaction\_queue\_size|Count|compaction\_queue\_size|userId, instanceId, and host|Average, Maximum, and Minimum|
|cpu\_idle|%|cpu\_idle|userId, instanceId, and host|Average, Maximum, and Minimum|
|cpu\_system|%|cpu\_system|userId, instanceId, and host|Average, Maximum, and Minimum|
|cpu\_user|%|cpu\_user|userId, instanceId, and host|Average, Maximum, and Minimum|
|cpu\_wio|%|cpu\_wio|userId, instanceId, and host|Average, Maximum, and Minimum|
|Disk read bytes|Bytes/s|disk\_readbytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|Disk write bytes|Bytes/s|disk\_writebytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|failed\_job\_count|Count|failed\_job\_count|userId, instanceId, and host|Average, Maximum, and Minimum|
|Get ops|CountS|get\_num\_ops|userId, instanceId, and host|Average, Maximum, and Minimum|
|get\_rt\_avg|Milliseconds|get\_rt\_avg|userId, instanceId, and host|Average, Maximum, and Minimum|
|Get P99 RT|Milliseconds|get\_rt\_p99|userId, instanceId, and host|Average, Maximum, and Minimum|
|handler\_queue\_size|Count|handler\_queue\_size|userId, instanceId, and host|Average, Maximum, and Minimum|
|load\_five|Load|load\_five|userId, instanceId, and host|Average, Maximum, and Minimum|
|load\_one|Load|load\_one|userId, instanceId, and host|Average, Maximum, and Minimum|
|mem\_buff\_cache|Bytes|mem\_buff\_cache|userId, instanceId, and host|Average, Maximum, and Minimum|
|mem\_free|Bytes|mem\_free|userId, instanceId, and host|Average, Maximum, and Minimum|
|mem\_shared|Bytes|mem\_shared|userId, instanceId, and host|Average, Maximum, and Minimum|
|mem\_total|Bytes|mem\_total|userId, instanceId, and host|Average, Maximum, and Minimum|
|mem\_used\_percent|%|mem\_used\_percent|userId, instanceId, and host|Average, Maximum, and Minimum|
|Put OPS|CountS|put\_num\_ops|userId, instanceId, and host|Average, Maximum, and Minimum|
|put\_rt\_avg|Milliseconds|put\_rt\_avg|userId, instanceId, and host|Average, Maximum, and Minimum|
|Put P99 RT|Milliseconds|put\_rt\_p99|userId, instanceId, and host|Average, Maximum, and Minimum|
|read\_data\_kb|KB/s|read\_data\_kb|userId, instanceId, and host|Average, Maximum, and Minimum|
|read\_ops|CountS|read\_ops|userId, instanceId, and host|Average, Maximum, and Minimum|
|read\_rt|Milliseconds|read\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|regions\_per\_ldserver|Count|regions\_per\_ldserver|userId, instanceId, and host|Average, Maximum, and Minimum|
|Scan ops|CountS|scan\_num\_ops|userId, instanceId, and host|Average, Maximum, and Minimum|
|Scan avg RT|Milliseconds|scan\_rt\_avg|userId, instanceId, and host|Average, Maximum, and Minimum|
|Scan P99 RT|Milliseconds|scan\_rt\_p99|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_bytes\_in|Bytes/s|search\_bytes\_in|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_bytes\_out|Bytes/s|search\_bytes\_out|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_cpu\_idle|%|search\_cpu\_idle|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_cpu\_system|%|search\_cpu\_system|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_cpu\_user|%|search\_cpu\_user|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_cpu\_wio|%|search\_cpu\_wio|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_disk\_readbytes|Bytes/s|search\_disk\_readbytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_disk\_writebytes|Bytes/s|search\_disk\_writebytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_load\_five|Load|search\_load\_five|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_load\_one|Load|search\_load\_one|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_mem\_buff\_cache|Bytes|search\_mem\_buff\_cache|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_mem\_free|Bytes|search\_mem\_free|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_mem\_shared|Bytes|search\_mem\_shared|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_mem\_total|Bytes|search\_mem\_total|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_mem\_used\_percent|%|search\_mem\_used\_percent|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_select\_15minRate|CountS|search\_select\_15minRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_select\_1minRate|CountS|search\_select\_1minRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_select\_5minRate|CountS|search\_select\_5minRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_select\_count|Count|search\_select\_count|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_select\_max\_rt|Milliseconds|search\_select\_max\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_select\_meanRate|CountS|search\_select\_meanRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_select\_mean\_rt|Milliseconds|search\_select\_mean\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|Select p75 RT|Milliseconds|search\_select\_p75\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|Select p95 RT|Milliseconds|search\_select\_p95\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|Select p999 RT|Milliseconds|search\_select\_p999\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|Select p99 RT|Milliseconds|search\_select\_p99\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_update\_15minRate|CountS|search\_update\_15minRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_update\_1minRate|CountS|search\_update\_1minRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_update\_5minRate|CountS|search\_update\_5minRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_update\_count|Count|search\_update\_count|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_update\_max\_rt|Milliseconds|search\_update\_max\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_update\_meanRate|CountS|search\_update\_meanRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|search\_update\_mean\_rt|Milliseconds|search\_update\_mean\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|Update P75 RT|Milliseconds|search\_update\_p75\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|Update P95 RT|Milliseconds|search\_update\_p95\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|Update P999 RT|Milliseconds|search\_update\_p999\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|Update P99 RT|Milliseconds|search\_update\_p99\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_bytes\_in|Bytes/s|solr\_bytes\_in|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_bytes\_out|Bytes/s|solr\_bytes\_out|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_cpu\_idle|%|solr\_cpu\_idle|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_cpu\_system|%|solr\_cpu\_system|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_cpu\_user|%|solr\_cpu\_user|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_cpu\_wio|%|solr\_cpu\_wio|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_disk\_readbytes|Bytes/s|solr\_disk\_readbytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_disk\_writebytes|Bytes/s|solr\_disk\_writebytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_load\_five|Load|solr\_load\_five|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_load\_one|Load|solr\_load\_one|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_mem\_buff\_cache|Bytes|solr\_mem\_buff\_cache|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_mem\_free|Bytes|solr\_mem\_free|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_mem\_shared|Bytes|solr\_mem\_shared|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_mem\_total|Bytes|solr\_mem\_total|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_mem\_used\_percent|%|solr\_mem\_used\_percent|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_select\_15minRate|CountS|solr\_select\_15minRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_select\_1minRate|CountS|solr\_select\_1minRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_select\_5minRate|CountS|solr\_select\_5minRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_select\_count|Count|solr\_select\_count|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_select\_max\_rt|Milliseconds|solr\_select\_max\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_select\_meanRate|CountS|solr\_select\_meanRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_select\_mean\_rt|Milliseconds|solr\_select\_mean\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|Select P75 RT|Milliseconds|solr\_select\_p75\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|Select P95 RT|Milliseconds|solr\_select\_p95\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|Select P999 RT|Milliseconds|solr\_select\_p999\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|Select P99 RT|Milliseconds|solr\_select\_p99\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_storage\_total\_bytes|Bytes|solr\_storage\_total\_bytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_storage\_used\_bytes|Bytes|solr\_storage\_used\_bytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_storage\_used\_percent|%|solr\_storage\_used\_percent|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_update\_15minRate|CountS|solr\_update\_15minRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_update\_1minRate|CountS|solr\_update\_1minRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_update\_5minRate|CountS|solr\_update\_5minRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_update\_count|Count|solr\_update\_count|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_update\_max\_rt|Milliseconds|solr\_update\_max\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_update\_meanRate|CountS|solr\_update\_meanRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_update\_mean\_rt|Milliseconds|solr\_update\_mean\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|Update p75 RT|Milliseconds|solr\_update\_p75\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|Update p95 RT|Milliseconds|solr\_update\_p95\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|Update p999 RT|Milliseconds|solr\_update\_p999\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|Update p99 RT|Milliseconds|solr\_update\_p99\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|storage\_total\_bytes|Bytes|storage\_total\_bytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|storage\_used\_bytes|Bytes|storage\_used\_bytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|storage usage|%|storage\_used\_percent|userId, instanceId, and host|Average, Maximum, and Minimum|
|store\_locality|%|store\_locality|userId, instanceId, and host|Average, Maximum, and Minimum|
|task\_delay\_max|ms|task\_delay\_max|userId, instanceId, and host|Average, Maximum, and Minimum|
|tsdb\_datapoints\_added|Count|tsdb\_datapoints\_added|userId, instanceId, and host|Average, Maximum, and Minimum|
|tsdb\_disk\_used|Gbyte|tsdb\_disk\_used|userId, instanceId, and host|Average, Maximum, and Minimum|
|tsdb\_jvm\_used\_percent|%|tsdb\_jvm\_used\_percent|userId, instanceId, and host|Average, Maximum, and Minimum|
|warn\_job\_count|Count|warn\_job\_count|userId, instanceId, and host|Average, Maximum, and Minimum|
|worker\_count|Count|worker\_count|userId, instanceId, and host|Average, Maximum, and Minimum|
|write\_data\_kb|KB/s|write\_data\_kb|userId, instanceId, and host|Average, Maximum, and Minimum|
|write\_ops|CountS|write\_ops|userId, instanceId, and host|Average, Maximum, and Minimum|
|write\_rt|Milliseconds|write\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|

