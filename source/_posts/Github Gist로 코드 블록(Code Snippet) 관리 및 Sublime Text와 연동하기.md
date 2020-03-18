---
title: Github Gist로 코드 블록(Code Snippet) 관리 및 Sublime Text와 연동하기
date: 2020-03-14 00:00
categories:
- [프로그래밍, Github]
mathjax: true
---

# Github Gist로 코드 블록(Code Snippet) 관리 및 Sublime Text와 연동하기

# 요약
* [Github Gist](https://gist.github.com/)에 Code Snippet을 만들어 둔다.
* Preferences - Pacakge Control - Install Pacakge 로 이동 후 "Gist"라는 이름의 패키지 설치
* [Gist 패키지 설명 사이트](https://github.com/condemil/Gist#generating-access-token)에 있는 Installation에 따라 API 설정 및 token에 입력한다.
* 키 바인딩 기본설정은 사용하기 애매하니 { "keys": ["ctrl+0"], "command": "insert_gist_list" } 같은 간단한 걸로 바꾼다.

# 코드 블록?
* 코드 짜다 보면 **이 코드는 나중에 다른 프로젝트에도 쓸 일이 있겠다** 싶은 부분이 있다. 그것들을 Code Snippet이라 부른다.
* 코드 블록, 코드 조각, Code Snippet이라고도 한다.

# 어떻게 연동할까?
* Code Snippet 만들기
    * [Github Gist](https://gist.github.com/)에 Code Snippet을 보관할 수 있다.
    * 다른 사람들 Code Snippet도 구경할 수 있다.
    * 제목은 기능 이름으로 적당히 짓는다. 모르겠으면 다른 사람들 걸 참고한다.
    * 연동할 때 보이는 건 description 부분이다. 검색하기 편하게 Python:File Writing 이런 식으로 적으면 된다.
    * 연동할 때 편하기 쓰려면 public으로 등록한다.
* Gist 패키지 설치하기
    * Preferences - Pacakge Control - Install Package 로 이동 후 "Gist"라는 이름의 패키지를 설치한다.
        * Package Control이 없는 경우 Tools - Install Package Control로 먼저 이 기능을 활성화해야 한다.
* 연동하기
    * [Gist 패키지 설명 사이트](https://github.com/condemil/Gist#generating-access-token)의 설명을 따라가면 된다.
    * (Github 토큰)[https://github.com/settings/tokens] 페이지에서 토큰을 만든다. 이름은 Sublime Gist로 하고, Gist 항목만 체크한 다음 생성하면 된다.
    * 생성된 키를 복사한 뒤 Sublime Text에서 Preferences - Package Settings - Gist - Settings User로 이동한다.
    * 아래처럼 입력한다.
    {
    "token":"복사해둔 토큰값"
    }
* 키 설정하기
    * Preferences - Package Settings - Gist - Key Bindings User로 이동한다.
    * 아래처럼 입력한다.
    [
    { "keys": ["ctrl+0"], "command": "insert_gist_list" },
    ]
* 사용하기
    * 빈 파일을 열고 컨트롤 + 0을 누르면 깃헙에서 만들어 둔 코드 블록을 활용할 수 있다.

# 참고문헌
* [개발자 분들은 코드 블록을 어떻게 보관하시는지 궁금합니다.](https://kin.naver.com/qna/detail.nhn?d1id=1&dirId=104&docId=349836240&ref=me1lnk&scrollTo=answer2)
* [not-for-me/Gist를 이용한 소스관리.markdown](https://gist.github.com/not-for-me/9852928)
* [Sublime Text에 Gist 연동하기](https://www.youtube.com/watch?time_continue=196&v=3cdkYdzgXLc&feature=emb_title)
