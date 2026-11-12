# week7

> **定义 4.1.3 ($\sigma$-代数)**
> 
> 设 $X$ 非空, $\mathcal{F}\subset\mathcal{P}\left(X\right)$. 称 $\mathcal{F}$ 为 $X$ 上的一个 $\sigma$-代数, 若满足: (1) $X\in\mathcal{F}$; (2) 对补运算封闭: $A\in\mathcal{F}\Rightarrow{A}^{c}\in\mathcal{F}$; (3) 对可数并封闭: $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal{F}$.

> **定义 5.1.2 (测度)**
> 
> 设 $\left(X,\mathcal{F}\right)$ 是一个可测空间. 函数 $\mu:\mathcal{F}\to\left[0,+\infty\right]$ 称为 $\left(X,\mathcal{F}\right)$ 上的一个测度, 如果满足: (1) 非负性: $\mu\left(E\right)\ge0$ 对一切 $E\in\mathcal{F}$ 成立; (2) 零空集性: $\mu\left(\emptyset\right)=0$; (3) 可数可加性 ($\sigma$-可加性): 对任意可数个两两不交的集合 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$, 有 $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **定义 5.1.5 ($\sigma$-有限测度)**
> 
> 设 $\left(X,\mathcal{F},\mu\right)$ 是测度空间. 如果存在一列可测集 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$ 使得 $X=\bigcup_{n=1}^{\infty}E_{n}$ 且 $\mu\left(E_{n}\right)<+\infty$ 对所有 $n\in\mathbb{N}$ 成立, 则称 $\mu$ 为 $\sigma$-有限测度.

> **定义 6.2.1 (准测度)**
> 
> 设 $X$ 是非空集合, $\mathcal{E}\subset\mathcal{P}\left(X\right)$ 是一个代数. 函数 $\mu_{0}:\mathcal{E}\to\left[0,+\infty\right]$ 称为一个准测度, 如果 $\mu_{0}\left(\emptyset\right)=0$, 且若 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{E}$ 两两不交且 $\bigcup_{n=1}^{\infty}E_{n}\in\mathcal{E}$, 则 $\mu_{0}\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu_{0}\left(E_{n}\right)$.

> **定理 6.3.3 (卡拉西奥多里定理)**
> 
> 设 $\mu^{*}$ 是 $X$ 上的外测度, 则: (1) $\mathcal{M}$ 是一个 $\sigma$-代数; (2) $\mu^{*}|_{\mathcal{M}}$ 是一个完备测度; (3) 如果 $\mu^{*}$ 是由准测度 $\mu_{0}$ 生成的, 且 $\mu_{0}$ 是 $\sigma$-有限的, 则 $\mu^{*}|_{\mathcal{M}}$ 是 $\mu_{0}$ 的唯一延拓.

> **定理 6.4.5 (勒贝格-斯蒂尔杰斯测度的正则性)**
> 
> 设 $\mu_{F}$ 是由增右连续函数 $F$ 生成的勒贝格-斯蒂尔杰斯测度, $\mathcal{M}^{*}$ 是 $\mu_{F}$-可测集的 $\sigma$-代数. 若 $E\in\mathcal{M}^{*}$, 则

> **命题 7.1.5 (复合保持可测性)**
> 
> 若 $f:X\to{Y}$ 是 $\left(\mathcal{F},\mathcal{G}\right)$-可测的, $g:Y\to{Z}$ 是 $\left(\mathcal{G},\mathcal{H}\right)$-可测的, 则 $g\circ{f}:X\to{Z}$ 是 $\left(\mathcal{F},\mathcal{H}\right)$-可测的.

> **命题 7.1.7 (乘积空间的可测性)**
> 
> 设 $f=\left(f_{1},\dots,f_{n}\right):X\to{Y}_{1}\times\cdots\times{Y}_{n}$. 在乘积空间配备乘积 $\sigma$-代数下, $f$ 可测当且仅当每个坐标映射 $f_{i}:X\to{Y}_{i}$ 可测.

> **定理 7.1.8 (实值可测函数的运算封闭性)**
> 
> 设 $f,g:X\to\mathbb{R}$ 可测, $c\in\mathbb{R}$, 则 $cf$, $f+g$, $fg$, $\max\left(f,g\right)$, $\min\left(f,g\right)$ 可测; 若 $\left\{f_{n}\right\}$ 可测且点点收敛, 则极限函数可测.

