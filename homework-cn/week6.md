# week6

> **定义 4.1.3 ($\sigma$-代数)**
> 
> 设 $X$ 非空, $\mathcal{F}\subset\mathcal{P}\left(X\right)$. 称 $\mathcal{F}$ 为 $X$ 上的一个 $\sigma$-代数, 若满足: (1) $X\in\mathcal{F}$; (2) 对补运算封闭: $A\in\mathcal{F}\Rightarrow{A}^{c}\in\mathcal{F}$; (3) 对可数并封闭: $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal{F}$.

> **定义 5.1.2 (测度)**
> 
> 设 $\left(X,\mathcal{F}\right)$ 是一个可测空间. 函数 $\mu:\mathcal{F}\to\left[0,+\infty\right]$ 称为 $\left(X,\mathcal{F}\right)$ 上的一个测度, 如果满足: (1) 非负性: $\mu\left(E\right)\ge0$ 对一切 $E\in\mathcal{F}$ 成立; (2) 零空集性: $\mu\left(\emptyset\right)=0$; (3) 可数可加性 ($\sigma$-可加性): 对任意可数个两两不交的集合 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$, 有 $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **定义 5.1.5 ($\sigma$-有限测度)**
> 
> 设 $\left(X,\mathcal{F},\mu\right)$ 是测度空间. 如果存在一列可测集 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$ 使得 $X=\bigcup_{n=1}^{\infty}E_{n}$ 且 $\mu\left(E_{n}\right)<+\infty$ 对所有 $n\in\mathbb{N}$ 成立, 则称 $\mu$ 为 $\sigma$-有限测度.

> **定理 6.4.5 (勒贝格-斯蒂尔杰斯测度的正则性)**
> 
> 设 $\mu_{F}$ 是由增右连续函数 $F$ 生成的勒贝格-斯蒂尔杰斯测度, $\mathcal{M}^{*}$ 是 $\mu_{F}$-可测集的 $\sigma$-代数. 若 $E\in\mathcal{M}^{*}$, 则

$$
\mu_{F}\left(E\right)=\inf\left\{\mu_{F}\left(U\right):E\subset{U},U\text{~开}\right\}=\sup\left\{\mu_{F}\left(K\right):K\subset{E},K\text{~紧}\right\}.
$$
特别地, 勒贝格测度在 $\left[a,b\right]$ 上内正则.

> **定理 7.1.8 (实值可测函数的运算封闭性)**
> 
> 设 $f,g:X\to\mathbb{R}$ 可测, $c\in\mathbb{R}$, 则 $cf$, $f+g$, $fg$, $\max\left(f,g\right)$, $\min\left(f,g\right)$ 可测; 若 $\left\{f_{n}\right\}$ 可测且点点收敛, 则极限函数可测.

> **定理 7.2.2 (可测函数的构造)**
> 
> 若 $f:X\to\left[0,+\infty\right]$ 是非负可测函数, 则存在一列非负简单函数 $\left\{f_{n}\right\}$ 满足 $0\le{f}_{1}\le{f}_{2}\le\cdots\le{f}$ 且 $\lim_{n\to\infty}f_{n}\left(x\right)=f\left(x\right)$ 对每个 $x\in{X}$ 成立.

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

> **注 8.2.3 (简单函数逼近)**
> 
> 单调收敛定理告诉我们积分可以用简单函数逼近.

> **命题 8.2.4 (积分关于集合的绝对连续性)**
> 
> 设 $f$ 为非负可测函数, 则 $A\mapsto\int_{A}f\,\mathrm{d}\mu$ 为一个测度; 若 $\mu\left(A\right)=0$, 则 $\int_{A}f\,\mathrm{d}\mu=0$.

