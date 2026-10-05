# 作业 4

> **定义 4.1.3** ($\sigma$-代数)<br>设 $X$ 非空, $\mathcal F\subset\mathcal P\left(X\right)$. 称 $\mathcal F$ 为 $X$ 上的一个 **$\sigma$-代数**, 若满足:<br>(1) $X\in\mathcal F$;<br>(2) 对补运算封闭: $A\in\mathcal F\Rightarrow A^{c}\in\mathcal F$;<br>(3) 对可数并封闭: $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal F\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal F$.

> **定义 4.3.2** (博雷尔 $\sigma$-代数)<br>设 $\left(X,\tau\right)$ 是一个拓扑空间. 由所有开集生成的 $\sigma$-代数称为**博雷尔 $\sigma$-代数**, 记作 $\mathcal B\left(X\right)$; 其元素称为**博雷尔集**.

> **定义 4.5.2** (乘积 $\sigma$-代数)<br>乘积 $\sigma$-代数 $\mathcal F\otimes\mathcal G$ 是包含所有可测矩形的最小 $\sigma$-代数: $\mathcal F\otimes\mathcal G:=\sigma\left(\left\{A\times B:A\in\mathcal F,B\in\mathcal G\right\}\right)$.

> **定理 4.5.4** (博雷尔集的乘积)<br>对于欧氏空间中的博雷尔 $\sigma$-代数, 有 $\mathcal B\left(\mathbb R^{m}\right)\otimes\mathcal B\left(\mathbb R^{n}\right)=\mathcal B\left(\mathbb R^{m+n}\right)$.

> **定义 7.1.1** (可测映射)<br>设 $\left(X,\mathcal F\right)$, $\left(Y,\mathcal G\right)$ 为两个可测空间. 映射 $f:X\to Y$ 称为 $\left(\mathcal F,\mathcal G\right)$-**可测**的, 若对任意 $B\in\mathcal G$ 有 $f^{-1}\left(B\right)\in\mathcal F$.

> **命题 7.1.7** (乘积空间的可测性)<br>设 $f=\left(f_{1},\dots,f_{n}\right):X\to Y_{1}\times\cdots\times Y_{n}$. 在乘积空间配备乘积 $\sigma$-代数下, $f$ 可测当且仅当每个坐标映射 $f_{i}:X\to Y_{i}$ 可测.

> **定理 7.1.8** (实值可测函数的运算封闭性)<br>设 $f,g:X\to\mathbb R$ 可测, $c\in\mathbb R$, 则:<br>(1) $cf$, $f+g$, $fg$, $\max\left(f,g\right)$, $\min\left(f,g\right)$ 可测;<br>(2) 若 $g\left(x\right)\ne0$ 对所有 $x$, 则 $f/g$ 可测;<br>(3) 若 $\left\{f_{n}\right\}$ 可测, 则 $\sup_{n}f_{n}$, $\inf_{n}f_{n}$, $\limsup_{n\to\infty}f_{n}$, $\liminf_{n\to\infty}f_{n}$ 可测;<br>(4) 若 $\left\{f_{n}\right\}$ 点点收敛, 则极限函数 $\lim_{n\to\infty}f_{n}$ 可测.

> **定理 7.1.9** (可测函数与连续函数的复合)<br>设 $f:X\to\mathbb R$ 可测, $g:\mathbb R\to\mathbb R$ 连续, 则 $g\circ f:X\to\mathbb R$ 可测.

> **例 7.3.5** (示性函数)<br>设 $A\subset X$, 则 $\chi_{A}:X\to\mathbb R$ 可测当且仅当 $A\in\mathcal F$.

> **基础知识**<br>**存在勒贝格不可测集** (维塔利集): 在勒贝格测度空间 $\left(\mathbb R,\mathcal L,m\right)$ 中, 存在 $A\subset\mathbb R$ 使 $A\notin\mathcal L$. 其构造基于选择公理: 在 $\mathbb R/\mathbb Q$ 的每个等价类中选取一个代表元, 所得集合即为勒贝格不可测集.

### 习题一

设 $\left(X,\mathcal M\right)$ 是可测空间, $\left\{f_{n}\right\}$ 是一列可测函数. 证明下列命题 (习题 3、6、11).

