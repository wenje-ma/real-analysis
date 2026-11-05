# week4

> **定义 4.1.1 (集合代数)**
> 
> 设 $X$ 是非空集合, $\mathcal A\subset\mathcal P\left(X\right)$. 称 $\mathcal A$ 为 $X$ 上的一个集合代数, 若满足: (1) $X\in\mathcal A$; (2) 对差运算封闭: $A,B\in\mathcal A\Rightarrow A\setminus B\in\mathcal A$; (3) 对有限并封闭: $A,B\in\mathcal A\Rightarrow A\cup B\in\mathcal A$.

> **定义 4.1.3 ($\sigma$-代数)**
> 
> 设 $X$ 非空, $\mathcal F\subset\mathcal P\left(X\right)$. 称 $\mathcal F$ 为 $X$ 上的一个 $\sigma$-代数, 若满足: (1) $X\in\mathcal F$; (2) 对补运算封闭: $A\in\mathcal F\Rightarrow A^{c}\in\mathcal F$; (3) 对可数并封闭: $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal F\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal F$.

> **定义 4.3.2 (博雷尔 $\sigma$-代数)**
> 
> 设 $\left(X,\tau\right)$ 是拓扑空间, 由所有开集生成的 $\sigma$-代数称为博雷尔 $\sigma$-代数, 记作 $\mathcal B\left(X\right)$, 其中元素称为博雷尔集.

> **定义 4.4.1 (单调类)**
> 
> 设 $\mathcal M\subset\mathcal P\left(X\right)$. 称 $\mathcal M$ 为单调类, 若满足: (1) 对单调递增序列封闭: $A_{1}\subset A_{2}\subset\cdots$ 且 $A_{n}\in\mathcal M\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal M$; (2) 对单调递减序列封闭: $A_{1}\supset A_{2}\supset\cdots$ 且 $A_{n}\in\mathcal M\Rightarrow\bigcap_{n=1}^{\infty}A_{n}\in\mathcal M$.

> **定理 4.4.2 (单调类定理)**
> 
> 设 $\mathcal A$ 是一个代数, $\mathcal M$ 是一个包含 $\mathcal A$ 的单调类, 则 $\sigma\left(\mathcal A\right)\subset\mathcal M$.

> **定义 4.5.2 (乘积 $\sigma$-代数)**
> 
> 乘积 $\sigma$-代数 $\mathcal F\otimes\mathcal G$ 是包含所有可测矩形的最小 $\sigma$-代数: $\mathcal F\otimes\mathcal G:=\sigma\left(\left\{A\times B:A\in\mathcal F,B\in\mathcal G\right\}\right)$.

> **定理 4.5.4 (博雷尔集的乘积)**
> 
> 对欧氏空间中的博雷尔 $\sigma$-代数, 有

> **定义 5.1.2 (测度)**
> 
> 设 $\left(X,\mathcal F\right)$ 是一个可测空间. 函数 $\mu:\mathcal F\to\left[0,+\infty\right]$ 称为 $\left(X,\mathcal F\right)$ 上的一个测度, 如果满足: (1) 非负性: $\mu\left(E\right)\ge0$ 对一切 $E\in\mathcal F$ 成立; (2) 零空集性: $\mu\left(\emptyset\right)=0$; (3) 可数可加性 ($\sigma$-可加性): 对任意可数个两两不交的集合 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$, 有 $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **命题 5.2.1 (有限可加性)**
> 
> 设 $\mu$ 是 $\left(X,\mathcal F\right)$ 上的测度, $E_{1},\dots,E_{n}\in\mathcal F$ 是两两不交的集合, 则

> **命题 5.2.3 (次可数可加性)**
> 
> 设 $\mu$ 是测度, $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$ 是任意可数个集合 (不一定两两不交), 则

> **命题 5.2.4 (下连续性)**
> 
> 设 $\mu$ 是测度, $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$ 是单调递增的集合序列 (即 $E_{1}\subset E_{2}\subset\cdots$), 则

