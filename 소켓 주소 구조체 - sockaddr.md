상대방의 주소 저장하는 구조체
### 유닉스 도메인 소켓의 주소 구조체
```c
struct sockaddr_un{
	__kernel_sa_family_t sun_family;          /* AF_UNIX 지정*/
	char sun_path[UNIX_PATH_MAX];             /*경로명 지정*/
}
```

### 인터넷 소켓의 주소 구조체
```c
struct sockaddr_in{
	__kernel_sa_family_t sin_family;   //주소 패밀리명
	__be16 sin_port;             //포트 번호
	struct in_addr sin_addr;     //인터넷 주소
};
```

### IPv4 주소 구조체
```c
#include <netinet/in.h>

struct sockaddr_in {
    short sin_family;        //주소 패밀리명 (AF_INET)
    unsigned short sin_port; //포트 번호
    struct in_addr sin_addr; //인터넷 주소
    char sin_zero[8];        // Padding to make the structure the same size as sockaddr
};

struct in_addr {
	__be32 s_addr;        /*32비트 주소*/
}
```

### IPv6 주소 구조체
```c
#include <netinet/in.h>

struct sockaddr_in6 {
    uint16_t sin6_family;     //주소 패밀리명 (AF_INET6)
    uint16_t sin6_port;       //포트 번호 (in network byte order)
    uint32_t sin6_flowinfo;   // IPv6 flow information
    struct in6_addr sin6_addr;// IPv6 주소
    uint32_t sin6_scope_id;   // Set of interfaces for a scope
};

```