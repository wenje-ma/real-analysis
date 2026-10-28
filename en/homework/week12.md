# week12

> **Basic Knowledge: NBV and Stieltjes Measures**<br>$NBV=\left\{F\in BV:F\text{ right-continuous},F\left(-\infty\right)=0\right\}$. For an increasing right-continuous $F$, a regular Borel measure $\mu_{F}$ is uniquely determined by $\mu_{F}\left(\left(a,b\right]\right)=F\left(b\right)-F\left(a\right)$.

> **Basic Knowledge: Total Variation of an Absolutely Continuous Function**<br>If $F$ is absolutely continuous on $\left[a,b\right]$, then its total variation is $V_{a}^{b}\left(F\right)=\int_{a}^{b}\left|F'\left(t\right)\right|\mathrm{d}t$.

> **Property 11.5.6 (Linearity of the Radon-Nikodym Derivative)**<br>If $\nu_{1},\nu_{2}\ll\mu$ and $a,b\in\mathbb R$, then $\frac{\mathrm{d}\left(a\nu_{1}+b\nu_{2}\right)}{\mathrm{d}\mu}=a\frac{\mathrm{d}\nu_{1}}{\mathrm{d}\mu}+b\frac{\mathrm{d}\nu_{2}}{\mathrm{d}\mu}$ holds $\mu$-a.e.

> **Corollary 13.4.5 (Monotone Functions Are Differentiable a.e.)**<br>Let $F$ be a right-continuous increasing function on $\mathbb R$. Then $F'\left(x\right)$ exists for almost every $x$.

> **Definition 14.0.6 (Functions of Bounded Variation)**<br>Let $f:\left[a,b\right]\to\mathbb R$. For any partition $P:a=x_{0}< x_{1}< \cdots< x_{n}=b$ of $\left[a,b\right]$, define the variation $V\left(f,P\right)=\sum_{i=1}^{n}\left|f\left(x_{i}\right)-f\left(x_{i-1}\right)\right|$. The total variation of $f$ on $\left[a,b\right]$ is $V_{a}^{b}\left(f\right)=\sup_{P}V\left(f,P\right)$. If $V_{a}^{b}\left(f\right)< +\infty$, $f$ is called a bounded-variation function, written $f\in BV\left(\left[a,b\right]\right)$.

> **Definition 15.0.11 (Absolute Continuity)**<br>A function $f:\left[a,b\right]\to\mathbb R$ is called absolutely continuous (written $f\in AC\left(\left[a,b\right]\right)$) if for every $\varepsilon> 0$ there exists $\delta> 0$ such that for any finite collection of disjoint subintervals $\left(a_{i},b_{i}\right)\subset\left[a,b\right]$, whenever $\sum_{i}\left(b_{i}-a_{i}\right)< \delta$, we have $\sum_{i}\left|f\left(b_{i}\right)-f\left(a_{i}\right)\right|< \varepsilon$.

> **Theorem 15.0.14 (Equivalent Characterization of Absolute Continuity)**<br>$f\in AC\left(\left[a,b\right]\right)$ if and only if there exists $g\in L^{1}\left(\left[a,b\right]\right)$ such that $f\left(x\right)=f\left(a\right)+\int_{a}^{x}g\left(t\right)\mathrm{d}t$ for all $x\in\left[a,b\right]$. In this case $f'\left(x\right)=g\left(x\right)$ a.e.

> **Theorem 15.0.16 (Inclusions Among Function Classes)**<br>The following strict inclusions hold: $C^{1}\left(\left[a,b\right]\right)\subset$ Lipschitz $\subset AC\left(\left[a,b\right]\right)\subset BV\left(\left[a,b\right]\right)\subset$ bounded functions.

---

## 1

Let $f:\left[a,b\right]\to\mathbb R$, and view the graph of $f$ as a subset of $\mathbb C$, namely $\left\{t+if\left(t\right):t\in\left[a,b\right]\right\}$. The length $L$ of the graph is defined as the supremum of the lengths of all inscribed polygons. (An inscribed polygon is the union of segments joining $t_{j-1}+if\left(t_{j-1}\right)$ to $t_{j}+if\left(t_{j}\right)$ for $1\le j\le n$, where $a=t_{0}< \cdots< t_{n}=b$.)

(a) Setting $F\left(t\right)=t+if\left(t\right)$, $L$ is the total variation of $F$ on $\left[a,b\right]$;

