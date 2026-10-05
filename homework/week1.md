# 作业 1

> **定理 1.2.9** (德摩根定律)<br>$$\begin{aligned}\left(A\cup B\right)^{c}&=A^{c}\cap B^{c},\\\left(A\cap B\right)^{c}&=A^{c}\cup B^{c}.\end{aligned}$$

> **定理 2.4.2** (原像运算的性质)<br>设 $f:A\to B$, 则 $$\begin{aligned}f^{-1}\left(B_{1}\cup B_{2}\right)&=f^{-1}\left(B_{1}\right)\cup f^{-1}\left(B_{2}\right),\\f^{-1}\left(B_{1}\cap B_{2}\right)&=f^{-1}\left(B_{1}\right)\cap f^{-1}\left(B_{2}\right),\\f^{-1}\left(B^{c}\right)&=\left(f^{-1}\left(B\right)\right)^{c},\\f^{-1}\left(\bigcup_{\alpha\in I}B_{\alpha}\right)&=\bigcup_{\alpha\in I}f^{-1}\left(B_{\alpha}\right),\\f^{-1}\left(\bigcap_{\alpha\in I}B_{\alpha}\right)&=\bigcap_{\alpha\in I}f^{-1}\left(B_{\alpha}\right).\end{aligned}$$

> **定理 3.2.1** (实数中开集的构造)<br>设 $U\subset\mathbb R$ 是非空开集, 则存在一列互不相交的开区间 $\left\{I_{n}\right\}_{n=1}^{\infty}$, 使 $U=\bigcup_{n=1}^{\infty}I_{n}$; 且此表示在重排意义下唯一.

> **定义 4.1.1** (集合代数)<br>设 $X$ 非空, $\mathcal A\subset\mathcal P\left(X\right)$. 称 $\mathcal A$ 为 $X$ 上的一个**集合代数** (布尔代数), 若满足:<br>(1) $X\in\mathcal A$;<br>(2) 对差运算封闭: $A,B\in\mathcal A\Rightarrow A\setminus B\in\mathcal A$;<br>(3) 对有限并封闭: $A,B\in\mathcal A\Rightarrow A\cup B\in\mathcal A$.

> **命题 4.1.2** (代数的等价定义)<br>设 $\mathcal A\subset\mathcal P\left(X\right)$, 则以下条件等价:<br>(1) $\mathcal A$ 是代数;<br>(2) $\mathcal A$ 满足: (a) $X\in\mathcal A$; (b) 对补运算封闭: $A\in\mathcal A\Rightarrow A^{c}=X\setminus A\in\mathcal A$; (c) 对有限并封闭: $A,B\in\mathcal A\Rightarrow A\cup B\in\mathcal A$.

> **定义 4.1.3** ($\sigma$-代数)<br>设 $X$ 非空, $\mathcal F\subset\mathcal P\left(X\right)$. 称 $\mathcal F$ 为 $X$ 上的一个 **$\sigma$-代数**, 若满足:<br>(1) $X\in\mathcal F$;<br>(2) 对补运算封闭: $A\in\mathcal F\Rightarrow A^{c}\in\mathcal F$;<br>(3) 对可数并封闭: $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal F\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal F$.<br>称 $\left(X,\mathcal F\right)$ 为**可测空间**, $\mathcal F$ 中的元素称为**可测集**.

> **定义 4.2.1** (生成代数)<br>包含 $\mathcal E\subset\mathcal P\left(X\right)$ 的最小代数称为由 $\mathcal E$ 生成的代数, 记作 $\alpha\left(\mathcal E\right)$: $$\alpha\left(\mathcal E\right)=\bigcap\left\{\mathcal A\subset\mathcal P\left(X\right):\mathcal A\text{ 是代数且 }\mathcal E\subset\mathcal A\right\}.$$

> **定义 4.2.2** (生成 $\sigma$-代数)<br>包含 $\mathcal E\subset\mathcal P\left(X\right)$ 的最小 $\sigma$-代数称为由 $\mathcal E$ 生成的 $\sigma$-代数, 记作 $\sigma\left(\mathcal E\right)$: $$\sigma\left(\mathcal E\right)=\bigcap\left\{\mathcal F\subset\mathcal P\left(X\right):\mathcal F\text{ 是 $\sigma$-代数且 }\mathcal E\subset\mathcal F\right\}.$$

