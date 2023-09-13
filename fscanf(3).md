자매품 : scanf()

~~~c
#include <stdio.h>
int scanf(const char *Format, ...);
int fscanf(FILE *stream, const char *format, ...);
~~~

형식 기반 입력 함수.
주어진 형식에 맞춰서 입력을 받는다.

scanf같은 경우에는 stream 의 [[파일 디스크립터]]가 0번을 가리키고 있다고 보면 된다.

성공적으로 수행하면 읽은 항목의 개수를 리턴,
실패하면 EOF를 리턴.