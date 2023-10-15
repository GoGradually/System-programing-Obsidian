~~~c
#include <sys/types.h>
#include <unistd.h>

pid_t getsid(pid_t pid);
~~~
pid로 지정한 프로세스가 속한
세션의 ID를 리턴.