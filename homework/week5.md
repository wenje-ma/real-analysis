# 作业 5

> **定义 5.1.2** (测度)<br>设 $\left(X,\mathcal F\right)$ 是一个可测空间. 函数 $\mu:\mathcal F\to\left[0,+\infty\right]$ 称为 $\left(X,\mathcal F\right)$ 上的一个测度, 如果满足:<br>(1) 非负性: $\mu\left(E\right)\ge0$ 对一切 $E\in\mathcal F$ 成立;<br>(2) 零空集性: $\mu\left(\emptyset\right)=0$;<br>(3) 可数可加性 (σ-可加性): 对任意可数个两两不交的集合 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$, 有 $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **定义 5.1.5** (σ-有限测度)<br>设 $\left(X,\mathcal F,\mu\right)$ 是测度空间. 如果存在一列可测集 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$ 使得 $X=\bigcup_{n=1}^{\infty}E_{n}$ 且 $\mu\left(E_{n}\right)<+\infty$ 对所有 $n\in\mathbb N$ 成立, 则称 $\mu$ 为 σ-有限测度.

> **定义 8.1.1** (非负简单函数的积分)<br>设 $f=\sum_{i=1}^{n}c_{i}\chi_{A_{i}}$ 是非负简单函数, 其中 $c_{i}\ge0$, $A_{i}\in\mathcal F$ 互不相交且 $\bigcup_{i}A_{i}=X$. 定义 $f$ 关于 $\mu$ 的积分为 $\int_{X}f\,\mathrm{d}\mu=\sum_{i=1}^{n}c_{i}\mu\left(A_{i}\right)$, 并约定 $0\cdot\infty=0$.

> **命题 8.1.2** (线性性)<br>设 $f,g$ 为非负简单函数, $\alpha,\beta\ge0$, 则 $\int_{X}\left(\alpha f+\beta g\right)\mathrm{d}\mu=\alpha\int_{X}f\,\mathrm{d}\mu+\beta\int_{X}g\,\mathrm{d}\mu$.

> **定义 8.2.1** (非负可测函数的积分)<br>设 $f:X\to\left[0,+\infty\right]$ 是非负可测函数. 定义 $f$ 关于 $\mu$ 的积分为 $\int_{X}f\,\mathrm{d}\mu=\sup\left\{\int_{X}\phi\,\mathrm{d}\mu:\phi\text{是简单函数},0\le\phi\le f\right\}$. 若 $\int_{X}f\,\mathrm{d}\mu<\infty$, 则称 $f$ 是可积的.

> **定理 8.2.2** (单调收敛定理)<br>设 $\left(X,\mathcal F,\mu\right)$ 是测度空间, $\left\{f_{n}\right\}$ 是一列非负可测函数, 满足 $0\le f_{1}\left(x\right)\le f_{2}\left(x\right)\le\cdots$ 对所有 $x\in X$ 成立, 且 $f_{n}\to f$ 点点收敛. 则 $\lim_{n\to\infty}\int_{X}f_{n}\,\mathrm{d}\mu=\int_{X}f\,\mathrm{d}\mu$.

> **注 8.2.3**<br>单调收敛定理告诉我们积分可以用简单函数逼近.

> **命题 8.2.4** (绝对连续性)<br>设 $f$ 为非负可测函数, 则 $A\mapsto\int_{A}f\,\mathrm{d}\mu$ 为一个测度; 若 $\mu\left(A\right)=0$, 则 $\int_{A}f\,\mathrm{d}\mu=0$.

> **定义 8.2.5** (一般可测函数的积分)<br>设 $f:X\to\left[-\infty,+\infty\right]$ 是可测函数. 定义 $f$ 的正部和负部分别为 $f^{+}\left(x\right)=\max\left\{f\left(x\right),0\right\}$, $f^{-}\left(x\right)=\max\left\{-f\left(x\right),0\right\}$. 若至少有一个积分 $\int_{X}f^{+}\mathrm{d}\mu$, $\int_{X}f^{-}\mathrm{d}\mu$ 有限, 则定义 $f$ 的积分为 $\int_{X}f\,\mathrm{d}\mu=\int_{X}f^{+}\mathrm{d}\mu-\int_{X}f^{-}\mathrm{d}\mu$. 若 $\int_{X}f^{+}\mathrm{d}\mu<\infty$ 且 $\int_{X}f^{-}\mathrm{d}\mu<\infty$, 则称 $f$ 是可积的.

> **定理 8.2.7** (法图引理)<br>设 $\left(X,\mathcal F,\mu\right)$ 是测度空间, $\left\{f_{n}\right\}$ 是一列非负可测函数, 则 $\int_{X}\liminf_{n\to\infty}f_{n}\,\mathrm{d}\mu\le\liminf_{n\to\infty}\int_{X}f_{n}\,\mathrm{d}\mu$.

> **定理 8.2.9** (控制收敛定理)<br>设 $\left(X,\mathcal F,\mu\right)$ 是测度空间, $\left\{f_{n}\right\}$ 是一列可测函数, $f_{n}\to f$ 几乎处处. 如果存在可积函数 $g$ 使得对所有 $n$ 有 $\left|f_{n}\right|\le g$ 几乎处处, 则 $\lim_{n\to\infty}\int_{X}f_{n}\,\mathrm{d}\mu=\int_{X}f\,\mathrm{d}\mu$.

> **引理 8.2.13** (级数逐项积分)<br>设 $\left\{f_{n}\right\}$ 是一列可测函数, 且 $\sum_{n=1}^{\infty}\int_{X}\left|f_{n}\right|\mathrm{d}\mu<\infty$, 则 $\int_{X}\left(\sum_{n=1}^{\infty}f_{n}\right)\mathrm{d}\mu=\sum_{n=1}^{\infty}\int_{X}f_{n}\,\mathrm{d}\mu$.

