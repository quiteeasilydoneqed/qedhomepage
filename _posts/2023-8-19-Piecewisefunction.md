---
layout: post
title: "如何将分段函数写成不分段的形式"
subtitle: ""
header-img: "img/post-bg-infinity.jpg"
header-mask: 0.3
math: true
tags:
  - 初等数学
---

绝对值函数一般定义为分段函数

$$

\lvert x \rvert=\left\{\begin{matrix}x & x \ge 0; \\-x & x < 0.\end{matrix}\right.

$$

我们可以使用 $\lvert x\rvert=\sqrt{x^2}$ 将其用不分段的形式表示出来, 如果给出其它更多的分段函数, 如何将其写成不分段的形式?

比如说分段函数

$$

f(x)=\left\{\begin{matrix}x & x \ge 0; \\0 & x < 0.\end{matrix}\right.

$$

根据它的形式, 我们可以自然地联想到绝对值函数, 考虑函数 $x+\lvert x\rvert$, 显然有

$$

x+\lvert x \rvert=\left\{\begin{matrix}2x & x \ge 0\\0 & x < 0\end{matrix}\right., 

$$

再乘上 $\dfrac{1}{2}$ 就是我们的目标, 即 $f(x)=\dfrac{x+\lvert x \rvert}{2}$.

将该式中的加号变成减号, $g(x)=\dfrac{x-\lvert x \rvert}{2}$, 显然, 这个函数就等价于分段函数

$$

g(x)=\left\{\begin{matrix}0 & x > 0;\\x & x \le 0.\end{matrix}\right.

$$

接下来我们考虑分段函数

$$

h(x)=\left\{\begin{matrix}x & x \ge a;\\a & x < a.\end{matrix}\right.

$$

这个函数相当于将函数 

$$

f(x)=\left\{\begin{matrix}x & x \ge 0\\0 & x < 0\end{matrix}\right.

$$

向右平移 $a$ 个单位, 再向上平移 $a$ 个单位, 所以的不分段形式就是 $h(x)=\frac{1}{2}(x-a+\lvert x-a \rvert)+a$, 整理即得 $h(x)=\frac{1}{2}(x+a+\lvert x-a\rvert).$

再考虑一个三段的函数,

$$

m(x)=\left\{\begin{matrix}b & x > b\\x & a\le x \le b\\a&x<a\end{matrix}\right..

$$

显然, 只使用一个绝对值是不够的, 我们需要两个绝对值来表达, $m(x)=\frac{1}{2}(a+b+\lvert x-a \rvert-\lvert x-b \rvert)$.

为了表示更复杂的分段函数, 我们先引入以下记号.

$$

I_{(-\infty, a]}=\frac{1}{2}(x+a-\lvert x-a \rvert)=\left\{\begin{matrix}a & x > a\\x & x \le a\end{matrix}\right.

$$

$$

I_{[a, +\infty)}=\frac{1}{2}(x+a+\lvert x-a \rvert)=\left\{\begin{matrix}x & x \ge a\\a & x < a\end{matrix}\right.

$$

$$

I_{[a, b]}=\frac{1}{2}(a+b+\lvert x-a \rvert-\lvert x-b \rvert)=\left\{\begin{matrix}b & x > b\\x & a\le x \le b\\a&x<a\end{matrix}\right.

$$


使用这三个函数可以表示更复杂的分段函数, 我们用一个例子来说明.

$$

f(x)=\left\{\begin{matrix}\ln x & x > 1;\\-x+1 & 0\le x\le 1;\\e^x&x<0.\end{matrix}\right.

$$

显然它是一个连续函数, 指数函数, 对数函数和多项式函数在其定义域内都是连续的, 且其在 0 和 1 两个点上也连续. 在 $(-\infty, 0]$ 内, $e^{I_{(-\infty, 0]}}=e^x$. 在 $[0, 1]$ 内, $-I_{[0, 1]}+1=-x+1$, 在 $[1, +\infty)$ 内, $\ln I_{[a, +\infty)}=\ln x$, 在其它的区间内, 三个函数均为常数值, 将三者相加即得

$$

f^*(x)=e^{I_{(-\infty, 0]}}-I_{[0, 1]}+1+\ln I_{[1, +\infty)},

$$

由于三个函数会相互干扰, 函数 $f^*(x)$ 是 $f(x)$ 向上或向下平移了某个长度, 就我们的例子而言, 它是 $f(x)$ 的图像向上平移了一个单位长度, 只需给它减去 $1$ 即可, 也就是

$$

f(x)=e^{I_{(-\infty, 0]}}-I_{[0, 1]}+\ln I_{[1, +\infty)}.

$$

按照这种方法, 可以将很大一类分段函数写成不分段的形式, 即在各个段内都是初等函数的连续分段函数. 有些更复杂的函数也可以写成不分段的形式, 只不过需要更复杂的工具, 比如说著名的狄利克雷函数：

$$

D(x)=\left\{\begin{matrix}1 & x\text{为有理数};\\ 0 &x\text{为无理数}.\end{matrix}\right. 

$$

写成不分段的形式就是：

$$

D(x)=\lim_{k\to\infty}\lim_{j\to\infty}\left((\cos k!\pi x)^{2j}\right)

$$

可以看到我们动用了三角函数, 阶乘和极限.

另一个例子是与 $3x+1$ 猜想相关的 $3x+1$ 函数, 它定义在正整数集上,

$$

f(x)=\left\{\begin{matrix}3x+1 & x\text{为奇数};\\ \dfrac{x}{2} &x\text{为偶数}.\end{matrix}\right. 

$$

利用三角函数的性质写成不分段的形式就是

$$

f(x)=(3x+1)\sin^2 \frac{\pi x}{2}+\frac{x}{2}\cos^2 \frac{\pi x}{2},

$$

这个表示不是唯一的, 而且对于 $3x+1$ 猜想的研究是无用的.
