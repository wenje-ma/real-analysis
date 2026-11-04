# week5

> **定义 5.1.2 (测度)**
> 
> 设 $\left(X,\mathcal F\right)$ 是一个可测空间. 函数 $\mu:\mathcal F\to\left[0,+\infty\right]$ 称为 $\left(X,\mathcal F\right)$ 上的一个测度, 如果满足: (1) 非负性: $\mu\left(E\right)\ge0$ 对一切 $E\in\mathcal F$ 成立; (2) 零空集性: $\mu\left(\emptyset\right)=0$; (3) 可数可加性 ($\sigma$-可加性): 对任意可数个两两不交的集合 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$, 有 $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **定义 5.1.5 ($\sigma$-有限测度)**
> 
> 设 $\left(X,\mathcal F,\mu\right)$ 是测度空间. 如果存在一列可测集 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$ 使得 $X=\bigcup_{n=1}^{\infty}E_{n}$ 且 $\mu\left(E_{n}\right)< +\infty$ 对所有 $n\in\mathbb N$ 成立, 则称 $\mu$ 为 $\sigma$-有限测度.

> **定义 8.1.1 (非负简单函数的积分)**
> 
> 设 $f=\sum_{i=1}^{n}c_{i}\chi_{A_{i}}$ 是非负简单函数, 其中 $c_{i}\ge0$, $A_{i}\in\mathcal F$ 互不相交且 $\bigcup_{i}A_{i}=X$. 定义 $f$ 关于 $\mu$ 的积分为 $\int_{X}f\,\mathrm{d}\mu=\sum_{i=1}^{n}c_{i}\mu\left(A_{i}\right)$, 并约定 $0\cdot\infty=0$.

> **命题 8.1.2 (简单函数积分的线性性)**
> 
> 设 $f,g$ 为非负简单函数, $\alpha,\beta\ge0$, 则 $\int_{X}\left(\alpha f+\beta g\right)\mathrm{d}\mu=\alpha\int_{X}f\,\mathrm{d}\mu+\beta\int_{X}g\,\mathrm{d}\mu$.

> **定义 8.2.1 (非负可测函数的积分)**
> 
> 设 $f:X\to\left[0,+\infty\right]$ 是非负可测函数. 定义 $f$ 关于 $\mu$ 的积分为 $\int_{X}f\,\mathrm{d}\mu=\sup\left\{\int_{X}\phi\,\mathrm{d}\mu:\phi\text{ 是简单函数},0\le\phi\le f\right\}$. 若 $\int_{X}f\,\mathrm{d}\mu< \infty$, 则称 $f$ 是可积的.

> **定理 8.2.2 (单调收敛定理)**
> 
> 设 $\left(X,\mathcal F,\mu\right)$ 是测度空间, $\left\{f_{n}\right\}$ 是一列非负可测函数, 满足 $0\le f_{1}\left(x\right)\le f_{2}\left(x\right)\le\cdots$ 对所有 $x\in X$ 成立, 且 $f_{n}\to f$ 点点收敛. 则 $\lim_{n\to\infty}\int_{X}f_{n}\,\mathrm{d}\mu=\int_{X}f\,\mathrm{d}\mu$.

> **注 8.2.3 (简单函数逼近)**
> 
> 单调收敛定理告诉我们积分可以用简单函数逼近.

> **命题 8.2.4 (积分关于集合的绝对连续性)**
> 
> 设 $f$ 为非负可测函数, 则 $A\mapsto\int_{A}f\,\mathrm{d}\mu$ 为一个测度; 若 $\mu\left(A\right)=0$, 则 $\int_{A}f\,\mathrm{d}\mu=0$.

> **定义 8.2.5 (一般可测函数的积分)**
> 
> 设 $f:X\to\left[-\infty,+\infty\right]$ 是可测函数. 定义 $f$ 的正部和负部分别为 $f^{+}\left(x\right)=\max\left\{f\left(x\right),0\right\}$, $f^{-}\left(x\right)=\max\left\{-f\left(x\right),0\right\}$. 若至少有一个积分 $\int_{X}f^{+}\mathrm{d}\mu$, $\int_{X}f^{-}\mathrm{d}\mu$ 有限, 则定义 $f$ 的积分为 $\int_{X}f\,\mathrm{d}\mu=\int_{X}f^{+}\mathrm{d}\mu-\int_{X}f^{-}\mathrm{d}\mu$. 若 $\int_{X}f^{+}\mathrm{d}\mu< \infty$ 且 $\int_{X}f^{-}\mathrm{d}\mu< \infty$, 则称 $f$ 是可积的.

