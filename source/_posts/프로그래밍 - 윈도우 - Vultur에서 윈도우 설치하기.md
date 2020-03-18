---
title: Vultur에서 윈도우 설치하기
date: 2020-02-26 00:00
categories:
- [프로그래밍, 윈도우]
mathjax: true
---

# Vultur에서 윈도우 설치하기
1. Windows 10 1909 Virtio ISO (64 bit) ISO 파일을 받아둔다(약 5GB)
2. vultur 로그인
3. ISO에 1번에서 받은 파일 추가(드랍박스 등 연동해야 할 수도 있음)
4. 새로운 서버 추가 메뉴에서 도쿄 - Upload ISO 탭에 있는 ISO 파일 선택 - 매달 10달러 - 서버 이름 정하고 Deploy Now 클릭
6. 서버 Status가 Running으로 바뀌면 그 오른쪽의 Mange 클릭
7. 윈도우 창이 뜨는데 다음과 같이 진행한다.
언어 건들지 말고 다음
Install Now 클릭
I don't have a product key 클릭
Windows 10 Pro 선택 후 Next
라이센스 체크 후 Next
Custom - Load driver - Browse - CD Drive\virtio\viostor\w10\amd64 선택 - Next
New - 25600 입력 - Apply - Ok - Next
지역 건들지 말고 Yes 클릭
키보드 US, 한글 고르기
network는 Skip for now 클릭
암호 입력
질문 답변 적당히 입력(안씀)
Cortana : No
privacy : Accept

8. 윈도우 설치가 끝났다. 드라이버를 다음과 같이 설치한다.
내 컴퓨터 우클릭 - Manage - Device Manager - Other devices로 이동
Ethernet Controller 우클릭 - Update driver - Browse... 선택 - Browse... 선택 - CD Drive\virtio 선택 후 Ok - Next
중간에 뭐가 뜨면 Install 클릭 - 설치 후 Do you want to allow... 는 Yes 클릭
PCI Device도 같은 과정으로 설치
9. 컴퓨터를 원격으로 조정해야 한다. 다음과 같이 진행한다.
검색창에 Allow remote 입력 - Allow remote access to your computer 클릭 - Allow remote connections to this computer 체크 - Allow connections only... 체크 해제 - Apply - Ok

서버 컴퓨터 말고 로컬 컴퓨터의 원격 데스크톱 연결(Remote Desktop Connection) 실행 - Vultur에 있는 IP 복사 - 유저명, 암호 입력 - Don't ask... 에 체크하고 Yes 클릭
원격 완료.
10. 가상 메모리 늘리기
내 컴퓨터 우클릭 - 속성(Properties) - 고급 시스템 설정(Advanced system settings) - Performance에서 시각 효과는 best performance, Advanced 탭에서 Change로 이동 - Custom size 체크 후 4000,8000 입력 후 Set, OK




## 참고문헌
* [윈도우에서 토르 서비스 실행하기](https://miloserdov.org/?p=1839)
* [9051 포트 에러 고치기 및 토르 서비스 설치하기(ConnectionRefusedError, stem.SocketError: [WinError 10061])](https://stackoverflow.com/questions/45972637/getting-tor-controlport-to-work)
* [Control Port가 무엇인가?](http://www.sunellsecurity.com/support_detail.php?id=1590)
