---
layout: post
title: "经典特殊函数"
subtitle: ""
header-img: "img/post-bg-infinity.jpg"
header-mask: 0.3
math: true
tags:
  - 分析

本文专注于一般分析学中常见的特殊函数, 尤其是在Wolfram计算中经常出现的特殊函数, 而不关注一些专门分支中的特殊函数, 例如椭圆函数, 数论中的特殊函数, 物理中的特殊函数等.

# Gamma函数

 $\Gamma$ 函数起源于阶乘的推广.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(Gamma函数)</b>

 $$\Gamma(z) = \int_0^{\infty} t^{z-1} e^{-t}\, \mathrm{d}t.$$ 

</div><br>

该积分在右半平面内绝对收敛, 并且 $\Gamma(n+1)=n!$ , 利用函数方程 $\Gamma(z+1) = z\Gamma(z)$ 可将 $\Gamma(z)$ 解析延拓至整个复平面.

 $\Gamma(z)$ 在 $z = 0$ 和负整数处具有一阶极点, 在 $z = -n$ 处的留数为 $\mathrm{Res}(\Gamma, -n) = \frac{(-1)^n}{n!}$ , $\Gamma(z)$ 在复平面上无零点, 因此 $\frac{1}{\Gamma(z)}$ 是一个整函数.

以下定理说明 $\Gamma$ 是阶乘在某种意义下唯一好的延拓.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理(波尔-莫勒鲁普定理)</b>

设 $ f(x) $ 是定义在 $(0, +\infty)$ 上的正实值函数, 若 $ f(x) $ 满足以下三个条件:
    
1, $f(1) = 1$ ;
    
2, 递推关系 $f(x+1) = xf(x)$ ;
    
3, 对数凸性, 即 $\ln f(x)$ 是一个凸函数,
    
则在 $(0, \infty)$ 上, 有 $f(x) \equiv \Gamma(x)$ .

</div><br>

以下为一些常见公式.

余元公式:

 $$\Gamma(z)\Gamma(1-z) = \frac{\pi}{\sin(\pi z)},$$ 

勒让德倍元公式:

 $$\Gamma(z)\Gamma\left(z + \frac{1}{2}\right) = 2^{1-2z} \sqrt{\pi} \Gamma(2z),$$ 

乘法公式:

 $$\prod_{k=0}^{m-1} \Gamma\left(z + \frac{k}{m}\right) = (2\pi)^{\frac{m-1}{2}} m^{\frac{1}{2}-mz} \Gamma(mz),$$ 

魏尔斯特拉斯乘积:

 $$\frac{1}{\Gamma(z)} = ze^{\gamma z} \prod_{n=1}^{\infty} \left(1 + \frac{z}{n}\right) e^{-z/n},$$ 

欧拉极限形式:

 $$\Gamma(z) = \lim_{n \to \infty} \frac{n! n^z}{z(z+1)\dots(z+n)},$$ 

斯特林公式:

 $$\Gamma(z) \sim \sqrt{\frac{2\pi}{z}} \left(\frac{z}{e}\right)^z \left(1 + \frac{1}{12z} + \frac{1}{288z^2} - \cdots\right),\quad |z| \to \infty, |\arg z| < \pi.$$ 

接下来是 $\Gamma$ 函数的一些衍生函数.

Beta函数

 $$B(x, y) = \int_0^1 t^{x-1} (1-t)^{y-1}\, \mathrm{d}t,$$ 

也称为第一类欧拉积分, 而 $\Gamma$ 函数称为第二类欧拉积分, 二者关系为

 $$B(x, y) = \frac{\Gamma(x)\Gamma(y)}{\Gamma(x+y)}.$$ 

双伽马函数定义为

 $$\psi(z) = \frac{\mathrm{d}}{\mathrm{d}z} \ln \Gamma(z) = \frac{\Gamma'(z)}{\Gamma(z)},$$ 

其各阶导数称为多伽马函数

 $$\psi^{(n)}=\left(\frac{\mathrm{d}}{\mathrm{d}z}\right)^n\psi(z).$$ 

当 $\Gamma$ 函数积分定义的限点不是 $[0, \infty]$ 时的积分称为不完全伽马函数, 上不完全伽马函数定义为

 $$\Gamma(s, x) = \int_x^{\infty} t^{s-1} e^{-t}\, \mathrm{d}t,$$ 

下不完全伽马函数定义为

 $$\gamma(s, x) = \int_0^x t^{s-1} e^{-t}\, \mathrm{d}t,$$ 

显然有恒等式 $\gamma(s, x) + \Gamma(s, x) = \Gamma(s)$ .

特别的, $\frac{\gamma\left(\frac{1}{2},x^2\right)}{\sqrt{\pi}}=\mathrm{erf}(x)$ 是误差函数.

# Zeta函数

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(Zeta函数)</b>

 $\zeta$ 函数定义为
    
 $$\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s}.$$ 