> **定理 7.2.2 (可测函数的构造)**
> 
> 若 $f:X\to\left[0,+\infty\right]$ 是非负可测函数, 则存在一列非负简单函数 $\left\{f_{n}\right\}$ 满足 $0\le{f}_{1}\le{f}_{2}\le\cdots\le{f}$ 且 $\lim_{n\to\infty}f_{n}\left(x\right)=f\left(x\right)$ 对每个 $x\in{X}$ 成立.

> **定义 9.1.1 (几乎处处收敛)**
> 
> 设 $\left\{f_{n}\right\}$ 是一列可测函数, $f$ 是可测函数. 如果存在零测度集 $E$ 使对所有 $x\notin{E}$ 有 $\lim_{n\to\infty}f_{n}\left(x\right)=f\left(x\right)$, 则称 $\left\{f_{n}\right\}$ $\mu$-几乎处处收敛到 $f$, 记作 $f_{n}\xrightarrow{\text{a.e.}}f$.

> **命题 9.1.2 (几乎处处收敛的刻画)**
> 
> $f_{n}\xrightarrow{\text{a.e.}}f$ 当且仅当对任意的 $\varepsilon>0$,

> **定义 9.1.3 (依测度收敛)**
> 
> 设 $\left\{f_{n}\right\}$ 是一列可测函数, $f$ 是可测函数. 如果对任意 $\varepsilon>0$ 有 $\lim_{n\to\infty}\mu\left(\left\{x:\left|f_{n}\left(x\right)-f\left(x\right)\right|>\varepsilon\right\}\right)=0$, 则称 $\left\{f_{n}\right\}$ 依测度收敛到 $f$, 记作 $f_{n}\xrightarrow{\mu}f$.

> **定理 9.1.8 (子序列性质)**
> 
> 如果 $f_{n}\xrightarrow{\mu}f$, 则存在子序列 $\left\{f_{n_{k}}\right\}$ 使得 $f_{n_{k}}\to{f}$ 几乎处处.

> **定理 9.1.15 (叶戈罗夫定理)**
> 
> 设 $\mu\left(X\right)<\infty$ 且 $f_{n}\to{f}$ 几乎处处. 则对任意 $\delta>0$ 存在可测集 $E\subset{X}$ 使得 $\mu\left(E\right)<\delta$, 且在 $X\setminus{E}$ 上 $f_{n}$ 一致收敛到 $f$. 特别地, 在有限测度空间中, 几乎处处收敛蕴含依测度收敛.

> **定义 10.1.1 (乘积 $\sigma$-代数)**
> 
> 设 $\left(X,\mathcal{A},\mu\right)$ 和 $\left(Y,\mathcal{B},\nu\right)$ 是两个测度空间. 乘积空间 $X\times{Y}$ 上的乘积 $\sigma$-代数定义为 $\mathcal{A}\otimes\mathcal{B}=\sigma\left(\left\{A\times{B}:A\in\mathcal{A},B\in\mathcal{B}\right\}\right)$, 即由所有可测矩形生成的 $\sigma$-代数.

> **定义 10.1.2 (截面)**
> 
> 对于 $E\subseteq{X}\times{Y}$, 定义 $E$ 的 x-截面 $E_{x}=\left\{y\in{Y}:\left(x,y\right)\in{E}\right\}$ 和 y-截面 $E^{y}=\left\{x\in{X}:\left(x,y\right)\in{E}\right\}$.

> **定理 10.1.4 (乘积测度的存在唯一性)**
> 
> 设 $\left(X,\mathcal{A},\mu\right)$ 和 $\left(Y,\mathcal{B},\nu\right)$ 是 $\sigma$-有限的测度空间. 存在唯一的测度 $\mu\times\nu$ 在 $\left(X\times{Y},\mathcal{A}\otimes\mathcal{B}\right)$ 上, 使得对所有 $A\in\mathcal{A}$, $B\in\mathcal{B}$ 有 $\left(\mu\times\nu\right)\left(A\times{B}\right)=\mu\left(A\right)\nu\left(B\right)$. 其构造为 $\phi\left(E\right)=\int_{X}\nu\left(E_{x}\right)\mathrm{d}\mu\left(x\right)$ 对 $E\in\mathcal{A}\otimes\mathcal{B}$.

