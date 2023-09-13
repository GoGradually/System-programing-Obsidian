~~~c
#include <stdlib.h>

void *malloc(size_t size);
~~~
인자로 지정한 크기의 메모리를 할당.
할당된 메모리를 초기화하지 않는다는 데 주의.
성공하면 메모리의 시작 주소
실패하면 NULL 포인터 반환

실제 사용 예시
~~~c
char *ptr;
ptr = malloc(sizeof(char) * 100);
~~~
