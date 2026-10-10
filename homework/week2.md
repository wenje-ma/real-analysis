# 作业 2

> **定义 1.3.1** (上极限)<br>集列 $\left\{E_{n}\right\}$ 的上极限定义为 $$\begin{aligned}\overline{\lim}_{n\to\infty}E_{n}&=\left\{x:x\text{ 属于无穷多个 }E_{n}\right\}\\&=\bigcap_{n=1}^{\infty}\bigcup_{k=n}^{\infty}E_{k}.\end{aligned}$$

> **定义 1.3.3** (下极限)<br>$$\begin{aligned}\underline{\lim}_{n\to\infty}E_{n}&=\left\{x:x\text{ 仅不属于有限多个 }E_{n}\right\}\\&=\bigcup_{n=1}^{\infty}\bigcap_{k=n}^{\infty}E_{k}.\end{aligned}$$

> **定义 4.1.3** ($\sigma$-代数)<br>设 $X$ 非空, $\mathcal F\subset\mathcal P\left(X\right)$. 称 $\mathcal F$ 为 $X$ 上的一个 **$\sigma$-代数**, 若满足:<br>(1) $X\in\mathcal F$;<br>(2) 对补运算封闭: $A\in\mathcal F\Rightarrow A^{c}\in\mathcal F$;<br>(3) 对可数并封闭: $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal F\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal F$.<br>称 $\left(X,\mathcal F\right)$ 为**可测空间**, $\mathcal F$ 中的元素称为**可测集**.

> **定义 5.1.2** (测度)<br>设 $\left(X,\mathcal F\right)$ 是可测空间. 函数 $\mu:\mathcal F\to\left[0,+\infty\right]$ 称为 $\left(X,\mathcal F\right)$ 上的一个测度, 若满足:<br>(1) 非负性: $\mu\left(E\right)\ge0$ 对一切 $E\in\mathcal F$;<br>(2) 零空集性: $\mu\left(\varnothing\right)=0$;<br>(3) 可数可加性 ($\sigma$-可加性): 对任意可数个两两不交的 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$, 有 $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **命题 5.2.1** (有限可加性)<br>设 $\mu$ 是 $\left(X,\mathcal F\right)$ 上的测度, $E_{1},\dots,E_{n}\in\mathcal F$ 是两两不交的集合, 则 $$\mu\left(\bigcup_{k=1}^{n}E_{k}\right)=\sum_{k=1}^{n}\mu\left(E_{k}\right).$$

> **命题 5.2.2** (单调性)<br>设 $\mu$ 是测度, $E,F\in\mathcal F$ 且 $E\subset F$, 则 $\mu\left(E\right)\le\mu\left(F\right)$. 若进一步 $\mu\left(E\right)<+\infty$, 则 $\mu\left(F\setminus E\right)=\mu\left(F\right)-\mu\left(E\right)$.

> **命题 5.2.3** (次可数可加性)<br>设 $\mu$ 是测度, $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$ 是任意可数个集合 (不一定两两不交), 则 $$\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)\le\sum_{n=1}^{\infty}\mu\left(E_{n}\right).$$

> **命题 5.2.4** (下连续性)<br>设 $\mu$ 是测度, $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$ 是单调递增的集合序列 (即 $E_{1}\subset E_{2}\subset\cdots$), 则 $$\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\lim_{n\to\infty}\mu\left(E_{n}\right).$$

> **命题 5.2.5** (上连续性)<br>设 $\mu$ 是测度, $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$ 是单调递减的集合序列 (即 $E_{1}\supset E_{2}\supset\cdots$), 且存在某个 $m$ 使得 $\mu\left(E_{m}\right)<+\infty$, 则 $$\mu\left(\bigcap_{n=1}^{\infty}E_{n}\right)=\lim_{n\to\infty}\mu\left(E_{n}\right).$$

> **定义 5.4.1** (零集)<br>设 $\left(X,\mathcal F,\mu\right)$ 是测度空间. 集合 $N\in\mathcal F$ 称为零集, 若 $\mu\left(N\right)=0$.

> **定义 5.4.2** (零测度集)<br>集合 $A\subset X$ 称为零测度集, 若存在 $N\in\mathcal F$ 使得 $A\subset N$ 且 $\mu\left(N\right)=0$.

> **定义 5.4.4** (完备测度)<br>测度空间 $\left(X,\mathcal F,\mu\right)$ 称为完备的, 若对任意满足 $\mu\left(N\right)=0$ 的 $N\in\mathcal F$, 以及任意 $A\subset N$, 都有 $A\in\mathcal F$.

