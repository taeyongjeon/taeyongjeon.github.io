---
title: Hexo 블로그 수학식 플러그인 설치하기
date: 2019-12-07 00:47:16
tags:
categories:
- [블로그 관리]
---

1. cmd를 열고 ```npm install hexo-filter-mathjax``` 로 Hexo Filter MathJax 플러그인을 설치한다.
    1. [Hexo Filter MathJax 플러그인 페이지](https://github.com/stevenjoezhang/hexo-filter-mathjax)
1. ```hexo deploy```로 Github.io 서버를 업데이트한다.
1. post를 작성할 때 ```mathjax: true```를 추가한다.
    1. 예시
    ```
    ---
    title: Title
    categories: Physics
    date: 1984-01-24 16:00:00
    tags:
    mathjax: true
    ---
    ```
1. 이제 post에 수학식을 적용할 수 있다.
