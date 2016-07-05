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

```

```
[standalone@192.168.102.88:9999 /] /subsystem=datasources/data-source=MysqlDS/statistics=pool:read-resource(include-runtime=true)
{
    "outcome" => "success",
    "result" => {
        "ActiveCount" => "20",                  #현재 사용 중인 연결 개수
       ＂AvailableCount＂ => ＂20＂,            #사용 가능한 연결 개수
        "AverageBlockingTime" => "0",           #연결을 위해서 대기했던 평균 시간(ms)
        "AverageCreationTime" => "7",           #데이터베이스와 연결에 걸린 평균 시간(ms)
        ＂CreatedCount＂ => ＂20＂,             #지금까지 만들어진 연결 개수
        "DestroyedCount" => "0",                #지금까지 소멸된 연결 개수
        "InUseCount" => "0",                    #현재 사용중인 연결 개수
        "MaxCreationTime" => "20",              #데이터베이스 연결에 걸린 최대 시간(ms) 
        "MaxUsedCount" => "1",                  #지금까지 동시에 사용된 최대 연결 수 
        "MaxWaitCount" => "0",                  #연결을 얻기 위해 대기한 스레드의 최댓값 
        ＂MaxWaitTime＂ => ＂0＂,               #연결을 얻기 위해 대기한 대기 시간의 최댓값
        "TimedOut" => "0",                      #접속을 얻기 위해 기다리다 타임아웃된 스레드의 개수  
        "TotalBlockingTime" => "0",             #연결을 위해 블록킹했던 시간의 총합
        "TotalCreationTime" => "147",           #연결을 생성하기 위해 걸린 시간의 총합
        "statistics-enabled" => true
    }
}
```















```

```
