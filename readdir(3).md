~~~c
#include <dirent.h>
struct dirent *readdir (DIR *dirp);
~~~

현재 DIR 객체 내에서 디렉터리 [[오프셋]] 이 가리키는 파일을 읽는다 
-> 디렉터리의 각 항목에 대하여 [[dirent 구조체]] 형태로 저장
성공하면 디렉터리에 있는 현재 오프셋이 가리키는 항목의 정보를 가리키는 [[dirent 구조체]]의 포인터 리턴,
실패하면 NULL 반환