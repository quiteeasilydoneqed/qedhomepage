---
layout: post
title: "直积分"
subtitle: ""
header-img: "img/post-bg-infinity.jpg"
header-mask: 0.3
math: true
tags:
  - 泛函分析
  - 抽象调和分析
---

设 $X$ 是一个集合, $\mathscr F$ 是 $X$ 上的一个 $\sigma$-代数, $\mu$ 是其上的 $\sigma$-有限测度, 对于 $X$ 中的每个点 $x$, 都指定一个复希尔伯特空间 $\mathcal H_x$, 其上的内积记作 $(\cdot,\cdot)_x$, 内积诱导的范数记作 $\|\cdot\|_x$, 这样得到的集合 $\\{\mathcal H_x\\}_{x\in X}$ 称为 $X$ 上的一个 **复希尔伯特空间场** 或简称为 **希尔伯特空间场**.

设 $F=\prod_{x\in X}\mathcal{H}_x$, 其中的元素即为 $f\colon X\to \bigsqcup_{x\in X}\mathcal{H}_x$ 且满足 $f(x)\in\mathcal{H}_x$ 的函数, 称为 **向量场** 或 **截面**.

如果存在 $F$ 中一个可数集 $\\{e_i\\}_{i=1}^\infty$, 使得对于任意一个 $x\in X$, $\mathrm{span}\\{e_i(x)\\}_{i=1}^\infty$ 在 $\mathcal{H}_x$ 中稠密, 也就是说 $\overline{\mathrm{span}\\{e_i(x)\\}_{i=1}^\infty}=\mathcal{H}_x$, 并且对任意正整数 $i,j$, 映射 $x\mapsto(e_i(x),e_j(x))_x$ 均可测, 此时称这个希尔伯特空间场为 **可测希尔伯特空间场**, 或称为 **希尔伯特丛**, $\\{e_i\\}_{i=1}^\infty$ 称为 **基本可测向量场** 或 **基本可测截面**. 注意, 这个条件表明可测希尔伯特空间场中的希尔伯特空间 $\mathcal{H}_x$ 都是可分的, 进而也都是至多可数维的.

设 $f\in F$ 是一个向量场, 如果对任意一个正整数 $i$, 映射 $x\mapsto (f(x),e_i(x))_x$ 都是可测的, 则称向量场 $f$ 是 **可测向量场** 或 **可测截面**. 可以证明, 向量场的可测性与基本可测向量场的选取无关, 并且如果 $f$ 和 $g$ 都是可测向量场, 那么映射 $x\mapsto(f(x),g(x))_x$ 是可测的, 所以 $x\mapsto\|f(x)\|_x=\sqrt{(f(x),f(x))_x}$ 也是可测的.

<div style="border: 3px solid #000; padding: 10px;">
<b>例</b>
设 $\mathcal{H}$ 是一个可分希尔伯特空间, 对于集合 $X$ 中的任何元素 $x$, 都有 $\mathcal{H}_x=\mathcal{H}$, 它显然是一个可测希尔伯特空间场, 称为 **常值希尔伯特空间场** 或简称为 **常值场**.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(直积分)</b>
设 $\mathcal{H}_x$ 是 $X$ 上的一个可测希尔伯特空间场, 则定义, 所有满足
    
$$
\int_X\|f(x)\|_x\mathrm{d}\mu(x)<\infty
$$

的可测向量场 $f$ 组成的复线性空间为 $\mathcal{H}_x$ 的 **直积分**
    
$$
\int_X^\oplus \mathcal{H}_x\mathrm{d}\mu(x),
$$

无混淆的情况下下标 $X$ 可省略不写.
</div>

给这个线性空间配备上一个内积
$$
(f,g):=\int_X(f(x),g(x))_x\mathrm{d}\mu(x)
$$
使其成为内积空间, 它诱导的范数记作
$$
\|f\|^2:=\int_X\|f(x)\|_x\mathrm{d}\mu(x),
$$
事实上, 可以证明这个内积使其成为一个希尔伯特空间.

<div style="border: 3px solid #000; padding: 10px;">
<b>例</b>
如果 $\mathcal{H}_x=\mathcal{H}$ 是常值场, 则直积分简记为

