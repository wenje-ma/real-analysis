# week2

> **定理 1.2.9 (德摩根定律)**
> 
> $\left(A\cup{}B\right)^{c}=A^{c}\cap{}B^{c}$, $\left(A\cap{}B\right)^{c}=A^{c}\cup{}B^{c}$.

> **定理 2.4.2 (原像运算的性质)**
> 
> 设 $f:A\to{}B$, 则 $f^{-1}\left(B_{1}\cup{}B_{2}\right)=f^{-1}\left(B_{1}\right)\cup{}f^{-1}\left(B_{2}\right)$, $f^{-1}\left(B_{1}\cap{}B_{2}\right)=f^{-1}\left(B_{1}\right)\cap{}f^{-1}\left(B_{2}\right)$, $f^{-1}\left(B^{c}\right)=\left(f^{-1}\left(B\right)\right)^{c}$, $f^{-1}\left(\bigcup_{\alpha\in{}I}B_{\alpha}\right)=\bigcup_{\alpha\in{}I}f^{-1}\left(B_{\alpha}\right)$, $f^{-1}\left(\bigcap_{\alpha\in{}I}B_{\alpha}\right)=\bigcap_{\alpha\in{}I}f^{-1}\left(B_{\alpha}\right)$.

> **定理 3.2.1 (实数中开集的构造)**
> 
> 设 $U\subset\mathbb{R}$ 是非空开集, 则存在一列互不相交的开区间 $\left\{I_{n}\right\}_{n=1}^{\infty}$, 使 $U=\bigcup_{n=1}^{\infty}I_{n}$; 且此表示在重排意义下唯一.

> **定义 4.1.1 (集合代数)**
> 
> 设 $X$ 是非空集合, $\mathcal{A}\subset\mathcal{P}\left(X\right)$. 称 $\mathcal{A}$ 为 $X$ 上的一个集合代数, 若满足: (1) $X\in\mathcal{A}$; (2) 对差运算封闭: $A,B\in\mathcal{A}\Rightarrow{}A\setminus{}B\in\mathcal{A}$; (3) 对有限并封闭: $A,B\in\mathcal{A}\Rightarrow{}A\cup{}B\in\mathcal{A}$.

> **命题 4.1.2 (代数的等价定义)**
> 
> 设 $\mathcal{A}\subset\mathcal{P}\left(X\right)$, 则以下条件等价: (1) $\mathcal{A}$ 是代数; (2) $\mathcal{A}$ 满足: (a) $X\in\mathcal{A}$; (b) 对补运算封闭: $A\in\mathcal{A}\Rightarrow{}A^{c}=X\setminus{}A\in\mathcal{A}$; (c) 对有限并封闭: $A,B\in\mathcal{A}\Rightarrow{}A\cup{}B\in\mathcal{A}$.

> **定义 4.1.3 ($\sigma$-代数)**
> 
> 设 $X$ 非空, $\mathcal{F}\subset\mathcal{P}\left(X\right)$. 称 $\mathcal{F}$ 为 $X$ 上的一个 $\sigma$-代数, 若满足: (1) $X\in\mathcal{F}$; (2) 对补运算封闭: $A\in\mathcal{F}\Rightarrow{}A^{c}\in\mathcal{F}$; (3) 对可数并封闭: $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal{F}$.

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
> 设 $\left(X,\mathcal{F}\right)$, $\left(Y,\mathcal{G}\right)$ 为可测空间. $A\times{}B\subseteq{}X\times{}Y$ 称为可测矩形, 若 $A\in\mathcal{F}$ 且 $B\in\mathcal{G}$. 乘积 $\sigma$-代数为包含所有可测矩形的最小 $\sigma$-代数: $\mathcal{F}\otimes\mathcal{G}:=\sigma\left(\left\{A\times{}B:A\in\mathcal{F},B\in\mathcal{G}\right\}\right)$.

