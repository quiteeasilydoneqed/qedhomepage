---
layout: post
title: "序与格"
subtitle: ""
header-img: "img/post-bg-infinity.jpg"
header-mask: 0.3
math: true
tags:
  - 序论
  - 格论
  - 代数
---

# 序

### 序结构

序结构一般指一个集合 $X$ 连带其上一个二元关系 $\le$, 该关系一般可以满足以下条件中的若干个.

* 自反性: $\forall x\in X$, $x\le x$;
* 传递性: $\forall x,y,z\in X$, 若 $x\le y$ 且 $y\le z$, 则 $z \le z$;
* 反称性: $\forall x,y\in X$, 若 $x\le y$ 且 $y\le x$, 则 $x=y$;
* 滤过性: $\forall x,y\in X$, $\exists z\in X$, 满足 $x\le z$ 且 $y\le z$;
* 线序性: $\forall x,y\in X$, $x\le y$ 与 $y\le x$ 二者至少成立一个;
* 良基性: $X$ 中任意非空子集 $S$, 都存在 $s\in S$, 使得对 $\forall x\in S$, 若 $x\le s$, 则 $x=s$, 即任意非空子集 $S$ 均有极小元 $s$.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(序结构)</b>

满足自反性和传递性的序结构称为预序集;<br>

满足自反性, 传递性和反称性的序结构称为偏序集;<br>

满足滤过性的预序集称为滤过预序集, 满足滤过性的偏序集称为滤过偏序集或有向集;<br>

满足线序性的偏序集称为全序集或线序集;<br>

满足良基性的全序集称为良序集.

</div>

对任意序结构 $(X,\le)$, 定义 $x<y$ 意为 $x\le y$ 且 $x\neq y$, 这是一个二元关系, 称 $(X,<)$ 为严格预序集, 严格偏序集或严格全序集.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(态射)</b>

设 $(P, \le_P)$ 和 $(Q, \le_Q)$ 是两个偏序集, $f\colon P \to Q$ 是从 $P$ 到 $Q$ 的映射.

如果对于任意 $x, y \in P$, $x \le_P y$ 蕴含 $f(x) \le_Q f(y)$, 则称 $f$ 是保序映射.

如果对于任意 $x, y \in P$, $x <_P y$ 蕴含 $f(x) <_Q f(y)$, 则称 $f$ 是严格增映射.

如果 $f$ 是双射, 且 $f$ 与其逆映射皆保序, 则称 $f$ 是序同构.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定义</b>

设 $(P, \le)$ 为预序集, $S \subseteq P$.<br>

若元素 $a \in P$ 满足对任意 $x \in P$, $a \le x$ 均蕴含 $x \le a$, 则称 $a$ 为 $P$ 的极大元;<br>

若元素 $a \in P$ 满足对任意 $x \in P$, $x \le a$ 均蕴含 $a \le x$, 则称 $a$ 为 $P$ 的极小元;<br>

若元素 $a \in P$ 满足对任意 $x \in P$, 均有 $x \le a$, 则称 $a$ 为 $P$ 的最大元;<br>

若元素 $a \in P$ 满足对任意 $x \in P$, 均有 $a \le x$, 则称 $a$ 为 $P$ 的最小元;<br>

若元素 $u \in P$ 满足对所有 $s \in S$ 都有 $s \le u$, 则称 $u$ 为 $S$ 的上界;<br>

若元素 $l \in P$ 满足对所有 $s \in S$ 都有 $l \le s$, 则称 $l$ 为 $S$ 的下界;<br>

若存在 $u \in P$, 使得 $u$ 是 $S$ 的上界, 且对 $S$ 的任一上界 $x$ 都有 $u \le x$, 则称 $u$ 为 $S$ 的上确界;<br>

若存在 $l \in P$, 使得 $l$ 是 $S$ 的下界, 且对 $S$ 的任一下界 $x$ 都有 $x \le l$, 则称 $l$ 为 $S$ 的下确界.

</div>

对于偏序集, 上下确界若存在则必唯一, 分别记为 $\sup S$ 和 $\inf S$.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(链与反链)</b>

设 $(P, \le)$ 为偏序集, $C \subseteq P$, 如果对 $\forall x, y \in C$, 都有 $x \le y$ 或 $y \le x$ 成立, 则称 $C$ 为 $P$ 的一条链, 即偏序集的全序子集称为链.<br>

设 $A \subseteq P$, 如果 $\forall x, y \in A$ 且 $x \ne y$, $x \le y$ 与 $y \le x$ 均不成立, 则称 $A$ 为 $P$ 的一条反链.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定理(佐恩引理)</b>

在ZFC公理体系中, 设 $(P, \le)$ 是一个非空的偏序集, 如果 $P$ 中的每一条链在 $P$ 中都有上界, 则 $P$ 至少存在一个极大元.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定理(良序定理)</b>

在ZFC公理体系中, 任何集合上都存在二元关系使其成为良序集.

</div>

佐恩引理与良序定理与选择公理是等价的.

由序结构可以得到一些其他结构.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(序拓扑)</b>

设 $(P,\le)$ 是一个全序集, 则如下形式的集合组成其上的一组拓扑基, 其生成的拓扑称为 $P$ 上的序拓扑:<br>

所有的开区间 $(a, b) = \{x \in P \mid a < x < b\}$, 其中 $a, b \in P$;<br>

若 $P$ 存在最小元 $a_0$, 则包含所有形如 $[a_0, b) = \{x \in P \mid a_0 \le x < b\}$ 的集合, 其中 $b \in P$;<br>

若 $P$ 存在最大元 $b_0$, 则包含所有形如 $(a, b_0] = \{x \in P \mid a < x \le b_0\}$ 的集合, 其中 $a \in P$.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(序作为范畴)</b>

设 $(P,\le)$ 是一个预序集, 定义范畴 $\mathsf{P}$ 的对象为集合 $P$, 任意两对象间存在唯一态射 $x\to y$ 当且仅当 $x\le y$, 显然它是范畴, 特别的, 全序集 $\{0,1,\cdots,n-1\}$ 给出的范畴记为 $\mathsf{n}$.

</div><br>

### 亚历山德罗夫拓扑

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(亚历山德罗夫拓扑)</b>

设 $(P,\le)$ 是预序集, 其上的拓扑由满足如下性质的集合组成: $U$ 是开集当且仅当 $x \in U$ 且 $x \le y$ 能推出 $y \in U$, 称这样的集合为上集, 这样的拓扑为亚历山德罗夫拓扑.

