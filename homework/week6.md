# week6

> **定义 5.1.2 (测度)**
> 
> 设 $\left(X,\mathcal{F}\right)$ 是一个可测空间. 函数 $\mu:\mathcal{F}\to\left[0,+\infty\right]$ 称为 $\left(X,\mathcal{F}\right)$ 上的一个测度, 如果满足: (1) 非负性: $\mu\left(E\right)\ge0$ 对一切 $E\in\mathcal{F}$ 成立; (2) 零空集性: $\mu\left(\emptyset\right)=0$; (3) 可数可加性 ($\sigma$-可加性): 对任意可数个两两不交的集合 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$, 有 $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **定义 5.1.5 ($\sigma$-有限测度)**
> 
> 设 $\left(X,\mathcal{F},\mu\right)$ 是测度空间. 如果存在一列可测集 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$ 使得 $X=\bigcup_{n=1}^{\infty}E_{n}$ 且 $\mu\left(E_{n}\right)<+\infty$ 对所有 $n\in\mathbb{N}$ 成立, 则称 $\mu$ 为 $\sigma$-有限测度.

> **定义 8.1.1 (非负简单函数的积分)**
> 
> 设 $f=\sum_{i=1}^{n}c_{i}\chi_{A_{i}}$ 是非负简单函数, 其中 $c_{i}\ge0$, $A_{i}\in\mathcal{F}$ 互不相交且 $\bigcup_{i}A_{i}=X$. 定义 $f$ 关于 $\mu$ 的积分为 $\int_{X}f\,\mathrm{d}\mu=\sum_{i=1}^{n}c_{i}\mu\left(A_{i}\right)$, 并约定 $0\cdot\infty=0$.

> **命题 8.1.2 (简单函数积分的线性性)**
> 
> 设 $f,g$ 为非负简单函数, $\alpha,\beta\ge0$, 则 $\int_{X}\left(\alpha{f}+\beta{g}\right)\mathrm{d}\mu=\alpha\int_{X}f\,\mathrm{d}\mu+\beta\int_{X}g\,\mathrm{d}\mu$.

> **定义 8.2.1 (非负可测函数的积分)**
> 
> 设 $f:X\to\left[0,+\infty\right]$ 是非负可测函数. 定义 $f$ 关于 $\mu$ 的积分为 $\int_{X}f\,\mathrm{d}\mu=\sup\left\{\int_{X}\phi\,\mathrm{d}\mu:\phi\text{~是简单函数},0\le\phi\le{f}\right\}$. 若 $\int_{X}f\,\mathrm{d}\mu<\infty$, 则称 $f$ 是可积的.

> **定理 8.2.2 (单调收敛定理)**
> 
> 设 $\left(X,\mathcal{F},\mu\right)$ 是测度空间, $\left\{f_{n}\right\}$ 是一列非负可测函数, 满足 $0\le{f}_{1}\left(x\right)\le{f}_{2}\left(x\right)\le\cdots$ 对所有 $x\in{X}$ 成立, 且 $f_{n}\to{f}$ 点点收敛. 则 $\lim_{n\to\infty}\int_{X}f_{n}\,\mathrm{d}\mu=\int_{X}f\,\mathrm{d}\mu$.

> **命题 8.2.4 (积分关于集合的绝对连续性)**
> 
> 设 $f$ 为非负可测函数, 则 $A\mapsto\int_{A}f\,\mathrm{d}\mu$ 为一个测度; 若 $\mu\left(A\right)=0$, 则 $\int_{A}f\,\mathrm{d}\mu=0$.

