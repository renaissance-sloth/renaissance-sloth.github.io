---
title: "플라즈마 물리학 소개"
excerpt: 책 기준 1장 내용
tags: physics plasma intro
header:
  teaser: https://encrypted-tbn2.gstatic.com/images?q=tbn:ANd9GcRZplqQsfMnOSyYRjjzr6zXYM-zkt-rm1oeXLK_GKncRFjhT2_n
---

# 1. Introduction

## 1.1 Occurrence of Plasmas in Nature

현재 우주는 69%의 암흑 에너지, 27%의 암흑 물질, 그리고 1%의 일반 물질로 구성되어 있다고 여겨진다. 우리가 하늘에서 볼 수 있는 것은 방사선을 방출하는 플라즈마 상태에 있는 일반 물질의 일부에 불과하다. 물리학에서의 plasma는 혈장(blood plasma)과는 다르며, 적어도 하나의 전자가 원자에서 떨어져 나가 양전하를 띤 원자핵(ion)만이 남은 “이온화된” 기체를 의미한다. 때때로 plasma는 “물질의 네 번째 상태”라고도 불린다. 고체를 가열하면 액체가 되고, 액체를 더 가열하면 기체가 된다. 기체를 추가로 가열하면 이온화되어 plasma가 된다. plasma는 전하를 띤 이온과 전자로 이루어져 있기 때문에 전기장이 도처에 존재하며, 입자들은 서로 부딪히는 경우뿐만 아니라 먼 거리에서도 전기장을 통해 “충돌”하게 된다.

수력학(hydrodynamics)은 예를 들어, 관을 통해 흐르는 물이나 요트 경주의 배 주변을 흐르는 물의 흐름, 또는 비행기 날개의 거동을 설명하는 데 사용되며, 이미 복잡한 학문 분야이다. plasma의 전기장이 추가되면 가능한 운동의 범위는 특히 자기장이 존재하는 경우 더욱 확장된다.

Plasma는 일반적으로 진공 상태에서만 존재한다. 그렇지 않으면 공기가 plasma를 냉각시켜 이온과 전자가 다시 결합하여 중성 원자가 되어 버린다. 실험실에서는 진공 챔버 내의 공기를 펌프로 제거해야 한다. 그러나 우주의 진공 상태에서는 많은 기체가 plasma 상태에 있으며, 우리는 그것을 볼 수 있다. 별의 내부와 대기, 가스 성운, 전체 은하계는 plasma 상태이기 때문에 관측 가능하다. 그러나 지구에서는 대기가 plasma의 존재를 제한하여 몇 가지 예외적인 경우를 제외하고는 plasma를 자연적으로 접할 수 없다. 예를 들면, 번개의 섬광, 오로라의 부드러운 빛, 형광등의 빛, 또는 plasma TV의 픽셀 등이 있다. 우리는 plasma가 자연적으로 발생하지 않는 우주의 일부에서 살고 있으며, 그렇기 때문에 생존이 가능하다.

이 현상은 다음의 **Saha 방정식**을 통해 이해할 수 있다. 이 방정식은 열평형 상태에 있는 기체에서 예상되는 이온화 정도를 나타낸다:

$$
\frac{n_i}{n_n} \sim \frac{1}{n_i} \exp\left( -\frac{U_i}{KT} \right)
\tag{1.1}
$$

여기서 $n_i$와 $n_n$은 각각 이온화된 원자와 중성 원자의 밀도(단위: m⁻³), $T$는 기체의 온도(K 단위), $K$는 Boltzmann 상수, $U_i$는 이온화 에너지(즉, 원자에서 가장 바깥 전자를 떼어내는 데 필요한 줄 단위의 에너지)이다. 이 책에서는 mks 단위계(국제단위계)를 사용한다. 상온에서의 일반적인 공기에 대해 $n_n ≈ 3 × 10^{25} \, \text{m}^{-3}$, $T ≈ 300\, \text{K}$, $U_i = 14.5\, \text{eV}$ (질소에 해당)라고 가정할 수 있으며, 여기서 $1\, \text{eV} = 1.6 × 10^{-19}\, \text{J}$이다. 방정식 (1.1)에 의해 예측되는 이온화 분율 $n_i/(n_n + n_i) ≈ n_i / n_n$은 극히 작다:

온도가 상승해도 이온화 정도는 $U_i$가 $KT$보다 몇 배 이상 클 때까지는 낮은 상태를 유지한다. 이후 $n_i / n_n$이 급격히 증가하여 기체는 plasma 상태가 된다. 온도가 더 올라가면 $n_n < n_i$가 되며, plasma는 결국 완전 이온화된다. 이것이 수백만 도의 온도를 지닌 천체에 plasma가 존재하는 이유이며, 지구에는 존재하지 않는 이유이다. 생명은 이러한 plasma—우리가 여기서 말하는 형태의 plasma—와는 쉽게 공존할 수 없다. 고온에서 자연적으로 발생하는 plasma는 “물질의 네 번째 상태”라는 명칭이 붙은 이유이기도 하다.

