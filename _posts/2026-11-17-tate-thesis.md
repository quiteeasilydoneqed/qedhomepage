---
layout: post
title: "Tate's thesis: 数域上的Fourier分析与Hecke的zeta函数"
subtitle: "Tate 的博士论文中文翻译"
header-img: "img/post-bg-infinity.jpg"
header-mask: 0.3
math: true
no-em-replace: true
tags:
  - 数论
  - 代数数论
  - 调和分析
---

**摘要.** 我们把与数域相联系, 取值于赋值向量群和伊代尔群中的抽象分析奠立在坚实的基础上. 这使我们可以把 $\zeta$ 函数按经典方式下的定义, 也就是某一类理想特征在整理想上的求和, 换成一个与之对应的, 对伊代尔群的定义, 即在一个相当一般的权函数上乘以一个在域元素上平凡地取值的伊代尔特征, 再沿伊代尔群积分. Hecke 那套为经典数论中 $n$ 维空间格上的 theta 函数所构造的, 繁复的 theta 公式, 它的地位可以由一个简单的 Poisson 公式来代替, 后者是说: 取值于赋值向量的一般函数, 沿域元素这个离散子群求和. 有了这个 Poisson 公式, 一方面它本身极为重要, 因为它正是 Riemann--Roch 定理在数论上的类比, 另一方面, 一切推广的 $\zeta$ 函数都可以一举得到解析延拓, 并且可以为它们建立一条形式简洁的函数方程. 把这些结果翻译回经典的语言, 就得到 Hecke 的函数方程, 同时还得到其中那个繁复因子的一种解释: 它是若干局部因子的乘积, 这些局部因子来自 Archimedean 素点与导子的素点. 局部 $\zeta$ 函数这个概念正是为了给出这些因子的局部定义而引进的, 并且已经算出了它们的一张表.

> **重印说明**: 这是 Tate 博士论文 (Princeton, 1950 年 5 月) 未经改动的重印. 会议的多位参加者都敦促编者把这篇文章收入论文集, 因为它虽然被广泛引用, 却从未发表过. 编者非常感谢 Tate 允许我们这样做, 并为他在近年文献上的评注 (第 346 页) 表示感谢.
>
> **译本说明**: 本文译自 Cassels--Fröhlich 所编的 Algebraic Number Theory 第 15 章, 使用 DeepSeek V4.1 flash 模型翻译, 并由人类校对, 但仍可能有部分错误. 本译本对原文一些难以用 LaTeX 打出的符号作了修改. 原文中使用的一些符号和术语已经过时, 但我相信识别出这些术语对应的现代概念并不困难. 以现代的眼光看, 虽然这篇博士论文具有开创性的意义, 但原文并不是最好的学习材料, 只适合对相关数学史感兴趣的人阅读.

## 1 引言

### 1.1. 相关历史

Hecke 是第一个证明任意代数数域的 Dedekind $\zeta$ 函数可以整平面解析延拓, 并且满足一条简单函数方程的人. 他随即意识到, 他的方法不仅可以用于 Dedekind $\zeta$ 函数与 L 级数, 而且可以用于由一种新型理想特征作出的 $\zeta$ 函数, 这种理想特征对主理想而言, 不仅依赖于该数模“导子”所在的剩余类, 而且依赖于该数在复域中的共轭所处的位置. 克服了相当不寻常的技术上的复杂性之后, 他证明了 (1918 年与 1920 年) 这些“Hecke 型”的 $\zeta$ 函数满足与 Dedekind $\zeta$ 函数同一类型的函数方程, 只是其中的因子要繁复得多.

在一项工作中 (Chevalley, 1940), 其主要目的在于把分析从类域论里移出去, Chevalley 引进了伊代尔群这个极好的概念, 以之作为理想群的精细化. 在伊代尔里, Chevalley 找到的不仅是通往类域论的最佳途径, 而且也是通往一般代数数论的最佳途径. 这一点由 Artin 与 Whaples (1945) 的工作显示出来. 他们把赋值向量定义为与伊代尔相对应的加法概念, 并由这些概念出发, 从简单的公理推导出代数数论的全部基本命题.

Matchett 是 Artin 的学生, 她作了第一次尝试 (1946) 去推进这一纲领, 用伊代尔与向量来做解析数论. 她成功地把经典 $\zeta$ 函数用伊代尔群上的积分重新定义, 并且把 Hecke 的特征解释为恰是那些可以由伊代尔特征导出的理想群特征. 但是在证明函数方程时她遵循的是 Hecke 的途径.

### 1.2. 本文

Artin 向我指出了这种可能性: 把 $\zeta$ 函数的概念加以推广, 并且比 Matchett 更充分地利用赋值向量空间与伊代尔空间本身上的分析, 从而简化它的解析延拓与函数方程的证明. 本文就是我按照他的提示所做工作的结果. 我把 $\zeta$ 函数按经典方式下的定义, 也就是某一类理想特征在整理想上的求和, 换成一个与之对应的, 对伊代尔的定义, 即: 在一个相当一般的权函数上乘以一个在域元素上平凡地取值的伊代尔特征, 再沿伊代尔群积分. Hecke 那套为经典数论中 $n$ 维空间格上的 theta 函数所构造的, 繁复的 theta 公式, 它的地位可以由一个简单的 Poisson 公式来代替, 后者是说: 取值于赋值向量的一般函数, 沿域元素这个离散子群求和. 有了这个 Poisson 公式, 一方面它本身极为重要, 因为它正是 Riemann--Roch 定理在数论上的类比, 另一方面, 一切推广的 $\zeta$ 函数都可以一举得到解析延拓, 并且可以为它们建立一条形式简洁的函数方程. 把这些结果翻译回经典的语言, 就得到 Hecke 的函数方程, 同时还得到其中那个繁复因子的一种解释: 它是若干局部因子的乘积, 这些局部因子来自 Archimedean 素点与导子的素点. 局部 $\zeta$ 函数这个概念正是为了给出这些因子的局部定义而引进的, 并且已经算出了它们的一张表.

我谨向 Artin 表示深切的谢意, 既感谢他向我提示了这个题目, 也感谢他在我工作过程中不断给予的鼓励.

### 1.3. “预备知识”

在数论方面, 我们只假定读者知道经典的代数数论, 以及它与局部理论的联系. 不需要预先知道伊代尔与赋值向量的观点, 因为为了在伊代尔群与向量群上引入抽象分析, 我们重新定义它们, 并详细讨论它们的结构.

在分析方面, 我们只假定读者知道单变量解析函数论中最基本的事实与定义. 经典解析数论的知识一概不需要. 相反, 读者必须知道局部紧交换群 $G$ 上抽象 Fourier 分析的基本事实: (1) 这种群上 Haar 测度的存在性与唯一性, 以及它与 $G$ 上连续函数空间 $L(G)$ 上的一个正不变泛函的等价性, 这里所说的连续函数在某个紧集之外为零. (2) $G$ 与其特征群 $\widehat G$ 之间的对偶, 以及 $G$ 的子群与 $\widehat G$ 的商群之间的对偶. (3) 函数 $f\in L\_1(G)$ 的 Fourier 变换 $\widehat f$ 的定义, 以及如下事实: 如果在 $\widehat G$ 中选取与 $G$ 中测度对偶的测度, 则对一切能够指望它成立的函数, 即对一切 $f\in L\_1(G)$ 而使 $f$ 连续并且 $\widehat f\in L\_1(\widehat G)$ 的函数, Fourier 反演公式在最朴素的意义下成立. (这一函数类我们记作 $\mathfrak B\_1(G)$.) 关于这一理论的精致叙述, 例如可以在 Cartan 与 Godement (1947) 中找到.

## 2 局部理论

### 2.1. 引言

本节中, $k$ 表示一个代数数域对某个素除子 $\mathfrak p$ 作完备化所得的域. 因此若 $\mathfrak p$ 是 Archimedean 素除子, $k$ 就是实域或复域; 若 $\mathfrak p$ 是离散的, $k$ 就是一个“$\mathfrak p$ 进”域. 在后一种情形, $k$ 包含一个整数环 $\mathfrak o$, 它只有一个素理想 $\mathfrak p$, 剩余类域 $\mathfrak o/\mathfrak p$ 有 $N\mathfrak p$ 个元素. 两种情形下, $k$ 在与素除子 $\mathfrak p$ 相联系的拓扑之下都是一个完备拓扑域.

从属于 $\mathfrak p$ 的 $k$ 的无穷多个等价赋值中, 我们选取如下的规范赋值: 

$$
\begin{array}{ll}
\vert \alpha\vert  = \text{通常的绝对值}, & \text{若 } k \text{ 是实域};\\[2pt]
\vert \alpha\vert  = \text{通常绝对值的平方}, & \text{若 } k \text{ 是复域};\\[2pt]
\vert \alpha\vert  = (N\mathfrak p)^{-v},\ \text{其中 } v \text{ 是 } \alpha \text{ 的阶数}, & \text{若 } k \text{ 是 } \mathfrak p \text{ 进域}.
\end{array}
$$

 我们知道 $k$ 是局部紧的. 可以证明的更精确的陈述是: 子集 $B\subset k$ 相对紧 (即其闭包紧) 当且仅当它在绝对值下有界. 事实上, 若 $k$ 是实域或复域, 这对直线或平面中的子集是众所周知的事实; 若 $k$ 是 $\mathfrak p$ 进域, 可以用一个涉及剩余类域有限性的“抽屉论证”以类似的方式证明之.

### 2.2. 加法特征与测度

用 $k^+$ 表示 $k$ 的加法群, 视其为一个局部紧交换群, 并用 $\xi$ 表示它的一般元素. 我们想确定 $k^+$ 的特征群, 而令人高兴的是, 这件事基本上由下面的事实完成:

<div class="tate-result qed-box" markdown="1">

**引理 2.2.1.** 若 $\xi\to \chi(\xi)$ 是 $k^+$ 的一个非平凡特征, 则对每个 $\eta\in k^+$, $\xi\to \chi(\eta\xi)$ 也是一个特征. 对应关系 $\eta\leftrightarrow \chi(\eta\xi)$ 给出 $k^+$ 与其特征群之间的一个同构, 既在拓扑上也在代数上成立.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** (1) 对任意固定的 $\eta$, $\chi(\eta\xi)$ 是一个特征, 因为映射 $\xi\to\eta\xi$ 是 $k^+$ 到自身的连续同态.

\(2\) $\chi((\eta\_1+\eta\_2)\xi) = \chi(\eta\_1\xi+\eta\_2\xi) = \chi(\eta\_1\xi)\chi(\eta\_2\xi)$ 表明映射 $\eta\to \chi(\eta\xi)$ 是 $k^+$ 到其特征群中的一个代数同态.

\(3\) 若对一切 $\xi$ 有 $\chi(\eta\xi)=1$, 则 $\eta k^+ \ne k^+$, 从而 $\eta = 0$. 故它是一个单射的代数同构.

\(4\) 若对一切 $\eta$ 有 $\chi(\eta\xi)=1$, 则 $k^+\xi \ne k^+$, 从而 $\xi = 0$. 因此形如 $\chi(\eta\xi)$ 的特征在特征群中处处稠密.

\(5\) 对某个大的 $M$, 用 $B$ 表示使 $\vert \xi\vert \le M$ 的一切 $\xi\in k^+$ 所成的 (紧) 集. 于是: $\eta$ 在 $k^+$ 中接近 $0$ $\Rightarrow$ $\eta B$ 在 $k^+$ 中接近 $0$ $\Rightarrow$ $\chi(\eta B)$ 在复平面中接近 $1$ $\Rightarrow$ $\chi(\eta\xi)$ 在特征群中接近恒等特征. 另一方面, 若 $\xi\_0$ 是使 $\chi(\xi\_0)\ne 1$ 的固定元素, 则: $\chi(\eta\xi)$ 接近恒等特征 $\Rightarrow$ $\chi(\eta B)$ 接近 $1$, 比方说比 $\chi(\xi\_0)$ 更接近 $1$ $\Rightarrow$ $\xi\_0\notin\eta B$ $\Rightarrow$ $\eta$ 在 $k^+$ 中接近 $0$. 因此对应关系 $\eta\leftrightarrow \chi(\eta\xi)$ 是双向连续的.

\(6\) 于是形如 $\chi(\eta\xi)$ 的特征构成特征群的一个局部紧子群. 局部紧性蕴含完备性, 从而蕴含闭性; 这一点与 (4) 合起来表明该映射是满射.

</div>

为了把前面引理所许诺的, $k^+$ 与其特征群之间的等同确定下来, 我们必须构造一个特殊的非平凡特征. 设 $p$ 是 $\mathfrak p$ 所整除的有理素除子, $R$ 是有理域在 $p$ 处的完备化. 如下定义 $R$ 到模 $1$ 实数中的一个映射 $x\to\lambda(x)$:

情形 1. $p$ 是 Archimedean 的, 于是 $R$ 是实数域. 

$$
\lambda(x) = -x\ (\mathrm{mod}\ 1)
$$



(注意负号!)

情形 2. $p$ 是离散的, $R$ 是 $p$ 进数域. $\lambda(x)$ 将由以下性质确定:

1.  $\lambda(x)$ 是一个有理数, 其分母只含 $p$ 的幂.

2.  $\lambda(x)-x$ 是一个 $p$ 进整数.

(要找这样的 $\lambda(x)$, 令 $p^v x$ 为整数, 并选取普通整数 $n$ 使 $n\equiv p^v x\ (\mathrm{mod}\ p^v)$. 然后令 $\lambda(x)=n/p^v$; 显然 $\lambda(x)$ 在模 $1$ 之下是唯一确定的.)

<div class="tate-result qed-box" markdown="1">

**引理 2.2.2.** $x\to\lambda(x)$ 是 $R$ 到模 $1$ 实数群中的一个非平凡连续加法映射.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 情形 1 是平凡的. 在情形 2 中我们验证数 $\lambda(x)+\lambda(y)$ 对 $x+y$ 满足性质 (a) 与 (b), 故该映射是加性的. 它在 $0$ 处连续, 然而并非平凡, 因为显然有: $\lambda(x)=0 \Leftrightarrow x$ 是 $p$ 进整数.

</div>

现在对 $\xi\in k^+$ 定义 $\Lambda(\xi)=\lambda(S\_{k/R}\,\xi)$. 注意 $S\_{k/R}$ 是 $k$ 到 $R$ 上的加法连续映射, 于是 $\xi\to e^{2\pi i\Lambda(\xi)}$ 是 $k^+$ 的一个非平凡特征. 我们已证得:

<div class="tate-result qed-box" markdown="1">

**定理 2.2.1.** 若把特征 $\xi\to e^{2\pi i\Lambda(\eta\xi)}$ 与元素 $\eta\in k^+$ 等同起来, 则 $k^+$ 自然地就是它自己的特征群.

</div>

<div class="tate-result qed-box" markdown="1">

**引理 2.2.3.** 若 $\mathfrak p$ 是离散的, 则与 $\eta$ 相联系的特征 $e^{2\pi i\Lambda(\eta\xi)}$ 在 $\mathfrak o$ 上平凡当且仅当 $\eta\in\mathfrak d^{-1}$, 其中 $\mathfrak d$ 表示 $k$ 的绝对差积.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 

$$
\Lambda(\eta\mathfrak o)=0
\Leftrightarrow \lambda(S\_{k/R}(\eta\mathfrak o))=0
\Leftrightarrow S\_{k/R}(\eta\mathfrak o)\subset \mathfrak o\_R
\Leftrightarrow \eta\in\mathfrak d^{-1}.
$$



</div>

现在设 $\mu$ 是 $k^+$ 的一个 Haar 测度.

<div class="tate-result qed-box" markdown="1">

**引理 2.2.4.** 若对 $\alpha\ne 0\in k$ 及 $k^+$ 中的可测集 $M$ 定义 $\mu\_1(M)=\mu(\alpha M)$, 则 $\mu\_1$ 是一个 Haar 测度, 从而存在一个数 $\varphi(\alpha)>0$ 使 $\mu\_1=\varphi(\alpha)\mu$.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** $\xi\to\alpha\xi$ 是 $k^+$ 的自同构, 既在拓扑上也在代数上成立. Haar 测度由 $k^+$ 的拓扑与代数结构在相差一个正常数的意义下唯一确定.

</div>

<div class="tate-result qed-box" markdown="1">

**引理 2.2.5.** 前一个引理中的常数 $\varphi(\alpha)$ 就是 $\vert \alpha\vert $, 亦即 $\mu(\alpha M)=\vert \alpha\vert \mu(M)$.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 若 $k$ 是实域, 这是明显的. 若 $k$ 是复域, 同样明显, 因为这时我们选取的 $\vert \alpha\vert $ 是通常绝对值的平方. 若 $k$ 是 $\mathfrak p$ 进的, 注意 $\mathfrak o$ 既紧又开, $0<\mu(\mathfrak o)<\infty$, 因此只需比较 $\mathfrak o$ 与 $\alpha\mathfrak o$ 的大小. 对整的 $\alpha$, $\mathfrak o$ 中 $\alpha\mathfrak o$ 的陪集共有 $N(\alpha\mathfrak o)$ 个, 故 $\mu(\alpha\mathfrak o)=(N(\alpha\mathfrak o))^{-1}\mu(\mathfrak o)=\vert \alpha\vert \mu(\mathfrak o)$. 对非整的 $\alpha$, 用 $\alpha^{-1}$ 代替 $\alpha$ 即可.

</div>

现在我们有了另一个理由称此规范赋值为自然的. $\vert \alpha\vert $ 可以解释为加法群 $k^+$ 在变换 $\xi\to\alpha\xi$ 之下被“拉伸”的倍数.

对积分而言, 前一个引理的意义显然是: 

$$
d\mu(\alpha\xi) = \vert \alpha\vert \, d\mu(\xi);
$$

 更完整地写: 

$$
\int f(\xi)\, d\mu(\xi) = \vert \alpha\vert  \int f(\alpha\xi)\, d\mu(\xi).
$$



一般的 Haar 测度就谈到这里. 现在让我们为加法群 $k^+$ 选取一个固定的 Haar 测度. 定理 2.2.1 使我们能以一种不变的方式这样做, 即选取那样一个测度, 在把 $k^+$ 解释为其自身的特征群 (这一解释由该定理给出) 之下, 它就是它自己的 Fourier 变换. 我们写出做出这件事的测度选取, 为简单起见用 $d\xi$ 代替 $d\mu(\xi)$: 

$$
\begin{array}{ll}
d\xi = \text{实直线上的通常 Lebesgue 测度}, & \text{若 } k \text{ 是实域};\\[2pt]
d\xi = \text{平面中通常 Lebesgue 测度的两倍}, & \text{若 } k \text{ 是复域};\\[2pt]
d\xi = \text{使 } \mathfrak o \text{ 具有测度 } (N\mathfrak d)^{-\frac12} \text{ 的那个测度}, & \text{若 } k \text{ 是 } \mathfrak p \text{ 进域}.
\end{array}
$$



<div class="tate-result qed-box" markdown="1">

**定理 2.2.2.** 若对函数 $f\in L\_1(k^+)$ 如下定义 Fourier 变换 $\widehat f$: 

$$
\widehat f(\eta) = \int f(\xi)\, e^{-2\pi i\Lambda(\eta\xi)}\, d\xi,
$$

 则在我们所选取的测度之下, 反演公式 

$$
f(\xi) = \int \widehat f(\eta)\, e^{2\pi i\Lambda(\xi\eta)}\, d\eta
= \widehat{\widehat f}(-\xi)
$$

 对 $f\in\mathfrak B\_1(k^+)$ 成立.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 我们只需对一个非平凡函数建立反演公式, 因为由抽象 Fourier 分析我们知道它成立, 至多相差一个常数因子. 对实域 $k$, 可以取 $f(\xi)=e^{-\pi\vert \xi\vert ^2}$; 对复域 $k$, 取 $f(\xi)=e^{-2\pi\vert \xi\vert }$; 对 $\mathfrak p$ 进域 $k$, 例如取 $f(\xi)$ 为 $\mathfrak o$ 的特征函数. 计算细节请读者参看下文第 2.6 节.

</div>

### 2.3. 乘法特征与测度

我们对 $k$ 的乘法群 $k^\ast $ 的结构的第一点认识, 来自连续同态 $\alpha\to\vert \alpha\vert $, 它是 $k^\ast $ 到正实数乘法群中的映射. 这个同态的核, 即一切满足 $\vert \alpha\vert =1$ 的 $\alpha$ 所成的子群, 显然将起重要作用. 我们用 $u$ 记它. 一切情形下 $u$ 都紧; 若 $k$ 是 $\mathfrak p$ 进的, $u$ 也是开的.

关于 $k^\ast $ 的特征, 情况与 $k^+$ 不同. 首先, 我们关心的是 $k^\ast $ 到复数中的一切连续乘法映射 $\alpha\to c(\alpha)$, 而不只是有界的那些, 这样的映射我们将称为拟特征, 而把 “特征” 这个词留给通常那种绝对值为 $1$ 的特征. 其次, 我们将找不到拟特征群的模型, 甚至也找不到特征群的模型, 尽管这样的模型会具有极大的重要性.

若一个拟特征在 $u$ 上平凡, 我们称它为非分歧的, 先来确定非分歧的拟特征.

<div class="tate-result qed-box" markdown="1">

**引理 2.3.1.** 非分歧的拟特征就是形如 $c(\alpha)=\vert \alpha\vert ^s\equiv e^{s\log\vert \alpha\vert }$ 的映射, 其中 $s$ 是任意复数. 若 $\mathfrak p$ 是 Archimedean 的, $s$ 由 $c$ 唯一确定; 而对离散的 $\mathfrak p$, $s$ 只在模 $2\pi i/\log N\mathfrak p$ 的意义下由 $c$ 确定.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 对任意 $s$, $\vert \alpha\vert ^s$ 显然是非分歧的拟特征. 另一方面, 任何非分歧的拟特征只依赖于 $\vert \alpha\vert $, 而作为 $\vert \alpha\vert $ 的函数, 它是 $k$ 的值群的一个拟特征. 这个值群或者是一切正实数所成的乘法群, 或者是一切 $N\mathfrak p$ 的幂所成的乘法群, 依 $\mathfrak p$ 是 Archimedean 的还是离散的而定; 众所周知, 这些群的拟特征就是上面所述的那些.

