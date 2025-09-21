# week3

> **定义 1.3.1 (上极限)**
> 
> 集列 $\left\{E_{n}\right\}$ 的上极限定义为 $\overline{\lim}_{n\to\infty}E_{n}=\left\{x:x\text{~属于无穷多个~}E_{n}\right\}=\bigcap_{n=1}^{\infty}\bigcup_{k=n}^{\infty}E_{k}$.

> **定义 1.3.3 (下极限)**
> 
> 集列 $\left\{E_{n}\right\}$ 的下极限定义为 $\underline{\lim}_{n\to\infty}E_{n}=\left\{x:x\text{~仅不属于有限多个~}E_{n}\right\}=\bigcup_{n=1}^{\infty}\bigcap_{k=n}^{\infty}E_{k}$.

> **定理 2.4.2 (原像运算的性质)**
> 
> 设 $f:A\to{B}$, 则 $f^{-1}\left(B_{1}\cup{B}_{2}\right)=f^{-1}\left(B_{1}\right)\cup{f}^{-1}\left(B_{2}\right)$, $f^{-1}\left(B_{1}\cap{B}_{2}\right)=f^{-1}\left(B_{1}\right)\cap{f}^{-1}\left(B_{2}\right)$, $f^{-1}\left(B^{c}\right)=\left(f^{-1}\left(B\right)\right)^{c}$, $f^{-1}\left(\bigcup_{\alpha\in{I}}B_{\alpha}\right)=\bigcup_{\alpha\in{I}}f^{-1}\left(B_{\alpha}\right)$, $f^{-1}\left(\bigcap_{\alpha\in{I}}B_{\alpha}\right)=\bigcap_{\alpha\in{I}}f^{-1}\left(B_{\alpha}\right)$.

> **定义 4.1.3 ($\sigma$-代数)**
> 
> 设 $X$ 非空, $\mathcal{F}\subset\mathcal{P}\left(X\right)$. 称 $\mathcal{F}$ 为 $X$ 上的一个 $\sigma$-代数, 若满足: (1) $X\in\mathcal{F}$; (2) 对补运算封闭: $A\in\mathcal{F}\Rightarrow{A}^{c}\in\mathcal{F}$; (3) 对可数并封闭: $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal{F}$.

> **定义 4.5.7 (任意乘积 $\sigma$-代数)**
> 
> 设 $\left\{\left(X_{\alpha},\mathcal{F}_{\alpha}\right)\right\}_{\alpha\in{I}}$ 是一族可测空间, 乘积 $\sigma$-代数 $\bigotimes_{\alpha\in{I}}\mathcal{F}_{\alpha}$ 是由所有柱集

> **定义 5.1.2 (测度)**
> 
> 设 $\left(X,\mathcal{F}\right)$ 是一个可测空间. 函数 $\mu:\mathcal{F}\to\left[0,+\infty\right]$ 称为 $\left(X,\mathcal{F}\right)$ 上的一个测度, 如果满足: (1) 非负性: $\mu\left(E\right)\ge0$ 对一切 $E\in\mathcal{F}$ 成立; (2) 零空集性: $\mu\left(\emptyset\right)=0$; (3) 可数可加性 ($\sigma$-可加性): 对任意可数个两两不交的集合 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$, 有 $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **命题 5.2.1 (有限可加性)**
> 
> 设 $\mu$ 是 $\left(X,\mathcal{F}\right)$ 上的测度, $E_{1},\dots,E_{n}\in\mathcal{F}$ 是两两不交的集合, 则 $\mu\left(\bigcup_{k=1}^{n}E_{k}\right)=\sum_{k=1}^{n}\mu\left(E_{k}\right)$.

> **命题 5.2.2 (单调性)**
> 
> 设 $\mu$ 是测度, $E,F\in\mathcal{F}$ 且 $E\subset{F}$, 则 $\mu\left(E\right)\le\mu\left(F\right)$. 若进一步 $\mu\left(E\right)<+\infty$, 则 $\mu\left(F\setminus{E}\right)=\mu\left(F\right)-\mu\left(E\right)$.

> **命题 5.2.3 (次可数可加性)**
> 
> 设 $\mu$ 是测度, $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$ 是任意可数个集合 (不一定两两不交), 则 $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)\le\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **命题 5.2.4 (下连续性)**
> 
> 设 $\mu$ 是测度, $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$ 是单调递增的集合序列 (即 $E_{1}\subset{E}_{2}\subset\cdots$), 则 $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\lim_{n\to\infty}\mu\left(E_{n}\right)$.