</div><br>

上式在 $ s>1 $ 的右半平面内收敛, 通过公式

 $$\zeta(s) = \frac{1}{\Gamma(s)} \int_0^{\infty} \frac{x^{s-1}}{e^x - 1}\, \mathrm{d}x$$ 

可将 $\zeta$ 函数延拓成为复平面上的亚纯函数, 其在 $s=1$ 处有唯一的 $ 1 $重极点, 留数为$ 1 $ .

设 $B_n$ 为伯努利数, 则对任意非负整数 $n$ , 都有

 $$\zeta(2n) = \frac{(-1)^{n+1} B_{2n} (2\pi)^{2n}}{2(2n)!},$$ 

 $$\zeta(-n) = (-1)^{n}\frac{ B_{n+1}}{n+1},$$ 

 $\zeta$ 函数在 $ s>1 $内无零点, 在$ s<0 $内零点只有负偶数, 黎曼猜想其余所有零点都位于直线$ \mathrm{Re}(s)=\frac{1}{2} $ 上.

 $\zeta$ 函数满足函数方程

 $$\zeta(s) = 2^s \pi^{s-1} \sin\left(\frac{\pi s}{2}\right) \Gamma(1-s) \zeta(1-s),$$ 

若定义 $\hat{\zeta}(s)= \pi^{-\frac{s}{2}} \Gamma\left(\frac{s}{2}\right) \zeta(s)$ , 则有

 $$\hat{\zeta}(s)=\hat{\zeta}(1-s).$$ 

 $\zeta$ 函数有欧拉乘积公式

 $$\zeta(s) = \prod_{p \in \mathbb{P}} \frac{1}{1 - p^{-s}},$$ 

其中 $\mathbb{P}$ 表示全体素数.

接下来是 $\zeta$ 函数的一些衍生函数.

赫尔维茨 Zeta 函数定义为

 $$\zeta(s, a) = \sum_{n=0}^{\infty} \frac{1}{(n+a)^s},$$ 

它亦可延拓为亚纯函数, 并满足某种函数方程, 其特殊值则与伯努利多项式相关.

狄利克雷 $\eta$ 函数定义为

 $$\eta(s) = \sum_{n=1}^{\infty} \frac{(-1)^{n-1}}{n^s} = (1 - 2^{1-s})\zeta(s),$$ 

狄利克雷 $\beta$ 函数定义为

 $$\beta(s) = \sum_{n=0}^{\infty} \frac{(-1)^{s}}{(2n+1)^s},$$ 

其特殊值则与欧拉数相关, $\beta(2)$ 称为卡塔兰常数.

# 贝塞尔函数

贝塞尔方程为如下的微分方程

 $$x^2\frac{\mathrm{d}^2y}{\mathrm{d}x^2}+x\frac{\mathrm{d}y}{\mathrm{d}x}+\left(x^2-a^2\right)y=0,$$ 

其中 $a\in\mathbb{R}$ 称为方程的阶, 其解统称为贝塞尔函数.

第一类贝塞尔函数由级数

 $$J_a(x) = \sum_{m=0}^{\infty} \frac{(-1)^m}{m! \Gamma(m+a+1)} \left( \frac{x}{2} \right)^{2m+a}$$ 

定义, 它是贝塞尔方程的解, 当 $a$ 不为整数时, $J_a(x)$ 与 $J_{-a}(x)$ 线性无关, 因此贝塞尔方程的通解就是 $C_1J_a(x)+C_2J_{-a}(x)$ , 而当 $ a $是整数时, 有关系式$ J_{-a}(x)=(-1)^aJ_a(x) $, 当$ a $ 是整数时, 第一类贝塞尔函数可由洛朗级数

 $$e^{\frac{x}{2}\left(t - \frac{1}{t}\right)} = \sum_{n=-\infty}^{\infty} J_n(x)t^n$$ 

生成.

