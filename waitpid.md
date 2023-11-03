```c
#include <sys/types.h>
#include <sys/wait.h>

pid_t waitpid(pid_t pid, int *wstatus, int options);
```

인자로 지정한 pid 프로세스가 종료할 때까지 대기.
상탯값을 리턴한다 = 프로세스가 종료됐다!!(exit(0))

### pid 로 지정할 수 있는 값
- pid < -1 : |pid| 와 같은 프로세스 그룹에 속한 자식 프로세스 중 임의의 프로세스의 상탯값을 요청.
- pid = 1 : wait 함수와 같은 역할.
- pid = 0 : 함수를 호출한 프로세스와 같은 프로세스 그룹에 속한 임의의 프로세스의 상탯값을 요청.
- pid > 0 : 지정한 pid 에 해당하는 프로세스의 상탯값 요청.

### options 로 지정할 수 있는 값.
- WCONTINUED (wait continued) : 수행중인 자식 프로세스의 상탯값 리턴.
- WNOHANG (wait no hang) : pid로 지정한 자식 프로세스의 상탯값을 즉시 리턴받을 수 없어도 이를 호출한 프로세스의 실행을 블로킹 하지 않고 다른 작업 계속 실행.
- WNOWAIT (w no wait) : 상탯값을 리턴한 프로세스가 대기 상태로 머물 수 있도록 한다.(같이 대기)
- WUNTRACED (w untraced) : 실행을 중단한 자식 프로세스의 상탯값을 리턴한다. 실행이 중단되었으므로 더이상 상탯값을 리턴하지 않는다.