</div>

容易验证亚历山德罗夫拓扑确实是拓扑.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

设 $f$ 是两个带亚历山德罗夫拓扑的预序集之间的映射, 则 $f$ 连续当且仅当 $f$ 保序.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

设 $f\colon X\to Y$ 保序, 若 $U$ 是 $Y$ 中开集, 设 $x\in f^{-1}(U)$, $x\le_X y$, 则 $f(x)\le_Y f(y)$, 因此 $f(y)\in U$, $y\in f^{-1}(U)$, 故 $f^{-1}(U)$ 是 $X$ 中开集, $f$ 连续.<br>

设 $f$ 连续, $x,y\in X$, $x\le_X y$, 定义 $U=\{z\in Y\mid f(x)\le_Y z\}$, 显然它是 $Y$ 中开集, 故 $f^{-1}(U)$ 是 $X$ 中开集, 所以 $y\in f^{-1}(U)$, $f(y)\in U$, 由 $U$ 的定义知 $f(x)\le_Y f(y)$.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

亚历山德罗夫拓扑满足 $T_0$ 公理当且仅当预序集 $P$ 是偏序集.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

设 $P$ 是预序集, 其上亚历山德罗夫拓扑满足 $T_0$, 设 $x,y\in P$, 且 $x\le y$, $y\le x$, 故包含 $x$ 的开集必包含 $y$, 反之亦然, 由 $T_0$ 性知只能有 $x=y$, 故 $P$ 是偏序集.<br>

设 $P$ 是偏序集, $x,y\in P$ 是两个不同的点, 则 $x\le y$ 和 $y\le x$ 不能同时成立, 不妨设 $x\not\le y$, 定义 $U=\{z\in P\mid x\le z\}$, 则 $x\in U$, $y\notin U$, 于是亚历山德罗夫拓扑满足 $T_0$ 公理.

</div>

设预序集连同保序映射组成的范畴为 $\mathsf{PerOrd}$, 其中偏序集组成的全子范畴为 $\mathsf{Pos}$.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(亚历山德罗夫空间)</b>

设 $X$ 是一个拓扑空间, 如果其中任意开集的交仍是开集, 任意闭集的并仍是闭集, 则称该拓扑空间为亚历山德罗夫空间.

</div>

设带亚历山德罗夫空间连同连续映射组成的范畴为 $\mathsf{Alex}$, 其中满足 $T_0$ 公理的空间组成的全子范畴为 $\mathsf{Alex_0}$.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

$\mathsf{PerOrd}$ 与 $\mathsf{Alex}$ 范畴同构, $\mathsf{Pos}$ 与 $\mathsf{Alex_0}$ 范畴同构.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

只需证明前者, 后者即可由上一定理推出.<br>

首先证明预序集上亚历山德罗夫拓扑构成一个亚历山德罗夫空间, 设 $\{U_i\}_{i\in I}$ 是一族以 $I$ 为指标集的开集, 任取 $x\in \bigcap_{i\in I}U_i$, 则对每个 $i$, 都有 $x\in U_i$, 于是对任意的 $y\ge x$ 都有 $y\in U_i$, 因此 $y\in\bigcap_{i\in I}U_i$, 故 $\bigcap_{i\in I}U_i$ 也是开集, 于是该拓扑空间是亚历山德罗夫空间.<br>

其次, 我们将亚历山德罗夫空间做成一个预序集, 对于亚历山德罗夫空间 $P$ 中的每个点 $x$, 定义 $U_x=\{z\in P\mid x\le z\}$, 再定义 $x\le y\Longleftrightarrow U_x\subseteq U_y$, 该序的自反性和传递性由集合的包含关系保证, 因此是预序.<br>

我们定义函子 $F\colon \mathsf{PerOrd}\to\mathsf{Alex}$ 将预序集映到它的亚历山德罗夫拓扑, 函子 $G\colon \mathsf{Alex}\to\mathsf{PerOrd}$ 将亚历山德罗夫空间映到其上的预序结构, 由以上讨论立刻知 $F\circ G=\mathrm{id}_\mathsf{Alex}$, $G\circ F=\mathrm{id}_\mathsf{PerOrd}$, 态射层面由连续当且仅当保序保证, 于是 $\mathsf{PerOrd}$ 与 $\mathsf{Alex}$ 范畴同构, $\mathsf{Pos}$ 与 $\mathsf{Alex_0}$ 范畴同构.

</div>

# 格

### 基础定义

格是满足特殊条件的偏序集.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(并与交)</b>

设 $(P,\le)$ 是偏序集, $x,y\in P$, 定义 $x\wedge y=\inf\{x,y\}$ 为 $x$ 和 $y$ 的交, $x\vee y=\sup\{x,y\}$ 为 $x$ 和 $y$ 的并. 对 $\forall S\subseteq P$, 定义 $\bigwedge S=\inf S$, $\bigvee S=\sup S$.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(格)</b>

设 $(P,\le)$ 是偏序集, 若对 $\forall x,y\in P$, $x\wedge y$ 都存在, 则称 $P$ 为交半格, 若 $x\vee y$ 都存在, 则称 $P$ 为并半格, 若二者都存在, 则称 $P$ 为格.

</div>

格有时也记作 $(P,\le,\wedge,\vee)$ 或 $(P,\wedge,\vee)$, 后面将看到满足一定性质的二元运算可以反过来诱导偏序结构. 设 $a,b,c\in P$, 则下列性质是显然的:

* 幂等律: $a \vee a = a$, $a \wedge a = a$;
* 交换律: $a \vee b = b \vee a$, $a \wedge b = b \wedge a$;
* 结合律: $a \vee (b \vee c) = (a \vee b) \vee c$, $a \wedge (b \wedge c) = (a \wedge b) \wedge c$;
* 吸收律: $a \vee (a \wedge b) = a$, $a \wedge (a \vee b) = a$.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(顶与底)</b>

设 $(P,\le)$ 是偏序集, 若 $\sup P$ 存在, 则称该元素为 $P$ 的顶元, 记为 $\top$ 或 $1$, 若 $\inf P$ 存在, 则称该元素为 $P$ 的底元, 记为 $\bot$ 或 $0$.

</div>

若顶元和底元皆存在, 则约定 $\sup \emptyset=\bot$, $\inf\emptyset=\top$.

格 $P$ 可能满足以下性质中的若干个.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义</b>

设 $P$ 是格,

