~~~c
#include <dirent.h>
struct dirent *readdir (DIR *dirp);
~~~

현재 DIR 객체 내에서 디렉터리 [[오프셋]] 이 가리키는 파일을 읽는다
성공하면 디렉터리에 있는 항목의 정보를 가리키는 dirent 구조체의 포인터 리턴,
실패하면 NULL 반환