우리는 이 책에서 **Saha 방정식**을 중점적으로 다루지는 않겠지만, 그 물리적 의미를 짚고 넘어가야 한다. 기체 내의 원자들은 다양한 열 에너지를 가지고 있으며, 원자가 이온화되기 위해서는 우연히 충분히 높은 에너지를 지닌 충돌을 겪어야 한다. 차가운 기체에서는 그러한 고에너지 충돌이 드물다. 평균보다 훨씬 높은 에너지를 얻기 위해서는 일련의 “유리한” 충돌을 겪어야 하기 때문이다. 식 (1.1)의 지수 항은 고속 원자의 수가 $U_i / KT$에 따라 지수적으로 감소함을 나타낸다. 일단 원자가 이온화되면, 전자를 만나기 전까지 전하를 띠게 되며, 전자를 만나면 대부분 재결합하여 다시 중성 원자가 된다. 이 재결합 속도는 전자 밀도—즉 $n_i$—에 의존한다. 따라서 평형 상태에서의 이온화 분율은 $n_i$가 증가할수록 감소해야 하며, 이것이 식 (1.1) 우변에 $n_i^{-1}$ 항이 존재하는 이유이다. 성간 매질의 plasma는 $n_i$ 값이 매우 작기 때문에—약 $1\, \text{cm}^{-3}$ 수준—재결합 속도가 낮아 존재할 수 있다.

## 1.2 Definition of Plasma

모든 이온화된 기체가 plasma인 것은 아니다. 어느 기체든 항상 소량의 이온화는 존재한다. 다음의 정의가 유용하다:

**A plasma is a quasineutral gas of charged and neutral particles which exhibits collective behavior.**

여기서 “quasineutral”과 “collective behavior”의 의미를 정의해야 한다. Quasineutrality의 개념은 **1.4절**에서 명확히 설명될 것이다. 먼저 “collective behavior”의 의미를 다음과 같이 설명할 수 있다.

예를 들어, 일반 공기 중의 분자 하나에 작용하는 힘을 생각해 보자. 이 분자는 중성이므로 전자기적 힘은 작용하지 않으며, 중력은 무시할 수 있을 정도로 작다. 따라서 이 분자는 다른 분자와 충돌할 때까지는 방해받지 않고 움직인다. 이러한 충돌이 입자의 운동을 지배한다. 중성 기체에 거시적인 힘(예: 스피커에 의한 음파)이 작용하면, 이 힘은 충돌을 통해 개별 원자에 전달된다. 그러나 plasma는 전하를 띤 입자들로 구성되어 있어 상황이 전혀 다르다. 이러한 전하들이 이동하면서 국소적으로 양전하 또는 음전하가 집중되는 현상이 발생하며, 이는 전기장을 유도한다. 전하의 운동은 전류를 생성하고, 이는 자기장을 유도한다. 이러한 전기장과 자기장은 멀리 떨어진 다른 전하 입자의 운동에도 영향을 준다.

두 개의 약간 전하를 띤 plasma 영역 A와 B가 거리 $r$만큼 떨어져 있다고 가정하자 (그림 1.1 참조). A와 B 사이의 쿨롱력은 $1/r^2$에 비례하여 감소한다. 그러나 주어진 입체각(즉, $\Delta r / r$이 일정할 경우)에서 B 영역 내 A에 영향을 줄 수 있는 plasma의 부피는 $r^3$에 비례하여 증가한다. 따라서 plasma는 매우 멀리 떨어진 영역 간에도 상호작용을 한다. 이 장거리 쿨롱력이 plasma에 다양한 운동 양식을 가능하게 하며, plasma physics라는 학문 분야를 풍부하게 만든다. 실제로 가장 흥미로운 결과는 **“collisionless” plasmas**에서 나타나는데, 여기서는 장거리 전자기력이 일반적인 국소 충돌에 의한 힘보다 훨씬 크기 때문에 충돌의 영향을 무시할 수 있다. “Collective behavior”란 국소 조건뿐만 아니라 멀리 떨어진 plasma 영역의 상태에 의해서도 결정되는 운동을 의미한다.

