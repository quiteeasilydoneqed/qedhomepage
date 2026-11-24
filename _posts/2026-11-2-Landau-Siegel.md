---
layout: post
title: "Landau-Siegel零点不存在"
subtitle: ""
header-img: "img/post-bg-infinity.jpg"
header-mask: 0.3
math: true
no-em-replace: true
tags:
  - 解析数论
  - 数论
---

## 简介

<div style="border: 3px solid #000; padding: 10px;" markdown="1">

**定理 1 (Landau定理).** 存在一个常数 $c>0$, 使得对任意正整数 $q\ge 3$, 在模$q$的所有 Dirichlet 特征中, 至多存在一个特征 $\chi$, 使$L(s,\chi)$ 有一个实零点 $\beta\in(0,1)$ 满足 

$$
(1-\beta)\log q\le c.
$$



</div>


以上定理中的特征称为对应于常数$c$的例外特征, 零点称为对应于常数$c$的例外零点或Landau-Siegel零点, 这样的特征若存在, 则必然是非主实特征. Landau-Siegel零点被认为是广义Riemann猜想的潜在反例, 排除Landau-Siegel零点的存在性是解析数论中的一个长期重大问题.

2026年10月1日, AI 公司 OpenAI [1] 发表预印本, 声称其证明了 Landau–Siegel 零点不存在, 随后, Banks [2], Kerr [3], Green [4], Pescador [5], Barreto [6]等人对这篇论文进行了简化和整理, Tao 在其博客[7]中介绍了 Green 的方法. 本文是基于 Barreto 论文的详细介绍, 证明关键是一个特定和式的上界估计, 目前看来, Barreto 论文中的方法是最简便的, 并且得到的结果也是最强的.

OpenAI 关于 $L$ 函数在半平面 $\operatorname{Re}(s)>7/8$ 内无零点的证明, 已蕴含 Landau–Siegel 零点不存在, 但该证明与本文的方法基本独立.

本文的写作使用了 DeepSeek 和 ChatGPT 辅助.

## 定理的证明

<div style="border: 3px solid #000; padding: 10px;" markdown="1">

**符号说明:**

- $x$是大于等于$3$的实数;

- $q$是大于等于$3$的正整数;

- $\chi$是模$q$的实原特征;

- $d$是满足$d\neq1$, $\vert d\vert \le q$, $d$无平方因子且 

$$
\chi(p)=\left(\frac{d}{p}\right),\qquad p\nmid q,\ p\neq2,
$$

 的整数, 其中等式右边是Kronecker符号, 由$q\ge3$和$\chi$实且本原知这样的$d$是存在的;

- $B=2\sqrt{2x}\;q^{1/4}$;

- $R$定义为平面格点上的矩形 

$$
R=\left\lbrace (u,v)\in\mathbb{Z}^2:0\le u<\frac{B}{2},\ 0\le v<\frac{B}{2\sqrt{q}}\right\rbrace ;
$$



- $\alpha\_i=u\_i+v\_i\sqrt{d}\in \mathbb{Z}[\sqrt{d}]$, 其中$(u\_i,v\_i)$为$R$中的点, 按任意顺序编号, 记$\overline{\alpha\_i}=u\_i-v\_i\sqrt{d}$为共轭元;

- $k=\lceil\log \left(x^2B\right)\rceil$;

- $T$定义为 

$$
T=\left\lbrace (r,s)\in\mathbb{Z}^2\_{\ge0}:r+ks<x\right\rbrace ;
$$



- $f\_{r,s}$定义为二元多项式 

$$
f\_{r,s}(z,w)=z^rw^s;
$$



- $\mathcal{M}$是一个$\vert T\vert $行, $2\vert R\vert \lceil2x/k\rceil$列的矩阵, 按如下方式定义: 首先, 对每个$(r,s)\in T$, $1\le i\le \vert R\vert $, $0\le j<2x/k$, 取矩阵元 

$$
\partial\_z^j f\_{r,s}(z,w)\vert \_{(z,w)=(\alpha\_i,\overline{\alpha\_i})},
$$

 这样得到一个$\vert T\vert $行, $\vert R\vert \left\lceil2x/k\right\rceil$列的矩阵, 由于其中每个矩阵元都是$\mathbb{Z}[\sqrt{d}]$中的数, 则可以写成$a+b\sqrt{d}$的形式, 将每个矩阵元拆成两个矩阵元$a, b\in\mathbb{Z}$, 就得到了$\vert T\vert $行, $2\vert R\vert \lceil2x/k\rceil$列的整数矩阵, 即矩阵$\mathcal{M}$;

- $D$是矩阵$\mathcal{M}$的某个$\vert T\vert $阶子方阵的行列式.

</div>


关于这些定义, 有以下几点简单的观察.

<div style="border: 3px solid #000; padding: 10px;" markdown="1">

- 

$$
\log B=\frac{1}{2}\log x+\frac{1}{4}\log q+\frac{3}{2}\log 2=\frac{1}{2}\log x+\frac{1}{4}\log q+O(1);
$$



- 

$$
\vert R\vert =\left\lceil\frac{B}{2}\right\rceil\left\lceil\frac{B}{2\sqrt{q}}\right\rceil\ge\frac{B^2}{4\sqrt{q}}=2x;
$$



- 由$\vert d\vert \le q$知 

$$
\vert \overline{\alpha\_i}\vert \le\vert \alpha\_i\vert \le u\_i+v\_i\sqrt{\vert d\vert }< \frac{B}{2}+\frac{B}{2\sqrt{q}}\sqrt{q}=B;
$$



- 由$k=\lceil\log \left(x^2B\right)\rceil$知 

$$
\frac{5}{2}\log x+\frac{1}{4}\log q+\frac{3}{2}\log2\le k\le \frac{5}{2}\log x+\frac{1}{4}\log q+\frac{3}{2}\log2+1,
$$

 若假设$x\ge e^3$且$x\ge\sqrt{q}$, 则直接计算可知 

$$
3<\frac{15}{2}+\frac{1}{4}\log 3+\frac{3}{2}\log2\le k\le 3\log x+\frac{3}{2}\log2+1\le x;
$$



- 在$\vert T\vert $中, $r$至多有$\lceil x\rceil$种取法, $s$至多有$\lceil x/k\rceil$种取法, 所以 

$$
\vert T\vert \le (x+1)\left(\frac{x}{k}+1\right)=\frac{x^2+x}{k}+x+1<\frac{2x^2}{k}+2x,
$$

 而 

