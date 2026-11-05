# week2

> **定理 1.2.9 (德摩根定律)**
> 
> $\left(A\cup B\right)^{c}=A^{c}\cap B^{c}$, $\left(A\cap B\right)^{c}=A^{c}\cup B^{c}$.

> **定义 1.3.1 (上极限)**
> 
> 集列 $\left\{E_{n}\right\}$ 的上极限定义为

$$
\overline{\lim}_{n\to\infty}E_{n}=\left\{x:x\text{ 属于无穷多个 }E_{n}\right\}=\bigcap_{n=1}^{\infty}\bigcup_{k=n}^{\infty}E_{k}.
$$

> **定义 1.3.3 (下极限)**
> 
> 集列 $\left\{E_{n}\right\}$ 的下极限定义为

$$
\underline{\lim}_{n\to\infty}E_{n}=\left\{x:x\text{ 仅不属于有限多个 }E_{n}\right\}=\bigcup_{n=1}^{\infty}\bigcap_{k=n}^{\infty}E_{k}.
$$

> **定理 2.4.2 (原像运算的性质)**
> 
> 设 $f:A\to B$, 则 $f^{-1}\left(B_{1}\cup B_{2}\right)=f^{-1}\left(B_{1}\right)\cup f^{-1}\left(B_{2}\right)$, $f^{-1}\left(B_{1}\cap B_{2}\right)=f^{-1}\left(B_{1}\right)\cap f^{-1}\left(B_{2}\right)$, $f^{-1}\left(B^{c}\right)=\left(f^{-1}\left(B\right)\right)^{c}$, $f^{-1}\left(\bigcup_{\alpha\in I}B_{\alpha}\right)=\bigcup_{\alpha\in I}f^{-1}\left(B_{\alpha}\right)$, $f^{-1}\left(\bigcap_{\alpha\in I}B_{\alpha}\right)=\bigcap_{\alpha\in I}f^{-1}\left(B_{\alpha}\right)$.

> **定理 3.2.1 (实数中开集的构造)**
> 
> 设 $U\subset\mathbb R$ 是非空开集, 则存在一列互不相交的开区间 $\left\{I_{n}\right\}_{n=1}^{\infty}$, 使 $U=\bigcup_{n=1}^{\infty}I_{n}$; 且此表示在重排意义下唯一.

> **定义 4.1.1 (集合代数)**
> 
> 设 $X$ 是非空集合, $\mathcal A\subset\mathcal P\left(X\right)$. 称 $\mathcal A$ 为 $X$ 上的一个集合代数, 若满足: (1) $X\in\mathcal A$; (2) 对差运算封闭: $A,B\in\mathcal A\Rightarrow A\setminus B\in\mathcal A$; (3) 对有限并封闭: $A,B\in\mathcal A\Rightarrow A\cup B\in\mathcal A$.

> **命题 4.1.2 (代数的等价定义)**
> 
> 设 $\mathcal A\subset\mathcal P\left(X\right)$, 则以下条件等价: (1) $\mathcal A$ 是代数; (2) $\mathcal A$ 满足: (a) $X\in\mathcal A$; (b) 对补运算封闭: $A\in\mathcal A\Rightarrow A^{c}=X\setminus A\in\mathcal A$; (c) 对有限并封闭: $A,B\in\mathcal A\Rightarrow A\cup B\in\mathcal A$.

> **定义 4.1.3 ($\sigma$-代数)**
> 
> 设 $X$ 非空, $\mathcal F\subset\mathcal P\left(X\right)$. 称 $\mathcal F$ 为 $X$ 上的一个 $\sigma$-代数, 若满足: (1) $X\in\mathcal F$; (2) 对补运算封闭: $A\in\mathcal F\Rightarrow A^{c}\in\mathcal F$; (3) 对可数并封闭: $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal F\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal F$.

> **定义 4.2.1 (生成代数)**
> 
> 包含 $\mathcal E\subset\mathcal P\left(X\right)$ 的最小代数称为由 $\mathcal E$ 生成的代数, 记作 $\alpha\left(\mathcal E\right)$:

