# week9

> **定理 8.2.9 (控制收敛定理)**
> 
> 设 $\left(X,\mathcal{F},\mu\right)$ 是测度空间, $\left\{f_{n}\right\}$ 是一列可测函数, 若存在可积函数 $g$ 使 $\left|f_{n}\right|\le{g}$ 对所有 $n$ 成立, 且 $f_{n}\to{f}$ 几乎处处, 则 $f$ 可积且 $\int{f}\,\mathrm{d}\mu=\lim_{n\to\infty}\int{f}_{n}\,\mathrm{d}\mu$.

> **定理 8.2.16 (可积简单函数在 $L^{1}$ 中稠密)**
> 
> 如果 $f\in{L}^{1}\left(\mu\right)$ 且 $\varepsilon>0$, 则存在可积简单函数 $\varphi=\sum{a}_{j}\chi_{E_{j}}$ 使得 $\int\left|f-\varphi\right|\mathrm{d}\mu<\varepsilon$.

> **定理 10.2.1 (富比尼定理)**
> 
> 设 $\left(X,\mathcal{A},\mu\right)$ 和 $\left(Y,\mathcal{B},\nu\right)$ 是 $\sigma$-有限的测度空间, $f:X\times{Y}\to\mathbb{R}$ 是 $\mathcal{A}\otimes\mathcal{B}$-可测函数. 若 $f$ 在 $X\times{Y}$ 上可积, 则对几乎所有 $x$, $y\mapsto{f}\left(x,y\right)$ 是 $\nu$-可积的; 对几乎所有 $y$, $x\mapsto{f}\left(x,y\right)$ 是 $\mu$-可积的; 且重积分相等:

> **定理 10.2.2 (托内利定理)**
> 
> 如果 $f:X\times{Y}\to\left[0,\infty\right]$ 是 $\mathcal{A}\otimes\mathcal{B}$-可测的, 则

> **定理 11.1.1 (勒贝格测度的正则性与矩形逼近)**
> 
> 假设 $E\in\mathcal{L}^{n}$. (a)

> **定理 11.4.1 (极坐标下的积分公式)**
> 
> 存在 $S^{n-1}$ 上唯一的博雷尔测度 $\sigma=\sigma_{n-1}$, 使得 $m^{*}=\rho\times\sigma$. 若 $f$ 是 $\mathbb{R}^{n}$ 上的博雷尔可测函数, 且 $f\ge0$ 或 $f\in{L}^{1}\left(m\right)$, 则

## 1

如果 $f$ 在 $\left(0,a\right)$ 上勒贝格可积, 且 $g\left(x\right)=\int_{x}^{a}t^{-1}f\left(t\right)\mathrm{d}t$, 则 $g$ 在 $\left(0,a\right)$ 上可积且 $\int_{0}^{a}g\left(x\right)\mathrm{d}x=\int_{0}^{a}f\left(x\right)\mathrm{d}x$.

### 解答 1

先在 $\left(0,a\right)\times\left(0,a\right)$ 上考虑二元函数 $h\left(x,t\right)=t^{-1}f\left(t\right)\chi_{\left\{x<{}t\right\}}\left(x,t\right)$ (即定义域 $\left\{\left(x,t\right):0<{}x<{}t<{}a\right\}$). 由**定理 10.2.2 (托内利定理)** 应用于非负函数 $\left|h\right|$,

$$
\int_{0}^{a}\int_{x}^{a}t^{-1}\left|f\left(t\right)\right|\mathrm{d}t\,\mathrm{d}x=\int_{0}^{a}\left(\int_{0}^{t}t^{-1}\left|f\left(t\right)\right|\mathrm{d}x\right)\mathrm{d}t=\int_{0}^{a}t^{-1}\left|f\left(t\right)\right|\cdot{t}\,\mathrm{d}t=\int_{0}^{a}\left|f\left(t\right)\right|\mathrm{d}t<\infty,
$$

