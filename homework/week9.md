# 作业 9

> **定义 11.1.1** (符号测度)<br>设 $\left(X,\mathcal F\right)$ 是一个可测空间. 函数 $\nu:\mathcal F\to\mathbb R\cup\left\{+\infty\right\}$ 或 $\mathbb R\cup\left\{-\infty\right\}$ 称为**符号测度**, 若满足:<br>(1) $\nu\left(\varnothing\right)=0$;<br>(2) 可列可加性: 对任意一列互不相交的可测集 $\left\{E_{i}\right\}_{i=1}^{\infty}\subset\mathcal F$, 有 $\nu\left(\bigcup_{i=1}^{\infty}E_{i}\right)=\sum_{i=1}^{\infty}\nu\left(E_{i}\right)$;<br>(3) $\nu$ 不能同时取 $+\infty$ 与 $-\infty$ 为值.

> **命题 11.1.2** (符号测度的基本性质)<br>设 $\nu$ 是符号测度, 则:<br>(1) 有限可加性: 对任意有限个互不相交的 $E_{1},\dots,E_{n}\in\mathcal F$, 有 $\nu\left(\bigcup_{i=1}^{n}E_{i}\right)=\sum_{i=1}^{n}\nu\left(E_{i}\right)$;<br>(2) 下连续性: 若 $\left\{E_{j}\right\}$ 单调上升可测, 则 $\lim_{j\to\infty}\nu\left(E_{j}\right)=\nu\left(\bigcup_{j}E_{j}\right)$;<br>(3) 上连续性: 若 $\left\{E_{j}\right\}$ 单调下降可测且 $\nu\left(E_{1}\right)<\infty$, 则 $\lim_{j\to\infty}\nu\left(E_{j}\right)=\nu\left(\bigcap_{j}E_{j}\right)$.

> **定义 11.2.1** (正集、负集、零集)<br>设 $\nu$ 是 $\left(X,\mathcal F\right)$ 上的符号测度.<br>称 $P\in\mathcal F$ 为**正集** (记为 $P\gtrsim0$), 若对任意 $E\in\mathcal F$ 且 $E\subset P$, 有 $\nu\left(E\right)\ge0$;<br>称 $N\in\mathcal F$ 为**负集** (记为 $N\lesssim0$), 若对任意 $E\in\mathcal F$ 且 $E\subset N$, 有 $\nu\left(E\right)\le0$;<br>称 $Z\in\mathcal F$ 为**零集**, 若对任意 $E\in\mathcal F$ 且 $E\subset Z$, 有 $\nu\left(E\right)=0$.

> **引理 11.2.2** (正集的性质)<br>(1) 正集的任意可测子集是正集;<br>(2) 正集的可列并是正集;<br>(3) 若 $\left\{P_{n}\right\}$ 是正集列, 则 $\bigcap_{n=1}^{\infty}P_{n}$ 是正集.<br>上述性质对负集仍然成立 (注 11.2.3).

> **引理 11.2.4**<br>设 $\nu$ 是符号测度. 若 $E$ 不是负集, 则存在正集 $F\subset E$ 使得 $\nu\left(F\right)>0$.

> **定理 11.3.2** (哈恩分解定理)<br>设 $\nu$ 是 $\left(X,\mathcal F\right)$ 上的符号测度, 则存在 $X$ 的分解 $X=P\cup N$, 其中 $P$ 是正集, $N$ 是负集, $P\cap N=\varnothing$; 并且该分解在相差一个 $\nu$-零集的意义下是唯一的.

> **定义 11.4.1** (相互奇异的符号测度)<br>设 $\mu$ 和 $\nu$ 是可测空间 $\left(X,\mathcal F\right)$ 上的两个符号测度. 若存在可测集 $E\in\mathcal F$ 使得 $E$ 为 $\mu$-零集且 $E^{c}$ 为 $\nu$-零集, 则称 $\mu$ 和 $\nu$ 相互奇异, 记为 $\mu\perp\nu$.

> **定理 11.4.3** (若尔当分解定理)<br>设 $\nu$ 是 $\left(X,\mathcal F\right)$ 上的符号测度, 则存在唯一的一对相互奇异的正测度 $\nu^{+}$ 和 $\nu^{-}$, 使得 $\nu=\nu^{+}-\nu^{-}$.

> **定义 11.4.4** (变差测度)<br>设 $\nu$ 是符号测度, 其 若尔当分解为 $\nu=\nu^{+}-\nu^{-}$.<br>称 $\nu^{+}$ 为 $\nu$ 的**正变差**, $\nu^{-}$ 为 $\nu$ 的**负变差**, $\left|\nu\right|=\nu^{+}+\nu^{-}$ 为 $\nu$ 的**全变差测度**.