> **定义 4.2.2 (生成 $\sigma$-代数)**
> 
> 包含 $\mathcal E\subset\mathcal P\left(X\right)$ 的最小 $\sigma$-代数称为由 $\mathcal E$ 生成的 $\sigma$-代数, 记作 $\sigma\left(\mathcal E\right)$:

> **定义 4.3.2 (博雷尔 $\sigma$-代数)**
> 
> 设 $\left(X,\tau\right)$ 是拓扑空间, 由所有开集生成的 $\sigma$-代数称为博雷尔 $\sigma$-代数, 记作 $\mathcal B\left(X\right)$, 其中元素称为博雷尔集.

> **例 4.3.3 (实数上的博雷尔代数)**
> 
> 在 $\mathbb R$ 上, 以下集合族生成相同的博雷尔 $\sigma$-代数 $\mathcal B\left(\mathbb R\right)$: 所有开集 $\tau$, 所有闭集 $\mathcal F$, 所有开区间 $\left\{\left(a,b\right)\right\}$, 所有闭区间 $\left\{\left[a,b\right]\right\}$, 所有左开右闭区间 $\left\{\left(a,b\right]\right\}$, 即

> **定义 4.5.1 (可测矩形与乘积 $\sigma$-代数)**
> 
> 设 $\left(X,\mathcal F\right)$, $\left(Y,\mathcal G\right)$ 为可测空间. $A\times B\subseteq X\times Y$ 称为可测矩形, 若 $A\in\mathcal F$ 且 $B\in\mathcal G$. 乘积 $\sigma$-代数为包含所有可测矩形的最小 $\sigma$-代数:

> **定理 4.5.3 (截面可测性)**
> 
> 若 $E\in\mathcal F\otimes\mathcal G$, 则对任意 $x\in X$, $y\in Y$, 其截面都可测:

> **定理 4.5.4 (博雷尔集的乘积)**
> 
> 对欧氏空间中的博雷尔 $\sigma$-代数, 有

> **定义 4.5.7 (任意乘积 $\sigma$-代数)**
> 
> 设 $\left\{\left(X_{\alpha},\mathcal F_{\alpha}\right)\right\}_{\alpha\in I}$ 是一族可测空间, 乘积 $\sigma$-代数 $\bigotimes_{\alpha\in I}\mathcal F_{\alpha}$ 是由所有柱集

> **定义 5.1.2 (测度)**
> 
> 设 $\left(X,\mathcal F\right)$ 是一个可测空间. 函数 $\mu:\mathcal F\to\left[0,+\infty\right]$ 称为 $\left(X,\mathcal F\right)$ 上的一个测度, 如果满足: (1) 非负性: $\mu\left(E\right)\ge0$ 对一切 $E\in\mathcal F$ 成立; (2) 零空集性: $\mu\left(\emptyset\right)=0$; (3) 可数可加性 ($\sigma$-可加性): 对任意可数个两两不交的集合 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$, 有 $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **命题 5.2.1 (有限可加性)**
> 
> 设 $\mu$ 是 $\left(X,\mathcal F\right)$ 上的测度, $E_{1},\dots,E_{n}\in\mathcal F$ 是两两不交的集合, 则

$$
\mu\left(\bigcup_{k=1}^{n}E_{k}\right)=\sum_{k=1}^{n}\mu\left(E_{k}\right).
$$

> **命题 5.2.2 (单调性)**
> 
> 设 $\mu$ 是测度, $E,F\in\mathcal F$ 且 $E\subset F$, 则 $\mu\left(E\right)\le\mu\left(F\right)$. 若进一步 $\mu\left(E\right)< +\infty$, 则 $\mu\left(F\setminus E\right)=\mu\left(F\right)-\mu\left(E\right)$.

> **命题 5.2.3 (次可数可加性)**
> 
> 设 $\mu$ 是测度, $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$ 是任意可数个集合 (不一定两两不交), 则

$$
\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)\le\sum_{n=1}^{\infty}\mu\left(E_{n}\right).
$$

