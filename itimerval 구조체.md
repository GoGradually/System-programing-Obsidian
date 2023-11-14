```c
struct itimerval{
	struct timeval it_interval;
	struct timeval it_value;
};
```

it_interval = 0 이면 다음 타이머가 만료될 때 타이머 기능이 멈춤.
it_value = 0 이면 타이머 기능이 멈춤.

각 값은 [[timeval 구조체]] 에 값이 저장됨.