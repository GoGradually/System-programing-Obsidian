```c
#include <stdlib.h>

int atexit(void (*function)(void));
int on_exit(void (*function)(int, void *), void *arg);
```

함수를 인자로 받아
해당 함수를 프로세스 종료 전에 실행시키고
프로세스를 종료한다.

만약 atexit가 여러개라면 주어진 순서가 
아래에서부터 위로 순서대로 함수를 실행하고 프로세스를 종료한다.