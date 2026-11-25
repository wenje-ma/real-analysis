# week11

> **定理 10.2.2 (托内利定理)**
> 
> 如果 $f:X\times{}Y\to\left[0,\infty\right]$ 是 $\mathcal{A}\otimes\mathcal{B}$-可测的, 则

> **定义 11.1.1 (符号测度)**
> 
> 设 $\left(X,\mathcal{F}\right)$ 是一个可测空间. 函数 $\nu:\mathcal{F}\to\mathbb{R}\cup\left\{+\infty\right\}$ 或 $\mathbb{R}\cup\left\{-\infty\right\}$ 称为符号测度, 若满足: (1) $\nu\left(\emptyset\right)=0$; (2) 可列可加性: 对任意一列互不相交的可测集 $\left\{E_{i}\right\}_{i=1}^{\infty}\subset\mathcal{F}$, 有 $\nu\left(\bigcup_{i=1}^{\infty}E_{i}\right)=\sum_{i=1}^{\infty}\nu\left(E_{i}\right)$; (3) $\nu$ 不能同时取 $+\infty$ 与 $-\infty$ 为值.

> **定义 11.4.1 (相互奇异的符号测度)**
> 
> 设 $\mu$ 和 $\nu$ 是可测空间 $\left(X,\mathcal{F}\right)$ 上的两个符号测度. 若存在可测集 $E\in\mathcal{F}$ 使得 $E$ 为 $\mu$-零集且 $E^{c}$ 为 $\nu$-零集, 则称 $\mu$ 和 $\nu$ 相互奇异, 记为 $\mu\perp\nu$.

> **定义 11.5.1 (绝对连续性)**
> 
> 设 $\mu$ 是正测度, $\nu$ 是符号测度. 称 $\nu$ 关于 $\mu$ 绝对连续 (记为 $\nu\ll\mu$), 若对任意 $E\in\mathcal{F}$ 有 $\mu\left(E\right)=0\Rightarrow\nu\left(E\right)=0$.

> **定理 11.5.5 (拉东-尼科迪姆定理)**
> 
> 设 $\mu$ 是 $\sigma$-有限正测度, $\nu$ 是符号测度且 $\nu\ll\mu$, 则存在可测函数 $f:X\to\mathbb{R}$ 使得 $\nu\left(E\right)=\int_{E}f\,\mathrm{d}\mu$ 对一切 $E\in\mathcal{F}$ 成立; 且 $\nu^{+}\left(E\right)=\int_{E}f^{+}\mathrm{d}\mu$, $\nu^{-}\left(E\right)=\int_{E}f^{-}\mathrm{d}\mu$, $\left|\nu\right|\left(E\right)=\int_{E}\left|f\right|\mathrm{d}\mu$. 函数 $f$ 称为 $\nu$ 关于 $\mu$ 的拉东-尼科迪姆导数, 记作 $f=\frac{\mathrm{d}\nu}{\mathrm{d}\mu}$.

> **定义 14.0.6 (有界变差函数)**
> 
> 设 $f:\left[a,b\right]\to\mathbb{R}$. 对 $\left[a,b\right]$ 的任意分划 $P:a=x_{0}<{}x_{1}<\cdots<{}x_{n}=b$, 定义变差 $V\left(f,P\right)=\sum_{i=1}^{n}\left|f\left(x_{i}\right)-f\left(x_{i-1}\right)\right|$. $f$ 在 $\left[a,b\right]$ 上的全变差为 $V_{a}^{b}\left(f\right)=\sup_{P}V\left(f,P\right)$. 若 $V_{a}^{b}\left(f\right)<+\infty$, 则称 $f$ 为有界变差函数, 记作 $f\in{}BV\left(\left[a,b\right]\right)$.

> **定理 14.0.7 (有界变差函数的基本性质)**
> 
> 设 $f,g\in{}BV\left(\left[a,b\right]\right)$, 则: (1) $BV\left(\left[a,b\right]\right)$ 构成一个线性空间; (2) $f$ 为有界函数; (3) 若 $f$ 满足利普希茨条件, 则 $f\in{}BV\left(\left[a,b\right]\right)$; (4) 单调函数必为有界变差函数.