> **定义 8.2.5 (一般可测函数的积分)**
> 
> 设 $f:X\to\left[-\infty,+\infty\right]$ 是可测函数. 定义 $f$ 的正部和负部分别为 $f^{+}\left(x\right)=\max\left\{f\left(x\right),0\right\}$, $f^{-}\left(x\right)=\max\left\{-f\left(x\right),0\right\}$. 若至少有一个积分 $\int_{X}f^{+}\mathrm{d}\mu$, $\int_{X}f^{-}\mathrm{d}\mu$ 有限, 则定义 $f$ 的积分为 $\int_{X}f\,\mathrm{d}\mu=\int_{X}f^{+}\mathrm{d}\mu-\int_{X}f^{-}\mathrm{d}\mu$. 若 $\int_{X}f^{+}\mathrm{d}\mu<\infty$ 且 $\int_{X}f^{-}\mathrm{d}\mu<\infty$, 则称 $f$ 是可积的.

> **定理 8.2.7 (法图引理)**
> 
> 设 $\left(X,\mathcal{F},\mu\right)$ 是测度空间, $\left\{f_{n}\right\}$ 是一列非负可测函数, 则 $\int_{X}\liminf_{n\to\infty}f_{n}\,\mathrm{d}\mu\le\liminf_{n\to\infty}\int_{X}f_{n}\,\mathrm{d}\mu$.

> **定理 8.2.9 (控制收敛定理)**
> 
> 设 $\left(X,\mathcal{F},\mu\right)$ 是测度空间, $\left\{f_{n}\right\}$ 是一列可测函数, 若存在可积函数 $g$ 使 $\left|f_{n}\right|\le{g}$ 对所有 $n$ 成立, 且 $f_{n}\to{f}$ 几乎处处, 则 $f$ 可积且 $\int{f}\,\mathrm{d}\mu=\lim_{n\to\infty}\int{f}_{n}\,\mathrm{d}\mu$.

> **引理 8.2.13 (级数逐项积分)**
> 
> 设 $\left\{f_{n}\right\}$ 是一列可测函数, 且 $\sum_{n=1}^{\infty}\int_{X}\left|f_{n}\right|\mathrm{d}\mu<\infty$, 则 $\int_{X}\left(\sum_{n=1}^{\infty}f_{n}\right)\mathrm{d}\mu=\sum_{n=1}^{\infty}\int_{X}f_{n}\,\mathrm{d}\mu$.

> **定理 8.2.17 (参数积分)**
> 
> 设 $f:X\times\left[a,b\right]\to\mathbb{R}$, 且对每个 $t\in\left[a,b\right]$, 函数 $f\left(\cdot,t\right):X\to\mathbb{R}$ 可积. 令 $F\left(t\right)=\int_{X}f\left(x,t\right)\mathrm{d}\mu\left(x\right)$. (a) 若存在 $g\in{L}^{1}\left(\mu\right)$ 使得对所有 $x,t$ 有 $\left|f\left(x,t\right)\right|\le{g}\left(x\right)$, 且对每个 $x$ 有 $\lim_{t\to{t}_{0}}f\left(x,t\right)=f\left(x,t_{0}\right)$, 则 $\lim_{t\to{t}_{0}}F\left(t\right)=F\left(t_{0}\right)$; (b) 若偏导数 $\partial{f}/\partial{t}$ 存在, 且存在 $g\in{L}^{1}\left(\mu\right)$ 使得对所有 $x,t$ 有 $\left|\frac{\partial{f}}{\partial{t}}\left(x,t\right)\right|\le{g}\left(x\right)$, 则 $F$ 可微, 且 $F'\left(t\right)=\int\frac{\partial{f}}{\partial{t}}\left(x,t\right)\mathrm{d}\mu\left(x\right)$.

> **定义 9.1.1 (几乎处处收敛)**
> 
> 设 $\left\{f_{n}\right\}$ 是一列可测函数, $f$ 是可测函数. 如果存在零测度集 $E$ 使对所有 $x\notin{E}$ 有 $\lim_{n\to\infty}f_{n}\left(x\right)=f\left(x\right)$, 则称 $\left\{f_{n}\right\}$ $\mu$-几乎处处收敛到 $f$, 记作 $f_{n}\xrightarrow{\text{a.e.}}f$.

> **命题 9.1.2 (几乎处处收敛的刻画)**
> 
> $f_{n}\xrightarrow{\text{a.e.}}f$ 当且仅当对任意的 $\varepsilon>0$,

