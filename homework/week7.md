# 作业 7

> **定义 5.1.2** (测度)<br>设 $\left(X,\mathcal F\right)$ 是一个可测空间. 函数 $\mu:\mathcal F\to\left[0,+\infty\right]$ 称为 $\left(X,\mathcal F\right)$ 上的一个测度, 如果满足:<br>(1) 非负性: $\mu\left(E\right)\ge0$ 对一切 $E\in\mathcal F$ 成立;<br>(2) 零空集性: $\mu\left(\emptyset\right)=0$;<br>(3) 可数可加性 (σ-可加性): 对任意可数个两两不交的集合 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$, 有 $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **定义 6.2.1** (准测度)<br>设 $X$ 是非空集合, $\mathcal E\subset\mathcal P\left(X\right)$ 是一个代数. 函数 $\mu_{0}:\mathcal E\to\left[0,+\infty\right]$ 称为一个准测度, 如果 $\mu_{0}\left(\emptyset\right)=0$, 且若 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal E$ 两两不交且 $\bigcup_{n=1}^{\infty}E_{n}\in\mathcal E$, 则 $\mu_{0}\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu_{0}\left(E_{n}\right)$.

> **定理 6.3.3** (卡拉西奥多里 定理)<br>设 $\mu^{*}$ 是 $X$ 上的外测度, 则 $\mathcal M$ (全部 $\mu^{*}$-可测集) 是一个 σ-代数, 且 $\mu^{*}|_{\mathcal M}$ 是一个完备测度. 如果 $\mu^{*}$ 是由准测度 $\mu_{0}$ 生成的, 且 $\mu_{0}$ 是 σ-有限的, 则 $\mu^{*}|_{\mathcal M}$ 是 $\mu_{0}$ 的唯一延拓.

> **命题 7.1.5** (复合保持可测性)<br>若 $f:X\to Y$ 是 $\left(\mathcal F,\mathcal G\right)$-可测的, $g:Y\to Z$ 是 $\left(\mathcal G,\mathcal H\right)$-可测的, 则 $g\circ f:X\to Z$ 是 $\left(\mathcal F,\mathcal H\right)$-可测的.

> **命题 7.1.7** (乘积空间的可测性)<br>设 $f=\left(f_{1},\dots,f_{n}\right):X\to Y_{1}\times\cdots\times Y_{n}$. 在乘积空间配备乘积 σ-代数下, $f$ 可测当且仅当每个坐标映射 $f_{i}:X\to Y_{i}$ 可测.

> **定义 10.1.1** (乘积 σ-代数)<br>设 $\left(X,\mathcal A,\mu\right)$ 和 $\left(Y,\mathcal B,\nu\right)$ 是两个测度空间. 乘积空间 $X\times Y$ 上的乘积 σ-代数定义为 $\mathcal A\otimes\mathcal B=\sigma\left(\left\{A\times B:A\in\mathcal A,B\in\mathcal B\right\}\right)$, 即由所有可测矩形生成的 σ-代数.

> **定义 10.1.2** (截面)<br>对于 $E\subseteq X\times Y$, 定义 $E$ 的 x-截面 $E_{x}=\left\{y\in Y:\left(x,y\right)\in E\right\}$ 和 y-截面 $E^{y}=\left\{x\in X:\left(x,y\right)\in E\right\}$.

> **定理 10.1.4** (乘积测度的存在唯一性)<br>设 $\left(X,\mathcal A,\mu\right)$ 和 $\left(Y,\mathcal B,\nu\right)$ 是 σ-有限的测度空间. 存在唯一的测度 $\mu\times\nu$ 在 $\left(X\times Y,\mathcal A\otimes\mathcal B\right)$ 上, 使得对所有 $A\in\mathcal A$, $B\in\mathcal B$ 有 $\left(\mu\times\nu\right)\left(A\times B\right)=\mu\left(A\right)\nu\left(B\right)$. 其构造为 $\phi\left(E\right)=\int_{X}\nu\left(E_{x}\right)\mathrm{d}\mu\left(x\right)$ 对 $E\in\mathcal A\otimes\mathcal B$.

