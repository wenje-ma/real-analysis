# 作业 6

> **定义 4.1.3** ($\sigma$-代数)<br>设 $X$ 非空, $\mathcal F\subset\mathcal P\left(X\right)$. 称 $\mathcal F$ 为 $X$ 上的一个 $\sigma$-代数, 若 $X\in\mathcal F$, 对补运算封闭, 且对可数并封闭. 由此 $\mathcal F$ 也对可数交封闭.

> **定义 5.1.5** (σ-有限测度)<br>设 $\left(X,\mathcal F,\mu\right)$ 是测度空间. 如果存在一列可测集 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$ 使得 $X=\bigcup_{n=1}^{\infty}E_{n}$ 且 $\mu\left(E_{n}\right)<+\infty$ 对所有 $n\in\mathbb N$ 成立, 则称 $\mu$ 为 σ-有限测度.

> **定理 6.4.5** (勒贝格-斯蒂尔杰斯测度的正则性)<br>设 $\mu_{F}$ 是由增右连续函数 $F$ 生成的勒贝格-斯蒂尔杰斯测度, $\mathcal M^{*}$ 是 $\mu_{F}$-可测集的 σ-代数. 若 $E\in\mathcal M^{*}$, 则 $$\begin{aligned}\mu_{F}\left(E\right)&=\inf\left\{\mu_{F}\left(U\right):E\subset U,U\text{开}\right\}\\&=\sup\left\{\mu_{F}\left(K\right):K\subset E,K\text{紧}\right\}.\end{aligned}$$ 特别地, 勒贝格测度在 $\left[a,b\right]$ 上内正则.

> **定理 7.1.8** (实值可测函数的运算封闭性)<br>设 $f,g:X\to\mathbb R$ 可测, $c\in\mathbb R$, 则 $cf$, $f+g$, $fg$, $\max\left(f,g\right)$, $\min\left(f,g\right)$ 可测; 若 $\left\{f_{n}\right\}$ 可测且点点收敛, 则极限函数可测.

> **定理 7.2.2** (可测函数的构造)<br>若 $f:X\to\left[0,+\infty\right]$ 是非负可测函数, 则存在一列非负简单函数 $\left\{f_{n}\right\}$ 满足 $0\le f_{1}\le f_{2}\le\cdots\le f$ 且 $\lim_{n\to\infty}f_{n}\left(x\right)=f\left(x\right)$ 对每个 $x\in X$ 成立.

> **定义 9.1.1** (几乎处处收敛)<br>设 $\left\{f_{n}\right\}$ 是一列可测函数, $f$ 是可测函数. 如果存在零测度集 $E$ 使对所有 $x\notin E$ 有 $\lim_{n\to\infty}f_{n}\left(x\right)=f\left(x\right)$, 则称 $\left\{f_{n}\right\}$ μ-几乎处处收敛到 $f$, 记作 $f_{n}\xrightarrow{\text{a.e.}}f$.

> **命题 9.1.2** (几乎处处收敛的刻画)<br>$f_{n}\xrightarrow{\text{a.e.}}f$ 当且仅当对任意的 $\epsilon>0$, $\mu\left(\bigcap_{k=1}^{\infty}\bigcup_{n=k}^{\infty}\left\{x:\left|f_{n}\left(x\right)-f\left(x\right)\right|>\epsilon\right\}\right)=0$.

> **定义 9.1.3** (依测度收敛)<br>设 $\left\{f_{n}\right\}$ 是一列可测函数, $f$ 是可测函数. 如果对任意 $\varepsilon>0$ 有 $\lim_{n\to\infty}\mu\left(\left\{x:\left|f_{n}\left(x\right)-f\left(x\right)\right|>\varepsilon\right\}\right)=0$, 则称 $\left\{f_{n}\right\}$ 依测度收敛到 $f$, 记作 $f_{n}\xrightarrow{\mu}f$.

> **定理 9.1.8** (子序列性质)<br>如果 $f_{n}\xrightarrow{\mu}f$, 则存在子序列 $\left\{f_{n_{k}}\right\}$ 使得 $f_{n_{k}}\to f$ 几乎处处.

> **定理 9.1.15** (叶戈罗夫定理)<br>设 $\mu\left(X\right)<\infty$ 且 $f_{n}\to f$ 几乎处处. 则对任意 $\delta>0$ 存在可测集 $E\subset X$ 使得 $\mu\left(E\right)<\delta$, 且在 $X\setminus E$ 上 $f_{n}$ 一致收敛到 $f$. 特别地, 在有限测度空间中, 几乎处处收敛蕴含依测度收敛.

