# week3

> **定义 1.3.1 (上极限)**
> 
> 集列 $\left\{E_{n}\right\}$ 的上极限定义为

> **定义 1.3.3 (下极限)**
> 
> 集列 $\left\{E_{n}\right\}$ 的下极限定义为

> **定义 4.1.1 (集合代数)**
> 
> 设 $X$ 是非空集合, $\mathcal{A}\subset\mathcal{P}\left(X\right)$. 称 $\mathcal{A}$ 为 $X$ 上的一个集合代数, 若满足: (1) $X\in\mathcal{A}$; (2) 对差运算封闭: $A,B\in\mathcal{A}\Rightarrow{A}\setminus{B}\in\mathcal{A}$; (3) 对有限并封闭: $A,B\in\mathcal{A}\Rightarrow{A}\cup{B}\in\mathcal{A}$.

> **定义 4.1.3 ($\sigma$-代数)**
> 
> 设 $X$ 非空, $\mathcal{F}\subset\mathcal{P}\left(X\right)$. 称 $\mathcal{F}$ 为 $X$ 上的一个 $\sigma$-代数, 若满足: (1) $X\in\mathcal{F}$; (2) 对补运算封闭: $A\in\mathcal{F}\Rightarrow{A}^{c}\in\mathcal{F}$; (3) 对可数并封闭: $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal{F}$.

> **定义 4.4.1 (单调类)**
> 
> 设 $\mathcal{M}\subset\mathcal{P}\left(X\right)$. 称 $\mathcal{M}$ 为单调类, 若满足: (1) 对单调递增序列封闭: $A_{1}\subset{A}_{2}\subset\cdots$ 且 $A_{n}\in\mathcal{M}\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal{M}$; (2) 对单调递减序列封闭: $A_{1}\supset{A}_{2}\supset\cdots$ 且 $A_{n}\in\mathcal{M}\Rightarrow\bigcap_{n=1}^{\infty}A_{n}\in\mathcal{M}$.

> **定理 4.4.2 (单调类定理)**
> 
> 设 $\mathcal{A}$ 是一个代数, $\mathcal{M}$ 是一个包含 $\mathcal{A}$ 的单调类, 则 $\sigma\left(\mathcal{A}\right)\subset\mathcal{M}$.

> **定义 5.1.2 (测度)**
> 
> 设 $\left(X,\mathcal{F}\right)$ 是一个可测空间. 函数 $\mu:\mathcal{F}\to\left[0,+\infty\right]$ 称为 $\left(X,\mathcal{F}\right)$ 上的一个测度, 如果满足: (1) 非负性: $\mu\left(E\right)\ge0$ 对一切 $E\in\mathcal{F}$ 成立; (2) 零空集性: $\mu\left(\emptyset\right)=0$; (3) 可数可加性 ($\sigma$-可加性): 对任意可数个两两不交的集合 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$, 有 $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **命题 5.2.1 (有限可加性)**
> 
> 设 $\mu$ 是 $\left(X,\mathcal{F}\right)$ 上的测度, $E_{1},\dots,E_{n}\in\mathcal{F}$ 是两两不交的集合, 则

> **命题 5.2.2 (单调性)**
> 
> 设 $\mu$ 是测度, $E,F\in\mathcal{F}$ 且 $E\subset{F}$, 则 $\mu\left(E\right)\le\mu\left(F\right)$. 若进一步 $\mu\left(E\right)<+\infty$, 则 $\mu\left(F\setminus{E}\right)=\mu\left(F\right)-\mu\left(E\right)$.

> **命题 5.2.3 (次可数可加性)**
> 
> 设 $\mu$ 是测度, $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$ 是任意可数个集合 (不一定两两不交), 则

> **命题 5.2.4 (下连续性)**
> 
> 设 $\mu$ 是测度, $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$ 是单调递增的集合序列 (即 $E_{1}\subset{E}_{2}\subset\cdots$), 则

> **命题 5.2.5 (上连续性)**
> 
> 设 $\mu$ 是测度, $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$ 是单调递减的集合序列 (即 $E_{1}\supset{E}_{2}\supset\cdots$), 且存在某个 $m$ 使得 $\mu\left(E_{m}\right)<+\infty$, 则

