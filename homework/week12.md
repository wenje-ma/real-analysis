# 作业 12

> **定义 14.0.6** (有界变差函数)<br>设 $f:\left[a,b\right]\to\mathbb R$. 对 $\left[a,b\right]$ 的任意分划 $P:a=x_{0}<x_{1}<\cdots<x_{n}=b$, 定义变差 $V\left(f,P\right)=\sum_{i=1}^{n}\left|f\left(x_{i}\right)-f\left(x_{i-1}\right)\right|$. $f$ 在 $\left[a,b\right]$ 上的全变差为 $V_{a}^{b}\left(f\right)=\sup_{P}V\left(f,P\right)$. 若 $V_{a}^{b}\left(f\right)<+\infty$, 则称 $f$ 为有界变差函数, 记作 $f\in BV\left(\left[a,b\right]\right)$.

> **定义 15.0.11** (绝对连续性)<br>函数 $f:\left[a,b\right]\to\mathbb R$ 称为**绝对连续的** (记 $f\in AC\left(\left[a,b\right]\right)$), 若对任意 $\varepsilon>0$, 存在 $\delta>0$, 使得对任意有限个互不相交的子区间 $\left(a_{i},b_{i}\right)\subset\left[a,b\right]$, 只要 $\sum_{i}\left(b_{i}-a_{i}\right)<\delta$, 就有 $\sum_{i}\left|f\left(b_{i}\right)-f\left(a_{i}\right)\right|<\varepsilon$.

> **定理 15.0.14** (等价刻画)<br>$f\in AC\left(\left[a,b\right]\right)$ 当且仅当存在 $g\in L^{1}\left(\left[a,b\right]\right)$ 使得 $f\left(x\right)=f\left(a\right)+\int_{a}^{x}g\left(t\right)\mathrm{d}t$ 对一切 $x\in\left[a,b\right]$ 成立. 此时 $f'\left(x\right)=g\left(x\right)$ 几乎处处成立.

> **定理 15.0.16**<br>有以下严格包含关系: $C^{1}\left(\left[a,b\right]\right)\subset$ 利普希茨 $\subset AC\left(\left[a,b\right]\right)\subset BV\left(\left[a,b\right]\right)\subset$ 有界函数.

> **推论 13.4.5**<br>设 $F$ 是 $\mathbb R$ 上的右连续的增函数, 则对几乎所有的 $x$, $F'\left(x\right)$ 存在.

> **性质 11.5.6** (线性性)<br>若 $\nu_{1},\nu_{2}\ll\mu$ 且 $a,b\in\mathbb R$, 则 $\frac{\mathrm{d}\left(a\nu_{1}+b\nu_{2}\right)}{\mathrm{d}\mu}=a\frac{\mathrm{d}\nu_{1}}{\mathrm{d}\mu}+b\frac{\mathrm{d}\nu_{2}}{\mathrm{d}\mu}$ $\mu$-几乎处处成立.

> **基础知识** (归一化的有界变差 $NBV$ 与 斯蒂尔杰斯测度)<br>$NBV=\left\{F\in BV:F\ \text{右连续},\ F\left(-\infty\right)=0\right\}$. 对递增右连续的 $F$, 由 $\mu_{F}\left(\left(a,b\right]\right)=F\left(b\right)-F\left(a\right)$ 唯一确定一个正则博雷尔测度 $\mu_{F}$.

> **基础知识** (绝对连续函数的全变差)<br>若 $F$ 在 $\left[a,b\right]$ 上绝对连续, 则 $F$ 的全变差 $V_{a}^{b}\left(F\right)=\int_{a}^{b}\left|F'\left(t\right)\right|\mathrm{d}t$.

### 习题一

