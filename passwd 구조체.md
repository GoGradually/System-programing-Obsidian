콜론 (:) 으로  구분된 etc/passwd 파일 내용을 쉽게 받아오기 위한 구조체
~~~c
struct passwd {
	char *pw_name;
	char *pw_passwd;  //의미없는 항목
	uid_t pw_uid;
	gid_t pw_gid;
	char *pw_gecos;  //사용자 실명 및 기타 정보
	char *pw_dir;    //홈 디렉터리
	char *pw_shell;   // 로그인 쉘
};
~~~