</div>

若 $\mathfrak p$ 是 Archimedean 的, 我们可以把一般元素 $\alpha\in k^\ast $ 唯一地写成 $\alpha=\tilde\alpha\rho$, 其中 $\tilde\alpha\in u$, $\rho>0$. 对离散的 $\mathfrak p$, 我们必须选取一个阶数为 $1$ 的固定元素 $\pi$, 才能同样唯一地写 $\alpha=\tilde\alpha\rho$, 其中 $\tilde\alpha\in u$, 而这一次 $\rho$ 是 $\pi$ 的一个幂. 两种情形下, 映射 $\alpha\to\tilde\alpha$ 都是 $k^\ast $ 到 $u$ 上的连续同态, 且在 $u$ 上是恒等映射.

<div class="tate-result qed-box" markdown="1">

**定理 2.3.1.** $k^\ast $ 的拟特征就是形如 $\alpha\to c(\alpha)=\tilde c(\tilde\alpha)\vert \alpha\vert ^s$ 的映射, 其中 $\tilde c$ 是 $u$ 的任意特征. $\tilde c$ 由 $c$ 唯一确定. $s$ 按前一个引理的方式确定.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 形如所给类型的映射显然是拟特征. 反之, 若 $c$ 是给定的拟特征, 我们定义 $\tilde c$ 为 $c$ 在 $u$ 上的限制, 则 $\tilde c$ 是 $u$ 的拟特征, 因此由于 $u$ 紧, 它是 $u$ 的特征. 而 $\alpha\to c(\alpha)/\tilde c(\tilde\alpha)$ 是非分歧的拟特征, 故按前一个引理它具有 $\vert \alpha\vert ^s$ 的形式.

</div>

于是 $k^\ast $ 的拟特征问题归结为 $u$ 的特征问题. 若 $k$ 是实域, $u=\{1,-1\}$, 特征是 $\tilde c(\tilde\alpha)=\tilde\alpha^n$, $n=0,1$. 若 $k$ 是复域, $u$ 是单位圆, 特征是 $\tilde c(\tilde\alpha)=\tilde\alpha^n$, $n$ 为任意整数. 若 $k$ 是 $\mathfrak p$ 进的, $u$ 的子群 $1+\mathfrak p^v$, $v>0$, 构成 $u$ 中 $1$ 的基本邻域组. 因此对充分大的 $v$ 必有 $\tilde c(1+\mathfrak p^v)=1$. 取 $v$ 最小 (若 $\tilde c=1$ 则 $v=0$), 称理想 $\mathfrak f=\mathfrak p^v$ 为 $\tilde c$ 的导子. 于是 $\tilde c$ 是有限商群 $u/(1+\mathfrak f)$ 的特征, 可由一张有限的数据表来描述.

由定理 2.3.1 中给出的, 一般拟特征的表达式 $c(\alpha)=\tilde c(\tilde\alpha)\vert \alpha\vert ^s$, 我们看到 $\vert c(\alpha)\vert =\vert \alpha\vert ^\sigma$, 其中 $\sigma=\operatorname{Re}(s)$ 由 $c(\alpha)$ 唯一确定. 称 $\sigma$ 为 $c$ 的指数是方便的. 一个拟特征是特征, 当且仅当它的指数为 $0$.

我们将通过把 $k^\ast $ 上的 Haar 测度 $\mathrm{d}\alpha$ 与 $k^+$ 上的测度 $d\xi$ 相联系的方法来选取它. 若 $g(\alpha)\in L(k^\ast )$, 则 $g(\xi)\vert \xi\vert ^{-1}\in L(k^+-0)$. 于是可以在 $L(k^\ast )$ 上定义一个泛函 

$$
\Phi(g) = \int\_{k^+-0} g(\xi)\,\vert \xi\vert ^{-1}\, d\xi .
$$

 若 $h(\alpha)=g(\beta\alpha)$ ($\beta\in k^\ast $ 固定) 是 $g(\alpha)$ 的一个乘法平移, 则 

$$
\Phi(h) = \int\_{k^+-0} g(\beta\xi)\,\vert \xi\vert ^{-1}\, d\xi = \Phi(g),
$$

 这一点由代换 $\xi\to\beta^{-1}\xi$ 以及引理 2.2.5 中讨论的 $d\xi\to\vert \beta\vert ^{-1}\,d\xi$ 看出. 因此, 显然非平凡并且为正的泛函 $\Phi$ 在平移下不变. 于是它必定来自 $k^\ast $ 上的某个 Haar 测度. 把这个测度记作 $\mathrm{d}\_1\alpha$, 我们可以写 

$$
\int g(\alpha)\, \mathrm{d}\_1\alpha = \int\_{k^+-0} g(\xi)\,\vert \xi\vert ^{-1}\, d\xi .
$$

 显然, 对应关系 $g(\alpha)\leftrightarrow g(\xi)\vert \xi\vert ^{-1}$ 是 $L(k^\ast )$ 与 $L(k^+-0)$ 之间的一一对应. 把 $L\_1(k^\ast )$ 与 $L\_1(k^+-0)$ 中的函数看作这些基本函数的极限, 我们得到:

<div class="tate-result qed-box" markdown="1">

**引理 2.3.2.** $g(\alpha)\in L\_1(k^\ast ) \Leftrightarrow g(\xi)\vert \xi\vert ^{-1}\in L\_1(k^+-0)$, 并且对这些函数有 

$$
\int g(\alpha)\, \mathrm{d}\_1\alpha = \int\_{k^+-0} g(\xi)\,\vert \xi\vert ^{-1}\, d\xi .
$$



</div>

为后面使用, 我们需要一个一般情形下使子群 $u$ 具有测度 $1$ 的乘法测度. 为此, 我们选取如下作为 $k^\ast $ 上的标准 Haar 测度: 

$$
\mathrm{d}\alpha = \mathrm{d}\_1\alpha = \frac{d\alpha}{\vert \alpha\vert }, \qquad \text{若 } \mathfrak p \text{ 是 Archimedean 的}.
$$

 

$$
\mathrm{d}\alpha = \frac{N\mathfrak p}{N\mathfrak p-1}\,\mathrm{d}\_1\alpha
= \frac{N\mathfrak p}{N\mathfrak p-1}\,\frac{d\alpha}{\vert \alpha\vert },
\qquad \text{若 } \mathfrak p \text{ 是离散的}.
$$



<div class="tate-result qed-box" markdown="1">

**引理 2.3.3.** 若 $\mathfrak p$ 是离散的, 则 

$$
\int\_u \mathrm{d}\alpha = (N\mathfrak d)^{-\frac12}.
$$



</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 

$$
\int\_u \mathrm{d}\_1\alpha = \int\_u \vert \xi\vert ^{-1}\, d\xi = \int\_u d\xi
= \frac{N\mathfrak p-1}{N\mathfrak p}\int\_{\mathfrak o} d\xi .
$$

 因此 

$$
\int\_u \mathrm{d}\alpha = \frac{N\mathfrak p}{N\mathfrak p-1}\int\_u \mathrm{d}\_1\alpha
= \int\_{\mathfrak o} d\xi = (N\mathfrak d)^{-\frac12}.
$$



</div>

### 2.4. 局部 $\zeta$ 函数, 函数方程

本节中 $f(\xi)$ 表示定义在 $k^+$ 上的一个复值函数, $f(\alpha)$ 表示它在 $k^\ast $ 上的限制. 用 $\mathfrak z$ 表示满足以下两个条件的全部这类函数所成的类:


$f(\xi)$ 与 $\widehat f(\xi)$ 连续, 属于 $L\_1(k^+)$, 即 $f(\xi)\in\mathfrak B\_1(k^+)$;

对 $\sigma>0$, $f(\alpha)\vert \alpha\vert ^\sigma$ 与 $\widehat f(\alpha)\vert \alpha\vert ^\sigma$ 属于 $L\_1(k^\ast )$.

所谓 $k$ 的 $\zeta$ 函数, 就是函数 $f\in\mathfrak z$ 的某种可称之为乘法拟 Fourier 变换的东西. 我们确切的意思陈述在

<div class="tate-result qed-box" markdown="1">

**定义 2.4.1.** 对每个 $f\in\mathfrak z$, 我们引进一个与拟特征 $c$ 相联系的函数 $\zeta(f,c)$, 它对一切指数大于 $0$ 的拟特征定义, 由 

$$
\zeta(f,c) = \int f(\alpha)\, c(\alpha)\, \mathrm{d}\alpha
$$

 给出, 并称这样的函数为 $k$ 的 $\zeta$ 函数.

</div>

若两个拟特征的商是非分歧拟特征, 就称它们等价. 按引理 2.3.1, 一个拟特征的等价类由一切形如 $c(\alpha)=c\_0(\alpha)\vert \alpha\vert ^s$ 的拟特征组成, 其中 $c\_0(\alpha)$ 是该类的一个固定代表, $s$ 是复变量. 显然, 通过引进复参数 $s$, 我们可以把一个拟特征的等价类看成一个 Riemann 曲面. 若 $\mathfrak p$ 是 Archimedean 的, $s$ 由 $c$ 唯一确定, 这个曲面将同构于复平面. 若 $\mathfrak p$ 是离散的, $s$ 只在模 $2\pi i/\log N\mathfrak p$ 的意义下确定, 于是这个曲面同构于一个复平面, 其中相差 $2\pi i/\log N\mathfrak p$ 的整数倍的点被等同起来, 这正是真正定义单周期函数的那种曲面. 把全部拟特征的整体看成一族 Riemann 曲面, 当我们谈论拟特征的函数在某点或某区域处的正则性, 或谈论奇点时, 意思就清楚了. 我们也可以考虑这种函数的解析延拓问题, 当然这必须在每个曲面 (拟特征的等价类) 上分别进行.

<div class="tate-result qed-box" markdown="1">

**引理 2.4.1.** $\zeta$ 函数在“一切指数大于 $0$ 的拟特征”这个域中是正则的.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 我们必须证明, 对每个指数 $>0$ 的 $c$, 积分 $\int f(\alpha)c(\alpha)\vert \alpha\vert ^s \mathrm{d}\alpha$ 在 $s$ 接近 $0$ 时表示 $s$ 的一个正则函数. 利用该积分在 $s$ 接近 $0$ 时绝对收敛这一事实作估计, 证明这个函数在 $s$ 接近 $0$ 时有导数就是例行公事. 事实上, 这个导数可以通过“在积分号下求导”算出来.

</div>

我们的目的是证明, 借助一条简单的函数方程, $\zeta$ 函数可以单值亚纯地解析延拓到全部拟特征的域上. 我们从下面出发:

<div class="tate-result qed-box" markdown="1">

**引理 2.4.2.** 设 $c$ 位于 $0<$ $c$ 的指数 $<1$ 的域中, 且 $\widehat c(\alpha)=\vert \alpha\vert c^{-1}(\alpha)$, 则对任意两个函数 $f,g\in\mathfrak z$ 有 

$$
\zeta(f,c)\,\zeta(\widehat g,\widehat c) = \zeta(\widehat f,\widehat c)\,\zeta(g,c).
$$



</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 在我们所考虑的区域内, $\zeta(f,c)\zeta(\widehat g,\widehat c)=\int f(\alpha)c(\alpha)\,\mathrm{d}\alpha\cdot\int \widehat g(\beta)c^{-1}(\beta)\vert \beta\vert \,\mathrm{d}\beta$, 两个积分都绝对收敛. 我们可以把它写成 $k^\ast $ 与自身直积 $k^\ast \times k^\ast $ 上的一个绝对收敛的“二重积分”: 

$$
\iint f(\alpha)\,\widehat g(\beta)\, c(\alpha\beta^{-1})\,\vert \beta\vert \, d(\alpha,\beta).
$$

 对 $k^\ast \times k^\ast $ 施以“剪切”自同构 $(\alpha,\beta)\to(\alpha,\alpha\beta)$, 在这一自同构下测度 $d(\alpha,\beta)$ 不变, 于是得到 

$$
\iint f(\alpha)\,\widehat g(\alpha\beta)\, c(\beta^{-1})\,\vert \alpha\beta\vert \, d(\alpha,\beta).
$$

 按 Fubini 定理, 这等于累次积分 

$$
\int\left(\int f(\alpha)\widehat g(\alpha\beta)\,\vert \alpha\vert \, \mathrm{d}\alpha\right) c(\beta^{-1})\,\vert \beta\vert \, \mathrm{d}\beta .
$$

 为证明我们的论断, 只需证明内层积分 $\int f(\alpha)\widehat g(\alpha\beta)\vert \alpha\vert \, \mathrm{d}\alpha$ 关于 $f$ 与 $g$ 对称. 为此, 我们写下显然对称的加法二重积分 

$$
\iint f(\xi)\, g(\eta)\, e^{-2\pi i\Lambda(\xi\beta\eta)}\, d(\xi,\eta),
$$

 用 Fubini 定理把它改写成 

$$
\int f(\xi)\left(\int g(\eta)\, e^{-2\pi i\Lambda(\xi\beta\eta)}\, d\eta\right)\, d\xi = \int f(\xi)\, \widehat g(\xi\beta)\, d\xi,
$$

 并注意按引理 2.3.2, 最后这个表达式等于乘法积分 

$$
\int f(\alpha)\,\widehat g(\alpha\beta)\,\vert \alpha\vert \, \mathrm{d}\_1\alpha = \text{常数}
\cdot \int f(\alpha)\,\widehat g(\alpha\beta)\,\vert \alpha\vert \, \mathrm{d}\alpha .
$$



</div>

现在可以宣布局部理论的主要定理了.

<div class="tate-result qed-box" markdown="1">

**定理 2.4.1.** $\zeta$ 函数可以解析延拓到全部拟特征的域上, 并由一条如下类型的函数方程给出: 

$$
\zeta(f,c) = \rho(c)\,\zeta(\widehat f,\widehat c).
$$

 因子 $\rho(c)$ 与函数 $f$ 无关, 它是拟特征的一个亚纯函数, 在 $0<$ $c$ 的指数 $<1$ 这个域中由函数方程本身定义, 而对一切拟特征则由解析延拓定义.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 在下一节中, 我们将对拟特征的每个等价类 $C$ 具体给出一个函数 $f\_C\in\mathfrak z$, 使得函数 

$$
\rho(c) = \zeta(f\_C,c)/\zeta(\widehat f\_C,\widehat c)
$$

 在 $C$ 上 $0<$ $c$ 的指数 $<1$ 的带形内是有定义的 (即分母不恒为零). 这样定义的函数 $\rho(c)$ 将表明是我们用来描述曲面 $C$ 的参数 $s$ 的一个熟悉的亚纯函数, 因此可以解析延拓到整个 $C$ 上.

由这些事实 (它们将在第 2.5 节中得到证明), 定理直接推出. 因为 $C$ 是任意的等价类, 所以 $\rho(c)$ 对一切拟特征有定义. 又若 $f(\xi)$ 是 $\mathfrak z$ 中任一函数, 则按前一个引理有 

$$
\zeta(f,c)\,\zeta(\widehat f\_C,\widehat c) = \zeta(\widehat f,\widehat c)\,\zeta(f\_C,c),
$$

 因此 

$$
\zeta(f,c) = \rho(c)\,\zeta(\widehat f,\widehat c),
$$

 其中 $c$ 是 $0<$ $c$ 的指数 $<1$ 的域中任一拟特征, 而 $\zeta(f,c)$ 与 $\zeta(\widehat f,\widehat c)$ 原本都有定义, $C$ 是 $c$ 的等价类.

</div>

在进入下一节的计算 (这些计算将为整个理论奠定坚实基础) 之前, 我们还可以证明函数方程中因子 $\rho(c)$ 的一些简单性质, 它们直接由函数方程本身推出.

<div class="tate-result qed-box" markdown="1">

**引理 2.4.3.**

1.  $\displaystyle \rho(\widehat c)=\frac{c(-1)}{\rho(c)}$.

2.  $\displaystyle \rho(\bar c)=c(-1)\,\overline{\rho(c)}$.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.**

1.  $\displaystyle \zeta(f,c)=\rho(c)\zeta(\widehat f,\widehat c)
    =\rho(c)\rho(\widehat c)\zeta(\widehat{\widehat f},\widehat{\widehat c})
    =c(-1)\zeta(f,c)$,\
    因为 $\widehat{\widehat f}(\alpha)=f(-\alpha)$ 且 $\widehat{\widehat c}(\alpha)=c(\alpha)$. 因此 $\rho(c)\rho(\widehat c)=c(-1)$.

2.  $\begin{aligned}[t]
    \overline{\zeta(f,c)} &= \zeta(\bar f,\bar c)
    =\rho(\bar c)\,\zeta(\widehat{\bar f},\widehat{\bar c})\\
    &=\rho(\bar c)\,c(-1)\,\zeta(\widehat{\widehat{\bar f}},\widehat{\widehat{\bar c}})
    =\rho(\bar c)\,c(-1)\,\overline{\zeta(\widehat f,\widehat c)},
    \end{aligned}$\
    因为 $\widehat{\bar f}(\alpha)=\overline{\widehat f(-\alpha)}$ 且 $\widehat{\bar c}(\alpha)=\overline{\widehat c(\alpha)}$. 另一方面, 

$$
\overline{\zeta(f,c)}=\overline{\rho(c)}\ \zeta(\widehat f,\widehat c).
$$

 因此 $\rho(\bar c)=c(-1)\overline{\rho(c)}$.

</div>

<div class="tate-result qed-box" markdown="1">

**推论 2.4.1.** 对指数为 $\tfrac12$ 的 $c$ 有 $\vert \rho(c)\vert =1$.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** (指数 $c=\tfrac12 \Rightarrow c(\alpha)\bar c(\alpha)=\vert c(\alpha)\vert ^2=\vert \alpha\vert =c(\alpha)\widehat c(\alpha)\Rightarrow \bar c(\alpha)=\widehat c(\alpha)$.) 把前一个引理中 $\rho(\bar c)$ 与 $\rho(\widehat c)$ 的两个表达式等同起来, 即得 $\rho(c)\overline{\rho(c)}=1$.

</div>

### 2.5. 用特殊 $\zeta$ 函数计算 $\rho(c)$

本节包含定理 2.4.1 的证明中所许诺的那些计算. 对拟特征的每个等价类 $C$, 我们给出一个特别简单的函数 $f\_C\in\mathfrak z$, 用它可以容易地在曲面 $C$ 上计算 $\rho(c)$. 完成这一计算, 我们得到一张表, 用每个曲面 $C$ 上的参数给出 $\rho(c)$ 的解析表达式. 必须分别处理 $k$ 实, $k$ 复, $k$ 为 $\mathfrak p$ 进这三种情形.

$k$ 为实域

<table class="tate-table">
<tbody>
<tr><td>$\xi$ 是实变量.</td><td>$\alpha$ 是非零实变量.</td></tr>
<tr><td>$\Lambda(\xi)=-\xi$.</td><td>$|\alpha|$ 是通常的绝对值.</td></tr>
<tr><td>$d\xi$ 表示通常的 Lebesgue 测度.</td><td>$\displaystyle \mathrm{d}\alpha=\frac{d\alpha}{|\alpha|}$.</td></tr>
</tbody>
</table>

**拟特征的等价类.** 形如 $\vert \alpha\vert ^s$ 的拟特征 (我们简单地记作 $\vert \,\vert ^s$) 构成一个等价类. 形如 $(\operatorname{sign}\alpha)\vert \alpha\vert ^s$ 的拟特征 (我们记作 $\pm\vert \,\vert ^s$) 构成另一个.

**$\mathfrak z$ 中与之对应的函数.** 我们令 

$$
f(\xi)=e^{-\pi\xi^2}\qquad \text{与}\qquad f\_\pm(\xi)=\xi\,e^{-\pi\xi^2}.
$$



**它们的 Fourier 变换.** 我们断言 

$$
\widehat f(\xi)=f(\xi)\qquad \text{与}\qquad \widehat f\_\pm(\xi)=i f\_\pm(\xi).
$$

 事实上, 这两个断言不过就是下面两个恒等式: 

$$
\int\_{-\infty}^{\infty} e^{-\pi\eta^2+2\pi i\xi\eta}\, d\eta
= e^{-\pi\xi^2}
\qquad\text{与}\qquad
\int\_{-\infty}^{\infty} \eta\, e^{-\pi\eta^2+2\pi i\xi\eta}\, d\eta
= i\xi\, e^{-\pi\xi^2},
$$

 它们在经典 Fourier 分析中是熟知的. 其中第一个可以在指数中配方, 作复代换 $\eta\to\eta+i\xi$ (由 Cauchy 积分定理这是允许的), 并把定积分 $\displaystyle\int\_{-\infty}^{\infty} e^{-\pi\xi^2}\,d\xi$ 换成它的熟知值 $1$ 而直接建立.

第二个恒等式由对第一个施行运算 $\displaystyle\frac{1}{2\pi i}\,\frac{d}{d\xi}$ 得到.

**$\zeta$ 函数.** 我们容易算出: 

$$
\begin{aligned}
\zeta(f,\vert \,\vert ^s) &= \int f(\alpha)\,\vert \alpha\vert ^s\, \mathrm{d}\alpha
= \int\_{-\infty}^{\infty} e^{-\pi\alpha^2}\vert \alpha\vert ^s\,\frac{d\alpha}{\vert \alpha\vert }\\
&= 2\int\_0^{\infty} e^{-\pi\alpha^2}\alpha^{s-1}\, d\alpha
= \pi^{-\frac{s}{2}}\,\Gamma\left(\frac{s}{2}\right),
\end{aligned}
$$

 

$$
\begin{aligned}
\zeta(f\_\pm,\pm\vert \,\vert ^s) &= \int f\_\pm(\alpha)\,(\pm\vert \alpha\vert ^s)\, \mathrm{d}\alpha
= \int\_{-\infty}^{0}\alpha\,e^{-\pi\alpha^2}(-1)\vert \alpha\vert ^s\,
\frac{d\alpha}{\vert \alpha\vert }
+ \int\_0^{\infty}\alpha\,e^{-\pi\alpha^2}\vert \alpha\vert ^s\,\frac{d\alpha}{\vert \alpha\vert }\\
&= 2\int\_0^{\infty} e^{-\pi\alpha^2}\alpha^{s}\, d\alpha
= \pi^{-\frac{s+1}{2}}\,\Gamma\left(\frac{s+1}{2}\right),
\end{aligned}
$$

 

