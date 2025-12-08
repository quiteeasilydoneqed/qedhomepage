<img width="2520" height="1619" alt="image" src="https://github.com/user-attachments/assets/e1f3ef39-4e70-482e-9ce7-aba16f928cf1" />---
layout: post
title: "测度论"
subtitle: ""
header-img: "img/post-bg-infinity.jpg"
header-mask: 0.3
math: true
tags:
  - 分析
---

# 实数集上的勒贝格测度

<div style="border: 3px solid #000; padding: 10px;">
<b>定义</b>

开区间 $I$ 的长度 $m(I)$ 定义为

$$
m(I) =
\begin{cases}
    b - a, & I = (a, b), a, b \in \mathbb{R} , a < b, \\
    0, & I = \emptyset, \\
    +\infty, & I = (-\infty, a) \text{ 或 } I = (a, +\infty), a \in \mathbb{R}, \\
    +\infty, & I = (-\infty, +\infty).
\end{cases}
$$

</div>

显然 $m$ 的值域是 $[0,+\infty]$, 右边的方括号代表有可能取到无穷大.

实数集中的任意开集都可以表示为无交的开区间的并, 比如 $F=\bigsqcup_{i}(a_i,b_i)$, 定义 $m(F)=\sum_{i}(b_i-a_i)$. 对于任意非空闭集 $G$, 取任意包含 $G$ 的开区间 $(a,b)$, 定义 $m(G)=b-a-m((a,b)-G)$, 其中集合间减号为差集.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(外测度,内测度)</b>

有界集合 $A \subseteq \mathbb{R}$ 的外测度 $m^*(A)$ 定义为

$$
m^*(A) = \inf_{A\subseteq F} m(F),
$$

其中 $\inf$ 取遍所有包含 $A$ 的开集.

定义 $A$ 的内测度 $m_*(A)$ 为

$$
m_*(A) = \sup_{G\subseteq A} m(G),
$$

其中 $\sup$ 取遍 $A$ 的所有闭子集.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(勒贝格测度)</b>

如果有界集合 $A$ 的外测度 $m^*(A)$ 和内测度 $m_*(A)$ 相等, 则称 $A$ 是勒贝格可测的, 记其勒贝格测度为 $m(A)=m^*(A)=m_*(A)$.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(卡拉泰奥多里条件)</b>

有界集 $A$ 勒贝格可测的充要条件是, 对任意开集 $E\subseteq\mathbb{R}$, 有

$$
\mu^*(E) = \mu^*(E \cap A) + \mu^*(E \cap A^c),
$$

其中 $A^c$ 是补集 $\mathbb{R}-A$.

</div>

如果承认选择公理, 则可以构造出不可测集, 例如维塔利集, 如果否认选择公理, 则存在使得所有实数子集都是勒贝格可测的模型, 例如梭罗维模型.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>

不存在一个函数 $\mu$ 满足以下所有性质:<br>

1, $\mu$ 是一个从 $\mathbb{R}$ 的幂集到 $[0, +\infty]$ 的函数;<br>

2, 对于 $\mathbb{R}$ 的每个开区间 $I$， $\mu(I) = m(I)$;<br>

3, 对于 $\mathbb{R}$ 的每个无交子集列 $A_1, A_2, \ldots$, 有

$$
\mu\left(\bigcup_{k=1}^{\infty} A_k\right) = \sum_{k=1}^{\infty} \mu(A_k);
$$

4, 对于每个子集 $A \subseteq \mathbb{R}$ 和每个实数 $t \in \mathbb{R}$， $\mu(t+A) = \mu(A)$.

</div>

# 抽象测度论

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(集合环)</b>

设 $\mathscr{R}$ 是以集合为元素的非空集族, 如果它满足以下条件, 则称它为一个集合环:<br>

1, 如果 $A,B\in\mathscr{R}$, 则 $A\cup B\in\mathscr{R}$;<br>

2, 如果 $A,B\in\mathscr{R}$, 则 $A- B\in\mathscr{R}$.

</div>

注1: 由于 $\mathscr{R}$ 非空, 则 $A-A=\emptyset$ 在 $\mathscr{R}$ 中, 又因为 $A-(A-B)=A\cap B$, 所以环对于交集也是封闭的.

注2: 设 $A,B\in\mathscr{R}$, 定义对称差为 $A\bigtriangleup B=(A-B)\cup(B-A)$, 显然对称差是可交换的, 容易验证集合环在交集(乘法)和对称差(加法)下构成一个代数环, 它还是交换布尔环, 它是否含幺取决于环中是否有一个包含其他所有集合的最大集合.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义($\delta$-环)</b>

设 $\mathscr{R}$ 是一个集合环, 如果它满足如下附加条件, 则称它是一个 $\delta$-环:<br>

3, 设 $\{A_n\}_{n=1}^\infty$ 是一列集合, 如果 $A_n\in\mathscr{R}$, 则 $\bigcap_{n=1}^\infty A_n\in\mathscr{R}$.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义($\sigma$-环)</b>

设 $\mathscr{R}$ 是一个集合环, 如果它满足如下附加条件, 则称它是一个 $\sigma$-环:<br>

3', 设 $\{A_n\}_{n=1}^\infty$ 是一列集合, 如果 $A_n\in\mathscr{R}$, 则 $\bigcup_{n=1}^\infty A_n\in\mathscr{R}$.

</div>

$\delta$ 和 $\sigma$ 分别来自德语中的交集和并集, 二者看似对偶, 但实际上 $\sigma$-环一定是 $\delta$-环, 反之则不一定.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(集合代数)</b>

设 $X$ 是一个集合, $\mathscr{A}$ 是 $\mathscr{P}(X)$ 的子集, 如果它满足以下条件, 则称它为一个集合代数:<br>

1, $\emptyset\in\mathscr{A}$;<br>

2, 如果 $A\in\mathscr{A}$, 则 $X - A\in\mathscr{A}$;<br>

3, 如果 $A,B\in\mathscr{A}$, 则 $A\cup B\in\mathscr{A}$.

</div>

这里的代数是指布尔代数, 也可以理解为它的布尔环自然的 $\mathbb{Z}$-代数结构. 集合代数有时也称为集合域, 但这里就与代数中的域没有关系了. 集合代数也有对应的 $\delta$-代数和 $\sigma$-代数, 但二者在这种情况下是等价的.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义($\sigma$-代数)</b>

设 $\mathscr{A}$ 是 $X$ 上的一个集合代数, 如果它满足如下附加条件, 则称它是一个 $\sigma$-代数:<br>

4, 设 $\{A_n\}_{n=1}^\infty$ 是一列集合, 如果 $A_n\in\mathscr{A}$, 则 $\bigcup_{n=1}^\infty A_n\in\mathscr{A}$.

</div>

所有勒贝格可测集组成的集族是一个 $\sigma$-代数, 记为 $\mathscr{L}$.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(可测空间, 可测集)</b>

设 $X$ 是一个集合, $\mathscr{A}$ 是 $X$ 上的一个 $\sigma$-代数, 则称 $(X,\mathscr{A})$ 是一个可测空间, 称 $\mathscr{A}$ 中的元素为可测集.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(博雷尔代数, 博雷尔集)</b>

设 $X$ 是一个拓扑空间, 定义 $\mathscr{B}(X)$ 是包含 $X$ 中所有开集的最小 $\sigma$-代数, 则称其为由 $X$ 上拓扑生成的博雷尔代数, 称 $\mathscr{B}(X)$ 中的元素为博雷尔集.

</div>

博雷尔代数中显然包含 $X$ 的所有开集和闭集, 以及开集的可数交和可数并, 闭集的可数交和可数并. 可数个开集的交集称为 $G_{\delta}$ 集, 可数个闭集的并集称为 $F_{\sigma}$ 集, 可数个 $G_{\delta}$ 集的并集称为 $G_{\delta\sigma}$ 集, 可数个 $F_{\sigma}$ 集的交集称为 $F_{\sigma\delta}$ 集, 依此类推.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(测度, 测度空间)</b>

设 $X$ 是一个配备有 $\sigma$-代数 $\mathscr{A}$ 的集合. 在 $\mathscr{A}$ 上的测度 $\mu$ 是一个函数 $\mu\colon \mathscr{A} \to [0, +\infty]$ 使得:<br>

1, $\mu(\emptyset) = 0,$<br>

2, 如果 $\{E_i\}_{i=1}^{\infty}$ 是 $\mathscr{A}$ 中无交集合的一个序列, 那么

$$
\mu\left(\bigcup_{i=1}^{\infty} E_i\right) = \sum_{i=1}^{\infty} \mu(E_i).
$$

配备了测度的可测空间称为测度空间, 记为 $(X,\mathscr{A},\mu)$.

</div>

若第二个条件改成有限序列, 则称为有限和测度. 如果 $\mu$ 的值域不包括无穷大, 等价的说, 如果 $\mu(X)$ 是一个有限数, 则称 $\mu$ 是一个有限测度. 如果 $X$ 可以表示为可数个测度为有限数的集合的并, 即 $X=\bigcup_{i=1}^\infty E_i$ 且 $\mu(E_i)<\infty$, 则称 $\mu$ 是一个 $\sigma$-有限测度. 如果集合 $E$ 可以表示为可数个测度为有限数的集合的并, 则称 $E$ 对于测度 $\mu$ 是 $\sigma$-有限的. 如果任意一个测度为无穷大的集合都有一个测度为有限数的子集, 则称测度是半有限的.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(计数测度)</b>

