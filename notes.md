# 实变函数

## 集合与预备知识

**定理 1.2.9** (德摩根定律)

$$
\begin{aligned}\left(A\cup B\right)^{c}&=A^{c}\cap B^{c},\\
\left(A\cap B\right)^{c}&=A^{c}\cup B^{c}.
\end{aligned}
$$

**定义 1.3.1** (上极限)

集列 $\left\{E_{n}\right\}$ 的上极限定义为

$$
\begin{aligned}&\quad\;\overline{\lim}_{n\to\infty}E_{n}\\
&=\left\{x:x\text{ 属于无穷多个 }E_{n}\right\}\\
&=\bigcap_{n=1}^{\infty}\bigcup_{k=n}^{\infty}E_{k}.
\end{aligned}
$$

**定义 1.3.3** (下极限)

$$
\begin{aligned}&\quad\;\underline{\lim}_{n\to\infty}E_{n}\\
&=\left\{x:x\text{ 仅不属于有限多个 }E_{n}\right\}\\
&=\bigcup_{n=1}^{\infty}\bigcap_{k=n}^{\infty}E_{k}.
\end{aligned}
$$

**定理 2.4.2** (原像运算的性质)

设 $f:A\to B$, 则

$$
\begin{aligned}f^{-1}\left(B_{1}\cup B_{2}\right)&=f^{-1}\left(B_{1}\right)\cup f^{-1}\left(B_{2}\right),\\
f^{-1}\left(B_{1}\cap B_{2}\right)&=f^{-1}\left(B_{1}\right)\cap f^{-1}\left(B_{2}\right),\\
f^{-1}\left(B^{c}\right)&=\left(f^{-1}\left(B\right)\right)^{c},\\
f^{-1}\left(\bigcup_{\alpha\in I}B_{\alpha}\right)&=\bigcup_{\alpha\in I}f^{-1}\left(B_{\alpha}\right),\\
f^{-1}\left(\bigcap_{\alpha\in I}B_{\alpha}\right)&=\bigcap_{\alpha\in I}f^{-1}\left(B_{\alpha}\right).
\end{aligned}
$$

**定理 3.2.1** (实数中开集的构造)

设 $U\subset\mathbb R$ 是非空开集, 则存在一列互不相交的开区间 $\left\{I_{n}\right\}_{n=1}^{\infty}$, 使 $U=\bigcup_{n=1}^{\infty}I_{n}$; 且此表示在重排意义下唯一.

## 代数与可测结构

**定义 4.1.1** (集合代数)

设 $X$ 非空, $\mathcal A\subset\mathcal P\left(X\right)$. 称 $\mathcal A$ 为 $X$ 上的一个**集合代数** (布尔代数), 若满足:

(1) $X\in\mathcal A$;

(2) 对差运算封闭: $A,B\in\mathcal A\Rightarrow A\setminus B\in\mathcal A$;

(3) 对有限并封闭: $A,B\in\mathcal A\Rightarrow A\cup B\in\mathcal A$.

**命题 4.1.2** (代数的等价定义)

设 $\mathcal A\subset\mathcal P\left(X\right)$, 则以下条件等价:

(1) $\mathcal A$ 是代数;

(2) $\mathcal A$ 满足: (a) $X\in\mathcal A$; (b) 对补运算封闭: $A\in\mathcal A\Rightarrow A^{c}=X\setminus A\in\mathcal A$; (c) 对有限并封闭: $A,B\in\mathcal A\Rightarrow A\cup B\in\mathcal A$.

**定义 4.1.3** ($\sigma$-代数)

设 $X$ 非空, $\mathcal F\subset\mathcal P\left(X\right)$. 称 $\mathcal F$ 为 $X$ 上的一个 **$\sigma$-代数**, 若满足:

(1) $X\in\mathcal F$;

(2) 对补运算封闭: $A\in\mathcal F\Rightarrow A^{c}\in\mathcal F$;

(3) 对可数并封闭:

$$
\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal F\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal F.
$$

称 $\left(X,\mathcal F\right)$ 为**可测空间**, $\mathcal F$ 中的元素称为**可测集**.

**定义 4.2.1** (生成代数)

包含 $\mathcal E\subset\mathcal P\left(X\right)$ 的最小代数称为由 $\mathcal E$ 生成的代数, 记作 $\alpha\left(\mathcal E\right)$:

$$
\alpha\left(\mathcal E\right)=\bigcap\left\{\mathcal A\subset\mathcal P\left(X\right):\mathcal A\text{ 是代数且 }\mathcal E\subset\mathcal A\right\}.
$$

**定义 4.2.2** (生成 $\sigma$-代数)

包含 $\mathcal E\subset\mathcal P\left(X\right)$ 的最小 $\sigma$-代数称为由 $\mathcal E$ 生成的 $\sigma$-代数, 记作 $\sigma\left(\mathcal E\right)$:

$$
\sigma\left(\mathcal E\right)=\bigcap\left\{\mathcal F\subset\mathcal P\left(X\right):\mathcal F\text{ 是 $\sigma$-代数且 }\mathcal E\subset\mathcal F\right\}.
$$

**定义 4.3.2** (博雷尔 $\sigma$-代数)

设 $\left(X,\tau\right)$ 是拓扑空间, 由所有开集生成的 $\sigma$-代数称为 **博雷尔 $\sigma$-代数**, 记作 $\mathcal B\left(X\right)$, 其中元素称为 **博雷尔集**.

**例 4.3.3** (实数上的博雷尔代数)

在 $\mathbb R$ 上, 以下集合族生成相同的博雷尔 $\sigma$-代数 $\mathcal B\left(\mathbb R\right)$: 所有开集 $\tau$、所有闭集 $\mathcal F$、所有开区间 $\left\{\left(a,b\right)\right\}$、所有闭区间 $\left\{\left[a,b\right]\right\}$、所有左开右闭区间 $\left\{\left(a,b\right]\right\}$, 即

