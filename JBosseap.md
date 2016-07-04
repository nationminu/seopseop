# seopseop
12. Monitoring

보통 WAS의 경우 APM Tool 을 이용하거나 자체적으로 제공하는 기능을 통하여 모니터링 할 수 있다.  JBossEAP6 는 JBoss console 이나 CLI 를 통하여 JBoss 의 상태를 모니터링 할 수 있으며,  주요 모니터링 항목은 다음과 같다
 - Thread 
 - DataSource
 - Memory 


 - Labs12_01 : Thread Monitoring
 - Labs12_02 : DataSource Monitoring
 - Labs12_03 : Memory Monitoring




CLI를 이용한 모니터링

```
/core-service=platform-mbean/type=memory:read-attribute(name=heap-memory-usage)
```