设 $X$ 是一个集合, 其上的 $\sigma$-代数是 $X$ 的幂集, 如果测度 $\mu$ 在任何单点集上的值都为 $1$, 即 $\mu(\{x\})=1$, $x\in X$, 则称 $\mu$ 为计数测度.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(狄拉克测度)</b>

设 $X$ 是一个集合, 其上的 $\sigma$-代数是 $X$ 的幂集, 如果测度 $\mu$ 在某一个单点集上的值为 $1$, 在其他单点集上的值为 $0$, 则称 $\mu$ 为狄拉克测度.

</div>

测度为 $0$ 的集合称为零测集.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(严格正测度)</b>

设 $\mathscr{A}$ 是拓扑空间 $X$ 上的包含博雷尔代数的 $\sigma$-代数, 其上的测度 $\mu$ 称为严格正测度, 如果它在除空集外的所有开集上取值严格正, 即零测集只有空集.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(完备性)</b>

如果一个测度 $\mu$ 的定义域包含所有零测集的子集, 则称 $\mu$ 是完备的.

</div>

设 $(X,\mathscr{A},\mu)$ 是测度空间, 则 $\mu$ 可以唯一的延拓到 $\overline{\mathscr{A}}=\\{E\cup F\mid E\in \mathscr{A},F\subseteq N\in\mathscr{A},\mu(N)=0\\}$ 上成为一个完备测度. 例如, 带博雷尔代数的实数集上的测度是不完备的, 其完备化后均为勒贝格可测集组成的 $\sigma$-代数 $\mathscr{L}$ 上的测度.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(乘积$\sigma$-代数)</b>

设 $\{X_i\}_{i \in I}$ 是一组由非空集合, $X = \prod_{i \in I} X_i$, 且 $\pi_i \colon X \to X_i$ 是投影映射. 如果 $\mathscr{A}_i$ 是 $X_i$ 上的 $\sigma$-代数, 那么 $X$ 上的乘积 $\sigma$-代数是由以下集合族生成的 $\sigma$-代数:

$$
\left\{\pi_i^{-1}(E_i) \colon E_i \in \mathscr{A}_i, i \in I\right\},
$$

记作 $\bigotimes_{i \in I} \mathscr{A}_i$.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>

$$
\mathscr{B}(\mathbb{R}^n)=\bigotimes_{i=1}^n\mathscr{B}(\mathbb{R}),
$$

特别的, $\mathscr{B}(\mathbb{C})=\mathscr{B}(\mathbb{R})\otimes\mathscr{B}(\mathbb{R})$.

</div>

# 特殊测度

### 外测度

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(外测度)</b>

设 $X$ 是一个集合, 函数 $\mu^*\colon\mathscr{P}(X)\to[0,+\infty]$ 如果满足如下条件, 则称其为 $X$ 上的一个外测度:<br>

1, $\mu^*(\emptyset)=0$;<br>

2, 如果 $A\subseteq B\subseteq X$, 则有 $\mu^*(A) \le \mu^*(B)$;<br>

3, 如果 $\{A\}_{n=1}^\infty\subseteq \mathscr{P}(X)$, 则有 $\mu^*\left(\bigcup_{n=1}^\infty A_n\right)\le \sum_{n=1}^\infty\mu^*(A_n)$.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(卡拉泰奥多里定理)</b>

设 $\mu^*$ 是集合 $X$ 上的外测度, 称使得

$$
\mu^*(E) = \mu^*(E \cap A) + \mu^*(E \cap A^c),\forall E\subseteq X
$$

成立的 $X$ 的子集 $A$ 是 $\mu^*$ 可测的, 所有 $\mu^*$ 可测集合组成一个 $\sigma$-代数, 并且 $\mu^*$ 限制在这个 $\sigma$-代数上是完备的.

</div>

特别的, 勒贝格测度是完备的.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(预测度)</b>

设 $X$ 是一个集合, $\mathscr{A}$ 是其上的代数, 函数 $\mu\colon\mathscr{A}\to[0,+\infty]$ 如果满足如下条件, 则称其为 $X$ 上的一个预测度:<br>

1, $\mu(\emptyset)=0$;<br>

2, 如果 $\{A\}_{n=1}^\infty$ 是 $X$ 中一列无交集合列, 则有 $\mu\left(\bigcup_{n=1}^\infty A_n\right)= \sum_{n=1}^\infty\mu(A_n)$.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>

设 $\mu$ 是 $(X,\mathscr{A})$ 上的一个预测度, 对 $X$ 的任意子集 $A$ 定义

$$
\mu^*(A)=\inf \left\{\sum_{j=1}^{\infty} \mu_0(A_j) \Bigg{\vert} A \subseteq \bigcup_{j=1}^{\infty} A_j, \{A_j\}_{j=1}^{\infty} \subseteq \mathscr{A}\right\},
$$

则这样定义的 $\mu^*$ 是 $X$ 上的一个外测度, 并且它限制在 $\mathscr{A}$ 上是与 $\mu$ 相等的, $\mathscr{A}$ 中所有集合都是 $\mu^*$ 可测的.

</div>

### 博雷尔测度

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(博雷尔测度)</b>

设 $X$ 是一个拓扑空间, 其上带博雷尔代数, 则博雷尔代数上的测度称为博雷尔测度.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(分布函数)</b>

设 $\mu$ 是实数集上的有限博雷尔测度, 定义函数 $F(x)=\mu((-\infty,x])$ 为 $\mu$ 的分布函数.

若 $\mu$ 是实数集上的未必有限博雷尔测度, 则定义分布函数为

$$
F(x)=
\begin{cases}
    \mu((0,x]), & x>0,\\
    0, & x=0,\\
    -\mu((x,0]), & x<0.
\end{cases}
$$

</div>

显然分布函数是单调递增且右连续的.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(勒贝格-斯蒂尔切斯测度)</b>

设 $F(x)$ 是一个单调递增且右连续的实函数, 则唯一存在一个实数集上的博雷尔测度 $\mu$, 使得 $\mu((a,b])=F(b)-F(a)$ 对任意实数 $a$ 和 $b$ 都成立, 它的完备化测度记作 $\mu_F$, 称为 $F$ 对应的勒贝格-斯蒂尔切斯测度.

</div>

当取 $F(x)=x$ 时, 对应的勒贝格-斯蒂尔切斯测度就是普通的勒贝格测度.

### 拉东测度

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(正则性)</b>

设 $X$ 是拓扑空间, $\mu$ 是 $X$ 上的测度, 如果对 $X$ 中的可测子集 $E$, 有

$$
\mu(E) = \inf\{\mu(U) \mid E \subseteq U, U \text{是开可测集}\},
$$

则称 $\mu$ 在 $E$ 上外正则, 若 $\mu$ 在所有可测集上都外正则, 则称 $\mu$ 为外正则测度;

如果有

$$
\mu(E) = \sup\{\mu(K) \mid K \subseteq E, K \text{是紧可测集}\},
$$

则称 $\mu$ 在 $E$ 上内正则, 若 $\mu$ 在所有可测集上都内正则, 则称 $\mu$ 为内正则测度;

既外正则又内正则的测度称为正则测度.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(局部有限性)</b>

设 $X$ 是拓扑空间, 其上的 $\sigma$-代数包含博雷尔代数, $\mu$ 是 $X$ 上的测度, 如果对 $X$ 中每一点 $x$, 都存在一个开邻域 $N_x$, 使得 $\mu(N_x)$ 是一个有限数, 则称 $\mu$ 是局部有限测度.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(拉东测度)</b>

设 $X$ 是一个局部紧豪斯多夫空间, 如果其上博雷尔测度满足局部有限性和外正则性, 并在所有开集上有内正则性, 则称其为拉东测度.

</div>

拉东测度未必是正则的, 最多只能推出它在每个 $\sigma$-有限集上内正则, 从而得到 $\sigma$-有限的拉东测度都是正则的. 但如果要求局部紧豪斯多夫空间 $X$ 是可数个紧集的并(该条件称为 $\sigma$-紧性), 则拉东测度都是正则的. 拉东测度可以推广到豪斯多夫空间或任意拓扑空间上, 但性质太差意义不大.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(拉东空间)</b>

如果一个拓扑空间上的所有有限博雷尔测度都是拉东测度, 则称这个拓扑空间为拉东空间, 如果这个空间上所有局部有限博雷尔测度都是拉东测度, 则称这个拓扑空间为强拉东空间.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(里斯表示定理)</b>

设 $X$ 是一个局部紧豪斯多夫空间, $C_c(X)$ 为 $X$ 上的紧支集连续函数空间, 设 $L$ 是 $C_c(X)$ 上的一个正线性泛函, 则存在唯一的拉东测度 $\mu$, 使得对任意 $f\in C_c(X)$, 有

$$
L(f)=\int_Xf\,\mathrm{d}\mu.
$$

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(卢津定理)</b>

设 $\mu$ 是 $X$ 上的拉东测度, 如果 $f\colon X \to \mathbb{C}$ 是可测函数且使得 $f(x)\neq0$ 的 $x$ 组成一个有限测度集, 则对任意正实数 $\varepsilon>0$, 存在函数 $\phi \in C_c(X)$, 使得 $f=\phi$ 在除一个测度小于 $\varepsilon$ 的集合外成立.

</div>

### 乘积测度

设 $(X,\mathscr{A}_1,\mu)$ 和 $(Y,\mathscr{A}_2,\nu)$ 是 $\sigma$-有限的测度空间, 则唯一存在一个测度, 记作 $\mu\times\nu$, 使得 $(\mu\times\nu)(A\times B)=\mu(A)\times\nu(B)$, 对任意 $A\in \mathscr{A}_1$ 和 $B\in\mathscr{A}_2$ 都成立, 由下式定义:

$$
(\mu\times\nu)(E)=\int_X\int_Y\chi_E(x,y)\,\mathrm{d}\nu(y)\,\mathrm{d}\mu(x), E\in\mathscr{A}_1\otimes\mathscr{A}_2.
$$

对任意集合 $E\in\mathscr{A}_1\otimes\mathscr{A}_2$, 定义其截面为

$$
E_x=\{y\in Y\mid (x,y)\in E\},\quad  E^y=\{x\in X\mid (x,y)\in E\},
$$

$X\times Y$ 上的可测函数 $f(x,y)$ 的截面为

$$
f_x(y)=f^y(x)=f(x,y),
$$

容易证明可测集的截面均为可测集, 可测函数的截面均为可测函数.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(托内利定理)</b>

设 $(X, \mathscr{A}_1, \mu)$ 和 $(Y, \mathscr{A}_2, \nu)$ 是 $\sigma$-有限测度空间, 设 $f\colon X \times Y \to [0, \infty]$ 是 $\mathscr{A}_1 \otimes \mathscr{A}_2$ 上的可测函数. 则

$$
x \mapsto \int_Y f_x(y) \, \mathrm{d}\nu(y)
$$

和

$$
y \mapsto \int_X f^y(x) \, \mathrm{d}\mu(x)
$$

均是可测函数, 且

$$
\int_{X \times Y} f \, \mathrm{d}(\mu \times \nu) = \int_X \left( \int_Y f(x, y) \, \mathrm{d}\nu(y) \right) \mathrm{d}\mu(x) = \int_Y \left( \int_X f(x, y) \, \mathrm{d}\mu(x) \right) \mathrm{d}\nu(y).
$$

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(富比尼定理)</b>

设 $(X, \mathscr{A}_1, \mu)$ 和 $(Y, \mathscr{A}_2, \nu)$ 是 $\sigma$-有限测度空间, 设 $f\colon X \times Y \to [-\infty, \infty]$ 是 $\mathscr{A}_1 \otimes \mathscr{A}_2$ 上的可积函数, 即 $\int_{X \times Y}\lvert f\rvert \,\mathrm{d}(\mu \times \nu)$ 有限, 则 $\int_Y \lvert f_x(y)\rvert \, \mathrm{d}\nu(y)$ 和 $\int_X \lvert f^y(x)\rvert \, \mathrm{d}\mu(x)$ 也有限,

$$
x \mapsto \int_Y f_x(y) \, \mathrm{d}\nu(y)
$$

和

$$
y \mapsto \int_X f^y(x) \, \mathrm{d}\mu(x)
$$

均是可测函数, 且

$$
\int_{X \times Y} f \, \mathrm{d}(\mu \times \nu) = \int_X \left( \int_Y f(x, y) \, \mathrm{d}\nu(y) \right) \mathrm{d}\mu(x) = \int_Y \left( \int_X f(x, y) \, \mathrm{d}\mu(x) \right) \mathrm{d}\nu(y).
$$

</div>

有限多个测度空间的积测度可递归的定义, 与以上步骤完全相同.

### 符号测度

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(符号测度)</b>

$(X,\mathscr{A})$ 是一个可测空间, 其上的符号测度 $\mu$ 是一个函数 $\mu\colon \mathscr{A} \to [-\infty, +\infty]$ 使得:<br>

1, $\mu(\emptyset) = 0,$<br>

2, 如果 $\{E_i\}_{i=1}^{\infty}$ 是 $\mathscr{A}$ 中无交集合的一个序列, 那么

$$
\mu\left(\bigcup_{i=1}^{\infty} E_i\right) = \sum_{i=1}^{\infty} \mu(E_i),
$$

3, $\mu$ 在 $+\infty$ 和 $\infty$ 中至多只能取到一个.

</div>

实践中一般假设符号测度有可能取到正无穷而不取负无穷, 相反的情况完全对偶. 显然任意测度都是符号测度, 为区分时称测度为正测度, 即测度和正测度为同义词.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(哈恩分解定理)</b>

设 $\mu$ 是 $(X,\mathscr{A})$ 上的一个符号测度, 则存在两个无交的可测集 $X^+$ 和 $X^-$ 使得 $X=X^+\sqcup X^-$, 且对任意 $A\in\mathscr{A}$, 有

$$
\mu(A\cap X^+)\ge0\ge\mu(A\cap X^-),
$$

如果 $X^+_1$ 和 $X^-_1$ 是满足该要求的令一对可测集, 那么有 $\mu(X^+\bigtriangleup X^+_1)=\mu(X^-\bigtriangleup X^-_1)=0$.

</div>

称定理里的无交集为 $X$ 在符号测度 $\mu$ 下的哈恩分解, 哈恩分解在对称差差一个零测集的意义下是唯一的.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(奇异性)</b>

设一个可测空间上有两个符号测度 $\mu$ 和 $\nu$, 如果存在一个可测集 $A$, 使得 $\mu(A)=\nu(X-A)=0$, 则称 $\mu$ 和 $\nu$ 是相互奇异的, 记为 $\mu\perp\nu$.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(若尔当分解定理)</b>

设 $\mu$ 是 $(X,\mathscr{A})$ 上的一个不取负无穷的符号测度, 则唯一存在 $X$ 上一个正测度 $\mu^+$ 和一个有限正测度 $\mu^-$ 有

$$
\mu=\mu^+-\mu^-,
$$

且 $\mu^+\perp\mu^-$.

</div>

称定理中的两个测度为测度 $\mu$ 的若尔当分解, 称 $\mu^+$ 为正变差测度, $\mu^-$ 为负变差测度, 定义 $\lvert\mu\rvert=\mu^++\mu^-$ 为 $\mu$ 的全变差测度. 如果 $\lvert\mu\rvert$ 是 $\sigma$-有限的, 我们就说符号测度 $\mu$ 是 $\sigma$-有限的. 定义 $L^1(\mu)=L^1(\mu^+)\cap L^1(\mu^-)$, 对于 $f\in L^1(\mu)$, 定义 $\int f\,\mathrm{d}\mu=\int f\,\mathrm{d}\mu^+-\int f\,\mathrm{d}\mu^-$.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(绝对连续)</b>

设一个可测空间上有一个符号测度 $\nu$ 和一个正测度 $\mu$, 对任意可测集 $A$, 如果 $\mu(A)=0$ 总能推出 $\nu(A)=0$, 则称 $\nu$ 对 $\mu$ 是绝对连续的, 记为 $\nu\ll\mu$.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(勒贝格分解定理)</b>

设 $(X, \mathscr{A})$ 是可测空间, $\nu$ 是其上一个 $\sigma$-有限符号测度, $\mu$ 是其上一个 $\sigma$-有限正测度, 则存在唯一的一对 $\sigma$-有限符号测度 $\lambda$ 和 $\rho$ 使得

$$
\lambda \perp \mu, \quad \rho \ll \mu, \quad  \nu = \lambda + \rho.
$$

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(拉东-尼科迪姆定理)</b>

设 $(X, \mathscr{A})$ 是可测空间, $\nu$ 是其上一个 $\sigma$-有限符号测度, $\mu$ 是其上一个 $\sigma$-有限正测度, 并且 $\nu\ll\mu$, 则在几乎处处相等的意义下存在唯一一个 $\mu$-可积函数 $f\colon X \to \mathbb{R}$ 使得

$$
\nu(A)=\int_A f\,\mathrm{d}\mu, \ \forall A\in\mathscr{A}.
$$

</div>

以后我们将 $\nu(A)=\int_A f\,\mathrm{d}\mu$ 记作 $\mathrm{d}\nu=f\,\mathrm{d}\mu$ 或 $f=\frac{\mathrm{d}\nu}{\mathrm{d}\mu}$, 称 $f$ 为 $\nu$ 对 $\mu$ 的拉东-尼科迪姆导数. 这里的分数符号仅是形式上的, 但接下来我们可以看到它确实具有某种意义下的换元法或链式法则.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>

设 $(X, \mathscr{A})$ 是可测空间, $\nu$ 是其上一个 $\sigma$-有限符号测度, $\mu$ 和 $\lambda$ 是其上是 $\sigma$-有限正测度, 并且满足 $\nu\ll\mu$, $\mu\ll\lambda$, 设 $g \in L^1(\nu)$, 那么 $g\frac{\mathrm{d}\nu}{\mathrm{d}\mu} \in L^1(\mu)$, 并且

$$
\int g\,\mathrm{d}\nu = \int g \frac{\mathrm{d}\nu}{\mathrm{d}\mu}\,\mathrm{d}\mu.
$$

此外还有 $\nu \ll \lambda$, 并且

$$
\frac{\mathrm{d}\nu}{\mathrm{d}\lambda} = \frac{\mathrm{d}\nu}{\mathrm{d}\mu} \frac{\mathrm{d}\mu}{\mathrm{d}\lambda}
$$

$\lambda$-几乎处处成立.

</div>

### 复测度

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(复测度)</b>

$(X,\mathscr{A})$ 是一个可测空间, 其上的复测度 $\mu$ 是一个函数 $\mu\colon \mathscr{A} \to \mathbb{C}$ 使得:<br>

1, $\mu(\emptyset) = 0,$<br>

2, 如果 $\{E_i\}_{i=1}^{\infty}$ 是 $\mathscr{A}$ 中无交集合的一个序列, 那么