$$
\mu\left(\bigcap_{k=1}^{\infty}\bigcup_{n=k}^{\infty}\left\{x:\left|f_{n}\left(x\right)-f\left(x\right)\right|>\varepsilon\right\}\right)=0.
$$

> **定义 9.1.3 (依测度收敛)**
> 
> 设 $\left\{f_{n}\right\}$ 是一列可测函数, $f$ 是可测函数. 如果对任意 $\varepsilon>0$ 有 $\lim_{n\to\infty}\mu\left(\left\{x:\left|f_{n}\left(x\right)-f\left(x\right)\right|>\varepsilon\right\}\right)=0$, 则称 $\left\{f_{n}\right\}$ 依测度收敛到 $f$, 记作 $f_{n}\xrightarrow{\mu}f$.

> **定理 9.1.8 (子序列性质)**
> 
> 如果 $f_{n}\xrightarrow{\mu}f$, 则存在子序列 $\left\{f_{n_{k}}\right\}$ 使得 $f_{n_{k}}\to{f}$ 几乎处处.

> **定理 9.1.15 (叶戈罗夫定理)**
> 
> 设 $\mu\left(X\right)<\infty$ 且 $f_{n}\to{f}$ 几乎处处. 则对任意 $\delta>0$ 存在可测集 $E\subset{X}$ 使得 $\mu\left(E\right)<\delta$, 且在 $X\setminus{E}$ 上 $f_{n}$ 一致收敛到 $f$. 特别地, 在有限测度空间中, 几乎处处收敛蕴含依测度收敛.

## 1

证明:

20. (广义控制收敛定理) 若 $f_{n},g_{n},f,g\in{L}^{1}$, $f_{n}\to{f}$ 且 $g_{n}\to{g}$ 几乎处处, $\left|f_{n}\right|\le{g}_{n}$, 且 $\int{g}_{n}\to\int{g}$, 则 $\int{f}_{n}\to\int{f}$.

23. 给定有界函数 $f:\left[a,b\right]\to\mathbb{R}$, 令

$$
H\left(x\right)=\limsup_{\delta\to0}\sup_{0<\left|y-x\right|\le\delta}f\left(y\right),\qquad{h}\left(x\right)=\liminf_{\delta\to0}\inf_{0<\left|y-x\right|\le\delta}f\left(y\right).
$$

证明: (a) $H\left(x\right)=h\left(x\right)$ 当且仅当 $f$ 在 $x$ 连续; (b) $H=G$ 几乎处处, $h=g$ 几乎处处, 且 $\int_{\left(a,b\right)}h\,\mathrm{d}m=\underline{\int}f$. 由此 $f$ 黎曼可积当且仅当 $f$ 的不连续点集测度为 0.

27. 设 $f_{n}\left(x\right)=ae^{-nax}-be^{-nbx}$, 其中 $0<{}a<{}b$. (a) $\sum_{n=1}^{\infty}\int_{0}^{\infty}\left|f_{n}\left(x\right)\right|\mathrm{d}x=\infty$; (b) $\sum_{n=1}^{\infty}\int_{0}^{\infty}f_{n}\left(x\right)\mathrm{d}x=0$; (c) $\sum_{n=1}^{\infty}f_{n}\in{L}^{1}\left(\left[0,\infty\right),m\right)$, 且 $\int_{0}^{\infty}\sum_{n=1}^{\infty}f_{n}\left(x\right)\mathrm{d}x=\log\left(b/a\right)$.

29. 通过对等式 $\int_{0}^{\infty}e^{-tx}\mathrm{d}x=1/t$ 求导, 证明 $\int_{0}^{\infty}x^{n}e^{-x}\mathrm{d}x=n!$; 类似地, 通过对等式 $\int_{-\infty}^{\infty}e^{-tx^{2}}\mathrm{d}x=\sqrt{\pi/t}$ 求导, 证明 $\int_{-\infty}^{\infty}x^{2n}e^{-x^{2}}\mathrm{d}x=\frac{\left(2n\right)!\sqrt\pi}{4^{n}n!}$.

