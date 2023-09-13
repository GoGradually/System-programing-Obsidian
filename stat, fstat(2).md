stat -> 지정된 경로로 들어가서 [[stat 구조체]]를 입력받음.
~~~c
#include <sys/types.h>
#include <sys/stat.h>
#include <unistd.h>

int stat(const char *pathname, struct stat *statbuf);
~~~
성공하면 statbuf 에 정보를 반환받고 0 반환.
실패하면 -1 반환.


fstat -> [[파일 디스크립터]]로 파일에 접근하여 [[stat 구조체]]를 입력받음.
~~~c
#include <sys/types.h>
#include <sys/stat.h>
#include <unistd.h>

int fstat(int fd, struct stat *statbuf);
~~~
성공하면 statbuf 에 정보를 반환받고 0 반환.
실패하면 -1 반환.
