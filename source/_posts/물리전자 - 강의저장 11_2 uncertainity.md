---
title: 물리전자 - 강의저장 11_2 uncertainity
date: 2019-11-18 23:31:47
tags:
categories:
- [4학기(2019-2), 물리전자]
mathjax: true
---

1. Infinite Potential Well
    1. Summary of Cpmfomed Electron
        1. Potential Well에 전자를 넣으면 이런 특성이 생긴다.
        1. 전자는 벽을 넘을 수 없기 때문에, 이 안에서 운동한다.
        1. 퍼텐셜 에너지=0이므로 운동 에너지만 갖고, 운동 에너지는 연속적이지 않다. discrete하다.
        1. 에너지 값은 $n^2$을 따른다.
        1. 에너지가 높을수록 짧은 파장 운동을 한다.
    1. Heisenberg's Uncertainty Principle
        1. 개요
            1. 질문 : 왜 $\Psi$의 값은 의미가 없는가?
            답변 : 불확정성 원리 때문이다.
            여기서는 불확정성 원리가 어떻게 이런 결론을 내는 지 배운다.
        1. 파동의 간섭
            1. ![](/images/물리전자/간섭.jpg)
                1. Fringe는 줄무늬라는 뜻
                1. 두 광자 1, 2가 있다.
                    1. 밝은 줄무늬 : 1, 2가 평행하게, 그리고 정수배의 파장 $\lambda$로 만난다.
                    1. 어두운 줄무늬 : 1,2가 평행하게, 그리고 정수배의 반파장 $\frac \lambda 2$로 만난다.
                        1. 꼭 $\frac 12$일 필요는 없다. 이 값에 가까워질 수록 어두워질 뿐이다.
1. Heisenberg's Uncertainty Principle        
    1. 하이젠베르그의 슬릿
        1. ![](/images/물리전자/하이젠베르그_간섭.jpg)
            1. 모멘텀 p, 슬릿의 간격 a, 파동이 나아가는 방향각 $\theta$, 그리고 y 방향 모멘텀 성분인 $\triangle p$
            1. $sin\theta = \frac{\triangle p}{p_x}$
            $\quad\quad\quad$영의 이중 슬릿 실험에서 아래와 같은 식을 도출한 적이 있다.
            $dsin\theta = \lambda$
            $\quad\quad\quad sin\theta=tan\theta$ ($\theta$가 작은 값)
            $tan\theta=\frac{\lambda}{a}$
            $\quad\quad\quad tan\theta = \frac{\Delta p_{y}}{p_{x}}$ (위 그림)
            $\quad\quad\quad p_x=\frac{h}{\lambda}$ (드브로이 정리)
            $\quad\quad\quad \Delta y=a$ (위 그림)
            $\frac{\Delta p_{y}}{p_{x}}=\Delta p_{y} \cdot \frac{\lambda}{h}=\frac{\lambda}{a}=\frac{\lambda}{\Delta y}$
            $\Delta y \cdot \Delta p_{y}=h$
            식 완성!
            1. 그래서, 이 식이 뭔데?
                1. $\Delta y \cdot \Delta p_{y}=h$
                1. y 방향 쪽의 변위 y와 y 방향 쪽의 모멘텀 p의 곱은 언제나 플랑크 상수 h만큼을 가지고 있다.
            1. 물리적으로 나타나는 현상
                1. **변위를 좁히면 모멘텀이 크게, 변위를 키우면 모멘텀이 작게 나타난다.**
                이게 하이젠베르그의 불확정성 원리에 대한 설명이다.
                1. ![](/images/물리전자/변위와_모멘텀.jpg)
                    1. $\Delta y$가 슬릿의 길이 a이다.
                    1. $\Delta p_y$가 y방향 모멘텀이다.
    1. Localized Wave
        1. Localized Wave의 경우 불확정성 정리의 우항이 $\frac 12$가 된다.
        1. 파수는 다음과 같다.
        $\mathrm{K}=\frac{2 \pi}{\lambda}$
        $\quad \quad \quad \lambda=\frac{h}{p_{x}}$
        $=\frac{2 \pi}{h} p_{x}$
        $\Delta k=\frac{2 \pi}{h} \Delta p_{x}$
        1. 이로부터
        $\Delta x \cdot \Delta k=\frac{1}{2}$
        $\quad \quad \quad$ 푸리에 변환 때문에 이런 값이 생기는 거니까, 일단 받아들일 것.
        $\Delta x \frac{2 \pi}{h} \Delta p_{x}=\frac{1}{2}$
        $\Delta x \cdot \Delta p_{x} \approx \frac{h}{4 \pi} \approx \frac{\hbar}{2}$
        1. 우항이 1인 경우
    1. Gaussian Wave
        1. 파수는 $\Delta k=\frac{2 \pi}{h} \Delta p_{x}$이다.
        1. 이로부터
        $\Delta x \cdot \Delta k=1$
        $\Delta x \frac{2 \pi}{h} \Delta p_{x}=1$
        $\Delta x \cdot \Delta p_{x} \approx \frac{h}{2 \pi} \approx \hbar$
    1. Waves
        1. 파동에는 $delta$, 삼각함수형태, top hat=Localized Wave, Gaussian 등의 다양한 종류가 있다.
    1. 에너지와 시간 관계
        1. $\Delta t \cdot \Delta E \approx \hbar$
            1. 계산
            $\Delta x \cdot \Delta p_{x} \approx \hbar$
            $\quad \quad \quad$ 운동에너지 형태를 만들어주기 위해 모멘텀에 v를 곱해주고 나눠준다.
            $\frac{\Delta x}{v} \cdot v \Delta p_{x} \approx \hbar$
            $\frac{\Delta x}{v} \cdot \Delta E \approx \hbar$
            $\quad \quad \quad \quad v=\frac{\Delta x}{\Delta t}$
            $\Delta t \cdot \Delta E \approx \hbar$
        1. 의미
            1. 시간을 정교하게 말하고자 한다면 에너지의 오차가 커지고,
            에너지를 정확하게 말하고자 한다면 시간의 오차가 커진다.
