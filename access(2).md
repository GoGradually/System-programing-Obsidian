~~~c
#include <unistd.h>

int access(const char *pathname, int mode);
~~~

pathname = 접근 권한을 알고자 하는 파일의 경로
mode = 확인하고 싶은 권한
권한이 존재하면 0, 존재하지 않으면 -1 반환

R_OK : 읽기 권한 확인
W_OK : 쓰기 권한 확인
X_OK : 실행 권한 확인
F_OK : 파일이 존재하는지 확인

단, 유효 사용자가 아닌 실제 사용자에 대한 접근 권한만 확인 가능