> **定理 8.2.7 (法图引理)**
> 
> 设 $\left(X,\mathcal F,\mu\right)$ 是测度空间, $\left\{f_{n}\right\}$ 是一列非负可测函数, 则 $\int_{X}\liminf_{n\to\infty}f_{n}\,\mathrm{d}\mu\le\liminf_{n\to\infty}\int_{X}f_{n}\,\mathrm{d}\mu$.

> **定理 8.2.9 (控制收敛定理)**
> 
> 设 $\left(X,\mathcal F,\mu\right)$ 是测度空间, $\left\{f_{n}\right\}$ 是一列可测函数, 若存在可积函数 $g$ 使 $\left|f_{n}\right|\le g$ 对所有 $n$ 成立, 且 $f_{n}\to f$ 几乎处处, 则 $f$ 可积且 $\int f\,\mathrm{d}\mu=\lim_{n\to\infty}\int f_{n}\,\mathrm{d}\mu$.

> **引理 8.2.13 (级数逐项积分)**
> 
> 设 $\left\{f_{n}\right\}$ 是一列可测函数, 且 $\sum_{n=1}^{\infty}\int_{X}\left|f_{n}\right|\mathrm{d}\mu< \infty$, 则 $\int_{X}\left(\sum_{n=1}^{\infty}f_{n}\right)\mathrm{d}\mu=\sum_{n=1}^{\infty}\int_{X}f_{n}\,\mathrm{d}\mu$.

> **定理 8.2.17 (参数积分)**
> 
> 设 $f:X\times\left[a,b\right]\to\mathbb R$, 且对每个 $t\in\left[a,b\right]$, 函数 $f\left(\cdot,t\right):X\to\mathbb R$ 可积. 令 $F\left(t\right)=\int_{X}f\left(x,t\right)\mathrm{d}\mu\left(x\right)$. (a) 若存在 $g\in L^{1}\left(\mu\right)$ 使得对所有 $x,t$ 有 $\left|f\left(x,t\right)\right|\le g\left(x\right)$, 且对每个 $x$ 有 $\lim_{t\to t_{0}}f\left(x,t\right)=f\left(x,t_{0}\right)$, 则 $\lim_{t\to t_{0}}F\left(t\right)=F\left(t_{0}\right)$; (b) 若偏导数 $\partial f/\partial t$ 存在, 且存在 $g\in L^{1}\left(\mu\right)$ 使得对所有 $x,t$ 有 $\left|\frac{\partial f}{\partial t}\left(x,t\right)\right|\le g\left(x\right)$, 则 $F$ 可微, 且 $F'\left(t\right)=\int\frac{\partial f}{\partial t}\left(x,t\right)\mathrm{d}\mu\left(x\right)$.

## 1

设 $f$ 为非负简单函数, 证明: $A\mapsto\int_{A}f\,\mathrm{d}\mu$ 是一个测度; 若 $\mu\left(A\right)=0$, 则 $\int_{A}f\,\mathrm{d}\mu=0$.

### 解答 1

设 $f=\sum_{i=1}^{n}c_{i}\chi_{A_{i}}$, 其中 $c_{i}\ge0$, $A_{i}\in\mathcal F$ 两两不交且 $\bigcup_{i}A_{i}=X$. 对 $E\in\mathcal F$, 由**定义 8.1.1 (非负简单函数的积分)**,

$$
\int_{E}f\,\mathrm{d}\mu=\int f\chi_{E}\,\mathrm{d}\mu=\sum_{i=1}^{n}c_{i}\mu\left(E\cap A_{i}\right).
$$