$$
\zeta(\widehat f,\widehat{\vert \,\vert ^s}) = \zeta(f,\vert \,\vert ^{1-s})
= \pi^{-\frac{1-s}{2}}\,\Gamma\left(\frac{1-s}{2}\right),
$$

 

$$
\zeta(\widehat f\_\pm,\widehat{\pm\vert \,\vert ^s}) = \zeta(i f\_\pm,\pm\vert \,\vert ^{1-s})
= i\,\pi^{-\frac{(1-s)+1}{2}}\,\Gamma\left(\frac{(1-s)+1}{2}\right).
$$



**$\rho(c)$ 的显式表达式:** 

$$
\rho(\vert \,\vert ^s) = \frac{\pi^{-\frac{s}{2}}\,\Gamma\left(\frac{s}{2}\right)}
{\pi^{-\frac{1-s}{2}}\,\Gamma\left(\frac{1-s}{2}\right)}
= 2^{1-s}\pi^{-s}\cos\left(\frac{\pi s}{2}\right)\,\Gamma(s),
$$

 

$$
\rho(\pm\vert \,\vert ^s) = i\,
\frac{\pi^{-\frac{s+1}{2}}\,\Gamma\left(\frac{s+1}{2}\right)}
{\pi^{-\frac{(1-s)+1}{2}}\,\Gamma\left(\frac{(1-s)+1}{2}\right)}
= -i\,2^{1-s}\pi^{-s}\sin\left(\frac{\pi s}{2}\right)\,\Gamma(s).
$$

 这里 $\rho$ 的商式表达式直接来自 $\rho$ 作为相应 $\zeta$ 函数之商的定义; 第二个形式由初等的 $\Gamma$ 函数恒等式得到.

$k$ 为复域

<table class="tate-table">
<tbody>
<tr><td>$\xi=x+iy$ 是复变量.</td><td>$\alpha=re^{i\theta}$ 是非零复变量.</td></tr>
<tr><td>$\Lambda(\xi)=-2\operatorname{Re}(\xi)=-2x$.</td><td>$|\alpha|=r^2$ 是通常绝对值的平方.</td></tr>
<tr><td>$d\xi=2|dx\,dy|$ 是通常 Lebesgue 测度的两倍.</td><td>$\displaystyle \mathrm{d}\alpha=\frac{d\alpha}{|\alpha|}=\frac{2r\,|dr\,d\theta|}{r^2}=\frac{2}{r}\,|dr\,d\theta|$.</td></tr>
</tbody>
</table>

**拟特征的等价类.** 由 $c\_n(re^{i\theta})=e^{in\theta}$ ($n$ 为任意整数) 定义的函数 $c\_n(\alpha)$ 代表不同的等价类. 第 $n$ 个等价类由特征 $c\_n(\alpha)\vert \alpha\vert ^s$ 组成, 我们记作 $c\_n\vert \,\vert ^s$.

**$\mathfrak z$ 中与之对应的函数.** 我们令 

$$
f\_n(\xi) = \begin{cases}
(x-iy)^{\vert n\vert }\, e^{-2\pi(x^2+y^2)}, & n\ge 0,\\
(x+iy)^{\vert n\vert }\, e^{-2\pi(x^2+y^2)}, & n\le 0.
\end{cases}
$$



**它们的 Fourier 变换.** 我们断言 

$$
\widehat f\_n(\xi) = i^{\vert n\vert } f\_{-n}(\xi),\qquad \text{对一切}\ n.
$$

 先对 $n\ge 0$ 用归纳法建立这个公式. 当 $n=0$ 时, 断言只是说 $f\_0(\xi)=e^{-2\pi(x^2+y^2)}$ 是自己的 Fourier 变换. 这可以把复平面上的 Fourier 积分拆成两个实变量上的积分的乘积, 并再次使用经典公式 

$$
\int\_{-\infty}^{+\infty} e^{-\pi u^2+2\pi i xu}\, du = e^{-\pi x^2}
$$

 来证明. (我们函数 $f\_0(\xi)$ 指数中的因子 $2$ 恰好补偿 $d\xi$ 与 $\Lambda(\xi)$ 中的因子 $2$.)

现在设对某个 $n\ge 0$ 已证明该断言. 这意味着我们已经建立了公式 

$$
\int f\_n(\eta)\, e^{-2\pi i\Lambda(\xi\eta)}\, d\eta = i^n f\_{-n}(\xi),
$$

 写出来就是 

$$
\int\_{-\infty}^{\infty}\!\int\_{-\infty}^{\infty} (u-iv)^n
e^{-2\pi(u^2+v^2)+4\pi i(xu-yv)}\, 2\, du\, dv
= i^n (x+iy)^n\, e^{-2\pi(x^2+y^2)}.
$$

 对两边施行算子 

$$
D = \frac{1}{4\pi i}\left(\frac{\partial}{\partial x}
+ i\,\frac{\partial}{\partial y}\right)
$$

 (这是件简单的事, 因为 $z^n$ 解析, 故 $D(x+iy)^n=0$), 我们得到 

$$
\int\_{-\infty}^{\infty}\!\int\_{-\infty}^{\infty} (u+iv)^{n+1}
e^{-2\pi(u^2+v^2)+4\pi i(xu-yv)}\, 2\, du\, dv
= i^{n+1}(x+iy)^{n+1}\, e^{-2\pi(x^2+y^2)}.
$$

 这就是对 $n+1$ 的断言. 归纳步骤完成.

为处理 $n<0$ 的情形, 对已经证明的公式 $\widehat f\_{-n}(\xi)=i^{\vert n\vert } f\_n(\xi)$ 再取一次 Fourier 变换, 并记住 

$$
\widehat{\widehat f}\_{-n}(\xi) = f\_{-n}(-\xi) = (-1)^{\vert n\vert } f\_{-n}(\xi).
$$



**$\zeta$ 函数.** 对 $\alpha=re^{i\theta}$ 我们有 

$$
\begin{array}{ll}
f\_n(\alpha) = r^{\vert n\vert }\, e^{-in\theta}\, e^{-2\pi r^2}, \qquad &
\vert \alpha\vert ^s = r^{2s},\\[6pt]
c\_n(\alpha) = e^{in\theta}, \qquad &
\displaystyle \mathrm{d}\alpha = \frac{2r\,dr\,d\theta}{r^2}.
\end{array}
$$



因此 

$$
\begin{aligned}
\zeta(f\_n,c\_n\vert \,\vert ^s) &= \int f\_n(\alpha)\, c\_n(\alpha)\,\vert \alpha\vert ^s\, \mathrm{d}\alpha
= \int\_0^{\infty}\!\int\_0^{2\pi} r^{2(s-1)+\vert n\vert }\, e^{-2\pi r^2}\, 2r\, dr\,
d\theta\\
&= 2\pi\int\_0^{\infty} (r^2)^{(s-1)+\frac{\vert n\vert }{2}}\, e^{-2\pi r^2}\, d(r^2)
= (2\pi)^{(1-s)+\frac{\vert n\vert }{2}}\,\Gamma\left(s+\frac{\vert n\vert }{2}\right),
\end{aligned}
$$

 并且 

$$
\zeta(\widehat f\_n,\widehat{c\_n\vert \,\vert ^s})
= \zeta(i^{\vert n\vert } f\_{-n}, c\_{-n}\vert \,\vert ^{1-s})
= i^{\vert n\vert }\,(2\pi)^{s+\frac{\vert n\vert }{2}}\,\Gamma\left(1-s+\frac{\vert n\vert }{2}\right).
$$



**$\rho(c)$ 的显式表达式.** 

$$
\rho(c\_n\vert \,\vert ^s) = (-i)^{\vert n\vert }\,
\frac{(2\pi)^{1-s}\,\Gamma\left(s+\frac{\vert n\vert }{2}\right)}
{(2\pi)^{s}\,\Gamma\left((1-s)+\frac{\vert n\vert }{2}\right)}.
$$



$k$ 为 $\mathfrak p$ 进域

<table class="tate-table tate-table--onecol">
<tbody>
<tr><td>$\xi$ 是一个 $\mathfrak p$ 进变量.</td></tr>
<tr><td>$\Lambda(\xi)=\lambda(S(\xi))$.</td></tr>
<tr><td>$d\xi$ 的选取使 $\mathfrak o$ 具有测度 $(N\mathfrak d)^{-\frac12}$.</td></tr>
<tr><td>$\alpha=\tilde\alpha\pi^v$, 非零 $\mathfrak p$ 进变量, 其中 $\pi$ 是阶数为 $1$ 的固定元素, $v$ 是整数.</td></tr>
<tr><td>$|\alpha|=(N\mathfrak p)^{-v}$.</td></tr>
<tr><td>$\displaystyle \mathrm{d}\alpha=\frac{N\mathfrak p}{N\mathfrak p-1}\cdot\frac{d\alpha}{|\alpha|}$, 于是 $u$ 具有乘法测度 $(N\mathfrak d)^{-\frac12}$.</td></tr>
</tbody>
</table>

**拟特征的等价类.** 对 $n\ge 0$, $c\_n(\alpha)$ 表示 $k^\ast $ 的任一导子恰为 $\mathfrak p^n$ 且满足 $c\_n(\pi)=1$ 的特征. 这些特征代表拟特征的不同等价类.

**$\mathfrak z$ 中与之对应的函数.** 我们令 

$$
f\_n(\xi) = \begin{cases}
e^{2\pi i\Lambda(\xi)}, & \text{对 } \xi\in\mathfrak d^{-1}\mathfrak p^{-n},\\
0, & \text{对 } \xi\notin\mathfrak d^{-1}\mathfrak p^{-n}.
\end{cases}
$$



**它们的 Fourier 变换.** 我们断言 

$$
\widehat f\_n(\xi) = \begin{cases}
(N\mathfrak d)^{\frac12}(N\mathfrak p)^n, & \text{对 } \xi\equiv 1
(\mathrm{mod}\ \mathfrak p^n),\\
0, & \text{对 } \xi\not\equiv 1 (\mathrm{mod}\ \mathfrak p^n).
\end{cases}
$$



<div class="tate-proof qed-box" markdown="1">

**证明.** 

$$
\widehat f\_n(\xi) = \int f\_n(\eta)\, e^{-2\pi i\Lambda(\xi\eta)}\, d\eta
= \int\_{\mathfrak d^{-1}\mathfrak p^{-n}}
e^{-2\pi i\Lambda((\xi-1)\eta)}\, d\eta .
$$

 这是紧子群 $\mathfrak d^{-1}\mathfrak p^{-n}\subset k^+$ 上加法特征 $\eta\to e^{-2\pi i\Lambda((\xi-1)\eta)}$ 的积分. 若 $\xi\equiv 1\ (\mathrm{mod}\ \mathfrak p^n)$, 这个特征在该子群上平凡, 积分就是该子群的测度, 即 $(N\mathfrak d)^{\frac12}(N\mathfrak p)^n$. 若 $\xi\not\equiv 1\ (\mathrm{mod}\ \mathfrak p^n)$, 这个特征在该子群上不平凡, 积分为 $0$.

</div>

**$\zeta$ 函数.** 先处理非分歧的情形: $n=0$. 类型 $c\_0$ 的唯一特征就是恒等特征, 而 $f\_0$ 是集合 $\mathfrak d^{-1}$ 的特征函数. 因此我们将计算 

$$
\zeta(f\_0,\vert \,\vert ^s) = \int\_{\mathfrak d^{-1}} \vert \alpha\vert ^s\, \mathrm{d}\alpha .
$$

 用 $A\_v$ 表示阶数为 $v$ 的元素所成的“环带”, 并令 $\mathfrak d=\mathfrak p^d$. 则 $\mathfrak d^{-1}=\bigcup\_{v=-d}^{\infty}A\_v$ 是不交并, 并且 

$$
\begin{aligned}
\zeta(f\_0,\vert \,\vert ^s) &= \sum\_{v=-d}^{\infty}\int\_{A\_v}\vert \alpha\vert ^s\, \mathrm{d}\alpha
= \sum\_{v=-d}^{\infty} (N\mathfrak p)^{-vs}\int\_{A\_v} \mathrm{d}\alpha\\
&= \left(\sum\_{v=-d}^{\infty} (N\mathfrak p)^{-vs}\right) (N\mathfrak d)^{-\frac12}
= \frac{(N\mathfrak p)^{ds}}{1-(N\mathfrak p)^{-s}}\, (N\mathfrak d)^{-\frac12}\\
&= \frac{(N\mathfrak d)^{\,s-\frac12}}{1-(N\mathfrak p)^{-s}}.
\end{aligned}
$$

 $\widehat f\_0$ 是 $(N\mathfrak d)^{\frac12}$ 乘以 $\mathfrak o$ 的特征函数, 所以类似地有 

$$
\begin{aligned}
\zeta(\widehat f\_0,\widehat{\vert \,\vert ^s}) &= \zeta(\widehat f\_0,\vert \,\vert ^{1-s})
= (N\mathfrak d)^{\frac12}\cdot\int\_{\mathfrak o}\vert \alpha\vert ^{1-s}\, \mathrm{d}\alpha\\
&= \sum\_{v=0}^{\infty} (N\mathfrak p)^{-v(1-s)}
= \frac{1}{1-(N\mathfrak p)^{s-1}}.
\end{aligned}
$$



在分歧的情形, $n>0$, 

$$
\begin{aligned}
\zeta(f\_n,c\_n\vert \,\vert ^s) &= \int\_{\mathfrak d^{-1}\mathfrak p^{-n}}
e^{2\pi i\Lambda(\alpha)}c\_n(\alpha)\vert \alpha\vert ^s\, \mathrm{d}\alpha\\
&= \sum\_{v=-d-n}^{\infty} (N\mathfrak p)^{-vs}\int\_{A\_v}
e^{2\pi i\Lambda(\alpha)}\, c\_n(\alpha)\, \mathrm{d}\alpha .
\end{aligned}
$$

 我们断言这个和中除第一项以外各项全为 $0$. 换句话说, 

$$
\int\_{A\_v} e^{2\pi i\Lambda(\alpha)}\, c\_n(\alpha)\, \mathrm{d}\alpha = 0
\qquad\text{对 } v>-d-n.
$$



<div class="tate-proof qed-box" markdown="1">

**证明.** 情形 1. $v\ge -d$. 这时 $A\_v\subset\mathfrak d^{-1}$, 故在 $A\_v$ 上 $e^{2\pi i\Lambda(\alpha)}=1$, 积分为 

$$
\int\_{A\_v} c\_n(\alpha)\, \mathrm{d}\alpha = \int\_u c\_n(\alpha\pi^v)\, \mathrm{d}\alpha
= \int\_u c\_n(\alpha)\, \mathrm{d}\alpha = 0,
$$

 因为 $c\_n(\alpha)$ 是分歧的, 从而在子群 $u$ 上不平凡.

情形 2. $-d>v>-d-n$. (只在有“高阶分歧”时才出现, 即 $n>1$ 时.) 为处理这一情形, 我们把 $A\_v$ 分成一些互不相交的集合, 其类型为 $\alpha\_0+\mathfrak d^{-1}=\alpha\_0+\mathfrak p^{-d}=\alpha\_0(1+\mathfrak p^{-d-v})$. 在这样的集合上 $\Lambda$ 为常数 $=\Lambda(\alpha\_0)$, 而 

$$
\int\_{\alpha\_0+\mathfrak d^{-1}} e^{2\pi i\Lambda(\alpha)}\, c\_n(\alpha)\,
\mathrm{d}\alpha = e^{2\pi i\Lambda(\alpha\_0)}\int\_{\alpha\_0+\mathfrak d^{-1}}
c\_n(\alpha)\, \mathrm{d}\alpha .
$$

 这等于 $0$, 因为 

$$
\begin{aligned}
\int\_{\alpha\_0+\mathfrak d^{-1}} c\_n(\alpha)\, \mathrm{d}\alpha
&= \int\_{\alpha\_0(1+\mathfrak p^{-d-v})} c\_n(\alpha)\, \mathrm{d}\alpha
= \int\_{1+\mathfrak p^{-d-v}} c\_n(\alpha\alpha\_0)\, \mathrm{d}\alpha\\
&= c\_n(\alpha\_0)\int\_{1+\mathfrak p^{-d-v}} c\_n(\alpha)\, \mathrm{d}\alpha,
\end{aligned}
$$

 而最后这个积分是乘法子群 $1+\mathfrak p^{-d-v}$ 上对特征 $c\_n(\alpha)$ 的积分, 该特征在此子群上不平凡. 具体地说, $-d>v\Rightarrow \mathfrak p\vert \mathfrak p^{-d-v}\Rightarrow 1+\mathfrak p^{-d-v}$ 是 $k^\ast $ 的子群, 而 $v>-d-n\Rightarrow$ 导子 $\mathfrak p^n\nmid\mathfrak p^{-d-v}\Rightarrow c\_n(\alpha)$ 在其上不平凡.

</div>

现在我们已经证明 

$$
\zeta(f\_n,c\_n\vert \,\vert ^s) = (N\mathfrak p)^{(d+n)s}\int\_{A\_{-d-n}}
e^{2\pi i\Lambda(\alpha)}\, c\_n(\alpha)\, \mathrm{d}\alpha .
$$

 为把这个式子写成更好的形式, 设 $\{\varepsilon\}$ 是商群 $u/(1+\mathfrak p^n)$ 的元素的一组代表, 于是 $u=\bigcup\_\varepsilon \varepsilon(1+\mathfrak p^n)$ 是不交并. 那么 

$$
A\_{-d-n} = u\pi^{-d-n}
= \bigcup\_\varepsilon \varepsilon\pi^{-d-n}(1+\mathfrak p^n)
= \bigcup\_\varepsilon (\varepsilon\pi^{-d-n}+\mathfrak d^{-1}).
$$

 在把 $A\_{-d-n}$ 剖分所得的每一个这样的集合上, $c\_n$ 为常数, 等于 $c\_n(\varepsilon\pi^{-d-n})=c\_n(\varepsilon)$, 而 $\Lambda$ 为常数, 等于 $\Lambda(\varepsilon\pi^{-d-n})$. 因此我们有 

$$
\begin{aligned}
\zeta(f\_n,c\_n\vert \,\vert ^s) &= (N\mathfrak p)^{(d+n)s}
\left(\sum\_\varepsilon c\_n(\varepsilon)\,
e^{2\pi i\Lambda(\varepsilon/\pi^{d+n})}\right)\,
\int\_{1+\mathfrak p^n} \mathrm{d}\alpha,
\end{aligned}
$$

 这个形式足够方便.

真正省力的地方在于计算 

$$
\zeta(\widehat f\_n,\widehat{c\_n\vert \,\vert ^s}) = \zeta(\widehat f\_n, c\_n^{-1}\vert \,\vert ^{1-s}).
$$

 因为 $\widehat f\_n$ 等于 $(N\mathfrak d)^{\frac12}(N\mathfrak p)^n$ 乘以集合 $1+\mathfrak p^n$ 的特征函数, 而在该集合上 $c\_n^{-1}(\alpha)\vert \alpha\vert ^{1-s}=1$. 因此 

$$
\zeta(\widehat f\_n,\widehat{c\_n\vert \,\vert ^s}) = (N\mathfrak d)^{\frac12}(N\mathfrak p)^n
\int\_{1+\mathfrak p^n} \mathrm{d}\alpha, \quad \text{是一个常数!}
$$



**$\rho(c)$ 的显式表达式** 

$$
\rho(\vert \,\vert ^s) = (N\mathfrak d)^{\,s-\frac12}\,
\frac{1-(N\mathfrak p)^{s-1}}{1-(N\mathfrak p)^{-s}}
$$

 

$$
\rho(c\vert \,\vert ^s) = N(\mathfrak d\mathfrak f)^{s-\frac12}\rho\_0(c),\quad \text{若 }
c \text{ 是导子为 } \mathfrak f \text{ 的分歧特征},
$$

 且满足 $c(\pi)=1$, 

$$
\rho\_0(c) = (N\mathfrak f)^{-\frac12}\sum\_\varepsilon c(\varepsilon)\,
e^{2\pi i\Lambda(\varepsilon/\pi^{\operatorname{ord}\mathfrak d\mathfrak f})}
$$

 是所谓根数, 其绝对值为 $1$. 其中 $\{\varepsilon\}$ 是 $1+\mathfrak f$ 在 $u$ 中的陪集的一组代表.

把我们算出的这些 $\zeta$ 函数取商, 如果记住 $\mathfrak d=\mathfrak p^d$ 以及在分歧情形下 $c\_n$ 的导子为 $\mathfrak f=\mathfrak p^n$, 就直接得到这些表达式. 常数 $\rho\_0(c)$ 的绝对值为 $1$ 这一事实由推论 2.4.1 推出. 因为 $c$ 是特征, $c\vert \,\vert ^{\frac12}$ 的指数为 $\frac12$, 故必有 $\vert \rho(c\vert \,\vert ^{\frac12})\vert =\vert \rho\_0(c)\vert =1$.

## 3 抽象的受限直积

### 3.1. 引言

设 $\{\mathfrak p\}$ 是一族指标. 设对每个 $\mathfrak p$ 给定一个局部紧交换群 $G\_{\mathfrak p}$, 并且对几乎所有的 $\mathfrak p$ (意思是除有限多个 $\mathfrak p$ 之外), 给定一个固定子群 $H\_{\mathfrak p}\subset G\_{\mathfrak p}$, 它是开而且紧的.

于是我们可以作一个新的抽象群 $G$, 它的元素 $a=(\ldots,a\_{\mathfrak p},\ldots)$ 是“向量”, 对每个 $\mathfrak p$ 有一个 分量 $a\_{\mathfrak p}\in G\_{\mathfrak p}$, 并且对几乎所有 $\mathfrak p$ 有 $a\_{\mathfrak p}\in H\_{\mathfrak p}$. 乘法按分量定义.

