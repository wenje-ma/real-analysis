# 作业 11

> **定义 14.0.6** (有界变差函数)<br>设 $f:\left[a,b\right]\to\mathbb R$. 对 $\left[a,b\right]$ 的任意分划 $P:a=x_{0}<x_{1}<\cdots<x_{n}=b$, 定义变差 $V\left(f,P\right)=\sum_{i=1}^{n}\left|f\left(x_{i}\right)-f\left(x_{i-1}\right)\right|$. $f$ 在 $\left[a,b\right]$ 上的全变差为 $V_{a}^{b}\left(f\right)=\sup_{P}V\left(f,P\right)$. 若 $V_{a}^{b}\left(f\right)<+\infty$, 则称 $f$ 为 $\left[a,b\right]$ 上的有界变差函数, 记作 $f\in BV\left(\left[a,b\right]\right)$.

> **定理 14.0.7** (基本性质)<br>设 $f,g\in BV\left(\left[a,b\right]\right)$, 则:<br>(1) $BV\left(\left[a,b\right]\right)$ 构成一个线性空间;<br>(2) $f$ 为有界函数;<br>(3) 若 $f$ 满足 利普希茨条件, 则 $f\in BV\left(\left[a,b\right]\right)$;<br>(4) 单调函数必为有界变差函数.

> **定理 14.0.10** (间断点性质)<br>若 $f\in BV\left(\left[a,b\right]\right)$, 则:<br>(1) $f$ 的不连续点至多可数;<br>(2) 所有不连续点都是第一类间断点.

> **基础知识** (归一化的有界变差 $NBV$)<br>$NBV=\left\{F\in BV:F\text{右连续},F\left(-\infty\right)=0\right\}$, 其中 $BV$ 指 $\mathbb R$ 上的有界变差函数, $T_{F}$ 表示 $F$ 的全变差函数.

> **基础知识** (级数)<br>几何级数 $\sum_{n=1}^{\infty}2^{-n}=1$ 收敛; 调和级数 $\sum_{k}\frac{1}{k}$ 发散.

### 习题一

**30.** 构造一个 $\mathbb R$ 上的递增函数, 使其间断点集恰为 $\mathbb Q$.

**31.** 设 $F\left(x\right)=x^{2}\sin\left(x^{-1}\right)$, $G\left(x\right)=x^{2}\sin\left(x^{-2}\right)$ 对 $x\ne0$, 且 $F\left(0\right)=G\left(0\right)=0$.
a. $F$ 与 $G$ 处处可微 (包括 $x=0$);
b. $F\in BV\left(\left[-1,1\right]\right)$, 但 $G\notin BV\left(\left[-1,1\right]\right)$.

**32.** 若 $F_{1},F_{2},\dots,F\in NBV$ 且 $F_{j}\to F$ 逐点收敛, 则 $T_{F}\le\liminf_{j\to\infty}T_{F_{j}}$.

### 解答 习题一

#### 30

枚举有理数 $\mathbb Q=\left\{q_{1},q_{2},\dots\right\}$, 定义

$$
F\left(x\right)=\sum_{q_{n}\le x}2^{-n},\quad x\in\mathbb R.
$$

这是至多可数项之和且每项非负, 值域含于 $\left[0,1\right]$. 由**基础知识** (级数), $\sum_{n}2^{-n}$ 收敛, 故 $F$ 取值有限. 若 $x<y$, 则 $\left\{n:q_{n}\le x\right\}\subset\left\{n:q_{n}\le y\right\}$, 从而 $F\left(x\right)\le F\left(y\right)$, 即 $F$ 递增.

**每个有理点是间断点.** 对 $q_{k}\in\mathbb Q$, 当 $x$ 自 $q_{k}$ 左侧趋于 $q_{k}$ 时, $\left\{q_{n}\le x\right\}$ 不含 $q_{k}$ (也趋于不含 $q_{k}$), 故左极限

$$
\begin{aligned}
&\quad\;F\left(q_{k}-\right)\\&=\sum_{q_{n}<q_{k}}2^{-n}\\&=\sum_{q_{n}\le q_{k}}2^{-n}-2^{-k}\\&=F\left(q_{k}\right)-2^{-k}\\&<F\left(q_{k}\right).
\end{aligned}
$$

而右极限 $F\left(q_{k}+\right)=\lim_{x\downarrow q_{k}}F\left(x\right)=F\left(q_{k}\right)$ (因 $x>q_{k}$ 时仍计入 $q_{k}$). 故 $F$ 在 $q_{k}$ 处左、右极限不相等, 是第一类间断点.

**每个无理点是连续点.** 设 $x_{0}\in\mathbb R\setminus\mathbb Q$. 给定 $\varepsilon>0$, 由**基础知识** (级数) 取 $N$ 使 $\sum_{n>N}2^{-n}<\varepsilon$. 因 $x_{0}$ 无理, 取 $\delta>0$ 小到开区间 $\left(x_{0}-\delta,x_{0}+\delta\right)$ 内不含 $q_{1},\dots,q_{N}$ (有限个点, 可分离). 则当 $\left|x-x_{0}\right|<\delta$ 时, 区间 $\left(\min\left(x,x_{0}\right),\max\left(x,x_{0}\right)\right]$ 内至多含 $q_{N+1},q_{N+2},\dots$, 故

$$
\begin{aligned}
&\quad\;\left|F\left(x\right)-F\left(x_{0}\right)\right|\\
&=\sum_{x_{0}<q_{n}\le x\text{ 或 }x<q_{n}\le x_{0}}2^{-n}\\&\le\sum_{n>N}2^{-n}<\varepsilon.
\end{aligned}
$$