> **定义 11.5.1** (绝对连续性)<br>设 $\mu$ 是正测度, $\nu$ 是符号测度. 称 $\nu$ 关于 $\mu$ 绝对连续 (记为 $\nu\ll\mu$), 若对任意 $E\in\mathcal F$ 有 $\mu\left(E\right)=0\Rightarrow\nu\left(E\right)=0$.

> **注 11.5.3**<br>设 $f\in L^{1}\left(\mu\right)$, 则 $\lim_{\mu\left(E\right)\to0}\int_{E}f\,\mathrm{d}\mu=0$.

> **定理 11.5.5** (拉东-尼科迪姆定理)<br>设 $\mu$ 是 $\sigma$-有限正测度, $\nu$ 是符号测度且 $\nu\ll\mu$, 则存在可测函数 $f:X\to\mathbb R$ 使得 $\nu\left(E\right)=\int_{E}f\,\mathrm{d}\mu$ 对一切 $E\in\mathcal F$ 成立; 且 $\nu^{+}\left(E\right)=\int_{E}f^{+}\mathrm{d}\mu$, $\nu^{-}\left(E\right)=\int_{E}f^{-}\mathrm{d}\mu$, $\left|\nu\right|\left(E\right)=\int_{E}\left|f\right|\mathrm{d}\mu$. 函数 $f$ 称为 $\nu$ 关于 $\mu$ 的 拉东-尼科迪姆导数, 记作 $f=\frac{\mathrm{d}\nu}{\mathrm{d}\mu}$.

> **定理 10.2.2** (托内利定理)<br>如果 $f:X\times Y\to\left[0,\infty\right]$ 是 $\mathcal A\otimes\mathcal B$-可测的, 则 $$\begin{aligned}&\quad\;\int_{X\times Y}f\,\mathrm{d}\left(\mu\times\nu\right)\\&=\int_{X}\left(\int_{Y}f\left(x,y\right)\mathrm{d}\nu\left(y\right)\right)\mathrm{d}\mu\left(x\right)\\&=\int_{Y}\left(\int_{X}f\left(x,y\right)\mathrm{d}\mu\left(x\right)\right)\mathrm{d}\nu\left(y\right),\end{aligned}$$ 其中所有积分值都在 $\left[0,\infty\right]$ 中.

### 习题一

设 $\nu$ 是 $\left(X,\mathcal F\right)$ 上的符号测度且不取 $-\infty$, $E$ 不是负集. 证明: 存在可测集 $G\subset E$ 使得

$$
\nu\left(G\right)=\sup\left\{\nu\left(F\right):F\subset E,\nu\left(F\right)>0\right\}>0,
$$

且 $E\setminus G$ 是负集. (哈恩分解定理证明中的嵌入习题.)

### 解答 习题一

记 $\alpha=\sup\left\{\nu\left(F\right):F\subset E,\nu\left(F\right)>0\right\}$. 因 $E$ 不是负集, 由**引理 11.2.4** 存在正集 $F_{0}\subset E$ 使 $\nu\left(F_{0}\right)>0$, 故 $\alpha\ge\nu\left(F_{0}\right)>0$, 即 $\alpha>0$.

先证 $\alpha$ 由正集取到. 令

$$
\beta=\sup\left\{\nu\left(P\right):P\subset E,P\text{是正集}\right\},
$$

则 $\beta\ge\nu\left(F_{0}\right)>0$. 显然 $\beta\le\alpha$, 因为正集 $P\subset E$ 若 $\nu\left(P\right)>0$ 则计入 $\alpha$ 的上确界类. 反之证 $\alpha\le\beta$: 任取 $F\subset E$ 且 $\nu\left(F\right)>0$. 若 $F$ 是正集, 则 $\nu\left(F\right)\le\beta$; 若 $F$ 不是正集, 则存在 $C\subset F$ 使 $\nu\left(C\right)<0$, 取 $F_{1}=F\setminus C$, 则 $\nu\left(F_{1}\right)=\nu\left(F\right)-\nu\left(C\right)>\nu\left(F\right)$. 反复应用此构造得下降可测列 $\left\{F_{n}\right\}$, 使 $\nu\left(F_{n}\right)$ 严格上升收敛于某 $\gamma$. 由**命题 11.1.2**(3) (上连续性), $\nu\left(\bigcap_{n}F_{n}\right)=\lim_{n}\nu\left(F_{n}\right)=\gamma$. 若 $\bigcap_{n}F_{n}$ 不是正集, 则又可从中取出测度更大的子集, 与 $\gamma$ 的收敛性矛盾, 故 $\bigcap_{n}F_{n}\subset E$ 是正集. 于是 $\gamma=\nu\left(\bigcap_{n}F_{n}\right)\le\beta$; 又 $\nu\left(F_{n}\right)\uparrow\gamma$ 且 $\nu\left(F_{1}\right)>\nu\left(F\right)$, 得 $\nu\left(F\right)<\gamma\le\beta$. 故对任意这样的 $F$ 有 $\nu\left(F\right)\le\beta$, 即 $\alpha\le\beta$. 合并得 $\alpha=\beta$.

