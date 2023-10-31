~~~c
#include <unistd.h>
ssize_t read(int fd, void *buf, size_t count);
~~~
[[파일 디스크립터]]가 가리키는 파일에 접근하여
최대 count 개수만큼 buf에 파일을 읽어 담는다.
read는 실제로 읽은 바이트 수를 리턴하며, 
리턴값이 0이면 파일의 끝에 도달해 더이상 읽을 내용이 없음을 의미한다.

만약 파일을 읽는 데 실패하면 -1을 리턴한다.

같이보기
[[fread(3)]]