> **定义 5.4.1 (零集)**
> 
> 设 $\left(X,\mathcal{F},\mu\right)$ 是测度空间. 集合 $N\in\mathcal{F}$ 称为零集, 若 $\mu\left(N\right)=0$.

> **定义 5.4.2 (零测度集)**
> 
> 集合 $A\subset{X}$ 称为零测度集, 若存在 $N\in\mathcal{F}$ 使得 $A\subset{N}$ 且 $\mu\left(N\right)=0$.

> **定义 5.4.4 (完备测度)**
> 
> 测度空间 $\left(X,\mathcal{F},\mu\right)$ 称为完备的, 若对任意满足 $\mu\left(N\right)=0$ 的 $N\in\mathcal{F}$, 以及任意 $A\subset{N}$, 都有 $A\in\mathcal{F}$.

> **定理 5.4.6 (测度完备化定理)**
> 
> 任意测度空间 $\left(X,\mathcal{F},\mu\right)$ 都可以完备化, 即存在完备测度空间 $\left(X,\mathcal{M},\overline\mu\right)$ 使得: (1) $\mathcal{F}\subset\mathcal{M}$; (2) $\overline\mu|_{\mathcal{F}}=\mu$; (3) $\mathcal{M}$ 是包含 $\mathcal{F}$ 的最小完备 $\sigma$-代数. 具体地, 令 $\mathcal{N}=\left\{N\in\mathcal{F}:\mu\left(N\right)=0\right\}$, $\mathcal{M}=\left\{A\subset{X}:\exists\,B\in\mathcal{F},\exists\,N\in\mathcal{N},B\subset{A}\subset{B}\cup{N}\right\}$, 并定义 $\overline\mu\left(A\right)=\mu\left(B\right)$.

> **定义 6.1.1 (外测度)**
> 
> 设 $X$ 非空. 函数 $\mu^{*}:\mathcal{P}\left(X\right)\to\left[0,+\infty\right]$ 称为 $X$ 上的一个外测度, 若满足: (1) 非负性: $\mu^{*}\left(\varnothing\right)=0$, 且 $\mu^{*}\left(E\right)\ge0$ 对一切 $E\subset{X}$; (2) 单调性: $E\subset{F}\Rightarrow\mu^{*}\left(E\right)\le\mu^{*}\left(F\right)$; (3) 次可数可加性: $\mu^{*}\left(\bigcup_{n=1}^{\infty}E_{n}\right)\le\sum_{n=1}^{\infty}\mu^{*}\left(E_{n}\right)$.

> **定义 6.2.1 (准测度)**
> 
> 设 $X$ 是非空集合, $\mathcal{E}\subset\mathcal{P}\left(X\right)$ 是一个代数. 函数 $\mu_{0}:\mathcal{E}\to\left[0,+\infty\right]$ 称为一个准测度, 如果 $\mu_{0}\left(\emptyset\right)=0$, 且若 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{E}$ 两两不交且 $\bigcup_{n=1}^{\infty}E_{n}\in\mathcal{E}$, 则 $\mu_{0}\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu_{0}\left(E_{n}\right)$.

> **定理 6.2.2 (由准测度生成外测度)**
> 
> 设 $\mathcal{E}\subset\mathcal{P}\left(X\right)$ 是一个覆盖类, $\mu_{0}:\mathcal{E}\to\left[0,+\infty\right]$ 是一个准测度. 对任意 $A\subset{X}$, 定义

$$
\mu^{*}\left(A\right)=\inf\left\{\sum_{n=1}^{\infty}\mu_{0}\left(E_{n}\right):E_{n}\in\mathcal{E},A\subset\bigcup_{n=1}^{\infty}E_{n}\right\}.
$$
则 $\mu^{*}$ 是 $X$ 上的外测度, 且 $\mu^{*}|_{\mathcal{E}}=\mu_{0}$.

> **定义 6.3.1 (卡拉西奥多里条件)**
> 
> 设 $\mu^{*}$ 是 $X$ 上的外测度. 子集 $A\subset{X}$ 称为 $\mu^{*}$-可测的, 若对任意 $T\subset{X}$ 有

$$
\mu^{*}\left(T\right)=\mu^{*}\left(T\cap{A}\right)+\mu^{*}\left(T\cap{A}^{c}\right).
$$
所有 $\mu^{*}$-可测集组成的集合记为 $\mathcal{M}_{\mu^{*}}$.