由 $\beta$ 的定义, 取正集列 $\left\{P_{n}\right\}\subset E$ 使 $\nu\left(P_{n}\right)\to\beta$. 令 $G=\bigcup_{n=1}^{\infty}P_{n}\subset E$, 则 $G$ 是正集 (**引理 11.2.2**(2)). 令 $Q_{n}=\bigcup_{k=1}^{n}P_{k}$, 则 $\left\{Q_{n}\right\}$ 是正集列的上升并, 仍为正集, 且 $\nu\left(Q_{n}\right)\ge\nu\left(P_{n}\right)\to\beta$; 又 $Q_{n}\subset E$ 为正集, 故 $\nu\left(Q_{n}\right)\le\beta$. 于是 $\nu\left(Q_{n}\right)\to\beta$, 由**命题 11.1.2**(2) (下连续性),

$$
\begin{aligned}
&\quad\;\nu\left(G\right)\\&=\lim_{n\to\infty}\nu\left(Q_{n}\right)\\&=\beta\\&=\alpha>0.
\end{aligned}
$$

最后证 $E\setminus G$ 是负集. 反设 $E\setminus G$ 不是负集, 由**引理 11.2.4** 存在正集 $F\subset E\setminus G$ 使 $\nu\left(F\right)>0$. 因 $G\cap F=\varnothing$, $G\cup F\subset E$ 且 $G\cup F$ 是正集 (**引理 11.2.2**(2)), 于是

$$
\begin{aligned}
&\quad\;\nu\left(G\cup F\right)\\&=\nu\left(G\right)+\nu\left(F\right)\\&=\alpha+\nu\left(F\right)\\&>\alpha\\&=\beta,
\end{aligned}
$$

与 $\beta$ 是 $E$ 中全体正集测度的上确界矛盾. 故 $E\setminus G$ 是负集. $\blacksquare$

### 习题二

证明习题 3、6、7.

**3.** 设 $\nu$ 是 $\left(X,\mathcal M\right)$ 上的符号测度.
a. $L^{1}\left(\nu\right)=L^{1}\left(\left|\nu\right|\right)$;
b. 若 $f\in L^{1}\left(\nu\right)$, 则 $\left|\int f\,\mathrm{d}\nu\right|\le\int\left|f\right|\mathrm{d}\left|\nu\right|$;
c. 若 $E\in\mathcal M$, 则 $\left|\nu\right|\left(E\right)=\sup\left\{\left|\int_{E}f\,\mathrm{d}\nu\right|:\left|f\right|\le1\right\}$.

**6.** 设 $\nu\left(E\right)=\int_{E}f\,\mathrm{d}\mu$, 其中 $\mu$ 是正测度, $f$ 是扩张的 $\mu$-可积函数. 用 $f$ 和 $\mu$ 描述 $\nu$ 的 哈恩分解, 以及 $\nu$ 的正变差、负变差与全变差.

**7.** 设 $\nu$ 是 $\left(X,\mathcal M\right)$ 上的符号测度, $E\in\mathcal M$.
a. $\nu^{+}\left(E\right)=\sup\left\{\nu\left(F\right):F\in\mathcal M,F\subset E\right\}$, 且 $\nu^{-}\left(E\right)=-\inf\left\{\nu\left(F\right):F\in\mathcal M,F\subset E\right\}$;
b. $\left|\nu\right|\left(E\right)=\sup\left\{\sum_{i}\left|\nu\left(E_{i}\right)\right|:n\in\mathbb N,E_{1},\dots,E_{n}\text{两两不交},\bigcup_{i=1}^{n}E_{i}=E\right\}$.

### 解答 习题二

#### 3

**(a)** 由**定义 11.4.4**, $\left|\nu\right|=\nu^{+}+\nu^{-}$. 于是对任意 $f$,

$$
\int\left|f\right|\mathrm{d}\left|\nu\right|=\int\left|f\right|\mathrm{d}\nu^{+}+\int\left|f\right|\mathrm{d}\nu^{-}.
$$

两边三项均非负, 故左端有限当且仅当右端两项均有限, 即 $f\in L^{1}\left(\nu^{+}\right)\cap L^{1}\left(\nu^{-}\right)=L^{1}\left(\nu\right)$ (由 $L^{1}\left(\nu\right)$ 的定义). 故 $L^{1}\left(\nu\right)=L^{1}\left(\left|\nu\right|\right)$. $\blacksquare$

**(b)** 由**定理 11.4.3** (若尔当分解), $\nu=\nu^{+}-\nu^{-}$. 于是由三角不等式与 (a),

