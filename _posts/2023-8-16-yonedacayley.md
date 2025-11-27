---
layout: post
title: "Yoneda 引理证明 Cayley 定理"
subtitle: ""
header-img: "img/post-bg-infinity.jpg"
header-mask: 0.3
math: true
tags:
  - 范畴论
  - 代数
---

Cayley定理是说:

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>

任意一个群 $ G $, 都同构于置换群 $ S_n $ 的子群, 其中 $ n=\left|G\right| $.
</div>

而Yoneda引理则是范畴论中一个结论, 下面我们将会看到, Yoneda引理可以看作Cayley定理的推广.

我们用大写字母 $ C $ 表示范畴,  $ \mathrm{Ob}(C) $ 表示 $ C $ 的所有对象组成的类,  $ \mathrm{Mor}(C) $ 表示 $ C $ 中的所有态射组成的类. 若 $ A,B\in \mathrm{Ob}(C) $, 则用 $ \mathrm{Hom}_C(A,B) $ 表示从 $ A $ 到 $ B $ 的所有态射组成的类. 若 $ F $ 和 $ G $ 都是从范畴 $ C $ 到范畴 $ C' $ 的函子, 则用 $ \mathrm{Nat}(F,G) $ 表示从函子 $ F $ 到函子 $ G $ 的所有自然变换组成的类.

Yoneda引理是说:

<div style="border: 3px solid #000; padding: 10px;">
<b>定理(Yoneda引理)</b>

对于 $ S, T\in \mathrm{Ob}(C) $, 有

$$
\displaylines{\mathrm{Nat}(\mathrm{Hom}_C(-,S),\mathrm{Hom}_C(-,T)) \cong \mathrm{Hom}_C(S,T).}
$$
</div>

Yoneda引理证明Cayley定理的关键是, 将每一个群看做只有一个对象的群胚, 其中群胚(或广群)的定义是所有态射均可逆的范畴. 对于群胚 $ C $, 若设 $ \mathrm{Ob}(C)=\{\mathrm1\} $, 则 $ \mathrm{Mor}(C) $ 中的元素都是从 $ \mathrm{1} $ 到自身的态射,  $ \mathrm{Mor}(C) $ 关于态射的复合构成一个群. 对于任意一个群 $ G $, 都可以找到一个只有一个对象的群胚 $ C $, 使得 $ G\cong \mathrm{Mor}(C). $ 

<div style="border: 3px solid #000; padding: 10px;">
<b>定理</b>

Yoneda引理 $ \Longrightarrow $ Cayley定理.
</div>

<div style="border: 3px solid #000; padding: 10px;">
<b>证明</b>

设范畴 $ C $ 是只有一个对象的群胚, 使得 $ G\cong \mathrm{Mor}(C). $ 

设 $ \mathrm{Ob}(C)=\{\mathrm1\} $, 那么由Yoneda引理即得

$$
\displaylines{\mathrm{Nat}(\mathrm{Hom}_C(-,\mathrm{1}),\mathrm{Hom}_C(-,\mathrm{1})) \cong \mathrm{Hom}_C(\mathrm{1},\mathrm{1})=\mathrm{Mor}(C)\cong G.}
$$

给定 $ \varphi\in\mathrm{Nat}(\mathrm{Hom}_C(-,\mathrm{1}),\mathrm{Hom}_C(-,\mathrm{1})) $ 是一个自然变换, 这个自然变换由态射

$$
\displaylines{\varphi_{\mathrm{1}}:\mathrm{Hom}_C(\mathrm{1},\mathrm{1})\rightarrow\mathrm{Hom}_C(\mathrm{1},\mathrm{1}).}
$$

确定.因为 $ \mathrm{Hom}_C(\mathrm{1},\mathrm{1})\cong G $, 所以 $ \varphi_{\mathrm{1}} $ 是群 $ G $ 到自身的一个置换.

于是 $ \mathrm{Nat}(\mathrm{Hom}_C(-,\mathrm{1}),\mathrm{Hom}_C(-,\mathrm{1}))  $ 同构于 $ G $ 上的置换群的一个子群, 所以 $ G $ 也同构于 $ G $ 上的置换群的一个子群. 若 $ \left|G\right|=n $, 则 $ G $ 同构于置换群 $ S_n $ 的子群.
</div>