其中内层交换次序用**定理 10.2.2 (托内利定理)** 于非负函数. 故 $\left(x,t\right)\mapsto{t}^{-1}f\left(t\right)\chi_{\left\{x<{}t\right\}}$ 可积, 从而 $g$ 可积. 再由**定理 10.2.1 (富比尼定理)** 交换次序,

$$
\int_{0}^{a}g\left(x\right)\mathrm{d}x=\int_{0}^{a}\int_{x}^{a}t^{-1}f\left(t\right)\mathrm{d}t\,\mathrm{d}x=\int_{0}^{a}\left(\int_{0}^{t}t^{-1}f\left(t\right)\mathrm{d}x\right)\mathrm{d}t=\int_{0}^{a}t^{-1}f\left(t\right)\cdot{t}\,\mathrm{d}t=\int_{0}^{a}f\left(t\right)\mathrm{d}t.
$$

$\blacksquare$

## 2

设 $f\left(x\right)=x^{-1}\sin{x}$.

(a) 证明 $\int_{0}^{\infty}\left|f\left(x\right)\right|\mathrm{d}x=\infty$.

(b) 证明 $\lim_{b\to\infty}\int_{0}^{b}f\left(x\right)\mathrm{d}x=\frac{1}{2}\pi$, 通过积分 $e^{-xy}\sin{x}$ 关于 $x$ 和 $y$.

### 解答 2

(a). 在区间 $\left[k\pi,\left(k+1\right)\pi\right]$ 上, $\left|\sin{x}\right|\ge0$ 且 $\int_{k\pi}^{\left(k+1\right)\pi}\left|\sin{x}\right|\mathrm{d}x=2$. 因 $\frac{1}{x}$ 在此区间上 $\ge\frac{1}{\left(k+1\right)\pi}$, 有 $\int_{k\pi}^{\left(k+1\right)\pi}\frac{\left|\sin{x}\right|}{x}\mathrm{d}x\ge\frac{2}{\left(k+1\right)\pi}$. 于是对任意 $N$, $\int_{0}^{\left(N+1\right)\pi}\frac{\left|\sin{x}\right|}{x}\mathrm{d}x\ge\sum_{k=0}^{N}\frac{2}{\left(k+1\right)\pi}\to\infty$ (调和级数发散), 故 $\int_{0}^{\infty}\left|f\right|\mathrm{d}x=\infty$.

(b). 对固定的 $b>0$, 因 $\int_{0}^{b}\int_{0}^{\infty}\left|e^{-xy}\sin{x}\right|\mathrm{d}y\,\mathrm{d}x=\int_{0}^{b}\frac{\left|\sin{x}\right|}{x}\mathrm{d}x<\infty$ (固定 $b$ 时 $x^{-1}\sin{x}$ 可积), 由**定理 10.2.2 (托内利定理)** 可交换次序:

$$
\int_{0}^{b}\frac{\sin{x}}{x}\mathrm{d}x=\int_{0}^{b}\int_{0}^{\infty}e^{-xy}\sin{x}\,\mathrm{d}y\,\mathrm{d}x=\int_{0}^{\infty}\left(\int_{0}^{b}e^{-xy}\sin{x}\,\mathrm{d}x\right)\mathrm{d}y.
$$

对固定的 $y$, 分部积分两次得 $\int_{0}^{b}e^{-xy}\sin{x}\,\mathrm{d}x=\frac{1-e^{-by}\left(y\sin{b}+\cos{b}\right)}{1+y^{2}}$. 故 $\int_{0}^{b}\frac{\sin{x}}{x}\mathrm{d}x=\int_{0}^{\infty}\frac{1-e^{-by}\left(y\sin{b}+\cos{b}\right)}{1+y^{2}}\mathrm{d}y$.

