~~~c
#include <stdio.h>
int rename(const char *oldpath, const char *newpath);
~~~

디렉터리의 이름을 바꾸는 함수.
만약 newpath 에 지정한 이름이 이미 존재하면 해당 디렉터리를 지운다.

실행 도중에 오류가 발생하면 원본과 새로운 디렉터리명이 모두 남는다.

수행에 성공하면 0, 실패하면 -1을 리턴.