> **定理 8.2.17** (参数积分)<br>设 $f:X\times\left[a,b\right]\to\mathbb R$, 且对每个 $t\in\left[a,b\right]$, 函数 $f\left(\cdot,t\right):X\to\mathbb R$ 可积. 令 $F\left(t\right)=\int_{X}f\left(x,t\right)\mathrm{d}\mu\left(x\right)$.<br>(a) 若存在 $g\in L^{1}\left(\mu\right)$ 使得对所有 $x,t$ 有 $\left|f\left(x,t\right)\right|\le g\left(x\right)$, 且对每个 $x$ 有 $\lim_{t\to t_{0}}f\left(x,t\right)=f\left(x,t_{0}\right)$, 则 $\lim_{t\to t_{0}}F\left(t\right)=F\left(t_{0}\right)$;<br>(b) 若偏导数 $\partial f/\partial t$ 存在, 且存在 $g\in L^{1}\left(\mu\right)$ 使得对所有 $x,t$ 有 $\left|\frac{\partial f}{\partial t}\left(x,t\right)\right|\le g\left(x\right)$, 则 $F$ 可微, 且 $F'\left(t\right)=\int\frac{\partial f}{\partial t}\left(x,t\right)\mathrm{d}\mu\left(x\right)$.

> **基础知识**<br>**非负可积函数积分为零则几乎处处为零**: 设 $h\ge0$ 可测且 $\int_{X}h\,\mathrm{d}\mu=0$, 则 $h=0$ 几乎处处. 事实上 $\left\{h>0\right\}=\bigcup_{n=1}^{\infty}\left\{h>\frac{1}{n}\right\}$, 且 $\int h\ge\frac{1}{n}\mu\left(\left\{h>\frac{1}{n}\right\}\right)$, 故 $\mu\left(\left\{h>\frac{1}{n}\right\}\right)=0$ 对所有 $n$ 成立.

> **基础知识**<br>**黎曼积分与达布和**: 设 $f$ 是 $\left[a,b\right]$ 上的有界实值函数. 对 $\left[a,b\right]$ 的一个分割 $P=\left\{t_{0}<\cdots<t_{n}\right\}$, 记 $M_{i}=\sup_{\left[t_{i-1},t_{i}\right]}f$, $m_{i}=\inf_{\left[t_{i-1},t_{i}\right]}f$, 定义上达布和 $\overline S\left(P\right)=\sum_{i}M_{i}\left(t_{i}-t_{i-1}\right)$, 下达布和 $\underline S\left(P\right)=\sum_{i}m_{i}\left(t_{i}-t_{i-1}\right)$. 上积分 $\overline{\int}f=\inf_{P}\overline S\left(P\right)$, 下积分 $\underline{\int}f=\sup_{P}\underline S\left(P\right)$. 若 $\overline{\int}f=\underline{\int}f$, 其公共值称为 $f$ 的黎曼积分, 此时称 $f$ 黎曼可积.

### 习题一

设 $f$ 为非负简单函数, 证明下列命题 : $A\mapsto\int_{A}f\,\mathrm{d}\mu$ 是一个测度; 若 $\mu\left(A\right)=0$, 则 $\int_{A}f\,\mathrm{d}\mu=0$.

### 解答 习题一

设 $f=\sum_{i=1}^{n}c_{i}\chi_{A_{i}}$, 其中 $c_{i}\ge0$, $A_{i}\in\mathcal F$ 两两不交且 $\bigcup_{i}A_{i}=X$. 对 $E\in\mathcal F$, 由**定义 8.1.1**,

$$
\begin{aligned}
&\quad\;\int_{E}f\,\mathrm{d}\mu\\&=\int f\chi_{E}\,\mathrm{d}\mu\\&=\sum_{i=1}^{n}c_{i}\mu\left(E\cap A_{i}\right).
\end{aligned}
$$

记 $\lambda\left(E\right):=\int_{E}f\,\mathrm{d}\mu$. 验证 $\lambda$ 是测度:

- $\lambda\left(\emptyset\right)=\sum_{i=1}^{n}c_{i}\mu\left(\emptyset\cap A_{i}\right)=0$;
- 非负性显然, 因 $c_{i}\ge0$ 且 $\mu\ge0$;
- σ-可加性: 设 $E=\bigsqcup_{j=1}^{\infty}E_{j}$ (两两不交). 由 $\mu$ 的 σ-可加性 (**定义 5.1.2**) 与**命题 8.1.2** (线性性),

$$
\begin{aligned}
&\quad\;\lambda\left(E\right)\\&=\sum_{i=1}^{n}c_{i}\mu\left(E\cap A_{i}\right)\\&=\sum_{i=1}^{n}c_{i}\sum_{j=1}^{\infty}\mu\left(E_{j}\cap A_{i}\right)\\&=\sum_{j=1}^{\infty}\sum_{i=1}^{n}c_{i}\mu\left(E_{j}\cap A_{i}\right)\\&=\sum_{j=1}^{\infty}\lambda\left(E_{j}\right).
\end{aligned}
$$

故 $\lambda$ 是 $\mathcal F$ 上的测度. 最后, 若 $\mu\left(A\right)=0$, 则

$$
\begin{aligned}
&\quad\;\lambda\left(A\right)\\&=\sum_{i=1}^{n}c_{i}\mu\left(A\cap A_{i}\right)\\&\le\sum_{i=1}^{n}c_{i}\mu\left(A\right)\\&=0,
\end{aligned}
$$

故 $\lambda\left(A\right)=0$. $\blacksquare$

### 习题二

设 $f,g$ 是可积函数, $a,b\in\mathbb R$, 证明下列性质 :

1. 线性性: $\int_{X}\left(af+bg\right)\mathrm{d}\mu=a\int_{X}f\,\mathrm{d}\mu+b\int_{X}g\,\mathrm{d}\mu$;
2. 单调性: 若 $f\le g$ 几乎处处, 则 $\int_{X}f\,\mathrm{d}\mu\le\int_{X}g\,\mathrm{d}\mu$;
3. 三角不等式: $\left|\int_{X}f\,\mathrm{d}\mu\right|\le\int_{X}\left|f\right|\mathrm{d}\mu$;
4. 若 $f=g$ 几乎处处, 则 $\int_{X}f\,\mathrm{d}\mu=\int_{X}g\,\mathrm{d}\mu$.

