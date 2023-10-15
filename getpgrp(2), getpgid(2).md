~~~c
#include <sys/types.h>
#include <unistd.h>

pid_t getpgrp(void);
pid_t getpgid(pid_t pid);
~~~

getpgrp() : 이 함수를 호출하는 프로세스가 속한 그룹의 PGID를 리턴한다.
getpgid() : pid인자로 지정한 프로세스가 속한 그룹의 PIGD를 리턴한다.