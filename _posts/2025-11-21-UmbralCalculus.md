---
layout: post
title: "哑演算"
subtitle: ""
header-img: "img/post-bg-infinity.jpg"
header-mask: 0.3
math: true
tags:
  - 代数
---

# 多项式列

设 $\\{p_n(x)\\}_{n=0}^\infty$ 是一列 $\\mathbb{C}[x]$ 中的多项式, 以后我们说的多项式列都要求有 $ \deg p_n=n $, 即第 $ n $ 个多项式的次数恰好为 $ n $, 其中当 $ n=0 $ 时解释为非零常函数($ p(x)=0 $ 的次数通常定义为无穷小). 显然这样的一列多项式组成线性空间 $ \\mathbb{C}[x] $ 的一组基.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(二项式型多项式列)</b>
设 $\\{p_n(x)\\}_{n=0}^\infty$ 是一列多项式, 如果它们满足以下条件, 则称其为二项式型多项式列:

$$
p_n(x+y)=\sum_{k=0}^n\binom{n}{k}p_{k}(x)p_{n-k}(y).
$$
</div>

显然有 $ p_0(x)=1 $, 当 $ n $ 为正整数时有 $ p_n(0)=0 $.

二项式型多项式的例子有: $ x^n $, 上升阶乘 $ (x)^n=x(x+ 1)\cdots (x + n - 1) $, 下降阶乘 $ (x)_n=x(x-1)\cdots (x - n + 1) $, 阿贝尔多项式 $ x(x-an)^{n-1} $, 贝尔多项式等.

设其指数型生成函数是

$$
G(x,t)=\sum_{n=0}^\infty p_n(x)\frac{t^n}{n!},
$$

则有函数方程 $ G(x+y,t)=G(x,t)G(y,t) $, 可以证明以下定理:

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
多项式列 $\\{p_n(x)\\}_{n=0}^\infty$ 是二项式型多项式列当且仅当其指数型生成函数为

$$
\sum_{n=0}^\infty p_n(x)\frac{t^n}{n!}=e^{xB(t)}
$$

的形式, 其中 $ B(t)=\sum_{k=1}^\infty B_kt^k=B_1t+B_2t^2+\cdots $, $ B_k\in \\mathbb{C} $ 且 $ B_1\neq0 $.
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(阿佩尔多项式列)</b>
设 $\\{p_n(x)\\}_{n=0}^\infty$ 是一列多项式, 如果它们满足以下条件, 则称其为阿佩尔多项式列:

$$
\frac{\mathrm{d}}{\mathrm{d}x}p_n(x)=np_{n-1}(x).
$$
</div>

设其指数型生成函数是 $ G(x,t) $, 则有微分方程 $ \frac{\mathrm{d}}{\mathrm{d}x}G(x,t)=tG(x,t) $, 于是有

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
多项式列 $\\{p_n(x)\\}_{n=0}^\infty$ 是阿佩尔多项式列当且仅当其指数型生成函数为

$$
\sum_{n=0}^\infty p_n(x)\frac{t^n}{n!}=A(t)e^{tx}
$$

的形式, 其中 $ A(t)=\sum_{k=0}^\infty A_kt^k=A_0+A_1t+A_2t^2+\cdots $, $ A_k\in \\mathbb{C} $ 且 $ A_0\neq0 $.
</div>

展开生成函数即可得到阿佩尔多项式列中多项式的具体表达式为

$$
p_n(x)=\sum_{k=0}^n\binom{n}{k}k!A_{k}x^{n-k}.
$$

阿佩尔多项式的例子有: $ x^n $, 伯努利多项式, 赫尔米特多项式, 欧拉多项式等.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(谢弗多项式列)</b>
设 $\\{p_n(x)\\}_{n=0}^\infty$ 是一列多项式, 如果它的生成函数有如下形式, 则称其为谢弗多项式列:

$$
\sum_{n=0}^\infty p_n(x)\frac{t^n}{n!}=A(t)e^{xB(t)},
$$

其中 $ B(t)=\sum_{k=1}^\infty B_kt^k=B_1t+B_2t^2+\cdots $, $ A(t)=\sum_{k=0}^\infty A_kt^k=A_0+A_1t+A_2t^2+\cdots $, $ A_k,B_k\in \\mathbb{C} $ 且 $ B_1\neq0 $, $ A_0\neq0 $.
</div>