$$
\begin{aligned}&\quad\;\mathcal B\left(\mathbb R\right)\\
&=\sigma\left(\tau\right)\\
&=\sigma\left(\mathcal F\right)\\
&=\sigma\left(\left\{\left(a,b\right)\right\}\right)\\
&=\sigma\left(\left\{\left[a,b\right]\right\}\right)\\
&=\sigma\left(\left\{\left(a,b\right]\right\}\right).\end{aligned}
$$

**定义 4.4.1** (单调类)

设 $\mathcal M\subset\mathcal P\left(X\right)$. 称 $\mathcal M$ 为**单调类**, 若满足:

(1) 对单调递增序列封闭: $A_{1}\subset A_{2}\subset\cdots$ 且

$$
A_{n}\in\mathcal M\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal M;
$$

(2) 对单调递减序列封闭: $A_{1}\supset A_{2}\supset\cdots$ 且

$$
A_{n}\in\mathcal M\Rightarrow\bigcap_{n=1}^{\infty}A_{n}\in\mathcal M.
$$

**定理 4.4.2** (单调类定理)

设 $\mathcal A$ 是一个代数, $\mathcal M$ 是一个包含 $\mathcal A$ 的单调类, 则 $\sigma\left(\mathcal A\right)\subset\mathcal M$.

**定义 4.5.1 / 4.5.2** (可测矩形与乘积 $\sigma$-代数)

设 $\left(X,\mathcal F\right)$、$\left(Y,\mathcal G\right)$ 为可测空间. $A\times B\subseteq X\times Y$ 称为**可测矩形**, 若 $A\in\mathcal F$ 且 $B\in\mathcal G$.**乘积 $\sigma$-代数**为包含所有可测矩形的最小 $\sigma$-代数:

$$
\mathcal F\otimes\mathcal G:=\sigma\left(\left\{A\times B:A\in\mathcal F,B\in\mathcal G\right\}\right).
$$

**定义 4.5.2** (乘积 $\sigma$-代数)

乘积 $\sigma$-代数 $\mathcal F\otimes\mathcal G$ 是包含所有可测矩形的最小 $\sigma$-代数:

$$
\mathcal F\otimes\mathcal G:=\sigma\left(\left\{A\times B:A\in\mathcal F,B\in\mathcal G\right\}\right).
$$

**定理 4.5.3** (截面可测性)

若 $E\in\mathcal F\otimes\mathcal G$, 则对任意 $x\in X$、$y\in Y$, 其截面都可测:

$$
\begin{aligned}E_{x}&=\left\{y\in Y:\left(x,y\right)\in E\right\}\in\mathcal G,\\
E^{y}&=\left\{x\in X:\left(x,y\right)\in E\right\}\in\mathcal F.\end{aligned}
$$

**定理 4.5.4** (博雷尔集的乘积)

对欧氏空间中的博雷尔 $\sigma$-代数, 有

$$
\mathcal B\left(\mathbb R^{m}\right)\otimes\mathcal B\left(\mathbb R^{n}\right)=\mathcal B\left(\mathbb R^{m+n}\right).
$$

**定义 4.5.7** (任意乘积 $\sigma$-代数)

设

$$
\left\{\left(X_{\alpha},\mathcal F_{\alpha}\right)\right\}_{\alpha\in I}
$$

是一族可测空间, 乘积 $\sigma$-代数

$$
\bigotimes_{\alpha\in I}\mathcal F_{\alpha}
$$

是由所有**柱集**

$$
\left\{x=\left(x_{\alpha}\right)_{\alpha\in I}\in\prod_{\alpha\in I}X_{\alpha}:x_{\beta}\in A_{\beta}\right\},\quad A_{\beta}\in\mathcal F_{\beta},\quad\beta\in I
$$

生成的 $\sigma$-代数.

## 测度与可测集

**定义 5.1.2** (测度)

设 $\left(X,\mathcal F\right)$ 是可测空间. 函数 $\mu:\mathcal F\to\left[0,+\infty\right]$ 称为 $\left(X,\mathcal F\right)$ 上的一个测度, 若满足:

(1) 非负性: $\mu\left(E\right)\ge0$ 对一切 $E\in\mathcal F$;

(2) 零空集性: $\mu\left(\varnothing\right)=0$;

(3) 可数可加性 ($\sigma$-可加性): 对任意可数个两两不交的 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$, 有

$$
\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu\left(E_{n}\right).
$$

**定义 5.1.5** (σ-有限测度)

设 $\left(X,\mathcal F,\mu\right)$ 是测度空间. 如果存在一列可测集 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$ 使得 $X=\bigcup_{n=1}^{\infty}E_{n}$ 且 $\mu\left(E_{n}\right)< +\infty$ 对所有 $n\in\mathbb N$ 成立, 则称 $\mu$ 为 σ-有限测度.

**命题 5.2.1** (有限可加性)

设 $\mu$ 是 $\left(X,\mathcal F\right)$ 上的测度, $E_{1},\dots,E_{n}\in\mathcal F$ 是两两不交的集合, 则

$$
\mu\left(\bigcup_{k=1}^{n}E_{k}\right)=\sum_{k=1}^{n}\mu\left(E_{k}\right).
$$

**命题 5.2.2** (单调性)

设 $\mu$ 是测度, $E,F\in\mathcal F$ 且 $E\subset F$, 则 $\mu\left(E\right)\le\mu\left(F\right)$. 若进一步 $\mu\left(E\right)< +\infty$, 则

$$
\mu\left(F\setminus E\right)=\mu\left(F\right)-\mu\left(E\right).
$$

**命题 5.2.3** (次可数可加性)

设 $\mu$ 是测度, $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$ 是任意可数个集合 (不一定两两不交), 则

$$
\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)\le\sum_{n=1}^{\infty}\mu\left(E_{n}\right).
$$

**命题 5.2.4** (下连续性)

设 $\mu$ 是测度, $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$ 是单调递增的集合序列 (即 $E_{1}\subset E_{2}\subset\cdots$), 则

$$
\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\lim_{n\to\infty}\mu\left(E_{n}\right).
$$

**命题 5.2.5** (上连续性)

