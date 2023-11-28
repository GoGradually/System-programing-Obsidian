### inet_ntoa(3)
```c
#include <sys/socket.h>
#include <netinet/in.h>
#include <arpa/inet.h>

char *inet_ntoa(const struct in_addr in);
```
IP주소를 in_addr 구조체 형태로 받아 점으로 구분된 문자열로 리턴.