> **定义 4.3.2** (博雷尔 $\sigma$-代数)<br>设 $\left(X,\tau\right)$ 是拓扑空间, 由所有开集生成的 $\sigma$-代数称为 **博雷尔 $\sigma$-代数**, 记作 $\mathcal B\left(X\right)$, 其中元素称为 **博雷尔集**.

> **例 4.3.3** (实数上的博雷尔代数)<br>在 $\mathbb R$ 上, 以下集合族生成相同的博雷尔 $\sigma$-代数 $\mathcal B\left(\mathbb R\right)$: 所有开集 $\tau$、所有闭集 $\mathcal F$、所有开区间 $\left\{\left(a,b\right)\right\}$、所有闭区间 $\left\{\left[a,b\right]\right\}$、所有左开右闭区间 $\left\{\left(a,b\right]\right\}$, 即 $$\begin{aligned}&\quad\;\mathcal B\left(\mathbb R\right)\\&=\sigma\left(\tau\right)\\&=\sigma\left(\mathcal F\right)\\&=\sigma\left(\left\{\left(a,b\right)\right\}\right)\\&=\sigma\left(\left\{\left[a,b\right]\right\}\right)\\&=\sigma\left(\left\{\left(a,b\right]\right\}\right).\end{aligned}$$

> **定义 4.5.1 / 4.5.2** (可测矩形与乘积 $\sigma$-代数)<br>设 $\left(X,\mathcal F\right)$、$\left(Y,\mathcal G\right)$ 为可测空间. $A\times B\subseteq X\times Y$ 称为**可测矩形**, 若 $A\in\mathcal F$ 且 $B\in\mathcal G$.**乘积 $\sigma$-代数**为包含所有可测矩形的最小 $\sigma$-代数: $$\mathcal F\otimes\mathcal G:=\sigma\left(\left\{A\times B:A\in\mathcal F,B\in\mathcal G\right\}\right).$$

> **定理 4.5.3** (截面可测性)<br>若 $E\in\mathcal F\otimes\mathcal G$, 则对任意 $x\in X$、$y\in Y$, 其截面都可测: $$\begin{aligned}E_{x}&=\left\{y\in Y:\left(x,y\right)\in E\right\}\in\mathcal G,\\E^{y}&=\left\{x\in X:\left(x,y\right)\in E\right\}\in\mathcal F.\end{aligned}$$

> **定理 4.5.4** (博雷尔集的乘积)<br>对欧氏空间中的博雷尔 $\sigma$-代数, 有 $$\mathcal B\left(\mathbb R^{m}\right)\otimes\mathcal B\left(\mathbb R^{n}\right)=\mathcal B\left(\mathbb R^{m+n}\right).$$

> **定义 4.5.7** (任意乘积 $\sigma$-代数)<br>设 $\left\{\left(X_{\alpha},\mathcal F_{\alpha}\right)\right\}_{\alpha\in I}$ 是一族可测空间, 乘积 $\sigma$-代数 $\bigotimes_{\alpha\in I}\mathcal F_{\alpha}$ 是由所有**柱集** $$\left\{x=\left(x_{\alpha}\right)_{\alpha\in I}\in\prod_{\alpha\in I}X_{\alpha}:x_{\beta}\in A_{\beta}\right\},\quad A_{\beta}\in\mathcal F_{\beta},\quad\beta\in I$$ 生成的 $\sigma$-代数.

> **基础知识**<br>$\mathbb R^{m+n}$ 中每个开集可表为可数个开矩形的并: $O=\bigcup_{k=1}^{\infty}\left(U_{k}\times V_{k}\right)$, 其中 $U_{k}\subset\mathbb R^{m}$、$V_{k}\subset\mathbb R^{n}$ 为开集 (有理端点的矩形构成可数基).

### 习题一

设 $\mathcal A\subset\mathcal P\left(X\right)$, 证明**命题 4.1.2**: $\mathcal A$ 是代数, 当且仅当 $\mathcal A$ 满足

(a) $X\in\mathcal A$; (b) 对补运算封闭: $A\in\mathcal A\Rightarrow A^{c}\in\mathcal A$; (c) 对有限并封闭: $A,B\in\mathcal A\Rightarrow A\cup B\in\mathcal A$.