> **定义 8.2.5 (一般可测函数的积分)**
> 
> 设 $f:X\to\left[-\infty,+\infty\right]$ 是可测函数. 定义 $f$ 的正部和负部分别为 $f^{+}\left(x\right)=\max\left\{f\left(x\right),0\right\}$, $f^{-}\left(x\right)=\max\left\{-f\left(x\right),0\right\}$. 若至少有一个积分 $\int_{X}f^{+}\mathrm{d}\mu$, $\int_{X}f^{-}\mathrm{d}\mu$ 有限, 则定义 $f$ 的积分为 $\int_{X}f\,\mathrm{d}\mu=\int_{X}f^{+}\mathrm{d}\mu-\int_{X}f^{-}\mathrm{d}\mu$. 若 $\int_{X}f^{+}\mathrm{d}\mu<\infty$ 且 $\int_{X}f^{-}\mathrm{d}\mu<\infty$, 则称 $f$ 是可积的. ## 1 设 $f$ 为非负简单函数, 证明: $A\mapsto\int_{A}f\,\mathrm{d}\mu$ 是一个测度; 若 $\mu\left(A\right)=0$, 则 $\int_{A}f\,\mathrm{d}\mu=0$. 设 $f=\sum_{i=1}^{n}c_{i}\chi_{A_{i}}$, 其中 $c_{i}\ge0$, $A_{i}\in\mathcal{F}$ 两两不交且 $\bigcup_{i}A_{i}=X$. 对 $E\in\mathcal{F}$, 由**定义 8.1.1 (非负简单函数的积分)**, $$ \int_{E}f\,\mathrm{d}\mu=\int{f}\chi_{E}\,\mathrm{d}\mu=\sum_{i=1}^{n}c_{i}\mu\left(E\cap{A}_{i}\right). $$ 记 $\lambda\left(E\right):=\int_{E}f\,\mathrm{d}\mu$. 验证 $\lambda$ 是测度: $\lambda\left(\emptyset\right)=\sum_{i=1}^{n}c_{i}\mu\left(\emptyset\cap{A}_{i}\right)=0$; 非负性显然, 因 $c_{i}\ge0$ 且 $\mu\ge0$; $\sigma$-可加性: 设 $E=\bigsqcup_{j=1}^{\infty}E_{j}$ (两两不交). 由 $\mu$ 的 $\sigma$-可加性 (**定义 5.1.2 (测度)**) 与**命题 8.1.2 (简单函数积分的线性性)**, $$ \lambda\left(E\right)=\sum_{i=1}^{n}c_{i}\mu\left(E\cap{A}_{i}\right)=\sum_{i=1}^{n}c_{i}\sum_{j=1}^{\infty}\mu\left(E_{j}\cap{A}_{i}\right)=\sum_{j=1}^{\infty}\sum_{i=1}^{n}c_{i}\mu\left(E_{j}\cap{A}_{i}\right)=\sum_{j=1}^{\infty}\lambda\left(E_{j}\right). $$ 故 $\lambda$ 是 $\mathcal{F}$ 上的测度. 最后, 若 $\mu\left(A\right)=0$, 则 $$ \lambda\left(A\right)=\sum_{i=1}^{n}c_{i}\mu\left(A\cap{A}_{i}\right)\le\sum_{i=1}^{n}c_{i}\mu\left(A\right)=0, $$ 故 $\lambda\left(A\right)=0$. $\blacksquare$

## 3

设 $f\in{L}^{1}$, 证明:

(a) 集合 $\left\{x:f\left(x\right)\ne0\right\}$ 是 $\sigma$-有限的;

(b) 对 $f,g\in{L}^{1}$, $\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\mu$ 对任意可测集 $E$ 成立, 当且仅当 $\int\left|f-g\right|\mathrm{d}\mu=0$, 当且仅当 $f=g$ 关于 $\mu$ 几乎处处.

### 解答 3

(a) 由**定义 8.2.5 (一般可测函数的积分)**, $f=f^{+}-f^{-}$, 故 $\left\{x:f\left(x\right)\ne0\right\}=\left\{x:f^{+}\left(x\right)>0\right\}\cup\left\{x:f^{-}\left(x\right)>0\right\}$. 而

$$
\left\{x:f^{+}\left(x\right)>0\right\}=\bigcup_{n=1}^{\infty}\left\{x:f^{+}\left(x\right)>\frac{1}{n}\right\},
$$

