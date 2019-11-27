---
title: 물리전자 - 강의저장 11_1 Wave_equation
date: 2019-11-15 21:37:20
tags:
categories:
- [4학기(2019-2), 물리전자]
mathjax: true
---
1. Electron as a Wave
    1. Double Slit Experiment
        1. 그림
        ![](/images/물리전자/이중슬릿.png)
        1. 더블 슬릿을 통해서 파일때만 간섭이 생길 수 있는 형태를 얻을 수 있었다.
    1. 이를 통해..
        1. $p=\frac{h}{\lambda}$
            1. 입자로써 모멘텀을, 파동으로써 파장을 가진다는 것을 알게 됨.
            1. 그리고 이런 성격은 원자와 같은 작은 곳에서만 일어난다.
    1. De Brogile Relationship
        1. 그림
        ![](/images/물리전자/드브로이.png)
        1. 더블 슬릿을 만들었을 때 판에서 얻은 것은 밝고, 어두운 띠였다.
        1. 밝은 곳은 constructive interference, 어두운 곳은 destructive interference가 일어났다.
        1. 드브로이라는 사람이 모멘텀과 파장을 관련시켰다.
    1. Derivation(유도) of De Brogile Relationship
        1. 유도를 위한 준비물
            1. $E=h\nu$
                1. v는 '브이'가 아니라 '누'라고 읽는다. 그리스 문자 f임. 즉, **주파수** 다.
            1. $E=mC^2$
        1. 유도
            1. $\nu=\frac c\lambda$
            두 개의 $E$ 식을 합치면
            $\frac h\lambda = mC$
            즉 $\lambda = \frac{h}{mC}=\frac hp$
        1. 결론
            1. 드브로이라는 사람은 질량 m, 속도 C를 가지는 입자는 파장을 가지는데
            그 파장 $lambda$가
            $\frac{h}{mC}$, 즉 $\frac hp$라고 했다.
        1. 의의
            1. 모멘텀과 파장을 관련시켰다.
                1. 질량이 없는 빛이, 어떻게 모멘텀을 가지는지를 설명할 수 있게 했다(파장을 통해 가짐)
                1. 질량을 갖는 전자가, 어떻게 파장을 가지는지를 설명할 수 있게 했다(모멘텀과 파장의 관계)
            1. atomic scale에서는 입자가 파동의 성질도 가진다는 것을 알아냈다.
            1. 파장이란?
                1. $\lambda=\frac{C}{f}=\frac{C}{\nu}$
                    1. C : 빛의 속도
                    f : 주파수
            1. 모멘텀이란?
                1. 뉴턴역학에서 $P=mv$
                1. 양자역학에서 $P$
                $=\frac{h}{\lambda}$
                $=\frac{h}{2\pi}\frac{2\pi}{\lambda}$
                $=\hbar k$
                    1. $\hbar = \frac h{2\pi}$
                    1. $k=\frac{2\pi}{\lambda}$
                1. $P=\frac{h}{\lambda}$
    1. De Brogile Relationship 계속
        1. 골프 공과 광자의 드브로이 관계
            1. 50g, 20m/s의 골프 공과 2200m/s의 광자가 있다.
            1. $\lambda=\mathrm{h} / \mathrm{mv}$
            $\mathrm{h}=6.63 \times 10^{-34} \mathrm{Js}$
            1. 골프 공은 파동wave의 성질을 가질 수 없다.
                1. $\lambda=6.63 \times 10^{-34} \mathrm{m}$
                wave의 성질을 갖기엔 파장의 값이 너무 작다.
            1. 광자는 wave의 성질을 가진다.
                1. $\lambda=0.18 \mathrm{nm}$
                wave의 성질을 가질 만큼 파장의 값이 충분히 크다.
            1. 그래서, 우리가 보는 물체들은 드브로이 관계를 적용할 수 없다.
            &nbsp;
            &nbsp;
            &nbsp;
