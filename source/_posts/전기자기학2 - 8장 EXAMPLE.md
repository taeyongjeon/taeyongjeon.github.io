#### 8-2.4 전자기파 $\tilde{\mathbf{E}}=\mathbf{a}_{x} E_{o} e^{-0.3 z} e^{-j z / 2}$ 가 $\mu=\mu_{o}, \varepsilon^{\prime}=2 \varepsilon_{o}$ 인 손실매질에서 진행한다. 이 매질의 고유임피던스를 구하라.
1. 개념
    1. $\hat{\eta}=\sqrt{\frac{\mu}{\hat{\varepsilon}}}=\sqrt{\frac{\mu}{\varepsilon^{\prime}-j \varepsilon^{\prime \prime}}}$
1. 풀이
    1. $\alpha$, $\beta$를 구한다.
        1. $e^{-0.3 z} e^{-j z / 2}$로부터
        $e^{-(0.3+\frac j2)z}=e^{-jkz}=e^{-(\alpha + j\beta)z}$
        $\alpha=0.3$, $\beta=0.5$
    1. 손실 탄젠트 $\tan \xi=\frac{\varepsilon^{\prime \prime}}{\varepsilon^{\prime}}$를 구한다.
        1. $\tan \xi=\frac{\varepsilon^{\prime \prime}}{\varepsilon^{\prime}}$
        1. $\left(\frac{\alpha}{\beta}\right)^{2}=\frac{\sqrt{1+\left(\frac{\varepsilon^{\prime \prime}}{\varepsilon^{\prime}}\right)^{2}}-1}{\sqrt{1+\left(\frac{\varepsilon^{\prime \prime}}{\varepsilon^{\prime}}\right)^{2}}+1}$
        $\frac{\varepsilon^{\prime \prime}}{\varepsilon^{\prime}}=1.88$
    1. 고유 임피던스를 구한다.
        1. $\hat{\eta}=\sqrt{\frac{\mu_{o}}{2 \varepsilon_{o}}} \frac{1}{\sqrt{1-j\frac{\varepsilon^{\prime \prime}}{\varepsilon^{\prime}}}}=\frac{120 \pi}{\sqrt{2}} \frac{1}{\sqrt{1-j 1.88}}=183 e^{j 0.54}$
            1. 우항의 첫 번째 루트식은 문제의 조건에 나와있는 값이다.
            $\sqrt{\frac{\mu_{o}}{2 \varepsilon_{o}}}=\frac{377}{\sqrt2}=\frac{120\pi}{\sqrt2}$

#### 8-2.4 비자성체의 복소고유임피던스가 100[MHz] 의 파에 대해 $\hat{\eta}=200 e^{j 0.5}$ 로 주어진다. 감쇠상수 및 위상상수를 구하라.
1. 개념
    1. $\hat{\eta}=\sqrt{\frac{\mu}{\hat{\varepsilon}}}=\sqrt{\frac{\mu}{\varepsilon^{\prime}-j \varepsilon^{\prime \prime}}}$
