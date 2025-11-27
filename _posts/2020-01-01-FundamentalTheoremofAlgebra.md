---
layout: post
title: "代数基本定理"
subtitle: "高斯的第一个证明"
header-img: "img/post-bg-infinity.jpg"
header-mask: 0.3
math: true
tags:
  - 代数
---

著名的代数基本定理指, 在 $\mathbb{C}[x]$ 中, 每一个复系数 $n>0$ 次多项式(已化为首一多项式)

$$

f(x)=x^n+a_{n-1}x^{n-1}+ \cdots +a_1x+a_0

$$

都有 $n$ 个复根, $k$ 重根按 $k$ 个根算.

证明代数基本定理只需要证明 $n>0$ 次多项式有一个根即可, 比如设为 $x_0$ , 则有

$$

f(x)=\left(x-x_0\right)g(x),

$$

这里 $g(x)$ 是一个 $n-1$ 次多项式, 对 $g(x)$ 再次使用上面的定理, 以此类推, 最终得到$f(x)$有$n$个根.

接下来展示高斯在1799年给出的第一种证明方法, 这是历史上代数基本定理的第一个(不严谨的)证明.

高斯将多项式$f(x)$重写成

$$

f(a+bi)=u(a,b)+v(a,b)i

$$

的形式, 其中设 $x=a+bi$, $u(a,b)$ 和 $v(a,b)$ 是以 $a$ 和 $b$ 为自变量的二元实系数实值多项式.

求$f(a+bi)$的根, 就是要找出$a$和$b$, 使得 $u(a,b)=0$ 和 $v(a,b)=0$ 同时成立, 而 $u(a,b)=0$ 和 $v(a,b)=0$ 可以看做 $a-O-b$ 平面上的两条曲线, 使得 $f(a+bi)=0$ 的 $(a,b)$ 就是曲线 $u(a,b)=0$ 和 $v(a,b)=0$ 的交点.

设 $\left\vert x\right\vert$ 是 $x$ 的模, 当 $\left\vert x\right\vert$ 足够大时, $f(x)=x^n+\cdots+a_1 x+a_0$ 的值和函数 $\phi(x)=x^n$ 的值是差不多的.
我们将 $x=a+bi$ 写成三角形式，即 $x=r(\cos\theta+i\sin\theta)$, 其中 $r=\left\vert x\right\vert$, $\theta$ 是复数 $x$ 的辐角, 由棣莫弗定理知

$$

x^n=r^n(\cos n \theta+i\sin n \theta),

$$

所以$\phi(x)=r^n\cos n \theta+ir^n\sin n \theta$, 于是在图像上, $u(a,b)$ 和 $r^n\cos n\theta$ 在距离原点足够远的地方看起来是差不多的, $v(a,b)$ 与 $r^n\sin n\theta$ 也同理.

$\cos n \theta=0$ 和 $\sin n \theta=0$ 是过原点的 $2n$ 条直线, 其中属于 $\cos n \theta$ 和 $\sin n \theta$ 的直线交错出现, 各有 $n$ 条.
现在画一个以原点为圆心, $N>0$ 为半径的圆 $C$, $N$ 是一个足够大的实数, 则当 $\left\vert x\right\vert >N $时, $u(a,b)=0$ 和 $v(a,b)=0$的图像也是交错出现的.

下面关注圆$C$内的情况, 因为任意多项式都一定是连续的, 图像上来说就是多项式的曲线一定是连续不断的, 而现在$u(a,b)=0$和$v(a,b)=0$的图像在圆外交错出现, 由几何直观可知, 在圆内二者必定相交, 也就是说$f(x)$至少有一个零点.

例如$f(x)=x^3+1+i$时, $u(a,b)=a^3-3ab^2+1$, $v(a,b)=3a^2b-b^3+1$, 图像如下:

![图像]({{ site.baseurl }}/img/algebra.jpg "图像")

在1799年之后, 高斯又发表了另外三个代数基本定理的证明.


参考文献: Klein, F. (2007). 高观点下的初等数学 (舒湘芹, 陈平, 译). 复旦大学出版社.