### 解答 1

20. 由 $g_{n}\to{g}$ 几乎处处且 $\left|f_{n}\right|\le{g}_{n}$, 取极限得 $\left|f\right|\le{g}$ 几乎处处, 故 $f\in{L}^{1}$. 因 $\left|f_{n}\right|\le{g}_{n}$ 意味着 $-g_{n}\le{f}_{n}\le{g}_{n}$, 函数列 $\left\{g_{n}+f_{n}\right\}$ 与 $\left\{g_{n}-f_{n}\right\}$ 非负, 且分别几乎处处收敛于 $g+f$ 与 $g-f$. 由**定理 8.2.7 (法图引理)**,

$$
\int\left(g+f\right)\mathrm{d}\mu\le\liminf_{n\to\infty}\int\left(g_{n}+f_{n}\right)\mathrm{d}\mu=\int{g}\,\mathrm{d}\mu+\liminf_{n\to\infty}\int{f}_{n}\,\mathrm{d}\mu,
$$

因 $\int{g}_{n}\to\int{g}$ 且积分为有限 (线性性, 习题二). 两边减 $\int{g}\,\mathrm{d}\mu$ 得 $\int{f}\,\mathrm{d}\mu\le\liminf_{n\to\infty}\int{f}_{n}\,\mathrm{d}\mu$. 同理, 对 $\left\{g_{n}-f_{n}\right\}$ 用法图引理,

$$
\int\left(g-f\right)\mathrm{d}\mu\le\liminf_{n\to\infty}\int\left(g_{n}-f_{n}\right)\mathrm{d}\mu=\int{g}\,\mathrm{d}\mu-\limsup_{n\to\infty}\int{f}_{n}\,\mathrm{d}\mu,
$$

即 $\limsup_{n\to\infty}\int{f}_{n}\,\mathrm{d}\mu\le\int{f}\,\mathrm{d}\mu$. 综合得

$$
\int{f}\,\mathrm{d}\mu\le\liminf_{n\to\infty}\int{f}_{n}\,\mathrm{d}\mu\le\limsup_{n\to\infty}\int{f}_{n}\,\mathrm{d}\mu\le\int{f}\,\mathrm{d}\mu,
$$

故 $\lim_{n\to\infty}\int{f}_{n}\,\mathrm{d}\mu=\int{f}\,\mathrm{d}\mu$. $\blacksquare$

23. 用黎曼积分与达布和 的记号. $f$ 黎曼可积当且仅当 $\overline{\int}f=\underline{\int}f$.

(a) 设 $f$ 在 $x$ 连续. 对 $\varepsilon>0$ 存在 $\delta>0$ 使 $\left|y-x\right|<\delta\Rightarrow\left|f\left(y\right)-f\left(x\right)\right|<\varepsilon$. 则对 $0<\left|y-x\right|\le\delta$, 有

$$
f\left(x\right)-\varepsilon\le\inf_{0<\left|y-x\right|\le\delta}f\left(y\right)\le{f}\left(x\right)\le\sup_{0<\left|y-x\right|\le\delta}f\left(y\right)\le{f}\left(x\right)+\varepsilon.
$$

令 $\delta\to0$, 由 $\varepsilon$ 任意得 $h\left(x\right)\ge{f}\left(x\right)\ge{H}\left(x\right)$; 但定义中恒有 $h\left(x\right)\le{f}\left(x\right)\le{H}\left(x\right)$, 故 $H\left(x\right)=h\left(x\right)=f\left(x\right)$.

反之, 设 $H\left(x\right)=h\left(x\right)=:L$. 对 $\varepsilon>0$, 由极限定义存在 $\delta>0$ 使对 $0<\delta'<\delta$ 有

$$
\inf_{0<\left|y-x\right|\le\delta'}f\left(y\right)>{}L-\varepsilon,\qquad\sup_{0<\left|y-x\right|\le\delta'}f\left(y\right)<{}L+\varepsilon.
$$

