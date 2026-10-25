# Assignment 8

> **Theorem 8.2.9** (Dominated Convergence Theorem)<br>Let $\left(X,\mathcal F,\mu\right)$ be a measure space and $\left\{f_{n}\right\}$ a sequence of measurable functions. If there exists an integrable function $g$ such that $\left|f_{n}\right|\le g$ for all $n$, and $f_{n}\to f$ almost everywhere, then $f$ is integrable and $\int f\,\mathrm{d}\mu=\lim_{n\to\infty}\int f_{n}\,\mathrm{d}\mu$.

> **Theorem 8.2.16**<br>If $f\in L^{1}\left(\mu\right)$ and $\varepsilon> 0$, then there exists an integrable simple function $\varphi=\sum a_{j}\chi_{E_{j}}$ such that $\int\left|f-\varphi\right|\mathrm{d}\mu< \varepsilon$ (i.e. integrable simple functions are dense in the $L^{1}$ metric).

> **Theorem 10.2.1** (Fubini's Theorem)<br>Let $\left(X,\mathcal A,\mu\right)$ and $\left(Y,\mathcal B,\nu\right)$ be $\sigma$-finite measure spaces, and let $f:X\times Y\to\mathbb R$ be an $\mathcal A\otimes\mathcal B$-measurable function. If $f$ is integrable on $X\times Y$, then for almost every $x$, $y\mapsto f\left(x,y\right)$ is $\nu$-integrable; for almost every $y$, $x\mapsto f\left(x,y\right)$ is $\mu$-integrable; and the iterated integrals are equal: $$\begin{aligned}\int_{X\times Y}f\,\mathrm{d}\left(\mu\times\nu\right)&=\int_{X}\left(\int_{Y}f\left(x,y\right)\mathrm{d}\nu\left(y\right)\right)\mathrm{d}\mu\left(x\right)\\&=\int_{Y}\left(\int_{X}f\left(x,y\right)\mathrm{d}\mu\left(x\right)\right)\mathrm{d}\nu\left(y\right).\end{aligned}$$

> **Theorem 10.2.2** (Tonelli's Theorem)<br>If $f:X\times Y\to\left[0,\infty\right]$ is $\mathcal A\otimes\mathcal B$-measurable, then $$\begin{aligned}\int_{X\times Y}f\,\mathrm{d}\left(\mu\times\nu\right)&=\int_{X}\left(\int_{Y}f\left(x,y\right)\mathrm{d}\nu\left(y\right)\right)\mathrm{d}\mu\left(x\right)\\&=\int_{Y}\left(\int_{X}f\left(x,y\right)\mathrm{d}\mu\left(x\right)\right)\mathrm{d}\nu\left(y\right).\end{aligned}$$<br>where all integral values lie in $\left[0,\infty\right]$.

> **Theorem 11.1.1**<br>Suppose $E\in\mathcal L^{n}$.
> (a) $$\begin{aligned}m\left(E\right)&=\inf\left\{m\left(U\right):U\supset E,U\text{开}\right\}\\&=\sup\left\{m\left(K\right):K\subset E,K\text{紧}\right\}\end{aligned}$$;
> 
> (b) If $m\left(E\right)< \infty$, then for any $\varepsilon> 0$ there exists a finite family of pairwise disjoint rectangles $\left\{R_{j}\right\}_{j=1}^{N}$ whose sides are intervals, such that $m\left(E\triangle\bigcup_{j=1}^{N}R_{j}\right)< \varepsilon$.

> **Theorem 11.4.1**<br>There exists a unique Borel measure $\sigma=\sigma_{n-1}$ on $S^{n-1}$ such that $m^{*}=\rho\times\sigma$. If $f$ is a Borel measurable function on $\mathbb R^{n}$ and either $f\ge0$ or $f\in L^{1}\left(m\right)$, then $$\int_{\mathbb R^{n}}f\left(x\right)\mathrm{d}x=\int_{0}^{\infty}\int_{S^{n-1}}f\left(rx'\right)r^{n-1}\mathrm{d}\sigma\left(x'\right)\mathrm{d}r.$$

> **Basic Knowledge**<br>**Invariance under 1-dimensional translation and scaling**: for $c\in\mathbb R$ and $\lambda\ne0$, the Lebesgue measure satisfies $m\left(E+c\right)=m\left(E\right)$ and $m\left(\lambda E\right)=\left|\lambda\right|m\left(E\right)$.

> **Basic Knowledge**<br>**Invertible linear transformations preserve measurability and null sets**: if $T\in GL\left(n,\mathbb R\right)$, then $T\left(E\right)\in\mathcal L^{n}$ if and only if $E\in\mathcal L^{n}$, and $T$ preserves null sets.

> **Basic Knowledge**<br>**Orthogonal transformations preserve the Lebesgue measure**: if $R\in O\left(n\right)$, i.e. $R^{T}R=I$, then $\left|\det R\right|=1$, and for any $E\in\mathcal L^{n}$, $m\left(R\left(E\right)\right)=m\left(E\right)$.

> **Basic Knowledge**<br>**The Gamma function and the beta identity**: the Gamma function $\Gamma\left(x\right)=\int_{0}^{\infty}t^{x-1}e^{-t}\mathrm{d}t$ satisfies the recurrence $\Gamma\left(x+1\right)=x\Gamma\left(x\right)$; the Beta function satisfies the identity $\frac{\Gamma\left(x\right)\Gamma\left(y\right)}{\Gamma\left(x+y\right)}=\int_{0}^{1}t^{x-1}\left(1-t\right)^{y-1}\mathrm{d}t$ for $x,y> 0$.

> **Basic Knowledge**<br>**Continuous approximation of indicator functions**: if $R\subset\mathbb R^{n}$ is a bounded closed rectangle, then for any $\varepsilon> 0$ there exists a continuous function $g$ with compact support such that $\int\left|\chi_{R}-g\right|\mathrm{d}m< \varepsilon$.

> **Basic Knowledge**<br>**Uniqueness of a measure on a generating family of the product $\sigma$-algebra**: two $\sigma$-finite measures that agree on a rectangle-admissible family generating the product $\sigma$-algebra agree on the whole product $\sigma$-algebra.

### Problem 1

Prove Theorem 11.1.2 of the lecture notes: if $f\in L^{1}\left(m\right)$ and $\varepsilon> 0$, then there exists a simple function $\varphi=\sum a_{j}\chi_{R_{j}}$, where each $R_{j}$ is a product of intervals, such that $\int\left|f-\varphi\right|< \varepsilon$; and there exists a continuous function $g$ that vanishes outside a bounded set, such that $\int\left|f-g\right|< \varepsilon$.

### Solution to Problem 1

**The simple-function part.** By **Theorem 8.2.16**, there exists an integrable simple function $\varphi=\sum_{j}a_{j}\chi_{E_{j}}$ such that $\int\left|f-\varphi\right|< \varepsilon/2$. For terms with $a_{j}\ne0$, since $\int a_{j}\chi_{E_{j}}\,\mathrm{d}m=a_{j}m\left(E_{j}\right)< \infty$, we have $m\left(E_{j}\right)< \infty$ (otherwise the integral diverges, contradicting integrability). By **Theorem 11.1.1** (b), for each such $E_{j}$ there exist finitely many pairwise disjoint rectangles with sides that are intervals, $\left\{R_{j,k}\right\}$, such that $m\left(E_{j}\triangle\bigcup_{k}R_{j,k}\right)$ is arbitrarily small. Then $\chi_{E_{j}}$ and $\chi_{R_{j}}$ (where $R_{j}=\bigcup_{k}R_{j,k}$) are arbitrarily close in $L^{1}$; taking the approximation errors small enough and combining over all $j$, we obtain a simple function $\varphi'=\sum_{j}a_{j}\chi_{R_{j}}$ (each $R_{j}$ is a finite union of rectangles with sides that are intervals, and the $R_{j}$ may be arranged as pairwise disjoint products of intervals) satisfying $\int\left|\varphi-\varphi'\right|< \varepsilon/2$. Hence $\int\left|f-\varphi'\right|\le\int\left|f-\varphi\right|+\int\left|\varphi-\varphi'\right|< \varepsilon$. $\blacksquare$

**The continuous-function part.** Suppose $\varphi'=\sum_{j}a_{j}\chi_{R_{j}}$ has been obtained as above, where each $R_{j}$ is a bounded closed rectangle. By the Basic Knowledge (continuous approximation of indicator functions), for each $R_{j}$ there exists a continuous function $g_{j}$ with compact support such that $\int\left|\chi_{R_{j}}-g_{j}\right|\mathrm{d}m$ is arbitrarily small. Taking the approximation errors small enough and setting $g=\sum_{j}a_{j}g_{j}$, then $g$ is continuous and supported in $\bigcup_{j}R_{j}$ (a bounded set), and $\int\left|\varphi'-g\right|\le\sum_{j}\left|a_{j}\right|\int\left|\chi_{R_{j}}-g_{j}\right|< \varepsilon/2$. Hence

$$
\int\left|f-g\right|\le\int\left|f-\varphi'\right|+\int\left|\varphi'-g\right|< \varepsilon.
$$

$g$ vanishes outside a bounded set. $\blacksquare$

### Problem 2

Prove Theorem 11.3.1 of the lecture notes (the linear change-of-variables formula). Assume $T\in GL\left(n,\mathbb R\right)$.

(a) If $f$ is a Lebesgue measurable function on $\mathbb R^{n}$, then so is $f\circ T$. If $f\ge0$ or $f\in L^{1}\left(m\right)$, then

$$
\int f\left(x\right)\mathrm{d}x=\left|\det T\right|\int f\circ T\left(x\right)\mathrm{d}x.
$$

(b) If $E\in\mathcal L^{n}$, then $T\left(E\right)\in\mathcal L^{n}$ and $m\left(T\left(E\right)\right)=\left|\det T\right|m\left(E\right)$.

### Solution to Problem 2

We first prove the three elementary-transformation cases, then combine them.

**Scaling** $T_{1}\left(x_{1},\dots,x_{j},\dots,x_{n}\right)=\left(x_{1},\dots,cx_{j},\dots,x_{n}\right)$ ($c\ne0$). By the Basic Knowledge (1-dimensional scaling invariance) and the product structure, scaling one coordinate at a time while keeping the others fixed gives $m\left(T_{1}\left(E\right)\right)=\left|c\right|m\left(E\right)$ and $\int f\circ T_{1}\left(x\right)\mathrm{d}x=\frac{1}{\left|c\right|}\int f\left(x\right)\mathrm{d}x$, i.e. $\int f\left(x\right)\mathrm{d}x=\left|c\right|\int f\circ T_{1}\left(x\right)\mathrm{d}x=\left|\det T_{1}\right|\int f\circ T_{1}\left(x\right)\mathrm{d}x$.

**Shear** $T_{2}\left(x_{1},\dots,x_{j},\dots,x_{n}\right)=\left(x_{1},\dots,x_{j}+cx_{k},\dots,x_{n}\right)$ ($k\ne j$). By the Basic Knowledge (1-dimensional translation invariance) applied slice by slice, $m\left(T_{2}\left(E\right)\right)=m\left(E\right)$ and $\int f\circ T_{2}\left(x\right)\mathrm{d}x=\int f\left(x\right)\mathrm{d}x$. Since $\det T_{2}=1$, the formula holds.

**Swap** $T_{3}$ swaps two coordinates, $\det T_{3}=-1$. By the symmetry of $m$ as a product measure, $m\left(T_{3}\left(E\right)\right)=m\left(E\right)$ and $\int f\circ T_{3}\left(x\right)\mathrm{d}x=\int f\left(x\right)\mathrm{d}x$, while $\left|\det T_{3}\right|=1$, so the formula holds.

**The general case.** By elementary linear algebra, every $T\in GL\left(n,\mathbb R\right)$ can be written as a product $T=T_{1}\circ\cdots\circ T_{k}$ of finitely many of the three elementary transformations above (an invertible matrix can be reduced to the identity by row operations). The formula holds for each elementary transformation, and determinants multiply, $\left|\det T\right|=\prod_{i}\left|\det T_{i}\right|$. Substituting successively gives

$$
\begin{aligned}\int f\left(x\right)\mathrm{d}x&=\left|\det T_{1}\right|\int f\circ T_{1}\left(x\right)\mathrm{d}x\\&=\cdots\\&=\left|\det T\right|\int f\circ T\left(x\right)\mathrm{d}x,
\end{aligned}
$$

which is (a). Measurability: $T$ is continuous, and by the Basic Knowledge (invertible linear transformations preserve measurability and null sets), $f\circ T$ is measurable and $T\left(E\right)\in\mathcal L^{n}$.

**Proof of (b).** Take $f=\chi_{T\left(E\right)}$ in (a); then

$$
\begin{aligned}m\left(T\left(E\right)\right)&=\int\chi_{T\left(E\right)}\left(x\right)\mathrm{d}x\\&=\left|\det T\right|\int\chi_{T\left(E\right)}\circ T\left(x\right)\mathrm{d}x\\&=\left|\det T\right|\int\chi_{E}\left(x\right)\mathrm{d}x\\&=\left|\det T\right|m\left(E\right).
\end{aligned}
$$

$T\left(E\right)\in\mathcal L^{n}$ has already been ensured by measurability. $\blacksquare$

### Problem 3

Prove Problem 55. Let $E=\left[0,1\right]\times\left[0,1\right]$. Study the existence and equality of $\int_{E}f\,\mathrm{d}m^{2}$, $\int_{0}^{1}\int_{0}^{1}f\left(x,y\right)\mathrm{d}x\,\mathrm{d}y$ and $\int_{0}^{1}\int_{0}^{1}f\left(x,y\right)\mathrm{d}y\,\mathrm{d}x$ for the following $f$.

a. $f\left(x,y\right)=\left(x^{2}-y^{2}\right)\left(x^{2}+y^{2}\right)^{-2}$;

b. $f\left(x,y\right)=\left(1-xy\right)^{-a}$ ($a> 0$);

c. $f\left(x,y\right)=\left(x-y\right)^{-3}$ if $0< y< x< 1$, and $0$ otherwise.

### Solution to Problem 3

#### a

**$\int_{E}f\,\mathrm{d}m^{2}$ does not exist.** $\left|f\left(x,y\right)\right|=\frac{\left|x^{2}-y^{2}\right|}{\left(x^{2}+y^{2}\right)^{2}}\le\frac{x^{2}+y^{2}}{\left(x^{2}+y^{2}\right)^{2}}=\frac{1}{x^{2}+y^{2}}$. On $E$, $\int_{E}\frac{1}{x^{2}+y^{2}}\mathrm{d}x\,\mathrm{d}y$ diverges (in polar coordinates, $\int_{0}^{\delta}\int_{0}^{\pi/2}\frac{1}{r^{2}}r\,\mathrm{d}\theta\,\mathrm{d}r=\frac{\pi}{2}\int_{0}^{\delta}\frac{1}{r}\mathrm{d}r=\infty$), so $\int_{E}\left|f\right|=\infty$, $f\notin L^{1}$, and $\int_{E}f\,\mathrm{d}m^{2}$ is undefined.

**$\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y$ (integrate first in $x$).** Fix $y$ and set $x=yt$; then

$$
\int_{0}^{1}\frac{x^{2}-y^{2}}{\left(x^{2}+y^{2}\right)^{2}}\mathrm{d}x=\frac{1}{y}\int_{0}^{1/y}\frac{t^{2}-1}{\left(t^{2}+1\right)^{2}}\mathrm{d}t.
$$

Since $\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{t}{t^{2}+1}\right)=\frac{1-t^{2}}{\left(t^{2}+1\right)^{2}}$, we have $\int\frac{t^{2}-1}{\left(t^{2}+1\right)^{2}}\mathrm{d}t=-\frac{t}{t^{2}+1}+C$, so the inner integral

$$
\begin{aligned}=\frac{1}{y}\left[-\frac{t}{t^{2}+1}\right]_{0}^{1/y}&=-\frac{1}{y}\cdot\frac{1/y}{1+1/y^{2}}\\&=-\frac{1}{y^{2}+1}.
\end{aligned}
$$

Hence

$$\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y=\int_{0}^{1}-\frac{1}{1+y^{2}}\mathrm{d}y=-\left[\arctan y\right]_{0}^{1}=-\frac{\pi}{4}.$$

**$\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x$ (integrate first in $y$).** Symmetrically, fix $x$ and set $y=xt$; the inner integral $\int_{0}^{1}f\,\mathrm{d}y=\frac{1}{x^{2}+1}$, so

$$
\begin{aligned}\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x&=\int_{0}^{1}\frac{1}{1+x^{2}}\mathrm{d}x\\&=\left[\arctan x\right]_{0}^{1}\\&=\frac{\pi}{4}.
\end{aligned}
$$

**Conclusion.** $\int_{E}f\,\mathrm{d}m^{2}$ does not exist ($f$ is not absolutely integrable); $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y=-\frac{\pi}{4}$ and $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x=\frac{\pi}{4}$ exist but are not equal and have opposite signs. Since $f\notin L^{1}$, Theorem 10.2.1 (Fubini) does not apply, and the two iterated integrals cannot be interchanged. $\blacksquare$

#### b

$f\ge0$.

**$f$ is integrable when $0< a\le1$.** Fix $y$; the inner integral $\int_{0}^{1}\left(1-xy\right)^{-a}\mathrm{d}x=\frac{1}{y}\cdot\frac{1-\left(1-y\right)^{1-a}}{1-a}$ (when $a\ne1$), and when $a=1$ the inner integral $=-\frac{\ln\left(1-y\right)}{y}$. For $0< a< 1$, the inner integral tends to $1$ as $y\to0$ and to $\frac{1}{1-a}$ as $y\to1$ (since $\left(1-y\right)^{1-a}\to0$), hence it is bounded, and $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y< \infty$. For $a=1$, $\int_{0}^{1}-\frac{\ln\left(1-y\right)}{y}\mathrm{d}y=\sum_{k=1}^{\infty}\frac{1}{k^{2}}=\frac{\pi^{2}}{6}< \infty$. Hence when $0< a\le1$, $f\in L^{1}$, and by **Theorem 10.2.2** (Tonelli), the three integrals all exist and are equal.

**$f\notin L^{1}$ when $a> 1$.** The inner integral is $\frac{1}{y}\cdot\frac{1-\left(1-y\right)^{1-a}}{1-a}$; since $1-a< 0$ and $\left(1-y\right)^{1-a}\to\infty$ as $y\to1$, the inner integral tends to $+\infty$, so $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y=+\infty$; symmetrically $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x=+\infty$, and $\int_{E}f\,\mathrm{d}m^{2}=+\infty$.

**Conclusion.** When $0< a\le1$, the three integrals exist and are equal, and $f\in L^{1}$; when $a> 1$, all three integrals are $+\infty$ (the integral of a nonnegative function diverges), and $f\notin L^{1}$. $\blacksquare$

#### c

The region is $\left\{\left(x,y\right):0< y< x< 1\right\}$.

**$\int_{E}f\,\mathrm{d}m^{2}$ does not exist.** $\left|f\right|=\left(x-y\right)^{-3}$. Integrating first in $x$, $\int_{y}^{1}\left(x-y\right)^{-3}\mathrm{d}x=\left[-\frac{1}{2}\left(x-y\right)^{-2}\right]_{y}^{1}=+\infty$, so $\int_{E}\left|f\right|=\infty$, $f\notin L^{1}$, and $\int_{E}f\,\mathrm{d}m^{2}$ is undefined.

**$\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y$ (integrate first in $x$).** Fix $y$; $\int_{y}^{1}\left(x-y\right)^{-3}\mathrm{d}x=\left[-\frac{1}{2}\left(x-y\right)^{-2}\right]_{y}^{1}$, and since $\lim_{x\to y^{+}}\left(x-y\right)^{-2}=\infty$, the inner integral $=+\infty$, so

$$
\begin{aligned}\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y&=\int_{0}^{1}\left(\int_{y}^{1}\left(x-y\right)^{-3}\mathrm{d}x\right)\mathrm{d}y\\&=+\infty.
\end{aligned}
$$

**$\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x$ (integrate first in $y$).** Fix $x$; $\int_{0}^{x}\left(x-y\right)^{-3}\mathrm{d}y=\left[-\frac{1}{2}\left(x-y\right)^{-2}\right]_{0}^{x}$, and since $\lim_{y\to x^{-}}\left(x-y\right)^{-2}=\infty$, the inner integral $=-\infty$, so

$$
\begin{aligned}\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x&=\int_{0}^{1}\left(\int_{0}^{x}\left(x-y\right)^{-3}\mathrm{d}y\right)\mathrm{d}x\\&=-\infty.
\end{aligned}
$$

**Conclusion.** $\int_{E}f\,\mathrm{d}m^{2}$ does not exist ($f\notin L^{1}$); $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y=+\infty$ while $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x=-\infty$; the two iterated integrals exist but are not equal and have opposite signs. This is a classic counterexample showing Fubini's theorem fails: when integrability is not absolute, the order of integration cannot be interchanged. $\blacksquare$

### Problem 4

Prove Problem 56. If $f$ is Lebesgue integrable on $\left(0,a\right)$ and $g\left(x\right)=\int_{x}^{a}t^{-1}f\left(t\right)\mathrm{d}t$, then $g$ is integrable on $\left(0,a\right)$ and $\int_{0}^{a}g\left(x\right)\mathrm{d}x=\int_{0}^{a}f\left(x\right)\mathrm{d}x$.

### Solution to Problem 4

First consider the two-variable function $h\left(x,t\right)=t^{-1}f\left(t\right)\chi_{\left\{x< t\right\}}\left(x,t\right)$ on $\left(0,a\right)\times\left(0,a\right)$ (i.e. on the domain $\left\{\left(x,t\right):0< x< t< a\right\}$). By **Theorem 10.2.2** (Tonelli, nonnegative function $\left|h\right|$),

$$
\begin{aligned}\int_{0}^{a}\int_{x}^{a}t^{-1}\left|f\left(t\right)\right|\mathrm{d}t\,\mathrm{d}x&=\int_{0}^{a}\left(\int_{0}^{t}t^{-1}\left|f\left(t\right)\right|\mathrm{d}x\right)\mathrm{d}t\\&=\int_{0}^{a}t^{-1}\left|f\left(t\right)\right|\cdot t\,\mathrm{d}t\\&=\int_{0}^{a}\left|f\left(t\right)\right|\mathrm{d}t\\&< \infty,
\end{aligned}
$$

where the interchange of order in the inner integral uses **Theorem 10.2.2** for a nonnegative function. Hence $\left(x,t\right)\mapsto t^{-1}f\left(t\right)\chi_{\left\{x< t\right\}}$ is integrable, and therefore $g$ is integrable. Then by **Theorem 10.2.1** (Fubini), interchanging the order,

$$
\begin{aligned}\int_{0}^{a}g\left(x\right)\mathrm{d}x&=\int_{0}^{a}\int_{x}^{a}t^{-1}f\left(t\right)\mathrm{d}t\,\mathrm{d}x\\&=\int_{0}^{a}\left(\int_{0}^{t}t^{-1}f\left(t\right)\mathrm{d}x\right)\mathrm{d}t\\&=\int_{0}^{a}t^{-1}f\left(t\right)\cdot t\,\mathrm{d}t\\&=\int_{0}^{a}f\left(t\right)\mathrm{d}t.
\end{aligned}
$$

$\blacksquare$

### Problem 5

Prove Problem 59. Let $f\left(x\right)=x^{-1}\sin x$.

a. Prove that $\int_{0}^{\infty}\left|f\left(x\right)\right|\mathrm{d}x=\infty$.

b. Prove that $\lim_{b\to\infty}\int_{0}^{b}f\left(x\right)\mathrm{d}x=\frac{1}{2}\pi$, by integrating $e^{-xy}\sin x$ with respect to $x$ and $y$. (In view of (a), taking the limit $b\to\infty$ requires care.)

### Solution to Problem 5

#### a

On the interval $\left[k\pi,\left(k+1\right)\pi\right]$, $\left|\sin x\right|\ge0$ and $\int_{k\pi}^{\left(k+1\right)\pi}\left|\sin x\right|\mathrm{d}x=2$. Since $\frac{1}{x}$ on this interval is $\ge\frac{1}{\left(k+1\right)\pi}$, we have

$$
\int_{k\pi}^{\left(k+1\right)\pi}\frac{\left|\sin x\right|}{x}\mathrm{d}x\ge\frac{2}{\left(k+1\right)\pi}.
$$

Hence for any $N$,

$$
\int_{0}^{\left(N+1\right)\pi}\frac{\left|\sin x\right|}{x}\mathrm{d}x\ge\sum_{k=0}^{N}\frac{2}{\left(k+1\right)\pi}\to\infty
$$

(the harmonic series diverges), so $\int_{0}^{\infty}\left|f\right|\mathrm{d}x=\infty$. $\blacksquare$

#### b

For fixed $b> 0$, since $\int_{0}^{b}\int_{0}^{\infty}\left|e^{-xy}\sin x\right|\mathrm{d}y\,\mathrm{d}x=\int_{0}^{b}\frac{\left|\sin x\right|}{x}\mathrm{d}x< \infty$ (for fixed $b$, $x^{-1}\sin x$ is integrable), by **Theorem 10.2.2** (Tonelli) the order may be interchanged:

$$
\begin{aligned}\int_{0}^{b}\frac{\sin x}{x}\mathrm{d}x&=\int_{0}^{b}\int_{0}^{\infty}e^{-xy}\sin x\,\mathrm{d}y\,\mathrm{d}x\\&=\int_{0}^{\infty}\left(\int_{0}^{b}e^{-xy}\sin x\,\mathrm{d}x\right)\mathrm{d}y.
\end{aligned}
$$

For fixed $y$, integrating by parts twice gives $\int_{0}^{b}e^{-xy}\sin x\,\mathrm{d}x=\frac{1-e^{-by}\left(y\sin b+\cos b\right)}{1+y^{2}}$. Hence

$$
\int_{0}^{b}\frac{\sin x}{x}\mathrm{d}x=\int_{0}^{\infty}\frac{1-e^{-by}\left(y\sin b+\cos b\right)}{1+y^{2}}\mathrm{d}y.
$$

**Taking the limit $b\to\infty$.** Split into two terms $\frac{1}{1+y^{2}}-\frac{e^{-by}\left(y\sin b+\cos b\right)}{1+y^{2}}$. The first integrates to $\int_{0}^{\infty}\frac{1}{1+y^{2}}\mathrm{d}y=\frac{\pi}{2}$. For the second, when $b\ge1$, $\left|\frac{e^{-by}\left(y\sin b+\cos b\right)}{1+y^{2}}\right|\le\frac{e^{-y}\left(y+1\right)}{1+y^{2}}=:g\left(y\right)$, and $\int_{0}^{\infty}g\left(y\right)\mathrm{d}y< \infty$ (dominated by the exponential decay of $e^{-y}$). By **Theorem 8.2.9** (Dominated Convergence Theorem, applied along any sequence $b_{n}\to\infty$), this term tends to $\int_{0}^{\infty}0\,\mathrm{d}y=0$. Hence

$$
\begin{aligned}\lim_{b\to\infty}\int_{0}^{b}\frac{\sin x}{x}\mathrm{d}x&=\frac{\pi}{2}-0\\&=\frac{\pi}{2}.
\end{aligned}
$$

$\blacksquare$

### Problem 6

Prove Problem 61. If $f$ is continuous on $\left[0,\infty\right)$, for $\alpha> 0$ and $x\ge0$, set

$$
I_{\alpha}f\left(x\right)=\frac{1}{\Gamma\left(\alpha\right)}\int_{0}^{x}\left(x-t\right)^{\alpha-1}f\left(t\right)\mathrm{d}t,
$$

$I_{\alpha}f$ is called the $\alpha$-th order fractional integral of $f$.

a. $I_{\alpha+\beta}f=I_{\alpha}\left(I_{\beta}f\right)$ for all $\alpha,\beta> 0$. (Use Problem 60.)

b. If $n\in\mathbb N$, $I_{n}f$ is the $n$-th antiderivative of $f$.

### Solution to Problem 6

#### a

Expand the composite integral and interchange the order over the region $\left\{\left(s,t\right):0< t< s< x\right\}$:

$$
I_{\alpha}\left(I_{\beta}f\right)\left(x\right)=\frac{1}{\Gamma\left(\alpha\right)}\int_{0}^{x}\left(x-s\right)^{\alpha-1}\left[\frac{1}{\Gamma\left(\beta\right)}\int_{0}^{s}\left(s-t\right)^{\beta-1}f\left(t\right)\mathrm{d}t\right]\mathrm{d}s.
$$

Since $f$ is continuous, the integrand is nonnegative or integrable; by **Theorem 10.2.1** (Fubini), interchanging the order gives

$$
=\frac{1}{\Gamma\left(\alpha\right)\Gamma\left(\beta\right)}\int_{0}^{x}f\left(t\right)\left[\int_{t}^{x}\left(x-s\right)^{\alpha-1}\left(s-t\right)^{\beta-1}\mathrm{d}s\right]\mathrm{d}t.
$$

For the inner integral, set $u=\frac{s-t}{x-t}$; then $s=t+u\left(x-t\right)$, $\mathrm{d}s=\left(x-t\right)\mathrm{d}u$, giving

$$
\int_{t}^{x}\left(x-s\right)^{\alpha-1}\left(s-t\right)^{\beta-1}\mathrm{d}s=\left(x-t\right)^{\alpha+\beta-1}\int_{0}^{1}\left(1-u\right)^{\alpha-1}u^{\beta-1}\mathrm{d}u.
$$

By the Basic Knowledge (the Gamma function and the beta identity), $\int_{0}^{1}\left(1-u\right)^{\alpha-1}u^{\beta-1}\mathrm{d}u=\frac{\Gamma\left(\alpha\right)\Gamma\left(\beta\right)}{\Gamma\left(\alpha+\beta\right)}$. Substituting gives

$$
\begin{aligned}I_{\alpha}\left(I_{\beta}f\right)\left(x\right)&=\frac{1}{\Gamma\left(\alpha+\beta\right)}\int_{0}^{x}\left(x-t\right)^{\alpha+\beta-1}f\left(t\right)\mathrm{d}t\\&=I_{\alpha+\beta}f\left(x\right).
\end{aligned}
$$

$\blacksquare$

#### b

First consider $\alpha=1$: since $\Gamma\left(1\right)=1$,

$$
I_{1}f\left(x\right)=\int_{0}^{x}f\left(t\right)\mathrm{d}t,
$$

by the fundamental theorem of calculus, $\frac{\mathrm{d}}{\mathrm{d}x}I_{1}f=f$. By (a), iterating gives $I_{n}f=\underbrace{I_{1}\circ\cdots\circ I_{1}}_{n\text{次}}f$, so $\frac{\mathrm{d}^{n}}{\mathrm{d}x^{n}}I_{n}f=f$. Also, since the lower limit of integration of $I_{\alpha}f$ is $0$, for $k< n$, $\left(\frac{\mathrm{d}}{\mathrm{d}x}\right)^{k}I_{n}f$ takes the value $0$ at $0$. Hence $I_{n}f$ is an $n$-th antiderivative of $f$. $\blacksquare$

### Problem 7

Prove Problem 62. The measure $\sigma$ on $S^{n-1}$ is invariant under rotations.

### Solution to Problem 7

Let $R\in O\left(n\right)$, i.e. $R^{T}R=I$; then $\left|\det R\right|=1$. By the Basic Knowledge (orthogonal transformations preserve the Lebesgue measure), $R$ preserves $m$ on $\mathbb R^{n}$. Since $R$ preserves the norm, $\left|Rx\right|=\left|x\right|$, under the spherical-coordinate decomposition $\Phi\left(x\right)=\left(r,x'\right)$ it acts on the spherical part: there exists a rotation $\rho$ on the sphere $S^{n-1}$ such that $R\left(rx'\right)=r\rho\left(x'\right)$. Let $m^{*}$ be the measure induced by polar coordinates ($m^{*}=\rho\times\sigma$ by **Theorem 11.4.1**); for a Borel set $A\subset\left(0,\infty\right)\times S^{n-1}$,

$$
\begin{aligned}m^{*}\left(\left(\mathrm{id}\times\rho\right)\left(A\right)\right)&=m\left(\Phi^{-1}\left(\left(\mathrm{id}\times\rho\right)\left(A\right)\right)\right)\\&=m\left(R\Phi^{-1}\left(A\right)\right)\\&=m\left(\Phi^{-1}\left(A\right)\right)\\&=m^{*}\left(A\right),
\end{aligned}
$$

so $m^{*}$ is rotation-invariant.

Define $\sigma_{R}\left(E\right):=\sigma\left(R^{-1}E\right)=\sigma\left(R^{T}E\right)$; it is a Borel measure on $S^{n-1}$. On a rectangle $\left(a,b\right]\times E\subset\left(0,\infty\right)\times S^{n-1}$,

$$
\begin{aligned}\left(\rho\times\sigma_{R}\right)\left(\left(a,b\right]\times E\right)&=\int_{a}^{b}r^{n-1}\mathrm{d}r\cdot\sigma_{R}\left(E\right)\\&=\rho\left(\left(a,b\right]\right)\cdot\sigma\left(R^{-1}E\right).
\end{aligned}
$$

By $m^{*}=\rho\times\sigma$ (**Theorem 11.4.1**), $\rho\left(\left(a,b\right]\right)\cdot\sigma\left(R^{-1}E\right)=m^{*}\left(\left(a,b\right]\times R^{-1}E\right)$. Also, by the rotation-invariance of $m^{*}$, $m^{*}\left(\left(a,b\right]\times R^{-1}E\right)=m^{*}\left(\left(a,b\right]\times E\right)=\rho\left(\left(a,b\right]\right)\cdot\sigma\left(E\right)$. Hence on rectangles, $\rho\times\sigma_{R}=\rho\times\sigma$. By the Basic Knowledge (uniqueness of a measure on a generating family of the product $\sigma$-algebra), $\rho\times\sigma_{R}=\rho\times\sigma$ on $\left(0,\infty\right)\times S^{n-1}$.

Finally, by the uniqueness in **Theorem 11.4.1** (the measure $\sigma$ such that $m^{*}=\rho\times\sigma$ is unique), from $\rho\times\sigma_{R}=m^{*}=\rho\times\sigma$ we get $\sigma_{R}=\sigma$, i.e. $\sigma\left(R^{-1}E\right)=\sigma\left(E\right)$ for every Borel $E$. Hence $\sigma$ is rotation-invariant. $\blacksquare$

### Problem 8

Prove Problem 64. For which real values of $a$ and $b$ is $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ integrable on the set $\left\{x\in\mathbb R^{n}:\left|x\right|< 1/2\right\}$? On the set $\left\{x\in\mathbb R^{n}:\left|x\right|> 2\right\}$?

### Solution to Problem 8

The function $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ is radial; by **Theorem 11.4.1** (polar-coordinate decomposition),

$$\int_{\mathbb R^{n}}\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}\mathrm{d}x=\sigma\left(S^{n-1}\right)\int_{0}^{\infty}r^{a+n-1}\left|\log r\right|^{b}\mathrm{d}r.$$

**The set $\left\{\left|x\right|< 1/2\right\}$.** Make the substitution $u=-\log r$ (i.e. $r=e^{-u}$, $\mathrm{d}r=-e^{-u}\mathrm{d}u$, so $r\in\left(0,1/2\right]$ corresponds to $u\in\left[\log 2,\infty\right)$):

$$
\begin{aligned}\int_{0}^{1/2}r^{a+n-1}\left|\log r\right|^{b}\mathrm{d}r&=\int_{\log 2}^{\infty}e^{-u\left(a+n-1\right)}e^{-u}u^{b}\mathrm{d}u\\&=\int_{\log 2}^{\infty}e^{-u\left(a+n\right)}u^{b}\mathrm{d}u.
\end{aligned}
$$

The convergence condition is determined by the exponential factor:

$$
\int_{\log 2}^{\infty}e^{-u\left(a+n\right)}u^{b}\mathrm{d}u\text{收敛}\iff\begin{cases}a+n> 0,&\text{指数衰减, 任意 }b,\\a+n=0\text{且}b< -1,&\int u^{b}\mathrm{d}u\text{收敛},\\a+n< 0,&\text{指数增长, 发散}.\end{cases}
$$

Hence $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ is integrable on $\left\{\left|x\right|< 1/2\right\}$ $\iff a> -n$, or $a=-n$ and $b< -1$.

**The set $\left\{\left|x\right|> 2\right\}$.** When $r\ge2$, $\left|\log r\right|=\log r$. Make the substitution $r=e^{u}$ ($\mathrm{d}r=e^{u}\mathrm{d}u$, $u\ge\log 2$):

$$
\begin{aligned}\int_{2}^{\infty}r^{a+n-1}\left(\log r\right)^{b}\mathrm{d}r&=\int_{\log 2}^{\infty}e^{u\left(a+n-1\right)}e^{u}u^{b}\mathrm{d}u\\&=\int_{\log 2}^{\infty}e^{u\left(a+n\right)}u^{b}\mathrm{d}u.
\end{aligned}
$$

Convergence condition:

$$
\int_{\log 2}^{\infty}e^{u\left(a+n\right)}u^{b}\mathrm{d}u\text{收敛}\iff a+n< 0
$$

(exponential decay; when $a+n> 0$ the exponential growth causes divergence, and when $a+n=0$, $\int u^{b}\mathrm{d}u$ diverges for any $b$). Hence $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ is integrable on $\left\{\left|x\right|> 2\right\}$ $\iff a< -n$.

**Conclusion.** Integrable on $\left\{\left|x\right|< 1/2\right\}$ $\iff a> -n$ or $\left(a=-n\text{且}b< -1\right)$; integrable on $\left\{\left|x\right|> 2\right\}$ $\iff a< -n$. $\blacksquare$