> **命题 5.2.5 (上连续性)**
> 
> 设 $\mu$ 是测度, $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$ 是单调递减的集合序列 (即 $E_{1}\supset{E}_{2}\supset\cdots$), 且存在某个 $m$ 使得 $\mu\left(E_{m}\right)<+\infty$, 则 $\mu\left(\bigcap_{n=1}^{\infty}E_{n}\right)=\lim_{n\to\infty}\mu\left(E_{n}\right)$.

> **定义 5.4.1 (零集)**
> 
> 设 $\left(X,\mathcal{F},\mu\right)$ 是测度空间. 集合 $N\in\mathcal{F}$ 称为零集, 若 $\mu\left(N\right)=0$.

> **定义 5.4.2 (零测度集)**
> 
> 集合 $A\subset{X}$ 称为零测度集, 若存在 $N\in\mathcal{F}$ 使得 $A\subset{N}$ 且 $\mu\left(N\right)=0$.

> **定理 5.4.6 (测度完备化定理)**
> 
> 任意测度空间 $\left(X,\mathcal{F},\mu\right)$ 都可以完备化, 即存在完备测度空间 $\left(X,\mathcal{M},\overline\mu\right)$ 使得: (1) $\mathcal{F}\subset\mathcal{M}$; (2) $\overline\mu|_{\mathcal{F}}=\mu$; (3) $\mathcal{M}$ 是包含 $\mathcal{F}$ 的最小完备 $\sigma$-代数. 具体地, 令 $\mathcal{N}=\left\{N\in\mathcal{F}:\mu\left(N\right)=0\right\}$, $\mathcal{M}=\left\{A\subset{X}:\exists\,B\in\mathcal{F},\exists\,N\in\mathcal{N},B\subset{A}\subset{B}\cup{N}\right\}$, 并定义 $\overline\mu\left(A\right)=\mu\left(B\right)$.

## 3

设 $\left(X,\mathcal{M},\mu\right)$ 是测度空间, $\left\{E_{j}\right\}_{j=1}^{\infty}\subset\mathcal{M}$. 证明 $\mu\left(\liminf_{j\to\infty}E_{j}\right)\le\liminf_{j\to\infty}\mu\left(E_{j}\right)$. 又若 $\mu\left(\bigcup_{j=1}^{\infty}E_{j}\right)<\infty$, 则 $\mu\left(\limsup_{j\to\infty}E_{j}\right)\ge\limsup_{j\to\infty}\mu\left(E_{j}\right)$.

### 解答 3

记 $F_{n}:=\bigcap_{j=n}^{\infty}E_{j}$. 由**定义 1.3.3 (下极限)**, $\liminf_{j\to\infty}E_{j}=\bigcup_{n=1}^{\infty}F_{n}$; 且 $\left\{F_{n}\right\}$ 单调递增. 由**命题 5.2.4 (下连续性)**,

$$
\mu\left(\liminf_{j\to\infty}E_{j}\right)=\mu\left(\bigcup_{n=1}^{\infty}F_{n}\right)=\lim_{n\to\infty}\mu\left(F_{n}\right).
$$

又因 $F_{n}\subset{E}_{j}$ 对一切 $j\ge{n}$, 由**命题 5.2.2 (单调性)** 得 $\mu\left(F_{n}\right)\le\inf_{j\ge{n}}\mu\left(E_{j}\right)$, 故

$$
\mu\left(\liminf_{j\to\infty}E_{j}\right)=\lim_{n\to\infty}\mu\left(F_{n}\right)\le\lim_{n\to\infty}\inf_{j\ge{n}}\mu\left(E_{j}\right)=\liminf_{j\to\infty}\mu\left(E_{j}\right).
$$

记 $G_{n}:=\bigcup_{j=n}^{\infty}E_{j}$. 由**定义 1.3.1 (上极限)**, $\limsup_{j\to\infty}E_{j}=\bigcap_{n=1}^{\infty}G_{n}$; 且 $\left\{G_{n}\right\}$ 单调递减. 因 $\mu\left(G_{1}\right)=\mu\left(\bigcup_{j=1}^{\infty}E_{j}\right)<\infty$, 由**命题 5.2.5 (上连续性)**,

$$
\mu\left(\limsup_{j\to\infty}E_{j}\right)=\mu\left(\bigcap_{n=1}^{\infty}G_{n}\right)=\lim_{n\to\infty}\mu\left(G_{n}\right).
$$

