---
layout: post
title: "素数通项公式"
subtitle: ""
header-img: "img/post-bg-infinity.jpg"
header-mask: 0.3
math: true
tags:
  - 数论
---

本文我们将讨论几种素数通项公式, 即$p(n)=p_n$为第$n$个素数, 这里我们认为$1$不是素数. 

按照习惯, 我们记$p_k$为第$k$个素数, 记$\pi(n)$为小于等于$n$的素数个数, 记$\chi(n)$为素数数列的特征函数, 即

$$
\chi(n)=  \left\{\begin{matrix} 
  1, & \text{n为素数};\\ 
  0, &\text{n不为素数}
\end{matrix}\right.    
$$

$[x]$为取整函数或高斯函数, 即小于等于$x$的最大整数.

# 不存在多项式作为素数通项公式

我们知道, Euler曾试图使用函数$f(n)=n^2+n+41$生成素数, 当$n$小于40时, $f(n)$都是素数, 否则则不一定. 事实上, 我们可以证明任何一个多项式都不可能是素数通项公式, 更进一步的, 任何一个非常数多项式在正整数处的值不可能都为素数.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
任何一个非常数多项式在正整数处的值不可能都为素数.
</div>
<div style="border: 3px solid #000; padding: 10px;">
<b>证明</b>
若存在多项式 $P(x)$, 使得 $P(n)=p_i$ 为素数, 那么显然 $P(n)\equiv 0\mod p_i$, 从而 $P(n+p_i)\equiv 0\mod p_i$, 故 $P(n+p_i)$ 要么不是素数, 要么等于 $p_i$.
</div>

实际上, 在所有正整数处的值都为素数的代数函数也只有常函数, 见[19].

但是, 通过丢番图集的理论, 可以使用多元多项式生成素数, 见[10].

# 素数通项公式

## 使用常数生成素数

我们需要Bertrand's postulate, 也叫Bertrand–Chebyshev定理.

<div style="border: 3px solid #000; padding: 10px;">
<b>引理(Bertrand–Chebyshev定理)</b>
对于所有大于$1$的整数$n$, 至少存在一个质数$p$, 满足$n < p < 2n$.
</div>

 Dylan Fridman等人给出了一种构造方法.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Fridman公式)</b>
令$f_1=2.920050977316\cdots$, 且有递推公式

$$
\displaylines{f_{n+1}=[f_n](f_n-[f_n]+1)}
$$

则$p_n=[f_n]$.

这里,

$$
\displaylines{f_1=\sum_{k=1}^\infty\dfrac{p_k-1}{\prod\limits_{i=1}^{k-1}p_i}}
$$
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>证明</b>
首先证明$f_1$收敛, 由Bertrand–Chebyshev定理可知, $p_{n-1}<p_{n}<2p_{n-1}-1$, 从而

$$
\displaylines{
f_1=(p_1-1)+\dfrac{p_2-1}{p_1}+\dfrac{p_3-1}{p_1p_2}+\dfrac{p_3-1}{p_1p_2p_3}+\cdots \\
< p_1-1+\dfrac{2p_1-2}{p_1}+\dfrac{2p_2-2}{p_1p_2}+\dfrac{2p_3-2}{p_1p_2p_3}+\cdots \\
= 2-1+2-\dfrac{2}{p_1}+\dfrac{2}{p_1}-\dfrac{2}{p_1p_2}+\dfrac{2}{p_1p_2}-\dfrac{2}{p_1p_2p_3}+\cdots \\
= 3
}
$$

故$f_1$存在, 且$\left[f_1\right]=2=p_1$.

定义$f_n=\begin{pmatrix}f_1-\sum\limits_{k=1}^{n-1}\dfrac{p_k-1}{\prod\limits_{i=1}^{k-1}p_i}\end{pmatrix}\prod\limits_{i=1}^{n-1}p_i=(p_n-1)+\dfrac{p_{n+1}-1}{p_n}+\dfrac{p_{n+2}-1}{p_np_{n+1}}+\dfrac{p_{n+2}-1}{p_np_{n+1}p_{n+2}}+\cdots$, 
则有$f_{n}=p_{n-1}(f_{n-1}-p_{n-1}+1)$.

再使用一次Bertrand–Chebyshev定理, 有

$$
\displaylines{f_n>(p_n-1)+\dfrac{p_n-1}{p_n}+\dfrac{p_{n+1}-1}{p_np_{n+1}}+\dfrac{p_{n+2}-1}{p_np_{n+1}p_{n+2}}+\cdots}
$$

和

$$
\displaylines{f_n<(p_n-1)+\dfrac{2p_n-2}{p_n}+\dfrac{2p_{n+1}-2}{p_np_{n+1}}+\dfrac{2p_{n+2}-2}{p_np_{n+1}p_{n+2}}+\cdots}
$$

故$p_n<f_n<p_n+1$, 即$[f_n]=p_n$.

则数列$\{f_n\}$可由递推公式

$$
\displaylines{f_{n+1}=[f_n](f_n-[f_n]+1)}
$$

生成.
</div>

1952年, Sierpiński提出,

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Sierpiński公式)</b>
设$A=0.02030005000000070\cdots$, 则有

$$
\displaylines{p_n=[10^{2^n} A]-10^{2^{n-1}}[10^{2^{n-1}} A]}
$$

这里,

$$
\displaylines{A=\sum_{m=1}^\infty p_m 10^{-2^m}}
$$
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>证明</b>
$A$显然收敛, 因为$p_m<2^{2^m}=4^{2^{m-1}}$, 故有

$$
\displaylines{
0<10^{2^{m}} \sum_{m=n+1}^{\infty} p_{m} 10^{-2^{m}}<\sum_{m=n+1}^{\infty} 4^{2^{m-1}} 10^{-2^{m-1}} \\
=\sum_{m=n+1}^{\infty}\left(\frac{2}{5}\right)^{2^{m-1}}<\left(\frac{2}{5}\right)^{2^{n}} \frac{1}{\left(1-\frac{2}{5}\right)}<\frac{4}{15}<1
}
$$