* 若对任意的子集 $S\subseteq P$, $\bigwedge S$ 和 $\bigvee S$ 都存在, 则称 $P$ 为完备格;
* 若对任意的 $a,b,c\in P$, $a \le c$ 均能推出 $a \vee (b \wedge c) = (a \vee b) \wedge c$, 则称 $P$ 为模格;
* 若对任意的 $a,b,c\in P$, 都有 $a \wedge (b \vee c) = (a \wedge b) \vee (a \wedge c)$, 则称 $P$ 为分配格;
* 若格中存在顶元和底元, 则称 $P$ 为有界格;
* 若 $P$ 是有界格且对任意的 $a\in P$，存在 $a'\in P$ 使得 $a \vee a' = \top$ 且 $a \wedge a' = \bot$, 称 $a'$ 是 $a$ 的补元, $P$ 为有补格;
* 若 $P$ 同时是有补格和分配格, 则称 $P$ 是布尔格或布尔代数.

</div>

注记1: 由于 $a \wedge (b \vee c) = (a \wedge b) \vee (a \wedge c)\Longleftrightarrow a \vee (b \wedge n) = (a \vee b) \wedge (a \vee c)$, 则分配格只需满足其中任一即可推出另一条.

注记2: 由分配性可推出补元若存在则唯一, 因此布尔格的补元唯一.

注记3: 完备格显然是有界格, 只需取 $S$ 为 $P$ 或 $\emptyset$ 即可.

### 布尔环

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(布尔环)</b>

设 $R$ 是含幺环, 如果对任意 $x\in R$, 都有 $x^2=x$, 即所有元素都是幂等元, 则称 $R$ 是布尔环.

</div>

布尔环一定是可交换的, 并且一定有 $x+x=0$, 这是因为, 

$$
\displaylines{x+y=(x+y)^2=x^2+y^2+xy+yx=x+y+xy+yx}
$$

于是 $xy=-yx$, 取 $y=1$ 即得 $x=-x$, 故 $xy=yx$ 且 $x+x=0$.

设所有布尔环连同环同态组成的范畴为 $\mathsf{BoolRing}$, 布尔代数连同布尔代数同态组成的范畴为 $\mathsf{BoolAlg}$, 这里布尔代数同态的意思是保持交, 并, 顶元以及底元的映射.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

$\mathsf{BoolRing}$ 与 $\mathsf{BoolAlg}$ 范畴同构.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

设 $R$ 是布尔环, 在其上引入序关系 $x\le y\Longleftrightarrow x=xy$, 再定义格运算 $x\vee y=x+y+xy$, $x\wedge y=xy$, 底元为 $0$, 顶元为 $1$, 补元由 $a'=1-a$ 确定, 容易验证这确实是一个布尔格.<br>

设 $L$ 是布尔格, 在其上引入环结构为 $x+y=(x\wedge y')\vee(x'\wedge y)$, $xy=x\wedge y$, 显然它构成一个布尔环.<br>

按如上方法将布尔环结构映为布尔代数结构的函子是一个范畴同构, 此处省略验证.

</div>

### 滤子

此处讲的是格论意义下的滤子, 集合意义下的滤子实际上是包含关系下的特殊情况, 滤子的对偶有时也称为理想, 此处只叙述滤子的情况, 取对偶即可得到关于理想的叙述.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(滤子)</b>

设 $P$ 是一个偏序集, 非空子集 $F\subseteq P$ 如果满足以下条件:<br>

1, $F \neq \emptyset$;<br>

2, 对于任意 $x \in F$ 和 $y \in P$, 如果 $x \le y$, 则 $y \in F$;<br>

3, 对于任意 $x, y \in F$, 存在元素 $z\in F$ 使得 $z \le x$ 且 $z \le y$,<br>

则称 $F$ 是 $P$ 的一个滤子, 如果 $P$ 还是格, 则第三条等价于说 $x\wedge y\in F$.

</div>

若滤子不是全集 $P$, 则称为真滤子, 形如 $\uparrow x=\{y\in P\mid x\le y\}$ 的集合称为 $x$ 生成的主滤子, 所有滤子组成的集合记为 $\mathrm{Fil}(P)$, 它在包含关系下显然构成偏序集.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(超滤子)</b>

设 $P$ 是一个偏序集, $\mathrm{Fil}(P)-\{P\}$ 里的极大元称为超滤子或极大滤子.

</div>

可以证明任何滤子都一定包含在某个超滤子中, 但该证明需要选择公理.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义</b>

设 $L$ 是一个格, $F$ 是一个真滤子, 如果对于任何 $a, b \in L$, $a \vee b \in P$ 都能推出 $a \in F$ 或 $b \in F$, 则称 $F$ 是一个素滤子.

</div>

如果格 $L$ 是分配格, 则超滤子都是素滤子, 如果 $L$ 是有补格, 则素滤子都是超滤子, 如果格是一个布尔格, 则素滤子和超滤子是等价的.

### 斯通表示定理

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(斯通空间)</b>

完全不连通的紧豪斯多夫空间称为斯通空间.

</div>

完全不连通指其连通子集只有单点集或空集. 假设所有斯通空间连同连续映射组成的范畴为 $\mathsf{Stone}$.

重要的是斯通空间的所有既开又闭的子集, 显然它们的有限交和有限并均既开又闭, 它们的补集也既开又闭, 又因为空集和全集均既开又闭, 容易验证斯通空间的所有既开又闭子集组成一个布尔格.

现在, 设 $B$ 是一个布尔格, 我们取 $B$ 中所有超滤子组成的集合为 $S(B)$, 设 $x\in B$, 由佐恩引理可推出集合 $\{ U\in S(B)\mid x\in U\}$ 非空, 所有的这些集合组成 $S(B)$ 上的一组拓扑基, 由它生成的拓扑称为 $S(B)$ 上的斯通拓扑, 可以验证这是一个斯通空间.

另一方面, 先前已知每个布尔格都是布尔环, 可以直接取其素谱, 仍记为 $\mathrm{Spec}(B)$, 其上拓扑取扎里斯基拓扑, 由交换代数容易证明它是斯通空间, 并且与 $S(B)$ 同胚.

