---
title: AbleElectromagnetics 9장
date: 2019-11-15 21:13:13
tags:
categories:
- [4학기(2019-2), 전기자기학2]
mathjax: true
---
## AbleElectromagnetics-9장
1. 페이저
    1. 페이저와 미분, 적분
        1. 페이저와 미분, 적분
            1. E의 미분 페이저
                1. $\frac{\partial E}{\partial t}=j\omega \bar E(\bar r)$
                1. $\frac{\partial E}{\partial t}$
                $=-\omega E_0sin(\omega t+\phi) $
                $=\omega E_0cos(\omega t+\phi+90)$
                $=Re[\omega E_0e^{j(\omega t+\phi+90})]$
                $=Re[\omega E_0e^{j\omega t}e^{j\phi}e^{j90}]$
                ($j=e^{j90}$)
                $=Re[j\omega E_0 e^{j\phi} e^{j\omega t}]$
                (Re에 의해 $j \omega t$ 탈락)
                $=j\omega \bar E(\bar r)$
            1. E의 적분 페이저
                1. $\int{Edt} ={1 \over j\omega}\omega \bar E(\bar r)$
                1. $\int{Edt}$
                $=\frac1\omega E_0 sin(\omega t +\phi)$
                $=Re[{1 \over j\omega}E_0e^{j\phi}e^{j\omega t}]$
                $={1 \over j\omega}\omega \bar E(\bar r)$
    &nbsp;
1. 페이저와 파동방정식
    1. $\triangledown^2\bar E-\mu \varepsilon {\partial^2 \bar E \over \partial t^2}=0 $
        1. $\triangledown \times \bar E=-\mu{\partial \bar H \over \partial t}$
        (컬을 양변에 취해준다)
        ($\triangledown \times (\triangledown \times \bar E)$)
        ($=\triangledown(\triangledown \cdot \bar E)-\triangledown^2 \bar E$)
        ($=-\triangledown^2 \bar E$)
        (정리한다)
        (그럼 위의 식 완성)
    1. $\triangledown^2\bar H-\mu \varepsilon {\partial^2 \bar H \over \partial t^2}=0 $
        1. 마찬가지로 컬을 씌워서 만들면 된다.
    &nbsp;
    1. **헬름홀츠 방정식** : 파동방정식에 페이저를 도입한다.
        1. 둘 다 페이저와 미분의 관계를 쓰면 된다.
        1. $k=\omega \sqrt{\mu \varepsilon}$
        1. $\triangledown^2\bar E+k^2 \bar E (\bar r)=0$
            1. $\triangledown^2\bar E-\mu \varepsilon {\partial^2 \bar E \over \partial t^2}=0$
            $\triangledown^2\bar E-\mu \varepsilon (j\omega)^2 \bar E (\bar r)=0$
        1. $\triangledown^2\bar H+k^2 \bar H (\bar r)=0$
            1. $\triangledown^2\bar H-\mu \varepsilon {\partial^2 \bar H \over \partial t^2}=0$
            $\triangledown^2\bar H-\mu \varepsilon (j\omega)^2 \bar H (\bar r)=0$
        1. 두 식 다 잘 보면 $k^2$으로 바뀌면서 부호가 +로 바뀌었다. $j^2=-1$이기 때문이다.
    &nbsp;
    1. 헬름홀츠 방정식의 해
        1. $\triangledown^2\bar E+k^2 \bar E (\bar r)=0$
            1. $\bar E(\bar r)=\bar E_x \bar x+\bar E_y \bar y+\bar E_z \bar z$ : 임의의 전기장
        1. $\bar E(z,t)$
        $=E_0 cos(\omega t - kz) \bar x$ (V/m)
        $=E_0 cos(\omega t + kz) \bar x$ (V/m)
        파동방정식의 해는 평면파 전기장의 식이 된다.
        (파동방정식의 해 = 파동의 움직임을 설명할 수 있는 수1. )
            1. ($\frac{\partial^2}{\partial x^2}+\frac{\partial^2}{\partial x^2}+\frac{\partial^2}{\partial x^2})(\bar E_x \bar x+\bar E_y \bar y+\bar E_z \bar z)+k^2(\bar E_x \bar x+\bar E_y \bar y+\bar E_z \bar z)=0$
            ($\bar E (\bar r)=\bar E_x \bar x$ : 편의상 $\bar x$ 방향만 가진다고 가정함)
            $\frac{\partial^2 \bar E_x}{\partial x^2}+\frac{\partial^2 \bar E_x}{\partial x^2}+\frac{\partial^2 \bar E_x}{\partial x^2}+k^2\bar E_x=0$
            $\frac{\partial^2 \bar E_x}{\partial z^2}+k^2\bar E_x=0$
            (2차 ODE의 해는 지수함수)
            $\bar E_x(z)=E_0e^{\pm jkz}$ : 파동방정식의 해(페이저)
            $E_x(z,t)=Re[\bar E_x e^{j \omega t}]=E_0 cos(\omega t \pm kz)$
            $\bar E(z,t)$
            $=E_0 cos(\omega t - kz) \bar x$
            $=E_0 cos(\omega t + kz) \bar x$
                1. Q. 갑자기 왠 z의 함수야(E(z,t))?
                A. E가 x방향으로 **진동** 한다면, 파의 진행방향은 x축에 수직인 y, z 중 하나일 것인데, 이번에는 y축을 자기장으로 잡아서 z축이 진행방향이 됨.
    &nbsp;
    1. 평면파 위상속도
        1. $v=\frac \omega k=\frac{1}{\sqrt{\mu\varepsilon}}$
        진공에서,
        $v=\frac{1}{\sqrt{\mu_0 \varepsilon_0}}=c=3 \times 10^8$ (m/s)
            1. $E_0 cos(\omega t - kz) \bar x$
            (각도를 시간으로 미분하면 거리 / 시간 = 속도다.)
            $\frac{d\phi}{dt}=\frac{d}{dt}(\omega t - kz)=\omega - k\frac{dz}{dt}=0$
        1. 파수
            $k=\omega \sqrt{\mu \varepsilon}=\frac{2 \pi f}{v}=\frac{2 \pi f}{f \lambda}=\frac{2 \pi}{\lambda}(\mathrm{rad} / \mathrm{m})$
            &nbsp;
