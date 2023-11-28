### sendto(2)
```c
#include <sys/types.h>
#include <sys/socket.h>
ssize_t sendto(int sockfd, const void *buf, size_t len, int flags, const struct sockaddr *dest_addr, socklen_t addrlen);
```

[[클라이언트가 서버에 접속 요청]] 하지 않은 데이터를 보낼 때 (SOCK_DGRAM)
일방적으로 데이터를 보내기 위해(UDP) 사용하는 함수.

send() 함수와 달리 매번 목적지 주소를 지정해야 한다.
실제로 전송한 데이터의 바이트 수 리턴.