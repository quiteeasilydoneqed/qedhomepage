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

设$ \{p_n(x)\}_{n=0}^\infty $是一列$ \mathbb{C}[x] $中的多项式, 以后我们说的多项式列都要求有$ \deg p_n=n $, 即第$ n $个多项式的次数恰好为$ n $, 其中当$ n=0 $时解释为非零常函数($ p(x)=0 $的次数通常定义为无穷小). 显然这样的一列多项式组成线性空间$ \mathbb{C}[x] $的一组基.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(二项式型多项式列)</b>
设$ \{p_n(x)\}_{n=0}^\infty $是一列多项式, 如果它们满足以下条件, 则称其为二项式型多项式列:

$$
p_n(x+y)=\sum_{k=0}^n\binom{n}{k}p_{k}(x)p_{n-k}(y).
$$
</div>

显然有$ p_0(x)=1 $, 当$ n $为正整数时有$ p_n(0)=0 $.

二项式型多项式的例子有: $ x^n $, 上升阶乘$ (x)^n=x(x+ 1)\cdots (x + n - 1) $, 下降阶乘$ (x)_n=x(x-1)\cdots (x - n + 1) $, 阿贝尔多项式$ x(x-an)^{n-1} $, 贝尔多项式等.

设其指数型生成函数是

$$
G(x,t)=\sum_{n=0}^\infty p_n(x)\frac{t^n}{n!},
$$

则有函数方程$ G(x+y,t)=G(x,t)G(y,t) $, 可以证明以下定理:

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
多项式列$ \{p_n(x)\}_{n=0}^\infty $是二项式型多项式列当且仅当其指数型生成函数为

$$
\sum_{n=0}^\infty p_n(x)\frac{t^n}{n!}=e^{xB(t)}
$$

的形式, 其中$ B(t)=\sum_{k=1}^\infty B_kt^k=B_1t+B_2t^2+\cdots $, $ B_k\in \mathbb{C} $且$ B_1\neq0 $.
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(阿佩尔多项式列)</b>
设$ \{p_n(x)\}_{n=0}^\infty $是一列多项式, 如果它们满足以下条件, 则称其为阿佩尔多项式列:

$$
\frac{\mathrm{d}}{\mathrm{d}x}p_n(x)=np_{n-1}(x).
$$
</div>

设其指数型生成函数是$ G(x,t) $, 则有微分方程$ \frac{\mathrm{d}}{\mathrm{d}x}G(x,t)=tG(x,t) $, 于是有

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
多项式列$ \{p_n(x)\}_{n=0}^\infty $是阿佩尔多项式列当且仅当其指数型生成函数为

$$
\sum_{n=0}^\infty p_n(x)\frac{t^n}{n!}=A(t)e^{tx}
$$

的形式, 其中$ A(t)=\sum_{k=0}^\infty A_kt^k=A_0+A_1t+A_2t^2+\cdots $, $ A_k\in \mathbb{C} $且$ A_0\neq0 $.
</div>

展开生成函数即可得到阿佩尔多项式列中多项式的具体表达式为

$$
p_n(x)=\sum_{k=0}^n\binom{n}{k}k!A_{k}x^{n-k}.
$$

阿佩尔多项式的例子有: $ x^n $, 伯努利多项式, 赫尔米特多项式, 欧拉多项式等.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(谢弗多项式列)</b>
设$ \{p_n(x)\}_{n=0}^\infty $是一列多项式, 如果它的生成函数有如下形式, 则称其为谢弗多项式列:

$$
\sum_{n=0}^\infty p_n(x)\frac{t^n}{n!}=A(t)e^{xB(t)},
$$

其中$ B(t)=\sum_{k=1}^\infty B_kt^k=B_1t+B_2t^2+\cdots $, $ A(t)=\sum_{k=0}^\infty A_kt^k=A_0+A_1t+A_2t^2+\cdots $, $ A_k,B_k\in \mathbb{C} $且$ B_1\neq0 $, $ A_0\neq0 $.
</div>

显然二项式型多项式列和阿佩尔多项式列均为特殊的谢弗多项式列.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(哑复合)</b>
若$ \{p_n(x)\}_{n=0}^\infty $和$ \{p_n(x)\}_{n=0}^\infty $是两列谢弗多项式列, 设$ p_n(x) = \sum_{k=0}^n a_{nk} x^k $, $ q_n(x) = \sum_{k=0}^n b_{nk} x^k $, $ a_{nk},b_{nk}\in\mathbb{C} $, 定义它们的哑复合为多项式列$ \{(p\circ q)_n(x)\}_{n=0}^\infty $, 其中

$$
(p\circ q)_n(x)=\sum_{k=0}^n a_{nk}q_k(x)=\sum_{0\le l\le k\le n}a_{nk}b_{kl}x^l.
$$
</div>

任何一个多项式列都可以对应一个无穷大的下三角矩阵, 定义$ \{p_n(x)\}_{n=0}^\infty $对应的下三角无穷矩阵为$ (a_{nk}) $, 即

$$
\begin{pmatrix}
a_{0,0} & 0 & 0 & 0 & \cdots \\
a_{1,0} & a_{1,1} & 0 & 0 & \cdots \\
a_{2,0} & a_{2,1} & a_{2,2} & 0 & \cdots \\
a_{3,0} & a_{3,1} & a_{3,2} & a_{3,3} & \cdots \\
\vdots & \vdots & \vdots & \vdots & \ddots
\end{pmatrix}
$$

