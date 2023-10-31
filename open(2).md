~~~c
#include <sys/types.h>
#include <sys/stat.h>
#iinclude <fcntl.h>

int open(const char *pathname, int flags);
int open(const char *pathname, int flags, mode_t mode);
~~~

pathname 경로 내에 있는 파일을  flag 모드로 연다.
만약 flag 가 O_CREAT모드라면 뒤 mode 변수를 받고, 그 mode 대로 권한을 지정하여 파일을 만들게 된다.

파일을 열 때의 flag 의 대표적인 예시
* O_RDONLY        -> 파일을 읽기 전용으로 연다.
* O_WRONLY       -> 파일을 쓰기 전용으로 연다.
* O_RDWR           -> 파일을 읽기/쓰기용으로 연다.
* O_CREAT           ->파일이 없으면 생성한다. 파일을 생성할 권한은 당연히 있어야 한다.
* O_EXCL              -> CREAT와 같이 사용할 경우 이미 파일이 있다면 오류를 출력한다.
* O_APPEND        -> 옵션 지정 시 파일의 맨 끝에 내용을 추가하는 방식으로 입력한다.
* O_TRUNC           -> 파일을 생성할 때 이미 있는 파일이고 쓰기 옵션으로 열었으면
                                   내용을 모두 지우고 파일 길이를 0으로 변경한다.
* O_SYNC/O_DSYNC        -> 스토리지에 기록을 마쳐야 쓰기 동작을 완료한다.


### 같이보기
- [[fopen(3)]]