设 $S$ 是一个有限的指标集, 至少包含一切使 $H\_{\mathfrak p}$ 未定义的 $\mathfrak p$. 满足当 $\mathfrak p\notin S$ 时 $a\_{\mathfrak p}\in
H\_{\mathfrak p}$ 的元素 $a\in G$ 构成 $G$ 的一个子群, 我们记作 $G\_S$. $G\_S$ 自然地同构于局部紧群的直积 $\prod\_{\mathfrak p\in S}G\_{\mathfrak p}\times
\prod\_{\mathfrak p\notin S}H\_{\mathfrak p}$, 其中几乎所有的群都紧, 因此它按 乘积拓扑是局部紧群. 我们在 $G$ 中如下定义拓扑: 取 $G\_S$ 中 $1$ 的邻域组作为 $G$ 中 $1$ 的基本邻域组. 由此得到的 $G$ 中的拓扑不依赖于我们所选取的指标集 $S$. 这可由以下事实看出:

<div class="tate-result qed-box" markdown="1">

**引理 3.1.1.** 一切形如 $N=\prod\_{\mathfrak p}N\_{\mathfrak p}$ 的“平行体”的全体构成 $G$ 中 $1$ 的基本邻域组, 其中对一切 $\mathfrak p$, $N\_{\mathfrak p}$ 是 $G\_{\mathfrak p}$ 中 $1$ 的邻域, 并且对几乎所有 $\mathfrak p$, $N\_{\mathfrak p}=H\_{\mathfrak p}$ (回忆一下, 按假设 $H\_{\mathfrak p}$ 是开的).

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 按乘积拓扑的定义, $G\_S$ 中 $1$ 的邻域含有所述类型的平行体. 另一方面, 因为对 几乎所有 $\mathfrak p$ 有 $N\_{\mathfrak p}=H\_{\mathfrak p}$, 交集 

$$
\left(\prod\_{\mathfrak p}N\_{\mathfrak p}\right)\cap G\_S
= \prod\_{\mathfrak p\in S}N\_{\mathfrak p}\times\prod\_{\mathfrak p\notin S}
(N\_{\mathfrak p}\cap H\_{\mathfrak p})
$$

 是 $G\_S$ 中 $1$ 的邻域.

</div>

显然 $G\_S$ 在 $G$ 中是开的, 且作为 $G$ 的子空间在 $G\_S$ 上诱导的拓扑, 与起初 我们在 $G\_S$ 上赋予的乘积拓扑相同. 因此 $G\_S$ 中 $1$ 的紧邻域也是 $G$ 中 $1$ 的紧邻域. 由此可见 $G$ 是局部紧的.

<div class="tate-result qed-box" markdown="1">

**定义 3.1.1.** 我们称 $G$ (作为一个局部紧交换群) 为诸群 $G\_{\mathfrak p}$ 相对于诸子群 $H\_{\mathfrak p}$ 的受限直积.

</div>

当然, 把基本群 $G\_{\mathfrak p}$ 与 $G$ 中由一切除第 $\mathfrak p$ 个分量外 其余分量均为 $1$ 的元素 $a\_{\mathfrak p}=(1,1,\ldots,a\_{\mathfrak p},\ldots)$ 所成的子群等同起来是方便的. 因为这个子群无论在拓扑上还是在代数上都自然地与 $G\_{\mathfrak p}$ 同构.

由于 $G$ 的任一元素 $a$ 的各分量 $a\_{\mathfrak p}$ 对几乎所有 $\mathfrak p$ 落在 $H\_{\mathfrak p}$ 中, $G$ 是诸子群 $G\_S$ 的并. 这一事实使我们能把对 $G$ 的研究归结为对各子群 $G\_S$ 的研究.

这些 $G\_S$ 又可借引入如下子群而得到有效的分析: 令 $G^S\subset G\_S$ 为一切满足 当 $\mathfrak p\in S$ 时 $a\_{\mathfrak p}=1$, 而当 $\mathfrak p\notin S$ 时 $a\_{\mathfrak p}\in H\_{\mathfrak p}$ 的元素 $a\in G$ 所成的子群. $G^S$ 是紧的, 因为它自然地同构于紧群的直积 $\prod\_{\mathfrak p\notin S}H\_{\mathfrak p}$. 于是 $G\_S$ 可以看成一个有限多个基本群 $G\_{\mathfrak p}$ 的直积与紧群 $G^S$ 的直积: $G\_S=\left(\prod\_{\mathfrak p\in S}G\_{\mathfrak p}\right)\times G^S$.

我们以下面的引理结束关于受限直积的引言:

<div class="tate-result qed-box" markdown="1">

**引理 3.1.2.** 子集 $C\subset G$ 相对紧 (即其闭包紧), 当且仅当它含于一个形如 $\prod\_{\mathfrak p}B\_{\mathfrak p}$ 的平行体中, 其中对一切 $\mathfrak p$, $B\_{\mathfrak p}$ 是 $G\_{\mathfrak p}$ 的紧子集, 并且对几乎所有 $\mathfrak p$, $B\_{\mathfrak p}=H\_{\mathfrak p}$.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** $G$ 的任一紧子集含于某个 $G\_S$ 中, 因为诸 $G\_S$ 是覆盖 $G$ 的开集族, 而有限 多个子群 $G\_S$ 的并仍是 $G\_S$. $G\_S$ 的任一紧子集含于所述类型的平行体中, 因为它含于它在各分量群 $G\_{\mathfrak p}$ 上的“投影”的笛卡儿积中. 这些投影 是紧的, 因为它们是连续像; 并且当 $\mathfrak p\notin S$ 时它们含于 $H\_{\mathfrak p}$ 中.

另一方面, 任一平行体 $\prod\_{\mathfrak p}B\_{\mathfrak p}$ 显然是某个 $G\_S$ 的 紧子集, 从而是 $G$ 的紧子集.

</div>

### 3.2. 特征

设 $c(a)$ 是 $G$ 的一个拟特征, 即 $G$ 到复数中的一个连续乘法映射. 用 $c\_{\mathfrak p}$ 表示 $c$ 在 $G\_{\mathfrak p}$ 上的限制, 即对 $a\_{\mathfrak p}\in G\_{\mathfrak p}$ 有 $c\_{\mathfrak p}(a\_{\mathfrak p})
= c(a\_{\mathfrak p}) = c(1,1,\ldots,a\_{\mathfrak p},\ldots)$. 显然 $c\_{\mathfrak p}$ 是 $G\_{\mathfrak p}$ 的拟特征.

<div class="tate-result qed-box" markdown="1">

**引理 3.2.1.** 对几乎所有 $\mathfrak p$, $c\_{\mathfrak p}$ 在 $H\_{\mathfrak p}$ 上平凡; 并且对任意 $a\in G$ 有 

$$
c(a) = \prod\_{\mathfrak p} c\_{\mathfrak p}(a\_{\mathfrak p}),
$$

 其中乘积的几乎所有因子为 $1$.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 设 $U$ 是复数中 $1$ 的一个邻域, 除 $\{1\}$ 之外不含任何乘法子群. 设 $N=\prod\_{\mathfrak p}N\_{\mathfrak p}$ 是 $G$ 中 $1$ 的一个邻域, 使得 $c(N)\subset U$. 选取 $S$ 包含一切使 $N\_{\mathfrak p}\ne H\_{\mathfrak p}$ 的 $\mathfrak p$. 那么 $G^S\subset N\Rightarrow c(G^S)\subset U\Rightarrow
c(G^S)=1\Rightarrow$ 对 $\mathfrak p\notin S$ 有 $c(H\_{\mathfrak p})=1$. 若 $a$ 是 $G$ 的一个固定元素, 我们对 $S$ 再加一个条件: $a\in G\_S$, 并写 $a=\prod\_{\mathfrak p\in S}a\_{\mathfrak p}\cdot a^S$, 其中 $a^S\in G^S$. 于是 

$$
c(a) = \prod\_{\mathfrak p\in S}c(a\_{\mathfrak p})\cdot c(a^S)
= \prod\_{\mathfrak p\in S}c\_{\mathfrak p}(a\_{\mathfrak p})
= \prod\_{\mathfrak p}c\_{\mathfrak p}(a\_{\mathfrak p}),
$$

 因为当 $\mathfrak p\notin S$ 时 $c\_{\mathfrak p}(a\_{\mathfrak p})=1$.

</div>

<div class="tate-result qed-box" markdown="1">

**引理 3.2.2.** 设对每个 $\mathfrak p$ 给定 $G\_{\mathfrak p}$ 的一个拟特征 $c\_{\mathfrak p}$, 且对几乎所有 $\mathfrak p$, $c\_{\mathfrak p}$ 在 $H\_{\mathfrak p}$ 上平凡. 那么若定义 $c(a)=\prod\_{\mathfrak p}
c\_{\mathfrak p}(a\_{\mathfrak p})$, 我们就得到 $G$ 的一个拟特征.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 显然 $c(a)$ 是乘性的. 为看出它连续, 选取 $S$ 包含一切使 $c\_{\mathfrak p}(H\_{\mathfrak p})\ne 1$ 的 $\mathfrak p$. 设 $s$ 是 $S$ 中 $\mathfrak p$ 的个数. 给定复数中 $1$ 的一个邻域 $U$, 选取邻域 $V$ 使 $V^s\subset U$. 对 $\mathfrak p\in S$, 设 $N\_{\mathfrak p}$ 是 $G\_{\mathfrak p}$ 中 $1$ 的邻域, 使 $c\_{\mathfrak p}(N\_{\mathfrak p})\subset V$; 对 $\mathfrak p\notin S$, 令 $N\_{\mathfrak p}=H\_{\mathfrak p}$. 那么 

$$
c\left(\prod\_{\mathfrak p}N\_{\mathfrak p}\right)\subset V^s\subset U.
$$



</div>

把考虑范围限制到特征上, 我们首先注意到 $c(a)=\prod\_{\mathfrak p}
c\_{\mathfrak p}(a\_{\mathfrak p})$ 是特征, 当且仅当一切 $c\_{\mathfrak p}$ 都是 特征. 对一切 $\mathfrak p$, 用 $\widehat G\_{\mathfrak p}$ 表示 $G\_{\mathfrak p}$ 的特征群; 对那些 $H\_{\mathfrak p}$ 有定义的 $\mathfrak p$, 用 $H\_{\mathfrak p}^\ast \subset \widehat G\_{\mathfrak p}$ 表示 $\widehat G\_{\mathfrak p}$ 中一切在 $H\_{\mathfrak p}$ 上平凡的元素 $c\_{\mathfrak p}$ 所成的子群. 那么 $H\_{\mathfrak p}$ 紧 $\Rightarrow \widehat H\_{\mathfrak p}\cong
\widehat G\_{\mathfrak p}/H\_{\mathfrak p}^\ast $ 离散 $\Rightarrow
H\_{\mathfrak p}^\ast $ 开, 而 $H\_{\mathfrak p}$ 开 $\Rightarrow
G\_{\mathfrak p}/H\_{\mathfrak p}$ 离散 $\Rightarrow
\widehat{G\_{\mathfrak p}/H\_{\mathfrak p}}\cong H\_{\mathfrak p}^\ast $ 紧.

<div class="tate-result qed-box" markdown="1">

**定理 3.2.1.** 诸群 $\widehat G\_{\mathfrak p}$ 相对于诸子群 $H\_{\mathfrak p}^\ast $ 的受限直积, 自然地与 $G$ 的特征群 $\widehat G$ 同构, 无论在拓扑上还是在代数上都是如此.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 当然, 我们的意思是指把 $c=(\ldots,c\_{\mathfrak p},\ldots)$ 与特征 $c(a)=\prod\_{\mathfrak p}c\_{\mathfrak p}(a\_{\mathfrak p})$ 等同起来. 把前面 两个引理用于特征, 表明这是两个群之间的代数同构. 我们只需检验拓扑相同. 为此 我们如下推理: $c=(\ldots,c\_{\mathfrak p},\ldots)$ 作为特征接近 $1$ $\Leftrightarrow$ 对某个大的紧集 $B\subset G$, $c(B)$ 接近 $1$ $\Leftrightarrow$ 当 $B\_{\mathfrak p}\subset G\_{\mathfrak p}$ 紧且对几乎所有 $\mathfrak p$ 有 $B\_{\mathfrak p}=H\_{\mathfrak p}$ 时, $c\left(\prod\_{\mathfrak p}B\_{\mathfrak p}\right)$ 接近 $1$ $\Leftrightarrow$ 凡是 $B\_{\mathfrak p}\ne H\_{\mathfrak p}$ 之处 $c\_{\mathfrak p}(B\_{\mathfrak p})$ 接近 $1$, 而在其余 $\mathfrak p$ 处 $c\_{\mathfrak p}(B\_{\mathfrak p})=c\_{\mathfrak p}(H\_{\mathfrak p})=1$ (因为 $H\_{\mathfrak p}$ 是子群, 只有当 $c\_{\mathfrak p}(H\_{\mathfrak p})=1$ 时 $c\_{\mathfrak p}(H\_{\mathfrak p})$ 才可能接近 $1$) $\Leftrightarrow$ 对有限 多个 $\mathfrak p$, $c\_{\mathfrak p}$ 在 $\widehat G\_{\mathfrak p}$ 中接近 $1$, 而在其余 $\mathfrak p$ 处 $c\_{\mathfrak p}\in H\_{\mathfrak p}^\ast $ $\Leftrightarrow$ $c$ 在诸 $\widehat G\_{\mathfrak p}$ 的受限直积中接近 $1$.

</div>

### 3.3. 测度

现在设我们在每个 $G\_{\mathfrak p}$ 上选定了 Haar 测度 $\mathrm{d}a\_{\mathfrak p}$, 使得对几乎所有 $\mathfrak p$ 有 $\int\_{H\_{\mathfrak p}}\mathrm{d}a\_{\mathfrak p}=1$. 我们希望定义 $G$ 上的一个 Haar 测度 $\mathrm{d}a$, 使得在某种意义上 $\mathrm{d}a=\prod\_{\mathfrak p}\mathrm{d}a\_{\mathfrak p}$. 为此 选取一个 $S$; 然后把 $G\_S$ 看成有限直积 $G\_S=\left(\prod\_{\mathfrak p\in S}G\_{\mathfrak p}\right)\times G^S$, 以便在 $G\_S$ 上定义测度 $\mathrm{d}a\_S=\left(\prod\_{\mathfrak p\in S}\mathrm{d}a\_{\mathfrak p}\right)
\cdot \mathrm{d}a^S$, 其中 $\mathrm{d}a^S$ 是紧群 $G^S$ 上使 $\int\_{G^S}\mathrm{d}a^S=\prod\_{\mathfrak p\notin S}\left(\int\_{H\_{\mathfrak p}}
\mathrm{d}a\_{\mathfrak p}\right)$ 的那个测度. 由于 $G\_S$ 是 $G$ 的开子群, $G$ 上的 Haar 测度 $\mathrm{d}a$ 现在就由这一要求确定. 为看出我们 刚才选取的 $\mathrm{d}a$ 确实不依赖于集合 $S$, 设 $T\supset S$ 是更大的指标集. 那么 $G\_S\subset G\_T$, 我们只需检验用 $T$ 作出的 $\mathrm{d}a\_T$ 在 $G\_S$ 上与用 $S$ 作出的 $\mathrm{d}a\_S$ 一致. 由分解 $G^S=\left(\prod\_{\mathfrak p\in T-S}H\_{\mathfrak p}
\right)\times G^T$ 可以看出 $\mathrm{d}a^S=\left(\prod\_{\mathfrak p\in T-S}
\mathrm{d}a\_{\mathfrak p}\right)\cdot \mathrm{d}a^T$; 因为右端的测度给予紧群 $G^S$ 所需要的 测度. 因此 

$$
\mathrm{d}a\_S = \prod\_{\mathfrak p\in S}\mathrm{d}a\_{\mathfrak p}\cdot \mathrm{d}a^S
= \prod\_{\mathfrak p\in S}\mathrm{d}a\_{\mathfrak p}\cdot\prod\_{\mathfrak p\in T-S}
\mathrm{d}a\_{\mathfrak p}\cdot \mathrm{d}a^T = \mathrm{d}a\_T.
$$

 因此我们确定了 $G$ 上唯一的 Haar 测度 $\mathrm{d}a$, 可以把它象征地记作 $\mathrm{d}a=\prod\_{\mathfrak p}\mathrm{d}a\_{\mathfrak p}$.

若 $\varphi(S)$ 是有限指标集 $S$ 的任一函数, 取值于一个拓扑空间, 则我们用 记号 $\lim\_S\varphi(S)=\varphi\_0$ 表示如下陈述: 给定 $\varphi\_0$ 的任一邻域 $V$, 存在集合 $S(V)$ 使得 $S\supset S(V)\Rightarrow \varphi(S)\in V$. 直观地说, $\lim\_S\varphi(S)$ 就是当 $S$ 变得越来越大时 $\varphi(S)$ 的极限.

<div class="tate-result qed-box" markdown="1">

**引理 3.3.1.** 若 $f(a)$ 是 $G$ 上的函数, 则 

$$
\int f(a)\, \mathrm{d}a = \lim\_S \int\_{G\_S} f(a)\, \mathrm{d}a,
$$

 只要满足以下之一: (1) $f(a)$ 可测, $f(a)\ge 0$, 此时积分值允许为 $+\infty$; 或 (2) $f(a)\in L\_1(G)$, 此时积分值为复数.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 无论情形 (1) 还是 (2), $\int f(a)\,\mathrm{d}a$ 都是 $\int\_B f(a)\,\mathrm{d}a$ 当紧集 $B\subset G$ 越来越大时的极限. 由于任一紧集 $B$ 含于某个 $G\_S$ 中, 命题得证.

</div>

<div class="tate-result qed-box" markdown="1">

**引理 3.3.2.** 设对每个 $\mathfrak p$ 给定连续函数 $f\_{\mathfrak p}\in L\_1(G\_{\mathfrak p})$, 使得对几乎所有 $\mathfrak p$ 在 $H\_{\mathfrak p}$ 上 $f\_{\mathfrak p}(a\_{\mathfrak p})=1$. 在 $G$ 上定义函数 $f(a)=\prod\_{\mathfrak p}f\_{\mathfrak p}(a\_{\mathfrak p})$ (这实际上是有限 乘积), 我们断言:

\(1\) $f(a)$ 在 $G$ 上连续.

\(2\) 对任一集合 $S$, 只要它至少包含那些使 $f\_{\mathfrak p}(H\_{\mathfrak p})\ne 1$ 或 $\int\_{H\_{\mathfrak p}}\mathrm{d}a\_{\mathfrak p}\ne 1$ 的 $\mathfrak p$, 就有 

$$
\int\_{G\_S} f(a)\, \mathrm{d}a = \prod\_{\mathfrak p\in S}\left[\int\_{G\_{\mathfrak p}}
f\_{\mathfrak p}(a\_{\mathfrak p})\, \mathrm{d}a\_{\mathfrak p}\right].
$$



</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** (1) 任一 $G\_S$ 上 $f(a)$ 显然连续, 从而在 $G$ 上连续.

\(2\) 对 $a\in G\_S$, $f(a)=\prod\_{\mathfrak p\in S}f\_{\mathfrak p}
(a\_{\mathfrak p})$. 因此 

$$
\begin{aligned}
\int\_{G\_S} f(a)\, \mathrm{d}a &= \int\_{G\_S} f(a)\, \mathrm{d}a\_S
= \int\_{G\_S}\left(\prod\_{\mathfrak p\in S}f\_{\mathfrak p}(a\_{\mathfrak p})
\right)\left(\prod\_{\mathfrak p\in S}\mathrm{d}a\_{\mathfrak p}\cdot \mathrm{d}a^S\right)\\
&= \prod\_{\mathfrak p\in S}\left[\int f\_{\mathfrak p}(a\_{\mathfrak p})\,
\mathrm{d}a\_{\mathfrak p}\right]\cdot\int\_{G^S} \mathrm{d}a^S
= \prod\_{\mathfrak p\in S}\left[\int f\_{\mathfrak p}(a\_{\mathfrak p})\,
\mathrm{d}a\_{\mathfrak p}\right].
\end{aligned}
$$



</div>

<div class="tate-result qed-box" markdown="1">

**定理 3.3.1.** 若 $f\_{\mathfrak p}(a\_{\mathfrak p})$ 与 $f(a)$ 是前一个引理中的函数, 并且 还有 

$$
\prod\_{\mathfrak p}\left[\int \vert f\_{\mathfrak p}(a\_{\mathfrak p})\vert \,
\mathrm{d}a\_{\mathfrak p}\right]\ \left(=\lim\_S\left\{\prod\_{\mathfrak p\in S}
\left[\int\vert f\_{\mathfrak p}(a\_{\mathfrak p})\vert \,\mathrm{d}a\_{\mathfrak p}\right]\right\}\right)
< \infty,
$$

 则 $f(a)\in L\_1(G)$, 并且 

$$
\int f(a)\, \mathrm{d}a = \prod\_{\mathfrak p}\left[\int f\_{\mathfrak p}
(a\_{\mathfrak p})\, \mathrm{d}a\_{\mathfrak p}\right].
$$



</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 把前一个引理与再前一个引理合起来用; 先对函数 $\vert f(a)\vert =\prod\_{\mathfrak p}\vert f\_{\mathfrak p}(a\_{\mathfrak p})\vert $ 用, 看出 $f(a)\in L\_1(G)$; 再对 $f(a)$ 本身用, 算出 $\int f(a)\,\mathrm{d}a$.

</div>

