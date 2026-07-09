---
layout: post
title: "八元数"
subtitle: ""
header-img: "img/post-bg-infinity.jpg"
header-mask: 0.3
math: true
tags:
  - 代数
  - 非结合代数
---


# Cayley-Dickson代数

本节参考自 [li2022algebraic] 第七章习题5和6.

以下均设 $F$ 为域, $A$ 为有限维 $F$-模, $A$ 中交换群运算记为加法, 在 $A$ 上有一个未必交换也未必结合的乘法运算, 但满足分配律, 并且含有幺元, 则称 $A$ 是一个非结合代数, 以下将非结合代数简称为代数.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(结合子)</b>

设 $x,y,z\in A$, 定义其结合子为

$$[x,y,z]=(xy)z-x(yz).$$

</div>

若 $[x,x,y]=[x,y,y]=0$ 恒成立, 则称 $A$ 是交错代数, 该恒等式称为交错律, Atin的一个定理指出, 一个代数交错当且仅当其中任意两个元素生成的子代数结合([schafer1995introduction]第三章). 若 $x\in A$, $(xx)x=x(xx)$ 且 $(xx)(xx)=((xx)x)x$, 则称 $A$ 是幂结合的, 这等价于说由 $x$ 生成的 $A$ 的子代数是结合的, 幂结合代数中可以自由的使用幂次符号 $x^n$.

一个代数是可除的当且仅当对任意 $x,y\in A$, 若 $xy=0$, 总有 $x=0$ 或 $y=0$. 当代数结合时, 该条件显然等价于任何非零元素都有乘法逆元(注意 $A$ 有限维这一条件是必须的), 但当代数非结合时则未必成立.

<div style="border: 3px solid #000; padding: 10px;">

<b>引理</b>

结合子对每个变元都是线性的, 当 $A$ 交错时, 有 $[x,y,z]=-[y,x,z]$ 和 $[x,y,z]=-[x,z,y]$.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

线性性由分配律直接验证即可. 当 $A$ 交错时,

$$0=[x+y,x+y,z]=[x,x,z]+[x,y,z]+[y,x,z]+[y,y,z],$$

而 $[x,x,z]=[y,y,z]=0$, 故 $[x,y,z]+[y,x,z]=0$, 即 $[x,y,z]=-[y,x,z]$, 同理可得 $[x,y,z]=-[x,z,y]$.

</div>

设映射 $(-)^*\in\operatorname{End}_F(A)$ 为自同态, 并且满足 $(xy)^*=y^*x^*$, $1_A^*=1_A$, $x^{**}=x$, 则称 $*$ 为 $A$ 上的对合, 带对合的代数称为 $*$-代数.

<div style="border: 3px solid #000; padding: 10px;">

<b>引理</b>

设对合 $*$ 满足 $t(x)=x+x^*\in F\cdot 1_A$, $n(x)=x^*x=xx^*\in F\cdot1_A$, 则任意 $x\in A$ 都满足二次方程 $x^2-t(x)x+n(x)1_A=0$.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

直接验证即可.

</div>

此后均要求对合满足该条件.

<div style="border: 3px solid #000; padding: 10px;">

<b>引理</b>

设 $A$ 交错且带有满足上一引理条件的对合 $*$, 则有 $(xy)y^*=n(y)x$, $x^*(xy)=n(x)y$, $n(xy)=n(x)n(y)$.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

由 $[x,y,y^*]=[x,y,y^*]+[x,y,y]=[x,y,t(y)]$ 和 $t(y)\in F\cdot1_A$ 知 $[x,y,y^*]=0$, 即 $(xy)y^*=n(y)x$, 同理 $x^*(xy)=n(x)y$.

由于 $n(xy)=(xy)(xy)^*=(xy)(y^*x^*)=((xy)y^*)x^*-[xy,y^*,x^*]=n(x)n(y)-[xy,y^*,x^*]$, 我们只需证明 $[xy,y^*,x^*]=[x^*,xy,y^*]=0$, 这等价于说 $n(x)n(y)-n(x)n(y)=0$, 显然成立.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>引理</b>

条件如上, 定义对称双线性型 $B(x,y)=n(x+y)-n(x)-n(y)$, 则有

$$B(xy,xz)=n(x)B(y,z)=B(yx,zx),$$

$$B(xz,wy)+B(xy,wz)=B(x,w)B(y,z),$$

$$B(xy,z)=B(y,x^*z)=B(x,zy^*).$$

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

$B(xy,xz)=n(xy+xz)-n(xy)-n(xz)=n(x)(n(y+z)-n(y)-n(z))=n(x)B(y,z)$, 由标量的交换性知亦有 $n(x)B(y,z)=B(yx,zx)$. 直接计算即可验证 $B(xz,wy)+B(xy,wz)=B(x,w)B(y,z)$.

