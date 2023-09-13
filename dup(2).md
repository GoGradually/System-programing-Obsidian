같은 파일을 가리키는 n번째 [[파일 디스크립터]]를 만들기 위한 함수.
입출력 방향 전환에 많이 사용된다.

~~~c
#include <unistd.h>
int dup(int oldfd);
~~~