> **引理 6.3.2 (代数含于可测集)**
> 
> 如果 $\mathcal{E}$ 是代数, $\mu_{0}$ 是准测度, 则 $\mathcal{E}\subset\mathcal{M}_{\mu^{*}}$.

> **定理 6.3.3 (卡拉西奥多里定理)**
> 
> 设 $\mu^{*}$ 是 $X$ 上的外测度, 则: (1) $\mathcal{M}$ 是一个 $\sigma$-代数; (2) $\mu^{*}|_{\mathcal{M}}$ 是一个完备测度; (3) 如果 $\mu^{*}$ 是由准测度 $\mu_{0}$ 生成的, 且 $\mu_{0}$ 是 $\sigma$-有限的, 则 $\mu^{*}|_{\mathcal{M}}$ 是 $\mu_{0}$ 的唯一延拓.

> **定义 6.4.1 (h 区间)**
> 
> 令 $-\infty\le{a}<{}b<\infty$, 所有左开右闭区间 $\left(a,b\right]$, 以及 $\left(a,\infty\right)$, $\varnothing$ 称为 h 区间. h 区间的有限不交并形成的集族 $\mathcal{E}$ 为一个代数.

> **命题 6.4.2 ($\mathcal{E}$ 上的准测度)**
> 
> 设 $F:\mathbb{R}\to\mathbb{R}$ 为增的右连续函数. 对于不交区间 $\left(a_{i},b_{i}\right]$, $i=1,\dots,n$, 定义 $\mu_{0}\left(\bigcup_{i=1}^{n}\left(a_{i},b_{i}\right]\right):=\sum_{i=1}^{n}\left[F\left(b_{i}\right)-F\left(a_{i}\right)\right]$, 并令 $\mu_{0}\left(\varnothing\right)=0$. 则 $\mu_{0}$ 为 $\mathcal{E}$ 上的准测度.

> **定理 6.4.5 (勒贝格-斯蒂尔杰斯测度的正则性)**
> 
> 设 $\mu_{F}$ 是由增右连续函数 $F$ 生成的勒贝格-斯蒂尔杰斯测度, $\mathcal{M}^{*}$ 是 $\mu_{F}$-可测集的 $\sigma$-代数. 若 $E\in\mathcal{M}^{*}$, 则

$$
\mu_{F}\left(E\right)=\inf\left\{\mu_{F}\left(U\right):E\subset{U},U\text{~开}\right\}=\sup\left\{\mu_{F}\left(K\right):K\subset{E},K\text{~紧}\right\}.
$$

> **定义 6.4.6 (勒贝格测度)**
> 
> 由 $F\left(x\right)=x$ 生成的测度称为勒贝格测度, 记作 $m$; 相应外测度定义的可测集称为勒贝格可测集, 全体记作 $\mathcal{L}$.

> **定义 6.5.1 (康托尔集的递归构造)**
> 
> 设 $C_{0}=\left[0,1\right]$. 对每个 $n\ge0$, 定义 $C_{n+1}=\frac{1}{3}C_{n}\cup\left(\frac{2}{3}+\frac{1}{3}C_{n}\right)$. 则康托尔集定义为 $C=\bigcap_{n=0}^{\infty}C_{n}$.

> **定理 6.5.2 (康托尔集的三进制刻画)**
> 
> 点 $x\in\left[0,1\right]$ 属于康托尔集 $C$ 当且仅当它的三进制展开 $x=\sum_{k=1}^{\infty}\frac{a_{k}}{3^{k}}$ 中不含数字 $1$ (即 $a_{k}\in\left\{0,2\right\}$).

## 1

设 $\left(X,\mathcal{M},\mu\right)$ 是有限测度空间.

(a) 若 $E,F\in\mathcal{M}$ 且 $\mu\left(E\triangle{F}\right)=0$, 则 $\mu\left(E\right)=\mu\left(F\right)$.

(b) 定义 $E\sim{F}$ 当且仅当 $\mu\left(E\triangle{F}\right)=0$, 则 $\sim$ 是 $\mathcal{M}$ 上的等价关系.