令 $w=1_A$ 得 $B(xz,y)+B(xy,z)=B(x,1_A)B(y,z)$, 而

$$B(x,1_A)=n(x+1_A)-n(x)-1_A=n(x)+x+x^*+1_A-n(x)-1_A=t(x),$$

于是有

$$B(xy,z)=t(x)B(y,z)-B(xz,y)=B(y,t(x)z)-B(y,xz)=B(y,x^*z),$$

同理可得 $B(xy,z)=B(x,zy^*)$.

</div>

以后均要求 $A$ 满足如下非退化性质:

$$B(x,-)=0\Longleftrightarrow x=0\Longleftrightarrow B(-,x)=0$$

对 $\forall x\in A$ 均成立.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(Cayley-Dickson代数)</b>

设 $A$ 是有限维非结合 $F$-代数, 并且带有对合 $*$ 满足 $x+x^*\in F\cdot 1_A$, $x^*x=xx^*\in F\cdot 1_A$ 对任意 $x\in A$ 成立, 约定 $t(x)=x+x^*$, $n(x)=x^*x$, 并且假设 $B_n(x,y)=n(x+y)-n(x)-n(y)$ 满足非退化条件. 对任意的 $\lambda\in F$, 定义 $A$ 的Cayley-Dickson代数为

$$\operatorname{CD}(A,\lambda)=A\oplus A,$$

加法逐分量计算, 乘法定义为

$$(a,b)\cdot(a',b')=(aa'+\lambda b'b^*,a^*b'+a'b),$$

再定义 $N(a,b)=n(a)-\lambda n(b)$, $\overline{(a,b)}=(a^*,-b)$, 通常引入形式符号 $v$, 将 $(a,b)$ 记为 $a+vb$, 显然 $v^2=v\cdot v=\lambda$.

</div>

注意我们使用点乘 $x\cdot y$ 表示 $\operatorname{CD}(A,\lambda)$ 中的乘法, 而并置 $ab$ 表示 $A$ 中的乘法. 容易验证 $a\cdot b=ab$, $v\cdot a=(0,a)=va$, 其中 $a,b\in A$, 这说明了我们符号的正当性.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

以上定义的 $\operatorname{CD}(A,\lambda)$ 是有限维非结合 $F$-代数, 幺元为 $(1_A,0)=1_A+v\cdot0$, 并且按第一分量的嵌入 $A\to A\oplus A$ 使得 $A$ 成为 $\operatorname{CD}(A,\lambda)$ 的子代数, $\overline{(-)}$ 是其上对合.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

验证乃例行公事.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

定义 $T(x)=x+\overline{x}$, 则对任意 $x\in\operatorname{CD}(A,\lambda)$, 都有 $T(x)\in F\cdot 1$ 和 $N(x)\in F\cdot1$, 这里 $1$ 为幺元 $(1_A,0)$, 并且满足 $N(x)=x\cdot\overline{x}=\overline{x}\cdot x$, 且当 $\lambda\neq0$ 时, $B_N(x,y)=N(x+y)-N(x)-N(y)$ 非退化.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

假设 $x=a+vb$, 则 $T(x)=a+vb+a^*-vb=a+a^*=t(a)\in F\cdot 1_A$, 这里我们自然的将 $A$ 视为 $\operatorname{CD}(A,\lambda)$ 的子代数.

同理 $N(x)=n(a)-\lambda n(b)\in F\cdot 1$, $x\cdot\overline{x}=(a+vb)\cdot(a^*-vb)=aa^*-\lambda bb^*=N(x)$.

设 $y=c+vd$, 则

$$B_N(x,y)=B_n(a,c)-\lambda B_n(b,d),$$

若 $B_N(x,-)=0$, 由 $\lambda\neq0$ 可知必有 $B_n(a,-)=0$ 且 $B_n(b,-)=0$, 由 $B_n$ 非退化知 $x=0$.

</div>

该定理说明当 $\lambda\neq0$ 时, 若一个代数有Cayley-Dickson代数, 则其Cayley-Dickson代数也有Cayley-Dickson代数.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

$A$ 结合等价于 $\operatorname{CD}(A,\lambda)$ 交错, $A$ 交换等价于 $\operatorname{CD}(A,\lambda)$ 结合, $A=F$ 等价于 $\operatorname{CD}(A,\lambda)$ 交换.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

设 $A$ 结合, 令 $x=a+vb$, $y=c+vd\in\operatorname{CD}(A,\lambda)$, 直接计算得

$$(x\cdot x)\cdot y = (a^2c + \lambda n(b)c + \lambda t(a)db^*) + v((a^*)^2d + \lambda n(b)d + t(a)cb),$$

