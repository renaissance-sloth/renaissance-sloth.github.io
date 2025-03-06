---
title: "LaTeX 수학 기호"
excerpt: "LaTeX의 수학 기호"

tags: latex math mathematics
header:
  teaser: https://images.ctfassets.net/nrgyaltdicpt/2RrzN8eVNXo7w6kd7CBNrs/55d916a167fa65d94441cc215558182c/overleaf-logo-primary.jpg
---
# $\LaTeX$의 수학 기호
더 일반적이지 않은 기호는 기본 $\LaTeX$ (NFSS)에 정의되어 있지 않으며 `\usepackage{amssymb}`가 필요하다.

## 그리스 문자

| 연산자 | 결과 | 연산자 | 결과 | 연산자 | 결과 |
|-|-|-|-|-|-|
| \alpha    | $\alpha$      | \iota     | $\iota$       | \rho      | $\rho$        |
| \beta     | $\beta$       | \kappa    | $\kappa$      | \sigma    | $\sigma$      |
| \gamma    | $\gamma$      | \lambda   | $\lambda$     | \tau      | $\tau$        |
| \delta    | $\delta$      | \mu       | $\mu$         | \upsilon  | $\upsilon$    |
| \epsilon  | $\epsilon$    | \nu       | $\nu$         | \phi      | $\phi$        |
| \zeta     | $\zeta$       | \xi       | $\xi$         | \chi      | $\chi$        |
| \eta      | $\eta$        | \omicron  | $\omicron$    | \psi      | $\psi$        |
| \theta    | $\theta$      | \pi       | $\pi$         | \omega    | $\omega$      |

## $\LaTeX$ 수학 구조

| 연산자 | 결과 | 연산자 | 결과 | 연산자 | 결과 |
|-|-|-|-|-|-|
| \frac{abc}{xyz} | $\frac{abc}{xyz}$ | \overline{abc} | $\overline{abc}$ | \overrightarrow{abc} | $\overrightarrow{abc}$ |
| f' | $f'$ | \underline{abc} | $\underline{abc}$ | \overleftarrow{abc} | $\overleftarrow{abc}$ |
| \sqrt{abc}  | $\sqrt{abc} $ | \widehat{abc} | $\widehat{abc}$ | \overbrace{abc} | $\overbrace{abc}$ |
| \sqrt[n]{abc} | $\sqrt[n]{abc}$ | \widetilde{abc} | $\widetilde{abc}$ | \underbrace{abc} | $\underbrace{abc}$ |
|||||||

## 구분 기호

| 연산자 | 결과 | 연산자 | 결과 | 연산자 | 결과 |
|-|-|-|-|-|-|
| &#124;    | &#124;    | \\{       | $\\{$      | \lfloor   | $\lfloor$ | 
| \vert     | $\vert$   | \\}       | $\\}$      | \rfloor   | $\rfloor$ |
| \\&#124;  | $\|$      | \langle   | $\langle$ | \lceil    | $\lceil$  |
| \Vert     | $\Vert$   | \rangle   | $\rangle$ | \rceil    | $\rceil$  | 
| /         | $/$       | \Uparrow  |$\Uparrow$ | \llcorner |$\llcorner$|
|\backslash|$\backslash$| \uparrow  |$\uparrow$ | \lrcorner |$\lrcorner$|
| [         | $[$       |\Downarrow |$\Downarrow$|\ulcorner |$\ulcorner$|
| ]         | $]$       |\downarrow |$\downarrow$|\urcorner |$\urcorner$|

\left $s1$과 \right $s2$ 쌍을 사용하여 구분 기호 $s1$과 $s2$의 높이를 해당 내용의 높이와 맞춘다. 예:

\left&#124; $expr$ \right&#124;$\rightarrow$ $\left&#124; expr \right&#124;$

\left\\{ $expr$ \right\\} $\rightarrow$ $\left\\{ expr \right\\}$

\left\Vert $expr$ \right. $\rightarrow$ $\left\Vert expr \right.$

## 가변 크기 기호(표시된 공식은 더 큰 버전을 보여준다)

| 연산자 | 결과 | 연산자 | 결과 | 연산자 | 결과 |
|-|-|-|-|-|-|
| \sum      | $\sum$        | \prod     | $\prod$       | \coprod   | $\coprod$ |
| \int      | $\int$        | \oint     | $\oint$       | \iint     | $\iint$   |
| \biguplus | $\biguplus$   | \bigcap   | $\bigcap$     | \bigcup   | $\bigcup$ |
| \bigoplus | $\bigoplus$   | \bigotimes| $\bigotimes$  | \bigodot  |$\bigodot$ |
| \bigvee   | $\bigvee$     | \bigwedge | $\bigwedge$   | \bigsqcup |$\bigsqcup$|

## 표준 함수 이름

함수 이름은 이탤릭체가 아닌 로마자로 표시해야 한다. 예:

\tan(at-n\pi) $\rightarrow \tan(at-n\pi)$ (O)

tan(at-n\pi) $\rightarrow tan(at-n\pi)$ (X)

$\arccos$, $\arcsin$, $\arctan$, $\arg$, $\cos$, $\cosh$, $\cot$, $\coth$, $\csc$, $\deg$, $\det$, $\dim$, $\exp$, $\gcd$, $\hom$, $\inf$, $\ker$, $\lg$, $\lim$, $\ln$, $\log$, $\max$, $\min$, $\Pr$, $\sec$, $\sin$, $\sinh$, $\sup$, $\tan$, $\tanh$

\liminf $\rightarrow\liminf$

\limsup $\rightarrow\limsup$

/TODO()

## 이진 연산/관계 기호
## 화살표 기호
## 기타 기호
## 수학 모드 악센트
## 배열 환경, 예
## 기타 스타일(수학 모드만 해당)
## 글꼴 크기
## 텍스트 모드: 악센트 및 기호