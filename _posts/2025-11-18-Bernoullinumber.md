---
layout: post
title: "伯努利数"
subtitle: ""
header-img: "img/post-bg-infinity.jpg"
header-mask: 0.3
math: true
tags:
  - 数论
---

# 基础定义和性质

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(伯努利数)</b>
伯努利数定义为以函数

$$
\frac{z}{e^z-1}
$$

为生成函数的数列, 即有幂级数

$$
\frac{z}{e^z-1}=\sum_{n=0}^\infty B_{n}\frac{z^n}{n!},
$$

上式在复数 $ |z|<2\pi $ 时收敛, 其中 $ B_n $ 称为伯努利数.
</div>

$ B_0 = 1 $, $ B_1 = -\frac{1}{2} $, $ B_2 = \frac{1}{6} $, $ B_3 = 0 $, $ B_4 = -\frac{1}{30} $.

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(伯努利多项式)</b>
在形式幂级数环 $ \mathbb{Q}[x][[z]] $ 中, 生成函数

$$
\frac{ze^{zx}}{e^z-1}=\sum_{n=0}^\infty B_n(x)\frac{z^n}{n!}
$$

中 $ B_n(x) $ 称为伯努利多项式, 显然有 $ B_n(0)=B_n $.
</div>

伯努利数有递推公式.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
当 $ n $ 是大于 $ 1 $ 的正整数时,

$$
\sum_{k=0}^{n-1} \binom{n}{k} B_k = 0,
$$

或等价的

$$
B_n = -\frac{1}{n+1} \sum_{k=0}^{n-1} \binom{n+1}{k} B_k.
$$
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>证明</b>
展开生成函数的分母为幂级数,

$$
\displaylines{
z = (e^z - 1) \sum_{k=0}^{\infty} \frac{B_k z^k}{k!} = \left(\sum_{n=1}^{\infty} \frac{z^{n+1}}{(n+1)!}\right)\left(\sum_{k=0}^{\infty} \frac{B_k z^k}{k!}\right) = \sum_{n=0}^{\infty} \sum_{k=0}^{n} \frac{B_k z^{n+1}}{(n+1-k)!k!} \\
= \sum_{n=0}^{\infty} \sum_{k=0}^{n} \frac{(n+1)!B_k}{(n+1-k)!k!} \cdot \frac{z^{n+1}}{(n+1)!} = \sum_{n=0}^{\infty} \sum_{k=0}^{n} \binom{n+1}{k} B_k \frac{z^{n+1}}{(n+1)!} = \sum_{n=1}^{\infty} \sum_{k=0}^{n-1} \binom{n}{k} B_k \frac{z^n}{n!},
}
$$

对比 $ z^n $ 的系数即可得证.
</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
当 $ n $ 是大于 $ 1 $ 的正整数时,

$$
B_{2n-1} = 0.
$$
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>证明</b>
定义

$$
f(z) = \frac{z(e^z + 1)}{2(e^z - 1)} = \frac{z}{e^z - 1} + \frac{1}{2}z = 1 + \sum_{n=2}^{\infty} B_n \frac{z^n}{n!},
$$

容易验证有$ f(z)=f(-z) $, 展开后对比系数即得$ B_{2n-1} = 0 $.
</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
当 $ n $ 是大于 $ 1 $ 的正整数时,

$$
B_n(0)=B_n(1),
$$

$$
\frac{\mathrm{d}}{\mathrm{d}x}B_n(x)=nB_{n-1}(x),
$$

$$
\int_0^1B_n(x)\mathrm{d}x=0.
$$
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>证明</b>
在生成函数中令 $ x $ 为 $ 1 $, 有

$$
\sum_{k=0}^{\infty} B_k(1)\frac{z^k}{k!} = \frac{z e^z}{e^z - 1} = \frac{z}{1 - e^{-z}} = \frac{-z}{e^{-z} - 1} = \sum_{k=0}^{\infty} (-1)^k B_k(0)\frac{z^k}{k!},
$$

故$ B_n(0)=(-1)^nB_n(1) $, 而 $ n $ 是大于 $ 1 $ 的奇数时 $ B_n(0) $ 为 $ 0 $, 故总有 $ B_n(0)=B_n(1) $.

生成函数两边对$ x $求导

$$
\frac{\mathrm{d}}{\mathrm{d}x} \frac{ze^{zx}}{e^z - 1} = \frac{\mathrm{d}}{\mathrm{d}x} \sum_{k=0}^{\infty} \frac{B_k(x)z^k}{k!}
$$