取极限 $b\to\infty$. 拆成两项 $\frac{1}{1+y^{2}}-\frac{e^{-by}\left(y\sin{b}+\cos{b}\right)}{1+y^{2}}$. 第一项积分 $\int_{0}^{\infty}\frac{1}{1+y^{2}}\mathrm{d}y=\frac{\pi}{2}$. 对第二项, 当 $b\ge1$ 时 $\left|\frac{e^{-by}\left(y\sin{b}+\cos{b}\right)}{1+y^{2}}\right|\le\frac{e^{-y}\left(y+1\right)}{1+y^{2}}=:g\left(y\right)$, 且 $\int_{0}^{\infty}g\left(y\right)\mathrm{d}y<\infty$ (被 $e^{-y}$ 指数衰减控制). 由**定理 8.2.9 (控制收敛定理)** (对任意序列 $b_{n}\to\infty$ 应用), 该项趋于 $\int_{0}^{\infty}0\,\mathrm{d}y=0$. 故 $\lim_{b\to\infty}\int_{0}^{b}\frac{\sin{x}}{x}\mathrm{d}x=\frac{\pi}{2}$. $\blacksquare$

## 3

若 $f$ 在 $\left[0,\infty\right)$ 上连续, 对 $\alpha>0$ 和 $x\ge0$, 令

$$
I_{\alpha}f\left(x\right)=\frac{1}{\Gamma\left(\alpha\right)}\int_{0}^{x}\left(x-t\right)^{\alpha-1}f\left(t\right)\mathrm{d}t,
$$

$I_{\alpha}f$ 称为 $f$ 的 $\alpha$ 阶分数阶积分.

(a) $I_{\alpha+\beta}f=I_{\alpha}\left(I_{\beta}f\right)$ 对所有 $\alpha,\beta>0$ 成立.

(b) 若 $n\in\mathbb{N}$, $I_{n}f$ 是 $f$ 的 $n$ 阶反导数.

### 解答 3

(a). 展开复合积分, 在区域 $\left\{\left(s,t\right):0<{}t<{}s<{}x\right\}$ 上交换次序:

$$
I_{\alpha}\left(I_{\beta}f\right)\left(x\right)=\frac{1}{\Gamma\left(\alpha\right)}\int_{0}^{x}\left(x-s\right)^{\alpha-1}\left[\frac{1}{\Gamma\left(\beta\right)}\int_{0}^{s}\left(s-t\right)^{\beta-1}f\left(t\right)\mathrm{d}t\right]\mathrm{d}s.
$$

因 $f$ 连续, 被积函数可积, 由**定理 10.2.1 (富比尼定理)** 交换次序得

$$
=\frac{1}{\Gamma\left(\alpha\right)\Gamma\left(\beta\right)}\int_{0}^{x}f\left(t\right)\left[\int_{t}^{x}\left(x-s\right)^{\alpha-1}\left(s-t\right)^{\beta-1}\mathrm{d}s\right]\mathrm{d}t.
$$

对内层积分, 令 $u=\frac{s-t}{x-t}$, 则 $s=t+u\left(x-t\right)$, $\mathrm{d}s=\left(x-t\right)\mathrm{d}u$, 得

$$
\int_{t}^{x}\left(x-s\right)^{\alpha-1}\left(s-t\right)^{\beta-1}\mathrm{d}s=\left(x-t\right)^{\alpha+\beta-1}\int_{0}^{1}\left(1-u\right)^{\alpha-1}u^{\beta-1}\mathrm{d}u.
$$

由伽马函数与贝塔恒等式, $\int_{0}^{1}\left(1-u\right)^{\alpha-1}u^{\beta-1}\mathrm{d}u=\frac{\Gamma\left(\alpha\right)\Gamma\left(\beta\right)}{\Gamma\left(\alpha+\beta\right)}$. 代入得 $I_{\alpha}\left(I_{\beta}f\right)\left(x\right)=\frac{1}{\Gamma\left(\alpha+\beta\right)}\int_{0}^{x}\left(x-t\right)^{\alpha+\beta-1}f\left(t\right)\mathrm{d}t=I_{\alpha+\beta}f\left(x\right)$.