$$
\begin{aligned}
&\quad\;\left|\int f\,\mathrm{d}\nu\right|\\&=\left|\int f\,\mathrm{d}\nu^{+}-\int f\,\mathrm{d}\nu^{-}\right|\\&\le\int\left|f\right|\mathrm{d}\nu^{+}+\int\left|f\right|\mathrm{d}\nu^{-}\\&=\int\left|f\right|\mathrm{d}\left|\nu\right|.
\end{aligned}
$$

$\blacksquare$

**(c)** 先证 $\le$: 对任意可测函数 $g$ 满足 $\left|g\right|\le1$, 由 (b) 得

$$
\left|\int_{E}g\,\mathrm{d}\nu\right|\le\int_{E}\left|g\right|\mathrm{d}\left|\nu\right|\le\int_{E}1\,\mathrm{d}\left|\nu\right|=\left|\nu\right|\left(E\right),
$$

故 $\sup\le\left|\nu\right|\left(E\right)$.

再证 $\ge$: 取 $\nu$ 的一个 哈恩分解 $X=P\cup N$ (**定理 11.3.2**), 令 $g=\chi_{E\cap P}-\chi_{E\cap N}$, 则 $\left|g\right|\le1$ 且 $g$ 可测. 由**定理 11.4.3** (若尔当分解), $\nu^{+}\left(E\right)=\nu\left(E\cap P\right)$, $\nu^{-}\left(E\right)=-\nu\left(E\cap N\right)$. 于是

$$
\begin{aligned}
&\quad\;\int_{E}g\,\mathrm{d}\nu\\&=\nu\left(E\cap P\right)-\nu\left(E\cap N\right)\\&=\nu^{+}\left(E\right)+\nu^{-}\left(E\right)\\&=\left|\nu\right|\left(E\right).
\end{aligned}
$$

故 $\sup\ge\left|\nu\right|\left(E\right)$. 合并得等式. $\blacksquare$

#### 6

$f$ 是实值可测函数, 至少一个 $\int f^{+}\mathrm{d}\mu$, $\int f^{-}\mathrm{d}\mu$ 有限. 由**定义 11.2.1**:

对 $E\in\mathcal M$, $E$ 是 $\nu$-正集当且仅当对任意可测 $F\subset E$, $\nu\left(F\right)=\int_{F}f\,\mathrm{d}\mu\ge0$; 因这对 $F=E\cap\left\{f<0\right\}$ 与 $F=E\cap\left\{f>0\right\}$ 均须成立, 故 $E$ 是正集当且仅当 $f\ge0$ $\mu$-几乎处处于 $E$ 上. 同理, $E$ 是负集当且仅当 $f\le0$ $\mu$-几乎处处于 $E$ 上; $E$ 是零集当且仅当 $f=0$ $\mu$-几乎处处于 $E$ 上.

因此 $X=P\cup N$, 其中

$$
\begin{aligned}
P&=\left\{x:f\left(x\right)\ge0\right\},\\N&=\left\{x:f\left(x\right)<0\right\},
\end{aligned}
$$

是 $\nu$ 的一个 哈恩分解 (**定理 11.3.2**): $P$ 是正集, $N$ 是负集, $P\cap N=\varnothing$, $P\cup N=X$. (零测集 $\left\{f=0\right\}$ 可并入 $P$ 或 $N$ 而不改变分解的本质.)

由**定理 11.4.3** (若尔当分解), $\nu^{+}\left(E\right)=\nu\left(E\cap P\right)=\int_{E\cap P}f\,\mathrm{d}\mu=\int_{E}f^{+}\mathrm{d}\mu$ (因 $f\ge0$ 于 $P$ 上), $\nu^{-}\left(E\right)=-\nu\left(E\cap N\right)=-\int_{E\cap N}f\,\mathrm{d}\mu=\int_{E}f^{-}\mathrm{d}\mu$ (因 $f\le0$ 于 $N$ 上). 故

$$
\begin{aligned}
\nu^{+}\left(E\right)&=\int_{E}f^{+}\mathrm{d}\mu,\\\nu^{-}\left(E\right)&=\int_{E}f^{-}\mathrm{d}\mu,\\\left|\nu\right|\left(E\right)&=\int_{E}\left|f\right|\mathrm{d}\mu.
\end{aligned}
$$

$\blacksquare$

#### 7

**(a)** 取 $\nu$ 的 哈恩分解 $X=P\cup N$ (**定理 11.3.2**), 则 $\nu^{+}\left(E\right)=\nu\left(E\cap P\right)$, $\nu^{-}\left(E\right)=-\nu\left(E\cap N\right)$ (**定理 11.4.3**).

