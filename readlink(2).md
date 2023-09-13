~~~c
#include <unistd.h>
ssize_t readlink(const char *pathname, char *buf, size_t bufsiz);
~~~
심벌릭 링크의 데이터 블록에 저장된 내용 확인하기
(심벌릭 링크를 vi로 열면 원본 파일이 열린다.)

성공하면 읽어온 데이터의 크기 (바이트 수),
실패하면 -1 반환