该矩阵称为Riordan矩阵, 无穷大矩阵的乘积按通常矩阵乘法推广, 显然两个多项式的哑复合为他们对应的矩阵的乘积$ (a_{nk})(b_{nk}) $对应的多项式, 因为$ p_n $是$ n $次多项式, 故矩阵对角线元都不是$ 0 $, 由矩阵乘法知哑复合运算是结合的和可逆的(逆元称为共轭多项式列), 并且有单位元$ \{x^n\}_{n=0}^\infty $, 哑复合一般不是可交换的. 全体二项式型多项式列组成的集合, 全体阿佩尔多项式列组成的集合以及全体谢弗多项式列组成的集合在该运算下均是群, 分别记为$ \mathbb{B} $, $ \mathbb{A} $和$ \mathbb{S} $, 分别称为阿佩尔子群, 拉格朗日子群和Riordan群. $ \mathbb{B} $和$ \mathbb{A} $均是$ \mathbb{S} $的子群, 其中$ \mathbb{A} $还是阿贝尔子群和正规子群, 并且有$ \mathbb{S}=\mathbb{A}\rtimes\mathbb{B} $.

如果$ \{p_n(x)\}_{n=0}^\infty $和$ \{q_n(x)\}_{n=0}^\infty $的生成函数分别是$ A(t)e^{xB(t)} $和$ C(t)e^{xD(t)} $, 可以验证, $ \{(p\circ q)_n(x)\}_{n=0}^\infty $的生成函数是$ A(t)C(B(t))e^{xD(B(t))} $.

谢弗多项式列之上还有广义阿佩尔多项式列和Boas-Buck多项式列等推广, 但我们此处不涉及它们.

# 泛函

设$ P=\mathbb{C}[x] $为多项式代数, 定义$ P^* $为其上所有线性泛函组成的集合, 即对偶空间.

设$ L\in P^* $, $ p(x)\in P $, 泛函在多项式上的作用写作

$$
\braket{L}{p(x)},
$$

这借鉴自物理学中的狄拉克符号,

设数列$ \{a_n\}_{n=0}^\infty $的指数型生成函数是

$$
f(t) = \sum_{k=0}^{\infty} \frac{a_k}{k!} t^k,
$$

定义它对应的线性泛函为
$ \langle A | x^n \rangle=a_n, $
称$ A $为该数列对应的哑元, 在经典哑演算中, 也写作$ A^n=a_n $, 对应经典哑演算将下标移为上标的操作.

设$ \mathbb{C}[[t]] $为以$ t $为变量的形式幂级数代数, 对于$ L\in P^* $, 定义映射

$$
L\mapsto f_L(t)=\sum_{k=0}^{\infty} \frac{\langle L | x^k \rangle}{k!} t^k,
$$

由前面的讨论知该映射是双射, 并且显然保持线性空间的结构, 因此它是从$ P^* $到$ \mathbb{C}[[t]] $的线性同构, 此后将两者看做同一. 先来看一些简单的性质.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
以下设$ f_k\in\mathbb{C}[[t]] $, $ p\in P $, $ o(f) $为幂级数$ f $的系数$ a_k $中不为$ 0 $的最小$ k $, 约定$ o(0)=\infty $.

$$
\langle f_1(t)f_2(t) | x^n \rangle = \sum_{k=0}^{n} \binom{n}{k} \langle f_1(t) | x^k \rangle \langle f_2(t) | x^{n-k} \rangle;
$$

$$
\langle f_1(t) \cdots f_m(t) | x^n \rangle = \sum_{\substack{i_1 + \cdots + i_m = n \\ i_1, \dots, i_m \geq 0}} \binom{n}{i_1, \dots, i_m} \langle f_1(t) | x^{i_1} \rangle \cdots \langle f_m(t) | x^{i_m} \rangle;
$$

$$
\langle f(t) | x p(x) \rangle = \langle \frac{\mathrm{d}}{\mathrm{d}t} f(t) | p(x) \rangle;
$$

$$
\langle f(ct) |  p(x) \rangle =\langle f(t) | p(cx) \rangle, \quad c\in\mathbb{C} ;
$$

如果$ o(f(t)) > \deg p(x) $, 则

$$
\langle f(t) | p(x) \rangle = 0;
$$

如果对正整数$ k $, $ o(f_k)=k $, 则

$$
\left\langle \sum_{k=0}^{\infty} a_k f_k(t) \bigg| p(x) \right\rangle = \sum_{k=0}^{\infty} a_k \langle f_k(t) | p(x) \rangle.
$$
</div>

接下来举几个例子.

<div style="border: 3px solid #000; padding: 10px;">
<b>例</b>
取$ f(t)=1 $, 则$ \braket{1}{x^n}=\delta_{0,n} $为克罗内克符号, 从而有$ \braket{1}{p(x)}=p(0) $.
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>例</b>
取$ f(t)=t^k $, 则$ \braket{t^k}{x^n}=\frac{\delta_{k,n}}{n!} $, 从而有$ \braket{t^k}{p(x)}=p^{(k)}(0) $.
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>例</b>
取$ f(t)=e^{yt} $, 则$ \braket{e^{yt}}{x^n}=y^n $, 从而有$ \braket{e^{yt}}{p(x)}=p(y) $, 因此称为取值泛函, 显然$ \braket{e^{yt}-1}{p(x)}=p(y)-p(0) $.
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>例</b>
取$ f(t)=te^{yt} $, 则$ \braket{te^{yt}}{x^n}=ny^{n-1} $, 从而有$ \braket{te^{yt}}{p(x)}=p'(y) $, 进而$ \braket{t^ke^{yt}-1}{p(x)}=p^{(k)}(y) $.
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>例</b>
取$ f(t)=(1 - t)^{-1} $, 则$ \braket{(1 - t)^{-1}}{x^n}=n! $, 因为$ n!=\int_0^\infty u^ne^{-u}\mathrm{d}u $, 从而有

