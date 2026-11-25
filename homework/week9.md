# week9

> **定理 8.2.9 (控制收敛定理)**
> 
> 设 $\left(X,\mathcal{F},\mu\right)$ 是测度空间, $\left\{f_{n}\right\}$ 是一列可测函数, 若存在可积函数 $g$ 使 $\left|f_{n}\right|\le{}g$ 对所有 $n$ 成立, 且 $f_{n}\to{}f$ 几乎处处, 则 $f$ 可积且 $\int{}f\,\mathrm{d}\mu=\lim_{n\to\infty}\int{}f_{n}\,\mathrm{d}\mu$.

> **定理 10.2.1 (富比尼定理)**
> 
> 设 $\left(X,\mathcal{A},\mu\right)$ 和 $\left(Y,\mathcal{B},\nu\right)$ 是 $\sigma$-有限的测度空间, $f:X\times{}Y\to\mathbb{R}$ 是 $\mathcal{A}\otimes\mathcal{B}$-可测函数. 若 $f$ 在 $X\times{}Y$ 上可积, 则对几乎所有 $x$, $y\mapsto{}f\left(x,y\right)$ 是 $\nu$-可积的; 对几乎所有 $y$, $x\mapsto{}f\left(x,y\right)$ 是 $\mu$-可积的; 且重积分相等:

> **定理 10.2.2 (托内利定理)**
> 
> 如果 $f:X\times{}Y\to\left[0,\infty\right]$ 是 $\mathcal{A}\otimes\mathcal{B}$-可测的, 则

> **定理 11.4.1 (极坐标下的积分公式)**
> 
> 存在 $S^{n-1}$ 上唯一的博雷尔测度 $\sigma=\sigma_{n-1}$, 使得 $m^{*}=\rho\times\sigma$. 若 $f$ 是 $\mathbb{R}^{n}$ 上的博雷尔可测函数, 且 $f\ge0$ 或 $f\in{}L^{1}\left(m\right)$, 则

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

(b). 先看 $\alpha=1$: 因 $\Gamma\left(1\right)=1$, $I_{1}f\left(x\right)=\int_{0}^{x}f\left(t\right)\mathrm{d}t$, 由微积分基本定理 $\frac{\mathrm{d}}{\mathrm{d}x}I_{1}f=f$. 由 (a), 迭代得 $I_{n}f=\underbrace{I_{1}\circ\cdots\circ{}I_{1}}_{n\text{~次}}f$, 故 $\frac{\mathrm{d}^{n}}{\mathrm{d}x^{n}}I_{n}f=f$. 又因 $I_{\alpha}f$ 的积分下限为 $0$, 对 $k<{}n$ 有 $\left(\frac{\mathrm{d}}{\mathrm{d}x}\right)^{k}I_{n}f$ 在 $0$ 处取值为 $0$. 故 $I_{n}f$ 是 $f$ 的一个 $n$ 阶反导数.

$\blacksquare$

## 4

$S^{n-1}$ 上的测度 $\sigma$ 在旋转下不变.

### 解答 4

