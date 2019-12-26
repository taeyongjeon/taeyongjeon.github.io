---
title: 물리전자 - 강의저장 10_2 blackbody_radiation
date: 2019-12-18 14:18:21
tags:
categories:
- [4학기(2019-2), 물리전자]
mathjax: true
---

1. Photoelectric Effect
    1. Workfunction
        1. 쿨롱 힘
            1. 전자와 금속 양이온 간의 결합력이 있다.
            1. 자유전자로 나오려면 이 결합력을 이겨내야 한다. 그 값이 일함수Workfunction이다.
            1. $h\nu-\Phi$
    1. Compton Scattering
        1. 입자끼리 충돌하면 에너지를 교환하는데, 파동에서는 이런 일이 일어날 수 없다. 즉 입자의 성질이다.
        1. 빛은 물체와 충돌할 때 일부가 산란된다. 빛이 온전한 파동이었으면 회절하든가 했을텐데 에너지를 주고 자기도 경로를 바꾸는 것이다.
        1. ***교수님 질문 : 광자가 충돌해서 에너지를 잃으면 광자는 어떻게 되는가?***
            1. 답변 : 주파수 값이 줄어들고 파장이 커진다.
        1. $P$
        $=\frac{h}{\lambda}$
        $=\frac{h}{2\pi} \frac{2\pi}{\lambda}$
            $\quad \frac{h}{2\pi}=\hbar$
            $\quad \frac{2\pi}{\lambda}=k$
        $=\hbar k$
        1. ![](/images/물리전자/10_2_compton.jpg)
            1. collimator라는 장치로 직선인 x선만 통과시킨다.
            1. x선은 충돌하며 파장이 그대로$\lambda_0$인 것과 파장이 길어진$\lambda^{\prime}$ 것이 관측되었다. 즉 충돌이 일어난 것이다.
            1. 이를 통해 입자와 빛은 interaction을 한다는 것을 알 수 있다. 이 interaction은 에너지의 교환의 형태이며, 이는 모멘텀이 있어야 가능하다. 모멘텀은 질량이 있어야 하며, 입자이기에 가능하다.
    1. What is Blackbody Radiation?
        1. 금속에 열을 가하면 전자가 나오는데 이를 좀 더 확실하게 실험한 조건이 Blackbody이다.
        1. 흑체의 정의
            1. 특정 온도의 벽으로 둘러쌓인 빈 공간cavity
            1. 그 안에서 벽을 이루는 원자들은 전자기 복사(EM radiation)를 emission도 하고 absorption도 한다.
                1. 여기서 EM radiation이란 결국 전자다. 전자를 내놓기도 하고 받기도 하는 것이다.
            1. 벽의 모든 방향에서 이런 현상이 일어난다.
            1. 평형 상태에서 에너지 방출량 = 흡수량이다.
        1. 이런 Blackbody 구멍을 하나 뚫으면 EM wave가 공간에서 빠져나오며 이를 실험에서 관측할 수 있다.
    1. Blackbody Radiation
        1. ![](/images/물리전자/10_2_흑체복사.jpg)
            1. 파장-빛의 양에 대한 그래프이다.
            1. 온도를 높이니(빨간색 그래프) 더 짧은 파장 쪽으로 그래프가 기울었다(눈에 띌 정도로 이동하진 않았다).
            1. 결국 온도가 파장에 영향을 준다는 것이다.
            $E=\frac{3}{2}kT$ 이 에너지가
            $E=hf$ 이 에너지와 같으니 결국 f를 높이는 데 영향을 준다는 말로 정리된다.
        1. 결론
            1. 온도가 높아질수록 파장이 짧아진다.
            1. UV 부근에서 UV Catastrophe가 일어난다.
    1. Wien's Law
        1. $\lambda_{m} T=b,$ where $b=2.8978 \times 10^{-3} mK$
        1. 야간투시경 만드는 데 쓴다.
    1. Max Plank's Postulate
        1. $E \geq n h c / \lambda$
            1. 복사파의 파장을 갖는 에너지는 $n h c / \lambda$보다 클것이라고 판단함.
1. Elementary Quantum Physics
    1. Einstein Explanation
        1. $E=W+E_{k}$
            1. $E=h c / \lambda$ : 광자의 에너지
            1. $E_k$ 나오는 전자의 운동에너지
            1. $W$ : 일함수(전자가 금속에서 나오기 위해 필요한 에너지)
        1. 텅스텐에 빨간 빛을 주면 $E<W$이므로 전자가 나올 수 없다.