**3.** 若 $\left\{f_{n}\right\}$ 是 $X$ 上的一列可测函数, 则 $\left\{x:\lim_{n\to\infty}f_{n}\left(x\right)\text{存在}\right\}$ 是可测集.

**6.** 证明: $X$ 上不可数个可测实值函数的上确界可以不是可测函数 (除非 $\sigma$-代数 $\mathcal M$ 十分特殊).

**11.** 设 $f$ 是 $\mathbb R\times\mathbb R^{k}$ 上的函数, 使得对每个 $x\in\mathbb R$, $f\left(x,\cdot\right)$ 是博雷尔可测的, 且对每个 $y\in\mathbb R^{k}$, $f\left(\cdot,y\right)$ 是连续的. 对 $n\in\mathbb N$, 令 $a_{i}=i/n$, 定义: 当 $a_{i}\le x\le a_{i+1}$ 时,

$$
f_{n}\left(x,y\right)=\frac{f\left(a_{i+1},y\right)\left(x-a_{i}\right)-f\left(a_{i},y\right)\left(x-a_{i+1}\right)}{a_{i+1}-a_{i}}.
$$

证明 $f_{n}$ 在 $\mathbb R\times\mathbb R^{k}$ 上博雷尔可测且 $f_{n}\to f$ 点点收敛, 从而 $f$ 在 $\mathbb R\times\mathbb R^{k}$ 上博雷尔可测. 并由此归纳证明: $\mathbb R^{n}$ 上每个逐变量连续的函数都是博雷尔可测的.

### 解答 习题一

#### 3

对 $m,n\in\mathbb N$, 由**定理 7.1.8**(1), 差 $f_{m}-f_{n}$ 可测. 由**定义 7.1.1**, 开区间 $\left(-\frac{1}{k},\frac{1}{k}\right)$ 的原像可测:

$$
E_{k,m,n}:=\left\{x:\left|f_{m}\left(x\right)-f_{n}\left(x\right)\right|<\frac{1}{k}\right\}=\left(f_{m}-f_{n}\right)^{-1}\left(\left(-\frac{1}{k},\frac{1}{k}\right)\right)\in\mathcal M.
$$

由实数的完备性, $\lim_{n\to\infty}f_{n}\left(x\right)$ 存在当且仅当 $\left\{f_{n}\left(x\right)\right\}$ 是柯西列, 即对每个 $k\in\mathbb N$ 存在 $N$ 使对所有 $m,n\ge N$ 有 $\left|f_{m}\left(x\right)-f_{n}\left(x\right)\right|<\frac{1}{k}$. 故

$$
\left\{x:\lim_{n\to\infty}f_{n}\left(x\right)\text{存在}\right\}=\bigcap_{k=1}^{\infty}\bigcup_{N=1}^{\infty}\bigcap_{m,n\ge N}E_{k,m,n}.
$$

由于 $\mathcal M$ 对可数交与可数并封闭 (**定义 4.1.3**), 且 $\bigcap_{m,n\ge N}E_{k,m,n}$ 是可数交, 故上述集合可测. $\blacksquare$

#### 6

取 $X=\mathbb R$ 配勒贝格 $\sigma$-代数 $\mathcal L$. 设 $A\subset\mathbb R$ 是勒贝格不可测集 (基础知识, 维塔利集). 对每个 $a\in A$, 定义 $f_{a}:=\chi_{\left\{a\right\}}$ 为单点指示函数. 因单点集 $\left\{a\right\}$ 是闭集, 从而是博雷尔集, 故 $f_{a}$ 可测. 但不可数族 $\left\{f_{a}:a\in A\right\}$ 的上确界满足

$$
\sup_{a\in A}f_{a}\left(x\right)=\begin{cases}1,&x\in A,\\0,&x\notin A,\end{cases}
$$

即 $\sup_{a\in A}f_{a}=\chi_{A}$. 由**例 7.3.5**, $\chi_{A}$ 可测当且仅当 $A\in\mathcal L$, 与 $A$ 不可测矛盾. 故不可数个可测实值函数的上确界可以不是可测函数. $\blacksquare$

#### 11