### 解答 习题二

先建立非负可测函数积分的线性性. 设 $\phi,\psi$ 为非负可测函数, $\alpha,\beta\ge0$. 由**注 8.2.3**, 存在简单函数 $\phi_{k}\uparrow\phi$, $\psi_{k}\uparrow\psi$. 由**命题 8.1.2** (简单函数的线性性),

$$
\int\left(\alpha\phi_{k}+\beta\psi_{k}\right)\mathrm{d}\mu=\alpha\int\phi_{k}\,\mathrm{d}\mu+\beta\int\psi_{k}\,\mathrm{d}\mu.
$$

因 $\alpha\phi_{k}+\beta\psi_{k}\uparrow\alpha\phi+\beta\psi$, 由**定理 8.2.2** (单调收敛定理) 两边取极限得

$$
\int\left(\alpha\phi+\beta\psi\right)\mathrm{d}\mu=\alpha\int\phi\,\mathrm{d}\mu+\beta\int\psi\,\mathrm{d}\mu.
$$

再设 $f,g$ 可积, 记 $f^{+},f^{-}$ 为其正负部 (**定义 8.2.5**).

1. 先对纯量乘: 若 $a\ge0$, 则 $\left(af\right)^{+}=af^{+}$, $\left(af\right)^{-}=af^{-}$, 故 $\int\left(af\right)\mathrm{d}\mu=a\int f^{+}\mathrm{d}\mu-a\int f^{-}\mathrm{d}\mu=a\int f\,\mathrm{d}\mu$; 若 $a<0$, 则 $\left(af\right)^{+}=\left|a\right|f^{-}$, $\left(af\right)^{-}=\left|a\right|f^{+}$, 同样得 $\int\left(af\right)\mathrm{d}\mu=a\int f\,\mathrm{d}\mu$; $a=0$ 平凡. 对加法, 由正负部分解 $f+g=\left(f^{++}g^{+}\right)-\left(f^{-}+g^{-}\right)$, 即

$$
\left(f+g\right)^{+}+f^{-}+g^{-}=\left(f+g\right)^{-}+f^{+}+g^{+},
$$

两边均为非负可测函数, 由非负线性性积分得

$$
\int\left(f+g\right)^{+}\mathrm{d}\mu+\int f^{-}\mathrm{d}\mu+\int g^{-}\mathrm{d}\mu=\int\left(f+g\right)^{-}\mathrm{d}\mu+\int f^{+}\mathrm{d}\mu+\int g^{+}\mathrm{d}\mu,
$$

移项 (各项有限, 因 $f,g$ 可积) 得 $\int\left(f+g\right)\mathrm{d}\mu=\int f\,\mathrm{d}\mu+\int g\,\mathrm{d}\mu$. 结合两者得 $\int\left(af+bg\right)\mathrm{d}\mu=a\int f\,\mathrm{d}\mu+b\int g\,\mathrm{d}\mu$.

2. 由线性性, $\int g\,\mathrm{d}\mu-\int f\,\mathrm{d}\mu=\int\left(g-f\right)\mathrm{d}\mu$. 因 $f\le g$ 几乎处处, $g-f\ge0$ 几乎处处. 由**定义 8.2.1**, 非负可测函数的积分为非负 (它是非负简单函数积分的上确界), 故 $\int\left(g-f\right)\mathrm{d}\mu\ge0$, 即 $\int f\,\mathrm{d}\mu\le\int g\,\mathrm{d}\mu$.

3. $\left|f\right|=f^{+}+f^{-}$, 由非负线性性 $\int\left|f\right|\mathrm{d}\mu=\int f^{+}\mathrm{d}\mu+\int f^{-}\mathrm{d}\mu$. 再由 $\int f\,\mathrm{d}\mu=\int f^{+}\mathrm{d}\mu-\int f^{-}\mathrm{d}\mu$, 有

$$
\begin{aligned}
&\quad\;\left|\int f\,\mathrm{d}\mu\right|\\&=\left|\int f^{+}\mathrm{d}\mu-\int f^{-}\mathrm{d}\mu\right|\\&\le\int f^{+}\mathrm{d}\mu+\int f^{-}\mathrm{d}\mu\\&=\int\left|f\right|\mathrm{d}\mu.
\end{aligned}
$$

4. $f=g$ 几乎处处, 则 $f^{+}=g^{+}$, $f^{-}=g^{-}$ 几乎处处. 于是 $h:=f^{+}-g^{+}$ 可积且 $h=0$ 几乎处处, 其正部 $h^{+}$ 与负部 $h^{-}$ 均在零测集外为零. 由**命题 8.2.4** (绝对连续性), $\int h^{+}\mathrm{d}\mu=\int_{\left\{h>0\right\}}h^{+}\mathrm{d}\mu=0$, $\int h^{-}\mathrm{d}\mu=0$, 故 $\int h\,\mathrm{d}\mu=0$, 即 $\int f^{+}\mathrm{d}\mu=\int g^{+}\mathrm{d}\mu$; 同理 $\int f^{-}\mathrm{d}\mu=\int g^{-}\mathrm{d}\mu$. 因此 $\int f\,\mathrm{d}\mu=\int g\,\mathrm{d}\mu$. $\blacksquare$

### 习题三

设 $f\in L^{1}$, 证明下列命题 :

(a) 集合 $\left\{x:f\left(x\right)\ne0\right\}$ 是 σ-有限的;
(b) 对 $f,g\in L^{1}$, $\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\mu$ 对任意可测集 $E$ 成立, 当且仅当 $\int\left|f-g\right|\mathrm{d}\mu=0$, 当且仅当 $f=g$ 关于 $\mu$ 几乎处处.