> **定理 10.2.1** (富比尼定理)<br>设 $\left(X,\mathcal A,\mu\right)$ 和 $\left(Y,\mathcal B,\nu\right)$ 是 σ-有限的测度空间, $f:X\times Y\to\mathbb R$ 是 $\mathcal A\otimes\mathcal B$-可测函数. 若 $f$ 在 $X\times Y$ 上可积, 即 $\int_{X\times Y}\left|f\right|\mathrm{d}\left(\mu\times\nu\right)<\infty$, 则对几乎所有 $x$, $y\mapsto f\left(x,y\right)$ 是 ν-可积的; 对几乎所有 $y$, $x\mapsto f\left(x,y\right)$ 是 μ-可积的; 且重积分相等: $$\begin{aligned}&\quad\;\int_{X\times Y}f\,\mathrm{d}\left(\mu\times\nu\right)\\&=\int_{X}\left(\int_{Y}f\left(x,y\right)\mathrm{d}\nu\left(y\right)\right)\mathrm{d}\mu\left(x\right)\\&=\int_{Y}\left(\int_{X}f\left(x,y\right)\mathrm{d}\mu\left(x\right)\right)\mathrm{d}\nu\left(y\right).\end{aligned}$$

> **定理 10.2.2** (托内利定理)<br>如果 $f:X\times Y\to\left[0,\infty\right]$ 是 $\mathcal A\otimes\mathcal B$-可测的, 则 $$\begin{aligned}&\quad\;\int_{X\times Y}f\,\mathrm{d}\left(\mu\times\nu\right)\\&=\int_{X}\left(\int_{Y}f\left(x,y\right)\mathrm{d}\nu\left(y\right)\right)\mathrm{d}\mu\left(x\right)\\&=\int_{Y}\left(\int_{X}f\left(x,y\right)\mathrm{d}\mu\left(x\right)\right)\mathrm{d}\nu\left(y\right),\end{aligned}$$ 其中所有积分值都在 $\left[0,\infty\right]$ 中.

> **基础知识**<br>**矩形代数的交补性质**: 对可测矩形成立 $\left(A\times B\right)\cap\left(C\times D\right)=\left(A\cap C\right)\times\left(B\cap D\right)$ 与 $\left(A\times B\right)^{c}=\left(A^{c}\times B\right)\cup\left(A\times B^{c}\right)$.

> **基础知识**<br>**测度限制在代数上是准测度**: 若 $\lambda$ 是 σ-代数 $\mathcal M$ 上的测度, $\mathcal E\subset\mathcal M$ 是一个代数, 则 $\lambda|_{\mathcal E}$ 满足准测度条件 (零空集性与 σ-可加性在 $\mathcal E$ 内成立).

### 习题一

设 $\mathcal E$ 为所有矩形框的有限不交并全体, 证明 $\mathcal E$ 为一个代数. 对于 $E=\bigcup_{i=1}^{n}A_{i}\times B_{i}$ (两两不交), 定义

$$
\pi\left(E\right):=\sum_{i=1}^{n}\mu\left(A_{i}\right)\nu\left(B_{i}\right).
$$

证明 $\pi$ 为 $\mathcal E$ 上的准测度, 且由该准测度导出的 $\sigma\left(\mathcal E\right)$ 上的测度与定理 10.1.4 中定义的乘积测度一致.

### 解答 习题一

**$\mathcal E$ 是代数.** 由基础知识 (矩形代数的交补性质), 可测矩形之交仍是可测矩形, 可测矩形之补是两个可测矩形之并. 空集 $\emptyset$ 与全空间 $X\times Y$ 都在 $\mathcal E$ 中. 对 $\mathcal E$ 中元素做补、交、并运算, 先把每个元素写成有限不交矩形并, 再由矩形之交仍是矩形、公共细分后两两不交, 得到的结果仍是有限不交矩形并, 仍属于 $\mathcal E$. 故 $\mathcal E$ 是一个代数.

**$\pi$ 良定义.** 设 $E=\bigcup_{i=1}^{m}A_{i}\times B_{i}=\bigcup_{j=1}^{n}C_{j}\times D_{j}$ 是 $E$ 的两种两两不交矩形分解. 对公共细分 $\left\{\left(A_{i}\cap C_{j}\right)\times\left(B_{i}\cap D_{j}\right)\right\}_{i,j}$, 由 $\mu,\nu$ 的有限可加性,

