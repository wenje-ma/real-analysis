# week8

> **定义 5.1.2 (测度)**
> 
> 设 $\left(X,\mathcal{F}\right)$ 是一个可测空间. 函数 $\mu:\mathcal{F}\to\left[0,+\infty\right]$ 称为 $\left(X,\mathcal{F}\right)$ 上的一个测度, 如果满足: (1) 非负性: $\mu\left(E\right)\ge0$ 对一切 $E\in\mathcal{F}$ 成立; (2) 零空集性: $\mu\left(\emptyset\right)=0$; (3) 可数可加性 ($\sigma$-可加性): 对任意可数个两两不交的集合 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$, 有 $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **定义 6.2.1 (准测度)**
> 
> 设 $X$ 是非空集合, $\mathcal{E}\subset\mathcal{P}\left(X\right)$ 是一个代数. 函数 $\mu_{0}:\mathcal{E}\to\left[0,+\infty\right]$ 称为一个准测度, 如果 $\mu_{0}\left(\emptyset\right)=0$, 且若 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{E}$ 两两不交且 $\bigcup_{n=1}^{\infty}E_{n}\in\mathcal{E}$, 则 $\mu_{0}\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu_{0}\left(E_{n}\right)$.

> **定理 6.3.3 (卡拉西奥多里定理)**
> 
> 设 $\mu^{*}$ 是 $X$ 上的外测度, 则: (1) $\mathcal{M}$ 是一个 $\sigma$-代数; (2) $\mu^{*}|_{\mathcal{M}}$ 是一个完备测度; (3) 如果 $\mu^{*}$ 是由准测度 $\mu_{0}$ 生成的, 且 $\mu_{0}$ 是 $\sigma$-有限的, 则 $\mu^{*}|_{\mathcal{M}}$ 是 $\mu_{0}$ 的唯一延拓.

> **命题 7.1.5 (复合保持可测性)**
> 
> 若 $f:X\to{Y}$ 是 $\left(\mathcal{F},\mathcal{G}\right)$-可测的, $g:Y\to{Z}$ 是 $\left(\mathcal{G},\mathcal{H}\right)$-可测的, 则 $g\circ{f}:X\to{Z}$ 是 $\left(\mathcal{F},\mathcal{H}\right)$-可测的.

> **命题 7.1.7 (乘积空间的可测性)**
> 
> 设 $f=\left(f_{1},\dots,f_{n}\right):X\to{Y}_{1}\times\cdots\times{Y}_{n}$. 在乘积空间配备乘积 $\sigma$-代数下, $f$ 可测当且仅当每个坐标映射 $f_{i}:X\to{Y}_{i}$ 可测.

> **定理 8.2.9 (控制收敛定理)**
> 
> 设 $\left(X,\mathcal{F},\mu\right)$ 是测度空间, $\left\{f_{n}\right\}$ 是一列可测函数, 若存在可积函数 $g$ 使 $\left|f_{n}\right|\le{g}$ 对所有 $n$ 成立, 且 $f_{n}\to{f}$ 几乎处处, 则 $f$ 可积且 $\int{f}\,\mathrm{d}\mu=\lim_{n\to\infty}\int{f}_{n}\,\mathrm{d}\mu$.

> **定理 8.2.16 (可积简单函数在 $L^{1}$ 中稠密)**
> 
> 如果 $f\in{L}^{1}\left(\mu\right)$ 且 $\varepsilon>0$, 则存在可积简单函数 $\varphi=\sum{a}_{j}\chi_{E_{j}}$ 使得 $\int\left|f-\varphi\right|\mathrm{d}\mu<\varepsilon$.

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

> **定理 11.1.1 (勒贝格测度的正则性与矩形逼近)**
> 
> 假设 $E\in\mathcal{L}^{n}$. (a)

$$
m\left(E\right)=\inf\left\{m\left(U\right):U\supset{E},U\text{~开}\right\}=\sup\left\{m\left(K\right):K\subset{E},K\text{~紧}\right\};
$$
(b) 若 $m\left(E\right)<\infty$, 则对任意 $\varepsilon>0$, 存在有限个边为区间的互不相交的矩形族 $\left\{R_{j}\right\}_{j=1}^{N}$, 使得 $m\left(E\triangle\bigcup_{j=1}^{N}R_{j}\right)<\varepsilon$.