且由**定义 8.2.1 (非负可测函数的积分)**,

$$
\int_{X}f^{+}\mathrm{d}\mu\ge\int_{\left\{f^{+}>\frac{1}{n}\right\}}f^{+}\mathrm{d}\mu\ge\frac{1}{n}\mu\left(\left\{x:f^{+}\left(x\right)>\frac{1}{n}\right\}\right).
$$

因 $f$ 可积, $\int{f}^{+}\mathrm{d}\mu<\infty$, 故 $\mu\left(\left\{x:f^{+}\left(x\right)>\frac{1}{n}\right\}\right)\le{n}\int{f}^{+}\mathrm{d}\mu<\infty$. 于是 $\left\{f^{+}>0\right\}$ 是可数个有限测度集之并; 同理 $\left\{f^{-}>0\right\}$ 亦然. 从而 $\left\{x:f\left(x\right)\ne0\right\}$ 也是可数个有限测度集之并, 在**定义 5.1.5 ($\sigma$-有限测度)** 的意义下是 $\sigma$-有限的.

$\blacksquare$

(b) 记 $h:=\left|f-g\right|\in{L}^{1}$, $h\ge0$.

(1) $\int\left|f-g\right|\mathrm{d}\mu=0\Rightarrow{f}=g$ 几乎处处: 由非负可积函数积分为零则几乎处处为零, $h=0$ 几乎处处, 即 $f=g$ 几乎处处.

(2) $f=g$ 几乎处处 $\Rightarrow\int\left|f-g\right|\mathrm{d}\mu=0$: 因 $h=0$ 在 $\left\{f\ne{g}\right\}$ 之外成立, 而 $\left\{f\ne{g}\right\}$ 是零测集. 由**命题 8.2.4 (积分关于集合的绝对连续性)**, $\int_{\left\{f\ne{g}\right\}}h\,\mathrm{d}\mu=0$, 且 $\int_{\left\{f=g\right\}}h\,\mathrm{d}\mu=0$, 故 $\int{h}\,\mathrm{d}\mu=0$.

(3) $\int\left|f-g\right|\mathrm{d}\mu=0\Rightarrow\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\mu$ 对所有 $E$: 由习题二 1, 3,

$$
\left|\int_{E}f\,\mathrm{d}\mu-\int_{E}g\,\mathrm{d}\mu\right|=\left|\int_{E}\left(f-g\right)\mathrm{d}\mu\right|\le\int_{E}\left|f-g\right|\mathrm{d}\mu\le\int_{X}\left|f-g\right|\mathrm{d}\mu=0.
$$

(4) $\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\mu$ 对所有 $E$ $\Rightarrow\int\left|f-g\right|\mathrm{d}\mu=0$: 取 $E:=\left\{x:f\left(x\right)\ge{g}\left(x\right)\right\}\in\mathcal{F}$. 由习题二 1 线性性, $\int_{E}\left(f-g\right)\mathrm{d}\mu=\int_{E}f\,\mathrm{d}\mu-\int_{E}g\,\mathrm{d}\mu=0$; 在 $E$ 上 $f-g\ge0$, 故 $\int_{E}\left|f-g\right|\mathrm{d}\mu=\int_{E}\left(f-g\right)\mathrm{d}\mu=0$. 同理对 $E^{c}$, $\int_{E^{c}}\left(g-f\right)\mathrm{d}\mu=0$, 在 $E^{c}$ 上 $g-f\ge0$, 故 $\int_{E^{c}}\left|f-g\right|\mathrm{d}\mu=0$. 于是 $\int\left|f-g\right|\mathrm{d}\mu=0$.

综合 (1)(2)(3)(4) 得三条件等价.

$\blacksquare$

## 4

证明:

14. 若 $f\in{L}^{+}$, 令 $\lambda\left(E\right)=\int_{E}f\,\mathrm{d}\mu$ (对 $E\in\mathcal{M}$). 则 $\lambda$ 是 $\mathcal{M}$ 上的测度, 且对任意 $g\in{L}^{+}$, $\int{g}\,\mathrm{d}\lambda=\int{f}g\,\mathrm{d}\mu$.

16. 若 $f\in{L}^{+}$ 且 $\int{f}<\infty$, 对每个 $\varepsilon>0$ 存在 $E\in\mathcal{M}$ 使得 $\mu\left(E\right)<\infty$ 且 $\int_{E}f>\left(\int{f}\right)-\varepsilon$.

### 解答 4

14. 先证 $\lambda$ 是测度. 由**定义 8.1.1 (非负简单函数的积分)** 与**定义 8.2.1 (非负可测函数的积分)**, $\lambda\left(\emptyset\right)=0$ 且非负. 对两两不交的可测集 $\left\{E_{n}\right\}$, 因 $f\chi_{\bigsqcup{E}_{n}}=\sum_{n}f\chi_{E_{n}}$ 且部分和 $\sum_{n=1}^{N}f\chi_{E_{n}}\uparrow{f}\chi_{\bigsqcup{E}_{n}}$ 点点, 由**定理 8.2.2 (单调收敛定理)**,

$$
\lambda\left(\bigsqcup_{n=1}^{\infty}E_{n}\right)=\int{f}\chi_{\bigsqcup{E}_{n}}\mathrm{d}\mu=\sum_{n=1}^{\infty}\int{f}\chi_{E_{n}}\mathrm{d}\mu=\sum_{n=1}^{\infty}\lambda\left(E_{n}\right).
$$

故 $\lambda$ 是 $\mathcal{M}$ 上的测度.

再证换元公式. 若 $g=\sum_{j=1}^{m}a_{j}\chi_{E_{j}}$ 是简单函数 (设 $E_{j}$ 两两不交), 由**定义 8.1.1 (非负简单函数的积分)** 与有限线性性,

$$
\int{g}\,\mathrm{d}\lambda=\sum_{j=1}^{m}a_{j}\lambda\left(E_{j}\right)=\sum_{j=1}^{m}a_{j}\int_{E_{j}}f\,\mathrm{d}\mu=\int\left(\sum_{j=1}^{m}a_{j}\chi_{E_{j}}f\right)\mathrm{d}\mu=\int{f}g\,\mathrm{d}\mu.
$$

对一般 $g\in{L}^{+}$, 由**注 8.2.3 (简单函数逼近)** 取简单函数 $g_{k}\uparrow{g}$. 因 $f\ge0$, $fg_{k}\uparrow{f}g$. 由**定理 8.2.2 (单调收敛定理)** (分别在测度 $\lambda$ 与 $\mu$ 下), $\int{g}_{k}\,\mathrm{d}\lambda\uparrow\int{g}\,\mathrm{d}\lambda$ 且 $\int{f}g_{k}\,\mathrm{d}\mu\uparrow\int{f}g\,\mathrm{d}\mu$. 对每个 $k$ 两式相等 (简单情形), 故极限相等: $\int{g}\,\mathrm{d}\lambda=\int{f}g\,\mathrm{d}\mu$.

$\blacksquare$

16. 对 $n\in\mathbb{N}$, 令 $E_{n}:=\left\{x:f\left(x\right)>\frac{1}{n}\right\}\in\mathcal{M}$. 则 $\left\{E_{n}\right\}$ 单调上升且 $\bigcup_{n}E_{n}=\left\{x:f\left(x\right)>0\right\}$. 由**定义 8.2.1 (非负可测函数的积分)**,

$$
\int{f}\,\mathrm{d}\mu\ge\int_{E_{n}}f\,\mathrm{d}\mu\ge\frac{1}{n}\mu\left(E_{n}\right),
$$