> **定义 6.1.1 (外测度)**
> 
> 设 $X$ 非空. 函数 $\mu^{*}:\mathcal P\left(X\right)\to\left[0,+\infty\right]$ 称为 $X$ 上的一个外测度, 若满足: (1) 非负性: $\mu^{*}\left(\varnothing\right)=0$, 且 $\mu^{*}\left(E\right)\ge0$ 对一切 $E\subset X$; (2) 单调性: $E\subset F\Rightarrow\mu^{*}\left(E\right)\le\mu^{*}\left(F\right)$; (3) 次可数可加性: $\mu^{*}\left(\bigcup_{n=1}^{\infty}E_{n}\right)\le\sum_{n=1}^{\infty}\mu^{*}\left(E_{n}\right)$.

> **定义 6.2.1 (准测度)**
> 
> 设 $X$ 是非空集合, $\mathcal E\subset\mathcal P\left(X\right)$ 是一个代数. 函数 $\mu_{0}:\mathcal E\to\left[0,+\infty\right]$ 称为一个准测度, 如果 $\mu_{0}\left(\emptyset\right)=0$, 且若 $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal E$ 两两不交且 $\bigcup_{n=1}^{\infty}E_{n}\in\mathcal E$, 则 $\mu_{0}\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu_{0}\left(E_{n}\right)$.

> **定理 6.2.2 (由准测度生成外测度)**
> 
> 设 $\mathcal E\subset\mathcal P\left(X\right)$ 是一个覆盖类, $\mu_{0}:\mathcal E\to\left[0,+\infty\right]$ 是一个准测度. 对任意 $A\subset X$, 定义

> **定义 6.3.1 (卡拉西奥多里条件)**
> 
> 设 $\mu^{*}$ 是 $X$ 上的外测度. 子集 $A\subset X$ 称为 $\mu^{*}$-可测的, 若对任意 $T\subset X$ 有

> **引理 6.3.2 (代数含于可测集)**
> 
> 如果 $\mathcal E$ 是代数, $\mu_{0}$ 是准测度, 则 $\mathcal E\subset\mathcal M_{\mu^{*}}$.

> **定理 6.3.3 (卡拉西奥多里定理)**
> 
> 设 $\mu^{*}$ 是 $X$ 上的外测度, 则: (1) $\mathcal M$ 是一个 $\sigma$-代数; (2) $\mu^{*}|_{\mathcal M}$ 是一个完备测度; (3) 如果 $\mu^{*}$ 是由准测度 $\mu_{0}$ 生成的, 且 $\mu_{0}$ 是 $\sigma$-有限的, 则 $\mu^{*}|_{\mathcal M}$ 是 $\mu_{0}$ 的唯一延拓.

> **定义 6.4.1 (h 区间)**
> 
> 令 $-\infty\le a< b< \infty$, 所有左开右闭区间 $\left(a,b\right]$, 以及 $\left(a,\infty\right)$, $\varnothing$ 称为 h 区间. h 区间的有限不交并形成的集族 $\mathcal E$ 为一个代数.

> **命题 6.4.2 ($\mathcal E$ 上的准测度)**
> 
> 设 $F:\mathbb R\to\mathbb R$ 为增的右连续函数. 对于不交区间 $\left(a_{i},b_{i}\right]$, $i=1,\dots,n$, 定义 $\mu_{0}\left(\bigcup_{i=1}^{n}\left(a_{i},b_{i}\right]\right):=\sum_{i=1}^{n}\left[F\left(b_{i}\right)-F\left(a_{i}\right)\right]$, 并令 $\mu_{0}\left(\varnothing\right)=0$. 则 $\mu_{0}$ 为 $\mathcal E$ 上的准测度.

> **定理 6.4.5 (勒贝格-斯蒂尔杰斯测度的正则性)**
> 
> 设 $\mu_{F}$ 是由增右连续函数 $F$ 生成的勒贝格-斯蒂尔杰斯测度, $\mathcal M^{*}$ 是 $\mu_{F}$-可测集的 $\sigma$-代数. 若 $E\in\mathcal M^{*}$, 则

> **定义 6.4.6 (勒贝格测度)**
> 
> 由 $F\left(x\right)=x$ 生成的测度称为勒贝格测度, 记作 $m$; 相应外测度定义的可测集称为勒贝格可测集, 全体记作 $\mathcal L$.

