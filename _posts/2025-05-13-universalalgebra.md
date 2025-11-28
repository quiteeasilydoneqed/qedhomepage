---
layout: post
title: "泛代数与泛代数几何"
subtitle: ""
header-img: "img/post-bg-infinity.jpg"
header-mask: 0.3
math: true
tags:
  - 代数
  - 代数几何
---

本文原为泛代数学习笔记, 后来作为大三代数几何课程的期末论文上交.

# 泛代数基础

### 基础构造

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(笛卡尔积)</b>

设 $I$ 是指标集, 对于每个 $i \in I$, $A_i$ 是一个集合, 集合族 $\{A_i\}_{i \in I}$ 的笛卡尔积, $\prod_{i \in I} A_i$, 定义为

$$
\prod_{i \in I} A_i = \{f \mid f\colon I \to \bigcup_{i \in I} A_i, \forall i \in I, f(i) \in A_i\}.
$$

当 $I$ 为有限集时, 比如设 $|I|=n$, 等价的将 $\prod_{i \in I} A_i$ 中的元素记作 $n$ 元有序组 $(a_1,\cdots,a_n), a_i\in A_i$, 特别的, 当 $I$ 是空集时, 空积为一元集 $\{\emptyset\}$.

当 $A=A_i=A_j, i,j\in I$ 时, 笛卡尔积记作 $A^I$, 若 $|I|=n$, 也记作 $A^n$.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定义(二元关系)</b>

设 $A$ 和 $B$ 是两个集合, 从 $A$ 到 $B$ 的二元关系 $\sim$ 是 $A \times B$ 的一个子集, 即 $\sim \subseteq A \times B$, 若 $(a,b)\in \sim$, 则称 $a$ 和 $b$ 有关系 $\sim$, 记作 $a\sim b$. 若 $A=B$, 则称 $\sim$ 是 $A$ 上的一个二元关系.

</div>

#### 泛代数

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(n元函数)</b>

对于一个非空集合 $A$, $A$ 上的一个 $n$ 元函数或 $n$ 元运算是一个从 $A^n$ 到 $A$ 的函数, $n$ 是 $f$ 的元数, $(a_1, \ldots, a_n)$ 在 $n$ 元运算 $f$ 下的的像用 $f(a_1, \ldots, a_n)$ 表示. 如果 $A$ 上的运算 $f$ 的元数为零, 则称为零元运算, 它完全由 $A^0=\{\emptyset\}$ 中唯一元素 $\emptyset$ 在 $A$ 中的像 $f(\emptyset)$ 确定, 因此零元运算一般认为是 $A$ 中的一个元素.

</div>

我们这里只考虑有限元运算而不考虑无限元运算, 所以当我们说运算的时候默认是有限元运算.

一些特殊的函数在书写时按照通常的习惯书写, 例如二元函数加法 $+(a,b)$ 可写作 $a+b$, 一元函数取逆 $^{-1}(a)$ 可写作 $a^{-1}$, 零元函数单位元 $1(\emptyset)$ 则直接写作 $1$.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(型)</b>

一个型或标签或语言, 是一个函数符号的集合 $\mathcal{F}$, 其中每个 $\mathcal{F}$ 的元素 $f$ 都关联一个非负整数 $n$, 称为 $f$ 的元数, 则 $f$ 称为一个 $n$ 元函数符号, $\mathcal{F}$ 中 $n$ 元函数符号组成的子集用 $\mathcal{F}_n$ 表示.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定义(代数)</b>

如果 $\mathcal{F}$ 是一个型, 那么 $\mathcal{F}$ 型的代数 $\mathbf{A}$ 定义为一个有序对 $(A, F)$, 其中 $A$ 是一个非空集合, 称为 $\mathbf{A} = (A, F)$ 的论域或宇宙或全域, $F$ 称为 $A$ 上的函数集或运算集, 使得对于 $\mathcal{F}$ 中的每个 $n$ 元函数符号 $f$, 都存在一个 $A$ 上的 $n$ 元运算 $f^{\mathbf{A}}$, 在不引起歧义的情况下, 我们使用 $f$ 来表示 $f^{\mathbf{A}}$. 如果 $\mathcal{F}$ 是有限集, $\mathcal{F} = \{f_1, \cdots, f_k\}$, 我们通常用 $(A, f_1, \cdots, f_k)$ 来代替 $(A, F)$, 其中函数符号按元数降序排列.

</div>

约定代数一般使用粗体字母表示.

当论域 $A$ 为单元集时, 称 $\mathbf{A}$ 为平凡代数.

<div style="border: 3px solid #000; padding: 10px;">

<b>例(群)</b>

一个群 $\mathbf{G}$ 是一个 $\{\cdot , {}^{-1}, 1\}$ 型代数 $(G,\cdot , {}^{-1}, 1)$, 其中 $\cdot$ 是二元运算, ${}^{-1}$ 是一元运算, $1$ 是零元运算, 并且要满足以下公式:
<br>

$\mathrm{(1)}$ $x \cdot (y \cdot z) \approx (x \cdot y) \cdot z;$
<br>

$\mathrm{(2)}$ $x \cdot 1 \approx 1 \cdot x \approx x ;$
<br>

$\mathrm{(3)}$ $x \cdot x^{-1} \approx x^{-1} \cdot x \approx 1.$

</div>

