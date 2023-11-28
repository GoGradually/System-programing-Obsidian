### bind(2)
```c
#include <sys/types.h>
#include <sys/socket.h>

int bind(int sockfd, const struct sockaddr *addr, socklen_t addrlen);
```
- sockfd : 소켓 기술자
- addr : 소켓의 이름 표현하는 구조체
- addrlen : addr 의 크기

소켓을 특정 IP 및 포트번호와 연결하기.
sockaddr 구조체에는 소켓의 종류, IP주소, 포트번호가 담겨있음.


성공하면 0, 실패하면 -1 반환.