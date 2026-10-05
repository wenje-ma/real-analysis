# 作业 8

> **定理 8.2.9** (控制收敛定理)<br>设 $\left(X,\mathcal F,\mu\right)$ 是测度空间, $\left\{f_{n}\right\}$ 是一列可测函数, 若存在可积函数 $g$ 使 $\left|f_{n}\right|\le g$ 对所有 $n$ 成立, 且 $f_{n}\to f$ 几乎处处, 则 $f$ 可积且 $\int f\,\mathrm{d}\mu=\lim_{n\to\infty}\int f_{n}\,\mathrm{d}\mu$.

> **定理 8.2.16**<br>如果 $f\in L^{1}\left(\mu\right)$ 且 $\epsilon>0$, 则存在可积简单函数 $\varphi=\sum a_{j}\chi_{E_{j}}$ 使得 $\int\left|f-\varphi\right|\mathrm{d}\mu<\epsilon$ (即可积简单函数在 $L^{1}$ 度量下稠密).

> **定理 10.2.1** (富比尼定理)<br>设 $\left(X,\mathcal A,\mu\right)$ 和 $\left(Y,\mathcal B,\nu\right)$ 是 σ-有限的测度空间, $f:X\times Y\to\mathbb R$ 是 $\mathcal A\otimes\mathcal B$-可测函数. 若 $f$ 在 $X\times Y$ 上可积, 则对几乎所有 $x$, $y\mapsto f\left(x,y\right)$ 是 ν-可积的; 对几乎所有 $y$, $x\mapsto f\left(x,y\right)$ 是 μ-可积的; 且重积分相等: $$\begin{aligned}&\quad\;\int_{X\times Y}f\,\mathrm{d}\left(\mu\times\nu\right)\\&=\int_{X}\left(\int_{Y}f\left(x,y\right)\mathrm{d}\nu\left(y\right)\right)\mathrm{d}\mu\left(x\right)\\&=\int_{Y}\left(\int_{X}f\left(x,y\right)\mathrm{d}\mu\left(x\right)\right)\mathrm{d}\nu\left(y\right).\end{aligned}$$

> **定理 10.2.2** (托内利定理)<br>如果 $f:X\times Y\to\left[0,\infty\right]$ 是 $\mathcal A\otimes\mathcal B$-可测的, 则 $$\begin{aligned}&\quad\;\int_{X\times Y}f\,\mathrm{d}\left(\mu\times\nu\right)\\&=\int_{X}\left(\int_{Y}f\left(x,y\right)\mathrm{d}\nu\left(y\right)\right)\mathrm{d}\mu\left(x\right)\\&=\int_{Y}\left(\int_{X}f\left(x,y\right)\mathrm{d}\mu\left(x\right)\right)\mathrm{d}\nu\left(y\right).\end{aligned}$$<br>其中所有积分值都在 $\left[0,\infty\right]$ 中.

> **定理 11.1.1**<br>假设 $E\in\mathcal L^{n}$.<br>(a) $$\begin{aligned}&\quad\;m\left(E\right)\\&=\inf\left\{m\left(U\right):U\supset E,U\text{开}\right\}\\&=\sup\left\{m\left(K\right):K\subset E,K\text{紧}\right\}\end{aligned}$$;<br>(b) 若 $m\left(E\right)<\infty$, 则对任意 $\epsilon>0$, 存在有限个边为区间的互不相交的矩形族 $\left\{R_{j}\right\}_{j=1}^{N}$, 使得 $m\left(E\triangle\bigcup_{j=1}^{N}R_{j}\right)<\epsilon$.

> **定理 11.4.1**<br>存在 $S^{n-1}$ 上唯一的博雷尔测度 $\sigma=\sigma_{n-1}$, 使得 $m^{*}=\rho\times\sigma$. 若 $f$ 是 $\mathbb R^{n}$ 上的博雷尔可测函数, 且 $f\ge0$ 或 $f\in L^{1}\left(m\right)$, 则 $$\int_{\mathbb R^{n}}f\left(x\right)\mathrm{d}x=\int_{0}^{\infty}\int_{S^{n-1}}f\left(rx'\right)r^{n-1}\mathrm{d}\sigma\left(x'\right)\mathrm{d}r.$$

> **基础知识**<br>**一维平移与伸缩的不变性**: 对 $c\in\mathbb R$ 与 $\lambda\ne0$, 勒贝格测度满足 $m\left(E+c\right)=m\left(E\right)$ 与 $m\left(\lambda E\right)=\left|\lambda\right|m\left(E\right)$.

> **基础知识**<br>**可逆线性变换保持可测性与零测集**: 若 $T\in GL\left(n,\mathbb R\right)$, 则 $T\left(E\right)\in\mathcal L^{n}$ 当且仅当 $E\in\mathcal L^{n}$, 且 $T$ 保持零测集.

