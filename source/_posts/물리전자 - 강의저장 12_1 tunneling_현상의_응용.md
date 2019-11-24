---
title: 물리전자 - 강의저장 12_1 tunneling_현상의_응용
date: 2019-11-24 22:34:13
tags:
categories:
- [4학기(2019-2), 물리전자]
mathjax: true
---

1. Tunneling Phenomenon 계속
    1. Summary of Tunneling
        1. **터널링이라는 건, 결국 다음을 의미한다.**
            1. Barrier가 특정한 조건을 만족할 때,
            즉 퍼텐셜 에너지가 작거나
            또는 width, Barrier의 폭이 얇으면
            wave가 penetrate되는 현상이 발생한다.
                1. 즉 Barrier를 뚫고 지나갈 확률이 에너지, 폭에 따라서 존재한다.
            1. 이 Barrier 안에서는
            wave가 아니라 감쇠attenuation가 되는 현상만 나타난다.
            1. 감쇠가 끝나는 지점에서, wave가 다시 나타난다.
            이때 wave의 특성은 입사파incident wave와 특성이 같다. 파장같은 거.
1. Scaaning Tunneling Microscope
    1. What is the STM?
        1. STM(Scaaning Tunneling Microscope)은 sensing으로 작동한다.
        뾰족한 바늘 끝sharp tip과 도체 표면에서 Tunneling current가 흐르게 하는 거다.
            1. **전류가 흘러야 하므로, 도체 표면, 뾰족한 바늘 끝 모두 도체여야 한다.**
                1. 뾰족한 끝 맨 아래부분은 원자 1개로 이루어져 있는 게 제일 좋다.
            1. 표면에 가까워질수록 터널링 확률이 높아진다. 최대한 붙은 뒤 스캔을 하면 Tunneling current 이미지를 얻을 수 있다.
                1. 전류가 많이 흐른다? 터널링이 많이 일어났겠구만. 이런 식으로 이해하면 됨.
            1. 그 current를 이미지로 매핑하면은 우리가 원하는 atomic scale 이미지가 된다.
    1. Why is it called STM?
        1. 끝부분과 측정 물질이 접촉하지 않음.
        1. 둘 사이엔 gap(혹은 진공 gap)이 존재.
        1. gap은 potential energy barrier로 기능함.
        1. 그러나, 이 상황에서도 전류는 gap을 통해 흐르며 이것이 electron의 quantum tunneling.
        1. 그래서, 이름이 STM인 것임.
    1. Scaaning Mode: Constant Height
        1. Tip은 XY 평면에서 움직인다.
        1. Z값은 고정이다.
            1. 왜? Current를 일정하게 하면 Z를 움직여가며 측정하는데, 이 기술적으로 굉장히 어렵기 때문(조금 움직이면 접촉할 수도 있으니) 이렇게 쓰는 것이다.
        1. Tip이 스캔되면 전류도 측정된다.
        1. 컴퓨터는 전류 신호를 선 분포나 이미지로 바꾼다. 이때 강한 전류는 밝게, 어두운 전류는 어둡게 변환한다.
    1. Scaaning Mode: Constant Current
        1. Tip은 XY 평면에서 움직인다.
        1. Tip이 스캔되면 Z값을 바꾼다. 컴퓨터가 해줌.
        1. 전류는 고정한다.
        1. 지형항적Topographic 맵이 XY 평면에서 스캔됨에 따라 Z 위치에 따라 만들어진다.
        1. 이 모드는 표면과 Tip간 충돌을 막아줌.
    1. ***교수님 질문 : 이 STM은 아까 조건이 있다고 그랬죠? 뭐였지?***
        1. 답변 : 전류가 흘러야 하기 때문에 Tip과 물질 모두 도체여야 함.
        Insulator, Semiconductor에는 STM을 못 쓴다.
    1. SPM
        1. 도체 아니라도 측정 가능.
        1. AFM 같은 모드들이 있다(이게 뭔진 안 알려줌)
        1. 대강 설명하면, 일단 TIP을 맞추고, 그 TIP이 움직이는데, 이것의 움직임을 측정하는 식으로 스캔함.
    1. Surface of Graphite
        1. STM을 통해 원자의 defect같은 걸 볼 수 있다.
    1. STM Image
        1. ![](/images/물리전자/stm.jpg)
            1. platinum 위에 놓인 iodine 원자가 있다. 이때 defect를 쉽게 관측할 수 있다.
    1. ***교수님 질문 : 반도체인 실리콘을 STM으로 보려면?***
        1. 도핑을 하면 됨.
    1. Image of Si Surface
        1. 111 표면 관측. 표면의 defect나 recrystallization등을 STM으로 관측할 수 있다.
