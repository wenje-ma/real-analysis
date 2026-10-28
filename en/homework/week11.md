# week11

> **Basic Knowledge: Normalized Bounded Variation ($NBV$)**<br>$NBV=\left\{F\in BV:F\text{ right-continuous},F\left(-\infty\right)=0\right\}$, where $BV$ denotes the bounded-variation functions on $\mathbb R$, and $T_{F}$ is the total-variation function of $F$.

> **Basic Knowledge: Series**<br>The geometric series $\sum_{n=1}^{\infty}2^{-n}=1$ converges; the harmonic series $\sum_{k}\frac{1}{k}$ diverges.

> **Definition 14.0.6 (Functions of Bounded Variation)**<br>Let $f:\left[a,b\right]\to\mathbb R$. For any partition $P:a=x_{0}< x_{1}< \cdots< x_{n}=b$ of $\left[a,b\right]$, define the variation $V\left(f,P\right)=\sum_{i=1}^{n}\left|f\left(x_{i}\right)-f\left(x_{i-1}\right)\right|$. The total variation of $f$ on $\left[a,b\right]$ is $V_{a}^{b}\left(f\right)=\sup_{P}V\left(f,P\right)$. If $V_{a}^{b}\left(f\right)< +\infty$, $f$ is called a bounded-variation function on $\left[a,b\right]$, written $f\in BV\left(\left[a,b\right]\right)$.

> **Theorem 14.0.7 (Basic Properties of Bounded-Variation Functions)**<br>Let $f,g\in BV\left(\left[a,b\right]\right)$. Then: (1) $BV\left(\left[a,b\right]\right)$ is a linear space; (2) $f$ is bounded; (3) if $f$ satisfies a Lipschitz condition, then $f\in BV\left(\left[a,b\right]\right)$; (4) a monotone function is always of bounded variation.

> **Theorem 14.0.10 (Discontinuity Properties of Bounded-Variation Functions)**<br>If $f\in BV\left(\left[a,b\right]\right)$, then: (1) $f$ has at most countably many discontinuities; (2) all discontinuities are jump discontinuities.

---

## 1

Construct an increasing function on $\mathbb R$ whose set of discontinuities is exactly $\mathbb Q$.

### Solution 1

Enumerate the rationals $\mathbb Q=\left\{q_{1},q_{2},\dots\right\}$ and define $F\left(x\right)=\sum_{q_{n}\le x}2^{-n}$ for $x\in\mathbb R$. This is a sum of at most countably many nonnegative terms, with values in $\left[0,1\right]$. By **Basic Knowledge: Series**, $\sum_{n}2^{-n}$ converges, so $F$ takes finite values. If $x< y$, then $\left\{n:q_{n}\le x\right\}\subset\left\{n:q_{n}\le y\right\}$, so $F\left(x\right)\le F\left(y\right)$; hence $F$ is increasing.

**Every rational point is a discontinuity.** For $q_{k}\in\mathbb Q$, as $x$ approaches $q_{k}$ from the left, $\left\{q_{n}\le x\right\}$ does not contain $q_{k}$, so the left limit $F\left(q_{k}-\right)=\sum_{q_{n}< q_{k}}2^{-n}=\sum_{q_{n}\le q_{k}}2^{-n}-2^{-k}=F\left(q_{k}\right)-2^{-k}< F\left(q_{k}\right)$. The right limit $F\left(q_{k}+\right)=\lim_{x\downarrow q_{k}}F\left(x\right)=F\left(q_{k}\right)$ (since for $x> q_{k}$, $q_{k}$ is still counted). Thus $F$ has unequal left and right limits at $q_{k}$, a jump discontinuity.

**Every irrational point is a continuity point.** Let $x_{0}\in\mathbb R\setminus\mathbb Q$. Given $\varepsilon> 0$, by **Basic Knowledge: Series** choose $N$ with $\sum_{n> N}2^{-n}< \varepsilon$. Since $x_{0}$ is irrational, choose $\delta> 0$ small enough that $\left(x_{0}-\delta,x_{0}+\delta\right)$ contains none of $q_{1},\dots,q_{N}$ (finitely many points, separable). Then whenever $\left|x-x_{0}\right|< \delta$, the interval $\left(\min\left(x,x_{0}\right),\max\left(x,x_{0}\right)\right]$ contains at most $q_{N+1},q_{N+2},\dots$, so $\left|F\left(x\right)-F\left(x_{0}\right)\right|=\sum_{x_{0}< q_{n}\le x\text{ or }x< q_{n}\le x_{0}}2^{-n}\le\sum_{n> N}2^{-n}< \varepsilon$. Hence $F$ is continuous at $x_{0}$.

Thus the discontinuity set of $F$ is exactly $\mathbb Q$. By **Theorem 14.0.7 (Basic Properties of Bounded-Variation Functions)** (4) and **Theorem 14.0.10 (Discontinuity Properties of Bounded-Variation Functions)**, $F$ is an increasing bounded function, hence of bounded variation, with at most countably many jump discontinuities, which here are exactly $\mathbb Q$. $\blacksquare$

---

## 2