故 $F$ 在 $x_{0}$ 连续.

综上, $F$ 的间断点集恰为 $\mathbb Q$. 由**定理 14.0.7**(4) 及**定理 14.0.10**, $F$ 为递增有界函数从而是有界变差函数, 其间断点至多可数且均为第一类, 此处恰与 $\mathbb Q$ 相符. $\blacksquare$

#### 31

**(a)** 对 $x\ne0$, 直接求导得

$$
\begin{aligned}
F'\left(x\right)&=2x\sin\left(x^{-1}\right)-\cos\left(x^{-1}\right),\\G'\left(x\right)&=2x\sin\left(x^{-2}\right)-\frac{2}{x}\cos\left(x^{-2}\right).
\end{aligned}
$$

在 $x=0$ 处, 用定义判别:

$$
\begin{aligned}
&\quad\;F'\left(0\right)\\&=\lim_{h\to0}\frac{F\left(h\right)-F\left(0\right)}{h}\\&=\lim_{h\to0}\frac{h^{2}\sin\left(h^{-1}\right)}{h}\\&=\lim_{h\to0}h\sin\left(h^{-1}\right)\\&=0,
\end{aligned}
$$

其中最后一个等式由 $\left|h\sin\left(h^{-1}\right)\right|\le\left|h\right|\to0$ 得; 同理

$$
\begin{aligned}
&\quad\;G'\left(0\right)\\&=\lim_{h\to0}\frac{h^{2}\sin\left(h^{-2}\right)}{h}\\&=\lim_{h\to0}h\sin\left(h^{-2}\right)\\&=0.
\end{aligned}
$$

故 $F,G$ 在 $\mathbb R$ 上处处可微 (含 $x=0$). $\blacksquare$

**(b)** 先证 $F\in BV\left(\left[-1,1\right]\right)$. 由 (a), 对 $x\ne0$, $\left|F'\left(x\right)\right|=\left|2x\sin\left(x^{-1}\right)-\cos\left(x^{-1}\right)\right|\le2\left|x\right|+1\le3$. 故 $F'$ 在 $\left[-1,1\right]$ 上有界. 由中值定理, $\left|F\left(x\right)-F\left(y\right)\right|\le3\left|x-y\right|$, 即 $F$ 满足 利普希茨条件, 由**定理 14.0.7**(3), $F\in BV\left(\left[-1,1\right]\right)$.

再证 $G\notin BV\left(\left[-1,1\right]\right)$. 取 $x_{k}=\frac{1}{\sqrt{\pi/2+k\pi}}$ ($k=0,1,2,\dots$), 则 $x_{k}\downarrow0$, 且 $\sin\left(x_{k}^{-2}\right)=\sin\left(\pi/2+k\pi\right)=\left(-1\right)^{k}$, 故 $G\left(x_{k}\right)=\left(-1\right)^{k}x_{k}^{2}$. 对分划 $0<x_{N}<\cdots<x_{0}$ (以及端点 $0$), 由交替符号,

$$
\begin{aligned}
&\quad\;\sum_{k=0}^{N-1}\left|G\left(x_{k}\right)-G\left(x_{k+1}\right)\right|\\&=\sum_{k=0}^{N-1}\left(x_{k}^{2}+x_{k+1}^{2}\right)\\&\ge\sum_{k=0}^{N-1}x_{k}^{2}\\&=\sum_{k=0}^{N-1}\frac{1}{\pi/2+k\pi}.
\end{aligned}
$$

由**基础知识** (级数), 调和级数 $\sum_{k}\frac{1}{k}$ 发散, 故上式随 $N\to\infty$ 趋于 $+\infty$. 于是 $G$ 在 $\left[0,1\right]\subset\left[-1,1\right]$ 上的全变差已为 $+\infty$, 从而 $V_{-1}^{1}\left(G\right)=+\infty$, 即 $G\notin BV\left(\left[-1,1\right]\right)$. $\blacksquare$

#### 32

固定 $x\in\mathbb R$ 与一个分划 $a=t_{0}<\cdots<t_{n}=x$ (取 $-\infty<a$). 因 $F_{j}\to F$ 逐点, 由有限项极限可交换 (求和为有限和),

$$
\begin{aligned}
&\quad\;\sum_{k=1}^{n}\left|F\left(t_{k}\right)-F\left(t_{k-1}\right)\right|\\&=\lim_{j\to\infty}\sum_{k=1}^{n}\left|F_{j}\left(t_{k}\right)-F_{j}\left(t_{k-1}\right)\right|\\&=\liminf_{j\to\infty}\sum_{k=1}^{n}\left|F_{j}\left(t_{k}\right)-F_{j}\left(t_{k-1}\right)\right|\\&\le\liminf_{j\to\infty}T_{F_{j}}\left(x\right),
\end{aligned}
$$

其中最后一个不等式由**定义 14.0.6** (每个分划的和不超过全变差 $T_{F_{j}}\left(x\right)$, 且 $\liminf$ 保持不等式) 得. 对全体分划取上确界,

$$
\begin{aligned}
&\quad\;T_{F}\left(x\right)\\&=\sup_{P}\sum_{k=1}^{n}\left|F\left(t_{k}\right)-F\left(t_{k-1}\right)\right|\\&\le\liminf_{j\to\infty}T_{F_{j}}\left(x\right).
\end{aligned}
$$

故 $T_{F}\le\liminf_{j\to\infty}T_{F_{j}}$. $\blacksquare$
