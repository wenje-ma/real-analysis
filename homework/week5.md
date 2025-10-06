# week5

> **定义 4.1.3 ($\sigma$-代数)**
> 
> 设 $X$ 非空, $\mathcal{F}\subset\mathcal{P}\left(X\right)$. 称 $\mathcal{F}$ 为 $X$ 上的一个 $\sigma$-代数, 若满足: (1) $X\in\mathcal{F}$; (2) 对补运算封闭: $A\in\mathcal{F}\Rightarrow{A}^{c}\in\mathcal{F}$; (3) 对可数并封闭: $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal{F}$.

> **定义 4.3.2 (博雷尔 $\sigma$-代数)**
> 
> 设 $\left(X,\tau\right)$ 是拓扑空间, 由所有开集生成的 $\sigma$-代数称为博雷尔 $\sigma$-代数, 记作 $\mathcal{B}\left(X\right)$, 其中元素称为博雷尔集.

> **定义 4.5.2 (乘积 $\sigma$-代数)**
> 
> 乘积 $\sigma$-代数 $\mathcal{F}\otimes\mathcal{G}$ 是包含所有可测矩形的最小 $\sigma$-代数: $\mathcal{F}\otimes\mathcal{G}:=\sigma\left(\left\{A\times{B}:A\in\mathcal{F},B\in\mathcal{G}\right\}\right)$.

> **定理 4.5.4 (博雷尔集的乘积)**
> 
> 对欧氏空间中的博雷尔 $\sigma$-代数, 有

> **定义 5.1.2 (测度)**
> 
> 设 $\left(X,\mathcal{F}\right)$ 是一个可测空间. 函数 $\mu:\mathcal{F}\to\left[0,+\infty\right]$ 称为 $\left(X,\mathcal{F}\right)$ 上的一个测度, 如果满足: (1) 非负性: $\mu\left(E\right)\ge0$ 对一切 $E\in\mathcal{F}$ 成立; (2) 零空集性: $\mu\left(\emptyset\right)=0$; (3) 可数可加性 ($\sigma$-可加性): 对任意可数个两两不交的集合 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$, 有 $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **定义 6.1.1 (外测度)**
> 
> 设 $X$ 非空. 函数 $\mu^{*}:\mathcal{P}\left(X\right)\to\left[0,+\infty\right]$ 称为 $X$ 上的一个外测度, 若满足: (1) 非负性: $\mu^{*}\left(\emptyset\right)=0$, 且 $\mu^{*}\left(E\right)\ge0$ 对一切 $E\subset{X}$; (2) 单调性: $E\subset{F}\Rightarrow\mu^{*}\left(E\right)\le\mu^{*}\left(F\right)$; (3) 次可数可加性: $\mu^{*}\left(\bigcup_{n=1}^{\infty}E_{n}\right)\le\sum_{n=1}^{\infty}\mu^{*}\left(E_{n}\right)$.

> **定义 6.2.1 (准测度)**
> 
> 设 $X$ 是非空集合, $\mathcal{E}\subset\mathcal{P}\left(X\right)$ 是一个代数. 函数 $\mu_{0}:\mathcal{E}\to\left[0,+\infty\right]$ 称为一个准测度, 如果 $\mu_{0}\left(\emptyset\right)=0$, 且若 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{E}$ 两两不交且 $\bigcup_{n=1}^{\infty}E_{n}\in\mathcal{E}$, 则 $\mu_{0}\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu_{0}\left(E_{n}\right)$.

> **定理 6.2.2 (由**定义 6.2.1 (准测度)**生成外测度)**
> 
> 设 $\mathcal{E}\subset\mathcal{P}\left(X\right)$ 是一个覆盖类, $\mu_{0}:\mathcal{E}\to\left[0,+\infty\right]$ 是一个准测度. 对任意 $A\subset{X}$, 定义

> **定义 6.3.1 (卡拉西奥多里条件)**
> 
> 设 $\mu^{*}$ 是 $X$ 上的外测度. 子集 $A\subset{X}$ 称为 $\mu^{*}$-可测的, 若对任意 $T\subset{X}$ 有

> **定义 6.4.1 (h 区间)**
> 
> 令 $-\infty\le{a}<{}b<\infty$, 所有左开右闭区间 $\left(a,b\right]$, 以及 $\left(a,\infty\right)$, $\emptyset$ 称为 h 区间. h 区间的有限不交并形成的集族 $\mathcal{E}$ 为一个代数.