从而有

$$
\displaylines{\left[10^{2^{n}} A\right]=10^{2^{n}} \sum_{m=1}^{n} p_{m} 10^{-2^{m}}}
$$

类似地,

$$
\displaylines{\left[10^{2^{n-1}} A\right]=10^{2^{n-1}} \sum_{m=1}^{n-1} p_{m} 10^{-2^{m}}}
$$

从而

$$
\displaylines{
\left[10^{2^{n}} A\right]-10^{2^{n-1}}\left[10^{2^{n-1}} A\right]=10^{2^{n}}\left(\sum_{m=1}^{n} p_{m} 10^{-2^{m}}-\sum_{m=1}^{n-1} p_{m} 10^{-2^{m}}\right)=p_{n}
}
$$
</div>

1950年, Moser提出,

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Moser公式)</b>
设$\gamma= 0.203005000700011\cdots$, 则有

$$
\displaylines{p_n=\left[\gamma \cdot 10^{\frac{n(n+1)}{2}}\right]-10^n \left[\gamma \cdot 10^{\frac{n(n-1)}{2}}\right]}
$$

这里,

$$
\displaylines{\gamma=\sum_{m=1}^\infty p_m 10^{-\frac{m(m+1)}{2}}}
$$
</div>

1952年, Bang提出,

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Bang公式)</b>
设

$$
\displaylines{a=\sum_{m=1}^\infty p_m 10^{-m^2}}
$$

则有

$$
\displaylines{p_n=\left[10^{2n-1}\left(a\cdot10^{(n-1)^2}-\left[a\cdot10^{(n-1)^2}\right]\right)\right]}
$$
</div>

Hardy和Wright则更进一步,

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Hardy-Wright公式)</b>
对于任意大于$1$的整数$r$, 设

$$
\displaylines{B=\sum_{m=1}^\infty p_m r^{-m^2}}
$$

则有

$$
\displaylines{p_n=[r^{n^2} B]-r^{2n-1} [r^{(n-1)^2} B]}
$$
</div>

Knopfmacher给出了另一种不同的方法.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Knopfmacher公式)</b>
$$
\displaylines{p_n=\left[1-\log_y\left(1-\dfrac{A_y}{(1-y^{-2})(1-y^{-3})\cdots(1-y^{-p_{n-1}})}\right)\right],y>3}
$$
这里$A_y=\prod\limits_{i=1}^\infty(1-y^{-p_i})<1$.
</div>

证明见[13].

这类公式有一个明显的缺陷, 当我们计算$p_n$时, 需要提前计算一个包含了素数信息的常数值, 而计算这个常数的精确值又需要所有素数的值, 所以这类公式实际上是无法使用的.


## 利用$\pi(n)$或$\chi(n)$

这类公式使用素数的各种性质来构造函数, 其中有两个重点, 一是构造出 $\pi(n)$ 或 $\chi(n)$, 二是从 $\pi(n)$ 构造 $p_n$, 使用不同的构造方法, 就能得到不同的通项公式. 显然, 当我们已经构造出 $\chi(n)$ 后, 就可以直接写出 $\pi(n)$, 即
$$
\pi(n)=\sum_{k=2}^n \chi(k),
$$

如果 $\chi(n)$ 可以解析延拓使得积分
$$
\frac{1}{2\pi i}\int_C\frac{(1-\chi(x))'}{1-\chi(x)}\mathrm{d}x,
$$

有意义的话, 上式的值也将等于 $\pi(x)$. 这里围道 $C$ 取包含 $x$ 轴上从 $1$ 到 $x$ 函数 $1-\chi(x)$ 的所有零点.

顺便插一句, 由 $\chi(x)$ 可以直接写出素数的递推公式,
$$
p_{n+1}=p_n+1+\sum_{m=p_n+1}^{2p_n}\prod_{i=p_n+1}^m(1-\chi(i)).
$$

首先来看基于 Wilson 定理的公式.

<div style="border: 3px solid #000; padding: 10px;">
<b>引理(Wilson定理)</b>
$n$ 是素数当且仅当
$$(n-1)!\equiv -1\mod n.$$
</div><br>
我们先推导著名的 Willans 公式.
<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Willans公式)</b>
$$
p_n=1+\sum_{m=1}^{2^n}\left[\begin{pmatrix}\dfrac{n}{\sum\limits_{k=1}^m\left[\cos^2\pi\dfrac{(k-1)!+1}{k}\right]}\end{pmatrix}^{\frac{1}{n}}\right].
$$
</div>

由 Wilson 定理知 $n$ 是素数当且仅当 $\dfrac{(n-1)!+1}{n}$ 是整数, 于是 $\cos\pi\dfrac{(n-1)!+1}{n}$ 当且仅当 $n$ 是素数时值为 $\pm1$, 否则其值属于 $(-1,1)$, 平方再取整后, 即可得到
$$
\left[\cos^2\pi\dfrac{(n-1)!+1}{n}\right]=\chi(n),n>1.
$$
但是 $n=1$ 时, 上式左边值为 $1$, 右边为 $0$, 我们需要稍作调整,
$$
\pi(n)=-1+\sum_{k=1}^n\left[\cos^2\pi\frac{(k-1)!+1}{k}\right].
$$

接着, Willans 给出一个函数 $A_n(a)=\left[\sqrt[n]{\dfrac{n}{1+a}}\right], n\in \mathbb Z_{>0},a\in \mathbb Z_{\ge0}$, 当 $a<n$ 时, $1\le\dfrac{n}{1+a}\le n$, $1\le\sqrt[n]{\dfrac{n}{1+a}}\le\sqrt[n]{n}<2$, 故 $A_n(a)=1$. 当 $a\ge n$ 时, $0<\sqrt[n]{\dfrac{n}{1+a}}<1$, 故 $A_n(a)=0$. 即
$$
A_n(a)=\begin{cases}
1, & a<n\\
0, &a\ge n
\end{cases}
$$