$$
\begin{aligned}
&\quad\;\sum_{i=1}^{m}\mu\left(A_{i}\right)\nu\left(B_{i}\right)\\&=\sum_{i,j}\mu\left(A_{i}\cap C_{j}\right)\nu\left(B_{i}\cap D_{j}\right)\\&=\sum_{j=1}^{n}\mu\left(C_{j}\right)\nu\left(D_{j}\right),
\end{aligned}
$$

故 $\pi\left(E\right)$ 与分解无关.

**$\pi$ 是 $\mathcal E$ 上的准测度.** 由**定理 10.1.4**, $\mu\times\nu$ 是 $\left(X\times Y,\mathcal A\otimes\mathcal B\right)$ 上的测度且对矩形取 $\mu\left(A\right)\nu\left(B\right)$; 对有限不交矩形并 $\bigcup_{i=1}^{n}A_{i}\times B_{i}$, 由测度的有限可加性,

$$
\begin{aligned}
&\quad\;\left(\mu\times\nu\right)\left(\bigcup_{i=1}^{n}A_{i}\times B_{i}\right)\\&=\sum_{i=1}^{n}\mu\left(A_{i}\right)\nu\left(B_{i}\right)\\&=\pi\left(E\right),
\end{aligned}
$$

故 $\pi=\left(\mu\times\nu\right)|_{\mathcal E}$. 由基础知识 (测度限制在代数上是准测度), $\pi$ 满足准测度条件: $\pi\left(\emptyset\right)=0$, 且对两两不交的 $\left\{E_{n}\right\}\subset\mathcal E$ 且 $\bigcup_{n}E_{n}\in\mathcal E$, 由 $\mu\times\nu$ 的 σ-可加性 (**定义 5.1.2**),

$$
\begin{aligned}
&\quad\;\pi\left(\bigcup_{n=1}^{\infty}E_{n}\right)\\&=\left(\mu\times\nu\right)\left(\bigcup_{n=1}^{\infty}E_{n}\right)\\&=\sum_{n=1}^{\infty}\left(\mu\times\nu\right)\left(E_{n}\right)\\&=\sum_{n=1}^{\infty}\pi\left(E_{n}\right).
\end{aligned}
$$

故 $\pi$ 是 $\mathcal E$ 上的准测度 (**定义 6.2.1**).

**唯一延拓与乘积测度一致.** 由**定义 10.1.1**, $\mathcal E$ 由所有可测矩形生成, 故 $\sigma\left(\mathcal E\right)=\mathcal A\otimes\mathcal B$. 因 $\mu,\nu$ σ-有限, 可取 $X=\bigcup_{p}X_{p}$, $Y=\bigcup_{q}Y_{q}$ 使 $\mu\left(X_{p}\right),\nu\left(Y_{q}\right)<\infty$, 则矩形 $X_{p}\times Y_{q}$ 覆盖 $X\times Y$ 且 $\pi\left(X_{p}\times Y_{q}\right)<\infty$, 故 $\pi$ 是 σ-有限的. 由**定理 6.3.3** (卡拉西奥多里 定理, 准测度的唯一延拓), $\pi$ 在 $\sigma\left(\mathcal E\right)$ 上有唯一延拓. 该延拓在 $\mathcal E$ 上等于 $\pi=\left(\mu\times\nu\right)|_{\mathcal E}$, 故在整个 $\sigma\left(\mathcal E\right)=\mathcal A\otimes\mathcal B$ 上等于 $\mu\times\nu$. 即与定理 10.1.4 中定义的乘积测度一致. $\blacksquare$

### 习题二

证明习题 46、48、50.

**46.** 设 $X=Y=\left[0,1\right]$, $\mathcal M=\mathcal N=\mathcal B_{\left[0,1\right]}$, $\mu$ 是勒贝格测度, $\nu$ 是计数测度. 若 $D=\left\{\left(x,x\right):x\in\left[0,1\right]\right\}$ 是 $X\times Y$ 中的对角线, 则 $\iint\chi_{D}\,\mathrm{d}\mu\,\mathrm{d}\nu$, $\iint\chi_{D}\,\mathrm{d}\nu\,\mathrm{d}\mu$ 与 $\int\chi_{D}\,\mathrm{d}\left(\mu\times\nu\right)$ 不全相等.

