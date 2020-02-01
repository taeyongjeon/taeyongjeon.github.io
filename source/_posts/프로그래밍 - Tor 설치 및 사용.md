---
title: Tor 설치 및 사용
date: 2020-01-18 14:07:55
tags:
categories:
- [프로그래밍, 리눅스]
---
## 설치
### 1) 기본 설치
```
sudo apt-get install tor
```
### 2) 파이선 라이브러리 설치
```
pip install requests
pip install -U requests[socks] # -U 옵션 : 이미 설치된 경우 업데이트한다.
pip install -U requests[security]
```

### 3) IP를 필요할 때 바꾸게 해 주는 stem 설치
```
pip install stem
```
## 설정
### 1) 서비스 실행
```
sudo service tor start # 서비스 시작
```

제대로 실행되는 지 확인하고자 다음 명령어를 입력한다.
```
curl --socks5 localhost:9050 --socks5-hostname localhost:9050 -s https://check.torproject.org/ | cat | grep -m 1 Congratulations | xargs
```
위 명령어를 입력하면 아래처럼 나온다.
```
Congratulations. This browser is configured to use Tor.
```
### 2) Stem 설정
```
sudo nano /etc/tor/torrc
```
아래 내용이 있다.
```
#ControlPort 9051

#CookieAuthentication 1
```
아래와 같이 변경한다.
```
ControlPort 9051

CookieAuthentication 1
```
서비스를 재시작한다.
```
sudo service tor restart
```

## 사용
### 1) Tor로 IP 얻기
```{.python}
# tor.py
import requests

proxies = {
    'http': 'socks5://127.0.0.1:9050',
    'https': 'socks5://127.0.0.1:9050'
}


print(requests.get('https://ident.me').text)# 원래 아이피
print(requests.get('https://ident.me', proxies=proxies).text) # 새로운 아이피
```

### 2) 다른 IP 받기
```{.python}
# tor.py
import requests
from stem import Signal
from stem.control import Controller

proxies = {
    'http': 'socks5://127.0.0.1:9050',
    'https': 'socks5://127.0.0.1:9050'
}

print(requests.get('https://ident.me', proxies=proxies).text) # Tor를 사용중일 때의 기존 아이피

with Controller.from_port(port = 9051) as c:
    c.authenticate()
    c.signal(Signal.NEWNYM)

print(requests.get('https://ident.me', proxies=proxies).text) # 새로 받은 아이피
```

## 참고자료
* [대부분은 여기를 참고했다.](https://www.sylvaindurand.org/use-tor-with-python/)
* [pip install requests[socks]가 안먹혀서 여기서 해결했다](https://stackoverflow.com/questions/12601316/how-to-make-python-requests-work-via-socks-proxy)
