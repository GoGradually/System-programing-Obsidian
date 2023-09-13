자매품 : printf()
~~~c
#include <stdio.h>
int printf(const char *format, ...);
int fprintf(FILE *stream, const char *format, ...);
~~~
형식 기반 출력 함수.
정해진 형식대로 출력한다.

printf()같은 경우에는 [[파일 디스크립터]]가 1번을 가리키고 있다고 보면 된다.

성공하면 출력한 문자 수를,
실패하면 EOF를 반환한다.