设 $\mu$ 是测度, $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$ 是单调递减的集合序列 (即 $E_{1}\supset E_{2}\supset\cdots$), 且存在某个 $m$ 使得 $\mu\left(E_{m}\right)< +\infty$, 则

$$
\mu\left(\bigcap_{n=1}^{\infty}E_{n}\right)=\lim_{n\to\infty}\mu\left(E_{n}\right).
$$

**定义 5.4.1** (零集)

设 $\left(X,\mathcal F,\mu\right)$ 是测度空间. 集合 $N\in\mathcal F$ 称为零集, 若 $\mu\left(N\right)=0$.

**定义 5.4.2** (零测度集)

集合 $A\subset X$ 称为零测度集, 若存在 $N\in\mathcal F$ 使得 $A\subset N$ 且 $\mu\left(N\right)=0$.

**定义 5.4.4** (完备测度)

测度空间 $\left(X,\mathcal F,\mu\right)$ 称为完备的, 若对任意满足 $\mu\left(N\right)=0$ 的 $N\in\mathcal F$, 以及任意 $A\subset N$, 都有 $A\in\mathcal F$.

## 勒贝格测度与正则性

**定义 6.1.1** (外测度)

设 $X$ 非空. 函数 $\mu^{*}:\mathcal P\left(X\right)\to\left[0,+\infty\right]$ 称为 $X$ 上的一个**外测度**, 若满足:

(1) 非负性: $\mu^{*}\left(\varnothing\right)=0$, 且 $\mu^{*}\left(E\right)\ge0$ 对一切 $E\subset X$;

(2) 单调性:

$$
E\subset F\Rightarrow\mu^{*}\left(E\right)\le\mu^{*}\left(F\right);
$$

(3) 次可数可加性:

$$
\mu^{*}\left(\bigcup_{n=1}^{\infty}E_{n}\right)\le\sum_{n=1}^{\infty}\mu^{*}\left(E_{n}\right).
$$

**定义 6.2.1** (准测度)

设 $X$ 非空, $\mathcal E\subset\mathcal P\left(X\right)$ 是一个代数. 函数 $\mu_{0}:\mathcal E\to\left[0,+\infty\right]$ 称为一个**准测度**, 若:

(1) $\mu_{0}\left(\varnothing\right)=0$;

(2) 若 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal E$ 两两不交且

$$
\bigcup_{n=1}^{\infty}E_{n}\in\mathcal E
$$

, 则

$$
\mu_{0}\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu_{0}\left(E_{n}\right).
$$

**定理 6.2.2** (由准测度生成外测度)

设 $\mathcal E\subset\mathcal P\left(X\right)$ 是一个覆盖类, $\mu_{0}:\mathcal E\to\left[0,+\infty\right]$ 是一个准测度. 对任意 $A\subset X$, 定义

$$
\mu^{*}\left(A\right)=\inf\left\{\sum_{n=1}^{\infty}\mu_{0}\left(E_{n}\right):E_{n}\in\mathcal E,A\subset\bigcup_{n=1}^{\infty}E_{n}\right\}.
$$

则 $\mu^{*}$ 是 $X$ 上的外测度, 且 $\mu^{*}|_{\mathcal E}=\mu_{0}$.

**定义 6.3.1** (卡拉西奥多里条件)

设 $\mu^{*}$ 是 $X$ 上的外测度. 子集 $A\subset X$ 称为 $\mu^{*}$-**可测**的, 若对任意 $T\subset X$ 有

$$
\mu^{*}\left(T\right)=\mu^{*}\left(T\cap A\right)+\mu^{*}\left(T\cap A^{c}\right).
$$

所有 $\mu^{*}$-可测集组成的集合记为 $\mathcal M_{\mu^{*}}$.

**引理 6.3.2**

如果 $\mathcal E$ 是代数, $\mu_{0}$ 是准测度, 则 $\mathcal E\subset\mathcal M_{\mu^{*}}$.

**定理 6.3.3** (卡拉西奥多里定理)

设 $\mu^{*}$ 是 $X$ 上的外测度, 则:

(1) $\mathcal M$ 是一个 $\sigma$-代数;

(2) $\mu^{*}|_{\mathcal M}$ 是一个完备测度;

(3) 如果 $\mu^{*}$ 是由准测度 $\mu_{0}$ 生成的, 且 $\mu_{0}$ 是 $\sigma$-有限的, 则 $\mu^{*}|_{\mathcal M}$ 是 $\mu_{0}$ 的唯一延拓.

**定义 6.4.1** (h 区间)

令 $-\infty\le a<  b<  \infty$, 所有左开右闭区间 $\left(a,b\right]$, 以及 $\left(a,\infty\right)$, $\varnothing$ 称为 **h 区间**. h 区间的有限不交并形成的集族 $\mathcal E$ 为一个代数.

**命题 6.4.2** ($\mathcal E$ 上的准测度)

设 $F:\mathbb R\to\mathbb R$ 为增的右连续函数. 对于不交区间 $\left(a_{i},b_{i}\right]$, $i=1,\dots,n$, 定义

$$
\mu_{0}\left(\bigcup_{i=1}^{n}\left(a_{i},b_{i}\right]\right):=\sum_{i=1}^{n}\left[F\left(b_{i}\right)-F\left(a_{i}\right)\right]
$$

, 并令 $\mu_{0}\left(\varnothing\right)=0$. 则 $\mu_{0}$ 为 $\mathcal E$ 上的准测度.

**定理 6.4.5** (勒贝格-斯蒂尔杰斯测度的正则性)

设 $F:\mathbb R\to\mathbb R$ 是右连续单调递增函数, $\mu_{F}$ 是由 $F$ 生成的勒贝格-斯蒂尔杰斯测度, $\mathcal M^{*}$ 是 $\mu_{F}$-可测集的 $\sigma$-代数. 若 $E\in\mathcal M^{*}$, 则