### 解答 习题一

依据**定义 4.1.1 (集合代数)** 与**命题 4.1.2**, 分两个方向证明.

**($\Rightarrow$)** 设 $\mathcal A$ 是代数, 则 $X\in\mathcal A$ (a) 成立, 有限并封闭 (c) 成立. 对补封闭 (b): 对任意 $A\in\mathcal A$, 由 $X,A\in\mathcal A$ 及差运算封闭, 得

$$
A^{c}=X\setminus A\in\mathcal A.
$$

故 (a)(b)(c) 均成立.

**($\Leftarrow$)** 设 (a)(b)(c) 成立. $X\in\mathcal A$ 即定义 4.1.1 (1); 有限并封闭即 (3). 只需验证差运算封闭 (2): 对任意 $A,B\in\mathcal A$, 由 (b) 得 $B^{c}\in\mathcal A$, 由 (c) 得 $A^{c}\cup B\in\mathcal A$, 再由 (b) 得

$$
\begin{aligned}
&\quad\;A\setminus B\\&=A\cap B^{c}\\&=\left(A^{c}\cup B\right)^{c}\in\mathcal A,
\end{aligned}
$$

其中第二式用到**定理 1.2.9 (德摩根定律)**. 故 $\mathcal A$ 是代数.

两方向结合, 命题得证. $\blacksquare$

### 习题二

证明: $\mathcal F$ 为 $\sigma$-代数, 当且仅当 $\mathcal F$ 为代数, 且对可数不交并封闭.

### 解答 习题二

**($\Rightarrow$)** 设 $\mathcal F$ 是 $\sigma$-代数 (**定义 4.1.3**). 则 $X\in\mathcal F$; 对补封闭 (b); 对可数并封闭, 特别地对有限并封闭 (c), 也对可数不交并封闭. 还需验证差运算封闭: 对 $A,B\in\mathcal F$, 由 (b)(c) 与 德摩根定律

$$
\begin{aligned}
&\quad\;A\setminus B\\&=A\cap B^{c}\\&=\left(A^{c}\cup B\right)^{c}\in\mathcal F.
\end{aligned}
$$

故由**命题 4.1.2** 得 $\mathcal F$ 是代数, 且显然对可数不交并封闭.

**($\Leftarrow$)** 设 $\mathcal F$ 是代数且对可数不交并封闭. 代数给出 $X\in\mathcal F$、对补封闭及有限并封闭; 只需再证对可数并封闭. 设 $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$, 作**不交化**:

$$
\begin{aligned}
B_{1}&:=A_{1},\\B_{n}&:=A_{n}\setminus\left(A_{1}\cup\cdots\cup A_{n-1}\right)\left(n\ge2\right).
\end{aligned}
$$

由代数的差运算与有限并封闭, 每个 $B_{n}\in\mathcal F$; 且 $\left\{B_{n}\right\}$ 两两不交, 并保持并集不变: $\bigcup_{n=1}^{\infty}B_{n}=\bigcup_{n=1}^{\infty}A_{n}$. 由可数不交并封闭,

$$
\bigcup_{n=1}^{\infty}A_{n}=\bigcup_{n=1}^{\infty}B_{n}\in\mathcal F.
$$

故 $\mathcal F$ 对可数并封闭, 是 $\sigma$-代数. $\blacksquare$

### 习题三

设 $\mathcal E\subset\mathcal P\left(X\right)$, 证明由 $\mathcal E$ 生成的代数

$$
\alpha\left(\mathcal E\right)=\bigcap\left\{\mathcal A\subset\mathcal P\left(X\right):\mathcal A\text{ 是代数且 }\mathcal E\subset\mathcal A\right\}
$$

是一个代数.

### 解答 习题三

记 $\mathscr C=\left\{\mathcal A\subset\mathcal P\left(X\right):\mathcal A\text{ 是代数且 }\mathcal E\subset\mathcal A\right\}$ 为所有含 $\mathcal E$ 的代数的全体. $\mathscr C$ 非空 (因 $\mathcal P\left(X\right)$ 是代数且含 $\mathcal E$), 故由**定义 4.2.1 (生成代数)**, $\alpha\left(\mathcal E\right)$ 良定义.

