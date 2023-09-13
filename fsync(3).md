메모리에 위치하고 있는 파일의 내용을 디스크로 보내 메모리와 디스크의 내용을 동기화하는 함수.

~~~c
#include <unistd.h>
int fsync(int fd);
~~~
