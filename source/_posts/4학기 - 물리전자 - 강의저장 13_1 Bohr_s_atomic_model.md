---
title: 물리전자 - 강의저장 13_1 Bohr_s_atomic_model
date: 2019-12-07 12:19:10
tags:
categories:
- [4학기(2019-2), 물리전자]
mathjax: true
---

1. Bohr's Model for Hydrogen Atom
    1. ![](/images/물리전자/13_1_보어모델.jpg)
    1. 1번 식 - 모멘텀 구하기
        1. $P \cdot r$
        $\quad$ $\lambda= \frac hp$
        $\quad$ $2 \pi r=n \lambda$
        $=\frac{h}{\lambda} \frac{n \lambda}{2 \pi}$
        $=\frac{n h}{2 \pi}$
        $\quad$ $p=mv$
        $=m v r$ : 1번 식
    1. 2번 식 - 원심력과 인력
        1. ${Ze^2 \over 4 \pi sr^2}={mv^2 \over r}$
        1. $Z$ : 원자번호
1. Quantized Electron Energy
    1. Bohr's Model for Hydrogen Atom
        1. 반지름과 에너지 구하기
            1. 1, 2번식을 조합하면
            $r=\frac{h^{2} \varepsilon}{\pi m e^{2}} \frac{n^{2}}{Z}$
            1. $E=\frac{1}{2} m v^{2}-\frac{Z e^{2}}{4 \pi \varepsilon r}$ 로 구할 수 있으므로
            $E=-\frac{Z e^{2}}{8 \pi \varepsilon r}=-\frac{Z e^{2}}{8 \pi \varepsilon} \frac{1}{r}=-\frac{Z e^{2}}{8 \pi \varepsilon} \frac{\pi Z m e^{2}}{h^{2} \varepsilon n^{2}}$
            $=-\frac{R h c Z^{2}}{n^{2}}$
            $\quad$ $R=\frac{m e^{4}}{8 \varepsilon^{2} h^{3} c}$
        1. $E_{n}=-\frac{R h c Z^{2}}{n^{2}}$
        $=-\frac{2.180 \times 10^{-18} Z^{2}}{n^{2}}$ Joule
        $=-\frac{13.6 Z^{2}}{n^{2}} e V$
1. Hydrogen Atom
    1. Energy level of Hydrogen Atom
        1. ![](/images/물리전자/13_1_에너지_레벨.jpg)
        1. 노란색 부분은 Contimum of energy, 전자가 원자에 속하지 않는 상태의, 즉 자유 전자의 에너지 영역이다.
        1. -13.6$eV$는 Vacuum energy level 기준으로 맨 아래 부분의 에너지를 나타낸 것이다.
1. Quantized Electron Energy
    1. Spectrum of Hydrogen
        1. ![](/images/물리전자/13_1_스펙트럼.jpg)
        1. 전자가 높은 에너지에서 낮은 에너지로 떨어질 때 빛을 방출하며 그 파장은 위 그림의 식을 따른다.
        1. $\frac{1}{\lambda}=R\left(\frac{1}{n_{1}^{2}}-\frac{1}{n_{2}^{2}}\right)$
    1. Separating Lights
        1. ![](/images/물리전자/13_1_프리즘.jpg)
            1. 전구 : 모든 파장의 빛이 관측됨.
            1. 뜨거운 수소 기체 : 수소 기체가 갖고 있는 에너지 state의 색만이 관측됨.
            1. 차가운 수소 기체 : 모든 파장의 빛에서 수소 기체가 갖는 에너지 state만 뺏기고 나머지 파장의 빛이 관측됨.
    1. Radiative Transitions
        1. $\frac{h c}{\lambda}=E_{2}-E_{1}$