> **定理 11.4.1 (极坐标下的积分公式)**
> 
> 存在 $S^{n-1}$ 上唯一的博雷尔测度 $\sigma=\sigma_{n-1}$, 使得 $m^{*}=\rho\times\sigma$. 若 $f$ 是 $\mathbb{R}^{n}$ 上的博雷尔可测函数, 且 $f\ge0$ 或 $f\in{L}^{1}\left(m\right)$, 则

$$
\int_{\mathbb{R}^{n}}f\left(x\right)\mathrm{d}x=\int_{0}^{\infty}\int_{S^{n-1}}f\left(rx'\right)r^{n-1}\mathrm{d}\sigma\left(x'\right)\mathrm{d}r.
$$

## 1

设 $X=Y=\mathbb{N}$, $\mathcal{M}=\mathcal{N}=\mathcal{P}\left(\mathbb{N}\right)$, $\mu=\nu$ 是计数测度. 定义 $f\left(m,n\right)=1$ 若 $m=n$, $f\left(m,n\right)=-1$ 若 $m=n+1$, $f\left(m,n\right)=0$ 否则. 则 $\int\left|f\right|\mathrm{d}\left(\mu\times\nu\right)=\infty$, 且 $\iint{f}\,\mathrm{d}\mu\,\mathrm{d}\nu$ 与 $\iint{f}\,\mathrm{d}\nu\,\mathrm{d}\mu$ 存在但不相等.

### 解答 1

计算 $\int\left|f\right|\mathrm{d}\left(\mu\times\nu\right)=\sum_{m,n}\left|f\left(m,n\right)\right|$. $f$ 在对角线 $\left\{\left(m,m\right)\right\}$ 上取 $1$, 在次对角线 $\left\{\left(m+1,m\right)\right\}$ 上取 $-1$, 故 $\left|f\right|$ 在这两族无限多个点上取 $1$, 于是 $\int\left|f\right|\mathrm{d}\left(\mu\times\nu\right)=\sum_{m,n}\left|f\left(m,n\right)\right|=\infty$.

算 $\iint{f}\,\mathrm{d}\mu\,\mathrm{d}\nu$ (内层按 $\mu$ 求和, 外层按 $\nu$ 求和). 对固定 $n$, $\sum_{m}f\left(m,n\right)=f\left(n,n\right)+f\left(n+1,n\right)=1+\left(-1\right)=0$, 故 $\iint{f}\,\mathrm{d}\mu\,\mathrm{d}\nu=\sum_{n}0=0$.

算 $\iint{f}\,\mathrm{d}\nu\,\mathrm{d}\mu$ (内层按 $\nu$ 求和). 对固定 $m$, 当 $m\ge1$ 时 $\sum_{n}f\left(m,n\right)=f\left(m,m\right)+f\left(m,m-1\right)=1+\left(-1\right)=0$; 而 $m=0$ 时 $f\left(0,n\right)$ 只在 $n=0$ 处为 $1$, 和为 $1$. 故 $\iint{f}\,\mathrm{d}\nu\,\mathrm{d}\mu=\sum_{m}\left(\sum_{n}f\left(m,n\right)\right)=1$.

故 $\iint{f}\,\mathrm{d}\mu\,\mathrm{d}\nu=0\ne1=\iint{f}\,\mathrm{d}\nu\,\mathrm{d}\mu$. 因 $\int\left|f\right|\mathrm{d}\left(\mu\times\nu\right)=\infty$, $f$ 非绝对可积, **定理 10.2.1 (富比尼定理)** 的假设 $\int\left|f\right|\mathrm{d}\left(\mu\times\nu\right)<\infty$ 不满足, 故不能交换积分次序. $\blacksquare$

## 2

设 $\left(X,\mathcal{M},\mu\right)$ 是 $\sigma$-有限测度空间且 $f\in{L}^{+}\left(X\right)$. 令 $G_{f}=\left\{\left(x,y\right)\in{X}\times\left[0,\infty\right]:y\le{f}\left(x\right)\right\}$. 则 $G_{f}$ 是 $\mathcal{M}\otimes\mathcal{B}_{\mathbb{R}}$-可测的且 $\mu\times{m}\left(G_{f}\right)=\int{f}\,\mathrm{d}\mu$; 若把定义中 $y\le{f}\left(x\right)$ 的不等式换成 $y<{}f\left(x\right)$, 结论同样成立.

