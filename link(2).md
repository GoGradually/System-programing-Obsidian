~~~c
#include <unistd.h>
int link(const char *oldpath, const char *newpath);
~~~
[[하드 링크]]를 생성한다.
oldpath = 기존 파일의 경로
newpath = 새로 생성할 링크의 경로

하드 링크는 같은 파일 시스템안에 있어야 하므로 두 경로를 반드시 같은 파일 시스템으로 지정해야 함.
성공하면 0,
실패하면 -1 반환