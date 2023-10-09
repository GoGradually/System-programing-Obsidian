인자로 지정한 사용자의 spwd 파일 정보를 읽어온다.

~~~c
#include <shadow.h>

#include <stdio.h>

  

int main(){

    struct spwd *spw;

  

    spw = getspnam("joonho");

    printf("Login Name : %s\n", spw->sp_namp);

    printf("Passwd : %s\n", spw->sp_pwdp);

    printf("last change : %ld\n", spw->sp_lstchg);

}
~~~