对 $\alpha\left(\mathcal E\right)$ 逐条验证**定义 4.1.1**:

(1) **$X\in\alpha\left(\mathcal E\right)$**: 每个 $\mathcal A\in\mathscr C$ 是代数, 故 $X\in\mathcal A$, 从而 $X$ 属于所有 $\mathcal A$ 之交, 即 $X\in\alpha\left(\mathcal E\right)$.

(2) **差运算封闭**: 设 $A,B\in\alpha\left(\mathcal E\right)$, 则对每个 $\mathcal A\in\mathscr C$ 有 $A,B\in\mathcal A$, 由 $\mathcal A$ 是代数得 $A\setminus B\in\mathcal A$. 因 $\mathcal A$ 任意, $A\setminus B\in\bigcap\mathscr C=\alpha\left(\mathcal E\right)$.

(3) **有限并封闭**: 同理, 对每个 $\mathcal A\in\mathscr C$ 有 $A\cup B\in\mathcal A$, 故 $A\cup B\in\alpha\left(\mathcal E\right)$.

故 $\alpha\left(\mathcal E\right)$ 是含 $\mathcal E$ 的代数. 又由定义其为所有含 $\mathcal E$ 的代数的交集, 故它是包含 $\mathcal E$ 的**最小**代数. $\blacksquare$

### 习题四

设 $\mathcal E\subset\mathcal P\left(X\right)$, 证明由 $\mathcal E$ 生成的 $\sigma$-代数

$$
\sigma\left(\mathcal E\right)=\bigcap\left\{\mathcal F\subset\mathcal P\left(X\right):\mathcal F\text{ 是 $\sigma$-代数且 }\mathcal E\subset\mathcal F\right\}
$$

是一个 $\sigma$-代数.

### 解答 习题四

记 $\mathscr C'=\left\{\mathcal F\subset\mathcal P\left(X\right):\mathcal F\text{ 是 }\sigma\text{-代数且 }\mathcal E\subset\mathcal F\right\}$. $\mathscr C'$ 非空 ($\mathcal P\left(X\right)$ 是 $\sigma$-代数且含 $\mathcal E$), 故由**定义 4.2.2 (生成 $\sigma$-代数)**, $\sigma\left(\mathcal E\right)$ 良定义.

逐条验证**定义 4.1.3**:

(1) **$X\in\sigma\left(\mathcal E\right)$**: 每个 $\mathcal F\in\mathscr C'$ 是 $\sigma$-代数, 含 $X$, 故 $X$ 属于其交集.

(2) **补运算封闭**: 设 $A\in\sigma\left(\mathcal E\right)$, 则对每个 $\mathcal F\in\mathscr C'$, $A\in\mathcal F$, 由 $\mathcal F$ 是 $\sigma$-代数得 $A^{c}\in\mathcal F$, 故 $A^{c}\in\sigma\left(\mathcal E\right)$.

(3) **可数并封闭**: 设 $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\sigma\left(\mathcal E\right)$, 则对每个 $\mathcal F\in\mathscr C'$, $\left\{A_{n}\right\}\subset\mathcal F$, 由 $\mathcal F$ 对可数并封闭得 $\bigcup_{n=1}^{\infty}A_{n}\in\mathcal F$, 故 $\bigcup_{n=1}^{\infty}A_{n}\in\sigma\left(\mathcal E\right)$.

故 $\sigma\left(\mathcal E\right)$ 是含 $\mathcal E$ 的 $\sigma$-代数, 且是**最小**的 (所有含 $\mathcal E$ 的 $\sigma$-代数之交). $\blacksquare$

### 习题五

在 $\mathbb R$ 上, 证明**例 4.3.3**: 以下集合族生成相同的博雷尔 $\sigma$-代数 $\mathcal B\left(\mathbb R\right)$:

所有开集 $\tau$、所有闭集 $\mathcal F$、所有开区间 $\left\{\left(a,b\right)\right\}$、所有闭区间 $\left\{\left[a,b\right]\right\}$、所有左开右闭区间 $\left\{\left(a,b\right]\right\}$.

即证明

