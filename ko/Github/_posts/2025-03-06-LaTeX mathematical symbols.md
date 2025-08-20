---
title: "LaTeX 수학 기호"
excerpt: "LaTeX의 수학 기호"

tags: latex math
header:
  teaser: https://images.ctfassets.net/nrgyaltdicpt/2RrzN8eVNXo7w6kd7CBNrs/55d916a167fa65d94441cc215558182c/overleaf-logo-primary.jpg
---

LaTeX는 기본적인 수학 기호 외에도 `\usepackage{amssymb}`와 같은 패키지를 사용하여 더 광범위한 기호를 지원합니다.

[LaTeX 사용법 pdf 다운로드](https://www.cmor-faculty.rice.edu/~heinken/latex/symbols.pdf)

---

# **LaTeX 수학 기호 및 기능**

## 1. **그리스 문자**
`\usepackage{amssymb}` 패키지를 사용하면 더 일반적이지 않은 그리스 문자를 사용할 수 있습니다.

| 연산자        | 결과        | 연산자         | 결과         | 연산자        | 결과         |
| :------------ | :---------- | :------------- | :----------- | :------------ | :----------- |
| `\alpha`      | $\alpha$    | `\iota`        | $\iota$      | `\rho`        | $\rho$       |
| `\beta`       | $\beta$     | `\kappa`       | $\kappa$     | `\sigma`      | $\sigma$     |
| `\gamma`      | $\gamma$    | `\lambda`      | $\lambda$    | `\tau`        | $\tau$       |
| `\delta`      | $\delta$    | `\mu`          | $\mu$        | `\upsilon`    | $\upsilon$   |
| `\epsilon`    | $\epsilon$  | `\nu`          | $\nu$        | `\phi`        | $\phi$       |
| `\zeta`       | $\zeta$     | `\xi`          | $\xi$        | `\chi`        | $\chi$       |
| `\eta`        | $\eta$      | `\omicron`     | $\omicron$   | `\psi`        | $\psi$       |
| `\theta`      | $\theta$    | `\pi`          | $\pi$        | `\omega`      | $\omega$     |

*   **변형 그리스 문자**:
    *   `\varepsilon` ($\varepsilon$)
    *   `\varkappa` ($\varkappa$)
    *   `\varphi` ($\varphi$)
    *   `\varpi` ($\varpi$)
    *   `\varrho` ($\varrho$)
    *   `\varsigma` ($\varsigma$)
    *   `\vartheta` ($\vartheta$)
    *   `\digamma` ($\digamma$)
*   **대문자 그리스 문자**:
    *   `\Delta` ($\Delta$), `\Gamma` ($\Gamma$), `\Lambda` ($\Lambda$), `\Omega` ($\Omega$), `\Phi` ($\Phi$), `\Pi` ($\Pi$), `\Psi` ($\Psi$), `\Sigma` ($\Sigma$), `\Theta` ($\Theta$), `\Upsilon` ($\Upsilon$), `\Xi` ($\Xi$)
*   **히브리어 문자**:
    *   `\aleph` ($\aleph$), `\beth` ($\beth$), `\gimel` ($\gimel$), `\daleth` ($\daleth$)

## 2. **수학적 구성 요소 (Math Constructs)**

| 연산자                 | 결과           | 설명                                                |
| :--------------------- | :------------- | :-------------------------------------------------- |
| `\frac{abc}{xyz}`      | $\frac{abc}{xyz}$ | 분수                                                |
| `\overline{abc}`       | $\overline{abc}$ | 윗줄                                                |
| `\underline{abc}`      | $\underline{abc}$ | 밑줄                                                |
| `\overrightarrow{abc}` | $\overrightarrow{abc}$ | 윗쪽 화살표                                         |
| `\overleftarrow{abc}`  | $\overleftarrow{abc}$ | 아랫쪽 화살표                                       |
| `\sqrt{abc}`           | $\sqrt{abc}$   | 제곱근                                              |
| `\sqrt[n]{abc}`        | $\sqrt[n]{abc}$ | n제곱근                                             |
| `\widehat{abc}`        | $\widehat{abc}$ | 모자 (넓은 윗꺾쇠)                                  |
| `\widetilde{abc}`      | $\widetilde{abc}$ | 물결표 (넓은 물결선)                                |
| `\overbrace{abc}`       | $\overbrace{abc}$ | 윗쪽 묶음                                           |
| `\underbrace{abc}`      | $\underbrace{abc}$ | 아랫쪽 묶음                                         |
| `f'`                   | $f'$           | 프라임 기호 (f prime)                               |

## 3. **구분자 및 크기 조정 (Delimiters and Sizing)**



| 연산자 | 결과 | 연산자 | 결과 | 연산자 | 결과 |
|-|-|-|-|-|-|
| `|`    | &#124;    | `\{`       | $\\{$      | `\lfloor`   | $\lfloor$ | 
| `\vert`     | $\vert$   | `\}`       | $\\}$      | `\rfloor`   | $\rfloor$ |
| `\|`  | $\|$      | `\langle`   | $\langle$ | `\lceil`    | $\lceil$  |
| `\Vert`     | $\Vert$   | `\rangle`   | $\rangle$ | `\rceil`    | $\rceil$  | 
| `/`         | $/$       | `\Uparrow`  |$\Uparrow$ | `\llcorner` |$\llcorner$|
|`\backslash`|$\backslash$| `\uparrow`  |$\uparrow$ | `\lrcorner` |$\lrcorner$|
| `[`         | $[$       |`\Downarrow` |$\Downarrow$|`\ulcorner` |$\ulcorner$|
| `]`         | $]$       |`\downarrow` |$\downarrow$|`\urcorner` |$\urcorner$|

