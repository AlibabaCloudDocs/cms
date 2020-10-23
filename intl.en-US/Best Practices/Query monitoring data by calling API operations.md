# Query monitoring data by calling API operations

This topic describes how to call API operations to query monitoring data of various Alibaba Cloud services.

Large enterprises have their own operations and maintenance \(O&M\) and monitoring systems. When they migrate business to Alibaba Cloud, these enterprises need to integrate monitoring data of cloud resources with their existing systems. This topic describes how to use Cloud Monitor API operations to query monitoring data of various services. This way, you can integrate monitoring data of Alibaba Cloud with your existing systems.

## API operations for querying monitoring data of metrics

Cloud Monitor provides the following operations to query monitoring data of metrics:

-   Operation used to query services: queries services that can be monitored by Cloud Monitor. For more information, see [DescribeProjectMeta](https://www.alibabacloud.com/help/doc-detail/114916.htm).
-   Operation used to query metrics: queries metrics that are available for a monitored service. For more information, see [DescribeMetricMetaList](https://www.alibabacloud.com/help/doc-detail/98846.htm).
-   Operations used to query monitoring data: query monitoring data based on services and metrics. For more information, see [DescribeMetricMetaList](https://www.alibabacloud.com/help/doc-detail/98846.htm) and [DescribeMetricLast](https://www.alibabacloud.com/help/doc-detail/51939.htm).

Usage notes:

-   The DescribeMetricList and DescribeMetricLast operations allow you to query data of a specific metric for all your instances. You can create multiple threads to query the monitoring data of multiple metrics at a time. Alternatively, you can create a single thread to obtain the monitoring data of multiple metrics one by one.
-   The DescribeMetricList operation supports a maximum of 20 queries per second \(QPS\), whereas the DescribeMetricLast operation supports a maximum of 30 QPS.
-   The DescribeMetricLast operation is applicable to scenarios where you need to obtain the most recent monitoring data at regular intervals. The time window automatically slides forward. For each window, the most recent record is retrieved.
-   Services may take some time to report monitoring data to Cloud Monitor. The delay varies with different services. We recommend that you extend the time window by 5 to 10 minutes when you call the DescribeMetricLast operation to query the latest data.
-   Cloud Monitor retains data that is obtained every few seconds for 7 days, and data that is obtained every few minutes for 31 days.
-   If you want to query the aggregate data of all your instances, you do not need to specify the Dimensions parameter.

## Example

The following example demonstrates how to call the DescribeMetricLast operation to query the latest monitoring data and the DescribeMetricList operation to query the monitoring data in a specified time range.

```
import com.aliyuncs.DefaultAcsClient;
import com.aliyuncs.IAcsClient;
import com.aliyuncs.exceptions.ClientException;
import com.aliyuncs.exceptions.ServerException;
import com.aliyuncs.profile.DefaultProfile;
import com.google.gson.Gson;
import java.util.*;
import com.aliyuncs.cms.model.v20190101. *;

/**
 * You can call the DescribeMetricList operation to query the monitoring data of a specified instance in a specified time range.
 * The DescribeMetricList operation can query the monitoring data of multiple instances at a time.
 * To query the monitoring data of multiple instances in a specified time range, specify these instances for the query. You can specify a maximum of 10 instances at a time.
 * Query monitoring data in a specified time range.
 */
public class DescribeMetricList {

    public static void main(String[] args) {
        DefaultProfile profile = DefaultProfile.getProfile("cn-hangzhou", "<accessKeyId>", "<accessSecret>");
        IAcsClient client = new DefaultAcsClient(profile);

        DescribeMetricListRequest request = new DescribeMetricListRequest();
        // You can call the DescribeMetricMetaList and DescribeProjectMeta operations to query the namespace and metric.
        request.setNamespace("acs_ecs_dashboard");
        request.setMetricName("cpu_total");
        // The Period parameter is set to 60, which specifies that monitoring data is obtained every 60 seconds. The value of the Period parameter varies with metrics. The period of most metrics are set to 60 seconds by default.
        request.setPeriod("60");
        // The number of entries to return on each page. A maximum of 1,000 entries can be returned for each query.
        request.setLength("1000");
        // The beginning of the time range to query.
        request.setStartTime("2019-07-22 11:00:00");
        // The end of the time range to query.
        request.setEndTime("2019-07-22 12:00:00");
        // Set the Dimensions parameter to filter monitoring data. The value can be a JSON array or a JSON object.
        request.setDimensions("[{\"instanceId\":\"i-8vb******\"}]");

        try {
            DescribeMetricListResponse response = client.getAcsResponse(request);
            System.out.println(new Gson().toJson(response));
        } catch (ServerException e) {
            e.printStackTrace();
        } catch (ClientException e) {
            System.out.println("ErrCode:" + e.getErrCode());
            System.out.println("ErrMsg:" + e.getErrMsg());
            System.out.println("RequestId:" + e.getRequestId());
        }

    }
}
                
```

```
import com.aliyuncs.DefaultAcsClient;
import com.aliyuncs.IAcsClient;
import com.aliyuncs.exceptions.ClientException;
import com.aliyuncs.exceptions.ServerException;
import com.aliyuncs.profile.DefaultProfile;
import com.google.gson.Gson;
import java.util.*;
import com.aliyuncs.cms.model.v20190101. *;

/**
 * Query the latest monitoring data.
 **/
public class DescribeMetricLast {

    public static void main(String[] args) {
        DefaultProfile profile = DefaultProfile.getProfile("cn-hangzhou", "<accessKeyId>", "<accessSecret>");
        IAcsClient client = new DefaultAcsClient(profile);

        DescribeMetricLastRequest request = new DescribeMetricLastRequest();

         // You can call the DescribeMetricMetaList and DescribeProjectMeta operations to query the namespace and metric.        
        request.setNamespace("acs_ecs_dashboard");
        request.setMetricName("cpu_total");
        // Set the Dimensions parameter to filter monitoring data. The value can be a JSON array or a JSON object.
        request.setDimensions("[{\"instanceId\":\"i-8vb6p*****\"}]");
        // The number of entries to return on each page. A maximum of 1,000 entries can be returned for each query.
        request.setLength("1000");
        // The beginning of the time range to query.
        request.setStartTime("2019-07-22 11:00:00");
        // The end of the time range to query.
        request.setEndTime("2019-07-22 12:00:00");
        request.setPeriod("60");

        try {
            DescribeMetricLastResponse response = client.getAcsResponse(request);
            System.out.println(new Gson().toJson(response));
        } catch (ServerException e) {
            e.printStackTrace();
        } catch (ClientException e) {
            System.out.println("ErrCode:" + e.getErrCode());
            System.out.println("ErrMsg:" + e.getErrMsg());
            System.out.println("RequestId:" + e.getRequestId());
        }

    }
}               
```

