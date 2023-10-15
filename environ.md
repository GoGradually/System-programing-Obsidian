```c
#include <unistd.h>

extern char **environ;
```
환경 변수 전체에 대한 포인터.
while문으로 해당 환경변수의 각 원소에 접근 가능.