1. Orbital Angular Momentum
    1. What is the Orbital Angular Momentum?
        1. 전자는 L(orbital angular momentum)이라는 모멘텀을 갖는다.
            1. 쿨롱 힘에 의해 전자는 중심으로 당겨진다.
            $L=r \times p=r \times m v$
        1. $L=\hbar[\ell(\ell+1)]^{1 / 2}$
            1. $\ell$은 양자수. orbital angular quantum number라고 부르는 그 값이다.
            1. $\ell$ 값은 $n$값에 따라 정해진다.
            1. $\ell=0$일 때 $\theta, \phi$에 의존하지 않으며 오로지 r에만 의존하므로 구형의 형태를 갖는다.
    1. Magnetic Quantum Number
        1. ***교수님 질문 : 양자수 3개를 뭐라고 불렀는가?***
            1. 답변 : $n$ : principle quantum number, $\ell$ : orbital angular quantum number, $m_l$ : magnetic quantum number
        1. 전자가 원운동을 하면 전류가 흐르고, 전류가 흐르면 자기장이 생긴다(오른나사 법칙). 그리고 이 자기장을 양자화quantize시킨 형태가 Magnetic Quantum Number이다.
        1. ***교수님 질문 : Magnetic Quantum Number는 왜 생기는가?***
            1. 답변 : 각운동 때문에 생김.
        1. 모멘텀 $L_z$
            1. 전자가 위에서 $L$이라는 모멘텀을 가진다고 말했고, 당연히 $L_z$ 성분도 있을 것이다. 그 값은 $m_l$에 의해 정해진다.
            1. $L_{z}=m_{\ell} \hbar$
        1. 자기장과 모멘텀
            1. ![](/images/물리전자/13_1_모멘텀.jpg)
            1. 모멘텀 $L$은 자기장 $B_z$와 각도를 이루며,
            $L_z$ 방향이 자기장 방향임을 고려했을 때
            $L\cos \theta= \hbar{\sqrt{\ell(\ell+1)}} \cos \theta$
            $=L_{z}=m_{\ell} \hbar$
            $\quad$ 정리하면
            $\cos \theta=\frac{m_{l}}{\sqrt{\ell(\ell+1)}}$
            의 식을 얻는다.
        1. 정리
            1. $L$이라는 모멘텀이 있다.
            전자가 운동해서 자기장을 만들었고 이 자기장을 설명하고 싶다.
            이 자기장 방향 모멘텀이 $L$를 $z$방향으로 투영한 값 $L_z$임을 알게 되었다.
            그래서, $L_z$를 설명하기 위해 $L\cos \theta$보다 간단히 적는 $m_l$이 등장했다.
    1. Selection Rule
        1. 정의
            1. 어떤 양자수에서 에너지를 얻거나 잃어 다른 양자수로 이동할 때, 이동하는 값은 규칙에 의해 범위가 정해져 있으며 이를 Selection Rule이라고 한다.
                1. $h \nu=E_{2}-E_{1}$
                    1. 이 식을 쓸 일이 있는 경우 Selection Rule을 쓴다는 소리다.
            1. 플라즈마에만 적용되고(빛이 될 때) 충돌로 인한 이동에는 이 규칙이 적용되지 않는다.
        1. 규칙
            1. $\Delta \ell=\pm 1$
            $\Delta m_{\ell}=0, \pm 1$
        1. 예시
            1. $\psi_{100}$에 위치한 전자가 $h\nu=E_2 - E_1$만큼의 에너지를 받아 $n=2$의 에너지 state로 올라간다.
            1. Selection Rule을 따르기 때문에, 이 전자는 $\psi_{200}$으로 갈 수 없다. 이 경우 $\Delta \ell=0$이기 때문이다.
            $\psi_{21-1}$, $\psi_{210}$, $\psi_{211}$의 오비탈로만 갈 수 있다.
            1. 마찬가지로 $2s$ 오비탈은 $3s$ 오비탈로 올라갈 수 없다.
1. Electron Spin
    1. What is the Spin?
        1. 슈뢰딩거 방정식은 3개의 양자수만 쓴다. 즉, 스핀은 고려하지 않는다.
        1. 그런데 전자는 1개의 양자수를 더 갖는다. 그것이 스핀이다.
        1. 모멘텀 $S$와 양자수 $m_s$
            1. $S$ : 스핀
            $m_s$ : spin magnetic quantum number
            1. $S=\hbar\{s(s+1)\}^{1 / 2}$
            $\quad s=\frac{1}{2}$
            $S_{z}=m_{s} \hbar$
            $\quad m_{s}=\pm \frac{1}{2}$
1. Hydrogen Atom
    1. Electron Spin and Intrinsic Angular Momentums
        1. $I = $charge/period : $-e(\omega / 2 \pi)=-q \omega / 2 \pi,$ where $q=1.6 \times 10^{-19} \mathrm{C}$
        1. Magnetic Momentum $\mu$
            1. $\mu=I A$
            $=-\frac{e \omega}{2 \pi} \pi r^{2}$
            $=-\frac{e \omega r^{2}}{2}$
            $\quad$ $e=q$
            $\quad$ $L=p r=m v r=m \omega r^{2}$
            $\quad$ $L$은 Orbital angular momentum이다.
            $=-\frac{q L}{2 m}$
                1. $L$과 반대 방향의 모멘텀임을 알 수 있다.
1. Electron Spin
    1. Quantum Number
        1. ![](images/물리전자/13_1_양자수.jpg)
1. Total Angular Momentum
    1. What is the Total angular momentum?
        1. Total angular momentum은 $J$라고 표기한다.
        $J=L+S$이다. $L,S$는 각각 Orbital angular momentum, Spin angular momentum이다.
1. He Atom and Periodic table
    1. He Atom case
        1. 전자가 2개라서 쿨롱 힘과 각각의 반발력을 고려해서 퍼텐셜 에너지를 구할 수 있다.
        1. $V\left(r_{1}, r_{12}\right)=\frac{-2 e^{2}}{4 \pi \varepsilon_{0} r_{1}}+\frac{e^{2}}{4 \pi \varepsilon_{0} r_{12}}$
            1. 쿨롱 힘은 각각의 전자에 적용되기 때문에 2가 곱해졌다.
        1. 이렇게 구한 $V$값을 슈뢰딩거 방정식에 있는 $H\psi + V\psi = E\psi$에 넣으면 He의 에너지를 구할 수 있다.
    1. 에너지 역전
        1. 3d>4s
        4d>5s
        4f>5p
        와 같은 형태로 낮은 n값에서 더 높은 에너지를 갖는 경우가 있다.
    1. Pauli Exclusion Principle
        1. 어떤 전자도 같은 quantum number를 가질 수 없다.
