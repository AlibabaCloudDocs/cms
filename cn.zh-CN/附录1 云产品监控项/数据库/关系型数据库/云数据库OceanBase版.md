# 云数据库OceanBase版

通过本文您可以了解云数据库OceanBase版的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_oceanbase**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|active\_memstore\_percent\_by\_trigger|%|active\_memstore\_percent\_by\_trigger|userId、obClusterId|Average|
|active\_memstore\_percent\_by\_trigger\_instance|%|active\_memstore\_percent\_by\_trigger\_instance|userId、obClusterId、obInstanceId|Average|
|active\_memstore\_percent\_by\_trigger\_tenant|%|active\_memstore\_percent\_by\_trigger\_tenant|userId、obClusterId、obTenantId|Average|
|active\_memstore\_used|Byte|active\_memstore\_used|userId、obClusterId、obTenantId|Sum|
|active\_memstore\_used\_instance|Byte|active\_memstore\_used\_instance|userId、obClusterId、obInstanceId|Average|
|active\_sessions|Count|active\_sessions|userId、obClusterId|Sum|
|active\_sessions\_instance|Count|active\_sessions\_instance|userId、obClusterId、obInstanceId|Average|
|active\_sessions\_max\_tenant|%|active\_sessions\_max\_tenant|userId、obClusterId、obTenantId|Max|
|active\_sessions\_tenant|Count|active\_sessions\_tenant|userId、obClusterId、obTenantId|Sum|
|active\_sessions\_tenant\_instance|Count|active\_sessions\_tenant\_instance|userId、obClusterId、obTenantId、obInstanceId|Sum|
|block\_cache\_hit\_percent|%|block\_cache\_hit\_percent|userId、obClusterId、obTenantId|Average|
|block\_cache\_hit\_percent\_instance|%|block\_cache\_hit\_percent\_instance|userId、obClusterId、obInstanceId|Average|
|block\_cache\_hit\_percent\_tenant|%|block\_cache\_hit\_percent\_tenant|userId、obClusterId、obTenantId|Average|
|block\_index\_cache\_hit\_percent|%|block\_index\_cache\_hit\_percent|userId、obClusterId、obTenantId|Average|
|block\_index\_cache\_hit\_percent\_instance|%|block\_index\_cache\_hit\_percent\_instance|userId、obClusterId、obInstanceId|Average|
|block\_index\_cache\_hit\_percent\_tenant|%|block\_index\_cache\_hit\_percent\_tenant|userId、obClusterId、obTenantId|Average|
|bloom\_filter\_cache\_hit\_percent|%|bloom\_filter\_cache\_hit\_percent|userId、obClusterId|Average|
|bloom\_filter\_cache\_hit\_percent\_instance|%|bloom\_filter\_cache\_hit\_percent\_instance|userId、obClusterId、obInstanceId|Average|
|bloom\_filter\_cache\_hit\_percent\_tenant|%|bloom\_filter\_cache\_hit\_percent\_tenant|userId、obClusterId、obTenantId|Average|
|core\_count\_instance|Count|core\_count\_instance|userId、obClusterId、obInstanceId|Average|
|cpu\_usage|%|cpu\_usage|userId、obClusterId|Average|
|cpu\_usage\_avg\_tenant|%|cpu\_usage\_avg\_tenant|userId、obClusterId、obTenantId|Average|
|cpu\_usage\_instance|%|cpu\_usage\_instance|userId、obClusterId、obInstanceId|Average|
|cpu\_usage\_max\_tenant|%|cpu\_usage\_max\_tenant|userId、obClusterId、obTenantId|Max|
|cpu\_usage\_tenant|%|cpu\_usage\_tenant|userId、obClusterId、obInstanceId|Average|
|cpu\_util\_instance|%|cpu\_util\_instance|userId、obClusterId、obInstanceId|Average|
|disk\_data\_size\_instance|GB|disk\_data\_size\_instance|userId、obClusterId、obInstanceId|Average|
|disk\_data\_usage\_instance|%|disk\_data\_usage\_instance|userId、obClusterId、obInstanceId|Average|
|disk\_genernal\_size\_instance|GB|disk\_genernal\_size\_instance|userId、obClusterId、obInstanceId|Average|
|disk\_genernal\_usage\_instance|%|disk\_genernal\_usage\_instance|userId、obClusterId、obInstanceId|Average|
|disk\_log\_size\_instance|GB|disk\_log\_size\_instance|userId、obClusterId、obInstanceId|Average|
|disk\_log\_usage\_instance|%|disk\_log\_usage\_instance|userId、obClusterId、obInstanceId|Average|
|disk\_ob\_data\_size\_instance|GB|disk\_ob\_data\_size\_instance|userId、obClusterId、obInstanceId|Average|
|io\_await\_instance|Milliseconds|io\_await\_instance|userId、obClusterId、obInstanceId|Average|
|io\_read\_bytes|Count|io\_read\_bytes|userId、obClusterId|Sum|
|io\_read\_bytes\_instance|%|io\_read\_bytes\_instance|userId、obClusterId、obInstanceId|Average|
|io\_read\_bytes\_tenant|Count|io\_read\_bytes\_tenant|userId、obClusterId、obTenantId|Sum|
|io\_read\_count|Count|io\_read\_count|userId、obClusterId|Sum|
|io\_read\_count\_instance|%|io\_read\_count\_instance|userId、obClusterId、obInstanceId|Average|
|io\_read\_count\_tenant|Count|io\_read\_count\_tenant|userId、obClusterId、obTenantId|Sum|
|io\_read\_delay|Milliseconds|io\_read\_delay|userId、obClusterId|Sum|
|io\_read\_delay\_instance|%|io\_read\_delay\_instance|userId、obClusterId、obInstanceId|Average|
|io\_read\_delay\_tenant|Count|io\_read\_delay\_tenant|userId、obClusterId、obTenantId|Sum|
|io\_read\_rt|Milliseconds|io\_read\_rt|userId、obClusterId|Average|
|io\_read\_rt\_instance|Milliseconds|io\_read\_rt\_instance|userId、obClusterId、obInstanceId|Average|
|io\_read\_rt\_tenant|Milliseconds|io\_read\_rt\_tenant|userId、obClusterId、obTenantId|Average|
|io\_write\_bytes|Count|io\_write\_bytes|userId、obClusterId|Sum|
|io\_write\_bytes\_instance|%|io\_write\_bytes\_instance|userId、obClusterId、obInstanceId|Average|
|io\_write\_bytes\_tenant|Count|io\_write\_bytes\_tenant|userId、obClusterId、obTenantId|Sum|
|io\_write\_count|Count|io\_write\_count|userId、obClusterId|Sum|
|io\_write\_count\_instance|%|io\_write\_count\_instance|userId、obClusterId、obInstanceId|Average|
|io\_write\_count\_tenant|Count|io\_write\_count\_tenant|userId、obClusterId、obTenantId|Sum|
|io\_write\_delay|ms|io\_write\_delay|userId、obClusterId|Sum|
|io\_write\_delay\_instance|%|io\_write\_delay\_instance|userId、obClusterId、obInstanceId|Average|
|io\_write\_delay\_tenant|Count|io\_write\_delay\_tenant|userId、obClusterId、obTenantId|Sum|
|io\_write\_rt|Milliseconds|io\_write\_rt|userId、obClusterId|Average|
|io\_write\_rt\_instance|Milliseconds|io\_write\_rt\_instance|userId、obClusterId、obInstanceId|Average|
|io\_write\_rt\_tenant|Milliseconds|io\_write\_rt\_tenant|userId、obClusterId、obTenantId|Average|
|load\_load1\_instance|%|load\_load1\_instance|userId、obClusterId、obInstanceId|Average|
|location\_cache\_hit\_percent|%|location\_cache\_hit\_percent|userId、obClusterId|Average|
|location\_cache\_hit\_percent\_instance|%|location\_cache\_hit\_percent\_instance|userId、obClusterId、obInstanceId|Average|
|location\_cache\_hit\_percent\_tenant|%|location\_cache\_hit\_percent\_tenant|userId、obClusterId、obTenantId|Average|
|machine\_mem\_used\_percent\_instance|%|machine\_mem\_used\_percent\_instance|userId、obClusterId、obInstanceId|Average|
|max\_memory\_size|Byte|max\_memory\_size|userId、obClusterId|Sum|
|max\_memory\_size\_instance|Byte|max\_memory\_size\_instance|userId、obClusterId、obInstanceId|Average|
|max\_memory\_size\_tenant|Count|max\_memory\_size\_tenant|userId、obClusterId、obTenantId|Sum|
|memstore\_limit|%|memstore\_limit|userId、obClusterId、obInstanceId|Average|
|memstore\_limit\_tenant|Count|memstore\_limit\_tenant|userId、obClusterId、obTenantId|Sum|
|min\_memory\_size|Byte|min\_memory\_size|userId、obClusterId|Sum|
|min\_memory\_size\_instance|Byte|min\_memory\_size\_instance|userId、obClusterId、obInstanceId|Average|
|min\_memory\_size\_tenant|Count|min\_memory\_size\_tenant|userId、obClusterId、obTenantId|Sum|
|ob\_server\_inactive\_count\_instance|Count|ob\_server\_inactive\_count\_instance|userId、obClusterId、obInstanceId|Average|
|ob\_sys\_clog\_unsync\_instance|Count|ob\_sys\_clog\_unsync\_instance|userId、obClusterId、obInstanceId|Average|
|ob\_sys\_daily\_merge\_timeout\_instance|Count|ob\_sys\_daily\_merge\_timeout\_instance|userId、obClusterId、obInstanceId|Average|
|ob\_sys\_disk\_invalid\_instance|Count|ob\_sys\_disk\_invalid\_instance|userId、obClusterId、obInstanceId|Average|
|ob\_sys\_election\_info\_instance|Count|ob\_sys\_election\_info\_instance|userId、obClusterId、obInstanceId|Average|
|ob\_sys\_leader\_election\_instance|Count|ob\_sys\_leader\_election\_instance|userId、obClusterId、obInstanceId|Average|
|qps|Count|qps|userId、obClusterId|Sum|
|qps\_instance|Count|qps\_instance|userId、obClusterId、obInstanceId|Average|
|qps\_rt|Milliseconds|qps\_rt|userId、obClusterId|Average|
|qps\_rt\_instance|Milliseconds|qps\_rt\_instance|userId、obClusterId、obInstanceId|Average|
|qps\_rt\_tenant|Milliseconds|qps\_rt\_tenant|userId、obClusterId、obTenantId|Average|
|qps\_tenant|Count|qps\_tenant|userId、obClusterId、obTenantId|Sum|
|request\_dequeue\_count|Count|request\_dequeue\_count|userId、obClusterId|Sum|
|request\_dequeue\_count\_instance|Count|request\_dequeue\_count\_instance|userId、obClusterId、obInstanceId|Average|
|request\_dequeue\_count\_tenant|Count|request\_dequeue\_count\_tenant|userId、obClusterId、obTenantId|Sum|
|request\_enqueue\_count|Count|request\_enqueue\_count|userId、obClusterId、obTenantId|Sum|
|request\_enqueue\_count\_instance|Count|request\_enqueue\_count\_instance|userId、obClusterId、obInstanceId|Average|
|request\_queue\_rt|Milliseconds|request\_queue\_rt|userId、obClusterId|Average|
|request\_queue\_rt\_instance|Milliseconds|request\_queue\_rt\_instance|userId、obClusterId、obInstanceId|Average|
|request\_queue\_rt\_tenant|Milliseconds|request\_queue\_rt\_tenant|userId、obClusterId、obTenantId|Average|
|request\_queue\_time|Milliseconds|request\_queue\_time|userId、obClusterId|Sum|
|request\_queue\_time\_instance|Count|request\_queue\_time\_instance|userId、obClusterId、obInstanceId|Average|
|request\_queue\_time\_tenant|Count|request\_queue\_time\_tenant|userId、obClusterId、obTenantId|Sum|
|row\_cache\_hit\_percent|%|row\_cache\_hit\_percent|userId、obClusterId|Average|
|row\_cache\_hit\_percent\_instance|%|row\_cache\_hit\_percent\_instance|userId、obClusterId、obInstanceId|Average|
|row\_cache\_hit\_percent\_tenant|%|row\_cache\_hit\_percent\_tenant|userId、obClusterId、obTenantId|Average|
|rpc\_packet\_in|Count|rpc\_packet\_in|userId、obClusterId|Sum|
|rpc\_packet\_in\_bytes\_ps|Count|rpc\_packet\_in\_bytes\_ps|userId、obClusterId|Sum|
|rpc\_packet\_in\_bytes\_ps\_instance|Count|rpc\_packet\_in\_bytes\_ps\_instance|userId、obClusterId、obInstanceId|Average|
|rpc\_packet\_in\_bytes\_ps\_tenant|Count|rpc\_packet\_in\_bytes\_ps\_tenant|userId、obClusterId、obTenantId|Sum|
|rpc\_packet\_in\_instance|Milliseconds|rpc\_packet\_in\_instance|userId、obClusterId、obInstanceId|Average|
|rpc\_packet\_in\_tenant|Count|rpc\_packet\_in\_tenant|userId、obClusterId、obTenantId|Sum|
|rpc\_packet\_out|Count|rpc\_packet\_out|userId、obClusterId|Sum|
|rpc\_packet\_out\_bytes|Count|rpc\_packet\_out\_bytes|userId、obClusterId|Sum|
|rpc\_packet\_out\_bytes\_instance|Count|rpc\_packet\_out\_bytes\_instance|userId、obClusterId、obInstanceId|Average|
|rpc\_packet\_out\_bytes\_tenant|Count|rpc\_packet\_out\_bytes\_tenant|userId、obClusterId|Sum|
|rpc\_packet\_out\_instance|Count|rpc\_packet\_out\_instance|userId、obClusterId、obInstanceId|Average|
|rpc\_packet\_out\_tenant|Count|rpc\_packet\_out\_tenant|userId、obClusterId、obTenantId|Sum|
|slow\_log\_count\_instance|Count|slow\_log\_count\_instance|userId、obClusterId、obInstanceId|Average|
|slow\_log\_count\_tenant|Count|slow\_log\_count\_tenant|userId、obClusterId、obTenantId|Sum|
|slow\_log\_max\_execute\_time\_tenant|Count|slow\_log\_max\_execute\_time\_tenant|userId、obClusterId、obTenantId|Max|
|sql\_delete\_count|Count|sql\_delete\_count|userId、obClusterId|Sum|
|sql\_delete\_count\_instance|Count|sql\_delete\_count\_instance|userId、obClusterId、obInstanceId|Average|
|sql\_delete\_count\_tenant|Count|sql\_delete\_count\_tenant|userId、obClusterId、obTenantId|Sum|
|sql\_delete\_rt|Milliseconds|sql\_delete\_rt|userId、obClusterId|Average|
|sql\_delete\_rt\_instance|Milliseconds|sql\_delete\_rt\_instance|userId、obClusterId、obInstanceId|Average|
|sql\_delete\_rt\_tenant|Milliseconds|sql\_delete\_rt\_tenant|userId、obClusterId、obTenantId|Average|
|sql\_distributed\_count|Count|sql\_distributed\_count|userId、obClusterId|Sum|
|sql\_distributed\_count\_instance|Count|sql\_distributed\_count\_instance|userId、obClusterId、obInstanceId|Average|
|sql\_distributed\_count\_tenant|Count|sql\_distributed\_count\_tenant|userId、obClusterId、obTenantId|Sum|
|sql\_dml\_rt|Milliseconds|sql\_dml\_rt|userId、obClusterId|Sum|
|sql\_dml\_rt\_instance|Milliseconds|sql\_dml\_rt\_instance|userId、obClusterId、obInstanceId|Average|
|sql\_dml\_rt\_tenant|Milliseconds|sql\_dml\_rt\_tenant|userId、obClusterId、obTenantId|Average|
|sql\_insert\_count|Count|sql\_insert\_count|userId、obClusterId|Sum|
|sql\_insert\_count\_instance|Count|sql\_insert\_count\_instance|userId、obClusterId、obInstanceId|Average|
|sql\_insert\_count\_tenant|Count|sql\_insert\_count\_tenant|userId、obClusterId、obTenantId|Sum|
|sql\_insert\_rt|Milliseconds|sql\_insert\_rt|userId、obClusterId|Average|
|sql\_insert\_rt\_instance|Milliseconds|sql\_insert\_rt\_instance|userId、obClusterId、obInstanceId|Average|
|sql\_insert\_rt\_tenant|Milliseconds|sql\_insert\_rt\_tenant|userId、obClusterId、obInstanceId|Average|
|sql\_remote\_count|Count|sql\_remote\_count|userId、obClusterId|Sum|
|sql\_remote\_count\_instance|Count|sql\_remote\_count\_instance|userId、obClusterId、obInstanceId|Average|
|sql\_remote\_count\_tenant|Count|sql\_remote\_count\_tenant|userId、obClusterId、obTenantId|Sum|
|sql\_replace\_count|Count|sql\_replace\_count|userId、obClusterId|Sum|
|sql\_replace\_count\_instance|Count|sql\_replace\_count\_instance|userId、obClusterId、obInstanceId|Average|
|sql\_replace\_count\_tenant|Count|sql\_replace\_count\_tenant|userId、obClusterId、obTenantId|Sum|
|sql\_replace\_rt|Milliseconds|sql\_replace\_rt|userId、obClusterId|Average|
|sql\_replace\_rt\_instance|Milliseconds|sql\_replace\_rt\_instance|userId、obClusterId、obInstanceId|Average|
|sql\_replace\_rt\_tenant|Milliseconds|sql\_replace\_rt\_tenant|userId、obClusterId、obTenantId|Average|
|sql\_select\_count\_instance|Count|sql\_select\_count\_instance|userId、obClusterId、obInstanceId|Average|
|sql\_select\_count\_tenant|Count|sql\_select\_count\_tenant|userId、obClusterId、obTenantId|Sum|
|sql\_select\_rt|Milliseconds|sql\_select\_rt|userId、obClusterId|Average|
|sql\_select\_rt\_instance|Milliseconds|sql\_select\_rt\_instance|userId、obClusterId、obInstanceId|Average|
|sql\_select\_rt\_tenant|Milliseconds|sql\_select\_rt\_tenant|userId、obClusterId、obTenantId|Average|
|sql\_update\_count|Count|sql\_update\_count|userId、obClusterId|Sum|
|sql\_update\_count\_instance|Count|sql\_update\_count\_instance|userId、obClusterId、obInstanceId|Average|
|sql\_update\_count\_tenant|Count|sql\_update\_count\_tenant|userId、obClusterId、obInstanceId|Average|
|sql\_update\_rt|Milliseconds|sql\_update\_rt|userId、obClusterId|Average|
|sql\_update\_rt\_instance|Milliseconds|sql\_update\_rt\_instance|userId、obClusterId、obInstanceId|Average|
|sql\_update\_rt\_tenant|Milliseconds|sql\_update\_rt\_tenant|userId、obClusterId、obInstanceId|Average|
|storage\_delete\_row\_count|Count|storage\_delete\_row\_count|userId、obClusterId|Sum|
|storage\_delete\_row\_count\_instance|Count|storage\_delete\_row\_count\_instance|userId、obClusterId、obInstanceId|Average|
|storage\_delete\_row\_count\_tenant|Count|storage\_delete\_row\_count\_tenant|userId、obClusterId、obTenantId|Sum|
|storage\_insert\_row\_count|Count|storage\_insert\_row\_count|userId、obClusterId|Sum|
|storage\_insert\_row\_count\_instance|Count|storage\_insert\_row\_count\_instance|userId、obClusterId、obInstanceId|Average|
|storage\_insert\_row\_count\_tenant|Count|storage\_insert\_row\_count\_tenant|userId、obClusterId、obTenantId|Sum|
|storage\_read\_row\_count|Count|storage\_read\_row\_count|userId、obClusterId、obTenantId|Sum|
|storage\_read\_row\_count\_instance|Count|storage\_read\_row\_count\_instance|userId、obClusterId、obInstanceId|Average|
|storage\_update\_row\_count|Count|storage\_update\_row\_count|userId、obClusterId|Sum|
|storage\_update\_row\_count\_instance|Count|storage\_update\_row\_count\_instance|userId、obClusterId、obInstanceId|Average|
|storage\_update\_row\_count\_tenant|Count|storage\_update\_row\_count\_tenant|userId、obClusterId、obTenantId|Sum|
|tcp\_retran\_instance|%|tcp\_retran\_instance|userId、obClusterId、obInstanceId|Average|
|total\_memstore\_percent\_by\_limit|%|total\_memstore\_percent\_by\_limit|userId、obClusterId|Average|
|total\_memstore\_percent\_by\_limit\_instance|%|total\_memstore\_percent\_by\_limit\_instance|userId、obClusterId、obInstanceId|Average|
|total\_memstore\_percent\_by\_limit\_tenant|%|total\_memstore\_percent\_by\_limit\_tenant|userId、obClusterId、obTenantId|Average|
|total\_memstore\_used|Byte|total\_memstore\_used|userId、obClusterId|Sum|
|total\_memstore\_used\_instance|Byte|total\_memstore\_used\_instance|userId、obClusterId、obInstanceId|Average|
|total\_memstore\_used\_tenant|Count|total\_memstore\_used\_tenant|userId、obClusterId、obTenantId|Sum|
|tps|Count|tps|userId、obClusterId|Sum|
|tps\_instance|Count|tps\_instance|userId、obClusterId、obInstanceId|Average|
|tps\_rt|Milliseconds|tps\_rt|userId、obClusterId|Average|
|tps\_rt\_instance|Milliseconds|tps\_rt\_instance|userId、obClusterId、obInstanceId|Average|
|tps\_rt\_tenant|Milliseconds|tps\_rt\_tenant|userId、obClusterId、obTenantId|Average|
|tps\_tenant|Count|tps\_tenant|userId、obClusterId、obTenantId|Sum|
|traffic\_bytin\_instance|Byte|traffic\_bytin\_instance|userId、obClusterId、obInstanceId|Average|
|traffic\_bytout\_instance|Byte|traffic\_bytout\_instance|userId、obClusterId、obInstanceId|Average|
|提交的事物数量|Count|trans\_commit\_count|userId、obClusterId|Sum|
|trans\_commit\_count\_instance|Count|trans\_commit\_count\_instance|userId、obClusterId、obInstanceId|Average|
|trans\_commit\_count\_tenant|Count|trans\_commit\_count\_tenant|userId、obClusterId、obTenantId|Sum|
|trans\_commit\_rt|Milliseconds|trans\_commit\_rt|userId、obClusterId|Average|
|trans\_commit\_rt\_instance|Milliseconds|trans\_commit\_rt\_instance|userId、obClusterId、obInstanceId|Average|
|trans\_commit\_rt\_tenant|Milliseconds|trans\_commit\_rt\_tenant|userId、obClusterId、obTenantId|Average|
|trans\_multi\_partition\_count|Count|trans\_multi\_partition\_count|userId、obClusterId、obInstanceId|Average|
|trans\_multi\_partition\_count\_tenant|Count|trans\_multi\_partition\_count\_tenant|userId、obClusterId、obTenantId|Sum|
|trans\_rollback\_count|Count|trans\_rollback\_count|userId、obClusterId|Sum|
|trans\_rollback\_count\_instance|Count|trans\_rollback\_count\_instance|userId、obClusterId、obInstanceId|Average|
|trans\_rollback\_count\_tenant|Count|trans\_rollback\_count\_tenant|userId、obClusterId、obTenantId|Sum|
|trans\_rollback\_rt|Milliseconds|trans\_rollback\_rt|userId、obClusterId|Average|
|trans\_rollback\_rt\_instance|Milliseconds|trans\_rollback\_rt\_instance|userId、obClusterId、obInstanceId|Average|
|trans\_rollback\_rt\_tenant|Milliseconds|trans\_rollback\_rt\_tenant|userId、obClusterId、obTenantId|Average|
|trans\_single\_partition\_count|Count|trans\_single\_partition\_count|userId、obClusterId|Sum|
|trans\_single\_partition\_count\_instance|Count|trans\_single\_partition\_count\_instance|userId、obClusterId、obInstanceId|Average|
|trans\_single\_partition\_count\_tenant|Count|trans\_single\_partition\_count\_tenant|userId、obClusterId、obTenantId|Sum|
|trans\_timeout\_count|Count|trans\_timeout\_count|userId、obClusterId|Sum|
|trans\_timeout\_count\_instance|Count|trans\_timeout\_count\_instance|userId、obClusterId、obInstanceId|Average|
|trans\_timeout\_count\_tenant|Count|trans\_timeout\_count\_tenant|userId、obClusterId、obTenantId|Sum|