取 $\delta'=\delta$, 则对 $0<\left|y-x\right|\le\delta$ 有 $L-\varepsilon<{}f\left(y\right)<{}L+\varepsilon$; 又 $f\left(x\right)$ 介于 $\inf$ 与 $\sup$ 之间, 故 $L-\varepsilon<{}f\left(x\right)<{}L+\varepsilon$. 于是 $\left|f\left(y\right)-f\left(x\right)\right|<2\varepsilon$ 对 $0<\left|y-x\right|\le\delta$ 成立, 即 $f$ 在 $x$ 连续.

(b) 取分割列 $\left\{P_{k}\right\}$, 使网格 $\max_{i}\left(t_{i}-t_{i-1}\right)\to0$ 且 $P_{k}\subset{P}_{k+1}$ (逐次加密), 定义

$$
G_{P_{k}}=\sum_{i}M_{i}^{\left(k\right)}\chi_{\left(t_{i-1}^{\left(k\right)},t_{i}^{\left(k\right)}\right)},\qquad{g}_{P_{k}}=\sum_{i}m_{i}^{\left(k\right)}\chi_{\left(t_{i-1}^{\left(k\right)},t_{i}^{\left(k\right)}\right)},
$$

并令 $G=\lim_{k}G_{P_{k}}$, $g=\lim_{k}g_{P_{k}}$. 固定 $x$ 不属于任何 $P_{k}$ 的分点 (所有分割的分点之并至多可数, 测度为 0). 设 $x\in\left(t_{i-1}^{\left(k\right)},t_{i}^{\left(k\right)}\right)$, 则 $G_{P_{k}}\left(x\right)=M_{i}^{\left(k\right)}=\sup_{\left[t_{i-1}^{\left(k\right)},t_{i}^{\left(k\right)}\right]}f$. 随 $k\to\infty$ 该小区间收缩到 $\left\{x\right\}$, 上确界递减趋于 $\sup_{0<\left|y-x\right|\le\delta}f\left(y\right)$ 随 $\delta\to0$ 的极限, 即 $H\left(x\right)$. 故 $G\left(x\right)=H\left(x\right)$; 同理 $g\left(x\right)=h\left(x\right)$. 因此在 $\left[a,b\right]$ 去掉可数分点集后 $H=G$, $h=g$ 几乎处处.

又 $G_{P_{k}}$ 有界且 $g_{P_{k}}\le{f}\le{G}_{P_{k}}$, 由**定理 8.2.9 (控制收敛定理)**,

$$
\int{H}\,\mathrm{d}m=\int{G}\,\mathrm{d}m=\lim_{k}\int{G}_{P_{k}}\mathrm{d}m=\lim_{k}\overline{S}\left(P_{k}\right)=\overline{\int}f,
$$

$$
\int{h}\,\mathrm{d}m=\int{g}\,\mathrm{d}m=\lim_{k}\int{g}_{P_{k}}\mathrm{d}m=\lim_{k}\underline{S}\left(P_{k}\right)=\underline{\int}f.
$$

特别地 $\int_{\left(a,b\right)}h\,\mathrm{d}m=\underline{\int}f$. 于是

$$
f\text{~黎曼可积}\iff\overline{\int}f=\underline{\int}f\iff\int{H}\,\mathrm{d}m=\int{h}\,\mathrm{d}m\iff\int\left(H-h\right)\mathrm{d}m=0.
$$

因 $H\ge{h}$, 由习题三 (b) 得 $\int\left(H-h\right)\mathrm{d}m=0\iff{H}=h$ 几乎处处. 结合 (a) ($H=h\iff{f}$ 连续于 $x$) 得 $f$ 黎曼可积当且仅当 $f$ 的不连续点集测度为 0. 此时黎曼积分 $\overline{\int}f=\int{H}\,\mathrm{d}m=\int{f}\,\mathrm{d}m$ (因 $H=f$ 几乎处处). $\blacksquare$

27. 先求 $f_{n}$ 的零点. 令 $f_{n}\left(x\right)=0$ 得 $ae^{-nax}=be^{-nbx}$, 即 $e^{n\left(b-a\right)x}=b/a$, 故唯一零点