$$
\mu\left(\bigcup_{i=1}^{\infty} E_i\right) = \sum_{i=1}^{\infty} \mu(E_i)
$$

绝对收敛.

</div>

需要注意的是复测度不允许取无穷远点, 显然, 有限的测度和符号测度都是复测度.

任何复测度可以由 $\mu(E)=\mathrm{Re}(\mu(E))+\mathrm{Im}(\mu(E))i$ 分解为实部和虚部, 分别为有限符号测度, 这样的分解显然是唯一的, 记为 $\mu_r$ 和 $\mu_i$, 定义 $L^1(\mu)=L^1(\mu_r)\cap L^1(\mu_i)$, 对于 $f\in L^1(\mu)$, 定义 $\int f\,\mathrm{d}\mu=\int f\,\mathrm{d}\mu_r+i\int f\,\mathrm{d}\mu_i$.

设 $\mu$ 和 $\nu$ 是复测度, 定义 $\mu\perp \nu$ 当且仅当 $\mu_r\perp\nu_r$ 且 $\mu_i\perp\nu_i$. 设 $\lambda$ 是正测度, 则定义 $\mu\ll\lambda$ 当且仅当 $\mu_r\ll\lambda$ 且 $\mu_i\ll\lambda$.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(复测度的勒贝格-拉东-尼科迪姆定理)</b>

设 $(X, \mathscr{A})$ 是可测空间, $\nu$ 是其上一个复测度, $\mu$ 是其上一个 $\sigma$-有限正测度, 则存在唯一的一对复测度 $\lambda$ 和 $\rho$ 使得

$$
\lambda \perp \mu, \quad \rho \ll \mu, \quad  \nu = \lambda + \rho
$$

成立, 并且在几乎处处相等的意义下存在唯一一个 $f\in L^1(\mu)$ 使得 $\mathrm{d}\rho=f\,\mathrm{d}\mu$.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(全变差测度)</b>

设 $(X, \mathscr{A})$ 是可测空间, $\nu$ 是其上一个复测度, $\mu$ 是其上一个 $\sigma$-有限正测度使得 $\nu\ll\mu$, 则存在唯一的 $f\in L^1(\mu)$, $\mathrm{d}\nu=f\,\mathrm{d}\mu$, 对任意 $A\in\mathscr{A}$, 定义 $\nu$ 的全变差测度为

$$
\lvert\nu\rvert(A)=\int_A \lvert f\rvert\,\mathrm{d}\mu,
$$

可以验证这样的定义与 $\mu$ 和 $f$ 的选取无关.

</div>

可以证明全变差测度确实是测度.

设 $X$ 是局部紧豪斯多夫空间, $C_0(X)$ 为 $X$ 上满足对 $\forall\varepsilon>0$, $\\{x\mid \lvert f(x)\rvert>\varepsilon\\}$ 是紧集的连续函数(也称为在无穷远点消失的连续函数) $f$ 组成的线性空间, 它是 $C_c(X)$ 的一致闭包, 即 $C_0(X)$ 中的每个函数都是 $C_c(X)$ 中一个函数列在上确界范数(也叫一致范数或无穷范数)下的极限.

符号拉东测度定义为正部和负部均为拉东测度的符号测度, 复拉东测度定义为实部和虚部均为符号拉东测度的复测度, 第二可数的局部紧豪斯多夫空间上的复测度都是复拉东测度.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(里斯表示定理)</b>

设局部紧豪斯多夫空间 $X$ 上所有复拉东测度组成的线性空间为 $M(X)$, 其上有范数 $\|\mu\|=|\mu|(X)$, 即全变差测度在空间 $X$ 上的值, 则对每个 $\mu\in M(X)$, 定义

$$
L_\mu(f)=\int_X f\,\mathrm{d}\mu,\forall f\in C_0(X)
$$

为 $C_0(X)$ 上的线性泛函, 则 $\mu\mapsto L_\mu$ 给出等距同构 $M(X)\cong C_0(X)^*$.

</div>

若 $X$ 是紧豪斯多夫空间, 则 $M(X)\cong C(X)^*$.

### 哈尔测度

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(拓扑群)</b>

设 $G$ 同时是拓扑空间和群, 如果乘法 $G\times G\to G$, $(g,h)\mapsto gh$ 和取逆 $G\to G$, $g\mapsto g^{-1}$ 是连续映射, 则称 $G$ 是拓扑群.

</div>

等价的抽象废话是, 拓扑群是拓扑空间范畴里的群对象.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(局部紧群)</b>

如果拓扑群 $G$ 是局部紧且豪斯多夫的, 则称其为局部紧群, 如果还是交换的, 则称其为局部紧交换群, 或简称为LCA群.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(不变测度)</b>

如果局部紧群 $G$ 上的博雷尔测度 $\mu$ 对任意可测集 $E$ 和任意元素 $g$, 有 $\mu(gE)=\mu(E)$, 则称它是左不变的, 如果有 $\mu(Eg)=\mu(E)$, 则称它是右不变的.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(哈尔测度)</b>

局部紧群 $G$ 上的非零左不变拉东测度称为左哈尔测度, 非零右不变拉东测度称为右哈尔测度, LCA群上的左右哈尔测度是等价的, 统称为哈尔测度.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(哈尔定理)</b>

局部紧群上一定存在左哈尔测度, 并且在差一个正数倍的意义下是唯一的, 右哈尔测度同理.

</div>

哈尔测度下的积分称为哈尔积分. 若 $\mu$ 是左哈尔测度, $f\in C_c(G)$, 则对任意 $h\in G$, 有

$$
\int_G f(g)\,\mathrm{d}\mu(g)=\int_G f(hg)\,\mathrm{d}\mu(g),
$$

右哈尔测度的积分类似.

左哈尔测度和右哈尔测度之间未必差常数倍, 二者直接的差异由模函数描述.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(模函数)</b>

设 $\mu$ 是局部紧群 $G$ 上的一个左不变测度, 对任意 $g\in G$, 定义 $\mu_g(E)=\mu(Eg)$, 显然 $\mu_g$ 也是一个左不变测度, 则它与 $\mu$ 相差一个正数倍, 设为 $\Delta(g)$, 这样定义的函数 $\Delta\colon G\to \mathbb{R}_{>0}$ 称为群 $G$ 的右模函数. 如果 $\Delta\equiv 1$, 则称群 $G$ 是酉模群.

</div>

由于 $\Delta(gh)\mu(E)=\mu(Egh)=\Delta(h)\mu(Eg)=\Delta(h)\Delta(g)\mu(E)=\Delta(g)\Delta(h)\mu(E)$, 所以 $\Delta$ 是从群 $G$ 到群 $(\mathbb{R}_{>0},\times)$ 的群同态. 对任意 $h\in G$, 有

$$
\int_G f(gh)\,\mathrm{d}\mu(g)=\Delta(h^{-1})\int_G f(g)\,\mathrm{d}\mu(g),
$$

右哈尔测度和左模函数的情形类似.

交换群显然是酉模群, 可以证明, 如果 $G$ 商掉交换子子群得到的商群 $G/[G,G]$ 是有限群, 则群 $G$ 一定是酉模群. 如果群 $G$ 是紧群, 则它一定是酉模群.

### 黎曼测度

设 $(M,g)$ 为黎曼流形, 我们定义其上的测度, 使得关于测度的积分和流形上微分形式的积分相等.

在 $M$ 中点 $p$ 附近的局部坐标 $(U_p,\varphi_p)$ 下, 黎曼度量可以写为

$$
g\vert _{U_p}=\sum _{i,j}g^p_{ij}\mathrm{d}x^i\otimes\mathrm{d}x^j,
$$

其中 $g^p_{ij}$ 是 $U_p$ 上的光滑函数, 它们组成一个处处正定的矩阵 $(g^p_{ij})_{n\times n}$, 其行列式记为 $\det(g_{ij}^p)>0$, 行列式的值在不同点附近相差坐标变换函数的雅可比行列式的平方倍.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(体积形式)</b>

设 $(M,g)$ 为可定向黎曼流形, $\{(U_p,\varphi_p)\}$ 是其上的定向坐标覆盖, 在 $U_p$ 上定义微分形式

$$
\Omega\vert _{U_p}=\sqrt{\det (g_{ij}^p)}\mathrm{d}x_p^1\wedge\cdots\wedge\mathrm{d}x_p^n,
$$

由于在坐标变换下, $\sqrt{\det (g_{ij}^p)}$ 相差坐标变换函数的雅可比行列式倍, 与 $x_p^1\wedge\cdots\wedge\mathrm{d}x_p^n$ 的变换产生的雅可比行列式刚好抵消, 因此以上定义的 $\Omega$ 在不同局部坐标系下相同, 是 $M$ 上整体的微分形式, 称为体积形式, 有时也记为 $\mathrm{d}V_g$.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(黎曼测度)</b>

设 $(M,g)$ 为可定向黎曼流形, $\{(U_p,\varphi_p)\}$ 是其上的定向坐标覆盖, 黎曼流形上的 $\sigma$-代数取博雷尔代数. 由单位分解定理, 存在从属于覆盖 $\{(U_p,\varphi_p)\}$ 的单位分解 $\{a_k\colon M\to\mathbb{R}\}_{k\in I}$, 使得 $\mathrm{supp}(a_k)\subseteq U_{p(k)}$, 对任意可测集 $E$, 定义