对任意 $F\in\mathcal M$ 且 $F\subset E$, 由 $\nu=\nu^{+}-\nu^{-}$ 及 $\nu^{-}\ge0$ 得 $\nu\left(F\right)=\nu^{+}\left(F\right)-\nu^{-}\left(F\right)\le\nu^{+}\left(F\right)\le\nu^{+}\left(E\right)$ (最后一式由 $\nu^{+}$ 的单调性, 因 $F\subset E$). 故 $\sup\left\{\nu\left(F\right):F\subset E\right\}\le\nu^{+}\left(E\right)$. 取 $F=E\cap P\subset E$, 则 $\nu\left(E\cap P\right)=\nu^{+}\left(E\cap P\right)-\nu^{-}\left(E\cap P\right)=\nu^{+}\left(E\cap P\right)=\nu^{+}\left(E\right)$ (因 $E\cap P\subset P$ 是正集, $\nu^{-}\left(E\cap P\right)=0$). 故 $\sup\ge\nu^{+}\left(E\right)$. 合并得 $\nu^{+}\left(E\right)=\sup\left\{\nu\left(F\right):F\subset E\right\}$.

同理, 对 $F\subset E$ 有 $\nu\left(F\right)=\nu^{+}\left(F\right)-\nu^{-}\left(F\right)\ge-\nu^{-}\left(F\right)\ge-\nu^{-}\left(E\right)$, 故 $\inf\left\{\nu\left(F\right):F\subset E\right\}\ge-\nu^{-}\left(E\right)$, 即 $-\inf\left\{\nu\left(F\right):F\subset E\right\}\le\nu^{-}\left(E\right)$. 取 $F=E\cap N$, 则 $\nu\left(E\cap N\right)=-\nu^{-}\left(E\cap N\right)=-\nu^{-}\left(E\right)$, 故 $\inf\le-\nu^{-}\left(E\right)$, 即 $-\inf\ge\nu^{-}\left(E\right)$. 合并得 $\nu^{-}\left(E\right)=-\inf\left\{\nu\left(F\right):F\subset E\right\}$. $\blacksquare$

**(b)** 先证 $\le$: 对任意两两不交且并等于 $E$ 的 $\left\{E_{i}\right\}$, 由 $\nu=\nu^{+}-\nu^{-}$ 与三角不等式,

$$
\begin{aligned}
&\quad\;\sum_{i}\left|\nu\left(E_{i}\right)\right|\\&=\sum_{i}\left|\nu^{+}\left(E_{i}\right)-\nu^{-}\left(E_{i}\right)\right|\\&\le\sum_{i}\left[\nu^{+}\left(E_{i}\right)+\nu^{-}\left(E_{i}\right)\right]\\&=\nu^{+}\left(E\right)+\nu^{-}\left(E\right)\\&=\left|\nu\right|\left(E\right),
\end{aligned}
$$

故 $\sup\le\left|\nu\right|\left(E\right)$.

再证 $\ge$: 取 哈恩分解 $X=P\cup N$ (**定理 11.3.2**), 令 $E_{1}=E\cap P$, $E_{2}=E\cap N$, 则 $E_{1},E_{2}$ 两两不交且 $E_{1}\cup E_{2}=E$. 于是

$$
\begin{aligned}
&\quad\;\left|\nu\left(E_{1}\right)\right|+\left|\nu\left(E_{2}\right)\right|\\&=\nu^{+}\left(E\cap P\right)+\nu^{-}\left(E\cap N\right)\\&=\nu^{+}\left(E\right)+\nu^{-}\left(E\right)\\&=\left|\nu\right|\left(E\right),
\end{aligned}
$$

故 $\sup\ge\left|\nu\right|\left(E\right)$. 合并得等式. $\blacksquare$

### 习题三

证明习题 9、11、12、16、17.

**9.** 设 $\left\{\nu_{j}\right\}$ 是一列正测度. 若 $\nu_{j}\perp\mu$ 对一切 $j$, 则 $\sum_{j}\nu_{j}\perp\mu$; 若 $\nu_{j}\ll\mu$ 对一切 $j$, 则 $\sum_{j}\nu_{j}\ll\mu$.

**11.** 设 $\mu$ 是正测度. 一族函数 $\left\{f_{\alpha}\right\}_{\alpha\in A}\subset L^{1}\left(\mu\right)$ 称为一致可积的, 若对任意 $\varepsilon>0$ 存在 $\delta>0$ 使得 $\left|\int_{E}f_{\alpha}\,\mathrm{d}\mu\right|<\varepsilon$ 对所有 $\alpha\in A$ 成立, 只要 $\mu\left(E\right)<\delta$.
a. $L^{1}\left(\mu\right)$ 的任意有限子集是一致可积的;
b. 若 $\left\{f_{n}\right\}$ 是 $L^{1}\left(\mu\right)$ 中的序列且在 $L^{1}$ 度量下收敛于 $f\in L^{1}\left(\mu\right)$, 则 $\left\{f_{n}\right\}$ 是一致可积的.

**12.** 对 $j=1,2$, 设 $\mu_{j},\nu_{j}$ 是 $\left(X_{j},\mathcal M_{j}\right)$ 上的 $\sigma$-有限测度且 $\nu_{j}\ll\mu_{j}$. 则 $\nu_{1}\times\nu_{2}\ll\mu_{1}\times\mu_{2}$, 且