第二类贝塞尔函数也称为诺依曼-韦伯函数, 由

 $$Y_a(x) = \frac{J_a(x)\cos(a\pi) - J_{-a}(x)}{\sin(a\pi)}$$ 

定义, 当 $ a $是整数时, 该式应按照极限理解, 它与$ J_a(x) $ 线性无关, 因此组成了贝塞尔方程的一组解系.

第三类贝塞尔函数也称为汉克尔函数, 由

 $$H_a^{(1)}(x) = J_a(x) + iY_a(x), \quad H_a^{(2)}(x) = J_a(x) - iY_a(x)$$ 

定义.

修正贝塞尔方程为

 $$x^2\frac{\mathrm{d}^2y}{\mathrm{d}x^2}+x\frac{\mathrm{d}y}{\mathrm{d}x}-\left(x^2+a^2\right)y=0,$$ 

它与通常贝塞尔方程仅差两个正负号, 第一类修正贝塞尔函数为

 $$I_a(x) = i^{-a} J_a(ix),$$ 

第二类修正贝塞尔函数为

 $$K_a(x) = \frac{\pi}{2} \frac{I_{-a}(x) - I_a(x)}{\sin(a\pi)}=\frac{\pi}{2} i^{a+1} H_a^{(1)}(ix),$$ 

由第三类贝塞尔函数的定义即可看出它无修正形式, 有时也将第二类修正贝塞尔函数称为第三类修正贝塞尔函数.

半整数阶的贝塞尔函数被称为球贝塞尔函数, 它是球贝塞尔方程

 $$x^2 \frac{\mathrm{d}^2y}{\mathrm{d}x^2} + 2x \frac{\mathrm{d}y}{\mathrm{d}x} + [x^2 - n(n+1)]y = 0$$ 

的解, 三类球贝塞尔函数分别为

 $$j_n(x) = \sqrt{\frac{\pi}{2x}} J_{n+\frac{1}{2}}(x), \quad y_n(x) = \sqrt{\frac{\pi}{2x}} Y_{n+\frac{1}{2}}(x),$$ 

 $$h_n^{(1)}(x) = j_n(x) + iy_n(x), \quad h_n^{(2)}(x) = j_n(x) - iy_n(x).$$ 

# 对数积分

对数积分定义为

 $$\mathrm{li}(x) = \int_{0}^{x} \frac{\mathrm{d}t}{\ln t},$$ 

当 $ x>1 $ 时, 该积分应按照柯西主值理解, 即

 $$\mathrm{li}(x) = \lim_{\varepsilon\to0} \left(\int_{0}^{1-\varepsilon} \frac{\mathrm{d}t}{\ln t}+\int_{1+\varepsilon}^x \frac{\mathrm{d}t}{\ln t}\right),$$ 

该式可延拓至复平面, 使得 $x=1$ 成为其唯一极点. 为了避开极点, 有欧拉形式对数积分定义为

 $$\mathrm{Li}(x) = \int_{2}^{x} \frac{\mathrm{d}t}{\ln t} = \mathrm{li}(x) - \mathrm{li}(2).$$ 

素数定理断言 $\pi(x)\sim \mathrm{li}(x)$ , 而黎曼猜想等价于其误差项为 $O\left(x^{\frac{1}{2}+\varepsilon}\right)$ , 其中 $\varepsilon>0$ 为任意正数. 对于较小的 $ x $, 总有$ \pi(x)<\mathrm{li}(x) $, 李特尔伍德证明了差值$ \mathrm{li}(x)-\pi(x) $会改变符号无穷多次, 而最小的使得$ \pi(x)>\mathrm{li}(x) $ 的整数被称为Skewes数, 仍未知其值为多少.

对数积分的唯一正零点称为Ramanujan–Soldner常数, 其值大约为 $1.4513\dots$ 

类似的, 有指数积分

 $$\mathrm{Ei}(x) = \int_{-\infty}^{x} \frac{e^t}{t} \, \mathrm{d}t,$$ 

当 $ x>0 $时仍按柯西主值理解, 它在复平面上有唯一极点, 即原点, 它与对数积分显然有关系$ \mathrm{li}(x) = \mathrm{Ei}(\ln x) $ . 正弦积分定义为

 $$\mathrm{Si}(x) = \int_{0}^{x} \frac{\sin t}{t} \, \mathrm{d}t,$$ 

