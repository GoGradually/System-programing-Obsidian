```c
#include <sys/types.h>
#include <sys/wait.h>

int waitid(idtype_t idtype, id_t id, siginfo_t *infop, int options);
```
[[waitpid]] 보다 상세한 특정 자식 프로세스와 동기화 함수.

### 인자별 설명
#### idtype 
기다리는 자식 프로세스를 지정하며, 다음 값 중 하나를 지정한다.
- P_PID : pid가 id와 일치하는 자식 프로세스를 기다린다.
- P_GID : gid가 id와 일ㅊ치하는 자식 프로세스를 기다린다.
- P_ALL : 모든 자식 프로세스를 기다린다. 이 경우 id 인자 값은 무시한다.

#### id
pid나 gid등 idtype과 엮어서 프로세스 (그룹) id를 지정한다.

#### infop
waitid 함수가 성공하면 결과값을 채워서 돌려주는 siginfo_t 구조체.
해당 구조체에 종료된 프로세스에 대한 정보를 저장한다.
- si_pid : 자식 프로세스의 PID
- si_uid : 자식 프로세스의 UID
- si_signo : 시그널로 항상 SiGCHLD 로 설정
- si_status : 자식 프로세스의 종료 상탯값
- si_code : 자식 프로세스가 종료된 이유 코드 저장
  - CLD_EXITED : 자식 프로세스가 \_exit()함수를 호출해 종료
  - CLD_KILLED : 자식 프로세스가 시그널을 받고 종료
  - CLD_DUMPED : 자식 프로세스가 시그널을 받고 종료하고 코어 덤프 수행
  - CLD_STOPPED : 자식 프로세스가 시그널을 받고 중단된 상태
  - CLD_CONTINUE : SIGCONT 시그널을 받고 자식 프로세스가 계속 실행

#### options
waitid() 함수의 리턴 조건을 or로 연결해두는 인자.
- WEXITED : 자식 프로세스가 종료될 때까지 기다린다.
- WSTOPPED : 시그널을 받아 중단된 자식 프로세스를 기다린다.
- WCONTINUED : 시그널을 받아 다시 수행 중인 자식 프로세스를 기다린다.
- WNOHANG : 블로킹 안한다.
- WNOWAIT : 상태값을 리턴한 프로세스가 대기 상태로 머물 수 있도록 한다.
