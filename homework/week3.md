# 作业 3

> **定义 4.1.1** (集合代数)<br>设 $X$ 是非空集合, $\mathcal A\subset\mathcal P\left(X\right)$. 称 $\mathcal A$ 为 $X$ 上的一个**集合代数**, 若满足:<br>(1) $X\in\mathcal A$;<br>(2) 对差运算封闭: $A,B\in\mathcal A\Rightarrow A\setminus B\in\mathcal A$;<br>(3) 对有限并封闭: $A,B\in\mathcal A\Rightarrow A\cup B\in\mathcal A$.

> **定义 4.1.3** ($\sigma$-代数)<br>设 $X$ 非空, $\mathcal F\subset\mathcal P\left(X\right)$. 称 $\mathcal F$ 为 $X$ 上的一个 **$\sigma$-代数**, 若满足:<br>(1) $X\in\mathcal F$;<br>(2) 对补运算封闭: $A\in\mathcal F\Rightarrow A^{c}\in\mathcal F$;<br>(3) 对可数并封闭: $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal F\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal F$.

> **定义 4.4.1** (单调类)<br>设 $\mathcal M\subset\mathcal P\left(X\right)$. 称 $\mathcal M$ 为**单调类**, 若满足:<br>(1) 对单调递增序列封闭: $A_{1}\subset A_{2}\subset\cdots$ 且 $A_{n}\in\mathcal M\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal M$;<br>(2) 对单调递减序列封闭: $A_{1}\supset A_{2}\supset\cdots$ 且 $A_{n}\in\mathcal M\Rightarrow\bigcap_{n=1}^{\infty}A_{n}\in\mathcal M$.

> **定理 4.4.2** (单调类定理)<br>设 $\mathcal A$ 是一个代数, $\mathcal M$ 是一个包含 $\mathcal A$ 的单调类, 则 $\sigma\left(\mathcal A\right)\subset\mathcal M$.

> **定义 5.1.2** (测度)<br>设 $\left(X,\mathcal F\right)$ 是可测空间. 函数 $\mu:\mathcal F\to\left[0,+\infty\right]$ 称为 $\left(X,\mathcal F\right)$ 上的一个测度, 若满足:<br>(1) 非负性: $\mu\left(E\right)\ge0$ 对一切 $E\in\mathcal F$;<br>(2) 零空集性: $\mu\left(\varnothing\right)=0$;<br>(3) 可数可加性: 对任意可数个两两不交的 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$, 有 $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **命题 5.2.1** (有限可加性)<br>设 $\mu$ 是测度, $E_{1},\dots,E_{n}\in\mathcal F$ 两两不交, 则 $\mu\left(\bigcup_{k=1}^{n}E_{k}\right)=\sum_{k=1}^{n}\mu\left(E_{k}\right)$.

> **命题 5.2.3** (次可数可加性)<br>设 $\mu$ 是测度, $\left\{E_{n}\right\}_{n=1}^{\infty}$ 任意, 则 $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)\le\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **命题 5.2.4** (下连续性)<br>设 $\mu$ 是测度, $\left\{E_{n}\right\}$ 单调递增, 则 $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\lim_{n\to\infty}\mu\left(E_{n}\right)$.

> **定义 6.1.1** (外测度)<br>设 $X$ 非空. 函数 $\mu^{*}:\mathcal P\left(X\right)\to\left[0,+\infty\right]$ 称为 $X$ 上的一个**外测度**, 若满足:<br>(1) 非负性: $\mu^{*}\left(\varnothing\right)=0$, 且 $\mu^{*}\left(E\right)\ge0$ 对一切 $E\subset X$;<br>(2) 单调性: $E\subset F\Rightarrow\mu^{*}\left(E\right)\le\mu^{*}\left(F\right)$;<br>(3) 次可数可加性: $\mu^{*}\left(\bigcup_{n=1}^{\infty}E_{n}\right)\le\sum_{n=1}^{\infty}\mu^{*}\left(E_{n}\right)$.

> **定义 6.2.1** (准测度)<br>设 $X$ 非空, $\mathcal E\subset\mathcal P\left(X\right)$ 是一个代数. 函数 $\mu_{0}:\mathcal E\to\left[0,+\infty\right]$ 称为一个**准测度**, 若:<br>(1) $\mu_{0}\left(\varnothing\right)=0$;<br>(2) 若 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal E$ 两两不交且 $\bigcup_{n=1}^{\infty}E_{n}\in\mathcal E$, 则 $\mu_{0}\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu_{0}\left(E_{n}\right)$.

> **定理 6.2.2** (由准测度生成外测度)<br>设 $\mathcal E\subset\mathcal P\left(X\right)$ 是一个覆盖类, $\mu_{0}:\mathcal E\to\left[0,+\infty\right]$ 是一个准测度. 对任意 $A\subset X$, 定义 $$\mu^{*}\left(A\right)=\inf\left\{\sum_{n=1}^{\infty}\mu_{0}\left(E_{n}\right):E_{n}\in\mathcal E,A\subset\bigcup_{n=1}^{\infty}E_{n}\right\}.$$ 则 $\mu^{*}$ 是 $X$ 上的外测度, 且 $\mu^{*}|_{\mathcal E}=\mu_{0}$.

