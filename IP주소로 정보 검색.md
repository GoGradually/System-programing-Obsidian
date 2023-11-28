### gethostbyaddr(3)
```c
#include <netdb.h>
#include <sys/socket.h>

struct hostent *gethostbyaddr(const void *addr, socklen_t len, int type);
```
addr 주소를 인자로 받아 DB에서 해당 항목을 검색해 hostent 구조체에 저장하고 그 주소를 리턴.
- addr : 검색하려는 IP 주소
- len : addr 길이
- type : IP주소 형식


type의 주소 형식 (대표적 3개만)
- AF_UNIX  : 호스트 내부 통신
- AF_INET  : IPv4 인터넷 프로토콜
- AF_INET6  : IPv6 인터넷 프로토콜