1. Infinite Potential Well 계속
    1. Heisenberg's Uncertainty Principle
        1. 개념
            1. 입자의 위치(x값)와 모멘텀(p값)을 동시에, 정확하게 아는 것은 불가능하다.
                1. ![](/images/물리전자/불확정성.jpg)
            1. $\Delta x \cdot \Delta p \geq \frac{h}{2\pi} \geq \hbar$
            $\Delta t \cdot \Delta E \geq \frac{h}{2\pi} \geq \hbar$
        1. 이게 어디 쓰이는데?
            1. 우리는 원자 입자의 궤도trajectory에 대해서 이야기를 할 수 없다.
            1. 입자는 확률적 상태probabilistic state로 존재한다.
                1. 입자는 여러 위치 후보값 중 하나를 가질 것이다.
                1. 입자는 여러 모멘텀 후보값 중 하나를 가질 것이다.
                1. Probability Cloud
                ![](/images/물리전자/확률_구름.jpg)
            1. 그래서, 양자 세계에서 사람들은 더 이상 입자의 움직임(위치와 모멘텀)을 파악하는 걸 포기하고, 확률로 이야기하게 되었음.
        1. 예제
            1. 전자의 위치가 $\Delta x=10^{-9} \mathrm{m}$의 정확성을 갖는다. 이 때 고려할 수 있는 가장 정확한 속도값은?
            1. 계산
                1. $\Delta x \cdot \Delta p \geq \frac{h}{2\pi}$
                $\Delta v \geq 1.16 \times 10^{5} \mathrm{m} / \mathrm{s}$
        1. 물리적인 의미
            1. 물리적으로, 위치와 모멘텀의 곱은 모든 확률의 합과 같다.
            1. ![](/images/물리전자/불확정성_2.jpg)
                1. 우리는 입자의 존재를 확률로 다루어야 한다고 결론지었다.
                1. 그럼, 어떤 영역(위 그림에서는 Box)에서 입자들의 존재 확률은 (각 위치의 확률)의 총합일 것이다.
                1. 위 그림에서, $\Delta p$와 $\Delta x$가 있다.
                1. 여기서 $\Delta x$는 확률함수의 파형을 모두 합한 형태다.
                1. 그런데, 각각의 에너지 준위에서 존재확률이 다를 것이므로, 그것까지 고려하기 위해 $\Delta p$도 곱한다.
                1. 그래서 p와 x의 곱인 것이다.
            &nbsp;