`\left $s1$`과 `\right $s2$` 쌍을 사용하여 구분 기호 $s1$과 $s2$의 높이를 해당 내용의 높이와 맞춘다. 예:

`\left| $expr$ \right|` $\rightarrow$ $\left&#124; expr \right&#124;$

`\left\{ $expr$ \right\}` $\rightarrow$ $\left\\{ expr \right\\}$

`\left\Vert $expr$ \right.` $\rightarrow$ $\left\Vert expr \right.$

## 4. **가변 크기 기호 (Variable-sized symbols)**
디스플레이 모드에서는 기호가 더 크게 표시됩니다.

| 연산자 | 결과 | 연산자 | 결과 | 연산자 | 결과 |
|-|-|-|-|-|-|
| `\sum`      | $\sum$        | `\prod`     | $\prod$       | `\coprod`   | $\coprod$ |
| `\int`      | $\int$        | `\oint`     | $\oint$       | `\iint`     | $\iint$   |
| `\biguplus` | $\biguplus$   | `\bigcap`   | $\bigcap$     | `\bigcup`   | $\bigcup$ |
| `\bigoplus` | $\bigoplus$   | `\bigotimes`| $\bigotimes$  | `\bigodot`  |$\bigodot$ |
| `\bigvee`   | $\bigvee$     | `\bigwedge` | $\bigwedge$   | `\bigsqcup` |$\bigsqcup$|

## 5. **표준 함수 이름 (Standard Function Names)**
함수 이름은 **로마체**로 표시되어야 합니다.
*   **올바른 예**: `\tan(at-n\pi)` $\to \tan(at-n\pi)$
*   **잘못된 예**: `tan(at-n\pi)` $\to tan(at-n\pi)$ (이탤릭체로 표시됨)

**주요 표준 함수 이름**:
`\arccos`, `\arcsin`, `\arctan`, `\arg`, `\cos`, `\cosh`, `\cot`, `\coth`, `\csc`, `\deg`, `\det`, `\dim`, `\exp`, `\gcd`, `\hom`, `\inf`, `\ker`, `\lg`, `\lim`, `\liminf`, `\limsup`, `\ln`, `\log`, `\max`, `\min`, `\Pr`, `\sec`, `\sin`, `\sinh`, `\sup`, `\tan`, `\tanh`

## 6. **이항 연산/관계 기호 (Binary Operation/Relation Symbols)**

*   **이항 연산 기호**:
    *   `\ast` ($\ast$), `\pm` ($\pm$), `\mp` ($\mp$), `\cdot` ($\cdot$), `\circ` ($\circ$), `\bullet` ($\bullet$), `\times` ($\times$), `\div` ($\div$)
    *   `\cap` ($\cap$), `\cup` ($\cup$), `\amalg` ($\amalg$), `\uplus` ($\uplus$), `\odot` ($\odot$), `\ominus` ($\ominus$), `\oplus` ($\oplus$), `\oslash` ($\oslash$), `\otimes` ($\otimes$)
    *   `\wedge` ($\wedge$), `\vee` ($\vee$), `\setminus` ($\setminus$), `\dotplus` ($\dotplus$) 등 다수.