> **命题 5.2.4 (下连续性)**
> 
> 设 $\mu$ 是测度, $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$ 是单调递增的集合序列 (即 $E_{1}\subset E_{2}\subset\cdots$), 则

$$
\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\lim_{n\to\infty}\mu\left(E_{n}\right).
$$

> **命题 5.2.5 (上连续性)**
> 
> 设 $\mu$ 是测度, $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$ 是单调递减的集合序列 (即 $E_{1}\supset E_{2}\supset\cdots$), 且存在某个 $m$ 使得 $\mu\left(E_{m}\right)< +\infty$, 则

$$
\mu\left(\bigcap_{n=1}^{\infty}E_{n}\right)=\lim_{n\to\infty}\mu\left(E_{n}\right).
$$

> **定义 5.4.1 (零集)**
> 
> 设 $\left(X,\mathcal F,\mu\right)$ 是测度空间. 集合 $N\in\mathcal F$ 称为零集, 若 $\mu\left(N\right)=0$.

> **定义 5.4.2 (零测度集)**
> 
> 集合 $A\subset X$ 称为零测度集, 若存在 $N\in\mathcal F$ 使得 $A\subset N$ 且 $\mu\left(N\right)=0$.

> **定义 5.4.4 (完备测度)**
> 
> 测度空间 $\left(X,\mathcal F,\mu\right)$ 称为完备的, 若对任意满足 $\mu\left(N\right)=0$ 的 $N\in\mathcal F$, 以及任意 $A\subset N$, 都有 $A\in\mathcal F$.

> **定理 5.4.6 (测度完备化定理)**
> 
> 任意测度空间 $\left(X,\mathcal F,\mu\right)$ 都可以完备化, 即存在完备测度空间 $\left(X,\mathcal M,\overline\mu\right)$ 使得: (1) $\mathcal F\subset\mathcal M$; (2) $\overline\mu|_{\mathcal F}=\mu$; (3) $\mathcal M$ 是包含 $\mathcal F$ 的最小完备 $\sigma$-代数. 具体地, 令 $\mathcal N=\left\{N\in\mathcal F:\mu\left(N\right)=0\right\}$, $\mathcal M=\left\{A\subset X:\exists\,B\in\mathcal F,\ \exists\,N\in\mathcal N,\ B\subset A\subset B\cup N\right\}$, 并定义 $\overline\mu\left(A\right)=\mu\left(B\right)$.

## 1

设 $\left\{\left(X_{\alpha},\mathcal F_{\alpha}\right)\right\}_{\alpha\in I}$ 是一族可测空间. 假定 $\mathcal F_{\alpha}=\sigma\left(\mathcal E_{\alpha}\right)$, 其中 $\mathcal E_{\alpha}$ 为 $X_{\alpha}$ 的子集族. 证明

$$
\bigotimes_{\alpha\in I}\mathcal F_{\alpha}=\sigma\left(\left\{\pi_{\alpha}^{-1}\left(\mathcal E_{\alpha}\right):\alpha\in I\right\}\right),
$$

其中 $\pi_{\beta}:\prod_{\alpha\in I}X_{\alpha}\to X_{\beta}$ 为乘积空间到 $X_{\beta}$ 的坐标投影.

(这里 $\bigotimes_{\alpha\in I}\mathcal F_{\alpha}$ 按**定义 4.5.7 (任意乘积 $\sigma$-代数)**, 是由所有柱集 $\pi_{\beta}^{-1}\left(A_{\beta}\right)$, $A_{\beta}\in\mathcal F_{\beta}$, $\beta\in I$ 生成的 $\sigma$-代数.)

### 解答 1

记 $\mathscr G:=\sigma\left(\left\{\pi_{\alpha}^{-1}\left(\mathcal E_{\alpha}\right):\alpha\in I\right\}\right)$. 分两个包含关系证明.

($\subset$) $\bigotimes_{\alpha\in I}\mathcal F_{\alpha}\subseteq\mathscr G$.