(c) 对 $E,F\in\mathcal{M}$, 定义 $\rho\left(E,F\right):=\mu\left(E\triangle{F}\right)$. 证明 $\rho\left(E,F\right)\le\rho\left(E,G\right)+\rho\left(F,G\right)$, 从而 $\rho$ 在商空间 $\mathcal{M}/\sim$ 上定义了一个度量.

### 解答 1

(a) $E=\left(E\cap{F}\right)\cup\left(E\setminus{F}\right)$, $F=\left(E\cap{F}\right)\cup\left(F\setminus{E}\right)$ 均为两两不交分解, 由**命题 5.2.1 (有限可加性)**,

$$
\mu\left(E\right)=\mu\left(E\cap{F}\right)+\mu\left(E\setminus{F}\right),\quad\mu\left(F\right)=\mu\left(E\cap{F}\right)+\mu\left(F\setminus{E}\right).
$$

又 $E\setminus{F}\subset{E}\triangle{F}$, $F\setminus{E}\subset{E}\triangle{F}$, 由**命题 5.2.2 (单调性)**, $\mu\left(E\setminus{F}\right)\le\mu\left(E\triangle{F}\right)=0$, 同理 $\mu\left(F\setminus{E}\right)=0$. 故 $\mu\left(E\right)=\mu\left(E\cap{F}\right)=\mu\left(F\right)$. $\blacksquare$

(b) 验证等价关系的三条性质:

(1) 自反性: $\mu\left(E\triangle{E}\right)=\mu\left(\varnothing\right)=0$, 故 $E\sim{E}$.

(2) 对称性: $E\triangle{F}=F\triangle{E}$, 故 $E\sim{F}\iff{F}\sim{E}$.

(3) 传递性: 因 $E\triangle{G}\subset\left(E\triangle{F}\right)\cup\left(F\triangle{G}\right)$, 由**命题 5.2.3 (次可数可加性)**, $\mu\left(E\triangle{G}\right)\le\mu\left(E\triangle{F}\right)+\mu\left(F\triangle{G}\right)=0$, 故 $E\sim{G}$.

故 $\sim$ 是 $\mathcal{M}$ 上的等价关系. $\blacksquare$

(c) 对称性与非负性显然: $\rho\left(E,F\right)=\rho\left(F,E\right)\ge0$, $\rho\left(E,E\right)=0$. 又 $E\triangle{G}\subset\left(E\triangle{F}\right)\cup\left(F\triangle{G}\right)$, 由**命题 5.2.3 (次可数可加性)**,

$$
\rho\left(E,G\right)=\mu\left(E\triangle{G}\right)\le\mu\left(E\triangle{F}\right)+\mu\left(F\triangle{G}\right)=\rho\left(E,F\right)+\rho\left(F,G\right).
$$

最后验证良定义与正定性: 若 $E\sim{E}'$, $F\sim{F}'$ (即 $\mu\left(E\triangle{E}'\right)=\mu\left(F\triangle{F}'\right)=0$), 则

$$
E\triangle{F}\subset\left(E\triangle{E}'\right)\cup\left(E'\triangle{F}'\right)\cup\left(F'\triangle{F}\right),
$$

故 $\rho\left(E,F\right)\le0+\rho\left(E',F'\right)+0=\rho\left(E',F'\right)$; 对称地 $\rho\left(E',F'\right)\le\rho\left(E,F\right)$, 故 $\rho\left(E,F\right)=\rho\left(E',F'\right)$, 即 $\rho$ 良定义于商空间 $\mathcal{M}/\sim$. 又 $\rho\left(E,F\right)=0\iff\mu\left(E\triangle{F}\right)=0\iff{E}\sim{F}$, 故 $\rho$ 是 $\mathcal{M}/\sim$ 上的度量. $\blacksquare$

## 2

证明**定理 6.3.3 (卡拉西奥多里定理)** 第 (3) 条的唯一性, 并证明习题 17, 24.

(1) 设 $\mathcal{E}\subset\mathcal{P}\left(X\right)$ 是代数, $\mu_{0}$ 是 $\mathcal{E}$ 上 $\sigma$-有限的准测度, $\mu^{*}$ 是由 $\mu_{0}$ 生成的外测度, $\mathcal{M}$ 是 $\mu^{*}$-可测集全体. 证明 $\mu^{*}|_{\mathcal{M}}$ 是 $\mu_{0}$ 到 $\mathcal{M}$ 的唯一延拓.

