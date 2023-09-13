~~~c
#include <stdio.h>
size_t frwrite(const svoid *ptr, size_t size, size_t nmemb, FILE *stream);
~~~

버퍼 기반 출력 함수.

항목의 크기가 size인 데이터를 nmemb에서 지정한 개수만큼 ptr에서 끊어 읽어 stream에 출력한다.

성공하면 출력한 항목 개수를
실패하면 -1(EOF)를 반환한다.