> **基础知识**<br>**正交变换保持勒贝格测度**: 若 $R\in O\left(n\right)$, 即 $R^{T}R=I$, 则 $\left|\det R\right|=1$, 且对任意 $E\in\mathcal L^{n}$ 有 $m\left(R\left(E\right)\right)=m\left(E\right)$.

> **基础知识**<br>**伽马函数与贝塔恒等式**: 伽马函数 $\Gamma\left(x\right)=\int_{0}^{\infty}t^{x-1}e^{-t}\mathrm{d}t$ 满足递推 $\Gamma\left(x+1\right)=x\Gamma\left(x\right)$; 贝塔函数满足恒等式 $\frac{\Gamma\left(x\right)\Gamma\left(y\right)}{\Gamma\left(x+y\right)}=\int_{0}^{1}t^{x-1}\left(1-t\right)^{y-1}\mathrm{d}t$ 对 $x,y>0$.

> **基础知识**<br>**特征函数的连续逼近**: 若 $R\subset\mathbb R^{n}$ 是有界闭矩形, 则对任意 $\epsilon>0$, 存在具有紧支撑的连续函数 $g$ 使得 $\int\left|\chi_{R}-g\right|\mathrm{d}m<\epsilon$.

> **基础知识**<br>**测度在乘积 σ-代数生成族上的唯一性**: 两个 σ-有限的测度若在某个生成乘积 σ-代数的矩形容许族上取值相等, 则在整个乘积 σ-代数上相等.

### 习题一

证明讲义定理 11.1.2: 若 $f\in L^{1}\left(m\right)$ 且 $\epsilon>0$, 则存在一个简单函数 $\varphi=\sum a_{j}\chi_{R_{j}}$, 其中每个 $R_{j}$ 是区间之积, 使得 $\int\left|f-\varphi\right|<\epsilon$; 且存在一个在有界集外为零的连续函数 $g$, 使得 $\int\left|f-g\right|<\epsilon$.

### 解答 习题一

**简单函数部分.** 由**定理 8.2.16**, 存在可积简单函数 $\varphi=\sum_{j}a_{j}\chi_{E_{j}}$ 使得 $\int\left|f-\varphi\right|<\epsilon/2$. 对 $a_{j}\ne0$ 的项, 由 $\int a_{j}\chi_{E_{j}}\,\mathrm{d}m=a_{j}m\left(E_{j}\right)<\infty$ 得 $m\left(E_{j}\right)<\infty$ (否则积分发散, 与可积性矛盾). 由**定理 11.1.1** (b), 对每个这样的 $E_{j}$ 存在有限个边为区间的互不相交矩形 $\left\{R_{j,k}\right\}$ 使 $m\left(E_{j}\triangle\bigcup_{k}R_{j,k}\right)$ 任意小. 于是 $\chi_{E_{j}}$ 与 $\chi_{R_{j}}$ (其中 $R_{j}=\bigcup_{k}R_{j,k}$) 在 $L^{1}$ 中任意接近, 取足够小的逼近误差并合并所有 $j$, 得到简单函数 $\varphi'=\sum_{j}a_{j}\chi_{R_{j}}$ (每个 $R_{j}$ 是边为区间的矩形之有限并, 且各 $R_{j}$ 可整理为区间之积的互不相交矩形) 满足 $\int\left|\varphi-\varphi'\right|<\epsilon/2$. 故 $\int\left|f-\varphi'\right|\le\int\left|f-\varphi\right|+\int\left|\varphi-\varphi'\right|<\epsilon$. $\blacksquare$

**连续函数部分.** 设 $\varphi'=\sum_{j}a_{j}\chi_{R_{j}}$ 已由上一步得到, 其中每个 $R_{j}$ 是有界闭矩形. 由基础知识 (特征函数的连续逼近), 对每个 $R_{j}$ 存在具有紧支撑的连续函数 $g_{j}$ 使 $\int\left|\chi_{R_{j}}-g_{j}\right|\mathrm{d}m$ 任意小. 取逼近误差足够小并令 $g=\sum_{j}a_{j}g_{j}$, 则 $g$ 连续且支撑在 $\bigcup_{j}R_{j}$ 中 (有界集), 且 $\int\left|\varphi'-g\right|\le\sum_{j}\left|a_{j}\right|\int\left|\chi_{R_{j}}-g_{j}\right|<\epsilon/2$. 于是

$$
\int\left|f-g\right|\le\int\left|f-\varphi'\right|+\int\left|\varphi'-g\right|<\epsilon.
$$

$g$ 在有界集外为零. $\blacksquare$

### 习题二

证明讲义定理 11.3.1 (线性变量替换公式). 假设 $T\in GL\left(n,\mathbb R\right)$.

(a) 如果 $f$ 是 $\mathbb R^{n}$ 上的勒贝格可测函数, 则 $f\circ T$ 也是. 如果 $f\ge0$ 或 $f\in L^{1}\left(m\right)$, 那么

$$
\int f\left(x\right)\mathrm{d}x=\left|\det T\right|\int f\circ T\left(x\right)\mathrm{d}x.
$$