$$
\int_X^\oplus \mathcal{H}_x\mathrm{d}\mu(x)=\int_X^\oplus \mathcal{H}\mathrm{d}\mu(x)=L^2(X,\mu,\mathcal{H}).
$$

如果 $X$ 是离散空间, 即带离散拓扑的空间, 并且其上的测度取计数测度, 那么直积分退化为直积

$$
\int_X^\oplus \mathcal{H}_x\mathrm{d}\mu(x)=\bigoplus_{x\in X}\mathcal{H}_x.
$$
</div>

以下是几个简单的性质.

<div style="border: 3px solid #000; padding: 10px;">
<b>性质</b>
如果 $X=\bigsqcup_{k=1}^\infty X_k$ 且各个 $X_k$ 都是可测集, 那么有

$$
\int_X^\oplus \mathcal{H}_x\mathrm{d}\mu(x)\cong\bigoplus_{k=1}^\infty\int_{X_k}^\oplus \mathcal{H}_{x}\mathrm{d}\mu(x).
$$

设 $X_k=\{x\in X\mid \dim\mathcal{H}_x=k\}, k=1,2,\dots,\infty$, 则它们都是可测集, 并且有

$$
\int_X^\oplus \mathcal{H}_x\mathrm{d}\mu(x)\cong L^2(X_\infty,\mu,l^2_\mathbb C)\oplus\bigoplus_{k=1}^\infty L^2(X_k,\mu,\mathbb C^k),
$$

需要注意的是其中 $l^2_{\mathbb C}=\mathbb C^\infty$.
</div>

接下来看直积分理论在抽象调和分析中的应用, 以下设 $X=G$ 是一个局部紧阿贝尔群, 其对偶群 $\hat{G}$ 定义为 $G$ 到复平面上单位圆群 $\mathbb T$ 的所以同态组成的乘法群, 也称为酉特征标群. 对偶群上也可以定义拓扑使其成为局部紧阿贝尔群, 对偶群上又有二次对偶群, 事实上, 庞特里亚金对偶定理表明有

$$

G\cong\widehat{\widehat{G}}.

$$

在 $G$ 和 $\hat{G}$ 上取归一化哈尔测度, 均由 $\mu$ 表示, 定义傅里叶变换为

$$
f\mapsto\hat{f}(\chi)=\int_Gf(g)\overline{\chi(g)}\mathrm{d}g,f\in L^1(G)\cap L^2(G),
$$

则有傅里叶反演公式

$$
f(x)=\int_{\hat{G}}\hat{f}(\chi)\chi(g)\mathrm{d}\chi,
$$

傅里叶变换可延拓为等距同构 $L^2(G)\cong L^2(\hat{G})$, 称为局部紧阿贝尔群上的普朗歇尔定理或帕塞瓦尔公式.

在对偶群 $\hat{G}$ 中, 设 $\chi$ 处的希尔伯特空间为 $\mathcal{H}_\chi$, 因为 $\chi$ 是 $G$ 的一维不可约表示, 可以证明必有 $\dim \mathcal{H}_\chi=1$, 即 $\mathcal{H}_\chi=\mathbb{C}$. 对比直积分的定义可知,

$$
L^2(\hat{G})=\int_{\hat{G}}^\oplus\mathbb C\mathrm{d}\mu(\chi)=L^2(\hat{G},\mu,\mathbb C),
$$

而由普朗歇尔定理知

$$
L^2(G)\cong L^2(\hat{G})=\int_{\hat{G}}^\oplus\mathbb C\mathrm{d}\mu(\chi),
$$

从元素上来说, 这就是说 $L^2(G)$ 中的元素 $f$ 可以分解为在各酉特征标上的分量之和, 即傅里叶逆变换. 显然, 由对偶性知还有
<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
设 $G$ 是局部紧阿贝尔群, $\hat{G}$ 是其对偶群, 则有

$$
L^2(G)\cong L^2(\hat{G})=\int_{\hat{G}}^\oplus\mathbb C\mathrm{d}\mu(\chi)\cong\int_{G}^\oplus\mathbb C\mathrm{d}\mu(g).
$$
</div>
