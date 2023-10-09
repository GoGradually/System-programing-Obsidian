현재 하드웨어가 사용할 수 있는 자원의 최댓값 확인하는 함수

~~~c
#include <stdio.h>

#include <unistd.h>

  

int main() {

    printf("Arg Max : %ld\n", sysconf(_SC_ARG_MAX));

    printf("Clock Tick : %ld\n", sysconf(_SC_CLK_TCK));

    printf("Max Open File : %ld\n", sysconf(_SC_OPEN_MAX));

    printf("Max Lo9gin Name Length : %ld\n", sysconf(_SC_LOGIN_NAME_MAX));

}
~~~