# week10

> **定义 11.1.1 (符号测度)**
> 
> 设 $\left(X,\mathcal{F}\right)$ 是一个可测空间. 函数 $\nu:\mathcal{F}\to\mathbb{R}\cup\left\{+\infty\right\}$ 或 $\mathbb{R}\cup\left\{-\infty\right\}$ 称为符号测度, 若满足: (1) $\nu\left(\emptyset\right)=0$; (2) 可列可加性: 对任意一列互不相交的可测集 $\left\{E_{i}\right\}_{i=1}^{\infty}\subset\mathcal{F}$, 有 $\nu\left(\bigcup_{i=1}^{\infty}E_{i}\right)=\sum_{i=1}^{\infty}\nu\left(E_{i}\right)$; (3) $\nu$ 不能同时取 $+\infty$ 与 $-\infty$ 为值.

> **命题 11.1.2 (符号测度的基本性质)**
> 
> 设 $\nu$ 是符号测度, 则: (1) 有限可加性: 对任意有限个互不相交的 $E_{1},\dots,E_{n}\in\mathcal{F}$, 有 $\nu\left(\bigcup_{i=1}^{n}E_{i}\right)=\sum_{i=1}^{n}\nu\left(E_{i}\right)$; (2) 下连续性: 若 $\left\{E_{j}\right\}$ 单调上升可测, 则 $\lim_{j\to\infty}\nu\left(E_{j}\right)=\nu\left(\bigcup_{j}E_{j}\right)$; (3) 上连续性: 若 $\left\{E_{j}\right\}$ 单调下降可测且 $\nu\left(E_{1}\right)<\infty$, 则 $\lim_{j\to\infty}\nu\left(E_{j}\right)=\nu\left(\bigcap_{j}E_{j}\right)$.

> **定义 11.2.1 (正集,负集,零集)**
> 
> 设 $\nu$ 是 $\left(X,\mathcal{F}\right)$ 上的符号测度. 称 $P\in\mathcal{F}$ 为正集 (记为 $P\gtrsim0$), 若对任意 $E\in\mathcal{F}$ 且 $E\subset{P}$, 有 $\nu\left(E\right)\ge0$; 称 $N\in\mathcal{F}$ 为负集 (记为 $N\lesssim0$), 若对任意 $E\in\mathcal{F}$ 且 $E\subset{N}$, 有 $\nu\left(E\right)\le0$; 称 $Z\in\mathcal{F}$ 为零集, 若对任意 $E\in\mathcal{F}$ 且 $E\subset{Z}$, 有 $\nu\left(E\right)=0$.

> **引理 11.2.2 (正集的性质)**
> 
> (1) 正集的任意可测子集是正集; (2) 正集的可列并是正集; (3) 若 $\left\{P_{n}\right\}$ 是正集列, 则 $\bigcap_{n=1}^{\infty}P_{n}$ 是正集. 上述性质对负集仍然成立.

> **引理 11.2.4 (非负集的判定)**
> 
> 设 $\nu$ 是符号测度. 若 $E$ 不是负集, 则存在正集 $F\subset{E}$ 使得 $\nu\left(F\right)>0$.

> **定理 11.3.2 (哈恩分解定理)**
> 
> 设 $\nu$ 是 $\left(X,\mathcal{F}\right)$ 上的符号测度, 则存在 $X$ 的分解 $X=P\cup{N}$, 其中 $P$ 是正集, $N$ 是负集, $P\cap{N}=\emptyset$; 并且该分解在相差一个 $\nu$-零集的意义下是唯一的.

> **定义 11.4.1 (相互奇异的符号测度)**
> 
> 设 $\mu$ 和 $\nu$ 是可测空间 $\left(X,\mathcal{F}\right)$ 上的两个符号测度. 若存在可测集 $E\in\mathcal{F}$ 使得 $E$ 为 $\mu$-零集且 $E^{c}$ 为 $\nu$-零集, 则称 $\mu$ 和 $\nu$ 相互奇异, 记为 $\mu\perp\nu$.

> **定理 11.4.3 (若尔当分解定理)**
> 
> 设 $\nu$ 是 $\left(X,\mathcal{F}\right)$ 上的符号测度, 则存在唯一的一对相互奇异的正测度 $\nu^{+}$ 和 $\nu^{-}$, 使得 $\nu=\nu^{+}-\nu^{-}$.