(b). 先看 $\alpha=1$: 因 $\Gamma\left(1\right)=1$, $I_{1}f\left(x\right)=\int_{0}^{x}f\left(t\right)\mathrm{d}t$, 由微积分基本定理 $\frac{\mathrm{d}}{\mathrm{d}x}I_{1}f=f$. 由 (a), 迭代得 $I_{n}f=\underbrace{I_{1}\circ\cdots\circ{I}_{1}}_{n\text{~次}}f$, 故 $\frac{\mathrm{d}^{n}}{\mathrm{d}x^{n}}I_{n}f=f$. 又因 $I_{\alpha}f$ 的积分下限为 $0$, 对 $k<{}n$ 有 $\left(\frac{\mathrm{d}}{\mathrm{d}x}\right)^{k}I_{n}f$ 在 $0$ 处取值为 $0$. 故 $I_{n}f$ 是 $f$ 的一个 $n$ 阶反导数. $\blacksquare$

## 4

$S^{n-1}$ 上的测度 $\sigma$ 在旋转下不变.

### 解答 4

设 $R\in{O}\left(n\right)$, 即 $R^{\top}R=I$, 则 $\left|\det{R}\right|=1$. 由正交变换保持勒贝格测度, $R$ 在 $\mathbb{R}^{n}$ 上保持 $m$. 由于 $R$ 保持范数 $\left|Rx\right|=\left|x\right|$, 它在球面坐标分解 $\Phi\left(x\right)=\left(r,x'\right)$ 下作用于球面部分: 存在球面 $S^{n-1}$ 上的旋转 $\rho$ 使 $R\left(rx'\right)=r\rho\left(x'\right)$. 记 $m^{*}$ 为极坐标诱导测度 ($m^{*}=\rho\times\sigma$ 由**定理 11.4.1 (极坐标下的积分公式)**), 对博雷尔集 $A\subset\left(0,\infty\right)\times{S}^{n-1}$,

$$
m^{*}\left(\left(\mathrm{id}\times\rho\right)\left(A\right)\right)=m\left(\Phi^{-1}\left(\left(\mathrm{id}\times\rho\right)\left(A\right)\right)\right)=m\left(R\Phi^{-1}\left(A\right)\right)=m\left(\Phi^{-1}\left(A\right)\right)=m^{*}\left(A\right),
$$

故 $m^{*}$ 旋转不变.

定义 $\sigma_{R}\left(E\right):=\sigma\left(R^{-1}E\right)=\sigma\left(R^{\top}E\right)$, 它是 $S^{n-1}$ 上的博雷尔测度. 对矩形 $\left(a,b\right]\times{E}\subset\left(0,\infty\right)\times{S}^{n-1}$,

$$
\left(\rho\times\sigma_{R}\right)\left(\left(a,b\right]\times{E}\right)=\int_{a}^{b}r^{n-1}\mathrm{d}r\cdot\sigma_{R}\left(E\right)=\rho\left(\left(a,b\right]\right)\cdot\sigma\left(R^{-1}E\right).
$$

由 $m^{*}=\rho\times\sigma$ (**定理 11.4.1 (极坐标下的积分公式)**), $\rho\left(\left(a,b\right]\right)\cdot\sigma\left(R^{-1}E\right)=m^{*}\left(\left(a,b\right]\times{R}^{-1}E\right)$. 又由 $m^{*}$ 的旋转不变性, $m^{*}\left(\left(a,b\right]\times{R}^{-1}E\right)=m^{*}\left(\left(a,b\right]\times{E}\right)=\rho\left(\left(a,b\right]\right)\cdot\sigma\left(E\right)$. 故在矩形上 $\rho\times\sigma_{R}=\rho\times\sigma$. 由测度在乘积 $\sigma$-代数生成族上的唯一性, $\rho\times\sigma_{R}=\rho\times\sigma$ 在 $\left(0,\infty\right)\times{S}^{n-1}$ 上成立.

最后由**定理 11.4.1 (极坐标下的积分公式)** 的唯一性 (使 $m^{*}=\rho\times\sigma$ 的测度 $\sigma$ 唯一), 从 $\rho\times\sigma_{R}=m^{*}=\rho\times\sigma$ 得 $\sigma_{R}=\sigma$, 即 $\sigma\left(R^{-1}E\right)=\sigma\left(E\right)$ 对一切博雷尔 $E$ 成立. 故 $\sigma$ 旋转不变. $\blacksquare$

## 5

对哪些实值 $a$ 和 $b$, $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ 在集合 $\left\{x\in\mathbb{R}^{n}:\left|x\right|<1/2\right\}$ 上可积? 在集合 $\left\{x\in\mathbb{R}^{n}:\left|x\right|>2\right\}$ 上可积?

### 解答 5

函数 $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ 是径向的, 由**定理 11.4.1 (极坐标下的积分公式)**,

$$
\int_{\mathbb{R}^{n}}\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}\mathrm{d}x=\sigma\left(S^{n-1}\right)\int_{0}^{\infty}r^{a+n-1}\left|\log{r}\right|^{b}\mathrm{d}r.
$$

