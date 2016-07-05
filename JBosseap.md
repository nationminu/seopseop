# 11. Monitoring 


보통 WAS의 모니터링 경우 APM Tool 을 이용하거나 자체적으로 제공하는 기능을 통하여 모니터링.  
JBossEAP6 는 JBoss console 이나 CLI 를 통하여 JBoss 의 상태를 모니터링 할 수 있으며,  주요 모니터링 항목은 다음과 같다.

 - Thread 
 - DataSource
 - Memory 


##Labs11_01 Thread Monitoring

### CLI
```
/subsystem=web/connector=ajp:read-resource(recursive=true, include-runtime=true)
{
    "outcome" => "success",
    "result" => {
        "bytesReceived" => "0",          #커넥터가 수신한 바이트 수 
        "bytesSent" => "0",              #커넥터가 전송한 바이트 수 
        "enable-lookups" => false,       #서블릿 API에서 DNS를 조회하는지 정보
        "enabled" => true,               #커넥터를 사용할 것인지 지정
        "errorCount" => "0",             #커넥터에서 요청 처리 시 발생한 에러의 개수
        "executor" => undefined,
        "max-connections" => undefined,  #최대 동시 접속 연결 수
        "max-post-size" => 2097152,      #컨테이너가 처리 가능한 POST의 최대 크기(byte)
        "max-save-post-size" => 4096,
        "maxTime" => "0",                #요청처리에 걸린 최대 시간
        "name" => "ajp",
        "processingTime" => "0",         #커넥터의 처리 시간(ms)
        "protocol" => "AJP/1.3",         
        "proxy-binding" => undefined,    
        "proxy-name" => undefined,
        "proxy-port" => undefined,
        "redirect-binding" => undefined,
        "redirect-port" => 443,
        "requestCount" => "0",           #커넥터가 처리한 요청 개수
        "scheme" => "http",
        "secure" => false,
        "socket-binding" => "ajp",
        "virtual-server" => undefined,
        "configuration" => undefined
    }
}

### CONSOLE
!쓰레드.png