> **定义 6.5.1 (康托尔集的递归构造)**
> 
> 设 $C_{0}=\left[0,1\right]$. 对每个 $n\ge0$, 定义 $C_{n+1}=\frac{1}{3}C_{n}\cup\left(\frac{2}{3}+\frac{1}{3}C_{n}\right)$. 则康托尔集定义为 $C=\bigcap_{n=0}^{\infty}C_{n}$.

> **定理 6.5.2 (康托尔集的三进制刻画)**
> 
> 点 $x\in\left[0,1\right]$ 属于康托尔集 $C$ 当且仅当它的三进制展开 $x=\sum_{k=1}^{\infty}\frac{a_{k}}{3^{k}}$ 中不含数字 $1$ (即 $a_{k}\in\left\{0,2\right\}$).

> **定义 7.1.1 (可测映射)**
> 
> 设 $\left(X,\mathcal F\right)$, $\left(Y,\mathcal G\right)$ 为两个可测空间. 映射 $f:X\to Y$ 称为 $\left(\mathcal F,\mathcal G\right)$-可测的, 若对任意 $B\in\mathcal G$ 有 $f^{-1}\left(B\right)\in\mathcal F$.

> **命题 7.1.7 (乘积空间的可测性)**
> 
> 设 $f=\left(f_{1},\dots,f_{n}\right):X\to Y_{1}\times\cdots\times Y_{n}$. 在乘积空间配备乘积 $\sigma$-代数下, $f$ 可测当且仅当每个坐标映射 $f_{i}:X\to Y_{i}$ 可测.

> **定理 7.1.8 (实值可测函数的运算封闭性)**
> 
> 设 $f,g:X\to\mathbb R$ 可测, $c\in\mathbb R$, 则 $cf$, $f+g$, $fg$, $\max\left(f,g\right)$, $\min\left(f,g\right)$ 可测; 若 $\left\{f_{n}\right\}$ 可测且点点收敛, 则极限函数可测.

> **定理 7.1.9 (可测函数与连续函数的复合)**
> 
> 设 $f:X\to\mathbb R$ 可测, $g:\mathbb R\to\mathbb R$ 连续, 则 $g\circ f:X\to\mathbb R$ 可测.

> **例 7.3.5 (示性函数)**
> 
> 设 $A\subset X$, 则 $\chi_{A}:X\to\mathbb R$ 可测当且仅当 $A\in\mathcal F$.

## 1

由 $F\left(x\right)=x$ 构造的勒贝格测度 $m$ (**定义 6.4.6 (勒贝格测度)**) 满足:

(1) $m$ 是平移不变的: $m\left(E+x\right)=m\left(E\right)$ 对所有可测集 $E$ 和 $x\in\mathbb R$ 成立;

(2) $m$ 是尺度不变的: $m\left(rE\right)=\left|r\right|m\left(E\right)$ 对所有可测集 $E$ 和 $r\in\mathbb R$ 成立.

### 解答 1

设 $\mathcal E$ 是 h 区间代数, $\mu_{0}$ 是由 $F\left(x\right)=x$ 经**命题 6.4.2 ($\mathcal E$ 上的准测度)** 定义的准测度, 即对 h 区间 $\mu_{0}\left(\left(a,b\right]\right)=b-a$ (区间长度); 由**定理 6.2.2 (由准测度生成外测度)**, $\mu_{0}$ 生成外测度

$$
m^{*}\left(A\right)=\inf\left\{\sum_{n}\left(b_{n}-a_{n}\right):A\subset\bigcup_{n}\left(a_{n},b_{n}\right]\right\},
$$

且勒贝格测度 $m=m^{*}|_{\mathcal L}$ (**定义 6.4.6 (勒贝格测度)**).

(1) 先证外测度平移不变. 对 $A\subset\mathbb R$ 与 $x\in\mathbb R$, 平移 $\tau_{x}:t\mapsto t+x$ 把 h 区间映为 h 区间并保持长度: $\mu_{0}\left(I+x\right)=\mu_{0}\left(I\right)$. 故 $\left\{I_{n}\right\}$ 覆盖 $A$ 当且仅当 $\left\{I_{n}+x\right\}$ 覆盖 $A+x$, 且

