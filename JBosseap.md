# seopseop
12. Monitoring

보통 WAS의 모니터링 경우 APM Tool 을 이용하거나 자체적으로 제공하는 기능을 통하여 모니터링.  
JBossEAP6 는 JBoss console 이나 CLI 를 통하여 JBoss 의 상태를 모니터링 할 수 있으며,  주요 모니터링 항목은 다음과 같다.

 - Thread 
 - DataSource
 - Memory 
 - 

Labs12_01 Thread Monitoring

```
/subsystem=web/connector=http:read-resource(recursive=true, include-runtime=true)
{
    "outcome" => "success",
    "result" => {
        "bytesReceived" => "0",
        "bytesSent" => "0",
        "enable-lookups" => false,
        "enabled" => true,
        "errorCount" => "0",
        "executor" => undefined,
        "max-connections" => undefined,
        "max-post-size" => 2097152,
        "max-save-post-size" => 4096,
        "maxTime" => "0",
        "name" => "http",
        "processingTime" => "0",
        "protocol" => "HTTP/1.1",
        "proxy-binding" => undefined,
        "proxy-name" => undefined,
        "proxy-port" => undefined,
        "redirect-binding" => undefined,
        "redirect-port" => 443,
        "requestCount" => "0",
        "scheme" => "http",
        "secure" => false,
        "socket-binding" => "http",
        "virtual-server" => undefined,
        "configuration" => undefined
    }
}

```
















```
/core-service=platform-mbean/type=memory:read-attribute(name=heap-memory-usage)
```
