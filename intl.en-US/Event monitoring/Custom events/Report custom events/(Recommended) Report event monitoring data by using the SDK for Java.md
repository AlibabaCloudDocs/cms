# \(Recommended\) Report event monitoring data by using the SDK for Java

This topic describes how to report monitoring data for custom events by using the SDK for Java.

## Install the SDK for Java

You can install the SDK for Java by adding the following Maven dependency:

```
<dependency>
            <groupId>com.aliyun.openservices</groupId>
            <artifactId>aliyun-cms</artifactId>
            <version>0.2.4</version>
</dependency>
```

## Sample code

The following sample code shows how to report event monitoring data by using the SDK for Java:

```
public void uploadEvent() throws CMSException, InterruptedException {
        // Initialize the client.
        CMSClient cmsClient = new CMSClient(endpoint, accKey, secret);
       // Construct two events to be reported.
         CustomEventUploadRequest request = CustomEventUploadRequest.builder()
                    .append(CustomEvent.builder()
                            .setContent("abc,123")
                            .setGroupId(101l)
                            .setName("Event001").build())
                    .append(CustomEvent.builder()
                            .setContent("abc,123")
                            .setGroupId(101l)
                            .setName("Event002").build())
                    .build();
            CustomEventUploadResponse response = cmsClient.putCustomEvent(request);
            List<CustomEvent> eventList = new ArrayList<CustomEvent>();
            eventList.add(CustomEvent.builder()
                    .setContent("abcd,1234")
                    .setGroupId(101l)
                    .setName("Event001").build());
            eventList.add(CustomEvent.builder()
                    .setContent("abcd,1234")
                    .setGroupId(101l)
                    .setName("Event002").build());
            request = CustomEventUploadRequest.builder()
                    .setEventList(eventList).build();
            response = cmsClient.putCustomEvent(request);
    }
```

**Note:** An endpoint is the access address of a cloud service. The endpoints of Cloud Monitor are in the format of `metrics.aliyuncs.com`. For more information about the endpoints of Cloud Monitor in different regions, see [Endpoint](/intl.en-US/Custom monitoring/Report monitoring data/Report monitoring data by sending an HTTP request.md).

## Sample response

The following code shows the sample response that is returned when you report event monitoring data by using the SDK for Java:

```
{
    "Message": "success",
    "RequestId": "E25EE651-9C97-4EFD-AF22-A753B674E8D4",
    "Code": "200"
}
```

The HTTP status code 200 indicates a success.