得

$$
\frac{z^2 e^{zx}}{e^z - 1} = \sum_{k=1}^{\infty} \frac{B_k'(x)z^k}{k!},
$$

两边除以一个 $ z $ 得

$$
\frac{ze^{zx}}{e^z - 1} = \sum_{k=1}^{\infty} \frac{B_k'(x)z^{k-1}}{k!} = \sum_{k=0}^{\infty} \frac{B_{k+1}'(x)z^k}{(k+1)!},
$$

与定义对比系数得

$$
\frac{B_{k+1}'(x)}{(k+1)!} = \frac{B_k(x)}{k!},
$$

即

$$
\frac{\mathrm{d}}{\mathrm{d}x}B_n(x)=nB_{n-1}(x).
$$

利用前两条可得

$$
\int_{0}^{1} B_n(x) \mathrm{d}x = \left. \frac{B_{n+1}(x)}{n+1} \right|_{0}^{1} = \frac{1}{n+1} \left( B_{n+1}(1) - B_{n+1}(0) \right) = 0,
$$

于是定理全部得证.
</div>

事实上, 只有 $ n=1 $ 时 $ B_n(0)\neq B_n(1) $, 其中 $ B_1(0)=-\frac{1}{2} $, $ B_1(1)=\frac{1}{2} $, 有时也有 $ B_n^+=B_n(1) $ 和 $ B_n^-=B_n(0) $ 的记法.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
对任意非负整数 $ n $, 有

$$
B_n(x) = \sum_{k=0}^{n} \binom{n}{k} B_k x^{n-k}.
$$
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>证明</b>
将

$$
\frac{z e^{zx}}{e^z - 1} =\left(\sum_{n=0}^{\infty} \frac{B_n}{n!} z^n \right)\left( \sum_{k=0}^{\infty} \frac{x^k z^k}{k!} \right) = \sum_{n=0}^{\infty} \left( \sum_{k=0}^{n} \frac{B_k x^{n-k}}{k!(n - k)!} \right) z^n
$$

与伯努利多项式对比系数得

$$
\frac{B_n(x)}{n!} = \sum_{k=0}^{n} \frac{B_k x^{n-k}}{k!(n - k)!},
$$

这与原定理等价.
</div>

# 等幂求和

伯努利数起源于伯努利对等幂求和问题的研究, 即求和式

$$
S_m(n)=\sum_{k=1}^n k^m
$$

的封闭形式.

例如

$$
S_1(n)=\frac{n(n+1)}{2}=\frac{1}{2}(n^2+n),
$$

$$
S_2(n)=\frac{n(n+1)(2n+1)}{6}=\frac{1}{3}\left(n^3+\frac{3}{2}n^2+\frac{1}{2}n\right),
$$

一般的, 有:

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(等幂求和)</b>
$$
S_m(n)=\frac{1}{m+1}\sum_{k=0}^m\binom{m+1}{k}B_k^+ n^{m+1-k}.
$$
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>证明</b>
考虑 $ S_m(n) $ 的生成函数

$$
f_n(z)=\sum_{m=0}^\infty S_m(n)\frac{z^m}{m!}=\sum_{m=0}^\infty \sum_{k=1}^n k^m\frac{z^m}{m!}=\sum_{k=1}^n\sum_{m=0}^\infty\frac{(kz)^m}{m!}=\sum_{k=1}^ne^{kz}=e^{z}\frac{1-e^{nz}}{1-e^z},
$$

而因为

$$
e^{z}\frac{1-e^{nz}}{1-e^z}=\frac{e^{nz}-1}{z}\frac{-z}{e^{-z}-1},
$$

幂级数展开即为

$$
\left( \sum_{m=0}^{\infty} \frac{n^{m+1}}{(m+1)!} z^{m} \right) \left( \sum_{k=0}^{\infty} \frac{(-1)^k B_k}{k!} z^k \right)=\sum_{m=0}^{\infty} \left( \sum_{k=0}^{m} \frac{m!(-1)^k B_k n^{m-k+1}}{k!(m - k + 1)!} \right) \frac{z^m}{m!},
$$

对比系数得

$$
S_m(n)=\sum_{k=0}^{m} \frac{m!(-1)^k B_k n^{m-k+1}}{k!(m - k + 1)!}=\frac{1}{m+1}\sum_{k=0}^m\binom{m+1}{k}(-1)^kB_k n^{m+1-k},
$$

又因 $ k $ 取大于 $ 1 $ 的奇数时 $ B_k=0 $, 故

$$
S_m(n)=\frac{1}{m+1}\sum_{k=0}^m\binom{m+1}{k}B^+_k n^{m+1-k},
$$

定理得证.
</div>

# 正切函数的泰勒展开

因为

$$
\frac{z}{e^z - 1}-B_1z = \frac{z}{e^z - 1} + \frac{1}{2}z = \frac{z(e^z + 1)}{2(e^z - 1)} = \frac{z}{2}\coth \frac{z}{2},
$$

故有

$$
\frac{z}{2} \coth \frac{z}{2} = \sum_{n=0}^{\infty} \frac{B_{2n} z^{2n}}{(2n)!},
$$

进而得到双曲余切函数的洛朗级数展开式

$$
\coth z = \frac{1}{z} + \sum_{n=1}^{\infty} \frac{4^{n} B_{2n} z^{2n-1}}{(2n)!},
$$

做代换 $ z\mapsto iz $, 因为 $ i\coth iz=\cot z $, 于是得到余切函数的洛朗展开式

$$
\cot z = \frac{i}{iz} + i\sum_{k=1}^{\infty} \frac{4^kB_{2k}}{(2k)!}(iz)^{2k-1} = \frac{1}{z} + \sum_{k=1}^{\infty} \frac{(-1)^k 4^k B_{2k}}{(2k)!} z^{2k-1},
$$

由三角恒等变换 $ \tan z=\cot z-2\cot2z $ 得

$$
\displaylines{\tan(z) = \frac{1}{z} - \frac{2}{2z} + \sum_{k=1}^{\infty} \frac{(-1)^k 4^k B_{2k}}{(2k)!}\left(z^{2k-1} - 2^{2k}z^{2k-1}\right) \\
= \sum_{k=1}^{\infty} \frac{(-1)^{k+1} 4^{k}(4^{k} - 1)B_{2k}}{(2k)!}z^{2k-1},}
$$

这就是正切函数的泰勒展开式, 它在圆盘 $ \lvert z \rvert < \frac{\pi}{2} $ 内收敛.

# 欧拉-麦克劳林求和公式

首先定义 $ b_1(u)=\left(u-[u]\right))-\frac{1}{2} $, 其中 $ [\cdot] $ 表示取整函数, 显然它是以 $ 1 $ 为周期的周期函数, 并且在 $ [0,1] $ 上的积分值为 $ 0 $, 我们按以下递推公式定义函数列 $ b_n(u) $:

$$
b_{n+1}(u) - b_{n+1}(0) = \int_{0}^{u} b_n(t)\mathrm{d}t,
$$

$$
\int_{0}^{1} b_{n+1}(u) \mathrm{d}u = 0,
$$

显然这两个条件由 $ b_n $ 完全确定了函数 $ b_{n+1} $, 并且这一列函数均以 $ 1 $ 为周期, 并且在 $ [0,1] $ 上的积分值为 $ 0 $.

由定义知 $ b_1(u)=B_1(u-[u]) $, 由以上两式和归纳法容易证明, 对任意正整数 $ n $, 有

$$
b_n(u)=\frac{B_n(u-[u])}{n!},
$$

因此当 $ u $ 取整数时, 就有 $ b_n(u)=\frac{B_n}{n!} $.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(欧拉-麦克劳林求和公式)</b>
设 $ f(u) $ 在区间 $ [u_1,u_2] $ 上 $ n $ 阶连续可导, 则有

$$
\sum_{u_1 < k \le u_2} f(k) = \int_{u_1}^{u_2} f(u) \mathrm{d}u + \left. \sum_{k=1}^{n} (-1)^k b_k(u) f^{(k-1)}(u) \right|_{u_1}^{u_2} + (-1)^{n+1} \int_{u_1}^{u_2} b_n(u) f^{(n)}(u)\mathrm{d}u.
$$
</div>

更常用的情形是 $ u_1,u_2 $ 均为整数, 并令 $ n\to\infty $, 公式变为

$$
\sum_{k=a}^{b} f(k)
 = \int_{a}^{b} f(x)  \mathrm{d}x + \frac{f(b) + f(a)}{2} + \sum_{k=1}^{\infty} \frac{B_{2k}}{(2k)!} \left( f^{(2k-1)}(b) - f^{(2k-1)}(a) \right).
$$

该定理的证明见[4]的第2.2节.

发散级数的拉马努金和是欧拉-麦克劳林求和公式的一个应用[1], 我们将公式改写成

$$
\sum_{k=1}^{n} f(k) = \int_{0}^{n} f(x)  \mathrm{d}x + \frac{f(n) - f(0)}{2} + \sum_{k=1}^{\infty} \frac{B_{2k}}{(2k)!} \left( f^{(2k-1)}(n) - f^{(2k-1)}(0) \right),
$$

等式右边拆分为与 $ n $ 有关和无关两部分, 得到

$$
\sum_{k=1}^{n} f(k) =C(a)+\int_{a}^{n} f(x)  \mathrm{d}x + \frac{ f(n)}{2} + \sum_{k=1}^{\infty} \frac{B_{2k}}{(2k)!} f^{(2k-1)}(n),
$$

其中

$$
C(a)=\int_0^af(x)\mathrm{d}x-\frac{f(0)}{2} - \sum_{k=1}^{\infty} \frac{B_{2k}}{(2k)!} f^{(2k-1)}(0),
$$

当 $\sum\limits_{k=1}^{\infty} f(k)$ 收敛时, 令 $ a\to\infty $, 则显然有 $\sum\limits_{k=1}^{n} f(k)=\lim\limits_{a\to\infty }C(a)$, 若 $\sum\limits_{k=1}^{\infty} f(k)$ 发散, 则令 $ C(0) $ 为其拉马努金和, 记作

$$
\sum_{k\ge1}^{\mathfrak{R}}f(k)=\begin{cases}
    \lim\limits_{a\to\infty}C(a)& \sum\limits_{k=1}^{\infty} f(k)\text{收敛,}\\
    C(0) & \sum\limits_{k=1}^{\infty} f(k)\text{发散}.
\end{cases}
$$

如果有$\lim\limits_{n\to\infty}f(n)=0$, 易证

$$
\sum_{k\ge1}^{\mathfrak{R}}f(k)=\lim_{n\to\infty}\left(\sum_{k=1}^{n} f(k)-\int_{0}^{n} f(x)  \mathrm{d}x\right).
$$

例如, $ f(x)=1 $时,

$$
\sum_{k\ge1}^{\mathfrak{R}}1=-\frac{1}{2},
$$

$f(x)=x$时,

$$
\sum_{k\ge1}^{\mathfrak{R}}k=-\frac{B_2}{2}f'(0)=-\frac{1}{12},
$$

$f(x)=\frac{1}{1+x}$时,

$$
1+\sum_{k\ge1}^{\mathfrak{R}}\frac{1}{1+k}=1+\lim_{n\to\infty}\left(\sum_{k=1}^{n} \frac{1}{k+1}-\int_{0}^{n}  \frac{1}{x+1} \mathrm{d}x\right)=\gamma,
$$

即调和级数的拉马努金和是欧拉常数.(因 $\frac{1}{x}$ 在 $ 0 $ 处无定义, 所以用 $\frac{1}{1+x}$ 将极点平移掉, 实际上当 $f$ 在 $ 0 $ 处无定义时有另一种拉马努金和, 其计算结果与这里相同.)

欧拉常数也是欧拉-麦克劳林求和公式的推论之一.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
设 $ k $ 是正整数, 当 $ x\ge2 $ 时, 有

$$
\sum_{\substack{n \leq x}} \frac{(\ln n)^k}{n} = \frac{1}{k+1} (\ln x)^{k+1} + \gamma_k + O\left( \frac{(\ln x)^k}{x} \right),
$$

其中

$$
\gamma_k = \int_{1}^{+\infty} (t - [t]) \frac{k(\ln t)^{k-1} - (\ln t)^k}{t^2} \mathrm{d}t.
$$
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>证明</b>
由欧拉-麦克劳林求和公式得

$$
\sum_{\substack{n \leq x}} \frac{(\ln n)^k}{n} = \int_{1}^{x} \frac{(\ln t)^k}{t}  \mathrm{d}t - (x - [x]) \frac{(\ln x)^k}{x} + \int_{1}^{x} (t - [t]) \frac{k(\ln t)^{k-1} - (\ln t)^k}{t^2} \mathrm{d}t.
$$

又因

$$
\int_{1}^{x} \frac{(\ln t)^k}{t}  \mathrm{d}t = \frac{1}{k+1} (\ln x)^{k+1}
$$

且当 $ x\ge2 $ 时

$$
\int_{x}^{+\infty} (t - [t]) \frac{k(\ln t)^{k-1} - (\ln t)^k}{t^2}  \mathrm{d}t = O\left( \frac{(\ln x)^k}{x} \right),
$$

三式合起来即可.
</div>

欧拉常数可以在某种意义下看做 $\gamma=\gamma_0$, 所有的 $\gamma_k$ 统称为斯蒂尔杰斯常数.

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
设$\gamma$是欧拉常数, $ B_k $是伯努利数, 则

$$
\gamma=\frac{1}{2}+\sum_{k=1}^{\infty} \frac{B_{2k}}{2k}.
$$
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>证明</b>
由欧拉-麦克劳林求和公式得

$$
\sum_{k=1}^{n} \frac{1}{k} = \int_{1}^{n} \frac{1}{x}\mathrm{d}x + \frac{\frac{1}{n} + 1}{2} + \sum_{k=1}^{\infty} \frac{B_{2k}}{(2k)!} (-1)(2k-1)!\left( \frac{1}{n^{2k}} - 1 \right),
$$

化简并令$ n\to\infty $得

$$
\gamma=\lim_{n\to\infty}\left(\sum_{k=1}^{n}\frac{1}{k}-\ln n\right)=\frac{1}{2}+\sum_{k=1}^{\infty} \frac{B_{2k}}{2k},
$$

定理得证.
</div>

斯蒂尔杰斯常数均可以由伯努利数表示, 但过于复杂.

# 黎曼$\zeta$函数

<div style="border: 3px solid #000; padding: 10px;">
<b>定义(黎曼 $ \zeta $ 函数)</b>
黎曼 $ \zeta $ 函数是定义在右半平面 $ \mathrm{Re}(s)>1 $ 上的函数

$$
\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s}.
$$
</div>

