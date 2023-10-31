특정 사용자의 정보가 아닌 모든 사용자의 정보를 순서대로 읽어온다.
여러 사용자가 있을 때 이를 전부 탐색하기 위한 함수

[[passwd 구조체]]
~~~c
#include <pwd.h>

#include <Stdio.h>

  

int main(){

    struct passwd *pw;

    int n;

  

    for(n = 0; n<3; n++){

        pw = getpwent();

        printf("UID : %d, LoginName: %s\n", (int)pw->pw_uid, pw->pw_name);

    }

}
~~~