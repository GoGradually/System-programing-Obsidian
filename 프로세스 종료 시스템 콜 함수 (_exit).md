```c
#include <unistd.h>

void _exit(int status)
```

프로세스 종료 시스템 콜 함수.

다음과 같은 과정을 통해 시스템 관련 자원을 정리한다.
1) 모든 파일 기술자를 닫는다.
2) 부모 프로세스에게 종료 상태를 알린다.
3) 자식 프로세스에 SIGHUP 시그널을 보낸다.
4) 부모 프로세스에 SIGCHLD 시그널을 보낸다.
5) 프로세스 간 통신에 사용한 자원을 반납한다.