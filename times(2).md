실행 시간을 측정하여 반환하는 함수.
매개변수로 넘겨받은 tms 포인터에 저장도 하고
지난 시간의 클록 틱도 반환한다.
오류가 발생하면 -1을 반환한다.

~~~c
#include <sys/times.h>

clock_t times(struct tms *buf);
~~~