$$
\braket{(1 - t)^{-1}}{p(x)}=\int_0^\infty p(u)e^{-u}\mathrm{d}u.
$$
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>例</b>
取$ f(t)=\frac{e^{yt}-1}{t} $, 则

$$
\braket{\frac{e^{yt}-1}{t}}{p(x)}=\int_0^y p(u)\mathrm{d}u,
$$

称为积分泛函.
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>例</b>
取$ f(t)=\frac{t}{e^t-1} $, 它是积分泛函的逆泛函, 设它对应的哑元为$ B $, 则$ \langle B | x^n \rangle=B_n $为伯努利数 经典哑演算中写作$ B^n=B_n $.
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>例</b>
取$ f(t)=\frac{1 + e^{yt}}{2} $, 则

$$
\left\langle \frac{1 + e^{yt}}{2} \bigg| p(x) \right\rangle = \frac{p(0) + p(y)}{2},
$$

它的逆是$ f(t)=\frac{2}{1 + e^{t}} $, 设它对应哑元为$ E $, 则$ \langle E | x^n \rangle=E_n $是欧拉多项式在$ 0 $处的值, 也叫欧拉数.
</div>

# 线性变换

接下来我们把$ P^* $中的元素做成$ P $上的线性变换, 设$ f_L(t)=\sum_{k=0}^{\infty} \frac{\langle L | x^k \rangle}{k!} t^k $, 再设$ \langle L | x^k \rangle=L_k $, 定义$ f_L(t) $的左乘作用为

$$
f_L(t)\cdot x^n=\sum_{k=0}^{n}\binom{n}{k} L_kx^{n-k},
$$

这定义了一个$ P\to P $的线性变换, 称它为由级数$ f_L(t) $生成的线性变换.

如果$ P $上的线性变换将$ n $次多项式映为$ n $次多项式, 则它显然是线性同构, 如果它还由$ f_L(t) $生成, 则显然有$ L_0=f_L(0)\neq0 $.

<div style="border: 3px solid #000; padding: 10px;">
<b>例</b>
设$ f(t)=e^{yt}=\sum_{k=0}^{\infty} \frac{y^k}{k!} t^k $, 故它在$ x^n $上的左乘作用就是

$$
f(t)\cdot x^n=\sum_{k=0}^{n}\binom{n}{k} y^kx^{n-k}=(x+y)^n,
$$

进而有

$$
e^{yt}\cdot p(x)=p(x+y),
$$

因此称其为平移变换或平移算子.
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>例</b>
设$ f(t)=t $, 则$ t\cdot p(x)=p'(x) $, 因此也称其为微分变换或微分算子, 记其哑元为$ D $, 因此形式上有

$$
e^{yt}=e^{yD},
$$

并且$ e^{yD}\cdot p(x)=p(x+y) $, 左边展开为级数就得到了$ p $在$ x $处的泰勒级数, 因为$ p $是多项式, 这里不必考虑收敛问题, 这就是经典哑演算中$ e^{\frac{\mathrm{d}}{\mathrm{d}x}} $的意义.
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>例</b>
更多的例子:

$$
t^ke^{yt}\cdot p(x)=p^{(k)}(x+y),
$$

$$
(1 - t)^{-1} \cdot p(x)=\int_0^\infty p(x+u)e^{-u}\mathrm{d}u,
$$

$$
\frac{e^{yt}-1}{t}\cdot p(x)=\int_x^{x+y} p(u)\mathrm{d}u,
$$

$$
\frac{t}{e^t-1}\cdot x^n=B_n(x)
$$

为伯努利多项式, 这对应经典哑演算中$ (B+x)^n=B_n(x). $

$$
\frac{1 + e^{yt}}{2}\cdot p(x)=\frac{p(x)+p(x+y)}{2},
$$

$$
\frac{2}{1 + e^{t}}\cdot x^n= E_n(x)
$$

为欧拉多项式.
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
设$ T $是$ P $上一个将$ n $次多项式映为$ n $次多项式的线性变换, 则$ T $可以由级数$ f_L(t) $生成当且仅当$ T $把$ x^n $映为阿佩尔多项式列.
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>证明</b>
设$ T $由幂级数$ f_L(t) $生成, 则$ T(x^n) $是指数型生成函数就是

$$
\sum_{n=0}^\infty T(x^n)\frac{t^n}{n!}=\sum_{n=0}^\infty\sum_{k=0}^{n}\binom{n}{k} L_kx^{n-k}\frac{t^n}{n!}=f_L(t)e^{xt},
$$

因为$ T $将$ n $次多项式映为$ n $次多项式, 所以必有$ f_L(0)\neq0 $, 由阿佩尔多项式列的性质知$ \{T(x^n)\}_{n=0}^\infty $为阿佩尔多项式列.

设$ T(x^n)=p_n(x) $为阿佩尔多项式列, 则它的生成函数为$ A(t)e^{xt} $的形式, 其中$ A(t)=\sum_{k=0}^\infty A_kx^k $为常数项非零的幂级数, 则

$$
A(t)\cdot x^n=\sum_{k=0}^n\binom{n}{k}A_kk!x^{n-k}=p_n(x),
$$