$$
2\vert R\vert \left\lceil\frac{2x}{k}\right\rceil\ge \frac{8x^2}{k},
$$

 故 

$$
\frac{8x^2}{k}> \frac{2x^2}{k}+2x
$$

 等价于 

$$
3x>k,
$$

 而$k<x$, 所以$\vert T\vert <2\vert R\vert \lceil2x/k\rceil$, 即矩阵$\mathcal{M}$的列数大于行数.

</div>


<div style="border: 3px solid #000; padding: 10px;" markdown="1">

**引理 1.** 假设$x\ge\max\lbrace e^3,\sqrt{q}\rbrace $, 则矩阵$\mathcal{M}$的$\vert T\vert $行在$\mathbb{Q}$上线性无关.

</div>


<div style="border: 3px solid #000; padding: 10px;" markdown="1">

**证明.** 若不然, 假设$\lbrace c\_{r,s}\rbrace \_{(r,s)\in T}$是不全为$0$的有理数, 使得 

$$
\sum\_{(r,s)\in T}c\_{r,s}\partial\_z^j f\_{r,s}(z,w)\vert \_{(z,w)=(\alpha\_i,\overline{\alpha\_i})}=0
$$

 对所有的$i$和$j$都成立. 设函数 

$$
F(z,w)=\sum\_{(r,s)\in T}c\_{r,s}z^rw^s\in\mathbb{Q}[z,w],
$$

 由$T$的定义知$\deg\_zF<x$, $\deg\_wF<x/k$.

对每个$i$, 一元多项式$F(z,\overline{\alpha\_i})$的前$\lceil2x/k\rceil-1$阶导都在$z=\alpha\_i$处为$0$, 所以有两种可能, 要么$F(z,\overline{\alpha\_i})\equiv0$, 要么$z=\alpha\_i$是$F(z,\overline{\alpha\_i})$的至少$\lceil2x/k\rceil$重零点. 现将$F$看做$\mathbb{Q}[z][w]$中的元素, 写成 

$$
F(z,w)=\sum\_{s=0}^{\deg\_wF}\mathcal{F}\_s(z)w^s,\qquad\mathcal{F}\_s(z)\in \mathbb{Q}[z],
$$

 若$F(z,\overline{\alpha\_i})\equiv0$, 这说明$\overline{\alpha\_i}$是$F(z,w)$作为$\mathbb{Q}(z)$系数多项式的一个根, 而由$\deg\_wF<x/k$知它至多有$[x/k]$个根, 因此对于其余至少 

$$
\vert R\vert -\left[\frac{x}{k}\right]\ge 2x-\frac{x}{k}> \frac{5}{3}x>x
$$

 个$i$来说, 只有可能$z=\alpha\_i$是$F(z,\overline{\alpha\_i})$的至少$\lceil2x/k\rceil$重零点.

令 

$$
V=\operatorname{span}\_\mathbb{C}\left\lbrace F(z,\overline{\alpha\_i})\right\rbrace \_{i=1}^{\vert R\vert },\qquad V'=\operatorname{span}\_\mathbb{C}\left\lbrace \mathcal{F}\_s(z)\right\rbrace \_{s=0}^{\deg\_wF},
$$

 它们均是$\mathbb{C}[z]$的子空间, 由 

$$
F(z,\overline{\alpha\_i})=\sum\_{s=0}^{\deg\_wF}\mathcal{F}\_s(z)\overline{\alpha\_i}^s
$$

 知$V$中每个元素都是$V'$中元素的线性组合, 所以 

$$
\dim\_\mathbb{C}V\le\dim\_\mathbb{C}V'\le\deg\_wF+1< \frac{x}{k}+1.
$$



现取$V$的一组基$\lbrace g\_b\rbrace \_{b=1}^{\dim\_\mathbb{C}V}$, 其中诸$g\_b$均为首一多项式, 并且次数两两不同, 显然这样的基总是存在的. 由$\deg\_zF<x$知$\deg\_zg\_b<x$对所有$b$成立. 定义Wronskian行列式 

$$
W(z)=\det\left(\frac{\mathrm{d}^a}{\mathrm{d}z^a}g\_b(z)\right)\_{\substack{0\le a< \dim\_\mathbb{C}V\\1\le b\le\dim\_\mathbb{C}V}},
$$

 显然$W(z)$的次数不超过 

$$
\sum\_{b=1}^{\dim\_\mathbb{C}V}\deg\_z g\_b-\sum\_{a=0}^{\dim\_\mathbb{C}V-1}a< x\dim\_\mathbb{C}V,
$$

 由于$\mathrm{d}^a(g\_b(z))/\mathrm{d}z^a$的最高次项系数为$(\deg\_zg\_b)!/(\deg\_zg\_b-a)!$, 所以$W(z)$的最高次项系数为 

$$
\det\left(\frac{(\deg\_zg\_b)!}{(\deg\_zg\_b-a)!}\right)\_{\substack{0\le a< \dim\_\mathbb{C}V\\1\le b\le\dim\_\mathbb{C}V}}=\det\left(a!\binom{\deg\_zg\_b}{a}\right)\_{\substack{0\le a< \dim\_\mathbb{C}V\\1\le b\le\dim\_\mathbb{C}V}},
$$

 若该行列式为$0$, 则一定存在一组不全为$0$的复数$\lambda\_a$使得 

$$
\sum\_{a=0}^{\dim\_\mathbb{C}V-1}\lambda\_aa!\binom{\deg\_zg\_b}{a}=0
$$

 对所有$b$成立, 设多项式 

$$
P(t)=\sum\_{a=0}^{\dim\_\mathbb{C}V-1}\lambda\_aa!\binom{t}{a}\not\equiv0,
$$

 由于 

$$
a!\binom{t}{a}=t(t-1)\cdots(t-a+1)
$$

 是$t$的$a$次多项式, 所以$P(t)$的次数不大于$\dim\_\mathbb{C}V-1$, 而$P(t)$却有$\dim\_\mathbb{C}V$个不同的根$\deg\_z g\_b$, 矛盾, 因此$W(z)\not\equiv0$, 并且次数小于$x\dim\_\mathbb{C}V$.

任取一个$i$使得$z=\alpha\_i$是$F(z,\overline{\alpha\_i})$的至少$\lceil2x/k\rceil$重零点, 将它扩充为$V$的一组基, 设为 

