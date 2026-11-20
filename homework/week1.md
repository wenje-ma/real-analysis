# week1

> **定理 1.2.9 (德摩根定律)**
> 
> $\left(A\cup{B}\right)^{c}=A^{c}\cap{B}^{c}$, $\left(A\cap{B}\right)^{c}=A^{c}\cup{B}^{c}$.

> **定理 2.4.2 (原像运算的性质)**
> 
> 设 $f:A\to{B}$, 则 $f^{-1}\left(B_{1}\cup{B}_{2}\right)=f^{-1}\left(B_{1}\right)\cup{f}^{-1}\left(B_{2}\right)$, $f^{-1}\left(B_{1}\cap{B}_{2}\right)=f^{-1}\left(B_{1}\right)\cap{f}^{-1}\left(B_{2}\right)$, $f^{-1}\left(B^{c}\right)=\left(f^{-1}\left(B\right)\right)^{c}$, $f^{-1}\left(\bigcup_{\alpha\in{I}}B_{\alpha}\right)=\bigcup_{\alpha\in{I}}f^{-1}\left(B_{\alpha}\right)$, $f^{-1}\left(\bigcap_{\alpha\in{I}}B_{\alpha}\right)=\bigcap_{\alpha\in{I}}f^{-1}\left(B_{\alpha}\right)$.

> **定理 3.2.1 (实数中开集的构造)**
> 
> 设 $U\subset\mathbb{R}$ 是非空开集, 则存在一列互不相交的开区间 $\left\{I_{n}\right\}_{n=1}^{\infty}$, 使 $U=\bigcup_{n=1}^{\infty}I_{n}$; 且此表示在重排意义下唯一.

> **定义 4.1.1 (集合代数)**
> 
> 设 $X$ 是非空集合, $\mathcal{A}\subset\mathcal{P}\left(X\right)$. 称 $\mathcal{A}$ 为 $X$ 上的一个集合代数, 若满足: (1) $X\in\mathcal{A}$; (2) 对差运算封闭: $A,B\in\mathcal{A}\Rightarrow{A}\setminus{B}\in\mathcal{A}$; (3) 对有限并封闭: $A,B\in\mathcal{A}\Rightarrow{A}\cup{B}\in\mathcal{A}$.

> **命题 4.1.2 (代数的等价定义)**
> 
> 设 $\mathcal{A}\subset\mathcal{P}\left(X\right)$, 则以下条件等价: (1) $\mathcal{A}$ 是代数; (2) $\mathcal{A}$ 满足: (a) $X\in\mathcal{A}$; (b) 对补运算封闭: $A\in\mathcal{A}\Rightarrow{A}^{c}=X\setminus{A}\in\mathcal{A}$; (c) 对有限并封闭: $A,B\in\mathcal{A}\Rightarrow{A}\cup{B}\in\mathcal{A}$.

> **定义 4.1.3 ($\sigma$-代数)**
> 
> 设 $X$ 非空, $\mathcal{F}\subset\mathcal{P}\left(X\right)$. 称 $\mathcal{F}$ 为 $X$ 上的一个 $\sigma$-代数, 若满足: (1) $X\in\mathcal{F}$; (2) 对补运算封闭: $A\in\mathcal{F}\Rightarrow{A}^{c}\in\mathcal{F}$; (3) 对可数并封闭: $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal{F}$.

> **定义 4.2.1 (生成代数)**
> 
> 包含 $\mathcal{E}\subset\mathcal{P}\left(X\right)$ 的最小代数称为由 $\mathcal{E}$ 生成的代数, 记作 $\alpha\left(\mathcal{E}\right)$: $\alpha\left(\mathcal{E}\right)=\bigcap\left\{\mathcal{A}\subset\mathcal{P}\left(X\right):\mathcal{A}\text{~是代数且~}\mathcal{E}\subset\mathcal{A}\right\}$.

> **定义 4.2.2 (生成 $\sigma$-代数)**
> 
> 包含 $\mathcal{E}\subset\mathcal{P}\left(X\right)$ 的最小 $\sigma$-代数称为由 $\mathcal{E}$ 生成的 $\sigma$-代数, 记作 $\sigma\left(\mathcal{E}\right)$: $\sigma\left(\mathcal{E}\right)=\bigcap\left\{\mathcal{F}\subset\mathcal{P}\left(X\right):\mathcal{F}\text{~是~$\sigma$-代数且~}\mathcal{E}\subset\mathcal{F}\right\}$.