Let $F\left(x\right)=x^{2}\sin\left(x^{-1}\right)$ and $G\left(x\right)=x^{2}\sin\left(x^{-2}\right)$ for $x\ne0$, with $F\left(0\right)=G\left(0\right)=0$.

(a) $F$ and $G$ are differentiable everywhere (including $x=0$);

(b) $F\in BV\left(\left[-1,1\right]\right)$, but $G\notin BV\left(\left[-1,1\right]\right)$.

### Solution 2

**(a).** For $x\ne0$, direct differentiation gives $F'\left(x\right)=2x\sin\left(x^{-1}\right)-\cos\left(x^{-1}\right)$ and $G'\left(x\right)=2x\sin\left(x^{-2}\right)-\frac{2}{x}\cos\left(x^{-2}\right)$. At $x=0$, use the definition:

$$
F'\left(0\right)=\lim_{h\to0}\frac{F\left(h\right)-F\left(0\right)}{h}=\lim_{h\to0}\frac{h^{2}\sin\left(h^{-1}\right)}{h}=\lim_{h\to0}h\sin\left(h^{-1}\right)=0,
$$

where the last equality uses $\left|h\sin\left(h^{-1}\right)\right|\le\left|h\right|\to0$; similarly $G'\left(0\right)=\lim_{h\to0}\frac{h^{2}\sin\left(h^{-2}\right)}{h}=\lim_{h\to0}h\sin\left(h^{-2}\right)=0$. Hence $F,G$ are differentiable on all of $\mathbb R$ (including $x=0$).

**(b).** First show $F\in BV\left(\left[-1,1\right]\right)$. By (a), for $x\ne0$, $\left|F'\left(x\right)\right|=\left|2x\sin\left(x^{-1}\right)-\cos\left(x^{-1}\right)\right|\le2\left|x\right|+1\le3$. Thus $F'$ is bounded on $\left[-1,1\right]$. By the mean value theorem, $\left|F\left(x\right)-F\left(y\right)\right|\le3\left|x-y\right|$, i.e. $F$ satisfies a Lipschitz condition, and by **Theorem 14.0.7 (Basic Properties of Bounded-Variation Functions)** (3), $F\in BV\left(\left[-1,1\right]\right)$.

Now show $G\notin BV\left(\left[-1,1\right]\right)$. Take $x_{k}=\frac{1}{\sqrt{\pi/2+k\pi}}$ ($k=0,1,2,\dots$); then $x_{k}\downarrow0$ and $\sin\left(x_{k}^{-2}\right)=\sin\left(\pi/2+k\pi\right)=\left(-1\right)^{k}$, so $G\left(x_{k}\right)=\left(-1\right)^{k}x_{k}^{2}$. For the partition $0< x_{N}< \cdots< x_{0}$ (and the endpoint $0$), by the alternating signs,

$$
\sum_{k=0}^{N-1}\left|G\left(x_{k}\right)-G\left(x_{k+1}\right)\right|=\sum_{k=0}^{N-1}\left(x_{k}^{2}+x_{k+1}^{2}\right)\ge\sum_{k=0}^{N-1}x_{k}^{2}=\sum_{k=0}^{N-1}\frac{1}{\pi/2+k\pi}.
$$

By **Basic Knowledge: Series**, the harmonic series $\sum_{k}\frac{1}{k}$ diverges, so the above tends to $+\infty$ as $N\to\infty$. Thus the total variation of $G$ on $\left[0,1\right]\subset\left[-1,1\right]$ is already $+\infty$, so $V_{-1}^{1}\left(G\right)=+\infty$, i.e. $G\notin BV\left(\left[-1,1\right]\right)$. $\blacksquare$

---

## 3

If $F_{1},F_{2},\dots,F\in NBV$ and $F_{j}\to F$ pointwise, then $T_{F}\le\liminf_{j\to\infty}T_{F_{j}}$.

### Solution 3

Fix $x\in\mathbb R$ and a partition $a=t_{0}< \cdots< t_{n}=x$ (with $-\infty< a$). Since $F_{j}\to F$ pointwise, limits exchange over the finite sum,

$$
\sum_{k=1}^{n}\left|F\left(t_{k}\right)-F\left(t_{k-1}\right)\right|=\lim_{j\to\infty}\sum_{k=1}^{n}\left|F_{j}\left(t_{k}\right)-F_{j}\left(t_{k-1}\right)\right|=\liminf_{j\to\infty}\sum_{k=1}^{n}\left|F_{j}\left(t_{k}\right)-F_{j}\left(t_{k-1}\right)\right|\le\liminf_{j\to\infty}T_{F_{j}}\left(x\right),
$$

where the last inequality uses **Definition 14.0.6 (Functions of Bounded Variation)** (the sum over any partition does not exceed the total variation $T_{F_{j}}\left(x\right)$, and $\liminf$ preserves inequalities). Taking the supremum over all partitions,

$$
T_{F}\left(x\right)=\sup_{P}\sum_{k=1}^{n}\left|F\left(t_{k}\right)-F\left(t_{k-1}\right)\right|\le\liminf_{j\to\infty}T_{F_{j}}\left(x\right).
$$

Hence $T_{F}\le\liminf_{j\to\infty}T_{F_{j}}$. $\blacksquare$