> **定理 4.5.3 (截面可测性)**
> 
> 若 $E\in\mathcal{F}\otimes\mathcal{G}$, 则对任意 $x\in{}X$, $y\in{}Y$, 其截面都可测: $E_{x}=\left\{y\in{}Y:\left(x,y\right)\in{}E\right\}\in\mathcal{G},\quad{}E^{y}=\left\{x\in{}X:\left(x,y\right)\in{}E\right\}\in\mathcal{F}$.

> **定理 4.5.4 (博雷尔集的乘积)**
> 
> 对欧氏空间中的博雷尔 $\sigma$-代数, 有 $\mathcal{B}\left(\mathbb{R}^{m}\right)\otimes\mathcal{B}\left(\mathbb{R}^{n}\right)=\mathcal{B}\left(\mathbb{R}^{m+n}\right)$. ## 1 设 $\mathcal{A}\subset\mathcal{P}\left(X\right)$, 证明**命题 4.1.2 (代数的等价定义)**: $\mathcal{A}$ 是代数, 当且仅当 $\mathcal{A}$ 满足 (a) $X\in\mathcal{A}$; (b) 对补运算封闭: $A\in\mathcal{A}\Rightarrow{}A^{c}\in\mathcal{A}$; (c) 对有限并封闭: $A,B\in\mathcal{A}\Rightarrow{}A\cup{}B\in\mathcal{A}$. 依据**定义 4.1.1 (集合代数)** 与**命题 4.1.2 (代数的等价定义)**, 分两个方向证明. ($\Rightarrow$) 设 $\mathcal{A}$ 是代数, 则 $X\in\mathcal{A}$ (a) 成立, 有限并封闭 (c) 成立. 对补封闭 (b): 对任意 $A\in\mathcal{A}$, 由 $X,A\in\mathcal{A}$ 及差运算封闭, 得 $$A^{c}=X\setminus{}A\in\mathcal{A}.$$ 故 (a)(b)(c) 均成立. ($\Leftarrow$) 设 (a)(b)(c) 成立. $X\in\mathcal{A}$ 即**定义 4.1.1 (集合代数)** (1); 有限并封闭即 (3). 只需验证差运算封闭 (2): 对任意 $A,B\in\mathcal{A}$, 由 (b) 得 $B^{c}\in\mathcal{A}$, 由 (c) 得 $A^{c}\cup{}B\in\mathcal{A}$, 再由 (b) 得 $$A\setminus{}B=A\cap{}B^{c}=\left(A^{c}\cup{}B\right)^{c}\in\mathcal{A},$$ 其中第二式用到**定理 1.2.9 (德摩根定律)**. 故 $\mathcal{A}$ 是代数. 两方向结合, 命题得证. $\blacksquare$

## 6

证明**定理 4.5.3 (截面可测性)**: 设 $\left(X,\mathcal{F}\right)$, $\left(Y,\mathcal{G}\right)$ 为可测空间. 若 $E\in\mathcal{F}\otimes\mathcal{G}$, 则对任意 $x\in{}X$ 和 $y\in{}Y$, 其截面

$$
E_{x}=\left\{y\in{}Y:\left(x,y\right)\in{}E\right\}\in\mathcal{G},\quad{}E^{y}=\left\{x\in{}X:\left(x,y\right)\in{}E\right\}\in\mathcal{F}.
$$

### 解答 6

固定 $x\in{}X$, 考虑集合族

$$
\mathscr{C}:=\left\{E\subseteq{}X\times{}Y:E_{x}\in\mathcal{G}\right\}.
$$

我们证明 $\mathscr{C}$ 是 $\sigma$-代数且包含所有可测矩形, 从而 $\mathcal{F}\otimes\mathcal{G}=\sigma\left(\text{可测矩形}\right)\subseteq\mathscr{C}$, 即每个 $E\in\mathcal{F}\otimes\mathcal{G}$ 都有 $E_{x}\in\mathcal{G}$. 对 $y$ 一侧完全对称.

$\mathscr{C}$ 是 $\sigma$-代数.