(b) 如果 $E\in\mathcal L^{n}$, 则 $T\left(E\right)\in\mathcal L^{n}$ 且 $m\left(T\left(E\right)\right)=\left|\det T\right|m\left(E\right)$.

### 解答 习题二

先证三种初等变换的情形, 再组合.

**伸缩变换** $T_{1}\left(x_{1},\dots,x_{j},\dots,x_{n}\right)=\left(x_{1},\dots,cx_{j},\dots,x_{n}\right)$ ($c\ne0$). 由基础知识 (一维伸缩的不变性) 并结合乘积结构, 逐坐标伸缩保持其余坐标不动, 有 $m\left(T_{1}\left(E\right)\right)=\left|c\right|m\left(E\right)$ 且 $\int f\circ T_{1}\left(x\right)\mathrm{d}x=\frac{1}{\left|c\right|}\int f\left(x\right)\mathrm{d}x$, 即 $\int f\left(x\right)\mathrm{d}x=\left|c\right|\int f\circ T_{1}\left(x\right)\mathrm{d}x=\left|\det T_{1}\right|\int f\circ T_{1}\left(x\right)\mathrm{d}x$.

**剪切变换** $T_{2}\left(x_{1},\dots,x_{j},\dots,x_{n}\right)=\left(x_{1},\dots,x_{j}+cx_{k},\dots,x_{n}\right)$ ($k\ne j$). 由基础知识 (一维平移的不变性) 逐切片应用, $m\left(T_{2}\left(E\right)\right)=m\left(E\right)$ 且 $\int f\circ T_{2}\left(x\right)\mathrm{d}x=\int f\left(x\right)\mathrm{d}x$. 因 $\det T_{2}=1$, 公式成立.

**交换变换** $T_{3}$ 交换两个坐标, $\det T_{3}=-1$. 由 $m$ 作为乘积测度的对称性, $m\left(T_{3}\left(E\right)\right)=m\left(E\right)$ 且 $\int f\circ T_{3}\left(x\right)\mathrm{d}x=\int f\left(x\right)\mathrm{d}x$, 而 $\left|\det T_{3}\right|=1$, 公式成立.

**一般情形.** 由初等线性代数, 每个 $T\in GL\left(n,\mathbb R\right)$ 都可写成有限个上述三种初等变换的乘积 $T=T_{1}\circ\cdots\circ T_{k}$ (可逆矩阵可通过行变换化为单位矩阵). 对每个初等变换上式成立, 且行列式相乘 $\left|\det T\right|=\prod_{i}\left|\det T_{i}\right|$. 逐次代入得

$$
\begin{aligned}
&\quad\;\int f\left(x\right)\mathrm{d}x\\&=\left|\det T_{1}\right|\int f\circ T_{1}\left(x\right)\mathrm{d}x\\&=\cdots\\&=\left|\det T\right|\int f\circ T\left(x\right)\mathrm{d}x,
\end{aligned}
$$

此即 (a). 可测性: $T$ 连续, 由基础知识 (可逆线性变换保持可测性与零测集) 得 $f\circ T$ 可测且 $T\left(E\right)\in\mathcal L^{n}$.

**证 (b).** 在 (a) 中取 $f=\chi_{T\left(E\right)}$, 则

$$
\begin{aligned}
&\quad\;m\left(T\left(E\right)\right)\\&=\int\chi_{T\left(E\right)}\left(x\right)\mathrm{d}x\\&=\left|\det T\right|\int\chi_{T\left(E\right)}\circ T\left(x\right)\mathrm{d}x\\&=\left|\det T\right|\int\chi_{E}\left(x\right)\mathrm{d}x\\&=\left|\det T\right|m\left(E\right).
\end{aligned}
$$

$T\left(E\right)\in\mathcal L^{n}$ 已由可测性保证. $\blacksquare$

### 习题三

证明习题 55. 设 $E=\left[0,1\right]\times\left[0,1\right]$. 研究 $\int_{E}f\,\mathrm{d}m^{2}$, $\int_{0}^{1}\int_{0}^{1}f\left(x,y\right)\mathrm{d}x\,\mathrm{d}y$ 与 $\int_{0}^{1}\int_{0}^{1}f\left(x,y\right)\mathrm{d}y\,\mathrm{d}x$ 的存在性和相等性, 对下列 $f$.

a. $f\left(x,y\right)=\left(x^{2}-y^{2}\right)\left(x^{2}+y^{2}\right)^{-2}$;

b. $f\left(x,y\right)=\left(1-xy\right)^{-a}$ ($a>0$);

c. $f\left(x,y\right)=\left(x-y\right)^{-3}$, 若 $0<y<x<1$, 否则为 $0$.

### 解答 习题三

#### a