故 $\mu\left(E_{n}\right)\le{n}\int{f}\,\mathrm{d}\mu<\infty$. 又由**定理 8.2.2 (单调收敛定理)**, $\int_{E_{n}}f\,\mathrm{d}\mu\uparrow\int_{\left\{f>0\right\}}f\,\mathrm{d}\mu=\int{f}\,\mathrm{d}\mu$. 故对给定 $\varepsilon>0$, 取 $n$ 充分大使 $\int_{E_{n}}f\,\mathrm{d}\mu>\int{f}\,\mathrm{d}\mu-\varepsilon$, 令 $E:=E_{n}$, 则 $\mu\left(E\right)<\infty$ 且 $\int_{E}f>\int{f}-\varepsilon$.

$\blacksquare$

## 2

证明: $f_{n}$ 依测度收敛到 $f$ 当且仅当对任意子列 $\left\{f_{n_{k}}\right\}$ 存在子子列 $\left\{f_{n'_{k}}\right\}$ 使得 $f_{n'_{k}}\to{f}$ 几乎处处. 特别地, 若 $\phi:\mathbb{R}\to\mathbb{R}$ 是连续函数, 则 $\phi\left(f_{n}\right)\xrightarrow{\mu}\phi\left(f\right)$.

### 解答 2

$\left(\Rightarrow\right)$ 由**定义 9.1.3 (依测度收敛)**, 若 $f_{n}\xrightarrow{\mu}f$, 则任意子列 $\left\{f_{n_{k}}\right\}$ 也依测度收敛到 $f$ (定义中的极限沿子列仍成立). 由**定理 9.1.8 (子序列性质)**, 存在子子列 $\left\{f_{n'_{k}}\right\}$ 使得 $f_{n'_{k}}\to{f}$ 几乎处处.

$\left(\Leftarrow\right)$ 反证. 若 $f_{n}$ 不依测度收敛到 $f$, 则存在 $\varepsilon>0$ 使 $\mu\left(\left\{\left|f_{n}-f\right|>\varepsilon\right\}\right)$ 不趋于 $0$, 即存在 $\delta>0$ 与子列 $\left\{f_{n_{k}}\right\}$ 使

$$
\mu\left(\left\{x:\left|f_{n_{k}}\left(x\right)-f\left(x\right)\right|>\varepsilon\right\}\right)\ge\delta\;\text{对所有~}k.
$$

由**命题 9.1.2 (几乎处处收敛的刻画)**, $\left\{f_{n_{k}}\right\}$ 的任何子子列 $\left\{f_{n'_{j}}\right\}$ 都不能几乎处处收敛到 $f$: 因为

$$
\mu\left(\bigcap_{j=1}^{\infty}\bigcup_{l\ge{j}}\left\{x:\left|f_{n'_{l}}\left(x\right)-f\left(x\right)\right|>\varepsilon\right\}\right)\ge\limsup_{j\to\infty}\mu\left(\left\{x:\left|f_{n'_{j}}\left(x\right)-f\left(x\right)\right|>\varepsilon\right\}\right)\ge\delta>0.
$$

这与假设 (任意子列存在几乎处处收敛子子列) 矛盾. 故 $f_{n}\xrightarrow{\mu}f$.

最后设 $\phi:\mathbb{R}\to\mathbb{R}$ 连续. 对任意子列 $\left\{\phi\left(f_{n_{k}}\right)\right\}$, 由 $f_{n}\xrightarrow{\mu}f$ 和已证的 $\left(\Rightarrow\right)$, 子列 $\left\{f_{n_{k}}\right\}$ 存在子子列 $f_{n'_{k}}\to{f}$ 几乎处处; $\phi$ 连续推出 $\phi\left(f_{n'_{k}}\right)\to\phi\left(f\right)$ 几乎处处. 故 $\left\{\phi\left(f_{n}\right)\right\}$ 的任意子列存在几乎处处收敛子子列, 由已证的 $\left(\Leftarrow\right)$, $\phi\left(f_{n}\right)\xrightarrow{\mu}\phi\left(f\right)$.

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