设 $\mathbf{2}$ 为二元集 $\{0,1\}$, 它显然是布尔格, 在 $\mathrm{Hom}_{\mathsf{BoolAlg}}(B,\mathbf{2})$ 上定义拓扑为由集族 $\{\{f \in \mathrm{Hom}_{\mathsf{BoolAlg}}(B,\mathbf{2}) \mid f(a) = 1\}\}_{a\in B}$ 生成的拓扑, 这使其同胚于 $S(B)$ 和 $\mathrm{Spec}(B)$. 也就是说, 从 $\mathsf{BoolAlg}$ 到 $\mathsf{Stone}^{op}$ 的三个函子 $S(\cdot)$, $\mathrm{Spec}(\cdot)$ 和 $\mathrm{Hom}_{\mathsf{BoolAlg}}(\cdot,\mathbf{2})$ 是三个同构的函子.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理(斯通表示定理)</b>

$\mathsf{BoolAlg}$ 与 $\mathsf{Stone}^{op}$ 范畴等价.

</div>

素谱的反变性由交换代数得出, $\mathrm{Hom}$ 函子对第一个槽位的反变性由范畴论得出, 超滤函子的反变性亦容易证明.

### 范畴等价

此处范畴等价指的是预序范畴的一系列子范畴与拓扑空间范畴的一系列子范畴之间的范畴等价或对偶等价, 包括之前提到的一些范畴同构或等价定理.

#### 伯克霍夫表示定理

伯克霍夫表示定理针对有限分配格, 即具有有限个元素的分配格.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(并不可约元)</b>

设 $L$ 是一个格, $x\in L$, 如果 $x\neq0$, 且 $x=a\wedge b$ 等价于 $x=a$ 或 $x=b$, 则称 $x$ 是 $L$ 中的一个并不可约元.

</div>

所有并不可约元组成的集合记为 $J(L)$, 它是 $L$ 的子集, 继承了 $L$ 中的偏序结构成为一个偏序集.

现在令 $P$ 是任意偏序集, $D$ 是 $P$ 的子集, 称 $D$ 是 $P$ 的下集当且仅当 $x \in D$ 且 $y \le x$ 能推出 $y \in D$, $P$ 的所有下集组成的集合记为 $O(P)$, 它显然关于集合的交和并构成一个分配格.

现在设所有有限分配格连同格同态组成的范畴为 $\mathsf{FDLat}$, 所有有限偏序集连同单调映射组成的范畴为 $\mathsf{FPos}$.

可以证明, 如果 $L$ 是有限分配格, $P$ 是有限偏序集时, $O(J(L))\cong L$, $J(O(P))\cong P$.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理(伯克霍夫表示定理)</b>

$\mathsf{FDLat}$ 与 $\mathsf{FPos}^{op}$ 范畴等价.

</div>

#### 普利斯特里对偶定理

普利斯特里对偶定理针对的是任意有界分配格, 它是斯通表示定理和伯克霍夫表示定理的推广.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(普利斯特里空间)</b>

设 $P$ 是一个斯通空间, 如果在其上有一个偏序 $\le$, 满足普利斯特里分离公理: $\forall x,y\in P$, 若 $x\not\le y$, 则存在 $P$ 中既开又闭的上集 $U$, 使得 $x\in U$, $y\notin U$.

</div>

事实上, 普利斯特里分离公理可以直接推出豪斯多夫性和完全不连通性, 每个普利斯特里空间的底层拓扑都是斯通空间, 而每个斯通空间关于集合间包含关系都是普利斯特里空间, 然而, 存在一些并非包含关系的偏序仍是普利斯特里空间. 设所有普利斯特里空间连通保序连续映射组成的范畴为 $\mathsf{Pries}$, 则 $\mathsf{Stone}$ 可以看做 $\mathsf{Pries}$ 的子范畴.

设 $P$ 是普利斯特里空间, 其所有既开又闭的上集关于集合的交和并组成一个有界分配格. 设 $L$ 是一个有界分配格, 所有形如 $\{ U\mid x\in U\},x\in L$ 的集合组成所有素滤子组成的集合上的一组拓扑基, 它生成的拓扑空间连同素滤子间包含关系组成一个普利斯特里空间.

设所有有界分配格连同保界格同态组成的范畴为 $\mathsf{DLat}$.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理(普利斯特里对偶定理)</b>

$\mathsf{DLat}$ 与 $\mathsf{Pries}^{op}$ 范畴等价.

</div>

#### 埃萨基亚对偶

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(海廷代数)</b>

设 $H$ 是一个有界格, 如果对 $\forall a,b\in H$, 集合 $\{x\mid a\wedge x\le b\}$ 有最大元, 则称 $H$ 为一个海廷代数, 记该最大元为 $a\to b$.

</div>

海廷代数是为直觉主义逻辑建立, $\to$ 运算称为伪补或直觉主义蕴含. 海廷代数一定是分配的. 布尔代数一定是海廷代数, 其中 $a\to b=a'\vee b$.

设所有海廷代数和海廷代数同态组成的范畴为 $\mathsf{HA}$.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(埃萨基亚空间)</b>

设 $E$ 是一个普利斯特里空间, 如果对于其中任意的既开又闭子集 $C$, $\{x\in E\mid \exists y\in C,x\le y\}$ 也是既开又闭的子集, 则称 $E$ 是埃萨基亚空间.

</div>

埃萨基亚同态指保持埃萨基亚空间结构的映射, 设所有埃萨基亚空间和埃萨基亚同态组成的范畴为 $\mathsf{Esa}$.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理(埃萨基亚对偶定理)</b>

$\mathsf{HA}$ 与 $\mathsf{Esa}^{op}$ 范畴等价.

</div>

#### 无点拓扑

无点拓扑的宗旨是不研究拓扑空间中具体的点, 而是研究开集族构成的格, 使得一些依赖于选择公理的拓扑学定理在翻译至无点拓扑语言后不依赖选择公理, 于是与直觉主义逻辑有深入联系. 无点拓扑也与拓扑斯理论有很多联系.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(框架)</b>

设 $F$ 是一个完备格, 并且满足无限分配率, 则称 $F$ 是一个框架, 即对 $F$ 的任意子集 $S$ 和任一元素 $a$, 都有

$$
\displaylines{a \wedge \left(\bigvee S\right) = \bigvee_{s \in S} (a \wedge s).}
$$

</div>

注: Frame目前无统一的中文翻译, 有人译为位格, 此处采用直译.

框架间的同态是保持任意并的格同态. 框架范畴记为 $\mathsf{Frm}$.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(位象)</b>

定义 $\mathsf{Loc}=\mathsf{Frm}^{op}$, 其中对象称为位象, 一般记函子 $\mathcal{O}\colon \mathsf{Frm}\to\mathsf{Loc}$, 如果 $f\colon X\to Y$ 是框架间态射, 则 $\mathcal{O}(f)\colon \mathcal{O}(Y) \to \mathcal{O}(X)$.