$$
x_{n}=\frac{\log\left(b/a\right)}{n\left(b-a\right)}.
$$

在 $\left[0,x_{n}\right)$ 上 $f_{n}<0$, 在 $\left(x_{n},\infty\right)$ 上 $f_{n}>0$.

(a) 计算

$$
\int_{0}^{\infty}\left|f_{n}\right|\mathrm{d}x=\int_{0}^{x_{n}}\left(be^{-nbx}-ae^{-nax}\right)\mathrm{d}x+\int_{x_{n}}^{\infty}\left(ae^{-nax}-be^{-nbx}\right)\mathrm{d}x.
$$

利用 $\int_{0}^{x_{n}}be^{-nbx}\mathrm{d}x=\frac{1}{n}\left(1-e^{-nbx_{n}}\right)$, $\int_{0}^{x_{n}}ae^{-nax}\mathrm{d}x=\frac{1}{n}\left(1-e^{-nax_{n}}\right)$, $\int_{x_{n}}^{\infty}ae^{-nax}\mathrm{d}x=\frac{1}{n}e^{-nax_{n}}$, $\int_{x_{n}}^{\infty}be^{-nbx}\mathrm{d}x=\frac{1}{n}e^{-nbx_{n}}$, 得

$$
\int_{0}^{\infty}\left|f_{n}\right|\mathrm{d}x=\frac{2}{n}\left(e^{-nax_{n}}-e^{-nbx_{n}}\right).
$$

记 $t=e^{-nx_{n}}$, 则由零点条件 $at^{a}=bt^{b}$, 即 $t^{a-b}=b/a$, 故 $t=\left(b/a\right)^{1/\left(a-b\right)}\in\left(0,1\right)$. 因 $t<1$ 且 $a<{}b$, 幂函数 $\lambda\mapsto{t}^{\lambda}$ 递减, 故 $t^{a}>{}t^{b}$, 常数 $c:=2\left(t^{a}-t^{b}\right)>0$. 因此

$$
\sum_{n=1}^{\infty}\int_{0}^{\infty}\left|f_{n}\right|\mathrm{d}x=c\sum_{n=1}^{\infty}\frac{1}{n}=\infty.
$$

(b) 逐项计算:

$$
\int_{0}^{\infty}f_{n}\left(x\right)\mathrm{d}x=\int_{0}^{\infty}ae^{-nax}\mathrm{d}x-\int_{0}^{\infty}be^{-nbx}\mathrm{d}x=\frac{1}{n}-\frac{1}{n}=0,
$$

故 $\sum_{n=1}^{\infty}\int_{0}^{\infty}f_{n}\left(x\right)\mathrm{d}x=0$.

(c) 由几何级数 $\sum_{n=1}^{\infty}e^{-nax}=\frac{e^{-ax}}{1-e^{-ax}}=\frac{1}{e^{ax}-1}$,

$$
\sum_{n=1}^{\infty}f_{n}\left(x\right)=a\sum_{n=1}^{\infty}e^{-nax}-b\sum_{n=1}^{\infty}e^{-nbx}=\frac{a}{e^{ax}-1}-\frac{b}{e^{bx}-1}.
$$

当 $x\to0^{+}$ 时, $\frac{a}{e^{ax}-1}=\frac{1}{x}-\frac{a}{2}+O\left(x\right)$, 故差 $\to\frac{b-a}{2}+O\left(x\right)$ 有限; 当 $x\to\infty$ 时指数衰减. 故 $\sum{f}_{n}\in{L}^{1}\left(\left[0,\infty\right),m\right)$.

对 $R>0$, 换元 $u=ax$ 与 $u=bx$:

$$
\int_{0}^{R}\frac{a}{e^{ax}-1}\mathrm{d}x=\int_{0}^{aR}\frac{\mathrm{d}u}{e^{u}-1},\qquad\int_{0}^{R}\frac{b}{e^{bx}-1}\mathrm{d}x=\int_{0}^{bR}\frac{\mathrm{d}u}{e^{u}-1}.
$$

故

