---
title: 물리전자 - 강의저장 15_1 density_of_state
date: 2019-12-18 14:23:56
tags:
categories:
- [4학기(2019-2), 물리전자]
mathjax: true
---


1. Si Energy Band Formation
    1. Fermi level : 전자가 채워지는 가장 높은 에너지
    1. 에너지 Split이 일어나 밑에서부터 채워진다.
    1. 높은 양자수의 energy state들은 중복된다.
1. Semiconductors
    1. How Si makes a Solid?
        1. hybridization : 3s, 3p 궤도가 반반 채워져서
        1. Band gap은 forbidden band라고도 한다.
    1. Si Energy Band Formation
        1. ![](/images/물리전자/15_1_에너지_밴드.jpg)
            1. 실리콘은 $3S^23P^2$만큼이 중첩이 되고, 그 아래는 core level이라 하여 interaction의 영향을 받지 않는다.
            1. 3S 오비탈은 2개의 state(스핀 고려)가 존재하고 $3S^2$이므로 2N개의 전자가 존재한다.
            3P 오비탈은 6개의 state가 존재하고 역시 $3P^2$이므로 2N개의 전자가 존재한다. $3P^3$이었으면 3N개였을 것이다.
            1. 거리가 더 가까워질수록 궤도가 중첩되며, state도 변하고 전자들도 state를 옮긴다. 최종적으로는 우리가 아는 half-occupied 형태가 된다.
            1. 중간에 있는 8N states는 hybridization혼성이 일어난 것이다.
            1. ***교수님 질문 : energy split이 왜 일어나는가?***
                1. 답변 : particle interaction 때문이다. 좀 더 정확히는, particle 간 인력과 반발력이 PE의 변화를 가져오고 이것이 슈뢰딩거 방정식의 해를 바꾼다. 슈뢰딩거 방정식의 해가 달라진다는 것은 에너지의 변화를 의미하며 이것이 energy split이다.
            1. ***교수님 질문 : 에너지와 에너지 사이의 값은?***
                1. 답변 : $10^{-21}$ 간격으로 state가 존재한다.
        1. ![](/images/물리전자/15_1_반도체.jpg)
            1. ***교수님 질문 : 실리콘과 GaAs의 차이는?***
                1. 답변 : 실리콘은 4족, GaAs은 3족과 5족의 compound.
                실리콘과 저마늄은 단일 원소로 구성되므로 Elementary semiconductor이다. GaAs는 compound semiconductor이다.
            1. GaAs는 다른 두 개와 달리 Valence band와 Conducton band의 minimum이 같은 곳에서 일어난다.
                1. 즉, 에너지 손실loss 없이 band gap을 올라가고 내려갈 수 있다.
                1. 이런 물질을 direct band gap 물질이라고 한다.
            1. 실리콘이나 저마늄은 maximum과 minimum의 위치가 다르다. 그래서 올라갈 때 lateral crystal 방향으로 천이를 해야 하며 이로부터 모멘텀이 발생한다. 이 모멘텀은 phonon을 만든다.
                1. indirect band gap 물질이라 한다.
                1. mobility가 부족해서 high speed device에 쓸 수가 없다.
            1. ***교수님 질문 : GaAs는 photonic이나 high speed device에도 쓸 수 있다. 그러면 단점은?***
                1. 답변 : 단가가 비싸다, 그리고 우리가 지금 사용하는 반도체의 기본 구조를 쓸 수가 없다? 왜냐? oxide 문제가 있다. $SiO_2$는 온도가 높아진다고 해서 분해되거나 하지 않으며 안정하다. GaAs옥사이드는 온도가 높아지면 나뉘어진다. 저마늄 또한 oxide 문제가 있다. 그래서 실리콘만 메모리, 반도체 device에 쓰는 것이다.
                high speed transistor, photonic 쪽은 GaAs를 쓴다.
    1. Si Energy Band
        1. ![](/images/물리전자/15_1_자유전자.jpg)
        1. 0K 이상에선 thermal energy가 존재한다. 이 에너지에 의해 어떤 전자들은 에너지를 얻어 bond를 깨뜨린다.
        1. bond가 깨지면 전자는 conduction band로 올라가 free electron이 되고 원래 위치에는 free hole을 만든다. 이런 형태를 thermal generation이라고 한다.
            1. 우리가 아는 이온화된 free electron이 아니고, valence band로부터 자유롭다는 의미에서 free이다.
        1. ***교수님 질문 : 그래서 hole과 free electron이 무엇때문에 만들어지는가?***
            1. 답변 : thermal energy
        1. free elctron과 hole는 움직이며 전류를 만드는데, 크기는 같고 방향은 반대다. hole은 실제로는 그냥 빈 공간이지만, free elctron과 함께 설명하기 위해 양전하를 갖는 입자인 것처럼 다룬다. 오로지 valence band에서만 hole을 언급한다.
        1. ***교수님 질문 : field를 가했을 때 free electron의 움직임과 hole의 움직임은 반대이다. 왜 그런가?***
            1. 답변 : conduction band와 valence band는 에너지의 coverture덮개가 반대이기 때문이다.
        1. valence band에 있는 empty state는 양전하로 간주한다. 이는 hole이라는 이름으로도 부른다.
    1. Electron-Hole Pair Generation
        1. 어떤 불순물을 넣어주느냐에 따라 electron을 만들 수도 있고 hole을 만들 수도 있다.
        1. electron이 VB에서 CB로 올라가며 pair를 만드는 현상을 thermal generation이라 한다.
        1. ***교수님 질문 : 상온에서 실리콘에 있는 전자 농도는?***
            1. 답변 : $10^{10} [1/cm^3]$개만큼이 CB에, 그리고 그 숫자만큼의 hole이 VB에 존재한다. 참고로 0K에서는 0이다.
        1. ***교수님 질문 : 반도체를 도체로 만드는 방법은?***
            1. 답변 : 불순물을 많이 넣는다. 온도를 높인다.
        1. ![](/images/물리전자/15_1_홀.jpg)
            1. ***교수님 질문 : 위 사진에서 분홍색 빈 공간은 무엇을 의미하는가?***
                1. 답변 : energy state.
            1. 전자가 CB에 머무는 시간을 lifetime이라 한다. lifetime의 함수는 온도에 대한 함수이다.