> **定义 6.3.1** (卡拉西奥多里条件)<br>设 $\mu^{*}$ 是 $X$ 上的外测度. 子集 $A\subset X$ 称为 $\mu^{*}$-**可测**的, 若对任意 $T\subset X$ 有 $$\mu^{*}\left(T\right)=\mu^{*}\left(T\cap A\right)+\mu^{*}\left(T\cap A^{c}\right).$$ 所有 $\mu^{*}$-可测集组成的集合记为 $\mathcal M_{\mu^{*}}$.

> **引理 6.3.2**<br>如果 $\mathcal E$ 是代数, $\mu_{0}$ 是准测度, 则 $\mathcal E\subset\mathcal M_{\mu^{*}}$.

> **定理 6.3.3** (卡拉西奥多里定理)<br>设 $\mu^{*}$ 是 $X$ 上的外测度, 则:<br>(1) $\mathcal M$ 是一个 $\sigma$-代数;<br>(2) $\mu^{*}|_{\mathcal M}$ 是一个完备测度;<br>(3) 如果 $\mu^{*}$ 是由准测度 $\mu_{0}$ 生成的, 且 $\mu_{0}$ 是 $\sigma$-有限的, 则 $\mu^{*}|_{\mathcal M}$ 是 $\mu_{0}$ 的唯一延拓.

> **定义 6.4.1** (h 区间)<br>令 $-\infty\le a<b<\infty$, 所有左开右闭区间 $\left(a,b\right]$, 以及 $\left(a,\infty\right)$, $\varnothing$ 称为 **h 区间**. h 区间的有限不交并形成的集族 $\mathcal E$ 为一个代数.

> **命题 6.4.2** ($\mathcal E$ 上的准测度)<br>设 $F:\mathbb R\to\mathbb R$ 为增的右连续函数. 对于不交区间 $\left(a_{i},b_{i}\right]$, $i=1,\dots,n$, 定义 $\mu_{0}\left(\bigcup_{i=1}^{n}\left(a_{i},b_{i}\right]\right):=\sum_{i=1}^{n}\left[F\left(b_{i}\right)-F\left(a_{i}\right)\right]$, 并令 $\mu_{0}\left(\varnothing\right)=0$. 则 $\mu_{0}$ 为 $\mathcal E$ 上的准测度.

> **定理 6.4.5** (勒贝格-斯蒂尔杰斯测度的正则性)<br>设 $F:\mathbb R\to\mathbb R$ 是右连续单调递增函数, $\mu_{F}$ 是由 $F$ 生成的勒贝格-斯蒂尔杰斯测度, $\mathcal M^{*}$ 是 $\mu_{F}$-可测集的 $\sigma$-代数. 若 $E\in\mathcal M^{*}$, 则 $$\begin{aligned}&\quad\;\mu_{F}\left(E\right)\\&=\inf\left\{\mu_{F}\left(U\right):E\subset U,U\text{开}\right\}\\&=\sup\left\{\mu_{F}\left(K\right):K\subset E,K\text{紧}\right\}.\end{aligned}$$

> **定义 6.4.6** (勒贝格测度)<br>由 $F\left(x\right)=x$ 生成的测度称为**勒贝格测度**, 记作 $m$; 相应外测度定义的可测集称为**勒贝格可测集**, 全体记作 $\mathcal L$.

> **定义 6.5.1** (康托尔集的递归构造)<br>设 $C_{0}=\left[0,1\right]$. 对每个 $n\ge0$, 定义 $C_{n+1}=\frac{1}{3}C_{n}\cup\left(\frac{2}{3}+\frac{1}{3}C_{n}\right)$. 则**康托尔集**定义为 $C=\bigcap_{n=0}^{\infty}C_{n}$.

> **定理 6.5.2** (康托尔集的三进制刻画)<br>点 $x\in\left[0,1\right]$ 属于康托尔集 $C$ 当且仅当它的三进制展开 $x=\sum_{k=1}^{\infty}\frac{a_{k}}{3^{k}}$ 中不含数字 $1$ (即 $a_{k}\in\left\{0,2\right\}$).

> **基础知识**<br>**广义康托尔集**: 设 $\left\{\alpha_{j}\right\}\subset\left(0,1\right)$, 从 $\left[0,1\right]$ 出发, 第 $j$ 步去掉每个剩余闭区间的中间 $\alpha_{j}$ 部分, 所得交集 $K=\bigcap_{j}K_{j}$ 称为广义康托尔集. 它满足 $m\left(K\right)=\prod_{j=1}^{\infty}\left(1-\alpha_{j}\right)$, 且对任意 $\beta\in\left(0,1\right)$ 可选取 $\left\{\alpha_{j}\right\}$ 使 $m\left(K\right)=\beta$; 广义康托尔集与普通康托尔集一样是紧、无处稠密、无孤立点的闭集.

### 习题一

证明**定理 6.3.3** 第 (3) 条的唯一性, 并证明习题 17、24.

