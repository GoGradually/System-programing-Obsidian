~~~c
#inclue <stdio.h>

void perror(const char *s)
~~~

전역 변수 내 [[errno]]파일을 참고하여
printf("%s : %s", s, errno_내용) 을 실행한다.

실제 구현 코드 형태

~~~c
#include <stdio.h>
#include <unistd.h>
#include <errno.h>
#include <stdlib.h>

int main(){
	if(access("test.txt", R_OK) == -1){
		perror("test.txt");
		exit(1);
	}
}
~~~