**$\int_{E}f\,\mathrm{d}m^{2}$ 不存在.** $\left|f\left(x,y\right)\right|=\frac{\left|x^{2}-y^{2}\right|}{\left(x^{2}+y^{2}\right)^{2}}\le\frac{x^{2}+y^{2}}{\left(x^{2}+y^{2}\right)^{2}}=\frac{1}{x^{2}+y^{2}}$. 在 $E$ 上 $\int_{E}\frac{1}{x^{2}+y^{2}}\mathrm{d}x\,\mathrm{d}y$ 发散 (用极坐标, $\int_{0}^{\delta}\int_{0}^{\pi/2}\frac{1}{r^{2}}r\,\mathrm{d}\theta\,\mathrm{d}r=\frac{\pi}{2}\int_{0}^{\delta}\frac{1}{r}\mathrm{d}r=\infty$), 故 $\int_{E}\left|f\right|=\infty$, $f\notin L^{1}$, $\int_{E}f\,\mathrm{d}m^{2}$ 无定义.

**$\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y$ (先对 $x$ 积分).** 固定 $y$, 令 $x=yt$, 则

$$
\int_{0}^{1}\frac{x^{2}-y^{2}}{\left(x^{2}+y^{2}\right)^{2}}\mathrm{d}x=\frac{1}{y}\int_{0}^{1/y}\frac{t^{2}-1}{\left(t^{2}+1\right)^{2}}\mathrm{d}t.
$$

因 $\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{t}{t^{2}+1}\right)=\frac{1-t^{2}}{\left(t^{2}+1\right)^{2}}$, 有 $\int\frac{t^{2}-1}{\left(t^{2}+1\right)^{2}}\mathrm{d}t=-\frac{t}{t^{2}+1}+C$, 故内层积分

$$
\begin{aligned}
&\quad\;=\frac{1}{y}\left[-\frac{t}{t^{2}+1}\right]_{0}^{1/y}\\&=-\frac{1}{y}\cdot\frac{1/y}{1+1/y^{2}}\\&=-\frac{1}{y^{2}+1}.
\end{aligned}
$$

于是 $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y=\int_{0}^{1}-\frac{1}{1+y^{2}}\mathrm{d}y=-\left[\arctan y\right]_{0}^{1}=-\frac{\pi}{4}$.

**$\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x$ (先对 $y$ 积分).** 对称地, 固定 $x$ 令 $y=xt$, 内层 $\int_{0}^{1}f\,\mathrm{d}y=\frac{1}{x^{2}+1}$, 故

$$
\begin{aligned}
&\quad\;\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x\\&=\int_{0}^{1}\frac{1}{1+x^{2}}\mathrm{d}x\\&=\left[\arctan x\right]_{0}^{1}\\&=\frac{\pi}{4}.
\end{aligned}
$$

**结论.** $\int_{E}f\,\mathrm{d}m^{2}$ 不存在 ($f$ 非绝对可积); $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y=-\frac{\pi}{4}$ 与 $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x=\frac{\pi}{4}$ 存在但不等, 且符号相反. 因 $f\notin L^{1}$, 定理 10.2.1 (富比尼) 不适用, 两个迭代积分不可交换. $\blacksquare$

#### b

$f\ge0$.

**$0<a\le1$ 时 $f$ 可积.** 固定 $y$, 内层 $\int_{0}^{1}\left(1-xy\right)^{-a}\mathrm{d}x=\frac{1}{y}\cdot\frac{1-\left(1-y\right)^{1-a}}{1-a}$ (当 $a\ne1$), 且 $a=1$ 时内层 $=-\frac{\ln\left(1-y\right)}{y}$. 对 $0<a<1$, 内层在 $y\to0$ 处趋于 $1$, 在 $y\to1$ 处趋于 $\frac{1}{1-a}$ (因 $\left(1-y\right)^{1-a}\to0$), 故有界, $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y<\infty$. 对 $a=1$, $\int_{0}^{1}-\frac{\ln\left(1-y\right)}{y}\mathrm{d}y=\sum_{k=1}^{\infty}\frac{1}{k^{2}}=\frac{\pi^{2}}{6}<\infty$. 故 $0<a\le1$ 时 $f\in L^{1}$, 由**定理 10.2.2** (托内利), 三个积分都存在且相等.

**$a>1$ 时 $f\notin L^{1}$.** 内层 $\frac{1}{y}\cdot\frac{1-\left(1-y\right)^{1-a}}{1-a}$, 因 $1-a<0$ 且 $y\to1$ 时 $\left(1-y\right)^{1-a}\to\infty$, 内层趋于 $+\infty$, 故 $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y=+\infty$; 对称地 $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x=+\infty$, 且 $\int_{E}f\,\mathrm{d}m^{2}=+\infty$.

**结论.** $0<a\le1$ 时三个积分存在且相等, $f\in L^{1}$; $a>1$ 时三个积分均为 $+\infty$ (作为非负函数的积分发散), $f\notin L^{1}$. $\blacksquare$

#### c

区域为 $\left\{\left(x,y\right):0<y<x<1\right\}$.