黎曼 $ \zeta $ 函数可以延拓为 $ \mathbb{C} $ 上的亚纯函数, 在 $ s=1 $ 处有唯一的极点, 阶数为 $  1 $, 在 $ s=1 $ 附近有洛朗展开式

$$
\zeta(s)=\frac{1}{s-1}+\gamma+\sum_{n=1}^\infty\gamma_n\frac{(s-1)^n}{n!},
$$

其中系数为斯蒂尔杰斯常数.

与伯努利数相关的是 $ \zeta $ 函数在正偶数和负整数处的值, 有:

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
设 $  n  $ 是正整数, 则

$$
\zeta(2n) = \sum_{k=1}^{\infty} \frac{1}{k^{2n}} = \frac{(-1)^{n-1}B_{2n} (2\pi)^{2n}}{2(2n)!}.
$$
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>证明</b>
由傅里叶分析知有无穷乘积

$$
\sin x = x \prod_{k=1}^{\infty} \left(1 - \frac{x^2}{k^2\pi^2}\right),
$$

所以有,

$$
\frac{\sin x}{x} = \prod_{k=1}^{\infty} \left(1 - \frac{x^2}{k^2\pi^2}\right),
$$

取对数,

$$
\ln\left(\frac{\sin x}{x}\right) = \sum_{k=1}^{\infty} \ln\left(1 - \frac{x^2}{k^2\pi^2}\right),
$$