1. 풀이
    1. 고유 임피던스 식을 세운다.
        1. $\hat{\eta}=200 e^{j 0.5}[\Omega]$
        $=\sqrt{\frac{\mu_{o}}{\varepsilon}} \sqrt{\frac{1}{1-j \sigma /(\omega \varepsilon)}}=\sqrt{\frac{\mu_{o}}{\varepsilon_{o} \varepsilon_{r}}} \frac{e^{j \xi / 2}}{\left[1+(\sigma / \omega \varepsilon)^{2}\right]^{1 / 4}}$
        $\xi=1, \tan \xi=1.56$
    1. 감쇠상수 $\alpha$와 위상상수 $\beta$를 구한다.
        $\frac{377}{\sqrt{\varepsilon_{r}}} \frac{1}{\left[1+(1.56)^{2}\right]^{1 / 4}}=200$
        $\varepsilon_{r}=1.92$
        $\alpha=\omega \sqrt{\frac{\mu_{o} \varepsilon_{o} \varepsilon_{r}}{2}}[\sqrt{1+\left(\frac{\sigma}{\omega \varepsilon}\right)^{2}}-1]^{1 / 2}=\frac{2 \pi \times 10^{8}}{3 \times 10^{8}} \sqrt{\frac{1.92}{2}}[\sqrt{1+(1.56)^{2}}-1]^{1 / 2}=1.90$
        $\beta=\omega \sqrt{\frac{\mu_{o} \varepsilon_{o} \varepsilon_{r}}{2}}[\sqrt{1+\left(\frac{\sigma}{\omega \varepsilon}\right)^{2}}+1]^{1 / 2}=\frac{2 \pi \times 10^{8}}{3 \times 10^{8}} \sqrt{\frac{1.92}{2}}[\sqrt{1+(1.56)^{2}}+1]^{1 / 2}=3.47$
        1. $\omega=2\pi f=2\pi \times 100 \times 10^6$
        1. $\sqrt{\mu_ 0 \varepsilon_0}=\frac 1c=\frac{1}{3 \times 10^8}$
            1. [유전율과 투자율 그리고 빛의 속도](http://blog.naver.com/applepop/220261819104)
        1. 손실 탄젠트 : 매질 내에서 전파되는 파동성 에너지가 열 에너지 등으로 손실되는 척도
        $\frac{\sigma }{\omega \varepsilon}=\tan \xi$
        $\begin{aligned} \tan \delta &=\frac{\mathbf{J}_{c}}{\mathbf{J}_{d}}=\frac{\sigma \mathbf{E}}{\omega \varepsilon \mathbf{E}}=\frac{\sigma}{\omega \varepsilon}&=\frac{\varepsilon^{\prime \prime}}{\varepsilon^{\prime}} \end{aligned}$
            1. [손실 탄젠트](http://www.ktword.co.kr/word/abbr_view.php?nav=2&id=157&m_temp1=4417)

=
#### 8-2.4 구리의 전도도는 $\sigma=5.8 \times 10^{7}[\mathrm{S} / \mathrm{m}]$ 이다. 표피두께를 주파수에 대한 함수로 표시하라.
1. 개념
    1. 양도체 = Good Conductor = 좋은 도체에서 표피두께 $\delta$는 다음과 같다.
    $\delta=\frac{1}{\sqrt{\pi f \mu \sigma}}=\frac{1}{\alpha}=\frac{1}{\beta}$
1. 풀이
    1. $\delta=\frac{1}{\sqrt{\pi f \mu_{o} \sigma}}=\frac{1}{\sqrt{\pi f \times 4 \pi \times 10^{-7} \times 5.8 \times 10^{7}}}$
    $\delta=\frac{0.066}{\sqrt{f}} [m]$

#### 8-2.4 앞 그림을 참조하여 $w \times l\left[\mathrm{m}^{2}\right]$ 의 도체 면을 통과하여 도체 안으로 전달되는 총 전력을 구하라.
1. 개념
    1. $\langle\mathbf{S}\rangle$
    $=\mathbf{a}_{z} \frac{E_{o}^{2}}{2} \sqrt{\frac{\varepsilon}{\mu}}$
    $\quad \quad \quad$ 양도체의 영역 $z \ge 0$에서 다음 식을 만족한다.
    $=\frac 12 E \times H$
    $=\frac{1}{2} \operatorname{Re}\left[\left(\mathbf{a}_{x} E_{o} e^{-z / \delta} e^{-j z / \delta}\right) \times\left(\mathbf{a}_{y} \frac{\sigma \delta}{1+j} E_{o} e^{-z / \delta} e^{-j z / \delta}\right)^{* }\right]$
    $=\frac{1}{2} \operatorname{Re}\left[\mathbf{a}_{z} E_{o}^{2} \frac{\sigma \delta(1+j)}{2} e^{-2 z / \delta}\right]$
    $=\mathbf{a}_{z} \frac{\sigma \delta}{4} E_{o}^{2} e^{-2 z / \delta}$

    1. 시간평균 전력밀도 * 전력 = 총 전력
    $<S> \times S = P$
1. 풀이
    1. 시간평균 전력밀도 \<S>를 구한다.
        1. $\langle\mathbf{S}\rangle=\mathbf{a}_{z} \frac{\sigma \delta}{4} E_{o}^{2}$
    1. 총 전력을 구한다.
        1. $\langle P\rangle=\int_{x=0}^{1} \int_{y=0}^{w}\langle\mathbf{S}\rangle \cdot d \mathbf{s}=\frac{1}{4} \sigma \delta E_{o}^{2} wl=\frac{1}{4 \sigma} w \delta l J_{o}^{2}$