> **定义 4.3.2 (博雷尔 $\sigma$-代数)**
> 
> 设 $\left(X,\tau\right)$ 是拓扑空间, 由所有开集生成的 $\sigma$-代数称为博雷尔 $\sigma$-代数, 记作 $\mathcal{B}\left(X\right)$, 其中元素称为博雷尔集.

> **例 4.3.3 (实数上的博雷尔代数)**
> 
> 在 $\mathbb{R}$ 上, 以下集合族生成相同的博雷尔 $\sigma$-代数 $\mathcal{B}\left(\mathbb{R}\right)$: 所有开集 $\tau$, 所有闭集 $\mathcal{F}$, 所有开区间 $\left\{\left(a,b\right)\right\}$, 所有闭区间 $\left\{\left[a,b\right]\right\}$, 所有左开右闭区间 $\left\{\left(a,b\right]\right\}$, 即 $\mathcal{B}\left(\mathbb{R}\right)=\sigma\left(\tau\right)=\sigma\left(\mathcal{F}\right)=\sigma\left(\left\{\left(a,b\right)\right\}\right)=\sigma\left(\left\{\left[a,b\right]\right\}\right)=\sigma\left(\left\{\left(a,b\right]\right\}\right)$.

> **定义 4.5.1 (可测矩形与乘积 $\sigma$-代数)**
> 
> 设 $\left(X,\mathcal{F}\right)$, $\left(Y,\mathcal{G}\right)$ 为可测空间. $A\times{B}\subseteq{X}\times{Y}$ 称为可测矩形, 若 $A\in\mathcal{F}$ 且 $B\in\mathcal{G}$. 乘积 $\sigma$-代数为包含所有可测矩形的最小 $\sigma$-代数: $\mathcal{F}\otimes\mathcal{G}:=\sigma\left(\left\{A\times{B}:A\in\mathcal{F},B\in\mathcal{G}\right\}\right)$.

> **定理 4.5.3 (截面可测性)**
> 
> 若 $E\in\mathcal{F}\otimes\mathcal{G}$, 则对任意 $x\in{X}$, $y\in{Y}$, 其截面都可测: $E_{x}=\left\{y\in{Y}:\left(x,y\right)\in{E}\right\}\in\mathcal{G},\quad{E}^{y}=\left\{x\in{X}:\left(x,y\right)\in{E}\right\}\in\mathcal{F}$.

> **定理 4.5.4 (博雷尔集的乘积)**
> 
> 对欧氏空间中的博雷尔 $\sigma$-代数, 有 $\mathcal{B}\left(\mathbb{R}^{m}\right)\otimes\mathcal{B}\left(\mathbb{R}^{n}\right)=\mathcal{B}\left(\mathbb{R}^{m+n}\right)$. ## 1 设 $\mathcal{A}\subset\mathcal{P}\left(X\right)$, 证明**命题 4.1.2 (代数的等价定义)**: $\mathcal{A}$ 是代数, 当且仅当 $\mathcal{A}$ 满足 (a) $X\in\mathcal{A}$; (b) 对补运算封闭: $A\in\mathcal{A}\Rightarrow{A}^{c}\in\mathcal{A}$; (c) 对有限并封闭: $A,B\in\mathcal{A}\Rightarrow{A}\cup{B}\in\mathcal{A}$. 依据**定义 4.1.1 (集合代数)** 与**命题 4.1.2 (代数的等价定义)**, 分两个方向证明. ($\Rightarrow$) 设 $\mathcal{A}$ 是代数, 则 $X\in\mathcal{A}$ (a) 成立, 有限并封闭 (c) 成立. 对补封闭 (b): 对任意 $A\in\mathcal{A}$, 由 $X,A\in\mathcal{A}$ 及差运算封闭, 得 $$A^{c}=X\setminus{A}\in\mathcal{A}.$$ 故 (a)(b)(c) 均成立. ($\Leftarrow$) 设 (a)(b)(c) 成立. $X\in\mathcal{A}$ 即**定义 4.1.1 (集合代数)** (1); 有限并封闭即 (3). 只需验证差运算封闭 (2): 对任意 $A,B\in\mathcal{A}$, 由 (b) 得 $B^{c}\in\mathcal{A}$, 由 (c) 得 $A^{c}\cup{B}\in\mathcal{A}$, 再由 (b) 得 $$A\setminus{B}=A\cap{B}^{c}=\left(A^{c}\cup{B}\right)^{c}\in\mathcal{A},$$ 其中第二式用到**定理 1.2.9 (德摩根定律)**. 故 $\mathcal{A}$ 是代数. 两方向结合, 命题得证. $\blacksquare$

