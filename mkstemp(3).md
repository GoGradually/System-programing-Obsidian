~~~c
#include <stdlib.h>
int mkstemp(char *template);
~~~

템플릿을 지정하여 임시 파일을 생성한다.
성공하면 파일 디스크립터를 반환한다.

사용법은 [[mktemp(3)]]와 같다. (XXXXXX)