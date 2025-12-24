---
layout: post
title: "魏尔斯特拉斯函数"
subtitle: ""
header-img: "img/post-bg-infinity.jpg"
header-mask: 0.3
math: true
tags:
  - 分析
---

由高中时笔记修改而来.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(魏尔斯特拉斯函数)</b>

    魏尔斯特拉斯函数定义为

    $$
    W(x)=\sum_{n=0}^\infty a^n\cos(b^n\pi x),
    $$

    其中 $a\in(0,1)$ ,  $b$ 是正奇数, 并且满足 $ab>1+\frac{3\pi}{2}$ .

</div>

魏尔斯特拉斯证明了该函数是良定的, 并且在实数轴上处处连续但处处不可导, 这种情况的证明比较容易.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理(魏尔斯特拉斯)</b>

     $W(x)$ 在 $\mathbb R$ 上处处连续但处处不可导.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

    首先证明函数良定. 因为

    $$
    \sum_{n=0}^\infty \left|a^n\cos(b^n\pi x)\right|\le\sum_{n=0}^\infty a^n=\frac{1}{1-a},
    $$

    由魏尔斯特拉斯判别法知级数一致收敛, 进而连续.<br>

    再证明函数处处不可导. 任取一固定实数 $x\in\mathbb R$ , 对任意正整数 $m$ , 令

    $$
    b^mx=\alpha_m+\varepsilon_m,
    $$

    其中 $\alpha_m$ 是距离 $b^mx$ 最近的整数,  $-\frac{1}{2}\le\varepsilon_m\le\frac{1}{2}$ , 令

    $$
    h_m=\frac{1-\varepsilon_m}{b^m},
    $$

    显然有

    $$
    0<\frac{1}{2b^m}\le\frac{1-\varepsilon_m}{b^m}\le\frac{3}{2b^m},
    $$

    令 $m\to\infty$ , 由夹逼定理得

    $$
    \lim_{m\to\infty}h_m=0,
    $$

    我们只需证明

    $$
    \lim_{m\to\infty}\frac{W(x+h_m)-W(x)}{h_m}
    $$

    不存在即可推出 $W$ 不可导.<br>

    因为

    \begin{align*}
        &\frac{W(x+h_m)-W(x)}{h_m}=\sum_{n=0}^\infty a^n\frac{\cos(b^n\pi (x+h_m))-\cos(b^n\pi x)}{h_m}\\
        =&\sum_{n=0}^{m-1} a^n\frac{\cos(b^n\pi (x+h_m))-\cos(b^n\pi x)}{h_m}+\sum_{n=m}^\infty a^n\frac{\cos(b^n\pi (x+h_m))-\cos(b^n\pi x)}{h_m},
    \end{align*}

    对于等式右边第一项, 由拉格朗日中值定理知存在 $\xi\in(0,h_m)$ , 

    $$
    |\cos(b^n\pi (x+h_m))-\cos(b^n\pi x)|=|h_m||b^n\pi\sin(b^n\pi(x+\xi))|\le b^n\pi|h_m|,
    $$

    因此

    $$
    \left|\sum_{n=0}^{m-1} a^n\frac{\cos(b^n\pi (x+h_m))-\cos(b^n\pi x)}{h_m}\right|\le\sum_{n=0}^{m-1}a^nb^n\pi=\frac{\pi (a^mb^m-1)}{ab-1}<\frac{\pi a^mb^m}{ab-1}.
    $$

<br>

    对于第二项, 因为

    $$
    b^n\pi (x+h_m)=b^{n-m}\pi(b^mx+b^mh_m)=b^{n-m}\pi(\alpha_m+\varepsilon_m+1-\varepsilon_m)=b^{n-m}\pi(\alpha_m+1),
    $$

    而 $b^{n-m}$ 是奇数, 则

    $$
    \cos(b^{n-m}\pi(\alpha_m+1))=(-1)^{\alpha_m+1}.
    $$

    又因为

    \begin{align*}
        \cos(b^n\pi x)&=\cos(b^{n-m}\pi(\alpha_m+\varepsilon_m))\\
        &=\cos(b^{n-m}\pi\alpha_m)\cos(b^{n-m}\pi\varepsilon_m)-\sin(b^{n-m}\pi\alpha_m)\sin(b^{n-m}\pi\varepsilon_m)\\
        &=(-1)^{\alpha_m}\cos(b^{n-m}\pi\varepsilon_m),
    \end{align*}

    则

    \begin{align*}
        \sum_{n=m}^\infty a^n\frac{\cos(b^n\pi (x+h_m))-\cos(b^n\pi x)}{h_m}&=\sum_{n=m}^\infty a^n\frac{(-1)^{\alpha_m+1}-(-1)^{\alpha_m}\cos(b^{n-m}\pi\varepsilon_m)}{h_m}\\
        &=\sum_{n=m}^\infty a^n\frac{(-1)^{\alpha_m+1}(1+\cos(b^{n-m}\pi\varepsilon_m))}{h_m}\\
        &=\frac{(-1)^{\alpha_m+1}}{h_m}\sum_{n=m}^\infty a^n(1+\cos(b^{n-m}\pi\varepsilon_m)),
    \end{align*}

    显然 $a^n(1+\cos(b^{n-m}\pi\varepsilon_m))\ge0$ , 因此

    $$
    \left|\frac{(-1)^{\alpha_m+1}}{h_m}\sum_{n=m}^\infty a^n(1+\cos(b^{n-m}\pi\varepsilon_m))\right|\ge\frac{a^m}{h_m}(1+\cos(\pi\varepsilon_m)),
    $$

    由 $-\frac{\pi}{2}\le\pi\varepsilon_m\le\frac{\pi}{2}$ 知 $\cos(\pi\varepsilon_m)\ge0$ ) , 故

    $$
    \left|\sum_{n=m}^\infty a^n\frac{\cos(b^n\pi (x+h_m))-\cos(b^n\pi x)}{h_m}\right|\ge\frac{a^m}{h_m}\ge\frac{2a^mb^m}{3}.
    $$
    