$$
\begin{aligned}
&\quad\;\mathcal B\left(\mathbb R\right)\\&=\sigma\left(\tau\right)\\&=\sigma\left(\mathcal F\right)\\&=\sigma\left(\left\{\left(a,b\right)\right\}\right)\\&=\sigma\left(\left\{\left[a,b\right]\right\}\right)\\&=\sigma\left(\left\{\left(a,b\right]\right\}\right).
\end{aligned}
$$

### 解答 习题五

记 $\tau$=开集族, $\mathcal F$=闭集族, $\mathcal G=\left\{\left(a,b\right)\right\}$, $\mathcal H=\left\{\left[a,b\right]\right\}$, $\mathcal K=\left\{\left(a,b\right]\right\}$. 由**定义 4.3.2**, $\mathcal B\left(\mathbb R\right)=\sigma\left(\tau\right)$.

**1. $\sigma\left(\mathcal F\right)=\sigma\left(\tau\right)$.**

闭集是开集的补、开集是闭集的补. 对任意闭集 $C$, $C^{c}$ 开, 故 $C=\left(C^{c}\right)^{c}\in\sigma\left(\tau\right)$ ($\sigma$-代数对补封闭), 从而 $\mathcal F\subset\sigma\left(\tau\right)\Rightarrow\sigma\left(\mathcal F\right)\subset\sigma\left(\tau\right)$. 对称地, 对任意开集 $O$, $O^{c}$ 闭, $O=\left(O^{c}\right)^{c}\in\sigma\left(\mathcal F\right)$, 故 $\tau\subset\sigma\left(\mathcal F\right)\Rightarrow\sigma\left(\tau\right)\subset\sigma\left(\mathcal F\right)$. 两者相等.

**2. $\sigma\left(\mathcal G\right)=\sigma\left(\tau\right)$.**

每个开区间 $\left(a,b\right)$ 是开集, 故 $\mathcal G\subset\tau\Rightarrow\sigma\left(\mathcal G\right)\subset\sigma\left(\tau\right)$. 反之, 由**定理 3.2.1**, $\mathbb R$ 中每个开集 $O$ 是可数个互不相交开区间的并: $O=\bigcup_{n=1}^{\infty}\left(a_{n},b_{n}\right)\in\sigma\left(\mathcal G\right)$ ($\sigma$-代数对可数并封闭), 故 $\tau\subset\sigma\left(\mathcal G\right)\Rightarrow\sigma\left(\tau\right)\subset\sigma\left(\mathcal G\right)$. 两者相等.

**3. $\sigma\left(\mathcal H\right)=\sigma\left(\tau\right)$.**

每个闭区间 $\left[a,b\right]$ 是闭集, 故 $\mathcal H\subset\mathcal F\Rightarrow\sigma\left(\mathcal H\right)\subset\sigma\left(\mathcal F\right)=\sigma\left(\tau\right)$. 反之, 开区间可用闭区间递增逼近:

$$
\left(a,b\right)=\bigcup_{n=n_{0}}^{\infty}\left[a+\frac{1}{n},b-\frac{1}{n}\right]\in\sigma\left(\mathcal H\right)
$$

(取 $n_{0}$ 使 $a+\frac1n<b-\frac1n$), 故 $\mathcal G\subset\sigma\left(\mathcal H\right)\Rightarrow\sigma\left(\tau\right)=\sigma\left(\mathcal G\right)\subset\sigma\left(\mathcal H\right)$. 两者相等.

**4. $\sigma\left(\mathcal K\right)=\sigma\left(\tau\right)$.**

一方面, $\left(a,b\right]=\bigcap_{n=1}^{\infty}\left(a,b+\frac1n\right)$ 是开区间之可数交, 故 $\left(a,b\right]\in\sigma\left(\tau\right)$ ($\sigma$-代数对可数交封闭: 取补后为可数并), 从而 $\mathcal K\subset\sigma\left(\tau\right)\Rightarrow\sigma\left(\mathcal K\right)\subset\sigma\left(\tau\right)$.

另一方面, 开区间用左开右闭区间递减逼近: 取 $n_{0}$ 使 $b-\frac1n>a$,

$$
\left(a,b\right)=\bigcup_{n=n_{0}}^{\infty}\left(a,b-\frac1n\right]\in\sigma\left(\mathcal K\right),
$$