**$\int_{E}f\,\mathrm{d}m^{2}$ 不存在.** $\left|f\right|=\left(x-y\right)^{-3}$. 先对 $x$ 积分, $\int_{y}^{1}\left(x-y\right)^{-3}\mathrm{d}x=\left[-\frac{1}{2}\left(x-y\right)^{-2}\right]_{y}^{1}=+\infty$, 故 $\int_{E}\left|f\right|=\infty$, $f\notin L^{1}$, $\int_{E}f\,\mathrm{d}m^{2}$ 无定义.

**$\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y$ (先对 $x$ 积分).** 固定 $y$, $\int_{y}^{1}\left(x-y\right)^{-3}\mathrm{d}x=\left[-\frac{1}{2}\left(x-y\right)^{-2}\right]_{y}^{1}$, 因 $\lim_{x\to y^{+}}\left(x-y\right)^{-2}=\infty$, 故内层积分 $=+\infty$, 于是

$$
\begin{aligned}
&\quad\;\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y\\&=\int_{0}^{1}\left(\int_{y}^{1}\left(x-y\right)^{-3}\mathrm{d}x\right)\mathrm{d}y\\&=+\infty.
\end{aligned}
$$

**$\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x$ (先对 $y$ 积分).** 固定 $x$, $\int_{0}^{x}\left(x-y\right)^{-3}\mathrm{d}y=\left[-\frac{1}{2}\left(x-y\right)^{-2}\right]_{0}^{x}$, 因 $\lim_{y\to x^{-}}\left(x-y\right)^{-2}=\infty$, 故内层积分 $=-\infty$, 于是

$$
\begin{aligned}
&\quad\;\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x\\&=\int_{0}^{1}\left(\int_{0}^{x}\left(x-y\right)^{-3}\mathrm{d}y\right)\mathrm{d}x\\&=-\infty.
\end{aligned}
$$

**结论.** $\int_{E}f\,\mathrm{d}m^{2}$ 不存在 ($f\notin L^{1}$); $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y=+\infty$ 而 $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x=-\infty$, 两个迭代积分存在但不等且符号相反. 这是富比尼失效的经典反例: 非绝对可积时积分次序不可交换. $\blacksquare$

### 习题四

证明习题 56. 如果 $f$ 在 $\left(0,a\right)$ 上勒贝格可积, 且 $g\left(x\right)=\int_{x}^{a}t^{-1}f\left(t\right)\mathrm{d}t$, 则 $g$ 在 $\left(0,a\right)$ 上可积且 $\int_{0}^{a}g\left(x\right)\mathrm{d}x=\int_{0}^{a}f\left(x\right)\mathrm{d}x$.

### 解答 习题四

先在 $\left(0,a\right)\times\left(0,a\right)$ 上考虑二元函数 $h\left(x,t\right)=t^{-1}f\left(t\right)\chi_{\left\{x<t\right\}}\left(x,t\right)$ (即定义域 $\left\{\left(x,t\right):0<x<t<a\right\}$). 由**定理 10.2.2** (托内利, 非负函数 $\left|h\right|$),

$$
\begin{aligned}
&\quad\;\int_{0}^{a}\int_{x}^{a}t^{-1}\left|f\left(t\right)\right|\mathrm{d}t\,\mathrm{d}x\\&=\int_{0}^{a}\left(\int_{0}^{t}t^{-1}\left|f\left(t\right)\right|\mathrm{d}x\right)\mathrm{d}t\\&=\int_{0}^{a}t^{-1}\left|f\left(t\right)\right|\cdot t\,\mathrm{d}t\\&=\int_{0}^{a}\left|f\left(t\right)\right|\mathrm{d}t\\&<\infty,
\end{aligned}
$$

其中内层交换次序用**定理 10.2.2** 于非负函数. 故 $\left(x,t\right)\mapsto t^{-1}f\left(t\right)\chi_{\left\{x<t\right\}}$ 可积, 从而 $g$ 可积. 再由**定理 10.2.1** (富比尼) 交换次序,

$$
\begin{aligned}
&\quad\;\int_{0}^{a}g\left(x\right)\mathrm{d}x\\&=\int_{0}^{a}\int_{x}^{a}t^{-1}f\left(t\right)\mathrm{d}t\,\mathrm{d}x\\&=\int_{0}^{a}\left(\int_{0}^{t}t^{-1}f\left(t\right)\mathrm{d}x\right)\mathrm{d}t\\&=\int_{0}^{a}t^{-1}f\left(t\right)\cdot t\,\mathrm{d}t\\&=\int_{0}^{a}f\left(t\right)\mathrm{d}t.
\end{aligned}
$$

$\blacksquare$

### 习题五

证明习题 59. 设 $f\left(x\right)=x^{-1}\sin x$.

a. 证明 $\int_{0}^{\infty}\left|f\left(x\right)\right|\mathrm{d}x=\infty$.

b. 证明 $\lim_{b\to\infty}\int_{0}^{b}f\left(x\right)\mathrm{d}x=\frac{1}{2}\pi$, 通过积分 $e^{-xy}\sin x$ 关于 $x$ 和 $y$. (鉴于 (a), 取极限 $b\to\infty$ 时需要小心.)

