### inet_addr(3)
```c
#include <sys/socket.h>
#include <netinet/in.h>
#include <arpa/inet.h>

in_addr_t inet_addr(const char *cp);
```
문자열로 된 IP 주소를 받아 이진값으로 바꿔서 리턴한다.
in_addr_t 는 long 형이다.