1. Potential Box
    1. 3 Dimensional Potentail Well
        1. ***교수님 질문 : 무한 퍼텐셜 Well 사이에 놓인 전자는 어떤 운동을 하는가?***
            1. 답변 : 1) 그 전자가 갖는 에너지에 따라서 운동함. 2) 그 에너지는 discrete함. 3) 에너지가 높을수록 짧은 파장 운동을 함.
        1. 이젠 전자가 어떤 상자 안에 갖혀있다고 가정함. 상자 밖은 무한 퍼텐셜 에너지.
            1. ***교수님 질문 : 3차원으로 확장 시 가장 먼저 떠올려야 할 것은?***
                1. 답변 : 슈뢰딩거의 파동방정식.
        1. 박스 안에 있는 전자의 운동을 어떻게 설명하죠?
            1. 3D 슈뢰딩거 방정식으로요.
            $\frac{\mathrm{d}^{2} \psi}{\mathrm{d} \mathrm{x}^{2}}+\frac{\mathrm{d}^{2} \psi}{\mathrm{d} y^{2}}+\frac{\mathrm{d}^{2} \psi}{\mathrm{d} z^{2}}+\frac{2 \mathrm{m}}{\hbar^{2}}(\mathrm{E}-\mathrm{V}) \psi=0$
                1. 보시다시피, 이걸 푸는 건 어렵다.
                1. 그래서, 모든 현상을 100% 대변해주지는 않지만, 간략화해서 풀기로 한다.
                이 '간략화'를 separating valuable이라는 방법을 통해 진행한다.
    1. Soultion of 3D Schrodinger Equation
        1. $\frac{\mathrm{d}^{2} \psi}{\mathrm{d} \mathrm{x}^{2}}+\frac{\mathrm{d}^{2} \psi}{\mathrm{d} y^{2}}+\frac{\mathrm{d}^{2} \psi}{\mathrm{d} z^{2}}+\frac{2 \mathrm{m}}{\hbar^{2}}(\mathrm{E}-\mathrm{V}) \psi=0$
        1. Separating variables :
        $\psi(x, y, z)=\psi(x) \psi(y) \psi(z)$
            1. 함수에서 변수 하나가 다른 아무 변수에 의존하면, 이 '간략화'를 써먹을 수가 없다!
        1. Total wave function
        $\psi(x, y, z)=A \sin \left(k_{x} x\right) \sin \left(k_{y} y\right) \sin \left(k_{z} z\right)$
        $\quad$ $A=A_1A_2A_3$
        $\quad$ $k$값만 찾으면 된다. $A$ 값은 $\psi^2$이기 때문이다.
        1. Boundaray conditions : k값 구하기
            1. $x=a, y=b, z=c$라면 이로부터 $k$값을 정의할 수 있다.
            $k_{x} a=n_{1} \pi, k_{y} b=n_{2} \pi, \quad k_{z} c=n_{3} \pi$
            $n_{1}=1,2,3, \cdots n_{2}=1,2,3, \cdots, n_{3}=1,2,3, \cdots$
        1. 결론
            1. $\psi_{n_1n_2n_3}(x, y, z)=A \sin {n_{1} \pi x \over a} \sin {n_{2} \pi y \over b} \sin {n_{3} \pi z \over c}$
        1. 파동함수의 값
            1. $n_1$은 $k_x$를, $n_2$는 $k_y$를 결정하기 때문에, $\psi_{211}$과 $\psi_{121}$은 다른 상태different states다.
            1. A
                1. $A=\left|\psi_{n_{1} n_{2} n_{3}}\left(x, y_{,} z\right)\right|^{2}$
                $\psi_{n_{x}, n_{y}, n_{z}}(x, y, z)=\sqrt{\frac{8}{a b c}} \sin \left(\frac{n_{x} \pi x}{a}\right) \sin \left(\frac{n_{y} \pi y}{b}\right) \sin \left(\frac{n_{z} \pi z}{a}\right)$
            1. 에너지
                1. $E=E\left(k_{x}, k_{y}, k_{z}\right)=\left(\hbar^{2} / 2 m\right)\left(k_{x}^{2}+k_{y}^{2}+k_{z}^{2}\right)$
                $E_{n_{1} n_{2} n_{0}}=\left(h^{2} / 8 m\right)\left(n_{1}^{2} / a^{2}+n_{2}^{2} / b^{2}+n_{3}^{2} / c^{2}\right)$
                1. 특수한 경우 : 큐빅 박스에서 $a=b=c$
                $E_{n_{1} n_{2} n_{3}}=\left(h^{2} / 8 m a^{2}\right)\left(n_{1}^{2}+n_{2}^{2}+n_{3}^{2}\right)$
                $\quad$ $\mathrm{N}^{2}=\left(\mathrm{n}_{1}^{2}+\mathrm{n}_{2}^{2}+\mathrm{n}_{3}^{2}\right)$
                $E_{n_{1} n_{2} n_{3}}=\frac{h^{2} N^{2}}{8 m a^{2}}$
                1. 에너지 레벨
                에너지는 3개의 양자수 $\left(n_{1}, n_{2}, n_{3}\right)$에 의존한다.
                이때 lowest energy는 $E_{111}$이다. 이 때에도 에너지는 zero가 아니다.
                다음 에너지 레벨은 숫자 하나가 1 올라가면 된다.
                $E_{121}=E_{211}=E_{112}$
                    $\quad$ 위 식은 Cubic box라서 성립하는 거다.
                    $\quad$ 이때 값이 같은 세 식을 fold degenerate되어 있다, 접으면 같다, 중복되어 있다고 표현한다.
                    $\quad$ 3 energy states are same.
    1. ***교수님 질문 : 3차원 포텐셜 well 안에 갖힌 전자의 운동을 어떻게 설명하는가?***
        1. 답변 : 1) 그 전자가 갖는 에너지에 따라서 운동함. 2) 에너지는 discrete함. 3) 에너지가 높을수록 짧은 파장 운동을 함. 4) 3개의 qunatum number에 의존함. 5) 그 number가 커질 수록 에너지는 제곱의 형태로 커짐.
            1. 1차원의 경우 1) 그 전자가 갖는 에너지에 따라서 운동함. 2) 그 에너지는 discrete함. 3) 에너지가 높을수록 짧은 파장 운동을 함.