> **定理 14.0.10 (有界变差函数的间断点性质)**
> 
> 若 $f\in{}BV\left(\left[a,b\right]\right)$, 则: (1) $f$ 的不连续点至多可数; (2) 所有不连续点都是第一类间断点.

## 3

设 $\left(X,\mathcal{M},\mu\right)$ 是 $\sigma$-有限测度空间, $\mathcal{N}$ 是 $\mathcal{M}$ 的子 $\sigma$-代数, $\nu=\mu|_{\mathcal{N}}$. 若 $f\in{}L^{1}\left(\mu\right)$, 则存在 $g\in{}L^{1}\left(\nu\right)$ (从而 $g$ 是 $\mathcal{N}$-可测的) 使得 $\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\nu$ 对一切 $E\in\mathcal{N}$ 成立; 若 $g'$ 是另一个这样的函数, 则 $g=g'$ $\nu$-几乎处处.

### 解答 3

按**定义 11.1.1 (符号测度)**, 对 $E\in\mathcal{N}$, 定义 $\nu_{0}\left(E\right):=\int_{E}f\,\mathrm{d}\mu$. 则 $\nu_{0}$ 是 $\mathcal{N}$ 上的符号测度: 有限可加性与可数可加性由 $\mu$ 的可数可加性及 $f$ 的可积性 (控制收敛) 保证, 且 $\left|\nu_{0}\left(E\right)\right|\le\int_{E}\left|f\right|\mathrm{d}\mu\le\int\left|f\right|\mathrm{d}\mu<\infty$, 故 $\nu_{0}$ 有限. 又 $\nu_{0}\ll\nu$ (**定义 11.5.1 (绝对连续性)**): 若 $E\in\mathcal{N}$ 且 $\nu\left(E\right)=\mu\left(E\right)=0$, 则 $\nu_{0}\left(E\right)=\int_{E}f\,\mathrm{d}\mu=0$ ($f\in{}L^{1}\left(\mu\right)$, 在零测集上积分为 $0$). 由于 $\nu=\mu|_{\mathcal{N}}$ 是 $\sigma$-有限的 (由 $\mu$ $\sigma$-有限), 由**定理 11.5.5 (拉东-尼科迪姆定理)**, 存在 $\mathcal{N}$-可测函数 $g=\frac{\mathrm{d}\nu_{0}}{\mathrm{d}\nu}\in{}L^{1}\left(\nu\right)$ 使得 $\int_{E}f\,\mathrm{d}\mu=\nu_{0}\left(E\right)=\int_{E}g\,\mathrm{d}\nu$ 对一切 $E\in\mathcal{N}$ 成立.