> **定理 10.2.1 (富比尼定理)**
> 
> 设 $\left(X,\mathcal{A},\mu\right)$ 和 $\left(Y,\mathcal{B},\nu\right)$ 是 $\sigma$-有限的测度空间, $f:X\times{Y}\to\mathbb{R}$ 是 $\mathcal{A}\otimes\mathcal{B}$-可测函数. 若 $f$ 在 $X\times{Y}$ 上可积, 则对几乎所有 $x$, $y\mapsto{f}\left(x,y\right)$ 是 $\nu$-可积的; 对几乎所有 $y$, $x\mapsto{f}\left(x,y\right)$ 是 $\mu$-可积的; 且重积分相等:

$$
\int_{X\times{Y}}f\,\mathrm{d}\left(\mu\times\nu\right)=\int_{X}\left(\int_{Y}f\left(x,y\right)\mathrm{d}\nu\left(y\right)\right)\mathrm{d}\mu\left(x\right)=\int_{Y}\left(\int_{X}f\left(x,y\right)\mathrm{d}\mu\left(x\right)\right)\mathrm{d}\nu\left(y\right).
$$

> **定理 10.2.2 (托内利定理)**
> 
> 如果 $f:X\times{Y}\to\left[0,\infty\right]$ 是 $\mathcal{A}\otimes\mathcal{B}$-可测的, 则

$$
\int_{X\times{Y}}f\,\mathrm{d}\left(\mu\times\nu\right)=\int_{X}\left(\int_{Y}f\left(x,y\right)\mathrm{d}\nu\left(y\right)\right)\mathrm{d}\mu\left(x\right)=\int_{Y}\left(\int_{X}f\left(x,y\right)\mathrm{d}\mu\left(x\right)\right)\mathrm{d}\nu\left(y\right),
$$
其中所有积分值都在 $\left[0,\infty\right]$ 中.

## 1

设 $\mu\left(X\right)<\infty$. 若 $f,g$ 是 $X$ 上的复值可测函数, 定义 $\rho\left(f,g\right)=\int\frac{\left|f-g\right|}{1+\left|f-g\right|}\,\mathrm{d}\mu$. 则 $\rho$ 是可测函数空间 (把几乎处处相等的函数视为同一) 上的一个度量, 且 $f_{n}\to{f}$ 关于此度量收敛当且仅当 $f_{n}\to{f}$ 依测度收敛.

### 解答 1

记 $d\left(t\right)=\frac{t}{1+t}$ ($t\ge0$). 由函数 $t\mapsto\frac{t}{1+t}$ 的性质, $d$ 递增且次可加. 被积函数 $\frac{\left|f-g\right|}{1+\left|f-g\right|}=d\left(\left|f-g\right|\right)$ 非负且有界 ($\le1$), 可测, 故可积, $\rho$ 良定义.

- $\rho\left(f,g\right)\ge0$; $\rho\left(f,g\right)=0$ 当且仅当 $d\left(\left|f-g\right|\right)=0$ 几乎处处 (由非负可积函数积分为零则几乎处处为零), 当且仅当 $\left|f-g\right|=0$ 几乎处处, 当且仅当 $f=g$ 几乎处处. 因此在把几乎处处相等的函数视为同一的商空间上, $\rho\left(f,g\right)=0$ 当且仅当 $f=g$.
- 对称性显然: $\rho\left(f,g\right)=\rho\left(g,f\right)$.
- 三角不等式: 由 $\left|f-g\right|\le\left|f-h\right|+\left|h-g\right|$, $d$ 递增且次可加,

$$
d\left(\left|f-g\right|\right)\le{d}\left(\left|f-h\right|+\left|h-g\right|\right)\le{d}\left(\left|f-h\right|\right)+d\left(\left|h-g\right|\right),
$$

积分得 $\rho\left(f,g\right)\le\rho\left(f,h\right)+\rho\left(h,g\right)$.

故 $\rho$ 是商空间上的度量.

