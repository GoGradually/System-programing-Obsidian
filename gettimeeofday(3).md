[[timeval 구조체]]를 이용해서 마이크로초 단위로 시간을 알려준다.

~~~c
#include <sys/time.h>

#include <stdio.h>

  

int main(){

	struct timeval tv;

  

	gettimeofday(&tv, NULL);
	printf("Time(sec) : %d\n", (int)tv.tv_sec);
	printf("Time(micro-sec) : %d\n", (int)tv.tv_usec);

}
~~~