```c
#include <stdlib.h>
int unsetenv(const char *name);
```

name에 지정한 환경 변수를 삭제한다.
현재 환경에 name으로 저장한 환경변수가 없으면 기존 환경을 변경하지 않는다.