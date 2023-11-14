```c
typedef struct{
	int si_signo;
	int si_errno;
	int si_code;
	union{
		/*...*/
	}
}
```
- si_signo : 관련된 시그널 번호
- si_errno : 0 또는 시그널과 관련된 오류 번호
- si_code : 시그널 발생 원인을 정의하는 코드

### si_code
si_code 의 값이 0보다 작거나 같다면
사용자 프로세스가 kill(), raise(), abort() 등의 함수로 시그널을 보낸 것.