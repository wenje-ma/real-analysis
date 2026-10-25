# Assignment 11

> **Definition 14.0.6** (Functions of Bounded Variation)<br>Let $f:\left[a,b\right]\to\mathbb R$. For any partition $P:a=x_{0}< x_{1}< \cdots< x_{n}=b$ of $\left[a,b\right]$, define the variation $V\left(f,P\right)=\sum_{i=1}^{n}\left|f\left(x_{i}\right)-f\left(x_{i-1}\right)\right|$. The total variation of $f$ on $\left[a,b\right]$ is $V_{a}^{b}\left(f\right)=\sup_{P}V\left(f,P\right)$. If $V_{a}^{b}\left(f\right)< +\infty$, then $f$ is called a function of bounded variation on $\left[a,b\right]$, denoted $f\in BV\left(\left[a,b\right]\right)$.

> **Theorem 14.0.7** (Basic Properties)<br>Let $f,g\in BV\left(\left[a,b\right]\right)$. Then:
> (1) $BV\left(\left[a,b\right]\right)$ forms a linear space;
> 
> (2) $f$ is a bounded function;
> 
> (3) if $f$ satisfies a Lipschitz condition, then $f\in BV\left(\left[a,b\right]\right)$;
> 
> (4) every monotone function is a function of bounded variation.

> **Theorem 14.0.10** (Discontinuity-Point Properties)<br>If $f\in BV\left(\left[a,b\right]\right)$, then:
> (1) $f$ has at most countably many discontinuity points;
> 
> (2) all discontinuity points are jump discontinuities of the first kind.

> **Basic Knowledge** (Normalized Bounded Variation $NBV$)<br>$NBV=\left\{F\in BV:F\text{右连续},F\left(-\infty\right)=0\right\}$, where $BV$ denotes the functions of bounded variation on $\mathbb R$, and $T_{F}$ denotes the total variation function of $F$.

> **Basic Knowledge** (Series)<br>The geometric series $\sum_{n=1}^{\infty}2^{-n}=1$ converges; the harmonic series $\sum_{k}\frac{1}{k}$ diverges.

### Problem 1

**30.** Construct an increasing function on $\mathbb R$ whose set of discontinuity points is exactly $\mathbb Q$.

**31.** Let $F\left(x\right)=x^{2}\sin\left(x^{-1}\right)$, $G\left(x\right)=x^{2}\sin\left(x^{-2}\right)$ for $x\ne0$, and $F\left(0\right)=G\left(0\right)=0$.
a. $F$ and $G$ are differentiable everywhere (including at $x=0$);
b. $F\in BV\left(\left[-1,1\right]\right)$, but $G\notin BV\left(\left[-1,1\right]\right)$.

**32.** If $F_{1},F_{2},\dots,F\in NBV$ and $F_{j}\to F$ pointwise, then $T_{F}\le\liminf_{j\to\infty}T_{F_{j}}$.

### Solution to Problem 1

#### 30

Enumerate the rationals $\mathbb Q=\left\{q_{1},q_{2},\dots\right\}$, and define

$$
F\left(x\right)=\sum_{q_{n}\le x}2^{-n},\ x\in\mathbb R.
$$

This is a sum of at most countably many nonnegative terms, and its range lies in $\left[0,1\right]$. By the **Basic Knowledge** (Series), $\sum_{n}2^{-n}$ converges, so $F$ takes finite values. If $x< y$, then $\left\{n:q_{n}\le x\right\}\subset\left\{n:q_{n}\le y\right\}$, hence $F\left(x\right)\le F\left(y\right)$, i.e. $F$ is increasing.

**Every rational point is a discontinuity point.** For $q_{k}\in\mathbb Q$, as $x$ approaches $q_{k}$ from the left side of $q_{k}$, $\left\{q_{n}\le x\right\}$ does not contain $q_{k}$ (and tends to excluding $q_{k}$), so the left limit

$$
\begin{aligned}F\left(q_{k}-\right)&=\sum_{q_{n}< q_{k}}2^{-n}\\&=\sum_{q_{n}\le q_{k}}2^{-n}-2^{-k}\\&=F\left(q_{k}\right)-2^{-k}\\&< F\left(q_{k}\right).
\end{aligned}
$$

while the right limit $F\left(q_{k}+\right)=\lim_{x\downarrow q_{k}}F\left(x\right)=F\left(q_{k}\right)$ (since for $x> q_{k}$, $q_{k}$ is still counted). Hence $F$ has unequal left and right limits at $q_{k}$, which is a jump discontinuity of the first kind.

**Every irrational point is a continuity point.** Let $x_{0}\in\mathbb R\setminus\mathbb Q$. Given $\varepsilon> 0$, by the **Basic Knowledge** (Series), choose $N$ such that $\sum_{n> N}2^{-n}< \varepsilon$. Since $x_{0}$ is irrational, choose $\delta> 0$ small enough that the open interval $\left(x_{0}-\delta,x_{0}+\delta\right)$ contains none of $q_{1},\dots,q_{N}$ (finitely many points, which can be separated). Then when $\left|x-x_{0}\right|< \delta$, the interval $\left(\min\left(x,x_{0}\right),\max\left(x,x_{0}\right)\right]$ contains at most $q_{N+1},q_{N+2},\dots$, so

$$
\begin{aligned}\left|F\left(x\right)-F\left(x_{0}\right)\right|\\
&=\sum_{x_{0}< q_{n}\le x\text{ 或 }x< q_{n}\le x_{0}}2^{-n}\\&\le\sum_{n> N}2^{-n}< \varepsilon.
\end{aligned}
$$

