[[dup(2)]]와 달리
새로 할당할 [[파일 디스크립터]]를 직접 정할 수 있게 해준다.
~~~c
#include <unistd.h>
int dup2(int oldfd, int newfd);
~~~