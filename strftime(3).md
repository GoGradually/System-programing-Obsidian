[[ctime(3)]]과 [[asctime(3)]]에서 더 발전하여 
출력 형식까지 마음대로 지정할 수 있게 되는 함수.
printf문처럼 사용할 수 있게 된다.

~~~c
#include <stdio.h>

#include <time.h>

  

char *output[] = {"%x %X", "%G년 %m월 %d일 %U주 %H:%M", "%r"};

  

int main() {
	struct tm *tm;
	
	time_t timep;
	int n;
	char buf[257];
	
	time(&timep);
	tm = localtime(&timep);
	
	for (n = 0; n < 3; n++) {
		strftime(buf, sizeof(buf), output[n], tm);
		printf("%s = %s\n", output[n], buf);	
	}
}
~~~