显然二项式型多项式列和阿佩尔多项式列均为特殊的谢弗多项式列.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(哑复合)</b>
若 $\\{p_n(x)\\}_{n=0}^\infty$ 和 $\\{p_n(x)\\}_{n=0}^\infty$ 是两列谢弗多项式列, 设 $ p_n(x) = \sum_{k=0}^n a_{nk} x^k $, $ q_n(x) = \sum_{k=0}^n b_{nk} x^k $, $ a_{nk},b_{nk}\in\\mathbb{C} $, 定义它们的哑复合为多项式列 $ \\{(p\circ q)_n(x)\\}_{n=0}^\infty $, 其中

$$
(p\circ q)_n(x)=\sum_{k=0}^n a_{nk}q_k(x)=\sum_{0\le l\le k\le n}a_{nk}b_{kl}x^l.
$$
</div>

任何一个多项式列都可以对应一个无穷大的下三角矩阵, 定义 $\\{p_n(x)\\}_{n=0}^\infty$ 对应的下三角无穷矩阵为 $ (a_{nk}) $, 即

$$
\begin{pmatrix}
a_{0,0} & 0 & 0 & 0 & \cdots \\
a_{1,0} & a_{1,1} & 0 & 0 & \cdots \\
a_{2,0} & a_{2,1} & a_{2,2} & 0 & \cdots \\
a_{3,0} & a_{3,1} & a_{3,2} & a_{3,3} & \cdots \\
\vdots & \vdots & \vdots & \vdots & \ddots
\end{pmatrix}
$$

该矩阵称为Riordan矩阵, 无穷大矩阵的乘积按通常矩阵乘法推广, 显然两个多项式的哑复合为他们对应的矩阵的乘积 $ (a_{nk})(b_{nk}) $ 对应的多项式, 因为 $ p_n $ 是 $ n $ 次多项式, 故矩阵对角线元都不是 $ 0 $, 由矩阵乘法知哑复合运算是结合的和可逆的(逆元称为共轭多项式列), 并且有单位元 $ \\{x^n\\}_{n=0}^\infty $, 哑复合一般不是可交换的. 全体二项式型多项式列组成的集合, 全体阿佩尔多项式列组成的集合以及全体谢弗多项式列组成的集合在该运算下均是群, 分别记为 $ \\mathbb{B} $, $ \\mathbb{A} $ 和 $ \\mathbb{S} $, 分别称为阿佩尔子群, 拉格朗日子群和Riordan群. $ \\mathbb{B} $ 和 $ \\mathbb{A} $ 均是 $ \\mathbb{S} $ 的子群, 其中 $ \\mathbb{A} $ 还是阿贝尔子群和正规子群, 并且有 $ \\mathbb{S}=\\mathbb{A}\rtimes\\mathbb{B} $.

如果 $\\{p_n(x)\\}_{n=0}^\infty$ 和 $\\{q_n(x)\\}_{n=0}^\infty$ 的生成函数分别是 $ A(t)e^{xB(t)} $ 和 $ C(t)e^{xD(t)} $, 可以验证, $ \\{(p\circ q)_n(x)\\}_{n=0}^\infty $ 的生成函数是 $ A(t)C(B(t))e^{xD(B(t))} $.

谢弗多项式列之上还有广义阿佩尔多项式列和Boas-Buck多项式列等推广, 但我们此处不涉及它们.
# 参考文献

[1] Francesco Aldo Costabile, Modern Umbral Calculus: An Elementary Introduction with Applications to Linear Interpolation and Operator Approximation Theory, De Gruyter Studies in Mathematics, vol. 72, Walter de Gruyter, Berlin, Boston, 2019.

[2] Adriano M. Garsia, An exposé of the Mullin-Rota theory of polynomials of binomial type, Linear and Multilinear Algebra 1 (1973), no. 1, 47–65.

[3] Steven Roman, The Umbral Calculus, Pure and Applied Mathematics, vol. 111, Academic Press, New York, 1984.

[4] , Advanced Linear Algebra, 3rd ed., Graduate Texts in Mathematics, vol. 135, Springer, New York, 2008.