$$
\begin{aligned}&\quad\;\mu_{F}\left(E\right)\\
&=\inf\left\{\mu_{F}\left(U\right):E\subset U,U\text{开}\right\}\\
&=\sup\left\{\mu_{F}\left(K\right):K\subset E,K\text{紧}\right\}.\end{aligned}
$$

**定义 6.4.6** (勒贝格测度)

由 $F\left(x\right)=x$ 生成的测度称为**勒贝格测度**, 记作 $m$; 相应外测度定义的可测集称为**勒贝格可测集**, 全体记作 $\mathcal L$.

**定义 6.5.1** (康托尔集的递归构造)

设 $C_{0}=\left[0,1\right]$. 对每个 $n\ge0$, 定义

$$
C_{n+1}=\frac{1}{3}C_{n}\cup\left(\frac{2}{3}+\frac{1}{3}C_{n}\right)
$$

. 则**康托尔集**定义为 $C=\bigcap_{n=0}^{\infty}C_{n}$.

**定理 6.5.2** (康托尔集的三进制刻画)

点 $x\in\left[0,1\right]$ 属于康托尔集 $C$ 当且仅当它的三进制展开

$$
x=\sum_{k=1}^{\infty}\frac{a_{k}}{3^{k}}
$$

中不含数字 $1$ (即 $a_{k}\in\left\{0,2\right\}$).

## 可测函数

**定义 7.1.1** (可测映射)

设 $\left(X,\mathcal F\right)$, $\left(Y,\mathcal G\right)$ 为两个可测空间. 映射 $f:X\to Y$ 称为 $\left(\mathcal F,\mathcal G\right)$-**可测**的, 若对任意 $B\in\mathcal G$ 有 $f^{-1}\left(B\right)\in\mathcal F$.

**命题 7.1.5** (复合保持可测性)

若 $f:X\to Y$ 是 $\left(\mathcal F,\mathcal G\right)$-可测的, $g:Y\to Z$ 是 $\left(\mathcal G,\mathcal H\right)$-可测的, 则 $g\circ f:X\to Z$ 是 $\left(\mathcal F,\mathcal H\right)$-可测的.

**命题 7.1.7** (乘积空间的可测性)

设

$$
f=\left(f_{1},\dots,f_{n}\right):X\to Y_{1}\times\cdots\times Y_{n}
$$

. 在乘积空间配备乘积 $\sigma$-代数下, $f$ 可测当且仅当每个坐标映射 $f_{i}:X\to Y_{i}$ 可测.

**定理 7.1.8** (实值可测函数的运算封闭性)

设 $f,g:X\to\mathbb R$ 可测, $c\in\mathbb R$, 则:

(1) $cf$, $f+g$, $fg$, $\max\left(f,g\right)$, $\min\left(f,g\right)$ 可测;

(2) 若 $g\left(x\right)\ne0$ 对所有 $x$, 则 $f/g$ 可测;

(3) 若 $\left\{f_{n}\right\}$ 可测, 则 $\sup_{n}f_{n}$, $\inf_{n}f_{n}$, $\limsup_{n\to\infty}f_{n}$, $\liminf_{n\to\infty}f_{n}$ 可测;

(4) 若 $\left\{f_{n}\right\}$ 点点收敛, 则极限函数 $\lim_{n\to\infty}f_{n}$ 可测.

**定理 7.1.9** (可测函数与连续函数的复合)

设 $f:X\to\mathbb R$ 可测, $g:\mathbb R\to\mathbb R$ 连续, 则 $g\circ f:X\to\mathbb R$ 可测.

**定理 7.2.2** (可测函数的构造)

若 $f:X\to\left[0,+\infty\right]$ 是非负可测函数, 则存在一列非负简单函数 $\left\{f_{n}\right\}$ 满足 $0\le f_{1}\le f_{2}\le\cdots\le f$ 且

$$
\lim_{n\to\infty}f_{n}\left(x\right)=f\left(x\right)
$$

对每个 $x\in X$ 成立.

**例 7.3.5** (示性函数)

设 $A\subset X$, 则 $\chi_{A}:X\to\mathbb R$ 可测当且仅当 $A\in\mathcal F$.

## 勒贝格积分与收敛定理

**定义 8.1.1** (非负简单函数的积分)

设 $f=\sum_{i=1}^{n}c_{i}\chi_{A_{i}}$ 是非负简单函数, 其中 $c_{i}\ge0$, $A_{i}\in\mathcal F$ 互不相交且 $\bigcup_{i}A_{i}=X$. 定义 $f$ 关于 $\mu$ 的积分为

$$
\int_{X}f\,\mathrm{d}\mu=\sum_{i=1}^{n}c_{i}\mu\left(A_{i}\right)
$$

, 并约定 $0\cdot\infty=0$.

**命题 8.1.2** (线性性)

设 $f,g$ 为非负简单函数, $\alpha,\beta\ge0$, 则

$$
\int_{X}\left(\alpha f+\beta g\right)\mathrm{d}\mu=\alpha\int_{X}f\,\mathrm{d}\mu+\beta\int_{X}g\,\mathrm{d}\mu.
$$

**定义 8.2.1** (非负可测函数的积分)

设 $f:X\to\left[0,+\infty\right]$ 是非负可测函数. 定义 $f$ 关于 $\mu$ 的积分为

$$
\int_{X}f\,\mathrm{d}\mu=\sup\left\{\int_{X}\phi\,\mathrm{d}\mu:\phi\text{是简单函数},0\le\phi\le f\right\}
$$

. 若 $\int_{X}f\,\mathrm{d}\mu< \infty$, 则称 $f$ 是可积的.

**定理 8.2.2** (单调收敛定理)

设 $\left(X,\mathcal F,\mu\right)$ 是测度空间, $\left\{f_{n}\right\}$ 是一列非负可测函数, 满足 $0\le f_{1}\left(x\right)\le f_{2}\left(x\right)\le\cdots$ 对所有 $x\in X$ 成立, 且 $f_{n}\to f$ 点点收敛. 则

$$
\lim_{n\to\infty}\int_{X}f_{n}\,\mathrm{d}\mu=\int_{X}f\,\mathrm{d}\mu.
$$