</div>

设 $(X,\mathcal{T})$ 是一个拓扑空间, $\mathcal{T}$ 在集合的包含关系下构成一个完备格, 并且显然满足无限分配率, 因此是框架, 也是位象, 我们定义函子 $\Omega\colon \mathsf{Top}\to\mathsf{Loc},(X,\mathcal{T})\mapsto(\mathcal{T},\subseteq)$, 态射层面, 设 $f\colon (X,\mathcal{T}_x)\to (Y,\mathcal{T}_Y)$ 是连续函数, 则容易验证 $f^{-1}\colon (\mathcal{T}_Y,\subseteq)\to(\mathcal{T}_X,\subseteq)$ 是框架同态, 于是 $f$ 的像 $\Omega(f)=\mathcal{O}(f^{-1})$ 就是位象同态.

另一方面, 设 $L$ 是一个位象, 定义 $pt(L)=\mathrm{Hom}_{\mathsf{Frm}}(L,\mathbf{2})$, 其中 $\mathbf{2}=\{0,1\}$ 是二元格, 在 $pt(L)$ 上定义拓扑如下, 对任意 $a\in L$, 定义 $U_a=\{p\in pt(L)\mid p(a)=1\}$, 可以验证 $\{U_a\}_{a\in L}$ 是一组拓扑基, 它生成的拓扑使 $pt(L)$ 成为拓扑空间, 另一方面, $pt$ 是一个 $\mathrm{Hom}$ 函子, 函子在态射层面的像由拉回映射给出, 并且它是从 $\mathsf{Frm}$ 到 $\mathsf{Top}$ 的反变函子, 于是也就是从 $\mathsf{Loc}$ 到 $\mathsf{Top}$ 的协变函子.

一个事实是, 如果在 $\mathbf{2}$ 上取拓扑为 $\{\emptyset,\{1\},\{0,1\}\}$, 即谢尔宾斯基空间, 则 $pt(L)$ 是乘积空间 $\mathbf{2}^L$ 的子空间.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

$\Omega$ 和 $pt$ 是一对伴随函子, $\Omega\dashv pt$, 具体来说就是对任意拓扑空间 $X$ 和任意位象 $L$ 有

$$
\displaylines{\mathrm{Hom}_{\mathsf{Loc}}(\Omega(X), L) \cong \mathrm{Hom}_{\mathsf{Top}}(X, pt(L)).}
$$

</div>

接下来将这两个函子限制在子范畴上构成两个子范畴的等价.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(清晰空间)</b>

如果一个拓扑空间的所有非空不可约闭集都是唯一一个单点集的闭包, 则称其为清晰空间. 就是说, 如果 $A$ 是清晰空间 $X$ 中的非空不可约闭集, 则存在唯一的 $x\in X$, 使得 $A=\overline{\{x\}}$. 所有清晰空间连同连续映射组成的范畴记为 $\mathsf{Sob}$.

</div>

清晰空间英文为 Sober, 这并非人名, 因此此处选择直译为清晰, 也有人译为索伯空间. 显然 $\mathsf{Sob}$ 是 $\mathsf{Top}$ 的全子范畴.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

拓扑空间 $X$ 是清晰空间当且仅当它同胚于某个位象在 $pt$ 函子下的像.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(空间式位象)</b>

设 $L$ 是一个位象, 如果对 $\forall a, b \in L$, $a \neq b$, 存在 $p\in\mathrm{Hom}_{\mathsf{Frm}}(L,\mathbf{2})$, 使得 $p(a) \neq p(b)$, 则称 $L$ 是一个空间式位象. 所有空间式位象连同位象同态组成的范畴记为 $\mathsf{SLoc}$.

</div>

不妨设 $p(a)=1$, 则称 $p$ 是 $a$ 中的一个点

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

设 $a$ 是位象 $L$ 中的一个元素, 并且 $a\neq \top$, 如果对任意的 $x,y\in L$, $x\wedge y\le a$ 都蕴含 $x\le a$ 或 $y\le a$, 则称 $a$ 是 $L$ 的一个交素元.

$L$ 是一个空间式位象当且仅当 $L$ 中的每一个元素都可以表示为一些交素元的交.

$L$ 是一个空间式位象当且仅当它同构于某个拓扑空间在 $\Omega$ 函子下的像.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

$\mathsf{SLoc}$ 与 $\mathsf{Sob}$ 范畴等价.

</div>

该定理说明, 有一些拓扑空间无法使用无点拓扑描述, 也有一些位象无法使用点集拓扑描述, 而点集拓扑与无点拓扑的交汇点就在于 $\mathsf{Sob}$ 和 $\mathsf{SLoc}$. 而使用无点拓扑的好处在于一些点集拓扑中的定理在无点拓扑中的模拟不依赖选择公理, 于是更受直觉主义数学家的青睐.

$\mathsf{SLoc}$ 有一个称为凝聚位象范畴的子范畴, 一般记为 $\mathsf{CohLoc}$, $\mathsf{Sob}$ 有一个称为凝聚空间范畴的子范畴, 一般记为 $\mathsf{CohTop}$, 则范畴 $\mathsf{DLat}$ 与 $\mathsf{CohLoc}^{op}$ 等价, $\mathsf{Pries}$ 与 $\mathsf{CohTop}$ 等价, 并且 $\mathsf{CohLoc}$ 与 $\mathsf{CohTop}$ 等价, 于是得到普利斯特里对偶定理, $\mathsf{DLat}$ 与 $\mathsf{Pries}^{op}$ 范畴等价.

已知 $\mathsf{BoolAlg}$ 是 $\mathsf{DLat}$ 的子范畴, 而 $\mathsf{Stone}$ 是 $\mathsf{Pries}$ 的子范畴, 限制在这两个子范畴上即可得到斯通表示定理, $\mathsf{BoolAlg}$ 与 $\mathsf{Stone}^{op}$ 范畴等价.

凡是 $\mathsf{Sob}$ 的子范畴与 $\mathsf{SLoc}$ 的子范畴之间的范畴等价定理, 都统称为斯通对偶性. 此处省略了所有技术性细节.

# 伽罗瓦连接

### 伽罗瓦连接

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(伽罗瓦连接)</b>

设 $(P_1,\le_1)$ 和 $(P_2,\le_2)$ 为两个偏序集, 设 $F\colon P_1\rightarrow P_2$ 和 $G\colon P_2\rightarrow P_1$ 为保序映射, 如果对 $\forall a\in P_1$, $b\in P_2$, 有<br>