1. Tunneling Phenomenon
    1. 개요
        1. 수조 두 개를 세워놓고 한 쪽만 물을 적당히 채웠다. 이러면 빈 수조로 물이 흘러갈리가 없다.
        1. 그런데, 절연체로 완전히 막아둔 두 개의 공간에서 하나만 전자로 채우면, 시간이 지난 뒤 다른 곳에도 전자가 존재하는 이상한 현상이 일어난다.
        1. 이를 Tunneling이라 한다.
    1. 고전역학과 양자역학의 Barrier
        1. 고전역학에서 Barrier에 의해 막혀 튕겨나가는 것을 reflect라고 한다.
        1. 양자역학에선 입자 하나를 다루지 않고 파동wave을 다루기 때문에, 벽을 향해 파동이 움직인다고 가정한다. Barrier에 wave가 부딛히면 일부는 reflect되고, 일부는 통과한다(터널링).
    1. Quantum Leak
        1. ![](/images/물리전자/터널링.jpg)
            1. Barrier를 통과할 때 wave가 나타나지 않는다.
    1. Potential Barrier Penetration
        1. 파동함수는 고전적인 운동의 한계를 넘어 potential barrier penetration이라는 현상을 일으킨다.
        1. Finite Potential Well에서(즉 V가 무한이 아님) 파동함수는 Well을 빠져나갈 수 있음.
    1. What is the Quantum Tunneling?
        1. ![](/images/물리전자/양자_터널링.jpg)
            1. 파동함수 $\Psi_1$이 barrier를 만나면 일부는 reflect되고 남은 값은 Tunneling을 통해 $\Psi_3$으로 존재하게 된다.
            1. 얼마나 터널링되느냐? 이는 Potential Barrier의 width(그림에서 길이 a)와 Potential energy에 따라서 결정된다.
        1. potential barrier width(=a)가 좁을 경우
            1. 입자는 barrier을 penetrate할 수 있다.
            그리고 다른 영역으로 나올 수 있다. 이 현상을 quantum tunneling이라 한다.
    1. Electron Density in Potential Step
        1. ![](/images/물리전자/지수적_감소.jpg)
            1. 영역 2에서 전자의 존재 확률은 지수적으로 감소한다.
            $e^{-2kx}$의 값이 곧 존재 확률이다(앞에서, 이 식이 파동함수(삼각함수 형태)의 형태가 아니라고 이미 말했다.)
            이 값이 0.1이면 10% 확률로 존재한다(=Density). 10%만이 터널링 현상을 통해 통과했다, 이런 식으로 받아들이면 된다.
            1. x 값은 barrier의 width이다.
            1. k 값은 상수이다. 이 값은 inverse decay length라고 한다.
            $\kappa=\frac{2 \pi \sqrt{2 m\left(\mathrm{V}_{\mathrm{o}}-\mathrm{E}\right)}}{h}$
    1. Electron Tunneling
        1. k 값에서, V가 클 경우 양자 터널링이 일어나지 않음을 알 수 있다.
    1. Heisenberg Uncertainty Principle and Quantum Tunneling
        1. 불확정성 원리와 양자 터널링이 동시에 성립하는가?
            1. 성립한다.
        1. 양자 입자는 $\Delta E$만큼의 에너지를 빌리고, barrier를 넘은 다음, 그 에너지를 돌려준다.
        이 현상에 $\Delta t$라는 시간 안에 일어난다.
        이 과정은 불확정성 원리를 위배하지 않는다.
    1. Quantum Tunneling for a Ball
        1. (예제) 탁구공이 있다. 2g, $E=10^{-3}J$이고 넘어야 할 barrier는 높이 20cm, 폭 2cm이다.
        이때 탁구공이 벽 너머에 나타날 확률은?
        1. 풀이
            1. $e^{-2kx}$라는 식을 쓴다.
            1. x값은 2cm이다. k값에서 h는 플랑크 상수, m은 2g, E는 $E=10^{-3}J$이고 $V_0=mgh=3.92 \times 10^{-3}J$이다.
                1. $\kappa=\frac{2 \pi \sqrt{2 m\left(\mathrm{V}_{\mathrm{o}}-\mathrm{E}\right)}}{h}$
            1. $T=e^{ -2 \times 3.24 \times 10^{31} \times 0.02}$
            무척 작은 값이다.
        1. 즉, 일상생활에서는 터널링이 일어나지 않는다.
    1. Quantum Tunneling for Elecron
        1. (예제) 전자. 에너지 1eV이고 barrier는 2eV, 폭 0.1nm이다.
        1. 풀이
            1. 모든 값이 주어져 있으므로 T를 구하면
            T=0.36, 즉 36%의 전자가 barrier를 넘는다는 의미이다.
    1. Reflection from a lower potential
        1. 반사 확률
        ![](/images/물리전자/reflection.jpg)
            1. 고전역학에서, 낮은 에너지로 내려간 입자가 돌아올 확률은 '없다'고 표현한다.
            1. 양자역학에서, 돌아올 확률은 '없다'가 아니라 '지극히 낮다'고 표현한다(0이 아니기 때문)