(1) $X\times{}Y\in\mathscr{C}$: $\left(X\times{}Y\right)_{x}=Y\in\mathcal{G}$.

(2) 补运算封闭: 若 $E\in\mathscr{C}$, 即 $E_{x}\in\mathcal{G}$, 则 $\left(E^{c}\right)_{x}=\left(E_{x}\right)^{c}\in\mathcal{G}$ (因 $\mathcal{G}$ 是 $\sigma$-代数, 对补封闭), 故 $E^{c}\in\mathscr{C}$.

(3) 可数并封闭: 若 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathscr{C}$, 则 $\left(\bigcup_{n=1}^{\infty}E_{n}\right)_{x}=\bigcup_{n=1}^{\infty}\left(E_{n}\right)_{x}\in\mathcal{G}$ ($\mathcal{G}$ 对可数并封闭), 故 $\bigcup{}E_{n}\in\mathscr{C}$.

由**定义 4.1.3 ($\sigma$-代数)**, $\mathscr{C}$ 是 $\sigma$-代数.

$\mathscr{C}$ 包含所有可测矩形. 设 $A\in\mathcal{F}$, $B\in\mathcal{G}$. 则

$$
\left(A\times{}B\right)_{x}=\begin{cases}B,&x\in{}A,\\\emptyset,&x\notin{}A.\end{cases}
$$

两种情况均在 $\mathcal{G}$ 中, 故 $A\times{}B\in\mathscr{C}$.

因此 $\mathscr{C}$ 是包含所有可测矩形的 $\sigma$-代数, 而 $\mathcal{F}\otimes\mathcal{G}$ 是包含可测矩形的最小 $\sigma$-代数 (**定义 4.5.1 (可测矩形与乘积 $\sigma$-代数)**), 故 $\mathcal{F}\otimes\mathcal{G}\subseteq\mathscr{C}$. 于是对任意 $E\in\mathcal{F}\otimes\mathcal{G}$, $E_{x}\in\mathcal{G}$.

对称地 (固定 $y\in{}Y$, 取截面 $E^{y}$, 用 $\mathcal{F}$ 作同样论证) 得 $E^{y}\in\mathcal{F}$.

$\blacksquare$

## 7

证明**定理 4.5.4 (博雷尔集的乘积)**: 对欧氏空间中的博雷尔 $\sigma$-代数,

$$
\mathcal{B}\left(\mathbb{R}^{m}\right)\otimes\mathcal{B}\left(\mathbb{R}^{n}\right)=\mathcal{B}\left(\mathbb{R}^{m+n}\right).
$$

### 解答 7

记 $\pi_{1}:\mathbb{R}^{m+n}\to\mathbb{R}^{m}$, $\pi_{2}:\mathbb{R}^{m+n}\to\mathbb{R}^{n}$ 为两个坐标投影. 先建立一个辅助事实: 投影 $\pi_{i}$ 连续, 故把博雷尔集拉回成博雷尔集.

辅助事实: 对连续映射 $f:\mathbb{R}^{m+n}\to\mathbb{R}^{m}$ (这里 $f=\pi_{1}$), 若 $A\in\mathcal{B}\left(\mathbb{R}^{m}\right)$, 则 $f^{-1}\left(A\right)\in\mathcal{B}\left(\mathbb{R}^{m+n}\right)$.

证明: 集合族 $\left\{A\subseteq\mathbb{R}^{m}:f^{-1}\left(A\right)\in\mathcal{B}\left(\mathbb{R}^{m+n}\right)\right\}$ 是 $\sigma$-代数 (原像保持补与可数并, **定理 2.4.2 (原像运算的性质)**), 且含所有开集 ($f$ 连续, 开集的原像是开集, 属于 $\mathcal{B}\left(\mathbb{R}^{m+n}\right)$), 故含 $\sigma\left(\text{开集}\right)=\mathcal{B}\left(\mathbb{R}^{m}\right)$. 辅助事实成立.