因为给定自然数 $n$， 满足 $\pi(m)<n$ 的 $m$ 的个数就是 $p_n-1$， 将 $A_n(a)$ 与 $\pi(n)$ 复合即可得到素数通项公式
$$
p_n=1+\sum_{m=1}^N A_n(\pi(m)).
$$
这里 $N$ 是足够大的正整数, 由 Bertrand–Chebyshev 定理可得 $p_n<2^n$ 对所有正整数 $n$ 都成立, 故可取 $N=2^n$， 整理即得,
$$
p_n=1+\sum_{m=1}^{2^n}\left[\begin{pmatrix}\dfrac{n}{\sum\limits_{k=1}^m\left[\cos^2\pi\dfrac{(k-1)!+1}{k}\right]}\end{pmatrix}^{\frac{1}{n}}\right].
$$


James P.Jones 给出了一个类似的公式.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Jones公式)</b>
$$
p_n=\sum_{m=0}^{2^n}(1\ominus ((1+\pi(m))\ominus n)).
$$
其中 $a\ominus b=\dfrac{|a-b|+a-b}{2}$.
</div>

Jones 使用模除运算给出 $\chi(n)$, 记 $a \mod b$ 为 $a$ 除以 $b$ 所得的余数, 显然由 Wilson 定理可得 $\chi(n)=((n-1)!^2\mod n)$, 此时就不需要排除 $n=1$ 处的干扰, 但该式本质上与 Willans 的式子没多大区别. 故有
$$
\pi(n)=\sum_{k=1}^n ((k-1)!^2\mod k).
$$

对于函数
$$
A_n(a)=\begin{cases}
1, & a<n\\
0, &a\ge n
\end{cases}
$$
Jones 给出了另一种构造 [4]， 他定义
$$
a\ominus b=\begin{cases}
0, & a<b\\
a-b, &a\ge b
\end{cases},
$$
即 $a\ominus b=\dfrac{|a-b|+a-b}{2}$, 则
$$
A_n(a)=1\ominus ((1+a)\ominus n).
$$

与 Willans 公式相同的方法即可证得 Jones 公式.

顺便一提, 1992 年, Tsangaris 和 Jones 合作又给出了另一个公式, 但这个公式并不是使用 Wilson 定理得到的, 证明见[24].

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Tsangaris-Jones公式)</b>
$$
\chi(n)=1\ominus\sum_{0<i<k\le [\sqrt{n}]}\left(2\left[\dfrac{in}{k}\right]-n+1\right).
$$
</div><br>
Willans 在自己的文章中还给出了几条素数通项公式.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Willans公式2)</b>
$$
p_n=\sum_{m=1}^{2^n}\left(m\left[\cos^2\pi\dfrac{(n-1)!+1}{n}\right]\left[2^{-|\pi(m)-n|}\right]\right).
$$
</div>

只需注意到
$$
B_n(a)=\left[2^{-|a-n|}\right]=\begin{cases}
1, & a=n\\
0, &a\neq n
\end{cases}
$$
即可.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Willans公式3)</b>
$$
p_n=2+\sum_{m=2}^{2^n}C_n\left(\sum_{k=2}^m\dfrac{\sin^2\pi\dfrac{(k-1)!^2}{k}}{\sin^2\dfrac{\pi}{k}}\right).
$$
其中 $C_n(a)=\sin\pi2^{y-1}, y=a^2(a-1)^2\cdots(a-n+1)^2$, $n$， $a$ 为正整数.
</div>

对于函数 $\dfrac{(n-1)!^2}{n}$， 当 $n$ 为素数时,
$$
\dfrac{(n-1)!^2}{n}=\dfrac{((n-1)!-1)((n-1)!+1)}{n}+\dfrac{1}{n}=\text{整数}+\dfrac{1}{n}.
$$
当 $n$ 不为素数时, $\dfrac{(n-1)!^2}{n}$ 为整数, 由正弦函数的性质可得
$$
\chi(n)=\dfrac{\sin^2\pi\dfrac{(k-1)!^2}{k}}{\sin^2\dfrac{\pi}{k}}, n>1.
$$

对于函数 $C_n(a)$, 由正弦函数的性质知
$$
C_n(a)=\begin{cases}
1, & a<n\\
0, &a\ge n
\end{cases}.
$$
将二者其组合起来即可.

Hardy 和 Wright 给出了另一种基于 Wilson 公式的素数通项公式.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Hardy-Wright公式)</b>
$$
p_n=1+\sum_{j=1}^{2^n}f\left(n,2+\sum_{k=5}^j\left((k-2)!-k\left[\dfrac{(k-2)!}{k}\right]\right)\right),n>4
$$
这里
$$
f(x,y)=\begin{cases}
0, & x=y\\
\dfrac{1}{2}\left(1+\dfrac{x-y}{|x-y|}\right), & x\neq y
\end{cases}
$$
</div>

由 Wilson 定理可得
$$
\pi(n)=2+\sum_{k=5}^n\left((k-2)!-k\left[\dfrac{(k-2)!}{k}\right]\right),k>4.
$$
显然
$$
f(x,y)=\begin{cases}
1, & x>y\\
0, & x\le y
\end{cases},
$$
将二者组合起来即可.

还有其它的构造方法, 仅罗列如下:

Willans公式4:
$$
\chi(n)=1-\left[\cos^2\pi\dfrac{(n-1)!^2}{n}\right].
$$

$$
\chi(n)=\dfrac{\sin^2\pi\dfrac{(n-1)!}{n}}{\sin^2\dfrac{\pi}{n}}, n>1.
$$

Tee公式:
$$
\pi(n)=1+\sum_{k=1}^{\frac{n-1}{2}}\dfrac{1-\cos\pi\dfrac{((2k+1)-1)!}{2k+1}}{1+\cos\dfrac{\pi}{2k+1}}, n>1.
$$