$$
\lbrace F(z,\overline{\alpha\_i}),h\_2(z),\dots,h\_{\dim\_\mathbb{C}V}(z)\rbrace ,
$$

 设这组基的Wronskian行列式为$W'(z)$, 则它与$W(z)$只差一个非零复数. 在行列式$W'(z)$中, 第一列为 

$$
(F(z,\overline{\alpha\_i}),\partial\_zF(z,\overline{\alpha\_i}),\dots,\partial\_z^{\dim\_\mathbb{C}V-1}F(z,\overline{\alpha\_i}))^{T},
$$

 将行列式按第一列展开即知$z=\alpha\_i$是$W'(z)$的至少$\lceil2x/k\rceil-\dim\_\mathbb{C}V+1$重零点, 从而也是$W(z)$的至少$\lceil2x/k\rceil-\dim\_\mathbb{C}V+1$重零点. 由于$\dim\_\mathbb{C}V$是整数且$\dim\_\mathbb{C}V<x/k+1$, 所以$\dim\_\mathbb{C}V\le\lceil x/k\rceil$, 故 

$$
2\dim\_\mathbb{C}V-2\le2\left\lceil \frac{x}{k}\right\rceil-2< \frac{2x}{k}\le\left\lceil\frac{2x}{k}\right\rceil,
$$

 由于两边都是整数, 所以 

$$
2\dim\_\mathbb{C}V-2\le\left\lceil\frac{2x}{k}\right\rceil-1,
$$

 则有 

$$
\left\lceil\frac{2x}{k}\right\rceil-\dim\_\mathbb{C}V+1\ge\dim\_\mathbb{C}V.
$$



由于使得$z=\alpha\_i$是$F(z,\overline{\alpha\_i})$的至少$\lceil2x/k\rceil$重零点的$i$的个数严格大于$x$, 所以$W(z)$的零点总重数严格大于 

$$
x\left(\left\lceil\frac{2x}{k}\right\rceil-\dim\_\mathbb{C}V+1\right)\ge x\dim\_\mathbb{C}V,
$$

 而这与$W(z)$的次数小于$x\dim\_\mathbb{C}V$矛盾, 因此假设中的$\lbrace c\_{r,s}\rbrace \_{(r,s)\in T}$不存在, 即矩阵$\mathcal{M}$的$\vert T\vert $行在$\mathbb{Q}$上线性无关. 

</div>


<div style="border: 3px solid #000; padding: 10px;" markdown="1">

**引理 2.** 假设$x\ge\max\lbrace e^3,\sqrt{q}\rbrace $, 取$\mathcal{M}$的一个$\vert T\vert $阶子方阵, 其行列式非零, 设为$D\neq0$, 则对任意素数$p$, 若满足$k\le p\le x$且$\chi(p)=-1$, 就有 

$$
p^{\sum\_{(r,s)\in T}[r/p]}\mid D.
$$



</div>


<div style="border: 3px solid #000; padding: 10px;" markdown="1">

**证明.** 首先由上一引理知这样的子方阵是存在的, 记为$\mathcal{N}$, 并且由于$\mathcal{M}$中的元素都是整数, 所以$D=\det\mathcal{N}\in\mathbb{Z}$.

由于$\chi(p)=-1$, 所以$(p,q)=1$, 即$p\nmid q$, 故有 

$$
\chi(p)=\left(\frac{d}{p}\right),
$$

 由二次剩余的Euler判别法知 

$$
-1\equiv\left(\frac{d}{p}\right)\equiv d^{(p-1)/2}\pmod p,
$$

 所以由Fermat小定理知 

$$
\alpha\_i^p\equiv\left(u\_i+v\_i\sqrt d\right)^p\equiv u\_i^p+v\_i^p\left(\sqrt d\right)^p\equiv u\_i+v\_id^{(p-1)/2}\sqrt d\equiv u\_i-v\_i\sqrt d\equiv\overline{\alpha\_i}\pmod{p\mathbb Z[\sqrt d]},
$$

 因此多项式$z^p-w$在$(\alpha\_i,\overline{\alpha\_i})$处的值在$p\mathbb{Z}[\sqrt{d}]$中, 此外显然其各阶导$\partial\_z^n(z^p-w)=p(p-1)\cdots(p-n+1)z^{p-n}$在$(\alpha\_i,\overline{\alpha\_i})$处的值也在$p\mathbb{Z}[\sqrt{d}]$中.

对每个$(r,s)\in T$, 令 

$$
h=\left[\frac{r}{p}\right],
$$

 考虑线性映射 

$$
z^rw^s\mapsto z^{r-ph}(z^p-w)^hw^s,
$$

 使用二项式定理展开得 

$$
z^{r-ph}(z^p-w)^h w^s=\sum\_{l=0}^h(-1)^l\binom{h}{l} z^{r-pl}w^{s+l}=z^rw^s+\sum\_{l=1}^h(-1)^l\binom{h}{l} z^{r-pl}w^{s+l},
$$

 每个新增单项式 $z^{r-pl}w^{s+l}$ 都满足 

$$
(r-pl)+k(s+l)=r+ks+l(k-p)\le r+ks<x,
$$

 故$(r-pl,s+l)$仍在 $T$ 中, 且 $z$ 的次数 $r-pl<r$.

此前并未规定$\mathcal{M}$中$\vert T\vert $行具体如何排列, 不妨设按$z$的次数升序排列, 则每个元素由$z^rw^s$变为$z^{r-ph}(z^p-w)^hw^s$相当于给$\mathcal{M}$左乘了一个方阵, 设为$\mathcal{L}$, 而且该方阵是下三角的, 对角元均为$1$, 因此$\det\mathcal{L}=1$, 故$\det(\mathcal{LN})=D$. 在新矩阵$\mathcal{LN}$中, 每个矩阵元是 

$$
\partial\_z^j\left(z^{r-ph}(z^p-w)^hw^s\right)\vert \_{(z,w)=(\alpha\_i,\overline{\alpha\_i})}
$$

 在基$\lbrace 1,\sqrt{d}\rbrace $下的第一分量或第二分量. 由 Leibniz 法则知$\partial\_z^j\left(z^{r-ph}(z^p-w)^hw^s\right)$展开后的每一项都至少含一些$z^p-w$或其导数, 总共$h$个, 而$z^p-w$及其导数在$(\alpha\_i,\overline{\alpha\_i})$处的值都在$p\mathbb{Z}[\sqrt{d}]$中, 所以$\partial\_z^j\left(z^{r-ph}(z^p-w)^hw^s\right)\vert \_{(z,w)=(\alpha\_i,\overline{\alpha\_i})}$在$p^h\mathbb{Z}[\sqrt{d}]$中, 即矩阵$\mathcal{LN}$中$(r,s)$对应的行中每个元素都被$p^h=p^{[r/p]}$整除, 从而 