17. 设 $\mu^{*}$ 是 $X$ 上的外测度, $\left\{A_{j}\right\}_{j=1}^{\infty}$ 是一列两两不交的 $\mu^{*}$-可测集. 证明对任意 $E\subset{X}$, 有

$$
\mu^{*}\left(E\cap\bigcup_{j=1}^{\infty}A_{j}\right)=\sum_{j=1}^{\infty}\mu^{*}\left(E\cap{A}_{j}\right).
$$

24. 设 $\mu$ 是 $\left(X,\mathcal{M}\right)$ 上的有限测度, $\mu^{*}$ 是由 $\mu$ 诱导的外测度. 设 $E\subset{X}$ 满足 $\mu^{*}\left(E\right)=\mu^{*}\left(X\right)$ (但 $E$ 未必属于 $\mathcal{M}$).

(a) 若 $A,B\in\mathcal{M}$ 且 $A\cap{E}=B\cap{E}$, 则 $\mu\left(A\right)=\mu\left(B\right)$.

(b) 记 $\mathcal{M}_{E}=\left\{A\cap{E}:A\in\mathcal{M}\right\}$, 在 $\mathcal{M}_{E}$ 上定义 $\nu\left(A\cap{E}\right)=\mu\left(A\right)$ (由 (a) 良定义). 证明 $\mathcal{M}_{E}$ 是 $E$ 上的 $\sigma$-代数, 且 $\nu$ 是 $\mathcal{M}_{E}$ 上的测度.

### 解答 2

(1) 唯一性. 由**定义 6.2.1 (准测度)**, $\mu_{0}$ 是代数 $\mathcal{E}$ 上的准测度. 先证 $\mu^{*}|_{\mathcal{M}}$ 确是 $\mu_{0}$ 的延拓: 由**定理 6.2.2 (由准测度生成外测度)**, $\mu^{*}|_{\mathcal{E}}=\mu_{0}$; 由**引理 6.3.2 (代数含于可测集)**, $\mathcal{E}\subset\mathcal{M}$; 由**定理 6.3.3 (卡拉西奥多里定理)** (1)(2), $\mathcal{M}$ 是 $\sigma$-代数且 $\mu^{*}|_{\mathcal{M}}$ 是完备测度. 故 $\mu^{*}|_{\mathcal{M}}$ 是 $\mu_{0}$ 到 $\mathcal{M}$ 的测度延拓.

再证唯一性. 设 $\nu$ 是 $\mathcal{M}$ 上任一满足 $\nu|_{\mathcal{E}}=\mu_{0}$ 的测度, 我们证明 $\nu=\mu^{*}|_{\mathcal{M}}$. 先设 $\mu_{0}\left(X\right)<\infty$.

步骤 1: $\nu\le\mu^{*}$ 在 $\mathcal{M}$ 上. 对任意 $A\in\mathcal{M}$ 和 $\varepsilon>0$, 由**定理 6.2.2 (由准测度生成外测度)** 中 $\mu^{*}$ 的定义, 存在 $\left\{E_{n}\right\}\subset\mathcal{E}$ 覆盖 $A$ 使 $\sum_{n}\mu_{0}\left(E_{n}\right)\le\mu^{*}\left(A\right)+\varepsilon$. 由 $\nu$ 的次可数可加性 (**命题 5.2.3 (次可数可加性)**) 及 $\nu|_{\mathcal{E}}=\mu_{0}$,

$$
\nu\left(A\right)\le\sum_{n}\nu\left(E_{n}\right)=\sum_{n}\mu_{0}\left(E_{n}\right)\le\mu^{*}\left(A\right)+\varepsilon.
$$

由 $\varepsilon$ 的任意性, $\nu\left(A\right)\le\mu^{*}\left(A\right)$.