### 解答 习题三

(a) 由**定义 8.2.5**, $f=f^{+}-f^{-}$, 故 $\left\{x:f\left(x\right)\ne0\right\}=\left\{x:f^{+}\left(x\right)>0\right\}\cup\left\{x:f^{-}\left(x\right)>0\right\}$. 而

$$
\left\{x:f^{+}\left(x\right)>0\right\}=\bigcup_{n=1}^{\infty}\left\{x:f^{+}\left(x\right)>\frac{1}{n}\right\},
$$

且由**定义 8.2.1** (非负积分为上确界),

$$
\int_{X}f^{+}\mathrm{d}\mu\ge\int_{\left\{f^{+}>\frac{1}{n}\right\}}f^{+}\mathrm{d}\mu\ge\frac{1}{n}\mu\left(\left\{x:f^{+}\left(x\right)>\frac{1}{n}\right\}\right).
$$

因 $f$ 可积, $\int f^{+}\mathrm{d}\mu<\infty$, 故 $\mu\left(\left\{x:f^{+}\left(x\right)>\frac{1}{n}\right\}\right)\le n\int f^{+}\mathrm{d}\mu<\infty$. 于是 $\left\{f^{+}>0\right\}$ 是可数个有限测度集之并; 同理 $\left\{f^{-}>0\right\}$ 亦然. 从而 $\left\{x:f\left(x\right)\ne0\right\}$ 也是可数个有限测度集之并, 在**定义 5.1.5** 的意义下是 σ-有限的. $\blacksquare$

(b) 记 $h:=\left|f-g\right|\in L^{1}$, $h\ge0$. 证明等价链.

(1) $\int\left|f-g\right|\mathrm{d}\mu=0\Rightarrow f=g$ 几乎处处: 由基础知识 (非负可积函数积分为零则几乎处处为零), $h=0$ 几乎处处, 即 $f=g$ 几乎处处.

(2) $f=g$ 几乎处处 $\Rightarrow\int\left|f-g\right|\mathrm{d}\mu=0$: 因 $h=0$ 在 $\left\{f\ne g\right\}$ 之外成立, 而 $\left\{f\ne g\right\}$ 是零测集. 由**命题 8.2.4** (绝对连续性), $\int_{\left\{f\ne g\right\}}h\,\mathrm{d}\mu=0$, 且 $\int_{\left\{f=g\right\}}h\,\mathrm{d}\mu=0$, 故 $\int h\,\mathrm{d}\mu=0$.

(3) $\int\left|f-g\right|\mathrm{d}\mu=0\Rightarrow\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\mu$ 对所有 $E$: 由习题二(1)(3) (线性与三角不等式),

$$
\begin{aligned}
&\quad\;\left|\int_{E}f\,\mathrm{d}\mu-\int_{E}g\,\mathrm{d}\mu\right|\\&=\left|\int_{E}\left(f-g\right)\mathrm{d}\mu\right|\\&\le\int_{E}\left|f-g\right|\mathrm{d}\mu\\&\le\int_{X}\left|f-g\right|\mathrm{d}\mu\\&=0.
\end{aligned}
$$

(4) $\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\mu$ 对所有 $E$ $\Rightarrow\int\left|f-g\right|\mathrm{d}\mu=0$: 取 $E:=\left\{x:f\left(x\right)\ge g\left(x\right)\right\}\in\mathcal F$. 由习题二(1) 线性性, $\int_{E}\left(f-g\right)\mathrm{d}\mu=\int_{E}f\,\mathrm{d}\mu-\int_{E}g\,\mathrm{d}\mu=0$; 在 $E$ 上 $f-g\ge0$, 故 $\int_{E}\left|f-g\right|\mathrm{d}\mu=\int_{E}\left(f-g\right)\mathrm{d}\mu=0$. 同理, 对 $E^{c}$, $\int_{E^{c}}\left(g-f\right)\mathrm{d}\mu=0$, 在 $E^{c}$ 上 $g-f\ge0$, 故 $\int_{E^{c}}\left|f-g\right|\mathrm{d}\mu=0$. 于是 $\int\left|f-g\right|\mathrm{d}\mu=\int_{E}\left|f-g\right|\mathrm{d}\mu+\int_{E^{c}}\left|f-g\right|\mathrm{d}\mu=0$.

综合 (1)(2)(3)(4) 得三条件等价. $\blacksquare$

### 习题四

证明习题 14、16.

**14.** 若 $f\in L^{+}$, 令 $\lambda\left(E\right)=\int_{E}f\,\mathrm{d}\mu$ (对 $E\in\mathcal M$). 则 $\lambda$ 是 $\mathcal M$ 上的测度, 且对任意 $g\in L^{+}$, $\int g\,d\lambda=\int fg\,\mathrm{d}\mu$.

**16.** 若 $f\in L^{+}$ 且 $\int f<\infty$, 对每个 $\varepsilon>0$ 存在 $E\in\mathcal M$ 使得 $\mu\left(E\right)<\infty$ 且 $\int_{E}f>\left(\int f\right)-\varepsilon$.

### 解答 习题四

#### 14

先证 $\lambda$ 是测度. 由**定义 8.1.1** 与**定义 8.2.1**, $\lambda\left(\emptyset\right)=0$ 且非负. 对两两不交的可测集 $\left\{E_{n}\right\}$, 因 $f\chi_{\bigsqcup E_{n}}=\sum_{n}f\chi_{E_{n}}$ 且部分和 $\sum_{n=1}^{N}f\chi_{E_{n}}\uparrow f\chi_{\bigsqcup E_{n}}$ 点点, 由**定理 8.2.2** (单调收敛定理),

$$
\begin{aligned}
&\quad\;\lambda\left(\bigsqcup_{n=1}^{\infty}E_{n}\right)\\&=\int f\chi_{\bigsqcup E_{n}}\mathrm{d}\mu\\&=\sum_{n=1}^{\infty}\int f\chi_{E_{n}}\mathrm{d}\mu\\&=\sum_{n=1}^{\infty}\lambda\left(E_{n}\right).
\end{aligned}
$$