再证收敛等价. 若 $f_{n}\xrightarrow{\mu}f$, 对 $\varepsilon\in\left(0,1\right)$ 有

$$
\rho\left(f_{n},f\right)=\int_{\left\{\left|f_{n}-f\right|\le\varepsilon\right\}}d\left(\left|f_{n}-f\right|\right)\mathrm{d}\mu+\int_{\left\{\left|f_{n}-f\right|>\varepsilon\right\}}d\left(\left|f_{n}-f\right|\right)\mathrm{d}\mu\le{d}\left(\varepsilon\right)\mu\left(X\right)+\mu\left(\left\{\left|f_{n}-f\right|>\varepsilon\right\}\right).
$$

由**定义 9.1.3 (依测度收敛)**, 先令 $n\to\infty$ 使第二项 $\to0$ (因 $f_{n}\xrightarrow{\mu}f$), 再令 $\varepsilon\to0$ 使 $d\left(\varepsilon\right)=\frac{\varepsilon}{1+\varepsilon}\to0$, 得 $\rho\left(f_{n},f\right)\to0$.

反之, 若 $\rho\left(f_{n},f\right)\to0$, 因 $d$ 递增, 在 $\left\{\left|f_{n}-f\right|>\varepsilon\right\}$ 上 $d\left(\left|f_{n}-f\right|\right)\ge{d}\left(\varepsilon\right)>0$, 故

$$
\rho\left(f_{n},f\right)\ge\int_{\left\{\left|f_{n}-f\right|>\varepsilon\right\}}d\left(\left|f_{n}-f\right|\right)\mathrm{d}\mu\ge{d}\left(\varepsilon\right)\mu\left(\left\{\left|f_{n}-f\right|>\varepsilon\right\}\right),
$$

即

$$
\mu\left(\left\{\left|f_{n}-f\right|>\varepsilon\right\}\right)\le\frac{\rho\left(f_{n},f\right)}{d\left(\varepsilon\right)}\to0.
$$

由**定义 9.1.3 (依测度收敛)**, $f_{n}\xrightarrow{\mu}f$.

$\blacksquare$

## 2

若 $\mu$ 是 $\sigma$-有限的且 $f_{n}\to{f}$ 几乎处处, 则存在可测集 $E_{1},E_{2},\dots\subset{X}$ 使得 $\mu\left(\left(\bigcup_{i=1}^{\infty}E_{i}\right)^{c}\right)=0$, 且 $f_{n}\to{f}$ 在每个 $E_{i}$ 上一致收敛.

### 解答 2

由**定义 5.1.5 ($\sigma$-有限测度)**, $\mu$ $\sigma$-有限, 存在 $X=\bigcup_{m=1}^{\infty}X_{m}$ 且 $\mu\left(X_{m}\right)<\infty$. 固定 $m$, 在 $X_{m}$ 上 $\mu\left(X_{m}\right)<\infty$ 且 $f_{n}\to{f}$ 几乎处处 (**定义 9.1.1 (几乎处处收敛)**), 由**定理 9.1.15 (叶戈罗夫定理)**, 对每个 $j\in\mathbb{N}$ 存在可测集 $E_{mj}\subset{X}_{m}$ 使 $\mu\left(X_{m}\setminus{E}_{mj}\right)<2^{-j}$ 且 $f_{n}\to{f}$ 在 $E_{mj}$ 上一致收敛.

令 $F_{m}:=\bigcup_{j=1}^{\infty}E_{mj}$. 则 $X_{m}\setminus{F}_{m}=\bigcap_{j=1}^{\infty}\left(X_{m}\setminus{E}_{mj}\right)$, 且 $\mu\left(X_{m}\setminus{F}_{m}\right)\le\mu\left(X_{m}\setminus{E}_{mj}\right)<2^{-j}$ 对所有 $j$ 成立, 故 $\mu\left(X_{m}\setminus{F}_{m}\right)=0$. 令 $F:=\bigcup_{m,j}E_{mj}=\bigcup_{m}F_{m}$, 则

$$
\mu\left(X\setminus{F}\right)=\mu\left(\bigcup_{m=1}^{\infty}\left(X_{m}\setminus{F}_{m}\right)\right)\le\sum_{m=1}^{\infty}\mu\left(X_{m}\setminus{F}_{m}\right)=0,
$$