**38.** 设 $f:\left[a,b\right]\to\mathbb R$, 把 $f$ 的图像看作 $\mathbb C$ 的子集 $\left\{t+if\left(t\right):t\in\left[a,b\right]\right\}$. 该图像的长度 $L$ 定义为所有内接多边形长度之和的上确界. (内接多边形是连接 $t_{j-1}+if\left(t_{j-1}\right)$ 与 $t_{j}+if\left(t_{j}\right)$ 的线段之并, $1\le j\le n$, 其中 $a=t_{0}<\cdots<t_{n}=b$.)
a. 令 $F\left(t\right)=t+if\left(t\right)$, 则 $L$ 是 $F$ 在 $\left[a,b\right]$ 上的全变差;
b. 若 $f$ 绝对连续, 则 $L=\int_{a}^{b}\left[1+\left(f'\left(t\right)\right)^{2}\right]^{1/2}\mathrm{d}t$.

**39.** 若 $\left\{F_{j}\right\}$ 是 $\left[a,b\right]$ 上的一列非负递增函数, 且 $F:=\sum_{j}F_{j}$ 满足 $F\left(x\right)<\infty$ 对所有 $x\in\left[a,b\right]$ 成立, 则 $F'\left(x\right)=\sum_{j}F_{j}'\left(x\right)$ 对几乎所有 $x\in\left[a,b\right]$ 成立. (可设 $F_{j}\in NBV$, 考虑测度 $\mu_{F_{j}}$.)

**42.** 函数 $F:\left(a,b\right)\to\mathbb R$ ($-\infty\le a<b\le\infty$) 称为**凸的**, 若 $F\left(\lambda s+\left(1-\lambda\right)t\right)\le\lambda F\left(s\right)+\left(1-\lambda\right)F\left(t\right)$ 对所有 $s,t\in\left(a,b\right)$ 和 $\lambda\in\left(0,1\right)$ 成立.
a. $F$ 凸当且仅当对所有 $s,t,s',t'\in\left(a,b\right)$ 满足 $s\le s'<t'$, $s<t\le t'$: $\frac{F\left(t\right)-F\left(s\right)}{t-s}\le\frac{F\left(t'\right)-F\left(s'\right)}{t'-s'}$;
b. $F$ 凸当且仅当 $F$ 在 $\left(a,b\right)$ 的每个紧子区间上绝对连续且 $F'$ 递增 (在其定义处);
c. 若 $F$ 凸且 $t_{0}\in\left(a,b\right)$, 则存在 $\beta\in\mathbb R$ 使 $F\left(t\right)-F\left(t_{0}\right)\ge\beta\left(t-t_{0}\right)$ 对所有 $t\in\left(a,b\right)$ 成立;
d. (延森不等式) 若 $\left(X,\mathcal M,\mu\right)$ 是测度空间且 $\mu\left(X\right)=1$, $g:X\to\left(a,b\right)\in L^{1}\left(\mu\right)$, $F$ 在 $\left(a,b\right)$ 上凸, 则 $F\left(\int g\,\mathrm{d}\mu\right)\le\int F\circ g\,\mathrm{d}\mu$.

### 解答 习题一

#### 38

**(a)** 令 $F\left(t\right)=t+if\left(t\right)$. 对 $\left[a,b\right]$ 的一个分划 $a=t_{0}<\cdots<t_{n}=b$, 相邻顶点 $t_{j-1}+if\left(t_{j-1}\right)$ 与 $t_{j}+if\left(t_{j}\right)$ 的距离为

$$
\left|F\left(t_{j}\right)-F\left(t_{j-1}\right)\right|=\sqrt{\left(t_{j}-t_{j-1}\right)^{2}+\left(f\left(t_{j}\right)-f\left(t_{j-1}\right)\right)^{2}},
$$

故内接多边形的长度恰为 $\sum_{j=1}^{n}\left|F\left(t_{j}\right)-F\left(t_{j-1}\right)\right|$. 于是 $L$ 等于该和式关于一切分划的上确界, 这正是 $F$ 在 $\left[a,b\right]$ 上的全变差 $V_{a}^{b}\left(F\right)$ (**定义 14.0.6**). $\blacksquare$

**(b)** 若 $f\in AC\left(\left[a,b\right]\right)$ (**定义 15.0.11**), 则 $F\left(t\right)=t+if\left(t\right)$ 的两个分量 $t$ (恒等函数) 与 $f$ 均绝对连续, 故 $F$ 绝对连续. 由**定理 15.0.14**, 对几乎所有 $t$,

$$
\begin{aligned}F'\left(t\right)&=\frac{\mathrm{d}}{\mathrm{d}t}\left(t+if\left(t\right)\right)\\&=1+if'\left(t\right),
\end{aligned}
$$

从而 $\left|F'\left(t\right)\right|=\left(1+\left(f'\left(t\right)\right)^{2}\right)^{1/2}$. 由**基础知识** (绝对连续函数的全变差),

$$
\begin{aligned}L&=V_{a}^{b}\left(F\right)\\&=\int_{a}^{b}\left|F'\left(t\right)\right|\mathrm{d}t\\&=\int_{a}^{b}\left[1+\left(f'\left(t\right)\right)^{2}\right]^{1/2}\mathrm{d}t.
\end{aligned}
$$

$\blacksquare$

#### 39

