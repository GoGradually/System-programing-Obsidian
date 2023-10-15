~~~c
#include <sys/sysinfo.h>

int sysinfo(struct sysinfo *info);
~~~
현재 실행중인 프로세스들의 메모리와 [[스왑]] 상태를 저장해 리턴한다.
[[sysinfo 구조체]]에 검색 결과를 저장해 리턴.
