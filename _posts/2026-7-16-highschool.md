---
layout: post
title: "Tarski高中代数问题"
subtitle: ""
header-img: "img/post-bg-infinity.jpg"
header-mask: 0.3
math: true
tags:
  - 泛代数
  - 数理逻辑
---


<div style="border: 3px solid #000; padding: 10px;">

<b>定义(Tarski高中代数,HSI-代数)</b>

设 $A$ 是集合, 其上带三个二元运算, 分别记为 $+$ , $\cdot$ 和 $\uparrow$ , 它们按习惯分别写作 $+(a,b)=a+b$ , $\cdot(a,b)=a\cdot b$ , $\uparrow(a,b)=a^b$ , $A$ 中还存在一个记为 $1$ 的元素, 这些资料满足以下十一条运算律,<br>

1. $a+b=b+a$;<br>
2. $a+(b+c)=(a+b)+c$;<br>
3. $a\cdot1=a$;<br>
4. $a\cdot b=b\cdot a$;<br>
5. $a\cdot(b\cdot c)=(a\cdot b)\cdot c$;<br>
6. $a\cdot(b+c)=a\cdot b+a\cdot c$;<br>
7. $1^a=1$;<br>
8. $a^1=a$;<br>
9. $a^{b+c}=a^b\cdot a^c$;<br>
10. $(a\cdot b)^c=a^c\cdot b^c$;<br>
11. $\left(a^b\right)^c=a^{b\cdot c}$,<br>
    
    则称 $A$ 是一个 $\mathrm{HSI}$ -代数或Tarski高中代数.
</div>

这十一条运算律均为高中代数中熟知的运算律, 因此得名, HSI是High School Identities的首字母缩写. HSI-代数显然是泛代数, 并且每个HSI-代数都可以看作一个一阶理论的模型.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(Tarski高中代数理论)</b>

设非逻辑符号集 $\mathcal{A} = \{ 1, F_+, F_\cdot, F_\uparrow \}$ , 其中 $1$ 为常元符号, $F_+, F_\cdot, F_\uparrow$ 为二元函数符号, 一阶语言 $\mathcal{L_A}$ 由 $\mathcal{A}$ 生成, 非逻辑公理为<br>

1. $\forall a \forall b \, (F_+(a, b) = F_+(b, a))$;<br>
2. $\forall a \forall b \forall c \, (F_+(a, F_+(b, c)) = F_+(F_+(a, b), c))$;<br>
3. $\forall a \, (F_\cdot(a, 1) = a)$;<br>
4. $\forall a \forall b \, (F_\cdot(a, b) = F_\cdot(b, a))$;<br>
5. $\forall a \forall b \forall c \, (F_\cdot(a, F_\cdot(b, c)) = F_\cdot(F_\cdot(a, b), c))$;<br>
6. $\forall a \forall b \forall c \, (F_\cdot(a, F_+(b, c)) = F_+(F_\cdot(a, b), F_\cdot(a, c)))$;<br>
7. $\forall a \, (F_\uparrow(1, a) = 1)$;<br>
8. $\forall a \, (F_\uparrow(a, 1) = a)$;<br>
9. $\forall a \forall b \forall c \, (F_\uparrow(a, F_+(b, c)) = F_\cdot(F_\uparrow(a, b), F_\uparrow(a, c)))$;<br>
10. $\forall a \forall b \forall c \, (F_\uparrow(F_\cdot(a, b), c) = F_\cdot(F_\uparrow(a, c), F_\uparrow(b, c)))$;<br>
11. $\forall a \forall b \forall c \, (F_\uparrow(F_\uparrow(a, b), c) = F_\uparrow(a, F_\cdot(b, c)))$.<br>
    
    以上定义的一阶理论称为Tarski高中代数理论, 记为 $\mathrm{HSI}$ .
</div>

显然正整数连同其上通常运算构成HSI-代数, 于是是HSI的一个模型.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

$(\mathbb{Z}_{\ge1},+,\times,\uparrow)\models \mathrm{HSI}$ .
</div>

还有其他例子, 例如下表描述了一个二元的HSI-代数 $(\{1,2\},+,\times,\uparrow)$ .

$$
\begin{array}{c|cc} 
+ & 1 & 2 \\ 
\hline 
1 & 2 & 1 \\ 
2 & 1 & 2 
\end{array} 
\qquad \qquad 
\begin{array}{c|cc} 
\times & 1 & 2 \\ 
\hline 
1 & 1 & 2 \\ 
2 & 2 & 2 \end{array} 
\qquad \qquad 
\begin{array}{c|cc} 
\uparrow & 1 & 2 \\ 
\hline 
1 & 1 & 1 \\
2 & 2 & 2 
\end{array}
$$

