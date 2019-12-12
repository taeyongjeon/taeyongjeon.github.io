1. Stimulated Emission and Lasers
    1. Photon Amplication
        1. ![](02:21 증폭.jpg)
        1. $h\nu_{32}$는 원하는 파장이 아니고, $h\nu_{21}$은 우리가 써먹으려는 파장이다.
        원하는 파장을 걸러내기 위해 거울의 초점거리를 사용한다.
        1. 특정 초점거리는 특정 파장만을 필터링시켜줄 수 있다.
    1. Laser
        1. 레이저?
            1. 동위상(in phase)의 빛 다발bundle을 의미한다.
        1. Ruby laser
            1. 첫 단계 Optical pumping : Xenon flashlight. 에너지가 높은 기체임.
            1. 두번째 단계 Metastable state로 이동 : Cr$^{+3}$(크롬 3가)의 defect를 이용함. 크롬 3가가 루비에 들어가면 이 defect가 metastable state 역할을 한다.
            1. 세번째 단계 파장 걸러내기 : 여러 거울을 써서 특정 파장만 필터링해냄.
            1. 위 과정을 통해 highly coherent light with high intensity가 만들어짐.
            1. 텅스벤 전구랑은 다름.
1. He-Ne laser
    1. 작동 방식
        1. ![](08:44 He_Ne_레이저.jpg)
        1. He-Ne 레이저는 혼합 기체로 이루어진다.
        1. 루비 레이저와 마찬가지로 거울로 특정 파장을 필터링한다.
        1. 끝부분이 볼록거울이기 때문에, 초점거리에 맞는 빛만 평행하게 나오게 된다. 안 맞으면 반사된다.
1. Stimulated Emission and Lasers
    1. Helium-Neon Laser
        1. 파장 632.8nm의 붉은 색 레이저를 만든다.
        1. 스위치(전원)을 누르면 He가 excited되고 충돌로 Ne도 excite된다.
        1. 네온은 비활성 기체라, 한번 excite되면 5s 오비탈로까지 올라간다.
            1. $1s^22s^22p^6 -> 1s^22s^22p^55s^1$
        1. 헬륨 역시 비활성 기체라, 높은 오비탈로 올라간다.
            1. $1s^2 -> 1s^12s^1$
        1. 핵심은, He과 Ne의 충돌로 population inversion을 얻는다는 것이다. 루비 레이저는 충돌이 아니라 optical pumping을 한다.
1. He-Ne laser
    1. 작동 방식 - 계속
        1. 전압을 주면 전자의 방전이 일어난다(전자가 전압에 의해 움직임).
            1. He가 전자와 충돌해서 excite된다.
            He + $e^- -> $He\*$ + e^-$
            (He*는 excite된 He)
        1. He의 전자 하나는 2s로 올라가고, 2s는 "metastable state"이므로 오래 머물 수 있다.
        1. He\*이 Ne과 충돌하여 Ne\*가 되고 population inversion이 일어난다.
        number of Ne\*($2p^55s^1$) > number of Ne($2p^53p^1$)
        1. ![](18:52 He_Ne.jpg)
    1. He-Ne 레이저는 루비 레이저와 달리 충돌을 이용하기 때문에 stimulate를 통한 raging을 하지 않는다.
1. Stimulated Emission and Lasers
    1. Laser Output Spectrum
        1. 레이저가 하나의 파장처럼 보이지만, 사실 아니다.
        실제로는 특정 파장을 중심으로 하는 스펙트럼을 이룬다.
        1. 도플러 효과 때문이다.
            1. 평균 운동 에너지 = $\frac 32 kT$
            1. 주파수 $\nu_0$의 기체의 경우
                1. 관측자에게 다가올 경우
                $\nu_2 = \nu_0 (1+v_x /c)$
                1. 멀어질 경우
                $\nu_2 = \nu_0 (1-v_x /c)$
            1. 원자가 random motion을 가지기 때문에 관측자는 주파수의 스펙트럼을 갖는다.
            $\delta \nu = \nu_2 - \nu_1$
            즉, 파장의 도플러 대역이다.
        1. ![](24:20 도플러.jpg)
            1. 레이저가 두께가 있는 것처럼 보이는데, 이는 Doppler broadening이 존재하기 때문이다.
            1. 레이저와 거울의 반사로 특정 파장만 필터링하는 건 틀림없다(붉은색이면 632.8nm의 파장만 나온다는 소리다). 근데 관측자에 의해 그 파장이 달라지는 것이다.