记 $\lambda\left(E\right):=\int_{E}f\,\mathrm{d}\mu$. 验证 $\lambda$ 是测度: $\lambda\left(\emptyset\right)=\sum_{i=1}^{n}c_{i}\mu\left(\emptyset\cap A_{i}\right)=0$; 非负性显然, 因 $c_{i}\ge0$ 且 $\mu\ge0$; $\sigma$-可加性: 设 $E=\bigsqcup_{j=1}^{\infty}E_{j}$ (两两不交). 由 $\mu$ 的 $\sigma$-可加性 (**定义 5.1.2 (测度)**) 与**命题 8.1.2 (简单函数积分的线性性)**,

$$
\lambda\left(E\right)=\sum_{i=1}^{n}c_{i}\mu\left(E\cap A_{i}\right)=\sum_{i=1}^{n}c_{i}\sum_{j=1}^{\infty}\mu\left(E_{j}\cap A_{i}\right)=\sum_{j=1}^{\infty}\sum_{i=1}^{n}c_{i}\mu\left(E_{j}\cap A_{i}\right)=\sum_{j=1}^{\infty}\lambda\left(E_{j}\right).
$$

故 $\lambda$ 是 $\mathcal F$ 上的测度. 最后, 若 $\mu\left(A\right)=0$, 则

$$
\lambda\left(A\right)=\sum_{i=1}^{n}c_{i}\mu\left(A\cap A_{i}\right)\le\sum_{i=1}^{n}c_{i}\mu\left(A\right)=0,
$$

故 $\lambda\left(A\right)=0$. $\blacksquare$

## 2

设 $f,g$ 是可积函数, $a,b\in\mathbb R$, 证明:

1. 线性性: $\int_{X}\left(af+bg\right)\mathrm{d}\mu=a\int_{X}f\,\mathrm{d}\mu+b\int_{X}g\,\mathrm{d}\mu$;

2. 单调性: 若 $f\le g$ 几乎处处, 则 $\int_{X}f\,\mathrm{d}\mu\le\int_{X}g\,\mathrm{d}\mu$;

3. 三角不等式: $\left|\int_{X}f\,\mathrm{d}\mu\right|\le\int_{X}\left|f\right|\mathrm{d}\mu$;

4. 若 $f=g$ 几乎处处, 则 $\int_{X}f\,\mathrm{d}\mu=\int_{X}g\,\mathrm{d}\mu$.

### 解答 2

先建立非负可测函数积分的线性性. 设 $\phi,\psi$ 为非负可测函数, $\alpha,\beta\ge0$. 由**注 8.2.3 (简单函数逼近)**, 存在简单函数 $\phi_{k}\uparrow\phi$, $\psi_{k}\uparrow\psi$. 由**命题 8.1.2 (简单函数积分的线性性)**,

$$
\int\left(\alpha\phi_{k}+\beta\psi_{k}\right)\mathrm{d}\mu=\alpha\int\phi_{k}\,\mathrm{d}\mu+\beta\int\psi_{k}\,\mathrm{d}\mu.
$$

因 $\alpha\phi_{k}+\beta\psi_{k}\uparrow\alpha\phi+\beta\psi$, 由**定理 8.2.2 (单调收敛定理)** 两边取极限得

$$
\int\left(\alpha\phi+\beta\psi\right)\mathrm{d}\mu=\alpha\int\phi\,\mathrm{d}\mu+\beta\int\psi\,\mathrm{d}\mu.
$$

再设 $f,g$ 可积, 记 $f^{+},f^{-}$ 为其正负部 (**定义 8.2.5 (一般可测函数的积分)**).

1. 先对纯量乘: 若 $a\ge0$, 则 $\left(af\right)^{+}=af^{+}$, $\left(af\right)^{-}=af^{-}$, 故 $\int\left(af\right)\mathrm{d}\mu=a\int f^{+}\mathrm{d}\mu-a\int f^{-}\mathrm{d}\mu=a\int f\,\mathrm{d}\mu$; 若 $a< 0$, 则 $\left(af\right)^{+}=\left|a\right|f^{-}$, $\left(af\right)^{-}=\left|a\right|f^{+}$, 同样得 $\int\left(af\right)\mathrm{d}\mu=a\int f\,\mathrm{d}\mu$; $a=0$ 平凡. 对加法, 由正负部分解 $f+g=\left(f^{+}+g^{+}\right)-\left(f^{-}+g^{-}\right)$, 即