$$
\mu_g(E)=\sum_{k\in I} \int_{\varphi_{p(k)}(U_{p(k)})}\chi_E(y)a_k(y)\sqrt{\det\left( g_{ij}^{y}\right)}\,\mathrm{d}x^1\cdots\mathrm{d}x^n,\quad \text{其中 }\, y=\varphi_{p(k)}^{-1}(x),
$$

右边的积分是 $\mathbb{R}^n$ 的勒贝格积分, 它有可能取到无穷大. 容易验证 $\mu_g$ 是良定的, 并且是 $M$ 上的一个博雷尔测度, 称为黎曼测度.

</div>

黎曼测度显然是局部有限的, 因为如果 $K$ 是 $M$ 的紧可测子集, $\mu_g(K)=\int_M\chi_K\,\mathrm{d}V_g$, 等式右边是具有紧支集 $K$ 的微分形式 $\chi_K \mathrm{d}V_g$ 的积分, 是一个有限数. 事实上黎曼测度还是一个拉东测度.

由构造即可得到以下定理.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>

如果 $f$ 是可定向黎曼流形 $(M,g)$ 上具有紧支集的函数, $\mu_g$ 是黎曼测度, 则

$$
\int_Mf\,\mathrm{d}\mu_g=\int_Mf\,\mathrm{d}V_g,
$$

等式左边为黎曼测度下的积分, 右边为微分形式的积分.

</div>

### 向量测度

本节中巴拿赫空间 $V$ 都指实数域或复数域上的巴拿赫空间.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(向量值简单函数)</b>

设 $V$ 是巴拿赫空间, 定义在可测空间 $X$ 上的函数如果取值为 $V$ 中有限个值, 则称其为向量值简单函数, 等价的说, 是有限个特征函数的 $V$-系数线性组合.

</div>

设 $(X,\mathscr{A},\mu)$ 是一个测度空间, $s$ 是 $X$ 上向量值简单函数, 设

$$
s(x)=\sum_{i=1}^nc_i\chi_{E_i},\quad c_i\in V-\{0\},
$$

$E_i$ 是 $X$ 的无交可测子集, 则定义 $s$ 的博赫纳积分为

$$
\int_Xs\,\mathrm{d}\mu=\sum_{i=1}^nc_i\mu(E_i).
$$

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(博赫纳可测)</b>

设 $(X,\mathscr{A},\mu)$ 是一个测度空间, $(V,\|\cdot\|)$ 是一个巴拿赫空间, $f\colon X\to V$, 如果存在一列简单函数 $\{s_i\}_{i=1}^\infty$ 使得

$$
\lim_{n\to\infty} \|f-s_n\|
$$

几乎处处成立, 则称 $f$ 是博赫纳可测的或强可测的.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(博赫纳可积)</b>

设 $(X,\mathscr{A},\mu)$ 是一个测度空间, $(V,\|\cdot\|)$ 是一个巴拿赫空间, $f\colon X\to V$ 是博赫纳可测函数, 如果存在一列简单函数 $\{s_i\}_{i=1}^\infty$ 使得

$$
\lim_{n\to\infty}\int_X \|f-s_n\|\,\mathrm{d}\mu=0,
$$

则称 $f$ 是博赫纳可积的.

</div>

博赫纳可积比博赫纳可测更强, 可积一定可测, $f$ 博赫纳可积当且仅当 $f$ 博赫纳可测且普通的标量值积分 $\int_X\|f(x)\|\,\mathrm{d}\mu(x)<\infty$. 可以证明, 如果一个函数博赫纳可积, 则定义中逼近它的简单函数的积分列 $\int_X s_n\,\mathrm{d}\mu$ 也收敛, 并且收敛的值与逼近函数列的选取无关.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(博赫纳积分)</b>

设 $(X,\mathscr{A},\mu)$ 是一个测度空间, $(V,\|\cdot\|)$ 是一个巴拿赫空间, $f\colon X\to V$ 是博赫纳可积函数, 则定义它的博赫纳积分为

$$
\int_Xf\,\mathrm{d}\mu=\lim_{n\to\infty}\int_X s_n\,\mathrm{d}\mu,\quad \int_E f\,\mathrm{d}\mu=\int_X \chi_E f\,\mathrm{d}\mu,
$$

其中 $\{s_i\}_{i=1}^\infty$ 是任意一列使得 $\lim_{n\to\infty}\int_X \|f-s_n\|\,\mathrm{d}\mu=0$ 成立的简单函数列, $E$ 是 $X$ 的可测子集.

</div>

当取 $V=\mathbb{C}$ 时, 博赫纳积分就是通常的勒贝格积分.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>

若 $f\colon X\to V$ 是博赫纳可积函数, 则对任意可测集 $E$, 有

$$
\left\|\int_E f\,\mathrm{d}\mu\right\|\le\int_E \|f\|\,\mathrm{d}\mu,
$$

对任意巴拿赫空间间的线性算子 $T\colon V\to W$, 有

$$
T\left(\int_E f\,\mathrm{d}\mu\right)=\int_E T(f)\,\mathrm{d}\mu.
$$

</div>

很多测度论的结论都能推广到博赫纳积分上.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(弱可测)</b>

设 $(X,\mathscr{A},\mu)$ 是一个测度空间, $(V,\|\cdot\|)$ 是域 $k$ 上的一个巴拿赫空间, $f\colon X\to V$.<br>

如果对偶空间 $V^*$ 内的任一元素 $\varphi\colon V\to k$, 都有 $\varphi\circ f\colon X\to k$ 是通常的可测函数, 其中域 $k$ 上带博雷尔代数, 则称 $f$ 是弱可测的.<br>

如果对于 $\varphi\in \Gamma\subseteq V^*$, 都有 $\varphi\circ f\colon X\to k$ 是可测函数, 则称 $f$ 是 $\Gamma$-弱可测的.<br>

将 $V$ 看做 $V^{**}$ 的子空间, 如果 $f\colon X\to V^*$ 是 $V$-弱可测的, 则称 $f$ 是弱 $\!^*$ 可测的.

</div>

强可测函数一定弱可测.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(邓福德)</b>

设 $(X,\mathscr{A},\mu)$ 是一个测度空间, $(V,\|\cdot\|)$ 是域 $k$ 上的一个巴拿赫空间, $f\colon X\to V$ 是弱可测的, 并且对任意的 $\varphi\in V^*$, $\varphi\circ f\colon X\to k$ 都是通常的可积函数, 则对于任意可测集 $E$, 存在唯一的 $I_E\in V^{**}$, 使得

$$
I_E(\varphi)=\int_E \varphi(f(x))\,\mathrm{d}\mu(x)
$$

对任意 $\varphi\in V^*$ 都成立.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(邓福德积分)</b>

设 $(X,\mathscr{A},\mu)$ 是一个测度空间, $(V,\|\cdot\|)$ 是域 $k$ 上的一个巴拿赫空间, $f\colon X\to V$ 是弱可测的, 并且对任意的 $\varphi\in V^*$, $\varphi\circ f\colon X\to k$ 都是通常的可积函数, 则称 $f$ 是邓福德可积的, 并定义使得 $I_E(\varphi)=\int_E \varphi(f(x))\,\mathrm{d}\mu(x)$ 成立的 $I_E$ 为 $f$ 在 $E$ 上的邓福德积分, 记作

$$
I_E=(D)\int_Ef\,\mathrm{d}\mu.
$$

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(弱可积)</b>

设 $(X,\mathscr{A},\mu)$ 是一个测度空间, $(V,\|\cdot\|)$ 是域 $k$ 上的一个巴拿赫空间, $f\colon X\to V$ 是弱可测的, 并且对任意的 $\varphi\in V^*$, $\varphi\circ f\colon X\to k$ 都是通常的可积函数, 如果存在 $I\in V$, 使得

$$
\varphi(I)=\int_X \varphi(f(x))\,\mathrm{d}\mu(x)
$$

成立, 则称 $f$ 在 $X$ 上弱可积.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(佩蒂斯积分)</b>

设 $(X,\mathscr{A},\mu)$ 是一个测度空间, $(V,\|\cdot\|)$ 是域 $k$ 上的一个巴拿赫空间, $f\colon X\to V$ 是弱可测的, 并且对任意的 $\varphi\in V^*$, $\varphi\circ f\colon X\to k$ 都是通常的可积函数, 如果对于任意可测集 $E$, 都存在 $I_E\in V$, 使得

$$
\varphi(I_E)=\int_E \varphi(f(x))\,\mathrm{d}\mu(x)
$$

成立, 则称 $f$ 是佩蒂斯可积的, 定义 $I_E$ 为 $f$ 在 $E$ 上的佩蒂斯积分, 记作

$$
I_E=(P)\int_Ef\,\mathrm{d}\mu.
$$

</div>

佩蒂斯积分也是唯一的, 将 $V$ 典范的嵌入 $V^{\*\*}$ 后, 有 $I_E^{\*\*}(\varphi)=\varphi(I_E)$, 显然佩蒂斯可积当且仅当邓德福可积且积分值 $I_E\in V$. 如果 $V$ 是自反的, 则两种积分是完全等价的.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(盖尔方德积分)</b>

设 $(X,\mathscr{A},\mu)$ 是一个测度空间, $(V,\|\cdot\|)$ 是域 $k$ 上的一个巴拿赫空间, $f\colon X\to V^*$ 是弱 $\!^*$ 可测的, 并且对任意的 $\varphi\in V$, 如果 $\varphi\circ f\colon X\to k$ 是通常的可积函数, 且对于任意可测集 $E$, 存在 $I_E\in V^*$, 使得

