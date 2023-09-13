~~~c
#include <sys/types.h>
#include <sys/stat.h>
#include <fcntl.h>

int creat(const char *pathname, mode_t mode);
~~~
[[open(2)]] 함수에 파일 생성 기능이 없었던
구버전 유닉스에서 사용하던 함수.