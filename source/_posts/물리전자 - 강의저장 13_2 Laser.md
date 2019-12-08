---
title: 물리전자 - 강의저장 13_2 Laser
date: 2019-12-08 23:29:35
tags:
categories:
- [4학기(2019-2), 물리전자]
mathjax: true
---

1. He Atom and Periodic table
    1. Pauli Exclusion Principle
        1. ***교수님 질문 : 파울리 배타 원리가 무엇인가?***
            1. 답변 : 한 시스템에서 전자는 같은 양자수를 가질 수 없다.
        1. 궤도 운동Orbital motion은 3개의 양자수, 스핀은 $m_s$에의해 정해진다.
    1. Electronic Structure of Many Electrons
        1. ***교수님 질문 : 전자가 올라갈 때 어떤 법칙을 따르는가?***
            1. 답변 : Selection Rule
        1. 전자가 채워지는 걸 간단히 표기하기 위해 box 그림을 이용한다.
        스핀을 나타내기 위해 화살표를 사용한다. 위쪽 화살표는 업 스핀이다.
        1. ![](/images/물리전자/13_2_전자스핀.jpg)
            1. 궤도가 1개일 때는 파울리 배타 법칙에 따라 스핀 쌍을 형성한다.
            2. 궤도가 여러개(p오비탈부터)일 때는 훈트 Rule에 의해 반발력을 최소화시키기 위해서 다른 궤도부터 전자를 채운다.
    1. Hund's Rule
        1. 전자는 가장 낮은 에너지의 오비탈부터 채운다.
        1. 여러 궤도가 있을 때는 훈트 규칙을 따라 다른 궤도부터 채운다.
        1. 이를 통해 system의 에너지가 낮아진다.
        1. Origin of Hund's Rule
            1. Reduce coulombic repulsion
            1. 같은 양자수의 스핀만 다른 전자 2개 : 쿨롱 반발력 강함
            1. 다른 양자수의 전자 2개 : 쿨롱 반발력 약함
        1. 예시
            1. 산소 : $1s^22s^22p^4$
                1. 1s, 2s 다 채우고 2p에서는 스핀쌍 1개 + 궤도마다 1개 해서 8개 전자가 채워짐.