(1) 设 $\mathcal E\subset\mathcal P\left(X\right)$ 是代数, $\mu_{0}$ 是 $\mathcal E$ 上 $\sigma$-有限的准测度, $\mu^{*}$ 是由 $\mu_{0}$ 生成的外测度, $\mathcal M$ 是 $\mu^{*}$-可测集全体. 证明 $\mu^{*}|_{\mathcal M}$ 是 $\mu_{0}$ 到 $\mathcal M$ 的唯一延拓.

**17.** 设 $\mu^{*}$ 是 $X$ 上的外测度, $\left\{A_{j}\right\}_{j=1}^{\infty}$ 是一列两两不交的 $\mu^{*}$-可测集. 证明对任意 $E\subset X$, 有

$$
\mu^{*}\left(E\cap\bigcup_{j=1}^{\infty}A_{j}\right)=\sum_{j=1}^{\infty}\mu^{*}\left(E\cap A_{j}\right).
$$

**24.** 设 $\mu$ 是 $\left(X,\mathcal M\right)$ 上的有限测度, $\mu^{*}$ 是由 $\mu$ 诱导的外测度. 设 $E\subset X$ 满足 $\mu^{*}\left(E\right)=\mu^{*}\left(X\right)$ (但 $E$ 未必属于 $\mathcal M$).

(a) 若 $A,B\in\mathcal M$ 且 $A\cap E=B\cap E$, 则 $\mu\left(A\right)=\mu\left(B\right)$.

(b) 记 $\mathcal M_{E}=\left\{A\cap E:A\in\mathcal M\right\}$, 在 $\mathcal M_{E}$ 上定义 $\nu\left(A\cap E\right)=\mu\left(A\right)$ (由 (a) 良定义). 证明 $\mathcal M_{E}$ 是 $E$ 上的 $\sigma$-代数, 且 $\nu$ 是 $\mathcal M_{E}$ 上的测度.

### 解答 习题一

**(1) 唯一性.** 由**定义 6.2.1**, $\mu_{0}$ 是代数 $\mathcal E$ 上的准测度. 先证 $\mu^{*}|_{\mathcal M}$ 确是 $\mu_{0}$ 的延拓: 由**定理 6.2.2**, $\mu^{*}|_{\mathcal E}=\mu_{0}$; 由**引理 6.3.2**, $\mathcal E\subset\mathcal M$; 由**定理 6.3.3**(1)(2), $\mathcal M$ 是 $\sigma$-代数且 $\mu^{*}|_{\mathcal M}$ 是完备测度. 故 $\mu^{*}|_{\mathcal M}$ 是 $\mu_{0}$ 到 $\mathcal M$ 的测度延拓.

再证唯一性. 设 $\nu$ 是 $\mathcal M$ 上任一满足 $\nu|_{\mathcal E}=\mu_{0}$ 的测度, 我们证明 $\nu=\mu^{*}|_{\mathcal M}$. 先设 $\mu_{0}\left(X\right)<\infty$.

**步骤 1: $\nu\le\mu^{*}$ 在 $\mathcal M$ 上.** 对任意 $A\in\mathcal M$ 和 $\varepsilon>0$, 由**定理 6.2.2** 中 $\mu^{*}$ 的定义, 存在 $\left\{E_{n}\right\}\subset\mathcal E$ 覆盖 $A$ 使 $\sum_{n}\mu_{0}\left(E_{n}\right)\le\mu^{*}\left(A\right)+\varepsilon$. 由 $\nu$ 的次可数可加性 (**命题 5.2.3**) 及 $\nu|_{\mathcal E}=\mu_{0}$,

$$
\nu\left(A\right)\le\sum_{n}\nu\left(E_{n}\right)=\sum_{n}\mu_{0}\left(E_{n}\right)\le\mu^{*}\left(A\right)+\varepsilon.
$$

由 $\varepsilon$ 的任意性, $\nu\left(A\right)\le\mu^{*}\left(A\right)$.

**步骤 2: $\nu=\mu^{*}$ 在 $\sigma\left(\mathcal E\right)$ 上.** 令 $\mathcal H=\left\{A\in\sigma\left(\mathcal E\right):\nu\left(A\right)=\mu^{*}\left(A\right)\right\}$. 对 $E\in\mathcal E$, 由**定理 6.2.2** 与 $\nu|_{\mathcal E}=\mu_{0}$ 得 $\mu^{*}\left(E\right)=\mu_{0}\left(E\right)=\nu\left(E\right)$, 故 $\mathcal E\subset\mathcal H$. 验证 $\mathcal H$ 是单调类 (**定义 4.4.1**): 若 $\left\{A_{n}\right\}\subset\mathcal H$ 且 $A_{n}\uparrow A$, 由 $\nu,\mu^{*}|_{\mathcal M}$ 的下连续性 (**命题 5.2.4**; $\sigma\left(\mathcal E\right)\subset\mathcal M$) 得 $\nu\left(A\right)=\lim_{n}\nu\left(A_{n}\right)=\lim_{n}\mu^{*}\left(A_{n}\right)=\mu^{*}\left(A\right)$, 故 $A\in\mathcal H$; 递减情形同理 (此处 $\mu^{*}\left(A_{1}\right)\le\mu^{*}\left(X\right)=\mu_{0}\left(X\right)<\infty$, 上连续性可用). 故 $\mathcal H$ 是包含代数 $\mathcal E$ 的单调类, 由**定理 4.4.2** (单调类定理), $\sigma\left(\mathcal E\right)\subset\mathcal H$, 即 $\nu=\mu^{*}$ 在 $\sigma\left(\mathcal E\right)$ 上.

