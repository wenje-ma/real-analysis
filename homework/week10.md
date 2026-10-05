# 作业 10

> **定义 11.4.1** (相互奇异)<br>设 $\mu$ 和 $\nu$ 是可测空间 $\left(X,\mathcal F\right)$ 上的两个符号测度. 若存在可测集 $E\in\mathcal F$ 使得 $E$ 为 $\mu$-零集且 $E^{c}$ 为 $\nu$-零集, 则称 $\mu$ 和 $\nu$ 相互奇异, 记为 $\mu\perp\nu$.

> **基础知识** (哈代-利特尔伍德极大函数)<br>设 $f\in L^{1}_{\mathrm{loc}}\left(\mathbb R^{n}\right)$. 定义 $f$ 的哈代-利特尔伍德极大函数 $$Mf\left(x\right)=\sup_{r>0}\frac{1}{\left|B\left(x,r\right)\right|}\int_{B\left(x,r\right)}\left|f\left(y\right)\right|\mathrm{d}y,$$ 其中 $B\left(x,r\right)$ 是以 $x$ 为中心、$r$ 为半径的开球, $\left|B\left(x,r\right)\right|$ 表示其勒贝格测度.

> **基础知识** (球体积公式)<br>设 $C_{n}=m\left(B\left(1,0\right)\right)$ 为单位球的勒贝格测度, 则对任意 $x\in\mathbb R^{n}$, $r>0$,<br>$$m\left(B\left(x,r\right)\right)=C_{n}r^{n}.$$

> **基础知识** (正则博雷尔测度)<br>设 $\nu$ 是 $\mathbb R^{n}$ 上的博雷尔测度. 称 $\nu$ 为**正则的**, 若:<br>(1) 对每个紧集 $K$, 有 $\nu\left(K\right)<\infty$;<br>(2) 对每个 $E\in\mathcal B\left(\mathbb R^{n}\right)$, 有 $\nu\left(E\right)=\inf\left\{\nu\left(U\right):U\text{开集},E\subset U\right\}$.

### 习题一

**22.** 设 $f\in L^{1}\left(\mathbb R^{n}\right)$ 且 $f\ne0$. 证明存在 $C,R>0$ 使得 $Hf\left(x\right)\ge C\left|x\right|^{-n}$ 对 $\left|x\right|>R$ 成立. 从而当 $\lambda$ 充分小时, $m\left(\left\{x:Hf\left(x\right)>\lambda\right\}\right)\ge C'\lambda^{-1}$, 故极大定理中的估计本质上是尖锐的.

**23.** 哈代-利特尔伍德极大函数的一个有用变体是

$$
H^{*}f\left(x\right)=\sup\left\{\frac{1}{m\left(B\right)}\int_{B}\left|f\left(y\right)\right|\mathrm{d}y:B\text{是球},x\in B\right\}.
$$

证明 $Hf\le H^{*}f\le2^{n}Hf$.

**26.** 若 $\lambda$ 和 $\mu$ 是 $\mathbb R^{n}$ 上正且相互奇异的博雷尔测度, 且 $\lambda+\mu$ 正则, 则 $\lambda$ 和 $\mu$ 均正则.

### 解答 习题一

#### 22

记 $Hf$ 为哈代-利特尔伍德极大函数 (基础知识). 因 $f\ne0$ 且 $f\in L^{1}\left(\mathbb R^{n}\right)$, 存在球 $K$ (取某个紧集即可) 使

$$
\int_{K}\left|f\right|\mathrm{d}y>0;
$$

否则 $\left|\int_{K}f\right|$ 全为零将推出 $f=0$ 几乎处处, 矛盾. 记 $c=\int_{K}\left|f\right|\mathrm{d}y>0$, 并取 $R>0$ 使 $K\subset B\left(0,R\right)$ (即 $\sup_{y\in K}\left|y\right|<R$). 对 $\left|x\right|>R$, 因 $K\subset B\left(0,R\right)$ 且 $R<\left|x\right|$, 有 $K\subset B\left(x,2\left|x\right|\right)$. 于是由极大函数定义与**基础知识** (球体积公式),