*   **관계 기호**:
    *   `\equiv` ($\equiv$), `\leq` ($\leq$), `\geq` ($\geq$), `\neq` ($\neq$), `\cong` ($\cong$), `\sim` ($\sim$), `\approx` ($\approx$), `\in` ($\in$), `\notin` ($\notin$)
    *   `\subset` ($\subset$), `\supset` ($\supset$), `\subseteq` ($\subseteq$), `\supseteq` ($\supseteq$)
    *   `\prec` ($\prec$), `\succ` ($\succ$), `\preceq` ($\preceq$), `\succeq`
    *   `\perp` ($\perp$), `\parallel` ($\parallel$), `\mid` ($\mid$) 등 다수.
*   **부정 관계 기호**:
    *   `\ncong` ($\ncong$), `\nleq` ($\nleq$), `\ngeq` ($\ngeq$), `\nsubseteq` ($\nsubseteq$), `\nparallel` ($\nparallel$), `\nless` ($\nless$), `\ngtr` ($\ngtr$) 등.

## 7. **화살표 기호 (Arrow Symbols)**

*   **기본 화살표**:
    *   `\leftarrow` ($\leftarrow$), `\rightarrow` ($\rightarrow$), `\uparrow` ($\uparrow$), `\downarrow` ($\downarrow$), `\leftrightarrow` ($\leftrightarrow$), `\updownarrow` ($\updownarrow$)
*   **긴 화살표**:
    *   `\longleftarrow` ($\longleftarrow$), `\longrightarrow` ($\longrightarrow$), `\longleftrightarrow` ($\longleftrightarrow$)
*   **두꺼운 화살표**:
    *   `\Leftarrow` ($\Leftarrow$), `\Rightarrow` ($\Rightarrow$), `\Uparrow` ($\Uparrow$), `\Downarrow` ($\Downarrow$), `\Leftrightarrow` ($\Leftrightarrow$), `\Updownarrow` ($\Updownarrow$)
*   **맵핑 화살표**:
    *   `\mapsto` ($\mapsto$), `\longmapsto` ($\longmapsto$)
*   **갈고리 화살표**:
    *   `\hookleftarrow` ($\hookleftarrow$), `\hookrightarrow` ($\hookrightarrow$)
*   **기타 화살표**:
    *   `\nearrow` ($\nearrow$), `\searrow` ($\searrow$), `\swarrow` ($\swarrow$), `\nwarrow` ($\nwarrow$)
    *   `\leftharpoonup` ($\leftharpoonup$), `\rightharpoonup` ($\rightharpoonup$), `\leftharpoondown` ($\leftharpoondown$), `\rightharpoondown` ($\rightharpoondown$) 등.
*   **부정 화살표**:
    *   `\nleftarrow` ($\nleftarrow$), `\nrightarrow` ($\nrightarrow$), `\nLeftarrow` ($\nLeftarrow$), `\nRightarrow` ($\nRightarrow$), `\nleftrightarrow` ($\nleftrightarrow$), `\nLeftrightarrow` ($\nLeftrightarrow$)

## 8. **기타 기호 (Miscellaneous Symbols)**

*   `\infty` ($\infty$) - 무한대
*   `\forall` ($\forall$) - 모든
*   `\exists` ($\exists$) - 존재
*   `\nabla` ($\nabla$) - 나블라 (델)
*   `\partial` ($\partial$) - 편미분
*   `\emptyset` ($\emptyset$) - 공집합
*   `\prime` ($\prime$) - 프라임
*   `\angle` ($\angle$) - 각도
*   `\triangle` ($\triangle$) - 삼각형
*   `\clubsuit` ($\clubsuit$), `\diamondsuit` ($\diamondsuit$), `\heartsuit` ($\heartsuit$), `\spadesuit` ($\spadesuit$) - 카드 기호
*   `\ell` ($\ell$), `\hbar` ($\hbar$), `\imath` ($\imath$), `\jmath` ($\jmath$) - 특수 문자
*   `\cdots` ($\cdots$), `\vdots` ($\vdots$), `\ddots` ($\ddots$) - 점 세 개 (수평, 수직, 대각선)
*   `\wp` ($\wp$) - 바이어슈트라스 p
*   `\Re` ($\Re$) - 실수부, `\Im` ($\Im$) - 허수부
*   `\Box` ($\Box$), `\square` ($\square$), `\blacklozenge` ($\blacklozenge$), `\blacksquare` ($\blacksquare$) 등.

## 9. **수학 모드 액센트 (Math mode accents)**
문자에 다양한 발음 기호나 특수 표시를 추가합니다.

