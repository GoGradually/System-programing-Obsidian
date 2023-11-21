### mkfifo(3)
```c
#include <sys/types.h>
#include <sys/stat.h>

int mkfifo(const char *pathname, mode_t mode);
```
pathname 경로에 mode 접근권한으로 FIFO 파일 생성.
성공하면 0, 실패하면 -1 반환