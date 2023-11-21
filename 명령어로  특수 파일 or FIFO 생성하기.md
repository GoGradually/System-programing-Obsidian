### 명령어로 특수파일 생성 - mknod
```sh
mknod 파일명 p
```
p = FIFO 파일 생성하라는 뜻.
해당 파일명으로 FIFO 파일 생성함

### 명령어로 FIFO 파일 생성 - mkfifo
```sh
mkfifo -m mode ... NAME ...
```
-m mode 로 파일의 접근 권한 지정
NAME 이라는 이름으로 FIFO 파일 생성한다.