($\subset$) $\mathcal{B}\left(\mathbb{R}^{m}\right)\otimes\mathcal{B}\left(\mathbb{R}^{n}\right)\subseteq\mathcal{B}\left(\mathbb{R}^{m+n}\right)$.

任取可测矩形 $A\times{}B$ ($A\in\mathcal{B}\left(\mathbb{R}^{m}\right)$, $B\in\mathcal{B}\left(\mathbb{R}^{n}\right)$), 有

$$
A\times{}B=\pi_{1}^{-1}\left(A\right)\cap\pi_{2}^{-1}\left(B\right).
$$

由辅助事实, $\pi_{1}^{-1}\left(A\right),\pi_{2}^{-1}\left(B\right)\in\mathcal{B}\left(\mathbb{R}^{m+n}\right)$, 其交亦在 $\mathcal{B}\left(\mathbb{R}^{m+n}\right)$. 故所有可测矩形都在 $\mathcal{B}\left(\mathbb{R}^{m+n}\right)$ 中; 而 $\mathcal{B}\left(\mathbb{R}^{m}\right)\otimes\mathcal{B}\left(\mathbb{R}^{n}\right)$ 是含可测矩形的最小 $\sigma$-代数, 故 $\subseteq$ 成立.

($\supset$) $\mathcal{B}\left(\mathbb{R}^{m+n}\right)\subseteq\mathcal{B}\left(\mathbb{R}^{m}\right)\otimes\mathcal{B}\left(\mathbb{R}^{n}\right)$.

由开集表为可数开矩形并, $\mathbb{R}^{m+n}$ 中任意开集 $O$ 可表为可数个开矩形的并: $O=\bigcup_{k=1}^{\infty}\left(U_{k}\times{}V_{k}\right)$, 其中 $U_{k}\subset\mathbb{R}^{m}$, $V_{k}\subset\mathbb{R}^{n}$ 为开集. 而每个开矩形 $U_{k}\times{}V_{k}$ 是可测矩形 ($U_{k}\in\mathcal{B}\left(\mathbb{R}^{m}\right)$, $V_{k}\in\mathcal{B}\left(\mathbb{R}^{n}\right)$), 故属于 $\mathcal{B}\left(\mathbb{R}^{m}\right)\otimes\mathcal{B}\left(\mathbb{R}^{n}\right)$. 于是 $O$ 作为可数并也属于该乘积 $\sigma$-代数. 故所有开集都在 $\mathcal{B}\left(\mathbb{R}^{m}\right)\otimes\mathcal{B}\left(\mathbb{R}^{n}\right)$ 中, 从而

$$
\mathcal{B}\left(\mathbb{R}^{m+n}\right)=\sigma\left(\text{开集}\right)\subseteq\mathcal{B}\left(\mathbb{R}^{m}\right)\otimes\mathcal{B}\left(\mathbb{R}^{n}\right).
$$

两方向结合, 即 $\mathcal{B}\left(\mathbb{R}^{m}\right)\otimes\mathcal{B}\left(\mathbb{R}^{n}\right)=\mathcal{B}\left(\mathbb{R}^{m+n}\right)$.

$\blacksquare$

## 1

设 $\left\{\left(X_{\alpha},\mathcal{F}_{\alpha}\right)\right\}_{\alpha\in{}I}$ 是一族可测空间. 假定 $\mathcal{F}_{\alpha}=\sigma\left(\mathcal{E}_{\alpha}\right)$, 其中 $\mathcal{E}_{\alpha}$ 为 $X_{\alpha}$ 的子集族. 证明

$$
\bigotimes_{\alpha\in{}I}\mathcal{F}_{\alpha}=\sigma\left(\left\{\pi_{\alpha}^{-1}\left(\mathcal{E}_{\alpha}\right):\alpha\in{}I\right\}\right),
$$

其中 $\pi_{\beta}:\prod_{\alpha\in{}I}X_{\alpha}\to{}X_{\beta}$ 为乘积空间到 $X_{\beta}$ 的坐标投影.

