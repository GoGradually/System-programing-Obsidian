초 단위 시간 정보를 연, 월, 일로 분해해 저장할 때 사용하는 구조체
time.h 파일에 정의되어 있다.


~~~c
struct tm{
	int tm_sec;
	int tm_min;
	int tm_hour;
	int tm_mday;
	int tm_mon;
	int tm_year;
	int tm_wday;     //요일.  0~6, 0은 일요일
	int tm_yday;     //일 수. 0~365
	int tm_isdst;    //서머타임제 시행 여부
};
~~~