그룹의 정보를 전달받을 수 있는 구조체.

~~~c
struct group{
	char *gr_name;   //그룹명
	char *gr_passwd;  //그룹 패스워드(보통 공백)
	gid_t gr_gid;     //그룹 아이디 번호
	char **gr_mem;   ///그룹 멤버의 로그인명. 문자열 가리키는 포인터
};
~~~