$$
\frac{\mathrm{d}\left(\nu_{1}\times\nu_{2}\right)}{\mathrm{d}\left(\mu_{1}\times\mu_{2}\right)}\left(x_{1},x_{2}\right)=\frac{\mathrm{d}\nu_{1}}{\mathrm{d}\mu_{1}}\left(x_{1}\right)\cdot\frac{\mathrm{d}\nu_{2}}{\mathrm{d}\mu_{2}}\left(x_{2}\right).
$$

**16.** 设 $\mu,\nu$ 是 $\left(X,\mathcal M\right)$ 上的测度且 $\nu\ll\mu$, 令 $\lambda=\mu+\nu$. 若 $f=\frac{\mathrm{d}\nu}{\mathrm{d}\lambda}$, 则 $0\le f<1$ $\mu$-几乎处处, 且 $\frac{\mathrm{d}\nu}{\mathrm{d}\mu}=\frac{f}{1-f}$.

**17.** 设 $\left(X,\mathcal M,\mu\right)$ 是 $\sigma$-有限测度空间, $\mathcal N$ 是 $\mathcal M$ 的子 $\sigma$-代数, $\nu=\mu|_{\mathcal N}$. 若 $f\in L^{1}\left(\mu\right)$, 则存在 $g\in L^{1}\left(\nu\right)$ (从而 $g$ 是 $\mathcal N$-可测的) 使得 $\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\nu$ 对一切 $E\in\mathcal N$ 成立; 若 $g'$ 是另一个这样的函数, 则 $g=g'$ $\nu$-几乎处处. (在概率论中, $g$ 称为 $f$ 关于 $\mathcal N$ 的条件期望.)

### 解答 习题三

#### 9

**(奇异情形)** 因 $\nu_{j}\perp\mu$ (**定义 11.4.1**), 对每个 $j$ 存在 $E_{j}\in\mathcal M$ 使 $E_{j}$ 是 $\mu$-零集且 $E_{j}^{c}$ 是 $\nu_{j}$-零集, 即 $\mu\left(E_{j}\right)=0$, $\nu_{j}\left(E_{j}^{c}\right)=0$. 令 $E=\bigcup_{j=1}^{\infty}E_{j}$. 由 $\mu$ 的次可数可加性,

$$
\mu\left(E\right)\le\sum_{j=1}^{\infty}\mu\left(E_{j}\right)=0,
$$

故 $E$ 是 $\mu$-零集. 又 $E^{c}=\bigcap_{j=1}^{\infty}E_{j}^{c}\subset E_{k}^{c}$ 对一切 $k$, 由 $\nu_{k}$ 的单调性 $\nu_{k}\left(E^{c}\right)\le\nu_{k}\left(E_{k}^{c}\right)=0$, 故 $\nu_{k}\left(E^{c}\right)=0$ 对一切 $k$, 从而 $\left(\sum_{j}\nu_{j}\right)\left(E^{c}\right)=\sum_{j}\nu_{j}\left(E^{c}\right)=0$. 故 $\sum_{j}\nu_{j}\perp\mu$. $\blacksquare$

**(绝对连续情形)** 设 $\nu_{j}\ll\mu$ 对一切 $j$ (**定义 11.5.1**). 若 $\mu\left(E\right)=0$, 则 $\nu_{j}\left(E\right)=0$ 对一切 $j$, 故 $\left(\sum_{j}\nu_{j}\right)\left(E\right)=\sum_{j}\nu_{j}\left(E\right)=0$. 因此 $\sum_{j}\nu_{j}\ll\mu$. $\blacksquare$

#### 11

**(a)** 设 $\left\{f_{1},\dots,f_{n}\right\}\subset L^{1}\left(\mu\right)$. 对每个 $j$, 由**注 11.5.3** ($f_{j}\in L^{1}\left(\mu\right)$, $\lim_{\mu\left(E\right)\to0}\int_{E}f_{j}\,\mathrm{d}\mu=0$), 存在 $\delta_{j}>0$ 使 $\mu\left(E\right)<\delta_{j}\Rightarrow\left|\int_{E}f_{j}\,\mathrm{d}\mu\right|<\varepsilon$. 取 $\delta=\min_{1\le j\le n}\delta_{j}>0$, 则当 $\mu\left(E\right)<\delta$ 时, 对所有 $j$ 有 $\mu\left(E\right)<\delta_{j}$, 故 $\left|\int_{E}f_{j}\,\mathrm{d}\mu\right|<\varepsilon$. 故 $\left\{f_{1},\dots,f_{n}\right\}$ 一致可积. $\blacksquare$