$$
\begin{aligned}
&\quad\;Hf\left(x\right)\\&\ge\frac{1}{\left|B\left(x,2\left|x\right|\right)\right|}\int_{B\left(x,2\left|x\right|\right)}\left|f\right|\mathrm{d}y\\&\ge\frac{1}{\left|B\left(x,2\left|x\right|\right)\right|}\int_{K}\left|f\right|\mathrm{d}y\\&=\frac{c}{C_{n}\left(2\left|x\right|\right)^{n}}\\&=\frac{c}{2^{n}C_{n}}\left|x\right|^{-n}.
\end{aligned}
$$

取 $C=\frac{c}{2^{n}C_{n}}>0$, 即得 $Hf\left(x\right)\ge C\left|x\right|^{-n}$ 对 $\left|x\right|>R$ 成立.

第二问: 由第一问, 当 $0<\lambda<C/R^{n}$ 时, $\left(C/\lambda\right)^{1/n}>R$, 故

$$
\left\{x:\left|x\right|>\left(C/\lambda\right)^{1/n}\right\}\subset\left\{x:Hf\left(x\right)>\lambda\right\}.
$$

由球体积公式, 该集合的测度为

$$
\begin{aligned}
&\quad\;m\left(\left\{x:\left|x\right|<\left(C/\lambda\right)^{1/n}\right\}\right)\\&=C_{n}\left(\frac{C}{\lambda}\right)^{1/n\cdot n}\\&=\frac{C_{n}C}{\lambda}.
\end{aligned}
$$

令 $C'=C_{n}C$, 得 $m\left(\left\{x:Hf\left(x\right)>\lambda\right\}\right)\ge C'\lambda^{-1}$ 对充分小的 $\lambda>0$ 成立. $\blacksquare$

#### 23

先证 $Hf\le H^{*}f$. 对任意 $r>0$, 球 $B\left(x,r\right)$ 是含 $x$ 的球, 故

$$
\frac{1}{\left|B\left(x,r\right)\right|}\int_{B\left(x,r\right)}\left|f\right|\mathrm{d}y\le H^{*}f\left(x\right).
$$

对 $r>0$ 取上确界得 $Hf\left(x\right)\le H^{*}f\left(x\right)$.

再证 $H^{*}f\le2^{n}Hf$. 设 $B$ 是含 $x$ 的任意球, 记其半径为 $\rho$、中心为 $c$. 因 $x\in B$, 有 $\left|x-c\right|\le\rho$, 故对任意 $y\in B$,

$$
\left|y-x\right|\le\left|y-c\right|+\left|c-x\right|\le\rho+\rho=2\rho,
$$

即 $B\subset B\left(x,2\rho\right)$. 由球体积公式, $\left|B\left(x,2\rho\right)\right|=C_{n}\left(2\rho\right)^{n}=2^{n}C_{n}\rho^{n}=2^{n}\left|B\right|$. 于是

$$
\begin{aligned}
&\quad\;\frac{1}{m\left(B\right)}\int_{B}\left|f\right|\mathrm{d}y\\&\le\frac{1}{m\left(B\right)}\int_{B\left(x,2\rho\right)}\left|f\right|\mathrm{d}y\\&=\frac{m\left(B\left(x,2\rho\right)\right)}{m\left(B\right)}\cdot\frac{1}{m\left(B\left(x,2\rho\right)\right)}\int_{B\left(x,2\rho\right)}\left|f\right|\mathrm{d}y\\&=2^{n}\cdot\frac{1}{m\left(B\left(x,2\rho\right)\right)}\int_{B\left(x,2\rho\right)}\left|f\right|\mathrm{d}y\\&\le2^{n}Hf\left(x\right).
\end{aligned}
$$