(b) If $f$ is absolutely continuous, then $L=\int_{a}^{b}\left[1+\left(f'\left(t\right)\right)^{2}\right]^{1/2}\mathrm{d}t$.

### Solution 1

**(a).** Set $F\left(t\right)=t+if\left(t\right)$. For a partition $a=t_{0}< \cdots< t_{n}=b$ of $\left[a,b\right]$, the distance between adjacent vertices $t_{j-1}+if\left(t_{j-1}\right)$ and $t_{j}+if\left(t_{j}\right)$ is

$$
\left|F\left(t_{j}\right)-F\left(t_{j-1}\right)\right|=\sqrt{\left(t_{j}-t_{j-1}\right)^{2}+\left(f\left(t_{j}\right)-f\left(t_{j-1}\right)\right)^{2}},
$$

so the length of the inscribed polygon is exactly $\sum_{j=1}^{n}\left|F\left(t_{j}\right)-F\left(t_{j-1}\right)\right|$. Hence $L$ equals the supremum of this sum over all partitions, which is precisely the total variation $V_{a}^{b}\left(F\right)$ of $F$ on $\left[a,b\right]$ (**Definition 14.0.6 (Functions of Bounded Variation)**).

**(b).** If $f\in AC\left(\left[a,b\right]\right)$ (**Definition 15.0.11 (Absolute Continuity)**), then both components of $F\left(t\right)=t+if\left(t\right)$, namely $t$ (the identity) and $f$, are absolutely continuous, so $F$ is absolutely continuous. By **Theorem 15.0.14 (Equivalent Characterization of Absolute Continuity)**, for almost every $t$, $F'\left(t\right)=\frac{\mathrm{d}}{\mathrm{d}t}\left(t+if\left(t\right)\right)=1+if'\left(t\right)$, and hence $\left|F'\left(t\right)\right|=\left(1+\left(f'\left(t\right)\right)^{2}\right)^{1/2}$. By **Basic Knowledge: Total Variation of an Absolutely Continuous Function**,

$$
L=V_{a}^{b}\left(F\right)=\int_{a}^{b}\left|F'\left(t\right)\right|\mathrm{d}t=\int_{a}^{b}\left[1+\left(f'\left(t\right)\right)^{2}\right]^{1/2}\mathrm{d}t.
$$

$\blacksquare$

---

## 2

If $\left\{F_{j}\right\}$ is a sequence of nonnegative increasing functions on $\left[a,b\right]$ and $F:=\sum_{j}F_{j}$ satisfies $F\left(x\right)< \infty$ for all $x\in\left[a,b\right]$, then $F'\left(x\right)=\sum_{j}F_{j}'\left(x\right)$ for almost every $x\in\left[a,b\right]$.

### Solution 2

Let $\mu_{F_{j}}$ be the Stieltjes measure associated with $F_{j}$, and $\mu_{F}$ that associated with $F=\sum_{j}F_{j}$ (**Basic Knowledge: NBV and Stieltjes Measures**). Since $\sum_{j}F_{j}$ converges and each term is nonnegative, by countable additivity of Stieltjes measures, $\mu_{F}=\sum_{j}\mu_{F_{j}}$. By **Corollary 13.4.5 (Monotone Functions Are Differentiable a.e.)** and the fact that the derivative of a monotone function is the Radon-Nikodym derivative of its Stieltjes measure with respect to Lebesgue measure, for $m$-a.e. $x$, $F_{j}'\left(x\right)=\frac{\mathrm{d}\mu_{F_{j}}}{\mathrm{d}m}\left(x\right)$; similarly $F'\left(x\right)=\frac{\mathrm{d}\mu_{F}}{\mathrm{d}m}\left(x\right)$. Hence by **Property 11.5.6 (Linearity of the Radon-Nikodym Derivative)** (adding two at a time),

$$
\frac{\mathrm{d}\mu_{F}}{\mathrm{d}m}\left(x\right)=\frac{\mathrm{d}\left(\sum_{j}\mu_{F_{j}}\right)}{\mathrm{d}m}\left(x\right)=\sum_{j}\frac{\mathrm{d}\mu_{F_{j}}}{\mathrm{d}m}\left(x\right)=\sum_{j}F_{j}'\left(x\right),
$$

for $m$-a.e. $x$. Thus $F'\left(x\right)=\sum_{j}F_{j}'\left(x\right)$ a.e. $\blacksquare$

---

## 3

A function $F:\left(a,b\right)\to\mathbb R$ ($-\infty\le a< b\le\infty$) is called convex if $F\left(\lambda s+\left(1-\lambda\right)t\right)\le\lambda F\left(s\right)+\left(1-\lambda\right)F\left(t\right)$ for all $s,t\in\left(a,b\right)$ and $\lambda\in\left(0,1\right)$.