> **定义 11.4.4 (变差测度)**
> 
> 设 $\nu$ 是符号测度, 其若尔当分解为 $\nu=\nu^{+}-\nu^{-}$. 称 $\nu^{+}$ 为 $\nu$ 的正变差, $\nu^{-}$ 为 $\nu$ 的负变差, $\left|\nu\right|=\nu^{+}+\nu^{-}$ 为 $\nu$ 的全变差测度.

> **定义 11.5.1 (绝对连续性)**
> 
> 设 $\mu$ 是正测度, $\nu$ 是符号测度. 称 $\nu$ 关于 $\mu$ 绝对连续 (记为 $\nu\ll\mu$), 若对任意 $E\in\mathcal{F}$ 有 $\mu\left(E\right)=0\Rightarrow\nu\left(E\right)=0$.

## 4

设 $\nu$ 是 $\left(X,\mathcal{M}\right)$ 上的符号测度, $E\in\mathcal{M}$.

(a) $\nu^{+}\left(E\right)=\sup\left\{\nu\left(F\right):F\in\mathcal{M},F\subset{E}\right\}$, 且 $\nu^{-}\left(E\right)=-\inf\left\{\nu\left(F\right):F\in\mathcal{M},F\subset{E}\right\}$;

(b) $\left|\nu\right|\left(E\right)=\sup\left\{\sum_{i}\left|\nu\left(E_{i}\right)\right|:n\in\mathbb{N},E_{1},\dots,E_{n}\text{~两两不交},\bigcup_{i=1}^{n}E_{i}=E\right\}$.

### 解答 4

(a). 取 $\nu$ 的哈恩分解 $X=P\cup{N}$ (**定理 11.3.2 (哈恩分解定理)**), 则 $\nu^{+}\left(E\right)=\nu\left(E\cap{P}\right)$, $\nu^{-}\left(E\right)=-\nu\left(E\cap{N}\right)$ (**定理 11.4.3 (若尔当分解定理)**).

对任意 $F\in\mathcal{M}$ 且 $F\subset{E}$, 由 $\nu=\nu^{+}-\nu^{-}$ 及 $\nu^{-}\ge0$ 得 $\nu\left(F\right)=\nu^{+}\left(F\right)-\nu^{-}\left(F\right)\le\nu^{+}\left(F\right)\le\nu^{+}\left(E\right)$ (最后一式由 $\nu^{+}$ 的单调性, 因 $F\subset{E}$). 故 $\sup\left\{\nu\left(F\right):F\subset{E}\right\}\le\nu^{+}\left(E\right)$. 取 $F=E\cap{P}\subset{E}$, 则 $\nu\left(E\cap{P}\right)=\nu^{+}\left(E\cap{P}\right)-\nu^{-}\left(E\cap{P}\right)=\nu^{+}\left(E\cap{P}\right)=\nu^{+}\left(E\right)$ (因 $E\cap{P}\subset{P}$ 是正集, $\nu^{-}\left(E\cap{P}\right)=0$). 故 $\sup\ge\nu^{+}\left(E\right)$. 合并得 $\nu^{+}\left(E\right)=\sup\left\{\nu\left(F\right):F\subset{E}\right\}$.

同理, 对 $F\subset{E}$ 有 $\nu\left(F\right)=\nu^{+}\left(F\right)-\nu^{-}\left(F\right)\ge-\nu^{-}\left(F\right)\ge-\nu^{-}\left(E\right)$, 故 $\inf\left\{\nu\left(F\right):F\subset{E}\right\}\ge-\nu^{-}\left(E\right)$, 即 $-\inf\left\{\nu\left(F\right):F\subset{E}\right\}\le\nu^{-}\left(E\right)$. 取 $F=E\cap{N}$, 则 $\nu\left(E\cap{N}\right)=-\nu^{-}\left(E\cap{N}\right)=-\nu^{-}\left(E\right)$, 故 $\inf\le-\nu^{-}\left(E\right)$, 即 $-\inf\ge\nu^{-}\left(E\right)$. 合并得 $\nu^{-}\left(E\right)=-\inf\left\{\nu\left(F\right):F\subset{E}\right\}$.

(b). 先证 $\le$: 对任意两两不交且并等于 $E$ 的 $\left\{E_{i}\right\}$, 由 $\nu=\nu^{+}-\nu^{-}$ 与三角不等式,

$$
\sum_{i}\left|\nu\left(E_{i}\right)\right|=\sum_{i}\left|\nu^{+}\left(E_{i}\right)-\nu^{-}\left(E_{i}\right)\right|\le\sum_{i}\left[\nu^{+}\left(E_{i}\right)+\nu^{-}\left(E_{i}\right)\right]=\nu^{+}\left(E\right)+\nu^{-}\left(E\right)=\left|\nu\right|\left(E\right),
$$

