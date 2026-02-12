---
layout: post
title: "克利福德代数"
subtitle: ""
header-img: "img/post-bg-infinity.jpg"
header-mask: 0.3
math: true
tags:
  - 代数
  - 几何
---

# 定义

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(二次型)</b>

 设 $R$ 是一个交换环,  $M$ 是一个 $R$ -模, 映射 $q\colon M\to R$ 如果满足以下条件, 则称 $q$ 是 $M$ 上的一个二次型:
    
    1, $\forall x\in M$ ,  $r\in R$ , 都有 $q(rx)=r^2q(x)$ ;

    2, $\forall a,b,c\in M$ , 都有 $q(a+b+c)-q(a+b)-q(b+c)-q(c+a)+q(a)+q(b)+q(c)=0$ ;

    3, $\forall a,b\in M$ ,  $r\in R$ , 都有 $q(ra+b)-r^2q(a)-q(b)=rq(a+b)-rq(a)-rq(b)$ .

</div>

条件中等价于说 $B(x,y)=q(x+y)-q(x)-q(y)$ 是一个 $R$ -对称双线性型, 事实上, 如果 $R$ 的特征不为 $2$ 时, 所有的二次型与所有的对称双线性型一一对应, 反向的对应由 $q(x)=\frac{1}{2}B(x,x)$ 给出.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(二次空间)</b>

 若 $M$ 是一个 $R$ -模, 映射 $q\colon M\to R$ 是二次型, 则称 $(M,q)$ 是一个二次空间, 二次空间间的态射为保持二次型的线性映射.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(克利福德代数)</b>

 二次空间 $(M,q)$ 的克利福德代数定义为一个 $R$ -代数 $\mathrm{Cl}(M,q)$ , 配备 $R$ -线性映射 $j\colon M\to \mathrm{Cl}(M,q)$ , 使得 $j(x)^2=q(x)\cdot1$ , 并且满足如下泛性质. 设 $A$ 也是带有 $R$ -线性映射 $i\colon M\to A$ , 使得 $i(x)^2=q(x)\cdot1_A$ 的 $R$ -代数, 则一定存在一个 $R$ -代数同态 $\varphi\colon \mathrm{Cl}(M,q)\to A$ , 使得 $i=j\circ\varphi$ .

</div>

克利福德代数的唯一性由泛性质给出, 现说明其存在性.

设 $T^n(M)=\bigotimes_{k=1}^n M$ ,  $n>0$ ,  $T^0(M)=R$ , 则 $M$ 的张量代数为

$$
\displaylines{T(M)=\bigoplus_{n=0}^\infty T^n(M),}
$$

设 $I(M)$ 为 $\{ x\otimes x-q(x)\cdot1\mid x\in M\}$ 生成的理想, 则定义

$$
\displaylines{\mathrm{Cl}(M,q)=T(M)/I(M),}
$$

若设自然的嵌入映射 $i\colon M\to T(M)$ 和商映射 $\pi\colon T(M)\to \mathrm{Cl}(M,q)$ , 则 $j=\pi\circ i$ 即为定义中的 $j$ . 如果 $R$ 是域, 则 $j$ 是单射, 此时将 $x$ 和 $j(x)$ 看做相同, 若 $\dim M=m$ , 则 $\dim\mathrm{Cl}(M,q)=2^m$ .

<div style="border: 3px solid #000; padding: 10px;">

<b>例</b>

 设 $q(x)=0$ , 则 $\mathrm{Cl}(M,0)=\bigwedge M$ 为外代数.

</div>