固定 $n$, 记 $c_{i}:=a_{i+1}-a_{i}=\frac{1}{n}$, 并取半开区间 $\Delta_{i}:=\left[a_{i},a_{i+1}\right)$ ($i\in\mathbb Z$). 由于题设的插值公式在端点 $x=a_{i+1}$ 处两段均取 $f\left(a_{i+1},y\right)$, 故可用半开区间无歧义地表示. 在 $\Delta_{i}$ 上,

$$
f_{n}\left(x,y\right)=\frac{x-a_{i}}{c_{i}}f\left(a_{i+1},y\right)+\frac{a_{i+1}-x}{c_{i}}f\left(a_{i},y\right),
$$

从而

$$
f_{n}\left(x,y\right)=\sum_{i\in\mathbb Z}\left[\frac{x-a_{i}}{c_{i}}\chi_{\Delta_{i}}\left(x\right)f\left(a_{i+1},y\right)+\frac{a_{i+1}-x}{c_{i}}\chi_{\Delta_{i}}\left(x\right)f\left(a_{i},y\right)\right].
$$

先证 $f_{n}$ 可测. 对每个 $i$, 函数 $\left(x,y\right)\mapsto\frac{x-a_{i}}{c_{i}}\chi_{\Delta_{i}}\left(x\right)$ 与 $\left(x,y\right)\mapsto\frac{a_{i+1}-x}{c_{i}}\chi_{\Delta_{i}}\left(x\right)$ 只依赖于 $x$, 是连续函数与半开区间示性函数之积, 故为 $\mathbb R$ 上的博雷尔函数; 由题设, $f\left(a_{i},y\right)$ 与 $f\left(a_{i+1},y\right)$ 是 $\mathbb R^{k}$ 上的博雷尔函数. 由**定理 4.5.4** 与**定义 4.5.2**, 乘积 $\sigma$-代数满足 $\mathcal B\left(\mathbb R\right)\otimes\mathcal B\left(\mathbb R^{k}\right)=\mathcal B\left(\mathbb R^{1+k}\right)$, 且由**命题 7.1.7**, 只依赖 $x$ 的博雷尔函数与只依赖 $y$ 的博雷尔函数之积, 作为 $\mathbb R\times\mathbb R^{k}$ 上的二元函数是可测的. 再由**定理 7.1.8**(1) (有限线性组合), $f_{n}$ 是 $\mathbb R\times\mathbb R^{k}$ 上的博雷尔函数.

再证 $f_{n}\to f$ 点点收敛. 固定 $\left(x,y\right)\in\mathbb R\times\mathbb R^{k}$. 因 $f\left(\cdot,y\right)$ 连续, 当 $n\to\infty$ 时网格 $a_{i}=i/n$ 加密, 使 $a_{i}\to x$, $a_{i+1}\to x$, 故 $f\left(a_{i},y\right)\to f\left(x,y\right)$, $f\left(a_{i+1},y\right)\to f\left(x,y\right)$; 而插值系数 $\frac{x-a_{i}}{c_{i}}$, $\frac{a_{i+1}-x}{c_{i}}\in\left[0,1\right]$ 有界. 故 $f_{n}\left(x,y\right)\to f\left(x,y\right)$.

由**定理 7.1.8**(4) (点点收敛极限可测), $f=\lim_{n}f_{n}$ 在 $\mathbb R\times\mathbb R^{k}$ 上博雷尔可测.

最后归纳证明: $\mathbb R^{n}$ 上逐变量连续的函数博雷尔可测. $n=1$ 时连续函数把开集拉回为开集, 故由**定义 4.3.2** 与**定义 7.1.1** 可测 (亦为**定理 7.1.9**). 设 $n-1$ 情形成立. 对 $\mathbb R^{n}=\mathbb R\times\mathbb R^{n-1}$ 上逐变量连续的函数 $f$, 对每个 $x$, $f\left(x,\cdot\right)$ 是 $\mathbb R^{n-1}$ 上的逐变量连续函数, 由归纳假设博雷尔可测; 对每个 $y$, $f\left(\cdot,y\right)$ 连续. 由上面已证的结论, $f$ 在 $\mathbb R\times\mathbb R^{n-1}$ 上博雷尔可测, 即 $f$ 在 $\mathbb R^{n}$ 上博雷尔可测. $\blacksquare$