因 $X=\bigcup_{m}X_{m}$. 故 $\mu\left(\left(\bigcup_{m,j}E_{mj}\right)^{c}\right)=0$. 把可数族 $\left\{E_{mj}:m,j\in\mathbb{N}\right\}$ 重排为 $E_{1},E_{2},\dots$, 则 $\mu\left(\left(\bigcup_{i}E_{i}\right)^{c}\right)=0$ 且 $f_{n}\to{f}$ 在每个 $E_{i}$ 上一致收敛.

$\blacksquare$

## 3

设 $\mu\left(X\right)<\infty$, $f:X\times\left[0,1\right]\to\mathbb{C}$ 满足: 对每个 $y\in\left[0,1\right]$, $f\left(\cdot,y\right)$ 可测; 对每个 $x\in{X}$, $f\left(x,\cdot\right)$ 连续.

(a) 若 $0<\varepsilon,\delta<1$, 则 $E_{\varepsilon,\delta}=\left\{x:\left|f\left(x,y\right)-f\left(x,0\right)\right|\le\varepsilon\text{~对所有~}y<\delta\right\}$ 是可测集;

(b) 对任意 $\varepsilon>0$ 存在集合 $E\subset{X}$ 使得 $\mu\left(E\right)<\varepsilon$ 且 $f\left(\cdot,y\right)\to{f}\left(\cdot,0\right)$ 在 $E^{c}$ 上一致收敛 ($y\to0$).

### 解答 3

(a) 对每个 $y\in\left[0,1\right]$, 由**定理 7.1.8 (实值可测函数的运算封闭性)** (复值按实虚部分量), $f\left(\cdot,y\right)-f\left(\cdot,0\right)$ 可测, 故 $\left\{x:\left|f\left(x,y\right)-f\left(x,0\right)\right|\le\varepsilon\right\}$ 是可测集. 又因 $f\left(x,\cdot\right)$ 连续, 函数 $y\mapsto\left|f\left(x,y\right)-f\left(x,0\right)\right|$ 连续, 故"对 $\left[0,\delta\right)$ 中所有 $y$ 有 $\left|f\left(x,y\right)-f\left(x,0\right)\right|\le\varepsilon$" 当且仅当"对 $\left[0,\delta\right)$ 中所有有理数 $y$ 有 $\le\varepsilon$" (由稠密性, 不等式在有理点成立则在闭包上成立). 因此

$$
E_{\varepsilon,\delta}=\bigcap_{y\in\left[0,\delta\right)\cap\mathbb{Q}}\left\{x:\left|f\left(x,y\right)-f\left(x,0\right)\right|\le\varepsilon\right\},
$$

这是可数个可测集之交, 由**定义 4.1.3 ($\sigma$-代数)** ($\sigma$-代数对可数交封闭) 可测.

$\blacksquare$

(b) 固定 $\eta>0$ 作为一致收敛的误差. 对每个 $\delta>0$, 记 $F_{\delta}:=\left\{x:\left|f\left(x,y\right)-f\left(x,0\right)\right|\le\eta\text{~对所有~}y<\delta\right\}$, 由 (a) 可测, 且随 $\delta$ 减小而增大. 因 $f\left(x,\cdot\right)$ 在 $0$ 处连续, 对每个 $x$ 有 $\lim_{y\to0}f\left(x,y\right)=f\left(x,0\right)$, 故存在 $\delta>0$ 使 $\left|f\left(x,y\right)-f\left(x,0\right)\right|\le\eta$ 对所有 $y<\delta$, 即 $x\in{F}_{\delta}$. 故 $\bigcup_{\delta>0}F_{\delta}=X$.

由测度的下连续性, 因 $\mu\left(X\right)<\infty$ 且 $F_{\delta}\uparrow{X}$, 有 $\mu\left(X\setminus{F}_{\delta}\right)\to0$. 给定 $\varepsilon>0$, 取 $\delta>0$ 使 $\mu\left(X\setminus{F}_{\delta}\right)<\varepsilon$, 令 $E:=X\setminus{F}_{\delta}$, 则 $\mu\left(E\right)<\varepsilon$, 且在 $E^{c}=F_{\delta}$ 上 $\left|f\left(x,y\right)-f\left(x,0\right)\right|\le\eta$ 对所有 $y<\delta$, 即 $f\left(\cdot,y\right)\to{f}\left(\cdot,0\right)$ 在 $E^{c}$ 上一致收敛 ($y\to0$).