余弦积分定义为

 $$\mathrm{Ci}(x) = \gamma + \ln x + \int_{0}^{x} \frac{\cos t - 1}{t} \, \mathrm{d}t,$$ 

其中 $\gamma$ 为欧拉-马斯刻若尼常数. 它们之间有关系式

 $$\mathrm{Ei}(ix) = \mathrm{Ci}(x) + i \left( \mathrm{Si}(x) - \frac{\pi}{2} \right).$$ 

此外还有另一种正余弦积分, 即菲涅耳积分

 $$\mathrm{S}(x) = \int_{0}^{x} \sin\left(\frac{\pi t^2}{2}\right) \, \mathrm{d}t, \quad \mathrm{C}(x) = \int_{0}^{x} \cos\left(\frac{\pi t^2}{2}\right) \, \mathrm{d}t,$$ 

此处使用Wolfram中使用的正规化定义.

# 多重对数函数

多重对数函数定义为

 $$\mathrm{Li}_s(z) = \sum_{k=1}^{\infty} \frac{z^k}{k^s},$$ 

其中 $ z $可解析延拓至复平面, 参数$ s $ 也可取任意复数值. 应小心多重对数函数与对数积分的符号混淆. 多重对数函数有递推公式

 $$\mathrm{Li}_{s+1}(z) = \int_{0}^{z} \frac{\mathrm{Li}_s(t)}{t} \mathrm{d}t,$$ 

 $$\frac{d}{dz} \mathrm{Li}_s(z) = \frac{1}{z} \mathrm{Li}_{s-1}(z).$$ 

以下是一些特例:

 $$\mathrm{Li}_1(z) = -\ln(1-z),$$ 

 $$\mathrm{Li}_2(z) = \int_{0}^{z} \frac{-\ln(1-t)}{t}\, \mathrm{d}t,$$ 

 $$\mathrm{Li}_s(1) = \zeta(s),$$ 

 $$\mathrm{Li}_s(-1) = -\eta(s).$$ 

类似的有多重指数函数

 $$\mathrm{E}_n(z) = \int_{1}^{\infty} \frac{e^{-zt}}{t^n}\,\mathrm{d} t,$$ 

有递推公式

 $$\mathrm{E}_{n+1}(z) = \frac{1}{n} \left( e^{-z} - z \mathrm{E}_n(z) \right),$$ 

 $$\frac{\mathrm{d}}{\mathrm{d}z} \mathrm{E}_n(z) = -\mathrm{E}_{n-1}(z),$$ 

多重指数函数与指数积分之间的关系为 $\mathrm{E}_1(z) = -\mathrm{Ei}(-z).$ 

# 超几何函数

回忆几何级数定义为

 $$\frac{1}{1-r}=\sum_{n=0}^\infty r^n,$$ 

为其添加更多参数, 高斯超几何函数定义为

 $$_2F_1(a, b; c; z) = \sum_{k=0}^{\infty} \frac{(a)_k (b)_k}{(c)_k} \frac{z^k}{k!},$$ 

其中 $(a)_k = a(a+1)(a+2)\dots(a+k-1)$ 为上升阶乘, 显然有 $_2F_1(1,b;b;z)=\frac{1}{1-r}$ .

超几何函数是超几何方程

 $$z(1-z)\frac{d^2w}{dz^2} + [c - (a + b + 1)z]\frac{dw}{dz} - abw = 0$$ 

的解. 概率论中超几何分布的名称也来源于此.

为超几何函数添加更多参数即得到广义超几何函数

 $$_pF_q \left[ \begin{matrix} a_1, a_2, \dots, a_p \\ b_1, b_2, \dots, b_q \end{matrix} ; z \right] = \sum_{k=0}^{\infty} \frac{\prod_{j=1}^p (a_j)_k}{\prod_{j=1}^q (b_j)_k} \frac{z^k}{k!},$$ 

作为特例, $_1F_1$ 称为合流超几何函数.

广义超几何函数有双边形式

 $$_pH_q \left[ \begin{matrix} a_1, a_2, \dots, a_p \\ b_1, b_2, \dots, b_q \end{matrix} ; z \right] = \sum_{k=-\infty}^{\infty} \frac{(a_1)_k (a_2)_k \cdots (a_p)_k}{(b_1)_k (b_2)_k \cdots (b_q)_k} z^k,$$ 

但它未必收敛.

广义超几何函数可以表示非常多已知的初等函数和特殊函数, 它还有其他各类推广.