设 $\mu_{F_{j}}$ 是 $F_{j}$ 对应的 斯蒂尔杰斯测度, $\mu_{F}$ 是 $F=\sum_{j}F_{j}$ 对应的 斯蒂尔杰斯测度 (**基础知识**). 因 $\sum_{j}F_{j}$ 收敛且各项非负, 由 斯蒂尔杰斯测度的可数可加性, $\mu_{F}=\sum_{j}\mu_{F_{j}}$. 由**推论 13.4.5** 与**定理 13.4.4** (应用于正则测度 $\mu_{F_{j}}$; 单调函数的导数即其 斯蒂尔杰斯测度的拉东-尼科迪姆导数), 对 $m$-几乎每个 $x$, $F_{j}'\left(x\right)=\frac{\mathrm{d}\mu_{F_{j}}}{\mathrm{d}m}\left(x\right)$; 同理 $F'\left(x\right)=\frac{\mathrm{d}\mu_{F}}{\mathrm{d}m}\left(x\right)$. 于是由**性质 11.5.6** (线性性, 逐次两两相加),

$$
\begin{aligned}\frac{\mathrm{d}\mu_{F}}{\mathrm{d}m}\left(x\right)&=\frac{\mathrm{d}\left(\sum_{j}\mu_{F_{j}}\right)}{\mathrm{d}m}\left(x\right)\\&=\sum_{j}\frac{\mathrm{d}\mu_{F_{j}}}{\mathrm{d}m}\left(x\right)\\&=\sum_{j}F_{j}'\left(x\right),
\end{aligned}
$$

对 $m$-几乎每个 $x$ 成立. 故 $F'\left(x\right)=\sum_{j}F_{j}'\left(x\right)$ 几乎处处. $\blacksquare$

#### 42

记差商 $S\left(u,v\right)=\frac{F\left(v\right)-F\left(u\right)}{v-u}$ ($u<v$).

**(a)** 先证 $\Rightarrow$. 设 $F$ 凸. 先建立两条差商单调性: 固定左端点 $s$, 对 $s<x_{1}<x_{2}$, 由凸性

$$
F\left(x_{1}\right)\le\frac{x_{2}-x_{1}}{x_{2}-s}F\left(s\right)+\frac{x_{1}-s}{x_{2}-s}F\left(x_{2}\right),
$$

整理得 $S\left(s,x_{1}\right)\le S\left(s,x_{2}\right)$, 即差商关于右端点递增; 同理固定右端点 $t$, 对 $s_{1}<s_{2}<t$, 由凸性

$$
F\left(s_{2}\right)\le\frac{t-s_{2}}{t-s_{1}}F\left(s_{1}\right)+\frac{s_{2}-s_{1}}{t-s_{1}}F\left(t\right),
$$

整理得 $S\left(s_{2},t\right)\le S\left(s_{1},t\right)$, 即差商关于左端点递减.