1. 부도체(무손실매질) 내부의 평면파 자기장
    1. E로부터 자기장을 구해보자. $\overrightarrow{\mathrm{H}}(z, t)=H_{0} \cos (\omega t-k z) \hat{\mathbf{y}}(\mathrm{A} / \mathrm{m})$
        1. $\tilde{\mathrm{E}}(\overrightarrow{\mathbf{r}})=\tilde{E}_{x} \hat{\mathbf{x}}+\tilde{E}_{y} \hat{\mathbf{y}}+\tilde{E}_{z} \hat{\mathbf{z}}$
        $\tilde{\mathbf{H}}(\overrightarrow{\mathbf{r}})=\tilde{H}_{x} \hat{\mathbf{x}}+\tilde{H}_{y} \hat{\mathbf{y}}+\tilde{H}_{z} \hat{\mathbf{z}}$
        &nbsp;
        위 식에서
        &nbsp;
        $\nabla \times \overrightarrow{\mathbf{E}}=-\mu \frac{\partial \overrightarrow{\mathbf{H}}}{\partial t}$
        위 맥스웰 방정식을 적용하면
        $\frac{\partial \tilde{E}_{x}}{\partial z}=-j \omega \mu \tilde{H}_{y}$
        H에 대해 정리하면
        $\tilde{H}_{y}(z)$
        $=-\frac{1}{j \omega \mu} \frac{\partial \tilde{E}_{x}}{\partial z}$
        $=-\frac{1}{j \omega \mu}(-j k) E_{0} e^{-j k z}$
        $=E_{0} \sqrt{\frac{\varepsilon}{\mu}} e^{-j k z}$
        따라서
        $\overrightarrow{\mathrm{H}}(z, t)$
        $=H_{y} \hat{\mathbf{y}}$
        $=E_{0} \sqrt{\frac{\varepsilon}{\mu}} \cos (\omega t-k z) \hat{\mathbf{y}}$
        $=H_{0} \cos (\omega t-k z) \hat{\mathbf{y}}(\mathrm{A} / \mathrm{m})$
        &nbsp;
    1. 평면파 전기장과 자기장의 관계
        1. 위의 E와 H는 다음과 같은 성질을 포함한다.
            1. E와 H의 진동방향은 수직
            1. E와 H의 위상은 동일
            1. E와 H의 크기 비율은 투자율과 유전율에 의해서 결정된다.
                1. 이를 고유임피던스라고 한다.
                $\eta=\frac{E_{0}}{H_{0}}=\sqrt{\frac{\mu}{\varepsilon}}$
                1. 진공에서는 특정한 값을 갖는다.
                $\eta_{0}=\sqrt{\frac{\mu_{0}}{\varepsilon_{0}}} \simeq 120 \pi \simeq 377(\Omega)$
        1. 문제
            1. 진공에서의 주어진 E를 H로 변환하라.
            $\overrightarrow{\mathrm{E}}(z, t)=10 \cos \left(3 \pi \times 10^{8} t-\pi z\right) \hat{\mathrm{x}}(\mathrm{V} / \mathrm{m})$
                1. 방향 : 진행 방향은 z, E의 진동방향은 x이므로 $x \times y = z$, 즉 H의 방향은 y이다.
                1. 크기 : $\eta=\frac{E_{0}}{H_{0}}$로부터
                $H=\frac{E}{377}$
                1. 따라서 H는
                $\overrightarrow{\mathrm{H}}(z, t)=\frac{10}{377} \cos \left(3 \pi \times 10^{8} t-\pi z\right) \hat{\mathrm{y}}(\mathrm{A} / \mathrm{m})$
    &nbsp;