我们以关于受限直积中 Fourier 分析的一些说明来结束本章. 如我们已经看到的, $G$ 的特征群 $\widehat G$ 是诸特征群 $\widehat G\_{\mathfrak p}$ 相对于与 $H\_{\mathfrak p}$ 正交的子群 $H\_{\mathfrak p}^\ast $ 的受限直积. 用 $c=(\ldots,c\_{\mathfrak p},\ldots)$ 表示 $\widehat G$ 的一般元素. (本段中 $c$ 与 $c\_{\mathfrak p}$ 都是特征, 不是拟特征.) 设 $\mathrm{d}c\_{\mathfrak p}$ 是 $\widehat G\_{\mathfrak p}$ 中与 $G\_{\mathfrak p}$ 中测度 $\mathrm{d}a\_{\mathfrak p}$ 对偶 的测度. 注意若 $f\_{\mathfrak p}(a\_{\mathfrak p})$ 是 $H\_{\mathfrak p}$ 的 特征函数, 则它的 Fourier 变换 $\widehat f\_{\mathfrak p}(c\_{\mathfrak p})
=\int f\_{\mathfrak p}(a\_{\mathfrak p})\overline{c\_{\mathfrak p}
(a\_{\mathfrak p})}\,\mathrm{d}a\_{\mathfrak p}=\int\_{H\_{\mathfrak p}}\mathrm{d}a\_{\mathfrak p}$ 乘以 $H\_{\mathfrak p}^\ast $ 的特征函数. 由这一事实与反演公式可得 

$$
\left(\int\_{H\_{\mathfrak p}}\mathrm{d}a\_{\mathfrak p}\right)
\left(\int\_{H\_{\mathfrak p}^\ast }\mathrm{d}c\_{\mathfrak p}\right) = 1.
$$

 因此对几乎所有 $\mathfrak p$ 有 $\int\_{H\_{\mathfrak p}^\ast }\mathrm{d}c\_{\mathfrak p}=1$, 于是可令 $\mathrm{d}c=\prod\_{\mathfrak p}\mathrm{d}c\_{\mathfrak p}$.

<div class="tate-result qed-box" markdown="1">

**引理 3.3.3.** 若对一切 $\mathfrak p$ 有 $f\_{\mathfrak p}(a\_{\mathfrak p})\in\mathfrak B\_1(G\_{\mathfrak p})$, 且对 几乎所有 $\mathfrak p$, $f\_{\mathfrak p}(a\_{\mathfrak p})$ 是 $H\_{\mathfrak p}$ 的特征函数, 则函数 $f(a)=\prod\_{\mathfrak p}f\_{\mathfrak p}(a\_{\mathfrak p})$ 的 Fourier 变换 为 $\widehat f(c)=\prod\_{\mathfrak p}\widehat f\_{\mathfrak p}(c\_{\mathfrak p})$, 并且 $f(a)\in\mathfrak B\_1(G)$.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 对函数 $f(a)\overline{c(a)}=\prod\_{\mathfrak p}
f\_{\mathfrak p}(a\_{\mathfrak p})\overline{c\_{\mathfrak p}(a\_{\mathfrak p})}$ 应用定理 3.3.1, 可知乘积的 Fourier 变换是 Fourier 变换的乘积. 由于 $f\_{\mathfrak p}(a\_{\mathfrak p})\in\mathfrak B\_1(G\_{\mathfrak p})$, 对一切 $\mathfrak p$ 有 $\widehat f\_{\mathfrak p}(c\_{\mathfrak p})\in L\_1(\widehat G\_{\mathfrak p})$. 对 几乎所有 $\mathfrak p$, 按上面的说明 $\widehat f\_{\mathfrak p}(c\_{\mathfrak p})$ 是 $H\_{\mathfrak p}^\ast $ 的特征函数. 由此看出 $\widehat f(c)\in L\_1(\widehat G)$, 从而 $f(a)\in\mathfrak B\_1(G)$.

</div>

<div class="tate-result qed-box" markdown="1">

**推论 3.3.1.** 测度 $\mathrm{d}c=\prod\_{\mathfrak p}\mathrm{d}c\_{\mathfrak p}$ 与 $\mathrm{d}a=\prod\_{\mathfrak p}\mathrm{d}a\_{\mathfrak p}$ 对偶.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 把前一个引理应用于群 $\widehat G$ 与测度 $\mathrm{d}c$, 我们对这些“乘积”函数得到 反演公式 

$$
f(a) = \int \widehat f(c)\,c(a)\,\mathrm{d}c,
$$

 它来自各分量上的反演公式.

</div>

## 4 大范围的理论

### 4.1. 加法理论

本章中, $k$ 表示一个有限代数数域, $\mathfrak p$ 表示 $k$ 的一般素除子. 今后 $k$ 在素除子 $\mathfrak p$ 处的完备化记作 $k\_{\mathfrak p}$, 而第 2 章中为局部域 $k\_{\mathfrak p}$ 定义的一切符号 $\mathfrak o$, $\Lambda$, $\mathfrak d$, $\vert \,\vert $, $c$ 等等, 也都在下标上标明 $\mathfrak p$, 即 $\mathfrak o\_{\mathfrak p}$, $\Lambda\_{\mathfrak p}$, $\mathfrak d\_{\mathfrak p}$, $\vert \,\vert \_{\mathfrak p}$, $c\_{\mathfrak p}$, 等等.

<div class="tate-result qed-box" markdown="1">

**定义 4.1.1.** $k$ 的赋值向量加法群 $V$ 是一切素除子 $\mathfrak p$ 上诸群 $k\_{\mathfrak p}^+$ 相对于诸子群 $\mathfrak o\_{\mathfrak p}$ 的受限直和.

</div>

我们用 $\mathfrak{x}=(\ldots,\mathfrak{x}\_{\mathfrak p},\ldots)$ 表示 $V$ 的一般元素 (即赋值向量). 由定理 3.2.1 与 2.2.1 以及引理 2.2.3 看出, $V$ 的特征群自然地是诸群 $k\_{\mathfrak p}^+$ 相对于诸子群 $\mathfrak d\_{\mathfrak p}^{-1}$ 的受限直和. 由于对几乎所有 $\mathfrak p$ 有 $\mathfrak d\_{\mathfrak p}=\mathfrak o\_{\mathfrak p}$, 这个和就又是 $V$ 自身! 更仔细地看这些定理中建立起来的等同关系, 我们看到元素 $\eta=(\ldots,\eta\_{\mathfrak p},\ldots)\in V$ 应与 $V$ 的如下特征等同起来: 

$$
\mathfrak{x} = (\ldots,\mathfrak{x}\_{\mathfrak p},\ldots) \to \prod\_{\mathfrak p}
\exp(2\pi i\Lambda\_{\mathfrak p}(\eta\_{\mathfrak p}\mathfrak{x}\_{\mathfrak p}))
= \exp\left[2\pi i\sum\_{\mathfrak p}\Lambda\_{\mathfrak p}
(\eta\_{\mathfrak p}\mathfrak{x}\_{\mathfrak p})\right].
$$

 这提示我们在 $V$ 上定义加性函数 

$$
\Lambda(\mathfrak{x}) = \sum\_{\mathfrak p}\Lambda\_{\mathfrak p}(\mathfrak{x}\_{\mathfrak p}),
$$

 并在 $V$ 的元素之间引入按分量定义的乘法 

$$
\eta \mathfrak{x} = (\ldots,\eta\_{\mathfrak p},\ldots)(\ldots,\mathfrak{x}\_{\mathfrak p},\ldots)
= (\ldots,\eta\_{\mathfrak p}\mathfrak{x}\_{\mathfrak p},\ldots),
$$

 以便能简洁地断言:

<div class="tate-result qed-box" markdown="1">

**定理 4.1.1.** 若把元素 $\eta\in V$ 与 $V$ 的特征 $\mathfrak{x}\to e^{2\pi i\Lambda(\eta\mathfrak{x})}$ 等同起来, 则 $V$ 自然地就是它自己的特征群.

</div>

当然, 我们在 $V$ 上取第 3.3 节中所述的测度 $d\mathfrak{x}=\prod\_{\mathfrak p}d\mathfrak{x}\_{\mathfrak p}$, 其中 $d\mathfrak{x}\_{\mathfrak p}$ 是第 2.2 节中定义的局部加法测度. 由于这些局部测度 $d\mathfrak{x}\_{\mathfrak p}$ 的选取使它们各自对偶于自身, 按推论 3.3.1, $d\mathfrak{x}$ 也一样. 我们把这一事实正式陈述为

<div class="tate-result qed-box" markdown="1">

**定理 4.1.2.** 若对函数 $f(\mathfrak{x})\in L\_1(V)$ 如下定义 Fourier 变换 

$$
\widehat f(\eta) = \int f(\mathfrak{x})\, e^{-2\pi i\Lambda(\eta\mathfrak{x})}\, d\mathfrak{x},
$$

 则对 $f(\mathfrak{x})\in\mathfrak B\_1(V)$, 反演公式 

$$
f(\mathfrak{x}) = \int \widehat f(\eta)\, e^{2\pi i\Lambda(\mathfrak{x}\eta)}\, d\eta
$$

 成立.

</div>

局部引理 2.2.4 与 2.2.5, 即对 $\alpha\in k^\ast $ 的陈述 $d(\alpha\xi)=\vert \alpha\vert \,d\xi$, 在大范围中的类比是什么? 在那个局部考虑中, $\alpha$ 起着 $k\_{\mathfrak p}^+$ 的自同构的作用, 即自同构 $\xi\to\alpha\xi$. 这就引导我们去考察如下问题: 对什么样的 $a\in V$, $x\to ax$ 是 $V$ 的自同构? 我们首先注意到, 对任意 $a\in V$, $x\to ax$ 是 $V$ 到 $V$ 的连续同态. 它成为自同构的必要条件是存在 $b\in V$ 使 $ab=1=(1,1,\ldots)$. 但这个条件也是充分的, 因为有了这个 $b$, 我们就得到同一形式的逆映射 $x\to bx$. 现在要让这样的 $b$ 作为一个“无限制的”向量存在, 就需要对一切 $\mathfrak p$ 有 $a\_{\mathfrak p}\ne 0$, 于是 $b\_{\mathfrak p}=a\_{\mathfrak p}^{-1}$. 进一步的条件 $b\in V$ 意味着对几乎所有 $\mathfrak p$ 有 $a\_{\mathfrak p}^{-1}\in\mathfrak o\_{\mathfrak p}$, 从而对几乎所有 $\mathfrak p$ 有 $\vert a\_{\mathfrak p}\vert \_{\mathfrak p}=1$. 这两个条件合起来正好说明 $a$ 是 Chevalley 意义下的伊代尔. 我们已证得

<div class="tate-result qed-box" markdown="1">

**引理 4.1.1.** 映射 $x\to ax$ 是 $V$ 的自同构, 当且仅当 $a$ 是伊代尔.

</div>

目前我们只在这样一个角色中考虑伊代尔. 后面我们将把伊代尔乘法群作为一个自身独立的群来研究, 赋予它自己的拓扑, 即作为诸群 $k\_{\mathfrak p}^\ast $ 相对于诸子群 $u\_{\mathfrak p}$ 的受限直积.

为回答关于这些自同构下测度变换的原始问题, 我们陈述

<div class="tate-result qed-box" markdown="1">

**引理 4.1.2.** 对伊代尔 $a$, 

$$
d(a\mathfrak{x}) = \vert a\vert \, d\mathfrak{x},
$$

 其中 

$$
\vert a\vert  = \prod\_{\mathfrak p}\vert a\_{\mathfrak p}\vert \_{\mathfrak p}
$$

 (实际上是有限乘积).

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 若 $N=\prod\_{\mathfrak p}N\_{\mathfrak p}$ 是 $V$ 中 $0$ 的紧邻域, 则由定理 3.3.1 与引理 2.2.5 有 

$$
\int\_N d\mathfrak{x} = \prod\_{\mathfrak p}\int\_{N\_{\mathfrak p}}d\mathfrak{x}\_{\mathfrak p},
\qquad\text{以及}\qquad
\int\_{aN}d\mathfrak{x} = \prod\_{\mathfrak p}\int\_{a\_{\mathfrak p}N\_{\mathfrak p}}
d\mathfrak{x}\_{\mathfrak p} = \prod\_{\mathfrak p}\vert a\_{\mathfrak p}\vert \_{\mathfrak p}
\int\_{N\_{\mathfrak p}}d\mathfrak{x}\_{\mathfrak p}.
$$



</div>

我们在关于 $V$ 的初步讨论中必须做的最后一件, 也是最重要的一件事, 是看出域 $k$ 怎样嵌入 $V$. 我们把元素 $\xi\in k$ 与各分量都等于 $\xi$ 的赋值向量 $\xi=(\xi,\xi,\ldots,\xi,\ldots)$ 等同起来, 并把 $k$ 看作 $V$ 的子群. 它是怎样一种子群?

<div class="tate-result qed-box" markdown="1">

**引理 4.1.3.** 若 $S\_{\infty}$ 表示 $k$ 的 Archimedean 素点的集合, 则 (1) $k\cap V\_{S\_{\infty}}=\mathfrak o$, 即 $k$ 中代数整数所成的环; (2) $k+V\_{S\_{\infty}}=V$.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** (1) 这不过是说, 元素 $\xi\in k$ 是代数整数当且仅当它在一切有限素点处是整数.

\(2\) $k+V\_{S\_{\infty}}=V$ 的意思是: 给定任意 $\mathfrak{x}\in V$, 存在 $\xi\in k$ 在如下意义下逼近它, 即对一切有限 $\mathfrak p$ 有 $\xi-\mathfrak{x}\_{\mathfrak p}\in\mathfrak o\_{\mathfrak p}$. 这样的 $\xi$ 可以通过在 $\mathfrak o$ 中解同余方程组找到. 解的存在性由孙子剩余定理保证.

</div>

现在用 $\overset{\infty}{V}$ 表示 $V$ 的“无穷部分”, 即 $k$ 的各 Archimedean 完备化的笛卡儿积 $\prod\_{\mathfrak p\in S\_{\infty}}k\_{\mathfrak p}$. 若 $k$ 在有理域上的一个生成方程有 $r\_1$ 个实根和 $r\_2$ 对共轭复根, 则 $\overset{\infty}{V}$ 是 $r\_1$ 条实直线与 $r\_2$ 个复平面的乘积. 作为这样的东西, 它自然是实数域上的向量空间, 维数为 $n=r\_1+2r\_2$, 即 $k$ 的绝对次数. 对任意 $\mathfrak{x}\in V$, 用 $\overset{\infty}{\mathfrak{x}}$ 表示 $\mathfrak{x}$ 在 $\overset{\infty}{V}$ 上的投影 $\overset{\infty}{\mathfrak{x}}=(\ldots,\mathfrak{x}\_{\mathfrak p},\ldots)\_{\mathfrak p\in S\_{\infty}}$.

<div class="tate-result qed-box" markdown="1">

**引理 4.1.4.** 若 $\{\omega\_1,\omega\_2,\ldots,\omega\_n\}$ 是 $k$ 的整数环 $\mathfrak o$ 在有理整数环上的极小基, 则 $\{\overset{\infty}{\omega}\_1,\overset{\infty}{\omega}\_2,\ldots, \overset{\infty}{\omega}\_n\}$ 是向量空间 $\overset{\infty}{V}$ 在实数域上的基. 由这一基张成的平行体 $\overset{\infty}{D}$ (即满足 $0\le x\_v<1$ 的一切 $\overset{\infty}{\mathfrak{x}}\equiv\sum\_{v=1}^{n} x\_v\overset{\infty}{\omega}\_v$ 所成的集合) 在我们这套设置中自然的测度 $d\overset{\infty}{\mathfrak{x}}=\prod\_{\mathfrak p\in S\_{\infty}} d\mathfrak{x}\_{\mathfrak p}$ 之下具有体积 $\sqrt{\vert d\vert }$, 其中 $d=(\det(\omega\_i^{(j)}))^2$ 是 $k$ 的绝对判别式.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** $k$ 到 $\overset{\infty}{V}$ 的投影 $\xi\to\overset{\infty}{\xi}$ 正是经典地把数域嵌入 $n$ 维空间的办法. 读者会记得经典的论证, 它这样说: 

$$
k \text{ 可分} \Rightarrow d=(\det(\omega\_i^{(j)}))^2\ne 0
\Rightarrow \{\overset{\infty}{\omega}\_1,\overset{\infty}{\omega}\_2,\ldots,
\overset{\infty}{\omega}\_n\}
$$

 线性无关, 并且 (经过一个简单的行列式计算) $\overset{\infty}{D}$ 的体积为 $2^{-r\_2}\sqrt{\vert d\vert }$. 对我们而言体积是这个的 $2^{r\_2}$ 倍, 因为在复 $\mathfrak p$ 处我们选取的测度是复平面中通常测度的两倍.

</div>

<div class="tate-result qed-box" markdown="1">

**定义 4.1.2.** 加法基本域 $D\subset V$ 是一切满足 $\mathfrak{x}\in V\_{S\_{\infty}}$ 且 $\overset{\infty}{\mathfrak{x}}\in\overset{\infty}{D}$ 的 $\mathfrak{x}$ 所成的集合.

</div>

<div class="tate-result qed-box" markdown="1">

**定理 4.1.3.**

1.  $D$ 之所以得此名, 是因为 $V$ 中任一向量 $\mathfrak{x}$ 模域元素 $\xi$ 与 $D$ 中唯一一个向量同余. 换句话说, $V=\bigcup\_{\xi\in k}(\xi+D)$ 是不交并.

2.  $D$ 的测度为 $1$.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** (1) 从任意 $\mathfrak{x}\in V$ 出发, 通过加上一个模 $\mathfrak o$ 唯一的域元素 (引理 4.1.3), 我们可以把它变到 $V\_{S\_{\infty}}$ 中. 一旦进了 $V\_{S\_{\infty}}$, 我们可以找到一个唯一的 $\mathfrak o$ 中元素, 加上它之后仍然留在 $V\_{S\_{\infty}}$ 中, 并把各无穷分量调整到落在 $\overset{\infty}{D}$ 内 (引理 4.1.4).

\(2\) 为计算 $D$ 的测度, 注意 $D\subset V\_{S\_{\infty}}$ 且 $D=\overset{\infty}{D}\times V^{S\_{\infty}}$. 因此 

$$
\begin{aligned}
\int\_D d\mathfrak{x} &= \int\_D d\mathfrak{x}\_{S\_{\infty}}
= \int\_{\overset{\infty}{D}\times V^{S\_{\infty}}}d\overset{\infty}{\mathfrak{x}}\,
d\mathfrak{x}^{S\_{\infty}} = \int\_{\overset{\infty}{D}}d\overset{\infty}{\mathfrak{x}}\cdot
\int\_{V^{S\_{\infty}}}d\mathfrak{x}^{S\_{\infty}}\\
&= \sqrt{\vert d\vert }\prod\_{\mathfrak p\notin S}(N\mathfrak d\_{\mathfrak p})^{-\frac12}.
\end{aligned}
$$

 现在, 由于判别式 $d$ (作为理想) 是 $k$ 的绝对差积 $\mathfrak d$ 的范数, 并且 $\mathfrak d$ 是各局部差积 $\mathfrak d\_{\mathfrak p}$ 的乘积, 我们有 $\vert d\vert =\prod\_{\mathfrak p\in S\_{\infty}}(N\mathfrak d\_{\mathfrak p})$. 因此我们算出的测度为 $1$.

</div>

<div class="tate-result qed-box" markdown="1">

**推论 4.1.1.** $k$ 是 $V$ 的离散子群. 商群 $V\ \mathrm{mod}\ k$ 紧.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** $k$ 是离散的, 因为 $D$ 有内点. $V\ \mathrm{mod}\ k$ 是紧的, 因为 $D$ 相对紧.

</div>

<div class="tate-result qed-box" markdown="1">

**引理 4.1.5.** 对一切 $\xi\in k$ 有 $\Lambda(\xi)=0$.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 

$$
\Lambda(\xi) = \sum\_{\mathfrak p}\Lambda\_{\mathfrak p}(\xi)
= \sum\_{\mathfrak p}\lambda\_{p}(S\_{\mathfrak p}(\xi))
= \sum\_{p}\lambda\_{p}\left(\sum\_{\mathfrak p\vert p}S\_{\mathfrak p}(\xi)\right)
= \sum\_{p}\lambda\_{p}(S(\xi)),
$$

 因为“迹是各局部迹之和”. 由于 $S(\xi)$ 是有理数, 问题归结为证明对有理 $x$ 有 $\sum\_{p}\lambda\_{p}(x)\equiv 0\ (\mathrm{mod}\ 1)$. 为此我们注意, 有理数 $\sum\_{p}\lambda\_{p}(x)$ 关于每个固定的有理素数 $q$ 都是整的. 即 

$$
\sum\_{p}\lambda\_{p}(x) = \left(\sum\_{p\ne q,\,
p\nmid\infty}\lambda\_{p}(x)\right) + \lambda\_q(x)
+ \lambda\_{\infty}(x) \equiv \left(\sum\_{p\ne q,\,
p\nmid\infty}\lambda\_{p}(x)\right) + (\lambda\_q(x)-x)
$$

 把 $\sum\_{p}\lambda\_{p}(x)$ 表示成 $q$ 进整数之和.

</div>

<div class="tate-result qed-box" markdown="1">

**定理 4.1.4.** $k^\ast  = k$, 即对一切 $\xi$ 有 $\Lambda(\mathfrak{x}\xi)=0\Leftrightarrow \mathfrak{x}\in k$.
 (注: 此处 $k^\ast $ 是 $k$ 的对偶, 不是 $k$ 的乘法群 (!).)

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 由于 $k^\ast $ 是紧商群 $V\ \mathrm{mod}\ k$ 的特征群, $k^\ast $ 离散. 按前一个引理, $k^\ast $ 包含 $k$, 因此我们可以考虑商群 $k^\ast \ \mathrm{mod}\ k$. 作为紧群 $V\ \mathrm{mod}\ k$ 的离散子群, $k^\ast \ \mathrm{mod}\ k$ 是有限群. 但先验地显然 $k^\ast $ 是 $k$ 上的向量空间, 而 $k$ 不是有限域, 故指数 $(k^\ast :k)$ 不可能有限, 除非它等于 $1$.

</div>

### 4.2. Riemann--Roch 定理

若对一切 $\xi\in k$ 有 $\varphi(\mathfrak{x}+\xi)=\varphi(\mathfrak{x})$, 就称函数 $\varphi(\mathfrak{x})$ 是周期的. 周期函数以自然的方式表示紧商群 $V\ \mathrm{mod}\ k$ 上的一切函数. $\varphi(\mathfrak{x})$ 表示 $V\ \mathrm{mod}\ k$ 上的连续函数, 当且仅当它在 $V$ 上自身连续.

<div class="tate-result qed-box" markdown="1">