第一个等号是左乘作用的定义, 第二个等号是之前得到的阿佩尔多项式列的具体形式, 所以由$ A(t) $就可以生成$ T $.
</div>

设阿佩尔多项式列$ \{p_n(x)\} $的指数型生成函数是

$$
G(x,t)=\sum_{n=0}^\infty p_n(x)\frac{t^n}{n!},
$$

则

$$
G(0,t)\cdot x^n=p_n(x),
$$

将$ G(x,t)) $解释为含参数$ x $的泛函$ \mathbb{C}[y]\to\mathbb{C} $时, 有

$$
\langle G(x,t)|y^n\rangle=p_n(x),
$$

所以

$$
p_n(x)=\langle G(x,t)|y^n\rangle=G(0,t)\cdot x^n=\sum_{k=0}^n\binom{n}{k}\langle G(0,t)|y^n\rangle x^{n-k}=\langle G(0,t)|(x+y)^n\rangle,
$$

在经典哑演算中, 设$ P $是数列$ \{p_n(0)\} $的哑元, 则上式就解释为

$$
p_n(x)=\sum_{k=0}^n\binom{n}{k}p_k(0)x^{n-k}=\sum_{k=0}^n\binom{n}{k}P^kx^{n-k}=(x+P)^n.
$$

另一方面,

$$
\sum_{k=0}^n\binom{n}{k}\langle G(0,t)|y^n\rangle x^{n-k}=\langle G(0,t)|(x+y)^n\rangle
$$

等价于说

$$
\sum_{k=0}^n\binom{n}{k}p_n(y) x^{n-k}=p_n(x+y),
$$

这个式子称为阿佩尔恒等式.

接下来介绍谢弗多项式列的另一种定义.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
对任意幂级数$ f(t),g(t) $, 满足$ o(f(t))=1,o(g(t))=0 $ $ ($这等价于说$ f(t) $有复合逆, $ g(t) $有逆$ ) $, 则方程

$$
\langle g(t)\left(f(t)\right)^k|p_n(x)\rangle=n!\delta_{nk}
$$

有唯一解$ \{p_n(x)\} $.
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
$ \{p_n(x)\} $是谢弗多项式列当且仅当存在唯一的幂级数对$ \left(f(t),g(t)\right) $, 满足$ o(f(t))=1,o(g(t))=0 $, 并且有

$$
\langle g(t)\left(f(t)\right)^k|p_n(x)\rangle=n!\delta_{nk}
$$

对任意非负整数$ n $和$ k $成立.
</div>

事实上, 如果$ \langle g(t)\left(f(t)\right)^k|p_n(x)\rangle=n!\delta_{nk}, $ 那么$ p_n(x) $的生成函数就是

$$
\sum_{n=0}^\infty p_n(x)\frac{t^n}{n!}=\frac{1}{g(\bar f(t))}e^{x\bar{f}(t)},
$$

其中$ f(\bar{f}(t))=\bar{f}(f(t))=t. $

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
$ \{p_n(x)\} $是阿佩尔多项式列当且仅当存在唯一幂级数$ g(t) $, 满足$ o(g(t))=0 $, 并且有

$$
\langle g(t)t^k|p_n(x)\rangle=n!\delta_{nk}
$$

对任意非负整数$ n $和$ k $成立.
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
$ \{p_n(x)\} $是二项式型多项式列当且仅当存在唯一幂级数对任意幂级数$ f(t) $, 如果满足$ o(f(t))=1 $, 那么满足

$$
\langle \left(f(t)\right)^k|p_n(x)\rangle=n!\delta_{nk}
$$

对任意非负整数$ n $和$ k $成立.
</div>

# 算子与伴随算子

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(哑算子, 谢弗算子)</b>
设$ \{q_n(x)\} $是二项式型多项式列, 如果线性算子$ \lambda: P\to P $满足条件

$$
\lambda(x^n)=q_n(x),
$$

则称其为哑算子.

设$ \{p_n(x)\} $是谢弗多项式列, 如果线性算子$ \lambda: P\to P $满足条件

$$
\lambda(x^n)=p_n(x),
$$

则称其为谢弗算子.
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(哑移位, 谢弗移位)</b>
设$ \{q_n(x)\} $是二项式型多项式列, 如果线性算子$ \lambda: P\to P $满足条件

$$
\theta(q_n(x))=q_{n+1}(x),
$$

则称其为哑移位.

设$ \{p_n(x)\} $是谢弗多项式列, 如果线性算子$ \lambda: P\to P $满足条件

$$
\theta(p_n(x))=p_{n+1}(x),
$$

则称其为谢弗移位.
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(连续)</b>
设$ T $是$ P^*\cong\mathbb{C}[[t]] $上的线性算子, 如果对于$ P^* $中一列满足

$$
\lim_{k\to\infty} o(f_k(t))=\infty
$$

的序列$ \{f_k(t)\} $, 都有

$$
T\left(\sum_{k=0}^\infty a_kf_k(t)\right)=\sum_{k=0}^\infty a_nT(f_k(t)),
$$

其中$ a_k\in\mathbb{C} $, 则称算子$ T $是连续的.
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
$ P^* $上的算子$ T $是连续的当且仅当对任意满足

$$
\lim_{k\to\infty} o(f_k(t))=\infty
$$

的序列$ \{f_k(t)\} $, 都有

$$
\lim_{k\to\infty} o(T(f_k(t)))=\infty.
$$
</div>

举两个例子.