$$x\cdot(x\cdot y) = (a(ac + \lambda db^*) + \lambda (a^*d + cb)b^*) + v(a^*(a^*d + cb) + (ac + \lambda db^*)b),$$

由结合律得 $[x,x,y]=0$, 同理 $[x,y,y]=0$, 即 $\operatorname{CD}(A,\lambda)$ 交错. 现设 $\operatorname{CD}(A,\lambda)$ 交错, 对任意的 $a,b,c,d\in A$, 由先前引理可知

$$N((a+vb)\cdot(c+vd))=N(a+vb)\cdot N(c+vd),$$

即

$$n(ac+\lambda db^*)-\lambda n(a^*d+cb)=n(a)n(c)+\lambda^2 n(b)n(d)-\lambda(n(a)n(d)+n(b)n(c)),$$

整理得

$$n(ac+\lambda db^*)-n(ac)-n(\lambda db^*)=\lambda(n(a^*d+cb)-n(a^*d)-n(cb)),$$

即

$$B_n(ac,\lambda db^*)=\lambda B_n(a^*d,cb),$$

由对称双线性性可消掉 $\lambda$, 得

$$B_n(ac,db^*)=B_n(cb,a^*d),$$

又由先前引理可得

$$B_n((ac)b,d)=B_n(ac,db^*)=B_n(cb,a^*d)=B_n(a(cb),d),$$

$$B_n((ac)b-a(cb),d)=0,$$

由于 $d$ 是任取的, $B_n$ 的非退化性导出 $(ac)b-a(cb)=0$, 这就是结合律.

设 $A$ 交换, 令 $x=a+vb$, $y=c+vd$,$z=e+vf\in\operatorname{CD}(A,\lambda)$, 计算

$$(x\cdot y)\cdot z = (ace + \lambda(dbe + fad + fcb)) + v(acf + dbf + ead + ecb),$$

$$x\cdot (y\cdot z) = (ace + \lambda(afd + cfb + edb)) + v(acf + aed + ceb + fdb),$$

由 $A$ 的交换律得 $(x\cdot y)\cdot z=x\cdot(y\cdot z)$. 现设 $\operatorname{CD}(A,\lambda)$ 结合, 对任意的 $a,b\in A$, 由结合律得 $v\cdot(a\cdot b)=(v\cdot a)\cdot b$, 又 $(v\cdot a)\cdot b=(0+va)(b+v\cdot0)=v(ba)$, $v\cdot (a\cdot b)=v(ab)$, 故 $v(ab)=v(ba)$, 这相当于说 $(0,ab)=(0,ba)$, 比较第二分量得 $ab=ba$, 交换律得证.

设 $A=F$, 则必有 $a^*=a$, $\operatorname{CD}(A,\lambda)$ 中乘法退化为

$$(a+vb)\cdot(a'+vb')=aa'+\lambda b'b+v(ab'+a'b),$$

又因 $A=F$ 时 $A$ 显然可交换, 由上式可知 $\operatorname{CD}(A,\lambda)$ 可交换. 现设 $\operatorname{CD}(A,\lambda)$ 可交换, 对任意 $a\in A$, 有 $a\cdot v=v\cdot a$, 即 $va=va^*$, 于是 $a=a^*$, 由 $a+a^*\in F\cdot1_A$ 知 $2a\in F\cdot1_A$, 若 $F$ 的特征不为 $2$, 则必有 $a\in F\cdot1_A$, 即 $A=F$. 假设 $F$ 特征 $2$, 由于 $A$ 是 $\operatorname{CD}(A,\lambda)$ 的子代数, 则 $A$ 也交换, 因为 $n(a)=aa^*=a
^2$, 则

$$B_n(a,b)=(a+b)^2-a^2-b^2=ab+ba=2ab=0$$

完全退化，这与先前的约定矛盾，因此 $F$ 的特征不可能为 $2$, 这就完成了定理的证明.

</div>

该定理有几个显然的推论, 首先由证明过程可知特征 $2$ 的域上的交换代数不存在Cayley-Dickson代数. 若一个存在Cayley-Dickson代数的代数交换, 则它一定结合, 这是因为结合代数一定是交错的. 任何Cayley-Dickson代数若交换, 则它一定结合, 这是因为 $A=F$ 也交换. 注意对于一般的代数, 交换并不蕴含结合.

# 八元数的构造

取 $A=F=\mathbb R$, $\lambda=-1$, 显然

$$\operatorname{CD}(\mathbb {R},-1)\cong\mathbb {C},$$

$$\operatorname{CD}(\mathbb {C},-1)\cong\mathbb {H},$$

$$\operatorname{CD}(\mathbb {H},-1)\cong\mathbb {O},$$

