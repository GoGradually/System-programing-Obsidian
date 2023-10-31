etc/group 순차적으로 읽는 함수.

[[group 구조체]]
~~~c
#include <grp.h>

#include <stdio.h>

  

int main() {

    struct group *grp;

    int n, m;

  

    for (n = 0; n < 3; n++) {

        grp = getgrent();

        printf("Group Name : %s\n", grp->gr_name);

        printf("GID : %d\n", (int)grp->gr_gid);

        m = 0;

        printf("Members : ");

        while (grp->gr_mem[m] != NULL) printf("%s ", grp->gr_mem[m++]);

        printf("\n");

    }

}
~~~