1. Stimulated Emission and Lasers
    1. Stimulated Emission
        1. 개요
            1. 전자는 Absorption과 Emission으로 energy state를 바꾼다.
            1. 에너지 레벨의 이동을 Excitation이라고 부르며 이 안에 Absorption과 Emission가 있는 것.
            1. Emission에는 두 종류가 있다. 하나는 Spontaneous emission, 다른 하나는 Stimulated emission이다.
            1. 이 중에서 인위적으로 빛을 줘서 emission을 일으키는 게 Stimulated emission이다.
        1. ![](/images/물리전자/13_2_방출.jpg)
            1. 에너지를 받으면 $E_1$에서 $E_2$로 갈 수 있다.
            1. 반대로, 내려갈 수도 있다.
            1. 그런데 $E_2$에서 잠깐 머물고 나중에 내려올 전자를 인위적으로 내려오게 만들 수 있다. 그리고 그 차이만큼 에너지도 방출한다. 그게 3번째 사진이다.
            이를 Amplication이라고도 한다.
        1. ***교수님 질문 : 실리콘이 반도체 시장의 90% 이상을 점하고 있지만 photonic 쪽으로 진출하지 못하는 이유는 무엇인가?***
            1. 답변 : 실리콘이 Indirect band gap 물질이기 때문에 빛으로부터의 Energy conversion 효율이 나쁘기 때문이다.
            에너지와 k(혹은 모멘텀 p)를 y, x축으로 두는 그래프를 그리면 이차함수 두개가 나오며 윗부분을 Conduction band, 아랫부분을 Valance Band라고 부른다.
            그리고, 그 두 그래프의 간격(=에너지 차이)을 Band Gap이라 한다.
            금속은 Band gap이 작거나 없다.
            $\delta k=0$일 때 direct band gap이라고 부른다. 그래프의 최소점, 최대점이 같은 x축상에 있음을 의미한다.
            0이 아니면 indirect band gap이라고 한다. 실리콘이 여기에 해당한다.
            indirect band gap 물질이면 어떻게 되는가?
            $\delta E$만큼은 photonic transition, $\delta k$만큼은 phonon transition이 일어난다. phonon transition은 $k$값의 존재 때문에 일어나며, 이는 모멘텀을 만들고 전자의 vibration 역시 만든다. 즉, 열이 발생하고 그만큼은 전부 다 소실되는 것이다. 즉, 에너지 효율이 낮다. 태양 전지 효율이 한 19%다.
        1. ***교수님 질문 : GaAs(갈륨아세나이드)는 direct band gap 물질인데 왜 태양 전지같은 데 안 쓸까?***
            1. 답변 : 비싸기 때문이다. 실리콘보다도 비싸다.
        1. Spontaneous emission
            1. $E_2$에서 $E_1$으로 내려올 때 $E_1$이 빈 공간이어야 한다(isn't occupied). 그러면 $h\nu = E_2 - E_1$만큼의 에너지를 방출하며, 마치 전자가 주파수 $\nu$의 진동을 하는 것처럼 보인다.
        1. Stimulated emission
            1. 현상의 설명
                1. 외부에서의 빛이 emission을 자극stimulate한다.
                1. $h\nu = E_2 - E_1$라는 에너지를 공급하면 올라가거나, 그 에너지를 그냥 방출하고 내려오게 된다. 그런데 $E_3$으로 갈 에너지는 아니므로 결국 떨어진다. 이를 통해 $E_2$에 머물 전자까지 에너지를 강제로 방출시키므로, photo amplication이 일어난다.
                1. 이때, 방출하는 광자와 공급하는 에너지는 같은 주파수 및 방향(in phase)를 지녀야 한다.
            1. Photo amplication
                1. $f=\left(E_{2}-E_{1}\right) /h$
                1. Stimulated emission은 photo amplication이라고도 한다. 광자 1개를 넣으면 2개가 나오기 때문이다.
                1. 그런데, 기껏 에너지를 방출시켰는데 $E_1$에서 에너지를 흡수해 $E_2$로 올라가버리면 안 되므로 다른 작업을 수행한다.
    1. Photo Amplication
        1. Population inversion
            1. 정의
                1. $E_2$의 원자가 $E_1$의 원자보다 많아지는 상태
            1. ***교수님 질문 : metastable, meta(quasi, semi)의 뜻이 무엇인가?***
                1. 답변 : meta는 '준'의 의미, metastable은 '준안정'이라는 의미.
            1. 방법
                1. 위로 간 전자는 불안정하므로 내려온다. 이걸 못 떨어지게 metastable state에 담아둔다. 그럼 준안정 상태로 $E_1$으로 떨어지지 않게 된다.
                1. 이 metastable state라는 보관장소는 사람들이 인위적으로 만드는 것이다.
                1. 이 보관장소란, 실제적으로 defect(결함)을 말한다. 즉 dangling bond를 말한다.
                    1. 물론 dangling bond를 만드는 건 아니고, 루비같은 곳에다가 크롬 defect를 넣어 크롬3가를 형성해서 전자를 담아두는 것이다.
            1. Population inversion를 만드는 방법 = 레이저의 원리이다.
            1. 일어나는 과정
                1. $E_3>E_2>E_1$의 3가지 에너지 state를 가정한다.
                1. optical pumping 과정 : Excitation에 의해 원자들은 $E_3$으로 excite된다.
                1. $E_3$은 $E_2$로 decay된다. $E_2$는 metastable state, long live state라고 부른다.
                    1. Artificial population inversion이 이루어졌다. $E_2$ 상태 원자의 갯수가 $E_1$보다 많다.