两边对 $  x  $ 求导

$$
\frac{x \cos x - \sin x}{x \sin x} = \sum_{k=1}^{\infty} \frac{-2x}{k^2\pi^2 - x^2},
$$

整理得

$$
\displaylines{\cot x - \frac{1}{x} = -2 \sum_{k=1}^{\infty} \frac{x}{k^2\pi^2 - x^2} = -2 \sum_{k=1}^{\infty} \frac{x}{k^2\pi^2} \cdot \frac{1}{1 - \frac{x^2}{k^2\pi^2}}=\\
-2 \sum_{k=1}^{\infty} \frac{x}{k^2\pi^2} \sum_{n=0}^{\infty} \left( \frac{x^2}{k^2\pi^2} \right)^n,}
$$

交换求和顺序并由 $ \zeta $ 函数定义即得

$$
\cot x - \frac{1}{x} = -2 \sum_{n=0}^{\infty}  \frac{\zeta(2n+2)}{\pi^{2n+2}} x^{2n+1} = -2 \sum_{n=1}^{\infty}  \frac{\zeta(2n)}{\pi^{2n}} x^{2n-1},
$$

又因为

$$
\cot x - \frac{1}{x} = \sum_{n=1}^{\infty} \frac{(-1)^n 2^{2n} B_{2n}}{(2n)!} x^{2n - 1},
$$