**48.** 设 $X=Y=\mathbb N$, $\mathcal M=\mathcal N=\mathcal P\left(\mathbb N\right)$, $\mu=\nu$ 是计数测度. 定义 $f\left(m,n\right)=1$ 若 $m=n$, $f\left(m,n\right)=-1$ 若 $m=n+1$, $f\left(m,n\right)=0$ 否则. 则 $\int\left|f\right|\mathrm{d}\left(\mu\times\nu\right)=\infty$, 且 $\iint f\,\mathrm{d}\mu\,\mathrm{d}\nu$ 与 $\iint f\,\mathrm{d}\nu\,\mathrm{d}\mu$ 存在但不相等.

**50.** 设 $\left(X,\mathcal M,\mu\right)$ 是 σ-有限测度空间且 $f\in L^{+}\left(X\right)$. 令 $G_{f}=\left\{\left(x,y\right)\in X\times\left[0,\infty\right]:y\le f\left(x\right)\right\}$. 则 $G_{f}$ 是 $\mathcal M\otimes\mathcal B_{\mathbb R}$-可测的且 $\mu\times m\left(G_{f}\right)=\int f\,\mathrm{d}\mu$; 若把定义中 $y\le f\left(x\right)$ 的不等式换成 $y<f\left(x\right)$, 结论同样成立.

### 解答 习题二

#### 46

由**定义 10.1.2**, 对角线 $D$ 的 x-截面为 $D_{x}=\left\{y:\left(x,y\right)\in D\right\}=\left\{x\right\}$, 是单点集.

先算 $\iint\chi_{D}\,\mathrm{d}\mu\,\mathrm{d}\nu$ (内层按 μ 积分, 外层按 ν 积分). 对固定 $y$,

$$
\begin{aligned}
&\quad\;\int_{X}\chi_{D}\left(x,y\right)\mathrm{d}\mu\left(x\right)\\&=\mu\left(\left\{x:\left(x,y\right)\in D\right\}\right)\\&=\mu\left(\left\{y\right\}\right)\\&=0,
\end{aligned}
$$

因勒贝格测度下单点集为零测集. 故 $\iint\chi_{D}\,\mathrm{d}\mu\,\mathrm{d}\nu=\int_{Y}0\,\mathrm{d}\nu=0$.

再算 $\iint\chi_{D}\,\mathrm{d}\nu\,\mathrm{d}\mu$ (内层按 ν 积分). 对固定 $x$,

$$
\begin{aligned}
&\quad\;\int_{Y}\chi_{D}\left(x,y\right)\mathrm{d}\nu\left(y\right)\\&=\nu\left(D_{x}\right)\\&=\nu\left(\left\{x\right\}\right)\\&=1,
\end{aligned}
$$

因计数测度下单点集的测度为 $1$. 故 $\iint\chi_{D}\,\mathrm{d}\nu\,\mathrm{d}\mu=\int_{X}1\,\mathrm{d}\mu\left(x\right)=\mu\left(\left[0,1\right]\right)=1$.

最后由**定理 10.1.4** (乘积测度的构造 $\phi\left(E\right)=\int\nu\left(E_{x}\right)\mathrm{d}\mu\left(x\right)$),

$$
\begin{aligned}
&\quad\;\int\chi_{D}\,\mathrm{d}\left(\mu\times\nu\right)\\&=\left(\mu\times\nu\right)\left(D\right)\\&=\int_{X}\nu\left(D_{x}\right)\mathrm{d}\mu\left(x\right)\\&=\int_{X}\nu\left(\left\{x\right\}\right)\mathrm{d}\mu\left(x\right)\\&=\int_{X}1\,\mathrm{d}\mu\left(x\right)\\&=1.
\end{aligned}
$$

故三个积分分别为 $0$, $1$, $1$, 不全相等; 特别 $\iint\chi_{D}\,\mathrm{d}\mu\,\mathrm{d}\nu=0\ne1=\iint\chi_{D}\,\mathrm{d}\nu\,\mathrm{d}\mu$. 原因是 $\nu$ 非 σ-有限, **定理 10.2.1** (富比尼) 的 σ-有限假设不满足, 故乘积积分与先对 μ 积分的迭代积分不一致. $\blacksquare$

#### 48

计算 $\int\left|f\right|\mathrm{d}\left(\mu\times\nu\right)=\sum_{m,n}\left|f\left(m,n\right)\right|$. $f$ 在对角线 $\left\{\left(m,m\right)\right\}$ 上取 $1$, 在次对角线 $\left\{\left(m+1,m\right)\right\}$ 上取 $-1$, 故 $\left|f\right|$ 在这两族无限多个点上取 $1$, 于是

