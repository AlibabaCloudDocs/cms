# Java SDK使用手册

本文为您介绍云监控Java SDK的相关信息。

## SDK安装

通过maven进行安装，需要添加的依赖如下：

```
<dependencies>
     <dependency>
       <groupId>com.aliyun</groupId>
       <artifactId>aliyun-java-sdk-core</artifactId>
       <version>3.2.6</version>
    </dependency>
<dependency>
  <groupId>com.aliyun</groupId>
  <artifactId>aliyun-java-sdk-cms</artifactId>
  <version>7.0.3</version>
</dependency>
</dependencies>
```

## SDK下载

Github下载地址：[aliyun-java-sdk-cms](https://github.com/aliyun/aliyun-openapi-java-sdk/tree/master/aliyun-java-sdk-cms)。

## 测试代码

-   查询监控数据
    -   请求示例

        使用时请将如下示例中的`accessKey`和`accessSecret`分别替换成您的AccessKey ID和AccessKey Secret。

        ```
        import com.aliyuncs.DefaultAcsClient;
        import com.aliyuncs.IAcsClient;
        import com.aliyuncs.exceptions.ClientException;
        import com.aliyuncs.exceptions.ServerException;
        import com.aliyuncs.profile.DefaultProfile;
        import com.google.gson.Gson;
        import java.util.*;
        import com.aliyuncs.cms.model.v20190101.*;
        
        public class DescribeMetricListDemo {
        
            public static void main(String[] args) {
                DefaultProfile profile = DefaultProfile.getProfile("cn-beijing", "<accessKeyId>", "<accessSecret>");
                IAcsClient client = new DefaultAcsClient(profile);
        
                DescribeMetricListRequest request = new DescribeMetricListRequest();
                request.setDimensions("{"instanceId":<instanceId_as_example>}");
                request.setEndTime("2019-05-13 11:06:27");
                request.setStartTime("2019-05-13 10:20:27");
                request.setPeriod("60");
                request.setNamespace("acs_ecs_dashboard");
                request.setMetricName("cpu_total");
        
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

    -   返回示例

        ```
        Code:200
        Message:null
        RequestId:727B48BD-55E3-4E5D-BEF4-1D092055F7A4
        Datapoints:[
            {
                "Maximum":100,
                "Minimum":25,
                "instanceId":"i-bp18abl200xk9599****",
                "Average":94.62,
                "userId":"127067667954****",
                "timestamp":1489472460000
            },
            {
                "Maximum":100,
                "Minimum":25,
                "instanceId":"i-bp18abl200xk9599****",
                "Average":95.11,
                "userId":"127067667954****",
                "timestamp":1489472520000
            },
            {
                "Maximum":100,
                "Minimum":25,
                "instanceId":"i-bp18abl200xk9599****",
                "Average":95.16,
                "userId":"127067667954****",
                "timestamp":1489472580000
            },
            {
                "Maximum":100,
                "Minimum":25,
                "instanceId":"i-bp18abl200xk9599****",
                "Average":94.69,
                "userId":"127067667954****",
                "timestamp":1489472640000
            },
            {
                "Maximum":100,
                "Minimum":20,
                "instanceId":"i-bp18abl200xk9599****",
                "Average":95.82,
                "userId":"127067667954****",
                "timestamp":1489472700000
            },
            {
                "Maximum":100,
                "Minimum":25,
                "instanceId":"i-bp18abl200xk9599****",
                "Average":94.77,
                "userId":"127067667954****",
                "timestamp":1489472760000
            },
            {
                "Maximum":100,
                "Minimum":33.33,
                "instanceId":"i-bp18abl200xk9599****",
                "Average":95.18,
                "userId":"127067667954****",
                "timestamp":1489472820000
            },
            {
                "Maximum":100,
                "Minimum":25,
                "instanceId":"i-bp18abl200xk9599****",
                "Average":95.11,
                "userId":"127067667954****",
                "timestamp":1489472880000
            },
            {
                "Maximum":100,
                "Minimum":20,
                "instanceId":"i-bp18abl200xk9599****",
                "Average":94.5,
                "userId":"127067667954****",
                "timestamp":1489472940000
            },
            {
                "Maximum":100,
                "Minimum":20,
                "instanceId":"i-bp18abl200xk9599****",
                "Average":94.99,
                "userId":"127067667954****",
                "timestamp":1489473000000
            }
        ]
        }
        ```

-   创建报警规则
    -   请求示例

        ```
        import com.aliyuncs.DefaultAcsClient;
        import com.aliyuncs.IAcsClient;
        import com.aliyuncs.exceptions.ClientException;
        import com.aliyuncs.exceptions.ServerException;
        import com.aliyuncs.profile.DefaultProfile;
        import com.google.gson.Gson;
        import java.util.*;
        import com.aliyuncs.cms.model.v20190101.*;
        
        public class CmsDemo {
        
            public static void main(String[] args) {
                DefaultProfile profile = DefaultProfile.getProfile("cn-hangzhou", "<accessKeyId>", "<accessSecret>");
                IAcsClient client = new DefaultAcsClient(profile);
        
                PutResourceMetricRuleRequest request = new PutResourceMetricRuleRequest();
                request.setNamespace("acs_ecs_dashboard");
                request.setRuleId("aabbcccdddxxx001");
                request.setInterval("60");
                request.setPeriod("60");
                request.setRuleName("aaabbbcc");
                request.setContactGroups("测试报警联系人");
                request.setResources("[{"instanceId":"i-8vb6p16*******"}]");
                request.setMetricName("cpu_total");
        
                List<PutResourceMetricRuleRequest.Escalations> escalationsList = new ArrayList<PutResourceMetricRuleRequest.Escalations>();
        
                PutResourceMetricRuleRequest.Escalations escalations1 = new PutResourceMetricRuleRequest.Escalations();
                escalations1.setStatistics("Average");
                escalations1.setComparisonOperator("GreaterThanOrEqualToThreshold");
                escalations1.setThreshold("90");
                escalations1.setTimes(2);
                escalationsList.add(escalations1);
                request.setEscalationss(escalationsList);
        
                try {
                    PutResourceMetricRuleResponse response = client.getAcsResponse(request);
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

    -   返回示例

        ```
        {
            "Message": "",
            "RequestId": "7aa25dfa-3bb9-4ed3-9704-a2d41bf67649",
            "Success": true,
            "Code": 200
        }
        ```