$$
p^{\sum\_{(r,s)\in T}[r/p]}\mid \det(\mathcal{LN})=D,
$$

 引理得证. 

</div>


<div style="border: 3px solid #000; padding: 10px;" markdown="1">

**定理 2.** 设正整数$q\ge3$, $\chi$是模$q$的实原特征, 则对任意$x\ge3$, 有 

$$
\sum\_{\substack{p\le x\\\chi(p)=-1}}\frac{\log p}{p}\le \frac{1}{2}\log x+\frac{1}{4}\log q+\log\log x+O(1).
$$



</div>


<div style="border: 3px solid #000; padding: 10px;" markdown="1">

**证明.** 当$x<e^3$时, 

$$
\sum\_{\substack{p\le x\\\chi(p)=-1}}\frac{\log p}{p}\le\sum\_{p\le x}\frac{\log p}{p}=O(1),
$$

 定理显然成立, 当$x<\sqrt{q}$时, 由Mertens定理知 

$$
\sum\_{\substack{p\le x\\\chi(p)=-1}}\frac{\log p}{p}\le\sum\_{p\le x}\frac{\log p}{p}=\log x+O(1)<\frac{1}{2}\log x+\frac{1}{4}\log q+O(1),
$$

 定理亦成立, 因此以下假设$x\ge\max\lbrace e^3,\sqrt{q}\rbrace $.

由$\vert \overline{\alpha\_i}\vert \le\vert \alpha\_i\vert \le B$知$\left\vert \partial\_z^j f\_{r,s}(z,w)\vert \_{(z,w)=(\alpha\_i,\overline{\alpha\_i})}\right\vert \le r(r-1)\cdots(r-j+1)B^{r+s}\le r^jB^{r+s}$, 由$r<x$, $s<x/k$ 和 $j<2x/k$知$\left\vert \partial\_z^j f\_{r,s}(z,w)\vert \_{(z,w)=(\alpha\_i,\overline{\alpha\_i})}\right\vert \le x^{2x/k}B^{r+x/k}=B^r(x^2B)^{x/k}$, 由于$k=\lceil\log \left(x^2B\right)\rceil$, 所以 

$$
(x^2B)^{x/k}=\exp\left(\frac{x}{k}\log (x^2B)\right)\le\exp\left(\frac{x}{\log (x^2B)}\log (x^2B)\right)=e^x,
$$

 所以$\mathcal{N}$中$(r,s)$对应的行中每个矩阵元的模长都不超过$B^re^x$, 由Hadamard不等式知 

$$
D^2\le \prod\_{(r,s)\in T}\vert T\vert B^{2r}e^{2x},
$$

 故 

$$
\log \vert D\vert \le \sum\_{(r,s)\in T}\left(r\log B+x+\frac{1}{2}\log \vert T\vert \right)=\log B\sum\_{(r,s)\in T}r+\vert T\vert x+\frac{\vert T\vert }{2}\log \vert T\vert ,
$$

 已知 

$$
\vert T\vert <\frac{2x^2}{k}+2x\ll\frac{x^2}{k},
$$

 而显然矩形 

$$
\left\lbrace (r,s)\in\mathbb{Z}^2:\frac{x}{3}<r<\frac{2x}{3},\, 0\le s<\frac{x}{3k}\right\rbrace \subseteq T,
$$

 故 

$$
\sum\_{(r,s)\in T}r \gg \frac{x}{3}\cdot \frac{x}{3}\cdot\frac{x}{3k}=\frac{x^3}{27k}\gg x\vert T\vert ,
$$

 

$$
\vert T\vert \log \vert T\vert \ll \frac{x^2\log x}{k}\ll\frac{x^3}{k}\ll\sum\_{(r,s)\in T}r,
$$

 所以有 

$$
\log \vert D\vert \le\log B\sum\_{(r,s)\in T}r+O\left(\sum\_{(r,s)\in T}r\right).
$$



由于$[r/p]>r/p-1$, 求和得 

$$
\sum\_{(r,s)\in T}\left[\frac{r}{p}\right]>\frac{1}{p}\sum\_{(r,s)\in T}r-\vert T\vert ,
$$

 而由前一引理知 

$$
p^{\sum\_{(r,s)\in T}[r/p]}\mid D
$$

 对所有$k\le p\le x$, $\chi(p)=-1$的素数$p$都成立, 所以 

$$
\log \vert D\vert \ge \sum\_{\substack{k\le p\le x\\ \chi(p)=-1}}\log p\sum\_{(r,s)\in T}\left[\frac{r}{p}\right]>\sum\_{\substack{k\le p\le x\\ \chi(p)=-1}}\frac{\log p}{p}\sum\_{(r,s)\in T}r-\sum\_{\substack{k\le p\le x\\ \chi(p)=-1}}\log p\vert T\vert ,
$$

 而由素数定理知 

$$
\sum\_{\substack{k\le p\le x\\ \chi(p)=-1}}\log p\vert T\vert \ll\vert T\vert \sum\_{\substack{p\le x}}\log p\ll x\vert T\vert \ll \sum\_{(r,s)\in T}r,
$$

 所以有 

$$
\sum\_{\substack{k\le p\le x\\ \chi(p)=-1}}\frac{\log p}{p}\sum\_{(r,s)\in T}r<\log \vert D\vert +O\left(\sum\_{(r,s)\in T}r\right)\le \log B\sum\_{(r,s)\in T}r+O\left(\sum\_{(r,s)\in T}r\right),
$$

 

$$
\sum\_{\substack{k\le p\le x\\ \chi(p)=-1}}\frac{\log p}{p}<\log B+O\left(1\right),
$$

 再由Mertens定理得 

$$
\sum\_{\substack{p<k\\ \chi(p)=-1}}\frac{\log p}{p}<\log k+O(1),
$$

 而 

$$
\log B=\frac{1}{2}\log x+\frac{1}{4}\log q+\frac{3}{2}\log 2=\frac{1}{2}\log x+\frac{1}{4}\log q+O(1);
$$

 