设 $R\in{}O\left(n\right)$, 即 $R^{\top}R=I$, 则 $\left|\det{}R\right|=1$. 由正交变换保持勒贝格测度, $R$ 在 $\mathbb{R}^{n}$ 上保持 $m$. 由于 $R$ 保持范数 $\left|Rx\right|=\left|x\right|$, 它在球面坐标分解 $\Phi\left(x\right)=\left(r,x'\right)$ 下作用于球面部分: 存在球面 $S^{n-1}$ 上的旋转 $\rho$ 使 $R\left(rx'\right)=r\rho\left(x'\right)$. 记 $m^{*}$ 为极坐标诱导测度 ($m^{*}=\rho\times\sigma$ 由**定理 11.4.1 (极坐标下的积分公式)**), 对博雷尔集 $A\subset\left(0,\infty\right)\times{}S^{n-1}$,

$$
m^{*}\left(\left(\mathrm{id}\times\rho\right)\left(A\right)\right)=m\left(\Phi^{-1}\left(\left(\mathrm{id}\times\rho\right)\left(A\right)\right)\right)=m\left(R\Phi^{-1}\left(A\right)\right)=m\left(\Phi^{-1}\left(A\right)\right)=m^{*}\left(A\right),
$$

故 $m^{*}$ 旋转不变.

定义 $\sigma_{R}\left(E\right):=\sigma\left(R^{-1}E\right)=\sigma\left(R^{\top}E\right)$, 它是 $S^{n-1}$ 上的博雷尔测度. 对矩形 $\left(a,b\right]\times{}E\subset\left(0,\infty\right)\times{}S^{n-1}$,

$$
\left(\rho\times\sigma_{R}\right)\left(\left(a,b\right]\times{}E\right)=\int_{a}^{b}r^{n-1}\mathrm{d}r\cdot\sigma_{R}\left(E\right)=\rho\left(\left(a,b\right]\right)\cdot\sigma\left(R^{-1}E\right).
$$

由 $m^{*}=\rho\times\sigma$ (**定理 11.4.1 (极坐标下的积分公式)**), $\rho\left(\left(a,b\right]\right)\cdot\sigma\left(R^{-1}E\right)=m^{*}\left(\left(a,b\right]\times{}R^{-1}E\right)$. 又由 $m^{*}$ 的旋转不变性, $m^{*}\left(\left(a,b\right]\times{}R^{-1}E\right)=m^{*}\left(\left(a,b\right]\times{}E\right)=\rho\left(\left(a,b\right]\right)\cdot\sigma\left(E\right)$. 故在矩形上 $\rho\times\sigma_{R}=\rho\times\sigma$. 由测度在乘积 $\sigma$-代数生成族上的唯一性, $\rho\times\sigma_{R}=\rho\times\sigma$ 在 $\left(0,\infty\right)\times{}S^{n-1}$ 上成立.

最后由**定理 11.4.1 (极坐标下的积分公式)** 的唯一性 (使 $m^{*}=\rho\times\sigma$ 的测度 $\sigma$ 唯一), 从 $\rho\times\sigma_{R}=m^{*}=\rho\times\sigma$ 得 $\sigma_{R}=\sigma$, 即 $\sigma\left(R^{-1}E\right)=\sigma\left(E\right)$ 对一切博雷尔 $E$ 成立. 故 $\sigma$ 旋转不变.

$\blacksquare$

## 5

对哪些实值 $a$ 和 $b$, $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ 在集合 $\left\{x\in\mathbb{R}^{n}:\left|x\right|<1/2\right\}$ 上可积? 在集合 $\left\{x\in\mathbb{R}^{n}:\left|x\right|>2\right\}$ 上可积?

### 解答 5

函数 $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ 是径向的, 由**定理 11.4.1 (极坐标下的积分公式)**,

$$
\int_{\mathbb{R}^{n}}\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}\mathrm{d}x=\sigma\left(S^{n-1}\right)\int_{0}^{\infty}r^{a+n-1}\left|\log{}r\right|^{b}\mathrm{d}r.
$$

集合 $\left\{\left|x\right|<1/2\right\}$. 作代换 $u=-\log{}r$ (即 $r=e^{-u}$, $\mathrm{d}r=-e^{-u}\mathrm{d}u$, 则 $r\in\left(0,1/2\right]$ 对应 $u\in\left[\log2,\infty\right)$):

$$
\int_{0}^{1/2}r^{a+n-1}\left|\log{}r\right|^{b}\mathrm{d}r=\int_{\log2}^{\infty}e^{-u\left(a+n-1\right)}e^{-u}u^{b}\mathrm{d}u=\int_{\log2}^{\infty}e^{-u\left(a+n\right)}u^{b}\mathrm{d}u.
$$

收敛条件由指数因子决定:

$$
\int_{\log2}^{\infty}e^{-u\left(a+n\right)}u^{b}\mathrm{d}u\text{~收敛}\Leftrightarrow\begin{cases}a+n>0,&\text{指数衰减,~任意~}b,\\a+n=0\text{~且~}b<-1,&\int{}u^{b}\mathrm{d}u\text{~收敛},\\a+n<0,&\text{指数增长,~发散}.\end{cases}
$$

故 $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ 在 $\left\{\left|x\right|<1/2\right\}$ 上可积 $\Leftrightarrow{}a>-n$, 或 $a=-n$ 且 $b<-1$.

集合 $\left\{\left|x\right|>2\right\}$. 当 $r\ge2$ 时 $\left|\log{}r\right|=\log{}r$. 作代换 $r=e^{u}$ ($\mathrm{d}r=e^{u}\mathrm{d}u$, $u\ge\log2$):

$$
\int_{2}^{\infty}r^{a+n-1}\left(\log{}r\right)^{b}\mathrm{d}r=\int_{\log2}^{\infty}e^{u\left(a+n-1\right)}e^{u}u^{b}\mathrm{d}u=\int_{\log2}^{\infty}e^{u\left(a+n\right)}u^{b}\mathrm{d}u.
$$

收敛条件: $\int_{\log2}^{\infty}e^{u\left(a+n\right)}u^{b}\mathrm{d}u\text{~收敛}\Leftrightarrow{}a+n<0$ (指数衰减; $a+n>0$ 时指数增长发散, $a+n=0$ 时 $\int{}u^{b}\mathrm{d}u$ 发散对任意 $b$). 故 $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ 在 $\left\{\left|x\right|>2\right\}$ 上可积 $\Leftrightarrow{}a<-n$.

结论. 在 $\left\{\left|x\right|<1/2\right\}$ 上可积 $\Leftrightarrow{}a>-n$ 或 $\left(a=-n\text{~且~}b<-1\right)$; 在 $\left\{\left|x\right|>2\right\}$ 上可积 $\Leftrightarrow{}a<-n$.

$\blacksquare$

## 2

设 $\nu$ 是 $\left(X,\mathcal{M}\right)$ 上的符号测度.

(a) $L^{1}\left(\nu\right)=L^{1}\left(\left|\nu\right|\right)$;

(b) 若 $f\in{}L^{1}\left(\nu\right)$, 则 $\left|\int{}f\,\mathrm{d}\nu\right|\le\int\left|f\right|\mathrm{d}\left|\nu\right|$;

(c) 若 $E\in\mathcal{M}$, 则 $\left|\nu\right|\left(E\right)=\sup\left\{\left|\int_{E}f\,\mathrm{d}\nu\right|:\left|f\right|\le1\right\}$.

### 解答 2

(a). 由**定义 11.4.4 (变差测度)**, $\left|\nu\right|=\nu^{+}+\nu^{-}$. 于是对任意 $f$,

$$
\int\left|f\right|\mathrm{d}\left|\nu\right|=\int\left|f\right|\mathrm{d}\nu^{+}+\int\left|f\right|\mathrm{d}\nu^{-}.
$$

三项均非负, 故左端有限当且仅当右端两项均有限, 即 $f\in{}L^{1}\left(\nu^{+}\right)\cap{}L^{1}\left(\nu^{-}\right)=L^{1}\left(\nu\right)$. 故 $L^{1}\left(\nu\right)=L^{1}\left(\left|\nu\right|\right)$.

(b). 由**定理 11.4.3 (若尔当分解定理)**, $\nu=\nu^{+}-\nu^{-}$. 于是由三角不等式与 (a),

$$
\left|\int{}f\,\mathrm{d}\nu\right|=\left|\int{}f\,\mathrm{d}\nu^{+}-\int{}f\,\mathrm{d}\nu^{-}\right|\le\int\left|f\right|\mathrm{d}\nu^{+}+\int\left|f\right|\mathrm{d}\nu^{-}=\int\left|f\right|\mathrm{d}\left|\nu\right|.
$$