![Fig. 1.1](https://)  
*그림 1.1. Plasma 내 정전기력의 장거리 작용을 설명하는 도해*

“Plasma”라는 단어는 어원상 부적절해 보일 수 있다. 이 단어는 그리스어 πλάσμα, −ατος, τό에서 유래하며, 이는 ‘형성된 것’ 혹은 ‘조작된 것’을 의미한다. 그러나 plasma는 collective behavior를 가지기 때문에 외부 영향에 순응하지 않으며, 오히려 자율적인 행동을 하는 듯한 특성을 보이곤 한다.

## 1.3 Concept of Temperature

본격적으로 논의를 진행하기에 앞서, “온도”에 대한 물리적 개념을 복습하고 확장해 두는 것이 좋다. 열평형 상태에 있는 기체는 모든 속도를 지닌 입자들을 포함하고 있으며, 이러한 속도들의 가장 확률이 높은 분포는 **Maxwellian distribution**으로 알려져 있다. 단순화를 위해, 입자가 한 방향(1차원)으로만 이동할 수 있는 기체를 고려하자. (이것은 완전히 의미 없는 설정은 아니다. 예를 들어 강한 자기장이 존재하면 전자는 자기장 선을 따라 한 방향으로만 움직일 수 있다.) 1차원 Maxwellian distribution은 다음과 같다:

$$
f\,du = A\,\exp\left( -\frac{mu^2}{2KT} \right)\,du
\tag{1.2}
$$

여기서 $f\,du$는 속도가 $u$와 $u + du$ 사이에 있는 입자의 밀도(단위: $\text{m}^{-3}$), $mu^2$는 운동에너지, $K$는 Boltzmann 상수이다.

여기서 대문자 $K$를 사용하는 이유는, 소문자 $k$는 파동의 전파 상수로 남겨두기 위함이다. 전체 밀도 $n$—즉 입자의 총수(m³당)—는 다음과 같이 주어진다 (그림 1.2 참조):

$$
n = \int_{-\infty}^{\infty} f\,du
\tag{1.3}
$$

정규화 상수 $A$는 다음 관계로부터 $n$과 관련된다 (문제 1.2 참조):

$$
A = n \left( \frac{m}{2\pi KT} \right)^{1/2}
\tag{1.4}
$$

이 분포의 폭은 상수 $T$에 의해 특징지어지며, 이 $T$를 우리는 **온도**라고 부른다. $T$의 정확한 의미를 보기 위해, 이 분포에서 입자의 평균 운동에너지를 계산할 수 있다:

$$
E_{\text{av}} = \frac{1}{n} \int_{-\infty}^{\infty} \frac{1}{2}mu^2\,f\,du
\tag{1.5}
$$

여기서 다음과 같이 정의하자:

$$
v_{\text{th}} = \left( \frac{2KT}{m} \right)^{1/2}
\tag{1.6}
$$

그러면 식 (1.2)는 다음과 같이 쓸 수 있으며, 식 (1.5)도 간단해진다.

분자의 적분은 부분적분으로 계산할 수 있으며,

분모와 분자의 적분이 서로 상쇄되어 다음을 얻게 된다:

$$
E_{\text{av}} = \frac{1}{2}KT
\tag{1.7}
$$

즉, 평균 운동에너지는 $KT$의 절반이다.

이 결과는 3차원으로 쉽게 확장된다. 이때의 Maxwell 분포는 다음과 같다:

$$
f(u,v,w)\,dudvdw = A\,\exp\left( -\frac{m(u^2 + v^2 + w^2)}{2KT} \right)\,dudvdw
\tag{1.8}
$$

여기서:

$$
A = n \left( \frac{m}{2\pi KT} \right)^{3/2}
\tag{1.9}
$$

평균 운동에너지는 다음과 같다:

$$
E_{\text{av}} = \frac{1}{n} \int \frac{1}{2}m(u^2 + v^2 + w^2)\,f\,dudvdw
$$

이 표현은 $u$, $v$, $w$에 대해 대칭적이다. Maxwell 분포는 등방성이기 때문에 분자의 세 항은 동일하다. 따라서 첫 항만 계산하여 3을 곱하면 된다:

이전에 얻은 결과를 사용하면,

$$
E_{\text{av}} = \frac{3}{2}KT
\tag{1.10}
$$

일반적으로, **각 자유도당 평균 에너지는 $KT/2$이다.**

$T$와 $E_{\text{av}}$ 사이의 관계가 매우 밀접하므로, plasma physics에서는 온도를 에너지 단위로 나타내는 것이 일반적이다. 자유도의 개수에 따라 혼동을 방지하기 위해, $E_{\text{av}}$가 아니라 $KT$에 해당하는 에너지가 온도의 지표로 사용된다. 예를 들어 $KT = 1\,\text{eV} = 1.6 × 10^{-19}\,\text{J}$라면:

$$
1\,\text{eV} = 1.6 × 10^{-19}\,\text{J}
\tag{1.11}
$$

따라서 **2-eV plasma**란 $KT = 2\,\text{eV}$, 즉 3차원에서는 $E_{\text{av}} = 3\,\text{eV}$인 plasma를 의미한다.

한 plasma가 동시에 여러 개의 서로 다른 온도를 가질 수 있다는 사실은 흥미롭다. 종종 이온과 전자가 각각 서로 다른 Maxwell 분포를 가지며 온도 $T_i$, $T_e$도 다르다. 이는 이온들끼리 또는 전자들끼리의 충돌률이 이온–전자 충돌보다 높기 때문에 발생한다. 따라서 각각의 종은 자체적으로 열평형 상태에 있을 수 있지만, plasma가 수명을 다하기 전에는 두 온도가 일치하지 않을 수도 있다. 자기장 $B$가 존재할 때, 단일 종(예: 이온)조차도 두 개의 서로 다른 온도를 가질 수 있다. 이는 이온이 자기장 방향과 수직 방향에서 받는 힘이 Lorentz 힘에 의해 서로 다르기 때문이다. $B$에 수직인 속도 성분과 평행한 성분은 서로 다른 Maxwell 분포에 속하게 되며, 각각 $T_\perp$와 $T_\parallel$로 표시된다.

온도의 개념을 논의하는 이 시점에서 “고온”이라는 것이 반드시 “많은 열”을 의미하는 것은 아님을 명확히 해 둘 필요가 있다. 사람들은 형광등 내부의 전자 온도가 약 20,000°K에 달한다는 것을 알고 놀라곤 한다. “그렇게 뜨겁게 느껴지지 않는데!” 물론 여기에선 **열용량(heat capacity)**도 고려되어야 한다. 형광등 내의 전자 밀도는 대기압 기체보다 훨씬 낮으며, 열속도에 따라 벽에 도달하는 전자가 전달하는 총열량은 그리 크지 않다. 누구나 손에 담뱃재가 떨어졌을 때의 경험이 있을 것이다. 그 온도는 화상을 입히기에 충분하지만, 전달된 총열량이 적기 때문에 심각하지 않다. 많은 실험실 plasma의 온도는 $10^6$K (100 eV) 수준이지만, 밀도가 $10^{18} - 10^{19}\,\text{m}^{-3}$ 정도이므로 벽의 가열은 심각한 문제가 되지 않는다.

## 1.4 Debye Shielding

Plasma의 가장 근본적인 특성 중 하나는 외부에서 가해진 전기 퍼텐셜을 **차폐(shielding)** 할 수 있는 능력이다. 예를 들어, 배터리에 연결된 두 개의 전하를 지닌 구체를 plasma 안에 삽입해 전기장을 만들려 한다고 하자 (그림 1.3 참조). 이때 음전하를 띤 구는 이온을 끌어당기고, 양전하를 띤 구는 전자를 끌어당겨, 거의 즉시 음전하 주위에는 양이온 구름, 양전하 주위에는 전자 구름이 형성된다. (단, plasma가 표면에서 재결합하지 않도록 절연층이 있거나, 퍼텐셜을 유지할 수 있을 만큼 충분히 큰 배터리가 있다고 가정한다.)

만약 plasma가 차갑고 열운동이 없다면, 구름 속의 전하 수는 구체의 전하 수와 동일하며 차폐는 완벽하게 이루어진다. 이 경우, plasma 내부(구름 외부)에는 전기장이 존재하지 않게 된다. 그러나 온도가 유한할 경우, 구름의 외곽에서는 전기장이 약하므로, 입자들이 그 퍼텐셜 우물에서 빠져나갈 정도의 열에너지를 가지고 있을 수 있다. 따라서 구름의 “가장자리”는 입자의 퍼텐셜 에너지가 $KT$에 해당하는 지점에서 형성되며, 차폐는 완전하지 않다. 전기 퍼텐셜이 $KT/e$ 정도가 되면 plasma 내부로 침투할 수 있고, 유한한 전기장이 존재하게 된다.

![Fig. 1.3](https://)  
*그림 1.3: Debye 차폐*

이제 이러한 전하 구름의 대략적인 두께를 계산해 보자. $x = 0$ 평면에 있는 투명한 격자가 퍼텐셜 $\phi_0$를 유지하고 있다고 하자 (그림 1.4). 우리는 $\phi(x)$를 계산하려 한다. 단순화를 위해, 이온과 전자의 질량비 $M/m$이 무한대라고 가정하여 이온은 움직이지 않고 양의 정전하 배경을 형성한다고 하자. 좀 더 정확히 말하면, $M/m$이 충분히 커서 실험 시간 척도에서 이온의 관성이 그들의 운동을 억제할 수 있다고 보자. 1차원 Poisson 방정식은 다음과 같다:

$$
\frac{d^2 \phi}{dx^2} = -\frac{e}{\varepsilon_0}(n_i - n_e)
\tag{1.12}
$$

멀리 떨어진 곳에서의 밀도를 $n_\infty$라고 하면, 이온 밀도는 일정하여 $n_i = n_\infty$이다.

전기 퍼텐셜 에너지 $q\phi$가 존재할 때, 전자의 분포 함수는 다음과 같이 주어진다:

$$
f(u) = A \exp\left( -\frac{mu^2/2 - e\phi}{KT} \right)
\tag{1.13}
$$

이 식은 여기서 증명하지는 않지만, 물리적으로 자명한 결과를 제시한다: 퍼텐셜 에너지가 큰 영역에서는 도달 가능한 입자의 수가 적어지므로, 밀도는 줄어든다. $u$에 대해 $f(u)$를 적분하고, $q = -e$ 및 $\phi \to 0$일 때 $n_e = n_\infty$임을 사용하면:

$$
n_e = n_\infty \exp\left( \frac{e\phi}{KT_e} \right)
$$

이 식은 이후 **3.5절**에서 물리적 통찰을 통해 다시 유도될 것이다. 위 식을 식 (1.12)에 대입하면:

$$
\frac{d^2 \phi}{dx^2} = -\frac{e}{\varepsilon_0} \left[ n_\infty - n_\infty \exp\left( \frac{e\phi}{KT_e} \right) \right]
$$

만약 $\left| \frac{e\phi}{KT_e} \right| \ll 1$ 이라면, 지수함수를 Taylor 급수로 전개하여:

$$
\exp\left( \frac{e\phi}{KT_e} \right) \approx 1 + \frac{e\phi}{KT_e}
\tag{1.14}
$$

격자 근처의 영역에서는 $\left| \frac{e\phi}{KT_e} \right|$가 클 수 있으므로 단순화가 어렵다. 다행히도 퍼텐셜은 이 영역에서 급격히 감소하므로, 구름의 두께(이른바 **sheath**)에 큰 기여를 하지 않는다. 따라서 식 (1.13)의 선형 항만 유지하면:

$$
\frac{d^2 \phi}{dx^2} = \frac{e^2 n_\infty}{\varepsilon_0 KT_e} \phi
\tag{1.15}
$$

여기서 다음과 같이 정의하자:

$$
\lambda_D^2 = \frac{\varepsilon_0 KT_e}{e^2 n}
\tag{1.16}
$$

여기서 $n = n_\infty$, $KT_e$는 줄 단위이며, 전자 온도를 eV 단위로 쓸 경우 이를 $T_e$[eV]로 표기하기도 한다.

이제 식 (1.14)의 해는 다음과 같이 쓸 수 있다:

$$
\phi(x) = \phi_0 \exp\left( -\frac{x}{\lambda_D} \right)
\tag{1.17}
$$

이때 **$\lambda_D$는 Debye 길이(Debye length)**라 불리며, 차폐 거리 또는 sheath 두께를 나타내는 척도이다.

밀도가 증가하면 $\lambda_D$는 감소하는데, 이는 plasma의 각 층이 더 많은 전자를 포함하므로 당연한 결과이다. 또한 $\lambda_D$는 $KT_e$가 증가하면 증가한다. 열운동이 없다면 전하 구름은 무한히 얇아지게 된다. Debye 길이의 정의에는 전자 온도만이 사용되는데, 이는 일반적으로 이온보다 전자가 훨씬 더 민첩하게 움직이며 전하의 과잉 또는 부족을 통해 차폐를 수행하기 때문이다. 특수한 경우를 제외하면 항상 그렇다 (문제 1.5 참조).

식 (1.16)의 다른 유용한 형태는 다음과 같다:

$$
\lambda_D = 743 \left( \frac{T_e [\text{eV}]}{n [\text{m}^{-3}]} \right)^{1/2} \, \text{m}
\tag{1.18}
$$

이제 **quasineutrality**의 정의가 가능해진다. 만약 시스템의 전형적인 크기 $L$이 $\lambda_D$보다 훨씬 크다면, 지역적인 전하 집중이나 외부 퍼텐셜이 유도되더라도 이는 $\lambda_D$ 길이 내에서 차폐되며, 시스템의 대부분 영역에는 큰 퍼텐셜이나 전기장이 존재하지 않게 된다. 벽 또는 장애물에서의 sheath를 제외하고는, $\nabla^2 \phi$는 매우 작으며, $n_i = n_e$는 보통 $10^{-6}$ 정도의 정확도로 성립한다. $KT/e$ 정도의 퍼텐셜이 형성되기 위해서는 극히 적은 전하 불균형만 있으면 충분하다. 따라서 plasma는 **quasineutral**, 즉 다음 조건을 만족한다고 본다:

$$
n_i \approx n_e \approx n
$$

여기서 $n$은 보통 **plasma 밀도**라 부른다. 다만 전자기력이 모두 소멸할 만큼 완전히 중성이어서는 안 된다.

따라서 어떤 이온화된 기체가 plasma로 간주되기 위한 조건 중 하나는, 밀도가 충분히 커서 **$\lambda_D \ll L$**이 되어야 한다는 것이다.

Debye 차폐는 단일 종만 존재하는 시스템에서도 (변형된 형태로) 발생한다. 예를 들어, klystron이나 magnetron 내의 전자 흐름, 사이클로트론의 양성자 빔 등이 이에 해당한다. 이 경우, 입자의 국소적 밀집은 큰 전기장을 유발하며, 차폐되지 않는다. 외부 퍼텐셜(예: 탐침 전극)에 의해 유도된 전위는, 전극 주변의 밀도 변화에 의해 차폐된다. 이러한 단일 종 시스템(비중성 plasma)은 엄밀히 말해 plasma는 아니지만, plasma physics의 수학적 기법을 이용해 분석할 수 있다.

한편, 전자가 지나치게 뜨거워 자주 충돌하지 않는 경우에는 Debye 차폐가 깨질 수 있다. 이후 장에서 보겠지만, 전자가 매우 고온일 경우 충돌은 드물어진다. 이 경우, 양이온의 양전하에 끌린 전자는 빠른 속도로 비스듬히 접근하면서 행성 주위를 도는 위성처럼 궤도를 형성하게 된다. 이러한 현상은 Langmuir probe를 다룰 때 더 자세히 설명된다. 어떤 사람들은 이를 **역차폐(anti-shielding)**라고 부르기도 한다.

## 1.5 The Plasma Parameter

앞서 제시한 Debye 차폐 그림은 전하 구름 내에 입자가 충분히 존재할 때만 통계적으로 유효한 개념이다. 구름(또는 Debye sphere) 내에 단지 한두 개의 입자만 있다면, Debye 차폐 개념은 성립하지 않는다. 식 (1.17)을 이용하여 Debye 구 내 입자 수 $N_D$를 계산하면 다음과 같다:

$$
N_D = \frac{4\pi}{3} n \lambda_D^3
\tag{1.19}
$$

따라서, plasma가 **collective behavior**를 나타내기 위해서는 위에서 제시한 $\lambda_D \ll L$ 조건 외에도 다음 조건을 만족해야 한다:

$$
N_D \gg 1
\tag{1.20}
$$

이는 Debye 구 내에 많은 입자가 존재해야 한다는 조건이다.

## 1.6 Criteria for Plasmas

지금까지 어떤 이온화된 기체가 plasma로 간주되기 위한 두 가지 조건을 제시하였다:

1. $\lambda_D \ll L$
2. $N_D \gg 1$

여기에 세 번째 조건을 추가해야 한다. 이는 **충돌(collisions)**과 관련이 있다.

예를 들어, 비행기 제트 배기에서 나오는 약하게 이온화된 기체는 이온과 전자가 중성 원자와 너무 자주 충돌하기 때문에, 이들의 운동은 전자기력보다는 일반적인 유체역학적 힘에 의해 지배된다. 만약 어떤 전형적인 plasma 진동의 주파수를 $\omega$라고 하고, 중성 원자와의 평균 충돌 시간(또는 자유 평균 시간)을 $\tau$라고 하면, 이 기체가 중성 기체가 아닌 plasma로 작용하기 위해서는 다음 조건이 필요하다:

$$
\omega \tau > 1
$$

즉, 전자기적 효과가 충돌 효과보다 우세해야 한다는 뜻이다.

결론적으로, 어떤 이온화된 기체가 **plasma**로 간주되기 위해서는 다음 **세 가지 조건**을 모두 만족해야 한다:

1. $$ \lambda_D \ll L $$
2. $$ N_D \gg 1 $$
3. $$ \omega \tau > 1 $$

## 1.7 Applications of Plasma Physics

Plasma는 밀도 $n$과 온도 $KT_e$라는 두 매개변수로 특성화될 수 있다. Plasma의 응용 범위는 $n$과 $KT_e$의 측면에서 **매우 광범위**하다: $n$은 $10^6$에서 $10^{34}\,\text{m}^{-3}$까지, $KT_e$는 $0.1$에서 $10^6$ eV까지 28자리 및 7자리의 오더에 걸쳐 다양하다. 이 절에서는 이러한 응용 분야 중 일부를 간단히 소개한다.

밀도의 엄청난 범위는, 예를 들어 공기와 물이 $10^3$배의 밀도 차이를 가지고, 물과 백색왜성은 $10^5$배, 중성자별은 물보다 $10^{15}$배 더 밀도가 크다는 점과 비교하면 더 인상적이다. 그런데 이러한 $10^{28}$ 범위에 걸친 기체성 plasma들은 모두 동일한 일련의 방정식들로 설명될 수 있다. 이는 양자역학적 효과를 무시할 수 있는 **고전역학(classical physics)**만으로도 충분하다는 것을 의미한다.

### 1.7.1 Gas Discharges (Gaseous Electronics)

Plasma에 대한 가장 초기의 연구는 1920년대 **Langmuir**, **Tonks** 및 그들의 공동연구자들에 의해 이루어졌다. 이 연구는 많은 전류를 흐르게 할 수 있는 진공관 개발을 목적으로 수행되었으며, 따라서 이온화된 기체가 필요했다. 이 연구는 약하게 이온화된 글로우 방전(glow discharge)과 양전주(positive column)를 대상으로 했으며, 일반적으로 $KT_e \simeq 2\,\text{eV}$, $10^{14} < n < 10^{18}\,\text{m}^{-3}$의 조건에서 진행되었다. 이곳에서 **차폐 현상**이 처음으로 관찰되었으며, 전극을 둘러싼 sheath는 육안으로 어두운 층으로 확인할 수 있었다.

반도체 이전 시대에는 gas discharge는 수은 정류기(mercury rectifier), 수소 thyratron, ignitron, 스파크 갭(spark gap), 아크 용접, 네온 및 형광등, 그리고 번개 방전 등에서만 접할 수 있었다. 그러나 최근 20년간의 반도체 산업의 폭발적인 성장은 gas discharge 연구를 작은 학문 분야에서 **거대한 산업 분야**로 탈바꿈시켰다. 컴퓨터 및 소형 디지털 기기의 핵심 부품인 **칩**은 plasma 없이는 제조할 수 없다. 현재는 일반적으로 **radiofrequency 전력**으로 구동되는 **부분 이온화 plasma(gas discharge)**가 반도체 제조 공정의 식각(etching) 및 증착(deposition)에 활용되고 있다.

### 1.7.2 Controlled Thermonuclear Fusion

현대 plasma physics의 출발점은 1952년경 수소폭탄의 **핵융합(fusion)** 반응을 제어하여 원자로로 만들자는 제안에서 비롯되었다. 1958년 제네바에서 개최된 핵심 회의에서는 각국이 자국의 핵융합 프로그램을 처음으로 공개하였다. 핵융합 에너지를 얻기 위해서는 **30 keV**의 plasma를 **1초 이상** 자기장으로 가두는 것이 필요하다. 이 목표를 위해 각국은 독자적인 연구를 수행해 왔으며, 2007년에는 **ITER** 프로젝트가 출범했다.

**ITER**는 **International Thermonuclear Experimental Reactor**의 약자로, 프랑스에서 건설 중인 거대 실험장치이며, 7개국의 공동 자금으로 운영된다. 우연히도 ITER는 라틴어로 “길”을 의미한다. 이는 인류가 **지구온난화와 석유 부족 문제를 2050년까지 해결하기 위한 길**이다. 제네바에서 제안된 여러 “자기 병(magnetic bottle)” 중에서 구소련의 **TOKAMAK**만이 살아남았고, 이는 현재 ITER의 기본 구성이기도 하다. ITER의 첫 plasma 발생은 **2021년경**으로 예정되어 있다.

핵융합 연료는 중수소(deuterium)이며, 이는 자연 상태의 물 속에 약 6000분의 1 비율로 존재한다. 주요 반응은 중수소(D)와 삼중수소(T) 사이의 반응으로, 다음과 같다:

(여기에 반응식이 들어갈 수 있음)

이 반응 단면적(cross section)은 **입사 에너지가 5 keV 이상**일 때만 의미 있는 값을 갖는다. 가속된 D 입자를 타겟에 충돌시키는 방식은 에너지 손실이 커서 핵융합에 적합하지 않다. 대신 **10 keV 이상의 온도에서 plasma를 형성**하여 충분한 수의 입자가 반응 단면적이 극대화되는 **40 keV** 근방에 도달하도록 해야 한다. 이러한 **고온 plasma의 가열과 유지**가 바로 1952년 이후 plasma physics가 급속도로 발전한 주된 이유이다.

### 1.7.3 Space Physics

Plasma physics의 또 다른 중요한 응용 분야는 **지구 주변 우주 환경**에 대한 연구이다. 태양으로부터는 **solar wind(태양풍)**라 불리는 **전하를 띤 입자 흐름**이 지속적으로 방출되며, 이는 지구의 자기장 영역인 **magnetosphere(자기권)**에 충돌한다. 자기권은 이 방사선으로부터 지구를 보호하는 역할을 하지만, 동시에 그 형태는 solar wind에 의해 왜곡된다. Solar wind의 전형적인 plasma 매개변수는 다음과 같다:

- 밀도: $n = 9 \times 10^6\, \text{m}^{-3}$  
- 이온 온도: $KT_i = 10\, \text{eV}$  
- 전자 온도: $KT_e = 12\, \text{eV}$  
- 자기장 세기: $B = 7 \times 10^{-9}\, \text{T}$  
- 흐름 속도: $450\, \text{km/s}$

**Ionosphere(전리층)**는 고도 약 50 km에서 10 지구 반경($R_E$)까지 확장되어 있으며, 약하게 이온화된 plasma로 구성되어 있다. 이곳의 밀도는 고도에 따라 $n \leq 10^{12}\, \text{m}^{-3}$까지 다양하며, 온도는 약 $0.1\, \text{eV}$ 정도이다. 태양풍은 지구의 자기장을 밤쪽으로 길게 늘어난 **magnetotail** 형태로 변화시키며, 여기서 자기장의 선들이 다시 연결(reconnect)되어 이온을 가속할 수 있다. 이 내용은 이후 장에서 자세히 다룬다.

**Van Allen radiation belts**는 적도 상공에 존재하는 두 개의 입자 고리로서, 지구의 자기장에 의해 입자들이 포획되어 있다. 이곳의 plasma 매개변수는 다음과 같다:

- 밀도: $n \leq 10^9\, \text{m}^{-3}$  
- 전자 온도: $KT_e \leq 1\, \text{keV}$  
- 이온 온도: $KT_i \approx 1\, \text{eV}$  
- 자기장: $B \approx 500 \times 10^{-9}\, \text{T}$

또한, $n = 10^3\, \text{m}^{-3}$, $KT_e = 40\, \text{keV}$의 고온 성분이 존재하며, 일부 이온은 수백 MeV의 에너지를 가진다.

다른 행성 탐사 결과, plasma 현상이 존재함이 밝혀졌다. 수성(Mercury), 금성(Venus), 화성(Mars)에서는 plasma 현상이 거의 없지만, **목성(Jupiter)**과 **토성(Saturn)** 같은 거대 행성과 그들의 위성들에서는 번개 등에 의해 plasma가 생성될 수 있다. 2013년에는 **Voyager 1**호가 태양계 경계에 도달했으며, 이 시점에서 **plasma 주파수(plasma frequency)**의 증가가 관측됨으로써 그 사실이 확인되었다.

### 1.7.4 Modern Astrophysics

별의 내부와 대기는 온도가 매우 높아 **plasma 상태**로 존재한다. 예를 들어, 태양 중심부의 온도는 약 **2 keV**로 추정되며, 이곳에서 발생하는 **열핵 반응(thermonuclear reactions)**이 태양의 복사 에너지의 원천이다. 태양의 코로나(corona)는 밀도가 낮은 plasma이며, 온도는 최대 **200 eV**에 이른다. 성간 매질(interstellar medium)은 $n \approx 10^6\, \text{m}^{-3}$ (즉, $1\, \text{cm}^{-3}$) 수준의 이온화 수소를 포함하고 있다.

다양한 plasma 이론은 **우주선(cosmic rays)**의 가속 과정을 설명하는 데 사용되어 왔다. 은하 내의 별들은 전하를 띠고 있지는 않지만, 이들은 마치 plasma를 이루는 입자처럼 행동하며, **plasma 운동론(plasma kinetic theory)**을 이용하여 은하의 형성 과정을 예측할 수 있다.

**전파 천문학(radio astronomy)**은 수많은 복사원의 존재를 밝혔으며, 이들 대부분은 plasma로부터 기인한 것이라 생각된다. 예를 들어, **Crab nebula(게 성운)**는 풍부한 plasma 현상을 보여주는 주요 천체이며, **자기장(magnetic field)**이 존재함이 확인되어 있다. 또한, 여기에는 가시광 영역에서 맥동하는 **pulsar(펄서)**도 존재한다. 현재 pulsar에 대한 이론은 그것을 **초신성 붕괴로 형성된 고속 자전하는 중성자별**로 간주하며, 표면에서 **synchrotron radiation**을 방출하는 plasma에 의해 복사가 발생한다고 본다.

최근에는 **활성 은하핵(active galactic nuclei)** 및 **블랙홀(black holes)**이 주요 관심 대상으로 떠올랐다. 오늘날의 astrophysics는 **plasma physics**에 대한 이해 없이는 설명할 수 없는 분야가 되었다.

### 1.7.5 MHD Energy Conversion and Ion Propulsion

다시 지구로 돌아와, plasma physics의 두 가지 실용적 응용을 살펴보자. 첫 번째는 **자기유체역학(Magnetohydrodynamics, MHD)**을 이용한 에너지 변환이다. 이는 **고밀도 plasma 제트**를 자기장 내에서 가로질러 흐르게 하여 **전기를 생성**하는 방식이다 (그림 1.5 참조). 이때 **Lorentz 힘 $q\,\mathbf{v} \times \mathbf{B}$**에 의해 이온은 위로, 전자는 아래로 휘어지며, 전극 사이에 전위차가 형성된다. 이를 통해 전류를 추출할 수 있으며, 기존의 열기관(heat cycle) 없이 전력을 생성할 수 있다.

![Fig. 1.5](https://)  
*그림 1.5: MHD 발전기의 원리*

보다 중요하게는, 이 원리를 **역방향으로 적용**하여 **우주 탐사용 엔진**을 개발할 수 있다. 그림 1.6에서 보듯, 두 전극에 전압을 가하면 plasma에 전류가 흐르며, $j \times B$ 힘이 plasma를 로켓의 뒷부분으로 밀어낸다. 이에 대한 반작용(force of reaction)으로 로켓은 가속된다. 최근에는 **Hall thruster**라는 장치가 개발되어, 자기장을 이용해 전자를 정지시키고 높은 전압으로 이온을 뒤로 가속하여 우주선을 추진한다. 별도로 방출되는 전자들은 우주선의 전기적 중성을 유지하는 역할을 한다. 그렇지 않으면 우주선은 높은 전위로 충전되어 버릴 것이다.

![Fig. 1.6](https://)  
*그림 1.6: 우주선 추진을 위한 plasma 제트 엔진의 원리*

### 1.7.6 Plasma Propulsion for Satellites

앞 절에서 소개한 Hall thruster는 NASA와 ESA를 포함한 여러 우주 기관에서 적극적으로 개발되고 있다. Hall thruster는 전자를 가로 자기장에 의해 전진하지 못하도록 제한한 뒤, 전기장을 가하여 양이온만을 가속하는 방식이다. 방출된 전자는 음전하로 남아 로켓 전체의 전기적 중성을 유지하게 한다. 이러한 장치는 특히 정지궤도 위성이나 행성 간 탐사용 우주선에서 매우 유용하다.

이 장치의 장점은 전통적인 화학 추진 방식보다 **비추력(specific impulse)**이 훨씬 크다는 점이다. 이는 더 적은 연료로 더 많은 속도를 낼 수 있다는 뜻이다. 단점은 작은 추력(thrust)밖에 얻을 수 없다는 점인데, 이는 우주에서는 큰 문제가 되지 않는다. 진공 상태에서는 약한 힘이라도 장시간 동안 작용하면 속도를 계속 높일 수 있기 때문이다.

오늘날 많은 통신 위성은 **플라즈마 추진 시스템**을 장착하고 있으며, 이는 자세 제어나 궤도 유지에 효과적으로 사용된다. 지구 저궤도에서 소형 인공위성을 대상으로 하는 **큐브셋(CubeSat)**에서도 플라즈마 추진 기술이 활발히 연구되고 있다.

### 1.7.7 Plasma in Industry and Medicine

플라즈마는 산업 및 의료 분야에서도 다양한 방식으로 활용되고 있다. 대표적인 예는 반도체 제조 공정에서의 **플라즈마 식각(plasma etching)**과 **플라즈마 증착(plasma deposition)** 기술이다. 반도체 웨이퍼의 표면을 미세한 패턴으로 가공하거나 얇은 막을 형성하는 과정에서 플라즈마는 핵심 역할을 한다. 이때 사용되는 플라즈마는 일반적으로 저온, 저밀도 상태이며, radiofrequency 전원에 의해 유지된다.

의료 분야에서는 플라즈마가 살균, 조직 절개, 지혈 등 다양한 수술 및 치료 기법에 응용된다. **차가운 대기압 플라즈마(cold atmospheric plasma)**는 살아 있는 조직을 손상시키지 않으면서 박테리아, 바이러스, 암세포 등을 선택적으로 제거할 수 있어, 차세대 치료 수단으로 각광받고 있다.

## 1.8 Basic Equations of Plasma Physics

앞서 언급했듯이, 플라즈마의 거동은 밀도 $n$과 전자 온도 $T_e$를 통해 기술된다. 그러나 플라즈마는 전기장 $\mathbf{E}$와 자기장 $\mathbf{B}$에 의해 영향을 받고, 또 그 자체가 전류를 생성하여 $\mathbf{E}$와 $\mathbf{B}$를 변화시킨다. 따라서 **Maxwell 방정식**이 기본적인 틀로 사용된다. 또한, 플라즈마 입자들은 충돌을 제외하면 고전 역학에 따라 움직이므로, **Newton의 운동 법칙**이나 **Boltzmann 방정식**이 함께 사용된다.

플라즈마를 기술하는 주요 수학적 모델은 다음 세 가지로 분류할 수 있다:

1. **Single-particle model (단일 입자 모형)**  
   이 모형은 $\mathbf{E}$와 $\mathbf{B}$가 주어졌을 때 한 입자의 운동을 추적하는 방식이다. 이를 통해 **gyration**, **magnetic mirror motion**, **guiding center drift** 등과 같은 현상을 분석할 수 있다.

2. **Fluid model (유체 모형)**  
   플라즈마를 연속체로 보고 밀도 $n(\mathbf{r}, t)$, 속도 $\mathbf{u}(\mathbf{r}, t)$, 온도 $T(\mathbf{r}, t)$ 등의 물리량을 사용하여 기술한다. 이를 위해 **연속 방정식**, **운동량 보존 법칙**, **에너지 방정식** 등을 사용하며, 여기에 Maxwell 방정식을 결합하여 **magnetohydrodynamics (MHD)**라는 체계를 형성한다.

3. **Kinetic model (운동론적 모형)**  
   이 모형은 분포 함수 $f(\mathbf{r}, \mathbf{v}, t)$를 도입하여 입자들의 통계적 거동을 기술한다. 가장 기본이 되는 방정식은 **Vlasov 방정식**으로, 입자 간 충돌이 없는 경우에 적용된다. 여기에 충돌 항을 추가하면 **Boltzmann 방정식** 또는 **Fokker–Planck 방정식**이 된다.

이 책에서는 먼저 단일 입자 모형을 소개하고, 이어서 유체 모형과 운동론적 모형을 설명할 것이다. 각각의 모형은 다양한 플라즈마 조건에 따라 서로 다른 장점과 적용 범위를 갖는다. 예를 들어, MHD는 거시적 스케일의 밀도가 높은 플라즈마에 적합하며, kinetic theory는 충돌이 거의 없는 우주 플라즈마나 고온 핵융합 플라즈마를 이해하는 데 필수적이다.