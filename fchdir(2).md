~~~c
#include <unistd.h>
int fchdir(int fd);
~~~
[[파일 디스크립터]]를 이용한 디렉터리 이동.
성공하면 0, 실패하면 -1 반환.