(c). 先证 $\le$: 对任意可测函数 $g$ 满足 $\left|g\right|\le1$, 由 (b) 得 $\left|\int_{E}g\,\mathrm{d}\nu\right|\le\int_{E}\left|g\right|\mathrm{d}\left|\nu\right|\le\int_{E}1\,\mathrm{d}\left|\nu\right|=\left|\nu\right|\left(E\right)$, 故 $\sup\le\left|\nu\right|\left(E\right)$.

再证 $\ge$: 取 $\nu$ 的一个哈恩分解 $X=P\cup{}N$ (**定理 11.3.2 (哈恩分解定理)**), 令 $g=\chi_{E\cap{}P}-\chi_{E\cap{}N}$, 则 $\left|g\right|\le1$ 且 $g$ 可测. 由**定理 11.4.3 (若尔当分解定理)**, $\nu^{+}\left(E\right)=\nu\left(E\cap{}P\right)$, $\nu^{-}\left(E\right)=-\nu\left(E\cap{}N\right)$. 于是 $\int_{E}g\,\mathrm{d}\nu=\nu\left(E\cap{}P\right)-\nu\left(E\cap{}N\right)=\nu^{+}\left(E\right)+\nu^{-}\left(E\right)=\left|\nu\right|\left(E\right)$. 故 $\sup\ge\left|\nu\right|\left(E\right)$. 合并得等式.

$\blacksquare$

## 3

设 $\nu\left(E\right)=\int_{E}f\,\mathrm{d}\mu$, 其中 $\mu$ 是正测度, $f$ 是扩张的 $\mu$-可积函数. 用 $f$ 和 $\mu$ 描述 $\nu$ 的哈恩分解, 以及 $\nu$ 的正变差,负变差与全变差.

### 解答 3

$f$ 是实值可测函数, 至少一个 $\int{}f^{+}\mathrm{d}\mu$, $\int{}f^{-}\mathrm{d}\mu$ 有限. 由**定义 11.2.1 (正集,负集,零集)**: 对 $E\in\mathcal{M}$, $E$ 是 $\nu$-正集当且仅当对任意可测 $F\subset{}E$, $\nu\left(F\right)=\int_{F}f\,\mathrm{d}\mu\ge0$; 因这对 $F=E\cap\left\{f<0\right\}$ 与 $F=E\cap\left\{f>0\right\}$ 均须成立, 故 $E$ 是正集当且仅当 $f\ge0$ $\mu$-几乎处处于 $E$ 上. 同理, $E$ 是负集当且仅当 $f\le0$ $\mu$-几乎处处于 $E$ 上; $E$ 是零集当且仅当 $f=0$ $\mu$-几乎处处于 $E$ 上.

因此 $X=P\cup{}N$, 其中 $P=\left\{x:f\left(x\right)\ge0\right\}$, $N=\left\{x:f\left(x\right)<0\right\}$, 是 $\nu$ 的一个哈恩分解 (**定理 11.3.2 (哈恩分解定理)**): $P$ 是正集, $N$ 是负集, $P\cap{}N=\emptyset$, $P\cup{}N=X$. (零测集 $\left\{f=0\right\}$ 可并入 $P$ 或 $N$ 而不改变分解的本质.)

由**定理 11.4.3 (若尔当分解定理)**, $\nu^{+}\left(E\right)=\nu\left(E\cap{}P\right)=\int_{E\cap{}P}f\,\mathrm{d}\mu=\int_{E}f^{+}\mathrm{d}\mu$ (因 $f\ge0$ 于 $P$ 上), $\nu^{-}\left(E\right)=-\nu\left(E\cap{}N\right)=-\int_{E\cap{}N}f\,\mathrm{d}\mu=\int_{E}f^{-}\mathrm{d}\mu$ (因 $f\le0$ 于 $N$ 上). 故 $\nu^{+}\left(E\right)=\int_{E}f^{+}\mathrm{d}\mu$, $\nu^{-}\left(E\right)=\int_{E}f^{-}\mathrm{d}\mu$, $\left|\nu\right|\left(E\right)=\int_{E}\left|f\right|\mathrm{d}\mu$.

$\blacksquare$
