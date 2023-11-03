초 단위로 현재 시간 정보를 얻는다.
1970년 1월 1일을 기준으로 지난 시간을 초 단위로 읽는다.

실패하면 -1 반환

~~~c
#include <sys/types.h>

#include <time.h>

#include <stdio.h>

  

int main(){
	time_t tloc;
	time(&tloc);
	printf("Time(sec) : %d\n", (int)tloc);
}
~~~