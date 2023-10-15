```c
#include <stdlib.h>

int setenv(const char *name, const char* value, int overwrite);
```

환경 변수명과 그 값을 각각 인자로 받아
해당 환경 변수를 만들어 저장한다.

overwrite 의 값이 0이 아니면 덮어쓰기를 하고
0이면 덮어쓰기를 하지 않는다.