**步骤 3: $\nu=\mu^{*}$ 在 $\mathcal M$ 上.** 对任意 $A\in\mathcal M$, 由步骤 1 得 $\nu\left(A\right)\le\mu^{*}\left(A\right)$. 又因 $X\in\mathcal E$ (**定义 4.1.1**), $\nu\left(X\right)=\mu_{0}\left(X\right)=\mu^{*}\left(X\right)$. 由步骤 1 作用于 $A^{c}\in\mathcal M$ (因 $\mathcal M$ 是 $\sigma$-代数, **定理 6.3.3**(1)), 以及 $A\in\mathcal M$ 给出 $\mu^{*}\left(X\right)=\mu^{*}\left(A\right)+\mu^{*}\left(A^{c}\right)$ (卡拉西奥多里条件于 $T=X$),

$$
\begin{aligned}
&\quad\;\nu\left(A\right)\\&=\nu\left(X\right)-\nu\left(A^{c}\right)\\&=\mu^{*}\left(X\right)-\nu\left(A^{c}\right)\\&\ge\mu^{*}\left(X\right)-\mu^{*}\left(A^{c}\right)\\&=\mu^{*}\left(A\right).
\end{aligned}
$$

故 $\nu\left(A\right)=\mu^{*}\left(A\right)$. 于是 $\mu_{0}\left(X\right)<\infty$ 时唯一性得证.

**$\sigma$-有限情形.** 设 $\mu_{0}$ 是 $\sigma$-有限的, 即存在两两不交的 $X_{k}\in\mathcal E$ 使 $X=\bigcup_{k=1}^{\infty}X_{k}$ 且 $\mu_{0}\left(X_{k}\right)<\infty$. 对任意 $A\in\mathcal M$, 由可数可加性与下连续性,

$$
\begin{aligned}
\mu^{*}\left(A\right)&=\sum_{k}\mu^{*}\left(A\cap X_{k}\right),\\\nu\left(A\right)&=\sum_{k}\nu\left(A\cap X_{k}\right).
\end{aligned}
$$

对每个 $k$, 把有限测度 $\mu_{0}\left(\cdot\cap X_{k}\right)$ 与 $\nu\left(\cdot\cap X_{k}\right)$ 限制在 $X_{k}$ 上即化为有限情形, 得 $\nu\left(A\cap X_{k}\right)=\mu^{*}\left(A\cap X_{k}\right)$. 求和得 $\nu\left(A\right)=\mu^{*}\left(A\right)$. 故 $\mu^{*}|_{\mathcal M}$ 是 $\mu_{0}$ 到 $\mathcal M$ 的唯一延拓. $\blacksquare$

**(2) 习题 17.** 一方面, 由**定义 6.1.1**(3) (次可数可加性),

$$
\mu^{*}\left(E\cap\bigcup_{j=1}^{\infty}A_{j}\right)\le\sum_{j=1}^{\infty}\mu^{*}\left(E\cap A_{j}\right).
$$

另一方面, 由每个 $A_{j}$ 可测 (**定义 6.3.1**), 对任意 $T\subset X$ 与任意 $N$, 归纳地使用卡拉西奥多里条件于 $T$ 得

$$
\mu^{*}\left(T\right)=\sum_{j=1}^{N}\mu^{*}\left(T\cap A_{j}\right)+\mu^{*}\left(T\cap\left(\bigcup_{j=1}^{N}A_{j}\right)^{c}\right).
$$

取 $T=E\cap\bigcup_{j=1}^{\infty}A_{j}$, 则 $T\cap A_{j}=E\cap A_{j}$, 且 $T\cap\left(\bigcup_{j=1}^{N}A_{j}\right)^{c}=E\cap\bigcup_{j=N+1}^{\infty}A_{j}$. 故

$$
\mu^{*}\left(E\cap\bigcup_{j=1}^{\infty}A_{j}\right)=\sum_{j=1}^{N}\mu^{*}\left(E\cap A_{j}\right)+\mu^{*}\left(E\cap\bigcup_{j=N+1}^{\infty}A_{j}\right)\ge\sum_{j=1}^{N}\mu^{*}\left(E\cap A_{j}\right).
$$

令 $N\to\infty$ 得 $\mu^{*}\left(E\cap\bigcup_{j=1}^{\infty}A_{j}\right)\ge\sum_{j=1}^{\infty}\mu^{*}\left(E\cap A_{j}\right)$. 合并即得等式. $\blacksquare$