$$
\sum_{n}\mu_{0}\left(I_{n}+x\right)=\sum_{n}\mu_{0}\left(I_{n}\right).
$$

由 $m^{*}$ 的定义 (下确界覆盖), 得 $m^{*}\left(A+x\right)=m^{*}\left(A\right)$.

再证可测性在平移下保持. 若 $E\in\mathcal L$ (即 $E$ 是 $m^{*}$-可测的, **定义 6.3.1 (卡拉西奥多里条件)**), 则对任意 $T\subset\mathbb R$,

$$
m^{*}\left(T\right)=m^{*}\left(T-x\right)=m^{*}\left(\left(T-x\right)\cap E\right)+m^{*}\left(\left(T-x\right)\cap E^{c}\right)=m^{*}\left(T\cap\left(E+x\right)\right)+m^{*}\left(T\cap\left(E+x\right)^{c}\right),
$$

其中第二步用 $E$ 的可测性于 $T-x$. 故 $E+x$ 可测. 于是对可测集 $E$,

$$
m\left(E+x\right)=m^{*}\left(E+x\right)=m^{*}\left(E\right)=m\left(E\right).
$$

(1) 得证.

(2) 对 $r\ne0$, 伸缩 $\delta_{r}:t\mapsto rt$ 把 h 区间 $\left(a,b\right]$ 映为 $\left(ra,rb\right]$ ($r> 0$) 或 $\left(rb,ra\right]$ ($r< 0$), 仍是 h 区间, 且长度变为 $\left|r\right|\left(b-a\right)$, 即 $\mu_{0}\left(rI\right)=\left|r\right|\mu_{0}\left(I\right)$. 与 (1) 同理得 $m^{*}\left(rA\right)=\left|r\right|m^{*}\left(A\right)$, 且 $E$ 可测推出 $rE$ 可测 (用**定义 6.3.1 (卡拉西奥多里条件)** 与伸缩). 故 $m\left(rE\right)=\left|r\right|m\left(E\right)$. 当 $r=0$ 时, $0\cdot E$ 为空集或 $\left\{0\right\}$, 测度均为 $0=\left|0\right|m\left(E\right)$. (2) 得证. $\blacksquare$

## 2

设康托尔集 $C=\bigcap_{n=0}^{\infty}C_{n}$ (**定义 6.5.1 (康托尔集的递归构造)**). 证明 $C$ 具有以下性质:

1. 紧致性: $C$ 是有界闭集;

2. 完备性: $C$ 是完备度量空间 (任何柯西序列收敛);

3. 完全不连通: $C$ 的连通子集只有单点集;

4. 无处稠密: $C$ 的内部为空集;

5. 完美集: $C$ 是闭集且没有孤立点.

### 解答 2

由**定理 6.5.2 (康托尔集的三进制刻画)**, $x\in C$ 当且仅当 $x$ 的三进制展开 $x=\sum_{k=1}^{\infty}\frac{a_{k}}{3^{k}}$ 满足 $a_{k}\in\left\{0,2\right\}$.

1. 紧致性. 由**定义 6.5.1 (康托尔集的递归构造)**, 每个 $C_{n}$ 是从 $\left[0,1\right]$ 去掉有限个开区间 (第 $n$ 步挖去的开区间) 所得, 故 $C_{n}$ 是有限个闭区间之并, 从而是闭集. $C=\bigcap_{n=0}^{\infty}C_{n}$ 是闭集的交, 故 $C$ 是闭集, 且 $C\subset\left[0,1\right]$ 有界. 由海涅-博雷尔定理, $\mathbb R$ 中有界闭集紧致, 故 $C$ 紧致. $\blacksquare$

2. 完备性. $\mathbb R$ 是完备度量空间, $C$ 是 $\mathbb R$ 的闭子集. 若 $\left\{x_{n}\right\}\subset C$ 是柯西列, 则它在 $\mathbb R$ 中收敛于某 $x$; 因 $C$ 闭, $x\in C$. 故 $C$ 中任何柯西列收敛, $C$ 完备. $\blacksquare$

