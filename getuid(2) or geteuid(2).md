uid 혹은 euid 를 찾아 반환

UID : 실제 사용자 ID. 프로그램을 실행하는 사용자의 ID
EUID : 유효 사용자 ID. 프로세스에 대한 접근 권한을 부여할 때 사용하는 ID

~~~c
#include <sys/types.h>

#include <unistd.h>

#include <stdio.h>

  

int main(){

    uid_t uid, euid;

    char * name;

  

    uid = getuid();

    euid = geteuid();

    name = getlogin();

  

    printf("Login Name = %s, UID = %d, EUID = %d\n", name, (int)uid, (int)euid);

}
~~~

setuid를 설정하여 일반사용자가 실행한다면 UID가 달라진다