**(3) 习题 24.** (a) 由 $A\cap E=B\cap E$ 得 $\left(A\setminus B\right)\cap E=\varnothing$, 且 $A\setminus B\in\mathcal M$. 因 $A\setminus B$ 可测, 用卡拉西奥多里条件于 $T=X$:

$$
\begin{aligned}
&\quad\;\mu^{*}\left(X\right)\\&=\mu^{*}\left(X\cap\left(A\setminus B\right)\right)+\mu^{*}\left(X\cap\left(A\setminus B\right)^{c}\right)\\&=\mu\left(A\setminus B\right)+\mu^{*}\left(X\setminus\left(A\setminus B\right)\right).
\end{aligned}
$$

由 $\left(A\setminus B\right)\cap E=\varnothing$ 得 $E\subset X\setminus\left(A\setminus B\right)$, 据外测度单调性 (**定义 6.1.1**(2)) 有 $\mu^{*}\left(X\setminus\left(A\setminus B\right)\right)\ge\mu^{*}\left(E\right)=\mu^{*}\left(X\right)$. 代入上式得 $\mu\left(A\setminus B\right)\le0$, 故 $\mu\left(A\setminus B\right)=0$. 同理 $\mu\left(B\setminus A\right)=0$. 于是由**命题 5.2.1** (有限可加性),

$$
\begin{aligned}
&\quad\;\mu\left(A\right)\\&=\mu\left(A\cap B\right)+\mu\left(A\setminus B\right)\\&=\mu\left(A\cap B\right)\\&=\mu\left(B\right).
\end{aligned}
$$

$\blacksquare$

(b) 先证 $\nu$ 良定义: 若 $A\cap E=B\cap E$, 由 (a) 得 $\mu\left(A\right)=\mu\left(B\right)$, 故 $\nu$ 不依赖于代表元.

再证 $\mathcal M_{E}$ 是 $E$ 上的 $\sigma$-代数 (**定义 4.1.3**): 因 $E=X\cap E\in\mathcal M_{E}$; 对 $A\cap E\in\mathcal M_{E}$, 其在 $E$ 内的补为 $E\setminus\left(A\cap E\right)=\left(X\setminus A\right)\cap E\in\mathcal M_{E}$; 且 $\bigcup_{n}\left(A_{n}\cap E\right)=\left(\bigcup_{n}A_{n}\right)\cap E\in\mathcal M_{E}$. 故 $\mathcal M_{E}$ 是 $E$ 上的 $\sigma$-代数.

最后证 $\nu$ 是 $\mathcal M_{E}$ 上的测度 (**定义 5.1.2**). 非负性由 $\mu\ge0$; $\nu\left(\varnothing\right)=\mu\left(\varnothing\right)=0$. 设 $\left\{A_{n}\cap E\right\}$ 两两不交. 则对 $n\ne m$, $\left(A_{n}\cap A_{m}\right)\cap E=\left(A_{n}\cap E\right)\cap\left(A_{m}\cap E\right)=\varnothing$, 由 (a) 得 $\mu\left(A_{n}\cap A_{m}\right)=0$. 于是由**命题 5.2.1** 与**命题 5.2.4** (下连续性),

$$
\begin{aligned}
&\quad\;\nu\left(\bigcup_{n}\left(A_{n}\cap E\right)\right)\\&=\nu\left(\left(\bigcup_{n}A_{n}\right)\cap E\right)\\&=\mu\left(\bigcup_{n}A_{n}\right)\\&=\sum_{n}\mu\left(A_{n}\right)\\&=\sum_{n}\nu\left(A_{n}\cap E\right).
\end{aligned}
$$

故 $\nu$ 是测度. $\blacksquare$

### 习题二

设 $-\infty\le a<b<\infty$, 所有左开右闭区间 $\left(a,b\right]$ 以及 $\left(a,\infty\right)$, $\varnothing$ 称为 h 区间. 证明 h 区间的有限不交并形成的集族 $\mathcal E$ 是一个代数 (**定义 6.4.1**).

### 解答 习题二

用**定义 4.1.1** (集合代数) 验证.

先证两个 h 区间的交仍是 h 区间. 事实上, $\left(a,b\right]\cap\left(c,d\right]=\left(\max\left(a,c\right),\min\left(b,d\right)\right]$ (若非空), $\left(a,b\right]\cap\left(c,\infty\right)=\left(\max\left(a,c\right),b\right]$, $\left(a,\infty\right)\cap\left(c,\infty\right)=\left(\max\left(a,c\right),\infty\right)$, 且与 $\varnothing$ 的交为 $\varnothing$. 故 h 区间的交是 h 区间. 由此, $\mathcal E$ 中任意两个有限不交并的交, 仍可展开为有限个 h 区间的不交并, 故 $\mathcal E$ 对有限交封闭.

再证 $\mathcal E$ 对补封闭. 单个 h 区间的补:

$$
\begin{aligned}
&\quad\;\varnothing^{c}=\mathbb R\\&=\left(-\infty,\infty\right),\\&\quad\;\left(a,\infty\right)^{c}=\left(-\infty,a\right],\\&\quad\;\left(a,b\right]^{c}=\left(-\infty,a\right]\cup\left(b,\infty\right),
\end{aligned}
$$

