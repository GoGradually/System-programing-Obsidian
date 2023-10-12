초 단위 시간 정보를 인자로 받아 [[tm 구조체]]형태로 리턴한다.
gmtime -> UTC 시간대
localtime -> 지역 시간대

~~~c
#include <time.h>

#include <stdio.h>

  

int main(){
	
	struct tm *tm;
	
	time_t timep;
	
	  
	
	time(&timep);
	
	printf("Time(sec) : %d\n", (int)timep);
	
	  
	
	tm = gmtime(&timep);
	
	printf("GMTIME=Y:%d ", tm->tm_year);
	
	printf("M:%d ", tm->tm_mon);
	
	printf("D:%d ", tm->tm_mday);
	
	printf("H:%d ", tm->tm_hour);
	
	printf("M:%d ", tm->tm_min);
	
	printf("S:%d ", tm->tm_sec);
	
	  
	
	tm = localtime(&timep);
	
	printf("LOCALTIME=Y:%d ", tm->tm_year);
	
	printf("M:%d ", tm->tm_mon);
	
	printf("D:%d ", tm->tm_mday);
	
	printf("H:%d ", tm->tm_hour);
	
	printf("M:%d ", tm->tm_min);
	
	printf("S:%d ", tm->tm_sec);

}
~~~