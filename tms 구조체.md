프로세스의 실행 시간을 측정한 데이터를 저장하는 구조체.

~~~c
struct tms{
	clock_t tms_uime;
	clock_t tms_stime;
	clock_t tms_cutime;
	clock_t tms_cstime;
};
~~~