### 解答 2

可测性. 考虑映射 $T:X\times\left[0,\infty\right]\to\left[0,\infty\right]\times\left[0,\infty\right]$, $T\left(x,y\right)=\left(f\left(x\right),y\right)$. 由**命题 7.1.7 (乘积空间的可测性)**, $T$ 可测当且仅当其坐标函数可测; 坐标函数 $\left(x,y\right)\mapsto{f}\left(x\right)=f\circ{p}_{1}$ 可测 (因 $f$ 可测), $\left(x,y\right)\mapsto{y}=p_{2}$ 连续可测. 故 $T$ 可测. 又 $\Phi\left(z,y\right)=z-y$ 连续, 博雷尔可测. 由**命题 7.1.5 (复合保持可测性)**, $\left(x,y\right)\mapsto{f}\left(x\right)-y=\Phi\circ{T}$ 可测. 因

$$
G_{f}=\left\{\left(x,y\right):f\left(x\right)-y\ge0\right\}=\left(f-y\right)^{-1}\left(\left[0,\infty\right]\right),
$$

是可测函数的原像, 由**定义 10.1.1 (乘积 $\sigma$-代数)**, $G_{f}\in\mathcal{M}\otimes\mathcal{B}_{\mathbb{R}}$.

测度值. 由**定理 10.2.2 (托内利定理)** (非负特征函数, $\mu\times{m}$ $\sigma$-有限),

$$
\left(\mu\times{m}\right)\left(G_{f}\right)=\int_{X}m\left(\left(G_{f}\right)_{x}\right)\mathrm{d}\mu\left(x\right),
$$

其中 $\left(G_{f}\right)_{x}=\left\{y\in\left[0,\infty\right]:y\le{f}\left(x\right)\right\}=\left[0,f\left(x\right)\right]$, 勒贝格测度 $m\left(\left[0,f\left(x\right)\right]\right)=f\left(x\right)$. 故 $\left(\mu\times{m}\right)\left(G_{f}\right)=\int_{X}f\left(x\right)\mathrm{d}\mu\left(x\right)$.

若把 $y\le{f}\left(x\right)$ 换成 $y<{}f\left(x\right)$, 则 $\left(G_{f}\right)_{x}=\left[0,f\left(x\right)\right)$, 仍有 $m=f\left(x\right)$, 结论不变. $\blacksquare$

## 3

若 $f\in{L}^{1}\left(m\right)$ 且 $\varepsilon>0$, 则存在一个简单函数 $\varphi=\sum{a}_{j}\chi_{R_{j}}$, 其中每个 $R_{j}$ 是区间之积, 使得 $\int\left|f-\varphi\right|<\varepsilon$; 且存在一个在有界集外为零的连续函数 $g$, 使得 $\int\left|f-g\right|<\varepsilon$.

### 解答 3

简单函数部分. 由**定理 8.2.16 (可积简单函数在 $L^{1}$ 中稠密)**, 存在可积简单函数 $\varphi=\sum_{j}a_{j}\chi_{E_{j}}$ 使得 $\int\left|f-\varphi\right|<\varepsilon/2$. 对 $a_{j}\ne0$ 的项, 由 $\int{a}_{j}\chi_{E_{j}}\,\mathrm{d}m=a_{j}m\left(E_{j}\right)<\infty$ 得 $m\left(E_{j}\right)<\infty$ (否则积分发散, 与可积性矛盾). 由**定理 11.1.1 (勒贝格测度的正则性与矩形逼近)** (b), 对每个这样的 $E_{j}$ 存在有限个边为区间的互不相交矩形 $\left\{R_{j,k}\right\}$ 使 $m\left(E_{j}\triangle\bigcup_{k}R_{j,k}\right)$ 任意小. 于是 $\chi_{E_{j}}$ 与 $\chi_{R_{j}}$ (其中 $R_{j}=\bigcup_{k}R_{j,k}$) 在 $L^{1}$ 中任意接近, 取足够小的逼近误差并合并所有 $j$, 得到简单函数 $\varphi'=\sum_{j}a_{j}\chi_{R_{j}}$ 满足 $\int\left|\varphi-\varphi'\right|<\varepsilon/2$. 故 $\int\left|f-\varphi'\right|\le\int\left|f-\varphi\right|+\int\left|\varphi-\varphi'\right|<\varepsilon$.