固定 $\alpha\in I$, 考虑 $\pi_{\alpha}:\prod_{\beta\in I}X_{\beta}\to X_{\alpha}$, 定义集合族

$$
\mathscr C_{\alpha}:=\left\{A\subseteq X_{\alpha}:\pi_{\alpha}^{-1}\left(A\right)\in\mathscr G\right\}.
$$

由原像运算保持补与可数并 (**定理 2.4.2 (原像运算的性质)**), $\mathscr C_{\alpha}$ 是 $\sigma$-代数. 又因 $\pi_{\alpha}^{-1}\left(\mathcal E_{\alpha}\right)\subseteq\mathscr G$ 由 $\mathscr G$ 的定义, 故 $\mathcal E_{\alpha}\subseteq\mathscr C_{\alpha}$. 从而 $\mathscr C_{\alpha}$ 是含 $\mathcal E_{\alpha}$ 的 $\sigma$-代数, 故含 $\sigma\left(\mathcal E_{\alpha}\right)=\mathcal F_{\alpha}$. 即对一切 $A\in\mathcal F_{\alpha}$, 有 $\pi_{\alpha}^{-1}\left(A\right)\in\mathscr G$.

由于 $\alpha\in I$ 任意, 所有柱集 $\pi_{\alpha}^{-1}\left(A\right)$ ($A\in\mathcal F_{\alpha}$, $\alpha\in I$) 都在 $\mathscr G$ 中. 而 $\bigotimes_{\alpha\in I}\mathcal F_{\alpha}$ 是由这些柱集生成的 $\sigma$-代数, 故

$$
\bigotimes_{\alpha\in I}\mathcal F_{\alpha}\subseteq\mathscr G.
$$

($\supset$) $\mathscr G\subseteq\bigotimes_{\alpha\in I}\mathcal F_{\alpha}$.

固定 $\alpha\in I$. 对任意 $E_{\alpha}\in\mathcal E_{\alpha}$, $\pi_{\alpha}^{-1}\left(E_{\alpha}\right)$ 恰是一个柱集 (**定义 4.5.7 (任意乘积 $\sigma$-代数)** 中取 $A_{\beta}=E_{\alpha}$ 当 $\beta=\alpha$), 故 $\pi_{\alpha}^{-1}\left(\mathcal E_{\alpha}\right)\subseteq\bigotimes_{\alpha\in I}\mathcal F_{\alpha}$. 于是所有生成元 $\pi_{\alpha}^{-1}\left(E_{\alpha}\right)$ ($\alpha\in I$) 都在乘积 $\sigma$-代数中, 而 $\bigotimes_{\alpha\in I}\mathcal F_{\alpha}$ 是含这些集合的 $\sigma$-代数, 故其生成的 $\sigma$-代数

$$
\mathscr G\subseteq\bigotimes_{\alpha\in I}\mathcal F_{\alpha}.
$$

两方向结合, 即

$$
\bigotimes_{\alpha\in I}\mathcal F_{\alpha}=\sigma\left(\left\{\pi_{\alpha}^{-1}\left(\mathcal E_{\alpha}\right):\alpha\in I\right\}\right).
$$

$\blacksquare$

## 2

证明**定理 5.4.6 (测度完备化定理)**: 任意测度空间 $\left(X,\mathcal F,\mu\right)$ 都可以完备化. 即存在完备测度空间 $\left(X,\mathcal M,\overline\mu\right)$ 使得:

(1) $\mathcal F\subset\mathcal M$;

(2) $\overline\mu|_{\mathcal F}=\mu$;

(3) $\mathcal M$ 是包含 $\mathcal F$ 的最小完备 $\sigma$-代数.

### 解答 2

记 $\mathcal N=\left\{N\in\mathcal F:\mu\left(N\right)=0\right\}$ 为零集全体 (**定义 5.4.1 (零集)**). 定义

$$
\mathcal M:=\left\{A\subset X:\exists\,B\in\mathcal F,\exists\,N\in\mathcal F,\mu\left(N\right)=0,\text{使 }B\subset A\subset B\cup N\right\},
$$