其中 $\mathbb{C}$ 是复数域, $\mathbb{H}$ 是四元数代数, $\mathbb{O}$ 成为八元数代数. 由上节定理可知 $\mathbb{C}$ 交换且结合, $\mathbb{H}$ 非交换但结合, $\mathbb{O}$ 非交换且非结合, 但是是交错代数.

除八元数外, 这些构造与克利福德代数中的构造是同构的, 区别是克利福德代数不处理非结合代数, 详见本网站克利福德代数的网页. 当 $\lambda$ 取 $1$ 或 $0$ 时也能构造出双曲复数和对偶数.

<div style="border: 3px solid #000; padding: 10px;">

<b>引理</b>

设 $A$ 是有限维交错代数, 则 $A$ 中非零元可逆等价于 $A$ 可除.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

假设 $A$ 可除, 这等价于说任何非零元 $a$ 定义的左乘映射 $L_a$ 和右乘映射 $R_a$ 均为双射, 这等价于说任何非零元都有左逆和右逆, 设非零元 $a$ 的左逆为 $b$, 右逆为 $c$. 由交错律知 $a=a(ba)=(ab)a$, 于是 $(1_A-ab)a=0$, 由于 $a\neq0$, 于是 $1_A=ab$, 故 $b$ 也是右逆, 同理 $c$ 也是左逆, $b=c$.

假设 $A$ 中任意非零元均可逆, 取 $a\neq0$, 设其逆为 $a^{-1}$, 由于 $A$ 有限维, 不妨设 $n=\dim A$, 则 $1_A,a, a^2,\dots,a^n$ 线性相关, 故 $a$ 存在极小多项式 $x^m+c_{m-1}x^{m-1}+\cdots+c_1x+c_0$, 其中诸 $c_i\in F$. 现假设 $c_0=0$, 则有

$$a^m + c_{m-1}a^{m-1} + \dots + c_1 a = 0,$$

由于交错代数一定满足幂结合性, 则

$$a \cdot (a^{m-1} + c_{m-1}a^{m-2} + \dots + c_1 \cdot 1_A) = 0,$$

左乘逆元得

$$a^{-1} \cdot \left( a \cdot (a^{m-1} + c_{m-1}a^{m-2} + \dots + c_1 \cdot 1_A) \right) = a^{-1} \cdot 0 = 0,$$

由于该式中只含 $a$ 和 $a^{-1}$ 两个元素, 它们生成的子代数一定结合, 则有

$$\left( a^{-1} \cdot a \right) \cdot (a^{m-1} + c_{m-1}a^{m-2} + \dots + c_1 \cdot 1_A) = 0,$$

$$a^{m-1} + c_{m-1}a^{m-2} + \dots + c_1 \cdot 1_A = 0,$$

这与极小多项式的定义矛盾, 故 $c_0\neq0$. 于是有

$$a \cdot \left( -\frac{1}{c_0} a^{m-1} - \frac{c_{m-1}}{c_0} a^{m-2} - \dots - \frac{c_1}{c_0} \cdot 1_A \right) = 1_A,$$

由逆元的唯一性可知

$$a^{-1} = -\frac{1}{c_0} a^{m-1} - \frac{c_{m-1}}{c_0} a^{m-2} - \dots - \frac{c_1}{c_0} \cdot 1_A,$$

即 $a^{-1}$ 在 $a$ 生成的子代数中. 现设 $A$ 中任意两元素 $a$ 和 $b$ 满足 $ab=0$, 假设 $a\neq0$, 则有

$$a^{-1}(ab)=0,$$

由于 $a^{-1}$, $a$ 和 $b$ 这三个元素均在 $a$ 和 $b$ 生成的子代数中, 所以是可结合的, 故能推出

$$a^{-1}(ab)=(a^{-1}a)b=b=0,$$

所以 $A$ 是可除的.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>引理</b>

设 $A$ 是具有Cayley-Dickson代数构造的 $\mathbb{R}$-代数, 满足 $A$ 中任意非零元 $a$ 都有 $n(a)>0$, 则当 $\lambda<0$ 时, $\operatorname{CD}(A,\lambda)$ 中任何非零元都可逆.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

设 $x=a+vb$ 是 $\operatorname{CD}(A,\lambda)$ 中任一非零元, 则 $a\neq0$ 或 $b\neq0$, 则 $n(a)>0$ 或 $n(b)>0$, 又由 $\lambda<0$ 知 $N(x)=n(a)-\lambda n(b)>0$, 而已知 $x\overline{x}=\overline{x}x=N(x)$, 则显然

$$x^{-1}=\frac{\overline{x}}{N(x)}.$$

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

八元数代数 $\mathbb{O}$ 是可除的.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

