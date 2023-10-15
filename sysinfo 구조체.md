~~~c
struct sysinfo{
	long uptime;             //부팅 후 경과된 시간
	unsigned long loads[3]; //시스템 부하 평균을 저장. 1분, 5분,15분 기준으로 계산 후 저장
	unsigned long totalram; //사용 가능한 총 메모리 크기
	unsigned long freeram;  //사용 가능한 메모리 크기
	unsigned long sharedram;//공유 메모리 크기
	unsigned long bufferram;//버퍼가 사용하는 메모리 크기
	unsigned long totalswap;//스왑 영역의 총 크기
	unsigned long freeswap; //사용 가능한 스왑 영역의 크기
	unsigned long procs;    //현재 실행 중인 프로세스 수
	unsigned long totalhigh;//사용자에게 할당된 메모리의 총 크기
	unsigned long freehigh; //사용 가능한 사용자 메모리의 크기
	unsigned int mem_unit;  //메모리 크기를 바이트 단위로 저장
	char _f[20-2*sizeof(long)-sizeof(int)];  //64 바이트를 맞추기 위한 패딩
};
~~~