**注 8.2.3**

单调收敛定理告诉我们积分可以用简单函数逼近.

**命题 8.2.4** (绝对连续性)

设 $f$ 为非负可测函数, 则 $A\mapsto\int_{A}f\,\mathrm{d}\mu$ 为一个测度; 若 $\mu\left(A\right)=0$, 则 $\int_{A}f\,\mathrm{d}\mu=0$.

**定义 8.2.5** (一般可测函数的积分)

设 $f:X\to\left[-\infty,+\infty\right]$ 是可测函数. 定义 $f$ 的正部和负部分别为 $f^{+}\left(x\right)=\max\left\{f\left(x\right),0\right\}$, $f^{-}\left(x\right)=\max\left\{-f\left(x\right),0\right\}$. 若至少有一个积分 $\int_{X}f^{+}\mathrm{d}\mu$, $\int_{X}f^{-}\mathrm{d}\mu$ 有限, 则定义 $f$ 的积分为

$$
\int_{X}f\,\mathrm{d}\mu=\int_{X}f^{+}\mathrm{d}\mu-\int_{X}f^{-}\mathrm{d}\mu
$$

. 若 $\int_{X}f^{+}\mathrm{d}\mu< \infty$ 且 $\int_{X}f^{-}\mathrm{d}\mu< \infty$, 则称 $f$ 是可积的.

**定理 8.2.7** (法图引理)

设 $\left(X,\mathcal F,\mu\right)$ 是测度空间, $\left\{f_{n}\right\}$ 是一列非负可测函数, 则

$$
\int_{X}\liminf_{n\to\infty}f_{n}\,\mathrm{d}\mu\le\liminf_{n\to\infty}\int_{X}f_{n}\,\mathrm{d}\mu.
$$

**定理 8.2.9** (控制收敛定理)

设 $\left(X,\mathcal F,\mu\right)$ 是测度空间, $\left\{f_{n}\right\}$ 是一列可测函数, $f_{n}\to f$ 几乎处处. 如果存在可积函数 $g$ 使得对所有 $n$ 有 $\left|f_{n}\right|\le g$ 几乎处处, 则

$$
\lim_{n\to\infty}\int_{X}f_{n}\,\mathrm{d}\mu=\int_{X}f\,\mathrm{d}\mu.
$$

**引理 8.2.13** (级数逐项积分)

设 $\left\{f_{n}\right\}$ 是一列可测函数, 且

$$
\sum_{n=1}^{\infty}\int_{X}\left|f_{n}\right|\mathrm{d}\mu< \infty
$$

, 则

$$
\int_{X}\left(\sum_{n=1}^{\infty}f_{n}\right)\mathrm{d}\mu=\sum_{n=1}^{\infty}\int_{X}f_{n}\,\mathrm{d}\mu.
$$

**定理 8.2.16**

如果 $f\in L^{1}\left(\mu\right)$ 且 $\epsilon> 0$, 则存在可积简单函数 $\varphi=\sum a_{j}\chi_{E_{j}}$ 使得

$$
\int\left|f-\varphi\right|\mathrm{d}\mu< \epsilon
$$

(即可积简单函数在 $L^{1}$ 度量下稠密).

**定理 8.2.17** (参数积分)

设 $f:X\times\left[a,b\right]\to\mathbb R$, 且对每个 $t\in\left[a,b\right]$, 函数 $f\left(\cdot,t\right):X\to\mathbb R$ 可积. 令

$$
F\left(t\right)=\int_{X}f\left(x,t\right)\mathrm{d}\mu\left(x\right).
$$

(a) 若存在 $g\in L^{1}\left(\mu\right)$ 使得对所有 $x,t$ 有 $\left|f\left(x,t\right)\right|\le g\left(x\right)$, 且对每个 $x$ 有

$$
\lim_{t\to t_{0}}f\left(x,t\right)=f\left(x,t_{0}\right)
$$

, 则

$$
\lim_{t\to t_{0}}F\left(t\right)=F\left(t_{0}\right);
$$

(b) 若偏导数 $\partial f/\partial t$ 存在, 且存在 $g\in L^{1}\left(\mu\right)$ 使得对所有 $x,t$ 有

$$
\left|\frac{\partial f}{\partial t}\left(x,t\right)\right|\le g\left(x\right)
$$

, 则 $F$ 可微, 且

$$
F'\left(t\right)=\int\frac{\partial f}{\partial t}\left(x,t\right)\mathrm{d}\mu\left(x\right).
$$

## 函数列的收敛

**定义 9.1.1** (几乎处处收敛)

设 $\left\{f_{n}\right\}$ 是一列可测函数, $f$ 是可测函数. 如果存在零测度集 $E$ 使对所有 $x\notin E$ 有

$$
\lim_{n\to\infty}f_{n}\left(x\right)=f\left(x\right)
$$

, 则称 $\left\{f_{n}\right\}$ μ-几乎处处收敛到 $f$, 记作 $f_{n}\xrightarrow{\text{a.e.}}f$.

**命题 9.1.2** (几乎处处收敛的刻画)

$f_{n}\xrightarrow{\text{a.e.}}f$ 当且仅当对任意的 $\epsilon> 0$,

$$
\mu\left(\bigcap_{k=1}^{\infty}\bigcup_{n=k}^{\infty}\left\{x:\left|f_{n}\left(x\right)-f\left(x\right)\right|> \epsilon\right\}\right)=0.
$$

**定义 9.1.3** (依测度收敛)

设 $\left\{f_{n}\right\}$ 是一列可测函数, $f$ 是可测函数. 如果对任意 $\varepsilon> 0$ 有

$$
\lim_{n\to\infty}\mu\left(\left\{x:\left|f_{n}\left(x\right)-f\left(x\right)\right|> \varepsilon\right\}\right)=0
$$

, 则称 $\left\{f_{n}\right\}$ 依测度收敛到 $f$, 记作 $f_{n}\xrightarrow{\mu}f$.

**定理 9.1.8** (子序列性质)