(这里 $\bigotimes_{\alpha\in{}I}\mathcal{F}_{\alpha}$ 按**定义 4.5.7 (任意乘积 $\sigma$-代数)**, 是由所有柱集 $\pi_{\beta}^{-1}\left(A_{\beta}\right)$, $A_{\beta}\in\mathcal{F}_{\beta}$, $\beta\in{}I$ 生成的 $\sigma$-代数.)

### 解答 1

按**定义 5.4.4** (完备测度)**, 记 $\mathscr{G}:=\sigma\left(\left\{\pi_{\alpha}^{-1}\left(\mathcal{E}_{\alpha}\right):\alpha\in{}I\right\}\right)$. 分两个包含关系证明.

($\subset$) $\bigotimes_{\alpha\in{}I}\mathcal{F}_{\alpha}\subseteq\mathscr{G}$.

固定 $\alpha\in{}I$, 考虑 $\pi_{\alpha}:\prod_{\beta\in{}I}X_{\beta}\to{}X_{\alpha}$, 定义集合族

$$
\mathscr{C}_{\alpha}:=\left\{A\subseteq{}X_{\alpha}:\pi_{\alpha}^{-1}\left(A\right)\in\mathscr{G}\right\}.
$$

由原像运算保持补与可数并 (**定理 2.4.2 (原像运算的性质)**), $\mathscr{C}_{\alpha}$ 是 $\sigma$-代数. 又因 $\pi_{\alpha}^{-1}\left(\mathcal{E}_{\alpha}\right)\subseteq\mathscr{G}$ 由 $\mathscr{G}$ 的定义, 故 $\mathcal{E}_{\alpha}\subseteq\mathscr{C}_{\alpha}$. 从而 $\mathscr{C}_{\alpha}$ 是含 $\mathcal{E}_{\alpha}$ 的 $\sigma$-代数, 故含 $\sigma\left(\mathcal{E}_{\alpha}\right)=\mathcal{F}_{\alpha}$. 即对一切 $A\in\mathcal{F}_{\alpha}$, 有 $\pi_{\alpha}^{-1}\left(A\right)\in\mathscr{G}$.

由于 $\alpha\in{}I$ 任意, 所有柱集 $\pi_{\alpha}^{-1}\left(A\right)$ ($A\in\mathcal{F}_{\alpha}$, $\alpha\in{}I$) 都在 $\mathscr{G}$ 中. 而 $\bigotimes_{\alpha\in{}I}\mathcal{F}_{\alpha}$ 是由这些柱集生成的 $\sigma$-代数, 故

$$
\bigotimes_{\alpha\in{}I}\mathcal{F}_{\alpha}\subseteq\mathscr{G}.
$$

($\supset$) $\mathscr{G}\subseteq\bigotimes_{\alpha\in{}I}\mathcal{F}_{\alpha}$.

固定 $\alpha\in{}I$. 对任意 $E_{\alpha}\in\mathcal{E}_{\alpha}$, $\pi_{\alpha}^{-1}\left(E_{\alpha}\right)$ 恰是一个柱集 (**定义 4.5.7 (任意乘积 $\sigma$-代数)** 中取 $A_{\beta}=E_{\alpha}$ 当 $\beta=\alpha$), 故 $\pi_{\alpha}^{-1}\left(\mathcal{E}_{\alpha}\right)\subseteq\bigotimes_{\alpha\in{}I}\mathcal{F}_{\alpha}$. 于是所有生成元 $\pi_{\alpha}^{-1}\left(E_{\alpha}\right)$ ($\alpha\in{}I$) 都在乘积 $\sigma$-代数中, 而 $\bigotimes_{\alpha\in{}I}\mathcal{F}_{\alpha}$ 是含这些集合的 $\sigma$-代数, 故其生成的 $\sigma$-代数

$$
\mathscr{G}\subseteq\bigotimes_{\alpha\in{}I}\mathcal{F}_{\alpha}.
$$

两方向结合, 即