Papadimitriou公式:
$$
\chi(n)=\mathrm{sgn}\left(\dfrac{2(n-1)!}{n}-\left[\dfrac{2(n-1)!}{n}\right]\right), n>2.
$$
$$
\chi(n)=\mathrm{sgn}\left(\dfrac{(n-1)!}{n}-\left[\dfrac{(n-1)!}{n}\right]\right), n>1.
$$
其中 $\mathrm{sgn}$ 为符号函数,
$$
\mathrm{sgn}(x)=\begin{cases}
1, & x>0\\
0, & x=0\\
-1,&x<0
\end{cases}.
$$

Mináč公式:
$$
\pi(n)=\sum_{j=2}^n\left[\dfrac{(j-1)!+1}{j}-\left[\dfrac{(j-1)!}{j}\right]\right]
$$

如果可以使用复数的话,
$$
\chi(n)=\dfrac{e^{\frac{2\pi i(n-1)!}{n}}-1}{e^{-\frac{2\pi i}{n}}-1}.
$$

这些公式都可以用 Wilson 定理证明, 且过程完全类似. 接下来我们介绍基于 Fermat 小定理得到的素数通项公式.

<div style="border: 3px solid #000; padding: 10px;">
<b>引理(Fermat小定理)</b>
若 $p$ 是素数, $a$ 和 $p$ 互素, 则有
$$
a^{p-1}\equiv 1\mod p.
$$
</div><br>
<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Harris公式)</b>
$$
\chi(n)=\prod_{2\le p\le \sqrt{n}}\dfrac{1-\cos\left(2n^{p-1}\dfrac{\pi}{p}\right)}{1-\cos\left(\dfrac{2\pi}{p}\right)},n\ge 4,p\text{是素数}.
$$
</div>

当 $n$ 不为素数时, 则必存在一个 $p$ 是 $n$ 的因子, 则 $\cos\left(2n^{p-1}\dfrac{\pi}{p}\right)=1$, 即整个函数取整为 $0$. 当 $n$ 为素数时, 由 Fermat 小定理即得 $\cos\left(2n^{p-1}\dfrac{\pi}{p}\right)=\cos\left(\dfrac{2\pi}{p}\right)$， 乘积中每一项都为 $1$， 则整个函数值为 $1$.

乘积符号下标为 $2\le p\le \sqrt{n}$ 是因为 $n$ 除自身外最大的因子不超过 $\sqrt{n}$， 按照之前的方法将 $\chi(n)$ 转化成 $p_n$ 即可， 注意当我们计算 $p_n$ 的时候需要知道小于等于 $\sqrt{n}$ 的所有素数值.

接下来介绍的是 Stephen Regimbal 基于取整函数的性质得出的素数通项公式.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Regimbal公式)</b>
$$
p_k=\sum_{m=2}^{2^k}m\begin{bmatrix}
\dfrac{1}{1+\left|
k-\begin{bmatrix}\dfrac{1}{\sum\limits_{i=1}^{m-1}\left[\dfrac{\left[\dfrac{m}{i}\right]}{\dfrac{m}{i}}\right]}\end{bmatrix}\sum\limits_{n=2}^m\begin{bmatrix}\dfrac{1}{\sum\limits_{i=1}^{n-1}\left[\dfrac{\left[\dfrac{n}{i}\right]}{\dfrac{n}{i}}\right]}\end{bmatrix}
\right|}
\end{bmatrix}.
$$
</div>

考虑函数
$$
g(n)=\sum\limits_{i=1}^{n-1}\left[\dfrac{\left[\dfrac{n}{i}\right]}{\dfrac{n}{i}}\right]
$$
对于任意大于 $0$ 的 $x$， 当 $x$ 为整数时， $\left[\dfrac{[x]}{x}\right]=1$， 当 $x$ 不是整数时 $\left[\dfrac{[x]}{x}\right]=0$. 设 $i=1,2,\cdots, n-1$， 如果 $n$ 是素数， $\dfrac{n}{i}$ 是整数当且仅当 $i=1$， 所以
$$
\sum\limits_{i=1}^{n-1}\left[\dfrac{\left[\dfrac{n}{i}\right]}{\dfrac{n}{i}}\right]=1,
$$
如果 $n$ 不是素数， 那么必然存在不等于 $1$ 的 $i$， 使得 $\dfrac{n}{i}$ 为整数， 故
$$
\sum\limits_{i=1}^{n-1}\left[\dfrac{\left[\dfrac{n}{i}\right]}{\dfrac{n}{i}}\right]>1,
$$
给 $g(n)$ 取倒数再取整即得素数特征函数， 即
$$
\chi(n)=\begin{bmatrix}\dfrac{1}{\sum\limits_{i=1}^{n-1}\left[\dfrac{\left[\dfrac{n}{i}\right]}{\dfrac{n}{i}}\right]}\end{bmatrix}
$$

因为
$$
\chi(n)\pi(n)=\begin{cases}
\pi(n), & n\text{是素数}\\
0, & n\text{不是素数}
\end{cases}
$$
令 $k$ 是一个正整数， 则有
$$
n\left[\dfrac{1}{1+|k-\chi(n)\pi(n)|}\right]=\begin{cases}
n, & n\text{是第}k\text{个素数}\\
0, & \text{其它}
\end{cases}
$$
故
$$
p_k=\sum_{m=2}^{2^k}m\begin{bmatrix}
\dfrac{1}{1+\left|k-\begin{bmatrix}\dfrac{1}{\sum\limits_{i=1}^{m-1}\left[\dfrac{\left[\dfrac{m}{i}\right]}{\dfrac{m}{i}}\right]}\end{bmatrix}\sum\limits_{n=2}^m\begin{bmatrix}\dfrac{1}{\sum\limits_{i=1}^{n-1}\left[\dfrac{\left[\dfrac{n}{i}\right]}{\dfrac{n}{i}}\right]}\end{bmatrix}
\right|}
\end{bmatrix}.
$$

