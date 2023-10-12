현재 지역의 시간대로 설정한다.
이 함수를 호출하면 전역 변수에 다음과 같은 정보가 설정된다
~~~c
extern char *tzname[2];     //지역 시간대와 보정된 시간대명을 약어로 저장한다
extern long timezone;       //UTC와 지역 시간대와의 시차를 초 단위로 저장한다
extern int daylight;        //서머타임제 시행하면 0이 아니다
~~~


~~~c
#include <time.h>

#include <stdio.h>

  

int main(){
	tzset();
	
	printf("Timezone : %d\n", (int)timezone);
	printf("Daylight : %d\n", daylight);
	printf("TZname[0] : %s\n", tzname[0];
	printf("TZname[1] : %s\n", tzname[1]);
	
}
~~~