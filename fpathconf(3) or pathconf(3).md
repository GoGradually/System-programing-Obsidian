파일과 디렉터리의 자원을 검색할 수 있게 해주는 함수
~~~c
#include <stdio.h>

#include <unistd.h>

  

int main() {

    printf("Link Max : %ld\n", pathconf(".", _PC_LINK_MAX));

    printf("Name Max : %ld\n", pathconf(".", _PC_NAME_MAX));

    printf("Path Max : %ld\n", pathconf(".", _PC_PATH_MAX));

}
~~~