## 3장 끝

## 4장 시작
## Modern Theory of Solids

1. 챕터 개요
    1. 양자역학에서 배운 전자들의 운동이, 분자나 그 이상(예를 들어, Solids)에서 어떻게 작용하는지를 배운다.
    1. Hydrogen Molecule
        1. 결합의 분자 오비탈 운동 이론을 배운다.
    1. ***교수님 질문 : Hydrogen 원자에 대해서 무엇을 배웠는가?***
        1. 답변 : Hydrogen 원자에 있는 전자는 불연속적인 에너지 state를 가진다. 즉, 현실세계에서의 에너지와 다르다.
    1.  ***교수님 질문 : 전자의 질량은?***
        1. $9.1 \times 10^{-31}$
    1. Electron Effective Mass
        1. 전자의 질량값이 물질에선 적용이 안 된다. 충돌로 인해서 힘의 값이 변하고 뉴턴역학이 성립하지 않게 된다.
        1. 이를 위해 물질 안에서 전자의 질량을 바꾼다. 심지어 마이너스로도 바꾼다. 이를 유효질량effective mass라고 부른다.
    1. Density of States in an Energy Band
        1. 전자가 활용할 수 있는 에너지 state의 밀도를 배운다.
1. Modern Theory of Solids
    1. Molecular Orbital Theory of Bonding
        1. 수소는 2개 합쳐서 분자를 만드는데 헬륨은 2개가 안 합쳐진다. 그 이유를 배운다.
        1. 원자 둘이 서로 멀리 있을 때
            1. 원자는 각각의 에너지 1s, 2s 등을 가짐.
            1. 각 원자에 있는 전자의 에너지 : -13.6 eV
            1. 시스템의 총 에너지 : -27.2 eV
        1. 원자가 더 가까워지면 새로운 wavefunction이 만들어진다.
            1. 새로운 에너지 값이 -13.6 eV보다 낮으면 수소는 분자를 이룬다. : Favorable하다 - 에너지가 더 낮아 안정적이기 때문.
            1. 결합의 형성
                1. 새로운 파동함수 : 분자 궤도를 사용한다.
        1. $H_2$ 분자
            1. 원자 두 개가 분자가 되면 파울리 배타 원리를 적용해야 한다. 수소 원자 2개가 똑같은 원자 궤도를 가질 수는 없다(1s).
            1. 그래서 파동함수는 ovelap되고, 새로운 함수를 형성한다.
            1. 새로운 파동함수는 선형 결합으로 이루어진다.
            1. 1[](40:57 오버랩.jpg)
            1. ***교수님 질문 : bonding state와 anti-bonding state 중 어느 쪽이 에너지가 더 높은가?***
                1. 답변 : anti-bonding state. 에너지를 더 낮출 수 있을 때 bonding state를 형성하기 때문이다.
1. Hydrogen Molecule
    1. Molecular Orbital Theory of Bondig
        1. ![](42:30 bonding.jpg)
            1. Bonding
                1. 대칭적이다.
                1. 원자 사이에도 전자의 존재 확률을 갖는다.
            1. Antibonding
                1. 비대칭적이다
                1. 원자 사이에 전자가 없다.
                1. 그림에서는 업-다운으 그려져있지만 업업, 다운다운도 가능하다.
        1. ***학생 질문 : Bonding과 Antibonding의 +, - 부호에 따르면 저 그래프가 나올 수 없는 게 아닌가?***
            1. 답변 : +, -는 결합과 비결합을 나타낸 기호일 뿐이며 숫자의 덧셈, 뺄셈을 말하는 건 아니다.
    1. Electron energy of two Hydrogen Atoms
        1. Energy split
            1. 원자가 가까워지면 particle interaction이 발생한다.
            1. particle interaction의 경우는 2가지 형태가 있고(Bonding, Antibonding), 그 결과가 energy split을 만들어낸다.
            1. 설명 2 : 두개의 파동함수가 중복overlap되고, 이로부터 파동함수의 split을 만들어낸다.
            1. 새롭게 만들어진 wavefunction은 새롭게 생긴 PE를 슈뢰딩거 방정식에 넣어서 구해낸 함수이다.
        1. R값이 작아지면(가까워지면)
            1. ![](53:49 결합.jpg)
            1. R < a 전자 2개가 'spin pair' 형성. 즉, 아래쪽에 2개가 다 위치함.
            1. $\Psi$ : 고립된 수소 원자보다 더 안정적이라 선호됨.
            1. 에너지 차이 : bonding energy
            1. PE는 음의 값 : 인력이 작용함.
    1. RLC Resonant Circuit
        1. 공진주파수에서 전류가 흐르는데, 두 회로를 coupling했을 때 분자의 형성과 같은 형태가 나타난다.
    1. Electron energy of two Hydrogen Atoms
        1. 파동함수 $\Psi_{\sigma}$
            1. bonding state라고 부름.
            1. 가장 낮은 에너지.
            1. 반대로, $\Psi_{\sigma}$* 는 Anti-bonding state라고 부른다.
    1. Two He Atoms
        1. 거리가 가까워지면 $E_{\sigma}$,$E_{\sigma}$* 두 개가 생긴다.
            1. 그런데, 낮은 에너지 state에 전자 2개 넣고, 높은 에너지 state에 전자 2개 넣으면? 전체적으로 에너지의 감소가 없다.
            1. 에너지의 감소가 없으므로 굳이 결합을 형성하지 않는다. 더 안정적인 형태가 아니기 때문이다.
        1. 예시
            1. He-He의 결합은 Overlap of full-occupied atomic orbital states라고 부르며, 결합을 형성하지 않는다.
            1. 단, energy split은 일어났다.
            1. 즉, 결합을 형성하려면 overlap of half-occupied orbital이 필요하다.