$$
\displaylines{F(a)\le_2 b\Longleftrightarrow a\le_1 G(b),}
$$<br>

则称 $F$ 和 $G$ 是 $P_1$ 和 $P_2$ 之间的一对的伽罗瓦连接, 称 $F$ 是 $G$ 的左伴随, $G$ 是 $F$ 的右伴随, 可记作 $F\dashv G$.

</div>

若将偏序集看做范畴, 则伽罗瓦连接无非是伴随函子. 也有人将左伴随称为下伴随, 右伴随称为上伴随, 这与序是对应的. 伽罗瓦连接的例子极多, 而最经典的例子由伽罗瓦理论基本定理给出.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

若 $F\colon P_1\rightarrow P_2$ 和 $G\colon P_2\rightarrow P_1$ 为偏序集间保序映射, 则以下条件等价:<br>

1, $F\dashv G$;<br>

2, 对 $\forall a\in P_1$, $b\in P_2$, 有 $a\le_1 G(F(a))$ 且 $F(G(b))\le_2 b$;<br>

3, 对 $\forall b\in P_2$, $G(b)=\max\{ a\in P_1\mid F(a)\le_2 b \}$;<br>

4, 对 $\forall a\in P_1$, $F(a)=\min\{ b\in P_2\mid a\le_1 G(b) \}$.

</div>

这说明一个函数的左或右伴随若存在则唯一, 并且伽罗瓦连接之间可以互相确定. 伽罗瓦连接关于单满性也有很好的对偶性质.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

若 $F\colon P_1\rightarrow P_2$ 和 $G\colon P_2\rightarrow P_1$ 为偏序集间保序映射, $F\dashv G$, 则以下条件等价:<br>

1, $F$ 是单射;<br>

2, $G\circ F$ 是恒等映射;<br>

3, $G$ 是满射.<br>

对偶的, 以下条件也等价:<br>

1, $F$ 是满射;<br>

2, $F\circ G$ 是恒等映射;<br>

3, $G$ 是单射.

</div>

完备格之间的伽罗瓦连接具有更好的结构.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

设 $(L_1,\le_1,\wedge_1,\vee_1)$ 和 $(L_2,\le_2,\wedge_2,\vee_2)$ 都是完备格, $F\colon L_1\rightarrow L_2$ 和 $G\colon L_2\to L_1$ 是保序映射, 则如下条件等价:<br>

1, $F\dashv G$;<br>

2, 对 $\forall S\subseteq L_1$, $F(\bigvee_1 S)=\bigvee_2\{F(s)\mid s\in S\}$;<br>

3, 对 $\forall S\subseteq L_2$, $G(\bigwedge_2 S)=\bigwedge_1\{G(s)\mid s\in S\}$.

</div>

这实际上是伴随函子定理的直接推论.

### DM完备化

已知对 $\forall a\in P_1$, $b\in P_2$, 有 $a\le_1 G(F(a))$ 且 $F(G(b))\le_2 b$, 这立刻得到 $G\circ F\circ G\circ F=G\circ F$ 和 $F\circ G\circ F\circ G=F\circ G$, 于是 $G\circ F$ 实际上给出 $P_1$ 上的一个闭包算子, $F\circ G$ 给出 $P_2$ 上的一个内部算子, 反之闭包算子和内部算子也可以给出伽罗瓦连接, 此处不展开.

利用这种思路, 考虑一个偏序集到自身的一对伽罗瓦连接, 就可以给出该偏序集的一个完备化方法. 称为Dedekind–MacNeille完备化.

设 $P$ 是一个偏序集, $A$ 是其子集, 定义 $A$ 的上集为

$$
\displaylines{u(A)=\{x\in P\mid \forall a\in A, a\le x\},}
$$

下集为

$$
\displaylines{l(A)=\{x\in P\mid \forall a\in A, x\le a\},}
$$

直接验证即可知道, 在 $u\circ l\circ u=u$, $l\circ u\circ l=l$, 我们设 $\mathcal{P}(P)$ 是 $P$ 的幂集, 其上序为包含关系, $\mathcal{P}(P)^{op}$ 表示反序集, 设 $u\colon \mathcal{P}(P)\to\mathcal{P}(P)^{op}$, $l\colon \mathcal{P}(P)^{op}\to\mathcal{P}(P)$, 则有 $u\dashv l$.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(Dedekind–MacNeille完备化)</b>

设 $P$ 是偏序集, 定义

$$
\displaylines{\mathrm{DM}(P)=\{A\subseteq P\mid l(u(A))=A\},}
$$

为 $P$ 的Dedekind–MacNeille完备化.

</div>

有时也称满足 $u(A)=B$, $l(B)=A$ 的集合对为 $P$ 的一个分割.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

符号如上, 则对任意 $x\in P$, 有 $l(\{x\})\in\mathrm{DM}(P)$, 映射 $\iota\colon P\to\mathrm{DM}(P),\iota(x)=l(\{x\})$ 是保序且保一切存在的交和并.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

$(\mathrm{DM}(P),\subseteq)$ 是完备格, 若 $P$ 本身就是完备格, 则有格同构 $\mathrm{DM}(P)\cong P$.

</div>

DM完备化的最基础例子是有理数集 $(\mathbb{Q},\le)$ 的完备化, 为扩展实数集 $\mathbb{R}\cup\{+\infty,-\infty\}$, 其中正负无穷分别对应 $\mathbb{Q}$ 自身和空集 $\emptyset$, 若忽略正负无穷, 就是通常的戴德金分割.

# 收敛理论

### 一致空间

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(邻域系)</b>

设 $(X,\mathcal{T})$ 是拓扑空间, $x\in X$, 设 $x$ 的所有邻域组成的集合为 $\mathfrak{N}_x$, 称为 $x$ 的邻域系.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(开邻域系)</b>

设 $(X,\mathcal{T})$ 是拓扑空间, $x\in X$, 设 $x$ 的所有开邻域组成的集合为 $\mathcal{N}_x$, 称为 $x$ 的开邻域系.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(一致空间)</b>

设 $X$ 是一个集合, 其对角线集为 $\Delta=\{(x,x)\mid x\in X\}$, 设 $\mathcal{U}\in\mathcal{P}(X\times X)$, 如果它满足如下条件:<br>

1, 对任意的 $U \in \mathcal{U}$, 都有 $\Delta \subseteq U$;<br>

