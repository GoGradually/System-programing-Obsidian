~~~c
#include <sys/types.h>
#include <unistd.h>

off_t lseek(int fd, off_t offset, int whence);
~~~

[[파일 디스크립터]]가 가리키는 파일의 오프셋 위치를
지정한 위치로 바꾼다.

위치를 지정하는 방법은
whence를
SEEK_SET     -> 파일의 시작 위치 기준
SEEK_CUR    -> 오프셋의 현재 위치 기준
SEEK_END    -> 파일의 끝 위치 기준

으로 offset만큼 이동시키는 방법으로 다룬다.

성공 시 반환 뒤 현재 오프셋의 위치,
실패 시 -1을 리턴한다.

- 오프셋의 현재 위치를 알고 싶다면
~~~c
now = lseek(fd, 0, SEEK_CUR);
~~~
을 이용하면 된다.


