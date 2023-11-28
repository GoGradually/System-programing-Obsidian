### send(2)
```c
#include <sys/types.h>
#include <sys/socket.h>
ssize_t send(int sockfd, const void *buf, size_t len, int flags);
```
- sockfd
- buf : 전송할 메시지를 지정한 메모리 주소
- len : 메시지의 크기
- flags : 메시지를 주고 받는 방법을 지정한 플래그.

sockfd를 통해 크기가 len인 메시지 buf를 flags에 지정한 방법으로 전송한다.

flag 에는 다음 값이 들어간다.
- 0 : 일반적인 전송
- MSG_OOB : Out-of-Band data. UDP 처럼 보내고 수신여부를 확인하지 않는다.
- MSG_DONTROUTE : 데이터의 라우팅 설정을 해제한다. 진단 프로그램이나 라우팅 프로그램에서 사용함.

성공하면 보낸 데이터의 크기, 실패하면 -1 반환.