故 $\lambda$ 是 $\mathcal M$ 上的测度.

再证换元公式. 若 $g=\sum_{j=1}^{m}a_{j}\chi_{E_{j}}$ 是简单函数 (设 $E_{j}$ 两两不交), 由**定义 8.1.1** 与有限线性性,

$$
\begin{aligned}
&\quad\;\int g\,\mathrm{d}\lambda\\&=\sum_{j=1}^{m}a_{j}\lambda\left(E_{j}\right)\\&=\sum_{j=1}^{m}a_{j}\int_{E_{j}}f\,\mathrm{d}\mu\\&=\int\left(\sum_{j=1}^{m}a_{j}\chi_{E_{j}}f\right)\mathrm{d}\mu\\&=\int fg\,\mathrm{d}\mu.
\end{aligned}
$$

对一般 $g\in L^{+}$, 由**注 8.2.3** 取简单函数 $g_{k}\uparrow g$. 因 $f\ge0$, $fg_{k}\uparrow fg$. 由**定理 8.2.2** (分别在测度 $\lambda$ 与 $\mu$ 下), $\int g_{k}\,d\lambda\uparrow\int g\,d\lambda$ 且 $\int fg_{k}\,\mathrm{d}\mu\uparrow\int fg\,\mathrm{d}\mu$. 对每个 $k$ 两式相等 (简单情形), 故极限相等: $\int g\,d\lambda=\int fg\,\mathrm{d}\mu$. $\blacksquare$

#### 16

对 $n\in\mathbb N$, 令 $E_{n}:=\left\{x:f\left(x\right)>\frac{1}{n}\right\}\in\mathcal M$. 则 $\left\{E_{n}\right\}$ 单调上升且 $\bigcup_{n}E_{n}=\left\{x:f\left(x\right)>0\right\}$. 由**定义 8.2.1**,

$$
\int f\,\mathrm{d}\mu\ge\int_{E_{n}}f\,\mathrm{d}\mu\ge\frac{1}{n}\mu\left(E_{n}\right),
$$

故 $\mu\left(E_{n}\right)\le n\int f\,\mathrm{d}\mu<\infty$. 又由**定理 8.2.2** (单调收敛定理), $\int_{E_{n}}f\,\mathrm{d}\mu\uparrow\int_{\left\{f>0\right\}}f\,\mathrm{d}\mu=\int f\,\mathrm{d}\mu$. 故对给定 $\varepsilon>0$, 取 $n$ 充分大使 $\int_{E_{n}}f\,\mathrm{d}\mu>\int f\,\mathrm{d}\mu-\varepsilon$, 令 $E:=E_{n}$, 则 $\mu\left(E\right)<\infty$ 且 $\int_{E}f>\int f-\varepsilon$. $\blacksquare$

### 习题五

证明习题 20、23、27、29.

**20.** (广义控制收敛定理) 若 $f_{n},g_{n},f,g\in L^{1}$, $f_{n}\to f$ 且 $g_{n}\to g$ 几乎处处, $\left|f_{n}\right|\le g_{n}$, 且 $\int g_{n}\to\int g$, 则 $\int f_{n}\to\int f$.

**23.** 给定有界函数 $f:\left[a,b\right]\to\mathbb R$, 令

$$
\begin{aligned}
H\left(x\right)&=\limsup_{\delta\to0}\sup_{0<\left|y-x\right|\le\delta}f\left(y\right),\\h\left(x\right)&=\liminf_{\delta\to0}\inf_{0<\left|y-x\right|\le\delta}f\left(y\right).
\end{aligned}
$$

通过证明下面的引理来证明定理 2.28b (f 黎曼可积当且仅当 f 在 $\left[a,b\right]$ 上的不连续点集测度为 0):

a. $H\left(x\right)=h\left(x\right)$ 当且仅当 $f$ 在 $x$ 连续;
b. 在定理 2.28a 的证明记号下, $H=G$ 几乎处处, $h=g$ 几乎处处, 且 $\int_{\left(a,b\right)}h\,\mathrm{d}m=L\left(f\right)$ (下达布积分).

**27.** 设 $f_{n}\left(x\right)=ae^{-nax}-be^{-nbx}$, 其中 $0<a<b$.

a. $\sum_{n=1}^{\infty}\int_{0}^{\infty}\left|f_{n}\left(x\right)\right|\mathrm{d}x=\infty$;
b. $\sum_{n=1}^{\infty}\int_{0}^{\infty}f_{n}\left(x\right)\mathrm{d}x=0$;
c. $\sum_{n=1}^{\infty}f_{n}\in L^{1}\left(\left[0,\infty\right),m\right)$, 且 $\int_{0}^{\infty}\sum_{n=1}^{\infty}f_{n}\left(x\right)\mathrm{d}x=\log\left(b/a\right)$.

**29.** 通过对等式 $\int_{0}^{\infty}e^{-tx}\mathrm{d}x=1/t$ 求导, 证明 $\int_{0}^{\infty}x^{n}e^{-x}\mathrm{d}x=n!$; 类似地, 通过对等式 $\int_{-\infty}^{\infty}e^{-tx^{2}}\mathrm{d}x=\sqrt{\pi/t}$ 求导, 证明 $\int_{-\infty}^{\infty}x^{2n}e^{-x^{2}}\mathrm{d}x=\frac{\left(2n\right)!\sqrt\pi}{4^{n}n!}$.

### 解答 习题五

#### 20

由 $g_{n}\to g$ 几乎处处且 $\left|f_{n}\right|\le g_{n}$, 取极限得 $\left|f\right|\le g$ 几乎处处, 故 $f\in L^{1}$. 因 $\left|f_{n}\right|\le g_{n}$ 意味着 $-g_{n}\le f_{n}\le g_{n}$, 函数列 $\left\{g_{n}+f_{n}\right\}$ 与 $\left\{g_{n}-f_{n}\right\}$ 非负, 且分别几乎处处收敛于 $g+f$ 与 $g-f$. 由**定理 8.2.7** (法图引理),