1. Time-Independent Schrödinger Equation
    1. 슈뢰딩거 방정식이 뭐임?
        1. 파동방정식임. 근데, **불확정성의 원리** 에 따라, 어떤 입자의 위치(=파동방정식의 함숫값)은 의미가 없기 때문에, 파동방정식 그 자체는 안 쓰고 그 **제곱 값** 을 확률로 다루어 입자가 있을 확률을 파악하는 데 쓴다.
        1. 전자는 wave야 : 드브로이
            1. $P=\frac h\lambda$
        1. 슈뢰딩거의 방정식은 파동 형태의 움직임을 설명함.
            1. 퍼텐셜 에너지와
            1. 경계 조건Boundary conditions을 알려주면
            이 식을 도출해낼 수 있다.
        1. 즉, 양자역학의 기본이 되는 식이다.
    1. 슈뢰딩거 방정식의 성질?
        1. 뉴턴역학에서 $F=ma$
        1. 슈뢰딩거 방정식은 작은 소자(atomic scale)에서 전자의 움직임을 예측할 수 있다. 전류가 어떻고, 장치가 어떻게 작동하고 같은 걸 알 수 있다.
        1. 즉 슈뢰딩거 방정식을 통해 반도체의 작동 원리를 이해할 수 있다.
    1. 파동방정식Wave Function
        1. 개요
            1. 말은 Wave Function이지만 x, y, z에 대해서 해석하는 건 옳지 않다. 그 이유는 하이젠베르그의 불확정성 원리 때문이다.
            1. Wave Function은 $\psi(x,t)$라고 적으며, 이는 입자의 속성을 설명한다.
                1. 너무도 당연히, 매개변수 t가 있으므로 시간도 다루는 함수지만, 식을 간단히 다루기 위해 시간 독립Time-Independent로 계산하는 것이다.
            1. 파동방정식은 물질의 확률 분포를 설명한다.
                1. 즉, 시간에 따른 wave의 위치같은 '전자기학에서 배우는 파동방정식'과는 무관하지만, 그냥 예전부터 그렇게 불러왔기 때문에(due to historical reason) Wave Function이라고 부른다.
            1. 실제로 쓰는 값은 $|\psi(x,t)|^2$이다.
                1. 이 값은 입자가 특정 영역, 특정 시간에서 발견될 수 있는 확률을 의미한다.
                    1. 그러니까, 위치가 나오는 게 아니라 0과 1 사이의 값(확률)이 나온다는 거다.
        1. 개념
            1. $\Psi(x, t)=E_{0}(x) e^{k x-\omega t}$
                1. 반복하지만, 이 식 자체로는 써먹을 데가 없다.
            1. 그림
            ![](/images/물리전자/파동방정식.png)
                1. $|\Psi|^2$이 큰 부분은 입자가 있을 가능성이 높다. 그 반대는 작다.
                &nbsp;
                &nbsp;
1. Wave Function
    1. 오비탈의 형태
        1. 그림
        ![](/images/물리전자/오비탈.png)
            1. 어떻게 저런 모양의 오비탈을 생각해냈는가?
            1. 사실, 생각해낸 게 아니라 계산한 거다.
            $|\Psi|$ 파동방정식을 구하고,
            $|\Psi|^2$를 구하고,
            $|\Psi|^2$를 x 값(위치)에 따라 점을 찍어서 저런 영역이 나온 거다.
            1. 저 형태는, 저 영역에서 전자가 돌고 있을 확률이 매우 높다는 뜻이지, 저기서 이런 식으로 돌고 이런 궤도로 돌고 이런 소리는 절대 할 수 없다.
    1. $\Psi$ 파동방정식 구하기
        1. $\Psi(x,t)$는 입자의 운동 상태, 경계조건에 따라 달라진다.
    1. Schrödinger Equation
        1. 뉴턴역학의 에너지
            1. $E(total)$
            $=E(kinetic)+E(potential)$
            $=\frac 12 mv^2+V$
            $={p^2 \over 2m}+V$
            (p는 모멘텀)
        1. 양자역학의 에너지
            1. 해밀턴이라는 사람이 Hamiltonian이라는 연산자를 만들었다.
                1. 라플라시안 같은 거다.
            1. 해밀터니안은 KE와 PE와 관련된 연산자를 포함한다.
            1. 이게 슈뢰딩거 방정식과 관련이 있다.
        1. 방정식의 유도
            1. 시간 독립 슈뢰딩거 방정식에서
            $\mathrm{H}_{\mathrm{op}} \psi=\mathrm{E} \psi$
            (해밀터니안 = $H_op =-\frac{\hbar^{2}}{2 m} \nabla^{2}+V$)
            $E=\frac{p^{2}}{2m}+V$
            위 식을 넣고, 시간에 관한 식을 추가한다.
            $E \Psi(x)=-\frac{\hbar^{2}}{2 m} \frac{d^{2} \Psi(x)}{d x^{2}}+V \Psi(x)$
            정리한다.
            $E \psi=-\frac{h^{2}}{8 \pi^{2} m} \frac{d^{2} \psi}{d x^{2}}+V \psi$
                1. 이때, 마지막 식에서 $\hbar$가 $h$로 변하며 분모에 $4\pi^2$이 추가되었다.
                1. h는 플랑크 상수.
                1. 근데, 식을 유심히 보면, 왜 V는 멀쩡하고 모멘텀 관련 식만 해밀턴 연산자가 들어간다.
1. Schrödinger Wave Equation
    1. 유도
    $E$
    $=p^{2} / 2 m+V$
    $=\frac{\hbar^{2} k^{2}}{2 m}+V$
    위 식을 기억해두자.
    $\Psi(x)=\operatorname{asin} k x+\operatorname{bcos} k x$
    한 번 미분한다.
    $\frac{d \Psi(x)}{d x}$
    $=\frac{d}{d x}(\operatorname{asin} k x+\text { bcos } k x)$
    $=k(\operatorname{acos} k x-b \sin k x)$
    한 번 더 미분한다.
    $\frac{d^{2} \Psi(x)}{d x^{2}}$
    $=k \frac{d}{d x}(\operatorname{acos} k x-b \sin k x)$
    $=-k^{2}(\operatorname{asin} k x+b \cos k x)$
    $=-k^{2} \Psi(x)$
    $-\frac{\hbar^{2}}{2 m}$를 곱한다
    $-\frac{\hbar^{2}}{2 m} \frac{d^{2} \Psi(x)}{d x^{2}}$
    $=\frac{\hbar^{2} k^{2}}{2 m} \Psi(x)$
    $=(E-V) \Psi(x)$
    (맨 위에 E와 V에 관한 식이 있다.)
    $-\frac{\hbar^{2}}{2 m} \frac{d^{2} \Psi(x)}{d x^{2}}+V \Psi(x)=E \Psi(x)$
    슈뢰딩거 방정식 완성.
    1. ***교수님 : 시험에 나온다. 교수님은 슈뢰딩거 방정식을 조립assemble했다는 말을 굉장히 좋아하신다. 유도라는 말 대신 조립이라는 말을 쓰도록 하자.***