### 解答 习题五

#### a

在区间 $\left[k\pi,\left(k+1\right)\pi\right]$ 上, $\left|\sin x\right|\ge0$ 且 $\int_{k\pi}^{\left(k+1\right)\pi}\left|\sin x\right|\mathrm{d}x=2$. 因 $\frac{1}{x}$ 在此区间上 $\ge\frac{1}{\left(k+1\right)\pi}$, 有

$$
\int_{k\pi}^{\left(k+1\right)\pi}\frac{\left|\sin x\right|}{x}\mathrm{d}x\ge\frac{2}{\left(k+1\right)\pi}.
$$

于是对任意 $N$,

$$
\int_{0}^{\left(N+1\right)\pi}\frac{\left|\sin x\right|}{x}\mathrm{d}x\ge\sum_{k=0}^{N}\frac{2}{\left(k+1\right)\pi}\to\infty
$$

(调和级数发散), 故 $\int_{0}^{\infty}\left|f\right|\mathrm{d}x=\infty$. $\blacksquare$

#### b

对固定的 $b>0$, 因 $\int_{0}^{b}\int_{0}^{\infty}\left|e^{-xy}\sin x\right|\mathrm{d}y\,\mathrm{d}x=\int_{0}^{b}\frac{\left|\sin x\right|}{x}\mathrm{d}x<\infty$ (固定 $b$ 时 $x^{-1}\sin x$ 可积), 由**定理 10.2.2** (托内利) 可交换次序:

$$
\begin{aligned}
&\quad\;\int_{0}^{b}\frac{\sin x}{x}\mathrm{d}x\\&=\int_{0}^{b}\int_{0}^{\infty}e^{-xy}\sin x\,\mathrm{d}y\,\mathrm{d}x\\&=\int_{0}^{\infty}\left(\int_{0}^{b}e^{-xy}\sin x\,\mathrm{d}x\right)\mathrm{d}y.
\end{aligned}
$$

对固定的 $y$, 分部积分两次得 $\int_{0}^{b}e^{-xy}\sin x\,\mathrm{d}x=\frac{1-e^{-by}\left(y\sin b+\cos b\right)}{1+y^{2}}$. 故

$$
\int_{0}^{b}\frac{\sin x}{x}\mathrm{d}x=\int_{0}^{\infty}\frac{1-e^{-by}\left(y\sin b+\cos b\right)}{1+y^{2}}\mathrm{d}y.
$$

**取极限 $b\to\infty$.** 拆成两项 $\frac{1}{1+y^{2}}-\frac{e^{-by}\left(y\sin b+\cos b\right)}{1+y^{2}}$. 第一项积分 $\int_{0}^{\infty}\frac{1}{1+y^{2}}\mathrm{d}y=\frac{\pi}{2}$. 对第二项, 当 $b\ge1$ 时 $\left|\frac{e^{-by}\left(y\sin b+\cos b\right)}{1+y^{2}}\right|\le\frac{e^{-y}\left(y+1\right)}{1+y^{2}}=:g\left(y\right)$, 且 $\int_{0}^{\infty}g\left(y\right)\mathrm{d}y<\infty$ (被 $e^{-y}$ 指数衰减控制). 由**定理 8.2.9** (控制收敛定理, 对任意序列 $b_{n}\to\infty$ 应用), 该项趋于 $\int_{0}^{\infty}0\,\mathrm{d}y=0$. 故

$$
\begin{aligned}
&\quad\;\lim_{b\to\infty}\int_{0}^{b}\frac{\sin x}{x}\mathrm{d}x\\&=\frac{\pi}{2}-0\\&=\frac{\pi}{2}.
\end{aligned}
$$

$\blacksquare$

### 习题六

证明习题 61. 若 $f$ 在 $\left[0,\infty\right)$ 上连续, 对 $\alpha>0$ 和 $x\ge0$, 令

$$
I_{\alpha}f\left(x\right)=\frac{1}{\Gamma\left(\alpha\right)}\int_{0}^{x}\left(x-t\right)^{\alpha-1}f\left(t\right)\mathrm{d}t,
$$

$I_{\alpha}f$ 称为 $f$ 的 $\alpha$ 阶分数阶积分.

a. $I_{\alpha+\beta}f=I_{\alpha}\left(I_{\beta}f\right)$ 对所有 $\alpha,\beta>0$ 成立. (用习题 60.)

b. 若 $n\in\mathbb N$, $I_{n}f$ 是 $f$ 的 $n$ 阶反导数.

### 解答 习题六

#### a

展开复合积分, 在区域 $\left\{\left(s,t\right):0<t<s<x\right\}$ 上交换次序:

$$
I_{\alpha}\left(I_{\beta}f\right)\left(x\right)=\frac{1}{\Gamma\left(\alpha\right)}\int_{0}^{x}\left(x-s\right)^{\alpha-1}\left[\frac{1}{\Gamma\left(\beta\right)}\int_{0}^{s}\left(s-t\right)^{\beta-1}f\left(t\right)\mathrm{d}t\right]\mathrm{d}s.
$$

因 $f$ 连续, 被积函数非负或可积, 由**定理 10.2.1** (富比尼) 交换次序得

$$
=\frac{1}{\Gamma\left(\alpha\right)\Gamma\left(\beta\right)}\int_{0}^{x}f\left(t\right)\left[\int_{t}^{x}\left(x-s\right)^{\alpha-1}\left(s-t\right)^{\beta-1}\mathrm{d}s\right]\mathrm{d}t.
$$

对内层积分, 令 $u=\frac{s-t}{x-t}$, 则 $s=t+u\left(x-t\right)$, $\mathrm{d}s=\left(x-t\right)\mathrm{d}u$, 得

$$
\int_{t}^{x}\left(x-s\right)^{\alpha-1}\left(s-t\right)^{\beta-1}\mathrm{d}s=\left(x-t\right)^{\alpha+\beta-1}\int_{0}^{1}\left(1-u\right)^{\alpha-1}u^{\beta-1}\mathrm{d}u.
$$

由基础知识 (伽马函数与贝塔恒等式), $\int_{0}^{1}\left(1-u\right)^{\alpha-1}u^{\beta-1}\mathrm{d}u=\frac{\Gamma\left(\alpha\right)\Gamma\left(\beta\right)}{\Gamma\left(\alpha+\beta\right)}$. 代入得

$$
\begin{aligned}
&\quad\;I_{\alpha}\left(I_{\beta}f\right)\left(x\right)\\&=\frac{1}{\Gamma\left(\alpha+\beta\right)}\int_{0}^{x}\left(x-t\right)^{\alpha+\beta-1}f\left(t\right)\mathrm{d}t\\&=I_{\alpha+\beta}f\left(x\right).
\end{aligned}
$$

$\blacksquare$

#### b

先看 $\alpha=1$: 因 $\Gamma\left(1\right)=1$,

$$
I_{1}f\left(x\right)=\int_{0}^{x}f\left(t\right)\mathrm{d}t,
$$

由微积分基本定理 $\frac{\mathrm{d}}{\mathrm{d}x}I_{1}f=f$. 由 (a), 迭代得 $I_{n}f=\underbrace{I_{1}\circ\cdots\circ I_{1}}_{n\text{次}}f$, 故 $\frac{\mathrm{d}^{n}}{\mathrm{d}x^{n}}I_{n}f=f$. 又因 $I_{\alpha}f$ 的积分下限为 $0$, 对 $k<n$ 有 $\left(\frac{\mathrm{d}}{\mathrm{d}x}\right)^{k}I_{n}f$ 在 $0$ 处取值为 $0$. 故 $I_{n}f$ 是 $f$ 的一个 $n$ 阶反导数. $\blacksquare$

### 习题七

证明习题 62. $S^{n-1}$ 上的测度 $\sigma$ 在旋转下不变.

### 解答 习题七