Tarski问, HSI是否可以推出正整数中所有为真的公式, 该问题称为Tarski高中代数问题, 回答是否定的, Wilkie给出了一个反例.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

Wilkie恒等式
$$\begin{aligned} &((1+x)^y + (1+x+x^2)^y)^x \cdot ((1+x^3)^x + (1+x^2+x^4)^x)^y \\  =\ & ((1+x)^x + (1+x+x^2)^x)^y \cdot ((1+x^3)^y + (1+x^2+x^4)^y)^x \end{aligned}$$
在正整数成立, 但存在 $\mathrm{HSI}$ 的模型 $M$ , 在 $M$ 中该恒等式不成立, 即 $\mathrm{HSI}$ 不能推出该恒等式. 注意该公式中的 $2,3,4$ 分别解释为 $1+1,1+1+1,1+1+1+1$ , 此处由结合律省略括号.
</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

首先在正整数中证明该恒等式. 容易验证
$$1+x^3=(1+x)(1-x+x^2),\qquad (1+x^2+x^4)=(1+x+x^2)(1-x+x^2),$$
代入即得
$$
\begin{aligned}
&((1+x)^y + (1+x+x^2)^y)^x\cdot ((1+x)^x + (1+x+x^2)^x)^y\cdot(1-x+x^2)^{xy}  \\  =\ & ((1+x)^x + (1+x+x^2)^x)^y \cdot ((1+x)^y + (1+x+x^2)^y)^x \cdot(1-x+x^2)^{xy}
\end{aligned}
$$
显然成立.

可以验证下表构造了HSI的一个模型,
$$
\scriptsize
\begin{array}{c|cccccccccccc} + & 1 & 2 & 3 & 4 & a & b & c & d & e & f & g & h \\ \hline 1 & 2 & 3 & 4 & 4 & 2 & 3 & d & 3 & 3 & 3 & 3 & 4 \\ 2 & 3 & 4 & 4 & 4 & 3 & 4 & 3 & 4 & 4 & 4 & 4 & 4 \\ 3 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 \\ 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 \\ a & 2 & 3 & 4 & 4 & b & 4 & b & 3 & h & 3 & 3 & 4 \\ b & 3 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 \\ c & d & 3 & 4 & 4 & b & 4 & b & 3 & 3 & 3 & 3 & 4 \\ d & 3 & 4 & 4 & 4 & 3 & 4 & 3 & 4 & 4 & 4 & 4 & 4 \\ e & 3 & 4 & 4 & 4 & h & 4 & 3 & 4 & 4 & 3 & h & 4 \\ f & 3 & 4 & 4 & 4 & 3 & 4 & 3 & 4 & 3 & 4 & 3 & 4 \\ g & 3 & 4 & 4 & 4 & 3 & 4 & 3 & 4 & h & 3 & 4 & 4 \\ h & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 
\end{array}
$$
$$
\scriptsize
\begin{array}{c|cccccccccccc} \times & 1 & 2 & 3 & 4 & a & b & c & d & e & f & g & h \\ \hline 1 & 1 & 2 & 3 & 4 & a & b & c & d & e & f & g & h \\ 2 & 2 & 4 & 4 & 4 & b & 4 & b & 4 & 4 & 4 & 4 & 4 \\ 3 & 3 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 \\ 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 \\ a & a & b & 4 & 4 & c & b & c & b & h & 4 & 4 & 4 \\ b & b & 4 & 4 & 4 & b & 4 & b & 4 & 4 & 4 & 4 & 4 \\ c & c & b & 4 & 4 & c & b & c & b & 4 & 4 & 4 & 4 \\ d & d & 4 & 4 & 4 & b & 4 & b & 4 & 4 & 4 & 4 & 4 \\ e & e & 4 & 4 & 4 & h & 4 & 4 & 4 & 4 & 4 & h & 4 \\ f & f & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 \\ g & g & 4 & 4 & 4 & 4 & 4 & 4 & 4 & h & 4 & 4 & 4 \\ h & h & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 
\end{array}
$$
$$
\scriptsize
\begin{array}{c|cccccccccccc} \uparrow & 1 & 2 & 3 & 4 & a & b & c & d & e & f & g & h \\ \hline 1 & 1 & 1 & 1 & 1 & 1 & 1 & 1 & 1 & 1 & 1 & 1 & 1 \\ 2 & 2 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & f & 4 & 4 & 4 \\ 3 & 3 & 4 & 4 & 4 & e & 4 & 4 & 4 & g & 4 & e & h \\ 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 \\ a & a & c & c & c & c & c & c & c & c & c & c & c \\ b & b & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 \\ c & c & c & c & c & c & c & c & c & c & c & c & c \\ d & d & 4 & 4 & 4 & f & 4 & 4 & 4 & 4 & 4 & 4 & 4 \\ e & e & 4 & 4 & 4 & 4 & 4 & 4 & 4 & h & 4 & 4 & 4 \\ f & f & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 \\ g & g & 4 & 4 & 4 & h & 4 & 4 & 4 & 4 & 4 & h & 4 \\ h & h & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 & 4 
\end{array}
$$
我们验证当 $(x,y)=(a,e)$ 时该式不成立, 左边<br>

