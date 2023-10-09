로그인명을 받아 사용자 정보 검색한 뒤 passwd 구조체 포인터를 반환.
실패하면 NULL 포인터를 반환한다.

~~~c
#include <sys/types.h>

#include <pwd.h>

#include <stdio.h>

  

int main(){

    struct passwd *pw;

  

    pw = getpwnam("joonho");

    printf("UID : %d\n", (int)pw->pw_uid);

    printf("Home Directory : %s\n", (pw->pw_dir));    

}
~~~