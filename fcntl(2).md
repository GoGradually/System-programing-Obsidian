[[파일 디스크립터]]를 제어하기 위한 함수(fd control)


~~~c
#include <unistd.h>
#include <fcntl.h>

int fcntl(int fd, int cmd, .../*arg*/);
~~~

fd = 파일 기술자
cmd = 명령
arg = cmd에 따라 필요 시 지정하는 인자들

주요 명령으로는 
- F_GETFL : 상태 플래그 정보를 읽어온다
- F_SETFL : 상태 플래그 정보를 새로 설정한다. 설정할 수 있는것은 대부분 [[open(2)]]함수에서 
  지정하는 플래그다.
가 존재한다.