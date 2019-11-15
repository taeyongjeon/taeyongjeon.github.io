---
title: 칸아카데미 - Complex Exponential Magnitude
date: 2019-11-15 21:09:09
tags:
categories:
- [4학기(2019-2), 전기자기학2]
mathjax: true
---
https://www.khanacademy.org/science/electrical-engineering/ee-circuit-analysis-topic/ee-ac-analysis/v/ee-complex-exponential-magnitude
https://www.khanacademy.org/science/electrical-engineering/ee-circuit-analysis-topic/ee-ac-analysis/v/ee-complex-exponentials-spin

1. 오일러 공식과 삼각함수
    1. $e^\theta = cos\theta + isin\theta$
        1. 기하학적으로 보면, 길이 1인 원에서 각도 $\theta$인 지점을 잡을 때 그 지점이 곧 $e^\theta$ 라는 것이다.
        &nbsp;
1. 코사인, 사인과 지수함수의 덧셈
    1. 개요
        1. $cos\omega t=\frac{1}{2}(e^{j\omega t}+e^{-j\omega t})$
        1. 위 식을 보면, 어떻게 지수 함수 2개를 더해서 삼각함수 형태를 만들 수 있는 거지...? 싶은 의문이 든다.
        1. 아래는 그 설명이다.
        &nbsp;
    1. 길이 1인 원을 생각하자.
        1. x축은 Real, y축은 Imaginary이다.
        1. 이때 한 점이 원운동을 하는데, 각도가 $\omega t$이다.
        1. 따라서, 시간 t에서 한 지점의 좌표는
        $(cos\omega t, sin\omega t)$이며,
        이는 우리가 알고 있는 $e^{\omega t}$ 와 같다.
            1. Q. 뭔 소리야? $e^{\omega t}=cos\omega t+isin\omega t$이긴 하지만 그게 어떻게 $(cos\omega t, sin\omega t)$라는 좌표라는 소리가 됨?
            A. 됨. 오일러 공식은 **"복소수를 복소평면 위의 하나의 점으로 볼 수 있다"** 라는 기하학적 의미를 복소수에게 부여함. 즉,  $e^{\omega t}=cos\omega t+isin\omega t$라는 식은, 어떤 복소수의 값인 동시에 평면의 한 좌표를 나타내기도 한다는 것임. 볼드체로 강조한 부분은 오일러도 눈
        1. ![](/images/전기자기학2/euler.png)
        그림으로 보자면 이렇다는 소리다.
        즉, 지수함수 $e^{j\omega t}$라는 녀석은 우리가 아는 지수함수의 형태가 아니라, 삼각함수처럼 돌고 도는 값이란 소리다. 즉, 코사인 = (삼각함수 형태로 변하는 값) + (삼각함수 형태로 변하는 값)이라는 소리다.
