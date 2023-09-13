디렉터리 생성 함수.

~~~c
#include <sys/stat.h>
#include <sys/types.h>

int mkdir(const char *pathname, mode_t mode);
~~~

디렉터리명을 포함한 경로와 생성하는 [[디렉터리]]의 기본 접근 권한을 지정한다.
수행에 성공하면 0, 실패하면 -1 반환.

실제 구현 예시
~~~c
#include <sys/stat.h>
#include <stdlib.h>
#include <stdio.h>

int main(){
	if(mkdir("han", 0755) == -1){
		perror("han");
		exit(1);
	}
}
~~~