```c
struct hostent{
	char *h_name;               //호스트명
	char **h_aliases;           //호스트 별명
	int h_addrtype;             //호스트 주소 형식
	int h_length;               //주소 길이
	char **h_addr_list;         //호스트의 주소 목록.
};
```