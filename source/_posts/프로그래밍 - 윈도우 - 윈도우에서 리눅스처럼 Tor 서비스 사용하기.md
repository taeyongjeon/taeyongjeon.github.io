---
title: 윈도우에서 리눅스처럼 Tor 서비스 사용하기
date: 2020-02-22 00:00
categories:
- [프로그래밍, 윈도우]
mathjax: true
---

# 윈도우에서 리눅스처럼 Tor 서비스 사용하기

## 개요
* 우분투 환경에서는 Tor 서비스와 파이썬의 stem 모듈을 통해 아이피 변경이 가능했다.
* 윈도우스에서 이와 같이 구현하려면 Tor 브라우저가 아닌 Expert Bundle을 다운로드받아야 한다.

## 다운로드 및 설치
* https://www.torproject.org/download/ 로 이동한다.
* Download Tor Source Code 를 클릭한다.
* Windows Expert Bundle을 다운로드받는다. tor-win32-0.4.2.6.zip이라는 이름을 가지고 있다.
* 압축을 풀고 Tor라는 폴더를 C드라이브에 옮긴다. 이제 다른 파일과 zip 파일은 삭제해도 된다.
* cmd를 실행한 다음 아래 명령어를 실행한다.

## 토르 실행해보기
```bash
c:\Tor\tor.exe
```
* 아래 결과가 나오면 성공이다.
```bash
[notice] Bootstrapped 100% (done): Done
```

이제 토르의 기능을 모두 사용할 수 있다.
하지만 윈도우 서비스가 아니라 실행했을 뿐이기 때문에, **윈도우를 종료하면 토르도 함께 종료**된다.

**토르를 서비스로 등록하려면 아래 과정을 따라가면 된다.**

## 토르 서비스를 설치하기
아래 명령어는 cmd(관리자 권한으로 실행)에 입력한다.

```bash
c:\Tor\tor.exe --service install -options ControlPort 9051
c:\Tor\tor.exe --service start
```

위 명령어를 입력할 때 오류가 뜬다면 tor 브라우저를 따로 다운로드받아 실행하고(브라우저를 켜놓고) 설치하면 된다. 그리고 브라우저를 지우면 된다.

이제 아래 명령어를 입력해서 제대로 실행되었는지 확인하면 된다.
```bash
netstat -aon | findstr ":9050"
netstat -aon | findstr ":9051"
```
토르 서비스는 기본 포트(서비스에 접근하는 용도)로 9150, ControlPort(데이터 통신용 포트)로 9151을 사용하기 때문에 두 포트가 사용중인지 확인하면 된다.

## 토르를 사용하기
* 파이썬의 stem 모듈은 파이썬에서 tor를 사용하기 위해 만들어졌다.
* 필요 라이브러리를 아래와 같이 설치한다.
```bash
pip3 install stem
pip3 install requests
```

* 아래의 코드로 토르 서비스가 실행되는 지를 확인할 수 있다.
**이 코드는 tor 서비스가 있는 우분투에서도 그대로 쓸 수 있다.**

```python
from stem import Signal
from stem.control import Controller
import requests

proxies = {"http": "socks5://127.0.0.1:9050","https": "socks5://127.0.0.1:9050"}
url = "https://api.ipify.org/?format=json"

response = requests.get(url)
print("IP : " + response.text)

with Controller.from_port(port=9051) as c:
    c.authenticate()
    c.signal(Signal.NEWNYM)

response = requests.get(url, proxies=proxies)
print("New IP : " + response.text)
```

두 IP가 다르게 나오면 성공이다.

만약 selenium을 사용한다면 아래와 같이 입력한다.

```python
from selenium import webdriver

PROXY = "socks5://localhost:9050"
options = webdriver.ChromeOptions()
options.add_argument('--proxy-server=%s' % PROXY)
driver = webdriver.Chrome(options=options, executable_path=r'chromedriver.exe')
driver.get("http://check.torproject.org")
```








## 참고문헌
* [윈도우에서 토르 서비스 실행하기](https://miloserdov.org/?p=1839)
* [9051 포트 에러 고치기 및 토르 서비스 설치하기(ConnectionRefusedError, stem.SocketError: [WinError 10061])](https://stackoverflow.com/questions/45972637/getting-tor-controlport-to-work)
* [Control Port가 무엇인가?](http://www.sunellsecurity.com/support_detail.php?id=1590)
