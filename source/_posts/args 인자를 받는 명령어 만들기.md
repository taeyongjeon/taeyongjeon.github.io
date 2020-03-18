---
title: args 인자를 받는 명령어 만들기
date: 2020-02-12 00:00
categories:
- [프로그래밍, Python]
mathjax: true
---

# 상황
youtube-dl로 mp3를 받아보려고 하는데 옵션이 너무 길어 alias로 줄이려고 했다.
그런데 필수 인자로 url이 있기 때문에 url을 인자로 넘겨주는 방법을 찾아야 했다.

# 해결
bash에서 인자를 받으려면 function을 써야 한다.
```bash
function hello() {
   echo "Hello $1!"
}
```

터미널 세션이 갱신되어야(=재부팅) 이 함수를 쓸 수 있지만, source 명령어를 통해 지금 세션에서 바뀐 설정을 적용시킬 수 있다.
```bash
source ~/.bashrc
hello abc
Hello abc! # 출력
```

# 참고문헌
[어떻게 alias에 인자를 넘겨주나요?](https://stackoverflow.com/questions/7131670/make-a-bash-alias-that-takes-a-parameter)