## 2

证明: $\mathcal{F}$ 为 $\sigma$-代数, 当且仅当 $\mathcal{F}$ 为代数, 且对可数不交并封闭.

### 解答 2

($\Rightarrow$) 设 $\mathcal{F}$ 是 $\sigma$-代数 (**定义 4.1.3 ($\sigma$-代数)**). 则 $X\in\mathcal{F}$; 对补封闭 (b); 对可数并封闭, 特别地对有限并封闭 (c), 也对可数不交并封闭. 还需验证差运算封闭: 对 $A,B\in\mathcal{F}$, 由 (b)(c) 与德摩根定律

$$
A\setminus{B}=A\cap{B}^{c}=\left(A^{c}\cup{B}\right)^{c}\in\mathcal{F}.
$$

故由**命题 4.1.2 (代数的等价定义)** 得 $\mathcal{F}$ 是代数, 且显然对可数不交并封闭.

($\Leftarrow$) 设 $\mathcal{F}$ 是代数且对可数不交并封闭. 代数给出 $X\in\mathcal{F}$, 对补封闭及有限并封闭; 只需再证对可数并封闭. 设 $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$, 作不交化:

$$
B_{1}:=A_{1},\quad{B}_{n}:=A_{n}\setminus\left(A_{1}\cup\cdots\cup{A}_{n-1}\right)\,\left(n\ge2\right).
$$

由代数的差运算与有限并封闭, 每个 $B_{n}\in\mathcal{F}$; 且 $\left\{B_{n}\right\}$ 两两不交, 并保持并集不变: $\bigcup_{n=1}^{\infty}B_{n}=\bigcup_{n=1}^{\infty}A_{n}$. 由可数不交并封闭,

$$
\bigcup_{n=1}^{\infty}A_{n}=\bigcup_{n=1}^{\infty}B_{n}\in\mathcal{F}.
$$

故 $\mathcal{F}$ 对可数并封闭, 是 $\sigma$-代数.

$\blacksquare$

## 3

设 $\mathcal{E}\subset\mathcal{P}\left(X\right)$, 证明由 $\mathcal{E}$ 生成的代数

$$
\alpha\left(\mathcal{E}\right)=\bigcap\left\{\mathcal{A}\subset\mathcal{P}\left(X\right):\mathcal{A}\text{~是代数且~}\mathcal{E}\subset\mathcal{A}\right\}
$$

是一个代数.

### 解答 3

记 $\mathscr{C}=\left\{\mathcal{A}\subset\mathcal{P}\left(X\right):\mathcal{A}\text{~是代数且~}\mathcal{E}\subset\mathcal{A}\right\}$ 为所有含 $\mathcal{E}$ 的代数的全体. $\mathscr{C}$ 非空 (因 $\mathcal{P}\left(X\right)$ 是代数且含 $\mathcal{E}$), 故由**定义 4.2.1 (生成代数)**, $\alpha\left(\mathcal{E}\right)$ 良定义.

对 $\alpha\left(\mathcal{E}\right)$ 逐条验证**定义 4.1.1 (集合代数)**:

(1) $X\in\alpha\left(\mathcal{E}\right)$: 每个 $\mathcal{A}\in\mathscr{C}$ 是代数, 故 $X\in\mathcal{A}$, 从而 $X$ 属于所有 $\mathcal{A}$ 之交, 即 $X\in\alpha\left(\mathcal{E}\right)$.

(2) 差运算封闭: 设 $A,B\in\alpha\left(\mathcal{E}\right)$, 则对每个 $\mathcal{A}\in\mathscr{C}$ 有 $A,B\in\mathcal{A}$, 由 $\mathcal{A}$ 是代数得 $A\setminus{B}\in\mathcal{A}$. 因 $\mathcal{A}$ 任意, $A\setminus{B}\in\bigcap\mathscr{C}=\alpha\left(\mathcal{E}\right)$.

