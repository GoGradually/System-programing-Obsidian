~~~c
#include <sys/types.h>
#include <unistd.h>

pid_t getppid(void);
~~~

현재 프로세스를 호출한 부모 프로세스의 ID 출력.