比较系数得

$$
-\frac{2 \zeta(2n)}{\pi^{2n}} = \frac{(-1)^{n} 2^{2n} B_{2n}}{(2n)!},
$$

$$
\zeta(2n) = \frac{(-1)^{n-1} B_{2n} (2\pi)^{2n}}{2(2n)!},
$$

定理得证.
</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>
设 $  n  $ 是非负整数, 则

$$
\zeta(-n) = (-1)^n \frac{B_{n+1}}{n+1}.
$$
</div>

这说明 $ \zeta $ 在负偶数处有零点, 它们称为平凡零点, 黎曼猜想除此之外的零点的实部均为 $ \frac{1}{2} $.

进一步定义黎曼-赫尔维茨 $ \zeta $ 函数为

$$
\zeta(s, a) = \sum_{n=0}^{\infty} \frac{1}{(n + a)^s}, \quad \mathrm{Re}(s) > 0,\ a > 0,
$$

显然

$$
\zeta(s,1)=\zeta(s),
$$

对于非负整数 $  n  $ , 有

$$
\zeta(-n, a) = -\frac{B_{n+1}(a)}{n+1}.
$$

# 哑演算

设 $  B  $ 是伯努利数的哑元, 记 $  B^n=B_n  $, 前者是 $  n  $ 次幂, 后者是第 $  n  $ 个伯努利数, 由二项式定理得