即 $A\in\mathcal M$ 当且仅当 $A$ 与某个可测集 $B$ 相差一个零测度集 (**定义 5.4.2 (零测度集)**). 分六步证明.

1. $\mathcal M$ 是 $\sigma$-代数. 逐条验证**定义 4.1.3 ($\sigma$-代数)**:

(1) $X\in\mathcal M$: 取 $B=X$, $N=\varnothing$, 则 $X\subset X\subset X\cup\varnothing$.

(2) 补运算封闭: 设 $B\subset A\subset B\cup N$, $\mu\left(N\right)=0$. 则 $\left(B\cup N\right)^{c}\subset A^{c}\subset B^{c}$, 且

$$
B^{c}\setminus\left(B\cup N\right)^{c}=B^{c}\cap\left(B\cup N\right)=B^{c}\cap N\subset N,
$$

故由**命题 5.2.2 (单调性)** 得 $\mu\left(B^{c}\setminus\left(B\cup N\right)^{c}\right)\le\mu\left(N\right)=0$. 于是 $A^{c}\in\mathcal M$ (取 $B'=\left(B\cup N\right)^{c}\in\mathcal F$, $N'=B^{c}\setminus\left(B\cup N\right)^{c}$).

(3) 可数并封闭: 设 $B_{n}\subset A_{n}\subset B_{n}\cup N_{n}$, $\mu\left(N_{n}\right)=0$. 则 $\bigcup_{n}B_{n}\subset\bigcup_{n}A_{n}\subset\left(\bigcup_{n}B_{n}\right)\cup\left(\bigcup_{n}N_{n}\right)$. 由**命题 5.2.3 (次可数可加性)**, $\mu\left(\bigcup_{n}N_{n}\right)\le\sum_{n}\mu\left(N_{n}\right)=0$, 故 $\bigcup_{n}N_{n}$ 是零测度集, 从而 $\bigcup_{n}A_{n}\in\mathcal M$.

故 $\mathcal M$ 是 $\sigma$-代数.

2. 定义 $\overline\mu:\mathcal M\to\left[0,+\infty\right]$, $\overline\mu\left(A\right):=\mu\left(B\right)$, 其中 $B\subset A\subset B\cup N$, $\mu\left(N\right)=0$. 先证良定义: 设 $B_{1}\subset A\subset B_{1}\cup N_{1}$ 与 $B_{2}\subset A\subset B_{2}\cup N_{2}$, $\mu\left(N_{1}\right)=\mu\left(N_{2}\right)=0$. 由 $B_{1}\subset A\subset B_{2}\cup N_{2}$ 得 $B_{1}\setminus B_{2}\subset N_{2}$, 故 $\mu\left(B_{1}\setminus B_{2}\right)\le\mu\left(N_{2}\right)=0$; 同理 $\mu\left(B_{2}\setminus B_{1}\right)=0$. 由**命题 5.2.1 (有限可加性)** 与**命题 5.2.2 (单调性)**,

$$
\mu\left(B_{1}\right)=\mu\left(B_{1}\cap B_{2}\right)+\mu\left(B_{1}\setminus B_{2}\right)=\mu\left(B_{1}\cap B_{2}\right)=\mu\left(B_{2}\right).
$$

故 $\overline\mu$ 良定义.

