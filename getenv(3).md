```c
#include <stdlib.h>

char *getenv(const char *name);
```

인자로 지정한 환경 변수가 설정되어 있는지 검색해 결과값을 저장하고 주소를 리턴.
실패하면 NULL 포인터 리턴.