### 习题九

证明**定理 5.4.6 (测度完备化定理)**: 任意测度空间 $\left(X,\mathcal F,\mu\right)$ 都可以完备化. 即存在完备测度空间 $\left(X,\mathcal M,\overline\mu\right)$ 使得:

(1) $\mathcal F\subset\mathcal M$;

(2) $\overline\mu|_{\mathcal F}=\mu$;

(3) $\mathcal M$ 是包含 $\mathcal F$ 的最小完备 $\sigma$-代数.

(注: 讲义中此定理的符号有 光学字符识别 残缺, 原式 "$\mathcal M\subset\mathcal M$" 应作 "$\mathcal F\subset\mathcal M$", 其余按标准结论还原.)

### 解答 习题九

记 $\mathcal N=\left\{N\in\mathcal F:\mu\left(N\right)=0\right\}$ 为零集全体 (**定义 5.4.1**). 定义

$$
\mathcal M:=\left\{A\subset X:\exists\,B\in\mathcal F,\exists\,N\in\mathcal F,\mu\left(N\right)=0,\text{使 }B\subset A\subset B\cup N\right\},
$$

即 $A\in\mathcal M$ 当且仅当 $A$ 与某个可测集 $B$ 相差一个零测度集 (定义 5.4.2). 分六步证明.

**1. $\mathcal M$ 是 $\sigma$-代数.** 逐条验证**定义 4.1.3**:

(1) **$X\in\mathcal M$**: 取 $B=X$, $N=\varnothing$, 则 $X\subset X\subset X\cup\varnothing$.

(2) **补运算封闭**: 设 $B\subset A\subset B\cup N$, $\mu\left(N\right)=0$. 则 $\left(B\cup N\right)^{c}\subset A^{c}\subset B^{c}$, 且

$$
\begin{aligned}B^{c}\setminus\left(B\cup N\right)^{c}&=B^{c}\cap\left(B\cup N\right)\\&=B^{c}\cap N\subset N,
\end{aligned}
$$

故由**命题 5.2.2** (单调性) 得 $\mu\left(B^{c}\setminus\left(B\cup N\right)^{c}\right)\le\mu\left(N\right)=0$. 于是 $A^{c}\in\mathcal M$ (取 $B'=\left(B\cup N\right)^{c}\in\mathcal F$, $N'=B^{c}\setminus\left(B\cup N\right)^{c}$).

(3) **可数并封闭**: 设 $B_{n}\subset A_{n}\subset B_{n}\cup N_{n}$, $\mu\left(N_{n}\right)=0$. 则 $\bigcup_{n}B_{n}\subset\bigcup_{n}A_{n}\subset\left(\bigcup_{n}B_{n}\right)\cup\left(\bigcup_{n}N_{n}\right)$. 由**命题 5.2.3** (次可数可加性), $\mu\left(\bigcup_{n}N_{n}\right)\le\sum_{n}\mu\left(N_{n}\right)=0$, 故 $\bigcup_{n}N_{n}$ 是零测度集, 从而 $\bigcup_{n}A_{n}\in\mathcal M$.

故 $\mathcal M$ 是 $\sigma$-代数.

**2. 定义 $\overline\mu:\mathcal M\to\left[0,+\infty\right]$, $\overline\mu\left(A\right):=\mu\left(B\right)$, 其中 $B\subset A\subset B\cup N$, $\mu\left(N\right)=0$.** 先证良定义: 设 $B_{1}\subset A\subset B_{1}\cup N_{1}$ 与 $B_{2}\subset A\subset B_{2}\cup N_{2}$, $\mu\left(N_{1}\right)=\mu\left(N_{2}\right)=0$. 由 $B_{1}\subset A\subset B_{2}\cup N_{2}$ 得 $B_{1}\setminus B_{2}\subset N_{2}$, 故 $\mu\left(B_{1}\setminus B_{2}\right)\le\mu\left(N_{2}\right)=0$; 同理 $\mu\left(B_{2}\setminus B_{1}\right)=0$. 由**命题 5.2.1** (有限可加性) 与**命题 5.2.2** (单调性),

$$
\begin{aligned}\mu\left(B_{1}\right)&=\mu\left(B_{1}\cap B_{2}\right)+\mu\left(B_{1}\setminus B_{2}\right)\\&=\mu\left(B_{1}\cap B_{2}\right)\\&=\mu\left(B_{2}\right).
\end{aligned}
$$