故 $\mathcal G\subset\sigma\left(\mathcal K\right)\Rightarrow\sigma\left(\tau\right)=\sigma\left(\mathcal G\right)\subset\sigma\left(\mathcal K\right)$. 两者相等.

综上五族生成的 $\sigma$-代数都等于 $\sigma\left(\tau\right)=\mathcal B\left(\mathbb R\right)$, 命题得证. $\blacksquare$

### 习题六

证明**定理 4.5.3 (截面可测性)**: 设 $\left(X,\mathcal F\right)$、$\left(Y,\mathcal G\right)$ 为可测空间. 若 $E\in\mathcal F\otimes\mathcal G$, 则对任意 $x\in X$ 和 $y\in Y$, 其截面

$$
\begin{aligned}
E_{x}&=\left\{y\in Y:\left(x,y\right)\in E\right\}\in\mathcal G,\\E^{y}&=\left\{x\in X:\left(x,y\right)\in E\right\}\in\mathcal F.
\end{aligned}
$$

### 解答 习题六

固定 $x\in X$, 考虑集合族

$$
\mathscr C:=\left\{E\subseteq X\times Y:E_{x}\in\mathcal G\right\}.
$$

我们证明 $\mathscr C$ 是 $\sigma$-代数且包含所有可测矩形, 从而 $\mathcal F\otimes\mathcal G=\sigma\left(\text{可测矩形}\right)\subseteq\mathscr C$, 即每个 $E\in\mathcal F\otimes\mathcal G$ 都有 $E_{x}\in\mathcal G$. 对 $y$ 一侧完全对称.

**$\mathscr C$ 是 $\sigma$-代数.**

(1) **$X\times Y\in\mathscr C$**: $\left(X\times Y\right)_{x}=Y\in\mathcal G$.

(2) **补运算封闭**: 若 $E\in\mathscr C$, 即 $E_{x}\in\mathcal G$, 则 $\left(E^{c}\right)_{x}=\left(E_{x}\right)^{c}\in\mathcal G$ (因 $\mathcal G$ 是 $\sigma$-代数, 对补封闭), 故 $E^{c}\in\mathscr C$.

(3) **可数并封闭**: 若 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathscr C$, 则 $\left(\bigcup_{n=1}^{\infty}E_{n}\right)_{x}=\bigcup_{n=1}^{\infty}\left(E_{n}\right)_{x}\in\mathcal G$ ($\mathcal G$ 对可数并封闭), 故 $\bigcup E_{n}\in\mathscr C$.

由**定义 4.1.3**, $\mathscr C$ 是 $\sigma$-代数.

**$\mathscr C$ 包含所有可测矩形.** 设 $A\in\mathcal F$, $B\in\mathcal G$. 则

$$
\left(A\times B\right)_{x}=\begin{cases}B,&x\in A,\\\varnothing,&x\notin A.\end{cases}
$$

两种情况均在 $\mathcal G$ 中, 故 $A\times B\in\mathscr C$.

因此 $\mathscr C$ 是包含所有可测矩形的 $\sigma$-代数, 而 $\mathcal F\otimes\mathcal G$ 是包含可测矩形的最小 $\sigma$-代数 (**定义 4.5.1 / 4.5.2 (可测矩形与乘积 $\sigma$-代数)**), 故 $\mathcal F\otimes\mathcal G\subseteq\mathscr C$. 于是对任意 $E\in\mathcal F\otimes\mathcal G$, $E_{x}\in\mathcal G$.

对称地 (固定 $y\in Y$, 取截面 $\left(E\right)^{y}$, 用 $\mathcal F$ 作同样论证) 得 $E^{y}\in\mathcal F$. $\blacksquare$

### 习题七

证明**定理 4.5.4 (博雷尔集的乘积)**: 对欧氏空间中的博雷尔 $\sigma$-代数,

$$
\mathcal B\left(\mathbb R^{m}\right)\otimes\mathcal B\left(\mathbb R^{n}\right)=\mathcal B\left(\mathbb R^{m+n}\right).
$$

### 解答 习题七

记 $\pi_{1}:\mathbb R^{m+n}\to\mathbb R^{m}$, $\pi_{2}:\mathbb R^{m+n}\to\mathbb R^{n}$ 为两个坐标投影. 先建立一个辅助事实: 投影 $\pi_{i}$ 连续, 故把博雷尔集拉回成博雷尔集.