如果 $f_{n}\xrightarrow{\mu}f$, 则存在子序列 $\left\{f_{n_{k}}\right\}$ 使得 $f_{n_{k}}\to f$ 几乎处处.

**定理 9.1.15** (叶戈罗夫定理)

设 $\mu\left(X\right)< \infty$ 且 $f_{n}\to f$ 几乎处处. 则对任意 $\delta> 0$ 存在可测集 $E\subset X$ 使得 $\mu\left(E\right)< \delta$, 且在 $X\setminus E$ 上 $f_{n}$ 一致收敛到 $f$. 特别地, 在有限测度空间中, 几乎处处收敛蕴含依测度收敛.

## 乘积测度与重积分

**定义 10.1.1** (乘积 σ-代数)

设 $\left(X,\mathcal A,\mu\right)$ 和 $\left(Y,\mathcal B,\nu\right)$ 是两个测度空间. 乘积空间 $X\times Y$ 上的乘积 σ-代数定义为

$$
\mathcal A\otimes\mathcal B=\sigma\left(\left\{A\times B:A\in\mathcal A,B\in\mathcal B\right\}\right)
$$

, 即由所有可测矩形生成的 σ-代数.

**定义 10.1.2** (截面)

对于 $E\subseteq X\times Y$, 定义 $E$ 的 x-截面 $E_{x}=\left\{y\in Y:\left(x,y\right)\in E\right\}$ 和 y-截面 $E^{y}=\left\{x\in X:\left(x,y\right)\in E\right\}$.

**定理 10.1.4** (乘积测度的存在唯一性)

设 $\left(X,\mathcal A,\mu\right)$ 和 $\left(Y,\mathcal B,\nu\right)$ 是 σ-有限的测度空间. 存在唯一的测度 $\mu\times\nu$ 在 $\left(X\times Y,\mathcal A\otimes\mathcal B\right)$ 上, 使得对所有 $A\in\mathcal A$, $B\in\mathcal B$ 有

$$
\left(\mu\times\nu\right)\left(A\times B\right)=\mu\left(A\right)\nu\left(B\right)
$$

. 其构造为

$$
\phi\left(E\right)=\int_{X}\nu\left(E_{x}\right)\mathrm{d}\mu\left(x\right)
$$

对 $E\in\mathcal A\otimes\mathcal B$.

**定理 10.2.1** (富比尼定理)

设 $\left(X,\mathcal A,\mu\right)$ 和 $\left(Y,\mathcal B,\nu\right)$ 是 σ-有限的测度空间, $f:X\times Y\to\mathbb R$ 是 $\mathcal A\otimes\mathcal B$-可测函数. 若 $f$ 在 $X\times Y$ 上可积, 即

$$
\int_{X\times Y}\left|f\right|\mathrm{d}\left(\mu\times\nu\right)< \infty
$$

, 则对几乎所有 $x$, $y\mapsto f\left(x,y\right)$ 是 ν-可积的; 对几乎所有 $y$, $x\mapsto f\left(x,y\right)$ 是 μ-可积的; 且重积分相等:

$$
\begin{aligned}&\quad\;\int_{X\times Y}f\,\mathrm{d}\left(\mu\times\nu\right)\\
&=\int_{X}\left(\int_{Y}f\left(x,y\right)\mathrm{d}\nu\left(y\right)\right)\mathrm{d}\mu\left(x\right)\\
&=\int_{Y}\left(\int_{X}f\left(x,y\right)\mathrm{d}\mu\left(x\right)\right)\mathrm{d}\nu\left(y\right).\end{aligned}
$$

**定理 10.2.2** (托内利定理)

如果 $f:X\times Y\to\left[0,\infty\right]$ 是 $\mathcal A\otimes\mathcal B$-可测的, 则

$$
\begin{aligned}&\quad\;\int_{X\times Y}f\,\mathrm{d}\left(\mu\times\nu\right)\\
&=\int_{X}\left(\int_{Y}f\left(x,y\right)\mathrm{d}\nu\left(y\right)\right)\mathrm{d}\mu\left(x\right)\\
&=\int_{Y}\left(\int_{X}f\left(x,y\right)\mathrm{d}\mu\left(x\right)\right)\mathrm{d}\nu\left(y\right),\end{aligned}
$$

 其中所有积分值都在 $\left[0,\infty\right]$ 中.

## 符号测度与拉东-尼科迪姆定理

**定义 11.1.1** (符号测度)

设 $\left(X,\mathcal F\right)$ 是一个可测空间. 函数 $\nu:\mathcal F\to\mathbb R\cup\left\{+\infty\right\}$ 或 $\mathbb R\cup\left\{-\infty\right\}$ 称为**符号测度**, 若满足:

(1) $\nu\left(\varnothing\right)=0$;

(2) 可列可加性: 对任意一列互不相交的可测集 $\left\{E_{i}\right\}_{i=1}^{\infty}\subset\mathcal F$, 有

$$
\nu\left(\bigcup_{i=1}^{\infty}E_{i}\right)=\sum_{i=1}^{\infty}\nu\left(E_{i}\right);
$$

(3) $\nu$ 不能同时取 $+\infty$ 与 $-\infty$ 为值.

**命题 11.1.2** (符号测度的基本性质)

设 $\nu$ 是符号测度, 则:

(1) 有限可加性: 对任意有限个互不相交的 $E_{1},\dots,E_{n}\in\mathcal F$, 有

$$
\nu\left(\bigcup_{i=1}^{n}E_{i}\right)=\sum_{i=1}^{n}\nu\left(E_{i}\right);
$$

(2) 下连续性: 若 $\left\{E_{j}\right\}$ 单调上升可测, 则

$$
\lim_{j\to\infty}\nu\left(E_{j}\right)=\nu\left(\bigcup_{j}E_{j}\right);
$$

(3) 上连续性: 若 $\left\{E_{j}\right\}$ 单调下降可测且 $\nu\left(E_{1}\right)< \infty$, 则