3. 完全不连通. 设 $K\subset C$ 连通且含有 $x< y$ 两点. 由**定理 6.5.2 (康托尔集的三进制刻画)**, $x,y$ 的三进制展开不含数字 $1$. 因 $x\ne y$, 存在最小的 $n$ 使 $x,y$ 的三进制第 $n$ 位不同, 不妨设 $x$ 的第 $n$ 位为 $0$, $y$ 的第 $n$ 位为 $2$ (前 $n-1$ 位相同). 则第 $n$ 步挖去的开区间中有一个 $J=\left(\alpha,\beta\right)$ 位于 $x$ 与 $y$ 之间 (即 $x< \alpha< \beta< y$), 且 $J\cap C=\varnothing$. 于是

$$
K=\left(K\cap\left(-\infty,\alpha\right]\right)\cup\left(K\cap\left[\beta,\infty\right)\right),
$$

是两个非空, 互不相交的 $K$-相对开集 (因 $K\subset C$, $K\cap J=\varnothing$), 与 $K$ 连通矛盾. 故 $K$ 只能是单点集. $\blacksquare$

4. 无处稠密. 任取非空开区间 $\left(\alpha,\beta\right)\subset\mathbb R$. 若它与 $\left[0,1\right]$ 相交, 取 $n$ 使 $3^{-n}< \beta-\alpha$. 第 $n$ 步后 $C_{n}$ 是 $2^{n}$ 个长度 $3^{-n}$ 的闭区间之并, 这些闭区间之间的 $2^{n}-1$ 个开区间 (第 $n$ 步挖去的) 覆盖了 $\left[0,1\right]$ 中除端点外的部分, 且挖去区间的长度均为 $3^{-n}$. 因 $\left(\alpha,\beta\right)$ 长度大于 $3^{-n}$, 它必包含某个第 $n$ 步挖去的开区间, 故 $\left(\alpha,\beta\right)$ 不全含于 $C$. 所以 $C$ 不含任何非空开区间, $\operatorname{int}\left(C\right)=\varnothing$, 即 $C$ 无处稠密. $\blacksquare$

5. 完美集. 闭集已由 (1) 证得. 证 $C$ 无孤立点: 设 $x\in C$, 对任意 $\varepsilon> 0$, 由**定理 6.5.2 (康托尔集的三进制刻画)** 写 $x=\sum_{k=1}^{\infty}\frac{a_{k}}{3^{k}}$, $a_{k}\in\left\{0,2\right\}$. 取 $n$ 使 $\frac{2}{3^{n+1}}< \varepsilon$, 令 $x_{n}$ 为三进制展开中把 $x$ 的第 $n+1$ 位 $a_{n+1}$ 换成 $2-a_{n+1}$, 其余位不变所得的点. 则 $x_{n}\in C$ (三进制不含 $1$), $x_{n}\ne x$, 且

$$
\left|x_{n}-x\right|=\left|\frac{2-a_{n+1}}{3^{n+1}}-\frac{a_{n+1}}{3^{n+1}}\right|=\frac{2}{3^{n+1}}< \varepsilon.
$$

故 $x$ 的 $\varepsilon$ 邻域内含有 $C$ 中异于 $x$ 的点, $x$ 不是孤立点. 所以 $C$ 是完美集. $\blacksquare$

## 3

证明习题 30, 33.

30. 设 $E\in\mathcal L$ 且 $m\left(E\right)> 0$. 证明对任意 $\alpha< 1$, 存在开区间 $I$ 使 $m\left(E\cap I\right)> \alpha m\left(I\right)$.

33. 证明存在博雷尔集 $A\subset\left[0,1\right]$ 使对 $\left[0,1\right]$ 的每个子区间 $I$, 都有 $0< m\left(A\cap I\right)< m\left(I\right)$. (提示: $\left[0,1\right]$ 的每个子区间都含正测度的康托尔型集.)

### 解答 3

30. 反证. 假设存在 $\alpha< 1$ 使对每个开区间 $I$, 均有 $m\left(E\cap I\right)\le\alpha m\left(I\right)$. 则对任意开集 $U$, 把 $U$ 表为可数个互不相交开区间的并 $U=\bigcup_{k}I_{k}$, 由 $m$ 的可数可加性,