$$
\bigotimes_{\alpha\in{}I}\mathcal{F}_{\alpha}=\sigma\left(\left\{\pi_{\alpha}^{-1}\left(\mathcal{E}_{\alpha}\right):\alpha\in{}I\right\}\right).
$$

$\blacksquare$

## 2

证明**定理 5.4.6 (测度完备化定理)**: 任意测度空间 $\left(X,\mathcal{F},\mu\right)$ 都可以完备化. 即存在完备测度空间 $\left(X,\mathcal{M},\overline\mu\right)$ 使得:

(1) $\mathcal{F}\subset\mathcal{M}$;

(2) $\overline\mu|_{\mathcal{F}}=\mu$;

(3) $\mathcal{M}$ 是包含 $\mathcal{F}$ 的最小完备 $\sigma$-代数.

### 解答 2

记 $\mathcal{N}=\left\{N\in\mathcal{F}:\mu\left(N\right)=0\right\}$ 为零集全体 (**定义 5.4.1 (零集)**). 定义

$$
\mathcal{M}:=\left\{A\subset{}X:\exists\,B\in\mathcal{F},\exists\,N\in\mathcal{F},\mu\left(N\right)=0,\text{使~}B\subset{}A\subset{}B\cup{}N\right\},
$$

即 $A\in\mathcal{M}$ 当且仅当 $A$ 与某个可测集 $B$ 相差一个零测度集 (**定义 5.4.2 (零测度集)**). 分六步证明.

1. $\mathcal{M}$ 是 $\sigma$-代数. 逐条验证**定义 4.1.3 ($\sigma$-代数)**:

(1) $X\in\mathcal{M}$: 取 $B=X$, $N=\emptyset$, 则 $X\subset{}X\subset{}X\cup\emptyset$.

(2) 补运算封闭: 设 $B\subset{}A\subset{}B\cup{}N$, $\mu\left(N\right)=0$. 则 $\left(B\cup{}N\right)^{c}\subset{}A^{c}\subset{}B^{c}$, 且

$$
B^{c}\setminus\left(B\cup{}N\right)^{c}=B^{c}\cap\left(B\cup{}N\right)=B^{c}\cap{}N\subset{}N,
$$

故由**命题 5.2.2 (单调性)** 得 $\mu\left(B^{c}\setminus\left(B\cup{}N\right)^{c}\right)\le\mu\left(N\right)=0$. 于是 $A^{c}\in\mathcal{M}$ (取 $B'=\left(B\cup{}N\right)^{c}\in\mathcal{F}$, $N'=B^{c}\setminus\left(B\cup{}N\right)^{c}$).

(3) 可数并封闭: 设 $B_{n}\subset{}A_{n}\subset{}B_{n}\cup{}N_{n}$, $\mu\left(N_{n}\right)=0$. 则 $\bigcup_{n}B_{n}\subset\bigcup_{n}A_{n}\subset\left(\bigcup_{n}B_{n}\right)\cup\left(\bigcup_{n}N_{n}\right)$. 由**命题 5.2.3 (次可数可加性)**, $\mu\left(\bigcup_{n}N_{n}\right)\le\sum_{n}\mu\left(N_{n}\right)=0$, 故 $\bigcup_{n}N_{n}$ 是零测度集, 从而 $\bigcup_{n}A_{n}\in\mathcal{M}$.

故 $\mathcal{M}$ 是 $\sigma$-代数.

2. 定义 $\overline\mu:\mathcal{M}\to\left[0,+\infty\right]$, $\overline\mu\left(A\right):=\mu\left(B\right)$, 其中 $B\subset{}A\subset{}B\cup{}N$, $\mu\left(N\right)=0$. 先证良定义: 设 $B_{1}\subset{}A\subset{}B_{1}\cup{}N_{1}$ 与 $B_{2}\subset{}A\subset{}B_{2}\cup{}N_{2}$, $\mu\left(N_{1}\right)=\mu\left(N_{2}\right)=0$. 由 $B_{1}\subset{}A\subset{}B_{2}\cup{}N_{2}$ 得 $B_{1}\setminus{}B_{2}\subset{}N_{2}$, 故 $\mu\left(B_{1}\setminus{}B_{2}\right)\le\mu\left(N_{2}\right)=0$; 同理 $\mu\left(B_{2}\setminus{}B_{1}\right)=0$. 由**命题 5.2.1 (有限可加性)** 与**命题 5.2.2 (单调性)**,

