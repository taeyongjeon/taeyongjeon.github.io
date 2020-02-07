---
title: 최적화 알고리즘 - SLSQP (scipy)
date: 2020-02-07 23:51:21
tags:
categories:
- [프로그래밍, Python]
mathjax: true
---

# 글 본론
## 1) 내가 처한 상황
좀 더 실질적인 상황 설명 : 지역1, 지역2, 지역3을 돌아야 하는데 재료1 50개, 재료2 70개, 재료3 80개가 필요하다. 각 지역 당 {재료1,재료2,재료3} 드랍 갯수를 정리하면 다음과 같다.
지역1 : {1,2,1}
지역2 : {2,1,3}
지역3 : {3,2,1}
각 지역을 몇번씩 돌아야 원하는 재료를 모두 파밍할 수 있을까?

## 2) 이렇게 구현합니다
$x_1+x_2+x_3$의 **최솟값** 을 구하고자 한다.

단, 다음 조건을 만족해야 한다.
$x_1 + 2x_2 + 3x_3 - 50 >= 0$
$2x_1 + x_2 + 2x_3 - 70 >= 0$
$3x_1 + 3x_2 + x_3 - 80 >= 0$

## 3) 파이선 코드입니다
```python
import numpy as np
from scipy.optimize import minimize
import math

objective = lambda x : x[0]+x[1]+x[2] # 최소값을 구하고자 하는 함수.
x0 = np.zeros(3)
x0 = [0,0,0] # 초기값
bounds = ((0,9999),(0,9999),(0,9999)) # SLSQP는 상한, 하한값을 지정해주어야 한다.
constraints_list = [] # 제약조건
# eq는 등호 조건, ineq는 부등호(>=) 조건이다.
constraints_list.append({'type': 'ineq', 'fun': lambda x:x[0]*1+x[1]*2+x[2]*3-50})
constraints_list.append({'type': 'ineq', 'fun': lambda x:x[0]*2+x[1]*1+x[2]*2-70})
constraints_list.append({'type': 'ineq', 'fun': lambda x:x[0]*3+x[1]*3+x[2]*1-80})
constraints = (constraints_list)

result = minimize(objective,x0,method='SLSQP',bounds=bounds,constraints=constraints).x

[print(int(round(element))) for element in result]
```


# 왜 이런 걸 찾게 되었나.
게임을 하다 이런 생각이 들었다. 지역마다 주는 보상이 다르고, 피로도 소모량도 다른데 원하는 재료를 최소 피로도 소모로 파밍할 수 있지 않을까? A, B, C 지역의 재료 보상이 겹치는 것도 있고 얻는 확률도 다르면, 원하는 물건을 얻기 위해 A는 몇번 B는 몇번 가야하느냐, 이런 문제였다.

나름대로 머리를 굴렸지만 생각 이상으로 쉽지 않다는 걸 알았다. 그러다 예전에 본 [영농플레이어들을 위한 자원탕진 플래너 "흙"을 소개합니다](https://gall.dcinside.com/board/view/?id=ogame&no=44533)라는 글이 생각났다. 이 글은 **엑셀의 해 찾기 기능** 을 쓰고 있었다.

내가 정확히 필요로 하던 정보였다.
**지금 가진 자원을 최대로 소모하는 방어시설 구매 종류와 수량 구하기**
**= 지금 가진 피로도를 최소로 소모하는 던전 종류와 횟수 구하기**
**= 지금 가진 자원을 최대/최소로 사용하여 정해둔 목표치를 맞추기**
이렇게 적을 수 있는 셈이다.

# GRG, Simplex Algorithm 그리고 SLSQP
## 1) GRG
이제 데이터베이스를 찾고 파이썬에서 구현하는 일만 남아있었다. 나는 후자부터 찾기로 했다. 엑셀은 **GRG Nonlinear 방식** 을 쓰고 있다고 적혀 있었고, 나는 GRG python, generalized reduced gradient in python 같은 검색어를 구글에 적어봤지만 바로 사용할 수 있는 건 없었다. 좀 더 정확히는 [Github에서 구하기는 했는데](https://github.com/ishank011/grgdescent)... 너무 어려웠다. 전공 책을 그대로 알고리즘으로 구현한 이 분에게 박수.

## 2) Simplex Algorithm
나는 다른 방법을 찾기로 했다. 기본적으로 이 기능은 몇 가지 부등식을 만족하는(**제약조건**) 함수의 값을 구하는 문제였다. [이 글](https://redtea.kr/pb/pb.php?id=qna&no=8742#78260)로부터 Simplex Algorithm이라는 부등식을 방정식으로 바꾸는 혁명적인 방법을 찾아냈다...만... 아래에서 설명할 SLSQP를 먼저 찾게 되었다.

## 3) 잠깐 딴소리
데이터 사이언스를 전문으로 하시는 어떤 분이 **라이브러리 임포트해서 변수 몇개 조작하고 결과 내는 사람들이 인공지능을 개발하고 있다** 고 했다. 예전에는 "아, 그래도 컴퓨터로 구현하려면 기술의 이론은 알아야지 ㅋㅋ"라고 생각했는데, 지금 와서는 잘 모르겠다. 스택 오버플로우 개발자 제프 앳우드는 자동차 기술자가 있는 건 다른 사람들이 자동차를 수리할 필요가 없게 만들기 위해서인 것처럼, 프로그래머가 있는 건 다른 사람들이 프로그래밍할 수고를 덜어주기 위해서라고 말했다. 어쩌면 일단 구현하고 나중에 리팩토링하는 것처럼 먼저 써보고 나중에 이론을 배우는 건 어떨까.(이론을 모르면 접근할 수 없는 low한 영역은 말고.)

## 4) SLSQP
Simplex Algorithm python을 검색해본 결과 만난 링크가 [여기](http://apmonitor.com/che263/index.php/Main/PythonOptimization)다. 소스 코드를 받아 수정했고 결과는 맨 위 본론 부분과 같다.

# 마치며
매 기능을 구현할 때마다 이렇게 고생할 것 같다. 그래도 깃헙 블로그에 이렇게 올릴 수 있어서 다행이다. 예전같았으면 코드를 에버노트에 그냥 복붙하고 말았겠지.