$$
\int_{0}^{R}\left(\frac{a}{e^{ax}-1}-\frac{b}{e^{bx}-1}\right)\mathrm{d}x=\int_{aR}^{bR}\frac{\mathrm{d}u}{e^{u}-1}.
$$

由于 $\frac{1}{e^{u}-1}-\frac{1}{u}=O\left(e^{-u}\right)$ 在无穷远可积, $\int_{aR}^{bR}\frac{\mathrm{d}u}{e^{u}-1}=\int_{aR}^{bR}\frac{\mathrm{d}u}{u}+o\left(1\right)$, 令 $R\to\infty$ 得

$$
\int_{0}^{\infty}\sum_{n=1}^{\infty}f_{n}\left(x\right)\mathrm{d}x=\lim_{R\to\infty}\int_{aR}^{bR}\frac{\mathrm{d}u}{u}=\log\left(b/a\right).
$$

注意到这里 $\sum\int\left|f_{n}\right|=\infty$ (由 a), 不满足**引理 8.2.13 (级数逐项积分)** 的条件 $\sum\int\left|f_{n}\right|<\infty$, 故不能逐项积分; 事实上 $\int\sum{f}_{n}=\log\left(b/a\right)\ne\sum\int{f}_{n}=0$, 正说明该条件是本质的. $\blacksquare$

29. 用**定理 8.2.17 (参数积分)** (b) (积分号下求导). 固定 $t_{0}>0$, 在 $t$ 的紧邻域 $\left[t_{0}/2,t_{0}\right]$ 上考察.

情形 1. 令 $F\left(t\right)=\int_{0}^{\infty}e^{-tx}\mathrm{d}x=\frac{1}{t}$ ($t>0$). 对每个 $k\ge1$, 在 $t\in\left[t_{0}/2,t_{0}\right]$ 上 $\left|\frac{\partial^{k}}{\partial{t}^{k}}e^{-tx}\right|=x^{k}e^{-tx}\le{x}^{k}e^{-\left(t_{0}/2\right)x}\in{L}^{1}\left(\left[0,\infty\right)\right)$, 故定理可反复应用:

$$
F^{\left(n\right)}\left(t\right)=\int_{0}^{\infty}\left(-x\right)^{n}e^{-tx}\mathrm{d}x.
$$

又 $F\left(t\right)=1/t$, 其 $n$ 阶导数为 $F^{\left(n\right)}\left(t\right)=\left(-1\right)^{n}n!/t^{n+1}$. 取 $t=1$:

$$
\int_{0}^{\infty}\left(-x\right)^{n}e^{-x}\mathrm{d}x=\left(-1\right)^{n}n!,
$$

即 $\int_{0}^{\infty}x^{n}e^{-x}\mathrm{d}x=n!$.

情形 2. 令 $G\left(s\right)=\int_{-\infty}^{\infty}e^{-sx^{2}}\mathrm{d}x=\sqrt{\pi/s}=\sqrt\pi\,s^{-1/2}$ ($s>0$). 对每个 $k\ge1$, 在 $s\in\left[s_{0}/2,s_{0}\right]$ 上 $\left|\frac{\partial^{k}}{\partial{s}^{k}}e^{-sx^{2}}\right|=x^{2k}e^{-sx^{2}}\le{x}^{2k}e^{-\left(s_{0}/2\right)x^{2}}\in{L}^{1}\left(\mathbb{R}\right)$, 故可反复求导:

$$
G^{\left(n\right)}\left(s\right)=\int_{-\infty}^{\infty}\left(-x^{2}\right)^{n}e^{-sx^{2}}\mathrm{d}x=\left(-1\right)^{n}\int_{-\infty}^{\infty}x^{2n}e^{-sx^{2}}\mathrm{d}x.
$$

又

$$
G^{\left(n\right)}\left(s\right)=\sqrt\pi\left(-\frac{1}{2}\right)\left(-\frac{3}{2}\right)\cdots\left(-\frac{2n-1}{2}\right)s^{-\frac{2n+1}{2}}.
$$

取 $s=1$:

$$
\left(-1\right)^{n}\int_{-\infty}^{\infty}x^{2n}e^{-x^{2}}\mathrm{d}x=\sqrt\pi\left(-1\right)^{n}\frac{1\cdot3\cdots\left(2n-1\right)}{2^{n}},
$$

即 $\int_{-\infty}^{\infty}x^{2n}e^{-x^{2}}\mathrm{d}x=\sqrt\pi\frac{1\cdot3\cdots\left(2n-1\right)}{2^{n}}$. 由 $1\cdot3\cdots\left(2n-1\right)=\frac{\left(2n\right)!}{2^{n}n!}$, 得

$$
\int_{-\infty}^{\infty}x^{2n}e^{-x^{2}}\mathrm{d}x=\frac{\left(2n\right)!\sqrt\pi}{4^{n}n!}.
$$

$\blacksquare$

## 2

证明: $f_{n}$ 依测度收敛到 $f$ 当且仅当对任意子列 $\left\{f_{n_{k}}\right\}$ 存在子子列 $\left\{f_{n'_{k}}\right\}$ 使得 $f_{n'_{k}}\to{f}$ 几乎处处. 特别地, 若 $\phi:\mathbb{R}\to\mathbb{R}$ 是连续函数, 则 $\phi\left(f_{n}\right)\xrightarrow{\mu}\phi\left(f\right)$.

### 解答 2

$\left(\Rightarrow\right)$ 由**定义 9.1.3 (依测度收敛)**, 若 $f_{n}\xrightarrow{\mu}f$, 则任意子列 $\left\{f_{n_{k}}\right\}$ 也依测度收敛到 $f$ (定义中的极限沿子列仍成立). 由**定理 9.1.8 (子序列性质)**, 存在子子列 $\left\{f_{n'_{k}}\right\}$ 使得 $f_{n'_{k}}\to{f}$ 几乎处处.

$\left(\Leftarrow\right)$ 反证. 若 $f_{n}$ 不依测度收敛到 $f$, 则存在 $\varepsilon>0$ 使 $\mu\left(\left\{\left|f_{n}-f\right|>\varepsilon\right\}\right)$ 不趋于 $0$, 即存在 $\delta>0$ 与子列 $\left\{f_{n_{k}}\right\}$ 使

$$
\mu\left(\left\{x:\left|f_{n_{k}}\left(x\right)-f\left(x\right)\right|>\varepsilon\right\}\right)\ge\delta\,\text{对所有~}k.
$$

由**命题 9.1.2 (几乎处处收敛的刻画)**, $\left\{f_{n_{k}}\right\}$ 的任何子子列 $\left\{f_{n'_{j}}\right\}$ 都不能几乎处处收敛到 $f$: 因为

$$
\mu\left(\bigcap_{j=1}^{\infty}\bigcup_{l\ge{j}}\left\{x:\left|f_{n'_{l}}\left(x\right)-f\left(x\right)\right|>\varepsilon\right\}\right)\ge\limsup_{j\to\infty}\mu\left(\left\{x:\left|f_{n'_{j}}\left(x\right)-f\left(x\right)\right|>\varepsilon\right\}\right)\ge\delta>0.
$$

这与假设 (任意子列存在几乎处处收敛子子列) 矛盾. 故 $f_{n}\xrightarrow{\mu}f$.

最后设 $\phi:\mathbb{R}\to\mathbb{R}$ 连续. 对任意子列 $\left\{\phi\left(f_{n_{k}}\right)\right\}$, 由 $f_{n}\xrightarrow{\mu}f$ 和已证的 $\left(\Rightarrow\right)$, 子列 $\left\{f_{n_{k}}\right\}$ 存在子子列 $f_{n'_{k}}\to{f}$ 几乎处处; $\phi$ 连续推出 $\phi\left(f_{n'_{k}}\right)\to\phi\left(f\right)$ 几乎处处. 故 $\left\{\phi\left(f_{n}\right)\right\}$ 的任意子列存在几乎处处收敛子子列, 由已证的 $\left(\Leftarrow\right)$, $\phi\left(f_{n}\right)\xrightarrow{\mu}\phi\left(f\right)$. $\blacksquare$