$$
\lim_{j\to\infty}\nu\left(E_{j}\right)=\nu\left(\bigcap_{j}E_{j}\right).
$$

**定义 11.2.1** (正集、负集、零集)

设 $\nu$ 是 $\left(X,\mathcal F\right)$ 上的符号测度.
称 $P\in\mathcal F$ 为**正集** (记为 $P\gtrsim0$), 若对任意 $E\in\mathcal F$ 且 $E\subset P$, 有 $\nu\left(E\right)\ge0$;
称 $N\in\mathcal F$ 为**负集** (记为 $N\lesssim0$), 若对任意 $E\in\mathcal F$ 且 $E\subset N$, 有 $\nu\left(E\right)\le0$;
称 $Z\in\mathcal F$ 为**零集**, 若对任意 $E\in\mathcal F$ 且 $E\subset Z$, 有 $\nu\left(E\right)=0$.

**引理 11.2.2** (正集的性质)

(1) 正集的任意可测子集是正集;

(2) 正集的可列并是正集;

(3) 若 $\left\{P_{n}\right\}$ 是正集列, 则 $\bigcap_{n=1}^{\infty}P_{n}$ 是正集.
上述性质对负集仍然成立 (注 11.2.3).

**引理 11.2.4**

设 $\nu$ 是符号测度. 若 $E$ 不是负集, 则存在正集 $F\subset E$ 使得 $\nu\left(F\right)> 0$.

**定理 11.3.2** (哈恩分解定理)

设 $\nu$ 是 $\left(X,\mathcal F\right)$ 上的符号测度, 则存在 $X$ 的分解 $X=P\cup N$, 其中 $P$ 是正集, $N$ 是负集, $P\cap N=\varnothing$; 并且该分解在相差一个 $\nu$-零集的意义下是唯一的.

**定理 11.4.1**

存在 $S^{n-1}$ 上唯一的博雷尔测度 $\sigma=\sigma_{n-1}$, 使得 $m^{*}=\rho\times\sigma$. 若 $f$ 是 $\mathbb R^{n}$ 上的博雷尔可测函数, 且 $f\ge0$ 或 $f\in L^{1}\left(m\right)$, 则

$$
\int_{\mathbb R^{n}}f\left(x\right)\mathrm{d}x=\int_{0}^{\infty}\int_{S^{n-1}}f\left(rx'\right)r^{n-1}\mathrm{d}\sigma\left(x'\right)\mathrm{d}r.
$$

**定理 11.4.3** (若尔当分解定理)

设 $\nu$ 是 $\left(X,\mathcal F\right)$ 上的符号测度, 则存在唯一的一对相互奇异的正测度 $\nu^{+}$ 和 $\nu^{-}$, 使得 $\nu=\nu^{+}-\nu^{-}$.

**定义 11.4.4** (变差测度)

设 $\nu$ 是符号测度, 其 若尔当分解为 $\nu=\nu^{+}-\nu^{-}$.
称 $\nu^{+}$ 为 $\nu$ 的**正变差**, $\nu^{-}$ 为 $\nu$ 的**负变差**, $\left|\nu\right|=\nu^{+}+\nu^{-}$ 为 $\nu$ 的**全变差测度**.

**定义 11.5.1** (绝对连续性)

设 $\mu$ 是正测度, $\nu$ 是符号测度. 称 $\nu$ 关于 $\mu$ 绝对连续 (记为 $\nu\ll\mu$), 若对任意 $E\in\mathcal F$ 有 $\mu\left(E\right)=0\Rightarrow\nu\left(E\right)=0$.

**注 11.5.3**

设 $f\in L^{1}\left(\mu\right)$, 则

$$
\lim_{\mu\left(E\right)\to0}\int_{E}f\,\mathrm{d}\mu=0.
$$

**定理 11.5.5** (拉东-尼科迪姆定理)

设 $\mu$ 是 $\sigma$-有限正测度, $\nu$ 是符号测度且 $\nu\ll\mu$, 则存在可测函数 $f:X\to\mathbb R$ 使得

$$
\nu\left(E\right)=\int_{E}f\,\mathrm{d}\mu
$$

对一切 $E\in\mathcal F$ 成立; 且

$$
\nu^{+}\left(E\right)=\int_{E}f^{+}\mathrm{d}\mu,
$$

$$
\nu^{-}\left(E\right)=\int_{E}f^{-}\mathrm{d}\mu,
$$

$$
\left|\nu\right|\left(E\right)=\int_{E}\left|f\right|\mathrm{d}\mu
$$

. 函数 $f$ 称为 $\nu$ 关于 $\mu$ 的 拉东-尼科迪姆导数, 记作 $f=\frac{\mathrm{d}\nu}{\mathrm{d}\mu}$.

**性质 11.5.6** (线性性)

若 $\nu_{1},\nu_{2}\ll\mu$ 且 $a,b\in\mathbb R$, 则

$$
\frac{\mathrm{d}\left(a\nu_{1}+b\nu_{2}\right)}{\mathrm{d}\mu}=a\frac{\mathrm{d}\nu_{1}}{\mathrm{d}\mu}+b\frac{\mathrm{d}\nu_{2}}{\mathrm{d}\mu}
$$

$\mu$-几乎处处成立.

## 有界变差与绝对连续

**推论 13.4.5**

设 $F$ 是 $\mathbb R$ 上的右连续的增函数, 则对几乎所有的 $x$, $F'\left(x\right)$ 存在.

**定义 14.0.6** (有界变差函数)

设 $f:\left[a,b\right]\to\mathbb R$. 对 $\left[a,b\right]$ 的任意分划 $P:a=x_{0}< x_{1}< \cdots< x_{n}=b$, 定义变差

$$
V\left(f,P\right)=\sum_{i=1}^{n}\left|f\left(x_{i}\right)-f\left(x_{i-1}\right)\right|
$$

. $f$ 在 $\left[a,b\right]$ 上的全变差为

$$
V_{a}^{b}\left(f\right)=\sup_{P}V\left(f,P\right)
$$