其中 $\left(-\infty,a\right]=\left(-\infty,a\right]$, $\left(b,\infty\right)$ 均为 h 区间, 且两两不交. 故每个 h 区间的补仍属于 $\mathcal E$. 对 $\mathcal E$ 中元素 $A=\bigcup_{i=1}^{n}I_{i}$ ($I_{i}$ 为不交 h 区间), 由德摩根律

$$
\begin{aligned}
&\quad\;A^{c}\\&=\left(\bigcup_{i=1}^{n}I_{i}\right)^{c}\\&=\bigcap_{i=1}^{n}I_{i}^{c}\in\mathcal E,
\end{aligned}
$$

因每个 $I_{i}^{c}\in\mathcal E$ 且 $\mathcal E$ 对有限交封闭.

最后, $X\in\mathcal E$: 因 $\mathbb R=\left(-\infty,\infty\right)=\left(-\infty,\infty\right)$ 是 $\left(a,\infty\right)$ 型 h 区间 ($a=-\infty$), 故 $\mathbb R\in\mathcal E$. 且对 $A,B\in\mathcal E$, 由德摩根律 $A\cup B=\left(A^{c}\cap B^{c}\right)^{c}\in\mathcal E$. 故 $\mathcal E$ 对有限并封闭.

综上, $\mathcal E$ 是代数. $\blacksquare$

### 习题三

由 $F\left(x\right)=x$ 构造的勒贝格测度 $m$ (**定义 6.4.6**) 满足:

(1) $m$ 是平移不变的: $m\left(E+x\right)=m\left(E\right)$ 对所有可测集 $E$ 和 $x\in\mathbb R$ 成立;

(2) $m$ 是尺度不变的: $m\left(rE\right)=\left|r\right|m\left(E\right)$ 对所有可测集 $E$ 和 $r\in\mathbb R$ 成立.

(即**定理 6.4.7** 的 (1)(2).)

### 解答 习题三

设 $\mathcal E$ 是 h 区间代数, $\mu_{0}$ 是由 $F\left(x\right)=x$ 经**命题 6.4.2** 定义的准测度, 即对 h 区间 $\mu_{0}\left(\left(a,b\right]\right)=b-a$ (区间长度); 由**定理 6.2.2**, $\mu_{0}$ 生成外测度

$$
m^{*}\left(A\right)=\inf\left\{\sum_{n}\left(b_{n}-a_{n}\right):A\subset\bigcup_{n}\left(a_{n},b_{n}\right]\right\},
$$

且勒贝格测度 $m=m^{*}|_{\mathcal L}$ (**定义 6.4.6**).

(1) 先证外测度平移不变. 对 $A\subset\mathbb R$ 与 $x\in\mathbb R$, 平移 $\tau_{x}:t\mapsto t+x$ 把 h 区间映为 h 区间并保持长度: $\mu_{0}\left(I+x\right)=\mu_{0}\left(I\right)$. 故 $\left\{I_{n}\right\}$ 覆盖 $A$ 当且仅当 $\left\{I_{n}+x\right\}$ 覆盖 $A+x$, 且

$$
\sum_{n}\mu_{0}\left(I_{n}+x\right)=\sum_{n}\mu_{0}\left(I_{n}\right).
$$

由 $m^{*}$ 的定义 (下确界覆盖), 得 $m^{*}\left(A+x\right)=m^{*}\left(A\right)$.

再证可测性在平移下保持. 若 $E\in\mathcal L$ (即 $E$ 是 $m^{*}$-可测的, **定义 6.3.1**), 则对任意 $T\subset\mathbb R$,

$$
\begin{aligned}
&\quad\;m^{*}\left(T\right)\\&=m^{*}\left(T-x\right)\\&=m^{*}\left(\left(T-x\right)\cap E\right)+m^{*}\left(\left(T-x\right)\cap E^{c}\right)\\&=m^{*}\left(T\cap\left(E+x\right)\right)+m^{*}\left(T\cap\left(E+x\right)^{c}\right),
\end{aligned}
$$

其中第二步用 $E$ 的可测性于 $T-x$. 故 $E+x$ 可测. 于是对可测集 $E$,

$$
\begin{aligned}
&\quad\;m\left(E+x\right)\\&=m^{*}\left(E+x\right)\\&=m^{*}\left(E\right)\\&=m\left(E\right).
\end{aligned}
$$

(1) 得证.

(2) 对 $r\ne0$, 伸缩 $\delta_{r}:t\mapsto rt$ 把 h 区间 $\left(a,b\right]$ 映为 $\left(ra,rb\right]$ ($r>0$) 或 $\left(rb,ra\right]$ ($r<0$), 仍是 h 区间, 且长度变为 $\left|r\right|\left(b-a\right)$, 即 $\mu_{0}\left(rI\right)=\left|r\right|\mu_{0}\left(I\right)$. 与 (1) 同理得 $m^{*}\left(rA\right)=\left|r\right|m^{*}\left(A\right)$, 且 $E$ 可测推出 $rE$ 可测 (用卡拉西奥多里条件与伸缩). 故 $m\left(rE\right)=\left|r\right|m\left(E\right)$. 当 $r=0$ 时, $0\cdot E$ 为空集或 $\left\{0\right\}$, 测度均为 $0=\left|0\right|m\left(E\right)$. (2) 得证. $\blacksquare$