连续函数部分. 设 $\varphi'=\sum_{j}a_{j}\chi_{R_{j}}$ 已由上一步得到, 其中每个 $R_{j}$ 是有界闭矩形. 由特征函数的连续逼近, 对每个 $R_{j}$ 存在具有紧支撑的连续函数 $g_{j}$ 使 $\int\left|\chi_{R_{j}}-g_{j}\right|\mathrm{d}m$ 任意小. 取逼近误差足够小并令 $g=\sum_{j}a_{j}g_{j}$, 则 $g$ 连续且支撑在 $\bigcup_{j}R_{j}$ 中 (有界集), 且 $\int\left|\varphi'-g\right|\le\sum_{j}\left|a_{j}\right|\int\left|\chi_{R_{j}}-g_{j}\right|<\varepsilon/2$. 于是 $\int\left|f-g\right|\le\int\left|f-\varphi'\right|+\int\left|\varphi'-g\right|<\varepsilon$, 且 $g$ 在有界集外为零. $\blacksquare$

## 4

(线性变量替换公式) 假设 $T\in{G}L\left(n,\mathbb{R}\right)$.

(a) 如果 $f$ 是 $\mathbb{R}^{n}$ 上的勒贝格可测函数, 则 $f\circ{T}$ 也是. 如果 $f\ge0$ 或 $f\in{L}^{1}\left(m\right)$, 那么 $\int{f}\left(x\right)\mathrm{d}x=\left|\det{T}\right|\int{f}\circ{T}\left(x\right)\mathrm{d}x$.

(b) 如果 $E\in\mathcal{L}^{n}$, 则 $T\left(E\right)\in\mathcal{L}^{n}$ 且 $m\left(T\left(E\right)\right)=\left|\det{T}\right|m\left(E\right)$.

### 解答 4

先证三种初等变换的情形, 再组合.

伸缩变换 $T_{1}\left(x_{1},\dots,x_{j},\dots,x_{n}\right)=\left(x_{1},\dots,cx_{j},\dots,x_{n}\right)$ ($c\ne0$). 由一维平移与伸缩的不变性 并结合乘积结构, 逐坐标伸缩保持其余坐标不动, 有 $m\left(T_{1}\left(E\right)\right)=\left|c\right|m\left(E\right)$ 且 $\int{f}\circ{T}_{1}\left(x\right)\mathrm{d}x=\frac{1}{\left|c\right|}\int{f}\left(x\right)\mathrm{d}x$, 即 $\int{f}\left(x\right)\mathrm{d}x=\left|\det{T}_{1}\right|\int{f}\circ{T}_{1}\left(x\right)\mathrm{d}x$.

剪切变换 $T_{2}\left(x_{1},\dots,x_{j},\dots,x_{n}\right)=\left(x_{1},\dots,x_{j}+cx_{k},\dots,x_{n}\right)$ ($k\ne{j}$). 由一维平移与伸缩的不变性 逐切片应用, $m\left(T_{2}\left(E\right)\right)=m\left(E\right)$ 且 $\int{f}\circ{T}_{2}\left(x\right)\mathrm{d}x=\int{f}\left(x\right)\mathrm{d}x$. 因 $\det{T}_{2}=1$, 公式成立.

交换变换 $T_{3}$ 交换两个坐标, $\det{T}_{3}=-1$. 由 $m$ 作为乘积测度的对称性, $m\left(T_{3}\left(E\right)\right)=m\left(E\right)$ 且 $\int{f}\circ{T}_{3}\left(x\right)\mathrm{d}x=\int{f}\left(x\right)\mathrm{d}x$, 而 $\left|\det{T}_{3}\right|=1$, 公式成立.