**引理 4.2.1.** 若 $\varphi(\mathfrak{x})$ 连续并且周期, 则 $\int\_D\varphi(\mathfrak{x})\,d\mathfrak{x}$ 等于:

> 在商群 $V\ \mathrm{mod}\ k$ 上, 对 $\varphi(\mathfrak{x})$ 所表示的函数所作的积分, 其中所用的测度是使整个群 $V\ \mathrm{mod}\ k$ 具有测度 $1$ 的那个 Haar 测度.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 定义 $I(\varphi)=\int\_D\varphi(\mathfrak{x})\,d\mathfrak{x}$, 并把它看成 $L(V\ \mathrm{mod}\ k)$ 上的泛函. 注意它具有刻画 Haar 积分的那些性质. (要检验平移不变性, 只需把 $D$ 拆成它与自身若干平移的交集的不交并.) 该泛函已归一化为 $1$, 因为 $\int\_D d\mathfrak{x}=1$.

</div>

由定理 4.1.4, $k$ 自然地是商群 $V\ \mathrm{mod}\ k$ 的特征群. 由 $\varphi(\mathfrak{x})$ 所表示的 $V\ \mathrm{mod}\ k$ 上连续函数的 Fourier 变换 $\widehat\varphi(\xi)$ 为 

$$
\widehat\varphi(\xi) = \int\_D \varphi(\mathfrak{x})\, e^{-2\pi i\Lambda(\xi\mathfrak{x})}\, d\mathfrak{x}.
$$



<div class="tate-result qed-box" markdown="1">

**引理 4.2.2.** 若 $\varphi(\mathfrak{x})$ 连续并且周期, 且 $\sum\_{\xi\in k} \vert \widehat\varphi(\xi)\vert <\infty$, 则 

$$
\varphi(\mathfrak{x}) = \sum\_{\xi\in k}\widehat\varphi(\xi)\, e^{2\pi i\Lambda(\mathfrak{x}\xi)}.
$$



</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 假设 $\sum\_{\xi\in k}\vert \widehat\varphi(\xi)\vert <\infty$ 意味着 Fourier 变换 $\widehat\varphi(\xi)$ 在 $k$ 上可和, 这保证反演公式成立. 所断言的等式不过是把反演公式显式写出来.

</div>

<div class="tate-result qed-box" markdown="1">

**引理 4.2.3.** 若 $f(\mathfrak{x})$ 连续, 属于 $L\_1(V)$, 并且 $\sum\_{\eta\in k}f(\mathfrak{x}+\eta)$ 对 $\mathfrak{x}\in D$ 一致收敛 (因为 $k$ 没有以任何方式排序, 这里的收敛指绝对收敛), 则由它们得到的连续周期函数 $\varphi(\mathfrak{x})=\sum\_{\eta\in k}f(\mathfrak{x}+\eta)$ 满足 $\widehat\varphi(\xi)=\widehat f(\xi)$.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 

$$
\begin{aligned}
\widehat\varphi(\xi) &= \int\_D\varphi(\mathfrak{x})\, e^{-2\pi i\Lambda(\xi\mathfrak{x})}\, d\mathfrak{x}\\
&= \int\_D \left(\sum\_{\eta\in k}f(\mathfrak{x}+\eta)\, e^{-2\pi i\Lambda(\mathfrak{x}\xi)}\right)
d\mathfrak{x}\\
&= \sum\_{\eta\in k}\int\_D f(\mathfrak{x}+\eta)\, e^{-2\pi i\Lambda(\mathfrak{x}\xi)}\, d\mathfrak{x}
\end{aligned}
$$

 (交换次序是允许的, 因为我们假设了在 $D$ 上一致收敛, 而 $D$ 的测度有限.) 

$$
\begin{aligned}
&= \sum\_{\eta\in k}\int\_{\eta+D}f(\mathfrak{x})\, e^{-2\pi i\Lambda(\mathfrak{x}\xi-\eta\xi)}\, d\mathfrak{x}\\
&= \sum\_{\eta\in k}\int\_{\eta+D}f(\mathfrak{x})\, e^{-2\pi i\Lambda(\mathfrak{x}\xi)}\, d\mathfrak{x}\\
\end{aligned}
$$

 (因为 $\Lambda(\eta\xi)=0$) 

$$
\begin{aligned}
&= \int f(\mathfrak{x})\, e^{-2\pi i\Lambda(\mathfrak{x}\xi)}\, d\mathfrak{x}\\
&= \widehat f(\xi).
\end{aligned}
$$



</div>

把最后两个引理 4.2.2 与 4.2.3 结合起来, 并在引理 4.2.2 的断言中令 $\mathfrak{x}=0$, 我们得到

<div class="tate-result qed-box" markdown="1">

**引理 4.2.4.** (Poisson 公式.) 若 $f(\mathfrak{x})$ 满足条件:

1.  $f(\mathfrak{x})$ 连续, 属于 $L\_1(V)$;

2.  $\sum\_{\xi\in k}f(\mathfrak{x}+\xi)$ 对 $\mathfrak{x}\in D$ 一致收敛;

3.  $\sum\_{\xi\in k}\vert \widehat f(\xi)\vert $ 收敛;

则 

$$
\sum\_{\xi\in k}\widehat f(\xi) = \sum\_{\xi\in k}f(\xi).
$$



</div>

若把 $f(\mathfrak{x})$ 换成 $f(a\mathfrak{x})$ ($a$ 为伊代尔), 我们得到一个可以看作 Riemann--Roch 定理在数论上的类比的定理.

<div class="tate-result qed-box" markdown="1">

**定理 4.2.1.** (Riemann--Roch 定理.) 若 $f(\mathfrak{x})$ 满足条件:

1.  $f(\mathfrak{x})$ 连续, 属于 $L\_1(V)$;

2.  对一切伊代尔 $a$ 与赋值向量 $\mathfrak{x}$, $\sum\_{\xi\in k}f(a(\mathfrak{x}+\xi))$ 收敛, 并且对 $\mathfrak{x}\in D$ 一致;

3.  对一切伊代尔 $a$, $\sum\_{\xi\in k}\vert \widehat f(a\xi)\vert $ 收敛;

则 

$$
\frac{1}{\vert a\vert }\sum\_{\xi\in k}\widehat f(\xi/a) = \sum\_{\xi\in k}f(a\xi).
$$



</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 函数 $g(\mathfrak{x})=f(a\mathfrak{x})$ 满足前一个引理的条件, 因为 

$$
\begin{aligned}
\widehat g(\mathfrak{x}) &= \int f(a\eta)\, e^{-2\pi i\Lambda(\mathfrak{x}\eta)}\, d\eta\\
&= \frac{1}{\vert a\vert }\int f(\eta)\, e^{-2\pi i\Lambda(\mathfrak{x}\eta/a)}\, d\eta .
\end{aligned}
$$

 (在代换 $\eta\to\eta/a$ 之下, $d\eta\to(1/\vert a\vert )\,d\eta$.) 

$$
= \frac{1}{\vert a\vert }\widehat f(\mathfrak{x}/a).
$$

 因此我们可以断定 

$$
\sum\_{\xi\in k}\widehat g(\xi) = \sum\_{\xi\in k}g(\xi);
$$

 也就是说, 

$$
\frac{1}{\vert a\vert }\sum\_{\xi\in k}\widehat f(\xi/a) = \sum\_{\xi\in k}f(a\xi).
$$



</div>

有一件事颇有趣味, 值得指出: 假如我们当初始终没有费心去计算 $D$ 的精确测度, 现在我们也会知道它是 $1$. 因为本节的全部论证都可以用一个未知的测度 $\mu(D)$ 来代替 $D$ 的测度来做. 唯一的改变是: 为使引理 4.2.2 的反演公式成立, 我们必须给 $k$ 的每个元素以权 $1/\mu(D)$. 于是 Poisson 公式将写成 

$$
\frac{1}{\mu(D)}\sum\_{\xi\in k}\widehat f(\xi) = \sum\_{\xi\in k}f(\xi).
$$

 把它再施行一次就得到 $(\mu(D))^2=1$, 从而 $\mu(D)=1$!

### 4.3. 乘法理论

本节中我们讨论伊代尔乘法群的基本特征.

<div class="tate-result qed-box" markdown="1">

**定义 4.3.1.** 伊代尔的乘法群 $I$ 是诸群 $k\_{\mathfrak p}^\ast $ 相对于诸子群 $u\_{\mathfrak p}$ 的受限直积.

</div>

我们用 $a=(\ldots,a\_{\mathfrak p},\ldots)$ 表示一般的伊代尔. 伊代尔这个名称之所以如此, 至少部分地可以由如下事实来解释: 伊代尔群可以看作 $k$ 的理想群的精细化. 因为若把一个理想 $\varphi(a)=\prod\_{\mathfrak p\notin S\_{\infty}}\mathfrak p^{\operatorname{ord}\_{\mathfrak p}a\_{\mathfrak p}}$ 与伊代尔 $a$ 相联系, 则映射 $a\to\varphi(a)$ 显然是伊代尔群到 $k$ 的离散理想群上的连续同态. 由于这个同态的核是 $I\_{S\_{\infty}}$, 我们可以说伊代尔在两方面是理想的精细化. 第一, Archimedean 素点出现在它的构成中; 第二, 它把离散素点处的单位也考虑进去了.

关于 $I$ 的拟特征, 按第 3.2 节我们只能说: 一般拟特征 $c(a)$ 具有形式 $c(a)=\prod\_{\mathfrak p}c\_{\mathfrak p}(a\_{\mathfrak p})$, 其中 $c\_{\mathfrak p}(a\_{\mathfrak p})$ 是局部拟特征 (第 2.3 节已描述过), 并且对几乎所有 $\mathfrak p$, $c\_{\mathfrak p}(a\_{\mathfrak p})$ 是非分歧的.

至于 $I$ 上的测度 $\mathrm{d}a$, 我们当然选取 $\mathrm{d}a=\prod\_{\mathfrak p}\mathrm{d}a\_{\mathfrak p}$, 其中 $\mathrm{d}a\_{\mathfrak p}$ 是第 2.3 节中定义的局部乘法测度.

在把 $k$ 的乘法群 $k^\ast $ 嵌入伊代尔群之前, 我们对伊代尔群做不了任何真正有意义的事情, 嵌入的办法是把元素 $\alpha\in k^\ast $ 与伊代尔 $\alpha=(\alpha,\alpha,\ldots,\alpha,\ldots)$ 等同起来. 本节余下的讨论都围绕 $I$ 相对于子群 $k^\ast $ 的结构进行. 首先要注意到的事实是: 与伊代尔 $\alpha\in k^\ast $ 相联系的理想 $\varphi(\alpha)$ 就是 $\alpha$ 生成的主理想 $\alpha\mathfrak o$, 这是理所当然的. 其次我们有对元素 $\alpha\in k^\ast $ 的“乘积公式”. 虽然这是熟知的, 我们还是把它正式陈述为一条定理, 以便给出一个有趣的证明.

<div class="tate-result qed-box" markdown="1">

**定理 4.3.1.** 对 $\alpha\in k^\ast $ 有 $\vert \alpha\vert \ \left(=\prod\_{\mathfrak p}\vert \alpha\vert \_{\mathfrak p}\right)=1$.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 按引理 4.1.2, $\alpha D$ 的 (加法) 测度是 $D$ 的测度的 $\vert \alpha\vert $ 倍. 由于 $\alpha k^+=k^+$, $\alpha D$ 与 $D$ 一样可以作为加法基本域. 由此直观上清楚 $\alpha D$ 与 $D$ 的测度相同, 从而 $\vert \alpha\vert =1$. 要作形式证明, 只需把 $D$ 与 $\alpha D$ 分别剖分成一些同余的片段, 其形状分别为 $D\cap(\xi+\alpha D)$ 与 $(-\xi+D)\cap\alpha D$, 其中 $\xi$ 取遍 $k$.

</div>

这一定理提醒我们明确提及连续同态 $\alpha\to\vert \alpha\vert =\prod\_{\mathfrak p}\vert \alpha\vert \_{\mathfrak p}$, 它是 $I$ 到正实数乘法群上的映射. 它的核是 $I$ 的一个闭子群, 将起重要作用. 我们用 $J$ 记这个子群, 用 $b$ 记它的一般元素 (即绝对值为 $1$ 的伊代尔).

选取 $I$ 的一个子群 $T$, 使得可以写 $I=T\times J$ (直积), 这样做是方便的 (虽然在审美上有点别扭, 而且并非真正必要). 为此我们从 $k$ 的 Archimedean 素点中随便挑一个, 记作 $\mathfrak p\_0$, 令 $T$ 为一切满足 $a\_{\mathfrak p\_0}>0$ 且对 $\mathfrak p\ne\mathfrak p\_0$ 有 $a\_{\mathfrak p}=1$ 的伊代尔 $a$ 所成的子群. 这样的伊代尔显然由它的绝对值唯一确定; 事实上, 把映射 $a\to\vert a\vert $ 限制在 $T$ 上, 它是 $T$ 与正实数乘法群之间的同构. 因此, 如果简单地用伊代尔的绝对值这个实数来记 $T$ 中的伊代尔, 不会引起混淆. 于是实数 $t>0$ 也可以表示伊代尔 $(t,1,1,\ldots)$ 或伊代尔 $(\sqrt t,1,1,\ldots)$, 依 $\mathfrak p\_0$ 是实的还是复的而定, 只要我们把 $\mathfrak p\_0$ 分量写在最前面. 由于任一伊代尔 $a$ 都可以唯一地写成 $a=\vert a\vert \cdot b$, 其中 $\vert a\vert \in T$, $b=a\vert a\vert ^{-1}\in J$, 所以很清楚 $I=T\times J$ (直积).

为在 $J$ 上选定一个固定的测度 $\mathrm{d}b$, 我们在 $T$ 上取测度 $\mathrm{d}t=\mathrm{d}t/t$ 并要求 $\mathrm{d}a=\mathrm{d}t\cdot \mathrm{d}b$. 于是为计算方便, 我们有 (在 Fubini 的意义下) 公式 

$$
\int\_I f(a)\, \mathrm{d}a = \int\_0^{\infty}\left[\int\_J f(tb)\, \mathrm{d}b\right]\frac{\mathrm{d}t}{t}
= \int\_J\left[\int\_0^{\infty}f(tb)\,\frac{\mathrm{d}t}{t}\right]\, \mathrm{d}b
$$

 对可和的伊代尔函数 $f(a)$ 成立.

乘积公式意味着 $k^\ast \subset J$, 我们现在想描述 $J\ \mathrm{mod}\ k^\ast $ 的一个“基本域”. 把伊代尔映到理想的映射使我们能下降到子群 $J\_{S\_{\infty}}=J\cap I\_{S\_{\infty}}$. 为研究 $J\_{S\_{\infty}}$, 我们把伊代尔 $b\in J\_{S\_{\infty}}$ 映到向量 $l(b)=(\ldots,\log\vert b\vert \_{\mathfrak p},\ldots)\_{\mathfrak p\in S'\_{\infty}}$, 它除 $\mathfrak p\_0$ 外对每个 Archimedean 素点有一个分量 $\log\vert b\vert \_{\mathfrak p}$. (这 $r=r\_1+r\_2-1$ 个素点所成的集合记作 $S'\_{\infty}$.) 显然映射 $b\to l(b)$ 是 $J\_{S\_{\infty}}$ 到欧氏 $r$ 空间的加法群上的连续同态. 满射性来自如下事实: 虽然伊代尔 $b\in J\_{S\_{\infty}}$ 的无穷分量受条件 $\prod\_{\mathfrak p}\vert b\vert \_{\mathfrak p}=\prod\_{\mathfrak p\in S\_{\infty}} \vert b\vert \_{\mathfrak p}=1$ 的约束, 它们在集合 $S'\_{\infty}$ 中却是完全自由的, 因为我们可以调整 $\mathfrak p\_0$ 分量.

$k^\ast \cap J\_{S\_{\infty}}$ 是一切在有限素点处为单位的元素 $\varepsilon\in k^\ast $ 所成的群, 即在环 $\mathfrak o$ 中为单位的那些元素. 满足 $l(\zeta)=0$ 的单位 $\zeta$ 是 $k$ 中的单位根, 构成一个有限循环群. 经典地证明了: 单位 $\varepsilon$ 所成的群模去单位根 $\zeta$ 所成的群之后, 是秩为 $r$ 的自由阿贝尔群. 这个证明是通过如下方式完成的: 证明单位的像 $l(\varepsilon)$ 在 $r$ 空间中构成一个最高维的格.

因此, 若 $\{\varepsilon\_i\}\_{1\le i\le r}$ 是单位群模去单位根之后的一组基, 则向量 $l(\varepsilon\_i)$ 是 $r$ 空间在实数域上的一组基, 于是对任意 $b\in J\_{S\_{\infty}}$ 可以写 