又因 $G_{n}\supset{E}_{j}$ 对一切 $j\ge{n}$, 由单调性得 $\mu\left(G_{n}\right)\ge\sup_{j\ge{n}}\mu\left(E_{j}\right)$, 故

$$
\mu\left(\limsup_{j\to\infty}E_{j}\right)=\lim_{n\to\infty}\mu\left(G_{n}\right)\ge\lim_{n\to\infty}\sup_{j\ge{n}}\mu\left(E_{j}\right)=\limsup_{j\to\infty}\mu\left(E_{j}\right).
$$

两不等式得证.

$\blacksquare$

## 4

设 $\left(X,\mathcal{M},\mu\right)$ 是测度空间, $E,F\in\mathcal{M}$. 证明 $\mu\left(E\right)+\mu\left(F\right)=\mu\left(E\cup{F}\right)+\mu\left(E\cap{F}\right)$.

### 解答 4

$$
E\cup{F}=\left(E\cap{F}\right)\cup\left(E\setminus{F}\right)\cup\left(F\setminus{E}\right),
$$

右侧三集合两两不交. 由**命题 5.2.1 (有限可加性)**,

$$
\mu\left(E\cup{F}\right)=\mu\left(E\cap{F}\right)+\mu\left(E\setminus{F}\right)+\mu\left(F\setminus{E}\right).
$$

又 $E=\left(E\cap{F}\right)\cup\left(E\setminus{F}\right)$, $F=\left(E\cap{F}\right)\cup\left(F\setminus{E}\right)$ 均为两两不交分解, 故

$$
\mu\left(E\right)+\mu\left(F\right)=2\mu\left(E\cap{F}\right)+\mu\left(E\setminus{F}\right)+\mu\left(F\setminus{E}\right)=\mu\left(E\cup{F}\right)+\mu\left(E\cap{F}\right).
$$

等式得证.

$\blacksquare$

## 5

给定测度空间 $\left(X,\mathcal{M},\mu\right)$ 与 $E\in\mathcal{M}$, 对 $A\in\mathcal{M}$ 定义 $\mu_{E}\left(A\right):=\mu\left(A\cap{E}\right)$. 证明 $\mu_{E}$ 是一个测度.

### 解答 5

逐条验证**定义 5.1.2 (测度)**:

(1) 非负性: $\mu_{E}\left(A\right)=\mu\left(A\cap{E}\right)\ge0$ 对一切 $A\in\mathcal{M}$.

(2) 零空集性: $\mu_{E}\left(\emptyset\right)=\mu\left(\emptyset\cap{E}\right)=\mu\left(\emptyset\right)=0$.

(3) 可数可加性: 设 $\left\{A_{j}\right\}_{j=1}^{\infty}\subset\mathcal{M}$ 两两不交, 则 $\left\{A_{j}\cap{E}\right\}$ 亦两两不交, 由 $\mu$ 的可数可加性

$$
\mu_{E}\left(\bigcup_{j=1}^{\infty}A_{j}\right)=\mu\left(\left(\bigcup_{j=1}^{\infty}A_{j}\right)\cap{E}\right)=\mu\left(\bigcup_{j=1}^{\infty}\left(A_{j}\cap{E}\right)\right)=\sum_{j=1}^{\infty}\mu\left(A_{j}\cap{E}\right)=\sum_{j=1}^{\infty}\mu_{E}\left(A_{j}\right).
$$

故 $\mu_{E}$ 是测度.

$\blacksquare$

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

由**命题 6.4.2 ($\mathcal{E}$ 上的准测度)**, **定义 5.4.4 (完备测度)**, **命题 5.2.5 (上连续性)**, (1) 唯一性. 由**定义 6.2.1 (准测度)**, $\mu_{0}$ 是代数 $\mathcal{E}$ 上的准测度. 先证 $\mu^{*}|_{\mathcal{M}}$ 确是 $\mu_{0}$ 的延拓: 由**定理 6.2.2 (由准测度生成外测度)**, $\mu^{*}|_{\mathcal{E}}=\mu_{0}$; 由**引理 6.3.2 (代数含于可测集)**, $\mathcal{E}\subset\mathcal{M}$; 由**定理 6.3.3 (卡拉西奥多里定理)** (1)(2), $\mathcal{M}$ 是 $\sigma$-代数且 $\mu^{*}|_{\mathcal{M}}$ 是完备测度. 故 $\mu^{*}|_{\mathcal{M}}$ 是 $\mu_{0}$ 到 $\mathcal{M}$ 的测度延拓.

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