$$
(x+B)^n=\sum_{k=0}^{n} \binom{n}{k} B^k x^{n-k},
$$

由伯努利多项式的伯努利数表示知 $ (x+B)^n $ 就代表第 $  n  $ 个伯努利多项式, 使用哑元, 伯努利数的生成函数可以表示为 $ \frac{z}{e^z-1}=e^{Bz} $, 伯努利多项式的生成函数就是 $  e^{(x+B)z}=e^{xz}e^B=\frac{ze^{xz}}{e^z-1} $, 代入 $  x=1 $, 有

$$
e^{Bz}-e^{(1+B)z}=e^{Bz}(e^z-1)=\frac{z}{e^z-1}(e^z-1)=z,
$$

左边展开为幂级数后比较系数得 $  n=1  $ 时 $ (1+B)^n-B^n=1 $, $ n>1  $ 时 $ (1+B)^n=B^n$, 所以 $  B_1(1)-B_1(0)=1 $, $ n>1 $ 时 $ B_n(0)=B_n(1) $, 与之前得到的结论一致. 在二项式展开式中令 $ x=1 $, 则有 $ n>1 $ 时,

$$
(1+B)^n-B^n=\sum_{k=0}^{n} \binom{n}{k} B^k =0,
$$

这就是之前证明过的伯努利数的递推公式.

考虑差分

$$
\Delta (n+B)^{k+1}=(n+(1+B))^{k+1}-(n+B)^{k+1},
$$

使用二项式定理展开后代入 $ (1+B)^n $ 和 $ B^n $ 得

$$
\Delta (n+B)^{k+1}=(k+1)n^{k},
$$

两边对 $ n $ 求和得

$$
(m+(1+B))^{k+1}-(1+B)^{k+1}=\sum_{n=1}^m\Delta (n+B)^{k+1}=(k+1)\sum_{n=1}^m n^{k}=(k+1)S_k(m),
$$

展开左边得

$$
S_k(n)=\frac{1}{k+1}\sum_{k=0}^m\binom{m+1}{k}(1+B)^k n^{m+1-k}=\frac{1}{k+1}\sum_{k=0}^m\binom{m+1}{k}B_k^+ n^{m+1-k},
$$

这就是幂等求和公式.

使用哑演算还能得到伯努利数的其他更多公式.

# 参考文献

[1] Bruce C. Berndt, Ramanujan’s Notebooks, Part I, Springer-Verlag, New York, 1985.

[2] 李文威, 模形式初步, 现代数学基础丛书; 183, 科学出版社, 北京, 6 2020.

[3] 潘承彪, 从切比雪夫到爱尔特希：素数定理的初等证明（上）, 哈尔滨工业大学出版社, 哈尔滨, 2013.

[4] 潘承洞, 潘承彪, 解析数论基础, 人民出版社, 北京, 1981.