步骤 2: $\nu=\mu^{*}$ 在 $\sigma\left(\mathcal{E}\right)$ 上. 令 $\mathcal{H}=\left\{A\in\sigma\left(\mathcal{E}\right):\nu\left(A\right)=\mu^{*}\left(A\right)\right\}$. 对 $E\in\mathcal{E}$, 由**定理 6.2.2 (由准测度生成外测度)** 与 $\nu|_{\mathcal{E}}=\mu_{0}$ 得 $\mu^{*}\left(E\right)=\mu_{0}\left(E\right)=\nu\left(E\right)$, 故 $\mathcal{E}\subset\mathcal{H}$. 验证 $\mathcal{H}$ 是单调类 (**定义 4.4.1 (单调类)**): 若 $\left\{A_{n}\right\}\subset\mathcal{H}$ 且 $A_{n}\uparrow{A}$, 由 $\nu,\mu^{*}|_{\mathcal{M}}$ 的下连续性 (**命题 5.2.4 (下连续性)**; $\sigma\left(\mathcal{E}\right)\subset\mathcal{M}$) 得 $\nu\left(A\right)=\lim_{n}\nu\left(A_{n}\right)=\lim_{n}\mu^{*}\left(A_{n}\right)=\mu^{*}\left(A\right)$, 故 $A\in\mathcal{H}$; 递减情形同理 (此处 $\mu^{*}\left(A_{1}\right)\le\mu^{*}\left(X\right)=\mu_{0}\left(X\right)<\infty$, 上连续性可用). 故 $\mathcal{H}$ 是包含代数 $\mathcal{E}$ 的单调类, 由**定理 4.4.2 (单调类定理)**, $\sigma\left(\mathcal{E}\right)\subset\mathcal{H}$, 即 $\nu=\mu^{*}$ 在 $\sigma\left(\mathcal{E}\right)$ 上.

步骤 3: $\nu=\mu^{*}$ 在 $\mathcal{M}$ 上. 对任意 $A\in\mathcal{M}$, 由步骤 1 得 $\nu\left(A\right)\le\mu^{*}\left(A\right)$. 又因 $X\in\mathcal{E}$ (**定义 4.1.1 (集合代数)**), $\nu\left(X\right)=\mu_{0}\left(X\right)=\mu^{*}\left(X\right)$. 由步骤 1 作用于 $A^{c}\in\mathcal{M}$ (因 $\mathcal{M}$ 是 $\sigma$-代数, **定理 6.3.3 (卡拉西奥多里定理)** (1)), 以及 $A\in\mathcal{M}$ 给出 $\mu^{*}\left(X\right)=\mu^{*}\left(A\right)+\mu^{*}\left(A^{c}\right)$ (**定义 6.3.1 (卡拉西奥多里条件)** 于 $T=X$),

$$
\nu\left(A\right)=\nu\left(X\right)-\nu\left(A^{c}\right)=\mu^{*}\left(X\right)-\nu\left(A^{c}\right)\ge\mu^{*}\left(X\right)-\mu^{*}\left(A^{c}\right)=\mu^{*}\left(A\right).
$$

故 $\nu\left(A\right)=\mu^{*}\left(A\right)$. 于是 $\mu_{0}\left(X\right)<\infty$ 时唯一性得证.

$\sigma$-有限情形. 设 $\mu_{0}$ 是 $\sigma$-有限的, 即存在两两不交的 $X_{k}\in\mathcal{E}$ 使 $X=\bigcup_{k=1}^{\infty}X_{k}$ 且 $\mu_{0}\left(X_{k}\right)<\infty$. 对任意 $A\in\mathcal{M}$, 由可数可加性与下连续性,

$$
\mu^{*}\left(A\right)=\sum_{k}\mu^{*}\left(A\cap{X}_{k}\right),\quad\nu\left(A\right)=\sum_{k}\nu\left(A\cap{X}_{k}\right).
$$

对每个 $k$, 把有限测度 $\mu_{0}\left(\cdot\cap{X}_{k}\right)$ 与 $\nu\left(\cdot\cap{X}_{k}\right)$ 限制在 $X_{k}$ 上即化为有限情形, 得 $\nu\left(A\cap{X}_{k}\right)=\mu^{*}\left(A\cap{X}_{k}\right)$. 求和得 $\nu\left(A\right)=\mu^{*}\left(A\right)$. 故 $\mu^{*}|_{\mathcal{M}}$ 是 $\mu_{0}$ 到 $\mathcal{M}$ 的唯一延拓. $\blacksquare$

