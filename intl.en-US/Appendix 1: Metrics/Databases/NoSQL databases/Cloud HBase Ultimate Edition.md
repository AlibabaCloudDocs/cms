# Cloud HBase Ultimate Edition

This topic describes the metrics for ApsaraDB for HBase Enhanced Edition.

-   Set the **Namespace** parameter to **acs\_hbaseue**.
-   Set the **Period** parameter to an integral multiple of 60s. The default value is 60s.

|Metric|Unit|MetricName|Dimensions|Statistics|
|------|----|----------|----------|----------|
|Above memstore|Frequency|above\_memstore\_count|userId, instanceId, and host|Average, Maximum, and Minimum|
|bytes\_in|byte/s|bytes\_in|userId, instanceId, and host|Average, Maximum, and Minimum|
|bytes\_out|byte/s|bytes\_out|userId, instanceId, and host|Average, Maximum, and Minimum|
|cold\_storage\_total\_bytes|byte|cold\_storage\_total\_bytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|cold\_storage\_used\_bytes|byte|cold\_storage\_used\_bytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|cold\_storage\_used\_percent|%|cold\_storage\_used\_percent|userId, instanceId, and host|Average, Maximum, and Minimum|
|compaction\_queue\_size|count|compaction\_queue\_size|userId, instanceId, and host|Average, Maximum, and Minimum|
|cpu\_idle|%|cpu\_idle|userId, instanceId, and host|Average, Maximum, and Minimum|
|cpu\_system|%|cpu\_system|userId, instanceId, and host|Average, Maximum, and Minimum|
|cpu\_user|%|cpu\_user|userId, instanceId, and host|Average, Maximum, and Minimum|
|cpu\_wio|%|cpu\_wio|userId, instanceId, and host|Average, Maximum, and Minimum|
|Disk read bytes|byte/s|disk\_readbytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|Disk write bytes|byte/s|disk\_writebytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|Get ops|count/s|get\_num\_ops|userId, instanceId, and host|Average, Maximum, and Minimum|
|get\_rt\_avg|ms|get\_rt\_avg|userId, instanceId, and host|Average, Maximum, and Minimum|
|Get P99 RT|ms|get\_rt\_p99|userId, instanceId, and host|Average, Maximum, and Minimum|
|handler\_queue\_size|count|handler\_queue\_size|userId, instanceId, and host|Average, Maximum, and Minimum|
|load\_five|Load|load\_five|userId, instanceId, and host|Average, Maximum, and Minimum|
|load\_one|load|load\_one|userId, instanceId, and host|Average, Maximum, and Minimum|
|mem\_buff\_cache|byte|mem\_buff\_cache|userId, instanceId, and host|Average, Maximum, and Minimum|
|mem\_free|byte|mem\_free|userId, instanceId, and host|Average, Maximum, and Minimum|
|mem\_shared|byte|mem\_shared|userId, instanceId, and host|Average, Maximum, and Minimum|
|mem\_total|byte|mem\_total|userId, instanceId, and host|Average, Maximum, and Minimum|
|mem\_used\_percent|%|mem\_used\_percent|userId, instanceId, and host|Average, Maximum, and Minimum|
|Put OPS|count/s|put\_num\_ops|userId, instanceId, and host|Average, Maximum, and Minimum|
|put\_rt\_avg|ms|put\_rt\_avg|userId, instanceId, and host|Average, Maximum, and Minimum|
|Put P99 RT|ms|put\_rt\_p99|userId, instanceId, and host|Average, Maximum, and Minimum|
|read\_data\_kb|KB/s|read\_data\_kb|userId, instanceId, and host|Average, Maximum, and Minimum|
|read\_ops|count/s|read\_ops|userId, instanceId, and host|Average, Maximum, and Minimum|
|read\_rt|ms|read\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|regions\_per\_ldserver|count|regions\_per\_ldserver|userId, instanceId, and host|Average, Maximum, and Minimum|
|Scan ops|count/s|scan\_num\_ops|userId, instanceId, and host|Average, Maximum, and Minimum|
|Scan avg RT|ms|scan\_rt\_avg|userId, instanceId, and host|Average, Maximum, and Minimum|
|Scan P99 RT|ms|scan\_rt\_p99|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_bytes\_in|byte/s|solr\_bytes\_in|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_bytes\_out|byte/s|solr\_bytes\_out|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_cpu\_idle|%|solr\_cpu\_idle|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_cpu\_system|%|solr\_cpu\_system|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_cpu\_user|%|solr\_cpu\_user|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_cpu\_wio|%|solr\_cpu\_wio|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_disk\_readbytes|byte/s|solr\_disk\_readbytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_disk\_writebytes|byte/s|solr\_disk\_writebytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_load\_five|load|solr\_load\_five|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_load\_one|load|solr\_load\_one|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_mem\_buff\_cache|byte|solr\_mem\_buff\_cache|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_mem\_free|byte|solr\_mem\_free|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_mem\_shared|byte|solr\_mem\_shared|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_mem\_total|byte|solr\_mem\_total|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_mem\_used\_percent|%|solr\_mem\_used\_percent|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_select\_15minRate|count/s|solr\_select\_15minRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_select\_1minRate|count/s|solr\_select\_1minRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_select\_5minRate|count/s|solr\_select\_5minRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_select\_count|count|solr\_select\_count|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_select\_max\_rt|ms|solr\_select\_max\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_select\_meanRate|count/s|solr\_select\_meanRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_select\_mean\_rt|ms|solr\_select\_mean\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_select\_p75\_rt|ms|solr\_select\_p75\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_select\_p95\_rt|ms|solr\_select\_p95\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_select\_p999\_rt|ms|solr\_select\_p999\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_select\_p99\_rt|ms|solr\_select\_p99\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_storage\_total\_bytes|byte|solr\_storage\_total\_bytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_storage\_used\_bytes|byte|solr\_storage\_used\_bytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_storage\_used\_percent|%|solr\_storage\_used\_percent|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_update\_15minRate|count/s|solr\_update\_15minRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_update\_1minRate|count/s|solr\_update\_1minRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_update\_5minRate|count/s|solr\_update\_5minRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_update\_count|count|solr\_update\_count|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_update\_max\_rt|ms|solr\_update\_max\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_update\_meanRate|count/s|solr\_update\_meanRate|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_update\_mean\_rt|ms|solr\_update\_mean\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_update\_p75\_rt|ms|solr\_update\_p75\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_update\_p95\_rt|ms|solr\_update\_p95\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_update\_p999\_rt|ms|solr\_update\_p999\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|solr\_update\_p99\_rt|ms|solr\_update\_p99\_rt|userId, instanceId, and host|Average, Maximum, and Minimum|
|storage\_total\_bytes|byte|storage\_total\_bytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|storage used bytes|byte|storage\_used\_bytes|userId, instanceId, and host|Average, Maximum, and Minimum|
|storage usage|%|storage\_used\_percent|userId, instanceId, and host|Average, Maximum, and Minimum|
|store\_locality|%|store\_locality|userId, instanceId, and host|Average, Maximum, and Minimum|
|write\_data\_kb|KB/s|write\_data\_kb|userId, instanceId, and host|Average, Maximum, and Minimum|
|write\_ops|count/s|write\_ops|userId, instanceId, and host|Average, Maximum, and Minimum|

