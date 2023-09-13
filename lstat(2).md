~~~c
#include <sys/types.h>
#include <sys/stat.h>
#include <unistd.h>

int lstat(const char *pathname, struct stat *statbuf);
~~~

[[심벌릭 링크]] 자체의 파일 정보를 검색한다.
(stat로 심벌릭 링크 검색하면 원본 파일의 정보가 나옴)

pathname = 궁금한 심벌릭 링크의 경로
statbuf = 저장할 stat 구조체 버퍼.

성공할 경우 0, 실패할 경우 -1 반환.