~~~c
#include <stdio.h>
int remove(const char *pathname);
~~~
[[rmdir(2)]] 과 [[unlink(2)]] 의 기능을 합쳐둔 함수.
성공하면 0, 실패하면 -1을 반환한다.