故 $\sup\le\left|\nu\right|\left(E\right)$.

再证 $\ge$: 取哈恩分解 $X=P\cup{N}$ (**定理 11.3.2 (哈恩分解定理)**), 令 $E_{1}=E\cap{P}$, $E_{2}=E\cap{N}$, 则 $E_{1},E_{2}$ 两两不交且 $E_{1}\cup{E}_{2}=E$. 于是 $\left|\nu\left(E_{1}\right)\right|+\left|\nu\left(E_{2}\right)\right|=\nu^{+}\left(E\cap{P}\right)+\nu^{-}\left(E\cap{N}\right)=\nu^{+}\left(E\right)+\nu^{-}\left(E\right)=\left|\nu\right|\left(E\right)$, 故 $\sup\ge\left|\nu\right|\left(E\right)$. 合并得等式.

$\blacksquare$

## 5

设 $\left\{\nu_{j}\right\}$ 是一列正测度. 若 $\nu_{j}\perp\mu$ 对一切 $j$, 则 $\sum_{j}\nu_{j}\perp\mu$; 若 $\nu_{j}\ll\mu$ 对一切 $j$, 则 $\sum_{j}\nu_{j}\ll\mu$.

### 解答 5

(奇异情形). 因 $\nu_{j}\perp\mu$ (**定义 11.4.1 (相互奇异的符号测度)**), 对每个 $j$ 存在 $E_{j}\in\mathcal{M}$ 使 $E_{j}$ 是 $\mu$-零集且 $E_{j}^{c}$ 是 $\nu_{j}$-零集, 即 $\mu\left(E_{j}\right)=0$, $\nu_{j}\left(E_{j}^{c}\right)=0$. 令 $E=\bigcup_{j=1}^{\infty}E_{j}$. 由 $\mu$ 的次可数可加性, $\mu\left(E\right)\le\sum_{j=1}^{\infty}\mu\left(E_{j}\right)=0$, 故 $E$ 是 $\mu$-零集. 又 $E^{c}=\bigcap_{j=1}^{\infty}E_{j}^{c}\subset{E}_{k}^{c}$ 对一切 $k$, 由 $\nu_{k}$ 的单调性 $\nu_{k}\left(E^{c}\right)\le\nu_{k}\left(E_{k}^{c}\right)=0$, 故 $\nu_{k}\left(E^{c}\right)=0$ 对一切 $k$, 从而 $\left(\sum_{j}\nu_{j}\right)\left(E^{c}\right)=\sum_{j}\nu_{j}\left(E^{c}\right)=0$. 故 $\sum_{j}\nu_{j}\perp\mu$.

(绝对连续情形). 设 $\nu_{j}\ll\mu$ 对一切 $j$ (**定义 11.5.1 (绝对连续性)**). 若 $\mu\left(E\right)=0$, 则 $\nu_{j}\left(E\right)=0$ 对一切 $j$, 故 $\left(\sum_{j}\nu_{j}\right)\left(E\right)=\sum_{j}\nu_{j}\left(E\right)=0$. 因此 $\sum_{j}\nu_{j}\ll\mu$.

$\blacksquare$

## 6

设 $\mu$ 是正测度. 一族函数 $\left\{f_{\alpha}\right\}_{\alpha\in{A}}\subset{L}^{1}\left(\mu\right)$ 称为一致可积的, 若对任意 $\varepsilon>0$ 存在 $\delta>0$ 使得 $\left|\int_{E}f_{\alpha}\,\mathrm{d}\mu\right|<\varepsilon$ 对所有 $\alpha\in{A}$ 成立, 只要 $\mu\left(E\right)<\delta$.

(a) $L^{1}\left(\mu\right)$ 的任意有限子集是一致可积的;

(b) 若 $\left\{f_{n}\right\}$ 是 $L^{1}\left(\mu\right)$ 中的序列且在 $L^{1}$ 度量下收敛于 $f\in{L}^{1}\left(\mu\right)$, 则 $\left\{f_{n}\right\}$ 是一致可积的.

### 解答 6