已知 $\mathbb{O}$ 是交错的, 应用以上两个引理即可.

</div>

现在显式的叙述八元数的结构, 它是 $\mathbb{R}$ 上的八维向量空间, 设基为 $1,e_1,\dots,e_7$, 有以下乘法表.

$$
\begin{array}{|c|c|c|c|c|c|c|c|c|}
\hline
 & 1 & e_1 & e_2 & e_3 & e_4 & e_5 & e_6 & e_7 \\
\hline
1 & 1 & e_1 & e_2 & e_3 & e_4 & e_5 & e_6 & e_7 \\
\hline
e_1 & e_1 & -1 & e_4 & e_7 & -e_2 & e_6 & -e_5 & -e_3 \\
\hline
e_2 & e_2 & -e_4 & -1 & e_5 & e_1 & -e_3 & e_7 & -e_6 \\
\hline
e_3 & e_3 & -e_7 & -e_5 & -1 & e_6 & e_2 & -e_4 & e_1 \\
\hline
e_4 & e_4 & e_2 & -e_1 & -e_6 & -1 & e_7 & e_3 & -e_5 \\
\hline
e_5 & e_5 & -e_6 & e_3 & -e_2 & -e_7 & -1 & e_1 & e_4 \\
\hline
e_6 & e_6 & e_5 & -e_7 & e_4 & -e_3 & -e_1 & -1 & e_2 \\
\hline
e_7 & e_7 & e_3 & e_6 & -e_1 & e_5 & -e_4 & -e_2 & -1 \\
\hline
\end{array}
$$

也可由以下几条性质刻画该表:
- $e_i^2=-1$, 其中 $i=1,\dots7$;
- $e_ie_j=-e_je_i$, 其中 $i\neq j$;
- 若 $e_ie_j=e_k$, 则 $e_{i+1}e_{j+1}=e_{k+1}$, 其中下标模 $7$ 计算;
- 若 $e_ie_j=e_k$, 则 $e_{2i}e_{2j}=e_{2k}$, 其中下标模 $7$ 计算.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理(Hurwitz定理)</b>

$\mathbb{R}$ 上的有限维赋范可除代数只有 $\mathbb{R}$, $\mathbb{C}$, $\mathbb{H}$ 和 $\mathbb{O}$.

</div>

<br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定理(Zorn定理)</b>

$\mathbb{R}$ 上的有限维可除交错代数只有 $\mathbb{R}$, $\mathbb{C}$, $\mathbb{H}$ 和 $\mathbb{O}$.

</div>

<br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定理(Bott-Milnor-Kervaire定理)</b>

$\mathbb{R}$ 上的有限维可除代数的维数只能是 $1$, $2$, $4$ 或 $8$.

</div>

# 射影空间

域上的射影空间的定义是熟知的, 即 $\mathbb{KP}^n=(\mathbb{K}^{n+1}-\\\{0\\\})/\sim$, 其中等价关系 $\sim$ 为 $x\sim y\Longleftrightarrow x=a y$, $x,y\in\mathbb{K}^{n+1}-\\\{0\\\},a\in\mathbb{K}-\\\{0\\\}$.

对于带对合的可除结合代数, 例如 $\mathbb{H}$, 类似的定义也是可行的, 只是等价关系有两种定义方式, 即左乘 $x=ay$ 和右乘 $x=ya$, 不妨设这样定义出的两个空间为 $\mathbb{KP}^n$ 和 $\mathbb{KP}^n_1$, 我们定义映射

$$\mathbb{KP}^n\to\mathbb{KP}^n_1$$

$$(x_0:\cdots:x_{n})\mapsto(\overline{x_0}:\cdots:\overline{x_{n}}),$$

其中 $\overline{(-)}$ 是对合, 若 $(x_0,\dots,x_{n})=a(y_0,\dots,y_n)$, 则

$$(\overline{x_0},\dots, \overline{x_n})=(\overline{ay_0},\dots,\overline{ay_n})=(\overline{y_0},\dots,\overline{y_n})\overline{a},$$

所以这样的映射是良定的双射, 因此我们可以不区分 $\mathbb{KP}^n$ 和 $\mathbb{KP}^n_1$. 特别的, 当 $\mathbb{K}=\mathbb{H}$ 时, 将 $\mathbb{KP}^n$ 和 $\mathbb{KP}^n_1$ 看做实流形, 它们还是微分拓扑的.

对于射影直线, 显然 $\mathbb{RP}^1\cong S^1$, $\mathbb{CP}^1\cong S^2$, 可以证明 $\mathbb{HP}^1\cong S^4$. 因此我们期望对于非结合代数也可以定义某种射影直线, 尤其是 $\mathbb{OP}^1$, 并且它应该同胚于 $S^8$. 先前的构造方式对于非结合代数是不成立的, 因为关系 $\sim$ 是未必传递的, 若 $x=ay$, $y=bz$, 则只有 $x=a(bz)$, 未必有 $x=(ab)z$, 因此我们需要另一种构造方式.