对一切含 $x$ 的球 $B$ 取上确界, 得 $H^{*}f\left(x\right)\le2^{n}Hf\left(x\right)$. 合并即 $Hf\le H^{*}f\le2^{n}Hf$. $\blacksquare$

#### 26

设 $\nu=\lambda+\mu$. 因 $\lambda\perp\mu$ (**定义 11.4.1**), 存在博雷尔集 $A$ 使 $\mu\left(A\right)=0$ 且 $\lambda\left(A^{c}\right)=0$.

**正则性的条件 (1).** 对任意紧集 $K$, 由 $\lambda,\mu\ge0$ 及 $\nu$ 正则 (基础知识), $\lambda\left(K\right)\le\nu\left(K\right)<\infty$, 同理 $\mu\left(K\right)<\infty$.

**正则性的条件 (2) 对 $\lambda$.** 先注意对任意 $E\in\mathcal B\left(\mathbb R^{n}\right)$,

$$
\begin{aligned}
&\quad\;\lambda\left(E\right)\\&=\lambda\left(E\cap A\right)\\&=\nu\left(E\cap A\right),
\end{aligned}
$$

其中第二式用到 $\mu\left(E\cap A\right)\le\mu\left(A\right)=0$; 同理 $\mu\left(E\right)=\nu\left(E\cap A^{c}\right)$.

对任意开集 $U\supset E$, $U\cap A\supset E\cap A$, 故 $\lambda\left(U\right)=\nu\left(U\cap A\right)\ge\nu\left(E\cap A\right)=\lambda\left(E\right)$, 于是

$$
\inf\left\{\lambda\left(U\right):U\text{开},U\supset E\right\}\ge\lambda\left(E\right).
$$

反向: 给定 $\varepsilon>0$. 因 $\nu$ 正则, $\nu|_{A}$ (限制到 $A$ 上) 也满足正则性条件 (1)(2): 条件 (1) 显然; 对条件 (2), 取 $\nu|_{A}$ 的外正则性, 对 $E\cap A$ 存在开集 $W\supset E\cap A$ 使 $\nu\left(W\cap A\right)<\nu\left(E\cap A\right)+\varepsilon=\lambda\left(E\right)+\varepsilon$ (用 $\nu$ 的正则性先取开集 $W'\supset E\cap A$ 使 $\nu\left(W'\right)<\nu\left(E\cap A\right)+\varepsilon$, 再令 $W=W'$ 并注意 $\nu\left(W'\cap A\right)\le\nu\left(W'\right)$). 又因 $\left(E\cap A^{c}\right)\cap A=\varnothing$ 且 $\lambda\left(E\cap A^{c}\right)=0$, 可取足够薄的开邻域 $V\supset E\cap A^{c}$ 使 $\nu\left(V\cap A\right)<\varepsilon$ (例如取 $V=\left\{x:\mathrm{dist}\left(x,E\cap A^{c}\right)<\delta\right\}$ 并令 $\delta\to0$, 则 $V\cap A\downarrow\left(E\cap A^{c}\right)\cap A=\varnothing$, 由上连续性使 $\nu\left(V\cap A\right)\to0$). 令 $U=W\cup V$, 则 $U$ 开、$U\supset E$, 且

$$
\lambda\left(U\right)=\nu\left(U\cap A\right)\le\nu\left(W\cap A\right)+\nu\left(V\cap A\right)<\lambda\left(E\right)+2\varepsilon.
$$

故 $\inf\left\{\lambda\left(U\right):U\text{开},U\supset E\right\}\le\lambda\left(E\right)$. 合并得 $\lambda\left(E\right)=\inf\left\{\lambda\left(U\right):U\text{开},U\supset E\right\}$.

**正则性的条件 (2) 对 $\mu$.** 用 $\mu\left(E\right)=\nu\left(E\cap A^{c}\right)$ 及 $\nu|_{A^{c}}$ 的正则性, 论证完全对称, 得 $\mu$ 也满足条件 (2).

综上, $\lambda$ 与 $\mu$ 均正则. $\blacksquare$
