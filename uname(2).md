운영체제 정보 검색 함수

~~~c
#include <stdio.h>

#include <stdlib.h>

#include <sys/utsname.h>

  

int main() {

    struct utsname uts;

  

    if (uname(&uts) == -1) {

        perror("uname");

        exit(1);

    }

    printf("OSname : %s\n", uts.sysname);

    printf("Nodename : %s\n", uts.nodename);

    printf("Release : %s\n", uts.release);

    printf("Version : %s\n", uts.version);

    printf("Machine : %s\n", uts.machine);

}
~~~