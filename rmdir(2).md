~~~c
#include <unistd.h>

int rmdir(const char *pathname);
~~~
해당 디렉터리 경로로 가서 그 [[디렉터리]]를 삭제한다.
삭제 하려는 디렉터리는 .과 ..을 제외하고 반드시 비어 있어야 한다.
수행에 성공하면 0, 실패하면 -1을 반환.
