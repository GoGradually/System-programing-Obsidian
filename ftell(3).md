~~~c
#include <stdio.h>
long ftell(FILE *stream);
~~~
입력받은 파일 포인터의 현재 오프셋 위치를 반환한다.
실패하면 EOF를 반환한다.