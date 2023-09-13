~~~c
#include <stdlib.h>
void *realloc(void* ptr, size_t size);
~~~
이미 할당받은 메모리에 추가로 메모리를 할당할 때 사용하는 함수
이전에 할당 받은 메모리와 추가할 메모리를 합한 크기의 메모리를 새롭게 할당하고 주소를 리턴.
이때 이전 메모리의 내용을 새로 할당된 메모리로 복사!!!!!

실제 구현 형태

~~~c
char *ptr, *new;
ptr = malloc (sizeof(char) * 100);
new = realloc(ptr, 100);
~~~