3. $\overline\mu$ 是测度. 逐条验证**定义 5.1.2 (测度)**: 非负性显然. 零空集性: $\overline\mu\left(\varnothing\right)=\mu\left(\varnothing\right)=0$. 可数可加性: 设 $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal M$ 两两不交, 写 $A_{n}=B_{n}\cup N_{n}$ ($B_{n}\in\mathcal F$, $N_{n}\subset N_{n}'\in\mathcal N$). 则 $\bigcup_{n}A_{n}=\left(\bigcup_{n}B_{n}\right)\cup\left(\bigcup_{n}N_{n}\right)\in\mathcal M$, 且 $\left\{B_{n}\right\}$ 两两不交 (因 $B_{n}\subset A_{n}$), 由 $\mu$ 的可数可加性

$$
\overline\mu\left(\bigcup_{n}A_{n}\right)=\mu\left(\bigcup_{n}B_{n}\right)=\sum_{n}\mu\left(B_{n}\right)=\sum_{n}\overline\mu\left(A_{n}\right).
$$

4. 延拓性: 对 $B\in\mathcal F$, 因 $B=B\cup\varnothing\in\mathcal M$, 故 $\overline\mu\left(B\right)=\mu\left(B\right)$, 即 $\overline\mu|_{\mathcal F}=\mu$.

5. 完备性 (定义 5.4.4 (完备测度)): 设 $\overline\mu\left(A\right)=0$, 即 $A=B\cup N$ 且 $\mu\left(B\right)=0$, $N\subset N_{0}\in\mathcal N$. 则 $A\subset B\cup N_{0}$, 且由**命题 5.2.3 (次可数可加性)**, $\mu\left(B\cup N_{0}\right)\le\mu\left(B\right)+\mu\left(N_{0}\right)=0$, 故 $A$ 是某个零测度集之子集. 于是 $A=\varnothing\cup A\in\mathcal M$, 且 $A$ 的任意子集 $C\subset A$ 亦满足 $C\subset B\cup N_{0}$, 故 $C\in\mathcal M$. 因此 $\mathcal M$ 完备.

6. 最小性: 设 $\mathcal M'$ 是任一包含 $\mathcal F$ 的完备 $\sigma$-代数. 对 $A=B\cup N\in\mathcal M$ ($B\in\mathcal F$, $N\subset N_{0}\in\mathcal N$), 因 $N_{0}\in\mathcal F\subset\mathcal M'$ 且 $\mu\left(N_{0}\right)=0$, 由 $\mathcal M'$ 的完备性得 $N\in\mathcal M'$; 又 $B\in\mathcal F\subset\mathcal M'$, 故 $A=B\cup N\in\mathcal M'$. 因此 $\mathcal M\subset\mathcal M'$. 故 $\mathcal M$ 是包含 $\mathcal F$ 的最小完备 $\sigma$-代数.

综上, $\left(X,\mathcal M,\overline\mu\right)$ 是满足 (1)(2)(3) 的完备测度空间, 定理得证. $\blacksquare$

## 3

设 $\left(X,\mathcal M,\mu\right)$ 是测度空间, $\left\{E_{j}\right\}_{j=1}^{\infty}\subset\mathcal M$. 证明 $\mu\left(\liminf_{j\to\infty}E_{j}\right)\le\liminf_{j\to\infty}\mu\left(E_{j}\right)$. 又若 $\mu\left(\bigcup_{j=1}^{\infty}E_{j}\right)< \infty$, 则 $\mu\left(\limsup_{j\to\infty}E_{j}\right)\ge\limsup_{j\to\infty}\mu\left(E_{j}\right)$.

### 解答 3

记 $F_{n}:=\bigcap_{j=n}^{\infty}E_{j}$. 由**定义 1.3.3 (下极限)**, $\liminf_{j\to\infty}E_{j}=\bigcup_{n=1}^{\infty}F_{n}$; 且 $\left\{F_{n}\right\}$ 单调递增. 由**命题 5.2.4 (下连续性)**,

$$
\mu\left(\liminf_{j\to\infty}E_{j}\right)=\mu\left(\bigcup_{n=1}^{\infty}F_{n}\right)=\lim_{n\to\infty}\mu\left(F_{n}\right).
$$

又因 $F_{n}\subset E_{j}$ 对一切 $j\ge n$, 由**命题 5.2.2 (单调性)** 得 $\mu\left(F_{n}\right)\le\inf_{j\ge n}\mu\left(E_{j}\right)$, 故

$$
\mu\left(\liminf_{j\to\infty}E_{j}\right)=\lim_{n\to\infty}\mu\left(F_{n}\right)\le\lim_{n\to\infty}\inf_{j\ge n}\mu\left(E_{j}\right)=\liminf_{j\to\infty}\mu\left(E_{j}\right).
$$

记 $G_{n}:=\bigcup_{j=n}^{\infty}E_{j}$. 由**定义 1.3.1 (上极限)**, $\limsup_{j\to\infty}E_{j}=\bigcap_{n=1}^{\infty}G_{n}$; 且 $\left\{G_{n}\right\}$ 单调递减. 因 $\mu\left(G_{1}\right)=\mu\left(\bigcup_{j=1}^{\infty}E_{j}\right)< \infty$, 由**命题 5.2.5 (上连续性)**,

$$
\mu\left(\limsup_{j\to\infty}E_{j}\right)=\mu\left(\bigcap_{n=1}^{\infty}G_{n}\right)=\lim_{n\to\infty}\mu\left(G_{n}\right).
$$

又因 $G_{n}\supset E_{j}$ 对一切 $j\ge n$, 由单调性得 $\mu\left(G_{n}\right)\ge\sup_{j\ge n}\mu\left(E_{j}\right)$, 故

$$
\mu\left(\limsup_{j\to\infty}E_{j}\right)=\lim_{n\to\infty}\mu\left(G_{n}\right)\ge\lim_{n\to\infty}\sup_{j\ge n}\mu\left(E_{j}\right)=\limsup_{j\to\infty}\mu\left(E_{j}\right).
$$

两不等式得证. $\blacksquare$

## 4

设 $\left(X,\mathcal M,\mu\right)$ 是测度空间, $E,F\in\mathcal M$. 证明 $\mu\left(E\right)+\mu\left(F\right)=\mu\left(E\cup F\right)+\mu\left(E\cap F\right)$.

### 解答 4

$$
E\cup F=\left(E\cap F\right)\cup\left(E\setminus F\right)\cup\left(F\setminus E\right),
$$

右侧三集合两两不交. 由**命题 5.2.1 (有限可加性)**,

$$
\mu\left(E\cup F\right)=\mu\left(E\cap F\right)+\mu\left(E\setminus F\right)+\mu\left(F\setminus E\right).
$$

又 $E=\left(E\cap F\right)\cup\left(E\setminus F\right)$, $F=\left(E\cap F\right)\cup\left(F\setminus E\right)$ 均为两两不交分解, 故

$$
\mu\left(E\right)+\mu\left(F\right)=2\mu\left(E\cap F\right)+\mu\left(E\setminus F\right)+\mu\left(F\setminus E\right)=\mu\left(E\cup F\right)+\mu\left(E\cap F\right).
$$

等式得证. $\blacksquare$

## 5

给定测度空间 $\left(X,\mathcal M,\mu\right)$ 与 $E\in\mathcal M$, 对 $A\in\mathcal M$ 定义 $\mu_{E}\left(A\right):=\mu\left(A\cap E\right)$. 证明 $\mu_{E}$ 是一个测度.

### 解答 5

逐条验证**定义 5.1.2 (测度)**:

(1) 非负性: $\mu_{E}\left(A\right)=\mu\left(A\cap E\right)\ge0$ 对一切 $A\in\mathcal M$.

(2) 零空集性: $\mu_{E}\left(\varnothing\right)=\mu\left(\varnothing\cap E\right)=\mu\left(\varnothing\right)=0$.

(3) 可数可加性: 设 $\left\{A_{j}\right\}_{j=1}^{\infty}\subset\mathcal M$ 两两不交, 则 $\left\{A_{j}\cap E\right\}$ 亦两两不交, 由 $\mu$ 的可数可加性

$$
\mu_{E}\left(\bigcup_{j=1}^{\infty}A_{j}\right)=\mu\left(\left(\bigcup_{j=1}^{\infty}A_{j}\right)\cap E\right)=\mu\left(\bigcup_{j=1}^{\infty}\left(A_{j}\cap E\right)\right)=\sum_{j=1}^{\infty}\mu\left(A_{j}\cap E\right)=\sum_{j=1}^{\infty}\mu_{E}\left(A_{j}\right).
$$

故 $\mu_{E}$ 是测度. $\blacksquare$