(2) 习题 17. 一方面, 由**定义 6.1.1 (外测度)** (3) (次可数可加性),

$$
\mu^{*}\left(E\cap\bigcup_{j=1}^{\infty}A_{j}\right)\le\sum_{j=1}^{\infty}\mu^{*}\left(E\cap{A}_{j}\right).
$$

另一方面, 由每个 $A_{j}$ 可测 (**定义 6.3.1 (卡拉西奥多里条件)**), 对任意 $T\subset{X}$ 与任意 $N$, 归纳地使用卡拉西奥多里条件于 $T$ 得

$$
\mu^{*}\left(T\right)=\sum_{j=1}^{N}\mu^{*}\left(T\cap{A}_{j}\right)+\mu^{*}\left(T\cap\left(\bigcup_{j=1}^{N}A_{j}\right)^{c}\right).
$$

取 $T=E\cap\bigcup_{j=1}^{\infty}A_{j}$, 则 $T\cap{A}_{j}=E\cap{A}_{j}$, 且 $T\cap\left(\bigcup_{j=1}^{N}A_{j}\right)^{c}=E\cap\bigcup_{j=N+1}^{\infty}A_{j}$. 故

$$
\mu^{*}\left(E\cap\bigcup_{j=1}^{\infty}A_{j}\right)=\sum_{j=1}^{N}\mu^{*}\left(E\cap{A}_{j}\right)+\mu^{*}\left(E\cap\bigcup_{j=N+1}^{\infty}A_{j}\right)\ge\sum_{j=1}^{N}\mu^{*}\left(E\cap{A}_{j}\right).
$$

令 $N\to\infty$ 得

$$
\mu^{*}\left(E\cap\bigcup_{j=1}^{\infty}A_{j}\right)\ge\sum_{j=1}^{\infty}\mu^{*}\left(E\cap{A}_{j}\right).
$$

合并即得等式. $\blacksquare$

(3) 习题 24. (a) 由 $A\cap{E}=B\cap{E}$ 得 $\left(A\setminus{B}\right)\cap{E}=\varnothing$, 且 $A\setminus{B}\in\mathcal{M}$. 因 $A\setminus{B}$ 可测, 用**定义 6.3.1 (卡拉西奥多里条件)** 于 $T=X$:

$$
\mu^{*}\left(X\right)=\mu^{*}\left(X\cap\left(A\setminus{B}\right)\right)+\mu^{*}\left(X\cap\left(A\setminus{B}\right)^{c}\right)=\mu\left(A\setminus{B}\right)+\mu^{*}\left(X\setminus\left(A\setminus{B}\right)\right).
$$

由 $\left(A\setminus{B}\right)\cap{E}=\varnothing$ 得 $E\subset{X}\setminus\left(A\setminus{B}\right)$, 据外测度单调性 (**定义 6.1.1 (外测度)** (2)) 有 $\mu^{*}\left(X\setminus\left(A\setminus{B}\right)\right)\ge\mu^{*}\left(E\right)=\mu^{*}\left(X\right)$. 代入上式得 $\mu\left(A\setminus{B}\right)\le0$, 故 $\mu\left(A\setminus{B}\right)=0$. 同理 $\mu\left(B\setminus{A}\right)=0$. 于是由**命题 5.2.1 (有限可加性)**,

$$
\mu\left(A\right)=\mu\left(A\cap{B}\right)+\mu\left(A\setminus{B}\right)=\mu\left(A\cap{B}\right)=\mu\left(B\right).
$$

$\blacksquare$

(b) 先证 $\nu$ 良定义: 若 $A\cap{E}=B\cap{E}$, 由 (a) 得 $\mu\left(A\right)=\mu\left(B\right)$, 故 $\nu$ 不依赖于代表元.

再证 $\mathcal{M}_{E}$ 是 $E$ 上的 $\sigma$-代数 (**定义 4.1.3 ($\sigma$-代数)**): 因 $E=X\cap{E}\in\mathcal{M}_{E}$; 对 $A\cap{E}\in\mathcal{M}_{E}$, 其在 $E$ 内的补为 $E\setminus\left(A\cap{E}\right)=\left(X\setminus{A}\right)\cap{E}\in\mathcal{M}_{E}$; 且 $\bigcup_{n}\left(A_{n}\cap{E}\right)=\left(\bigcup_{n}A_{n}\right)\cap{E}\in\mathcal{M}_{E}$. 故 $\mathcal{M}_{E}$ 是 $E$ 上的 $\sigma$-代数.