$$
\left(f+g\right)^{+}+f^{-}+g^{-}=\left(f+g\right)^{-}+f^{+}+g^{+},
$$

两边均为非负可测函数, 由非负线性性积分得

$$
\int\left(f+g\right)^{+}\mathrm{d}\mu+\int f^{-}\mathrm{d}\mu+\int g^{-}\mathrm{d}\mu=\int\left(f+g\right)^{-}\mathrm{d}\mu+\int f^{+}\mathrm{d}\mu+\int g^{+}\mathrm{d}\mu,
$$

移项 (各项有限, 因 $f,g$ 可积) 得 $\int\left(f+g\right)\mathrm{d}\mu=\int f\,\mathrm{d}\mu+\int g\,\mathrm{d}\mu$. 结合两者得 $\int\left(af+bg\right)\mathrm{d}\mu=a\int f\,\mathrm{d}\mu+b\int g\,\mathrm{d}\mu$.

2. 由线性性, $\int g\,\mathrm{d}\mu-\int f\,\mathrm{d}\mu=\int\left(g-f\right)\mathrm{d}\mu$. 因 $f\le g$ 几乎处处, $g-f\ge0$ 几乎处处. 由**定义 8.2.1 (非负可测函数的积分)**, 非负可测函数的积分为非负 (它是非负简单函数积分的上确界), 故 $\int\left(g-f\right)\mathrm{d}\mu\ge0$, 即 $\int f\,\mathrm{d}\mu\le\int g\,\mathrm{d}\mu$.

3. $\left|f\right|=f^{+}+f^{-}$, 由非负线性性 $\int\left|f\right|\mathrm{d}\mu=\int f^{+}\mathrm{d}\mu+\int f^{-}\mathrm{d}\mu$. 再由 $\int f\,\mathrm{d}\mu=\int f^{+}\mathrm{d}\mu-\int f^{-}\mathrm{d}\mu$, 有

$$
\left|\int f\,\mathrm{d}\mu\right|=\left|\int f^{+}\mathrm{d}\mu-\int f^{-}\mathrm{d}\mu\right|\le\int f^{+}\mathrm{d}\mu+\int f^{-}\mathrm{d}\mu=\int\left|f\right|\mathrm{d}\mu.
$$

4. $f=g$ 几乎处处, 则 $f^{+}=g^{+}$, $f^{-}=g^{-}$ 几乎处处. 于是 $h:=f^{+}-g^{+}$ 可积且 $h=0$ 几乎处处, 其正部 $h^{+}$ 与负部 $h^{-}$ 均在零测集外为零. 由**命题 8.2.4 (积分关于集合的绝对连续性)**, $\int h^{+}\mathrm{d}\mu=\int_{\left\{h> 0\right\}}h^{+}\mathrm{d}\mu=0$, $\int h^{-}\mathrm{d}\mu=0$, 故 $\int h\,\mathrm{d}\mu=0$, 即 $\int f^{+}\mathrm{d}\mu=\int g^{+}\mathrm{d}\mu$; 同理 $\int f^{-}\mathrm{d}\mu=\int g^{-}\mathrm{d}\mu$. 因此 $\int f\,\mathrm{d}\mu=\int g\,\mathrm{d}\mu$. $\blacksquare$

## 3

设 $f\in L^{1}$, 证明:

(a) 集合 $\left\{x:f\left(x\right)\ne0\right\}$ 是 $\sigma$-有限的;

(b) 对 $f,g\in L^{1}$, $\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\mu$ 对任意可测集 $E$ 成立, 当且仅当 $\int\left|f-g\right|\mathrm{d}\mu=0$, 当且仅当 $f=g$ 关于 $\mu$ 几乎处处.

### 解答 3

(a) 由**定义 8.2.5 (一般可测函数的积分)**, $f=f^{+}-f^{-}$, 故 $\left\{x:f\left(x\right)\ne0\right\}=\left\{x:f^{+}\left(x\right)> 0\right\}\cup\left\{x:f^{-}\left(x\right)> 0\right\}$. 而