若 $g'\in{}L^{1}\left(\nu\right)$ 也满足同样等式, 则 $\int_{E}\left(g-g'\right)\mathrm{d}\nu=0$ 对一切 $E\in\mathcal{N}$. 取 $E=\left\{g>g'\right\}\in\mathcal{N}$, 因 $g-g'\in{}L^{1}\left(\nu\right)$ 且 $\int_{\left\{g>g'\right\}}\left(g-g'\right)\mathrm{d}\nu=0$, 由非负函数积分为零则几乎处处为零, 得 $g=g'$ $\nu$-几乎处处于 $\left\{g>g'\right\}$ 上; 同理于 $\left\{g<{}g'\right\}$ 上. 故 $g=g'$ $\nu$-几乎处处.

$\blacksquare$

## 4

设 $f\in{}L^{1}\left(\mathbb{R}^{n}\right)$ 且 $f\ne0$. 证明存在 $C,R>0$ 使得 $Hf\left(x\right)\ge{}C\left|x\right|^{-n}$ 对 $\left|x\right|>R$ 成立. 从而当 $\lambda$ 充分小时, $m\left(\left\{x:Hf\left(x\right)>\lambda\right\}\right)\ge{}C'\lambda^{-1}$, 故极大定理中的估计本质上是尖锐的.

### 解答 4

记 $Hf$ 为哈代-利特尔伍德极大函数 (哈代-利特尔伍德极大函数). 因 $f\ne0$ 且 $f\in{}L^{1}\left(\mathbb{R}^{n}\right)$, 存在球 $K$ (取某个紧集即可) 使 $\int_{K}\left|f\right|\mathrm{d}y>0$; 否则 $\left|\int_{K}f\right|$ 全为零将推出 $f=0$ 几乎处处, 矛盾. 记 $c=\int_{K}\left|f\right|\mathrm{d}y>0$, 并取 $R>0$ 使 $K\subset{}B\left(0,R\right)$ (即 $\sup_{y\in{}K}\left|y\right|<{}R$). 对 $\left|x\right|>R$, 因 $K\subset{}B\left(0,R\right)$ 且 $R<\left|x\right|$, 有 $K\subset{}B\left(x,2\left|x\right|\right)$. 于是由极大函数定义与球体积公式,

$$
Hf\left(x\right)\ge\frac{1}{\left|B\left(x,2\left|x\right|\right)\right|}\int_{B\left(x,2\left|x\right|\right)}\left|f\right|\mathrm{d}y\ge\frac{1}{\left|B\left(x,2\left|x\right|\right)\right|}\int_{K}\left|f\right|\mathrm{d}y=\frac{c}{C_{n}\left(2\left|x\right|\right)^{n}}=\frac{c}{2^{n}C_{n}}\left|x\right|^{-n}.
$$

取 $C=\frac{c}{2^{n}C_{n}}>0$, 即得 $Hf\left(x\right)\ge{}C\left|x\right|^{-n}$ 对 $\left|x\right|>R$ 成立.

第二问: 由第一问, 当 $0<\lambda<{}C/R^{n}$ 时, $\left(C/\lambda\right)^{1/n}>R$, 故 $\left\{x:\left|x\right|>\left(C/\lambda\right)^{1/n}\right\}\subset\left\{x:Hf\left(x\right)>\lambda\right\}$. 由球体积公式, 该集合的补集测度为 $m\left(\left\{x:\left|x\right|<\left(C/\lambda\right)^{1/n}\right\}\right)=C_{n}\left(\frac{C}{\lambda}\right)=\frac{C_{n}C}{\lambda}$. 令 $C'=C_{n}C$, 得 $m\left(\left\{x:Hf\left(x\right)>\lambda\right\}\right)\ge{}C'\lambda^{-1}$ 对充分小的 $\lambda>0$ 成立.

$\blacksquare$

## 5

哈代-利特尔伍德极大函数的一个有用变体是 $H^{*}f\left(x\right)=\sup\left\{\frac{1}{m\left(B\right)}\int_{B}\left|f\left(y\right)\right|\mathrm{d}y:B\text{~是球},x\in{}B\right\}$. 证明 $Hf\le{}H^{*}f\le2^{n}Hf$.

### 解答 5

先证 $Hf\le{}H^{*}f$. 对任意 $r>0$, 球 $B\left(x,r\right)$ 是含 $x$ 的球, 故 $\frac{1}{\left|B\left(x,r\right)\right|}\int_{B\left(x,r\right)}\left|f\right|\mathrm{d}y\le{}H^{*}f\left(x\right)$. 对 $r>0$ 取上确界得 $Hf\left(x\right)\le{}H^{*}f\left(x\right)$.

再证 $H^{*}f\le2^{n}Hf$. 设 $B$ 是含 $x$ 的任意球, 记其半径为 $\rho$,中心为 $c$. 因 $x\in{}B$, 有 $\left|x-c\right|\le\rho$, 故对任意 $y\in{}B$, $\left|y-x\right|\le\left|y-c\right|+\left|c-x\right|\le\rho+\rho=2\rho$, 即 $B\subset{}B\left(x,2\rho\right)$. 由球体积公式, $\left|B\left(x,2\rho\right)\right|=C_{n}\left(2\rho\right)^{n}=2^{n}C_{n}\rho^{n}=2^{n}\left|B\right|$. 于是

$$
\frac{1}{m\left(B\right)}\int_{B}\left|f\right|\mathrm{d}y\le\frac{1}{m\left(B\right)}\int_{B\left(x,2\rho\right)}\left|f\right|\mathrm{d}y=2^{n}\cdot\frac{1}{m\left(B\left(x,2\rho\right)\right)}\int_{B\left(x,2\rho\right)}\left|f\right|\mathrm{d}y\le2^{n}Hf\left(x\right).
$$

对一切含 $x$ 的球 $B$ 取上确界, 得 $H^{*}f\left(x\right)\le2^{n}Hf\left(x\right)$. 合并即 $Hf\le{}H^{*}f\le2^{n}Hf$.

$\blacksquare$

## 6

若 $\lambda$ 和 $\mu$ 是 $\mathbb{R}^{n}$ 上正且相互奇异的博雷尔测度, 且 $\lambda+\mu$ 正则, 则 $\lambda$ 和 $\mu$ 均正则.

### 解答 6

设 $\nu=\lambda+\mu$. 因 $\lambda\perp\mu$ (**定义 11.4.1 (相互奇异的符号测度)**), 存在博雷尔集 $A$ 使 $\mu\left(A\right)=0$ 且 $\lambda\left(A^{c}\right)=0$.

正则性的条件 (1). 对任意紧集 $K$, 由 $\lambda,\mu\ge0$ 及 $\nu$ 正则 (正则博雷尔测度), $\lambda\left(K\right)\le\nu\left(K\right)<\infty$, 同理 $\mu\left(K\right)<\infty$.

正则性的条件 (2) 对 $\lambda$. 先注意对任意 $E\in\mathcal{B}\left(\mathbb{R}^{n}\right)$, $\lambda\left(E\right)=\lambda\left(E\cap{}A\right)=\nu\left(E\cap{}A\right)$, 其中第二式用到 $\mu\left(E\cap{}A\right)\le\mu\left(A\right)=0$; 同理 $\mu\left(E\right)=\nu\left(E\cap{}A^{c}\right)$.

对任意开集 $U\supset{}E$, $U\cap{}A\supset{}E\cap{}A$, 故 $\lambda\left(U\right)=\nu\left(U\cap{}A\right)\ge\nu\left(E\cap{}A\right)=\lambda\left(E\right)$, 于是 $\inf\left\{\lambda\left(U\right):U\text{~开},U\supset{}E\right\}\ge\lambda\left(E\right)$.

反向: 给定 $\varepsilon>0$. 因 $\nu$ 正则, 对 $E\cap{}A$ 存在开集 $W\supset{}E\cap{}A$ 使 $\nu\left(W\cap{}A\right)<\nu\left(E\cap{}A\right)+\varepsilon=\lambda\left(E\right)+\varepsilon$ (用 $\nu$ 的外正则性先取开集 $W'\supset{}E\cap{}A$ 使 $\nu\left(W'\right)<\nu\left(E\cap{}A\right)+\varepsilon$, 再令 $W=W'$ 并注意 $\nu\left(W'\cap{}A\right)\le\nu\left(W'\right)$). 又因 $\left(E\cap{}A^{c}\right)\cap{}A=\emptyset$ 且 $\lambda\left(E\cap{}A^{c}\right)=0$, 可取足够薄的开邻域 $V\supset{}E\cap{}A^{c}$ 使 $\nu\left(V\cap{}A\right)<\varepsilon$ (例如取 $V=\left\{x:\mathrm{dist}\left(x,E\cap{}A^{c}\right)<\delta\right\}$ 并令 $\delta\to0$, 则 $V\cap{}A\downarrow\left(E\cap{}A^{c}\right)\cap{}A=\emptyset$, 由上连续性使 $\nu\left(V\cap{}A\right)\to0$). 令 $U=W\cup{}V$, 则 $U$ 开,$U\supset{}E$, 且 $\lambda\left(U\right)=\nu\left(U\cap{}A\right)\le\nu\left(W\cap{}A\right)+\nu\left(V\cap{}A\right)<\lambda\left(E\right)+2\varepsilon$. 故 $\inf\left\{\lambda\left(U\right):U\text{~开},U\supset{}E\right\}\le\lambda\left(E\right)$. 合并得 $\lambda\left(E\right)=\inf\left\{\lambda\left(U\right):U\text{~开},U\supset{}E\right\}$.

正则性的条件 (2) 对 $\mu$. 用 $\mu\left(E\right)=\nu\left(E\cap{}A^{c}\right)$ 及 $\nu|_{A^{c}}$ 的正则性, 论证完全对称, 得 $\mu$ 也满足条件 (2).

综上, $\lambda$ 与 $\mu$ 均正则.

$\blacksquare$

## 7

构造一个 $\mathbb{R}$ 上的递增函数, 使其间断点集恰为 $\mathbb{Q}$.

### 解答 7

按**定义 14.0.6 (有界变差函数)**, 枚举有理数 $\mathbb{Q}=\left\{q_{1},q_{2},\dots\right\}$, 定义 $F\left(x\right)=\sum_{q_{n}\le{}x}2^{-n}$, $x\in\mathbb{R}$. 这是至多可数项之和且每项非负, 值域含于 $\left[0,1\right]$. 由级数, $\sum_{n}2^{-n}$ 收敛, 故 $F$ 取值有限. 若 $x<{}y$, 则 $\left\{n:q_{n}\le{}x\right\}\subset\left\{n:q_{n}\le{}y\right\}$, 从而 $F\left(x\right)\le{}F\left(y\right)$, 即 $F$ 递增.

每个有理点是间断点. 对 $q_{k}\in\mathbb{Q}$, 当 $x$ 自 $q_{k}$ 左侧趋于 $q_{k}$ 时, $\left\{q_{n}\le{}x\right\}$ 不含 $q_{k}$, 故左极限 $F\left(q_{k}-\right)=\sum_{q_{n}<{}q_{k}}2^{-n}=\sum_{q_{n}\le{}q_{k}}2^{-n}-2^{-k}=F\left(q_{k}\right)-2^{-k}<{}F\left(q_{k}\right)$. 而右极限 $F\left(q_{k}+\right)=\lim_{x\downarrow{}q_{k}}F\left(x\right)=F\left(q_{k}\right)$ (因 $x>q_{k}$ 时仍计入 $q_{k}$). 故 $F$ 在 $q_{k}$ 处左,右极限不相等, 是第一类间断点.

每个无理点是连续点. 设 $x_{0}\in\mathbb{R}\setminus\mathbb{Q}$. 给定 $\varepsilon>0$, 由级数 取 $N$ 使 $\sum_{n>N}2^{-n}<\varepsilon$. 因 $x_{0}$ 无理, 取 $\delta>0$ 小到开区间 $\left(x_{0}-\delta,x_{0}+\delta\right)$ 内不含 $q_{1},\dots,q_{N}$ (有限个点, 可分离). 则当 $\left|x-x_{0}\right|<\delta$ 时, 区间 $\left(\min\left(x,x_{0}\right),\max\left(x,x_{0}\right)\right]$ 内至多含 $q_{N+1},q_{N+2},\dots$, 故 $\left|F\left(x\right)-F\left(x_{0}\right)\right|=\sum_{x_{0}<{}q_{n}\le{}x\text{~或~}x<{}q_{n}\le{}x_{0}}2^{-n}\le\sum_{n>N}2^{-n}<\varepsilon$. 故 $F$ 在 $x_{0}$ 连续.

综上, $F$ 的间断点集恰为 $\mathbb{Q}$. 由**定理 14.0.7 (有界变差函数的基本性质)** (4) 及**定理 14.0.10 (有界变差函数的间断点性质)**, $F$ 为递增有界函数从而是有界变差函数, 其间断点至多可数且均为第一类, 此处恰与 $\mathbb{Q}$ 相符.

$\blacksquare$