(a). 设 $\left\{f_{1},\dots,f_{n}\right\}\subset{L}^{1}\left(\mu\right)$. 对每个 $j$, 由**注 11.5.3 (积分关于测度的绝对连续)** ($f_{j}\in{L}^{1}\left(\mu\right)$, $\lim_{\mu\left(E\right)\to0}\int_{E}f_{j}\,\mathrm{d}\mu=0$), 存在 $\delta_{j}>0$ 使 $\mu\left(E\right)<\delta_{j}\Rightarrow\left|\int_{E}f_{j}\,\mathrm{d}\mu\right|<\varepsilon$. 取 $\delta=\min_{1\le{j}\le{n}}\delta_{j}>0$, 则当 $\mu\left(E\right)<\delta$ 时, 对所有 $j$ 有 $\mu\left(E\right)<\delta_{j}$, 故 $\left|\int_{E}f_{j}\,\mathrm{d}\mu\right|<\varepsilon$. 故 $\left\{f_{1},\dots,f_{n}\right\}$ 一致可积.

(b). 因 $\int\left|f_{n}-f\right|\mathrm{d}\mu\to0$, 存在 $N$ 使当 $n\ge{N}$ 时 $\int\left|f_{n}-f\right|\mathrm{d}\mu<\frac{\varepsilon}{2}$. 由 (a), 单元素集 $\left\{f\right\}$ 一致可积: 存在 $\delta_{1}>0$ 使 $\mu\left(E\right)<\delta_{1}\Rightarrow\left|\int_{E}f\,\mathrm{d}\mu\right|<\frac{\varepsilon}{2}$. 又有限集 $\left\{f_{1},\dots,f_{N-1}\right\}$ 由 (a) 一致可积: 存在 $\delta_{2}>0$ 使 $\mu\left(E\right)<\delta_{2}\Rightarrow\left|\int_{E}f_{n}\,\mathrm{d}\mu\right|<\varepsilon$ 对 $n<{}N$ 成立. 取 $\delta=\min\left\{\delta_{1},\delta_{2}\right\}$. 当 $\mu\left(E\right)<\delta$ 时, 对 $n\ge{N}$,

$$
\left|\int_{E}f_{n}\,\mathrm{d}\mu\right|\le\left|\int_{E}f\,\mathrm{d}\mu\right|+\int_{E}\left|f_{n}-f\right|\mathrm{d}\mu\le\frac{\varepsilon}{2}+\int\left|f_{n}-f\right|\mathrm{d}\mu<\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon,
$$

而对 $n<{}N$ 亦有 $\left|\int_{E}f_{n}\,\mathrm{d}\mu\right|<\varepsilon$. 故 $\left\{f_{n}\right\}$ 一致可积.

$\blacksquare$

## 1

对 $j=1,2$, 设 $\mu_{j},\nu_{j}$ 是 $\left(X_{j},\mathcal{M}_{j}\right)$ 上的 $\sigma$-有限测度且 $\nu_{j}\ll\mu_{j}$. 则 $\nu_{1}\times\nu_{2}\ll\mu_{1}\times\mu_{2}$, 且

$$
\frac{\mathrm{d}\left(\nu_{1}\times\nu_{2}\right)}{\mathrm{d}\left(\mu_{1}\times\mu_{2}\right)}\left(x_{1},x_{2}\right)=\frac{\mathrm{d}\nu_{1}}{\mathrm{d}\mu_{1}}\left(x_{1}\right)\cdot\frac{\mathrm{d}\nu_{2}}{\mathrm{d}\mu_{2}}\left(x_{2}\right).
$$

### 解答 1

因 $\nu_{j}\ll\mu_{j}$ 且 $\mu_{j}$ 是 $\sigma$-有限正测度, 由**定理 11.5.5 (拉东-尼科迪姆定理)**, 存在 $\mathcal{M}_{j}$-可测函数 $f_{j}=\frac{\mathrm{d}\nu_{j}}{\mathrm{d}\mu_{j}}\ge0$ 使得 $\nu_{j}\left(E\right)=\int_{E}f_{j}\,\mathrm{d}\mu_{j}$ 对一切 $E\in\mathcal{M}_{j}$ 成立. 定义 $F:\left(X_{1}\times{X}_{2}\right)\to\left[0,\infty\right]$, $F\left(x_{1},x_{2}\right)=f_{1}\left(x_{1}\right)f_{2}\left(x_{2}\right)$, 则 $F$ 是 $\mathcal{M}_{1}\otimes\mathcal{M}_{2}$-可测的. 对可测矩形 $A\times{B}\in\mathcal{M}_{1}\otimes\mathcal{M}_{2}$, 由**定理 10.2.2 (托内利定理)**,

$$
\int_{A\times{B}}F\,\mathrm{d}\left(\mu_{1}\times\mu_{2}\right)=\left(\int_{A}f_{1}\,\mathrm{d}\mu_{1}\right)\left(\int_{B}f_{2}\,\mathrm{d}\mu_{2}\right)=\nu_{1}\left(A\right)\nu_{2}\left(B\right)=\left(\nu_{1}\times\nu_{2}\right)\left(A\times{B}\right).
$$