1. Band Theory of Solids
    1. Energy Bond Formation : 3 Hydrogen Atoms
        1. ![](1:01:00 조합.jpg)
            1. 파동함수 3개의 조합으로 3개의 새로운 파동함수가 만들어진다.
            1. 전부 다 더해지는 경우(전부 밀어냄)(a)
            파동함수 하나가 관여 안 하는 경우(b)
            하나만 빼지는 경우(c)
        1. ![](1:01:00 조합.jpg)
            1. 3개의 중첩은 위 그림처럼 나타난다.
    1. n Li Atoms
        1. n개의 Li Atoms는 고체다.
        리튬에서부터 energy band에 대한 이야기를 하기 시작한다.
        1. $1s^2$는 다른 Li의 영향을 받지 않는다.
        그러나 $2s^1$의 경우 상호작용의 영향을 받는다.
        1. n개의 전자는 n개의 2s 파동함수를 $E_{2s}$에서 가진다.
        이게 합쳐지면
        $E_{2s}$는 n개의 에너지 레벨로 나눠진다.
        R=a 구간 밖에서 energy split이 일어난다.
            1. a : 원자간 거리
1. N Li Atoms
    1. ![](01:08:25 리튬.jpg)
        1. N개의 전자가 system에 존재한다. 왜 리튬인데 3N이 아니냐면 $1s^2$에 있는 전자들은 참여하지 않기 때문이다.
    1. 물질 속 전자는 더이상 discrete하지 않고, 특정한 대역 안의 어딘가에 있는 state에 존재한다.
    1. ***교수님 질문 : 왜 state의 절반만 채워지는가?***
        1. 답변 : 한 state에 전자가 2개씩 들어가서.
1. Band Theory of Solids
    1. n Li Atoms
        1. ![](01:11:27 리튬_결합.jpg)
            1. 셋 다 결합할 때 가장 낮은 에너지를 갖는다.
            1. +, -, +, -로 결합할 때 가장 높은 에너지를 갖는다.
    1. ***교수님 질문 : 리튬이 모여서 분자 궤도를 만드는 이유는?***
        1. 답변 : particle interaction 때문. 전자와 양성자의 상호작용에 의해 PE가 바뀌고, 이에 따라 슈뢰딩거 방정식의 값이 바뀌었기 때문.
    1. 지금까지 다룬 내용은 0K에서만 성립한다. 온도가 올라가면 전자가 높은 에너지로 얼마든지 올라갈 수 있게 된다. 아래쪽 state만 채워지는 건 절대0도에서만 가능하다.
    1. 에너지 state의 중첩은 energy band라고 표현되며, 이 때부터 전자가 어떤 state에 있느냐는 이야기하지 않고 energy band 안에 전자가 얼마나 있느냐만 다루게 된다.
    즉, 2s와 2p가 겹쳐지면 이게 2s에 있는지, 2p에 있는지 말할 수 없고 이를 이야기할 필요도 없어진다.