故 $\overline\mu$ 良定义.

**3. $\overline\mu$ 是测度.** 逐条验证**定义 5.1.2**: 非负性显然. 零空集性: $\overline\mu\left(\varnothing\right)=\mu\left(\varnothing\right)=0$. 可数可加性: 设 $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal M$ 两两不交, 写 $A_{n}=B_{n}\cup N_{n}$ ($B_{n}\in\mathcal F$, $N_{n}\subset N_{n}'\in\mathcal N$). 则 $\bigcup_{n}A_{n}=\left(\bigcup_{n}B_{n}\right)\cup\left(\bigcup_{n}N_{n}\right)\in\mathcal M$, 且 $\left\{B_{n}\right\}$ 两两不交 (因 $B_{n}\subset A_{n}$), 由 $\mu$ 的可数可加性

$$
\begin{aligned}\overline\mu\left(\bigcup_{n}A_{n}\right)&=\mu\left(\bigcup_{n}B_{n}\right)\\&=\sum_{n}\mu\left(B_{n}\right)\\&=\sum_{n}\overline\mu\left(A_{n}\right).
\end{aligned}
$$

**4. 延拓性:** 对 $B\in\mathcal F$, 因 $B=B\cup\varnothing\in\mathcal M$, 故 $\overline\mu\left(B\right)=\mu\left(B\right)$, 即 $\overline\mu|_{\mathcal F}=\mu$.

**5. 完备性 (**定义 5.4.4**):** 设 $\overline\mu\left(A\right)=0$, 即 $A=B\cup N$ 且 $\mu\left(B\right)=0$, $N\subset N_{0}\in\mathcal N$. 则 $A\subset B\cup N_{0}$, 且由**命题 5.2.3**, $\mu\left(B\cup N_{0}\right)\le\mu\left(B\right)+\mu\left(N_{0}\right)=0$, 故 $A$ 是某个零测度集之子集. 于是 $A=\varnothing\cup A\in\mathcal M$, 且 $A$ 的任意子集 $C\subset A$ 亦满足 $C\subset B\cup N_{0}$, 故 $C\in\mathcal M$. 因此 $\mathcal M$ 完备.

**6. 最小性:** 设 $\mathcal M'$ 是任一包含 $\mathcal F$ 的完备 $\sigma$-代数. 对 $A=B\cup N\in\mathcal M$ ($B\in\mathcal F$, $N\subset N_{0}\in\mathcal N$), 因 $N_{0}\in\mathcal F\subset\mathcal M'$ 且 $\mu\left(N_{0}\right)=0$, 由 $\mathcal M'$ 的完备性得 $N\in\mathcal M'$; 又 $B\in\mathcal F\subset\mathcal M'$, 故 $A=B\cup N\in\mathcal M'$. 因此 $\mathcal M\subset\mathcal M'$. 故 $\mathcal M$ 是包含 $\mathcal F$ 的最小完备 $\sigma$-代数.

综上, $\left(X,\mathcal M,\overline\mu\right)$ 是满足 (1)(2)(3) 的完备测度空间, 定理得证. $\blacksquare$

### 习题十

证明习题 8、9、10、12.

**8.** 设 $\left(X,\mathcal M,\mu\right)$ 是测度空间, $\left\{E_{j}\right\}_{j=1}^{\infty}\subset\mathcal M$. 证明 $\mu\left(\liminf_{j\to\infty}E_{j}\right)\le\liminf_{j\to\infty}\mu\left(E_{j}\right)$. 又若 $\mu\left(\bigcup_{j=1}^{\infty}E_{j}\right)<\infty$, 则 $\mu\left(\limsup_{j\to\infty}E_{j}\right)\ge\limsup_{j\to\infty}\mu\left(E_{j}\right)$.

**9.** 设 $\left(X,\mathcal M,\mu\right)$ 是测度空间, $E,F\in\mathcal M$. 证明 $\mu\left(E\right)+\mu\left(F\right)=\mu\left(E\cup F\right)+\mu\left(E\cap F\right)$.

**10.** 给定测度空间 $\left(X,\mathcal M,\mu\right)$ 与 $E\in\mathcal M$, 对 $A\in\mathcal M$ 定义 $\mu_{E}\left(A\right):=\mu\left(A\cap E\right)$. 证明 $\mu_{E}$ 是一个测度.

**12.** 设 $\left(X,\mathcal M,\mu\right)$ 是有限测度空间.

(a) 若 $E,F\in\mathcal M$ 且 $\mu\left(E\triangle F\right)=0$, 则 $\mu\left(E\right)=\mu\left(F\right)$.

(b) 定义 $E\sim F$ 当且仅当 $\mu\left(E\triangle F\right)=0$, 则 $\sim$ 是 $\mathcal M$ 上的等价关系.

(c) 对 $E,F\in\mathcal M$, 定义 $\rho\left(E,F\right):=\mu\left(E\triangle F\right)$. 证明 $\rho\left(E,F\right)\le\rho\left(E,G\right)+\rho\left(F,G\right)$, 从而 $\rho$ 在商空间 $\mathcal M/\sim$ 上定义了一个度量.

### 解答 习题十

#### 8

记 $F_{n}:=\bigcap_{j=n}^{\infty}E_{j}$. 由**定义 1.3.3** (下极限), $\liminf_{j\to\infty}E_{j}=\bigcup_{n=1}^{\infty}F_{n}$; 且 $\left\{F_{n}\right\}$ 单调递增. 由**命题 5.2.4** (下连续性),

$$
\begin{aligned}\mu\left(\liminf_{j\to\infty}E_{j}\right)&=\mu\left(\bigcup_{n=1}^{\infty}F_{n}\right)\\&=\lim_{n\to\infty}\mu\left(F_{n}\right).
\end{aligned}
$$

又因 $F_{n}\subset E_{j}$ 对一切 $j\ge n$, 由**命题 5.2.2** (单调性) 得 $\mu\left(F_{n}\right)\le\inf_{j\ge n}\mu\left(E_{j}\right)$, 故

$$
\begin{aligned}\mu\left(\liminf_{j\to\infty}E_{j}\right)&=\lim_{n\to\infty}\mu\left(F_{n}\right)\\&\le\lim_{n\to\infty}\inf_{j\ge n}\mu\left(E_{j}\right)\\&=\liminf_{j\to\infty}\mu\left(E_{j}\right).
\end{aligned}
$$

记 $G_{n}:=\bigcup_{j=n}^{\infty}E_{j}$. 由**定义 1.3.1** (上极限), $\limsup_{j\to\infty}E_{j}=\bigcap_{n=1}^{\infty}G_{n}$; 且 $\left\{G_{n}\right\}$ 单调递减. 因 $\mu\left(G_{1}\right)=\mu\left(\bigcup_{j=1}^{\infty}E_{j}\right)<\infty$, 由**命题 5.2.5** (上连续性),

$$
\begin{aligned}\mu\left(\limsup_{j\to\infty}E_{j}\right)&=\mu\left(\bigcap_{n=1}^{\infty}G_{n}\right)\\&=\lim_{n\to\infty}\mu\left(G_{n}\right).
\end{aligned}
$$

又因 $G_{n}\supset E_{j}$ 对一切 $j\ge n$, 由单调性得 $\mu\left(G_{n}\right)\ge\sup_{j\ge n}\mu\left(E_{j}\right)$, 故

$$
\begin{aligned}\mu\left(\limsup_{j\to\infty}E_{j}\right)&=\lim_{n\to\infty}\mu\left(G_{n}\right)\\&\ge\lim_{n\to\infty}\sup_{j\ge n}\mu\left(E_{j}\right)\\&=\limsup_{j\to\infty}\mu\left(E_{j}\right).
\end{aligned}
$$

两不等式得证. $\blacksquare$

#### 9

$$
E\cup F=\left(E\cap F\right)\cup\left(E\setminus F\right)\cup\left(F\setminus E\right),
$$

右侧三集合两两不交. 由**命题 5.2.1** (有限可加性),

$$
\mu\left(E\cup F\right)=\mu\left(E\cap F\right)+\mu\left(E\setminus F\right)+\mu\left(F\setminus E\right).
$$

又 $E=\left(E\cap F\right)\cup\left(E\setminus F\right)$, $F=\left(E\cap F\right)\cup\left(F\setminus E\right)$ 均为两两不交分解, 故

$$
\begin{aligned}\mu\left(E\right)+\mu\left(F\right)&=2\mu\left(E\cap F\right)+\mu\left(E\setminus F\right)+\mu\left(F\setminus E\right)\\&=\mu\left(E\cup F\right)+\mu\left(E\cap F\right).
\end{aligned}
$$

等式得证. $\blacksquare$

#### 10

逐条验证**定义 5.1.2**:

(1) **非负性**: $\mu_{E}\left(A\right)=\mu\left(A\cap E\right)\ge0$ 对一切 $A\in\mathcal M$.

(2) **零空集性**: $\mu_{E}\left(\varnothing\right)=\mu\left(\varnothing\cap E\right)=\mu\left(\varnothing\right)=0$.

(3) **可数可加性**: 设 $\left\{A_{j}\right\}_{j=1}^{\infty}\subset\mathcal M$ 两两不交, 则 $\left\{A_{j}\cap E\right\}$ 亦两两不交, 由 $\mu$ 的可数可加性

$$
\begin{aligned}\mu_{E}\left(\bigcup_{j=1}^{\infty}A_{j}\right)&=\mu\left(\left(\bigcup_{j=1}^{\infty}A_{j}\right)\cap E\right)\\&=\mu\left(\bigcup_{j=1}^{\infty}\left(A_{j}\cap E\right)\right)\\&=\sum_{j=1}^{\infty}\mu\left(A_{j}\cap E\right)\\&=\sum_{j=1}^{\infty}\mu_{E}\left(A_{j}\right).
\end{aligned}
$$

故 $\mu_{E}$ 是测度. $\blacksquare$

#### 12

**(a)** $E=\left(E\cap F\right)\cup\left(E\setminus F\right)$, $F=\left(E\cap F\right)\cup\left(F\setminus E\right)$ 均为两两不交分解, 由**命题 5.2.1** (有限可加性),

$$
\begin{aligned}\mu\left(E\right)&=\mu\left(E\cap F\right)+\mu\left(E\setminus F\right),\\\mu\left(F\right)&=\mu\left(E\cap F\right)+\mu\left(F\setminus E\right).
\end{aligned}
$$

又 $E\setminus F\subset E\triangle F$, $F\setminus E\subset E\triangle F$, 由**命题 5.2.2** (单调性), $\mu\left(E\setminus F\right)\le\mu\left(E\triangle F\right)=0$, 同理 $\mu\left(F\setminus E\right)=0$. 故 $\mu\left(E\right)=\mu\left(E\cap F\right)=\mu\left(F\right)$. $\blacksquare$

**(b)** 验证等价关系的三条性质:

(1) **自反性**: $\mu\left(E\triangle E\right)=\mu\left(\varnothing\right)=0$, 故 $E\sim E$.

(2) **对称性**: $E\triangle F=F\triangle E$, 故 $E\sim F\iff F\sim E$.

(3) **传递性**: 因 $E\triangle G\subset\left(E\triangle F\right)\cup\left(F\triangle G\right)$, 由**命题 5.2.3** (次可数可加性), $\mu\left(E\triangle G\right)\le\mu\left(E\triangle F\right)+\mu\left(F\triangle G\right)=0$, 故 $E\sim G$.

故 $\sim$ 是 $\mathcal M$ 上的等价关系. $\blacksquare$

**(c)** 对称性与非负性显然: $\rho\left(E,F\right)=\rho\left(F,E\right)\ge0$, $\rho\left(E,E\right)=0$. 又 $E\triangle G\subset\left(E\triangle F\right)\cup\left(F\triangle G\right)$, 由**命题 5.2.3** (次可数可加性),

$$
\begin{aligned}\rho\left(E,G\right)&=\mu\left(E\triangle G\right)\\&\le\mu\left(E\triangle F\right)+\mu\left(F\triangle G\right)\\&=\rho\left(E,F\right)+\rho\left(F,G\right).
\end{aligned}
$$

最后验证良定义与正定性: 若 $E\sim E'$, $F\sim F'$ (即 $\mu\left(E\triangle E'\right)=\mu\left(F\triangle F'\right)=0$), 则

$$
E\triangle F\subset\left(E\triangle E'\right)\cup\left(E'\triangle F'\right)\cup\left(F'\triangle F\right),
$$

故 $\rho\left(E,F\right)\le0+\rho\left(E',F'\right)+0=\rho\left(E',F'\right)$; 对称地 $\rho\left(E',F'\right)\le\rho\left(E,F\right)$, 故 $\rho\left(E,F\right)=\rho\left(E',F'\right)$, 即 $\rho$ 良定义于商空间 $\mathcal M/\sim$. 又 $\rho\left(E,F\right)=0\iff\mu\left(E\triangle F\right)=0\iff E\sim F$, 故 $\rho$ 是 $\mathcal M/\sim$ 上的度量. $\blacksquare$
