~~~c
#include <unistd.h>
int unlink(const char *pathname);
~~~
링크를 끊는다.
심벌릭 링크를 경로로 지정하면 심벌릭 링크가 삭제되고,
하드 링크라면 하드 링크가 삭제된다.
원본 파일이라면 원본 파일도 삭제시킨다.