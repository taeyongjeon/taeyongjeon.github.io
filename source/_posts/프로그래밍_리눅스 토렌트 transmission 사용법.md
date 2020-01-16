---
title: 리눅스 토렌트 transmission 사용법
date: 2020-01-16 23:46:50
tags:
categories:
- [프로그래밍, 리눅스]
---
## 설치
```
sudo apt-get install transmission-daemon
sudo service transmission-daemon start
```

## 설정
```
sudo nano /etc/transmission-daemon/settings.json # 설정 파일을 연다
```

```
"rpc-username": "<로그인 아이디>"
"rpc-password": "<로그인 패스워드>" # 설정 파일을 저장하고 서비스를 실행하면 패스워드를 암호화 시켜 버리므로 설정 파일을 열어 패스워드가 노출되는 일은 걱정 하지 않아도 된다.
"rpc-whitelist-enabled": false # 특정 아이피에서만 연결되도록 하는 기능이다 보안을 위해 필요하지만 편의상 끄도록 하겠다.
"ratio-limit-enabled": true # 다운로드 대비 업로드 비율을 조절할 수 있다.
"ratio-limit": 0.5 # 1은 토렌트로 다운받는 파일이 100MB 라면 100MB 를 업로드 한 후 Seeding이 멈춘다. 0.5는 50%.
"download-queue-size": 2 # 동시에 다운로드하는 수를 제한 할 수 있다.
"preallocation": 1 # 다운로드 파일을 미리 생성하는 방식을 정한다. 1은 파일 용량만큼 미리 파일을 만들어 두고 다운로드 하면서 채우는 방식. 0은 다운로드 받으면서 파일 용량을 늘린다.
"download-dir": "<다운로드경로>" # 가장 중요한 다운로드 경로. 기본값은 /var/lib/transmission-daemon/downloads
```

## 사용
* 윈도우 웹 브라우저에서 http://(리눅스 서버의 호스트 네임 혹은 아이피):9091/ 로 접속한다.
  - * 9091은 기본 포트로 settings.json에서 변경할 수 있다.
* 아이디, 비밀번호를 입력해준다.
* ![트랜스미션 서비스](/images/2020/01/transmission.png)
* 여기에 마그넷 링크나 토렌트 파일을 업로드하면 자동으로 업로드된다.
* 모바일 : Transmission Remote 어플로 다운로드 상태를 확인할 수 있다.

## 참고 링크
[남아도는 우분투 리눅스 서버가 있어서 토렌트를 설치했다.](https://zenr.me/2124)