<br>

    综上,

    \begin{align*}
        \frac{2a^mb^m}{3}\le&\left|\sum_{n=m}^\infty a^n\frac{\cos(b^n\pi (x+h_m))-\cos(b^n\pi x)}{h_m}\right|\\
        =&\left|\frac{W(x+h_m)-W(x)}{h_m}-\sum_{n=0}^{m-1} a^n\frac{\cos(b^n\pi (x+h_m))-\cos(b^n\pi x)}{h_m}\right|
        &\\
        \le&\left|\frac{W(x+h_m)-W(x)}{h_m}\right|+\left|\sum_{n=m}^\infty a^n\frac{\cos(b^n\pi (x+h_m))-\cos(b^n\pi x)}{h_m}\right|\\
        <&\left|\frac{W(x+h_m)-W(x)}{h_m}\right|+\frac{\pi a^mb^m}{ab-1},
    \end{align*}

    则

    $$
    \left|\frac{W(x+h_m)-W(x)}{h_m}\right|>\left(\frac{2}{3}-\frac{\pi}{ab-1}\right)a^mb^m,
    $$

    由 $ab>1+\frac{3\pi}{2}$ 知 $\frac{2}{3}-\frac{\pi}{ab-1}>0$ , 因此

    $$
    \lim_{m\to\infty}\left|\frac{W(x+h_m)-W(x)}{h_m}\right|\ge\lim_{m\to\infty}\left(\frac{2}{3}-\frac{\pi}{ab-1}\right)a^mb^m=+\infty,
    $$

    由于 $x$ 是任意取的, 则 $W(x)$ 在 $\mathbb R$ 上处处不可导.

</div>

哈代随后证明了, 只需要将条件放宽到 $ab\ge1$ , 其中 $a\in(0,1)$ ,  $b\in(1,+\infty)$ , 即可证明函数处处连续但处处不可导, 具体见[1].

<div style="border: 3px solid #000; padding: 10px;">

<b>定理(哈代)</b>

     设 $a\in(0,1)$ ,  $b>1$ , 且满足 $ab\ge1$ , 则函数

    $$
    C(x) = \sum_{n=0}^{\infty} a^n \cos(b^n \pi x),
    $$

    $$
    S(x) = \sum_{n=0}^{\infty} a^n \sin(b^n \pi x),
    $$

    均在 $\mathbb R$ 上处处连续 but 处处不可导.

</div>

魏尔斯特拉斯函数的图像是一个分形, 简单验证即可得到函数方程

$$
W(x)=\cos \pi x+aW(bx),
$$

说明了其图像的自相似性质. 沈维孝于2015年证明了魏尔斯特拉斯函数的豪斯多夫维数为 $2+\frac{\ln a}{\ln b}$ , 这可由以下定理推出[2].

<div style="border: 3px solid #000; padding: 10px;">

<b>定理(沈维孝)</b>

     设 $\phi$ 是一个定义在实数轴上的周期函数, 并且有连续的二阶导数, 对于任意大于 $1$ 的整数 $b$ , 存在只依赖于 $\phi$ 和 $b$ 的常数 $K>1$ , 则对任意满足 $1<ab<K$ 的 $a$ , 函数

    $$
    \sum_{n=0}^\infty a^n\phi(b^nx)
    $$

    图像的豪斯多夫维数为

    $$
    2+\frac{\ln a}{\ln b}.
    $$

</div>

取 $\phi(x)=\cos(2\pi x)$ 即为魏尔斯特拉斯函数, 其中 $K=b$ , 此时 $a\in\left(\frac{1}{b},1\right)$ , 所以 $\frac{\ln a}{\ln b}<0$ , 又因 $ab\ge1$ , 则 $\ln a+\ln b=\ln ab<\ln1=0$ , 即 $-1<\frac{\ln a}{\ln b}$ , 因此 $1<2+\frac{\ln a}{\ln b}<2$ , 即维数不为整数, 这也符合曼德博对分形的定义.

# 参考文献

[1] Hardy, G. H. (1916). Weierstrass's non-differentiable function. Transactions of the American Mathematical Society, 17(3), 301–325. [https://doi.org/10.1090/S0002-9947-1916-1501044-1](https://doi.org/10.1090/S0002-9947-1916-1501044-1)

[2] Shen, W. (2018). Hausdorff dimension of the graphs of the classical Weierstrass functions. Mathematische Zeitschrift, 289(1-2), 223–266. [https://doi.org/10.1007/s00209-017-1949-1](https://doi.org/10.1007/s00209-017-1949-1)


