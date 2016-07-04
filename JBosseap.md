# seopseop
12. Monitoring
1)서버 모니터링
JBossEAP6 의 서버 기본 정보는 platform-mbean 코에 서비스(core-service=platform-mbean)에서 얻을 수 있으며, 다음과 같은 정보를 모니터링 한다.

* OS 정보
* 메모리 정보
* Thread 정보
* 런타임 정보


CLI를 이용한 모니터링

...
/core-service=platform-mbean/type=memory:read-attribute(name=heap-memory-usage)
...