对每个 $k$, 把有限测度 $\mu_{0}\left(\cdot\cap{X}_{k}\right)$ 与 $\nu\left(\cdot\cap{X}_{k}\right)$ 限制在 $X_{k}$ 上即化为有限情形, 得 $\nu\left(A\cap{X}_{k}\right)=\mu^{*}\left(A\cap{X}_{k}\right)$. 求和得 $\nu\left(A\right)=\mu^{*}\left(A\right)$. 故 $\mu^{*}|_{\mathcal{M}}$ 是 $\mu_{0}$ 到 $\mathcal{M}$ 的唯一延拓.

$\blacksquare$

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

合并即得等式.

$\blacksquare$

(3) 习题 24. (a) 由 $A\cap{E}=B\cap{E}$ 得 $\left(A\setminus{B}\right)\cap{E}=\emptyset$, 且 $A\setminus{B}\in\mathcal{M}$. 因 $A\setminus{B}$ 可测, 用**定义 6.3.1 (卡拉西奥多里条件)** 于 $T=X$:

$$
\mu^{*}\left(X\right)=\mu^{*}\left(X\cap\left(A\setminus{B}\right)\right)+\mu^{*}\left(X\cap\left(A\setminus{B}\right)^{c}\right)=\mu\left(A\setminus{B}\right)+\mu^{*}\left(X\setminus\left(A\setminus{B}\right)\right).
$$

由 $\left(A\setminus{B}\right)\cap{E}=\emptyset$ 得 $E\subset{X}\setminus\left(A\setminus{B}\right)$, 据外测度单调性 (**定义 6.1.1 (外测度)** (2)) 有 $\mu^{*}\left(X\setminus\left(A\setminus{B}\right)\right)\ge\mu^{*}\left(E\right)=\mu^{*}\left(X\right)$. 代入上式得 $\mu\left(A\setminus{B}\right)\le0$, 故 $\mu\left(A\setminus{B}\right)=0$. 同理 $\mu\left(B\setminus{A}\right)=0$. 于是由**命题 5.2.1 (有限可加性)**,

$$
\mu\left(A\right)=\mu\left(A\cap{B}\right)+\mu\left(A\setminus{B}\right)=\mu\left(A\cap{B}\right)=\mu\left(B\right).
$$

$\blacksquare$

(b) 先证 $\nu$ 良定义: 若 $A\cap{E}=B\cap{E}$, 由 (a) 得 $\mu\left(A\right)=\mu\left(B\right)$, 故 $\nu$ 不依赖于代表元.

再证 $\mathcal{M}_{E}$ 是 $E$ 上的 $\sigma$-代数 (**定义 4.1.3 ($\sigma$-代数)**): 因 $E=X\cap{E}\in\mathcal{M}_{E}$; 对 $A\cap{E}\in\mathcal{M}_{E}$, 其在 $E$ 内的补为 $E\setminus\left(A\cap{E}\right)=\left(X\setminus{A}\right)\cap{E}\in\mathcal{M}_{E}$; 且 $\bigcup_{n}\left(A_{n}\cap{E}\right)=\left(\bigcup_{n}A_{n}\right)\cap{E}\in\mathcal{M}_{E}$. 故 $\mathcal{M}_{E}$ 是 $E$ 上的 $\sigma$-代数.

最后证 $\nu$ 是 $\mathcal{M}_{E}$ 上的测度 (**定义 5.1.2 (测度)**). 非负性由 $\mu\ge0$; $\nu\left(\emptyset\right)=\mu\left(\emptyset\right)=0$. 设 $\left\{A_{n}\cap{E}\right\}$ 两两不交. 则对 $n\ne{m}$, $\left(A_{n}\cap{A}_{m}\right)\cap{E}=\left(A_{n}\cap{E}\right)\cap\left(A_{m}\cap{E}\right)=\emptyset$, 由 (a) 得 $\mu\left(A_{n}\cap{A}_{m}\right)=0$. 于是由**命题 5.2.1 (有限可加性)** 与**命题 5.2.4 (下连续性)**,

$$
\nu\left(\bigcup_{n}\left(A_{n}\cap{E}\right)\right)=\nu\left(\left(\bigcup_{n}A_{n}\right)\cap{E}\right)=\mu\left(\bigcup_{n}A_{n}\right)=\sum_{n}\mu\left(A_{n}\right)=\sum_{n}\nu\left(A_{n}\cap{E}\right).
$$

故 $\nu$ 是测度.

$\blacksquare$
