```c
#include <sys/types.h>
#include <sys/wait.h>

pid_t wait(int *wstatus);
```

자식 프로세스 중 아무거나 종료할 때까지 대기한다.
자식 프로세스 중 하나가 종료되면 해당 프로세스의 ID를 반환한다.

status 에 자식 프로세스의 종료 상태값을 저장받는다.

exit(0), exit(1), exit(2) 위와 같은 종료될 때의 상태값을 반환받는다는 뜻.