**辅助事实**: 对连续映射 $f:\mathbb R^{m+n}\to\mathbb R^{m}$ (这里 $f=\pi_{1}$), 若 $A\in\mathcal B\left(\mathbb R^{m}\right)$, 则 $f^{-1}\left(A\right)\in\mathcal B\left(\mathbb R^{m+n}\right)$.

证明: 集合族 $\left\{A\subseteq\mathbb R^{m}:f^{-1}\left(A\right)\in\mathcal B\left(\mathbb R^{m+n}\right)\right\}$ 是 $\sigma$-代数 (原像保持补与可数并, **定理 2.4.2**), 且含所有开集 ($f$ 连续, 开集的原像是开集, 属于 $\mathcal B\left(\mathbb R^{m+n}\right)$), 故含 $\sigma\left(\text{开集}\right)=\mathcal B\left(\mathbb R^{m}\right)$. 辅助事实成立.

**($\subset$) $\mathcal B\left(\mathbb R^{m}\right)\otimes\mathcal B\left(\mathbb R^{n}\right)\subseteq\mathcal B\left(\mathbb R^{m+n}\right)$.**

任取可测矩形 $A\times B$ ($A\in\mathcal B\left(\mathbb R^{m}\right)$, $B\in\mathcal B\left(\mathbb R^{n}\right)$), 有

$$
A\times B=\pi_{1}^{-1}\left(A\right)\cap\pi_{2}^{-1}\left(B\right).
$$

由辅助事实, $\pi_{1}^{-1}\left(A\right),\pi_{2}^{-1}\left(B\right)\in\mathcal B\left(\mathbb R^{m+n}\right)$, 其交亦在 $\mathcal B\left(\mathbb R^{m+n}\right)$. 故所有可测矩形都在 $\mathcal B\left(\mathbb R^{m+n}\right)$ 中; 而 $\mathcal B\left(\mathbb R^{m}\right)\otimes\mathcal B\left(\mathbb R^{n}\right)$ 是含可测矩形的最小 $\sigma$-代数, 故 $\subseteq$ 成立.

**($\supset$) $\mathcal B\left(\mathbb R^{m+n}\right)\subseteq\mathcal B\left(\mathbb R^{m}\right)\otimes\mathcal B\left(\mathbb R^{n}\right)$.**

由**基础知识**, $\mathbb R^{m+n}$ 中任意开集 $O$ 可表为可数个开矩形的并: $O=\bigcup_{k=1}^{\infty}\left(U_{k}\times V_{k}\right)$, 其中 $U_{k}\subset\mathbb R^{m}$、$V_{k}\subset\mathbb R^{n}$ 为开集. 而每个开矩形 $U_{k}\times V_{k}$ 是可测矩形 ($U_{k}\in\mathcal B\left(\mathbb R^{m}\right)$, $V_{k}\in\mathcal B\left(\mathbb R^{n}\right)$), 故 $\in\mathcal B\left(\mathbb R^{m}\right)\otimes\mathcal B\left(\mathbb R^{n}\right)$. 于是 $O$ 作为可数并也属于该乘积 $\sigma$-代数. 故所有开集都在 $\mathcal B\left(\mathbb R^{m}\right)\otimes\mathcal B\left(\mathbb R^{n}\right)$ 中, 从而

$$
\mathcal B\left(\mathbb R^{m+n}\right)=\sigma\left(\text{开集}\right)\subseteq\mathcal B\left(\mathbb R^{m}\right)\otimes\mathcal B\left(\mathbb R^{n}\right).
$$

两方向结合, 即 $\mathcal B\left(\mathbb R^{m}\right)\otimes\mathcal B\left(\mathbb R^{n}\right)=\mathcal B\left(\mathbb R^{m+n}\right)$. $\blacksquare$

### 习题八

设 $\left\{\left(X_{\alpha},\mathcal F_{\alpha}\right)\right\}_{\alpha\in I}$ 是一族可测空间. 假定 $\mathcal F_{\alpha}=\sigma\left(\mathcal E_{\alpha}\right)$, 其中 $\mathcal E_{\alpha}$ 为 $X_{\alpha}$ 的子集族. 证明