一般情形. 由初等线性代数, 每个 $T\in{G}L\left(n,\mathbb{R}\right)$ 都可写成有限个上述三种初等变换的乘积 $T=T_{1}\circ\cdots\circ{T}_{k}$ (可逆矩阵可通过行变换化为单位矩阵). 对每个初等变换上式成立, 且行列式相乘 $\left|\det{T}\right|=\prod_{i}\left|\det{T}_{i}\right|$. 逐次代入得

$$
\int{f}\left(x\right)\mathrm{d}x=\left|\det{T}_{1}\right|\int{f}\circ{T}_{1}\left(x\right)\mathrm{d}x=\cdots=\left|\det{T}\right|\int{f}\circ{T}\left(x\right)\mathrm{d}x,
$$

此即 (a). 可测性: $T$ 连续, 由可逆线性变换保持可测性与零测集 得 $f\circ{T}$ 可测且 $T\left(E\right)\in\mathcal{L}^{n}$.

证 (b). 在 (a) 中取 $f=\chi_{T\left(E\right)}$, 则

$$
m\left(T\left(E\right)\right)=\int\chi_{T\left(E\right)}\left(x\right)\mathrm{d}x=\left|\det{T}\right|\int\chi_{T\left(E\right)}\circ{T}\left(x\right)\mathrm{d}x=\left|\det{T}\right|\int\chi_{E}\left(x\right)\mathrm{d}x=\left|\det{T}\right|m\left(E\right).
$$

$T\left(E\right)\in\mathcal{L}^{n}$ 已由可测性保证. $\blacksquare$

## 5

设 $E=\left[0,1\right]\times\left[0,1\right]$. 研究 $\int_{E}f\,\mathrm{d}m^{2}$, $\int_{0}^{1}\int_{0}^{1}f\left(x,y\right)\mathrm{d}x\,\mathrm{d}y$ 与 $\int_{0}^{1}\int_{0}^{1}f\left(x,y\right)\mathrm{d}y\,\mathrm{d}x$ 的存在性和相等性, 对下列 $f$.

(a) $f\left(x,y\right)=\left(x^{2}-y^{2}\right)\left(x^{2}+y^{2}\right)^{-2}$;

(b) $f\left(x,y\right)=\left(1-xy\right)^{-a}$ ($a>0$);

(c) $f\left(x,y\right)=\left(x-y\right)^{-3}$, 若 $0<{}y<{}x<1$, 否则为 $0$.

### 解答 5

(a). $\left|f\left(x,y\right)\right|=\frac{\left|x^{2}-y^{2}\right|}{\left(x^{2}+y^{2}\right)^{2}}\le\frac{x^{2}+y^{2}}{\left(x^{2}+y^{2}\right)^{2}}=\frac{1}{x^{2}+y^{2}}$. 在 $E$ 上 $\int_{E}\frac{1}{x^{2}+y^{2}}\mathrm{d}x\,\mathrm{d}y$ 发散 (用极坐标, $\int_{0}^{\delta}\int_{0}^{\pi/2}\frac{1}{r^{2}}r\,\mathrm{d}\theta\,\mathrm{d}r=\frac{\pi}{2}\int_{0}^{\delta}\frac{1}{r}\mathrm{d}r=\infty$), 故 $\int_{E}\left|f\right|=\infty$, $f\notin{L}^{1}$, $\int_{E}f\,\mathrm{d}m^{2}$ 无定义.

先对 $x$ 积分. 固定 $y$, 令 $x=yt$, 则 $\int_{0}^{1}\frac{x^{2}-y^{2}}{\left(x^{2}+y^{2}\right)^{2}}\mathrm{d}x=\frac{1}{y}\int_{0}^{1/y}\frac{t^{2}-1}{\left(t^{2}+1\right)^{2}}\mathrm{d}t$. 因 $\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{t}{t^{2}+1}\right)=\frac{1-t^{2}}{\left(t^{2}+1\right)^{2}}$, 有 $\int\frac{t^{2}-1}{\left(t^{2}+1\right)^{2}}\mathrm{d}t=-\frac{t}{t^{2}+1}+C$, 故内层积分 $=\frac{1}{y}\left[-\frac{t}{t^{2}+1}\right]_{0}^{1/y}=-\frac{1}{y^{2}+1}$. 于是 $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y=\int_{0}^{1}-\frac{1}{1+y^{2}}\mathrm{d}y=-\left[\arctan{y}\right]_{0}^{1}=-\frac{\pi}{4}$.