$$
l(b) = \sum\_{v=1}^{r}x\_v\, l(\varepsilon\_v),
$$

 其中实数 $x\_v$ 唯一. 用 $P$ 表示由向量 $l(\varepsilon\_i)$ 在 $r$ 空间中张成的平行体, 即满足 $0\le x\_v<1$ 的一切向量 $\sum\_{v=1}^{r}x\_v l(\varepsilon\_v)$ 所成的集合. 用 $Q$ 表示 $r$ 空间中的“单位立方体”, 即满足 $0\le x\_{\mathfrak p}<1$ 的一切向量 $(\ldots,x\_{\mathfrak p},\ldots)\_{\mathfrak p\in S'\_{\infty}}$ 所成的集合.

<div class="tate-result qed-box" markdown="1">

**引理 4.3.1.** 

$$
\int\_{l^{-1}(P)}\mathrm{d}b = \frac{2^{r\_1}(2\pi)^{r\_2}}{\sqrt{\vert d\vert }}\,R,
$$

 其中 $l^{-1}(P)$ 是一切满足 $l(b)\in P$ 的 $b\in J\_{S\_{\infty}}$ 所成的集合, 而 

$$
R = \pm\det\left(\log\vert \varepsilon\_i\vert \_{\mathfrak p}\right)\_{\substack{1\le i\le
r\\ \mathfrak p\in S'\_{\infty}}}
$$

 是 $k$ 的调节子.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 因为 $l$ 是同态, 

$$
\frac{l^{-1}(P)\text{ 的测度}}{l^{-1}(Q)\text{ 的测度}}
= \frac{P\text{ 的体积}}{Q\text{ 的体积}}
= \pm\det(\log\vert \varepsilon\_i\vert \_{\mathfrak p}) = R,
$$

 所以我们只需证明 

$$
\int\_{l^{-1}(Q)}\mathrm{d}b = \frac{2^{r\_1}(2\pi)^{r\_2}}{\sqrt{\vert d\vert }}.
$$

 $l^{-1}(Q)$ 是一切满足对 $\mathfrak p\in S'\_{\infty}$ 有 $1\le\vert b\vert \_{\mathfrak p}<e$ 的 $b\in J\_{S\_{\infty}}$ 所成的集合. 设 $Q^\ast $ 是一切满足对 $\mathfrak p\in S\_{\infty}$ 有 $1\le\vert a\vert \_{\mathfrak p}<e$ 的 $a\in I\_{S\_{\infty}}$ 所成的集合. 那么 

$$
\begin{aligned}
\int\_{Q^\ast }\mathrm{d}a &= \int\_J\left[\int\_{tb\in Q^\ast }\frac{\mathrm{d}t}{t}\right]\mathrm{d}b
= \int\_{l^{-1}(Q)}\left[\int\_{\vert b\vert \_{\mathfrak p\_0}^{-1}}^{e\vert b\vert \_{\mathfrak p\_0}^{-1}}
\frac{\mathrm{d}t}{t}\right]\mathrm{d}b = \int\_{l^{-1}(Q)}\mathrm{d}b,
\end{aligned}
$$

 因为 $tb\in Q^\ast \Leftrightarrow b\in l^{-1}(Q)$ 且 $1\le\vert tb\vert \_{\mathfrak p\_0}<e$. 因此我们只需证明 

$$
\int\_{Q^\ast }\mathrm{d}a = \frac{2^{r\_1}(2\pi)^{r\_2}}{\sqrt{\vert d\vert }}.
$$

 把 $Q^\ast $ 写成笛卡儿积 $Q^\ast =\prod\_{\mathfrak p\in S\_{\infty}} Q\_{\mathfrak p}^\ast \times I^{S\_{\infty}}$, 其中对 $\mathfrak p\in S\_{\infty}$, $Q\_{\mathfrak p}^\ast $ 是满足 $1\le\vert a\_{\mathfrak p}\vert \_{\mathfrak p}<e$ 的一切 $a\_{\mathfrak p}\in k\_{\mathfrak p}^\ast $ 所成的集合. 那么 

$$
\int\_{Q^\ast }\mathrm{d}a = \prod\_{\mathfrak p\in S\_{\infty}}\int\_{Q\_{\mathfrak p}^\ast }\mathrm{d}a\_{\mathfrak p}
\cdot\int\_{I^{S\_{\infty}}}\mathrm{d}a^{S\_{\infty}}
= \frac{2^{r\_1}(2\pi)^{r\_2}}{\sqrt{\vert d\vert }},
$$

 因为对实 $\mathfrak p$, 

$$
\int\_{Q\_{\mathfrak p}^\ast }\mathrm{d}a\_{\mathfrak p}
= \left[\int\_{-e}^{-1}+\int\_1^{e}\right]\frac{dx}{\vert x\vert }
= 2\int\_1^{e}\frac{dx}{x} = 2,
$$

 对复 $\mathfrak p$, 

$$
\int\_{Q\_{\mathfrak p}^\ast }\mathrm{d}a\_{\mathfrak p}
= \int\_0^{2\pi}\!\!\int\_1^{\sqrt e}\frac{2\,dr\,d\theta}{r} = 2\pi,
$$

 并且 

$$
\int\_{I^{S\_{\infty}}}\mathrm{d}a^{S\_{\infty}}
= \prod\_{\mathfrak p\notin S\_{\infty}}\int\_{u\_{\mathfrak p}}\mathrm{d}a\_{\mathfrak p}
= \prod\_{\mathfrak p\notin S\_{\infty}}
(N\mathfrak d\_{\mathfrak p})^{-\frac12}
= \frac{1}{\sqrt{\vert d\vert }}.
$$



</div>

<div class="tate-result qed-box" markdown="1">

**定义 4.3.2.** 设 $h$ 是 $k$ 的类数, 并选取伊代尔 $b^{(1)},\ldots,b^{(h)}\in J$, 使对应的理想 $\varphi(b^{(1)}),\ldots,\varphi(b^{(h)})$ 代表不同的理想类. 设 $w$ 是 $k$ 中单位根的个数. 设 $E\_0$ 是一切满足 $0\le\arg b\_{\mathfrak p\_0}<\dfrac{2\pi}{w}$ 的 $b\in l^{-1}(P)$ (见前一个引理) 所成的子集. 我们定义 $J\ \mathrm{mod}\ k^\ast $ 的乘法基本域 $E$ 为 

$$
E = E\_0b^{(1)}\cup E\_0b^{(2)}\cup\ldots\cup E\_0b^{(h)}.
$$



</div>

<div class="tate-result qed-box" markdown="1">

**定理 4.3.2.**

1.  $J=\bigcup\_\alpha\alpha E$ 是不交并.

2.  $\displaystyle \int\_E \mathrm{d}b=\frac{2^{r\_1}(2\pi)^{r\_2}hR}{\sqrt{\vert d\vert }\,w}$.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** (1) 从任意伊代尔 $b\in J$ 出发, 把它除以一个唯一确定的 $b^{(i)}$, 就可以把它变成一个表示主理想的伊代尔. 若这个主理想是 $\alpha\mathfrak o$ ($\alpha$ 模单位唯一确定), 则乘以 $\alpha^{-1}$ 就把我们带到表示理想 $\mathfrak o$ 的 $J$ 中伊代尔, 从而进入 $J\_{S\_{\infty}}$. 一旦进了 $J\_{S\_{\infty}}$, 我们可以找到基本单位 $\varepsilon\_i$ 的唯一的幂积, 把我们带到 $l^{-1}(P)$ 中, 此时手中只有一个单位根 $\zeta$. 这个 $\zeta$ 正是我们所需要的, 用来把 $\mathfrak p\_0$ 分量的辐角调整到区间 $\left(0,\frac{2\pi}{w}\right)$ 内. 于是我们就落在 $E\_0$ 中了! 对原来的伊代尔 $b$, 我们找到了唯一的 $\beta\in k^\ast $ 和唯一的 $b^{(i)}$, 使 $b\in\beta b^{(i)}E\_0$.

\(2\) 按两个不交分解 

$$
E = \bigcup\_{v=1}^{h}b^{(v)}E\_0,\qquad
l^{-1}(P) = \bigcup\_\zeta \zeta E\_0
$$

 以及前一个引理, 有 $(\text{$E$ 的测度})=h\cdot(\text{$E_0$ 的测度})=\frac{h}{w}\cdot(\text{$l^{-1}(P)$ 的测度}) =\frac{2^{r\_1}(2\pi)^{r\_2}hR}{\sqrt{\vert d\vert }\,w}$.

</div>

<div class="tate-result qed-box" markdown="1">

**推论 4.3.1.** $k^\ast $ 是 $J$ (从而也是 $I$) 的离散子群. $J\ \mathrm{mod}\ k^\ast $ 紧.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 容易看出 $E$ 在 $J$ 中有内点. 另一方面, $E$ 含于一个紧集之中.

</div>

我们真正关心的并不是 $I$ 的全部拟特征, 而只是那些在 $k^\ast $ 上平凡的拟特征. 今后我们说“拟特征”时, 指的总是这一类. 我们以关于这些拟特征的几点说明来结束对伊代尔群的介绍.

首先要注意到的是: 在子群 $J$ 上, 拟特征就是特征, 即对一切 $b\in J$ 有 $\vert c(b)\vert =1$, 因为 $J\ \mathrm{mod}\ k^\ast $ 紧.

其次我们指出, 在 $J$ 上平凡的拟特征恰是形如 $c(a)=\vert a\vert ^s$ 的那些, 其中 $s$ 是由 $c(a)$ 唯一确定的复数. 因为若 $c(a)$ 在 $J$ 上平凡, 则 $c(a)$ 只依赖于 $\vert a\vert $, 而在这种依赖中, 它是正实数到复数的一个连续乘法映射. 众所周知这样的映射具有 $t\to t^s$ 的形式.

对每个拟特征 $c(a)$, 存在唯一的实数 $\sigma$ 使 $\vert c(a)\vert =\vert a\vert ^\sigma$. 因为 $\vert c(a)\vert $ 是一个在 $J$ 上平凡的拟特征. 因此对某个复数 $s$ 有 $\vert c(a)\vert =\vert a\vert ^s$. 由于 $\vert c(a)\vert >0$, $s$ 是实的. 我们称 $\sigma$ 为 $c$ 的指数. 一个拟特征是特征, 当且仅当它的指数为 $0$.

### 4.4. $\zeta$ 函数, 函数方程

本节中 $f(\mathfrak{x})$ 表示赋值向量的一个复值函数, $f(a)$ 表示它在伊代尔上的限制. 用 $\mathfrak z$ 表示满足以下三个条件的全部函数 $f(\mathfrak{x})$ 所成的类:


$f(\mathfrak{x})$ 与 $\widehat f(\mathfrak{x})$ 连续, 属于 $L\_1(V)$, 即 $f(\mathfrak{x})\in\mathfrak B\_1(V)$.

对每个伊代尔 $a$ 与向量 $\mathfrak{x}$, $\sum\_{\xi\in k}f(a(\mathfrak{x}+\xi))$ 与 $\sum\_{\xi\in k}\widehat f(a(\mathfrak{x}+\xi))$ 都收敛, 并且这种收敛关于对 $(a,\mathfrak{x})$ 一致, 其中 $\mathfrak{x}$ 取遍 $D$, $a$ 取遍 $I$ 的任一固定紧子集.

对 $\sigma>1$, $f(a)\cdot\vert a\vert ^\sigma$ 与 $\widehat f(a)\vert a\vert ^\sigma$ 属于 $L\_1(I)$.

(注意若 $f(\mathfrak{x})$ 在 $V$ 上连续, 则更有理由 $f(a)$ 在 $I$ 上连续, 因为我们在 $I$ 中采用的拓扑比 $I$ 作为 $V$ 的子空间所得到的拓扑更强.)

鉴于 $(\mathfrak z\_1)$ 与 $(\mathfrak z\_2)$, Riemann--Roch 定理对 $\mathfrak z$ 中的函数成立. $(\mathfrak z\_3)$ 的用处在于使我们能用它们定义 $\zeta$ 函数:

<div class="tate-result qed-box" markdown="1">

**定义 4.4.1.** 对每个 $f\in\mathfrak z$, 我们引进一个与拟特征相联系的函数 $\zeta(f,c)$, 它对一切指数大于 $1$ 的拟特征 $c$ 定义, 由 

$$
\zeta(f,c) = \int f(a)\, c(a)\, \mathrm{d}a
$$

 给出. 我们称这样的函数为 $k$ 的 $\zeta$ 函数.

</div>

记住我们现在只考虑那些在 $k^\ast $ 上平凡的拟特征. 这些已在上一节末尾讨论过, 那里解释了“指数”这个概念. 若两个拟特征在 $J$ 上一致, 就称它们等价; 那么一个拟特征的等价类由一切形如 $c(a)=c\_0(a)\vert a\vert ^s$ 的拟特征组成, 其中 $c\_0(a)$ 是该类的一个固定代表, $s$ 是由 $c$ 唯一确定的复数. 用复变量 $s$ 作这样的参数化, 使我们能把拟特征的一个等价类看成一个 Riemann 曲面, 正如我们在局部理论中所做的那样 (参看第 2.4 节). 由 $\zeta$ 函数作为积分的定义显然可知, 它们在一切指数大于 $1$ 的拟特征的域中是正则的 (参看相应的局部引理). 至于解析延拓呢????

<div class="tate-result qed-box" markdown="1">

**主要定理 4.4.1.** [(解析延拓与 $\zeta$ 函数的函数方程.)]{.upright}  通过解析延拓, 我们可以把任一 $\zeta$ 函数 $\zeta(f,c)$ 的定义扩充到全部拟特征的域上. 扩充后的函数单值而且正则, 除 $c(a)=1$ 与 $c(a)=\vert a\vert $ 两处之外; 在这两处它有单极点, 留数分别为 $-\kappa f(0)$ 与 $+\kappa\widehat f(0)$, 其中 $\kappa=2^{r\_1}(2\pi)^{r\_2}hR/(\sqrt{\vert d\vert }w)$ 是乘法基本域的体积. $\zeta(f,c)$ 满足函数方程 

$$
\zeta(f,c) = \zeta(\widehat f,\widehat c),
$$

 其中 $\widehat c(a)=\vert a\vert c^{-1}(a)$, 与局部理论中相同.

</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 对指数大于 $1$ 的 $c$ 我们有 

$$
\zeta(f,c) = \int f(a)\,c(a)\,\mathrm{d}a
= \int\_0^{\infty}\left[\int\_J f(tb)\,c(tb)\,\mathrm{d}b\right]\frac{\mathrm{d}t}{t}
= \int\_0^{\infty}\zeta\_t(f,c)\,\frac{\mathrm{d}t}{t}, \quad \text{记作}.
$$

 这里 

$$
\zeta\_t(f,c) = \int\_J f(tb)\,c(tb)\,\mathrm{d}b
$$

 对任意指数的 $c$ 都绝对收敛, 至少对几乎所有 $t$ 如此, 因为对某个 $c$ 它收敛, 而 $\vert c(tb)\vert =t^{c\text{ 的指数}}$ 在 $b\in J$ 上为常数. 我们证明的关键一步在于用 Riemann--Roch 定理为 $\zeta\_t(f,c)$ 建立一条函数方程:

</div>

<div class="tate-result qed-box" markdown="1">

**引理 A.** 对一切拟特征 $c$ 有 

$$
\zeta\_t(f,c) + f(0)\int\_E c(tb)\,\mathrm{d}b
= \zeta\_{1/t}(\widehat f,\widehat c) + \widehat f(0)\int\_E\widehat c\left(\frac{1}{t}b\right)\mathrm{d}b.
$$



</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 

$$
\zeta\_t(f,c) + f(0)\int\_E c(tb)\,\mathrm{d}b
= \sum\_{\alpha\in k^\ast }\int\_{\alpha E}f(tb)c(tb)\,\mathrm{d}b + f(0)\int\_E c(tb)\,\mathrm{d}b
$$

 (因为 $J=\bigcup\_\alpha\alpha E$ 是不交并) 

$$
= \sum\_{\alpha\in k^\ast }\int\_E f(\alpha tb)c(tb)\,\mathrm{d}b + f(0)\int\_E c(tb)\,\mathrm{d}b
$$

 ($d(\alpha b)=\mathrm{d}b$; $c(\alpha tb)=c(tb)$) 

$$
= \int\_E\left[\sum\_{\alpha\in k^\ast }f(\alpha tb)\right]c(tb)\,\mathrm{d}b
+ \int\_E f(0)c(tb)\,\mathrm{d}b .
$$

 (按 $f$ 的假设 $(\mathfrak z\_2)$, 该和对相对紧子集 $E$ 中的 $b$ 一致收敛) 

$$
\begin{aligned}
&= \int\_E\left[\sum\_{\xi\in k}f(\xi tb)\right]c(tb)\,\mathrm{d}b\\
&= \int\_E\left[\sum\_{\xi\in k}\widehat f\left(\frac{\xi}{tb}\right)\right]
\frac{1}{\vert tb\vert }\,c(tb)\,\mathrm{d}b
\end{aligned}
$$

 (Riemann--Roch 定理 4.2.1) 

$$
= \int\_E\left[\sum\_{\xi\in k}\widehat f\left(\xi\frac{1}{t}b\right)
\right]\widehat c\left(\frac{1}{t}b\right)\,\mathrm{d}b
$$

 ($b\to 1/b$; $\mathrm{d}b\to \mathrm{d}b$).

</div>

把步骤倒过来就完成了证明.

<div class="tate-result qed-box" markdown="1">

**引理 B.** 

$$
\int\_E c(tb)\,\mathrm{d}b = \begin{cases}
\kappa t^s, & \text{若 } c(a)=\vert a\vert ^s,\\
0, & \text{若 } c(a) \text{ 在 } J \text{ 上不平凡}.
\end{cases}
$$



</div>

<div class="tate-proof qed-box" markdown="1">

**证明.** 

$$
\int\_E c(tb)\,\mathrm{d}b = c(t)\int\_E c(b)\,\mathrm{d}b .
$$

 这里 $\int\_E c(b)\,\mathrm{d}b$ 是商群 $J\ \mathrm{mod}\ k^\ast $ 上对 $c(b)$ 所表示的特征的积分. 因此它等于 $\kappa$ ($E$ 的测度), 或 $0$, 依 $c(a)$ 在 $J$ 上是否平凡而定. 在前一种情形我们须注意 $c(t)=\vert t\vert ^s=t^s$.

</div>

为证明定理, 对指数大于 $1$ 的 $c$ 写下 

$$
\zeta(f,c) = \int\_0^{\infty}\zeta\_t(f,c)\,\frac{\mathrm{d}t}{t}
= \int\_0^{1}\zeta\_t(f,c)\,\frac{\mathrm{d}t}{t}
+ \int\_1^{\infty}\zeta\_t(f,c)\,\frac{\mathrm{d}t}{t}.
$$

 $\int\_1^{\infty}$ 这一项没有问题. 因为它等于 $f(a)\,c(a)\,\mathrm{d}a$ 在 $I$ 中 $\vert a\vert \ge 1$ 的那一半上的积分. 因此 $c$ 的指数越小, 它收敛得越好; 而既然它对指数大于 $1$ 的 $c$ 收敛, 它对一切 $c$ 都必须收敛. 现在的关键在于, 我们可以用引理 A (以及辅助的引理 B) 把 $\int\_0^{1}$ 变换成 $\int\_1^{\infty}$, 从而得到 $\zeta(f,c)$ 的一个对一切 $c$ 都适用的解析表达式. 即: 

$$
\int\_0^{1}\zeta\_t(f,c)\,\frac{\mathrm{d}t}{t}
= \int\_0^{1}\zeta\_{1/t}(\widehat f,\widehat c)\,\frac{\mathrm{d}t}{t}
+ \left\{\left\{\int\_0^{1}\kappa\widehat f(0)\left(\frac{1}{t}\right)^{1-s}
\frac{\mathrm{d}t}{t} - \int\_0^{1}\kappa f(0)\,t^s\frac{\mathrm{d}t}{t}\right\}\right\},
$$

 其中表达式 $\{\{\ldots\}\}$ 只在 $c$ 于 $J$ 上平凡时才计入, 此时我们设 $c(a)=\vert a\vert ^s$. 我们仍然只看指数大于 $1$ 的 $c$. 若 $c(a)=\vert a\vert ^s$, 这意味着 $\operatorname{Re}(s)>1$, 这正是双括号下的辅助积分有意义所需要的. 把它们算出来, 并在表达式的主要部分作代换 $t\to 1/t$, 我们得到 

$$
\int\_0^{1}\zeta\_t(f,c)\,\frac{\mathrm{d}t}{t}
= \int\_1^{\infty}\zeta\_t(\widehat f,\widehat c)\,\frac{\mathrm{d}t}{t}
+ \left\{\left\{\frac{\kappa\widehat f(0)}{s-1} - \frac{\kappa f(0)}{s}
\right\}\right\},
$$

 因此 

$$
\zeta(f,c) = \int\_1^{\infty}\zeta\_t(f,c)\,\frac{\mathrm{d}t}{t}
+ \int\_1^{\infty}\zeta\_t(\widehat f,\widehat c)\,\frac{\mathrm{d}t}{t}
+ \left\{\left\{\frac{\kappa\widehat f(0)}{s-1} - \frac{\kappa f(0)}{s}
\right\}\right\}.
$$

 两个积分对一切 $c$ 都解析. 因此这个表达式给出了 $\zeta(f,c)$ 到全部拟特征的域上的解析延拓. 由它可以直接读出极点和留数. 注意到对 $c(a)=\vert a\vert ^s$ 有 $\widehat c(a)=\vert a\vert ^{1-s}$, 我们看到甚至在代换 $(f,c)\to(\widehat f,\widehat c)$ 下, 表达式的形式也不变. 因此函数方程 

$$
\zeta(f,c) = \zeta(\widehat f,\widehat c)
$$

 成立. 主要定理证毕!

### 4.5. 与经典理论的比较

现在我们要说明, 我们的理论并非空洞无物, 因为确实存在非平凡的 $\zeta$ 函数. 事实上, 我们将对拟特征的每个等价类 $C$ 具体给出一个函数 $f\in\mathfrak z$, 使相应的 $\zeta$ 函数 $\zeta(f,c)$ 在 $C$ 上非平凡. 这些特殊的 $\zeta$ 函数将表明本质上就是经典的 $\zeta$ 函数与 L 级数. 我们的 $\zeta$ 函数的解析延拓与函数方程, 将给出经典函数的解析延拓与函数方程.

我们可以仿照第 2.5 节中计算特殊局部 $\zeta$ 函数的办法来展开讨论. 那里我们处理了 $k$ 实, $k$ 复, $k$ 为 $\mathfrak p$ 进三种情形. 现在我们处理

大范围的 $k$!

**拟特征的等价类.** 按第 4.3 节末尾的说明, 拟特征的每个类都可以用一个特征来代表. 为详细描述这些特征, 我们取定一个任意的, 但固定的有限素点集 $S$ (至少包含一切 Archimedean 素点), 并讨论那些在 $S$ 之外非分歧的特征. 这样的特征不过是局部特征 $c\_{\mathfrak p}$ 的乘积 

$$
c(a) = \prod\_{\mathfrak p}c\_{\mathfrak p}(a\_{\mathfrak p}),
$$

 满足以下两个条件:

1.  $c\_{\mathfrak p}$ 在 $S$ 之外非分歧.

2.  对 $\alpha\in k^\ast $ 有 $\prod\_{\mathfrak p}c\_{\mathfrak p}(\alpha)=1$.

为构造这样的特征并以更具体的方式表达它们, 我们对 $\mathfrak p\in S$ 写 

$$
c\_{\mathfrak p}(a\_{\mathfrak p}) = \tilde c\_{\mathfrak p}(\tilde a\_{\mathfrak p})
\vert a\_{\mathfrak p}\vert \_{\mathfrak p}^{it\_{\mathfrak p}},
$$

 其中 $\tilde c\_{\mathfrak p}$ 是 $u\_{\mathfrak p}$ 的特征, $t\_{\mathfrak p}$ 是实数 (参看定理 2.3.1). 对 $\mathfrak p\notin S$, 我们把各局部特征并成一个特征, 记作 

$$
c^\ast (a) = \prod\_{\mathfrak p\notin S}c\_{\mathfrak p}(a\_{\mathfrak p}),
$$

 并把 $c^\ast $ 解释为来自一个理想特征. 即: 映射 

$$
a\to\varphi\_S(a) = \prod\_{\mathfrak p\notin S}\mathfrak p^{\operatorname{ord}
\_{\mathfrak p}a}
$$

 是伊代尔群到与 $S$ 互素的理想所成的乘法群上的同态. 它的核是 $I\_S$. $c^\ast (a)$ 在 $I\_S$ 上是恒等映射. 因此我们有 

$$
c^\ast (a) = \chi(\varphi\_S(a)),
$$

 其中 $\chi$ 是与 $S$ 互素的理想群的某个特征. 于是我们的特征 $c(a)$ 现在可以写成 

$$
c(a) = \prod\_{\mathfrak p\in S}\tilde c\_{\mathfrak p}(\tilde a\_{\mathfrak p})
\cdot\prod\_{\mathfrak p\in S}\vert a\_{\mathfrak p}\vert \_{\mathfrak p}^{it\_{\mathfrak p}}
\cdot\chi(\varphi\_S(a)).
$$

 为构造这样的特征, 我们必须选取 $\tilde c\_{\mathfrak p}$, $t\_{\mathfrak p}$ 与 $\chi$, 使得对 $\alpha\in k^\ast $ 有 $c(\alpha)=1$. 为此我们先看 $k$ 的 $S$ 单位 $\varepsilon$, 即 $k^\ast \cap I\_S$ 中满足 $\varphi\_S(\varepsilon)=\mathfrak o$ 的那些元素. 设 $S$ 包含 $m+1$ 个素点; 设 $\varepsilon\_0$ 是 $k$ 中一个本原单位根, $\{\varepsilon\_1,\varepsilon\_2,\ldots,\varepsilon\_m\}$ 是 $S$ 单位群模单位根所成的自由阿贝尔群的一组基. 于是 $c(a)$ 在 $S$ 单位上平凡, 其充要条件是 $c(\varepsilon\_v)=1$, $0\le v\le m$. 条件 $c(\varepsilon\_0)=1$ 只是对 $\tilde c\_{\mathfrak p}$ 的一个限制: 

$$
(\mathrm{A})\qquad\qquad
\prod\_{\mathfrak p\in S}\tilde c\_{\mathfrak p}(\varepsilon\_0) = 1.
$$

 因此我们先选取一组 $\tilde c\_{\mathfrak p}$ ($\mathfrak p\in S$), 使它们满足 A. 条件 $c(\varepsilon\_v)=1$ ($1\le v\le m$) 给出对 $t\_{\mathfrak p}$ 的限制: 

$$
\prod\_{\mathfrak p\in S}\vert \varepsilon\_v\vert \_{\mathfrak p}^{it\_{\mathfrak p}}
= \prod\_{\mathfrak p\in S}\tilde c\_{\mathfrak p}^{-1}
(\tilde\varepsilon\_{v\mathfrak p}),\qquad 1\le v\le m,
$$

 它成立当且仅当各数 $t\_{\mathfrak p}$ 满足实线性方程组 

$$
(\mathrm{B})\qquad\qquad
\sum\_{\mathfrak p\in S}t\_{\mathfrak p}\log\vert \varepsilon\_v\vert \_{\mathfrak p}
= i\log\left(\prod\_{\mathfrak p\in S}\tilde c\_{\mathfrak p}
(\tilde\varepsilon\_{v\mathfrak p})\right),\qquad 1\le v\le m,
$$

 其中右端的对数取某一组值. 现在我们取定这些对数的一组值, 并取定一组解此方程的实数 $t\_{\mathfrak p}$. 由于众所周知矩阵 $(\log\vert \varepsilon\_v\vert \_{\mathfrak p})$ 的秩为 $m$, 这样的 $t\_{\mathfrak p}$ 总是存在的. 又因为对一切 $v$ 有 $\sum\_{\mathfrak p\in S}\log\vert \varepsilon\_v\vert \_{\mathfrak p}=0$, 故通解为 $t\_{\mathfrak p}=t\_{\mathfrak p}^{(0)}+t$, 其中 $t$ 任意. 既然谈到 $t\_{\mathfrak p}$ 的存在性与唯一性, 我们可以提醒读者: 若 $\mathfrak p$ 是 Archimedean 的, 不同的 $t\_{\mathfrak p}$ 给出不同的局部特征 $c\_{\mathfrak p}=\tilde c\_{\mathfrak p}\vert \,\vert \_{\mathfrak p}^{it\_{\mathfrak p}}$; 但若 $\mathfrak p$ 是离散的, 则相差 $2\pi/\log N\mathfrak p$ 的整数倍的 $t\_{\mathfrak p}$ 给出相同的局部 $c\_{\mathfrak p}$.

选定了 $\tilde c\_{\mathfrak p}$ 与 $t\_{\mathfrak p}$ 之后, 理想特征 $\chi$ 还剩下多少自由度? 不多. 要求对一切 $\alpha\in k^\ast $ 有 $c(\alpha)=1$, 意思是 $\chi$ 必须满足条件 

$$
(\mathrm{C})\qquad\qquad
\chi(\varphi\_S(\alpha)) = \prod\_{\mathfrak p\in S}\tilde c\_{\mathfrak p}^{-1}
(\tilde\alpha\_{\mathfrak p})\vert \alpha\vert \_{\mathfrak p}^{-it\_{\mathfrak p}},
$$

 对一切形如 $\varphi\_S(\alpha)$ 的理想成立, 即从主理想出发, 把其分解式中 $S$ 内素点的幂约去所得到的那些理想. 这些理想在与 $S$ 互素的全部理想所成的群中构成一个有限指数的子群 $h\_S$ (不超过类数 $h$; 若 $S$ 足够大则 $h\_S=1$). 由于条件 (C) 右端关于 $\alpha$ 的乘法函数已经被调整成在 $S$ 单位上平凡, 它就给出这个形如 $\varphi\_S(\alpha)$ 的理想子群的一个特征. 我们必须把 $\chi$ 选成这个特征到与 $S$ 互素的全部理想群上的有限多个 ($h\_S$ 个) 扩张之一.

**$\mathfrak z$ 中与之对应的函数.** 选定了在 $S$ 之外非分歧的特征 

$$
c(a) = \prod\_{\mathfrak p}c\_{\mathfrak p}(a\_{\mathfrak p})
= \prod\_{\mathfrak p\in S}\tilde c\_{\mathfrak p}(\tilde a\_{\mathfrak p})
\vert a\_{\mathfrak p}\vert \_{\mathfrak p}^{it\_{\mathfrak p}}\cdot\chi(\varphi\_S(a)),
$$

 之后, 我们希望找到一个简单的函数 $f(\mathfrak{x})\in\mathfrak z$, 使它的 $\zeta$ 函数在 $c(a)$ 所在的曲面上非平凡. 为此, 对每个 $\mathfrak p\in S$ 选取某个函数 $f\_{\mathfrak p}(\mathfrak{x}\_{\mathfrak p})\in\mathfrak z\_{\mathfrak p}$, 使它的 (局部) $\zeta$ 函数在 $c\_{\mathfrak p}$ 所在的曲面上非平凡 (例如把 $f$ 选成第 2.5 节中用来计算 $\rho\_{\mathfrak p}(c\_{\mathfrak p}\vert \,\vert \_{\mathfrak p}^s)$ 的那个函数). 对 $\mathfrak p\notin S$, 令 $f\_{\mathfrak p}(\mathfrak{x}\_{\mathfrak p})$ 为集合 $\mathfrak o\_{\mathfrak p}$ 的特征函数. 然后我们令 

$$
f(\mathfrak{x}) = \prod\_{\mathfrak p}f\_{\mathfrak p}(\mathfrak{x}\_{\mathfrak p}).
$$

 (我们将在计算过程中说明, 这个 $f(\mathfrak{x})$ 属于类 $\mathfrak z$.)

**它们的 Fourier 变换.** 按引理 3.3.3, 

$$
\widehat f(\mathfrak{x}) = \prod\_{\mathfrak p}\widehat f\_{\mathfrak p}(\mathfrak{x}\_{\mathfrak p}),
$$

 不仅如此, $f\in\mathfrak B\_1(V)$, 即 $f$ 满足公理 $(\mathfrak z\_1)$. 注意 $\widehat f(\mathfrak{x})$ 与 $f(\mathfrak{x})$ 是同一类型的函数, 只是对那些使 $\mathfrak d\_{\mathfrak p}\ne 1$ 的 $\mathfrak p\notin S$, $\widehat f\_{\mathfrak p}(\mathfrak{x}\_{\mathfrak p})$ 等于 $(N\mathfrak d\_{\mathfrak p})^{-\frac12}$ 乘以 $\mathfrak d\_{\mathfrak p}^{-1}$ 的特征函数, 而不是 $\mathfrak o\_{\mathfrak p}$ 的特征函数.

**$\zeta$ 函数.** 由于 $\vert f(a)\vert \,\vert a\vert ^\sigma=\prod\_{\mathfrak p}\vert f\_{\mathfrak p}(a\_{\mathfrak p})\vert  \vert a\vert \_{\mathfrak p}^\sigma$ 是局部函数的乘积, 其中几乎所有的函数在 $u\_{\mathfrak p}$ 上都等于 $1$, 我们可以用定理 3.3.1 来检验 $\vert f(a)\vert \,\vert a\vert ^\sigma$ 在 $\sigma>1$ 时的可和性. 一个简单的计算表明, 对 $\mathfrak p\notin S$, 

$$
\int\_{k\_{\mathfrak p}^\ast }\vert f\_{\mathfrak p}(a\_{\mathfrak p})\vert \,\vert a\_{\mathfrak p}\vert 
\_{\mathfrak p}^{\sigma}\, \mathrm{d}a\_{\mathfrak p}
= \frac{(N\mathfrak d\_{\mathfrak p})^{-\frac12}}{1-(N\mathfrak p)^{-\sigma}}.
$$

 因此可和性由如下众所周知的事实推出: 乘积 

$$
\prod\_{\mathfrak p\notin S\_{\infty}}\frac{1}{1-(N\mathfrak p)^{-\sigma}}
$$

 在 $\sigma>1$ 时收敛. 不管这个事实多么众所周知, 仍应强调它是整个理论的基石. 我们的 $\zeta$ 函数的存在性, 正如经典函数的存在性一样, 都以此为基础. 它的证明可以直接下降到有理数基本域来做 (例如见 E. Landau, “Algebraische Zahlen”, 第 2 版, 第 55 与 56 页). 由于 $\widehat f(\mathfrak{x})$ 与 $f(\mathfrak{x})$ 是同一类型的函数, 我们看到 $\vert \widehat f(a)\vert \,\vert a\vert ^\sigma$ 在 $\sigma>1$ 时也可和. 因此 $f(\mathfrak{x})$ 满足公理 $(\mathfrak z\_3)$.

确立了可和性之后, 我们也可以用定理 3.3.1 把 $\zeta$ 函数表示成局部 $\zeta$ 函数的乘积. 即对任一指大于 $1$ 的拟特征 $c=\prod\_{\mathfrak p}c\_{\mathfrak p}$ 有 

$$
\zeta(f,c) = \prod\_{\mathfrak p}\zeta\_{\mathfrak p}(f\_{\mathfrak p},
c\_{\mathfrak p}).
$$

 现在设 $c$ 表示我们的特殊特征, 

$$
c(a) = \prod\_{\mathfrak p}c\_{\mathfrak p}(a\_{\mathfrak p})
= \prod\_{\mathfrak p\in S}c\_{\mathfrak p}(a\_{\mathfrak p})\cdot
\chi(\varphi\_S(a)),
$$

 我们可以对 $\mathfrak p\notin S$ 显式算出 $\zeta(f,c\vert \,\vert ^s)$ 的局部因子. 确实, 

$$
\begin{aligned}
\zeta\_{\mathfrak p}(f\_{\mathfrak p},c\_{\mathfrak p}\vert \,\vert \_{\mathfrak p}^s)
&= \int\_{\mathfrak o\_{\mathfrak p}}c\_{\mathfrak p}(a\_{\mathfrak p})
\vert a\_{\mathfrak p}\vert \_{\mathfrak p}^s\, \mathrm{d}a\_{\mathfrak p}\\
&= \sum\_{v=0}^{\infty}\chi(\mathfrak p^v)\,(N\mathfrak p)^{-vs}\cdot
(N\mathfrak d\_{\mathfrak p})^{-\frac12}\\
&= \frac{(N\mathfrak d\_{\mathfrak p})^{-\frac12}}{1-\chi(\mathfrak p)
(N\mathfrak p)^{-s}},
\end{aligned}
$$

 因为对 $\mathfrak p\notin S$ 有 $c\_{\mathfrak p}(a\_{\mathfrak p}) =\chi(\mathfrak p^{\operatorname{ord}\_{\mathfrak p}a\_{\mathfrak p}})$. 因此, 如果我们引进经典的 $\zeta$ 函数 $\zeta(s,\chi)$, 它对 $\operatorname{Re}(s)>1$ 由 Euler 乘积 

$$
\zeta(s,\chi) = \prod\_{\mathfrak p\notin S}\frac{1}{1-\chi(\mathfrak p)
(N\mathfrak p)^{-s}}
$$

 定义, 我们就可以写 

$$
\zeta(f,c\vert \,\vert ^s) = \prod\_{\mathfrak p\in S}\zeta\_{\mathfrak p}(f\_{\mathfrak p},
c\_{\mathfrak p}\vert \,\vert \_{\mathfrak p}^s)\cdot\prod\_{\mathfrak p\notin S}
(N\mathfrak d\_{\mathfrak p})^{-\frac12}\cdot\zeta(s,\chi).
$$

 我们看到 $\zeta(f,c\vert \,\vert ^s)$ 本质上就是经典函数 $\zeta(s,\chi)$. 这里可以指出, 我们本来也可以直接得到 $\zeta(s,\chi)$ 的加性表达式 

$$
\zeta(s,\chi) = \sum\_{\substack{\mathfrak a\text{ 整理想}\\ \text{与 }S\text{ 互素}}}\frac{\chi(\mathfrak a)}{(N\mathfrak a)^s},
$$

 办法是把 $I$ 按 $I\_S$ 的陪集分解, 在每个陪集上积分再求和, 而不是用定理 3.3.1 把 $\zeta$ 函数积分表示成局部积分的乘积.

用同样的办法处理 $\widehat f$ 的 $\zeta$ 函数, 我们得到 

$$
\zeta(\widehat f,\widehat{c\vert \,\vert ^s}) = \prod\_{\mathfrak p\in S}
\zeta(\widehat f\_{\mathfrak p},
\widehat{c\_{\mathfrak p}\vert \,\vert \_{\mathfrak p}^s})\cdot\prod\_{\mathfrak p\notin S}
\chi(\mathfrak d\_{\mathfrak p})\,(N\mathfrak d\_{\mathfrak p})^{-s}\cdot
\zeta(1-s,\chi^{-1}),
$$

 对 $\operatorname{Re}(s)<0$.

在讨论由此得到的 $\zeta(s,\chi)$ 的解析延拓与函数方程之前, 我们应当先放下心来, 检验我们的 $f(\mathfrak{x})$ 满足公理 $(\mathfrak z\_2)$; 也就是说, 检验和 

$$
\sum\_{\xi\in k}f(a(\mathfrak{x}+\xi))
$$

 对 $I$ 的紧子集中的 $a$ 与 $\mathfrak{x}\in D$ 一致收敛. 在如下假设之下这很容易做到: 对 $\mathfrak p\in S$, 我们构造 $f$ 时所用的局部函数 $f\_{\mathfrak p}$ 与第 2.5 节中写下的标准局部函数相去不远. 即: 对离散的 $\mathfrak p\in S$, 设 $f\_{\mathfrak p}$ 在一个紧集之外为零; 对 Archimedean 的 $\mathfrak p$, 设 $f\_{\mathfrak p}(\mathfrak{x}\_{\mathfrak p})$ 在 $\mathfrak{x}\_{\mathfrak p}$ 趋于无穷时按指数速度趋于零. 在这些假设之下, 首先看出存在 $k$ 的一个理想 $\mathfrak a$, 使得当 $\xi\notin\mathfrak a$ 时, 对紧集中的一切 $a$ 与 $D$ 中的 $\mathfrak{x}$ 有 $f(a(\mathfrak{x}+\xi))=0$. 于是该和可以看成一个格上的求和, 这个格位于 $V$ 的无穷部分所成的 $n$ 维空间中, 而被求和的函数随到原点的距离按指数速度趋于零. 当然, 这个格依赖于 $a$ 与 $\mathfrak{x}$, 但把 $a$ 限制在紧集内意味着某个固定的一个小立方体总能嵌入该格的平行体之中. 于是该和的一致收敛性就是显然的了.

**$\zeta(s,\chi)$ 的解析延拓与函数方程.** 我们为 $\zeta$ 函数所建立的解析延拓, 无论在大范围还是局部, 现在直接给出 $\zeta(s,\chi)$ 到整个平面的解析延拓. 我们的函数方程 

$$
\zeta(\widehat f,\widehat c) = \zeta(f,c)\qquad\text{与}\qquad
\zeta\_{\mathfrak p}(f\_{\mathfrak p},c\_{\mathfrak p})
= \rho\_{\mathfrak p}(c\_{\mathfrak p})\zeta(\widehat f\_{\mathfrak p},
\widehat c\_{\mathfrak p})
$$

 给出 $\zeta(s,\chi)$ 的函数方程 

$$
\zeta(1-s,\chi^{-1}) = \prod\_{\mathfrak p\in S}\rho\_{\mathfrak p}
(\tilde c\_{\mathfrak p}\vert \,\vert \_{\mathfrak p}^{s+it\_{\mathfrak p}})\cdot
\prod\_{\mathfrak p\notin S}(N\mathfrak d\_{\mathfrak p})^{s-\frac12}
\chi^{-1}(\mathfrak d\_{\mathfrak p})\cdot\zeta(s,\chi).
$$

 局部函数 $\rho\_{\mathfrak p}$ 的显式表达式列在第 2.5 节中. $\tilde c\_{\mathfrak p}$ 与 $t\_{\mathfrak p}$ 的意义, 以及它们与理想特征 $\chi$ 的关系, 已在本节第一段中讨论过.

这些由伊代尔特征构造出来的理想特征 $\chi$, 正是 Hecke 为了定义他的“新型 $\zeta$ 函数”而引进的那些特征. $\zeta(s,\chi)$ 就是那个 $\zeta$ 函数; 而我们刚才写下的函数方程, 就是 Hecke 为它所证明的函数方程.

## 关于近年相关文献的几点评论

\[1967 年 1 月补加\]

Lang 的书“Algebraic Numbers”(Addison-Wesley, 1964) 中有一篇关于上述理论的综述, 其中把大范围的结果重新归一化, 使之与经典理论更相符合, 也更便于应用. 该书还处理了在素数密度, Brauer--Siegel 定理与“显式公式”上的应用. Lang 敦促我指出: 在关于素数等分布的定理 (同书第 6 定理, 第 130 页) 中, 必须假设 $\sigma(J\_k^0)=G$, 而不只是 $\sigma(J\_k)=G$; 因此紧接该定理之后的第一个应用, 即关于 $\log p$ 的等分布, 并不成立.

关于上文所给函数方程证明的另一种解释, 见 Weil,“Fonction zéta et distributions”, Séminaire Bourbaki, 第 312 号, 1966 年 6 月.

Siegel 关于二次型的工作近年在激励着大量的 adele 式分析 (adele 是赋值向量的现代名称). 关于这一方向的一些关键结果与文献目录, 见 Weil 在“Acta Mathematica”1964 年与 1965 年的论文.

## 参考文献

Artin, E. and Whaples, G. (1945). Axiomatic characterization of fields by the product formula for valuations. *Bull. Am. math. Soc.* **51**, 469--492.

Cartan, H. and Godement, R. (1947). Théorie de la dualité et analyse harmonique dans les groupes abéliens localement compacts. *Annls. scient. Éc. norm. sup., Paris* (3), **64**, 79--99.

Chevalley, C. (1940). La théorie du corps de classes. *Ann. Math.* **41**, 394--418.

Hecke, E. Über eine neue Art von Zetafunktionen und ihre Beziehungen zur Verteilung der Primzahlen. *Math. Z.* **1** (1918), 357--376; **4** (1920), 11--21. Reprinted in “Mathematische Werke”, Vandenhoeck und Ruprecht, Göttingen, 1959.

Matchett, M. *Thesis*, Indiana University (1946), unpublished.

## 附录 符号对照表

按首次出现顺序列出全书主要符号. 局部符号在大范围情形下加下标 $\mathfrak p$.

<table class="tate-table tate-symbols">
<thead><tr><th>符号</th><th>含义</th><th>首见</th></tr></thead>
<tbody>
<tr><td>$k$</td><td>代数数域; 局部理论中为它在某素除子处的完备化</td><td>2.1</td></tr>
<tr><td>$k^+$</td><td>$k$ 的加法群</td><td>2.2</td></tr>
<tr><td>$k^\ast $</td><td>$k$ 的乘法群; 4.1.4 处专指 $k$ 的对偶群</td><td>2.3</td></tr>
<tr><td>$\mathfrak p$</td><td>$k$ 的素除子</td><td>2.1</td></tr>
<tr><td>$\mathfrak o$</td><td>$\mathfrak p$ 进域 $k$ 的整数环</td><td>2.1</td></tr>
<tr><td>$u$</td><td>$\{\alpha\in k^\ast :\vert \alpha\vert =1\}$</td><td>2.3</td></tr>
<tr><td>$\vert \alpha\vert $</td><td>规范赋值</td><td>2.1</td></tr>
<tr><td>$\lambda,\ \Lambda$</td><td>局部与整体的加法特征指数</td><td>2.2</td></tr>
<tr><td>$S\_{k/R}$</td><td>$k$ 到 $R$ 的迹映射</td><td>2.2</td></tr>
<tr><td>$\mathfrak d$</td><td>$k$ 的绝对差积</td><td>2.2</td></tr>
<tr><td>$d\xi$</td><td>$k^+$ 上选定的 Haar 测度</td><td>2.2</td></tr>
<tr><td>$\mathrm{d}\alpha$</td><td>$k^\ast $ 上选定的乘法测度</td><td>2.3</td></tr>
<tr><td>$\mathfrak f$</td><td>特征的导子</td><td>2.3</td></tr>
<tr><td>$\mathfrak z$</td><td>定义 $\zeta$ 函数所用的函数类</td><td>2.4</td></tr>
<tr><td>$\mathfrak B\_1(G)$</td><td>$f$ 与 $\widehat f$ 都连续可和的函数类</td><td>1.3</td></tr>
<tr><td>$\zeta(f,c)$</td><td>$\zeta$ 函数 (局部或整体)</td><td>2.4.1</td></tr>
<tr><td>$\rho(c),\ \rho\_0(c)$</td><td>函数方程中的因子与根数</td><td>2.4.1, 2.5</td></tr>
<tr><td>$V$</td><td>赋值向量群</td><td>4.1.1</td></tr>
<tr><td>$\mathfrak{x}$</td><td>$V$ 的一般元素</td><td>4.1</td></tr>
<tr><td>$\overset{\infty}{V}$</td><td>$V$ 的无穷部分</td><td>4.1</td></tr>
<tr><td>$D$</td><td>加法基本域</td><td>4.1.2</td></tr>
<tr><td>$S\_{\infty},\ S'\_{\infty}$</td><td>Archimedean 素点集; 去掉 $\mathfrak p\_0$ 后所得者</td><td>3.1, 4.3</td></tr>
<tr><td>$r\_1,\ r\_2$</td><td>实素点与复素点对的个数</td><td>4.1</td></tr>
<tr><td>$I$</td><td>伊代尔乘法群</td><td>4.3.1</td></tr>
<tr><td>$J$</td><td>绝对值为 $1$ 的伊代尔所成的子群</td><td>4.3</td></tr>
<tr><td>$T$</td><td>使 $I=T\times J$ 的补子群</td><td>4.3</td></tr>
<tr><td>$l(b)$</td><td>伊代尔 $b$ 的对数向量</td><td>4.3</td></tr>
<tr><td>$P,\ Q$</td><td>$r$ 空间中的平行体与单位立方体</td><td>4.3</td></tr>
<tr><td>$R$</td><td>调节子</td><td>4.3.1</td></tr>
<tr><td>$h,\ h\_S,\ w$</td><td>类数, $S$ 类数, 单位根个数</td><td>4.3.2</td></tr>
<tr><td>$E$</td><td>乘法基本域</td><td>4.3.2</td></tr>
<tr><td>$\kappa$</td><td>乘法基本域的测度</td><td>4.4.1</td></tr>
<tr><td>$\chi$</td><td>与 $S$ 互素的理想群的特征</td><td>4.5</td></tr>
<tr><td>$\zeta(s,\chi)$</td><td>经典 $\zeta$ 函数</td><td>4.5</td></tr>
<tr><td>$\varphi\_S(a)$</td><td>伊代尔到与 $S$ 互素理想的映射</td><td>4.5</td></tr>
<tr><td>$N\mathfrak a$</td><td>理想 $\mathfrak a$ 的绝对范数</td><td>2.1</td></tr>
</tbody>
</table>

pdf: <a href="{{ site.baseurl }}/pdf/tate-thesis-zh-full.pdf">数域上的Fourier分析与Hecke的zeta函数</a>.