2, 若 $U \in \mathcal{U}$ 且 $U \subseteq V \subseteq X \times X$, 则 $V \in \mathcal{U}$;<br>

3, 若 $U \in \mathcal{U}$ 且 $V \in \mathcal{U}$，则 $U \cap V \in \mathcal{U}$;<br>

4, 对于任意 $U \in \mathcal{U}$, 定义其逆 $U^{-1} = \{(y, x) \mid (x, y) \in U\}$, 则有 $U^{-1}\in\mathcal{U}$;<br>

5, 对于任意 $U \in \mathcal{U}$, 存在 $V \in \mathcal{U}$, 使得 $V \circ V \subseteq U$, 其中 $V \circ V = \{(x, z) \in X \times X \mid \exists y \in X, (x, y)\in V , (y, z) \in V\}$ 为 $V$ 和自身的复合,<br>

则称 $\mathcal{U}$ 是 $X$ 上的一个一致结构, 再定义 $U[x] = \{ y \in X \mid (x, y) \in U \}$, $\mathfrak{B}_x=\{U[x]\mid U\in\mathcal{U}\}$, 可以验证它满足邻域公理, 由此定义 $X$ 的子集 $O$ 是开集当且仅当对于其中的任一点 $x \in O$, 都有 $O \in \mathfrak{B}(x)$, 这样得到 $X$ 上的一个拓扑结构, 称为一致拓扑, 称二元组 $(X,\mathcal{U})$ 为一致空间.

</div>

容易验证一致拓扑是良定的. 一致空间的基本想法是使用纯粹的拓扑语言严格化两个元素距离相近这一直观概念, 它是度量空间和拓扑群的共同推广, 首先, 设 $(X, d)$ 为度量空间, 定义 $U_\varepsilon = \{ (x, y) \in X \times X \mid d(x, y) \le \varepsilon \}$, $\mathcal{U} = \{ U \subseteq X \times X \mid \exists \varepsilon > 0, U_\varepsilon \subseteq U \}$ 就是满足要求的一致结构.

其次, 设 $G$ 是拓扑群, $e$ 为单位元, 记 $\mathfrak{N}_e$ 为 $e$ 点的邻域系, 设 $U_V = \{ (x, y) \mid x^{-1}y \in V \}$, 构造左一致结构为 $\mathcal{U} = \{ U \subseteq G \times G \mid \exists V \in \mathcal{N}_e, U_V \subseteq U \}$, 类似可构造右一致结构, 二者未必是相同的, 除非群是交换群.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(一致连续)</b>

设 $f\colon X\to Y$ 是一致空间间的函数, 如果对任意的 $U\in\mathcal{U}_Y$, 都存在 $V\in\mathcal{U}_X$, 使得 $(a,b)\in V$ 总能推出 $(f(a),f(b))\in U$, 则称 $f$ 是一致连续的.

</div>

一致连续函数显然是连续的.

收敛理论可以从一致空间推广到更一般的情况, 如柯西空间, 收敛空间.

### 网

回忆有向集就是滤过的偏序集.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(网)</b>

设 $I$ 是一个有向集, $X$ 是一个非空集合, 称从 $I$ 到 $X$ 的映射 $x\colon I\to X$ 为网, 常记为 $x_i$ 或 $\{x_i\}_{i\in I}$.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(最终在)</b>

符号如上, 设 $A\subseteq X$, 如果存在 $i_0\in I$, 使得只要 $i_0\le i$, 总能推出 $x_i\in A$, 则称网 $x$ 最终在 $A$ 中.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(超网)</b>

设 $x\colon I\to X$ 是网, 如果对 $X$ 的每个子集 $A$, 该网都最终在 $A$ 中或最终在其补集 $X-A$ 中, 则称 $x$ 是一个超网.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(收敛)</b>

设 $X$ 是非空的拓扑空间, $x\colon I\to X$ 为网, 若存在 $a\in X$, 使得对 $a$ 的任意邻域 $U\in \mathfrak{N}_a$, 网 $x$ 都最终在 $U$ 中, 则称网 $x$ 收敛到 $a$, 记为 $\lim_{i\in I}x_i=a$

</div>

收敛网未必只收敛到一个点, 但如果空间是豪斯多夫的, 则若收敛则一定收敛到唯一点.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(柯西网)</b>

设 $I$ 是有向集, $(X,\mathcal{U})$ 是一致空间, $x\colon I\to X$ 是网, 如果对任意 $U\in\mathcal{U}$, 都存在 $i\in I$, 使得对任意 $j,k\in I$, $i\le j$ 且 $i\le k$ 都能推出 $(x_j,x_k)\in U$, 则称 $x$ 是一个柯西网.

</div>

收敛的网一定是柯西网, 柯西网未必收敛. 柯西网均收敛的一致空间称为完备空间, 使用柯西网可给出一致空间的完备化, 但该过程不如滤子方法简便, 二者的等价性后续叙述.

现给出一个例子, 给定区间 $[a,b]\subseteq\mathbb{R}$ 和其上的函数 $f$, 设 $P$ 由该区间的所有黎曼分拆组成, 按分拆里的最大区间长度大小给出 $P$ 上的一个偏序, 它是滤过的, 因此是有向集. 给定每个黎曼分拆, 黎曼和 $D\mapsto\sum_{x_i\in D} f(x_i)\Delta_i$ 给出一个从 $P$ 到 $\mathbb{R}$ 的网, 该网收敛当且仅当 $f$ 在该区间上黎曼可积, 这便是黎曼积分的严格定义.

### 滤子

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(滤子基)</b>

设 $X$ 是一个非空集合, 如果非空集族 $\mathfrak{B}\subseteq\mathcal{P}(X)$ 满足如下条件:

1, $\emptyset\notin\mathfrak{B}$;

2, 若 $A, B \in \mathfrak{B}$, 则存在 $C \in \mathfrak{B}$ 使得 $C \subseteq A \cap B$,

则称 $\mathfrak{B}$ 是 $X$ 的一个滤子基.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(滤子)</b>

设 $X$ 是一个非空集合, 如果非空集族 $\mathfrak{F}\subseteq\mathcal{P}(X)$ 满足如下条件:

1, $\emptyset\notin\mathfrak{F}$;

2, 若 $A, B \in \mathfrak{F}$, 则 $A \cap B\in\mathfrak{F}$;

3, 若 $A\in \mathfrak{F}$, 并且 $A\subseteq B\subseteq X$, 则 $B\in\mathfrak{F}$,

