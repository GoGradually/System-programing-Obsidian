~~~c
#include <unistd.h>
int getopt(int argc, char* const argv[], const char *optstring)
~~~

optstring 에 저장된 순서대로 각 옵션의 기능을 지정하는 함수
getopt에 지정된 옵션을 반환한다.

이를 변수에 저장한뒤 switch - case 문으로 각 옵션의 기능을 지정한다.

:  <- 인자를 받은 뒤 다음 문자열도 옵션에 필요한 인자로 인식한다