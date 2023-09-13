현재 파일의 status 정보를 받기 위해 만들어진 구조체.
~~~c
struct stat {
	dev_t st_dev;  // 파일이 저장되어 있는 장치 번호
	ino_t st_ino;  // inode 번호
	mode_t st_mode; // 파일의 종류 & 접근 권한. stat 에서 가장 중요한 것
	nlink_t st_nlink; // 하드 링크의 개수
	uid_t st_uid;   // 파일 소유자의 uid
	gid_t st_gid    // 파일 소유 그룹의 GID
	dev_t st_rdev;  // 장치 파일이면 주 장치 번호와 부 장치 번호 저장. 아니면 아무 의미 없음.
	off_t st_size;  
	blksize_t st_blksize;  // 파일 내용을 입출력할 때 사용하는 버퍼의 크기 저장
	blkcnt_t st_blocks;    // 파일에 할당된 파일 시스템의 블록 수. 블록의 크기=512byte
	struct timespec st_atim; // 마지막으로 파일을 읽거나 실행한 시각. timespec 구조체로 저장
	struct timespec st_mtim; // 마지막으로 "쓰기"한 시각. timespec 구조체로 저장.
	struct timespec st_ctim; // 마지막으로 inode를 변경한 시각. timespec 구조체로 저장.

	//리눅스 커널 2.6 이전 버전과의 호환성을 위해 타임스탬프 값 초단위로 매핑해 정의
	#define st_atime st_atim.tv_sec
	#define st_mtime st_mtim.tv_sec
	#define st_ctime st_ctim.tv_sec
};
~~~
핵심은 [[st_mode]]