**(b)** 因 $\int\left|f_{n}-f\right|\mathrm{d}\mu\to0$, 存在 $N$ 使当 $n\ge N$ 时 $\int\left|f_{n}-f\right|\mathrm{d}\mu<\frac{\varepsilon}{2}$. 由 (a), 单元素集 $\left\{f\right\}$ 一致可积: 存在 $\delta_{1}>0$ 使 $\mu\left(E\right)<\delta_{1}\Rightarrow\left|\int_{E}f\,\mathrm{d}\mu\right|<\frac{\varepsilon}{2}$. 又有限集 $\left\{f_{1},\dots,f_{N-1}\right\}$ 由 (a) 一致可积: 存在 $\delta_{2}>0$ 使 $\mu\left(E\right)<\delta_{2}\Rightarrow\left|\int_{E}f_{n}\,\mathrm{d}\mu\right|<\varepsilon$ 对 $n<N$ 成立. 取 $\delta=\min\left\{\delta_{1},\delta_{2}\right\}$. 当 $\mu\left(E\right)<\delta$ 时, 对 $n\ge N$,

$$
\left|\int_{E}f_{n}\,\mathrm{d}\mu\right|\le\left|\int_{E}f\,\mathrm{d}\mu\right|+\int_{E}\left|f_{n}-f\right|\mathrm{d}\mu\le\frac{\varepsilon}{2}+\int\left|f_{n}-f\right|\mathrm{d}\mu<\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon,
$$

而对 $n<N$ 亦有 $\left|\int_{E}f_{n}\,\mathrm{d}\mu\right|<\varepsilon$. 故 $\left\{f_{n}\right\}$ 一致可积. $\blacksquare$

#### 12

因 $\nu_{j}\ll\mu_{j}$ 且 $\mu_{j}$ 是 $\sigma$-有限正测度, 由**定理 11.5.5** (拉东-尼科迪姆定理), 存在 $\mathcal M_{j}$-可测函数 $f_{j}=\frac{\mathrm{d}\nu_{j}}{\mathrm{d}\mu_{j}}\ge0$ 使得 $\nu_{j}\left(E\right)=\int_{E}f_{j}\,\mathrm{d}\mu_{j}$ 对一切 $E\in\mathcal M_{j}$ 成立. 定义 $F:\left(X_{1}\times X_{2}\right)\to\left[0,\infty\right]$, $F\left(x_{1},x_{2}\right)=f_{1}\left(x_{1}\right)f_{2}\left(x_{2}\right)$, 则 $F$ 是 $\mathcal M_{1}\otimes\mathcal M_{2}$-可测的 (由乘积空间的可测性). 对可测矩形 $A\times B\in\mathcal M_{1}\otimes\mathcal M_{2}$, 由**定理 10.2.2** (托内利定理),

$$
\begin{aligned}
&\quad\;\int_{A\times B}F\,\mathrm{d}\left(\mu_{1}\times\mu_{2}\right)\\&=\int_{A\times B}f_{1}\left(x_{1}\right)f_{2}\left(x_{2}\right)\mathrm{d}\left(\mu_{1}\times\mu_{2}\right)\\&=\left(\int_{A}f_{1}\,\mathrm{d}\mu_{1}\right)\left(\int_{B}f_{2}\,\mathrm{d}\mu_{2}\right)\\&=\nu_{1}\left(A\right)\nu_{2}\left(B\right)\\&=\left(\nu_{1}\times\nu_{2}\right)\left(A\times B\right).
\end{aligned}
$$

由乘积测度的唯一性 (矩形容许族上相等), 对一切 $E\in\mathcal M_{1}\otimes\mathcal M_{2}$ 有

$$
\left(\nu_{1}\times\nu_{2}\right)\left(E\right)=\int_{E}F\,\mathrm{d}\left(\mu_{1}\times\mu_{2}\right).
$$

这蕴含 $\nu_{1}\times\nu_{2}\ll\mu_{1}\times\mu_{2}$ (**定义 11.5.1**: 若 $\left(\mu_{1}\times\mu_{2}\right)\left(E\right)=0$, 则上式右端为 $0$). 又 $\nu_{1}\times\nu_{2}$ 是 $\sigma$-有限的 (因 $\nu_{j}$ $\sigma$-有限), 由**定理 11.5.5** 的唯一性, $F$ 就是 $\nu_{1}\times\nu_{2}$ 关于 $\mu_{1}\times\mu_{2}$ 的 拉东-尼科迪姆导数, 即

$$
\begin{aligned}
&\quad\;\frac{\mathrm{d}\left(\nu_{1}\times\nu_{2}\right)}{\mathrm{d}\left(\mu_{1}\times\mu_{2}\right)}\left(x_{1},x_{2}\right)\\&=f_{1}\left(x_{1}\right)f_{2}\left(x_{2}\right)\\&=\frac{\mathrm{d}\nu_{1}}{\mathrm{d}\mu_{1}}\left(x_{1}\right)\cdot\frac{\mathrm{d}\nu_{2}}{\mathrm{d}\mu_{2}}\left(x_{2}\right).
\end{aligned}
$$