> **命题 6.4.2 ($\mathcal{E}$ 上的准测度)**
> 
> 设 $F:\mathbb{R}\to\mathbb{R}$ 为增的右连续函数. 对于不交区间 $\left(a_{i},b_{i}\right]$, $i=1,\dots,n$, 定义 $\mu_{0}\left(\bigcup_{i=1}^{n}\left(a_{i},b_{i}\right]\right):=\sum_{i=1}^{n}\left[F\left(b_{i}\right)-F\left(a_{i}\right)\right]$, 并令 $\mu_{0}\left(\emptyset\right)=0$. 则 $\mu_{0}$ 为 $\mathcal{E}$ 上的准测度.

> **定理 6.4.5 (勒贝格-斯蒂尔杰斯测度的正则性)**
> 
> 设 $\mu_{F}$ 是由增右连续函数 $F$ 生成的勒贝格-斯蒂尔杰斯测度, $\mathcal{M}^{*}$ 是 $\mu_{F}$-可测集的 $\sigma$-代数. 若 $E\in\mathcal{M}^{*}$, 则

> **定义 6.4.6 (勒贝格测度)**
> 
> 由 $F\left(x\right)=x$ 生成的测度称为勒贝格测度, 记作 $m$; 相应外测度定义的可测集称为勒贝格可测集, 全体记作 $\mathcal{L}$.

> **定义 6.5.1 (康托尔集的递归构造)**
> 
> 设 $C_{0}=\left[0,1\right]$. 对每个 $n\ge0$, 定义 $C_{n+1}=\frac{1}{3}C_{n}\cup\left(\frac{2}{3}+\frac{1}{3}C_{n}\right)$. 则康托尔集定义为 $C=\bigcap_{n=0}^{\infty}C_{n}$.

> **定理 6.5.2 (康托尔集的三进制刻画)**
> 
> 点 $x\in\left[0,1\right]$ 属于康托尔集 $C$ 当且仅当它的三进制展开 $x=\sum_{k=1}^{\infty}\frac{a_{k}}{3^{k}}$ 中不含数字 $1$ (即 $a_{k}\in\left\{0,2\right\}$).

> **定义 7.1.1 (可测映射)**
> 
> 设 $\left(X,\mathcal{F}\right)$, $\left(Y,\mathcal{G}\right)$ 为两个可测空间. 映射 $f:X\to{Y}$ 称为 $\left(\mathcal{F},\mathcal{G}\right)$-可测的, 若对任意 $B\in\mathcal{G}$ 有 $f^{-1}\left(B\right)\in\mathcal{F}$.

> **命题 7.1.7 (乘积空间的可测性)**
> 
> 设 $f=\left(f_{1},\dots,f_{n}\right):X\to{Y}_{1}\times\cdots\times{Y}_{n}$. 在乘积空间配备乘积 $\sigma$-代数下, $f$ 可测当且仅当每个坐标映射 $f_{i}:X\to{Y}_{i}$ 可测.

> **定理 7.1.8 (实值可测函数的运算封闭性)**
> 
> 设 $f,g:X\to\mathbb{R}$ 可测, $c\in\mathbb{R}$, 则 $cf$, $f+g$, $fg$, $\max\left(f,g\right)$, $\min\left(f,g\right)$ 可测; 若 $\left\{f_{n}\right\}$ 可测且点点收敛, 则极限函数可测.

> **定理 7.1.9 (可测函数与连续函数的复合)**
> 
> 设 $f:X\to\mathbb{R}$ 可测, $g:\mathbb{R}\to\mathbb{R}$ 连续, 则 $g\circ{f}:X\to\mathbb{R}$ 可测.

> **例 7.3.5 (示性函数)**
> 
> 设 $A\subset{X}$, 则 $\chi_{A}:X\to\mathbb{R}$ 可测当且仅当 $A\in\mathcal{F}$.

## 4

设 $\left(X,\mathcal{M}\right)$ 是可测空间, $\left\{f_{n}\right\}$ 是一列可测函数. 证明: 若 $\left\{f_{n}\right\}$ 是 $X$ 上的一列可测函数, 则 $\left\{x:\lim_{n\to\infty}f_{n}\left(x\right)\text{~存在}\right\}$ 是可测集.

### 解答 4

对 $m,n\in\mathbb{N}$, 由**定理 7.1.8 (实值可测函数的运算封闭性)** (1), 差 $f_{m}-f_{n}$ 可测. 由**定义 7.1.1 (可测映射)**, 开区间 $\left(-\frac{1}{k},\frac{1}{k}\right)$ 的原像可测:

$$
E_{k,m,n}:=\left\{x:\left|f_{m}\left(x\right)-f_{n}\left(x\right)\right|<\frac{1}{k}\right\}=\left(f_{m}-f_{n}\right)^{-1}\left(\left(-\frac{1}{k},\frac{1}{k}\right)\right)\in\mathcal{M}.
$$

由实数的完备性, $\lim_{n\to\infty}f_{n}\left(x\right)$ 存在当且仅当 $\left\{f_{n}\left(x\right)\right\}$ 是柯西列, 即对每个 $k\in\mathbb{N}$ 存在 $N$ 使对所有 $m,n\ge{N}$ 有 $\left|f_{m}\left(x\right)-f_{n}\left(x\right)\right|<\frac{1}{k}$. 故

$$
\left\{x:\lim_{n\to\infty}f_{n}\left(x\right)\text{~存在}\right\}=\bigcap_{k=1}^{\infty}\bigcup_{N=1}^{\infty}\bigcap_{m,n\ge{N}}E_{k,m,n}.
$$

由于 $\mathcal{M}$ 对可数交与可数并封闭 (**定义 4.1.3 ($\sigma$-代数)**), 且 $\bigcap_{m,n\ge{N}}E_{k,m.n}$ 是可数交, 故上述集合可测.

$\blacksquare$

## 5

证明: $X$ 上不可数个可测实值函数的上确界可以不是可测函数 (除非 $\sigma$-代数 $\mathcal{M}$ 十分特殊).

### 解答 5

取 $X=\mathbb{R}$ 配勒贝格 $\sigma$-代数 $\mathcal{L}$. 设 $A\subset\mathbb{R}$ 是勒贝格不可测集 (存在勒贝格不可测集 (维塔利集)). 对每个 $a\in{A}$, 定义 $f_{a}:=\chi_{\left\{a\right\}}$ 为单点指示函数. 因单点集 $\left\{a\right\}$ 是闭集, 从而是博雷尔集, 故 $f_{a}$ 可测. 但不可数族 $\left\{f_{a}:a\in{A}\right\}$ 的上确界满足

$$
\sup_{a\in{A}}f_{a}\left(x\right)=\begin{cases}1,&x\in{A},\\0,&x\notin{A},\end{cases}
$$

即 $\sup_{a\in{A}}f_{a}=\chi_{A}$. 由**例 7.3.5 (示性函数)**, $\chi_{A}$ 可测当且仅当 $A\in\mathcal{L}$, 与 $A$ 不可测矛盾. 故不可数个可测实值函数的上确界可以不是可测函数.

$\blacksquare$

## 6

设 $f$ 是 $\mathbb{R}\times\mathbb{R}^{k}$ 上的函数, 使得对每个 $x\in\mathbb{R}$, $f\left(x,\cdot\right)$ 是博雷尔可测的, 且对每个 $y\in\mathbb{R}^{k}$, $f\left(\cdot,y\right)$ 是连续的. 对 $n\in\mathbb{N}$, 令 $a_{i}=i/n$, 定义: 当 $a_{i}\le{x}\le{a}_{i+1}$ 时,

$$
f_{n}\left(x,y\right)=\frac{f\left(a_{i+1},y\right)\left(x-a_{i}\right)-f\left(a_{i},y\right)\left(x-a_{i+1}\right)}{a_{i+1}-a_{i}}.
$$

证明 $f_{n}$ 在 $\mathbb{R}\times\mathbb{R}^{k}$ 上博雷尔可测且 $f_{n}\to{f}$ 点点收敛, 从而 $f$ 在 $\mathbb{R}\times\mathbb{R}^{k}$ 上博雷尔可测. 并由此归纳证明: $\mathbb{R}^{n}$ 上每个逐变量连续的函数都是博雷尔可测的.

### 解答 6

固定 $n$, 记 $c_{i}:=a_{i+1}-a_{i}=\frac{1}{n}$, 并取半开区间 $\Delta_{i}:=\left[a_{i},a_{i+1}\right)$ ($i\in\mathbb{Z}$). 由于题设的插值公式在端点 $x=a_{i+1}$ 处两段均取 $f\left(a_{i+1},y\right)$, 故可用半开区间无歧义地表示. 在 $\Delta_{i}$ 上,

$$
f_{n}\left(x,y\right)=\frac{x-a_{i}}{c_{i}}f\left(a_{i+1},y\right)+\frac{a_{i+1}-x}{c_{i}}f\left(a_{i},y\right),
$$