(3) 有限并封闭: 同理, 对每个 $\mathcal{A}\in\mathscr{C}$ 有 $A\cup{B}\in\mathcal{A}$, 故 $A\cup{B}\in\alpha\left(\mathcal{E}\right)$.

故 $\alpha\left(\mathcal{E}\right)$ 是含 $\mathcal{E}$ 的代数. 又由定义其为所有含 $\mathcal{E}$ 的代数的交集, 故它是包含 $\mathcal{E}$ 的最小代数.

$\blacksquare$

## 4

设 $\mathcal{E}\subset\mathcal{P}\left(X\right)$, 证明由 $\mathcal{E}$ 生成的 $\sigma$-代数

$$
\sigma\left(\mathcal{E}\right)=\bigcap\left\{\mathcal{F}\subset\mathcal{P}\left(X\right):\mathcal{F}\text{~是~$\sigma$-代数且~}\mathcal{E}\subset\mathcal{F}\right\}
$$

是一个 $\sigma$-代数.

### 解答 4

记 $\mathscr{C}'=\left\{\mathcal{F}\subset\mathcal{P}\left(X\right):\mathcal{F}\text{~是~}\sigma\text{-代数且~}\mathcal{E}\subset\mathcal{F}\right\}$. $\mathscr{C}'$ 非空 ($\mathcal{P}\left(X\right)$ 是 $\sigma$-代数且含 $\mathcal{E}$), 故由**定义 4.2.2 (生成 $\sigma$-代数)**, $\sigma\left(\mathcal{E}\right)$ 良定义.

逐条验证**定义 4.1.3 ($\sigma$-代数)**:

(1) $X\in\sigma\left(\mathcal{E}\right)$: 每个 $\mathcal{F}\in\mathscr{C}'$ 是 $\sigma$-代数, 含 $X$, 故 $X$ 属于其交集.

(2) 补运算封闭: 设 $A\in\sigma\left(\mathcal{E}\right)$, 则对每个 $\mathcal{F}\in\mathscr{C}'$, $A\in\mathcal{F}$, 由 $\mathcal{F}$ 是 $\sigma$-代数得 $A^{c}\in\mathcal{F}$, 故 $A^{c}\in\sigma\left(\mathcal{E}\right)$.

(3) 可数并封闭: 设 $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\sigma\left(\mathcal{E}\right)$, 则对每个 $\mathcal{F}\in\mathscr{C}'$, $\left\{A_{n}\right\}\subset\mathcal{F}$, 由 $\mathcal{F}$ 对可数并封闭得 $\bigcup_{n=1}^{\infty}A_{n}\in\mathcal{F}$, 故 $\bigcup_{n=1}^{\infty}A_{n}\in\sigma\left(\mathcal{E}\right)$.

故 $\sigma\left(\mathcal{E}\right)$ 是含 $\mathcal{E}$ 的 $\sigma$-代数, 且是最小的 (所有含 $\mathcal{E}$ 的 $\sigma$-代数之交).

$\blacksquare$

## 5

在 $\mathbb{R}$ 上, 证明**例 4.3.3 (实数上的博雷尔代数)**: 以下集合族生成相同的博雷尔 $\sigma$-代数 $\mathcal{B}\left(\mathbb{R}\right)$:

所有开集 $\tau$, 所有闭集 $\mathcal{F}$, 所有开区间 $\left\{\left(a,b\right)\right\}$, 所有闭区间 $\left\{\left[a,b\right]\right\}$, 所有左开右闭区间 $\left\{\left(a,b\right]\right\}$.

即证明

$$
\mathcal{B}\left(\mathbb{R}\right)=\sigma\left(\tau\right)=\sigma\left(\mathcal{F}\right)=\sigma\left(\left\{\left(a,b\right)\right\}\right)=\sigma\left(\left\{\left[a,b\right]\right\}\right)=\sigma\left(\left\{\left(a,b\right]\right\}\right).
$$

### 解答 5

记 $\tau$ 为开集族, $\mathcal{F}$ 为闭集族, $\mathcal{G}=\left\{\left(a,b\right)\right\}$, $\mathcal{H}=\left\{\left[a,b\right]\right\}$, $\mathcal{K}=\left\{\left(a,b\right]\right\}$. 由**定义 4.3.2 (博雷尔 $\sigma$-代数)**, $\mathcal{B}\left(\mathbb{R}\right)=\sigma\left(\tau\right)$.