集合 $\left\{\left|x\right|<1/2\right\}$. 作代换 $u=-\log{r}$ (即 $r=e^{-u}$, $\mathrm{d}r=-e^{-u}\mathrm{d}u$, 则 $r\in\left(0,1/2\right]$ 对应 $u\in\left[\log2,\infty\right)$):

$$
\int_{0}^{1/2}r^{a+n-1}\left|\log{r}\right|^{b}\mathrm{d}r=\int_{\log2}^{\infty}e^{-u\left(a+n-1\right)}e^{-u}u^{b}\mathrm{d}u=\int_{\log2}^{\infty}e^{-u\left(a+n\right)}u^{b}\mathrm{d}u.
$$

收敛条件由指数因子决定:

$$
\int_{\log2}^{\infty}e^{-u\left(a+n\right)}u^{b}\mathrm{d}u\text{~收敛}\iff\begin{cases}a+n>0,&\text{指数衰减,~任意~}b,\\a+n=0\text{~且~}b<-1,&\int{u}^{b}\mathrm{d}u\text{~收敛},\\a+n<0,&\text{指数增长,~发散}.\end{cases}
$$

故 $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ 在 $\left\{\left|x\right|<1/2\right\}$ 上可积 $\iff{a}>-n$, 或 $a=-n$ 且 $b<-1$.

集合 $\left\{\left|x\right|>2\right\}$. 当 $r\ge2$ 时 $\left|\log{r}\right|=\log{r}$. 作代换 $r=e^{u}$ ($\mathrm{d}r=e^{u}\mathrm{d}u$, $u\ge\log2$):

$$
\int_{2}^{\infty}r^{a+n-1}\left(\log{r}\right)^{b}\mathrm{d}r=\int_{\log2}^{\infty}e^{u\left(a+n-1\right)}e^{u}u^{b}\mathrm{d}u=\int_{\log2}^{\infty}e^{u\left(a+n\right)}u^{b}\mathrm{d}u.
$$

收敛条件: $\int_{\log2}^{\infty}e^{u\left(a+n\right)}u^{b}\mathrm{d}u\text{~收敛}\iff{a}+n<0$ (指数衰减; $a+n>0$ 时指数增长发散, $a+n=0$ 时 $\int{u}^{b}\mathrm{d}u$ 发散对任意 $b$). 故 $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ 在 $\left\{\left|x\right|>2\right\}$ 上可积 $\iff{a}<-n$.

结论. 在 $\left\{\left|x\right|<1/2\right\}$ 上可积 $\iff{a}>-n$ 或 $\left(a=-n\text{~且~}b<-1\right)$; 在 $\left\{\left|x\right|>2\right\}$ 上可积 $\iff{a}<-n$. $\blacksquare$
