- [[hostent 구조체]]
### gethostent(3)
```c
#include <netdb.h>
struct hostent *gethostent(void);
```
호스트명과 IP 주소 읽어서 hostent 구조체에 저장
### sethostent(3)
```c
#include <netdb.h>
void sethostent(int stayopen);
```
데이터베이스의 현재 읽기 위치를 시작부분으로 재설정
stayopen != 0 이면 데이터베이스 열린채로 둠

### endhostent(3)
```c
#include <netdb.h>
void endhostent(void);
```
데이터베이스 닫기

컴파일 안되면
-> 네트워크 라이브러리 지정(-lnsl)