(a) $F$ is convex iff for all $s,t,s',t'\in\left(a,b\right)$ with $s\le s'< t'$ and $s< t\le t'$: $\frac{F\left(t\right)-F\left(s\right)}{t-s}\le\frac{F\left(t'\right)-F\left(s'\right)}{t'-s'}$;

(b) $F$ is convex iff $F$ is absolutely continuous on every compact subinterval of $\left(a,b\right)$ and $F'$ is increasing (where defined);

(c) If $F$ is convex and $t_{0}\in\left(a,b\right)$, then there exists $\beta\in\mathbb R$ such that $F\left(t\right)-F\left(t_{0}\right)\ge\beta\left(t-t_{0}\right)$ for all $t\in\left(a,b\right)$;

(d) (Jensen's inequality) If $\left(X,\mathcal M,\mu\right)$ is a measure space with $\mu\left(X\right)=1$, $g:X\to\left(a,b\right)\in L^{1}\left(\mu\right)$, and $F$ is convex on $\left(a,b\right)$, then $F\left(\int g\,\mathrm{d}\mu\right)\le\int F\circ g\,\mathrm{d}\mu$.

### Solution 3

Write the difference quotient $S\left(u,v\right)=\frac{F\left(v\right)-F\left(u\right)}{v-u}$ ($u< v$).

**(a).** First prove $\Rightarrow$. Assume $F$ is convex. First establish two monotonicities of the difference quotient: fixing the left endpoint $s$, for $s< x_{1}< x_{2}$, convexity gives

$$
F\left(x_{1}\right)\le\frac{x_{2}-x_{1}}{x_{2}-s}F\left(s\right)+\frac{x_{1}-s}{x_{2}-s}F\left(x_{2}\right),
$$

which simplifies to $S\left(s,x_{1}\right)\le S\left(s,x_{2}\right)$, i.e. the difference quotient is increasing in the right endpoint; similarly fixing the right endpoint $t$, for $s_{1}< s_{2}< t$, convexity gives

$$
F\left(s_{2}\right)\le\frac{t-s_{2}}{t-s_{1}}F\left(s_{1}\right)+\frac{s_{2}-s_{1}}{t-s_{1}}F\left(t\right),
$$

which simplifies to $S\left(s_{2},t\right)\le S\left(s_{1},t\right)$, i.e. the difference quotient is decreasing in the left endpoint.

Now given $s\le s'< t'$ and $s< t\le t'$. By the right-endpoint monotonicity, $S\left(s,t\right)\le S\left(s,t'\right)$ (equality when $t=t'$); by the left-endpoint monotonicity, $S\left(s,t'\right)\ge S\left(s',t'\right)$ (equality when $s=s'$). Hence $S\left(s,t\right)\le S\left(s,t'\right)\le S\left(s',t'\right)$, i.e. $\frac{F\left(t\right)-F\left(s\right)}{t-s}\le\frac{F\left(t'\right)-F\left(s'\right)}{t'-s'}$.

Now prove $\Leftarrow$. Take any $s< t$, $\lambda\in\left(0,1\right)$, and set $u=\lambda s+\left(1-\lambda\right)t$; then $s< u< t$. Applying the inequality in (a) with $s'=u$, $t'=t$, which satisfies $s\le s'< t'$ and $s< t\le t'$, gives $\frac{F\left(u\right)-F\left(s\right)}{u-s}\le\frac{F\left(t\right)-F\left(u\right)}{t-u}$. Since $u=\lambda s+\left(1-\lambda\right)t$, we have $u-s=\lambda\left(t-s\right)$ and $t-u=\left(1-\lambda\right)\left(t-s\right)$. Substituting and simplifying gives $F\left(u\right)\le\lambda F\left(s\right)+\left(1-\lambda\right)F\left(t\right)$, i.e. $F$ is convex. This proves (a).

**(b).** First prove $\Rightarrow$. Assume $F$ is convex, and take a compact subinterval $\left[\alpha,\beta\right]\subset\left(a,b\right)$. By the difference-quotient monotonicity in (a), for $\alpha\le x< y\le\beta$, $S\left(\alpha,x\right)\le S\left(x,y\right)\le S\left(y,\beta\right)$ (slopes at three points increasing), while $S\left(\alpha,x\right)\ge S\left(\alpha,\beta\right)$ (right-endpoint monotonicity) and $S\left(y,\beta\right)\le S\left(\alpha,\beta\right)$ (left-endpoint monotonicity), so $\left|S\left(x,y\right)\right|\le S\left(\alpha,\beta\right)< \infty$. Hence $F$ satisfies a Lipschitz condition on $\left[\alpha,\beta\right]$ (Lipschitz constant $S\left(\alpha,\beta\right)$), and by **Theorem 15.0.16 (Inclusions Among Function Classes)**, $F\in AC\left(\left[\alpha,\beta\right]\right)$. Also $F'$ exists everywhere (convex function) and is the limit of difference quotients; by (a) the difference quotient is monotone in the left endpoint, so $F'$ is increasing.

Now prove $\Leftarrow$. Assume $F$ is absolutely continuous on every compact subinterval of $\left(a,b\right)$ and $F'$ is increasing. By **Theorem 15.0.14 (Equivalent Characterization of Absolute Continuity)**, for any $s< t\in\left(a,b\right)$ and intermediate point $u$, $F\left(u\right)-F\left(s\right)=\int_{s}^{u}F'$ and $F\left(t\right)-F\left(u\right)=\int_{u}^{t}F'$. Since $F'$ on $\left(s,u\right)$ is no larger than $F'$ on $\left(u,t\right)$, averaging gives $\frac{1}{u-s}\int_{s}^{u}F'\le\frac{1}{t-u}\int_{u}^{t}F'$, i.e. $S\left(s,u\right)\le S\left(u,t\right)$. Taking $u=\lambda s+\left(1-\lambda\right)t$ and simplifying (as in the $\Leftarrow$ part of (a)) gives $F\left(u\right)\le\lambda F\left(s\right)+\left(1-\lambda\right)F\left(t\right)$, i.e. $F$ is convex. This proves (b).

**(c).** By the difference-quotient monotonicity in (a), the left and right derivatives of $F$ at $t_{0}$ exist: the left derivative $F'_{-}\left(t_{0}\right)=\sup_{t< t_{0}}S\left(t,t_{0}\right)$ and the right derivative $F'_{+}\left(t_{0}\right)=\inf_{t> t_{0}}S\left(t_{0},t\right)$, with $F'_{-}\left(t_{0}\right)\le F'_{+}\left(t_{0}\right)$ (for $t_{1}< t_{0}< t_{2}$, three-point slopes $S\left(t_{1},t_{0}\right)\le S\left(t_{0},t_{2}\right)$). Take $\beta\in\left[F'_{-}\left(t_{0}\right),F'_{+}\left(t_{0}\right)\right]$. When $t> t_{0}$, $S\left(t_{0},t\right)\ge F'_{+}\left(t_{0}\right)\ge\beta$, so $F\left(t\right)-F\left(t_{0}\right)\ge\beta\left(t-t_{0}\right)$; when $t< t_{0}$, $S\left(t,t_{0}\right)\le F'_{-}\left(t_{0}\right)\le\beta$, and since $t-t_{0}< 0$, multiplying by the negative reverses the inequality, giving $F\left(t\right)-F\left(t_{0}\right)\ge\beta\left(t-t_{0}\right)$. Equality holds at $t=t_{0}$.

**(d).** Set $t_{0}=\int g\,\mathrm{d}\mu$. Since $g$ takes values in $\left(a,b\right)$ and $g\in L^{1}\left(\mu\right)$, we have $t_{0}\in\left(a,b\right)$. By (c), there exists $\beta\in\mathbb R$ such that $F\left(t\right)-F\left(t_{0}\right)\ge\beta\left(t-t_{0}\right)$ for all $t\in\left(a,b\right)$. Substituting $t=g\left(x\right)$ gives $F\left(g\left(x\right)\right)\ge F\left(t_{0}\right)+\beta\left(g\left(x\right)-t_{0}\right)$ for all $x\in X$. Integrating with respect to $\mu$ (the right side is in $L^{1}$, so the integral is well-defined):

$$
\int F\circ g\,\mathrm{d}\mu\ge\int\left[F\left(t_{0}\right)+\beta\left(g-t_{0}\right)\right]\mathrm{d}\mu=F\left(t_{0}\right)+\beta\left(\int g\,\mathrm{d}\mu-t_{0}\right)=F\left(t_{0}\right)=F\left(\int g\,\mathrm{d}\mu\right).
$$

Hence $F\left(\int g\,\mathrm{d}\mu\right)\le\int F\circ g\,\mathrm{d}\mu$. $\blacksquare$
