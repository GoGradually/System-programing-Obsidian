root 사용자만이 접근할 수 있는 shadow 구조체

똑같이 콜론으로 구분된 정보들이 순서대로 있다.

~~~c
struct spwd {
	char *sp_namp;   //로그인 명 저장
	char *sp_pwdp;  //사용자의 패스워드 암호화해 저장
	int sp_lstchg;  //패스워드를 변경한 날짜 정보. 1970년 1월 1일부터 일수로 계산해 저장
	int sp_min;  //변경된 패스워드를 사용해야 하는 최소 일 수
	int sp_max;  //변경된 패스워드를 사용해야 하는 최대 일 수
	int sp_warn;  //변경할 날이 되기 전 경고문이 뜨기 시작하는 일 수
	int sp_inact;  //만료된 이후 사용자 계정이 정지될 때까지의 일 수
	int sp_expire;  //계정이 만료되는 날짜 정보. 1970년 1월 1일부터 일수로 계산해 저장
	unsigned int sp_flag;  //나중에 사용하기 위해 예약된 공간. 현재는 사용 X	
};
~~~