先对 $y$ 积分. 对称地, 固定 $x$ 令 $y=xt$, 内层 $\int_{0}^{1}f\,\mathrm{d}y=\frac{1}{x^{2}+1}$, 故 $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x=\int_{0}^{1}\frac{1}{1+x^{2}}\mathrm{d}x=\frac{\pi}{4}$.

结论: $\int_{E}f\,\mathrm{d}m^{2}$ 不存在; $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y=-\frac{\pi}{4}$ 与 $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x=\frac{\pi}{4}$ 存在但不等, 符号相反. 因 $f\notin{L}^{1}$, **定理 10.2.1 (富比尼定理)** 不适用, 两个迭代积分不可交换.

(b). $f\ge0$. 固定 $y$, 内层 $\int_{0}^{1}\left(1-xy\right)^{-a}\mathrm{d}x=\frac{1}{y}\cdot\frac{1-\left(1-y\right)^{1-a}}{1-a}$ (当 $a\ne1$), 且 $a=1$ 时内层 $=-\frac{\ln\left(1-y\right)}{y}$. 对 $0<{}a<1$, 内层在 $y\to0$ 处趋于 $1$, 在 $y\to1$ 处趋于 $\frac{1}{1-a}$ (因 $\left(1-y\right)^{1-a}\to0$), 故有界, $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y<\infty$. 对 $a=1$, $\int_{0}^{1}-\frac{\ln\left(1-y\right)}{y}\mathrm{d}y=\sum_{k=1}^{\infty}\frac{1}{k^{2}}=\frac{\pi^{2}}{6}<\infty$. 故 $0<{}a\le1$ 时 $f\in{L}^{1}$, 由**定理 10.2.2 (托内利定理)**, 三个积分都存在且相等.

$a>1$ 时, 内层 $\frac{1}{y}\cdot\frac{1-\left(1-y\right)^{1-a}}{1-a}$, 因 $1-a<0$ 且 $y\to1$ 时 $\left(1-y\right)^{1-a}\to\infty$, 内层趋于 $+\infty$, 故 $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y=+\infty$; 对称地 $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x=+\infty$, 且 $\int_{E}f\,\mathrm{d}m^{2}=+\infty$.

结论: $0<{}a\le1$ 时三个积分存在且相等, $f\in{L}^{1}$; $a>1$ 时三个积分均为 $+\infty$, $f\notin{L}^{1}$.

(c). 区域为 $\left\{\left(x,y\right):0<{}y<{}x<1\right\}$. $\left|f\right|=\left(x-y\right)^{-3}$. 先对 $x$ 积分, $\int_{y}^{1}\left(x-y\right)^{-3}\mathrm{d}x=\left[-\frac{1}{2}\left(x-y\right)^{-2}\right]_{y}^{1}=+\infty$, 故 $\int_{E}\left|f\right|=\infty$, $f\notin{L}^{1}$, $\int_{E}f\,\mathrm{d}m^{2}$ 无定义.

先对 $x$ 积分: 固定 $y$, $\int_{y}^{1}\left(x-y\right)^{-3}\mathrm{d}x=\left[-\frac{1}{2}\left(x-y\right)^{-2}\right]_{y}^{1}$, 因 $\lim_{x\to{y}^{+}}\left(x-y\right)^{-2}=\infty$, 故内层积分 $=+\infty$, 于是 $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y=+\infty$.

先对 $y$ 积分: 固定 $x$, $\int_{0}^{x}\left(x-y\right)^{-3}\mathrm{d}y=\left[-\frac{1}{2}\left(x-y\right)^{-2}\right]_{0}^{x}$, 因 $\lim_{y\to{x}^{-}}\left(x-y\right)^{-2}=\infty$, 故内层积分 $=-\infty$, 于是 $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x=-\infty$.

结论: $\int_{E}f\,\mathrm{d}m^{2}$ 不存在; $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y=+\infty$ 而 $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x=-\infty$, 两个迭代积分存在但不等且符号相反. 这是富比尼失效的经典反例: 非绝对可积时积分次序不可交换. $\blacksquare$