下面的公式是 Sebastián Martín Ruiz 基于除数函数 $d(n)$ 的性质构造出来的.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Ruiz公式)</b>
$$
p_n=1+\sum_{k=1}^{2([n\ln n]+1)}
\begin{bmatrix}
1-
\begin{bmatrix}
\dfrac{\sum\limits_{j=2}^k 1+
\begin{bmatrix}
-\dfrac{\sum\limits_{s=1}^j\left(\left[ \dfrac{j}{s}\right]-\left[\dfrac{j-1}{s}\right]\right)-2}{j}
\end{bmatrix}
}{n}
\end{bmatrix}
\end{bmatrix}
.
$$
</div>

设 $d(i)$ 为除数函数， 即 $i$ 的正因子的个数， 因为
$$
\left[\dfrac{i}{j}\right]-\left[\dfrac{i-1}{j}\right]=\begin{cases}
1, & j\ |\ i\\
0, & j\not|\ i
\end{cases},
$$
故
$$
d(i)=\sum_{j=1}^i \left[\dfrac{i}{j}\right]-\left[\dfrac{i-1}{j}\right].
$$

Ruiz 构造出函数
$$
-\left[-\dfrac{d(i)-2}{i}\right],i>1.
$$
当 $i$ 是素数时， 因为它只有 $1$ 和其自身两个因子， $d(i)=2$， $-\left[-\dfrac{d(i)-2}{i}\right]=0$， $i$ 不是素数时， $d(i)>2$， 从而 $0<\dfrac{d(i)-2}{i}<1$， $-\left[-\dfrac{d(i)-2}{i}\right]=1$. 故
$$
\chi(i)=1-\left(-\left[-\dfrac{d(i)-2}{i}\right]\right)=1+\left[-\dfrac{d(i)-2}{i}\right], i>1.
$$
与之前相同的,
$$
\pi(n)=\sum_{i=2}^n \chi(i).
$$

因为 $1\le k\le p_n-1$ 时， 一定有 $\left[\dfrac{\pi(k)}{n}\right]=0$， Ruiz 希望找出一个仅与 $n$ 有关的上界 $C_n$， 使得 $p_n\le k\le C_n$ 时， 有 $1\le \dfrac{\pi(k)}{n}<2$， 即 $\left[\dfrac{\pi(k)}{n}\right]=1$， 从而
$$
p_n=1+\sum_{k=1}^{C_n}\left(1-\left[\dfrac{\pi(k)}{n}\right]\right).
$$

Ruiz 选定的 $C_n$ 等于 $2([n\ln n]+1)$， 有以下两个不等式成立，
$$
p_n\le2([n\ln n]+1),
$$
$$
\pi\left(2([n\ln n]+1)\right)<2n.
$$
我们省略其证明， 由这两个不等式可以推出 $p_n\le k\le C_n$ 时， $\left[\dfrac{\pi(k)}{n}\right]=1$.

将 $C_n$ 代入并整理即得 Ruiz 的公式.

一个更简单些的方法是
$$
\chi(n)=\left[\dfrac{2}{d(n)}\right].
$$

定理 $\ref{Lamber}$ 给出了 $d(n)$ 的另一种构造方法.

除数函数有推广
$$
\sigma_x(n)=\sum\limits_{k|n}k^x,
$$
则 $d(n)=\sigma_0(n)$. 如果 $n=p_1^{a_1}p_2^{a_2}\cdots p_r^{a_r}$， 则有
$$
\sigma_x(n)=\prod\limits_{i=1}^r\dfrac{p_i^{(a_i+1)x}-1}{p_i^x-1},x>0.
$$

当 $n$ 是素数时， 它只有 $1$ 和 $n$ 两个因数， 故 $\sigma_x(n)=n^x+1$， 若 $n$ 不是素数， 则 $\sigma_x(n)>n^x+1$， 故有
$$
\chi(n)=\left[\dfrac{n^x+1}{\sigma_x(n)}\right],n>1
$$

基于 Euler $\varphi$ 函数的性质也可给出一个素数通项公式.
<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Vassilev公式)</b>
$$
\chi(n)=\begin{bmatrix}
\dfrac{n\prod\limits_{p|n}\left(1-\dfrac{1}{p}\right)}{n-1}
\end{bmatrix},n>1.
$$
</div>

因为 Euler $\varphi$ 函数为小于 $n$ 的正整数中与 $n$ 互素的数的数目， $n$ 为素数时当然有 $\varphi(n)=n-1$， 从而
$$
\begin{bmatrix}
\dfrac{\varphi(n)}{n-1}
\end{bmatrix}=1.
$$
当 $n$ 不为素数时有 $\varphi(n)<n-1$， 从而
$$
\begin{bmatrix}
\dfrac{\varphi(n)}{n-1}
\end{bmatrix}=0.
$$

初等数论中有公式 $\varphi(n)=n\prod\limits_{p|n}\left(1-\dfrac{1}{p}\right)$， 将其代入即得
$$
\chi(n)=\begin{bmatrix}
\dfrac{n\prod\limits_{p|n}\left(1-\dfrac{1}{p}\right)}{n-1}
\end{bmatrix},n>1.
$$