Hence $F$ is continuous at $x_{0}$.

In summary, the set of discontinuity points of $F$ is exactly $\mathbb Q$. By **Theorem 14.0.7**(4) and **Theorem 14.0.10**, $F$ is an increasing bounded function and hence of bounded variation; its discontinuity points are at most countable and all of the first kind, which here are exactly $\mathbb Q$. $\blacksquare$

#### 31

**(a)** For $x\ne0$, differentiating directly gives

$$
\begin{aligned}F'\left(x\right)&=2x\sin\left(x^{-1}\right)-\cos\left(x^{-1}\right),\\G'\left(x\right)&=2x\sin\left(x^{-2}\right)-\frac{2}{x}\cos\left(x^{-2}\right).
\end{aligned}
$$

At $x=0$, check by definition:

$$
\begin{aligned}F'\left(0\right)&=\lim_{h\to0}\frac{F\left(h\right)-F\left(0\right)}{h}&=\lim_{h\to0}\frac{h^{2}\sin\left(h^{-1}\right)}{h}\\&=\lim_{h\to0}h\sin\left(h^{-1}\right)\\&=0,
\end{aligned}
$$

where the last equality follows from $\left|h\sin\left(h^{-1}\right)\right|\le\left|h\right|\to0$; similarly,

$$
\begin{aligned}G'\left(0\right)&=\lim_{h\to0}\frac{h^{2}\sin\left(h^{-2}\right)}{h}\\&=\lim_{h\to0}h\sin\left(h^{-2}\right)\\&=0.
\end{aligned}
$$

Hence $F,G$ are differentiable everywhere on $\mathbb R$ (including at $x=0$). $\blacksquare$

**(b)** We first prove $F\in BV\left(\left[-1,1\right]\right)$. By (a), for $x\ne0$, $\left|F'\left(x\right)\right|=\left|2x\sin\left(x^{-1}\right)-\cos\left(x^{-1}\right)\right|\le2\left|x\right|+1\le3$. Hence $F'$ is bounded on $\left[-1,1\right]$. By the mean value theorem, $\left|F\left(x\right)-F\left(y\right)\right|\le3\left|x-y\right|$, i.e. $F$ satisfies a Lipschitz condition; by **Theorem 14.0.7**(3), $F\in BV\left(\left[-1,1\right]\right)$.

We next prove $G\notin BV\left(\left[-1,1\right]\right)$. Take $x_{k}=\frac{1}{\sqrt{\pi/2+k\pi}}$ ($k=0,1,2,\dots$); then $x_{k}\downarrow0$, and $\sin\left(x_{k}^{-2}\right)=\sin\left(\pi/2+k\pi\right)=\left(-1\right)^{k}$, so $G\left(x_{k}\right)=\left(-1\right)^{k}x_{k}^{2}$. For the partition $0< x_{N}< \cdots< x_{0}$ (together with the endpoint $0$), by the alternating signs,

$$
\begin{aligned}\sum_{k=0}^{N-1}\left|G\left(x_{k}\right)-G\left(x_{k+1}\right)\right|&=\sum_{k=0}^{N-1}\left(x_{k}^{2}+x_{k+1}^{2}\right)\\&\ge\sum_{k=0}^{N-1}x_{k}^{2}\\&=\sum_{k=0}^{N-1}\frac{1}{\pi/2+k\pi}.
\end{aligned}
$$

By the **Basic Knowledge** (Series), the harmonic series $\sum_{k}\frac{1}{k}$ diverges, so the above tends to $+\infty$ as $N\to\infty$. Thus the total variation of $G$ on $\left[0,1\right]\subset\left[-1,1\right]$ is already $+\infty$, and hence $V_{-1}^{1}\left(G\right)=+\infty$, i.e. $G\notin BV\left(\left[-1,1\right]\right)$. $\blacksquare$

#### 32

Fix $x\in\mathbb R$ and a partition $a=t_{0}< \cdots< t_{n}=x$ (take $-\infty< a$). Since $F_{j}\to F$ pointwise, and limits over finitely many terms may be interchanged (the sum is a finite sum),

$$
\begin{aligned}\sum_{k=1}^{n}\left|F\left(t_{k}\right)-F\left(t_{k-1}\right)\right|&=\lim_{j\to\infty}\sum_{k=1}^{n}\left|F_{j}\left(t_{k}\right)-F_{j}\left(t_{k-1}\right)\right|\\&=\liminf_{j\to\infty}\sum_{k=1}^{n}\left|F_{j}\left(t_{k}\right)-F_{j}\left(t_{k-1}\right)\right|\\&\le\liminf_{j\to\infty}T_{F_{j}}\left(x\right),
\end{aligned}
$$

where the last inequality follows from **Definition 14.0.6** (the sum over any partition is at most the total variation $T_{F_{j}}\left(x\right)$, and $\liminf$ preserves the inequality). Taking the supremum over all partitions,

$$
\begin{aligned}T_{F}\left(x\right)&=\sup_{P}\sum_{k=1}^{n}\left|F\left(t_{k}\right)-F\left(t_{k-1}\right)\right|\\&\le\liminf_{j\to\infty}T_{F_{j}}\left(x\right).
\end{aligned}
$$

Hence $T_{F}\le\liminf_{j\to\infty}T_{F_{j}}$. $\blacksquare$