1. Hydrogen Atom
    1. 개요
        1. 전자가 원자핵 주변으로 오비탈 운동을 한다.
        1. 그 운동을 해석할 모델을 알아본다.
    1. Electron wave function in hydrogen atom
        1. ![](/images/물리전자/운동.jpg)
        1. 그림에서 보다시피, 전자의 운동은 쿨롱 힘에 의해서 이루어진다.
        1. 이 system이 갖는 퍼텐셜 에너지는 아래와 같다.
        $V(r)=-\frac{Z e^{2}}{4 \pi \epsilon r}$
        $\quad$ 수소 원자라서, proton 갯수 $Z=1$이다.
        1. ***교수님 질문 : 퍼텐셜 에너지가 있다. 이걸 풀어서 어떤 운동을 하는 지 알아내려면 뭘 먼저 생각해야 하느냐?***
            1. 답변 : 슈뢰딩거 파동방정식Wave Function.
    1. Electron Wavefunctions
        1. ![](/images/물리전자/전자의_운동.jpg)
            1. 단순히 생각해서, 구형이니까 슈뢰딩거 방정식을 구형으로 전개한다는 발상이다.
        1. $\psi(r, \theta, \phi)$라는 슈뢰딩거 방정식은 다음을 만족해야 한다.
            1. 경계조건을 만족해야 한다.
                1. $\psi(r, \theta, \phi)=\psi(r, \theta, \phi+2 \pi)$
                1. $\psi(r, \theta, \phi) -> 0$ when $r -> \infty$
                    1. 표현할 수 없을 만큼 멀리 가면 확률이 0이 된다.
            1. Single valued function의 형태여야 한다.
                1. x의 한 좌표에서, 함숫값은 오로지 하나여야 한다.
            1. 연속이어야 한다(Continuous).
            1. 미분했을 때도 연속이어야 한다.
            1. 이런 것들을 만족하면 방정식 풀기가 쉬워진다.
        1. 양자수quantum number
            1. $r, \theta, \phi$로 표시되는 좌표계에서는 양자수가 $n$ 3개로 표시되지 않는다. 대신 다른 걸 쓴다/
                1. n, Principal quantum number : 주양자수라고 불린다. r의 거리에 따라 n 값이 변한다.
                1. l, Oribital angular momentum quantum number : 좌표계에 $\theta, \phi$와 관련된 값으로, 각도와 관련된 운동을 지배하는 숫자.
                1. $m_l$, Magnetic quantum number : 전하가 charge를 갖고 있어서 운동하면 자기장을 만드는데, 이 field에 의한 운동의 영향을 $m_l$이라고 표시한다.
                    1. ***교수님 질문 : 전자가 오비탈 운동을 하면 자기장이 생긴다는 걸 어떻게 아는가?***
                        1. 답 : 암페어 법칙. 전류는 자기장을 만든다.
                1. 스핀 : 슈뢰딩거 파동방정식에는 위 3개만 필요하다. 파울리 배타 원리에 따라 어떤 전자도 동일한 양자수도 가질 수 없는데, 양자수가 같은 전자는 결국 스핀이 다른 것이다. 한 에너지 레벨에는 스핀이 다른 두 개의 전자가 있을 수 있다.
            1. 어쨌건, n l $m_l$ 3개만 있으면 파동함수를 규정지을 수 있다.
            1. 또, n l $m_l$은 종속적이다.
