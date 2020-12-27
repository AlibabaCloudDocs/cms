# Connect Cloud Monitor to Grafana

Cloud Monitor monitors and visualizes metrics of Alibaba Cloud services and custom metrics sent to Cloud Monitor. You can view monitoring charts in the Cloud Monitor console. You can also use Grafana to display metrics.

1.  Install Grafana.

    **Note:**

    -   If you have installed Grafana, skip this step.
    -   For more information, see [Install Grafana](http://docs.grafana.org/installation/?spm=a2c63.p38356.a3.23.7f634246zuXN5l).
    1.  Install the Grafana software.

        In this example, the Linux CentOS operating system is used. You can install Grafana in Linux CentOS by using one of the following methods:

        -   Method 1:

            yum installhttps://dl.grafana.com/oss/release/grafana-5.3.4-1.x86\_64.rpm

        -   Method 2:

            wgethttps://dl.grafana.com/oss/release/grafana-5.3.4-1.x86\_64.rpm

            sudo yum localinstallgrafana-5.3.4-1.x86\_64.rpm

    2.  Run the following command to start the Grafana service:

        service grafana-server start

    3.  Optional. Install the Grafana panel plug-ins.

        To install a Grafana panel \(for example, a pie chart panel\), run the following command:

        grafana-cli plugins install grafana-piechart-panel

        **Note:** For more information about how to install other Grafana panel plug-ins, see [Plugins](https://grafana.com/grafana/plugins?orderBy=weight&direction=asc&type=panel).

2.  Install the Cloud Monitor data source plug-in.

    1.  Find the plug-in directory of Grafana.

        For example, the plug-in directory is /var/lib/grafana/plugins/ in CentOS Linux.

    2.  Run the following commands to install the Cloud Monitor data source plug-in:

        cd /var/lib/grafana/plugins/

        git clone https://github.com/aliyun/aliyun-cms-grafana.git

    3.  Run the following command to restart the Grafana service:

        service grafana-server restart

    You can also download the aliyun-cms-grafana.zip package, decompress the package, and upload the plug-in to the /var/lib/grafana/plugins/ directory. Then, restart the Grafana service.

    **Note:** The Cloud Monitor data source plug-in does not support the alert feature for metrics.

3.  Configure the Cloud Monitor data source plug-in.

    Log on to Grafana after it is installed. The default port is 3000 and the default username is admin.

    **Note:** To prevent security risks, we recommend that you change the password the first time you log on to Grafana.

    1.  Log on to Grafana.

    2.  On the Grafana homepage, choose **Configuration** \> **Data Sources** in the upper-left corner.

    3.  On the Data Sources page, click **Add data source** in the upper-right corner.

    4.  Set the parameters for the Cloud Monitor data source.

        |Parameter|Description|
        |---------|-----------|
        |**Name**|The name of the data source. You can specify the name based on your business requirements.|
        |**type**|The type of the data source. Select **CMS Grafana Service** as **Type**.|
        |**HTTP**|The URL of the data source. Example: `http://metrics.cn-shanghai.aliyuncs.com`. For more information about the endpoints for different regions, see [Request method](/intl.en-US/API Reference/Request method.md).|
        |**Access**|The method used to access the data source. Use the default setting.|
        |**Auth**|The authentication method. Use the default setting.|
        |**cloudmonitor service details**|The AccessKey ID and AccessKey secret of the account that has read permissions on Cloud Monitor. We recommend that you use the AccessKey pair of a Resource Access Management \(RAM\) user.|

        The following figure shows the parameter settings of the Cloud Monitor data source plug-in.

        ![Configure the data source plug-in on Grafana](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2790287951/p73947.png)

    5.  Click **Save & Test**.

4.  Create and configure a dashboard.

    1.  On the Grafana homepage, click **Dashboards** in the upper-left corner. On the Dashboards page, click the **Manage** tab.

        ![Manage](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2790287951/p39940.png)

    2.  Click **Dashboard** to create a dashboard.

        You can click **Folder** to create a folder and then create a dashboard. You can also click **Import** to import a dashboard.

    3.  Configure a graph.

        1.  Choose **New Panel** \> **Add** \> **Graph**.
        2.  Click **Panel Title**. In the dialog box that appears, click **Edit**.
        3.  On the **Metrics** tab, select **cms-grafana** from the **datasource** drop-down list. Set the Project, Metric, Period, Dimensions, Y - column, and X - column parameters.

            For more information about how to set the Project, Metric, and Period parameters, see [QueryMetricList](/intl.en-US/API Reference/Monitoring data on time series metrics of cloud services/DescribeMetricList.md). The following table describes the parameters of a graph.

            |Parameter|Description|
            |---------|-----------|
            |**Group**|The ID of the application group that is created in Cloud Monitor within your Alibaba Cloud account.|
            |**Dimensions**|The instances from which the latest monitoring data of the metrics is collected for the specified project. If you set this parameter to Group, monitoring data is collected from all instances in the specified application group.|
            |**Y-column**|The data to display in the Y-axis. You can select more than one option.|
            |**X-column**|The data to display in the X-axis. Set the value to timestamp.|
            |**Y-column describe**|The description of each option selected for the Y - column parameter.|

            **Note:**

            -   For more information about the graph, see [Graph panel](https://grafana.com/docs/grafana/latest/features/panels/graph/).
            -   You can follow the instructions in [QueryMetricList](/intl.en-US/API Reference/Monitoring data on time series metrics of cloud services/DescribeMetricList.md) to specify all the parameters.
            -   You can enter null to invalidate a parameter.
            -   If the value of the Dimensions parameter is incomplete, refresh the page or specify the instance IDs in the required format.
            ![Metrics](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2790287951/p73950.png)

            For custom monitoring data, you must manually set the parameters that are described in the following table.

            |Parameter|Description|
            |---------|-----------|
            |**Project**|The name of the project. Format: acs\_customMetric\_ID of your Alibaba Cloud account.|
            |**Metric**|The name of the custom metric.|
            |**Period**|The time period during which the monitoring data of the custom metric is reported.|
            |**Group**|The ID of the application group to which the custom metric belongs.|
            |**Dimensions**|The dimension of the custom monitoring data. You must enter a value. Only one dimension is supported. If you enter multiple dimensions, only the first one is valid. **Note:** If the dimensions in the Cloud Monitor console are in the format of `env: public, step: 5-ReadFromAlertOnline`, you must replace the commas \(`,`\) with ampersands \(`&`\). |
            |**Y-column**|The data to display in the Y-axis. You can select multiple options to aggregate the monitoring data, including Average, Maximum, Minimum, Sum, SampleCount, P10, P20, and P99.|
            |**X-column**|The data to display in the X-axis. Set the value to timestamp.|

            ![Custom monitoring](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3790287951/p39967.png)

        4.  Configure a Singlestat panel.
            1.  Choose **New Panel** \> **Add** \> **Singlestat**.
            2.  On the page that appears, click **Panel Title**. In the dialog box that appears, click **Edit**.
            3.  On the **Metrics** tab, set relevant parameters.

                **Note:** For more information about [Singlestat](http://docs.grafana.org/features/panels/singlestat/), see [Graph panel](http://docs.grafana.org/features/panels/graph/).

                ![Configure the Singlestat panel](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3790287951/p39968.png)

    4.  Configure variables.

        You can create **query** variables and **custom** variables.****

        -   Create a **query** variable.****

            Query variables support the following functions.

            |Parameter|Definition|Description|Example|
            |---------|----------|-----------|-------|
            |`$namespace`|`namespace(filter)`|Filters the metrics of cloud services by the specified filter conditions. The filter field can be set to null. For more information about the metrics of Alibaba Cloud services, see [Overview](/intl.en-US/Appendix 1: Metrics/Overview.md).|`namespace(ecs)`|
            |`$metric`|`metric($namespace,filter)`|Filters the metrics of cloud services by the specified namespace and filter conditions. The namespace field can be a variable and must be specified. The filter field can be set to null. For more information about the metrics of Alibaba Cloud services, see [Overview](/intl.en-US/Appendix 1: Metrics/Overview.md).|`metric($namespace,disk)`, `metric($namespace,null)`, and `metric(acs_ecs_dashboard,disk)`|
            |`$tagsFilter`|`tagsFilter(type, regionId, tagType, tagKey)`|Queries the `keys` and `values` of the tags attached to ApsaraDB RDS instances or Elastic Compute Service \(ECS\) instances within the account. For more information, see [ListTagResources](/intl.en-US/API Reference/Tags/ListTagResources.md) and [Query tags](/intl.en-US/API Reference/Tag management/Query tags.md). `type`: the type of the service. Set the value to ECS or RDS. `tagType`: the key or value of the tag. Set the value to key or value.

**Note:** The RAM user must be authorized to access ECS and ApsaraDB RDS.

|            -   Sample definition used to query the keys of the tags attached to ApsaraDB RDS instances in the China \(Beijing\) region within the account: `tagFilter(RDS, cn-beijing, key, null)`
            -   Sample definition used to query the values of the tags attached to ApsaraDB RDS instances in the China \(Beijing\) region within the account:`` `tagFilter(RDS, cn-beijing, value, null)` |
            |`$tags`|`tags(type, regionId, resourceType, resourceId_array, tag_array)`|Queries the IDs of the ApsaraDB RDS instances or ECS instances that are attached the specified tags within the account. For more information, see [ListTagResources](/intl.en-US/API Reference/Tags/ListTagResources.md) and [Query tags](/intl.en-US/API Reference/Tag management/Query tags.md).             -   `type`: the type of the service. Set the value to ECS or RDS.
            -   `resourceType`: the type of the resources. Set the value to instance if the type field is set to ECS. Set the value to INSTANCE if the type field is set to RDS.
            -   resourceId\_array: the IDs of the instances to be filtered. Format: ResourceId.N.

Example: `[instanceId_1,instanceId_2,instanceId_3]`.

            -   tag\_array: the keys or key-value pairs of the tags that are used to filter instances. Format: `keyN:/:valueN` or `keyN`.````

Example: `[key1:/:value1,key2:/:value2,key3:/:value3]` or \[key1,key2,key3\].

**Note:** The account must be authorized to access ECS and ApsaraDB RDS.

|Sample definition used to query the IDs of the ApsaraDB RDS instances that are attached the specified tags in the China \(Beijing\) region within the account: `tag(RDS,cn-beijing, INSTANCE, [instanceId_1,instanceId_2], [key1:/:value1,key2:/:value2])`|
            |`$dimension`|`dimension($namespace,metric,filterFirst,filterSecond)`|Queries the dimensions within the account. filterFirst\[g99hxhnnyr;1egdhoza;kty4zk40hh\] or /dev/vda1

filterSecond \[g99hxhnnyr;1egdhoza;kty4zk40hh\] or /dev/vda1

|            -   `dimension(acs_ecs_dashboard,diskusage_used,i-2zed,/dev/vd),`
            -   `dimension($namespace,$metric,[i-2zed;i-2zeg;i-2zeb],/dev/vda1),`
            -   `dimension($namespace,$metric,i-2zed;i-2zeg;i-2zeb,/dev/vda1),`
            -   `dimension($namespace,$metric,/dev/vda1,[i-2zed;i-2zeg;i-2zeb]),`
            -   `dimension($namespace,$metric,/dev/vda1,null)` |

            In the left-side navigation pane of the **Dashboard settings** page, click **Variables**. On the Variables page, click New to create a variable and set the parameters.

            ![Variables](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3790287951/p73977.png)

            You can edit the query tags of a variable in the **Value groups/tags \(Experimental feature\)** section. The following figure shows an example.

            ![Value Groups](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3790287951/p73980.png)

            After the required variables are created, specify the variables as the parameter values in the corresponding panel. The variables must be in the format of `$Variable name`, as shown in the following figure.

            ![Panel](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3790287951/p73982.png)

            **Note:** For more information, see the README file in the plug-in. You can view and use the sample code for this example in the `json(ecs,rds)` file of the src directory.

        -   Create a **custom** variable.****

            On the created dashboard, click the **Dashboard settings** icon at the top of the page. In the left-side navigation pane, click **Variables**. On the Variables page, click New to create a variable and set the parameters. The following figure shows how to create a custom variable.

            ![Variables](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3790287951/p73983.png)

            After the required variables are created, specify the variables as the values of the parameters in the corresponding panel. The variables must be in the format of `$Variable name`, as shown in the following figure.

            ![panel](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3790287951/p73984.png)

            **Note:** You can specify custom variables as the values of the Project, Metric, Period, Group, Dimensions, and Y - column parameters. We recommend that you set the names of the variables to project, metric, period, group, dimensions, and ycol.

5.  View the monitoring data.

    After the preceding steps are performed, you can view the monitoring data in the dashboard.

    ![Dashboard](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/3790287951/p39971.png)

    ![Dashboard](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/4790287951/p39973.png)


