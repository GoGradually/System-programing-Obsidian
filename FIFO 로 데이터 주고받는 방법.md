## 서버 프로그램과 클라이언트 프로그램의 통신 샘플 코드

#### 서버 프로그램
```c
#include <sys/stat.h>
#include <fcntl.h>
#include <unistd.h>
#include <stdlib.h>
#include <stdio.h>
#include <string.h>

int main(){
	int pd, n;
	char msg[] = "Hello, FIFO";
	printf("Server=======\n");
	// HAN-FIFO 라는 FIFO 파일 생성
	if(mkfifo("./HAN-FIFO", 0666) == -1){
		perror("mkfifo");
		exit(1);
	}
	// 생성한 FIFO 파일 열기
	if((pd = open("./HAN-FIFO", O_WRONLY))==-1){
		perror("open");
		exit(1);
	}
	
	printf("To Client : %s\n", msg);
	
	// FIFO 파일에 해당 메시지 입력 = 메시지 전송
	n = write(pd, msg, strlen(msg) + 1);
	if(n==-1){
		perror("write");
		exit(1);
	}
	close(pd);
}
```

#### 클라이언트 프로그램
```c
#include <fcntl.h>
#include <unistd.h>
#include <stdlib.h>
#include <stdio.h>

int main(){
	int pd, n;
	char inmsg[80];
	
	// FIFO 파일 열기
	if((pd=open("./HAN-FIFO", O_RDONLY))==-1){
		perror("open");
	}
	
	printf("Client ========\n");
	// write(1, ~~~) = 표준 출력 하기
	write(1, "From Server : ", 13);
	
	//FIFO 안에 있는 내용 읽어들이기
	while((n=read(pd, inmsg, 80))>0)
		write(1, inmsg, n);
	
	if(n==-1){
		perror("read");
		exit(1);
	}
	
	write(1, "\n", 1);
	close(pd);
}
```

주의) 클라이언트 프로그램은 HAN-FIFO 특수 파일이 이미 존재한다고 가정하고 작성되어 있다.
그러므로 반드시 서버 프로그램을 먼저 실행한 뒤 클라이언트 프로그램을 실행해야 한다.
주의2) 서버 프로세스는 클라이언트 프로세스가 실행할 때까지 대기하고 있다가 실행된다.