最后证 $\nu$ 是 $\mathcal{M}_{E}$ 上的测度 (**定义 5.1.2 (测度)**). 非负性由 $\mu\ge0$; $\nu\left(\varnothing\right)=\mu\left(\varnothing\right)=0$. 设 $\left\{A_{n}\cap{E}\right\}$ 两两不交. 则对 $n\ne{m}$, $\left(A_{n}\cap{A}_{m}\right)\cap{E}=\left(A_{n}\cap{E}\right)\cap\left(A_{m}\cap{E}\right)=\varnothing$, 由 (a) 得 $\mu\left(A_{n}\cap{A}_{m}\right)=0$. 于是由**命题 5.2.1 (有限可加性)** 与**命题 5.2.4 (下连续性)**,

$$
\nu\left(\bigcup_{n}\left(A_{n}\cap{E}\right)\right)=\nu\left(\left(\bigcup_{n}A_{n}\right)\cap{E}\right)=\mu\left(\bigcup_{n}A_{n}\right)=\sum_{n}\mu\left(A_{n}\right)=\sum_{n}\nu\left(A_{n}\cap{E}\right).
$$

故 $\nu$ 是测度. $\blacksquare$

## 3

设 $-\infty\le{a}<{}b<\infty$, 所有左开右闭区间 $\left(a,b\right]$ 以及 $\left(a,\infty\right)$, $\varnothing$ 称为 h 区间. 证明 h 区间的有限不交并形成的集族 $\mathcal{E}$ 是一个代数 (**定义 6.4.1 (h 区间)**).

### 解答 3

用**定义 4.1.1 (集合代数)** 验证.

先证两个 h 区间的交仍是 h 区间. 事实上, $\left(a,b\right]\cap\left(c,d\right]=\left(\max\left(a,c\right),\min\left(b,d\right)\right]$ (若非空), $\left(a,b\right]\cap\left(c,\infty\right)=\left(\max\left(a,c\right),b\right]$, $\left(a,\infty\right)\cap\left(c,\infty\right)=\left(\max\left(a,c\right),\infty\right)$, 且与 $\varnothing$ 的交为 $\varnothing$. 故 h 区间的交是 h 区间. 由此, $\mathcal{E}$ 中任意两个有限不交并的交, 仍可展开为有限个 h 区间的不交并, 故 $\mathcal{E}$ 对有限交封闭.

再证 $\mathcal{E}$ 对补封闭. 单个 h 区间的补:

$$
\varnothing^{c}=\mathbb{R}=\left(-\infty,\infty\right),\quad\left(a,\infty\right)^{c}=\left(-\infty,a\right],\quad\left(a,b\right]^{c}=\left(-\infty,a\right]\cup\left(b,\infty\right),
$$

其中 $\left(-\infty,a\right]$, $\left(b,\infty\right)$ 均为 h 区间, 且两两不交. 故每个 h 区间的补仍属于 $\mathcal{E}$. 对 $\mathcal{E}$ 中元素 $A=\bigcup_{i=1}^{n}I_{i}$ ($I_{i}$ 为不交 h 区间), 由德摩根律

$$
A^{c}=\left(\bigcup_{i=1}^{n}I_{i}\right)^{c}=\bigcap_{i=1}^{n}I_{i}^{c}\in\mathcal{E},
$$

因每个 $I_{i}^{c}\in\mathcal{E}$ 且 $\mathcal{E}$ 对有限交封闭.

最后, $X\in\mathcal{E}$: 因 $\mathbb{R}=\left(-\infty,\infty\right)$ 是 $\left(a,\infty\right)$ 型 h 区间 ($a=-\infty$), 故 $\mathbb{R}\in\mathcal{E}$. 且对 $A,B\in\mathcal{E}$, 由德摩根律 $A\cup{B}=\left(A^{c}\cap{B}^{c}\right)^{c}\in\mathcal{E}$. 故 $\mathcal{E}$ 对有限并封闭.

综上, $\mathcal{E}$ 是代数. $\blacksquare$
