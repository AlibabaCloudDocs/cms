# Cloud Monitor SDK for PHP

This topic describes how to install and use Cloud Monitor SDK for PHP.

## Download and install Cloud Monitor SDK for PHP

For more information, see [Quick start]().

## Sample code

```
<? php
use AlibabaCloud\Client\AlibabaCloud;
use AlibabaCloud\Client\Exception\ClientException;
use AlibabaCloud\Client\Exception\ServerException;

// Download URL: https://github.com/aliyun/openapi-sdk-php
// Usage guide: https://github.com/aliyun/openapi-sdk-php/blob/master/README.md

AlibabaCloud::accessKeyClient('<accessKeyId>', '<accessSecret>')
                        ->regionId('cn-beijing')
                        ->asDefaultClient();

try {
    $result = AlibabaCloud::rpc()
                          ->product('Cms')
                          // ->scheme('https') // https | http
                          ->version('2019-01-01')
                          ->action('DescribeMetricList')
                          ->method('POST')
                          ->options([
                                        'query' => [
                                          'RegionId' => 'cn-beijing',
                                          'MetricName' => 'cpu_idle',
                                          'Namespace' => 'acs_ecs_dashboard',
                                          'Period' => '60',
                                          'StartTime' => '2019-05-13 10:20:27',
                                          'EndTime' => '2019-05-13 11:06:27',
                                          'Dimensions' => '{\"instanceId\":<instanceId_as_example>}',
                                        ],
                                    ])
                          ->request();
    print_r($result->toArray());
} catch (ClientException $e) {
    echo $e->getErrorMessage() . PHP_EOL;
} catch (ServerException $e) {
    echo $e->getErrorMessage() . PHP_EOL;
}
```