$$
((1+a)^e + (1+a+a^2)^e)^a \cdot ((1+a^3)^a + (1+a^2+a^4)^a)^e
$$
$$
=(2^e+3^e)^a\cdot(d^a+3^a)^e=3^a\cdot 3^e=h,
$$<br>

右边<br>

$$
((1+a)^a + (1+a+a^2)^a)^e \cdot ((1+a^3)^e + (1+a^2+a^4)^e)^a
$$
$$
=(2^a+3^a)^e\cdot(d^e+3^e)^a=4^e\cdot 4^a=4,
$$<br>

$h\neq4$ .
</div>

**猜想.** 上述HSI代数是使得Wilkie恒等式不成立的元数最小的HSI代数.

另一方面, 这也说明HSI是不完备的, 我们说Wilkie恒等式是独立于HSI的, 这并不出乎意料, 因为恒等式 $x=y$ 在只含一个元素的平凡HSI代数中成立, 而在其他任何非平凡HSI代数中都不成立, 并且我们知道非平凡的HSI代数是存在的, 所以 $x=y$ 也独立于HSI.

另一个方向是考虑在HSI中添加多少个公理, 才能使其完全刻画正整数上的加法, 乘法和指数运算, 该问题的答案是添加任意有限多条公理都不能, 具体的构造详见[4].

如果我们不考虑指数运算, 生活将会容易的多, HSI中的前六条公理足以完全刻画正整数中的加法和乘法运算.

给定任意两个只包含加法和乘法的项 $t_1(x_1,\dots,x_n)$ 和 $t_2(x_1,\dots,x_n)$ , 其中 $x_i$ 为形式变元, 假设 $t_1(x_1,\dots,x_n)=t_2(x_1,\dots,x_n)$ 对任意正整数 $x_1,\dots,x_n$ 都成立. 由多项式理论知, 反复使用上述公理, 可以将它们分别展开为唯一的标准形式, 即
$$\sum_{i=1}^n a_{i_1\cdots i_n} x_1^{k_{i_1}}\cdots x_n^{k_{i_n}}$$
的形式, 其中每个系数 $a_i$ 都是由若干个 $1$ 相加得到的元素, 设 $t_1(x_1,\dots,x_n)$ 和 $t_2(x_1,\dots,x_n)$ 的标准多项式为 $P(x_1,\dots,x_n)$ 和 $Q(x_1,\dots,x_n)$ , 由归纳法可证, 若将 $x_1,\dots,x_n$ 代入任意正整数, $P=Q$ 成立, 则必然有 $P(x_1,\dots,x_n)=Q(x_1,\dots,x_n)$ 作为形式多项式成立, 因此有项 $t_1(x_1,\dots,x_n)=t_2(x_1,\dots,x_n)$ . 这说明正整数中成立的任何只关于加法和乘法的恒等式都可只使用前六条公理证明.

[1] Stanley Burris and Simon Lee, Tarski’s high school identities, The American Mathematical Monthly 100 (1993), no. 3, 231–236.

[2] Stanley Burris and Karen Yeats, The saga of the high school identities, Algebra Universalis 52 (2005), 325–342.

[3] R. Gurevič, Equational theory of positive numbers with exponentiation, Proceedings of the American Mathematical Society 94 (1985), no. 1, 135–141.

[4] R. Gurevič, Equational theory of positive numbers with exponentiation is not finitely axiomatizable, Annals of Pure and Applied Logic 49 (1990), no. 1, 1–30.