1. 도체(손실매질) 내부의 평면파
    1. 부도체는 손실이 없는데, 도체는 손실이 생김. 이걸 감쇠라고 함.
        1. 도체 내부의 평면파 전기장
        $\frac{\partial^{2} \tilde{E}_{x}}{\partial z^{2}}+k_{c}^{2} \tilde{E}_{x}=0$
        이때
        $\left(k_{c}=\omega \sqrt{\mu \varepsilon_{c}}\right)$
        라고 두면
        $\tilde{E}_{x}=E_{0} e^{-j k z z}$
        전파상수에 j가 붙었으므로
        $j k_{c}=\gamma=\alpha+j \beta$
        라고 두면
        $\tilde{E}_{x}(z)$
        $=E_{0} e^{-\gamma z}$
        $=E_{0} e^{-\alpha z} e^{-j \beta z}$
        정리하면
        $\overrightarrow{\mathrm{E}}(z, t)$
        $=\operatorname{Re}\left[\tilde{E}_{x} e^{j \omega t}\right] \hat{\mathbf{x}}$
        $=E_{0} e^{-\alpha z} \cos (\omega t-\beta z) \hat{\mathbf{x}}(\mathrm{V} / \mathrm{m})$
        라는 값을 얻는다.
        이것이 도체 내부의 평면파 전기장이다.
    1. 감쇠일까? 증폭일까?
        1. $\alpha$의 값에 따라 증폭 혹은 감쇠된다.
        $\alpha>0$일 때 감쇠계수 -> 손실매질Lossy Medium
        $\alpha<0$일 때 증폭계수 -> 레이저의 증폭매질 등
        1. $\beta$는 위상상수 -> 부도체매질의 파수 k와 같음
    1. 감쇠계수와 위상상수의 식
        1. $\gamma=j k_{c}$
        $=j \omega \sqrt{\mu\left(\varepsilon^{\prime}-j \varepsilon^{\prime \prime}\right)}=\alpha+j \beta$
        로부터
        $\alpha^{2}-\beta^{2}=-\omega^{2} \mu \varepsilon^{\prime}$
        $2 \alpha \beta=\omega^{2} \mu \varepsilon^{\prime \prime}$
            1. $\alpha$
            $=\operatorname{Re}\{\gamma\}$
            $=\omega \sqrt{\frac{\mu \varepsilon^{\prime}}{2}}(\sqrt{1+\left(\frac{\varepsilon^{\prime \prime}}{\varepsilon^{\prime}}\right)^{2}}-1)^{1 / 2}(\mathrm{Np} / \mathrm{m})$
            1. $\beta$
            $=\operatorname{Im}\{\gamma\}$
            $=\omega \sqrt{\frac{\mu \varepsilon^{\prime}}{2}}(\sqrt{1+\left(\frac{\varepsilon^{\prime \prime}}{\varepsilon^{\prime}}\right)^{2}}+1)^{1 / 2}(\mathrm{rad} / \mathrm{m})$
        1. 손실매질의 고유 고유임피던스
            1. $\eta_{c}=\frac{E_{0}}{H_{0}}=\sqrt{\frac{\mu}{\varepsilon_{c}}}=\sqrt{\frac{\mu}{\varepsilon^{\prime}-j \varepsilon^{\prime \prime}}}$
            1. 임피던스가 허수인 경우 전기장과 자기장의 위상이 다름.
    1. 표피심도
        1. 표피심도: 도체 내부에서 전자기파 진폭이 63% 줄어드는 이동거리
        1. $\delta_{S}$로 표현한다.
        $\left|\frac{E\left(z=3 \delta_{S}\right)}{E(z=0)}\right|=\frac{E_{0} e^{-3}}{E_{0}}$
    1. 저손실부도체
        1. 생략
1. 전기장과 자기장의 상호관계
    1. 임의 방향 전기장의 식
        1. $\tilde{\mathbf{E}}(x, y, z)$
        $=\tilde{\mathbf{E}}_{0} e^{-j \mathbf{k} \cdot \mathbf{r}}$
        $=\tilde{\mathbf{E}}_{0} e^{-j\left(k_{x} x+k_{y} y+k z\right)}$
    1. 진동방향과 진행방향의 관계
        1. 둘은 항상 수직임.
    1. 전기장과 자기장의 관계
        1. 전기장 방향 X 자기장 방향 = 진행방향이다.
        1. $\tilde{H}(\vec{r})=\frac{1}{\eta} \hat{k} \times \tilde{E}(\vec{r})(A / m)$
        1. 예제
            1. $\overrightarrow{\mathrm{H}}(z, t)=H_{0} \cos (\omega t-k z) \hat{\mathrm{y}}$
            진행방향은 z, 자기장 진동방향은 y이므로 전기장 진동방향은 x이다.
            $\frac EH=\eta$이므로
            $\overrightarrow{\mathrm{E}}(z, t)=\sqrt{\frac{\mu_{0}}{\varepsilon_{0}}} H_{0} \cos (\omega t-k z) \hat{\mathbf{x}}(\mathrm{V} / \mathrm{m})$
