```c
#include <stdlib.h>

void exit(int status);
```

프로세스 종료.
표준 입출력 스트림에 데이터가 남아있으면 이를 모두 기록한다.
내부에서 _exit() 함수를 호출한다.