$$
\log k=\log\log(x^2B)+O(1)=\log\log x+O(1),
$$

 所以 

$$
\sum\_{\substack{p\le x\\\chi(p)=-1}}\frac{\log p}{p}\le \frac{1}{2}\log x+\frac{1}{4}\log q+\log\log x+O(1),
$$

 定理得证. 

</div>


<div style="border: 3px solid #000; padding: 10px;" markdown="1">

**定理 3.** 设正整数$q\ge3$, $\chi$是模$q$的实原特征, 若$\beta$是$L(s,\chi)$的非平凡实零点, 则 

$$
(1-\beta)\log q\ge 1-O\left(\frac{\log\log q}{\log q}\right),
$$

 特别的, 存在一个常数$c>0$, 使得 

$$
(1-\beta)\log q\ge c.
$$



</div>


<div style="border: 3px solid #000; padding: 10px;" markdown="1">

**证明.** 对任意实数$\eta\in(0,1)$, 由于 

$$
\eta\int\_{p}^\infty\frac{\log p}{p} x^{-1-\eta}\,\mathrm{d}x=\frac{\log p}{p^{1+\eta}},
$$

 对所有$\chi(p)=-1$的素数求和得 

$$
\sum\_{\chi(p)=-1}\frac{\log p}{p^{1+\eta}}=\eta\sum\_{\chi(p)=-1}\int\_{p}^\infty\frac{\log p}{p} x^{-1-\eta}\,\mathrm{d}x=\eta\int\_{1}^\infty\left(\sum\_{\substack{p\le x\\\chi(p)=-1}}\frac{\log p}{p}\right) x^{-1-\eta}\,\mathrm{d}x,
$$

 代入上一定理计算得 

$$
\begin{align}
        \sum\_{\chi(p)=-1}\frac{\log p}{p^{1+\eta}}&\le \eta\int\_{1}^\infty\left(\frac{1}{2}\log x+\frac{1}{4}\log q+\log\log x+O(1)\right) x^{-1-\eta}\,\mathrm{d}x+O(1)\\
        &=\frac{1}{2\eta}+\frac{1}{4}\log q-\log\eta+O(1).
\end{align}
$$



当$s$是大于$1$的实数时, 由 

