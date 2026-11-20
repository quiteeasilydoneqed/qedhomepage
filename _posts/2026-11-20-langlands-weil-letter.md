---
layout: post
title: "Langlands 1967 年致 André Weil 的信"
subtitle: "中文翻译"
header-img: "img/post-bg-infinity.jpg"
header-mask: 0.3
math: true
no-em-replace: true
gallery: langlands-weil
tags:
  - 翻译
  - 数论
  - 自守表示
  - Langlands 纲领
---

> <p style="font-size: 24px; font-weight: bold;">译注</p>
>
> **1.** 本译本依据 <https://sunsite.ubc.ca/DigitalMathArchive/Langlands/functoriality.html>.
>
> **2.** 哥特体 $\mathfrak{G}$ 被排成了小写 $\mathfrak{g}$.
>
> 转录版第 6 页, 手写原稿第 9 页末尾: 转录作 $\mathfrak{g}' \times\_{\delta'} {}^cG'\_{\mathbb{C}}$, 应为 $\mathfrak{G}' \times\_{\delta'} {}^cG'\_{\mathbb{C}}$.
>
> 转录版第 6 页, 手写原稿第 10 页开头: 转录作 $\mathfrak{g} \times\_\delta {}^cG\_{\mathbb{C}}$, 应为 $\mathfrak{G} \times\_\delta {}^cG\_{\mathbb{C}}$.
>
> 转录版第 7 页, 手写原稿第 12 页: 转录作 $\mu\_i \in \mathfrak{g}\_1$, 应为 $\mu\_i \in \mathfrak{G}\_1$.
>
> **3.** $z\_1$ 的下标应为 $i$.
>
> 转录版第 8 页, 手写原稿第 14 页第一个格: 转录作 $\sum\_{i=1}^{m} z\_1 = 0$, 应为 $\sum\_{i=1}^{m} z\_i = 0$.
>
> 转录版第 8 页, 手写原稿第 14 页第二个格: 转录作 $z\_1 + \dfrac{z}{m} \in \mathbb{Z}$, 应为 $z\_i + \dfrac{z}{m} \in \mathbb{Z}$.
>
> 转录版第 8 页, 手写原稿第 14 页第三个格: 转录作 $z, z\_1 \in \mathbb{Z}$, 应为 $z, z\_i \in \mathbb{Z}$.
>
> **4.** 转录版第 5 页, 手写原稿第 8 页末尾: 转录作 $L(s, \phi, \pi)/L(s, \phi, \tilde\pi)$, 应为 $L(s, \phi, \pi)/L(s, \psi, \tilde\pi)$.
>
> **5.** 转录版第 9 页, 手写原稿第 15 页: 转录作 $\overline{F}\_{S'}$, 应为 $\overline{G}\_{S'}$.
>
> **6.** Weil 没有书面回信.

## 附函

Professor Weil:

为回应您邀我前去做的交谈, 我写了随信附上的这封信. 写完后我才意识到, 信中几乎没有一句话是我能确定的. 如果您愿意把它当作纯粹的猜想来看, 我会很感激; 如果不愿意, 我想您手边一定有废纸篓.

<div class="letter-signature">Yours truly,<br>R. Langlands<br><span class="letter-signature-date">Jan. 16, '67</span></div>

Dear André:

Langlands 把信交给我, 让我看一看再转给您. 我眼下正忙, 只草草扫了一遍就转给您了. 希望过些日子您能让我拿回来.

<div class="letter-signature">Yours Sincerely<br>Harish</div>

## 正文

Dear Professor Weil,

在设法把陈省身做报告之前我问过您的那个问题说清楚时, 我引出了两个更一般的问题. 我很想听听您对这两个问题的意见. 我还没有机会认真想过它们; 若不是想接着此前一次随意的谈话往下谈, 我也不会提出来. 请您按这两个问题目前所处的阶段, 以应有的宽容对待它们. 提完问题, 我会简短说明它们的来历.

这里要花些篇幅, 因为我想定义某一类 Euler 乘积, 称它们为 Artin-Hecke $L$ 级数. 理由是 Artin $L$ 级数、带 Grössencharaktere 的 $L$ 级数, 以及 Hecke 引入自守形式理论的那类级数, 都是这类级数的特例. 第一个问题自然是: 这些级数是否给出带函数方程的亚纯函数. 关于函数方程, 我稍后再说几句. 第二个问题我稍后再陈述. 它是对如下问题的一个推广: Abel $L$ 级数是否就是带 Grössencharaktere 的 $L$ 级数. 由于我想对任意约化群上的自守形式陈述这个问题, 就必须假定约化理论里某些结果可以再推进一步, 超出目前已有的程度.

遗憾的是, 我不得不写得相当拘谨. 设 $k$ 为有理数域或它的一个完备化. 设 $\tilde{G}$ 是若干单群的乘积, 这些单群可以交换, 并且在 $k$ 上分裂. 假定非交换的因子都是单连通的. 乘积为空、即 $\tilde{G} = \{1\}$ 的情形并非没有意思. 取一个分裂 Cartan 子群 $\tilde{T}$, 设 $\tilde{L}$ 为 $\tilde{T}$ 的权格. $\tilde{L}$ 包含根. 我想定义“$\tilde{G}$ 的”共轭群, 以及“$\tilde{L}$ 的”共轭格. 只需对单群做这件事即可, 之后可以取直积和直和来拼合. 若 $\tilde{G}$ 交换且单, 就取 $\tilde{L}$ 的任一子格 $\tilde{L}'$, 令共轭格 ${}^cL$ 为 $\tilde{L}'$ 的对偶(即 $\mathrm{Hom}(\tilde{L}',\mathbb{Z})$). ${}^cL$ 包含 $\tilde{L}'$ 的对偶 ${}^cL'$. 取一维分裂环面 ${}^c\tilde{G}$, 使其权格等同于 ${}^cL$. 若 $\tilde{G}$ 单且非交换, 则取 $\tilde{L}'$ 为根生成的格, 取 ${}^cL$ 为 $\tilde{L}'$ 的对偶. 此时 ${}^cL$ 包含 $\tilde{L}$ 的对偶 ${}^cL'$. 对每个根 $\alpha$, 按通常方式在对应于 $\tilde{T}$ 的 Cartan 子代数中取元素 $H\_\alpha$, 使 $\alpha(H\_\alpha) = 2$. 线性函数 $^c\alpha(\lambda) = \lambda(H\_\alpha)$ 生成 $\tilde{L}'$. 存在唯一的单连通群 ${}^c\tilde{G}$, 它的权格与 ${}^cL$ 同构, 并且它的根正好对应这些元素 $^c\alpha$. 取定 $\tilde{G}$ 的单根 $\alpha\_1,\dots,\alpha\_e$, 则 $^c\alpha\_1,\dots,^c\alpha\_e$ 可以取作 ${}^c\tilde{G}$ 的单根. 现在回到一般情形.

若 $L$ 是介于 $\tilde{L}'$ 与 $\tilde{L}$ 之间的格, 就可以自然地把一个被 $\tilde{G}$ 覆盖的群 $G$ 联系到 $L$. $L$ 的对偶格 ${}^cL$ 介于 ${}^c\tilde{L}'$ 与 ${}^c\tilde{L}$ 之间, 它确定一个被 ${}^c\tilde{G}$ 覆盖的群 ${}^cG$, 我称 ${}^cG$ 为 $G$ 的共轭群. 设 $\mathfrak{h}$ 为 $\tilde{T}$ 的 Lie 代数, 对每个根 $\alpha$ 取根向量 $X\_\alpha$, 使 Chevalley 条件成立. 再设 $^c\mathfrak{h}$ 是 $^c\mathfrak{g}$ 的分裂 Cartan 子代数, 对每个根 $^c\alpha$ 取根向量 $^cX\_\alpha$, 使 Chevalley 条件成立. 设 $\Omega$ 是 $\mathfrak{g}$ 的自同构群, 这些自同构把 $\mathfrak{h}$ 映到自身, 置换单根所对应的 $X\_\alpha$, 并且把 $\tilde{L}$, $L$, $\tilde{L}'$ 都映到自身. 照同样方式定义 ${}^c\Omega$. ${}^c\Omega$ 是 $\Omega$ 的逆步对象, 所以 $\Omega$ 与 ${}^c\Omega$ 典范同构. 于是 $\Omega$ 作用为 $G$ 与 ${}^cG$ 的自同构群. 设 $K$ 是 $k$ 的有限 Galois 扩张, $\delta$ 是从 $\mathfrak{G} = \mathfrak{G}(K/k)$ 到 $\Omega$ 的同态, 像为 $\Omega^\delta$. 令 $G^\delta$ 与 ${}^cG^\delta$ 分别为 $G$ 与 ${}^cG$ 的相应形式.

要定义 $L$ 级数的局部因子, 我得先回顾 Hecke 代数的一些事实: 这里 $K$ 是 $p$ 进域 $k$ 的非分歧扩张, $G\_k^\delta$ 是相应的群. 若按适当方式取 $G\_k^\delta$ 的极大紧子群, 则按 Bruhat 与 Satake 的结果, Hecke 代数同构于 ${}^cL^\delta$ 的群代数中的一个子集, 这个子集由在 ${}^c\Omega^\delta$ 下不变、并且在 ${}^cG^\delta$ 的限制 Weyl 群 ${}^cW^\delta$ 下不变的 ${}^cL$ 中元素组成. (实际上, 我们得把他们的结果稍作引申.) 这样一来, Hecke 代数到复数的任一特征标 $\chi$ 都可以延拓成 ${}^cL$ 的群代数到复数的同态 $\chi'$. ${}^cT$ 中至少有一个元素 $g$, 使得若 $f = \sum\_{\lambda\in{}^cL} a\_\lambda \xi\_\lambda$ ($\xi\_\lambda$ 是把 $\lambda$ 写成乘法形式), 则 $\chi'(f) = \sum a\_\lambda \xi\_\lambda(g)$. 半直积 $\mathfrak{G} \times\_\delta {}^cG$ 是一个复群. 设 $\pi$ 是它的一个复表示. 若 $\sigma$ 是 Frobenius 元, 则 

$$
\frac{1}{\det\left(1 - x\pi(\sigma \times g)\right)} \qquad \text{（x 为不定元）}
$$

就是对应于 $\chi$ 与 $\pi$ 的局部 zeta 函数, 其中 $x$ 为不定元. 我还得验证它只依赖 $\chi$, 不依赖 $g$. 设 $\lambda$ 为任一权, 令 $n\_\lambda$ 为使 $\sigma$ 固定 $\lambda$ 的最小幂次; $n\_\lambda \mid n$ 时, 若 $\pi$ 作用在 $V$ 上, 令 $t\_\lambda(n)$ 为 $\sigma^n$ 在特征空间 

$$
\left\{ v \in V \;\middle\vert \; \pi(h)v = \xi\_\lambda(h)v, \ \forall h \in {}^cT \right\}
$$

 上的迹. 于是 

$$
\begin{align*}
\log \frac{1}{\det\left(1 - x\pi(\sigma \times g)\right)}
&= \sum\_{n=0}^{\infty} \frac{x^n}{n} \sum\_{\lambda \in L} \sum\_{n\_\lambda \mid n} t\_\lambda(n)\, \xi\_\lambda\left(g^{\sigma^{n-1}} g^{\sigma^{n-2}} \cdots g\right) \\
&= \sum\_{n=0}^{\infty} \frac{x^n}{n} \sum\_{\lambda \in L} \sum\_{n\_\lambda \mid n} t\_\lambda(n)\, \xi\_{\frac{n}{n\_\lambda}\left(\textstyle\sum\_{k=0}^{n\_\lambda - 1} \lambda^{\sigma^k}\right)}(g).
\end{align*}
$$

 再者, 若 $\omega$ 是 ${}^cW^\delta$ 的元素, 总可以挑一个与 $\sigma$ 交换的代表元 $w$. 于是把 $g$ 换成 $w^{-1}gw$ 时局部 zeta 函数不变, 所以它等于 

$$
\frac{1}{[{}^cW^\delta : 1]} \sum\_{n=0}^{\infty} \frac{x^n}{n} \sum\_{\lambda} \sum\_{n\_\lambda \mid n} t\_\lambda(n) \sum\_{\omega \in {}^cW^\delta} \xi\_{\frac{n}{n\_\lambda}\left(\textstyle\sum\_{k=0}^{n\_\lambda - 1} \lambda^{\sigma^k}\right)} \omega(g).
$$

由于

$$
\sum\_{\omega} \xi\_{\frac{n}{n\_\lambda}\left(\sum\_{k=0}^{n\_\lambda - 1} \lambda^{\sigma^k}\right)}\omega
$$

属于 Hecke 代数的像, 断言得证.

我不知道这样做是否站得住脚, 但且假定复表示的特征标能把 $\mathfrak{G} \times\_\delta {}^cG$ 里的半单共轭类分开. 那么由上述结果, Hecke 代数到复数的每个同态 $\chi$ 都联系到半单元素 $\sigma \times g$ 所在的共轭类. 反过来, 给定 $\mathfrak{G} \times\_\delta {}^cG$ 中的一个半单共轭类, 由 Borel-Mostow 定理, 它含有 ${}^cT$ 正规化子中的一个元素; 它甚至含有把正根映成正根的元素. 于是, 如果这个共轭类在 $\mathfrak{G}$(交换群)上的投影是 $\sigma$, 那么它含有形如 $\sigma \times g$ 的元素, $g \in {}^cT$. 如上, $g$ 确定 Hecke 代数到复数的同态. 若这个同态 $\chi$ 由附于它的局部 zeta 因子完全确定, 那么它也就由 $\sigma \times g$ 的共轭类完全确定; 于是 Hecke 代数到复数的同态与 $\mathfrak{G} \times\_\delta {}^cG$ 中投影为 $\sigma$ 的半单共轭类一一对应. 只需检验: $\chi$ 在形如 

$$
\sum\_{w \in {}^cW^\delta} \xi_{\left(\sum\_{n=1}^{n\_\lambda} \lambda^{\sigma^k}\right)}\omega
$$

 的元素上的值由局部 zeta 函数确定, 其中 $\sum\_{n=1}^{n\_\lambda} \lambda^{\sigma^k}$ 落在正 Weyl 腔中. 这用通常的归纳法就能做到, 因为 $\sum \lambda^{\sigma^k}$ 在 $\mathfrak{G}$ 下不变, 从而是 $\mathfrak{G} \times\_\delta {}^cG$ 某个表示的最高权, 该表示限制到 ${}^cG$ 时不可约.

> 注：这大概是对的, 证明所需的材料大概在文献里都能找到. 不过, 写这封信时, 我觉得它远没有我当初想的那么显然.

下面我设法定义 Artin-Hecke $L$ 级数. 为此, 对每个 $p$ 取定 $\overline{\mathbb{Q}}$(即 $\mathbb{Q}$ 的代数闭包)到 $\overline{\mathbb{Q}}\_p$ 的一个嵌入. 我们之后还要回过头来检验, 这些级数与所做的选择无关. 下一段的叙述会隐含这种选择.

设有 $G$ 在有理数域上的一个扭形式 $\overline{G}$. 扭的过程分两步. 第一步, 对 $\mathbb{Q}$ 的适当 Galois 扩张 $K$, 取 $\mathfrak{G} = \mathfrak{G}(K/\mathbb{Q})$ 到 $\Omega$ 的同态 $\delta$, 得到 $G^\delta$. 第二步, 用上闭链 $\{a\_\tau \mid \tau \in \mathfrak{G}\}$ 对 $G^\delta$ 作内扭. 我且假定以下两条成立:

**(i)** 设 $G$ 是作用在 $V$ 上的线性群, $L$ 是 $V\_{\mathbb{Q}}$ 中的 Chevalley 格. 则对几乎所有的 $p$, $G^\delta\_{\mathbb{Z}\_p}$(即 $G^\delta\_{\mathbb{Q}\_p}$ 与 $L \otimes\_{\mathbb{Z}} \overline{\mathbb{Z}}\_p$ 的稳定化子之交, 其中 $\overline{\mathbb{Z}}\_p$ 是 $\overline{\mathbb{Q}}\_p$ 中的整数环)是前面提到的那种极大紧子群之一.

**(ii)** 对几乎所有的 $p$, $\{a\_\tau\}$ 在 $\mathfrak{G}(K\mathbb{Q}\_p/\mathbb{Q}\_p) = \mathfrak{G}(K\_p/\mathbb{Q}\_p) = \mathfrak{G}\_p$ 上的限制是可裂的. 此外, 对这种 $p$, $G\_{K\_p}$ 与 $L \otimes\_{\mathbb{Z}} \overline{\mathbb{Z}}\_p$ 的稳定化子之交里有元素 $b$, 使 $a\_\sigma = b^\sigma b^{-1}$, $\sigma \in \mathfrak{G}\_p$.

现在取满足 (i) 与 (ii)、且在 $K$ 中非分歧的 $p$. 因为 

$$
\overline{G}\_{\mathbb{Q}\_p} = \left\{ g \in G^\delta\_{K\_p} \;\middle\vert \; g^{\sigma a\_\sigma} = g \ (\sigma \in \mathfrak{G}\_p) \right\},
$$

 映射 $g \mapsto g^b$ 是 $\overline{G}\_{\mathbb{Q}\_p}$ 与 $G^\delta\_{\mathbb{Q}\_p}$ 之间的同构. 而且可以把 $\overline{G}\_{\mathbb{Z}\_p}$ 取成 $\overline{G}\_{\mathbb{Q}\_p}$ 与 $L \otimes\_{\mathbb{Z}} \overline{\mathbb{Z}}\_p$ 稳定化子之交, 于是这个映射把 $\overline{G}\_{\mathbb{Z}\_p}$ 送到 $G\_{\mathbb{Z}\_p}$. 由此诱导的 Hecke 代数同构与 $b$ 的选取无关. 现在 $\overline{G}\_{\mathbb{A}} = \prod \overline{G}\_{\mathbb{Q}\_p}$. 设有 $\overline{G}\_{\mathbb{Q}} \backslash \overline{G}\_{\mathbb{A}}$ 上的自守形式 $\phi$, 它是几乎所有 $p$ 的 Hecke 代数的特征函数. 那么对几乎所有的 $p$, 我们得到 Hecke 代数到复数的同态, 从而得到 $\mathfrak{G}\_p \times\_\delta {}^cG \subseteq \mathfrak{G} \times\_\delta {}^cG$ 中的一个半单共轭类 $\alpha\_p$. 若 $\pi$ 是 $\mathfrak{G} \times\_\delta {}^cG\_{\mathbb{Q}}$ 的复表示, 我把 Artin-Hecke $L$ 级数定义为下面的乘积 (取遍几乎所有的 $p$): 

$$
L(s,\pi,\phi) = \prod\_{p} \frac{1}{\det\left(1 - \dfrac{\pi(\alpha\_p)}{p^s}\right)}\qquad \text{(乘积取遍几乎所有}$p$\text{)}.
$$

我得检验这些级数不依赖 $\overline{\mathbb{Q}}$ 到 $\overline{\mathbb{Q}}\_p$ 的嵌入. 眼下先固定 $p$. 我们已经用原来的嵌入把 $\overline{\mathbb{Q}}$ 与 $\overline{\mathbb{Q}}\_p$ 的一个子域等同起来. 保持这个等同关系. 别的嵌入都是把 $x$ 送到 $x^\tau$, $\tau \in \mathfrak{G}(\overline{\mathbb{Q}}/\mathbb{Q})$. 若用原来的嵌入把 $\mathfrak{G}\_p$ 与 $\mathfrak{G}$ 的一个子群等同, 那么新嵌入给出 $\mathfrak{G}\_p$ 到 $\mathfrak{G}$ 的映射 $\sigma \mapsto \tau\sigma\tau^{-1}$ (这里把 $\tau$ 与其在 $\mathfrak{G}$ 中的像等同). $\delta$ 在 $\mathfrak{G}\_p$ 上的限制换成 $\delta'$, 其中 $\delta'(\sigma) = \delta(\tau\sigma\tau^{-1})$. 于是 $G^\delta\_{\mathbb{Q}\_p}$ 换成 $G^{\delta'}\_{\mathbb{Q}\_p}$. 映射 $g \mapsto g^{\delta(\tau)}$ 是 $G^{\delta'}\_{\mathbb{Q}\_p}$ 与 $G^\delta\_{\mathbb{Q}\_p}$ 之间的同构. 若 $g \in G^\delta\_{\mathbb{Q}} \subset G^\delta\_{\mathbb{Q}\_p}$, 则 $g$ 是 $g^\tau$ 的像, 所以这个映射与 $G^\delta\_{\mathbb{Q}}$ 在两个群中的嵌入相容. 新的上闭链 $\{a'\_\sigma\}$ 是 $a\_{\tau\sigma\tau^{-1}} = a\_\tau^{\tau^{-1}} a\_\sigma^{\tau^{-1}} a\_{\tau^{-1}} = a\_\sigma^{\tau^{-1}} a\_\tau^{-\tau^{-1}} a\_{\tau^{-1}}$ 的像, 其中用到所有 $\sigma$, $\tau$ 都有 $a\_{\sigma\tau} = a\_\sigma^\tau a\_\tau$. 像就是 $\delta(\tau) a\_\sigma^\tau a\_\sigma \tau\tau^{-1} \delta(\tau^{-1})$. 于是 

$$
\overline{G}\_{\mathbb{Q}\_p} = \left\{ g \in G\_{K\_p} \;\middle\vert \; g = g^{\delta(\tau)\sigma\delta(\sigma)a\_\sigma^\tau a\_\sigma a\_\tau^{-1}\delta(\tau^{-1})}  = g^{\delta(\tau)a\_\tau \sigma\delta(\sigma)a\_\sigma a\_\tau^{-1}\sigma(\tau^{-1})} ,\text{对于} \sigma \in \mathfrak{G}\_p \right\}.
$$

 而映射 $g \mapsto g^{\delta(\tau)a\_\tau}$ 是 $\overline{G}\_{\mathbb{Q}\_p}$ 到 $\overline{G}\_{\mathbb{Q}\_p}$ 的同构. 它与 $\overline{G}\_{\mathbb{Q}}$ 在两个群中的嵌入相容, 因为 $\overline{G}\_{\mathbb{Q}} = \{ g \in G\_K \mid g^{\rho\delta(\rho)a\_\rho} = g, \ \forall \rho \in \mathfrak{G} \}$. 此外, 对几乎所有的 $\rho$, 它把 $\overline{G}\_{\mathbb{Z}\_p}$ 送到 $\overline{G}\_{\mathbb{Q}\_p}$. 若再对每个 $\rho$ 选一个新嵌入, 就得到新的 adèle 群 $\overline{G}'\_{\mathbb{A}}$. 上述映射给出 $\overline{G}'\_{\mathbb{A}}$ 到 $\overline{G}\_{\mathbb{A}}$ 的同构, 并且把 $\overline{G}\_{\mathbb{Q}}$ 送到自身. 于是我们有从 $\overline{G}\_{\mathbb{Q}} \backslash \overline{G}'\_{\mathbb{A}}$ 到 $\overline{G}\_{\mathbb{Q}} \backslash \overline{G}\_{\mathbb{A}}$ 的映射, 前面引入的自守形式就给出 $\overline{G}\_{\mathbb{Q}} \vert  \overline{G}'\_{\mathbb{A}}$ 上一个具有同样性质的自守形式 $\phi'$. 我们得检验 

$$
L(s,\phi',\pi) = L(s,\phi,\pi).

$$

> 注：还应检验该级数在 $\mathrm{Re}(s)$ 充分大时收敛. 有办法做到这一点, 但我还没有验证它对所有群都行得通.

再固定 $p$. 此时若 $a\_\sigma = b^\sigma b^{-1}$, 则 

$$
\begin{align*}
a'\_\sigma &= \delta(\tau) a\_\tau^\sigma b^\sigma \delta(\tau^{-1}) \delta(\tau) b^{-1} a\_\tau^{-1} \delta(\tau\_\delta^{-1}) \\
&= \left[\delta'(\sigma^{-1}) \sigma^{-1} \delta(\tau) a\_\tau b \delta(\tau^{-1}) \sigma\sigma'(\sigma)\right] \left[\delta(\tau) a\_\tau b \delta(\tau^{-1})\right]^{-1}.
\end{align*}
$$

所以 $a'\_\sigma$ 被 $b' = \delta(\tau) a\_\tau b \delta(\tau^{-1})$ 分出. 对几乎所有的 $p$, $b'$ 落在 $L \otimes\_{\mathbb{Z}} \overline{\mathbb{Z}}\_p$ 的稳定化子里. 于是有下面的交换图

<figure class="letter-diagram"><img src="{{ site.baseurl }}/img/langlands-weil/diagram-1.svg" alt="交换图：G′ 与 G 的两种内形式"></figure>

这意味着, 若 $\alpha'\_p$ 是与 $\phi'$ 相联系的 $Z\mathfrak{g}\_p\tau^{-1} \times\_\delta {}^cG$ 中的共轭类, 则 $\alpha'\_p = \tau\alpha\_p\tau^{-1}$. 可见对几乎所有的 $p$, $\alpha'\_p$ 与 $\alpha\_p$ 共轭; 于是 $L(s,\phi',\pi)$ 与 $L(s,\phi,\pi)$ 只相差有限个因子.

第一个问题是: 这些乘积是否给出在整个复平面上亚纯、极点具有通常类型的函数; 以及是否对每个 $\phi$ 都有自守形式 $\psi$, 使商 $L(s,\phi,\pi)/L(s,\psi,\tilde\pi)$ 对所有 $\pi$ 都等于初等函数. 这里 $\tilde\pi$ 是 $\pi$ 的逆步表示.

> 注：看来可以取 $\psi = \phi$.

在进入第二个问题之前, 先说一句: Eisenstein 级数方面我做过一些试验, 工作虽远未完成, 但看起来我会得到上述类型的一些级数, 它们与 Eisenstein 级数相关, 因而在整个平面上亚纯. 在较少的某些情形下, 甚至可能借 Eisenstein 级数的函数方程得到函数方程. 眼下的定义, 是我试图找出这样一类 Euler 乘积的结果: 它包含来自 Eisenstein 级数的那些乘积, 又不作任何人为的限制.

现在若 $G = \mathrm{GL}(n)$, $\mathfrak{G}$ 的作用是平凡的, $\pi$ 是表示 $g \mapsto g$, 那么或许可以用 Tamagawa 的想法来处理上述级数. 这就引出第二个问题. 设如上取定 $K$, $G$, $\delta$, 并另取 $K'$, $G'$, $\delta'$. 若 $K \subset K'$, 则有一个同态 $\mathfrak{G}' \to \mathfrak{G}$. 再设 $\omega$ 是从 $\mathfrak{G}' \times\_{\delta'} {}^cG'$ 到 $\mathfrak{G} \times\_\delta {}^cG$ 的同态, 使下面的图交换

<figure class="letter-diagram"><img src="{{ site.baseurl }}/img/langlands-weil/diagram-2.svg" alt="交换图：两个半直积之间的同态"></figure>

若 $\phi'$ 是 $G'^{\delta'}$ 的某个内形式上满足前述条件的自守形式, 则对几乎所有的 $p$, $\phi'$ 确定 $\mathfrak{G}' \times\_{\delta'} {}^cG'\_{\mathbb{C}}$ 中的一个共轭类 $\alpha'\_p$. 设 $\alpha\_p$ 是 $\alpha'\_p$ 在 $\mathfrak{G} \times\_\delta {}^cG\_{\mathbb{C}}$ 中的像. 第二个问题如下: 是否存在与 $G^\delta$ 的某个内形式相联系的自守形式 $\phi$, 使得对几乎所有的 $p$, 与它联系的共轭类正是 $\alpha\_p$?

下面举几例, 说明对这个问题作肯定回答意味着什么.

**(i)** 取 $\mathfrak{G}' = \mathfrak{G}$, 取 $G'$ 为秩 $\ell$ 的分裂环面, 秩 $\ell$ 等于 ${}^cG^\delta$ 的有理秩, 并让 $\mathfrak{G}'$ 平凡地作用于其上. 设 $A$ 是 ${}^cG^\delta$ 的极大分裂环面. 由于 $\mathfrak{G}$ 平凡地作用在 $A$ 上, 有 $\mathfrak{G}' \times\_{\delta'} {}^cG'\_{\mathbb{C}} \cong \mathfrak{G} \times A\_{\mathbb{C}} \subseteq \mathfrak{G} \times\_\delta {}^cG\_{\mathbb{C}}$. 既然 $G'\_{\mathbb{Q}} \backslash G'\_{\mathbb{A}}$ 上有 $\ell$ 个参数族的自守形式, 肯定回答就意味着 $G^\delta$ 的某个内形式上也有同样多的自守形式. 而这一点从 Eisenstein 级数的理论中我们是知道的.

**(ii)** 取 $\mathfrak{G}' = \mathfrak{G}$, $G' = \{1\}$. 把 $\mathfrak{G}' \times\_{\delta'} {}^cG'$ 映入 $\mathfrak{G} \times \{1\} \subseteq \mathfrak{G} \times\_\delta {}^cG\_{\mathbb{C}}$. 这种情形下应当可以通过取 $\phi$ 为某个适当 Eisenstein 级数中把参数取零所得的自守形式, 来给出问题的肯定回答. $\phi'$ 当然是一个常数.

**(iii)** 下面说几句这个问题与 Artin 互反律的关系. 对有理数域, 取 $\mathfrak{G}'$ 交换, $G = \{1\}$, 设 $\chi$ 是 $\mathfrak{G}'$ 的一个特征标. 令 $\mathfrak{G} = \mathfrak{G}'$, 并令 $G$ 是一维分裂环面, $\mathfrak{G}$ 平凡地作用于它. 令 $\omega$ 把 $\tau \times 1$ 送到 $\tau \times \chi(\tau)$. 那么肯定回答恰恰就是有理数域循环扩张的 Artin 互反律. 现在设有如下情形

<figure class="letter-diagram"><img src="{{ site.baseurl }}/img/langlands-weil/diagram-3.svg" alt="交换图：域扩张的塔"></figure>

$K/\mathbb{Q}$ 是 Galois 扩张, $K'\_1 \vert  K\_1$ 是 Abel 扩张. 令 $\mathfrak{G} = \mathfrak{G}(K/\mathbb{Q})$, $\mathfrak{G}\_1$ 为 $\mathfrak{G}$ 中固定 $K\_1$ 的元素, $\mathfrak{G}'\_1$ 为 $\mathfrak{G}$ 中固定 $K'\_1$ 的元素. 最后设 $\chi$ 是 $\mathfrak{G}(K'\_1/K\_1) = \mathfrak{G}\_1 \vert  \mathfrak{G}'\_1$ 的特征标, 从而也是 $\mathfrak{G}\_1$ 的特征标. 我取 $\mathfrak{G}' = \mathfrak{G}$, $G' = \{1\}$. 令 $\ell = [\mathfrak{G}\_1 : \mathfrak{G}]$, 并令 $\mathfrak{G} = \bigcup\_{i=1}^{\ell} \mathfrak{G}\_1\tau\_i$, 其中 $\tau\_1 \in \mathfrak{G}\_1$. $i\_\sigma$ 由 $\tau\_i\sigma \in \mathfrak{G}\_1\tau\_{i\_\sigma}$ 确定. 令 $G$ 为 $\ell$ 个一维分裂环面的直积 $T\_1 \times \dots \times T\_\ell$. 用 $(t\_1 \times \dots \times t\_\ell)^{\delta(\sigma)} = t\_{1\_{\sigma^{-1}}} \times \dots \times t\_{\ell\_{\sigma^{-1}}}$ 定义 $\delta$. 容易验证 $\delta(\sigma)\delta(\tau) = \delta(\sigma\tau)$. 而且 $G^\delta$ 就是 $K\_1$ 的乘法群. 又 ${}^cG = G$. 由 $\tau\_i\sigma^{-1} = \rho\_i^{-1}(\sigma)\tau\_{i\_{\sigma^{-1}}}$ 定义 $\rho\_i(\sigma)$. 则 $\tau\_i\tau^{-1}\sigma^{-1} = \rho\_1^{-1}(\tau)\tau\_{i\_{\tau^{-1}}}\sigma^{-1} = \rho\_1^{-1}(\tau)\rho\_{i\_{\tau^{-1}}}(\sigma)\tau\_{i\_{\tau^{-1}}\sigma^{-1}}$, 所以 $\rho\_i(\sigma\tau) = \rho\_{i\_{\tau^{-1}}}(\sigma)\rho\_i(\tau)$. 再定义 $\omega$ 为 

$$
\omega(\sigma \times 1) = \sigma \times \left(\chi(\rho\_1(\sigma)) \times \dots \times \chi(\rho\_\ell(\sigma))\right).
$$

于是 

$$
\begin{align*}
\omega(\sigma \times 1)\omega(\tau \times 1) &= \sigma\tau \times \prod\_{i=1}^{\ell} \chi(\rho\_{i\_{\tau^{-1}}}(\sigma))\chi(\rho\_i(\tau)) \\
&= \omega(\sigma\tau \times 1).
\end{align*}
$$

 顺便说一下, 若把 $\tau\_i$ ($1 \le i \le \ell$)换成 $\tau'\_i = \mu\_1\tau\_i$, $\mu\_i \in \mathfrak{G}\_1$, 则 $\rho'\_i(\sigma) = \mu\_{i\_{\sigma^{-1}}}^{-1}\rho\_i(\sigma)\mu\_1$, 并且 

$$
\omega'(\sigma \times 1) = (\chi(\mu\_1) \times \dots \times \chi(\mu\_\ell))^{-1}\,\omega(\sigma \times 1)\,(\chi(\mu\_1) \times \dots \times \chi(\mu\_\ell)).
$$

 可见这个映射在本质上不依赖陪集代表元的选取.

我取 $\phi'$ 为常数. 由 Artin 互反律, $\chi$ 对应 $K\_1^\ast  \backslash I\_{K\_1}$ 的一个特征标, 亦即 $G^\delta\_{\mathbb{Q}} \backslash G^\delta\_{\mathbb{A}}$ 上的一个自守形式 $\phi$. 我断言 $\phi$ 就是给问题以肯定回答的那个自守形式.

为了说明这一点, 我们要利用陪集代表元选取的自由. 设 $p$ 是 $K$ 中非分歧的素数. 取定 $K$ 到 $\overline{\mathbb{Q}}\_p$ 的一个嵌入, 并把 $K$ 与其像等同. 设 $\mathfrak{p}\_1,\dots,\mathfrak{p}\_r$ 是 $p$ 在 $K\_1$ 中的素因子. 在 $\mathfrak{G}$ 中选取 $\mu\_1,\dots,\mu\_r$, 使得 $K\_1$ 到 $\overline{\mathbb{Q}}\_p$ 的映射 $x \mapsto x^{\mu\_j}$ 可以延拓成 $K\_1$ 关于 $\mathfrak{p}\_j$ 的完备化到 $\overline{\mathbb{Q}}\_p$ 的连续映射. 令 $L\_j = K\_1^{\mu\_j}\mathbb{Q}\_p$, 并令 $n\_j = [L\_j : \mathbb{Q}\_p]$. 若 $\sigma\_p$ 是 Frobenius 自同构, 则自同构 $\mu\_j\sigma\_p^k$ ($1 \le j \le r$, $0 \le k \le n\_j$)构成 $\mathfrak{G}\_1$ 的陪集的一组代表元. 若 $\tau\_i = \mu\_j\sigma\_p^k$, 则 $\rho\_i(\sigma\_p) = 1$, 除非 $k = 0$; $k = 0$ 时 $\rho\_i(\sigma\_p) = \mu\_j\sigma\_p^{n\_j}\mu\_j^{-1}$. 于是 $\omega(\alpha'\_p) = \alpha\_p$ 的共轭类可以取成 

$$
\sigma\_p \times \prod\_{j=1}^{\ell} \left(\chi(\mu\_j\sigma\_p^{n\_j}\mu\_j^{-1}) \times 1 \times \dots \times 1\right)
$$

 所在的类. 而 $\mu\_j\sigma\_p^{n\_j}\mu\_j^{-1}$ 属于 $\mathfrak{G}\_1$ 中对应于 $\mathfrak{p}\_j$ 的 Frobenius 共轭类.

另一方面, $G^\delta\_{\mathbb{Q}\_p} \subseteq G^\delta\_{\mathbb{A}}$ 由形如 $\prod\_{j=1}^{r}\prod\_{k=0}^{n\_j-1} x\_j^{\sigma\_p^k}$ 的元素组成, 其中 $x\_j$ 是 $L\_j$ 中的非零元. 按定义, $\phi$ 在这种元素上的限制为 

$$
\prod\_{j=1}^{\ell} \chi(\mu\_j\sigma\_p^{n\_j}\mu\_j^{-1})^{o(x\_j)},
$$

 其中 $\vert x\_j\vert  = p^{-o(x\_j)}$. 由于 ${}^cG = G$, 相应的共轭类由满足 

$$
\prod\_{j=1}^{r}\prod\_{k=0}^{n\_j-1} \alpha\_{jk}^{o(x\_j)} = \prod\_{j=1}^{r} \chi(\mu\_j\sigma\_p^{n\_j}\mu\_j^{-1})^{o(x\_j)}
$$

 的任一元素 

$$
\sigma\_p \times \prod\_{j=1}^{r}\prod\_{k=0}^{n\_j-1} \alpha\_{jk}
$$

 确定. 回看上面的讨论, 我们看到 $\omega(\alpha'\_p)$ 正是这样一个元素.

**(iv)** 最后, 我想说说对第二个问题作肯定回答, 对于寻找非交换扩张的分裂律会有什么推论. 我本来打算讨论任意基域, 但现在意识到必须把基域取成 $\mathbb{Q}$.

> 注：不过大概可以回过头来, 把这两个问题放到数域上群的框架里重新表述. 第一个问题对基域的选取不敏感, 第二个问题则敏感.

设 $K$ 是 $\mathbb{Q}$ 的 Galois 扩张, $\mathfrak{G} = \mathfrak{G}(K/\mathbb{Q})$. 我们想找一种方法, 对几乎所有的 $p$ 求 $\mathfrak{G}$ 中的 Frobenius 共轭类 $\{\sigma\_p\}$. 因此, 对所有表示 $\pi: \mathfrak{G} \to \mathrm{GL}(m,\mathbb{C})$, 我们得求出 $\mathrm{GL}(m,\mathbb{C})$ 中 $\pi(\sigma\_p)$ 的迹, 或者 $\pi(\sigma\_p)$ 的共轭类. 先固定 $\pi$. 如前, 我取 $\mathfrak{G}' = \mathfrak{G}$, $G' = \{1\}$, $\phi'$ 为常函数. 我取 $G = \mathrm{GL}(m)$. 先验证 ${}^cG$ 也是 $\mathrm{GL}(m)$.

取 $\tilde{G} = {}^c\tilde{G} = A \times \mathrm{SL}(m)$, 其中 $A$ 是一维分裂环面. 则 

$$
\begin{align*}
{}^c\tilde{L} = \tilde{L} &= \left\{ (z,z\_1,\dots,z\_m) \;\middle\vert \; z,\, z\_i - z\_j \in \mathbb{Z},\ \textstyle\sum\_{i=1}^{m} z\_i = 0 \right\}, \\
{}^cL = L &= \left\{ (z,z\_1,\dots,z\_m) \;\middle\vert \; z\_i + \dfrac{z}{m} \in \mathbb{Z},\ \textstyle\sum\_{i=1}^{m} z\_i = 0 \right\}, \\
{}^c\tilde{L}' = \tilde{L}' &= \left\{ (mz,\, z\_1,\, z\_2 - z\_1,\dots, z\_{m-1} - z\_{m-2},\, -z\_{m-1}) \;\middle\vert \; z, z\_i \in \mathbb{Z} \right\}.
\end{align*}
$$

 配对取为 

$$
\left\langle (z,z\_1,\dots,z\_m),\, (y,y\_1,\dots,y\_m) \right\rangle = \frac{zy}{m} + \sum\_{i=1}^{m} z\_i y\_i.
$$

 不管怎样, 都有 $G = {}^cG = \mathrm{GL}(m)$. 用 

$$
\omega(\sigma \times 1) = \sigma \times \pi(\sigma)
$$

 定义 $\omega$. $\mathfrak{G}$ 对 $G$ 的作用取为平凡. $\omega(\alpha'\_p) = \alpha\_p$ 就是 $\sigma\_p \times \pi(\sigma\_p)$ 所在的共轭类, 它当然决定了 $\pi(\sigma\_p)$ 的共轭类. 我们需要一种求 $\pi(\sigma\_p)$ 所在类的方法.

设 $\mathrm{GL}(m)$ 的某个内形式上有自守形式 $\phi$, 给上述问题以肯定回答. 要求出 $\{\pi(\sigma\_p)\}$, 只需计算对应于特征函数 $\phi$ 的 Hecke 代数 $H\_p$ 的有限个元素的特征值. 取一个含无穷素数的有限素数集 $S$, 使得若 $\overline{G}\_S = \prod\_{q\in S}\overline{G}\_{\mathbb{Q}\_q}$, $\overline{G}\_{S'} = \prod\_{q\notin S}\overline{G}\_{\mathbb{Z}\_q}$, 则 $\overline{G}\_{\mathbb{A}} = \overline{G}\_{\mathbb{Q}}\overline{G}\_S\overline{G}\_{S'}$, 并且 $\phi$ 是 $\overline{G}\_{\mathbb{Q}} \backslash \overline{G}\_{\mathbb{A}} / \overline{G}\_{S'}$ 上的函数.

设 $p \notin S$, $f$ 是 $\overline{G}\_{\mathbb{Z}\_p} a \overline{G}\_{\mathbb{Z}\_p}$ 的特征函数, 而后者是不相交并 $\bigcup\_{i=1}^{n} a\_i\overline{G}\_{\mathbb{Z}\_p}$. 若 $g \in \overline{G}\_S$, 则 

$$
\begin{align*}
\lambda(f)\phi(g) &= \int\_{\overline{G}\_{\mathbb{Q}\_p}} \phi(gh)f(h)\,dh \\
&= \sum\_{i=1}^{n} \phi(ga\_i) = \sum\_{i=1}^{n} \phi(a\_ig),
\end{align*}
$$

 因为 $a\_i \in \overline{G}\_{\mathbb{Q}\_p}$. 在 $\overline{G}\_{\mathbb{Q}}$ 中取 $\overline{a}\_1,\dots,\overline{a}\_n$, 使 $\overline{a}\_i^{-1}a\_i \in \overline{G}\_{S'}\overline{G}\_S$, 并令 $b\_i$ 为 $\overline{a}\_i$ 在 $\overline{G}\_S$ 上的投影. 若 $\chi(f)$ 是 $f$ 的特征值, 则 

$$
\chi(f)\phi(g) = \sum \phi(\overline{a}\_i^{-1}a\_ig) = \sum \phi(b\_i^{-1}g).
$$

 粗略地说, 元素 $\overline{a}\_1,\dots,\overline{a}\_n$ 由一些以 $p$ 为参数的丢番图方程的求解得到. 于是 $\phi(b\_i^{-1}g)$ 依赖于 $\overline{a}\_i$ 在模 $S$ 中有限素数的幂下的同余性质, 以及 $\overline{a}\_i$ 在 $\overline{G}\_{\mathbb{Q}\_\infty} = \overline{G}\_{\mathbb{R}}$ 上的投影. 如果对每个 $g \in \overline{G}\_S$, 把 $\phi(hg)$ 看作 $\overline{G}\_{\mathbb{R}}$ 连通分支中 $h$ 的函数是有理的, 我们就能得到好的分裂律. 它会相当复杂, 但原则上不会比 Dedekind-Hasse 关于三次方程分裂域的分裂律更差. 然而由于强逼近, $\phi(hg)$ 大概不会是有理的, 除非 $m = 1$ 或 $2$. 因此我们只能得到超越的分裂律.

尽管如此, 如果取 $G$ 为 $2n$ 个变量上的辛群, ${}^cG$ 为 $2n + 1$ 个变量上的正交群, 那么强逼近就不是障碍了, 因为 $G$ 有使 $\overline{G}\_{\mathbb{R}}$ 紧的内形式. 我们可以指望通过考虑 $\mathfrak{G}$ 到 ${}^cG$ 的嵌入, 得到关于 $\sigma\_p$ 的阶之类东西的规律.

<div class="letter-signature">Yours truly,<br>R. Langlands</div>

<p style="font-size: 24px; font-weight: bold;">补充</p>

**(v)** 设 $K$ 是 $\mathbb{Q}$ 的二次扩张. 令 $\mathfrak{G}' = \mathfrak{G}(K/\mathbb{Q})$. 令 $G' = {}^cG' = A\_1 \times A\_2$, 其中 $A\_1$ 与 $A\_2$ 是一维分裂环面. 若 $\sigma$ 是 $\mathfrak{G}$ 的非平凡元, 令 $(t\_1 \times t\_2)^{\delta'(\sigma)} = t\_2 \times t\_1$. 令 $G = \mathrm{GL}(2)$, $\mathfrak{G}$ 平凡地作用于 $G$. 用 

$$
\begin{align*}
\omega(1 \times (t\_1,t\_2)) &= \begin{pmatrix} t\_1 & 0 \\ 0 & t\_2 \end{pmatrix} \\
\omega(\sigma \times (t\_1,t\_2)) &= \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}\begin{pmatrix} t\_1 & 0 \\ 0 & t\_2 \end{pmatrix}
= \begin{pmatrix} 0 & t\_2 \\ t\_1 & 0 \end{pmatrix}
\end{align*}
$$

 定义 $\omega$. $G'^{\delta'}\_{\mathbb{A}}$ 就是 $K$ 的 adèle 群. 取 $\phi'$ 为 Grössencharakter. Hecke 与 Maass 关于二次域上带 Grössencharakter 的 $L$ 级数与自守形式之间关系的工作, 很可能正好给第二个问题的这一情形提供肯定回答.
