### 소켓의 종류
- 유닉스 도메인 소켓
	- 같은 호스트에서 프로세스 사이에 통신할 때 사용
	- AF_UNIX
- 인터넷 소켓
	- 인터넷을 통해 다른 호스트와 통신할 때 사용
	- AF_INET
### 소켓의 통신방식
- SOCK_STREAM : TCP 사용
- SOCK_DGRAM  : UDP 사용

### 통신 유형
- AF_UNIX - SOCK_STREAM
- AF_UNIX - SOCK_DGRAM
- AF_INET - SOCK_STREAM
- AF_INET - SOCK_DGRAM

###  [[소켓 주소 구조체 - sockaddr]]

### 바이트 순서
- 빅 엔디언 : 높은 주소부터 차례대로 데이터 저장
	- 0x1234 -> 0x12, 0x34
	- 네트워크 바이트 순서(NBO) 가 이 방식 채택.
- 리틀 엔디언 : 낮은 주소부터 거꾸로 데이터 저장
	- 0x1234 -> 0x34, 0x12
	- intel CPU의 경우 이 방식을 호스트 바이트 순서(HBO)로 채택

- [[바이트 순서 함수]]
- [[IP주소 변환 함수]]


# [[소켓 인터페이스 함수]]