在一些抽象代数课本中通常不将取逆 $^{-1}$ 当作一个运算, 而是将上述定义中的第三条公式换成含量词的公理: 对任意的 $x\in G$, 存在元素 $y$ 使得 $x \cdot y \approx y \cdot x \approx 1$. 我们不采用这种定义方式, 因为如果这样定义, 在后续定义的子代数中, 群的子代数可能只是半群而不一定是群.

<div style="border: 3px solid #000; padding: 10px;">

<b>例(环)</b>

环可以看作含两个二元运算, 加法和乘法, 一个一元运算, 加法逆元, 一个零元运算, 加法单位元 $0$, 的代数, 幺环则多一个零元运算, 即乘法单位元 $1$. 域则通常不能被看作代数, 因为域上的乘法逆只对非零元有定义, 即所谓的偏函数, 在泛代数中, 域只能看作特殊的环. 域也就是所谓的偏代数, 但我们在这里不考虑偏代数.

<br>

<b>例($R$-模)</b>

R-模即环 R 作用到交换群上得到的结构, 其上有无穷多个一元函数, 由左乘作用定义.

</div>

#### 同态与同构

设 $\mathbf{A}=(A,F)$ 和 $\mathbf{B}=(B,F')$ 是 $\mathcal{F}$ 型的两个代数, 则 $F$ 和 $F'$ 有一一对应 $f^{\mathbf{A}}\mapsto f^{\mathbf{B}}$.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(同态)</b>

设 $\mathbf{A}=(A,F)$ 和 $\mathbf{B}=(B,F')$ 是 $\mathcal{F}$ 型的两个代数, $\alpha$ 是 $A \to B$ 的映射, 如果对于每个 $n$ 元函数 $f \in \mathcal{F}$, 对于 $a_1, \cdots, a_n \in A$, 有

$$
\alpha (f^{\mathbf{A}}(a_1, \cdots, a_n)) = f^{\mathbf{B}}(\alpha (a_1), \cdots, \alpha (a_n)),
$$

则称 $\alpha$ 是 $\mathbf{A}$ 到 $\mathbf{B}$ 的同态.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定义(同构)</b>

设 $\mathbf{A}=(A,F)$ 和 $\mathbf{B}=(B,F')$ 是同型的两个代数, 设 $\alpha$ 是 $\mathbf{A}$ 到 $\mathbf{B}$ 的同态, 如果 $\alpha$ 是双射, 则称 $\alpha$ 是 $\mathbf{A}$ 到 $\mathbf{B}$ 的同构, 记作 $\mathbf{A} \cong \mathbf{B}$, 称 $\mathbf{A}$ 与 $\mathbf{B}$ 同构.

</div>

同态为单射则称为单同态, 同态为满射则称为满同态, 从一个代数到自身的同态称为自同态, 从一个代数到自身的同构称为自同构.

设 $\mathbf{A}=(A,F)$ 和 $\mathbf{B}=(B,F')$ 是 $\mathcal{F}$ 型的两个代数, 从 $\mathbf{A}$ 到 $\mathbf{B}$ 的所有同态记作 $\operatorname{Hom}(\mathbf{A},\mathbf{B})$.

容易验证, 同态的复合仍是同态, 若一对同态互逆, 则它们是同构.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(核)</b>

设 $\mathbf{A}=(A,F)$ 和 $\mathbf{B}=(B,F')$ 是同型的两个代数, 设 $\alpha$ 是 $\mathbf{A}$ 到 $\mathbf{B}$ 的同态, 那么 $\alpha$ 的核, 记作 $\ker(\alpha)$, 定义为 $\mathbf{A}$ 上的一个二元关系

$$
\ker(\alpha) = \{(a, b) \in A^2 \mid \alpha(a) = \alpha(b)\}.
$$

</div>

#### 子代数

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(子代数)</b>

设 $\mathbf{A}=(A,F)$ 和 $\mathbf{B}=(B,F')$ 是 $\mathcal{F}$ 型的两个代数, 如果 $B \subseteq A$ 并且 $\mathbf{B}$ 中的每个运算都是 $\mathbf{A}$ 中相应运算的限制, 即如果 $f^{\mathbf{A}}$ 是 $\mathbf{A}$ 中的一个 $n$ 元运算, 并且 $a_1, \cdots, a_n \in B$, 那么 $f^{\mathbf{B}}(a_1, \ldots, a_n) \in B$, 则称 $B$ 是 $\mathbf{A}$ 的一个子论域, $\mathbf{B}$ 是 $\mathbf{A}$ 的一个子代数, 记作 $\mathbf{B} \le \mathbf{A}$.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定义(嵌入)</b>

设 $\mathbf{A}=(A,F)$ 和 $\mathbf{B}=(B,F')$ 是同型的两个代数, 设 $\alpha$ 是 $\mathbf{A}$ 到 $\mathbf{B}$ 的同态, 如果 $\alpha$ 是单射, 则称 $\alpha$ 是 $\mathbf{A}$ 到 $\mathbf{B}$ 的嵌入.

</div>

若 $\alpha$ 是 $\mathbf{A}$ 到 $\mathbf{B}$ 的嵌入, 则 $\alpha(A)$ 是 $\mathbf{B}$ 的子论域, 若记 $\alpha(\mathbf{A})=(\alpha(A),F')$, 则 $\alpha(\mathbf{A})$ 是 $\mathbf{B}$ 的子代数.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(生成)</b>

给定一个代数 $\mathbf{A}=(A,F)$, 对于 $X \subseteq A$, 定义

$$
\operatorname{Sg}(X) = \bigcap \{B \mid X \subseteq B \text{ 且 } B \text{ 是 } \mathbf{A} \text{ 的一个子论域} \}.
$$

称 $\operatorname{Sg}(X)$ 为 $X$ 生成的子论域.

若 $\operatorname{Sg}(X)=A$, 则称 $X$ 生成 $\mathbf{A}$, 若 $X$ 还是有限集, 则称 $\mathbf{A}$ 是有限生成的.

</div>

#### 积代数

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(直积)</b>

设 $I$ 是指标集, $\{\mathbf{A}_i=(A_i,F_i)\}_{i \in I}$ 是一族 $\mathcal{F}$ 型的代数, 它们的直积 $\mathbf{A} = \prod_{i \in I} \mathbf{A}_i$ 是一个代数, 其论域为 $\prod_{i \in I} A_i$, 并且对于 $n$ 元函数 $f \in \mathcal{F}$ 和 $a_1, \cdots, a_n \in \prod_{i \in I} A_i$, 有

$$
f^{\mathbf{A}}(a_1, \cdots, a_n)(i) = f^{\mathbf{A}_i}(a_1(i), \cdots, a_n(i)), i \in I.
$$

空积 $\prod_{i \in \emptyset} \mathbf{A}_i$ 是论域为 $\{\emptyset\}$ 的平凡代数.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定义(投影)</b>

设 $I$ 是指标集, $\{\mathbf{A}_i=(A_i,F_i)\}_{i \in I}$ 是一族同型的代数, 它们的直积为 $\mathbf{A} = \prod_{i \in I} \mathbf{A}_i$, 定义投影映射为

$$
\displaylines{
\pi_j \colon \prod_{i \in I} A_i \to A_j \\
a \mapsto a(j).
}
$$

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定理(直积的交换约束和结合约束)</b>

如果 $\mathbf{A}_1$, $\mathbf{A}_2$, 和 $\mathbf{A}_3$ 是三个同型的代数, 那么有 $\mathbf{A}_1 \times \mathbf{A}_2 \cong \mathbf{A}_2 \times \mathbf{A}_1$, $\mathbf{A}_1 \times (\mathbf{A}_2 \times \mathbf{A}_3) \cong (\mathbf{A}_1 \times \mathbf{A}_2) \times \mathbf{A}_3$.

</div>

显然交换约束和结合约束可以推广到任意积, 此处省略.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(不可直积分解)</b>

如果一个代数 $\mathbf{A}$ 不同构于两个非平凡代数的直积, 则称代数 $\mathbf{A}$ 是不可直积分解的.

</div>

#### 同余与商代数

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(等价关系集)</b>

集合 $A$ 上所有等价关系组成的集合记作 $\operatorname{Eq}(A)$.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定义(同余关系)</b>

设 $\mathbf{A}=(A,F)$ 是 $\mathcal{F}$ 型代数, $\equiv \in \operatorname{Eq}(A)$, 对于任意的 $a_1, \cdots, a_n , b_1 , \cdots , b_n \in A$ 和 $n$ 元函数 $f \in \mathcal{F}_n$, 当 $a_i\equiv b_i,1\le i\le n$ 时有

$$
f^{\mathbf{A}}(a_1,\cdots,a_n)\equiv f^{\mathbf{A}}(b_1,\cdots,b_n)
$$

成立, 则称 $\equiv$ 是 $\mathbf{A}$ 上的一个同余关系.

$\mathbf{A}$ 上的所有同余关系组成的集合记作 $\operatorname{Con}(\mathbf{A})$.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定理(同余的任意交仍是同余)</b>

设 $S$ 是代数 $\mathbf{A}$ 上的任意一族同余关系, 即 $S\subseteq\operatorname{Con}(\mathbf{A})$, 则 $\cap S$ 仍是同余.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定义(生成同余)</b>

设 $\mathbf{A}=(A,F)$ 是一个代数, $R\subseteq A\times A$, 则由 $R$ 生成的同余为包含 $R$ 的最小同余关系, 记作 $\operatorname{Cg}^{\mathbf{A}}(R)$, 即 $\operatorname{Cg}^{\mathbf{A}}(R)=\cap\{\equiv\in\operatorname{Con}(\mathbf{A})\mid R\subseteq\equiv\}$.
<br>

若 $R$ 是有限集, 则称同余 $\operatorname{Cg}^{\mathbf{A}}(R)$ 是有限生成的, 若 $R$ 形如 $\{(x_1,x_2)\}$, 则称 $\operatorname{Cg}^{\mathbf{A}}(R)=\operatorname{Cg}^{\mathbf{A}}(x_1,x_2)$ 是一个主同余.

</div>

显然主同余在环论中对应环的主理想, 例如整数环中 $\operatorname{Cg}^{\mathbf{A}}(3,5)$ 即为主理想 $(2)$.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理(生成同余的构造)</b>

设 $\mathbf{A}=(A,F)$ 是一个 $\mathcal{F}$ 型代数, $R\subseteq A\times A$, 先由 $R$ 定义集合 $R_1$,

$$
R_1=R\cup\{(a,a)\mid a\in A\}\cup\{(a,b)\mid (b,a)\in R,a,b\in A)\},
$$

再递归的定义集合 $R_n$,

$$
\displaylines{
R_n=\{(a,c)\mid (a,b)\in R_{n-1},(b,c)\in R_{n-1},a,b,c\in A\}\cup \\
\{(f^{\mathbf{A}}(a_1,\cdots,a_n),f^{\mathbf{A}}(b_1,\cdots,b_n))\mid f\in \mathcal{F}_n,(a_i,b_i)\in R_{n-1},a_i,b_i\in A,1\le i\le n\},
}
$$

则

$$
\operatorname{Cg}^{\mathbf{A}}(R)=\bigcup_{n=1}^\infty R_n.
$$

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定义(诺特代数)</b>

如果代数 $\mathbf{A}$ 的任意同余都可以由一个有限集生成, 则称 $\mathbf{A}$ 是一个诺特代数.

</div>

使用与环论中相同的方法可以证明, 代数 $\mathbf{A}$ 是诺特代数当且仅当 $\operatorname{Con}(\mathbf{A})$ 中不存在无限长的严格同余升链.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

设 $\mathbf{A}=(A,F)$ 和 $\mathbf{B}=(B,F')$ 是同型的两个代数, 设 $\alpha$ 是 $\mathbf{A}$ 到 $\mathbf{B}$ 的同态, 那么 $\alpha$ 的核 $\ker(\alpha)$, 是 $\mathbf{A}$ 上的一个同余关系.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定义(商代数)</b>

设 $\mathbf{A}=(A,F)$ 是 $\mathcal{F}$ 型代数, 若 $\equiv$ 是 $\mathbf{A}$ 上的一个同余关系, 则 $\mathbf{A}$ 商掉 $\equiv$ 得到的商代数记作 $\mathbf{A}/\equiv$, 它的论域为商集 $A/\equiv$, 其中的元素记作 $[a]_{\equiv}$, 其中 $a\in A$ 是等价类的代表元, $\mathbf{A}/\equiv$ 上的函数由

$$
f^{\mathbf{A}/\equiv}([a_1]_{\equiv},\cdots,[a_n]_{\equiv})=[f^{\mathbf{A}}(a_1,\cdots,a_n)]_{\equiv}
$$

定义, 其中 $f\in\mathcal{F}$ 为 $n$ 元函数符号, $a_1,\cdots,a_n\in A$.

</div>

在无歧义的情况下, $[a]_{\equiv}$ 简写为 $[a]$.

设 $\mathbf{G}$ 是一个群, $\equiv$ 是其上的一个同余关系, 则 $[1]$ 便是一个正规子群, 反之, 若 $\mathbf{N}$ 是 $\mathbf{G}$ 的一个正规自群, 则由

$$
a\equiv b\Longleftrightarrow a\cdot b^{-1}\in N
$$

定义的二元关系便是一个同余关系, 且显然有 $[1]=N$. 同理, 环中的 $[0]$ 便对应理想.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(自然同态)</b>

设 $\mathbf{A}=(A,F)$ 是一个代数, 若 $\equiv$ 是 $\mathbf{A}$ 上的一个同余关系, 则从 $\mathbf{A}$ 到商代数 $\mathbf{A}/\equiv$ 有一个自然满同态, 由下式定义,

$$
\displaylines{
\pi \colon A \to A/\equiv \\
a \mapsto [a].
}
$$

</div>

#### 同态基本定理

<div style="border: 3px solid #000; padding: 10px;">

<b>定理(第一同构定理)</b>

设 $\mathbf{A}=(A,F)$ 和 $\mathbf{B}=(B,F')$ 是同型的两个代数, 设 $\alpha$ 是 $\mathbf{A}$ 到 $\mathbf{B}$ 的同态, 则 $\mathbf{A}/\ker(\alpha)\cong \alpha(\mathbf{A})$.

</div>
<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

设 $A \to A/\ker(\alpha)$ 的自然同态为 $\pi$, 设映射 $\beta\colon A/\ker(\alpha)\to \alpha(A)$ 由 $\alpha=\beta\circ\pi$ 确定, 则 $\beta$ 即为所求的同构映射.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定义</b>

设 $\mathbf{A}=(A,F)$ 和 $\mathbf{B}=(B,F')$ 是同型的两个代数, $\mathbf{B}$ 是 $\mathbf{A}$ 的子代数, $\equiv$ 是 $\mathbf{A}$ 上的一个同余关系, 令

$$
\equiv\mid_B = \equiv \cap (B \times B),
$$

称为 $\equiv$ 在 $B$ 上的的限制, 并令

$$
B^\equiv = \{a \in A \mid [a] \cap B \ne \emptyset \},
$$

设 $\mathbf{B}^\equiv$ 为 $B^\equiv$ 生成的 $\mathbf{A}$ 的子代数.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定理(第二同构定理)</b>

设 $\mathbf{A}=(A,F)$ 和 $\mathbf{B}=(B,F')$ 是同型的两个代数, $\mathbf{B}$ 是 $\mathbf{A}$ 的子代数, $\equiv$ 是 $\mathbf{A}$ 上的一个同余关系, 则 $\equiv\mid_B$ 是 $\mathbf{B}$ 上的同余关系, $\equiv\mid_{B^\equiv}$ 是 $\mathbf{B^\equiv}$ 上的同余关系, 且
$ \mathbf{B}/\equiv\mid_B\cong\mathbf{B}^\equiv/\equiv\mid_{B^\equiv}$.

</div>
<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

同构由 $[b]_{\equiv\mid_B}\mapsto[b]_{\equiv\mid_{B^{\equiv}}}$ 给出.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定义</b>

设 $\mathbf{A}=(A,F)$ 是一个代数, 若 $\equiv_1,\equiv_2\in \operatorname{Con}(\mathbf{A})$, 且 $\equiv_1\subseteq\equiv_2$, 定义

$$
\equiv_2/\equiv_1=\{([a]_{\equiv_1},[b]_{\equiv_1})\in (A/\equiv_1)^2 \mid (a,b)\in\equiv_2\}.
$$

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定理(第三同构定理)</b>

设 $\mathbf{A}=(A,F)$ 是一个代数, 若 $\equiv_1,\equiv_2\in \operatorname{Con}(\mathbf{A})$, 且 $\equiv_1\subseteq\equiv_2$, 则 $\equiv_2/\equiv_1$ 是 $\mathbf{A}/\equiv_1$ 上的同余关系, 且 $(\mathbf{A}/\equiv_1)/(\equiv_2/\equiv_1)\cong \mathbf{A}/\equiv_2$.

</div>
<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

同构由 $[[a]_{\equiv_1}]_{\equiv_2/\equiv_1}\mapsto[a]_{\equiv_2}$ 给出.

</div>

设 $\mathbf{A}=(A,F)$ 是一个代数, 显然 $\operatorname{Con}(\mathbf{A})$ 在集合的包含关系下构成一个偏序集, 并且这个偏序集中有最小元和最大元, 最小元即为 $A\times A$ 的对角线集

$$
\Delta_A=\{(a,a)\mid a\in A\},
$$

最大元即为 $A\times A$ 本身, 我们对偶的将它记作 $\nabla_A=A\times A$.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(平凡同余和真同余)</b>

代数 $\mathbf{A}=(A,F)$ 中的同余 $\Delta_A=\{(a,a)\mid a\in A\}$ 和 $\nabla_A=A\times A$ 称为 $\mathbf{A}$ 的平凡同余, 除此之外的同余称为真同余.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定义(偏序集的闭区间)</b>

设 $(P,\le)$ 是偏序集, 设 $a, b \in X$, 则闭区间 $[a,b]$ 定义为

$$
[a, b] = \{ x \in P \mid a \leq x \leq b \}.
$$

</div>

显然偏序集的闭区间是子偏序集, 下面叙述泛代数的对应定理, 有时也称为第四同构定理.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理(对应定理)</b>

设 $\mathbf{A}=(A,F)$ 是一个代数, $\equiv\in\operatorname{Con}(\mathbf{A})$, 则 $[\equiv,\nabla_A]\cong \operatorname{Con}(\mathbf{A}/\equiv)$ 是序同构.

</div>
<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

序同构由 $\equiv'\mapsto\equiv'/\equiv$ 给出.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定义(单代数)</b>

设 $\mathbf{A}$ 是一个代数, 若 $\operatorname{Con}(\mathbf{A})=\{\Delta_A,\nabla_A\}$, 则称 $\mathbf{A}$ 是单代数, 若 $\mathbf{A}$ 的论域是有限集, 则称 $\mathbf{A}$ 为有限单代数.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定义(极大同余)</b>

设 $\mathbf{A}$ 是一个代数, $\equiv\in\operatorname{Con}(\mathbf{A})$ 且 $\equiv\neq\nabla_A$, 若 $[\equiv,\nabla_A]=\{\equiv,\nabla_A\}$, 则称 $\equiv$ 是 $\mathbf{A}$ 的极大同余.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

设 $\mathbf{A}$ 是一个代数, $\equiv\in\operatorname{Con}(\mathbf{A})$, $\mathbf{A}/\equiv$ 是一个单代数当且仅当 $\equiv$ 是极大同余.

</div>
<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

由对应定理显然.

</div>


### HSP定理

本章内容并未完全忠实于参考文献, 但此处定义和定理与参考文献里的是等价的.

#### 项代数

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(项)</b>

设 $X$ 是一个集合, 其中元素称为变元, 设 $\mathcal{F}$ 为一个型, 定义基于 $X$ 的 $\mathcal{F}$ 型项的集合 $T(X)$ 是满足以下条件的最小集合:
<br>

$\mathrm{(1)}$ $X \cup \mathcal{F}_0 \subseteq T(X)$;
<br>
 
$\mathrm{(2)}$ 若 $p_1,\cdots,p_n \in T(X)$ 且 $f \in \mathcal{F}_n$, 则 $f(p_1, \dots, p_n) \in T(X)$.
<br>

$T(X)$ 中元素称为项.

</div>

对于一个项 $p$, 易知 $p$ 中含有的变元只有有限个, 比如 $p$ 含有的变元在 $x_1,\cdots,x_n$ 之中, 那么可将 $p$ 记作 $p(x_1,\cdots,x_n)$.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(项代数)</b>

给定型 $\mathcal{F}$ 和集合 $X$, 项的集合为 $T(X) \neq \emptyset$, 则 $X$ 上的 $\mathcal{F}$ 型项代数记作 $\mathbf{T}(X)$, 其论域为集合 $T(X)$, 其上运算满足

$$
\displaylines{
f^{\mathbf{T}(X)} \colon T(X)^n \to T(X) \\
(p_1, \dots, p_n) \mapsto f(p_1, \dots, p_n),
}
$$

其中 $f \in \mathcal{F}_n$, $p_i \in T(X)$, $1 \leq i \leq n$. 亦称 $\mathbf{T}(X)$ 为 $X$ 生成的项代数.

</div>

项代数也称为绝对自由代数.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(项函数)</b>

对于集合 $X$ 上 $\mathcal{F}$ 型的项 $p(x_1, \cdots, x_n)$ 和一个 $\mathcal{F}$ 型的代数 $\mathbf{A}$, 我们递归的定义一个映射 $p^{\mathbf{A}}: A^n \rightarrow A$ 如下:

$\mathrm{(1)}$ 如果 $p$ 是一个变元 $x_i$, 那么

$$
p^{\mathbf{A}}(a_1, \cdots, a_n) = a_i,
$$

其中 $a_1, \dots, a_n \in A$;
 
$\mathrm{(2)}$ 如果 $p$ 的形式是 $f(p_1(x_1, \cdots, x_n), \cdots, p_k(x_1, \cdots, x_n))$, 其中 $f \in \mathcal{F}_k, p_i\in T(X),x_j\in X$, 那么

$$
p^{\mathbf{A}}(a_1, \cdots, a_n) = f^{\mathbf{A}}(p_1^{\mathbf{A}}(a_1, \cdots, a_n), \cdots, p_k^{\mathbf{A}}(a_1, \cdots, a_n)).
$$

称 $p^{\mathbf{A}}$ 是对应于项 $p$ 在 $\mathbf{A}$ 上的项函数.

</div>

#### 簇

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(等式)</b>

给定型 $\mathcal{F}$ 和集合 $X$, 项的集合为 $T(X) \neq \emptyset$, 则 $X$ 上的 $\mathcal{F}$ 型等式形如

$$
p\approx q,
$$

其中 $p,q\in T(X)$, 记 $X$ 上所有 $\mathcal{F}$ 型等式组成的集合为 $\operatorname{Id}_{\mathcal{F}}(X)$, 它与 $T(X)\times T(X)$ 之间有自然的双射, 于是等式可以理解为 $T(X)$ 上的二元关系.
<br>
 
$\operatorname{Id}_{\mathcal{F}}(X)$ 的子集称为等式集或理论, 通常用 $\Sigma$ 表示, 即 $\Sigma\subseteq\operatorname{Id}_{\mathcal{F}}(X). $

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定义(满足)</b>

给定型 $\mathcal{F}$ 和集合 $X$, 项的集合为 $T(X)$, 设 $\mathbf{A}=(A,F)$ 是一个 $\mathcal{F}$ 型代数, 若对于两个项 $p(x_1,\cdots,x_n),q(x_1,\cdots,x_n)\in T(X)$, 有

$$
p^{\mathbf{A}}(a_1,\cdots,a_n)=q^{\mathbf{A}}(a_1,\cdots,a_n),\forall a_1,\cdots, a_n\in A,
$$

则称代数 $\mathbf{A}$ 满足 $p\approx q$ 或 $\mathbf{A}$ 是 $p\approx q$ 的一个模型, 记作 $\mathbf{A}\models p\approx q$.
<br>
 
若 $\Sigma$ 是公式集, 且 $\mathbf{A}$ 满足 $\Sigma$ 中的每一条等式, 则称 $\mathbf{A}$ 满足 $\Sigma$ 或 $\mathbf{A}$ 是 $\Sigma$ 的一个模型, 记作 $\mathbf{A}\models \Sigma$.

</div>

约定使用无衬线字体表示范畴, 多数泛代数教材中使用了类的概念, 但为避免集合论的麻烦, 这里使用范畴语言叙述.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(簇)</b>

给定型 $\mathcal{F}$, 集合 $X$ 及其上等式集 $\Sigma$, 一个簇是一个范畴 $\mathsf{V}$, 其对象为 $\Sigma$ 的全体 $\mathcal{F}$ 型模型, 态射为代数间同态, 这个簇记作 $\mathsf{V}=\operatorname{Mod}(\Sigma)$.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>例</b>

群范畴 $\mathsf{Grp}$ 是一个簇, 环范畴 $\mathsf{Rng}$ 是一个簇, 幺环范畴 $\mathsf{Ring}$ 是一个簇, 交换幺环范畴 $\mathsf{CRing}$ 是一个簇, 交换幺环 $R$ 上的模范畴 $R-\mathsf{Mod}$ 是一个簇.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定义(演绎闭包)</b>

设 $\mathsf{A}$ 是由一些 $\mathcal{F}$ 型代数及其同态组成的范畴, 记 $\operatorname{Id}(\mathsf{A})$ 是 $\mathsf{A}$ 满足的 $X$ 上所有 $\mathcal{F}$ 型等式组成的等式集, 则对于等式集 $\Sigma$, 称 $\operatorname{Id}(\operatorname{Mod}(\Sigma))$ 为 $\Sigma$ 的演绎闭包. 若 $\Sigma=\operatorname{Id}(\operatorname{Mod}(\Sigma))$, 则称 $\Sigma$ 是演绎闭的.

</div>

显然 $\Sigma\subseteq \operatorname{Id}(\operatorname{Mod}(\Sigma))$, 且 $\operatorname{Id}(\operatorname{Mod}(\operatorname{Id}(\operatorname{Mod}(\Sigma))))=\operatorname{Id}(\operatorname{Mod}(\Sigma))$, 这就是演绎闭包名称的来源.

可以证明, $\operatorname{Id}(\mathsf{A})$ 一定是演绎闭的. 若 $\Sigma$ 是演绎闭的, 则存在一个簇 $\mathsf{V}$ 满足 $\Sigma=\operatorname{Id}(\mathsf{V)}$.

称 $\operatorname{Mod}(\operatorname{Id}(\mathsf{A}))$ 为 $\mathsf{A}$ 生成的簇, 若 $\mathsf{A}$ 是单元集 $\{\mathbf{A}\}$, 则记作 $\operatorname{Mod}(\operatorname{Id}(\mathbf{A}))$, 显然 $\operatorname{Mod}(\operatorname{Id}(\cdot))$ 也是一个闭包算子, 称为同语闭包. 若范畴 $\mathsf{V}$ 是簇, 则 $\operatorname{Mod}(\operatorname{Id}(\mathsf{V}))=\mathsf{V}$, 即同语闭, 反之, 若一个代数范畴同语闭则一定是簇, 显然此时 $\Sigma=\operatorname{Id}(\mathsf{V})$.

设 $\mathsf{C}$ 是一个范畴, 其中对象为 $\mathcal{F}$ 型代数的范畴 $\mathsf{A}$, 态射为各对象自身的对象集 $\operatorname{Ob}(\mathsf{A})$ 之间的包含映射给出的范畴间的函子. 再设 $\mathsf{E}=\mathscr{P}(\operatorname{Id}_{\mathcal{F}}(X))$ 为 $\operatorname{Id}_{\mathcal{F}}(X)$ 的幂集, 它关于集合间包含关系构成一个偏序集, 可以将其做成一个范畴, 对象为所有等式集, 态射为包含映射. 这样, $\operatorname{Id}(\cdot)$ 和 $\operatorname{Mod}(\cdot)$ 即为 $\mathsf{C}$ 和 $\mathsf{E}$ 之间的一对伴随函子. 设 $\mathsf{V}$ 是所有簇组成的范畴, 它是 $\mathsf{C}$ 的子范畴, 设 $\mathsf{D}$ 是所有演绎闭的等式集组成的范畴, 它是 $\mathsf{E}$ 的子范畴, 则 $\operatorname{Id}(\cdot)$ 和 $\operatorname{Mod}(\cdot)$ 为 $\mathsf{V}$ 和 $\mathsf{D}$ 之间的范畴同构.

<div style="border: 3px solid #000; padding: 10px;">

<b>例</b>

如果取簇为半群范畴 $\mathsf{Sg}$, 取 $X=\{a,b,c\}$, 若取 $\Sigma=\{(a\cdot b)\cdot c\approx a\cdot(b\cdot c)\}$, 则 $\operatorname{Mod}(\Sigma)=\mathsf{Sg}$, 但 $\operatorname{Id}(\operatorname{Mod}(\Sigma))=\operatorname{Id}(\mathsf{Sg})=\{(a\cdot a)\cdot a\approx a\cdot(a\cdot a),\cdots,(c\cdot c)\cdot c\approx c\cdot(c\cdot c)\}$, 这个集合中一共有 $3^3=9$ 个元素.

</div>

#### 自由代数

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(自由代数)</b>

给定型 $\mathcal{F}$ 和集合 $X$, 对应的项代数为 $\mathbf{T}(X)$, $\Sigma$ 是一个等式集, 在 $\mathbf{T}(X)$ 上定义同余关系 $\sim$, 若 $p,q\in T(X)$, 则 $p\sim q \Longleftrightarrow p\approx q\in \operatorname{Id}(\operatorname{Mod}(\Sigma))$, 则商代数 $\mathbf{T}(X)/\sim$ 称为 $X$ 上的 $\mathcal{F}$ 型 $\Sigma$ 自由代数, 记作 $\mathbf{F}_{\Sigma}(X)$, 其论域记作 $F_{\Sigma}(X)$.

</div>

自由代数常简写为 $\mathbf{F}(X)$, 论域简写为 $F(X)$.

<div style="border: 3px solid #000; padding: 10px;">

<b>例</b>

在所有岩浆组成的簇中, 自由代数与项代数是相同的, 因为岩浆满足的等式集为空集. 在自由岩浆中 $(a\cdot a)\cdot a$ 和 $a\cdot(a\cdot a)$ 是两个不同的元素.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定理(自由代数的泛性质)</b>

给定型 $\mathcal{F}$, 集合 $X$ 及其上等式集 $\Sigma$, 设 $X$ 上的 $\mathcal{F}$ 型 $\Sigma$ 自由代数为 $\mathbf{F}_{\Sigma}(X)$, $\iota\colon X\to F_{\Sigma}(X)$ 是自然的映射, 则对 $\Sigma$ 的任意一个 $\mathcal{F}$ 型模型 $\mathbf{A}=(A,F)$ 和映射 $\iota'\colon X \to A$, 都存在一个唯一的同态 $\varphi\colon F_{\Sigma}(X)\to A$, 使得下图交换:

$$
\require{AMScd}
\begin{CD}
X @>{\iota}>> F_{\Sigma}(X) \\
@>{\iota'}>> @V{\varphi}V{\text{...}}V \\
@. A
\end{CD}
$$

</div>

也有人直接使用泛性质定义自由代数, 即自由代数 $F_\Sigma(X)$ 是范畴 $\mathsf{M}(\Sigma)$ 中 $X$ 上的自由对象, 亦即自由函子 $U\colon\mathsf{Set}\to\mathsf{M}(\Sigma)$ 在 $X$ 处的像 $U(X)$, 自由函子与遗忘函子互相伴随, 此处不多赘述.

#### HSP定理

一些同型代数连同代数间同态组成的范畴 $\mathsf{C}$ 在取同态像, 取子代数, 取积代数下封闭的意思是, 对任意一个代数 $\mathbf{A}\in\operatorname{Ob}(\mathsf{C})$ 和从 $A$ 射出的同态 $\alpha$, 其同态像 $\alpha(\mathbf{A})\in\operatorname{Ob}(\mathsf{C})$, $\mathbf{A}$ 的任意子代数也在 $\operatorname{Ob}(\mathsf{C})$ 中, 对任意一族代数 $\{\mathbf{A}_i\}_{i\in I}\subseteq\operatorname{Ob}(\mathsf{C})$, 其中 $I$ 是指标集, 则积代数 $\prod_{i \in I} \mathbf{A}_i\in\operatorname{Ob}(\mathsf{C})$.

定义如下闭包算子 $H(\mathsf{C}), S(\mathsf{C}), P(\mathsf{C})$ 分别为:

$H(\mathsf{C})$ 为包含 $\mathsf{C}$ 的最小范畴, 使得 $\mathsf{C}$ 中代数的任意同态像都在 $H(\mathsf{C})$ 中;

$S(\mathsf{C})$ 为包含 $\mathsf{C}$ 的最小范畴, 使得 $\mathsf{C}$ 中代数的任意子代数都在 $S(\mathsf{C})$ 中;

$P(\mathsf{C})$ 为包含 $\mathsf{C}$ 的最小范畴, 使得 $\mathsf{C}$ 中代数的任意积代数都在 $P(\mathsf{C})$ 中.

若算子 $O_1$ 和 $O_2$ 是以上任意算子或其复合, 则 $O_1\le O_2$ 意味着 $O_1(\mathsf{C})\subseteq O_2(\mathsf{C})$, 并且算子的复合通常省略括号或复合符号.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

$SH\le HS$, $PS\le SP$, $PH\le HP$.

</div>

关于这三种闭包算子之间的强度关系, 有如下图表:

<div style="border: 3px solid #000; padding: 10px;">
$$
\begin{array}{ccccc}
 & & HSP & & \\
 & & \uparrow & & \\
 & & SHPS & & \\
HPS & \nearrow & \uparrow & & \\
\uparrow & \nearrow & SPHS & \nearrow & SHP \\
PHS \uparrow & & \uparrow & & \uparrow \\
\uparrow & & SPH & \nearrow & \\
HS \uparrow & & HP & \searrow \searrow & \\
\uparrow \nearrow & & \uparrow \nearrow & & PSH \\
SH \searrow & PH \uparrow & PS \nearrow & SP \uparrow \\
\uparrow \nearrow & \uparrow \nearrow & \uparrow \nearrow & \\
H & S & P & \\
\uparrow \nearrow \nearrow & \uparrow \nearrow \nearrow & \uparrow \nearrow & \\
 & \mathsf{C} & & & 
\end{array}
$$
</div>

如图, $HSP$ 位于该图的最顶端, 实际上, 有以下定理.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

对于一个由一些同型代数连同代数间同态组成的范畴 $\mathsf{C}$, 包含它的最小的在取同态像, 取子代数, 取积代数下封闭的范畴正是 $H(S(P(\mathsf{C})))$.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

$\operatorname{Id}(\mathsf{C})=\operatorname{Id}(H(\mathsf{C}))=\operatorname{Id}(S(\mathsf{C}))=\operatorname{Id}(P(\mathsf{C}))=\operatorname{Id}(HSP(\mathsf{C}))$.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

给定型 $\mathcal{F}$ 和集合 $X$, $\Sigma$ 是一个等式集, $X$ 上的 $\mathcal{F}$ 型 $\Sigma$ 自由代数为 $\mathbf{F}_{\Sigma}(X)$, 则有

$$
\operatorname{Id}(\operatorname{Mod}(\Sigma))=\operatorname{Id}(\mathbf{F}_{\Sigma}(X)).
$$

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

若一个由一些同型代数连同代数间同态组成的范畴 $\mathsf{C}$ 在取同态像, 取子代数, 取积代数下封闭, 即 $\mathsf{C}=HSP(\mathsf{C})$, 则有 $\mathsf{C}=\operatorname{Mod}(\operatorname{Id}(\mathsf{C))}$.

</div><br>
<div style="border: 3px solid #000; padding: 10px;">

<b>定理(HSP定理)</b>

一些同型的代数连同代数间同态组成的范畴 $\mathsf{C}$ 是簇当且仅当它在取同态像, 取子代数, 取积代数下封闭.

</div>

HSP定理中的 H 指同态像 Homomorphic image, S 指子代数 Subalgebra, P 指积代数 Product.

<div style="border: 3px solid #000; padding: 10px;">

<b>HSP定理的证明</b>

若 $\mathsf{V}$ 是簇, 设 $\mathsf{V}=\operatorname{Mod}(\Sigma)$, 因为 $\operatorname{Id}(\mathsf{V})=\operatorname{Id}(\operatorname{Mod}(\Sigma))=\operatorname{Id}(HSP(\mathsf{V}))$, 则 $HSP(\mathsf{V})\subseteq \operatorname{Mod}(\Sigma)=\mathsf{V}$, 而由因 $\mathsf{V}\subseteq HSP(\mathsf{V})$ 知 $\mathsf{V}=HSP(\mathsf{V})$, 即它在取同态像, 取子代数, 取积代数下封闭.
<br>
若一个由一些同型代数连同代数间同态组成的范畴 $\mathsf{C}$ 在取同态像, 取子代数, 取积代数下封闭, 即 $\mathsf{C}=HSP(\mathsf{C})$, 则有 $\mathsf{C}=\operatorname{Mod}(\operatorname{Id}(\mathsf{C))}$, 所以 $\mathsf{C}$ 是簇.

</div>


# 泛代数几何


### 泛代数观点下的古典代数几何


### 基础构造

#### 带常数的簇

#### 代数集与根同余

#### 扎里斯基拓扑

#### 诺特性

#### 坐标代数

#### 希尔伯特零点定理


### 新问题


# 参考文献