*   `\acute{a}` ($\acute{a}$) - 엑센트
*   `\bar{a}` ($\bar{a}$) - 바
*   `\breve{a}` ($\breve{a}$) - 브레베
*   `\check{a}` ($\check{a}$) - 체크
*   `\ddot{a}` ($\ddot{a}$) - ë (움라우트)
*   `\dot{a}` ($\dot{a}$) - 닷
*   `\grave{a}` ($\grave{a}$) - 그레이브
*   `\hat{a}` ($\hat{a}$) - 삿갓
*   `\tilde{a}` ($\tilde{a}$) - 물결
*   `\vec{a}` ($\vec{a}$) - 벡터

## 10. **어레이 환경 (Array environment)**
행렬, 연립 방정식, 구간별 정의 함수 등 표 형식의 수학적 내용을 구현하는 데 사용됩니다.

```latex
\begin{array}{cols}
row1 \\
row2 \\
...
rowm
\end{array}
```
*   `cols`: 각 열의 정렬 방식(`l`=좌측, `r`=우측, `c`=중앙)을 지정합니다. `|`를 사용하여 수직선을 그릴 수 있습니다.
*   `&`: 열을 구분합니다.
*   `\\`: 행을 바꿉니다.

**예시**:
*   **행렬**:
    ```latex
    \left( \begin{array}{cc}
    2\tau & 7\phi-\frac{5}{12} \\
    3\psi & \frac{\pi}{8}
    \end{array} \right)
    ```
    결과: $$\left( \begin{array}{cc} 2\tau & 7\phi-\frac{5}{12} \\ 3\psi & \frac{\pi}{8} \end{array} \right)$$

*   **구간별 정의 함수**:
    ```latex
    f(z) = \left\{ \begin{array}{rcl}
    \overline{\overline{z^2}+\cos z} & \mbox{for} & |z|<3 \\
    0 & \mbox{for} & 3\leq|z|\leq5 \\
    \sin\overline{z} & \mbox{for} & |z|>5
    \end{array}\right.
    ```
    결과: $$f(z) = \left\{ \begin{array}{rcl} \overline{\overline{z^2}+\cos z} & \mbox{for} & |z|<3 \\ 0 & \mbox{for} & 3\leq|z|\leq5 \\ \sin\overline{z} & \mbox{for} & |z|>5 \end{array}\right.$$

## 11. **다양한 수학 글꼴 스타일 (Other Math Styles)**
수식 내에서 특정 문자에 특별한 글꼴 스타일을 적용할 수 있습니다.

*   **캘리그라피 글자**: `\mathcal{A}` $\to \mathcal{A}$
*   **칠판 볼드체**: `\mathbb{A}` $\to \mathbb{A}$
*   **프락투어 글자**: `\mathfrak{A}` $\to \mathfrak{A}$
*   **산세리프 글자**: `\mathsf{A}` $\to \mathsf{A}$
*   **볼드체 글자**: `\mathbf{A}` $\to \mathbf{A}$
*   **볼드 이탤릭체**: `\def\mathbi#1{\textbf{\em #1}}` 정의 후 `\mathbi{A}` $\to \textbf{\em A}$

## 12. **수학 모드 글꼴 크기 조정 (Font sizes in Math Mode)**
수식의 크기를 조절하는 명령입니다.

*   `\displaystyle` : 인라인 모드에서도 디스플레이 모드처럼 크게 표시
    *   `{\displaystyle \int f^{-1}(x-x_a)\,dx}` $\to {\displaystyle \int f^{-1}(x-x_a)\,dx}$
*   `\textstyle` : 일반 텍스트 크기로 표시 (기본 인라인 모드 크기)
    *   `{\textstyle \int f^{-1}(x-x_a)\,dx}` $\to {\textstyle \int f^{-1}(x-x_a)\,dx}$
*   `\scriptstyle` : 작은 첨자/아래첨자 크기로 표시
    *   `{\scriptstyle \int f^{-1}(x-x_a)\,dx}` $\to {\scriptstyle \int f^{-1}(x-x_a)\,dx}$
*   `\scriptscriptstyle` : 더 작은 첨자/아래첨자 크기로 표시
    *   `{\scriptscriptstyle \int f^{-1}(x-x_a)\,dx}` $\to {\scriptscriptstyle \int f^{-1}(x-x_a)\,dx}$

이러한 핵심 기능들을 통해 LaTeX는 복잡하고 다양한 수학적 표현을 정교하게 구현할 수 있도록 지원합니다.