1. Infinite Potential Well
    1. 그래서, 슈뢰딩거 방정식을 어떻게 해석하느냐? Infinite Potential Well을 가지고 해석한다.
    1. 그림
    ![](/images/물리전자/구속전자.png)
        1. 전자가 퍼텐셜 에너지가 무한인 경계 사이에 갖혀 있다.
        1. 전자는 경계를 넘어갈 수 없기에, 그 안에서만 움직이게 된다.
        1. 위와 같은 그림을 1D potential box라고 부른다. : 양면에 무한한 퍼텐셜 에너지가 있는 상자
            1. 1차원 quantum well이라고도 부른다.
        1. 상자 안에서의 V는 0이다.
    1. 식 풀기
        1. $-\frac{h^{2}}{8 \pi^{2} m} \frac{d^{2} \psi}{d x^{2}}+0 \psi=E \psi$
        상자 안에서의 V=0이므로 0을 대입했다.
        1. 파동방정식은 코사인 함수가 아니다.
        $\frac{d^{2} \psi}{d x^{2}}=-k^{2} \psi, \quad k^{2}=\frac{8 \pi^{2} m E}{h^{2}}$
        이때, 파동방정식을 삼각함수이다.
        **좀 더 정확히는, 파동함수는 코사인 또는 사인 또는 코사인과 사인의 합성으로 이루어져야 한다. 그렇지 않으면 '파동'함수가 아니기 때문이다. 즉 cos 아니면 sin이다.**
        $\Psi=B \cos (k x)$이라고 두자.
        그러나 경계 조건으로부터 $x=0$일 때 $\Phi=0$, $x=L$일 때 $\Phi=0$이므로
        코사인 함수는 이를 만족하지 않는다.
        1. 파동방정식은 사인 함수다.
        그래서 파동함수는 sin함수여야 한다.
        $\Psi(x)=A \sin (k x)$
        위 식은 경계면 조건 $\Psi(x=0)=\Psi(x=L)=0$을 만족한다고 가정하자.
        $\Psi(x=0)=0$이다.
    1. Quantization of Energy Levels
        1. 경계면 조건 계속
        $\Psi(x=L)=0$이어야 하므로,
        $A \sin (k L)=0$이다.
        즉, $\mathrm{kL}=\mathrm{n} \pi$이다.
        $\mathrm{kL}=\mathrm{n} \pi$로부터,
        $E=\frac{h^{2} k^{2}}{8 \pi^{2} m}=\frac{h^{2} n^{2}}{8 m L^{2}}$
        이로부터 에너지 준위Energy Levels를 구할 수 있다.
        1. 에너지 준위
        ![](/images/물리전자/에너지_준위.png)
            1. 위 식에 따라, 4E와 9E 사이에는 에너지가 존재할 수 없음을 알 수 있다.
        1. n
            1. $k=n\pi L$에서, n을 **양자수Quantum Number** 라고 부른다.
            1. k에 대한 파장의 식으로부터 파장도 구할 수 있다.
            $\mathrm{K}_{1}=2 \pi / \lambda=\pi / \mathrm{L}, \therefore \lambda=2 \mathrm{L}$ : 반파장 운동
            $\mathrm{K}_{2}=2 \pi / \lambda=2 \pi / \mathrm{L}, \therefore \lambda=\mathrm{L}$
            1. 그림과 해석
                1. ![](/images/물리전자/파장과_에너지.png)
                1. 에너지는 연속적이지 않다. discrete하다.
                1. 에너지는 양자수의 제곱값만큼 증가한다.
                1. 낮은 level에서 운동하는 원자의 파장은 길다. level이 높을수록 짧은 파장의 운동을 한다.
        1. 확률
        $\Psi(x)=\sqrt{2 \over L} \sin \sqrt{n \pi x \over L}$
        $\int_{x=0}^{x=L}\left\lfloor\Psi(x)^{2}\right\rfloor d x=1$
        1. 결론
            1. 입자는 discrete한 에너지를 갖는다.
            1. 에너지가 높아질 수록 짧은 파장 운동을 한다.
            1. 이런 입자의 움직임은 전자의 움직임과 유사하다.
            1. 현실 세계에서 이런 현상을 써먹는가?
                1. 그렇다. Quantum Well, Quantum Wire, Quantum dots라고 해서 나노 기술 쪽에서 써먹는다.

## 이번 강의 전부 필기 끝.
