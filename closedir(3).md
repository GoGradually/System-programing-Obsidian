~~~c
#include <sys/types.h>
#include <dirent.h>

int closedir(DIR *dirp);
~~~
dirp 가 가리키는 객체를 닫는다.
성공하면 0, 실패하면 -1 반환.