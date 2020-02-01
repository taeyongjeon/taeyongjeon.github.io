---
title: 파일전송 vsftpd 설치 및 설정
date: 2020-01-16 23:46:47
tags:
categories:
- [프로그래밍, 리눅스]
---
## 설치
```
apt-get update
apt-get install vsftpd
```

## 설정
### 1) root 계정으로의 접속을 허용하기
```
nano /etc/ftpusers
# ftpusers안에 있는 사용자는 ftp 접속이 제한된다.
# root계정을 사용하고싶으면 파일안에 root를 삭제하고 저장한다.
```

### 2) 외부에서 파일 쓰기(생성, 복사, 삭제)를 가능하게 하기
```
nano  /etc/vsftpd.conf # 설정파일 실행

#write_enable=YES # 위 항목 찾아서 아래와 같이 주석 제거
write_enable=YES

# nano를 나온다.

/etc/init.d/vsftpd restart # 설정이 적용되게끔 재시작
```

## 사용
* 파일질라나 다른 프로그램으로 접속하면 된다.
* 윈도우 폴더에서 ftp://(리눅스 IP):(포트)의 형태로도 접속 가능하다.