再把 $\chi(n)$ 按照之前的方法转化成 $p_n$ 即可得到素数通项公式， 通过这个公式计算第 $n$ 个素数时， 需要提前知道小于等于 $n$ 的所有素数.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Ortega Costa公式)</b>
$$
\pi(n)=n-\dfrac{1}{2\pi}\int_0^{2\pi}\sum_{m=1}^n\cos\left(x\prod_{1\le j,k\le m-1}(jk-m)\right)\dd x.
$$
</div>
<div style="border: 3px solid #000; padding: 10px;">
<b>证明</b>
注意到 $m$ 为合数时 $\prod\limits_{1\le j,k\le m-1}(jk-m)=0$， $m$ 为素数时， $\prod\limits_{1\le j,k\le m-1}(jk-m)$ 等于一个整数， 故
$$
\dfrac{1}{2\pi}\int_0^{2\pi}\sum\limits_{m=1}^n\cos\left(x\prod\limits_{1\le j,k\le m-1}(jk-m)\right)\dd x
$$
实际上就是小于等于 $n$ 的合数的数量， 故
$$
\pi(n)=n-\dfrac{1}{2\pi}\int_0^{2\pi}\sum_{m=1}^n\cos\left(x\prod_{1\le j,k\le m-1}(jk-m)\right)\dd x.
$$
将 $\pi(n)$ 按照之前的方法转化成 $p_n$ 即可.
</div><br>
一个类似的公式是 Wormell 公式.
<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Wormell公式)</b>
$$
\pi(n)=\sum_{m=2}^n\dfrac{1+(-1)^{2^{B(m)}}}{2}.
$$
这里 $B(m)=\prod\limits_{1\le j,k\le m-1}(jk-m)^2.$
</div><br>
1953 年, Sierpiński 提出下面这个包含极限的公式, 但这里的极限也可以设法用取整函数代替.
<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Sierpiński公式)</b>
$$
\pi(n)=1+\sum_{k=3}^n \left(
1-\lim_{m\to\infty}\left(
1-\prod_{j=2}^{k-1}\sin^2\left(\dfrac{k\pi}{j}\right)
\right)^m
\right),n\ge3.
$$
</div>
<div style="border: 3px solid #000; padding: 10px;">
<b>证明</b>
对于 $j=2,3,\cdots,k-1$， 当 $k$ 为素数时， $\dfrac{k}{j}$ 都不是整数， 故 $\prod\limits_{j=2}^{k-1}\sin^2\left(\dfrac{k\pi}{j}\right)$ 中每一项都不为 $0$， $\left(1-\prod\limits_{j=2}^{k-1}\sin^2\left(\dfrac{k\pi}{j}\right)\right)\in(0,1)$. 当 $k$ 不为素数时， 存在 $j$ 使得 $\dfrac{k}{j}$ 是整数， 故 $\prod\limits_{j=2}^{k-1}\sin^2\left(\dfrac{k\pi}{j}\right)=0$， 从而有
$$
\chi(k)= 1-\lim_{m\to\infty}\left(
1-\prod_{j=2}^{k-1}\sin^2\left(\dfrac{k\pi}{j}\right)
\right)^m,k\ge3.
$$
故
$$
\pi(n)=1+\sum_{k=3}^n \left(
1-\lim_{m\to\infty}\left(
1-\prod_{j=2}^{k-1}\sin^2\left(\dfrac{k\pi}{j}\right)
\right)^m
\right),n\ge3.
$$
</div>

2012 年, Kaddoura 和 Abdul-Nabi 基于模 $6$ 的筛法给出下面这个公式.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Kaddoura-Abdul-Nabi公式)</b>
$$
p_{n}=3+2[n\ln n]-\sum_{x=7}^{2([n\ln n]+1)}\left(\left[\frac{1}{n}\left(4+\left(\sum_{j=1}^{\left[\frac{x-1}{6} \right] }\left[S(6 j+1)\right ]+\sum_{j=1}^{\left[\frac{x+1}{6}\right]}\left[ S(6 j-1)\right]\right)\right)\right]\right).
$$

$$
p_n=7+\sum_{x=7}^{2([n\ln n]+1)}\begin{bmatrix}
\dfrac{2}{5+n+\sum\limits_{j=1}^{\left[\frac{x-1}{6} \right] }\left[S(6 j+1)\right ]+\sum\limits_{j=1}^{\left[\frac{x+1}{6}\right]}\left[ S(6 j-1)\right]}
\end{bmatrix}
$$

其中, $S(n)=\dfrac{S_1(n)+S_2(n)}{2}$,
$$
S_1(n)=\dfrac{-1}{\left[\dfrac{\left[\sqrt{n}\right]}{6}\right]+1}\sum_{k=1}^{\left[\frac{\left[\sqrt{n}\right]}{6}\right]+1}\left[\left[\dfrac{n}{6k+1}\right]-\dfrac{n}{6k+1}\right].
$$
$$
S_2(n)=\dfrac{-1}{\left[\dfrac{\left[\sqrt{n}\right]}{6}\right]+1}\sum_{k=1}^{\left[\frac{\left[\sqrt{n}\right]}{6}\right]+1}\left[\left[\dfrac{n}{6k-1}\right]-\dfrac{n}{6k-1}\right].
$$
</div>

作者在 [11] 中首先证明了, $n$ 为与 $6$ 互素的整数时,
$$
[S(n)]=\begin{cases}
1, & n\text{是素数}\\
0, & n\text{不是素数}
\end{cases}
$$
因为素数只可能是 $6j+1$ 或 $6j-1$ 的形式, 所以
$$
\pi(n)=4+\sum\limits_{j=1}^{\left[\frac{n-1}{6} \right] }\left[S(6 j+1)\right ]+\sum\limits_{j=1}^{\left[\frac{n+1}{6}\right]}\left[ S(6 j-1)\right].
$$

然后利用函数
$$
1-\left[\dfrac{x}{n}\right]=\begin{cases}
1, & x<n\\
0, & x\ge n
\end{cases}
$$
和
$$
\left[\dfrac{2n}{x+n+1}\right]=\begin{cases}
1, & x<n\\
0, & x\ge n
\end{cases}
$$
分别可得
$$
p_n=7+\sum_{x=7}^{2([n\ln n]+1)}\left(1-\left[\dfrac{\pi(x)}{n}\right]\right)
$$
和
$$
p_n=7+\sum_{x=7}^{2([n\ln n]+1)}\left[\dfrac{2n}{\pi(x)+n+1}\right],
$$
整理即得 Kaddoura-Abdul-Nabi 公式.


## 其他方法

1971 年, J.W. Gandhi 证明了 $p_{n+1}$ 是满足下面这个不等式的唯一正整数 $t$,

$$
1<2^t\left(\sum_{d|P_n}\dfrac{\mu(d)}{2^d-1}-\dfrac{1}{2}\right)<2
$$

