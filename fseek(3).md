~~~c
#include <stdio.h>
int fseek(FILE* stream, long offset, int whence);
~~~

파일 오프셋을 이동시킨다.
whence 로부터 offset만큼 오프셋을 이동시킨다.
whence 의 가능한 값은
- SEEK_SET : 파일의 시작 위치 기준
- SEEK_CUR : 오프셋의 현재 위치 기준
- SEEK_END : 파일의 끝 위치 기준
이 있다.

성공하면 0, 실패하면 -1을 반환한다.
[[lseek(2)]]과는 다르게 현재 오프셋의 위치를 알 수는 없기 때문에
현재 오프셋을 알기 위해선 [[ftell(3)]] 이라는 함수가 필요하다.