1. Quantized Electron Energy
    1. Schrodinger Equation for Hydrogen Atom
        1. $-\frac{h^{2}}{8 \pi^{2} m}\left(\frac{d^{2} \psi}{d x^{2}}+\frac{d^{2} \psi}{d y^{2}}+\frac{d^{2} \psi}{d z^{2}}\right)-\frac{Z e^{2}}{4 \pi \varepsilon_{0} r} \psi=E \psi$
            1. 이 식을 풀면 뭐다? 전자의 운동을 설명할 수 있다(확률로!)
        1. ***교수님 질문 : 왜 $\psi$로 설명하는게 무의미한가?***
            1. 답변 : 불확정성 원리 때문.
        1. 양자수의 종속성
            1. n값이 거리 r에 의해 정해진다.
            1. l값은 0부터 n-1까지 정해진다.
            1. $m_l$값은 -l부터 l까지 정해진다.
    1. Solution of Schrodinger Equation
        1. Separating Valuables로 간략화해서 풀어보기
            1. $\psi(r, \theta, \phi)=R(r) Y(\theta, \phi)$
            $\quad$오직 거리에만 의존하는 함수 $R$과 각도 함수 $y$
            $\psi(r, \theta, \phi)=\psi_{n, \ell, m_{\ell}}(r, \theta, \phi)=R_{n, \ell}(r) Y_{\ell, m_{\ell}}(\theta, \phi)$
            $\quad$ 각각 의존하는 양자수 종류가 다르다. $R$ 함수는 거리 r에 의존, $Y$ 함수는 오비탈 운동의 형태(원, 타원, 도넛 모양...)를 결정한다.
        1. $R(r)$ : radial function
        $Y(\theta, \phi)$ : angular dependent function
        1. 참고 : l 값에 따른 명칭
            1. l = 0일 때 sharp라고 한다. 이니셜을 따, s 오비탈이라 한다.
            l = 1 : principal, p 오비탈.
            l = 2 : diffuse, d 오비탈
            l = 3 : fundamental, f 오비탈.
