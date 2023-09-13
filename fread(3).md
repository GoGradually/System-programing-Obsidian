~~~c
#include <stdio.h>
size_t fread(void *ptr, size_t size, size_t nmemb, FILE *stream);
~~~

버퍼 기반 입출력.
좀 더 직관적으로 설정할 수 있다.

ptr = 버퍼 주소
size = 버퍼 크기
nmemb = 읽어올 항목 수
stream = 파일 포인터

