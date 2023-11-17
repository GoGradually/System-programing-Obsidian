파일 입출력 방식
```c
fd = open(...);
lseek(fd, ofset, whence);
read(fd, buf, len);
```


메모리 매핑 방식
```c
fd = open(...);
address = mmap((caddr_t) 0, len, (PROT_READ|PROT_WRITE), MAP_PRIVATE, fd, offset);
```