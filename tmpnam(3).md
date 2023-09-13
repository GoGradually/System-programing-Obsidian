~~~c
#include <stdio.h>
char *tmpnam(char *s);
~~~
인자가 있으면 해당 인자가 가리키는 곳에 임시 파일명 저장
인자가 없으면 임시 파일명을 반환한다.