从而

$$
f_{n}\left(x,y\right)=\sum_{i\in\mathbb{Z}}\left[\frac{x-a_{i}}{c_{i}}\chi_{\Delta_{i}}\left(x\right)f\left(a_{i+1},y\right)+\frac{a_{i+1}-x}{c_{i}}\chi_{\Delta_{i}}\left(x\right)f\left(a_{i},y\right)\right].
$$

先证 $f_{n}$ 可测. 对每个 $i$, 函数 $\left(x,y\right)\mapsto\frac{x-a_{i}}{c_{i}}\chi_{\Delta_{i}}\left(x\right)$ 与 $\left(x,y\right)\mapsto\frac{a_{i+1}-x}{c_{i}}\chi_{\Delta_{i}}\left(x\right)$ 只依赖于 $x$, 是连续函数与半开区间示性函数之积, 故为 $\mathbb{R}$ 上的博雷尔函数; 由题设, $f\left(a_{i},y\right)$ 与 $f\left(a_{i+1},y\right)$ 是 $\mathbb{R}^{k}$ 上的博雷尔函数. 由**定理 4.5.4 (博雷尔集的乘积)** 与**定义 4.5.2 (乘积 $\sigma$-代数)**, 乘积 $\sigma$-代数满足 $\mathcal{B}\left(\mathbb{R}\right)\otimes\mathcal{B}\left(\mathbb{R}^{k}\right)=\mathcal{B}\left(\mathbb{R}^{1+k}\right)$, 且由**命题 7.1.7 (乘积空间的可测性)**, 只依赖 $x$ 的博雷尔函数与只依赖 $y$ 的博雷尔函数之积, 作为 $\mathbb{R}\times\mathbb{R}^{k}$ 上的二元函数是可测的. 再由**定理 7.1.8 (实值可测函数的运算封闭性)** (1) (有限线性组合), $f_{n}$ 是 $\mathbb{R}\times\mathbb{R}^{k}$ 上的博雷尔函数.

再证 $f_{n}\to{f}$ 点点收敛. 固定 $\left(x,y\right)\in\mathbb{R}\times\mathbb{R}^{k}$. 因 $f\left(\cdot,y\right)$ 连续, 当 $n\to\infty$ 时网格 $a_{i}=i/n$ 加密, 使 $a_{i}\to{x}$, $a_{i+1}\to{x}$, 故 $f\left(a_{i},y\right)\to{f}\left(x,y\right)$, $f\left(a_{i+1},y\right)\to{f}\left(x,y\right)$; 而插值系数 $\frac{x-a_{i}}{c_{i}}$, $\frac{a_{i+1}-x}{c_{i}}\in\left[0,1\right]$ 有界. 故 $f_{n}\left(x,y\right)\to{f}\left(x,y\right)$.

由**定理 7.1.8 (实值可测函数的运算封闭性)** (4) (点点收敛极限可测), $f=\lim_{n}f_{n}$ 在 $\mathbb{R}\times\mathbb{R}^{k}$ 上博雷尔可测.

最后归纳证明: $\mathbb{R}^{n}$ 上逐变量连续的函数博雷尔可测. $n=1$ 时连续函数把开集拉回为开集, 故由**定义 4.3.2 (博雷尔 $\sigma$-代数)** 与**定义 7.1.1 (可测映射)** 可测 (亦为**定理 7.1.9 (可测函数与连续函数的复合)**). 设 $n-1$ 情形成立. 对 $\mathbb{R}^{n}=\mathbb{R}\times\mathbb{R}^{n-1}$ 上逐变量连续的函数 $f$, 对每个 $x$, $f\left(x,\cdot\right)$ 是 $\mathbb{R}^{n-1}$ 上的逐变量连续函数, 由归纳假设博雷尔可测; 对每个 $y$, $f\left(\cdot,y\right)$ 连续. 由上面已证的结论, $f$ 在 $\mathbb{R}\times\mathbb{R}^{n-1}$ 上博雷尔可测, 即 $f$ 在 $\mathbb{R}^{n}$ 上博雷尔可测.

$\blacksquare$

## 2

设 $f,g$ 是可积函数, $a,b\in\mathbb{R}$, 证明:

1. 线性性: $\int_{X}\left(af+bg\right)\mathrm{d}\mu=a\int_{X}f\,\mathrm{d}\mu+b\int_{X}g\,\mathrm{d}\mu$;

