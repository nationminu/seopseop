# seopseop
12. Monitoring

보통 WAS의 모니터링 경우 APM Tool 을 이용하거나 자체적으로 제공하는 기능을 통하여 모니터링.  
JBossEAP6 는 JBoss console 이나 CLI 를 통하여 JBoss 의 상태를 모니터링 할 수 있으며,  주요 모니터링 항목은 다음과 같다.

 - Thread 
 - DataSource
 - Memory 
```
/subsystem=web/connector=http:read-resource(recursive=true, include-runtime=true)
```
```
/core-service=platform-mbean/type=memory:read-attribute(name=heap-memory-usage)
```
