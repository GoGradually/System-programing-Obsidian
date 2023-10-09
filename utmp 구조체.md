로그인 기록을 검색하기 위한 구조체.

~~~c
struct utmp{
	short ut_type;               //현재 읽어온 항목에 저장도니 데이터의 형식
	pid_t ut_pid;                //로그인 프로세스의 PID
	char ut_line[UT_LINESIZE];    // 사용자가 로그인한 장치명
	char ut_it[4];                 // 터미널 이름 or /etc/inittab 파일에서 읽어온 ID
	char ut_user[UT_NAMESIZE];       //사용자명
	char ut_host[UT_HOSTSIZE];   
	struct exit_status ut_exit;     //프로세스의 종료 상태
	long ut_session;               //해당 정보의 세션 정보
	struct timeval ut_tv;          //해당 정보를 마지막으로 변경한 시각
	int32_t ut_addr_v6[4];         //원격 접속한 경우 원격 호스트의 인터넷 주소
	char __unused[20];             //추후 사용을 위해 예약해둔 부분
};
~~~