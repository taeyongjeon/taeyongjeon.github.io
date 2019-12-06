---
title: Hexo 블로그 처음부터 만들기
date: 2019-12-07 00:45:30
tags:
categories:
- [블로그 관리]
---

1. 설치
    1. Git 설치
        1. https://git-scm.com/ 에서 깃 설치
        1. 바탕화면 마우스 우클릭 - Git Bash Here 실행
            1. ```git --version ``` 입력하여 버전이 뜨면 설치 성공.
    1. Node.js 및 NPM 설치
        1. Hexo는 Node.js기반의 정적 사이트 생성 라이브러리이기 때문에
        Hexo를 사용하기 위해서는 Node.js설치가 필요하다.
        또한 NPM은 자바스크립트의 패키지 관리도구로 Hexo설치시에 필요하다.
        1. https://nodejs.org/ko/ 로 이동하여 다운로드
        1. 설치 후 ``` node -v ``` 입력하여 설치가 성공했는지 확인
    1. Git 설정
        1. Git Bash 실행 후
        ```
        git config --global user.name 계정명
        git config --global user.email 사용자 이메일
        ```
        위 코드를 입력
    1. Hexo 설치
        1. CMD 실행
        1. ``` npm install -g hexo-cli ```를 입력하여 설치
            1. hexo-cli 라는 모듈을 어디서든 사용 가능하게(-g) 설치
    1. 페이지 관리 디렉터리 생성
        1. 블로그 폴더를 만들 경로로 이동
        1. 해당 폴더에서 CMD 실행
        1. ``` hexo init 디렉토리명 ``` 으로 블로그 디렉터리 생성
        1. ``` cd 디렉토리명 ``` 입력으로 으로 디렉터리 이동
        1. ``` npm install ``` 입력으로 블로그에 필요한 모듈 설치  
    1. Github 레포지토리 생성
        1. Github 로그인
        1. New Repository로 계정이름.github.io이라는 이름의 레포지토리 생성.
            1. 예)username.github.io
    1. Hexo 블로그 Github 연동
        1. 블로그 디렉터리의 \_config.yml 파일을 연 뒤
        ```
        # Deployment
        ## Docs: https://hexo.io/docs/deployment.html
        deploy:
        type: git
        repo: https://github.com/계정이름/계정이름.github.io.git
        ```
        위 형식의 구조를 찾아 위 코드와 같이 수정한다.
        2. 해당 경로에서 CMD를 연다.
        3. ```npm install hexo-deployer-git --save```를 입력하면 github.io와 연동된다.
1. Hexo 사용법
    1. 블로그 포스트 생성하기
        1. 디렉터리 경로에서 CMD 실행
        1. ```hexo new post 포스터명``` 입력.
    1. Hexo 빌드
        1. md 파일을 브라우저로 보여주기 위해 html로 변환하는 작업이다.
        1. 디렉터리 경로에서 CMD 실행
        1. ```hexo generate ``` 또는 ```hexo g``` 입력.
        1. public 디렉터리가 생성되고 그 안에 실제 블로그 페이지 구조가 변환되어 만들어진다.
    1. 로컬에서 확인하기
        1. 디렉터리 경로에서 CMD 실행
        1. ```hexo server``` 입력으로 서버를 연다.
        1. https://localhost:4000으로 접속하여 확인한다.
        1. 보통 깃허브 호스팅 전 테스트용으로 사용한다.
    1. Github에 업로드(호스팅하기)
        1. 디렉터리 경로에서 CMD 실행
        1. ```hexo deploy``` 또는 ```hexo d``` 입력
        1. \_config.yml 파일에서 설정한 Github.io 경로로 블로그 파일들이 업로드된다.
        1. https://계정명.github.io로 접속하여 확인할 수 있다.
