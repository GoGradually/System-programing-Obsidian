### recvfrom(2)
```c
#include <sys/types.h>
#include <sys/socket.h>
ssize_t recvfrom(int sockfd, const void *buf, size_t len, int flags, const struct sockaddr *src_addr, socklen_t *addrlen);
```

[[데이터 송신(SOCK_DGRAM)]]으로 전달된 데이터를 수신하는데 사용하는 함수.
메시지를 발신한 시스템의 주소를 저장받을 수 있다(Call-by-reference)