以下设 $A$ 是一个有限维未必结合的 $F$-代数, $F$ 的特征不为 $2$, 带有对合 $\overline{(-)}$, 设 $M_n(A)$ 为 $A$ 上的 $n$ 阶矩阵代数, 注意矩阵乘法未必结合.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义</b>

设 $M\in M_n(A)$, 定义其伴随矩阵为 $M^*$, 若 $M=(a_{ij})$, 则 $M^*=(\overline{a_{ji}})$, 即每个元素取对合后再转置.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(Hermite矩阵)</b>

设 $M\in M_n(A)$, 并且 $M=M^*$, 则称 $M$ 是一个Hermite矩阵, 所有Hermite矩阵组成的集合记为 $\mathfrak{h}_n(A)$, 在其上定义乘法

$$M\circ N=\frac{1}{2}(MN+NM)$$

使其成为一个交换代数, 注意它仍未必结合.

</div>

以上定义中的乘法 $\circ$ 称为Jordan乘法, 容易验证Jordan乘法对于Hermite矩阵是封闭的, 并且满足以下Jordan恒等式

$$(M\circ N)\circ(M\circ M)=M\circ(N\circ(M\circ M)).$$

事实上, 代数 $\mathfrak{h}_n(A)$ 是所谓的Jordan代数的特例.

显然对任意Hermite矩阵 $M$, 有 $M\circ M=MM$, 我们称幂等元为一个投影, 即投影为满足 $M^2=M$ 的Hermite矩阵, 此处平方符号理解为矩阵乘法或Jordan乘法都无所谓.

现考虑 $\mathfrak{h}_2(A)$ 中的投影, 零矩阵和单位矩阵显然是投影, 可以验证除此之外的投影都有

$$ 
\begin{pmatrix}
a \\ b
\end{pmatrix}
\begin{pmatrix}
\overline{a} & \overline{b}
\end{pmatrix}
=
\begin{pmatrix}
a\overline{a} & a\overline{b} \\
b\overline{a} & b\overline{b}
\end{pmatrix}
$$

的形式, 其中 $(a,b)\in A^2$, $n(a)+n(b)=a\overline{a}+b\overline{b}=1_A$. 我们将这些矩阵组成的集合称为 $A$ 的射影直线, 即

$$A\mathbb{P}^1=\\\{M\in\mathfrak{h}_2(A):M^2=M,M\neq0,1\\\},$$

其中 $0$ 和 $1$ 分别为零矩阵和单位矩阵.

显然可以将它等同为 $A^2$ 中满足 $n(a)+n(b)=1_A$ 的元素 $(a,b)$ 组成的集合商掉一个等价关系, $(a,b)\sim(c,d)$ 当且仅当

$$\begin{pmatrix}
a \\ b
\end{pmatrix}
\begin{pmatrix}
\overline{a} & \overline{b}
\end{pmatrix}
=\begin{pmatrix}
c \\ d
\end{pmatrix}
\begin{pmatrix}
\overline{c} & \overline{d}
\end{pmatrix},
$$

当 $A$ 上带拓扑时可以赋予其商拓扑, 我们来证明这与之前的构造是相同的.

<div style="border: 3px solid #000; padding: 10px;">

<b>引理</b>

设 $A$ 是带对合的有限维可除结合 $F$-代数, 则 $(a,b)\sim(c,d)$ 当且仅当存在 $u\in A$, $u\overline{u}=1_A$, 并且 $(a,b)=(c,d)u$.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

若 $(a,b)=(c,d)u$, 则

$$ 
\begin{pmatrix}
a \\ b
\end{pmatrix}
\begin{pmatrix}
\overline{a} & \overline{b}
\end{pmatrix}
=
\begin{pmatrix}
c(u\overline{u})\overline{c} & c(u\overline{u})\overline{d} \\
d(u\overline{u})\overline{c} & d(u\overline{u})\overline{d}
\end{pmatrix}
=
\begin{pmatrix}
c\overline{c} & c\overline{d} \\
d\overline{c} & d\overline{d}
\end{pmatrix}
=
\begin{pmatrix}
c \\ d
\end{pmatrix}
\begin{pmatrix}
\overline{c} & \overline{d}
\end{pmatrix}.
$$