$$
m\left(E\cap U\right)=\sum_{k}m\left(E\cap I_{k}\right)\le\alpha\sum_{k}m\left(I_{k}\right)=\alpha m\left(U\right).
$$

由勒贝格-斯蒂尔杰斯测度的外正则性 (**定理 6.4.5 (勒贝格-斯蒂尔杰斯测度的正则性)**), $m\left(E\right)=\inf\left\{m\left(U\right):E\subset U\text{ 开}\right\}$. 取一列开集 $U_{n}\supset E$ 使 $m\left(U_{n}\right)\to m\left(E\right)$. 因 $E\subset U_{n}$, $E=E\cap U_{n}$, 故

$$
m\left(E\right)=m\left(E\cap U_{n}\right)\le\alpha m\left(U_{n}\right)\to\alpha m\left(E\right).
$$

于是 $m\left(E\right)\le\alpha m\left(E\right)$. 因 $m\left(E\right)> 0$, 得 $\alpha\ge1$, 与 $\alpha< 1$ 矛盾. 故存在开区间 $I$ 使 $m\left(E\cap I\right)> \alpha m\left(I\right)$. $\blacksquare$

33. 用正测度的广义康托尔集 (广义康托尔集). 设 $\left\{I_{n}\right\}$ 是 $\left[0,1\right]$ 中所有以有理数为端点的开区间的枚举. 归纳地选取两两不交的闭区间 $J_{n}\subset I_{n}$ (取 $J_{n}$ 避开之前所有 $J_{k}$), 使每个子区间 $I$ 都含某个 $J_{n}$ (因 $\left\{I_{n}\right\}$ 枚举有理区间, 每个子区间含某个 $I_{n}$, 而 $J_{n}\subset I_{n}$). 固定 $c\in\left(0,1\right)$. 在每个 $J_{n}$ 内取广义康托尔集 $C_{n}\subset J_{n}$, 使 $m\left(C_{n}\right)=c\,m\left(J_{n}\right)$ (由广义康托尔集测度可为任意 $\beta\in\left(0,1\right)$). 因 $J_{n}$ 两两不交, $C_{n}$ 两两不交. 令 $A=\bigcup_{n=1}^{\infty}C_{n}$, 则 $A$ 是可数个闭集之并, 从而是博雷尔集, 且 $A\subset\left[0,1\right]$.

先证下界. 对任意子区间 $I\subset\left[0,1\right]$, 存在 $n$ 使 $J_{n}\subset I_{n}\subset I$, 故

$$
m\left(A\cap I\right)\ge m\left(A\cap J_{n}\right)=m\left(C_{n}\right)=c\,m\left(J_{n}\right)> 0.
$$

再证上界. 因 $C_{n}\subset J_{n}$ 且 $\left\{J_{n}\right\}$ 两两不交,

$$
m\left(A\cap I\right)=m\left(\bigcup_{n}C_{n}\cap I\right)=\sum_{n}m\left(C_{n}\cap I\right)=\sum_{J_{n}\subset I}m\left(C_{n}\right)=c\sum_{J_{n}\subset I}m\left(J_{n}\right)=c\,m\left(\bigcup_{J_{n}\subset I}J_{n}\right)\le c\,m\left(I\right)< m\left(I\right),
$$

其中仅当 $J_{n}\cap I$ 有正测度 (即 $J_{n}\subset I$, 至多相差端点) 时 $m\left(C_{n}\cap I\right)=m\left(C_{n}\right)$ 非零. 故对 $\left[0,1\right]$ 的每个子区间 $I$, 有 $0< m\left(A\cap I\right)< m\left(I\right)$. $\blacksquare$

## 4

设 $\left(X,\mathcal M\right)$ 是可测空间, $\left\{f_{n}\right\}$ 是一列可测函数. 证明: 若 $\left\{f_{n}\right\}$ 是 $X$ 上的一列可测函数, 则 $\left\{x:\lim_{n\to\infty}f_{n}\left(x\right)\text{ 存在}\right\}$ 是可测集.

### 解答 4

对 $m,n\in\mathbb N$, 由**定理 7.1.8 (实值可测函数的运算封闭性)** (1), 差 $f_{m}-f_{n}$ 可测. 由**定义 7.1.1 (可测映射)**, 开区间 $\left(-\frac{1}{k},\frac{1}{k}\right)$ 的原像可测:

$$
E_{k,m,n}:=\left\{x:\left|f_{m}\left(x\right)-f_{n}\left(x\right)\right|< \frac{1}{k}\right\}=\left(f_{m}-f_{n}\right)^{-1}\left(\left(-\frac{1}{k},\frac{1}{k}\right)\right)\in\mathcal M.
$$

由实数的完备性, $\lim_{n\to\infty}f_{n}\left(x\right)$ 存在当且仅当 $\left\{f_{n}\left(x\right)\right\}$ 是柯西列, 即对每个 $k\in\mathbb N$ 存在 $N$ 使对所有 $m,n\ge N$ 有 $\left|f_{m}\left(x\right)-f_{n}\left(x\right)\right|< \frac{1}{k}$. 故

$$
\left\{x:\lim_{n\to\infty}f_{n}\left(x\right)\text{ 存在}\right\}=\bigcap_{k=1}^{\infty}\bigcup_{N=1}^{\infty}\bigcap_{m,n\ge N}E_{k,m,n}.
$$

由于 $\mathcal M$ 对可数交与可数并封闭 (**定义 4.1.3 ($\sigma$-代数)**), 且 $\bigcap_{m,n\ge N}E_{k,m.n}$ 是可数交, 故上述集合可测. $\blacksquare$

## 5

证明: $X$ 上不可数个可测实值函数的上确界可以不是可测函数 (除非 $\sigma$-代数 $\mathcal M$ 十分特殊).

### 解答 5

取 $X=\mathbb R$ 配勒贝格 $\sigma$-代数 $\mathcal L$. 设 $A\subset\mathbb R$ 是勒贝格不可测集 (存在勒贝格不可测集 (维塔利集)). 对每个 $a\in A$, 定义 $f_{a}:=\chi_{\left\{a\right\}}$ 为单点指示函数. 因单点集 $\left\{a\right\}$ 是闭集, 从而是博雷尔集, 故 $f_{a}$ 可测. 但不可数族 $\left\{f_{a}:a\in A\right\}$ 的上确界满足

$$
\sup_{a\in A}f_{a}\left(x\right)=\begin{cases}1,&x\in A,\\0,&x\notin A,\end{cases}
$$

即 $\sup_{a\in A}f_{a}=\chi_{A}$. 由**例 7.3.5 (示性函数)**, $\chi_{A}$ 可测当且仅当 $A\in\mathcal L$, 与 $A$ 不可测矛盾. 故不可数个可测实值函数的上确界可以不是可测函数. $\blacksquare$

## 6

设 $f$ 是 $\mathbb R\times\mathbb R^{k}$ 上的函数, 使得对每个 $x\in\mathbb R$, $f\left(x,\cdot\right)$ 是博雷尔可测的, 且对每个 $y\in\mathbb R^{k}$, $f\left(\cdot,y\right)$ 是连续的. 对 $n\in\mathbb N$, 令 $a_{i}=i/n$, 定义: 当 $a_{i}\le x\le a_{i+1}$ 时,

$$
f_{n}\left(x,y\right)=\frac{f\left(a_{i+1},y\right)\left(x-a_{i}\right)-f\left(a_{i},y\right)\left(x-a_{i+1}\right)}{a_{i+1}-a_{i}}.
$$

证明 $f_{n}$ 在 $\mathbb R\times\mathbb R^{k}$ 上博雷尔可测且 $f_{n}\to f$ 点点收敛, 从而 $f$ 在 $\mathbb R\times\mathbb R^{k}$ 上博雷尔可测. 并由此归纳证明: $\mathbb R^{n}$ 上每个逐变量连续的函数都是博雷尔可测的.

### 解答 6

固定 $n$, 记 $c_{i}:=a_{i+1}-a_{i}=\frac{1}{n}$, 并取半开区间 $\Delta_{i}:=\left[a_{i},a_{i+1}\right)$ ($i\in\mathbb Z$). 由于题设的插值公式在端点 $x=a_{i+1}$ 处两段均取 $f\left(a_{i+1},y\right)$, 故可用半开区间无歧义地表示. 在 $\Delta_{i}$ 上,