$$
\begin{aligned}
&\quad\;\int\left|f\right|\mathrm{d}\left(\mu\times\nu\right)\\&=\sum_{m,n}\left|f\left(m,n\right)\right|\\&=\infty.
\end{aligned}
$$

算 $\iint f\,\mathrm{d}\mu\,\mathrm{d}\nu$ (内层按 μ 求和, 外层按 ν 求和). 对固定 $n$, $\sum_{m}f\left(m,n\right)=f\left(n,n\right)+f\left(n+1,n\right)=1+\left(-1\right)=0$, 故 $\iint f\,\mathrm{d}\mu\,\mathrm{d}\nu=\sum_{n}0=0$.

算 $\iint f\,\mathrm{d}\nu\,\mathrm{d}\mu$ (内层按 ν 求和). 对固定 $m$, $\sum_{n}f\left(m,n\right)=f\left(m,m\right)+f\left(m,m-1\right)$ (当 $m\ge1$) $=1+\left(-1\right)=0$; 而 $m=0$ 时 $f\left(0,n\right)$ 只在 $n=0$ 处为 $1$, 和为 $1$. 故 $\iint f\,\mathrm{d}\nu\,\mathrm{d}\mu=\sum_{m}\left(\sum_{n}f\left(m,n\right)\right)=1$.

故 $\iint f\,\mathrm{d}\mu\,\mathrm{d}\nu=0\ne1=\iint f\,\mathrm{d}\nu\,\mathrm{d}\mu$. 因 $\int\left|f\right|\mathrm{d}\left(\mu\times\nu\right)=\infty$, $f$ 非绝对可积, **定理 10.2.1** (富比尼) 的假设 $\int\left|f\right|\mathrm{d}\left(\mu\times\nu\right)<\infty$ 不满足, 故不能交换积分次序. $\blacksquare$

#### 50

**可测性.** 考虑映射 $T:X\times\left[0,\infty\right]\to\left[0,\infty\right]\times\left[0,\infty\right]$, $T\left(x,y\right)=\left(f\left(x\right),y\right)$. 由**命题 7.1.7** (乘积空间的可测性), $T$ 可测当且仅当其坐标函数可测; 坐标函数 $\left(x,y\right)\mapsto f\left(x\right)=f\circ p_{1}$ 可测 (因 $f$ 可测), $\left(x,y\right)\mapsto y=p_{2}$ 连续可测. 故 $T$ 可测. 又 $\Phi\left(z,y\right)=z-y$ 连续, 博雷尔可测. 由**命题 7.1.5** (复合保持可测性), $\left(x,y\right)\mapsto f\left(x\right)-y=\Phi\circ T$ 可测. 因

$$
\begin{aligned}
&\quad\;G_{f}\\&=\left\{\left(x,y\right):f\left(x\right)-y\ge0\right\}\\&=\left(f-y\right)^{-1}\left(\left[0,\infty\right]\right),
\end{aligned}
$$

是可测函数的原像, 由**定义 10.1.1** (乘积 σ-代数), $G_{f}\in\mathcal M\otimes\mathcal B_{\mathbb R}$.

**测度值.** 由**定理 10.2.2** (托内利定理, 非负特征函数, $\mu\times m$ σ-有限),

$$
\left(\mu\times m\right)\left(G_{f}\right)=\int_{X}m\left(\left(G_{f}\right)_{x}\right)\mathrm{d}\mu\left(x\right),
$$

其中 $\left(G_{f}\right)_{x}=\left\{y\in\left[0,\infty\right]:y\le f\left(x\right)\right\}=\left[0,f\left(x\right)\right]$, 勒贝格测度 $m\left(\left[0,f\left(x\right)\right]\right)=f\left(x\right)$. 故

$$
\left(\mu\times m\right)\left(G_{f}\right)=\int_{X}f\left(x\right)\mathrm{d}\mu\left(x\right).
$$

若把 $y\le f\left(x\right)$ 换成 $y<f\left(x\right)$, 则 $\left(G_{f}\right)_{x}=\left[0,f\left(x\right)\right)$, 仍有 $m=f\left(x\right)$, 结论不变. $\blacksquare$