$\blacksquare$

#### 16

因 $\lambda=\mu+\nu\ge\mu$ 且 $\nu\ll\mu$, 有 $\nu\ll\lambda$ (若 $\lambda\left(E\right)=0$, 则 $\mu\left(E\right)=0$, 从而 $\nu\left(E\right)=0$), 故 $f=\frac{\mathrm{d}\nu}{\mathrm{d}\lambda}$ 存在且 $f\ge0$ $\lambda$-几乎处处 (**定理 11.5.5**).

先证 $f<1$ $\mu$-几乎处处. 反设 $\mu\left(\left\{f\ge1\right\}\right)>0$. 因 $\nu\left(\left\{f\ge1\right\}\right)=\int_{\left\{f\ge1\right\}}f\,\mathrm{d}\lambda\ge\lambda\left(\left\{f\ge1\right\}\right)$, 而 $\lambda=\mu+\nu$, 故

$$
\nu\left(\left\{f\ge1\right\}\right)\ge\lambda\left(\left\{f\ge1\right\}\right)=\mu\left(\left\{f\ge1\right\}\right)+\nu\left(\left\{f\ge1\right\}\right),
$$

推出 $\mu\left(\left\{f\ge1\right\}\right)\le0$, 矛盾. 故 $0\le f<1$ $\mu$-几乎处处.

最后证 $\frac{\mathrm{d}\nu}{\mathrm{d}\mu}=\frac{f}{1-f}$. 对任意 $E\in\mathcal M$, 由 $\lambda=\mu+\nu$ 与 $f=\frac{\mathrm{d}\nu}{\mathrm{d}\lambda}$,

$$
\begin{aligned}
&\quad\;\nu\left(E\right)\\&=\int_{E}f\,\mathrm{d}\lambda\\&=\int_{E}f\,\mathrm{d}\mu+\int_{E}f\,\mathrm{d}\nu,
\end{aligned}
$$

即 $\int_{E}\left(1-f\right)\mathrm{d}\nu=\int_{E}f\,\mathrm{d}\mu$. 因 $1-f>0$ $\mu$-几乎处处 (也 $\lambda$-几乎处处), 由**定理 11.5.5** 的唯一性,

$$
\frac{\mathrm{d}\nu}{\mathrm{d}\mu}=\frac{f}{1-f}.
$$

$\blacksquare$

#### 17

对 $E\in\mathcal N$, 定义 $\nu_{0}\left(E\right):=\int_{E}f\,\mathrm{d}\mu$. 则 $\nu_{0}$ 是 $\mathcal N$ 上的符号测度: 有限可加性与可数可加性由 $\mu$ 的可数可加性及 $f$ 的可积性 (控制收敛) 保证, 且 $\left|\nu_{0}\left(E\right)\right|\le\int_{E}\left|f\right|\mathrm{d}\mu\le\int\left|f\right|\mathrm{d}\mu<\infty$, 故 $\nu_{0}$ 有限. 又 $\nu_{0}\ll\nu$ (**定义 11.5.1**): 若 $E\in\mathcal N$ 且 $\nu\left(E\right)=\mu\left(E\right)=0$, 则 $\nu_{0}\left(E\right)=\int_{E}f\,\mathrm{d}\mu=0$ ($f\in L^{1}\left(\mu\right)$, 在零测集上积分为 $0$). 由于 $\nu=\mu|_{\mathcal N}$ 是 $\sigma$-有限的 (由 $\mu$ $\sigma$-有限), 由**定理 11.5.5** (拉东-尼科迪姆定理), 存在 $\mathcal N$-可测函数 $g=\frac{\mathrm{d}\nu_{0}}{\mathrm{d}\nu}\in L^{1}\left(\nu\right)$ 使得

$$
\begin{aligned}
&\quad\;\int_{E}f\,\mathrm{d}\mu\\&=\nu_{0}\left(E\right)\\&=\int_{E}g\,\mathrm{d}\nu,
\end{aligned}
\quad \forall E\in\mathcal N.
$$

若 $g'\in L^{1}\left(\nu\right)$ 也满足同样等式, 则 $\int_{E}\left(g-g'\right)\mathrm{d}\nu=0$ 对一切 $E\in\mathcal N$. 取 $E=\left\{g>g'\right\}\in\mathcal N$, 因 $g-g'\in L^{1}\left(\nu\right)$ 且 $\int_{\left\{g>g'\right\}}\left(g-g'\right)\mathrm{d}\nu=0$, 由非负函数积分为零则几乎处处为零, 得 $g=g'$ $\nu$-几乎处处于 $\left\{g>g'\right\}$ 上; 同理于 $\left\{g<g'\right\}$ 上. 故 $g=g'$ $\nu$-几乎处处. $\blacksquare$