其中 $P_n=p_1p_2\cdots p_n$, $\mu(n)$ 为 Möbius 函数,
$$\mu(n)=\begin{cases}
1, & n=1\\
(-1)^r, & n\text{为}r\text{个不同的素数的积}\\
0,&\text{其它}
\end{cases}$$
它可以由单位根给出一个不分段的形式,

$$
\mu(n)=\sum\limits_{\substack{1\le k<n\\(k,n)=1}}e^{\frac{2\pi ik}{n}}.
$$

从而有
<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Gandhi公式)</b>

$$
p_{n+1}=\left[1-\log_2 \left(\sum_{d|P_n}\dfrac{\mu(d)}{2^d-1}-\dfrac{1}{2}\right)\right].
$$
</div>

证明见 [5,27].

Golomb 在 1976 年得到了一个定理, 这个定理的一种特殊情况可以直接推出 Gandhi 的不等式, 这个定理也将以下四个公式作为其特殊情况, 详细证明见[29].

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Golomb公式)</b>

$$
p_{n+1}=\lim_{s\to\infty}\left(P_n(s)\zeta(s) -1\right)^{-\frac{1}{s}}
$$

$$
p_{n+1}=\lim_{s\to\infty}\left(P_n(s) -\dfrac{1}{\zeta(s)}\right)^{-\frac{1}{s}}
$$

$$
p_{n+1}=\lim_{s\to\infty}\left(\zeta(s) -\dfrac{1}{P_n(s)}\right)^{-\frac{1}{s}}
$$

$$
p_{n+1}=\lim_{s\to\infty}\left(1 -\dfrac{1}{P_n(s)\zeta(s)}\right)^{-\frac{1}{s}}
$$
</div>

其中 $P_n(s)=\prod\limits_{p_i|P_n}(1-p_i^{-s})$, $P_n=p_1p_2\cdots p_n$, $\zeta(s)=\sum\limits_{n=1}^\infty\dfrac{1}{n^s}$ 为 Riemann $\zeta$ 函数.

这四个公式也可以用 Euler 乘积公式直接证明, 举例明之.
$$\displaylines{
P_n(s)\zeta(s)=\left(\prod\limits_{p_i|P_n}(1-p_i^{-s})\right)\left(\sum\limits_{n=1}^\infty\dfrac{1}{n^s}\right)\\
=\left(\prod\limits_{i=1}^n(1-p_i^{-s})\right)\left(\prod\limits_{j=1}^\infty(1-p_j^{-s})^{-1}\right)\\
=\prod\limits_{j=n+1}^\infty(1-p_j^{-s})^{-1}.
}$$

而 $s\to\infty$ 时, $\prod\limits_{j=n+1}^\infty(1-p_j^{-s})^{-1}\sim1+p_{n+1}^{-s}$, 故

$$
p_{n+1}=\lim_{s\to\infty}\left(P_n(s)\zeta(s) -1\right)^{-\frac{1}{s}}.
$$
\qed

Lambert 级数是数论常见的一个工具, 其定义为
$$
F(x)=\sum_{n=1}^\infty a_n\dfrac{x^n}{1-x^n}.
$$

其中 $a_n$ 是算数函数. 当 $0\le x<1$ 时, 这类级数都绝对收敛. Lambert 级数里有一个几何级数, 将其展开即得
$$
F(x)=\sum_{n=1}^\infty \left(a_n\sum_{m=1}^\infty x^{mn}\right)=\sum_{k=1}^\infty b_k x^k,
$$

其中

$$
b_k=\sum_{n|k}a_n.
$$

取 $a_n=\mu(n)$ 时, 因为

$$
\sum_{n|k}\mu(n)=\left[\dfrac{1}{k}\right],
$$
有

$$
\sum_{n=1}^\infty \dfrac{\mu(n)x^n}{1-x^n}=x,
$$

$x$ 取 $\dfrac{1}{2}$ 即得

$$
\sum_{n=1}^\infty \dfrac{\mu(n)}{2^n-1}-\dfrac{1}{2}=0.
$$

Golomb 在 1992 年利用 Lambert 级数又给出了 Gandhi 公式 [28] 的另一个证明, 详见.

当我们取 $a_n=1$ 时,

$$
b_k=\sum_{n|k}1=d(k),
$$

则 $\sum\limits_{n=1}^\infty \dfrac{x^n}{1-x^n}$ 的展开式中, $x$ 的系数是 $1$, $x$ 的素数次方项的系数全为 $2$, 其它的系数全大于 $2$, Lambert 早在 1771 年就发现了这个事实 [14].

所以我们有:

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Lambert公式)</b>

$$
d(k)=\left.\left(\dfrac{1}{k!}\dfrac{\mathrm{d}^k}{\mathrm{d}x^k}\left(\sum\limits_{n=1}^\infty \dfrac{x^n}{1-x^n}\right)\right)\right|_{x=0}, k>1
$$
</div>

按照定理 $\ref{ruiz}$ 的方法将其转化为 $p_k$ 即可.\qed

1955 年, Teuffel 利用 Riemann $\zeta$ 函数给出了一个素数通项公式.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Teuffel公式)</b>

$$
p_n=\left[1+\left(1-\dfrac{1}{1-\zeta(k)\Pi_n}\right)^{\frac{1}{k}}\right].
$$

这里 $\Pi_n=\prod\limits_{i=1}^{n-1}(1-p_i^{-k})$, $k\ge 2p_{n-1}$.
</div>

由 Euler 乘积公式可知 $\zeta(k)=\prod\limits_{i=1}^\infty\dfrac{1}{1-p_i^{-k}}$, 令 $\vartheta=\prod\limits_{i=n+1}^{\infty}(1-p_i^{-k})$, 则有

$$
\dfrac{1}{\zeta(k)}=\left(1-\dfrac{1}{p_n^k}\right)\Pi_n\vartheta.
$$

故

$$
p_n=\left(1-\dfrac{1}{1-\zeta(k)\Pi_n\vartheta}\right)^{\frac{1}{k}},
$$

再令