1. Electron Effective Mass
    1. Electron Mass in Crystal
        1. ***교수님 질문 : 전자의 질량은?***
            1. 답변 : $9.1 \times 10^{-31}kg$
        1. 정해진 질량은 scattering이 없는 곳에서만 유효하다.
        1. scattering이 있는 상황에서는 effective mass를 적용해야 한다.
        1. ![](/images/물리전자/15_1_유효질량.jpg)
            1. 전자는 진공이 아닌 곳에서 전기장의 영향으로 운동할 때,
            충돌 시 가속도가 변하는데 힘의 방향은 전기장의 방향인, 뉴턴역학으로 받아들일 수 없는 상황이 생긴다.
            1. 그래서 유효질량을 쓰는 것이다.
            1. ***교수님 질문 : 전자는 더이상 절대적인 질량값을 갖지 않는다. 왜 그런가?***
                1. 답변 : scattering이 존재하기 때문이다.
            1. $a=\frac{F_{ext}}{m_e^{'}} $
        1. ***교수님 질문 : E-k 다이어그램을 두 번 미분하면 무엇이 나오는가?***
            1. 답변 : 오목, 볼록 특성
        1. ![](/images/물리전자/15_1_유효질량_식.jpg)
            1. $m_{e}=\left(\frac{1}{\hbar^{2}} \frac{d^{2} \varepsilon}{d k^{2}}\right)^{-1}$
            1. 유효질량은 에너지를 두 번 미분한 값의 역수이다.
            1. curvature가 크면 유효질량은 작고, 작으면 질량은 크다.
1. Density of States in an Energy Band
    1. Density of states
        1. ***교수님 질문 : 왜 electron concentration을 구하려고 하는가?***
            1. 답변 : 그로부터 전류를 알아낼 수 있기 때문이다.
        1. state의 숫자를 알아내기
            1. 단위 에너지 당 per unit energy
            1. 단위 부피 당 per unit volume
            1. 원자 간 거리가 가까워질 수록 split이 증가한다.
        1. ![](/images/물리전자/15_1_밀도.jpg)
            1. 가운데로 갈 수록 state가 많아진다.
            1. 이런 분포(밀도)를 함수로 나타내고자 한다.
    1. Density of states : g(E)
        1. g(E) : state 밀도(density of states)
            1. $g(E)=\frac{dN}{dE}$
                1. state를 에너지에 대해 미분한 값
                1. 에너지의 변화에 따라 states가 어떻게 변하는지를 나타낸다.
                1. g(E)dE : dE 구간에서 존재하는 states 갯수
            1. $S_{v}\left(E^{\prime}\right)=\int_{0}^{E^{\prime}} g(E) d E$
                1. S_v(E^{\prime}) : 단위 부피 당 특정 에너지 $E^{\prime}$까지의 states 갯수
    1. Determination of Density of States
        1. $S_{v}\left(E^{\prime}\right)=\int_{0}^{E^{\prime}} g(E) d E$
        1. ![](/images/물리전자/15_1_2차원.jpg)
            1. 3차원에서의 밀도를 구하기 전에 2차원에서의 밀도를 구해 본다.
            1. 노란색 네모 칸 한칸은 단위면적이며 동시에 state 하나를 의미한다.
            1. $n^{\prime}: \frac{1}{4}\left(\pi n^{\prime 2}\right)$
            1. 다 포함은 못 시키지만 비슷한 값을 취하는 것이다.
        1. ![](/images/물리전자/15_1_3차원.jpg)
            1. $n_1,n_2,n_3$가 존재한다. 세 양자수로부터 정해지는 한 구간이 한 개의 state이다.
            1. 이로부터 부피는 $(1 / 8)(4 / 3)\left(\pi n^{\prime 3}\right)=\frac{1}{6} \pi n^{\prime 3}$와 같이 구할 수 있다.
            1. 스핀을 고려하면 2가 곱해지므로
            $S_{o r b}\left(n^{\prime}\right)=S\left(E^{\prime}\right)=\frac{1}{3} \pi n^{\prime 3}$
            1. n에다가 집어넣으면
            $E=\frac{h^{2}}{8 m_{e} L^{2}}\left(n^{\prime 2}\right)$
            $n^{\prime 2}=\frac{8 E^{\prime} m_{e} L^{2}}{h^{2}}$
            $S\left(E^{\prime}\right)=\frac{\pi L^{3}\left(8 m_{e} E^{\prime}\right)^{3 / 2}}{3 h^{3}}$
            1. 단위 부피 당 값으로 구하면
            $S_{v}\left(E^{\prime}\right)=\frac{\pi\left(8 m_{e} E^{\prime}\right)^{3 / 2}}{3 h^{3}}$
            1. g(E)를 구하기 위해 E로 미분하면
            $g(E)=d S_{v} / d E$
            $g(E)=(8 \pi \sqrt{2})\left(\frac{m_{e}}{h^{2}}\right)^{3 / 2} E^{1 / 2}$
            1. 즉, g(E)는 $\sqrt E$에 비례함을 알 수 있다.
            꼭대기에서는 $\left(E_{\text {top }}-E\right)^{1 / 2}$가 된다.
            1. 위 모델은 metal과 같은 free electron model에만 써먹을 수 있다.