$$
-\frac{\zeta'}{\zeta}(s)=\sum\_p\frac{\log p}{p^s-1}
$$

 和 

$$
\sum\_p\frac{\log p}{p^s-1}-\sum\_p\frac{\log p}{p^s}=\sum\_p\frac{\log p}{p^s(p^s-1)}<\infty
$$

 可知 

$$
\sum\_p\frac{\log p}{p^s}=-\frac{\zeta'}{\zeta}(s)+O(1),
$$

 而 

$$
-\frac{\zeta'(s)}{\zeta(s)}=\frac{1}{s-1}+O(1),
$$

 所以 

$$
\sum\_p\frac{\log p}{p^{1+\eta}}=\frac1\eta+O(1),
$$

 类似的有 

$$
\sum\_p\frac{\chi(p)\log p}{p^{1+\eta}}=-\frac{L'}{L}(1+\eta,\chi)+O(1),
$$

 由于$\chi$是实特征, 所以 

$$
2\sum\_{\chi(p)=-1}\frac{\log p}{p^{1+\eta}}=\sum\_p\frac{\log p}{p^{1+\eta}}-\sum\_{p}\frac{\chi(p)\log p}{p^{1+\eta}}-\sum\_{p\vert q}\frac{\log p}{p^{1+\eta}},
$$

 由Mertens定理得 

$$
\sum\_{p\vert q}\frac{\log p}{p^{1+\eta}}<\sum\_{\substack{p\vert q\\p\le \log q}}\frac{\log p}{p}+\sum\_{\substack{p\vert q\\p> \log q}}\frac{\log p}{p}<\sum\_{\substack{p\vert q\\p\le \log q}}\frac{\log p}{p}+\frac{1}{\log q}\sum\_{\substack{p\vert q}}\log p\ll\log\log q,
$$

 所以 

$$
2\sum\_{\chi(p)=-1}\frac{\log p}{p^{1+\eta}}=\frac{1}{\eta}+\frac{L'}{L}(1+\eta,\chi)+O(\log\log q),
$$

 故 

$$
\frac{L'}{L}(1+\eta,\chi)\le \frac{1}{2}\log q-2\log\eta+O(\log\log q).
$$



由$L$函数的Hadamard乘积公式知 

$$
\frac{L'}{L}(1+\eta,\chi)=\sum\_{\rho}\operatorname{Re}\frac{1}{1+\eta-\rho}-\frac{1}{2}\log q+O(1)\ge\frac{1}{1+\eta-\beta}-\frac{1}{2}\log q+O(1),
$$

 其中不等式是因为各零点都满足$\operatorname{Re}(1/(1+\eta-\rho))\ge0$, 求和中只保留$\beta$即可, 所以有 

$$
\frac{1}{1+\eta-\beta}\le \log q-2\log\eta+O(\log\log q),
$$

 取 

$$
\eta=\frac{1}{(\log q)^2}
$$

 即得 

$$
\frac1{1+\eta-\beta}\leq \log q+O(\log\log q),
$$

 

$$
(1-\beta)\log q\ge \frac{\log q}{\log q+O(\log\log q)}-\frac{1}{\log q}=1-O\left(\frac{\log\log q}{\log q}\right).
$$

 现取正整数$Q$, 使得当$q>Q$时总有 

$$
1-O\left(\frac{\log\log q}{\log q}\right)>\frac{1}{2},
$$

 对于$q\le Q$, 只有有限多个实零点, 逐个检查即可, 设 

$$
c\_1=\min\lbrace (1-\beta)\log q:3\le q\le Q\rbrace >0,
$$

 取$c=\min\lbrace c\_1,1/2\rbrace $即得定理结论. 

</div>


由于复特征对应的$L$函数一定不存在 Landau–Siegel 零点, 且$q=1$或$2$时也不存在 Landau–Siegel 零点, 而非原特征可以化为其对应的原特征, 它们的$L$函数在$\operatorname{Re}(s)>0$内的零点完全相同. 因此, 对任意正整数 $q$ 及任意模 $q$ 的 Dirichlet 特征 $\chi$, $L(s,\chi)$ 均不存在 Landau–Siegel 零点.

## 虚二次域的类数

Tao在[8]中提出挑战, 要求由Landau-Siegel零点不存在这一事实给出如下定理的新证明.

<div style="border: 3px solid #000; padding: 10px;" markdown="1">

**定理 4 (Gauss-Heegner).** 设正整数$d$无平方因子, 则虚二次域$\mathbb{Q}(\sqrt{-d})$的类数为$1$当且仅当$d$取以下$9$个值, 

$$
d=1,2,3,7,11,19,43,67,163.
$$



</div>


该定理最初由 Gauss 猜想, 后来由 Heegner 给出了优雅的证明, 相比之下, 通过排除 Landau–Siegel 零点来证明这一定理可能更容易理解, 但论证不如 Heegner 的优雅.

<div style="border: 3px solid #000; padding: 10px;" markdown="1">

**定理 5 (虚二次域的Dirichlet类数公式).** 设域$K=\mathbb{Q}(\sqrt{-d})$, $h\_K$是其类数, $w\_K$是$K$中包含的单位根个数, $D\_K$是$K$的判别式, 则 

$$
h\_K=\frac{w\_K\sqrt{\vert D\_K\vert }}{2\pi}L(1,\chi),
$$

 其中 

$$
\chi(\cdot)=\left(\dfrac{D\_K}{\cdot}\right)
$$

 是Kronecker符号.

</div>


由于对于虚二次域 

$$
w\_K=\begin{cases}
6,&K=\mathbb Q(\sqrt{-3}),\\
4,&K=\mathbb Q(i),\\
2,&K \text{ 是其他虚二次域},
\end{cases}
$$

 而我们只关心$d>163$的情况, 类数公式可以简化为 

$$
h\_K=\frac{\sqrt{\vert D\_K\vert }}{\pi}L(1,\chi),
$$

 若$h\_K=1$, 则 

$$
L(1,\chi)=\frac{\pi}{\sqrt{\vert D\_K\vert }}.
$$



<div style="border: 3px solid #000; padding: 10px;" markdown="1">

**定理 6.** 符号如上, 若$h\_K=1$, 则$d<e^{100}$.

</div>


<div style="border: 3px solid #000; padding: 10px;" markdown="1">

**证明.** 设$q=\vert D\_K\vert $, 设 

$$
\sum\_{\substack{p\le x\\\chi(p)=-1}}\frac{\log p}{p}\le \frac{1}{2}\log x+\frac{1}{4}\log q+\log\log x+C,
$$

 其中$C$是常数, 则当$\eta\in(0,1/2]$时, 

$$
\begin{align}
        \sum\_{\chi(p)=-1}\frac{\log p}{p^{1+\eta}}&=\eta\int\_{1}^3\left(\sum\_{\substack{p\le x\\\chi(p)=-1}}\frac{\log p}{p}\right) x^{-1-\eta}\,\mathrm{d}x+\eta\int\_{3}^\infty\left(\sum\_{\substack{p\le x\\\chi(p)=-1}}\frac{\log p}{p}\right) x^{-1-\eta}\,\mathrm{d}x \\
        &\le\frac{\log2}{2}\eta\int\_2^3x^{-1-\eta}\,dx+\eta\int\_3^\infty\left(\frac{1}{2}\log x+\frac{1}{4}\log q+\log\log x+C\right)x^{-1-\eta}\,\mathrm{d}x\\
        &\le\frac{1}{2\eta}+\frac{1}{4}\log q-\log\eta+C\_1,
\end{align}
$$

 其中 

$$
C\_1=C-\gamma+\frac12+\frac{\log2}{4}\log\frac{3}{2},
$$

 而 

$$
2\sum\_{\chi(p)=-1}\frac{\log p}{p^s}=-\frac{\zeta'}{\zeta}(s)+\frac{L'}{L}(s,\chi)-\sum\_{p\mid q}\frac{\log p}{p^s}-\sum\_p\frac{\log p}{p^s(p^s-1)}+\sum\_p\frac{\chi(p)^2\log p}{p^s(p^s-\chi(p))},
$$

 所以 

$$
\begin{align}
        \frac{L'}{L}(1+\eta,\chi)&\le2\sum\_{\chi(p)=-1}\frac{\log p}{p^{1+\eta}}+\frac{\zeta'}{\zeta}(1+\eta)+\sum\_{p\mid q}\frac{\log p}{p^{1+\eta}}+\sum\_p\frac{\log p}{p^{1+\eta}(p^{1+\eta}-1)}\\
        &<2\sum\_{\chi(p)=-1}\frac{\log p}{p^{1+\eta}}+\frac{\zeta'}{\zeta}(1+\eta)+\log\log q+3-2\zeta'(2)\\
        &\le\frac{\zeta'}{\zeta}(1+\eta)+\frac{1}{\eta}+\frac{1}{2}\log q-2\log\eta+\log\log q+C\_2,
\end{align}
$$

 其中 

$$
C\_2=2C\_1+3-2\zeta'(2).
$$

 对$\eta$积分得 

$$
\begin{align}
        \int\_0^{1/2}\frac{L'}{L}(1+\eta,\chi)\,\mathrm{d}\eta&\le \int\_0^{1/2}\frac{\zeta'}{\zeta}(1+\eta)+\frac{1}{\eta}\,\mathrm{d}\eta+1+\log2+\frac{1}{4}\log q+\frac{1}{2}\log\log q+\frac{C\_2}{2}\\
        &=\frac{1}{4}\log q+\frac{1}{2}\log\log q+1+\log\zeta(3/2)+\frac{C\_2}{2},
\end{align}
$$

 由于 

$$
L(s,\chi)=\prod\_p\left(1-\frac{\chi(p)}{p^s}\right)^{-1}\geq\prod\_p\left(1+\frac1{p^s}\right)^{-1}=\frac{\zeta(2s)}{\zeta(s)},
$$

 取$s=3/2$得 

$$
L(3/2,\chi)\geq\frac{\zeta(3)}{\zeta(3/2)},
$$

 于是 

$$
\int\_0^{1/2}\frac{L'}{L}(1+\eta,\chi)\,\mathrm{d}\eta=\log L(3/2,\chi)-\log L(1,\chi)\ge\log\frac{\zeta(3)}{\zeta(3/2)}-\log L(1,\chi),
$$

 代入类数公式得 

$$
\int\_0^{1/2}\frac{L'}{L}(1+\eta,\chi)\,\mathrm{d}\eta\ge\log\frac{\zeta(3)}{\zeta(3/2)}-\log \frac{\pi}{\sqrt{q}}=\frac{1}{2}\log q-\log\frac{\pi\zeta(3/2)}{\zeta(3)}.
$$

 比较上下界并整理得 

$$
\frac{1}{2}\log q-\log\frac{\pi\zeta(3/2)}{\zeta(3)}\le\frac{1}{4}\log q+\frac{1}{2}\log\log q+1+\log\zeta(3/2)+\frac{C\_2}{2},
$$

 

$$
\frac{1}{4}\log q\le\frac{1}{2}\log\log q+C\_3,
$$

 其中 

$$
C\_3=\frac{C\_2}{2}+1+\log\frac{\pi\zeta(3/2)^2}{\zeta(3)}=C-\gamma+3+\frac{\log2}{4}\log\frac{3}{2}-\zeta'(2)+\log\frac{\pi\zeta(3/2)^2}{\zeta(3)}<C+6.4.
$$

 现在问题的关键就是确定常数$C$, 将所有证明中的常数显式化可以证明$C<16$ (见附录), 所以 

$$
\log q-2\log\log q\le90,
$$

 数值计算得到满足该不等式的$q$的一个上界为$e^{100}$, 而$q=\vert D\_K\vert $等于$d$或$d$的四倍, 所以$d<e^{100}$, 定理得证. 

</div>


$e^{100}$大约为$2.7\times10^{43}$量级, 该上界太大, 逐一检验超出目前计算能力. 通过更细致的分析[10]可以将上界降到$d<17000$, Tao在[8]的[评论区](https://terrytao.wordpress.com/2026/10/20/an-experimental-ai-math-challenge-using-tenth-discriminant-bounds-to-explore-arguments-ruling-out-siegel-zeroes/#comment-698471)指出, 如果假设$L$函数在实部大于$7/8$的半平面内无零点, 可以证明$d<655$, 这个上界已经足够小, 可以对小于它的$d$逐一验证.

## 附录

正文中需要用到以下经典定理.

<div style="border: 3px solid #000; padding: 10px;" markdown="1">

**定理 7 (Mertens 定理).** 对实数 $x\ge 2$, 有 

$$
\sum\_{p\le x}\frac{\log p}{p}=\log x+O(1),
$$

 其中$O(1)$可以换成显式的常数$2$, 即 

$$
\left\vert \sum\_{p\le x}\frac{\log p}{p}-\log x\right\vert \le 2.
$$



</div>


<div style="border: 3px solid #000; padding: 10px;" markdown="1">

**定理 8 (Hadamard不等式).** 设方阵 $A=(a\_{ij})\_{ij}\in M\_{n\times n}(\mathbb{C})$, 则有 

$$
\vert \det A\vert ^2\le\prod\_{j=1}^{n}\sum\_{i=1}^{n}\vert a\_{ij}\vert ^2,
$$

 等号成立当且仅当 

$$
\sum\_{k=1}^{n}\overline{a\_{ki}}a\_{kj}=0,\qquad i\ne j.
$$



</div>


<div style="border: 3px solid #000; padding: 10px;" markdown="1">

**定理 9 ($L$函数的Hadamard乘积).** 设$\chi$是模$q$的实原特征, 设 

$$
a=\frac{1-\chi(-1)}2=
    \begin{cases}
        0,&\chi(-1)=1,\\
        1,&\chi(-1)=-1,
    \end{cases}
$$

 $s$是大于$1$的实数, 则有 

$$
\frac{L'}{L}(s,\chi)=\sum\_\rho\operatorname{Re}\frac1{s-\rho}-\frac12\log\frac q\pi-\frac12\frac{\Gamma'}{\Gamma}\left(\frac{s+a}{2}\right),
$$

 其中$\rho$取遍$L$函数的非平凡零点.

</div>


<div style="border: 3px solid #000; padding: 10px;" markdown="1">

**证明.** 对完备$L$函数 

$$
\Lambda(s,\chi)=\left(\frac q\pi\right)^{\frac{s+a}{2}}\Gamma\left(\frac{s+a}{2}\right)L(s,\chi)
$$

 使用Hadamard乘积定理得 

$$
\Lambda(s,\chi)=\Lambda(0,\chi)e^{Bs}\prod\_{\rho}\left(1-\frac{s}{\rho}\right)e^{s/\rho},
$$

 其中$\rho$取遍$\Lambda$的所有零点, $B$是常数, 并且由$\Lambda$的函数方程易知 

$$
\operatorname{Re}B=-\sum\_{\rho}\operatorname{Re}\frac{1}{\rho},
$$

 取对数导数得 

$$
\frac{L'}{L}(s,\chi)=B+\frac{1}{2}\log\frac{\pi}{q}-\frac{1}{2}\frac{\Gamma'}{\Gamma}\left(\frac{s+a}{2}\right)+\sum\_\rho\left(\frac{1}{s-\rho}+\frac{1}{\rho}\right),
$$

 取实部, 由于$\chi$是实特征且$s$是实数, 所以 

$$
\frac{L'}{L}(s,\chi)=\sum\_\rho\operatorname{Re}\frac1{s-\rho}-\frac12\log\frac q\pi-\frac12\frac{\Gamma'}{\Gamma}\left(\frac{s+a}{2}\right),
$$

 定理得证. 

</div>


接下来说明正文第三节中的$C<16$.

Rosser–Schoenfeld [9]关于Chebyshev界的改进给出 

$$
\sum\_{p\le x}\log p<1.01624x,
$$

 接下来我们比较$\vert T\vert $和$\sum\_{(r,s)\in T}r$. 由$T$的定义知 

$$
\vert T\vert =\sum\_{s=0}^{\lceil x/k\rceil-1}\lceil x-ks\rceil,\qquad \sum\_{(r,s)\in T}r=\sum\_{s=0}^{\lceil x/k\rceil-1}\sum\_{r=0}^{\lceil x-ks\rceil-1}r,
$$

 记$S=\lceil x/k\rceil-1$, $m\_s=\lceil x-ks\rceil$, 则 

$$
\sum\_{(r,s)\in T}r=\sum\_{s=0}^{S}\frac{m\_s(m\_s-1)}{2}=\frac{1}{2}\sum\_{s=0}^{S}m\_s^2-\frac{1}{2}\sum\_{s=0}^{S}m\_s=\frac{1}{2}\sum\_{s=0}^{S}m\_s^2-\frac{\vert T\vert }{2},
$$

 由 Cauchy–Schwarz 不等式得 

$$
\vert T\vert ^2=\left(\sum\_{s=0}^{S}m\_s\right)^2\le (S+1)\sum\_{s=0}^{S}m\_s^2=(S+1)\left(2\sum\_{(r,s)\in T}r+\vert T\vert \right),
$$

 而 

$$
\vert T\vert \ge\sum\_{s=0}^{S}(x-ks)=(S+1)\left(x-\frac{kS}{2}\right)\ge(S+1)\left(x-\frac{x}{2}\right)=\frac{x}{2}(S+1),
$$

 所以 

$$
2(S+1)\sum\_{(r,s)\in T}r\ge \vert T\vert ^2-(S+1)\vert T\vert \ge\vert T\vert \left(\frac{x}{2}(S+1)-(S+1)\right)=\frac{\vert T\vert (S+1)(x-2)}{2},
$$

 由于$x\ge e^3>10$, 有$(x-2)/2\ge 2x/5$, 所以 

$$
\sum\_{(r,s)\in T}r\ge\frac{\vert T\vert x}{5}.
$$

 接下来, 由 

$$
\sum\_{\substack{k\le p\le x\\ \chi(p)=-1}}\frac{\log p}{p}\sum\_{(r,s)\in T}r<\log \vert D\vert +\vert T\vert \sum\_{\substack{k\le p\le x\\\chi(p)=-1}}\log p\le \log \vert D\vert + 1.01624\vert T\vert x\le  \log \vert D\vert + 5.0812\sum\_{(r,s)\in T}r
$$

 和 

$$
\log \vert D\vert \le\log B\sum\_{(r,s)\in T}r+\vert T\vert x+\frac{\vert T\vert }{2}\log \vert T\vert \le \sum\_{(r,s)\in T}r\left(\log B+5+\frac{5\log\vert T\vert }{2x}\right)
$$

 得 

$$
\sum\_{\substack{k\le p\le x\\ \chi(p)=-1}}\frac{\log p}{p}\le\log B+\frac{5\log\vert T\vert }{2x}+10.0812\le\frac{1}{2}\log x+\frac{1}{4}\log q+\frac{5\log\vert T\vert }{2x}+\frac{3}{2}\log 2+10.0812,
$$

 由于$\vert T\vert \le(S+1)(x+1)<(x+1)^2$, 所以 

$$
\frac{5\log\vert T\vert }{2x}<\frac{5\log(x+1)}{x}<\frac{5\log(e^3+1)}{e^3}<0.76,
$$

 

$$
\sum\_{\substack{k\le p\le x\\ \chi(p)=-1}}\frac{\log p}{p}<\frac{1}{2}\log x+\frac{1}{4}\log q+0.76+\frac{3}{2}\log 2+10.0812<\frac{1}{2}\log x+\frac{1}{4}\log q+12.
$$

 对于小素数, 

$$
\sum\_{\substack{p<k\\ \chi(p)=-1}}\frac{\log p}{p}\le\log k+2\le\log(\log(x^2B)+1)+2,
$$

 其中 

$$
\log(x^2B)=\frac{5}{2}\log x+\frac{1}{4}\log q+\frac{3}{2}\log2\le3\log x+\frac{3}{2}\log2,
$$

 所以 

$$
\log(\log(x^2B)+1)+2\le\log\left(3\log x+1+\frac{3}{2}\log2\right)+2\le \log\log x+3.303,
$$

 综上即得 

$$
\sum\_{\substack{p\le x\\ \chi(p)=-1}}\frac{\log p}{p}=\sum\_{\substack{k\le p\le x\\ \chi(p)=-1}}\frac{\log p}{p}+\sum\_{\substack{p<k\\ \chi(p)=-1}}\frac{\log p}{p}\le \frac{1}{2}\log x+\frac{1}{4}\log q+\log\log x+16.
$$

## 参考文献

1. OpenAI, *Uniform exclusion of Landau–Siegel zeros*, 1 October 2026, (<https://github.com/openai/math/blob/main/preprints/Uniform-exclusion-of-Landau-Siegel-zeros-October-1-2026/paper.pdf>).

2. W. D. Banks, *On the OpenAI proof that Landau–Siegel zeros do not exist*, preprint v1, 11 October 2026, arXiv:2610.15483v1 (<https://arxiv.org/abs/2610.15483v1>).

3. B. Kerr, *A simpler proof that there are no Landau–Siegel zeros*, preprint v1, 15 October 2026, arXiv:2610.21099v1 (<https://arxiv.org/abs/2610.21099v1>).

4. B. Green, *On Landau–Siegel zeros*, preprint v2, 17 October 2026, hexagon:2610.00311v2 (<https://hexagonmath.org/2610.00311v2>).

5. J. Pescador, *Landau–Siegel zeros and a Stepanov-type nonvanishing lemma*, preprint v3, 22 October 2026, (<https://jacobpescador.github.io/ai-math/papers/landau-siegel-stepanov/>).

6. K. Barreto, *An elementary proof of the non-existence of Landau–Siegel zeros*, 19 October 2026, X post (<https://x.com/acerfur/status/2112239827077026128>).

7. T. Tao, *A sketch of the proof of non-existence of Siegel zeroes*, 19 October 2026, *What’s New* (<https://terrytao.wordpress.com/2026/10/19/a-sketch-of-the-proof-of-non-existence-of-siegel-zeroes/>).

8. T. Tao, *An experimental AI-math challenge: using tenth discriminant bounds to explore arguments ruling out Siegel zeroes*, 20 October 2026, *What’s New* (<https://terrytao.wordpress.com/2026/10/20/an-experimental-ai-math-challenge-using-tenth-discriminant-bounds-to-explore-arguments-ruling-out-siegel-zeroes/>).

9. J. B. Rosser and L. Schoenfeld, *Approximate formulas for some functions of prime numbers*, Illinois Journal of Mathematics, **6** (1962), no. 1, 64–94, (<https://doi.org/10.1215/ijm/1255631807>).

10. R. van Dijk, *A proof Gauss might have found*, preprint v1, 26 October 2026, hexagon:2610.00568v1 (<https://hexagonmath.org/2610.00568v1>).


pdf: <a href="{{ site.baseurl }}/pdf/Landau_Siegel零点不存在.pdf">Landau-Siegel零点不存在</a>.
