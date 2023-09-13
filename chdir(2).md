~~~c
#include <unistd.h>
int chdir(const char *path);
~~~
해당 디렉터리로 이동, 절대 경로와 상대 경로 모두 사용가능

성공하면 0, 실패하면 -1 반환