$$
I_E(\varphi)=\int_E \varphi(f(x))\,\mathrm{d}\mu(x)
$$

成立, 则称 $f$ 是盖尔方德可积或弱 $\!^*$ 可积的, 定义 $I_E$ 为 $f$ 在 $E$ 上的盖尔方德积分或弱 $\!^*$ 积分, 记作

$$
I_E=(\Gamma)\int_Ef\,\mathrm{d}\mu.
$$

</div>

可以证明盖尔方德积分也是唯一存在的.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(向量测度)</b>

设 $\mathscr{A}$ 是 $X$ 的子集构成的代数, $V$ 是一个巴拿赫空间, 函数 $F\colon \mathscr{A}\to V$ 如果满足 $F(\emptyset)=0$, 并且有有限可加性 $F\left(\bigcup_{i=1}^{n} E_i\right) = \sum_{i=1}^{n} F(E_i)$, 其中诸 $E_i\in\mathscr{A}$ 无交, 则称 $F$ 是 $X$ 上的一个向量测度, 如果还有可数可加性 $F\left(\bigcup_{i=1}^{\infty} E_i\right) = \sum_{i=1}^{\infty} F(E_i)$ 按范数收敛, 其中诸 $E_i\in\mathscr{A}$ 无交, 则称 $F$ 是可数可加向量测度.

</div>

向量测度 $F$ 的变差定义为

$$
\lvert F \rvert (A) = \sup \left\{ \sum_{i=1}^{\infty} \| F(A_i) \| \middle\vert A = \bigsqcup_{i=1}^{\infty} A_i,A_i\in \mathscr{A}\right\},
$$

半变差定义为

$$
\| F \| (A) = \sup \left\{ \lvert \varphi\circ F\rvert(A) \middle\vert \varphi\in V^*,\|\varphi\|\le1\right\},
$$

其中 $\lvert \varphi\circ F\rvert$ 是符号测度或复测度的全变差测度. 变差有界的向量测度称为有界变差向量测度, 半变差有界的向量测度称为有界半变差向量测度或有界向量测度.

设 $\mathscr{A}$ 是 $X$ 的子集构成的代数, $F$ 是 $X$ 上的一个有界向量测度, $s$ 是 $X$ 上标量值简单函数, 设

$$
s(x)=\sum_{i=1}^nc_i\chi_{E_i},\quad c_i\in k-\{0\},
$$

$E_i$ 是 $X$ 的无交可测子集, 则定义 $s$ 的巴特尔积分为

$$
T_F(s)=\sum_{i=1}^nc_i F(E_i)\in V.
$$

令 $B(\mathscr{A})$ 是 $X$ 上所有有界可测标量值函数构成的线性空间, 它是所有简单函数组成的集合的一致闭包, 可将线性泛函 $T_F$ 延拓到 $B(\mathscr{A})$ 上, 仍记为 $T_F$.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(巴特尔积分)</b>

设 $\mathscr{A}$ 是 $X$ 的子集构成的代数, $F$ 是 $X$ 上的一个有界向量测度, 对于 $f\in B(\mathscr{A})$, 定义其巴特尔积分为

$$
\int_Xf\,\mathrm{d}F=T_F(f),\quad \int_Ef\,\mathrm{d}F=\int_X\chi_E f\,\mathrm{d}F.
$$

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>

设 $\mathscr{A}$ 是 $X$ 的子集构成的代数, 则 $F\mapsto T_F$ 给出所有有界向量测度组成的线性空间与 $L(B(\mathscr{A}),V)$ 之间的线性同构, 并且有 $\|F\|(X)=\|T_F\|$, 后者为算子范数.

</div>

### 豪斯多夫测度

以下使用度量空间理论中常见的记号, $d(A,B)=\inf\\{d(a,b)\mid a\in A,b\in B\\}$, $\mathrm{diam}(A)=\sup\\{d(a,b)\mid a,b\in A\\}$.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(度量外测度)</b>

设 $(X,d)$ 是度量空间, $\mu^*$ 是 $X$ 上的一个外测度, 对任意 $A,B\subseteq X$, 如果 $d(A,B)>0$, 有 $\mu^*(A\cup B)=\mu^*(A)+\mu^*(B)$ 成立, 则称 $\mu^*$ 是一个度量外测度.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(豪斯多夫测度)</b>

设 $(X,d)$ 是度量空间, $p\in\mathbb{R}_{\ge0}$, $\delta\in\mathbb{R}_{>0}$, 对于 $A\subseteq X$, 定义

$$
H_\delta^p(A)=\inf\left\{\sum_{i=1}^\infty\left(\mathrm{diam(E_i)}\right)^p\middle\vert A\subseteq\bigcup_{i=1}^\infty E_i, \mathrm{diam}(E_i)\le\delta,\forall i\in\mathbb{Z}_{\ge1}\right\},
$$

令 $\delta\to0$, 定义

$$
H^p(A)=\lim_{\delta\to0}H^p_\delta(A),
$$

由此定义了 $X$ 上的一个外测度 $H^p$, 称为 $p$ 维豪斯多夫外测度, 简称豪斯多夫测度.

</div>

首先要说明豪斯多夫测度是良定的, 可以证明 $H_\delta^p$ 是一个外测度. 设 $0<\delta_1<\delta_2$, 则 $\mathrm{diam}(E)<\delta_1$ 自然能推出 $\mathrm{diam}(E)<\delta_2$, 故 $H_{\delta_1}^p\ge H_{\delta_2}^p$, 当 $\delta\to0$ 时, $H_\delta^p$ 收敛到一个非负实数或趋于无穷大, 直觉上来说, 这与海岸线悖论是相符的. 可以证明 $H^p$ 是一个度量外测度.

注1: 取 $X=\mathbb{R}^n$ 时, $n$ 维豪斯多夫测度与勒贝格外测度之间差一个常数倍, 这个常数与 $n$ 维球的体积有关, 事实上, 设 $m^*$ 是勒贝格外测度, 则有

$$
\frac{\pi^{\frac{n}{2}}}{2^n\Gamma\left(\frac{n}{2}+1\right)}H^n=m^*.
$$

注2: $H^0$ 实际上就是计数测度.

注3: 将 $\mathbb{R}^n$ 上的 $n$ 维豪斯多夫外测度 $H^n$ 做成真正的测度后, 再限制定义域到博雷尔代数上, 得到的测度是一个拉东测度.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>

设 $H^p$ 是度量空间 $X$ 上的豪斯多夫测度, 则对任意子集 $A\subseteq X$, 若 $H_p(A)<\infty$, 则对任意 $q>p$, 有 $H^q(A)=0$; 若 $H_p(A)>0$, 则对任意 $q<p$, 有 $H^q(A)=+\infty$.

</div>

这意味着, 对大多数集合, 随着 $p$ 增大, $p$ 维豪斯多夫测度由无穷突变到一个有限数再突变为 $0$, 也就是说

$$
\inf \{ p \ge 0 \mid H^p(A) = 0 \} = \sup \{ p \ge 0 \mid H^p(A) = + \infty \},
$$

我们称这个数为集合 $A$ 的豪斯多夫维数.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(豪斯多夫维数)</b>

设 $H^p$ 是度量空间 $X$ 上的豪斯多夫测度, 则对任意子集 $A\subseteq X$, 定义 $A$ 的豪斯多夫维数为

$$
\dim_H(A)=\inf \{ p \ge 0 \mid H^p(A) = 0 \}.
$$

</div>

可以证明豪斯多夫维数一定大于等于拓扑维数, 曼德博将分形定义为豪斯多夫维数严格大于其拓扑维数的集合, 这个定义是不够好的, 因为它将一些被人们认为是分形的集合排除在外, 目前一般认为分形并没有一个严格的定义.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(相似变换)</b>

设 $r > 0$, 比例因子为 $r$ 的相似变换是映射

\begin{align*}
    S\colon \mathbb{R}^n &\to \mathbb{R}^n\\
    x & \mapsto rO(x) + b,
\end{align*}

其中 $O$ 是一个正交变换, $b \in \mathbb{R}^n$.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(不变性)</b>

设 $S=(S_1,\dots,S_m)$ 为比例因子都为 $r$ 的相似变换组成的 $m$ 元组, 其中 $0<r<1$, 对于 $\mathbb{R}^n$ 中子集 $E$, 定义

$$
S^0(E)=E,\quad S^1(E)=\bigcup_{i=1}^m S_i(E),\quad S^{k+1}(E)=S(S^k(E)),
$$

如果 $S(E)=E$, 则称 $E$ 在相似变换族 $S$ 下是不变的.

</div>

不变性是不够好的, 例如 $\mathbb{R}^n$ 和空集 $\emptyset$ 在任何相似变换族下都是是不变的, 但显然不是我们想要的自相似分形.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(分离集)</b>

设 $S=(S_1,\dots,S_m)$ 为比例因子都为 $r$ 的相似变换组成的 $m$ 元组, 其中 $0<r<1$, 如果有一个非空有界开集 $U$, 满足 $S(U)\subseteq U$, 且 $S_i(U)\cap S_j(U)=\emptyset$, $i\neq j$, 则称 $U$ 是 $S$ 的分离集.

</div>

如果相似函数族有分离集, 有时也称它满足开集条件.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>

设 $S=(S_1,\dots,S_m)$ 为比例因子都为 $r$ 的相似变换组成的 $m$ 元组, 其中 $0<r<1$, 并且它有分离集 $U$, 则

$$
\bigcap_{k=1}^\infty S^k(\overline{U})
$$