### 习题四

设康托尔集 $C=\bigcap_{n=0}^{\infty}C_{n}$ (**定义 6.5.1**). 证明**定理 6.5.3**: $C$ 具有以下性质:

1. 紧致性: $C$ 是有界闭集;

2. 完备性: $C$ 是完备度量空间 (任何柯西序列收敛);

3. 完全不连通: $C$ 的连通子集只有单点集;

4. 无处稠密: $C$ 的内部为空集;

5. 完美集: $C$ 是闭集且没有孤立点.

### 解答 习题四

由**定理 6.5.2**, $x\in C$ 当且仅当 $x$ 的三进制展开 $x=\sum_{k=1}^{\infty}\frac{a_{k}}{3^{k}}$ 满足 $a_{k}\in\left\{0,2\right\}$.

**1. 紧致性.** 由**定义 6.5.1**, 每个 $C_{n}$ 是从 $\left[0,1\right]$ 去掉有限个开区间 (第 $n$ 步挖去的开区间) 所得, 故 $C_{n}$ 是有限个闭区间之并, 从而是闭集. $C=\bigcap_{n=0}^{\infty}C_{n}$ 是闭集的交, 故 $C$ 是闭集, 且 $C\subset\left[0,1\right]$ 有界. 由海涅-博雷尔定理, $\mathbb R$ 中有界闭集紧致, 故 $C$ 紧致. $\blacksquare$

**2. 完备性.** $\mathbb R$ 是完备度量空间, $C$ 是 $\mathbb R$ 的闭子集. 若 $\left\{x_{n}\right\}\subset C$ 是柯西列, 则它在 $\mathbb R$ 中收敛于某 $x$; 因 $C$ 闭, $x\in C$. 故 $C$ 中任何柯西列收敛, $C$ 完备. $\blacksquare$

**3. 完全不连通.** 设 $K\subset C$ 连通且含有 $x<y$ 两点. 由**定理 6.5.2**, $x,y$ 的三进制展开不含数字 $1$. 因 $x\ne y$, 存在最小的 $n$ 使 $x,y$ 的三进制第 $n$ 位不同, 不妨设 $x$ 的第 $n$ 位为 $0$, $y$ 的第 $n$ 位为 $2$ (前 $n-1$ 位相同). 则第 $n$ 步挖去的开区间中有一个 $J=\left(\alpha,\beta\right)$ 位于 $x$ 与 $y$ 之间 (即 $x<\alpha<\beta<y$), 且 $J\cap C=\varnothing$. 于是

$$
K=\left(K\cap\left(-\infty,\alpha\right]\right)\cup\left(K\cap\left[\beta,\infty\right)\right),
$$

是两个非空、互不相交的 $K$-相对开集 (因 $K\subset C$, $K\cap J=\varnothing$), 与 $K$ 连通矛盾. 故 $K$ 只能是单点集. $\blacksquare$

**4. 无处稠密.** 任取非空开区间 $\left(\alpha,\beta\right)\subset\mathbb R$. 若它与 $\left[0,1\right]$ 相交, 取 $n$ 使 $3^{-n}<\beta-\alpha$. 第 $n$ 步后 $C_{n}$ 是 $2^{n}$ 个长度 $3^{-n}$ 的闭区间之并, 这些闭区间之间的 $2^{n}-1$ 个开区间 (第 $n$ 步挖去的) 覆盖了 $\left[0,1\right]$ 中除端点外的部分, 且挖去区间的长度均为 $3^{-n}$. 因 $\left(\alpha,\beta\right)$ 长度大于 $3^{-n}$, 它必包含某个第 $n$ 步挖去的开区间, 故 $\left(\alpha,\beta\right)$ 不全含于 $C$. 所以 $C$ 不含任何非空开区间, $\operatorname{int}\left(C\right)=\varnothing$, 即 $C$ 无处稠密. $\blacksquare$

**5. 完美集.** 闭集已由 (1) 证得. 证 $C$ 无孤立点: 设 $x\in C$, 对任意 $\varepsilon>0$, 由**定理 6.5.2** 写 $x=\sum_{k=1}^{\infty}\frac{a_{k}}{3^{k}}$, $a_{k}\in\left\{0,2\right\}$. 取 $n$ 使 $\frac{2}{3^{n+1}}<\varepsilon$, 令 $x_{n}$ 为三进制展开中把 $x$ 的第 $n+1$ 位 $a_{n+1}$ 换成 $2-a_{n+1}$、其余位不变所得的点. 则 $x_{n}\in C$ (三进制不含 $1$), $x_{n}\ne x$, 且

$$
\begin{aligned}
&\quad\;\left|x_{n}-x\right|\\&=\left|\frac{2-a_{n+1}}{3^{n+1}}-\frac{a_{n+1}}{3^{n+1}}\right|\\&=\frac{2}{3^{n+1}}<\varepsilon.
\end{aligned}
$$

