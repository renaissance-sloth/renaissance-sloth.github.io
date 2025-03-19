---
title: "LaTeX Mathematical Symbols"
excerpt: "Mathematical symbols in latex"

tags: latex math mathematics
header:
  teaser: https://images.ctfassets.net/nrgyaltdicpt/2RrzN8eVNXo7w6kd7CBNrs/55d916a167fa65d94441cc215558182c/overleaf-logo-primary.jpg
---
# $\LaTeX$ Mathematical Symbols
The more unusual symbols are not defined in base $\LaTeX$ (NFSS) and require `\usepackage{amssymb}`

## Greek letters

| operator  | result        | operator  | result        | operator  | result        |
|-----------|---------------|-----------|---------------|-----------|---------------|
| \alpha    | $\alpha$      | \iota     | $\iota$       | \rho      | $\rho$        |
| \beta     | $\beta$       | \kappa    | $\kappa$      | \sigma    | $\sigma$      |
| \gamma    | $\gamma$      | \lambda   | $\lambda$     | \tau      | $\tau$        |
| \delta    | $\delta$      | \mu       | $\mu$         | \upsilon  | $\upsilon$    |
| \epsilon  | $\epsilon$    | \nu       | $\nu$         | \phi      | $\phi$        |
| \zeta     | $\zeta$       | \xi       | $\xi$         | \chi      | $\chi$        |
| \eta      | $\eta$        | \omicron  | $\omicron$    | \psi      | $\psi$        |
| \theta    | $\theta$      | \pi       | $\pi$         | \omega    | $\omega$      |

## $\LaTeX$ math construct

| operator | result | operator | result | operator | result |
|-|-|-|-|-|-|
| \frac{abc}{xyz} | $\frac{abc}{xyz}$ | \overline{abc} | $\overline{abc}$ | \overrightarrow{abc} | $\overrightarrow{abc}$ |
| f' | $f'$ | \underline{abc} | $\underline{abc}$ | \overleftarrow{abc} | $\overleftarrow{abc}$ |
| \sqrt{abc}  | $\sqrt{abc} $ | \widehat{abc} | $\widehat{abc}$ | \overbrace{abc} | $\overbrace{abc}$ |
| \sqrt[n]{abc} | $\sqrt[n]{abc}$ | \widetilde{abc} | $\widetilde{abc}$ | \underbrace{abc} | $\underbrace{abc}$ |
|||||||

## Delimiters

| operator | result | operator | result | operator | result |
|-|-|-|-|-|-|
| &#124;    | &#124;    | \\{       | $\\{$      | \lfloor   | $\lfloor$ | 
| \vert     | $\vert$   | \\}       | $\\}$      | \rfloor   | $\rfloor$ |
| \\&#124;  | $\|$      | \langle   | $\langle$ | \lceil    | $\lceil$  |
| \Vert     | $\Vert$   | \rangle   | $\rangle$ | \rceil    | $\rceil$  | 
| /         | $/$       | \Uparrow  |$\Uparrow$ | \llcorner |$\llcorner$|
|\backslash|$\backslash$| \uparrow  |$\uparrow$ | \lrcorner |$\lrcorner$|
| [         | $[$       |\Downarrow |$\Downarrow$|\ulcorner |$\ulcorner$|
| ]         | $]$       |\downarrow |$\downarrow$|\urcorner |$\urcorner$|

Use the pair \left $s1$ and \right $s2$ to match height of delimiters $s1$ and $s2$ to the height of their contents, e.g.,

\left&#124; $expr$ \right&#124;$\rightarrow$ $\left&#124; expr \right&#124;$

\left\\{ $expr$ \right\\} $\rightarrow$ $\left\\{ expr \right\\}$

\left\Vert $expr$ \right. $\rightarrow$ $\left\Vert expr \right.$

## Variable-sized symbols (displayed formulae show larger version)

| operator | result | operator | result | operator | result |
|-|-|-|-|-|-|
| \sum      | $\sum$        | \prod     | $\prod$       | \coprod   | $\coprod$ |
| \int      | $\int$        | \oint     | $\oint$       | \iint     | $\iint$   |
| \biguplus | $\biguplus$   | \bigcap   | $\bigcap$     | \bigcup   | $\bigcup$ |
| \bigoplus | $\bigoplus$   | \bigotimes| $\bigotimes$  | \bigodot  |$\bigodot$ |
| \bigvee   | $\bigvee$     | \bigwedge | $\bigwedge$   | \bigsqcup |$\bigsqcup$|

## Standard Function Names

Function names should appear in Roman, not Italic, e.g.,

\tan(at-n\pi) $\rightarrow \tan(at-n\pi)$ (O)

tan(at-n\pi) $\rightarrow tan(at-n\pi)$ (X)

$\arccos$, $\arcsin$, $\arctan$, $\arg$, $\cos$, $\cosh$, $\cot$, $\coth$, $\csc$, $\deg$, $\det$, $\dim$, $\exp$, $\gcd$, $\hom$, $\inf$, $\ker$, $\lg$, $\lim$, $\ln$, $\log$, $\max$, $\min$, $\Pr$, $\sec$, $\sin$, $\sinh$, $\sup$, $\tan$, $\tanh$

\liminf $\rightarrow\liminf$

\limsup $\rightarrow\limsup$

<!-- /TODO()
## Binary Operation/Relation Symbols
## Arrow symbols
## Miscellaneous symbols
## Math mode accents
## Array environment, examples
## Other Styles (math mode only)
## Font sizes
## Text Mode: Accents and Symbols -->