$\blacksquare$

## 4

(卢津定理) 若 $f:\left[a,b\right]\to\mathbb{C}$ 是勒贝格可测的且 $\varepsilon>0$, 则存在紧集 $E\subset\left[a,b\right]$ 使得 $\mu\left(E^{c}\right)<\varepsilon$ 且 $f|_{E}$ 连续.

### 解答 4

先证简单函数情形. 设 $\phi=\sum_{j=1}^{N}c_{j}\chi_{A_{j}}$ 是 $\left[a,b\right]$ 上的简单函数, $A_{j}$ 两两不交可测且 $\bigcup_{j}A_{j}=\left[a,b\right]$. 由勒贝格测度的内正则性 (**定理 6.4.5 (勒贝格-斯蒂尔杰斯测度的正则性)**), 对每个 $j$ 取紧集 $K_{j}\subset{A}_{j}$ 使 $m\left(A_{j}\setminus{K}_{j}\right)<\varepsilon/\left(2N\right)$. 令 $K:=\bigcup_{j=1}^{N}K_{j}\subset\left[a,b\right]$, 则 $K$ 紧 (有限个紧集之并), 且

$$
m\left(\left[a,b\right]\setminus{K}\right)\le\sum_{j=1}^{N}m\left(A_{j}\setminus{K}_{j}\right)<\varepsilon/2.
$$

因 $K_{j}$ 两两不交且 $\phi$ 在 $K_{j}$ 上为常数 $c_{j}$, $\phi|_{K}$ 连续.

再证一般情形. $f$ 复值, 写 $f=\left(\operatorname{Re}f\right)^{+}-\left(\operatorname{Re}f\right)^{-}+i\left[\left(\operatorname{Im}f\right)^{+}-\left(\operatorname{Im}f\right)^{-}\right]$. 由**定理 7.2.2 (可测函数的构造)** 对每个非负部分取简单函数逐点逼近, 存在简单函数 $\phi_{n}\to{f}$ 处处. 因 $m\left(\left[a,b\right]\right)<\infty$, 由**定理 9.1.15 (叶戈罗夫定理)**, 对 $\varepsilon>0$ 存在可测集 $B\subset\left[a,b\right]$ 使 $m\left(B\right)<\varepsilon/3$ 且 $\phi_{n}\to{f}$ 在 $\left[a,b\right]\setminus{B}$ 上一致收敛. 由简单函数情形, 对每个 $n$ 取紧集 $K_{n}\subset\left[a,b\right]$ 使 $m\left(\left[a,b\right]\setminus{K}_{n}\right)<\varepsilon/\left(3\cdot2^{n}\right)$ 且 $\phi_{n}|_{K_{n}}$ 连续.

令 $E:=\left(\left[a,b\right]\setminus{B}\right)\cap\bigcap_{n=1}^{\infty}K_{n}$. 则 $E$ 是 $\left[a,b\right]$ 中闭集之交, 紧; 且

$$
m\left(\left[a,b\right]\setminus{E}\right)\le{m}\left(B\right)+\sum_{n=1}^{\infty}m\left(\left[a,b\right]\setminus{K}_{n}\right)<\varepsilon/3+\varepsilon/3=2\varepsilon/3<\varepsilon.
$$

在 $E$ 上, 每个 $\phi_{n}$ 连续 (因 $E\subset{K}_{n}$), 且 $\phi_{n}\to{f}$ 一致 (因 $E\subset\left[a,b\right]\setminus{B}$). 一致收敛的连续函数列的极限连续, 故 $f|_{E}$ 连续.

$\blacksquare$

## 5