2. 单调性: 若 $f\le{g}$ 几乎处处, 则 $\int_{X}f\,\mathrm{d}\mu\le\int_{X}g\,\mathrm{d}\mu$;

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

1. 先对纯量乘: 若 $a\ge0$, 则 $\left(af\right)^{+}=af^{+}$, $\left(af\right)^{-}=af^{-}$, 故 $\int\left(af\right)\mathrm{d}\mu=a\int{f}^{+}\mathrm{d}\mu-a\int{f}^{-}\mathrm{d}\mu=a\int{f}\,\mathrm{d}\mu$; 若 $a<0$, 则 $\left(af\right)^{+}=\left|a\right|f^{-}$, $\left(af\right)^{-}=\left|a\right|f^{+}$, 同样得 $\int\left(af\right)\mathrm{d}\mu=a\int{f}\,\mathrm{d}\mu$; $a=0$ 平凡. 对加法, 由正负部分解 $f+g=\left(f^{+}+g^{+}\right)-\left(f^{-}+g^{-}\right)$, 即

$$
\left(f+g\right)^{+}+f^{-}+g^{-}=\left(f+g\right)^{-}+f^{+}+g^{+},
$$

两边均为非负可测函数, 由非负线性性积分得

$$
\int\left(f+g\right)^{+}\mathrm{d}\mu+\int{f}^{-}\mathrm{d}\mu+\int{g}^{-}\mathrm{d}\mu=\int\left(f+g\right)^{-}\mathrm{d}\mu+\int{f}^{+}\mathrm{d}\mu+\int{g}^{+}\mathrm{d}\mu,
$$

移项 (各项有限, 因 $f,g$ 可积) 得 $\int\left(f+g\right)\mathrm{d}\mu=\int{f}\,\mathrm{d}\mu+\int{g}\,\mathrm{d}\mu$. 结合两者得 $\int\left(af+bg\right)\mathrm{d}\mu=a\int{f}\,\mathrm{d}\mu+b\int{g}\,\mathrm{d}\mu$.

2. 由线性性, $\int{g}\,\mathrm{d}\mu-\int{f}\,\mathrm{d}\mu=\int\left(g-f\right)\mathrm{d}\mu$. 因 $f\le{g}$ 几乎处处, $g-f\ge0$ 几乎处处. 由**定义 8.2.1 (非负可测函数的积分)**, 非负可测函数的积分为非负 (它是非负简单函数积分的上确界), 故 $\int\left(g-f\right)\mathrm{d}\mu\ge0$, 即 $\int{f}\,\mathrm{d}\mu\le\int{g}\,\mathrm{d}\mu$.

3. $\left|f\right|=f^{+}+f^{-}$, 由非负线性性 $\int\left|f\right|\mathrm{d}\mu=\int{f}^{+}\mathrm{d}\mu+\int{f}^{-}\mathrm{d}\mu$. 再由 $\int{f}\,\mathrm{d}\mu=\int{f}^{+}\mathrm{d}\mu-\int{f}^{-}\mathrm{d}\mu$, 有

$$
\left|\int{f}\,\mathrm{d}\mu\right|=\left|\int{f}^{+}\mathrm{d}\mu-\int{f}^{-}\mathrm{d}\mu\right|\le\int{f}^{+}\mathrm{d}\mu+\int{f}^{-}\mathrm{d}\mu=\int\left|f\right|\mathrm{d}\mu.
$$

4. $f=g$ 几乎处处, 则 $f^{+}=g^{+}$, $f^{-}=g^{-}$ 几乎处处. 于是 $h:=f^{+}-g^{+}$ 可积且 $h=0$ 几乎处处, 其正部 $h^{+}$ 与负部 $h^{-}$ 均在零测集外为零. 由**命题 8.2.4 (积分关于集合的绝对连续性)**, $\int{h}^{+}\mathrm{d}\mu=\int_{\left\{h>0\right\}}h^{+}\mathrm{d}\mu=0$, $\int{h}^{-}\mathrm{d}\mu=0$, 故 $\int{h}\,\mathrm{d}\mu=0$, 即 $\int{f}^{+}\mathrm{d}\mu=\int{g}^{+}\mathrm{d}\mu$; 同理 $\int{f}^{-}\mathrm{d}\mu=\int{g}^{-}\mathrm{d}\mu$. 因此 $\int{f}\,\mathrm{d}\mu=\int{g}\,\mathrm{d}\mu$.

$\blacksquare$