> **基础知识**<br>**非负可积函数积分为零则几乎处处为零**: 设 $h\ge0$ 可测且 $\int_{X}h\,\mathrm{d}\mu=0$, 则 $h=0$ 几乎处处.

> **基础知识**<br>**函数 $t\mapsto\frac{t}{1+t}$ 的性质**: 设 $d\left(t\right)=\frac{t}{1+t}$, $t\ge0$. 则 $d$ 在 $\left[0,\infty\right)$ 上递增, 且次可加: $d\left(a+b\right)\le d\left(a\right)+d\left(b\right)$ 对所有 $a,b\ge0$.

> **基础知识**<br>**测度的下连续性**: 若 $\left\{E_{n}\right\}$ 是可测集的单调上升序列, 则 $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\lim_{n\to\infty}\mu\left(E_{n}\right)$; 特别当 $\mu\left(X\right)<\infty$ 时, 若 $E_{n}\uparrow X$, 则 $\mu\left(X\setminus E_{n}\right)\to0$.

### 习题一

证明讲义推论 9.1.10: $f_{n}$ 依测度收敛到 $f$ 当且仅当对任意子列 $\left\{f_{n_{k}}\right\}$ 存在子子列 $\left\{f_{n'_{k}}\right\}$ 使得 $f_{n'_{k}}\to f$ 几乎处处. 特别地, 若 $\phi:\mathbb R\to\mathbb R$ 是连续函数, 则 $\phi\left(f_{n}\right)\xrightarrow{\mu}\phi\left(f\right)$.

### 解答 习题一

$\left(\Rightarrow\right)$ 由**定义 9.1.3**, 若 $f_{n}\xrightarrow{\mu}f$, 则任意子列 $\left\{f_{n_{k}}\right\}$ 也依测度收敛到 $f$ (定义中的极限沿子列仍成立). 由**定理 9.1.8** (子序列性质), 存在子子列 $\left\{f_{n'_{k}}\right\}$ 使得 $f_{n'_{k}}\to f$ 几乎处处.

$\left(\Leftarrow\right)$ 反证. 若 $f_{n}$ 不依测度收敛到 $f$, 则存在 $\epsilon>0$ 使 $\mu\left(\left\{\left|f_{n}-f\right|>\epsilon\right\}\right)$ 不趋于 $0$, 即存在 $\delta>0$ 与子列 $\left\{f_{n_{k}}\right\}$ 使

$$
\mu\left(\left\{x:\left|f_{n_{k}}\left(x\right)-f\left(x\right)\right|>\epsilon\right\}\right)\ge\delta\quad\text{对所有}k.
$$

由**命题 9.1.2** (几乎处处收敛的刻画), $\left\{f_{n_{k}}\right\}$ 的任何子子列 $\left\{f_{n'_{j}}\right\}$ 都不能几乎处处收敛到 $f$: 因为

$$
\mu\left(\bigcap_{j=1}^{\infty}\bigcup_{l\ge j}\left\{x:\left|f_{n'_{l}}\left(x\right)-f\left(x\right)\right|>\epsilon\right\}\right)\ge\limsup_{j\to\infty}\mu\left(\left\{x:\left|f_{n'_{j}}\left(x\right)-f\left(x\right)\right|>\epsilon\right\}\right)\ge\delta>0.
$$

这与假设 (任意子列存在几乎处处收敛子子列) 矛盾. 故 $f_{n}\xrightarrow{\mu}f$.

最后设 $\phi:\mathbb R\to\mathbb R$ 连续. 对任意子列 $\left\{\phi\left(f_{n_{k}}\right)\right\}$, 由 $f_{n}\xrightarrow{\mu}f$ 和已证的 $\left(\Rightarrow\right)$, 子列 $\left\{f_{n_{k}}\right\}$ 存在子子列 $f_{n'_{k}}\to f$ 几乎处处; $\phi$ 连续推出 $\phi\left(f_{n'_{k}}\right)\to\phi\left(f\right)$ 几乎处处. 故 $\left\{\phi\left(f_{n}\right)\right\}$ 的任意子列存在几乎处处收敛子子列, 由已证的 $\left(\Leftarrow\right)$, $\phi\left(f_{n}\right)\xrightarrow{\mu}\phi\left(f\right)$. $\blacksquare$

### 习题二

证明习题 32、41、43、44.

**32.** 设 $\mu\left(X\right)<\infty$. 若 $f,g$ 是 $X$ 上的复值可测函数, 定义 $\rho\left(f,g\right)=\int\frac{\left|f-g\right|}{1+\left|f-g\right|}\,\mathrm{d}\mu$. 则 $\rho$ 是可测函数空间 (把几乎处处相等的函数视为同一) 上的一个度量, 且 $f_{n}\to f$ 关于此度量收敛当且仅当 $f_{n}\to f$ 依测度收敛.

**41.** 若 $\mu$ 是 σ-有限的且 $f_{n}\to f$ 几乎处处, 则存在可测集 $E_{1},E_{2},\dots\subset X$ 使得 $\mu\left(\left(\bigcup_{i=1}^{\infty}E_{i}\right)^{c}\right)=0$, 且 $f_{n}\to f$ 在每个 $E_{i}$ 上一致收敛.

**43.** 设 $\mu\left(X\right)<\infty$, $f:X\times\left[0,1\right]\to\mathbb C$ 满足: 对每个 $y\in\left[0,1\right]$, $f\left(\cdot,y\right)$ 可测; 对每个 $x\in X$, $f\left(x,\cdot\right)$ 连续.

a. 若 $0<\varepsilon,\delta<1$, 则 $E_{\varepsilon,\delta}=\left\{x:\left|f\left(x,y\right)-f\left(x,0\right)\right|\le\varepsilon\text{对所有}y<\delta\right\}$ 是可测集;
b. 对任意 $\varepsilon>0$ 存在集合 $E\subset X$ 使得 $\mu\left(E\right)<\varepsilon$ 且 $f\left(\cdot,y\right)\to f\left(\cdot,0\right)$ 在 $E^{c}$ 上一致收敛 ($y\to0$).

**44.** (卢津定理) 若 $f:\left[a,b\right]\to\mathbb C$ 是勒贝格可测的且 $\varepsilon>0$, 则存在紧集 $E\subset\left[a,b\right]$ 使得 $\mu\left(E^{c}\right)<\varepsilon$ 且 $f|_{E}$ 连续.

### 解答 习题二

#### 32

记 $d\left(t\right)=\frac{t}{1+t}$ ($t\ge0$). 由基础知识, $d$ 递增且次可加. 被积函数 $\frac{\left|f-g\right|}{1+\left|f-g\right|}=d\left(\left|f-g\right|\right)$ 非负且有界 (≤1), 可测, 故可积, $\rho$ 良定义.

- $\rho\left(f,g\right)\ge0$; $\rho\left(f,g\right)=0$ 当且仅当 $d\left(\left|f-g\right|\right)=0$ 几乎处处 (由基础知识, 非负可积积分为零则几乎处处为零), 当且仅当 $\left|f-g\right|=0$ 几乎处处, 当且仅当 $f=g$ 几乎处处. 因此在把几乎处处相等的函数视为同一的商空间上, $\rho\left(f,g\right)=0$ 当且仅当 $f=g$.
- 对称性显然: $\rho\left(f,g\right)=\rho\left(g,f\right)$.
- 三角不等式: 由 $\left|f-g\right|\le\left|f-h\right|+\left|h-g\right|$, $d$ 递增且次可加,

$$
d\left(\left|f-g\right|\right)\le d\left(\left|f-h\right|+\left|h-g\right|\right)\le d\left(\left|f-h\right|\right)+d\left(\left|h-g\right|\right),
$$

积分得 $\rho\left(f,g\right)\le\rho\left(f,h\right)+\rho\left(h,g\right)$.

故 $\rho$ 是商空间上的度量.

再证收敛等价. 若 $f_{n}\xrightarrow{\mu}f$, 对 $\varepsilon\in\left(0,1\right)$ 有

$$
\rho\left(f_{n},f\right)=\int_{\left\{\left|f_{n}-f\right|\le\varepsilon\right\}}d\left(\left|f_{n}-f\right|\right)\mathrm{d}\mu+\int_{\left\{\left|f_{n}-f\right|>\varepsilon\right\}}d\left(\left|f_{n}-f\right|\right)\mathrm{d}\mu\le d\left(\varepsilon\right)\mu\left(X\right)+\mu\left(\left\{\left|f_{n}-f\right|>\varepsilon\right\}\right).
$$

由**定义 9.1.3**, 先令 $n\to\infty$ 使第二项 $\to0$ (因 $f_{n}\xrightarrow{\mu}f$), 再令 $\varepsilon\to0$ 使 $d\left(\varepsilon\right)=\frac{\varepsilon}{1+\varepsilon}\to0$, 得 $\rho\left(f_{n},f\right)\to0$.

反之, 若 $\rho\left(f_{n},f\right)\to0$, 因 $d$ 递增, 在 $\left\{\left|f_{n}-f\right|>\varepsilon\right\}$ 上 $d\left(\left|f_{n}-f\right|\right)\ge d\left(\varepsilon\right)>0$, 故

$$
\rho\left(f_{n},f\right)\ge\int_{\left\{\left|f_{n}-f\right|>\varepsilon\right\}}d\left(\left|f_{n}-f\right|\right)\mathrm{d}\mu\ge d\left(\varepsilon\right)\mu\left(\left\{\left|f_{n}-f\right|>\varepsilon\right\}\right),
$$

即 $\mu\left(\left\{\left|f_{n}-f\right|>\varepsilon\right\}\right)\le\frac{\rho\left(f_{n},f\right)}{d\left(\varepsilon\right)}\to0$. 由定义 9.1.3, $f_{n}\xrightarrow{\mu}f$. $\blacksquare$

#### 41

由**定义 5.1.5**, $\mu$ σ-有限, 存在 $X=\bigcup_{m=1}^{\infty}X_{m}$ 且 $\mu\left(X_{m}\right)<\infty$. 固定 $m$, 在 $X_{m}$ 上 $\mu\left(X_{m}\right)<\infty$ 且 $f_{n}\to f$ 几乎处处 (**定义 9.1.1**), 由**定理 9.1.15** (叶戈罗夫定理), 对每个 $j\in\mathbb N$ 存在可测集 $E_{mj}\subset X_{m}$ 使 $\mu\left(X_{m}\setminus E_{mj}\right)<2^{-j}$ 且 $f_{n}\to f$ 在 $E_{mj}$ 上一致收敛.

令 $F_{m}:=\bigcup_{j=1}^{\infty}E_{mj}$. 则 $X_{m}\setminus F_{m}=\bigcap_{j=1}^{\infty}\left(X_{m}\setminus E_{mj}\right)$, 且 $\mu\left(X_{m}\setminus F_{m}\right)\le\mu\left(X_{m}\setminus E_{mj}\right)<2^{-j}$ 对所有 $j$ 成立, 故 $\mu\left(X_{m}\setminus F_{m}\right)=0$. 令 $F:=\bigcup_{m,j}E_{mj}=\bigcup_{m}F_{m}$, 则

$$
\begin{aligned}\mu\left(X\setminus F\right)&=\mu\left(\bigcup_{m=1}^{\infty}\left(X_{m}\setminus F_{m}\right)\right)\\&\le\sum_{m=1}^{\infty}\mu\left(X_{m}\setminus F_{m}\right)\\&=0,
\end{aligned}
$$

因 $X=\bigcup_{m}X_{m}$. 故 $\mu\left(\left(\bigcup_{m,j}E_{mj}\right)^{c}\right)=0$. 把可数族 $\left\{E_{mj}:m,j\in\mathbb N\right\}$ 重排为 $E_{1},E_{2},\dots$, 则 $\mu\left(\left(\bigcup_{i}E_{i}\right)^{c}\right)=0$ 且 $f_{n}\to f$ 在每个 $E_{i}$ 上一致收敛. $\blacksquare$

#### 43

**a.** 对每个 $y\in\left[0,1\right]$, 由**定理 7.1.8** (可测函数的运算, 复值按实虚部分量), $f\left(\cdot,y\right)-f\left(\cdot,0\right)$ 可测, 故 $\left\{x:\left|f\left(x,y\right)-f\left(x,0\right)\right|\le\varepsilon\right\}$ 是可测集. 又因 $f\left(x,\cdot\right)$ 连续, 函数 $y\mapsto\left|f\left(x,y\right)-f\left(x,0\right)\right|$ 连续, 故"对 $\left[0,\delta\right)$ 中所有 $y$ 有 $\left|f\left(x,y\right)-f\left(x,0\right)\right|\le\varepsilon$" 当且仅当"对 $\left[0,\delta\right)$ 中所有有理数 $y$ 有 $\le\varepsilon$" (由稠密性, 不等式在有理点成立则在闭包上成立). 因此

$$
E_{\varepsilon,\delta}=\bigcap_{y\in\left[0,\delta\right)\cap\mathbb Q}\left\{x:\left|f\left(x,y\right)-f\left(x,0\right)\right|\le\varepsilon\right\},
$$

这是可数个可测集之交, 由**定义 4.1.3** (σ-代数对可数交封闭) 可测. $\blacksquare$

**b.** 固定 $\eta>0$ 作为一致收敛的误差. 对每个 $\delta>0$, 记 $F_{\delta}:=\left\{x:\left|f\left(x,y\right)-f\left(x,0\right)\right|\le\eta\text{对所有}y<\delta\right\}$, 由 a 可测, 且随 $\delta$ 减小而增大. 因 $f\left(x,\cdot\right)$ 在 $0$ 处连续, 对每个 $x$ 有 $\lim_{y\to0}f\left(x,y\right)=f\left(x,0\right)$, 故存在 $\delta>0$ 使 $\left|f\left(x,y\right)-f\left(x,0\right)\right|\le\eta$ 对所有 $y<\delta$, 即 $x\in F_{\delta}$. 故 $\bigcup_{\delta>0}F_{\delta}=X$.

由基础知识 (测度的下连续性), 因 $\mu\left(X\right)<\infty$ 且 $F_{\delta}\uparrow X$, 有 $\mu\left(X\setminus F_{\delta}\right)\to0$. 给定 $\varepsilon>0$, 取 $\delta>0$ 使 $\mu\left(X\setminus F_{\delta}\right)<\varepsilon$, 令 $E:=X\setminus F_{\delta}$, 则 $\mu\left(E\right)<\varepsilon$, 且在 $E^{c}=F_{\delta}$ 上 $\left|f\left(x,y\right)-f\left(x,0\right)\right|\le\eta$ 对所有 $y<\delta$, 即 $f\left(\cdot,y\right)\to f\left(\cdot,0\right)$ 在 $E^{c}$ 上一致收敛 ($y\to0$). $\blacksquare$

#### 44

先证简单函数情形. 设 $\phi=\sum_{j=1}^{N}c_{j}\chi_{A_{j}}$ 是 $\left[a,b\right]$ 上的简单函数, $A_{j}$ 两两不交可测且 $\bigcup_{j}A_{j}=\left[a,b\right]$. 由勒贝格测度的内正则性 (**定理 6.4.5**), 对每个 $j$ 取紧集 $K_{j}\subset A_{j}$ 使 $m\left(A_{j}\setminus K_{j}\right)<\varepsilon/\left(2N\right)$. 令 $K:=\bigcup_{j=1}^{N}K_{j}\subset\left[a,b\right]$, 则 $K$ 紧 (有限个紧集之并), 且

$$
m\left(\left[a,b\right]\setminus K\right)\le\sum_{j=1}^{N}m\left(A_{j}\setminus K_{j}\right)<\varepsilon/2.
$$

因 $K_{j}$ 两两不交且 $\phi$ 在 $K_{j}$ 上为常数 $c_{j}$, $\phi|_{K}$ 连续.

再证一般情形. $f$ 复值, 写 $f=\left(\operatorname{Re}f\right)^{+}-\left(\operatorname{Re}f\right)^{-}+i\left[\left(\operatorname{Im}f\right)^{+}-\left(\operatorname{Im}f\right)^{-}\right]$. 由**定理 7.2.2** (可测函数的构造) 对每个非负部分取简单函数逐点逼近, 存在简单函数 $\phi_{n}\to f$ 处处. 因 $m\left(\left[a,b\right]\right)<\infty$, 由**定理 9.1.15** (叶戈罗夫定理), 对 $\varepsilon>0$ 存在可测集 $B\subset\left[a,b\right]$ 使 $m\left(B\right)<\varepsilon/3$ 且 $\phi_{n}\to f$ 在 $\left[a,b\right]\setminus B$ 上一致收敛. 由简单函数情形, 对每个 $n$ 取紧集 $K_{n}\subset\left[a,b\right]$ 使 $m\left(\left[a,b\right]\setminus K_{n}\right)<\varepsilon/\left(3\cdot2^{n}\right)$ 且 $\phi_{n}|_{K_{n}}$ 连续.

令 $E:=\left(\left[a,b\right]\setminus B\right)\cap\bigcap_{n=1}^{\infty}K_{n}$. 则 $E$ 是 $\left[a,b\right]$ 中闭集之交, 紧; 且

$$
m\left(\left[a,b\right]\setminus E\right)\le m\left(B\right)+\sum_{n=1}^{\infty}m\left(\left[a,b\right]\setminus K_{n}\right)<\varepsilon/3+\varepsilon/3=2\varepsilon/3<\varepsilon.
$$

在 $E$ 上, 每个 $\phi_{n}$ 连续 (因 $E\subset K_{n}$), 且 $\phi_{n}\to f$ 一致 (因 $E\subset\left[a,b\right]\setminus B$). 一致收敛的连续函数列的极限连续, 故 $f|_{E}$ 连续. $\blacksquare$