设 $R$ 的特征不为 $2$ , 定义 $R$ -模 $M$ 上的自同构 $a\colon M\to M$ ,  $a(x)=-x$ , 记 $j'=j\circ a$ , 于是 $j'(x)^2=(-x)^2=x^2=j(x)^2$ , 因此 $(\mathrm{Cl}(M,q),j')$ 满足泛性质的条件, 故存在自同构 $\mathrm{Cl}(M,q)\to\mathrm{Cl}(M,q)$ , 仍记为 $a$ , 满足 $a|_{j(M)}(x)=-x$ . 定义

$$
\displaylines{\mathrm{Cl}^+(M,q)=\{x\mid x\in\mathrm{Cl}(M,q),a(x)=x\},}
$$


$$
\displaylines{\mathrm{Cl}^-(M,q)=\{x\mid x\in\mathrm{Cl}(M,q),a(x)=-x\},}
$$

由于 $a$ 满足 $a^2=\mathrm{id}$ , 其特征值即为 $\pm1$ , 于是有直和分解

$$
\displaylines{\mathrm{Cl}(M,q)=\mathrm{Cl}^+(M,q)\oplus\mathrm{Cl}^-(M,q),}
$$

显然这给出一个 $\mathbb{Z}_2$ -分次结构, 若 $R$ 是域, 则 $\dim \mathrm{Cl}^+(M,q)=\dim \mathrm{Cl}^+(M,q)=2^{\dim M-1}$ .






# 实情形

以下均设 $R=\mathbb{R}$ 为实数域,  $V$ 是实向量空间.

<div style="border: 3px solid #000; padding: 10px;">

<b>例</b>

 设 $V=\mathbb{R}$ , 于是 $T(\mathbb{R})=T^0(\mathbb{R})\oplus T^1(\mathbb{R})\oplus T^2(\mathbb{R})\oplus\cdots$ , 我们约定 $1\in \mathbb{R}=T^0(\mathbb{R})$ 和 $e\in T^1(\mathbb{R})$ 分别为第 $0$ 分次和第 $1$ 分次的基. 设 $q(x\cdot e)=-x^2$ , 于是 $j(e)^2=[e]^2=[e\otimes e]=[q(e)]=[-1]=-[1]$ , 我们记 $j(e)$ 为 $i$ , 记 $[1]$ 仍为 $1$ , 所以 $i^2=-1$ , 则 $\mathrm{Cl}(V,q)=\mathbb{C}$ 为复数集, 其中 $T^0(\mathbb{R})$ 的像为纯实数, $T^1(\mathbb{R})$ 的像为纯虚数.

</div>

通常的复数也叫圆复数.

<div style="border: 3px solid #000; padding: 10px;">

<b>例</b>

 仍设 $V=\mathbb{R}$ , 符号如上, 设 $q(x\cdot e)=x^2$ , 于是 $j(e)^2=[e]^2=[1]$ , 记 $[e]=j$ , 则 $j^2=1$ 而 $j\neq\pm1$ , 于是 $\mathrm{Cl}(V,q)$ 为双曲复数或分裂复数.

</div>

现取 $V=\mathbb{R}^n$ ,  $n$ 为正整数, 则由惯性定理, 在选取适当的基后,  $V$ 上的二次型一定有

$$
\displaylines{q(x_1e_1+\cdots+x_ne_n) = x_1^2 + \dots + x_p^2 - x_{p+1}^2 - \dots - x_{p+q}^2 + 0 \cdot (x_{p+q+1}^2 + \dots + x_{p+q+r}^2)}
$$

的形状, 其中 $p+q+r=n$ 为正惯性指数, 负惯性指数和退化项的个数, 此时我们将克利福德代数记为 $\mathrm{Cl}_{p,q,r}(\mathbb{R})$ .

如果 $r=0$ , 则简记为 $\mathrm{Cl}_{p,q}(\mathbb{R})$ , 而符号 $\mathrm{Cl}_{n}(\mathbb{R})$ 通常指代 $\mathrm{Cl}_{n,0}(\mathbb{R})$ 或 $\mathrm{Cl}_{0,n}(\mathbb{R})$ , 我们不使用这种可能引起混淆的符号. 按照这种记号, 则 $\mathrm{Cl}_{0,1}(\mathbb{R})$ 即为复数集,  $\mathrm{Cl}_{1,0}(\mathbb{R})$ 为双曲复数.

<div style="border: 3px solid #000; padding: 10px;">

<b>例</b>

 设 $V=\mathbb{R}$ ,  $q(x\cdot e)=0$ , 则 $j(e)^2=[e]^2=[0]$ , 记 $[e]=\varepsilon$ , 则 $\varepsilon^2=0$ 且 $\varepsilon\neq0$ , 于是 $\mathrm{Cl}(V,q)=\mathrm{Cl}_{0,0,1}(\mathbb{R})$ 为抛物复数或对偶数.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

 实数域上的二维代数在同构意义下只有复数, 双曲复数和对偶数, 它们都是可交换的.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

 设 $V=\mathbb{R}^2$ , 记 $1=(1,0)$ , 选取 $v=(a,b)$ 且 $b\neq0$ , 于是 $1$ 和 $v$ 组成 $V$ 的一组基, 我们设 $v^2$ 在这组基下表示为

$$
\displaylines{v^2=x\cdot 1+y\cdot v,}
$$

 令 $e=v-\frac{y}{2}\cdot 1$ , 于是

$$
\displaylines{e^2 = \left(v - \frac{y}{2}\cdot 1\right)^2 = v^2 - y\cdot v + \frac{y^2}{4}\cdot 1=\left(x+\frac{y^2}{4}\right)\cdot 1,}
$$

 我们设 $k=x+\frac{y^2}{4}$ , 于是 $e^2=k\cdot1$ .

 若 $k<0$ , 令 $i=\frac{e}{\sqrt{-k}}$ , 则有 $i^2=-1$ , 这样得到的代数结构就是 $\mathrm{Cl}_{0,1}(\mathbb{R})$ 复数集.

 若 $k>0$ , 令 $j=\frac{e}{\sqrt{k}}$ , 则有 $j^2=1$ , 这样得到的代数结构就是 $\mathrm{Cl}_{1,0}(\mathbb{R})$ 双曲复数.

 若 $k=0$ , 则 $e^2=0$ , 这样得到的代数结构就是 $\mathrm{Cl}_{0,0,1}(\mathbb{R})$ 对偶数.

</div>

从克利福德代数的角度来看, 二维实克利福德代数一定是一维空间 $V=\mathbb{R}$ 的克利福德代数, 即 $\mathrm{Cl}_{p,q,r}(\mathbb{R})$ , 其中 $p+q+r=1$ , 所以可能只有三种情况,  $\mathrm{Cl}_{1,0,0}(\mathbb{R})$ ,  $\mathrm{Cl}_{0,1,0}(\mathbb{R})$ 和 $\mathrm{Cl}_{0,0,1}(\mathbb{R})$ .

<div style="border: 3px solid #000; padding: 10px;">

<b>例</b>

 设 $V=\mathbb{R}^2$ ,  $1\in T^0(V)$ ,  $e_1,e_2\in T^1(V)$ ,  $q(xe_1+ye_2)=-x^2-y^2$ , 于是 $[e_1]^2=-[1]$ ,  $[e_2]^2=-[1]$ ,  $[e_1e_2]=-[1]$ , 设 $i=[e_1]$ ,  $j=[e_2]$ ,  $k=[e_1e_2]$ , 则 $\mathrm{Cl}(V,q)=\mathrm{Cl}_{0,2}(\mathbb{R})=\mathbb{H}$ 为四元数.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定理(弗罗贝尼乌斯定理)</b>

 $\mathbb{R}$ 上的有限维可除代数在同构意义下只有 $\mathbb{R}$ ,  $\mathbb{C}$ 和 $\mathbb{H}$ .

</div>

该定理的证明比较复杂且深刻, 顺带一提, 若放弃结合性, 有如下定理.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理(胡尔维兹定理)</b>

 $\mathbb{R}$ 上的有限维赋范可除代数在同构意义下只有 $\mathbb{R}$ ,  $\mathbb{C}$ ,  $\mathbb{H}$ 和八元数 $\mathbb{O}$ , 其中范数满足积性 $\|xy\|=\|x\|\|y\|$ .

</div>

若放弃有限维的条件, 则需要添加其他更强的条件.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理(Gelfand-Mazur 定理)</b>

 $\mathbb{R}$ 上任何满足可除性的巴拿赫代数在同构意义下只有 $\mathbb{R}$ ,  $\mathbb{C}$ 和 $\mathbb{H}$ .

</div><br>

克利福德代数有以下关系. 我们使用 $M_n(\mathbb{R})$ 表示元素均为实数的 $n$ 阶方阵代数.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

 1, $\mathrm{Cl}_{1,1}(\mathbb{R})\cong M_2(\mathbb{R})$ ;

 2, $\mathrm{Cl}_{p+1,q+1}(\mathbb{R})\cong \mathrm{Cl}_{p,q}(\mathbb{R})\otimes_{\mathbb{R}}\mathrm{Cl}_{1,1}(\mathbb{R})$ ;

 3, $M_n(\mathbb{R})\otimes_{\mathbb{R}} M_m(\mathbb{R})\cong M_{nm}(\mathbb{R})$ ;

 4, $\mathrm{Cl}_{n,n}(\mathbb{R})\cong M_{2^n}(\mathbb{R})$ ;

 5, $\mathrm{Cl}_{q,p+2}(\mathbb{R})\cong\mathrm{Cl}_{p, q}(\mathbb{R}) \otimes_{\mathbb{R}} \mathrm{Cl}_{0, 2}(\mathbb{R})$ ;

 6, $\mathrm{Cl}_{q+2,p}(\mathbb{R})\cong\mathrm{Cl}_{p, q}(\mathbb{R}) \otimes_{\mathbb{R}} \mathrm{Cl}_{2,0}(\mathbb{R})$ .

</div><br>

由以上递推公式可以推出实克利福德代数的结构, 它只与 $p-q$ 有关.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

 设 $p$ 和 $q$ 是非负整数, 则下表完全分类了 $\mathrm{Cl}_{p, q}(\mathbb{R})$ .
        
| $p - q\mod 8$ | $\mathrm{Cl}_{p, q}(\mathbb{R})$ | $d$ |
| :---: | :---: | :---: |
| $0$ | $\mathrm{M}_d(\mathbb{R})$ | $2^{\frac{p+q}{2}}$ |
| $1$ | $\mathrm{M}_d(\mathbb{C})$ | $2^{\frac{p+q-1}{2}}$ |
| $2$ | $\mathrm{M}_d(\mathbb{H})$ | $2^{\frac{p+q-2}{2}}$ |
| $3$ | $\mathrm{M}_d(\mathbb{H}) \times \mathrm{M}_d(\mathbb{H})$ | $2^{\frac{p+q-3}{2}}$ |
| $4$ | $\mathrm{M}_d(\mathbb{H})$ | $2^{\frac{p+q-2}{2}}$ |
| $5$ | $\mathrm{M}_d(\mathbb{C})$ | $2^{\frac{p+q-1}{2}}$ |
| $6$ | $\mathrm{M}_d(\mathbb{R})$ | $2^{\frac{p+q}{2}}$ |
| $7$ | $\mathrm{M}_d(\mathbb{R}) \times \mathrm{M}_d(\mathbb{R})$ | $2^{\frac{p+q-1}{2}}$ |

</div>

该定理与拓扑K理论中的Bott周期律相关.







# 复情形

复数情形比较简单, 由于复数域上的所有二次型都能通过选取基底成为

$$
\displaylines{q(x_1e_1+\cdots+x_ne_n)=x_1^2+\cdots+x_n^n}
$$

的形状, 我们记 $\mathrm{Cl}_n(\mathbb{C})=\mathrm{Cl}(\mathbb{C},q)$ .

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>


$$
\displaylines{\mathrm{Cl}_n(\mathbb{C}) \simeq \left\{ \begin{array}{cc} M_d(\mathbb{C}) \times M_d(\mathbb{C}), & 2\nmid n; \\ M_d(\mathbb{C}), & 2|n, \end{array} \right.}
$$

 其中 $2\nmid n$ 时,  $d = 2^{\frac{n-1}{2}}$ ,  $2|n$ 时,  $d = 2^{\frac{n}{2}}$ .

</div>
