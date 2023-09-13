[[DIR]] 객체를 이용한 폴더 열기

~~~c
#include <sys/types.h>
#include <dirent.h>

DIR *opendir(const char *name);
~~~

성공하면 DIR 객체의 포인터, 실패하면 NULL 반환.