$$
f_{n}\left(x,y\right)=\frac{x-a_{i}}{c_{i}}f\left(a_{i+1},y\right)+\frac{a_{i+1}-x}{c_{i}}f\left(a_{i},y\right),
$$

从而

$$
f_{n}\left(x,y\right)=\sum_{i\in\mathbb Z}\left[\frac{x-a_{i}}{c_{i}}\chi_{\Delta_{i}}\left(x\right)f\left(a_{i+1},y\right)+\frac{a_{i+1}-x}{c_{i}}\chi_{\Delta_{i}}\left(x\right)f\left(a_{i},y\right)\right].
$$

先证 $f_{n}$ 可测. 对每个 $i$, 函数 $\left(x,y\right)\mapsto\frac{x-a_{i}}{c_{i}}\chi_{\Delta_{i}}\left(x\right)$ 与 $\left(x,y\right)\mapsto\frac{a_{i+1}-x}{c_{i}}\chi_{\Delta_{i}}\left(x\right)$ 只依赖于 $x$, 是连续函数与半开区间示性函数之积, 故为 $\mathbb R$ 上的博雷尔函数; 由题设, $f\left(a_{i},y\right)$ 与 $f\left(a_{i+1},y\right)$ 是 $\mathbb R^{k}$ 上的博雷尔函数. 由**定理 4.5.4 (博雷尔集的乘积)** 与**定义 4.5.2 (乘积 $\sigma$-代数)**, 乘积 $\sigma$-代数满足 $\mathcal B\left(\mathbb R\right)\otimes\mathcal B\left(\mathbb R^{k}\right)=\mathcal B\left(\mathbb R^{1+k}\right)$, 且由**命题 7.1.7 (乘积空间的可测性)**, 只依赖 $x$ 的博雷尔函数与只依赖 $y$ 的博雷尔函数之积, 作为 $\mathbb R\times\mathbb R^{k}$ 上的二元函数是可测的. 再由**定理 7.1.8 (实值可测函数的运算封闭性)** (1) (有限线性组合), $f_{n}$ 是 $\mathbb R\times\mathbb R^{k}$ 上的博雷尔函数.

再证 $f_{n}\to f$ 点点收敛. 固定 $\left(x,y\right)\in\mathbb R\times\mathbb R^{k}$. 因 $f\left(\cdot,y\right)$ 连续, 当 $n\to\infty$ 时网格 $a_{i}=i/n$ 加密, 使 $a_{i}\to x$, $a_{i+1}\to x$, 故 $f\left(a_{i},y\right)\to f\left(x,y\right)$, $f\left(a_{i+1},y\right)\to f\left(x,y\right)$; 而插值系数 $\frac{x-a_{i}}{c_{i}}$, $\frac{a_{i+1}-x}{c_{i}}\in\left[0,1\right]$ 有界. 故 $f_{n}\left(x,y\right)\to f\left(x,y\right)$.

由**定理 7.1.8 (实值可测函数的运算封闭性)** (4) (点点收敛极限可测), $f=\lim_{n}f_{n}$ 在 $\mathbb R\times\mathbb R^{k}$ 上博雷尔可测.

最后归纳证明: $\mathbb R^{n}$ 上逐变量连续的函数博雷尔可测. $n=1$ 时连续函数把开集拉回为开集, 故由**定义 4.3.2 (博雷尔 $\sigma$-代数)** 与**定义 7.1.1 (可测映射)** 可测 (亦为**定理 7.1.9 (可测函数与连续函数的复合)**). 设 $n-1$ 情形成立. 对 $\mathbb R^{n}=\mathbb R\times\mathbb R^{n-1}$ 上逐变量连续的函数 $f$, 对每个 $x$, $f\left(x,\cdot\right)$ 是 $\mathbb R^{n-1}$ 上的逐变量连续函数, 由归纳假设博雷尔可测; 对每个 $y$, $f\left(\cdot,y\right)$ 连续. 由上面已证的结论, $f$ 在 $\mathbb R\times\mathbb R^{n-1}$ 上博雷尔可测, 即 $f$ 在 $\mathbb R^{n}$ 上博雷尔可测. $\blacksquare$