是一个非空紧集, 且在相似变换族 $S$ 下不变, 并且在 $S$ 下不变的非空紧集只有这一个.

</div>

称该定理中在 $S$ 下不变的非空紧集是在 $S$ 下自相似的.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>

设 $S=(S_1,\dots,S_m)$ 为比例因子都为 $r$ 的相似变换组成的 $m$ 元组, 其中 $0<r<1$, 它有分离集, 设 $X$ 在 $S$ 下自相似, 则

$$
\dim_H(X)=-\frac{\ln m}{\ln r}=\log_{\frac{1}{r}}m,
$$

并且有

$$
H^d(S_i(X)\cap S_j(X))=0,i\neq j,
$$

其中 $d=\dim_H(X)$.

</div>

直观来说, 因为 $X$ 是不变的, 并且诸 $S_i(X)$ 间交集的测度为 $0$, 则

$$
H^d(X)=H^d(S(X))=\sum_{i=1}^mH^d(S_i(X))=\sum_{i=1}^m r H^d(X)=mr^dH^d(X),
$$

消掉 $H^d(X)$ 即得 $mr^d=1$, 解得 $d=\log_{\frac{1}{r}}m$.

康托集是 $S=(S_1,S_2)$ 下的自相似集, 其中 $S$ 定义在 $\mathbb{R}$ 上, $r=\frac{1}{3}$,

$$
S_1(x)=\frac{x}{3},\quad S_2(x)=\frac{x+2}{3},
$$

它的分离集为开区间 $(0,1)$, 豪斯多夫维数为 $\log_3 2$.

谢尔宾斯基三角形是 $S=(S_1,S_2,S_3)$ 下的自相似集, 其中 $S$ 定义在 $\mathbb{R}^2$ 上, $r=\frac{1}{2}$,

$$
S_i(x,y)=\frac{(x,y)}{2}+b_i,\quad b_1=(0,0),\quad b_2=\left(\frac{1}{2},0\right),\quad b_3=\left(\frac{1}{4},\frac{1}{2}\right),
$$

它的分离集为以 $(0,0)$, $(\frac{1}{2},1)$ 和 $(1,0)$ 为顶点的开三角形, 豪斯多夫维数为 $\log_2 3$.

科赫雪花是 $S=(S_1,S_2,S_3,S_4)$ 下的自相似集, 其中 $S$ 定义在 $\mathbb{R}^2$ 上, $r=\frac{1}{2}$,

$$
S_i(x,y)=\frac{O_i(x,y)}{3}+b_i,\quad b_1=(0,0),\quad b_2=\left(\frac{1}{3},0\right),\quad b_3=\left(\frac{1}{2},\frac{\sqrt{3}}{6}\right), b_4=\left(\frac{2}{3},0\right),
$$

$$
O_1(x,y)=O_2(x,y)=(x,y),
$$

$$
\quad O_2(x,y)=\left( \frac{1}{2}x - \frac{\sqrt{3}}{2}y,\frac{\sqrt{3}}{2}x + \frac{1}{2}y \right),\quad O_3(x,y)=\left( \frac{1}{2}x + \frac{\sqrt{3}}{2}y,-\frac{\sqrt{3}}{2}x + \frac{1}{2}y \right),
$$

即 $O_2$ 和 $O_3$ 分别为绕原点逆时针旋转 $\frac{\pi}{3}$ 和 $-\frac{\pi}{3}$, 它的分离集为以 $(0,0)$, $\left(\frac{1}{3},0\right)$, $\left(\frac{1}{2},\frac{\sqrt{3}}{6}\right)$, $\left(\frac{2}{3},0\right)$ 和 $(1,0)$ 为顶点的折线段的凸包的内部, 也就是以 $(0,0)$, $\left(\frac{1}{2},\frac{\sqrt{3}}{6}\right)$ 和 $(1,0)$ 为顶点的开三角形, 它的豪斯多夫维数为 $\log_3 4$.

### 概率测度

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(概率空间)</b>

设 $(\Omega,\mathscr{A},P)$ 是测度空间, 如果满足 $P(\Omega)=1$, 则称 $(\Omega,\mathscr{A},P)$ 是概率空间, 称 $\Omega$ 为样本空间, $P$ 为概率测度或概率, $\mathscr{A}$ 为事件域, 其中元素称为事件, 称 $\Omega$ 为必然事件, $\emptyset$ 为不可能事件.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(独立事件)</b>

若 $A,B\in\mathscr{A}$, 且 $P(A\cap B)=P(A)P(B)$, 则称事件 $A$ 和 $B$ 是独立的, 更多元的情况类似.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(随机变量)</b>

设 $f$ 是从 $\Omega$ 到实数集 $\mathbb{R}$ 的可测函数, 则称 $f$ 为一个随机变量, 对实数集中任一博雷尔集 $B$, 称 $P(\{\omega\mid f(\omega)\in B\})=P(f^{-1}(B))$ 为 $f$ 的概率分布.

</div>

如果两个随机变量对任意博雷尔集确定的事件都是独立的, 则称两个随机变量是独立的.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(分布函数)</b>

设 $f$ 是 $\Omega$ 上的随机变量, 定义函数 $F\colon \mathbb{R}\to\mathbb{R}_{\ge0}$ 为

$$
F(x)=P(\{\omega\mid f(\omega)<x\}),
$$

称 $F$ 为 $f$ 的分布函数, 记为 $f(\omega)\sim F(x)$, 读作随机变量 $f$ 服从分布函数 $F$.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(密度函数)</b>

设 $f$ 是 $\Omega$ 上的随机变量, $f(\omega)\sim F(x)$, 如果存在可积实函数 $p(x)$ 使得

$$
F(x)=\int_{-\infty}^x p(y)\,\mathrm{d}y,
$$

则称 $p$ 为 $f$ 的密度函数.

</div>

例如, 密度函数为

$$
p(x) = \frac{1}{\sqrt{2\pi}\sigma} e^{-\frac{(x-\mu)^2}{2\sigma^2}}
$$

的分布函数为

$$
F(x) = \frac{1}{\sqrt{2\pi}\sigma} \int_{-\infty}^{x} e^{-\frac{(y-\mu)^2}{2\sigma^2}}\, dy.
$$

其中 $\mu$ 是实常数, $\sigma$ 是正常数, 则称该分布为正态分布, 简记为 $N(\mu,\sigma^2)$, 当 $\mu=0$, $\sigma=1$ 时称为标准正态分布. 服从正态分布的随机变量称为正态变量.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(数学期望)</b>

若随机变量 $f$ 可积, 则称积分

$$
E(f)=\int_\Omega f(\omega)\,\mathrm{d}P
$$

为 $f$ 的数学期望.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(方差, 标准差)</b>

若随机变量 $f$ 平方可积, 则称

$$
D(f)=E\left((f-E(f))^2\right)
$$

为 $f$ 的方差, 称

$$
\sigma(f)=\sqrt{E\left((f-E(f))^2\right)}
$$

为 $f$ 的标准差.

</div>

容易验证有 $\sigma^2(f)=E(f^2)-E^2(f)$. 如果随机变量 $f$ 有密度函数 $p(x)$, 则使用拉东-尼科迪姆导数理论可得

$$
E(f)=\int_{-\infty}^\infty xp(x)\,\mathrm{d}x.
$$

