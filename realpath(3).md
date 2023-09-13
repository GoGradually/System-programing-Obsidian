~~~c
#include <limits.h>
#include <stdlib.h>

char *realpath (const char *path, char *resolved_path);
~~~
심벌릭 링크가 가리키는 원본 파일의 실제 경로를 resolved_path에 저장한다.

성공하면 실제 경로명이 저장된 곳의 주소를,
실패하면 NULL 반환