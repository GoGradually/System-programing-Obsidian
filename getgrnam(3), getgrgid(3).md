group 구조체를 반환받는 함수. 그룹의 정보를 파악할 수 있다.
~~~c
#include <grp.h>

#include <stdio.h>

  

int main(){

    struct group *grp;

    int n;

  

    grp = getgrnam("adm");

    printf("Group Name : %s\n", grp->gr_name);

    printf("GID : %d\n",(int)grp->gr_gid);

  

    n = 0;

    printf("Members : ");

    while(grp->gr_mem[n] != NULL) printf("%s ", grp->gr_mem[n++]);

    printf("\n");

}
~~~