则称 $\mathfrak{F}$ 是 $X$ 的一个滤子.

</div>

滤子基自然能生成滤子, 对于滤子基 $\mathfrak{B}$, 只需定义 $\mathfrak{F}=\{F\subseteq X\mid \exists B\in\mathfrak{B},B\subseteq F\}$ 为 $\mathfrak{B}$ 生成的滤子, 对应的称 $\mathfrak{B}$ 为 $\mathfrak{F}$ 的基.

作为例子, 设 $X$ 是拓扑空间, 对任意 $x\in X$, 邻域系 $\mathfrak{N}_x$ 就是 $X$ 上的一个滤子.

集合的滤子无非是其幂集格上的滤子, 于是也有超滤子和素滤子的概念, 由于幂集一定是布尔格, 于是集合的超滤子和素滤子是等价的.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(收敛)</b>

设 $\mathfrak{F}$ 是拓扑空间 $X$ 上的一个滤子, 如果存在 $x\in X$, 使得 $\mathfrak{N}_x\subseteq\mathfrak{F}$, 则称滤子 $\mathfrak{F}$ 收敛到 $x$, 记为 $\lim \mathfrak{F}=x$ 或 $\mathfrak{F}\to x$.

</div>

收敛滤子只收敛到唯一一点当且仅当空间是豪斯多夫的.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(柯西滤子)</b>

设 $(X,\mathcal{U})$ 是一个一致空间, $\mathfrak{F}$ 是 $X$ 上的一个滤子, 如果对任意 $U\in\mathcal{U}$, 都存在 $F\in\mathfrak{F}$, 使得 $F\times F\subseteq U$, 则称 $\mathfrak{F}$ 是柯西滤子.

</div>

容易验证收敛滤子一定是柯西滤子.

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(完备空间)</b>

如果一致空间中的所有柯西滤子均收敛, 则称该空间是完备的.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

设 $X$ 是一个一致空间, 则存在一个完备的豪斯多夫一致空间 $\hat{X}$ 和一致连续映射 $i\colon X\to\hat{X}$ 满足如下泛性质, 对于任何完备的豪斯多夫一致空间 $Y$ 以及任何一致连续映射 $f\colon X \to Y$, 存在唯一的一致连续映射 $\hat{f}\colon \hat{X} \to Y$, 使得$f=\hat{f}\cric i$.

</div>

该定理中的 $\hat{X}$ 称为完备化, 其大致构造流程是, 可以证明对于任一柯西滤子, 都存在包含关系下的极小柯西滤子, 所有极小柯西滤子组成的集合记为 $\hat{X}$, 由于邻域系 $\mathfrak{N}_x$ 一定是极小柯西滤子, 于是 $i(x)$ 就定义为 $\mathfrak{N}_x$, 由于 $X$ 未必豪斯多夫, 该映射未必是单射, 但若 $X$ 豪斯多夫则 $i$ 必单. $i(X)$ 在 $\hat{X}$ 中一定是稠密的. 在 $\hat{X}$ 上定义一致结构以及具体性质的验证见相关文献, 此处不展开.

### 网与滤子

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(导出网)</b>

设 $X$ 是非空集合, $\mathfrak{F}$ 是其上的一个滤子, 定义 $D=\{(a,A)\mid a\in A\in\mathfrak{F}\}$, 在 $D$ 上定义序关系 $(a, A) \le (b, B) \iff B \subseteq A$, 这使得 $D$ 成为一个有向集, 定义 $x\colon D \to X,(a,A)\mapsto a$ 称为 $\mathfrak{F}$ 的导出网.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定义(导出滤子)</b>

设 $I$ 是有向集, $X$ 是非空集合, $x\colon I\to X$ 是网, 定义 $x$ 的导出滤子为 $\mathfrak{F}=\{F\mid x \text{ 最终在 }F\text{ 中 }\}$.

</div><br>

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

任意滤子的导出网的导出滤子仍是该滤子.

</div>

该定理说明, 任何滤子都是某个网的导出滤子, 而未必所有网都是某个滤子的导出网, 所以直观而言网是比滤子更多的, 二者在各类实践中各有优势, 而以下定理表明二者在收敛性上本质是等价的.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

设 $X$ 是非空拓扑空间, 则其上的一个网收敛当且仅当其导出滤子收敛, 其上的一个滤子收敛当且仅当其导出网收敛.

</div>

### 范畴极限

设 $X$ 上的所有滤子组成的集合为 $\mathsf{Fil}$, 它关于包含关系构成一个偏序集, 于是也构成范畴, 对于 $X$ 上的一个滤子 $\mathfrak{F}$, $\forall x\in X$, 定义 $\mathsf{Fil}_x$ 为所有包含 $\mathfrak{F}\cap\mathfrak{N}_x$ 的滤子组成的集合, 它关于包含关系也构成偏序集, 它是 $\mathsf{Fil}$ 的全子范畴, 于是有包含函子 $\iota\colon \mathsf{Fil}_x\to\mathsf{Fil}$.

<div style="border: 3px solid #000; padding: 10px;">

<b>定理</b>

符号如上, 滤子 $\mathfrak{F}$ 收敛到 $x$ 当且仅当函子 $\iota$ 的极限为 $\mathfrak{F}$.

</div>

<div style="border: 3px solid #000; padding: 10px;">

<b>证明</b>

$\lim \mathcal{F} = x \iff \mathfrak{N}_x \subset \mathcal{F} \iff \mathcal{F} \cup \mathfrak{N}_x = \mathcal{F} \iff \mathcal{F} = \bigcap_{\mathfrak{G} \in \mathsf{Fil}_x} \iota(\mathfrak{G}) \iff \varprojlim \iota = \mathcal{F}.$

</div>

这可能是范畴极限叫该名称的原因.

# 参考文献

姚卫, 路玲霞. 序与格论基础[M]. 北京: 清华大学出版社, 2023. ISBN: 9787302643418.

Davey, B. A., & Priestley, H. A. Introduction to Lattices and Order (2nd ed.)[M]. Cambridge: Cambridge University Press, 2002.

Bourbaki, N. General Topology: Chapters 1–4[M]. Berlin Heidelberg: Springer-Verlag, 1995. (Elements of Mathematics). ISBN: 978-3-540-64241-1. (Translated from the French).

Gierz, G., Hofmann, K. H., Keimel, K., Lawson, J. D., Mislove, M. W., & Scott, D. S. Continuous Lattices and Domains[M]. Cambridge: Cambridge University Press, 2003.
