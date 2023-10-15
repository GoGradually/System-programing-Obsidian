~~~c
#include <sys/types.h>
#include <unistd.h>

pid_t setsid(void);
~~~
호출에 성공하면 새로운 세션ID 리턴.
오류가 발생하면 -1 리턴.