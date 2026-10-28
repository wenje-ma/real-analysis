# week8

> **Basic Knowledge: Invariance Under Translation and Dilation in One Dimension**<br>For $c\in\mathbb R$ and $\lambda\ne0$, Lebesgue measure satisfies $m\left(E+c\right)=m\left(E\right)$ and $m\left(\lambda E\right)=\left|\lambda\right|m\left(E\right)$.

> **Basic Knowledge: Invertible Linear Maps Preserve Measurability and Null Sets**<br>If $T\in GL\left(n,\mathbb R\right)$, then $T\left(E\right)\in\mathcal L^{n}$ iff $E\in\mathcal L^{n}$, and $T$ preserves null sets.

> **Basic Knowledge: Orthogonal Transformations Preserve Lebesgue Measure**<br>If $R\in O\left(n\right)$, i.e. $R^{\top}R=I$, then $\left|\det R\right|=1$, and $m\left(R\left(E\right)\right)=m\left(E\right)$ for every $E\in\mathcal L^{n}$.

> **Basic Knowledge: Gamma Function and the Beta Identity**<br>The gamma function $\Gamma\left(x\right)=\int_{0}^{\infty}t^{x-1}e^{-t}\mathrm{d}t$ satisfies $\Gamma\left(x+1\right)=x\Gamma\left(x\right)$; the beta function satisfies $\frac{\Gamma\left(x\right)\Gamma\left(y\right)}{\Gamma\left(x+y\right)}=\int_{0}^{1}t^{x-1}\left(1-t\right)^{y-1}\mathrm{d}t$ for $x,y> 0$.

> **Basic Knowledge: Continuous Approximation of Characteristic Functions**<br>If $R\subset\mathbb R^{n}$ is a bounded closed rectangle, then for every $\varepsilon> 0$ there exists a continuous compactly supported function $g$ with $\int\left|\chi_{R}-g\right|\mathrm{d}m< \varepsilon$.

> **Basic Knowledge: Uniqueness of Measures on a Generating Rectangle Family**<br>Two $\sigma$-finite measures that agree on a rectangle family generating the product $\sigma$-algebra agree on the whole product $\sigma$-algebra.

> **Theorem 8.2.9 (Dominated Convergence Theorem)**<br>Let $\left(X,\mathcal F,\mu\right)$ be a measure space and $\left\{f_{n}\right\}$ a sequence of measurable functions. If there exists an integrable $g$ with $\left|f_{n}\right|\le g$ for all $n$ and $f_{n}\to f$ a.e., then $f$ is integrable and $\int f\,\mathrm{d}\mu=\lim_{n\to\infty}\int f_{n}\,\mathrm{d}\mu$.

> **Theorem 8.2.16 (Integrable Simple Functions Are Dense in $L^{1}$)**<br>If $f\in L^{1}\left(\mu\right)$ and $\varepsilon> 0$, then there exists an integrable simple function $\varphi=\sum a_{j}\chi_{E_{j}}$ with $\int\left|f-\varphi\right|\mathrm{d}\mu< \varepsilon$.