设 $\mathcal{E}$ 为所有矩形框的有限不交并全体, 证明 $\mathcal{E}$ 为一个代数. 对于 $E=\bigcup_{i=1}^{n}A_{i}\times{B}_{i}$ (两两不交), 定义 $\pi\left(E\right):=\sum_{i=1}^{n}\mu\left(A_{i}\right)\nu\left(B_{i}\right)$. 证明 $\pi$ 为 $\mathcal{E}$ 上的准测度, 且由该准测度导出的 $\sigma\left(\mathcal{E}\right)$ 上的测度与**定理 10.1.4 (乘积测度的存在唯一性)** 中定义的乘积测度一致.

### 解答 5

$\mathcal{E}$ 是代数. 由矩形代数的交补性质, 可测矩形之交仍是可测矩形, 可测矩形之补是两个可测矩形之并. 空集 $\emptyset$ 与全空间 $X\times{Y}$ 都在 $\mathcal{E}$ 中. 对 $\mathcal{E}$ 中元素做补,交,并运算, 先把每个元素写成有限不交矩形并, 再由矩形之交仍是矩形,公共细分后两两不交, 得到的结果仍是有限不交矩形并, 仍属于 $\mathcal{E}$. 故 $\mathcal{E}$ 是一个代数.

$\pi$ 良定义. 设 $E=\bigcup_{i=1}^{m}A_{i}\times{B}_{i}=\bigcup_{j=1}^{n}C_{j}\times{D}_{j}$ 是 $E$ 的两种两两不交矩形分解. 对公共细分 $\left\{\left(A_{i}\cap{C}_{j}\right)\times\left(B_{i}\cap{D}_{j}\right)\right\}_{i,j}$, 由 $\mu,\nu$ 的有限可加性,

$$
\sum_{i=1}^{m}\mu\left(A_{i}\right)\nu\left(B_{i}\right)=\sum_{i,j}\mu\left(A_{i}\cap{C}_{j}\right)\nu\left(B_{i}\cap{D}_{j}\right)=\sum_{j=1}^{n}\mu\left(C_{j}\right)\nu\left(D_{j}\right),
$$

故 $\pi\left(E\right)$ 与分解无关.

$\pi$ 是 $\mathcal{E}$ 上的准测度. 由**定理 10.1.4 (乘积测度的存在唯一性)**, $\mu\times\nu$ 是 $\left(X\times{Y},\mathcal{A}\otimes\mathcal{B}\right)$ 上的测度且对矩形取 $\mu\left(A\right)\nu\left(B\right)$; 对有限不交矩形并 $\bigcup_{i=1}^{n}A_{i}\times{B}_{i}$, 由测度的有限可加性,

$$
\left(\mu\times\nu\right)\left(\bigcup_{i=1}^{n}A_{i}\times{B}_{i}\right)=\sum_{i=1}^{n}\mu\left(A_{i}\right)\nu\left(B_{i}\right)=\pi\left(E\right),
$$

故 $\pi=\left(\mu\times\nu\right)|_{\mathcal{E}}$. 由测度限制在代数上是准测度, $\pi$ 满足准测度条件: $\pi\left(\emptyset\right)=0$, 且对两两不交的 $\left\{E_{n}\right\}\subset\mathcal{E}$ 且 $\bigcup_{n}E_{n}\in\mathcal{E}$, 由 $\mu\times\nu$ 的 $\sigma$-可加性 (**定义 5.1.2 (测度)**),

$$
\pi\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\left(\mu\times\nu\right)\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\left(\mu\times\nu\right)\left(E_{n}\right)=\sum_{n=1}^{\infty}\pi\left(E_{n}\right).
$$

故 $\pi$ 是 $\mathcal{E}$ 上的准测度 (**定义 6.2.1 (准测度)**).