1. Quantum Leak
    1. Quantum Leak나 Quantum Tunneling이나 똑같은 의미다. 같은 거라고 이해하면 된다.
    1. **그래서, 각 영역 1, 2, 3에서 실제 파동함수는 어떻게 구할까?**
    ![](/images/물리전자/leak.jpg)
        1. 영역 1과 3에서 퍼텐셜 에너지=0이므로(왜냐하면 그렇게 약속한 게 Potential Well이니까.) 쉽게 계산이 가능하다.
        1. 근데 영역 2는 안 그렇거든. $V=V_0$이니까 이걸 고려해야 된다.
        1. 그래서 구한 값은 위 그림과 같다.
        영역 1은 입사파와 반사파가 모두 있다.
        영역 2는 파동이 아니다. 지수적으로 감소한다.
        영역 3은 반사파가 없다. 오로지 투과파만 있음.
    1. STM
        1. 장비 이름이다.
        1. Quantum Leak를 알면 만들 수 있다.
        1. 단점이 있는데 이를 극복한 장치가 SPM이다.
        1. STM은 오로지 conductor의 atomic scale image만을 mapping할 수 있다.
        SPM은 어떤 물질이든지 image를 찍어낼 수 있다.
1. Tunneling Phenomenon 계속
    1. Transmission/Reflection Coefficient
        1. Transmission Coefficient
            1. T라고 적는다.
            $T=\frac{\left|\psi_{I II}(x)\right|^{2}}{\left|\psi_{I}(x)\right|^{2}}=\frac{\mathrm{C} _ {1}^{2}}{\mathrm{A} _ {1}^{2}}=\frac{1}{1+\operatorname{Dsinh}^{2}(\alpha \mathrm{a})}$
            $\mathrm{D}=\frac{\mathrm{V_0}^{2}}{4 \mathrm{E}(\mathrm{V}_0-\mathrm{E})}$
            1. 장벽에 더 넓거나 높다면, $\alpha a>>1$이 된다.
            즉, $T=T_{0} \exp (-2 \alpha a) \approx 0$가 된다.
            $\quad$ 이때 $T_{0}=\frac{16 E\left(V_{0}-E\right)}{V_{0}^{2}}$이다.
        1. Reflection Coefficient
            1. R이라고 적는다.
            $R=\frac{A_{2}^{2}}{A_{1}^{2}}=1-T$
            $\quad R+T=1$이다.