反之, 若 $\begin{pmatrix}
a \\ b
\end{pmatrix}
\begin{pmatrix}
\overline{a} & \overline{b}
\end{pmatrix}
=\begin{pmatrix}
c \\ d
\end{pmatrix}
\begin{pmatrix}
\overline{c} & \overline{d}
\end{pmatrix},
$
当 $a\neq0$ 时, 令 $u=a^{-1}c$, 则 $au=c$. 由 $a\overline{a}=c\overline{c}=a(u\overline{u})\overline{a}$ 可知 $u\overline{u}=1$. 因为 $a\overline{b}=c\overline{d}=au\overline{d}$, 左乘 $a^{-1}$ 得 $\overline{b}=u\overline{d}$, 取对合得 $b=d\overline{u}$, 右乘 $u$ 得 $bu=d$, 故 $(a,b)u=(c,d)$, $(a,b)=(c,d)\overline{u}$. 当 $a=0$ 时, 绝不可能有 $b=0$, 对 $b$ 做相同的构造即可.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>引理</b>

设 $A$ 是带对合的有限维可除结合 $\mathbb{R}$-代数, 并且 $A$ 中非零元 $a$ 满足 $n(a)>0$, 则上述构造的两种射影空间之间存在双射.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

对于 $A^2-\\\{0\\\}$ 中的元素 $(a,b)$, 均可标准化为

$$\frac{1}{\sqrt{n(a)+n(b)}}(a,b),$$

该标准化过程保持右乘的等价关系, 因此显然两种射影空间之间存在双射.

</div>

当 $F=\mathbb{R}$ 时, 可以为射影直线赋予实流形结构, 由Hurwitz定理知以上构造的射影直线只有 $\mathbb{RP}^1$, $\mathbb{CP}^1$, $\mathbb{HP}^1$ 和 $\mathbb{OP}^1$ 四种. 因此以下设 $\mathbb{K}=\mathbb{R}$ 或 $\mathbb{C}$ 或 $\mathbb{H}$ 或 $\mathbb{O}$, $d=\dim_\mathbb{R}\mathbb{K}=1$ 或 $2$ 或 $4$ 或 $8$.

设 $(a,b)\in\mathbb{K}^2-\\\{0\\\}$, 以 $[(a,b)]$ 记 $(a,b)$ 的标准化所在的等价类. 设 $U_1=\\\{[(a,b)]:b\neq0\\\}$, $U_1=\\\{[(a,b)]:a\neq0\\\}$, 定义 $\varphi_1\colon U_1\to\mathbb{R}^d$, $[(a,b)]\mapsto ab^{-1}$, $\varphi_2\colon U_2\to\mathbb{R}^d$, $[(a,b)]\mapsto ba^{-1}$, 显然 $\varphi_1$ 和 $\varphi_2$ 是良定的光滑映射, 而在 $U_1\cap U_2$ 内, 令 $z=ab^{-1}$, 则

$$\varphi_2\circ\varphi_1^{-1}(z)=ba^{-1}=\left(ab^{-1}\right)^{-1}=z^{-1}$$

是光滑映射(此处依赖于交错律), 这样 $\mathbb{KP}^1$ 就是一个 $d$ 维光滑实流形, 它与 $S^d$ 微分同胚只是 $d$ 为 $1$ 或 $2$ 时标准方法的重复.

# Hopf纤维化

先前说道, $\mathbb{KP}^1$ 是 $\mathbb{K}^2$ 中满足 $n(a)+n(b)=1_\mathbb{K}$ 的元素 $(a,b)$ 组成的集合的商集, 考虑 $\mathbb{K}=\mathbb{R}$ 时, $n(a)+n(b)=1_\mathbb{K}$ 就是 $a^2+b^2=1$, 即单位圆 $S^1$, 当 $\mathbb{K}=\mathbb{C}$ 时, $n(a)+n(b)=1_\mathbb{K}$ 就是 $|a|^2+|b|^2=1$, 设 $a=x+iy$, $b=z+iw$, 就是 $x^2+y^2+z^2+w^2$, 即四维实空间中的球面 $S^3$, 同理, 由Cayley-Dickson代数的构造知, 该集合就是球面 $S^{2d-1}$, 其中 $d=1$ 或 $2$ 或 $4$ 或 $8$, 所以有商映射

$$S^{2d-1}\to \mathbb{KP}^1=S^{d}.$$

接下来考察等价关系, 先前说 $(a,b)\sim(c,d)$ 当且仅当存在 $u$ 使得 $(a,b)=(c,d)u$, 这里 $u\overline{u}=1$, 所以在选定一个点时, 该点所在的等价类由 $u$ 参数化, 而该参数空间就是

$$\\\{u\in\mathbb{K}:u\overline{u}=1\\\}=S^{d-1},$$

这就给出了嵌入映射

$$S^{d-1}\hookrightarrow S^{2d-1},$$

与之前的商映射合起来给出

$$S^{d-1}\hookrightarrow S^{2d-1}\to S^{d},$$

