~~~c
#include <stdlib.h>

void *calloc(size_t nmemb, size_t size);
~~~

nmemb X size 바이트 크기의 배열을 저장할 메모리를 할당.
calloc 함수는 할당된 메모리를 0으로 초기화시킨다.

실제 사용 예시
~~~c
char* ptr;
//요소가 10개, 각 요소의 크기가 20바이트
ptr = calloc(10, 20);
~~~