$$
q_n=\left(1-\dfrac{1}{1-\zeta(k)\Pi_n}\right)^{\frac{1}{k}}.
$$

Teuffel 在 [23] 中证明了当 $k\ge 2p_{n-1}$ 时, 有 $0<p_n-q_n<1$, 从而可以由前 $n-1$ 个素数计算第 $n$ 个素数,

$$
p_n=\left[1+\left(1-\dfrac{1}{1-\zeta(k)\Pi_n}\right)^{\frac{1}{k}}\right].
$$
\qed

1979 年, Knopfmacher 使用类似的方法给出公式:

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>

$$
p_{n}=\left[2^{\frac{1}{s}}\left(1-\dfrac{1}{\zeta(s)\Pi_n}\right)^{-\frac{1}{s}}\right].
$$

这里 $\Pi_n=\prod\limits_{i=1}^{n-1}(1-p_i^{-k})$, $s\ge 2p_{n-1}$.
</div>

Knopfmacher 在 [13] 中证明了, 当 $s$ 足够大时, 有不等式
$$
p_{n}<2^{\frac{1}{s}}\left(1-\dfrac{1}{\zeta(s)\Pi_n}\right)^{-\frac{1}{s}}<p_{n}+1
$$
成立, 故

$$
p_{n}=\left[2^{\frac{1}{s}}\left(1-\dfrac{1}{\zeta(s)\Pi_n}\right)^{-\frac{1}{s}}\right].
$$

# 参考文献

[1] Thøger Bang, A function representing all prime numbers., Norsk Mat. Tidsskr 34 (1952), 117–118.

[2] Joaquín Ortega Costa, La formulación explícita de la función pi(x) de los números primos., Revista Matemática Hispano-Americana (1950), 72–76.

[3] Underwood Dudley, Formulas for Primes, Mathematics Magazine 56 (1983), no. 1, 17–22.

[4] Dylan Fridman, Juli Garbulsky, Bruno Glecer, James Grime, and Massi Tron Florentin, A Prime-Representing Constant, The American Mathematical Monthly 126 (2019), no. 1, 70–73.

[5] J. M. Gandhi, Formulae for the Nth Prime., Proc. Washington State University Conferences on Number Theory (1971), 96–107.

[6] R. L. Goodstein and C. P. Wormell, Formulae For Primes, The Mathematical Gazette 51 (1967), no. 375, 35–38.

[7] G.H. Hardy and E.M. Wright, An Introduction to the Theory of Numbers, 6th edition, Contemporary Physics 51 (2010), no. 3, 283–283.

[8] V. C. Harris, A test for primality., Nordisk Matematisk Tidsskrift (1969), 82.

[9] James P. Jones, Formula for the Nth Prime Number, Canadian Mathematical Bulletin 18 (1975), no. 3, 433–434.

[10] James P. Jones, Daihachiro Sato, Hideo Wada, and Douglas Wiens, Diophantine representation of the set of prime numbers, The American Mathematical Monthly 83 (1976), no. 6, 449–464.

[11] Issam Kaddoura and Samih Abdul-Nabi, On Formula to Compute Primes and the n th Prime, arXiv: Number Theory (2012).

[12] Joseph B. Keller, A recursion equation for prime numbers, 2008.

[13] John Knopfmacher, Recursive formulae for prime numbers, Archiv der Mathematik (Basel) 33 (1979/80), no. 2, 144–149.

[14] J. H. Lambert, Anlage zur Architectonik, 2 (1771).

[15] Makis Papadimitriou, A Recursion Formula for the Sequence of Odd Primes, The American Mathematical Monthly 82 (1975), no. 3, 289–289.

[16] Stephen Regimbal, An Explicit Formula For The kth Prime Number, Mathematics Magazine 48 (1975), no. 4, 230–232.

[17] Paulo Ribenboim, The Little Book of Bigger Primes, Second Edition, Springer, 2004.

[18] Sebastián Martín Ruiz and Avda De Regla, The general term of the prime number sequence and the Smarandache prime function, Smarandache Notions (2000).

[19] Daihachiro Sato and Ernst G. Straus, P‐Adic Proof of Non‐Existence of Proper Prime Representing Algebraic Functions and Related Problems, Journal of The London Mathematical Society-second Series (1970), 45–48.

[20] Wacław Sierpiński, Sur une formule donnant tous les nombres premiers, Comptes Rendus Acad. Sci. Paris 235 (1952), 1078–1079.

[21] Juan Fernández Sánchez, Rocío Sánchez Alcalde, and Manuel Úbeda Flores, Fórmulas que generan números primos., Epsilon (2022), no. 110, 77–101.

[22] Garry J. Tee, Simple analytic expressions for primes, and for prime pairs., The New Zealand Mathematics Magazine 9 (1972), 32–44.

[23] E. Teuffel, Eine Rekursionsformel für Primzahlen., Jahresbericht der Deutschen Mathematiker-Vereinigung 57 (1955), 34–36.

[24] P. G. Tsangaris and J. P. Jones, An old theorem on the gcd and its application to primes., Fibonacci Quarterly 30:3 (1992), 194–198.

[25] Panayiotis G. Tsangaris, Formulae for the kth prime number., Bulletin of the Greek Mathematical Society 53 (2007), 147–149.

[26] Mladen Vassilev-Missana, Three formulae for n-th prime and six for n-th term of twin primes., Notes Number Theory Discrete Math (2001), no. 1, 15–20.

[27] Solomon W. Golomb, A Direct Interpretation of Gandhi's Formula, The American Mathematical Monthly 81 (1974), no. 7, 752–754.

[28] Solomon W. Golomb, Probability, information theory, and prime number theory, Discrete Mathematics 106-107 (1992), 219–229.

[29] Solomon W. Golomb, Formulas for the next prime, Pacific Journal of Mathematics 63 (1976), 401–404.

[30] C. P. Willans, On Formulae for the Nth Prime Number, The Mathematical Gazette 48 (1964), no. 366, 413–415.