故 $x$ 的 $\varepsilon$ 邻域内含有 $C$ 中异于 $x$ 的点, $x$ 不是孤立点. 所以 $C$ 是完美集. $\blacksquare$

### 习题五

证明习题 30、33.

**30.** 设 $E\in\mathcal L$ 且 $m\left(E\right)>0$. 证明对任意 $\alpha<1$, 存在开区间 $I$ 使 $m\left(E\cap I\right)>\alpha m\left(I\right)$.

**33.** 证明存在博雷尔集 $A\subset\left[0,1\right]$ 使对 $\left[0,1\right]$ 的每个子区间 $I$, 都有 $0<m\left(A\cap I\right)<m\left(I\right)$. (提示: $\left[0,1\right]$ 的每个子区间都含正测度的康托尔型集.)

### 解答 习题五

**30.** 反证. 假设存在 $\alpha<1$ 使对每个开区间 $I$, 均有 $m\left(E\cap I\right)\le\alpha m\left(I\right)$. 则对任意开集 $U$, 把 $U$ 表为可数个互不相交开区间的并 $U=\bigcup_{k}I_{k}$, 由 $m$ 的可数可加性,

$$
\begin{aligned}
&\quad\;m\left(E\cap U\right)\\&=\sum_{k}m\left(E\cap I_{k}\right)\\&\le\alpha\sum_{k}m\left(I_{k}\right)\\&=\alpha m\left(U\right).
\end{aligned}
$$

由勒贝格-斯蒂尔杰斯测度的外正则性 (**定理 6.4.5**), $m\left(E\right)=\inf\left\{m\left(U\right):E\subset U\text{开}\right\}$. 取一列开集 $U_{n}\supset E$ 使 $m\left(U_{n}\right)\to m\left(E\right)$. 因 $E\subset U_{n}$, $E=E\cap U_{n}$, 故

$$
m\left(E\right)=m\left(E\cap U_{n}\right)\le\alpha m\left(U_{n}\right)\to\alpha m\left(E\right).
$$

于是 $m\left(E\right)\le\alpha m\left(E\right)$. 因 $m\left(E\right)>0$, 得 $\alpha\ge1$, 与 $\alpha<1$ 矛盾. 故存在开区间 $I$ 使 $m\left(E\cap I\right)>\alpha m\left(I\right)$. $\blacksquare$

**33.** 用正测度的广义康托尔集 (基础知识). 设 $\left\{I_{n}\right\}$ 是 $\left[0,1\right]$ 中所有以有理数为端点的开区间的枚举. 归纳地选取两两不交的闭区间 $J_{n}\subset I_{n}$ (取 $J_{n}$ 避开之前所有 $J_{k}$), 使每个子区间 $I$ 都含某个 $J_{n}$ (因 $\left\{I_{n}\right\}$ 枚举有理区间, 每个子区间含某个 $I_{n}$, 而 $J_{n}\subset I_{n}$). 固定 $c\in\left(0,1\right)$. 在每个 $J_{n}$ 内取广义康托尔集 $C_{n}\subset J_{n}$, 使 $m\left(C_{n}\right)=c\,m\left(J_{n}\right)$ (由广义康托尔集测度可为任意 $\beta\in\left(0,1\right)$). 因 $J_{n}$ 两两不交, $C_{n}$ 两两不交. 令 $A=\bigcup_{n=1}^{\infty}C_{n}$, 则 $A$ 是可数个闭集之并, 从而是博雷尔集, 且 $A\subset\left[0,1\right]$.

先证下界. 对任意子区间 $I\subset\left[0,1\right]$, 存在 $n$ 使 $J_{n}\subset I_{n}\subset I$, 故

$$
\begin{aligned}
&\quad\;m\left(A\cap I\right)\\&\ge m\left(A\cap J_{n}\right)\\&=m\left(C_{n}\right)\\&=c\,m\left(J_{n}\right)>0.
\end{aligned}
$$

再证上界. 因 $C_{n}\subset J_{n}$ 且 $\left\{J_{n}\right\}$ 两两不交,

$$
\begin{aligned}
&\quad\;m\left(A\cap I\right)\\&=m\left(\bigcup_{n}C_{n}\cap I\right)\\&=\sum_{n}m\left(C_{n}\cap I\right)\\&=\sum_{J_{n}\subset I}m\left(C_{n}\right)\\&=c\sum_{J_{n}\subset I}m\left(J_{n}\right)\\&=c\,m\left(\bigcup_{J_{n}\subset I}J_{n}\right)\\&\le c\,m\left(I\right)\\&<m\left(I\right),
\end{aligned}
$$

其中仅当 $J_{n}\cap I$ 有正测度 (即 $J_{n}\subset I$, 至多相差端点) 时 $m\left(C_{n}\cap I\right)=m\left(C_{n}\right)$ 非零. 故对 $\left[0,1\right]$ 的每个子区间 $I$, 有 $0<m\left(A\cap I\right)<m\left(I\right)$. $\blacksquare$
