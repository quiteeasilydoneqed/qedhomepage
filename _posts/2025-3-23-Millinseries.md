---
layout: post
title: "米林级数"
subtitle: "Millin’s series"
header-img: "img/post-bg-infinity.jpg"
header-mask: 0.3
math: true
tags:
  - 初等数学
---

以下用 $ F_n $ 表示第 $ n $ 个斐波那契数, $ F_0=0 $, $ F_1=1 $, $ F_n=F_{n-1}+F_{n-2} $, $ n>1 $.

米林级数是指:

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Millin, Good)</b>
$$
\sum_{n=0}^\infty\frac{1}{F_{2^n}}=\frac{7-\sqrt{5}}{2}.
$$
</div><br>

<div style="border: 3px solid #000; padding: 10px;">
<b>引理1</b>
$$
F_{n+1}F_{n-1}-F_{n}^2=(-1)^n.
$$

</div>

从而有

$$
F_{2^k+1}F_{2^k-1}-1=F_{2^k}^2.
$$

<div style="border: 3px solid #000; padding: 10px;">
<b>引理2</b>
$$
F_{m+n}=F_{m-1} F_n+F_m F_{n+1}.
$$
</div>

从而有

$$
F_{2^{k+1}}=F_{2^k-1}F_{2^k}+F_{2^k} F_{2^k+1}.
$$

<div style="border: 3px solid #000; padding: 10px;">
<b>引理3</b>
$$
F_{m+n-1}=F_{m} F_n+F_{m-1}F_{n-1}.
$$

</div>

从而有

$$
F_{2^{k+1}-1}=F_{2^k}^2+F_{2^k-1}^2.
$$

<div style="border: 3px solid #000; padding: 10px;">
<b>引理4</b>

$$
\lim_{n\to\infty}\frac{F_{n-1}}{F_{n}}=\frac{\sqrt{5}-1}{2}.
$$
</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>米林级数的证明</b>
先证

$$
\sum_{n=0}^k\frac{1}{F_{2^n}}=3-\frac{F_{2^k-1}}{F_{2^k}},
$$

$k=1$ 时显然成立, 而

\begin{align*}
3-\frac{F_{2^k-1}}{F_{2^k}}+\frac{1}{F_{2^{k+1}}}=&3-\left(\frac{F_{2^k-1}}{F_{2^k}}-\frac{1}{F_{2^{k+1}}}\right)=3-\frac{\frac{F_{2^{k}-1}F_{2^{k+1}}}{F_{2^{k}}}-1}{F_{2^{k+1}}}\\
=&3-\frac{F_{2^{k}-1}(F_{2^{k}-1}+F_{2^{k}+1})-1}{F_{2^{k+1}}}\\
=&3-\frac{F_{2^{k}-1}^2+F_{2^{k}-1}F_{2^{k}+1}-1}{F_{2^{k+1}}}\\
=&3-\frac{F_{2^{k}-1}^2+F_{2^{k}}^2}{F_{2^{k+1}}}\\        
=&3-\frac{F_{2^{k+1}-1}}{F_{2^{k+1}}}
\end{align*}

由归纳法知

$$
\sum_{n=0}^k\frac{1}{F_{2^n}}=3-\frac{F_{2^k-1}}{F_{2^k}},
$$

令 $k\to\infty$, 即得

$$
\sum_{n=0}^\infty\frac{1}{F_{2^n}}=3-\frac{\sqrt{5}-1}{2}=\frac{7-\sqrt{5}}{2}.
$$
</div>



<b>趣闻: </b>

该公式首先由宾夕法尼亚州的一个中学生 Millin 在 1974 年发现并证明, 但 Millin 并没有发表他的证明, 而是将该问题投稿给专门刊登斐波那契数列相关研究的期刊 The Fibonacci Quarterly 上, 向数学家征集证明. 几乎同一时间, I. J. Good 也发现了这一结果, 并发表在同一期刊上, 本视频展示的就是 Good 的证明方法, 也是最简单的一种.

1976 年, 同一期刊刊登了数学家 A. G. Shannon (不是信息论的那个香农) 使用另一种方法的证明, 具体可见 [https://www.fq.math.ca/Scanned/14-2/advanced14-2.pdf](https://www.fq.math.ca/Scanned/14-2/advanced14-2.pdf).

但 1976 年的文章中表明, 该问题的提出者名叫 Miller 而非 Millin, 有人于 2022 年在数学论坛 Stack Exchange 上提出了这一问题, Miller 本人在该问题下回答道: "在 LaTeX 出现之前，我使用手写和打字机来撰写提交给 FQ (Fibonacci Quarterly) 的文章。显然，我的手写签名不是很清楚，当时被误读了。" Miller 还说, 他喜欢 Millin Series 这个名字, 他希望不要有人试图修正它.

Miller 在自己的个人网站上公开了自己的原始证明, 具体可见 [https://www.lix.polytechnique.fr/Labo/Dale.Miller/papers/Millin-series-proof.pdf](https://www.lix.polytechnique.fr/Labo/Dale.Miller/papers/Millin-series-proof.pdf).

关于该故事的来源, 可见 [https://hsm.stackexchange.com/questions/14434/who-was-d-a-millin-the-eponym-of-the-millin-series](https://hsm.stackexchange.com/questions/14434/who-was-d-a-millin-the-eponym-of-the-millin-series).