$$
\int\left(g+f\right)\mathrm{d}\mu\le\liminf_{n\to\infty}\int\left(g_{n}+f_{n}\right)\mathrm{d}\mu=\int g\,\mathrm{d}\mu+\liminf_{n\to\infty}\int f_{n}\,\mathrm{d}\mu,
$$

因 $\int g_{n}\to\int g$ 且积分为有限 (线性性, 习题二). 两边减 $\int g\,\mathrm{d}\mu$ 得 $\int f\,\mathrm{d}\mu\le\liminf_{n\to\infty}\int f_{n}\,\mathrm{d}\mu$. 同理, 对 $\left\{g_{n}-f_{n}\right\}$ 用法图引理,

$$
\int\left(g-f\right)\mathrm{d}\mu\le\liminf_{n\to\infty}\int\left(g_{n}-f_{n}\right)\mathrm{d}\mu=\int g\,\mathrm{d}\mu-\limsup_{n\to\infty}\int f_{n}\,\mathrm{d}\mu,
$$

即 $\limsup_{n\to\infty}\int f_{n}\,\mathrm{d}\mu\le\int f\,\mathrm{d}\mu$. 综合得

$$
\int f\,\mathrm{d}\mu\le\liminf_{n\to\infty}\int f_{n}\,\mathrm{d}\mu\le\limsup_{n\to\infty}\int f_{n}\,\mathrm{d}\mu\le\int f\,\mathrm{d}\mu,
$$

故 $\lim_{n\to\infty}\int f_{n}\,\mathrm{d}\mu=\int f\,\mathrm{d}\mu$. $\blacksquare$

#### 23

先用基础知识中达布和的记号. 记 $\overline{\int}f=\inf_{P}\overline S\left(P\right)$, $\underline{\int}f=\sup_{P}\underline S\left(P\right)$; $f$ 黎曼可积当且仅当 $\overline{\int}f=\underline{\int}f$.

**a.** 设 $f$ 在 $x$ 连续. 对 $\varepsilon>0$ 存在 $\delta>0$ 使 $\left|y-x\right|<\delta\Rightarrow\left|f\left(y\right)-f\left(x\right)\right|<\varepsilon$. 则对 $0<\left|y-x\right|\le\delta$, 有 $f\left(x\right)-\varepsilon<f\left(y\right)<f\left(x\right)+\varepsilon$, 故

$$
f\left(x\right)-\varepsilon\le\inf_{0<\left|y-x\right|\le\delta}f\left(y\right)\le f\left(x\right)\le\sup_{0<\left|y-x\right|\le\delta}f\left(y\right)\le f\left(x\right)+\varepsilon.
$$

令 $\delta\to0$, 由 $\varepsilon$ 任意得 $h\left(x\right)\ge f\left(x\right)\ge H\left(x\right)$; 但定义中恒有 $h\left(x\right)\le f\left(x\right)\le H\left(x\right)$, 故 $H\left(x\right)=h\left(x\right)=f\left(x\right)$.

反之, 设 $H\left(x\right)=h\left(x\right)=:L$. 对 $\varepsilon>0$, 由极限定义存在 $\delta>0$ 使对 $0<\delta'<\delta$ 有

$$
\inf_{0<\left|y-x\right|\le\delta'}f\left(y\right)>L-\varepsilon,\quad \sup_{0<\left|y-x\right|\le\delta'}f\left(y\right)<L+\varepsilon.
$$

取 $\delta'=\delta$, 则对 $0<\left|y-x\right|\le\delta$ 有 $L-\varepsilon<f\left(y\right)<L+\varepsilon$; 又 $f\left(x\right)$ 介于 $\inf$ 与 $\sup$ 之间, 故 $L-\varepsilon<f\left(x\right)<L+\varepsilon$. 于是 $\left|f\left(y\right)-f\left(x\right)\right|<2\varepsilon$ 对 $0<\left|y-x\right|\le\delta$ 成立, 即 $f$ 在 $x$ 连续.

**b.** 沿用定理 2.28a 证明中的记号: 取分割列 $\left\{P_{k}\right\}$, 使网格 $\max_{i}\left(t_{i}-t_{i-1}\right)\to0$ 且 $P_{k}\subset P_{k+1}$ (逐次加密), 定义

$$
\begin{aligned}
G_{P_{k}}&=\sum_{i}M_{i}^{\left(k\right)}\chi_{\left(t_{i-1}^{\left(k\right)},t_{i}^{\left(k\right)}\right)},\\g_{P_{k}}&=\sum_{i}m_{i}^{\left(k\right)}\chi_{\left(t_{i-1}^{\left(k\right)},t_{i}^{\left(k\right)}\right)},
\end{aligned}
$$

并令 $G=\lim_{k}G_{P_{k}}$, $g=\lim_{k}g_{P_{k}}$. 固定 $x$ 不属于任何 $P_{k}$ 的分点 (所有分割的分点之并至多可数, 测度为 0). 设 $x\in\left(t_{i-1}^{\left(k\right)},t_{i}^{\left(k\right)}\right)$, 则 $G_{P_{k}}\left(x\right)=M_{i}^{\left(k\right)}=\sup_{\left[t_{i-1}^{\left(k\right)},t_{i}^{\left(k\right)}\right]}f$. 随 $k\to\infty$ 该小区间收缩到 $\left\{x\right\}$, 上确界递减趋于 $\sup_{0<\left|y-x\right|\le\delta}f\left(y\right)$ 随 $\delta\to0$ 的极限, 即 $H\left(x\right)$. 故 $G\left(x\right)=H\left(x\right)$; 同理 $g\left(x\right)=h\left(x\right)$. 因此在 $\left[a,b\right]$ 去掉可数分点集后 $H=G$, $h=g$ 几乎处处.