$$
\bigotimes_{\alpha\in I}\mathcal F_{\alpha}=\sigma\left(\left\{\pi_{\alpha}^{-1}\left(\mathcal E_{\alpha}\right):\alpha\in I\right\}\right),
$$

其中 $\pi_{\beta}:\prod_{\alpha\in I}X_{\alpha}\to X_{\beta}$ 为乘积空间到 $X_{\beta}$ 的坐标投影.

(这里 $\bigotimes_{\alpha\in I}\mathcal F_{\alpha}$ 按**定义 4.5.7**, 是由所有柱集 $\pi_{\beta}^{-1}\left(A_{\beta}\right)$, $A_{\beta}\in\mathcal F_{\beta}$, $\beta\in I$ 生成的 $\sigma$-代数. ) 

### 解答 习题八

记 $\mathscr G:=\sigma\left(\left\{\pi_{\alpha}^{-1}\left(\mathcal E_{\alpha}\right):\alpha\in I\right\}\right)$. 分两个包含关系证明.

**($\subset$) $\bigotimes_{\alpha\in I}\mathcal F_{\alpha}\subseteq\mathscr G$.**

固定 $\alpha\in I$, 考虑 $\pi_{\alpha}:\prod_{\beta\in I}X_{\beta}\to X_{\alpha}$, 定义集合族

$$
\mathscr C_{\alpha}:=\left\{A\subseteq X_{\alpha}:\pi_{\alpha}^{-1}\left(A\right)\in\mathscr G\right\}.
$$

由原像运算保持补与可数并 (**定理 2.4.2**), $\mathscr C_{\alpha}$ 是 $\sigma$-代数. 又因 $\pi_{\alpha}^{-1}\left(\mathcal E_{\alpha}\right)\subseteq\mathscr G$ 由 $\mathscr G$ 的定义, 故 $\mathcal E_{\alpha}\subseteq\mathscr C_{\alpha}$. 从而 $\mathscr C_{\alpha}$ 是含 $\mathcal E_{\alpha}$ 的 $\sigma$-代数, 故含 $\sigma\left(\mathcal E_{\alpha}\right)=\mathcal F_{\alpha}$. 即对一切 $A\in\mathcal F_{\alpha}$, 有 $\pi_{\alpha}^{-1}\left(A\right)\in\mathscr G$.

由于 $\alpha\in I$ 任意, 所有柱集 $\pi_{\alpha}^{-1}\left(A\right)$ ($A\in\mathcal F_{\alpha}$, $\alpha\in I$) 都在 $\mathscr G$ 中. 而 $\bigotimes_{\alpha\in I}\mathcal F_{\alpha}$ 是由这些柱集生成的 $\sigma$-代数, 故

$$
\bigotimes_{\alpha\in I}\mathcal F_{\alpha}\subseteq\mathscr G.
$$

**($\supset$) $\mathscr G\subseteq\bigotimes_{\alpha\in I}\mathcal F_{\alpha}$.**

固定 $\alpha\in I$. 对任意 $E_{\alpha}\in\mathcal E_{\alpha}$, $\pi_{\alpha}^{-1}\left(E_{\alpha}\right)$ 恰是一个柱集 (定义 4.5.7 中取 $A_{\beta}=E_{\alpha}$ 当 $\beta=\alpha$), 故 $\pi_{\alpha}^{-1}\left(\mathcal E_{\alpha}\right)\subseteq\bigotimes_{\alpha\in I}\mathcal F_{\alpha}$. 于是所有生成元 $\pi_{\alpha}^{-1}\left(E_{\alpha}\right)$ ($\alpha\in I$) 都在乘积 $\sigma$-代数中, 而 $\bigotimes_{\alpha\in I}\mathcal F_{\alpha}$ 是含这些集合的 $\sigma$-代数, 故其生成的 $\sigma$-代数

$$
\mathscr G\subseteq\bigotimes_{\alpha\in I}\mathcal F_{\alpha}.
$$

两方向结合, 即

$$
\boxed{\bigotimes_{\alpha\in I}\mathcal F_{\alpha}=\sigma\left(\left\{\pi_{\alpha}^{-1}\left(\mathcal E_{\alpha}\right):\alpha\in I\right\}\right)}\quad\blacksquare
$$
