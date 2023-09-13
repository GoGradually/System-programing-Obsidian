현재 [[디렉터리]]의 위치를 검색하는 라이브러리 함수.
(cwd = current working directory)

~~~c
#include <unistd.h>

char *getcwd(char* buf, size_t size);
~~~
인자를 받는 방법에는 크게 세가지 방법이 있다.

1. buf 에 경로를 저장할 만큼 충분히 메모리를 할당하고 그 크기를 size에 저장한다.
   -> 사용자가 지정한 버퍼에 경로를 저장.
2. buf 에 NULL을 지정하고 할당이 필요한 메모리 크기를 size에 지정한다.
   ->size에 지정한 크기로 버퍼를 할당하고 이 버퍼에 경로를 저장한다.
3. buf 에 NULL을 지정하고 size는 0으로 지정한다
   ->저장할 경로의 크기에 맞게 시스템이 알아서 버퍼를 할당하고 경로를 저장한다.
   = [[get_current_dir_name(3)]]

2와 3은 사용이 끝나면 [[free(3)]] 함수를 이용해 메모리를 따로 해제해줘야 함.