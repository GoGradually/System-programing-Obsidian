UID로 /etc/passwd 파일을 읽어 passwd 구조체 포인터를 반환한다.
실패할경우 NULL 포인터를 반환한다.


~~~c
#include <unistd.h>

#include <sys/types.h>

#include <pwd.h>

#include <stdio.h>

  

int main(){

    struct passwd *pw;

  

    pw = getpwuid(getuid());

    printf("UID : %d\n", (int)pw->pw_uid);

    printf("Login Name : %s\n", pw->pw_name);

}
~~~