设 $R\in O\left(n\right)$, 即 $R^{T}R=I$, 则 $\left|\det R\right|=1$. 由基础知识 (正交变换保持勒贝格测度), $R$ 在 $\mathbb R^{n}$ 上保持 $m$. 由于 $R$ 保持范数 $\left|Rx\right|=\left|x\right|$, 它在球面坐标分解 $\Phi\left(x\right)=\left(r,x'\right)$ 下作用于球面部分: 存在球面 $S^{n-1}$ 上的旋转 $\rho$ 使 $R\left(rx'\right)=r\rho\left(x'\right)$. 记 $m^{*}$ 为极坐标诱导测度 ($m^{*}=\rho\times\sigma$ 由**定理 11.4.1**), 对博雷尔集 $A\subset\left(0,\infty\right)\times S^{n-1}$,

$$
\begin{aligned}
&\quad\;m^{*}\left(\left(\mathrm{id}\times\rho\right)\left(A\right)\right)\\&=m\left(\Phi^{-1}\left(\left(\mathrm{id}\times\rho\right)\left(A\right)\right)\right)\\&=m\left(R\Phi^{-1}\left(A\right)\right)\\&=m\left(\Phi^{-1}\left(A\right)\right)\\&=m^{*}\left(A\right),
\end{aligned}
$$

故 $m^{*}$ 旋转不变.

定义 $\sigma_{R}\left(E\right):=\sigma\left(R^{-1}E\right)=\sigma\left(R^{T}E\right)$, 它是 $S^{n-1}$ 上的博雷尔测度. 对矩形 $\left(a,b\right]\times E\subset\left(0,\infty\right)\times S^{n-1}$,

$$
\begin{aligned}
&\quad\;\left(\rho\times\sigma_{R}\right)\left(\left(a,b\right]\times E\right)\\&=\int_{a}^{b}r^{n-1}\mathrm{d}r\cdot\sigma_{R}\left(E\right)\\&=\rho\left(\left(a,b\right]\right)\cdot\sigma\left(R^{-1}E\right).
\end{aligned}
$$

由 $m^{*}=\rho\times\sigma$ (**定理 11.4.1**), $\rho\left(\left(a,b\right]\right)\cdot\sigma\left(R^{-1}E\right)=m^{*}\left(\left(a,b\right]\times R^{-1}E\right)$. 又由 $m^{*}$ 的旋转不变性, $m^{*}\left(\left(a,b\right]\times R^{-1}E\right)=m^{*}\left(\left(a,b\right]\times E\right)=\rho\left(\left(a,b\right]\right)\cdot\sigma\left(E\right)$. 故在矩形上 $\rho\times\sigma_{R}=\rho\times\sigma$. 由基础知识 (测度在乘积 σ-代数生成族上的唯一性), $\rho\times\sigma_{R}=\rho\times\sigma$ 在 $\left(0,\infty\right)\times S^{n-1}$ 上成立.

最后由**定理 11.4.1** 的唯一性 (使 $m^{*}=\rho\times\sigma$ 的测度 $\sigma$ 唯一), 从 $\rho\times\sigma_{R}=m^{*}=\rho\times\sigma$ 得 $\sigma_{R}=\sigma$, 即 $\sigma\left(R^{-1}E\right)=\sigma\left(E\right)$ 对一切博雷尔 $E$ 成立. 故 $\sigma$ 旋转不变. $\blacksquare$

### 习题八

证明习题 64. 对哪些实值 $a$ 和 $b$, $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ 在集合 $\left\{x\in\mathbb R^{n}:\left|x\right|<1/2\right\}$ 上可积? 在集合 $\left\{x\in\mathbb R^{n}:\left|x\right|>2\right\}$ 上可积?

### 解答 习题八

函数 $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ 是径向的, 由**定理 11.4.1** (极坐标分解), $\int_{\mathbb R^{n}}\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}\mathrm{d}x=\sigma\left(S^{n-1}\right)\int_{0}^{\infty}r^{a+n-1}\left|\log r\right|^{b}\mathrm{d}r$.

**集合 $\left\{\left|x\right|<1/2\right\}$.** 作代换 $u=-\log r$ (即 $r=e^{-u}$, $\mathrm{d}r=-e^{-u}\mathrm{d}u$, 则 $r\in\left(0,1/2\right]$ 对应 $u\in\left[\log 2,\infty\right)$):

$$
\begin{aligned}
&\quad\;\int_{0}^{1/2}r^{a+n-1}\left|\log r\right|^{b}\mathrm{d}r\\&=\int_{\log 2}^{\infty}e^{-u\left(a+n-1\right)}e^{-u}u^{b}\mathrm{d}u\\&=\int_{\log 2}^{\infty}e^{-u\left(a+n\right)}u^{b}\mathrm{d}u.
\end{aligned}
$$

收敛条件由指数因子决定:

$$
\int_{\log 2}^{\infty}e^{-u\left(a+n\right)}u^{b}\mathrm{d}u\text{收敛}\iff\begin{cases}a+n>0,&\text{指数衰减, 任意 }b,\\a+n=0\text{且}b<-1,&\int u^{b}\mathrm{d}u\text{收敛},\\a+n<0,&\text{指数增长, 发散}.\end{cases}
$$

故 $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ 在 $\left\{\left|x\right|<1/2\right\}$ 上可积 $\iff a>-n$, 或 $a=-n$ 且 $b<-1$.

**集合 $\left\{\left|x\right|>2\right\}$.** 当 $r\ge2$ 时 $\left|\log r\right|=\log r$. 作代换 $r=e^{u}$ ($\mathrm{d}r=e^{u}\mathrm{d}u$, $u\ge\log 2$):

$$
\begin{aligned}
&\quad\;\int_{2}^{\infty}r^{a+n-1}\left(\log r\right)^{b}\mathrm{d}r\\&=\int_{\log 2}^{\infty}e^{u\left(a+n-1\right)}e^{u}u^{b}\mathrm{d}u\\&=\int_{\log 2}^{\infty}e^{u\left(a+n\right)}u^{b}\mathrm{d}u.
\end{aligned}
$$

收敛条件:

$$
\int_{\log 2}^{\infty}e^{u\left(a+n\right)}u^{b}\mathrm{d}u\text{收敛}\iff a+n<0
$$

(指数衰减; $a+n>0$ 时指数增长发散, $a+n=0$ 时 $\int u^{b}\mathrm{d}u$ 发散对任意 $b$). 故 $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ 在 $\left\{\left|x\right|>2\right\}$ 上可积 $\iff a<-n$.

**结论.** 在 $\left\{\left|x\right|<1/2\right\}$ 上可积 $\iff a>-n$ 或 $\left(a=-n\text{且}b<-1\right)$; 在 $\left\{\left|x\right|>2\right\}$ 上可积 $\iff a<-n$. $\blacksquare$