又 $G_{P_{k}}$ 有界且 $g_{P_{k}}\le f\le G_{P_{k}}$, 由**定理 8.2.9** (控制收敛定理, 或单调收敛),

$$
\begin{aligned}
&\quad\;\int H\,\mathrm{d}m\\&=\int G\,\mathrm{d}m\\&=\lim_{k}\int G_{P_{k}}\mathrm{d}m\\&=\lim_{k}\overline S\left(P_{k}\right)\\&=\overline{\int}f,
\end{aligned}
$$

$$
\begin{aligned}
&\quad\;\int h\,\mathrm{d}m\\&=\int g\,\mathrm{d}m\\&=\lim_{k}\int g_{P_{k}}\mathrm{d}m\\&=\lim_{k}\underline S\left(P_{k}\right)\\&=\underline{\int}f.
\end{aligned}
$$

(在定理 2.28a 的证明中取 $P_{k}$ 已保证 $\overline S\left(P_{k}\right)\to\overline{\int}f$, $\underline S\left(P_{k}\right)\to\underline{\int}f$.) 特别地 $\int_{\left(a,b\right)}h\,\mathrm{d}m=L\left(f\right)$. 于是

$$
\begin{aligned}
&\quad\;f\text{黎曼可积}\\&\iff\overline{\int}f=\underline{\int}f\\&\iff\int H\,\mathrm{d}m=\int h\,\mathrm{d}m\\&\iff\int\left(H-h\right)\mathrm{d}m=0.
\end{aligned}
$$

因 $H\ge h$, 由习题三(b) 得 $\int\left(H-h\right)\mathrm{d}m=0\iff H=h$ 几乎处处. 结合引理 a ($H=h\iff f$ 连续于 $x$) 得 $f$ 黎曼可积当且仅当 $f$ 的不连续点集测度为 0. 此时黎曼积分 $\overline{\int}f=\int H\,\mathrm{d}m=\int f\,\mathrm{d}m$ (因 $H=f$ 几乎处处), 定理 2.28b 得证. $\blacksquare$

#### 27

先求 $f_{n}$ 的零点. 令 $f_{n}\left(x\right)=0$ 得 $ae^{-nax}=be^{-nbx}$, 即 $e^{n\left(b-a\right)x}=b/a$, 故唯一零点

$$
x_{n}=\frac{\log\left(b/a\right)}{n\left(b-a\right)}.
$$

在 $\left[0,x_{n}\right)$ 上 $f_{n}<0$, 在 $\left(x_{n},\infty\right)$ 上 $f_{n}>0$ (因 $x<x_{n}$ 时 $e^{n\left(b-a\right)x}<b/a$, 故 $ae^{-nax}<be^{-nbx}$).

**a.** 计算

$$
\int_{0}^{\infty}\left|f_{n}\right|\mathrm{d}x=\int_{0}^{x_{n}}\left(be^{-nbx}-ae^{-nax}\right)\mathrm{d}x+\int_{x_{n}}^{\infty}\left(ae^{-nax}-be^{-nbx}\right)\mathrm{d}x.
$$

利用 $\int_{0}^{x_{n}}be^{-nbx}\mathrm{d}x=\frac{1}{n}\left(1-e^{-nbx_{n}}\right)$, $\int_{0}^{x_{n}}ae^{-nax}\mathrm{d}x=\frac{1}{n}\left(1-e^{-nax_{n}}\right)$, $\int_{x_{n}}^{\infty}ae^{-nax}\mathrm{d}x=\frac{1}{n}e^{-nax_{n}}$, $\int_{x_{n}}^{\infty}be^{-nbx}\mathrm{d}x=\frac{1}{n}e^{-nbx_{n}}$, 得

$$
\int_{0}^{\infty}\left|f_{n}\right|\mathrm{d}x=\frac{2}{n}\left(e^{-nax_{n}}-e^{-nbx_{n}}\right).
$$

记 $t=e^{-nx_{n}}$, 则由零点条件 $at^{a}=bt^{b}$, 即 $t^{a-b}=b/a$, 故 $t=\left(b/a\right)^{1/\left(a-b\right)}\in\left(0,1\right)$. 因 $t<1$ 且 $a<b$, 幂函数 $\lambda\mapsto t^{\lambda}$ 递减, 故 $t^{a}>t^{b}$, 常数 $c:=2\left(t^{a}-t^{b}\right)>0$. 因此

$$
\begin{aligned}
&\quad\;\sum_{n=1}^{\infty}\int_{0}^{\infty}\left|f_{n}\right|\mathrm{d}x\\&=c\sum_{n=1}^{\infty}\frac{1}{n}\\&=\infty.
\end{aligned}
$$

**b.** 逐项计算:

$$
\begin{aligned}
&\quad\;\int_{0}^{\infty}f_{n}\left(x\right)\mathrm{d}x\\&=\int_{0}^{\infty}ae^{-nax}\mathrm{d}x-\int_{0}^{\infty}be^{-nbx}\mathrm{d}x\\&=\frac{1}{n}-\frac{1}{n}\\&=0,
\end{aligned}
$$

故 $\sum_{n=1}^{\infty}\int_{0}^{\infty}f_{n}\left(x\right)\mathrm{d}x=0$.

**c.** 由几何级数 $\sum_{n=1}^{\infty}e^{-nax}=\frac{e^{-ax}}{1-e^{-ax}}=\frac{1}{e^{ax}-1}$,

$$
\begin{aligned}
&\quad\;\sum_{n=1}^{\infty}f_{n}\left(x\right)\\&=a\sum_{n=1}^{\infty}e^{-nax}-b\sum_{n=1}^{\infty}e^{-nbx}\\&=\frac{a}{e^{ax}-1}-\frac{b}{e^{bx}-1}.
\end{aligned}
$$

