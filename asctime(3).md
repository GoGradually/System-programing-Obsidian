[[tm 구조체]]의 값을 완전히 읽기 쉽게 변환해 주는 함수.

~~~c
#include <time.h>

#include <stdio.h>

  

int main(){
	struct tm *tm;
	time_t timep;
	
	time(&timep);
	tm = localtime(&timep);
	printf("Time(sec) : %d\n", (int)timep);
	printf("Time(date) : %s\n", asctime(tm));
}
~~~