[[파일 디스크립터]]를 제어하기 위한 함수(fd control)


~~~c
#include <unistd.h>
#include <fcntl.h>

int fcntl(int fd, int cmd, .../*arg*/);
~~~

주요 기능으로는 
- F_GETFL : 상태 플래그 정보를 읽어온다
- F_SETFL : 상태 플래그 정보를 새로 설정한다. 설정할 수 있는것은 대부분 [[open(2)]]함수에서 
  지정하는 플래그다.