定义两个随机变量 $f$ 和 $g$ 的协方差为 $\mathrm{Cov}(f,g)=E\left((f-E(f))(g-E(g)\right)$, 相关系数为 $\rho_{fg}=\frac{\mathrm{Cov}(f,g)}{\sigma(f)\sigma(g)}$, 相关系数为正时称二者正相关, 为负时称二者负相关, 为 $0$ 时称二者不相关. 独立的随机变量一定不相关, 反之未必.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(切比雪夫大数定理)</b>

设随机变量序列 $f_1, f_2, \ldots$ 相互独立, 并且方差有公共上界 $D(f_i) < C$, 则对任意的 $\varepsilon>0$, 有

$$
\lim_{n \to \infty} P\left(\left\{x\middle\vert x\in X,\,\left|\frac{1}{n} \sum_{i=1}^{n} f_i(x) - \frac{1}{n} \sum_{i=1}^{n} E(f_i)\right| < \epsilon\right\}\right) = 1.
$$

</div>

切比雪夫大数定理可由马尔科夫大数定理推出.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(马尔科夫大数定理)</b>

设随机变量序列 $f_1, f_2, \ldots$ 满足

$$
\lim_{n \to \infty} \frac{1}{n^2} D\left(\sum_{i=1}^{n} f_i\right)= 0,
$$

则对于任意 $\varepsilon>0$, 有

$$
\lim_{n \to \infty} P\left(\left\{x\middle\vert x\in X,\, \left|\frac{1}{n} \sum_{i=1}^{n} f_i(x) - \frac{1}{n} \sum_{i=1}^{n} E(f_i)\right| < \varepsilon\right\}\right) = 1.
$$

</div>

# 积分理论

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(可测函数)</b>

设 $(X,\mathscr{A}_1)$ 和 $(Y,\mathscr{A}_2)$ 是可测空间, 函数 $f\colon X\to Y$ 如果满足

$$
\{f(E)\mid E\in\mathscr{A}_2 \}\subseteq\mathscr{A}_1,
$$

则称 $f$ 是 $(\mathscr{A}_1,\mathscr{A}_2)$-可测的或简称可测的.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(博雷尔函数)</b>

如果 $X$ 和 $Y$ 是两个拓扑空间, 其上的 $\sigma$-代数取博雷尔代数, 则可测函数 $f\colon X\to Y$ 称为博雷尔函数.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(实可测函数)</b>

设 $(X,\mathscr{A}_1)$ 是可测空间, 取 $Y$ 为实数集, $\sigma$-代数取博雷尔代数 $\mathscr{B}(\mathbb{R})$, 则可测函数 $f\colon X\to Y$ 称为实可测函数.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(勒贝格可测函数)</b>

如果 $X$ 是实数集, $Y$ 是实数或复数集, $X$ 上 $\sigma$-代数为勒贝格可测集组成的代数 $\mathscr{L}$, $Y$ 上 $\sigma$-代数为博雷尔代数, 则可测函数 $f\colon X\to Y$ 称为勒贝格可测函数.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(复可测函数)</b>

设 $(X,\mathscr{A}_1)$ 是可测空间, 取 $Y$ 为复数集, $\sigma$-代数取博雷尔代数 $\mathscr{B}(\mathbb{C})$, 则可测函数 $f\colon X\to Y$ 称为复可测函数.

</div>

需要注意复数集作为拓扑空间和实平面是同胚的, 对于复函数 $f(x)=u(x)+iv(x)$, $f$ 复可测当且仅当实函数 $u$ 和 $v$ 是实可测的. 之后的积分均对复可测函数定义, 它们对于实可测函数一般也是成立的.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(特征函数)</b>

设集合 $E$ 是 $X$ 的可测子集, 定义 $E$ 的特征函数为 $\chi_E\colon X\to\mathbb{R}$,

$$
\chi_E=
\begin{cases}
    1, & x\in E,\\
    0, & x\notin E.
\end{cases}
$$

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(简单函数)</b>

简单函数定义为取值为有限个复数值的函数, 等价的说, 是有限个特征函数的复系数线性组合.

</div>

显然特征函数和简单函数都是可测的. 如果简单函数 $\phi$ 的值域是 $\\{z_1,\dots,z_n\\}$, $z_i\neq0$, 设 $E_i=\phi^{-1}(\{z_i\})$, 则有标准表示

$$
\phi=\sum_{i=1}^n z_i\chi_{E_i}.
$$

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>

设 $(X, \mathscr{A})$ 是一个可测空间, 如果 $f\colon X \to [0, +\infty]$ 是可测的, 则存在一个简单函数序列 $\{\phi_n\}$ 使得 $0 \le \phi_1 \le \phi_2 \le \dots \le f$, $\phi_n \to f$ 逐点收敛, 并且在任何 $f$ 有界的集合上 $\phi_n \to f$ 一致收敛.

如果 $f\colon X \to \mathbb{C}$ 是可测的, 则存在一个简单函数序列 $\{\phi_n\}$ 使得 $0 \le |\phi_1| \le |\phi_2| \le \dots \le |f|$, $\phi_n \to f$ 逐点收敛, 并且在任何 $f$ 有界的集合上 $\phi_n \to f$ 一致收敛.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(非负函数的积分)</b>

设 $(X, \mathscr{A},\mu)$ 是一个测度空间, $\phi=\sum_{i=1}^n z_i\chi_{E_i}$ 是简单函数, 定义其积分为

$$
\int_X\phi\,\mathrm{d}\mu=\sum_{i=1}^nz_i\mu(\chi_{E_i}),
$$

设 $f\colon X\to [0,+\infty]$ 可测, 则定义其积分为

$$
\int_Xf\,\mathrm{d}\mu=\sup\left\{\int_X\phi\,\mathrm{d}\mu\middle\vert0\le\phi\le f,\phi\text{是简单函数}\right\}.
$$

</div>

积分区域和测度在自明的情况下可以省略. 积分线性性及单调性实属显然.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(勒贝格单调收敛定理)</b>

设 $\{f_n\}$ 是 $X$ 上一列非负实函数, 并且满足 $f_i\le f_{i+1}$, 令 $f=\lim_{n\to\infty} f_n$, 则有

$$
\int_X f \, \mathrm{d}\mu=\lim_{n\to\infty}\int_Xf_n\,\mathrm{d}\mu,
$$

其中等式两边可能取到无穷大.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>

设 $f$ 是 $X$ 上的非负实函数, 则 $\int f=0$ 当且仅当 $f$ 几乎处处为 $0$.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(法图引理)</b>

设 $\{f_n\}$ 是 $X$ 上一列非负实函数, 则

$$
\int \liminf_{m\to\infty} f_n \,\mathrm{d}\mu\le\liminf_{n\to\infty} \int f_n\,\mathrm{d}\mu.
$$

</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(实函数的积分)</b>

设 $(X, \mathscr{A},\mu)$ 是一个测度空间, $f\colon X\to [-\infty,+\infty]$ 可测, 设

$$
f^+\colon X\to[0,+\infty],\qquad\qquad\qquad f^-\colon X\to[0,+\infty],
$$

$$
f^+(x)=\begin{cases}
    f(x),&f(x)\ge0,\\
    0,& f(x)<0.
\end{cases}
\quad
f^-(x)=\begin{cases}
    0,&f(x)\ge0,\\
    -f(x),& f(x)<0.
\end{cases}
$$

如果 $\int f^+$ 和 $\int f^-$ 中至少有一个是有限数, 则定义 $f$ 的积分为

$$
\int_Xf\,\mathrm{d}\mu=\int_Xf^+\,\mathrm{d}\mu-\int_Xf^-\,\mathrm{d}\mu.
$$

</div>

若 $\int f$ 是有限数, 则称 $f$ 是勒贝格可积的, 简称可积.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(复函数的积分)</b>

设 $(X, \mathscr{A},\mu)$ 是一个测度空间, $f\colon X\to\mathbb{C}$ 可测, 如果 $\int \lvert f\rvert$ 是有限数, 则称 $f$ 是可积的, 定义其积分为

$$
\int_Xf\,\mathrm{d}\mu=\int_X\mathrm{Re}(f)\,\mathrm{d}\mu+i\int_X\mathrm{Im}(f)\,\mathrm{d}\mu.
$$

</div>

由于 $\lvert f\rvert\le\lvert \mathrm{Re}(f)\rvert+\lvert \mathrm{Im}(f)\rvert\le2\lvert f\rvert$, 则 $f$ 可积当且仅当其实部和复部可积.

可积复函数组成复数域上的一个线性空间, 记为 $L^1$ 空间或 $L^1(X)$ 或 $L^1(\mu)$. 它商掉几乎处处相等这个等价关系后, 按 $\|f\|_1=\int \lvert f\rvert$ 定义 $L^1$ 范数成为巴拿赫空间, 仍记为 $L^1$ 空间.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(勒贝格控制收敛定理)</b>

设 $\{f_n\}$ 是 $X$ 上一列可积函数, $f_n\to f$ 几乎处处收敛, 并且存在非负实函数 $g$, 使得 $\lvert f_n\rvert<g$ 对所有 $n$ 几乎处处成立, 则 $f$ 可积, 且

$$
\int f=\lim_{n\to\infty}\int f_n.
$$

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(勒贝格定理)</b>

设 $f$ 是区间 $[a,b]$ 上的有界实函数, 如果 $f$ 黎曼可积, 则一定也勒贝格可积, $f$ 黎曼可积当且仅当 $f$ 的不连续点组成一个零测集.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(几乎处处收敛, 沿测度收敛, 几乎一致收敛)</b>

设 $\{f_n\}$ 是 $X$ 上一列函数.<br>

如果对任意正数 $\varepsilon$,

$$
\lim_{n\to\infty}\mu(\{x\mid  x\in X, \lvert f_n(x)-f(x)\rvert>\varepsilon\})\to0,
$$

则称其沿测度收敛到 $f$.<br>

如果 $f_n\to f$ 在除一个零测集外逐点收敛到 $f$, 则称其几乎处处收敛到 $f$.<br>

如果 $f_n\to f$ 在除一个测度可以任意小的集合外一致收敛到 $f$, 则称其几乎一致收敛到 $f$.

</div>

显然一致收敛强于几乎一致收敛强于几乎处处收敛强于沿测度收敛, 沿 $L^1$ 范数收敛强于沿测度收敛, 当测度有限时, 几乎处处收敛等价于几乎一致收敛.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(叶果罗夫定理)</b>

假设 $\mu(X)$ 有限, 且 $f_1$, $f_2,$ $\dots$ 和 $f$ 是 $X$ 上的可测复值函数, 使得 $f_n \to f$ 几乎处处收敛, 则对任意的 $\varepsilon > 0$, 存在子集 $E \subset X$, 使得 $\mu(E) < \varepsilon$ 且 $f_n \to f$ 在 $X-E$ 上一致收敛.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(勒贝格微分定理)</b>

设 $f\in L^1(\mathbb{R})$, 令 $F(x)=\int_{-\infty}^x f\,\mathrm{d}\mu$, 则 $F'(x)=f(x)$ 几乎处处成立.

设 $f\in L^1(\mathbb{R}^n)$, 令 $B_r(a)=\{x\mid x\in X,\lvert x-a\rvert\le r \}$, 则

$$
\lim_{r\to0} \frac{1}{\mu(B_r(a))}\int_{B_r(a)}\lvert f-f(a)\rvert\,\mathrm{d}\mu=0,\quad\lim_{r\to0} \frac{1}{\mu(B_r(a))}\int_{B_r(a)} f\,\mathrm{d}\mu=f(a)
$$

对 $a\in\mathbb{R}^n$ 几乎处处成立.

</div>
