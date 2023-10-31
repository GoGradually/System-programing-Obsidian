~~~c
#include <unistd.h>
ssize_t write(int fd, const void *buf, size_t count);
~~~
buf에 기록할 내용을 받아 count만큼 [[파일 디스크립터]]가 가리키는 파일에 기록한다.

성공하면 기록한 바이트 수를 리턴하고,
오류가 발생하면 -1을 리턴한다.


같이보기
[[fwrite(3)]]