<div style="border: 3px solid #000; padding: 10px;">
<b>例(自同构算子, 导数算子)</b>
如果$ T $是$ P^* $上的代数自同构, 则可以证明一定有$ o(T(f))=o(f) $, 进而是连续的, $ T $称为自同构算子.

如果$ D $是$ P^* $上满足莱布尼兹律

$$
D(fg)=D(f)g+fD(g),\quad f,g\in P^*
$$

的线性算子, 则称其为一个导数算子. 当$ o(f)>1 $时, 可以证明任何一个满射的导数算子都有$ o(D(f))=o(f)-1 $, 并且$ D(c)=0 $, $ c\in\mathbb{C} $, 所以任何满射的导数算子都是连续的.
</div>

伴随算子的定义与通常泛函分析中相同.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(伴随)</b>
设$ \tau\in L(P) $是$ P $上的线性变换, 定义其伴随$ \tau^\times:P^*\to P^* $为满足

$$
\tau^\times(f(t))=f(t)\circ \tau,\quad f(t)\in P^*
$$

也就是说对任意$ f(t)\in P^* $和$ p(x)\in P $, 有

$$
\langle \tau^\times(f(t))|p(x)\rangle=\langle f(t)|\tau(p(x))\rangle.
$$
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
伴随有如下性质:

$ (\tau + \sigma)^\times = \tau^\times + \sigma^\times, $

若$ r \in \mathbb{C} $, $ (r\tau)^\times = r\tau^\times , $

$ (\tau\sigma)^\times = \sigma^\times\tau^\times, $

若$ \tau $可逆, $ (\tau^{-1})^\times = (\tau^\times)^{-1} . $
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
幂级数$ f(t) $以左乘作用在$ P $上时, 为$ P $上的线性变换, 它的伴随$ f(t)^\times $作用在$ g(t) $上是幂级数的乘法$ f(t)^\times (g(t))=f(t)g(t) $.
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>证明</b>
只需证明当$ f(t),g(t)\in P^* $时,

$$
\langle f(t)g(t) | p(x) \rangle = \langle g(t) | f(t)\cdotp(x) \rangle
$$

对任意$ p(x)\in P $都成立, 设

$$
f(t) = \sum_{k=0}^{\infty} \frac{\langle f(t) | x^k \rangle}{k!} t^k,
$$

$$
 g(t) = \sum_{k=0}^{\infty} \frac{\langle g(t) | x^k \rangle}{k!} t^k,
$$

则

\begin{align*}
    \langle g(t) | f(t) \cdot x^n \rangle =& \left\langle g(t) \bigg| \sum_{k=0}^{n} \binom{n}{k} \langle f(t) | x^k \rangle x^{n-k} \right\rangle\\ 
    =& \sum_{k=0}^{n} \binom{n}{k} \langle f(t) | x^k \rangle \langle g(t) | x^{n-k} \rangle\\
    =&\langle f(t)g(t) | x^n \rangle,
\end{align*}

进而

$$
\langle f(t)g(t) | p(x) \rangle = \langle g(t) | f(t)\cdot p(x) \rangle
$$

对任意$ p(x)\in P $都成立.
</div>

举一个例子,

$$
\delta_{1n}=\langle1|x^n\rangle=\left\langle\frac{e^t-1}{t}\frac{t}{e^t-1}\bigg|x^n\right\rangle=\left\langle\frac{e^t-1}{t}\bigg|\frac{t}{e^t-1}\cdot x^n\right\rangle=\left\langle\frac{e^t-1}{t}\bigg|B_n(x)\right\rangle=\int_0^1 B_n(x)\mathrm{d}x,
$$

其中$ B_n(x) $是伯努利多项式, 这就是伯努利多项式的积分性质, 另一方面,

$$
\delta_{1n}=\langle1|x^n\rangle=\left\langle\frac{t}{e^t-1}\frac{e^t-1}{t}\bigg|x^n\right\rangle=\left\langle\frac{t}{e^t-1}\bigg|\frac{e^t-1}{t}\cdot x^n\right\rangle=\left\langle\frac{t}{e^t-1}\bigg|\int_x^{x+1}u^n\mathrm{d}u\right\rangle
$$

$$
=\left\langle\frac{t}{e^t-1}\bigg|\frac{(x+1)^{n+1}-x^{n+1}}{n+1}\right\rangle=\frac{1}{n+1}\sum_{k=0}^{n}\binom{n+1}{k}B_k,
$$

这就是伯努利数的递推公式.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
$ P^* $上的算子$ T $是$ P $上中某个算子的伴随当且仅当$ T $连续, 也就是说, 线性同态

$$
\times:L(P)\to L(P^{*})
$$

的像是所有连续算子组成的线性子空间.
</div>

既然伴随$ \times $是从$ :L(P) $到$ L(P^*) $中所有连续算子组成的子空间的同构, 自然的想法是考虑该映射下$ L(P) $中各种类型元素的对应关系, 事实上, 先前介绍的$ L(P) $中两类重要的算子, 哑算子和哑移位, 在该映射下的像恰好分别是$ P^* $上自同构算子和满导数算子.

假设$ \lambda\in L(P) $将$ x^n $映为$ p_n(x) $, $ \{p_n(x)\} $是二项式型多项式列, 并且有$ f(t)\in P^* $,

$$
\langle \left(f(t)\right)^k|p_n(x)\rangle=n!\delta_{nk}
$$

