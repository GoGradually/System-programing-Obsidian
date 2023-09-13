~~~c
#include <sys/stat.h>
int chmod(const char *pathname, mode_t mode);
~~~
pathname = 접근 권한을 변경하려는 파일의 경로
mode = 접근 권한 변경하려는 값

권한의 변경 방식 -> 대입!!!
해당 비트를 mode 의 비트로 바꾼다.

기존 설정을 유지한 채 권한을 추가로 변경하려면?
stat 구조체에 접근하여 .st_mode를 변경 후 chmod!!!

