---
title: 물리전자 - 강의저장 12_2 wave_function
date: 2019-11-27 23:09:58
tags:
categories:
- [4학기(2019-2), 물리전자]
mathjax: true
---

1. Hydrogen Atom 계속
    1. Radial Distribution Function
        1. 여러 함수들
            1. 밀도함수 Electron density
                1. 공간의 어떤 point에서 electron density를 나타내는 함수.
                1. $\rho(r)=|\psi(r)|^{2}$
            1. 확률함수 Probability
                1. 공간의 어떤 공간에서 electron 발견 확률을 나타내는 함수.
                1. $P(r)=|\psi(r)|^{2}dr$
            1. 방사분포함수 Radial distribution
                1. 원이나 구에서 거리 r에 따른 전자 분포를 나타내는 함수.
                1. $P(r)=4\pi r^2|\psi(r)|^{2}$
            1. 전자 발견 확률
                1. 거리 r, 두께 dr인 곳에서의 발견 확률을 나타내는 함수.
                1. $P(r)=|\psi(r)|^{2}dr$
            1. 구체가 아닌 오비탈(p,d,f)
                1. 위 식을 응용한다.
                1. $P(r)=r^2|\psi(r)|^{2}$
        1. Radial distribution function, RDF
            1. RDF라고도 쓴다.
            1. $g(r)$로 표현한다.
                1. 위에서 말했듯 거리 r에 따른 분포를 나타내는 함수다.
                1. 쉽게 구분하자면 다음과 같다.
                $\Psi$ = wave function
                $\Psi ^2$ = prabability (electron) density
                 $4\pi r^2 \Psi ^2$ = radial distribution function
            1. 밀도
                1. 밀도는 사실 숫자/부피다.
                1. 근데 이 밀도값이 상수 = 골고루 분포 라면 괜찮은데,
                거리에 따라 밀도도 달라져서 RDF같은 게 필요해진 거다.
    1. Radial Distribution functions in Sphere
        1. 거리 r에서 전자 발견 확률을 알아보자
            1. 부피를 구한다.
                1. $\frac 43 \pi(r+\delta r)^3 - \frac 43 \pi(r)^3$
                $\quad$ $\delta$가 아주 작다고 했으니 저 식을 쉽게 전개할 수 있다.
                $\quad$ 정리하면 1개 항만 남는다.
                $4\pi r^2 \delta r$
            1. ***교수님 질문 : 위 식에서 뭐라고 가정했는가?***
                1. 답변 : 델타가 아주 작다.
            1. RDF를 구한다.
                1. $g(r)$
                $=4\pi r^2 \rho dr$
                $=4\pi r^2 \Psi ^2$
                $\quad$ 저 위에 올려보면 방사분포함수 설명에 나왔던 $P(r)$과 결과가 같다.
                $\quad$ 밀도 = $\rho$ = 갯수 / 부피이다.
                $\quad$ RDF는 어디까지나 전자 분포 함수다. 밀도함수가 아니라 발견 확률 함수!
    1. Radial Distribution Function 계속
        1. $P_{n, \ell, m_{\ell}}(r)=4 \pi r^{2}\left|R_{n, \ell}(r)\right|^{2}\left|Y_{\ell, m_{\ell}}(\theta, \phi)\right|^{2}$
            1. 거리 의존 함수 $R$과 각도 의존 함수 $Y$.
        1. ***교수님 질문 : Quantum number는 하나 더 있다. 무엇인가?***
            1. 답변 : 스핀.
        1. ![](/images/물리전자/오비탈.jpg)
            1. 양자수에 따라 식이 표와 같이 바뀐다.
    1. Radial Wavefunctions(R)
        1. 위 표에서 언급했듯이, $2\left(\frac{Z}{a_{0}}\right)^{\frac{3}{2}} \mathrm{e}^{-Z r / a_{0}}$이다.
        1. $n=1, l=0$일 때 $\left(\frac{1}{a_{o}}\right)^{3 / 2} 2 \exp \left(\frac{-r}{a_{o}}\right)$이다.
        $\quad$ $Z$ 값은 수소 원자가 원자핵이 1개라 1임.
            1. ![](/images/물리전자/radial_wavefunction.jpg)
            **교수님 코멘트 : 이것만 보고 $r=0$에서 값이 제일 크구만. 그럼 발견확률도 제일 높겠지? 이렇게 생각하면 완전 틀렸다. 파동함수는 여기에 $4\pi r^2$이 곱해진다는 걸 명심하라.**
        1. $n=2$일 때, $\ell$ 값에 따라 오비탈 모양이 달라진다.
            1. ![](/images/물리전자/radial_wavefunction_2.jpg)
            **교수님 코멘트 : $\ell=1$일 때부터 $m_l$ 값이 0이 아닌 다른 값을 가지며, 이에 따라 오비탈 형태가 바뀐다.**
    1. Probability density of Radial Wavefunctions
        1. 지금까지의 내용 복습
            1. $\quad$ 어떤 구간 $dr$에서의 확률함수가 있다.
            $P(r)=|\psi(r)|^{2} d r$
            $\quad$ 수소 원자에서 이 $dr$은 구의 넓이가 된다.
            $p(r)=4 \pi r^{2}|\psi(r, \theta, \phi)|^{2}$
            $=4 \pi r^{2}\left|R_{n, \ell}(r) Y_{\ell, m_{\ell}}(\theta, \phi)\right|^{2}$
            $\quad$ 변수분리법에 따라 아래와 같이 쓴다.
            $=4 \pi r^{2}\left|R_{n, \ell}(r)\right|^{2}\left|Y_{\ell, m_{\ell}}(\theta, \phi)\right|^{2}$
                1. $\ell=0$일 때, $Y$ 함수는 언제나 1이며 $R$ 함수에만 의존한다. 그래서 구형이다.
                1. $\ell \ge 1$일 때, $R$ 함수와 $Y$ 함수가 동시에 존재하게 된다. 그래서 구형이 아니게 된다.
                1. 확률은 $r \rightarrow ,r \rightarrow \infty$ 둘 모두 0에 수렴한다.
        1. 오비탈 함수
            1. ![https://onsaem9134.tistory.com/53](/images/물리전자/오비탈_함수.png)
            1. 확률의 방향 의존성
                1. $Y$함수에 의해 결정됨.
                    1. s 오비탈 = $(\frac {1}{\sqrt 2 \sqrt{2\pi}})^2=\frac{1}{4\pi}$
                        1. 제곱한 이유 : 우리가 쓰는 함수는 $\Psi ^2$이기 때문이다.
                        1. ![](/images/물리전자/확률함수.jpg)
                        1. $\delta P(r)$
                        $=\left|R_{n, l}(r) \cdot \overline{y_{\ell, m_{l}}(\theta, \phi)}\right|^{2} \times 4 \pi r^{2} \delta r$
                        $=\left|R_{n, \ell}(r)\right|^{2} r^{2} \delta r$
                        $\quad$ 위에서 언급한 $\frac 1{4\pi}$가 곱해진 것이다.
                        1. ![](/images/물리전자/s_오비탈.jpg)
                        양자수가 큰 s 오비탈은 확률도 작아진다. 애초에 멀어서 전자가 거기까지 가기 힘들다고 생각할 것.
        1. Solution of Schrodinger Equation
            1. ![](/images/물리전자/p_오비탈.jpg)
                1. $m_l$의 값에 따라 삼각함수가 추가된다.
        1. Polar probability distribution of $Y$
            1. ![](/images/물리전자/타원형_오비탈.jpg)
                1. 왜 타원형이 나타나는가?
                    1. 답변 : $\ell$ 값이 0이 아닌 값을 가짐에 따라 $Y$ 함수가 $\theta, \phi$에 의존하기 때문이다.
            1. ***교수님 질문 : $m_l$이 7개면 전자는 몇개인가?***
                1. 답변 : 14개. 파울리 배타 원리에 의해서 2개가 들어감.
    1. Quantized Electron Energy
        1. ***교수님 질문 : 양자역학에서는 에너지가 Quantized되어 있으며, 그 예를 이미 공부한 바 있다. 무엇인가?***
            1. 답변 : Quantum Well.
        1. 어떻게 전자의 에너지를 구하는가?
            1. 파동함수를 슈뢰딩거 파동방정식의 형태로 만들면 된다.
                1. 그 형태란, $H\Psi + V\Psi = E\Psi$이다.
                    1. $H$는 해밀터니안 연산자.
                    1. 이때 $E_K = \frac{1}{2} mv^2 = \frac {p^2}{2m} = \frac {\hbar ^2 k^2}{2m}$
            1. 그래서 이를 풀면, 다음 식을 얻는다.
                1. $E_{n}$
                $=-\frac{m e^{4} Z^{2}}{8 \varepsilon h^{2} n^{2}}$
                $\quad$ 여기서 $Z, n$을 제외한 값은 상수로 묶인다.
                $=-\frac{Z^{2} E_{I}}{n^{2}}$
                $=-\frac{Z^{2}(13.6 e V)}{n^{2}}$
                    1. $Z$ 값은 원자번호atomic number다.
            1. ***교수님 질문 : $eV$의 정의는?***
                1. 답변 : 에너지의 단위. 전하량과 전압의 $[QV]=[J]$
            1. ***교수님 질문 : 수소의 에너지 분포를 알면 헬륨의 에너지 분포를 구할 수 있는가?***
                1. 그렇다. 에너지 분포 $E_n$이 $Z^2$에 비례하므로, 수소 에너지 분포의 4배가 헬륨 에너지 분포다.
    1. Ionization Energy
        1. Lowest energy of electron
            1. $E_1$ 즉 $n=1$일 때의 에너지
            1. Ground state라고 부른다.
        1. 높은 상태의 에너지
            1. Excited state라고 부른다.
        1. 맨 위 상태의 에너지
            1. 진공 상태의 에너지
            1. $n$이 한없이 커졌을 때의 에너지, 전자가 궤도 운동에서 벗어나게 만드는 에너지, 자유 전자를 만드는 에너지.
            즉, Ionization Energy라고 부른다.
            1. 그러나 한 번 나온 전자가 언제까지나 자유전자로 있을 수는 없다.
                1. 자유전자는 누군가와 충돌하며 에너지를 주고받으며, 에너지를 대체로 잃어 다시 궤도로 돌아온다.
                1. 이온화된 전자가 궤도로 돌아올때까지의 시간을 전자의 lifetime이라고 한다.
        1. 정리
            1. 에너지를 얻으면 에너지 state가 올라간다.
            올라간 state에서는 그에 맞는 짧은 파장의 운동을 한다.
            에너지 state가 떨어질때는 빛이나 열을 낸다.
    1. Excitation of Electron
        1. 전자를 다음 state로 올리기 가장 간단한 방법은 빛을 쬐어주는 것이다.
        1. 광자가 전자를 때린다.
            1. 이때 Photon energy : $h\nu = E_2 -E_1$
            Absorption of $h\nu$ : 전자는 다음 state로 올라간다.
            1. 이에 따라, $\psi_{100}(r, \theta, \phi) \rightarrow \psi_{210}(r, \theta, \phi)$의 형태로 파동함수가 변한다.
        1. 전자는 언젠가 ground state로 돌아간다.
            1. Emitting "light" : characteristic wavelength
            1. Quantization of energy : 에너지는 특정한 값만을 갖는다. 양자화되어 있다.
        1. Absorption
            1. 광자는 파장 $\lambda$를 가지고 전자를 때린다.
            충돌은 에너지를 전달하며, 전자를 더 높은 state로 올려보낸다.
            $h\nu = E_2 -E_1$
        1. Emission
            1. 전자는 낮은 state로 내려오며 빛이나 열을 방출한다.
            1. 실리콘은 열을 주로 방출한다. 빛 말고.
    1. Qunatized Electron Energy
        1. 원자 충돌은 비슷한 현상을 만든다.
            1. Excited electron은 원래 상태로 돌아오며 광자를 방출한다.
            1. 이게, 플라즈마의 원리다.
