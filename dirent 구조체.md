```c
struct dirent{
	ino_t d_ino; //해당 항목의 inode
	off_t d_off; //디렉터리 오프셋의 위치(폴더의 몇번째 파일인가)
	unsigned d_reclen; // 해당 항목의 레코드 길이
	unsigned char d_type; //파일의 종류
	char d_name[256]; //항목의 이름
}
```