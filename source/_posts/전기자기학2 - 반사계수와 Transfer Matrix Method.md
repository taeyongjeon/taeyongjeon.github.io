---
title: 전기자기학2 - 반사계수와 Transfer Matrix Method
date: 2019-11-24 23:38:03
tags:
categories:
- [4학기(2019-2), 전기자기학2]
mathjax: true
---

1. 동영상 링크
    1. 전기자기학2 폴더에 반사계수 관련 영상 3개를 다운로드받아놓았다.
    1. https://www.youtube.com/watch?v=XuSxmb9-viY
    https://www.youtube.com/watch?v=dE7Yi3u9cvI
    https://www.youtube.com/watch?v=BX_-1ei12sU
1. 개요
    1. 경계면이 3개인 경우(즉 임피던스 n3이 존재하는 경우)부터는 반사계수를 구하기 굉장히 까다로워진다.
    1. 왜냐? n1에서 투과된 걸 n2에서 n3 경계에서 반사한 다음 이걸 n1에 투과하고... 이런 걸 다 더해야 하기 때문이다.
    1. 그래서, 쉬운 방법을 쓰기로 했다. 바로 Transfer Matrix Method이다.
1. 방법
    1. Transmission Matrix
        1. Transfer Matrix Method는 각 경계면을 독립된 계로 본다. n1과 n2의 경계에는 n3를 배제한다(이래도 풀 수 있다).
        1. 그리고 n1, n2 사이의 입사-투과파의 관계를 행렬로 나타낸다. 이를 Transmission Matrix라 한다.
        1. 행렬 D로 나타낸다.
    1. Propagation Matrix
        1. n2에는 두 가지 다른 파를 가정할 수 있다. n2의 왼쪽(n1) 경계와 오른쪽(n3) 경계이다.
        1. 이들 두 개의 관계를 행렬로 나타낸다. 이를 Propagation Matrix라 한다.
        1. 행렬 P로 나타낸다.
    1. 행렬 곱의 연쇄
        1. ![](/images/전기자기학2/행렬곱_연쇄.jpg)
        1. 위 그림과 같이 행렬이 싹 사라지고, 오로지 시작점과 끝점의 값만이 남는다.
    1. Transfer Matrix
        1. 위 그림에서, D와 P의 곱들을 묶어서 M이라 칭하는데, 이를 Transfer Matrix라 한다.
1. Transmission Matrix 구하기
    1. 경계면이 있고 그 왼쪽에 $E_0$, 오른쪽에 $E_1$이 있다고 하자.
    그리고 왼쪽으로 향하면 위첨자 $l$, 오른쪽으로 향하면 위첨자 $r$이 붙었다고 하자.
        1. ![](/images/전기자기학2/경계면.jpg)
    1. 그러면 다음 관계식을 얻는다.
    $E_1^r = t_{01}E_0^r+r_{10}E_1^l$
    $E_0^l=r_{01}E_0^r+t_{10}E_1^l$
    $\quad t_{01}t_{10}-r_{01}r_{10}=1$이다.
        1. 위 식을 정리하면 다음 행렬을 얻는다.
        $\begin{bmatrix}  E_0^r \\  E_0^l  \end{bmatrix}$
        $=\frac{1}{t_{01}}\left[\begin{array}{cc}{1} & {r_{01}} \\ {r_{01}} & {1}\end{array}\right]\left[\begin{array}{c}{E_{1}^{r}} \\ {E_{1}^{\prime}}\end{array}\right]$
        $=D_{01}\left[\begin{array}{c}{E_{1}^{r}} \\ {E_{1}^{\prime}}\end{array}\right]$
1. Propagation Matrix
    1. 동일한 임피던스가 있는 구간이 있다. 길이는 $L_1$이라 하고, 구간 왼쪽을 A사이드, 오른쪽을 B사이드라 하자.
    그리고 왼쪽으로 향하면 위첨자 $l$, 오른쪽으로 향하면 위첨자 $r$이 붙었다고 하자.
        1. ![](/images/전기자기학2/동일_임피던스_구간.jpg)
    1. 다음 관계식을 얻는다.
    오른쪽 파의 경우 다음과 같다.
    $E_B^r(x)=E_A^r(x+L_1)$
    $=E_0e^{j(\omega t-k(x+L_1))}$
    $\quad$ 갑자기 $E_0$라던가 다른 건 뭔가, 신경쓰지 않아도 된다. 그냥 평범한 평면파 식 하나를 가정했다.
    $=E_0e^{j(\omega t-kx)}e^{-jk_1L_1}$
    $=E_A^r(x)e^{-jk_1L_1}$
    왼쪽 파의 경우 다음과 같다.
    $E_A^l=E_B^le^{-jk_1L_1}$    
    1. 위 식을 정리하면 다음 행렬을 얻는다.
    $\begin{bmatrix} E_{ A }^{ r } \\ E_{ A }^{ l } \end{bmatrix}$
    $=\begin{bmatrix} e^{ +jk_{ 1 }L_{ 1 } } & 0 \\ 0 & e^{ -jk_{ 1 }L_{ 1 } } \end{bmatrix}\begin{bmatrix} E_{ B }^{ r } \\ E_{ B }^{ l } \end{bmatrix}$
    $=P_1\begin{bmatrix} E_{ B }^{ r } \\ E_{ B }^{ l } \end{bmatrix}$