由乘积测度的唯一性 (矩形容许族上相等), 对一切 $E\in\mathcal{M}_{1}\otimes\mathcal{M}_{2}$ 有 $\left(\nu_{1}\times\nu_{2}\right)\left(E\right)=\int_{E}F\,\mathrm{d}\left(\mu_{1}\times\mu_{2}\right)$. 这蕴含 $\nu_{1}\times\nu_{2}\ll\mu_{1}\times\mu_{2}$ (**定义 11.5.1 (绝对连续性)**: 若 $\left(\mu_{1}\times\mu_{2}\right)\left(E\right)=0$, 则上式右端为 $0$). 又 $\nu_{1}\times\nu_{2}$ 是 $\sigma$-有限的 (因 $\nu_{j}$ $\sigma$-有限), 由**定理 11.5.5 (拉东-尼科迪姆定理)** 的唯一性, $F$ 就是 $\nu_{1}\times\nu_{2}$ 关于 $\mu_{1}\times\mu_{2}$ 的拉东-尼科迪姆导数, 即

$$
\frac{\mathrm{d}\left(\nu_{1}\times\nu_{2}\right)}{\mathrm{d}\left(\mu_{1}\times\mu_{2}\right)}\left(x_{1},x_{2}\right)=\frac{\mathrm{d}\nu_{1}}{\mathrm{d}\mu_{1}}\left(x_{1}\right)\cdot\frac{\mathrm{d}\nu_{2}}{\mathrm{d}\mu_{2}}\left(x_{2}\right).
$$

$\blacksquare$

## 2

设 $\mu,\nu$ 是 $\left(X,\mathcal{M}\right)$ 上的测度且 $\nu\ll\mu$, 令 $\lambda=\mu+\nu$. 若 $f=\frac{\mathrm{d}\nu}{\mathrm{d}\lambda}$, 则 $0\le{f}<1$ $\mu$-几乎处处, 且 $\frac{\mathrm{d}\nu}{\mathrm{d}\mu}=\frac{f}{1-f}$.

### 解答 2

因 $\lambda=\mu+\nu\ge\mu$ 且 $\nu\ll\mu$, 有 $\nu\ll\lambda$ (若 $\lambda\left(E\right)=0$, 则 $\mu\left(E\right)=0$, 从而 $\nu\left(E\right)=0$), 故 $f=\frac{\mathrm{d}\nu}{\mathrm{d}\lambda}$ 存在且 $f\ge0$ $\lambda$-几乎处处 (**定理 11.5.5 (拉东-尼科迪姆定理)**).

先证 $f<1$ $\mu$-几乎处处. 反设 $\mu\left(\left\{f\ge1\right\}\right)>0$. 因 $\nu\left(\left\{f\ge1\right\}\right)=\int_{\left\{f\ge1\right\}}f\,\mathrm{d}\lambda\ge\lambda\left(\left\{f\ge1\right\}\right)$, 而 $\lambda=\mu+\nu$, 故 $\nu\left(\left\{f\ge1\right\}\right)\ge\lambda\left(\left\{f\ge1\right\}\right)=\mu\left(\left\{f\ge1\right\}\right)+\nu\left(\left\{f\ge1\right\}\right)$, 推出 $\mu\left(\left\{f\ge1\right\}\right)\le0$, 矛盾. 故 $0\le{f}<1$ $\mu$-几乎处处.

最后证 $\frac{\mathrm{d}\nu}{\mathrm{d}\mu}=\frac{f}{1-f}$. 对任意 $E\in\mathcal{M}$, 由 $\lambda=\mu+\nu$ 与 $f=\frac{\mathrm{d}\nu}{\mathrm{d}\lambda}$,

$$
\nu\left(E\right)=\int_{E}f\,\mathrm{d}\lambda=\int_{E}f\,\mathrm{d}\mu+\int_{E}f\,\mathrm{d}\nu,
$$

即 $\int_{E}\left(1-f\right)\mathrm{d}\nu=\int_{E}f\,\mathrm{d}\mu$. 因 $1-f>0$ $\mu$-几乎处处 (也 $\lambda$-几乎处处), 由**定理 11.5.5 (拉东-尼科迪姆定理)** 的唯一性, $\frac{\mathrm{d}\nu}{\mathrm{d}\mu}=\frac{f}{1-f}$.

$\blacksquare$