. 若 $V_{a}^{b}\left(f\right)< +\infty$, 则称 $f$ 为 $\left[a,b\right]$ 上的有界变差函数, 记作 $f\in BV\left(\left[a,b\right]\right)$.

**定理 14.0.7** (基本性质)

设 $f,g\in BV\left(\left[a,b\right]\right)$, 则:

(1) $BV\left(\left[a,b\right]\right)$ 构成一个线性空间;

(2) $f$ 为有界函数;

(3) 若 $f$ 满足 利普希茨条件, 则 $f\in BV\left(\left[a,b\right]\right)$;

(4) 单调函数必为有界变差函数.

**定理 14.0.10** (间断点性质)

若 $f\in BV\left(\left[a,b\right]\right)$, 则:

(1) $f$ 的不连续点至多可数;

(2) 所有不连续点都是第一类间断点.

**定义 15.0.11** (绝对连续性)

函数 $f:\left[a,b\right]\to\mathbb R$ 称为**绝对连续的** (记 $f\in AC\left(\left[a,b\right]\right)$), 若对任意 $\varepsilon> 0$, 存在 $\delta> 0$, 使得对任意有限个互不相交的子区间 $\left(a_{i},b_{i}\right)\subset\left[a,b\right]$, 只要 $\sum_{i}\left(b_{i}-a_{i}\right)< \delta$, 就有

$$
\sum_{i}\left|f\left(b_{i}\right)-f\left(a_{i}\right)\right|< \varepsilon.
$$

**定理 15.0.14** (等价刻画)

$f\in AC\left(\left[a,b\right]\right)$ 当且仅当存在 $g\in L^{1}\left(\left[a,b\right]\right)$ 使得

$$
f\left(x\right)=f\left(a\right)+\int_{a}^{x}g\left(t\right)\mathrm{d}t
$$

对一切 $x\in\left[a,b\right]$ 成立. 此时 $f'\left(x\right)=g\left(x\right)$ 几乎处处成立.

**定理 15.0.16**

有以下严格包含关系: $C^{1}\left(\left[a,b\right]\right)\subset$ 利普希茨

$$
\subset AC\left(\left[a,b\right]\right)\subset BV\left(\left[a,b\right]\right)\subset
$$

有界函数.

## 基础知识

**基础知识**
**黎曼积分与达布和**: 设 $f$ 是 $\left[a,b\right]$ 上的有界实值函数. 对 $\left[a,b\right]$ 的一个分割 $P=\left\{t_{0}< \cdots<  t_{n}\right\}$, 记

$$
M_{i}=\sup_{\left[t_{i-1},t_{i}\right]}f,
$$

$$
m_{i}=\inf_{\left[t_{i-1},t_{i}\right]}f
$$

, 定义上达布和

$$
\overline S\left(P\right)=\sum_{i}M_{i}\left(t_{i}-t_{i-1}\right)
$$

, 下达布和

$$
\underline S\left(P\right)=\sum_{i}m_{i}\left(t_{i}-t_{i-1}\right)
$$

. 上积分

$$
\overline{\int}f=\inf_{P}\overline S\left(P\right)
$$

, 下积分

$$
\underline{\int}f=\sup_{P}\underline S\left(P\right)
$$

. 若 $\overline{\int}f=\underline{\int}f$, 其公共值称为 $f$ 的黎曼积分, 此时称 $f$ 黎曼可积.

**基础知识** (哈代-利特尔伍德极大函数)

设 $f\in L^{1}_{\mathrm{loc}}\left(\mathbb R^{n}\right)$. 定义 $f$ 的哈代-利特尔伍德极大函数

$$
Mf\left(x\right)=\sup_{r> 0}\frac{1}{\left|B\left(x,r\right)\right|}\int_{B\left(x,r\right)}\left|f\left(y\right)\right|\mathrm{d}y,
$$

其中 $B\left(x,r\right)$ 是以 $x$ 为中心、$r$ 为半径的开球, $\left|B\left(x,r\right)\right|$ 表示其勒贝格测度.

**基础知识** (球体积公式)

设 $C_{n}=m\left(B\left(1,0\right)\right)$ 为单位球的勒贝格测度, 则对任意 $x\in\mathbb R^{n}$, $r> 0$,

$$
m\left(B\left(x,r\right)\right)=C_{n}r^{n}.
$$

**基础知识** (正则博雷尔测度)

设 $\nu$ 是 $\mathbb R^{n}$ 上的博雷尔测度. 称 $\nu$ 为**正则的**, 若:

(1) 对每个紧集 $K$, 有 $\nu\left(K\right)< \infty$;

(2) 对每个 $E\in\mathcal B\left(\mathbb R^{n}\right)$, 有

$$
\nu\left(E\right)=\inf\left\{\nu\left(U\right):U\text{开集},E\subset U\right\}.
$$

**基础知识** (归一化的有界变差 $NBV$)

$$
NBV=\left\{F\in BV:F\text{右连续},F\left(-\infty\right)=0\right\}
$$

, 其中 $BV$ 指 $\mathbb R$ 上的有界变差函数, $T_{F}$ 表示 $F$ 的全变差函数.

**基础知识** (级数)

几何级数 $\sum_{n=1}^{\infty}2^{-n}=1$ 收敛; 调和级数 $\sum_{k}\frac{1}{k}$ 发散.

**基础知识** (归一化的有界变差 $NBV$ 与 斯蒂尔杰斯测度)

$$
NBV=\left\{F\in BV:F\ \text{右连续},\ F\left(-\infty\right)=0\right\}
$$

. 对递增右连续的 $F$, 由

$$
\mu_{F}\left(\left(a,b\right]\right)=F\left(b\right)-F\left(a\right)
$$

唯一确定一个正则博雷尔测度 $\mu_{F}$.

**基础知识** (绝对连续函数的全变差)

若 $F$ 在 $\left[a,b\right]$ 上绝对连续, 则 $F$ 的全变差

$$
V_{a}^{b}\left(F\right)=\int_{a}^{b}\left|F'\left(t\right)\right|\mathrm{d}t.
$$
