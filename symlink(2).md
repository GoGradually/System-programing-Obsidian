~~~c
#include <unistd.h>
int symlink(const char *target, const char *linkpath);
~~~
[[심벌릭 링크]]를 생성한다.
수행에 성공하면 0, 실패하면 -1을 반환한다.