$$
\mu\left(B_{1}\right)=\mu\left(B_{1}\cap{}B_{2}\right)+\mu\left(B_{1}\setminus{}B_{2}\right)=\mu\left(B_{1}\cap{}B_{2}\right)=\mu\left(B_{2}\right).
$$

故 $\overline\mu$ 良定义.

3. $\overline\mu$ 是测度. 逐条验证**定义 5.1.2 (测度)**: 非负性显然. 零空集性: $\overline\mu\left(\emptyset\right)=\mu\left(\emptyset\right)=0$. 可数可加性: 设 $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal{M}$ 两两不交, 写 $A_{n}=B_{n}\cup{}N_{n}$ ($B_{n}\in\mathcal{F}$, $N_{n}\subset{}N_{n}'\in\mathcal{N}$). 则 $\bigcup_{n}A_{n}=\left(\bigcup_{n}B_{n}\right)\cup\left(\bigcup_{n}N_{n}\right)\in\mathcal{M}$, 且 $\left\{B_{n}\right\}$ 两两不交 (因 $B_{n}\subset{}A_{n}$), 由 $\mu$ 的可数可加性

$$
\overline\mu\left(\bigcup_{n}A_{n}\right)=\mu\left(\bigcup_{n}B_{n}\right)=\sum_{n}\mu\left(B_{n}\right)=\sum_{n}\overline\mu\left(A_{n}\right).
$$

4. 延拓性: 对 $B\in\mathcal{F}$, 因 $B=B\cup\emptyset\in\mathcal{M}$, 故 $\overline\mu\left(B\right)=\mu\left(B\right)$, 即 $\overline\mu|_{\mathcal{F}}=\mu$.

5. 完备性 (定义 5.4.4 (完备测度)): 设 $\overline\mu\left(A\right)=0$, 即 $A=B\cup{}N$ 且 $\mu\left(B\right)=0$, $N\subset{}N_{0}\in\mathcal{N}$. 则 $A\subset{}B\cup{}N_{0}$, 且由**命题 5.2.3 (次可数可加性)**, $\mu\left(B\cup{}N_{0}\right)\le\mu\left(B\right)+\mu\left(N_{0}\right)=0$, 故 $A$ 是某个零测度集之子集. 于是 $A=\emptyset\cup{}A\in\mathcal{M}$, 且 $A$ 的任意子集 $C\subset{}A$ 亦满足 $C\subset{}B\cup{}N_{0}$, 故 $C\in\mathcal{M}$. 因此 $\mathcal{M}$ 完备.

6. 最小性: 设 $\mathcal{M}'$ 是任一包含 $\mathcal{F}$ 的完备 $\sigma$-代数. 对 $A=B\cup{}N\in\mathcal{M}$ ($B\in\mathcal{F}$, $N\subset{}N_{0}\in\mathcal{N}$), 因 $N_{0}\in\mathcal{F}\subset\mathcal{M}'$ 且 $\mu\left(N_{0}\right)=0$, 由 $\mathcal{M}'$ 的完备性得 $N\in\mathcal{M}'$; 又 $B\in\mathcal{F}\subset\mathcal{M}'$, 故 $A=B\cup{}N\in\mathcal{M}'$. 因此 $\mathcal{M}\subset\mathcal{M}'$. 故 $\mathcal{M}$ 是包含 $\mathcal{F}$ 的最小完备 $\sigma$-代数.

综上, $\left(X,\mathcal{M},\overline\mu\right)$ 是满足 (1)(2)(3) 的完备测度空间, 定理得证.

$\blacksquare$