当 $x\to0^{+}$ 时, $\frac{a}{e^{ax}-1}=\frac{1}{x}-\frac{a}{2}+O\left(x\right)$, 故差 $\frac{a}{e^{ax}-1}-\frac{b}{e^{bx}-1}\to\frac{b-a}{2}+O\left(x\right)$ 有限; 当 $x\to\infty$ 时指数衰减. 故 $\sum f_{n}\in L^{1}\left(\left[0,\infty\right),m\right)$.

对 $R>0$, 换元 $u=ax$ 与 $u=bx$:

$$
\begin{aligned}
\int_{0}^{R}\frac{a}{e^{ax}-1}\mathrm{d}x&=\int_{0}^{aR}\frac{\mathrm{d}u}{e^{u}-1},\\\int_{0}^{R}\frac{b}{e^{bx}-1}\mathrm{d}x&=\int_{0}^{bR}\frac{\mathrm{d}u}{e^{u}-1}.
\end{aligned}
$$

故

$$
\int_{0}^{R}\left(\frac{a}{e^{ax}-1}-\frac{b}{e^{bx}-1}\right)\mathrm{d}x=\int_{aR}^{bR}\frac{\mathrm{d}u}{e^{u}-1}.
$$

由于 $\frac{1}{e^{u}-1}-\frac{1}{u}=O\left(e^{-u}\right)$ 在无穷远可积, $\int_{aR}^{bR}\frac{\mathrm{d}u}{e^{u}-1}=\int_{aR}^{bR}\frac{\mathrm{d}u}{u}+o\left(1\right)$, 令 $R\to\infty$ 得

$$
\begin{aligned}
&\quad\;\int_{0}^{\infty}\sum_{n=1}^{\infty}f_{n}\left(x\right)\mathrm{d}x\\&=\lim_{R\to\infty}\int_{aR}^{bR}\frac{\mathrm{d}u}{u}\\&=\log\left(b/a\right).
\end{aligned}
$$

注意到这里 $\sum\int\left|f_{n}\right|=\infty$ (由 a), 不满足**引理 8.2.13** (级数逐项积分) 的条件 $\sum\int\left|f_{n}\right|<\infty$, 故不能逐项积分; 事实上 $\int\sum f_{n}=\log\left(b/a\right)\ne\sum\int f_{n}=0$, 正说明该条件是本质的. $\blacksquare$

#### 29

用**定理 8.2.17**(b) (积分号下求导). 固定 $t_{0}>0$, 在 $t$ 的紧邻域 $\left[t_{0}/2,t_{0}\right]$ 上考察.

**情形 1.** 令 $F\left(t\right)=\int_{0}^{\infty}e^{-tx}\mathrm{d}x=\frac{1}{t}$ ($t>0$). 对每个 $k\ge1$, 在 $t\in\left[t_{0}/2,t_{0}\right]$ 上 $\left|\frac{\partial^{k}}{\partial t^{k}}e^{-tx}\right|=x^{k}e^{-tx}\le x^{k}e^{-\left(t_{0}/2\right)x}\in L^{1}\left(\left[0,\infty\right)\right)$, 故定理 8.2.17(b) 可反复应用:

$$
F^{\left(n\right)}\left(t\right)=\int_{0}^{\infty}\left(-x\right)^{n}e^{-tx}\mathrm{d}x.
$$

又 $F\left(t\right)=1/t$, 其 $n$ 阶导数为 $F^{\left(n\right)}\left(t\right)=\left(-1\right)^{n}n!/t^{n+1}$. 取 $t=1$:

$$
\int_{0}^{\infty}\left(-x\right)^{n}e^{-x}\mathrm{d}x=\left(-1\right)^{n}n!,
$$

即 $\int_{0}^{\infty}x^{n}e^{-x}\mathrm{d}x=n!$.

**情形 2.** 令 $G\left(s\right)=\int_{-\infty}^{\infty}e^{-sx^{2}}\mathrm{d}x=\sqrt{\pi/s}=\sqrt\pi\,s^{-1/2}$ ($s>0$). 对每个 $k\ge1$, 在 $s\in\left[s_{0}/2,s_{0}\right]$ 上 $\left|\frac{\partial^{k}}{\partial s^{k}}e^{-sx^{2}}\right|=x^{2k}e^{-sx^{2}}\le x^{2k}e^{-\left(s_{0}/2\right)x^{2}}\in L^{1}\left(\mathbb R\right)$, 故可反复求导:

$$
\begin{aligned}
&\quad\;G^{\left(n\right)}\left(s\right)\\&=\int_{-\infty}^{\infty}\left(-x^{2}\right)^{n}e^{-sx^{2}}\mathrm{d}x\\&=\left(-1\right)^{n}\int_{-\infty}^{\infty}x^{2n}e^{-sx^{2}}\mathrm{d}x.
\end{aligned}
$$

又 $G^{\left(n\right)}\left(s\right)=\sqrt\pi\left(-\frac{1}{2}\right)\left(-\frac{3}{2}\right)\cdots\left(-\frac{2n-1}{2}\right)s^{-\frac{2n+1}{2}}$. 取 $s=1$:

$$
\left(-1\right)^{n}\int_{-\infty}^{\infty}x^{2n}e^{-x^{2}}\mathrm{d}x=\sqrt\pi\left(-1\right)^{n}\frac{1\cdot3\cdots\left(2n-1\right)}{2^{n}},
$$

即 $\int_{-\infty}^{\infty}x^{2n}e^{-x^{2}}\mathrm{d}x=\sqrt\pi\frac{1\cdot3\cdots\left(2n-1\right)}{2^{n}}$. 由 $1\cdot3\cdots\left(2n-1\right)=\frac{\left(2n\right)!}{2^{n}n!}$, 得

$$
\int_{-\infty}^{\infty}x^{2n}e^{-x^{2}}\mathrm{d}x=\frac{\left(2n\right)!\sqrt\pi}{4^{n}n!}.
$$

$\blacksquare$