1. $\sigma\left(\mathcal{F}\right)=\sigma\left(\tau\right)$. 闭集是开集的补, 开集是闭集的补. 对任意闭集 $C$, $C^{c}$ 开, 故 $C=\left(C^{c}\right)^{c}\in\sigma\left(\tau\right)$ ($\sigma$-代数对补封闭), 从而 $\mathcal{F}\subset\sigma\left(\tau\right)\Rightarrow\sigma\left(\mathcal{F}\right)\subset\sigma\left(\tau\right)$. 对称地, 对任意开集 $O$, $O^{c}$ 闭, $O=\left(O^{c}\right)^{c}\in\sigma\left(\mathcal{F}\right)$, 故 $\tau\subset\sigma\left(\mathcal{F}\right)\Rightarrow\sigma\left(\tau\right)\subset\sigma\left(\mathcal{F}\right)$. 两者相等.

2. $\sigma\left(\mathcal{G}\right)=\sigma\left(\tau\right)$. 每个开区间 $\left(a,b\right)$ 是开集, 故 $\mathcal{G}\subset\tau\Rightarrow\sigma\left(\mathcal{G}\right)\subset\sigma\left(\tau\right)$. 反之, 由**定理 3.2.1 (实数中开集的构造)**, $\mathbb{R}$ 中每个开集 $O$ 是可数个互不相交开区间的并: $O=\bigcup_{n=1}^{\infty}\left(a_{n},b_{n}\right)\in\sigma\left(\mathcal{G}\right)$ ($\sigma$-代数对可数并封闭), 故 $\tau\subset\sigma\left(\mathcal{G}\right)\Rightarrow\sigma\left(\tau\right)\subset\sigma\left(\mathcal{G}\right)$. 两者相等.

3. $\sigma\left(\mathcal{H}\right)=\sigma\left(\tau\right)$. 每个闭区间 $\left[a,b\right]$ 是闭集, 故 $\mathcal{H}\subset\mathcal{F}\Rightarrow\sigma\left(\mathcal{H}\right)\subset\sigma\left(\mathcal{F}\right)=\sigma\left(\tau\right)$. 反之, 开区间可用闭区间递增逼近:

$$
\left(a,b\right)=\bigcup_{n=n_{0}}^{\infty}\left[a+\frac{1}{n},b-\frac{1}{n}\right]\in\sigma\left(\mathcal{H}\right)
$$

(取 $n_{0}$ 使 $a+\frac1n<{}b-\frac1n$), 故 $\mathcal{G}\subset\sigma\left(\mathcal{H}\right)\Rightarrow\sigma\left(\tau\right)=\sigma\left(\mathcal{G}\right)\subset\sigma\left(\mathcal{H}\right)$. 两者相等.

4. $\sigma\left(\mathcal{K}\right)=\sigma\left(\tau\right)$. 一方面, $\left(a,b\right]=\bigcap_{n=1}^{\infty}\left(a,b+\frac1n\right)$ 是开区间之可数交, 故 $\left(a,b\right]\in\sigma\left(\tau\right)$ ($\sigma$-代数对可数交封闭: 取补后为可数并), 从而 $\mathcal{K}\subset\sigma\left(\tau\right)\Rightarrow\sigma\left(\mathcal{K}\right)\subset\sigma\left(\tau\right)$.

另一方面, 开区间用左开右闭区间递减逼近: 取 $n_{0}$ 使 $b-\frac1n>a$,

$$
\left(a,b\right)=\bigcup_{n=n_{0}}^{\infty}\left(a,b-\frac1n\right]\in\sigma\left(\mathcal{K}\right),
$$

故 $\mathcal{G}\subset\sigma\left(\mathcal{K}\right)\Rightarrow\sigma\left(\tau\right)=\sigma\left(\mathcal{G}\right)\subset\sigma\left(\mathcal{K}\right)$. 两者相等.

综上五族生成的 $\sigma$-代数都等于 $\sigma\left(\tau\right)=\mathcal{B}\left(\mathbb{R}\right)$, 命题得证.

$\blacksquare$