$$
\left\{x:f^{+}\left(x\right)> 0\right\}=\bigcup_{n=1}^{\infty}\left\{x:f^{+}\left(x\right)> \frac{1}{n}\right\},
$$

且由**定义 8.2.1 (非负可测函数的积分)**,

$$
\int_{X}f^{+}\mathrm{d}\mu\ge\int_{\left\{f^{+}> \frac{1}{n}\right\}}f^{+}\mathrm{d}\mu\ge\frac{1}{n}\mu\left(\left\{x:f^{+}\left(x\right)> \frac{1}{n}\right\}\right).
$$

因 $f$ 可积, $\int f^{+}\mathrm{d}\mu< \infty$, 故 $\mu\left(\left\{x:f^{+}\left(x\right)> \frac{1}{n}\right\}\right)\le n\int f^{+}\mathrm{d}\mu< \infty$. 于是 $\left\{f^{+}> 0\right\}$ 是可数个有限测度集之并; 同理 $\left\{f^{-}> 0\right\}$ 亦然. 从而 $\left\{x:f\left(x\right)\ne0\right\}$ 也是可数个有限测度集之并, 在**定义 5.1.5 ($\sigma$-有限测度)** 的意义下是 $\sigma$-有限的. $\blacksquare$

(b) 记 $h:=\left|f-g\right|\in L^{1}$, $h\ge0$.

(1) $\int\left|f-g\right|\mathrm{d}\mu=0\Rightarrow f=g$ 几乎处处: 由非负可积函数积分为零则几乎处处为零, $h=0$ 几乎处处, 即 $f=g$ 几乎处处.

(2) $f=g$ 几乎处处 $\Rightarrow\int\left|f-g\right|\mathrm{d}\mu=0$: 因 $h=0$ 在 $\left\{f\ne g\right\}$ 之外成立, 而 $\left\{f\ne g\right\}$ 是零测集. 由**命题 8.2.4 (积分关于集合的绝对连续性)**, $\int_{\left\{f\ne g\right\}}h\,\mathrm{d}\mu=0$, 且 $\int_{\left\{f=g\right\}}h\,\mathrm{d}\mu=0$, 故 $\int h\,\mathrm{d}\mu=0$.

(3) $\int\left|f-g\right|\mathrm{d}\mu=0\Rightarrow\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\mu$ 对所有 $E$: 由习题二 1, 3,

$$
\left|\int_{E}f\,\mathrm{d}\mu-\int_{E}g\,\mathrm{d}\mu\right|=\left|\int_{E}\left(f-g\right)\mathrm{d}\mu\right|\le\int_{E}\left|f-g\right|\mathrm{d}\mu\le\int_{X}\left|f-g\right|\mathrm{d}\mu=0.
$$

(4) $\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\mu$ 对所有 $E$ $\Rightarrow\int\left|f-g\right|\mathrm{d}\mu=0$: 取 $E:=\left\{x:f\left(x\right)\ge g\left(x\right)\right\}\in\mathcal F$. 由习题二 1 线性性, $\int_{E}\left(f-g\right)\mathrm{d}\mu=\int_{E}f\,\mathrm{d}\mu-\int_{E}g\,\mathrm{d}\mu=0$; 在 $E$ 上 $f-g\ge0$, 故 $\int_{E}\left|f-g\right|\mathrm{d}\mu=\int_{E}\left(f-g\right)\mathrm{d}\mu=0$. 同理对 $E^{c}$, $\int_{E^{c}}\left(g-f\right)\mathrm{d}\mu=0$, 在 $E^{c}$ 上 $g-f\ge0$, 故 $\int_{E^{c}}\left|f-g\right|\mathrm{d}\mu=0$. 于是 $\int\left|f-g\right|\mathrm{d}\mu=0$.

综合 (1)(2)(3)(4) 得三条件等价. $\blacksquare$

## 4

证明:

**14.** 若 $f\in L^{+}$, 令 $\lambda\left(E\right)=\int_{E}f\,\mathrm{d}\mu$ (对 $E\in\mathcal M$). 则 $\lambda$ 是 $\mathcal M$ 上的测度, 且对任意 $g\in L^{+}$, $\int g\,\mathrm{d}\lambda=\int fg\,\mathrm{d}\mu$.

