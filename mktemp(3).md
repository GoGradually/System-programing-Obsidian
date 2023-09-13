~~~c
#include <stdlib.h>
char *mktemp(char *template);
~~~
임시 파일의 템플릿을 인자로 받아 이를 임시 파일명으로 변환해 리턴한다.
인자인 템플릿의 형태는
반드시 뒤에 "XXXXXX" (X 6개)가 들어있어야 한다.