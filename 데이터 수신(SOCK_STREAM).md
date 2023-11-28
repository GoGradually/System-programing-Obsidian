### recv(2)
```c
#include <sys/types.h>
#include <sys/socket.h>
ssize_t recv(int sockfd, void *buf, size_t len, int flags)
```
flags 는 [[데이터 송신(SOCK_STREAM)]]에 사용하는 flags 와 같다.

소켓 sockfd 를 통해 전송받은 메시지를 크기가 len 인 버퍼 buf에 저장한다.

성공하면 받은 데이터의 크기, 실패하면 -1 반환.