---
title: 가상환경 venv 사용법
date: 2020-02-07 23:51:25
tags:
categories:
- [프로그래밍, Python]
---

# 설치
```bash
pip3 install virtualenv
```

# 새로운 가상환경 만들기
```bash
virtualenv folder_name
```

# 가상환경으로 들어가기
```bash
source folder_name/bin/activate
git clone git@github.com:nodejs/node.git # 기존 프로젝트를 가져온다.
pip3 install -r requirements.txt # 보통 프로젝트에 함께 들어있는 실행환경을 설치한다.
pip3 install ...
```

# 가상환경에서 나가기
```bash
deactivate
```
