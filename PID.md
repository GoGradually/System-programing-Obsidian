프로세스를 식별하는 ID.
0번부터 시작한다.
- 0번 프로세스 → 스케쥴러. 프로세스에 cpu 시간을 할당하는 역할. 커널의 일부분이므로 별도의 실행 파일은 없다.
- 1번 프로세스 → init. 프로세스가 새로 생성될때마다 기존 PID와 중복되지 않은 번호가 할당된다.

PPID → Parent Process ID. 현재 프로세스를 호출한 부모 프로세스의 ID.