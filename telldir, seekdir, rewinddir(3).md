~~~c
#include <sys/types.h>
#include <dirent.h>

long telldir(DIR *dirp);
void seekdir(DIR *drip, long loc);
void rewinddir(DIR *dirp);
~~~
디렉터리의 오프셋을 이동시키는 함수.

사용법이 세개가 얽힌다.

1. telldir 로 현재 위치를 알 수 있다. 오류가 발생하면 -1 을 리턴한다.

2. seekdir로 현재 위치에서 loc로 넘어갈 수 있다. 이 때 loc 는 telldir로 반환받은 값이어야 한다.

3. rewinddir은 디렉터리 오프셋의 위치를 디렉터리 시작 지점으로 이동시킨다.