> **Theorem 10.2.1 (Fubini's Theorem)**<br>Let $\left(X,\mathcal A,\mu\right)$ and $\left(Y,\mathcal B,\nu\right)$ be $\sigma$-finite measure spaces and $f:X\times Y\to\mathbb R$ be $\mathcal A\otimes\mathcal B$-measurable. If $f$ is integrable on $X\times Y$, then for almost every $x$, $y\mapsto f\left(x,y\right)$ is $\nu$-integrable; for almost every $y$, $x\mapsto f\left(x,y\right)$ is $\mu$-integrable; and the iterated integrals agree:

$$
\int_{X\times Y}f\,\mathrm{d}\left(\mu\times\nu\right)=\int_{X}\left(\int_{Y}f\left(x,y\right)\mathrm{d}\nu\left(y\right)\right)\mathrm{d}\mu\left(x\right)=\int_{Y}\left(\int_{X}f\left(x,y\right)\mathrm{d}\mu\left(x\right)\right)\mathrm{d}\nu\left(y\right).
$$

> **Theorem 10.2.2 (Tonelli's Theorem)**<br>If $f:X\times Y\to\left[0,\infty\right]$ is $\mathcal A\otimes\mathcal B$-measurable, then

$$
\int_{X\times Y}f\,\mathrm{d}\left(\mu\times\nu\right)=\int_{X}\left(\int_{Y}f\left(x,y\right)\mathrm{d}\nu\left(y\right)\right)\mathrm{d}\mu\left(x\right)=\int_{Y}\left(\int_{X}f\left(x,y\right)\mathrm{d}\mu\left(x\right)\right)\mathrm{d}\nu\left(y\right),
$$

with all integral values in $\left[0,\infty\right]$.

> **Theorem 11.1.1 (Regularity of Lebesgue Measure and Rectangle Approximation)**<br>Let $E\in\mathcal L^{n}$. (a)

$$
m\left(E\right)=\inf\left\{m\left(U\right):U\supset E,U\text{ open}\right\}=\sup\left\{m\left(K\right):K\subset E,K\text{ compact}\right\};
$$

(b) if $m\left(E\right)< \infty$, then for every $\varepsilon> 0$ there is a finite family of pairwise-disjoint rectangles $\left\{R_{j}\right\}_{j=1}^{N}$ with interval sides such that $m\left(E\triangle\bigcup_{j=1}^{N}R_{j}\right)< \varepsilon$.

> **Theorem 11.4.1 (Integration in Polar Coordinates)**<br>There is a unique Borel measure $\sigma=\sigma_{n-1}$ on $S^{n-1}$ such that $m^{*}=\rho\times\sigma$. If $f$ is Borel measurable on $\mathbb R^{n}$ and either $f\ge0$ or $f\in L^{1}\left(m\right)$, then

$$
\int_{\mathbb R^{n}}f\left(x\right)\mathrm{d}x=\int_{0}^{\infty}\int_{S^{n-1}}f\left(rx'\right)r^{n-1}\mathrm{d}\sigma\left(x'\right)\mathrm{d}r.
$$

---

## 1

If $f\in L^{1}\left(m\right)$ and $\varepsilon> 0$, then there is a simple function $\varphi=\sum a_{j}\chi_{R_{j}}$, each $R_{j}$ a product of intervals, with $\int\left|f-\varphi\right|< \varepsilon$; and there is a continuous function $g$ vanishing outside a bounded set with $\int\left|f-g\right|< \varepsilon$.

### Solution 1

**Simple-function part.** By **Theorem 8.2.16 (Integrable Simple Functions Are Dense in $L^{1}$)**, there is an integrable simple function $\varphi=\sum_{j}a_{j}\chi_{E_{j}}$ with $\int\left|f-\varphi\right|< \varepsilon/2$. For the terms with $a_{j}\ne0$, since $\int a_{j}\chi_{E_{j}}\,\mathrm{d}m=a_{j}m\left(E_{j}\right)< \infty$, we have $m\left(E_{j}\right)< \infty$ (otherwise the integral diverges, contradicting integrability). By **Theorem 11.1.1 (Regularity of Lebesgue Measure and Rectangle Approximation)** (b), for each such $E_{j}$ there are finitely many pairwise-disjoint rectangles $\left\{R_{j,k}\right\}$ with interval sides such that $m\left(E_{j}\triangle\bigcup_{k}R_{j,k}\right)$ is arbitrarily small. Thus $\chi_{E_{j}}$ and $\chi_{R_{j}}$ (with $R_{j}=\bigcup_{k}R_{j,k}$) are arbitrarily close in $L^{1}$; taking the approximation errors small enough and combining over all $j$, we obtain a simple function $\varphi'=\sum_{j}a_{j}\chi_{R_{j}}$ with $\int\left|\varphi-\varphi'\right|< \varepsilon/2$. Hence $\int\left|f-\varphi'\right|\le\int\left|f-\varphi\right|+\int\left|\varphi-\varphi'\right|< \varepsilon$.

**Continuous-function part.** Let $\varphi'=\sum_{j}a_{j}\chi_{R_{j}}$ be as obtained above, each $R_{j}$ a bounded closed rectangle. By **Basic Knowledge: Continuous Approximation of Characteristic Functions**, for each $R_{j}$ there is a continuous compactly supported $g_{j}$ with $\int\left|\chi_{R_{j}}-g_{j}\right|\mathrm{d}m$ arbitrarily small. Taking the errors small enough and setting $g=\sum_{j}a_{j}g_{j}$, $g$ is continuous, supported in $\bigcup_{j}R_{j}$ (bounded), and $\int\left|\varphi'-g\right|\le\sum_{j}\left|a_{j}\right|\int\left|\chi_{R_{j}}-g_{j}\right|< \varepsilon/2$. Hence $\int\left|f-g\right|\le\int\left|f-\varphi'\right|+\int\left|\varphi'-g\right|< \varepsilon$, and $g$ vanishes outside a bounded set. $\blacksquare$

---

## 2

(Linear change of variables) Assume $T\in GL\left(n,\mathbb R\right)$.

(a) If $f$ is Lebesgue measurable on $\mathbb R^{n}$, then $f\circ T$ is also. If $f\ge0$ or $f\in L^{1}\left(m\right)$, then $\int f\left(x\right)\mathrm{d}x=\left|\det T\right|\int f\circ T\left(x\right)\mathrm{d}x$.

(b) If $E\in\mathcal L^{n}$, then $T\left(E\right)\in\mathcal L^{n}$ and $m\left(T\left(E\right)\right)=\left|\det T\right|m\left(E\right)$.

### Solution 2

First treat the three elementary transformations, then combine.

**Dilation** $T_{1}\left(x_{1},\dots,x_{j},\dots,x_{n}\right)=\left(x_{1},\dots,cx_{j},\dots,x_{n}\right)$ ($c\ne0$). By **Basic Knowledge: Invariance Under Translation and Dilation in One Dimension** and the product structure, dilating one coordinate while fixing the others gives $m\left(T_{1}\left(E\right)\right)=\left|c\right|m\left(E\right)$ and $\int f\circ T_{1}\left(x\right)\mathrm{d}x=\frac{1}{\left|c\right|}\int f\left(x\right)\mathrm{d}x$, i.e. $\int f\left(x\right)\mathrm{d}x=\left|\det T_{1}\right|\int f\circ T_{1}\left(x\right)\mathrm{d}x$.

**Shear** $T_{2}\left(x_{1},\dots,x_{j},\dots,x_{n}\right)=\left(x_{1},\dots,x_{j}+cx_{k},\dots,x_{n}\right)$ ($k\ne j$). By **Basic Knowledge: Invariance Under Translation and Dilation in One Dimension** applied slicewise, $m\left(T_{2}\left(E\right)\right)=m\left(E\right)$ and $\int f\circ T_{2}\left(x\right)\mathrm{d}x=\int f\left(x\right)\mathrm{d}x$. Since $\det T_{2}=1$, the formula holds.

**Swap** $T_{3}$ swaps two coordinates, $\det T_{3}=-1$. By the symmetry of $m$ as a product measure, $m\left(T_{3}\left(E\right)\right)=m\left(E\right)$ and $\int f\circ T_{3}\left(x\right)\mathrm{d}x=\int f\left(x\right)\mathrm{d}x$, and $\left|\det T_{3}\right|=1$, so the formula holds.

**General case.** By elementary linear algebra, each $T\in GL\left(n,\mathbb R\right)$ is a finite product $T=T_{1}\circ\cdots\circ T_{k}$ of the three elementary transformations above (an invertible matrix reduces to the identity by row operations). For each elementary transform the above holds, and determinants multiply: $\left|\det T\right|=\prod_{i}\left|\det T_{i}\right|$. Substituting successively,

$$
\int f\left(x\right)\mathrm{d}x=\left|\det T_{1}\right|\int f\circ T_{1}\left(x\right)\mathrm{d}x=\cdots=\left|\det T\right|\int f\circ T\left(x\right)\mathrm{d}x,
$$

which is (a). Measurability: $T$ is continuous, and by **Basic Knowledge: Invertible Linear Maps Preserve Measurability and Null Sets**, $f\circ T$ is measurable and $T\left(E\right)\in\mathcal L^{n}$.

**Proof of (b).** Take $f=\chi_{T\left(E\right)}$ in (a):

$$
m\left(T\left(E\right)\right)=\int\chi_{T\left(E\right)}\left(x\right)\mathrm{d}x=\left|\det T\right|\int\chi_{T\left(E\right)}\circ T\left(x\right)\mathrm{d}x=\left|\det T\right|\int\chi_{E}\left(x\right)\mathrm{d}x=\left|\det T\right|m\left(E\right).
$$

$T\left(E\right)\in\mathcal L^{n}$ follows from measurability. $\blacksquare$

---

## 3

Let $E=\left[0,1\right]\times\left[0,1\right]$. Study the existence and equality of $\int_{E}f\,\mathrm{d}m^{2}$, $\int_{0}^{1}\int_{0}^{1}f\left(x,y\right)\mathrm{d}x\,\mathrm{d}y$, and $\int_{0}^{1}\int_{0}^{1}f\left(x,y\right)\mathrm{d}y\,\mathrm{d}x$, for the following $f$.

(a) $f\left(x,y\right)=\left(x^{2}-y^{2}\right)\left(x^{2}+y^{2}\right)^{-2}$;

(b) $f\left(x,y\right)=\left(1-xy\right)^{-a}$ ($a> 0$);

(c) $f\left(x,y\right)=\left(x-y\right)^{-3}$ if $0< y< x< 1$, and $0$ otherwise.

### Solution 3

**(a).** $\left|f\left(x,y\right)\right|=\frac{\left|x^{2}-y^{2}\right|}{\left(x^{2}+y^{2}\right)^{2}}\le\frac{x^{2}+y^{2}}{\left(x^{2}+y^{2}\right)^{2}}=\frac{1}{x^{2}+y^{2}}$. On $E$, $\int_{E}\frac{1}{x^{2}+y^{2}}\mathrm{d}x\,\mathrm{d}y$ diverges (in polar coordinates, $\int_{0}^{\delta}\int_{0}^{\pi/2}\frac{1}{r^{2}}r\,\mathrm{d}\theta\,\mathrm{d}r=\frac{\pi}{2}\int_{0}^{\delta}\frac{1}{r}\mathrm{d}r=\infty$), so $\int_{E}\left|f\right|=\infty$, $f\notin L^{1}$, and $\int_{E}f\,\mathrm{d}m^{2}$ is undefined.

First integrating in $x$. Fix $y$, set $x=yt$; then $\int_{0}^{1}\frac{x^{2}-y^{2}}{\left(x^{2}+y^{2}\right)^{2}}\mathrm{d}x=\frac{1}{y}\int_{0}^{1/y}\frac{t^{2}-1}{\left(t^{2}+1\right)^{2}}\mathrm{d}t$. Since $\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{t}{t^{2}+1}\right)=\frac{1-t^{2}}{\left(t^{2}+1\right)^{2}}$, we have $\int\frac{t^{2}-1}{\left(t^{2}+1\right)^{2}}\mathrm{d}t=-\frac{t}{t^{2}+1}+C$, so the inner integral $=\frac{1}{y}\left[-\frac{t}{t^{2}+1}\right]_{0}^{1/y}=-\frac{1}{y^{2}+1}$. Hence $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y=\int_{0}^{1}-\frac{1}{1+y^{2}}\mathrm{d}y=-\left[\arctan y\right]_{0}^{1}=-\frac{\pi}{4}$.

First integrating in $y$. Symmetrically, fix $x$, set $y=xt$; the inner integral $\int_{0}^{1}f\,\mathrm{d}y=\frac{1}{x^{2}+1}$, so $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x=\int_{0}^{1}\frac{1}{1+x^{2}}\mathrm{d}x=\frac{\pi}{4}$.

Conclusion: $\int_{E}f\,\mathrm{d}m^{2}$ does not exist; $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y=-\frac{\pi}{4}$ and $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x=\frac{\pi}{4}$ exist but are unequal and opposite in sign. Since $f\notin L^{1}$, **Theorem 10.2.1 (Fubini's Theorem)** does not apply, and the iterated integrals cannot be exchanged.

**(b).** $f\ge0$. Fix $y$; the inner integral $\int_{0}^{1}\left(1-xy\right)^{-a}\mathrm{d}x=\frac{1}{y}\cdot\frac{1-\left(1-y\right)^{1-a}}{1-a}$ (when $a\ne1$), and for $a=1$ the inner integral $=-\frac{\ln\left(1-y\right)}{y}$. For $0< a< 1$, the inner integral tends to $1$ as $y\to0$ and to $\frac{1}{1-a}$ as $y\to1$ (since $\left(1-y\right)^{1-a}\to0$), hence is bounded, and $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y< \infty$. For $a=1$, $\int_{0}^{1}-\frac{\ln\left(1-y\right)}{y}\mathrm{d}y=\sum_{k=1}^{\infty}\frac{1}{k^{2}}=\frac{\pi^{2}}{6}< \infty$. Thus for $0< a\le1$, $f\in L^{1}$, and by **Theorem 10.2.2 (Tonelli's Theorem)**, all three integrals exist and agree.

For $a> 1$, the inner integral $\frac{1}{y}\cdot\frac{1-\left(1-y\right)^{1-a}}{1-a}$; since $1-a< 0$ and $\left(1-y\right)^{1-a}\to\infty$ as $y\to1$, the inner integral tends to $+\infty$, so $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y=+\infty$; symmetrically $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x=+\infty$, and $\int_{E}f\,\mathrm{d}m^{2}=+\infty$.

Conclusion: for $0< a\le1$, the three integrals exist and agree, $f\in L^{1}$; for $a> 1$, all three are $+\infty$, $f\notin L^{1}$.

**(c).** The region is $\left\{\left(x,y\right):0< y< x< 1\right\}$. $\left|f\right|=\left(x-y\right)^{-3}$. First integrating in $x$, $\int_{y}^{1}\left(x-y\right)^{-3}\mathrm{d}x=\left[-\frac{1}{2}\left(x-y\right)^{-2}\right]_{y}^{1}=+\infty$, so $\int_{E}\left|f\right|=\infty$, $f\notin L^{1}$, and $\int_{E}f\,\mathrm{d}m^{2}$ is undefined.

First integrating in $x$: fix $y$, $\int_{y}^{1}\left(x-y\right)^{-3}\mathrm{d}x=\left[-\frac{1}{2}\left(x-y\right)^{-2}\right]_{y}^{1}$; since $\lim_{x\to y^{+}}\left(x-y\right)^{-2}=\infty$, the inner integral $=+\infty$, so $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y=+\infty$.

First integrating in $y$: fix $x$, $\int_{0}^{x}\left(x-y\right)^{-3}\mathrm{d}y=\left[-\frac{1}{2}\left(x-y\right)^{-2}\right]_{0}^{x}$; since $\lim_{y\to x^{-}}\left(x-y\right)^{-2}=\infty$, the inner integral $=-\infty$, so $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x=-\infty$.

Conclusion: $\int_{E}f\,\mathrm{d}m^{2}$ does not exist; $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}x\,\mathrm{d}y=+\infty$ while $\int_{0}^{1}\int_{0}^{1}f\,\mathrm{d}y\,\mathrm{d}x=-\infty$. This is the classic counterexample where Fubini fails: without absolute integrability the order of integration cannot be exchanged. $\blacksquare$

---

## 4

If $f$ is Lebesgue integrable on $\left(0,a\right)$ and $g\left(x\right)=\int_{x}^{a}t^{-1}f\left(t\right)\mathrm{d}t$, then $g$ is integrable on $\left(0,a\right)$ and $\int_{0}^{a}g\left(x\right)\mathrm{d}x=\int_{0}^{a}f\left(x\right)\mathrm{d}x$.

### Solution 4

Consider on $\left(0,a\right)\times\left(0,a\right)$ the function $h\left(x,t\right)=t^{-1}f\left(t\right)\chi_{\left\{x< t\right\}}\left(x,t\right)$ (domain $\left\{\left(x,t\right):0< x< t< a\right\}$). By **Theorem 10.2.2 (Tonelli's Theorem)** applied to the nonnegative $\left|h\right|$,

$$
\int_{0}^{a}\int_{x}^{a}t^{-1}\left|f\left(t\right)\right|\mathrm{d}t\,\mathrm{d}x=\int_{0}^{a}\left(\int_{0}^{t}t^{-1}\left|f\left(t\right)\right|\mathrm{d}x\right)\mathrm{d}t=\int_{0}^{a}t^{-1}\left|f\left(t\right)\right|\cdot t\,\mathrm{d}t=\int_{0}^{a}\left|f\left(t\right)\right|\mathrm{d}t< \infty,
$$

where the inner exchange uses **Theorem 10.2.2 (Tonelli's Theorem)** on a nonnegative function. Thus $\left(x,t\right)\mapsto t^{-1}f\left(t\right)\chi_{\left\{x< t\right\}}$ is integrable, and hence $g$ is integrable. Then by **Theorem 10.2.1 (Fubini's Theorem)** exchanging the order,

$$
\int_{0}^{a}g\left(x\right)\mathrm{d}x=\int_{0}^{a}\int_{x}^{a}t^{-1}f\left(t\right)\mathrm{d}t\,\mathrm{d}x=\int_{0}^{a}\left(\int_{0}^{t}t^{-1}f\left(t\right)\mathrm{d}x\right)\mathrm{d}t=\int_{0}^{a}t^{-1}f\left(t\right)\cdot t\,\mathrm{d}t=\int_{0}^{a}f\left(t\right)\mathrm{d}t.
$$

$\blacksquare$

---

## 5

Let $f\left(x\right)=x^{-1}\sin x$.

(a) Prove $\int_{0}^{\infty}\left|f\left(x\right)\right|\mathrm{d}x=\infty$.

(b) Prove $\lim_{b\to\infty}\int_{0}^{b}f\left(x\right)\mathrm{d}x=\frac{1}{2}\pi$, by integrating $e^{-xy}\sin x$ in $x$ and $y$.

### Solution 5

**(a).** On $\left[k\pi,\left(k+1\right)\pi\right]$, $\int_{k\pi}^{\left(k+1\right)\pi}\left|\sin x\right|\mathrm{d}x=2$. Since $\frac{1}{x}$ on this interval is $\ge\frac{1}{\left(k+1\right)\pi}$, we have $\int_{k\pi}^{\left(k+1\right)\pi}\frac{\left|\sin x\right|}{x}\mathrm{d}x\ge\frac{2}{\left(k+1\right)\pi}$. Thus for any $N$, $\int_{0}^{\left(N+1\right)\pi}\frac{\left|\sin x\right|}{x}\mathrm{d}x\ge\sum_{k=0}^{N}\frac{2}{\left(k+1\right)\pi}\to\infty$ (harmonic series diverges), so $\int_{0}^{\infty}\left|f\right|\mathrm{d}x=\infty$.

**(b).** For fixed $b> 0$, since $\int_{0}^{b}\int_{0}^{\infty}\left|e^{-xy}\sin x\right|\mathrm{d}y\,\mathrm{d}x=\int_{0}^{b}\frac{\left|\sin x\right|}{x}\mathrm{d}x< \infty$ (for fixed $b$, $x^{-1}\sin x$ is integrable), by **Theorem 10.2.2 (Tonelli's Theorem)** we may exchange the order:

$$
\int_{0}^{b}\frac{\sin x}{x}\mathrm{d}x=\int_{0}^{b}\int_{0}^{\infty}e^{-xy}\sin x\,\mathrm{d}y\,\mathrm{d}x=\int_{0}^{\infty}\left(\int_{0}^{b}e^{-xy}\sin x\,\mathrm{d}x\right)\mathrm{d}y.
$$

For fixed $y$, integrating by parts twice gives $\int_{0}^{b}e^{-xy}\sin x\,\mathrm{d}x=\frac{1-e^{-by}\left(y\sin b+\cos b\right)}{1+y^{2}}$. Hence $\int_{0}^{b}\frac{\sin x}{x}\mathrm{d}x=\int_{0}^{\infty}\frac{1-e^{-by}\left(y\sin b+\cos b\right)}{1+y^{2}}\mathrm{d}y$.

**Taking $b\to\infty$.** Split into $\frac{1}{1+y^{2}}-\frac{e^{-by}\left(y\sin b+\cos b\right)}{1+y^{2}}$. The first integrates to $\int_{0}^{\infty}\frac{1}{1+y^{2}}\mathrm{d}y=\frac{\pi}{2}$. For the second, when $b\ge1$, $\left|\frac{e^{-by}\left(y\sin b+\cos b\right)}{1+y^{2}}\right|\le\frac{e^{-y}\left(y+1\right)}{1+y^{2}}=:g\left(y\right)$, and $\int_{0}^{\infty}g\left(y\right)\mathrm{d}y< \infty$ (dominated by the exponential decay $e^{-y}$). By **Theorem 8.2.9 (Dominated Convergence Theorem)** (applied along any sequence $b_{n}\to\infty$), this term tends to $\int_{0}^{\infty}0\,\mathrm{d}y=0$. Hence $\lim_{b\to\infty}\int_{0}^{b}\frac{\sin x}{x}\mathrm{d}x=\frac{\pi}{2}$. $\blacksquare$

---

## 6

If $f$ is continuous on $\left[0,\infty\right)$, for $\alpha> 0$ and $x\ge0$ set

$$
I_{\alpha}f\left(x\right)=\frac{1}{\Gamma\left(\alpha\right)}\int_{0}^{x}\left(x-t\right)^{\alpha-1}f\left(t\right)\mathrm{d}t,
$$

called the $\alpha$-th order fractional integral of $f$.

(a) $I_{\alpha+\beta}f=I_{\alpha}\left(I_{\beta}f\right)$ for all $\alpha,\beta> 0$.

(b) If $n\in\mathbb N$, $I_{n}f$ is an $n$-th antiderivative of $f$.

### Solution 6

**(a).** Expand the composite integral and exchange the order over $\left\{\left(s,t\right):0< t< s< x\right\}$:

$$
I_{\alpha}\left(I_{\beta}f\right)\left(x\right)=\frac{1}{\Gamma\left(\alpha\right)}\int_{0}^{x}\left(x-s\right)^{\alpha-1}\left[\frac{1}{\Gamma\left(\beta\right)}\int_{0}^{s}\left(s-t\right)^{\beta-1}f\left(t\right)\mathrm{d}t\right]\mathrm{d}s.
$$

Since $f$ is continuous, the integrand is integrable; by **Theorem 10.2.1 (Fubini's Theorem)**, exchanging the order gives

$$
=\frac{1}{\Gamma\left(\alpha\right)\Gamma\left(\beta\right)}\int_{0}^{x}f\left(t\right)\left[\int_{t}^{x}\left(x-s\right)^{\alpha-1}\left(s-t\right)^{\beta-1}\mathrm{d}s\right]\mathrm{d}t.
$$

For the inner integral, set $u=\frac{s-t}{x-t}$; then $s=t+u\left(x-t\right)$, $\mathrm{d}s=\left(x-t\right)\mathrm{d}u$, giving

$$
\int_{t}^{x}\left(x-s\right)^{\alpha-1}\left(s-t\right)^{\beta-1}\mathrm{d}s=\left(x-t\right)^{\alpha+\beta-1}\int_{0}^{1}\left(1-u\right)^{\alpha-1}u^{\beta-1}\mathrm{d}u.
$$

By **Basic Knowledge: Gamma Function and the Beta Identity**, $\int_{0}^{1}\left(1-u\right)^{\alpha-1}u^{\beta-1}\mathrm{d}u=\frac{\Gamma\left(\alpha\right)\Gamma\left(\beta\right)}{\Gamma\left(\alpha+\beta\right)}$. Substituting, $I_{\alpha}\left(I_{\beta}f\right)\left(x\right)=\frac{1}{\Gamma\left(\alpha+\beta\right)}\int_{0}^{x}\left(x-t\right)^{\alpha+\beta-1}f\left(t\right)\mathrm{d}t=I_{\alpha+\beta}f\left(x\right)$.

**(b).** For $\alpha=1$, since $\Gamma\left(1\right)=1$, $I_{1}f\left(x\right)=\int_{0}^{x}f\left(t\right)\mathrm{d}t$, and by the fundamental theorem of calculus $\frac{\mathrm{d}}{\mathrm{d}x}I_{1}f=f$. By (a), iterating gives $I_{n}f=\underbrace{I_{1}\circ\cdots\circ I_{1}}_{n\text{ times}}f$, so $\frac{\mathrm{d}^{n}}{\mathrm{d}x^{n}}I_{n}f=f$. Also, since the lower limit of $I_{\alpha}f$ is $0$, for $k< n$, $\left(\frac{\mathrm{d}}{\mathrm{d}x}\right)^{k}I_{n}f$ takes the value $0$ at $0$. Thus $I_{n}f$ is an $n$-th antiderivative of $f$. $\blacksquare$

---

## 7

The measure $\sigma$ on $S^{n-1}$ is rotation invariant.

### Solution 7

Let $R\in O\left(n\right)$, i.e. $R^{\top}R=I$, so $\left|\det R\right|=1$. By **Basic Knowledge: Orthogonal Transformations Preserve Lebesgue Measure**, $R$ preserves $m$ on $\mathbb R^{n}$. Since $R$ preserves the norm $\left|Rx\right|=\left|x\right|$, under the spherical-coordinate decomposition $\Phi\left(x\right)=\left(r,x'\right)$ it acts on the spherical part: there is a rotation $\rho$ of $S^{n-1}$ with $R\left(rx'\right)=r\rho\left(x'\right)$. Let $m^{*}$ be the polar-coordinate measure ($m^{*}=\rho\times\sigma$ by **Theorem 11.4.1 (Integration in Polar Coordinates)**); for a Borel set $A\subset\left(0,\infty\right)\times S^{n-1}$,

$$
m^{*}\left(\left(\mathrm{id}\times\rho\right)\left(A\right)\right)=m\left(\Phi^{-1}\left(\left(\mathrm{id}\times\rho\right)\left(A\right)\right)\right)=m\left(R\Phi^{-1}\left(A\right)\right)=m\left(\Phi^{-1}\left(A\right)\right)=m^{*}\left(A\right),
$$

so $m^{*}$ is rotation invariant.

Define $\sigma_{R}\left(E\right):=\sigma\left(R^{-1}E\right)=\sigma\left(R^{\top}E\right)$, a Borel measure on $S^{n-1}$. On a rectangle $\left(a,b\right]\times E\subset\left(0,\infty\right)\times S^{n-1}$,

$$
\left(\rho\times\sigma_{R}\right)\left(\left(a,b\right]\times E\right)=\int_{a}^{b}r^{n-1}\mathrm{d}r\cdot\sigma_{R}\left(E\right)=\rho\left(\left(a,b\right]\right)\cdot\sigma\left(R^{-1}E\right).
$$

By $m^{*}=\rho\times\sigma$ (**Theorem 11.4.1 (Integration in Polar Coordinates)**), $\rho\left(\left(a,b\right]\right)\cdot\sigma\left(R^{-1}E\right)=m^{*}\left(\left(a,b\right]\times R^{-1}E\right)$. By rotation invariance of $m^{*}$, $m^{*}\left(\left(a,b\right]\times R^{-1}E\right)=m^{*}\left(\left(a,b\right]\times E\right)=\rho\left(\left(a,b\right]\right)\cdot\sigma\left(E\right)$. Hence on rectangles $\rho\times\sigma_{R}=\rho\times\sigma$. By **Basic Knowledge: Uniqueness of Measures on a Generating Rectangle Family**, $\rho\times\sigma_{R}=\rho\times\sigma$ on $\left(0,\infty\right)\times S^{n-1}$.

Finally, by the uniqueness in **Theorem 11.4.1 (Integration in Polar Coordinates)** (the measure $\sigma$ with $m^{*}=\rho\times\sigma$ is unique), from $\rho\times\sigma_{R}=m^{*}=\rho\times\sigma$ we get $\sigma_{R}=\sigma$, i.e. $\sigma\left(R^{-1}E\right)=\sigma\left(E\right)$ for all Borel $E$. Thus $\sigma$ is rotation invariant. $\blacksquare$

---

## 8

For which real $a$ and $b$ is $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ integrable on $\left\{x\in\mathbb R^{n}:\left|x\right|< 1/2\right\}$? On $\left\{x\in\mathbb R^{n}:\left|x\right|> 2\right\}$?

### Solution 8

The function $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ is radial; by **Theorem 11.4.1 (Integration in Polar Coordinates)**,

$$
\int_{\mathbb R^{n}}\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}\mathrm{d}x=\sigma\left(S^{n-1}\right)\int_{0}^{\infty}r^{a+n-1}\left|\log r\right|^{b}\mathrm{d}r.
$$

**Set $\left\{\left|x\right|< 1/2\right\}$.** Substitute $u=-\log r$ (i.e. $r=e^{-u}$, $\mathrm{d}r=-e^{-u}\mathrm{d}u$, so $r\in\left(0,1/2\right]$ corresponds to $u\in\left[\log 2,\infty\right)$):

$$
\int_{0}^{1/2}r^{a+n-1}\left|\log r\right|^{b}\mathrm{d}r=\int_{\log 2}^{\infty}e^{-u\left(a+n-1\right)}e^{-u}u^{b}\mathrm{d}u=\int_{\log 2}^{\infty}e^{-u\left(a+n\right)}u^{b}\mathrm{d}u.
$$

The convergence is determined by the exponential factor:

$$
\int_{\log 2}^{\infty}e^{-u\left(a+n\right)}u^{b}\mathrm{d}u\text{ converges}\iff\begin{cases}a+n> 0,&\text{exponential decay, any }b,\\a+n=0\text{ and }b< -1,&\int u^{b}\mathrm{d}u\text{ converges},\\a+n< 0,&\text{exponential growth, diverges}.\end{cases}
$$

Thus $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ is integrable on $\left\{\left|x\right|< 1/2\right\}$ iff $a> -n$, or $a=-n$ and $b< -1$.

**Set $\left\{\left|x\right|> 2\right\}$.** For $r\ge2$, $\left|\log r\right|=\log r$. Substitute $r=e^{u}$ ($\mathrm{d}r=e^{u}\mathrm{d}u$, $u\ge\log 2$):

$$
\int_{2}^{\infty}r^{a+n-1}\left(\log r\right)^{b}\mathrm{d}r=\int_{\log 2}^{\infty}e^{u\left(a+n-1\right)}e^{u}u^{b}\mathrm{d}u=\int_{\log 2}^{\infty}e^{u\left(a+n\right)}u^{b}\mathrm{d}u.
$$

Convergence: $\int_{\log 2}^{\infty}e^{u\left(a+n\right)}u^{b}\mathrm{d}u\text{ converges}\iff a+n< 0$ (exponential decay; for $a+n> 0$ exponential growth diverges, for $a+n=0$, $\int u^{b}\mathrm{d}u$ diverges for any $b$). Thus $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ is integrable on $\left\{\left|x\right|> 2\right\}$ iff $a< -n$.

**Conclusion.** Integrable on $\left\{\left|x\right|< 1/2\right\}$ iff $a> -n$ or $\left(a=-n\text{ and }b< -1\right)$; integrable on $\left\{\left|x\right|> 2\right\}$ iff $a< -n$. $\blacksquare$
