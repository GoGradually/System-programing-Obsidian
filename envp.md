```c
int main(int argc, char **argv, char ** envp)
{
	env = envp;
}
```


main 함수의 세번째 인자인 envp로 환경 변수에 대한 포인터를 받아
while문을 이용해 환경변수 전체 출력.