对任意非负整数$ n $和$ k $成立, 此后将明确了$ f $的哑算子$ \lambda $记为$ \lambda_f $.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
算子$ \lambda\in L(P) $是哑算子当且仅当其伴随$ \lambda^\times $是$ P^* $上自同构算子.
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>证明</b>
假设$ \lambda=\lambda_f $将$ x^n $映为$ p_n(x) $, 则有

$$
\langle\lambda_f^\times(f(t)^k)|x^n\rangle=\langle f(t)^k|\lambda_f(x^n)\rangle=\langle f(t)^k|p_n(x)\rangle=n!\delta_{kn}=\langle t^k|x^n\rangle,
$$

这就是说, $ \lambda^\times $将$ f(x)^k $映为$ t^k $对任意非负整数$ k $都成立, 已知伴随像都是连续算子, 所以对任意$ g(t)\in P^* $, 都有

$$
\lambda^\times(g(f(t)))=g(t),
$$

假设$ f $的逆是$ \bar{f} $, 则

$$
\lambda^\times(g(t)=g(\bar{f}(t)),
$$

这说明

$$
\times:\lambda_f\mapsto\left[\lambda_f^\times:g(t)\mapsto g(\bar{f}(t)),g\in P^*\right],
$$

并且显然

$$
\lambda_f^\times(g(t)h(t)) = g(\bar{f}(t))h(\bar{f}(t))=\lambda_f^\times(g(t))\lambda_f^\times(h(t)),
$$

所以$ \lambda_f^\times $是代数自同构.

如果$ \lambda^\times $是自同构算子, 则它是满射, 故存在幂级数$ f $使得$ \lambda^\times(f(t))=t $, 由之前的讨论知一定存在二项式型多项式列$ \{p_n(x)\} $使得

$$
\langle \left(f(t)\right)^k|p_n(x)\rangle=n!\delta_{nk}
$$

对任意非负整数$ n $和$ k $成立, 故有

$$
\langle f(t)^k|\lambda(x^n)\rangle=\langle\lambda^\times(f(t)^k)|x^n\rangle=n!\delta_{kn}=\langle t^k|x^n\rangle=\langle f(t)^k|p_n(x)\rangle,
$$

由唯一性知

$$
\lambda(x^n)=p_n(x),
$$

所以算子$ \lambda\in L(P) $是哑算子.
</div>

设$ \lambda_f $和$ \lambda_g $是哑算子, 并且$ \lambda_f(x^n)=p_n(x) $, $ \lambda_g(x^n)=q_n(x) $, 则它们的复合$ \lambda_f\circ\lambda_g(x^n)=\lambda_fq_n(x)=(q\circ p)_n(x) $是哑复合, 先前已说明二项式型多项式列在哑复合下构成群, 所以哑算子在算子复合下也构成群, 并且与$ \mathbb{B} $同构. 另一方面, 还有$ \lambda_f\circ\lambda_g=\lambda_{g\circ f} $, 其中下标是幂级数的复合, 这是因为二者的生成函数分别是$ e^{x\bar{f}(t)} $和$ e^{x\bar{g}(t)} $, 哑复合的生成函数就是$ e^{x\bar{f}(\bar{g}(t))}=e^{x\overline{g\circ f}(t)} $, 其中$ \bar{f} $是$ f $的复合逆, 所以还有$ \lambda_f^{-1}=\lambda_{\bar{f}} $.

因为谢弗多项式列在哑复合下也构成群, 所以谢弗算子在算子下也构成群, 并且同构于$ \mathbb{S} $. 假设$ \lambda\in L(P) $将$ x^n $映为$ p_n(x) $, $ \{p_n(x)\} $是谢弗多项式列, 并且有$ f(t),g(t)\in P^* $,

$$
\langle g(t)\left(f(t)\right)^k|p_n(x)\rangle=n!\delta_{nk}
$$

对任意非负整数$ n $和$ k $成立, 此后将明确了$ f $和$ g $的谢弗算子$ \lambda $记为$ \lambda_{f,g} $, 由生成函数易知有

$$
\lambda_{f,g}=\frac{1}{g(t)}\circ\lambda_{1,f}=\frac{1}{g(t)}\circ\lambda_f,
$$

即谢弗算子一定与哑算子差一个由可逆幂级数定义的线性算子, 并且有

$$
\lambda_{f,g}\circ\lambda_{h,k}=\lambda_{g\cdot h\circ f,k\circ f},
$$

其中$ \circ $是幂级数复合, $ \cdot $是幂级数乘法, 故有$ \lambda_{f,g}^{-1}=\lambda_{\frac{1}{g}\circ\bar{f},\bar{f}} $.

与之类似, 可以证明如下定理:

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
算子$ \theta\in L(P) $是哑移位当且仅当其伴随$ \lambda^\times $是$ P^* $上满的导数算子.
</div>

如果哑移位$ \theta (p_n(x))=p_{n+1}(x) $, 有$ \langle \left(f(t)\right)^k|p_n(x)\rangle=n!\delta_{nk} $成立时将其记为$ \theta_f $, 有$ \langle g(t)\left(f(t)\right)^k|p_n(x)\rangle=n!\delta_{nk} $成立时则记作$ \theta_{f,g} $, 那么有

$$
\theta_f^\times(f(t)^k)=kf(t)^{k-1}
$$

对所有正整数$ k $成立, 还有

$$
\theta_{f,g}=\frac{1}{g(t)}\theta_f(g(t))
$$

伴随$ \times $将所有哑移位组成的集合映为所有满导数算子组成的集合, 一般记$ \theta_f^\times=D_f $.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
若$ \theta\in L(P) $是哑移位, 那么对任意$ f(t)\in P^* $, 有

$$
\theta^\times f(t)=f(t)\circ\theta-\theta\circ f(t).
$$
</div>

例如, 如果$ \theta_t(x^n)=x^{n+1} $, 那么记$ \theta^\times_t=D_t $, 有

$$
f'(t)=D_t(f(t))=f(t)\circ\theta_t-\theta_t\circ f(t)=f(t)\circ x-x\circ f(t),
$$

两边均为$ P $上的算子, 最后一个等号是因为$ \theta_t $作用在多项式上等价于给多项式乘$ x $.

若$ \theta_{f,g} $是谢弗移位, 则有

$$
\theta_{f,g}=\frac{1}{g(t)}\circ\theta_f\circ g(t).
$$

# 总结

哑演算的理论并不是解释为什么哑演算有时是正确的, 而是找出哑演算在什么时候是正确的, 我们工作的主要舞台是复数域(实际上可以是任意域)上的一元多项式代数$ \mathbb{C}[x] $(因此不需要考虑收敛), 简写为$ \mathbb{C}[x]=P $, $ P $的对偶空间, 也就是所有线性泛函组成的空间, 同构于复数域上的形式幂级数代数$ \mathbb{C}[[t]] $, 即$ P^*\cong\mathbb{C}[[t]] $, 其中的形式幂级数

$$
f(t) = \sum_{k=0}^{\infty} \frac{a_k}{k!} t^k
$$

有两种功能, 一种是作为线性泛函, 写作

$$
\langle f(t)|x^n\rangle=a_n,
$$

另一种是作为$ P $上的线性变换, 也就是将$ \mathbb{C}[[t]] $看作$ L(P) $的子集, 写作左乘作用

$$
f(t)\cdot x^n=\sum_{k=0}^{n}\binom{n}{k} a_kx^{n-k},
$$

这里我们仅写了在$ x^n $上作用的结果, 因为$ \{x^n\} $是$ P $的一组基, 由线性性, 知道在它们上的作用结果就能确定在$ P $里任意多项式上的作用结果, 二者以

$$
\langle f(t)|p(x)\rangle=\langle1|f(t)\cdot p(x)\rangle
$$

相关联.

接下来考察$ P $上线性变换$ \lambda $在$ x^n $上的像, 假设$ \lambda(x^n)=p_n(x) $, 我们重点关注$ \{p_n(x)\} $分别是阿佩尔多项式列, 二项式型多项式列和谢弗多项式列的情形, 其中前二者是后者的子集.

有两种方式生成$ P $上的线性变换, 第一种是$ \lambda(x^n)=f(t)\cdot x^n=p_n(x) $, 线性变换将$ x^n $映为阿佩尔多项式列当且仅当该线性变换可以由这种方式生成, 其中$ f(t) $是这个阿佩尔多项式列的生成函数$ f(t)e^{xt} $在$ x=0 $处的值. 全体阿佩尔多项式列组成的集合记作$ \mathbb{A} $, 它在加法, 数乘和哑复合下构成一个$ \mathbb{C} $代数, 它与全体可逆幂级数在加法, 数乘和乘法下构成的$ \mathbb{C} $代数同构, 也与全体将$ x^n $映为阿佩尔多项式列的线性变换在加法, 数乘和复合构成的$ \mathbb{C} $代数同构. 对于将$ x^n $映为阿佩尔多项式列$ B_n(x) $的线性变换, 记

$$
B^n=\langle f(t)|x^n\rangle=\langle1|f(t)\cdot x^n\rangle=\langle1|p_n(x)\rangle=B_n(0),
$$

称$ B=B^1 $为这个阿佩尔多项式列对应的哑元, 显然有

$$
B^nB^m=\langle f(t)|x^{n+m}\rangle=B^{n+m},B^n+B^m=\langle f(t)|x^n+x^m\rangle,
$$

哑元的数乘定义为$ (kB)^n=\langle kf(t)|x^n\rangle=kB^n $, 哑元间加法定义为$ (B+E)^n=\langle f(t)+g(t)|x^n\rangle=B^n+E^n $, 哑元之间的乘法定义为$ (BE)^n=(EB)^n=\langle f(t)g(t)|x^n\rangle $, 哑元在加法, 数乘和乘法下构成一个$ \mathbb{C} $代数, 并且也与$ \mathbb{A} $同构, 即有交换代数同构

$$
\mathbb{A}\cong(P^*,+,\cdot)^\times\cong\left(\{\lambda:x^n\mapsto  p_n(x) | p_n(x)\text{是阿佩尔多项式列}\},+,\circ\right)\cong\left(\{B|B\text{是哑元}\},+,\cdot\right).
$$

对于多项式$ p(x)=\sum_{n=0}p_nx^n\in P $, 定义$ p(B)=\sum_{n=0}p_nB^n $, 对任意哑元可以定义哑元代数上的一个算子, 例如$ B $对应的算子依然记为$ B $, 作用在$ E $上得到的就是

$$
B(E)=BE, B(E^n)=(BE)^n,
$$

如果$ B^n=\langle 1| f(t)\cdot x^n\rangle $, 那么$ B(p(E))=p(BE)=[f(t)\cdot p(x)]_{x=E} $.

举几个例子, 如果哑元$ V_y $由$ f_y(t)=e^{yt} $定义, 那么$ f_y(t)\cdot p(x)=p(x+y) $, 故$ V_y(E^n)=(E+y)^n=E_n(y) $对任意哑元$ E $和任意正整数$ n $成立.

如果哑元$ D $由$ f(t)=t $定义, 那么$ f(t)\cdot p(x)=p'(x) $, 故$ D(E^n)=nE^{n-1} $对任意哑元$ E $和任意正整数$ n $成立. 将$ V_y $和$ D $复合, 就有$ nE_{n-1}(y)=(V_yD)(E^n)=(DV_y)(E^n)=E_n'(y) $.

如果哑元$ \Delta $由$ f(t)=e^t-1 $定义, 那么$ f(t)\cdot p(x)=p(x+1)-p(x) $, 故$ \Delta(E^n)=(E+1)^n-E^n $对任意哑元$ E $和非负整数$ n $成立.

只要按以上规则对哑元进行运算, 并正确解释其含义, 就能得到正确的结论.

另一种生成$ P $上的线性变换的方式是, 定义$ \lambda_{f,g}(x^n) $等于满足$ \langle g(t)\left(f(t)\right)^k|p_n(x)\rangle=n!\delta_{nk} $的谢弗多项式列$ p_n(x) $, 这种生成方式实际上包含了上一种方式, 因为$ \lambda_{t,\frac{1}{g}} $就是将$ x^n $映为阿佩尔多项式列$ g(t)\cdot x^n $的线性变换.

线性变换的伴随将$ L(P) $中的元素映为$ L(P^*) $中的连续算子, 记所有连续算子组成的集合在加法, 数乘和复合下构成的$ \mathbb{C} $代数为$ CL(P^*) $, 则有代数同构

$$
L(P)\cong CL(P^*)^{op},
$$

其中上标$ op $代表反乘法下的反环.

一个重要的子集是哑算子$ \lambda_{f,1} $, 它将$ x^n $映为二项式型多项式列, 设二项式行列式列在哑复合下构成的非交换群为$ \mathbb{B} $, 那么它同构于所有将$ x^n $映为二项式型多项式列的线性变换在反复合下构成的群, 也由伴随同构于$ \mathrm{Aut}(P^*) $在复合下构成的群, 由于每个将$ x^n $映为二项式型多项式列的线性变换$ \lambda_{f,1} $都对应一个存在复合逆的幂级数$ f $, 所以$ \mathbb{S} $在还同构于$ (P^*,\circ)^\times $, 即有非交换群同构

$$
\mathbb{B}\cong \left(\{\lambda:x^n\mapsto p_n(x)|p_n(x)\text{是二项式型多项式列\}},\circ\right)^{op}\cong\mathrm{Aut}(P^*)\cong(P^*,\circ)^\times.
$$

设$ \mathbb{S} $是全体谢弗多项式列, 则有群同构

$$
\mathbb{S}\cong\left(\{\lambda:x^n\mapsto p_n(x)|p_n(x)\text{是谢弗多项式列\}},\circ\right)^{op}
$$

因为$ \lambda_{f,g} $是谢弗算子, 则$ \lambda_{f,g}=\frac{1}{g(t)}\circ\lambda_f $说明有群同构

$$
\mathbb{S}\cong\mathbb{A}\rtimes\mathbb{B}\cong(P^*,\cdot)^\times\rtimes(P^*,\circ)^\times.
$$

另一个重要的子集是哑移位$ \theta $, 它将第$ n $个二项式型多项式映为第$ n+1 $个二项式型多项式列, 如果记$ P^* $上所有满的导数算子组成的线性空间是$ \mathrm{SDer}(P^*) $, 则有线性空间的同构

$$
(\theta,+)\cong \left(\mathrm{SDer}(P^*),+\right).
$$

如果$ \theta $, 它将第$ n $个谢弗多项式映为第$ n+1 $个谢弗多项式列, 则$ \theta $是谢弗移位, 则有, $ \theta_{f,g}=\frac{1}{g(t)}\circ\theta_f\circ g(t) $, 这说明在$ \mathrm{End}(P) $内, 所有谢弗移位组成的集合恰好就是$ \mathbb{A} $在所有哑移位组成的集合上的共轭作用.

以上结论用图可以表示为:

\begin{tikzpicture}[
    box/.style={draw, rectangle, align=center, inner sep=5pt, text width=2.5cm},
    circ/.style={draw, circle},
    >=Stealth
]
    \node[circ, minimum width=5cm, minimum height=5cm] (L) at (0,0) {L(P)};
    
    \node[box] (U_ops) at ($(L.center) + (0, 1)$) { $P$上的哑算子};
    
    \node[box] (U_shifts) at ($(L.center) + (0, -1)$) {$P$上的哑移位};
    
    \node[circ, minimum width=6cm, minimum height=6cm, right=2cm of L, label={below:$L(P^*)$}] (R) {};
    
    \node[circ, minimum width=5cm, minimum height=5cm, at=(R.center)] (R_in) {$CL(P^*)$};
    
    \node[box, text width=2cm] (Auto) at ($(R_in.center) + (0, 1)$) {$\mathrm{Aut}(P^*)$};
    
    \node[box, text width=2cm] (Deriv) at ($(R_in.center) + (0, -1)$) {$\mathrm{SDer}(P^*)$};
    
    \draw[->] (U_ops.east) -- (Auto.west) node[midway, above, font=\small] {};
    \draw[->] (U_shifts.east) -- (Deriv.west);
    \draw[->] (L.east) -- (R_in.west) node[midway, above, font=\small] {$\lambda \to \lambda^\times$};
\end{tikzpicture}