现在给定 $s\le s'<t'$ 且 $s<t\le t'$. 由差商关于右端点递增, $S\left(s,t\right)\le S\left(s,t'\right)$ (当 $t=t'$ 时取等); 由差商关于左端点递减, $S\left(s,t'\right)\ge S\left(s',t'\right)$ (当 $s=s'$ 时取等). 故

$$
S\left(s,t\right)\le S\left(s,t'\right)\le S\left(s',t'\right),
$$

即 $\frac{F\left(t\right)-F\left(s\right)}{t-s}\le\frac{F\left(t'\right)-F\left(s'\right)}{t'-s'}$.

再证 $\Leftarrow$. 任取 $s<t$, $\lambda\in\left(0,1\right)$, 令 $u=\lambda s+\left(1-\lambda\right)t$, 则 $s<u<t$. 在题设不等式 (a) 中取 $s'=u$, $t'=t$, 满足 $s\le s'<t'$ 且 $s<t\le t'$, 得

$$
\frac{F\left(u\right)-F\left(s\right)}{u-s}\le\frac{F\left(t\right)-F\left(u\right)}{t-u}.
$$

由 $u=\lambda s+\left(1-\lambda\right)t$, 有 $u-s=\lambda\left(t-s\right)$, $t-u=\left(1-\lambda\right)\left(t-s\right)$. 代入整理得 $F\left(u\right)\le\lambda F\left(s\right)+\left(1-\lambda\right)F\left(t\right)$, 即 $F$ 凸. 合并即得 (a). $\blacksquare$

**(b)** 先证 $\Rightarrow$. 设 $F$ 凸, 取紧子区间 $\left[\alpha,\beta\right]\subset\left(a,b\right)$. 由 (a) 的差商单调性, 对 $\alpha\le x<y\le\beta$, $S\left(\alpha,x\right)\le S\left(x,y\right)\le S\left(y,\beta\right)$ (三点斜率递增), 而 $S\left(\alpha,x\right)\ge S\left(\alpha,\beta\right)$ (差商关于右端点递增) 且 $S\left(y,\beta\right)\le S\left(\alpha,\beta\right)$ (差商关于左端点递减), 故 $\left|S\left(x,y\right)\right|\le S\left(\alpha,\beta\right)<\infty$. 于是 $F$ 在 $\left[\alpha,\beta\right]$ 上满足利普希茨条件 (利普希茨常数为 $S\left(\alpha,\beta\right)$), 由**定理 15.0.16**, $F\in AC\left(\left[\alpha,\beta\right]\right)$. 又 $F'$ 处处存在 (凸函数) 且为差商的极限, 由 (a) 差商关于左端点单调, 得 $F'$ 递增.

再证 $\Leftarrow$. 设 $F$ 在 $\left(a,b\right)$ 的每个紧子区间上绝对连续且 $F'$ 递增. 由**定理 15.0.14**, 对任意 $s<t\in\left(a,b\right)$ 与中间点 $u$, 有 $F\left(u\right)-F\left(s\right)=\int_{s}^{u}F'$, $F\left(t\right)-F\left(u\right)=\int_{u}^{t}F'$. 因 $F'$ 在 $\left(s,u\right)$ 上的值不超过其在 $\left(u,t\right)$ 上的值, 平均化得

$$
\frac{1}{u-s}\int_{s}^{u}F'\le\frac{1}{t-u}\int_{u}^{t}F',
$$

即 $S\left(s,u\right)\le S\left(u,t\right)$. 取 $u=\lambda s+\left(1-\lambda\right)t$ 并整理 (同 (a) 的 $\Leftarrow$), 得 $F\left(u\right)\le\lambda F\left(s\right)+\left(1-\lambda\right)F\left(t\right)$, 即 $F$ 凸. 合并即得 (b). $\blacksquare$

**(c)** 由 (a) 的差商单调性, $F$ 在 $t_{0}$ 处的左、右导数存在: 左导数 $F'_{-}\left(t_{0}\right)=\sup_{t<t_{0}}S\left(t,t_{0}\right)$, 右导数 $F'_{+}\left(t_{0}\right)=\inf_{t>t_{0}}S\left(t_{0},t\right)$, 且 $F'_{-}\left(t_{0}\right)\le F'_{+}\left(t_{0}\right)$ (对 $t_{1}<t_{0}<t_{2}$, 三点斜率 $S\left(t_{1},t_{0}\right)\le S\left(t_{0},t_{2}\right)$). 取 $\beta\in\left[F'_{-}\left(t_{0}\right),F'_{+}\left(t_{0}\right)\right]$. 当 $t>t_{0}$ 时, $S\left(t_{0},t\right)\ge F'_{+}\left(t_{0}\right)\ge\beta$, 故 $F\left(t\right)-F\left(t_{0}\right)\ge\beta\left(t-t_{0}\right)$; 当 $t<t_{0}$ 时, $S\left(t,t_{0}\right)\le F'_{-}\left(t_{0}\right)\le\beta$, 因 $t-t_{0}<0$ 两边乘以负数翻转, 得 $F\left(t\right)-F\left(t_{0}\right)\ge\beta\left(t-t_{0}\right)$. 对 $t=t_{0}$ 取等号成立. $\blacksquare$

**(d)** 记 $t_{0}=\int g\,\mathrm{d}\mu$. 因 $g$ 取值于 $\left(a,b\right)$, 且 $g\in L^{1}\left(\mu\right)$, 有 $t_{0}\in\left(a,b\right)$. 由 (c), 存在 $\beta\in\mathbb R$ 使 $F\left(t\right)-F\left(t_{0}\right)\ge\beta\left(t-t_{0}\right)$ 对所有 $t\in\left(a,b\right)$ 成立. 代入 $t=g\left(x\right)$ 得 $F\left(g\left(x\right)\right)\ge F\left(t_{0}\right)+\beta\left(g\left(x\right)-t_{0}\right)$ 对一切 $x\in X$. 对 $\mu$ 积分 (右端 $\in L^{1}$, 故积分良定义):

$$
\begin{aligned}\int F\circ g\,\mathrm{d}\mu\\&\ge\int\left[F\left(t_{0}\right)+\beta\left(g-t_{0}\right)\right]\mathrm{d}\mu&=F\left(t_{0}\right)+\beta\left(\int g\,\mathrm{d}\mu-t_{0}\right)\\&=F\left(t_{0}\right)\\&=F\left(\int g\,\mathrm{d}\mu\right).
\end{aligned}
$$

故 $F\left(\int g\,\mathrm{d}\mu\right)\le\int F\circ g\,\mathrm{d}\mu$. $\blacksquare$