唯一延拓与乘积测度一致. 由**定义 10.1.1 (乘积 $\sigma$-代数)**, $\mathcal{E}$ 由所有可测矩形生成, 故 $\sigma\left(\mathcal{E}\right)=\mathcal{A}\otimes\mathcal{B}$. 因 $\mu,\nu$ $\sigma$-有限, 可取 $X=\bigcup_{p}X_{p}$, $Y=\bigcup_{q}Y_{q}$ 使 $\mu\left(X_{p}\right),\nu\left(Y_{q}\right)<\infty$, 则矩形 $X_{p}\times{Y}_{q}$ 覆盖 $X\times{Y}$ 且 $\pi\left(X_{p}\times{Y}_{q}\right)<\infty$, 故 $\pi$ 是 $\sigma$-有限的. 由**定理 6.3.3 (卡拉西奥多里定理)** (准测度的唯一延拓), $\pi$ 在 $\sigma\left(\mathcal{E}\right)$ 上有唯一延拓. 该延拓在 $\mathcal{E}$ 上等于 $\pi=\left(\mu\times\nu\right)|_{\mathcal{E}}$, 故在整个 $\sigma\left(\mathcal{E}\right)=\mathcal{A}\otimes\mathcal{B}$ 上等于 $\mu\times\nu$. 即与**定理 10.1.4 (乘积测度的存在唯一性)** 中定义的乘积测度一致.

$\blacksquare$

## 6

设 $X=Y=\left[0,1\right]$, $\mathcal{M}=\mathcal{N}=\mathcal{B}_{\left[0,1\right]}$, $\mu$ 是勒贝格测度, $\nu$ 是计数测度. 若 $D=\left\{\left(x,x\right):x\in\left[0,1\right]\right\}$ 是 $X\times{Y}$ 中的对角线, 则 $\iint\chi_{D}\,\mathrm{d}\mu\,\mathrm{d}\nu$, $\iint\chi_{D}\,\mathrm{d}\nu\,\mathrm{d}\mu$ 与 $\int\chi_{D}\,\mathrm{d}\left(\mu\times\nu\right)$ 不全相等.

### 解答 6

由**定义 10.1.2 (截面)**, 对角线 $D$ 的 x-截面为 $D_{x}=\left\{y:\left(x,y\right)\in{D}\right\}=\left\{x\right\}$, 是单点集.

先算 $\iint\chi_{D}\,\mathrm{d}\mu\,\mathrm{d}\nu$ (内层按 $\mu$ 积分, 外层按 $\nu$ 积分). 对固定 $y$,

$$
\int_{X}\chi_{D}\left(x,y\right)\mathrm{d}\mu\left(x\right)=\mu\left(\left\{x:\left(x,y\right)\in{D}\right\}\right)=\mu\left(\left\{y\right\}\right)=0,
$$

因勒贝格测度下单点集为零测集. 故 $\iint\chi_{D}\,\mathrm{d}\mu\,\mathrm{d}\nu=\int_{Y}0\,\mathrm{d}\nu=0$.

再算 $\iint\chi_{D}\,\mathrm{d}\nu\,\mathrm{d}\mu$ (内层按 $\nu$ 积分). 对固定 $x$,

$$
\int_{Y}\chi_{D}\left(x,y\right)\mathrm{d}\nu\left(y\right)=\nu\left(D_{x}\right)=\nu\left(\left\{x\right\}\right)=1,
$$

因计数测度下单点集的测度为 $1$. 故 $\iint\chi_{D}\,\mathrm{d}\nu\,\mathrm{d}\mu=\int_{X}1\,\mathrm{d}\mu\left(x\right)=\mu\left(\left[0,1\right]\right)=1$.

最后由**定理 10.1.4 (乘积测度的存在唯一性)** (乘积测度的构造 $\phi\left(E\right)=\int\nu\left(E_{x}\right)\mathrm{d}\mu\left(x\right)$),

$$
\int\chi_{D}\,\mathrm{d}\left(\mu\times\nu\right)=\left(\mu\times\nu\right)\left(D\right)=\int_{X}\nu\left(D_{x}\right)\mathrm{d}\mu\left(x\right)=\int_{X}\nu\left(\left\{x\right\}\right)\mathrm{d}\mu\left(x\right)=\int_{X}1\,\mathrm{d}\mu\left(x\right)=1.
$$

故三个积分分别为 $0$, $1$, $1$, 不全相等; 特别 $\iint\chi_{D}\,\mathrm{d}\mu\,\mathrm{d}\nu=0\ne1=\iint\chi_{D}\,\mathrm{d}\nu\,\mathrm{d}\mu$. 原因是 $\nu$ 非 $\sigma$-有限, **定理 10.2.1 (富比尼定理)** 的 $\sigma$-有限假设不满足, 故乘积积分与先对 $\mu$ 积分的迭代积分不一致.

$\blacksquare$