用微分几何的语言, 就是说 $S^{2d-1}$ 是 $S^d$ 上的纤维丛, 纤维为 $S^{d-1}$, 这样的纤维丛称为Hopf纤维化.

$$
\displaylines{
\mathbb K = \mathbb R : \qquad S^0 \quad \hookrightarrow \quad S^1 \ \longrightarrow \ S^1 \cr
\mathbb K = \mathbb C : \qquad S^1 \quad \hookrightarrow \quad S^3 \ \longrightarrow \ S^2 \cr
\mathbb K = \mathbb H : \qquad S^3 \quad \hookrightarrow \quad S^7 \ \longrightarrow \ S^4 \cr
\mathbb K = \mathbb O : \qquad S^7 \quad \hookrightarrow \quad S^{15}  \longrightarrow \ S^8
}
$$

Hopf纤维化是微分几何和代数拓扑中的重要例子, 相关的概念有Hopf不变量, Adams定理等.

# Jordan代数

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(Jordan岩浆)</b>

设 $(A,\circ)$ 是一个岩浆, 并且对任意 $a,b\in A$, 满足交换律 $a\circ b=a\circ b$ 和Jordan恒等式

$$(a\circ b)\circ (a\circ a)=a\circ (b\circ (a\circ a)),$$

则称 $A$ 是一个Jordan岩浆.

</div>

Jordan恒等式相当于说 $[a,b,a^2]=0$, 这比交错律更弱. Jordan岩浆显然是泛代数, 但疑似基本没人研究这玩意.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(Jordan代数)</b>

设 $F$ 是域, $F$ 上的Jordan代数是兼具 $F$-模和Jordan岩浆的结构, 其中Jordan乘法 $\circ$ 满足双线性性.

</div>

Jordan代数不是泛代数, 因为泛代数中无法刻画域结构.

先前已经说明过Hermite矩阵 $\mathfrak{h}_n(A)$ 是Jordan代数.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

Jordan代数满足幂结合律.

</div>

该定理的证明必须用到加法结构, 而类似的结论对Jordan岩浆未必成立.

以下皆假设域 $F=\mathbb{R}$.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(理想)</b>

设 $A$ 是一个Jordan代数, $I$ 是 $A$ 的 $F$-线性子空间, 若对任意的 $a\in A$ 和 $b\in I$, 都有 $a\circ b\in I$, 则称 $I$ 是 $A$ 的一个理想, 若 $A$ 无非平凡理想, 则称 $A$ 是单的.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(形式实Jordan代数)</b>

若对Jordan代数 $A$ 中任意 $n$ 个元素 $a_1,\dots,a_n$, 都有

$$a_1^2+\cdots+a_n^2=0\Longrightarrow a_1=0,\dots,a_n=0,$$

则称 $A$ 是一个形式实Jordan代数.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>定理(Jordan, von Neumann, Wigner 1934)</b>

$\mathbb{R}$ 上的有限维形式实单Jordan代数由下表完全分类.
<ul>
<li>$\mathfrak{h}_n(\mathbb{R})$, $n\ge3;$</li>
<li>$\mathfrak{h}_n(\mathbb{C})$, $n\ge3;$</li>
<li>$\mathfrak{h}_n(\mathbb{H})$, $n\ge3;$</li>
<li>$\mathbb{R}^n\oplus \mathbb{R}$, 乘法定义为 $(x,t)\circ(x',t')=(tx'+t'x,x\cdot x'+tt')$, 其中点乘 $\cdot$ 为通常的向量点乘, $n$ 为正整数 $\!;$</li>
<li>$\mathfrak{h}_3(\mathbb{O})$.</li>
</ul>

</div>

前三行中 $n\ge3$ 只是为了不与第四条重复, 容易验证

$$
\displaylines{
H_1(\mathbb {R})  \cong  H_1(\mathbb {C}) \cong H_1(\mathbb {H})\cong H_1(\mathbb {O}) \cong \mathbb {R}, \\
H_2(\mathbb {R})  \cong \mathbb {R}^2 \oplus \mathbb {R}, \quad H_2(\mathbb {C}) \cong \mathbb {R}^3 \oplus \mathbb {R}, \\
H_2(\mathbb {H})  \cong \mathbb {R}^5 \oplus \mathbb {R}, \quad
H_2(\mathbb {O}) \cong \mathbb {R}^9 \oplus \mathbb {R}.
}
$$

前三行称为Hermite型的, 第四行称为旋量因子 $\mathfrak{h}_3(\mathbb{O})$ 称为例外Jordan代数或Albert代数.

Jordan代数与李群和李代数有一定联系.

\bibliography{books}
\addcontentsline{toc}{chapter}{参考文献}
\nocite{*}