**16.** 若 $f\in L^{+}$ 且 $\int f< \infty$, 对每个 $\varepsilon> 0$ 存在 $E\in\mathcal M$ 使得 $\mu\left(E\right)< \infty$ 且 $\int_{E}f> \left(\int f\right)-\varepsilon$.

### 解答 4

**14.** 先证 $\lambda$ 是测度. 由**定义 8.1.1 (非负简单函数的积分)** 与**定义 8.2.1 (非负可测函数的积分)**, $\lambda\left(\emptyset\right)=0$ 且非负. 对两两不交的可测集 $\left\{E_{n}\right\}$, 因 $f\chi_{\bigsqcup E_{n}}=\sum_{n}f\chi_{E_{n}}$ 且部分和 $\sum_{n=1}^{N}f\chi_{E_{n}}\uparrow f\chi_{\bigsqcup E_{n}}$ 点点, 由**定理 8.2.2 (单调收敛定理)**,

$$
\lambda\left(\bigsqcup_{n=1}^{\infty}E_{n}\right)=\int f\chi_{\bigsqcup E_{n}}\mathrm{d}\mu=\sum_{n=1}^{\infty}\int f\chi_{E_{n}}\mathrm{d}\mu=\sum_{n=1}^{\infty}\lambda\left(E_{n}\right).
$$

故 $\lambda$ 是 $\mathcal M$ 上的测度.

再证换元公式. 若 $g=\sum_{j=1}^{m}a_{j}\chi_{E_{j}}$ 是简单函数 (设 $E_{j}$ 两两不交), 由**定义 8.1.1 (非负简单函数的积分)** 与有限线性性,

$$
\int g\,\mathrm{d}\lambda=\sum_{j=1}^{m}a_{j}\lambda\left(E_{j}\right)=\sum_{j=1}^{m}a_{j}\int_{E_{j}}f\,\mathrm{d}\mu=\int\left(\sum_{j=1}^{m}a_{j}\chi_{E_{j}}f\right)\mathrm{d}\mu=\int fg\,\mathrm{d}\mu.
$$

对一般 $g\in L^{+}$, 由**注 8.2.3 (简单函数逼近)** 取简单函数 $g_{k}\uparrow g$. 因 $f\ge0$, $fg_{k}\uparrow fg$. 由**定理 8.2.2 (单调收敛定理)** (分别在测度 $\lambda$ 与 $\mu$ 下), $\int g_{k}\,\mathrm{d}\lambda\uparrow\int g\,\mathrm{d}\lambda$ 且 $\int fg_{k}\,\mathrm{d}\mu\uparrow\int fg\,\mathrm{d}\mu$. 对每个 $k$ 两式相等 (简单情形), 故极限相等: $\int g\,\mathrm{d}\lambda=\int fg\,\mathrm{d}\mu$. $\blacksquare$

**16.** 对 $n\in\mathbb N$, 令 $E_{n}:=\left\{x:f\left(x\right)> \frac{1}{n}\right\}\in\mathcal M$. 则 $\left\{E_{n}\right\}$ 单调上升且 $\bigcup_{n}E_{n}=\left\{x:f\left(x\right)> 0\right\}$. 由**定义 8.2.1 (非负可测函数的积分)**,

$$
\int f\,\mathrm{d}\mu\ge\int_{E_{n}}f\,\mathrm{d}\mu\ge\frac{1}{n}\mu\left(E_{n}\right),
$$

故 $\mu\left(E_{n}\right)\le n\int f\,\mathrm{d}\mu< \infty$. 又由**定理 8.2.2 (单调收敛定理)**, $\int_{E_{n}}f\,\mathrm{d}\mu\uparrow\int_{\left\{f> 0\right\}}f\,\mathrm{d}\mu=\int f\,\mathrm{d}\mu$. 故对给定 $\varepsilon> 0$, 取 $n$ 充分大使 $\int_{E_{n}}f\,\mathrm{d}\mu> \int f\,\mathrm{d}\mu-\varepsilon$, 令 $E:=E_{n}$, 则 $\mu\left(E\right)< \infty$ 且 $\int_{E}f> \int f-\varepsilon$. $\blacksquare$
