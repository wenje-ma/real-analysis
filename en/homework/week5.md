# Assignment 5

> **Definition 5.1.2** (Measure)<br>Let $\left(X,\mathcal F\right)$ be a measurable space. A function $\mu:\mathcal F\to\left[0,+\infty\right]$ is called a **measure** on $\left(X,\mathcal F\right)$ if it satisfies:
> (1) nonnegativity: $\mu\left(E\right)\ge0$ for all $E\in\mathcal F$;
>
> (2) the empty set has measure zero: $\mu\left(\emptyset\right)=0$;
>
> (3) countable additivity ($\sigma$-additivity): for any countably many pairwise disjoint sets $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$, we have $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **Definition 5.1.5** ($\sigma$-Finite Measure)<br>Let $\left(X,\mathcal F,\mu\right)$ be a measure space. If there exists a sequence of measurable sets $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$ such that $X=\bigcup_{n=1}^{\infty}E_{n}$ and $\mu\left(E_{n}\right)<+\infty$ for all $n\in\mathbb N$, then $\mu$ is called a $\sigma$-finite measure.

> **Definition 8.1.1** (Integral of a Nonnegative Simple Function)<br>Let $f=\sum_{i=1}^{n}c_{i}\chi_{A_{i}}$ be a nonnegative simple function, where $c_{i}\ge0$, the $A_{i}\in\mathcal F$ are pairwise disjoint, and $\bigcup_{i}A_{i}=X$. The integral of $f$ with respect to $\mu$ is defined as $\int_{X}f\,\mathrm{d}\mu=\sum_{i=1}^{n}c_{i}\mu\left(A_{i}\right)$, with the convention $0\cdot\infty=0$.

> **Proposition 8.1.2** (Linearity)<br>Let $f,g$ be nonnegative simple functions and $\alpha,\beta\ge0$. Then $\int_{X}\left(\alpha f+\beta g\right)\mathrm{d}\mu=\alpha\int_{X}f\,\mathrm{d}\mu+\beta\int_{X}g\,\mathrm{d}\mu$.

> **Definition 8.2.1** (Integral of a Nonnegative Measurable Function)<br>Let $f:X\to\left[0,+\infty\right]$ be a nonnegative measurable function. The integral of $f$ with respect to $\mu$ is defined as $\int_{X}f\,\mathrm{d}\mu=\sup\left\{\int_{X}\phi\,\mathrm{d}\mu:\phi\text{是简单函数},0\le\phi\le f\right\}$. If $\int_{X}f\,\mathrm{d}\mu<\infty$, then $f$ is called integrable.

> **Theorem 8.2.2** (Monotone Convergence Theorem)<br>Let $\left(X,\mathcal F,\mu\right)$ be a measure space and $\left\{f_{n}\right\}$ a sequence of nonnegative measurable functions satisfying $0\le f_{1}\left(x\right)\le f_{2}\left(x\right)\le\cdots$ for all $x\in X$, and $f_{n}\to f$ pointwise. Then $\lim_{n\to\infty}\int_{X}f_{n}\,\mathrm{d}\mu=\int_{X}f\,\mathrm{d}\mu$.

> **Remark 8.2.3**<br>The monotone convergence theorem tells us that the integral can be approximated by simple functions.

> **Proposition 8.2.4** (Absolute Continuity)<br>Let $f$ be a nonnegative measurable function. Then $A\mapsto\int_{A}f\,\mathrm{d}\mu$ is a measure; and if $\mu\left(A\right)=0$, then $\int_{A}f\,\mathrm{d}\mu=0$.

> **Definition 8.2.5** (Integral of a General Measurable Function)<br>Let $f:X\to\left[-\infty,+\infty\right]$ be a measurable function. The positive and negative parts of $f$ are defined by $f^{+}\left(x\right)=\max\left\{f\left(x\right),0\right\}$ and $f^{-}\left(x\right)=\max\left\{-f\left(x\right),0\right\}$. If at least one of the integrals $\int_{X}f^{+}\mathrm{d}\mu$, $\int_{X}f^{-}\mathrm{d}\mu$ is finite, the integral of $f$ is defined as $\int_{X}f\,\mathrm{d}\mu=\int_{X}f^{+}\mathrm{d}\mu-\int_{X}f^{-}\mathrm{d}\mu$. If $\int_{X}f^{+}\mathrm{d}\mu<\infty$ and $\int_{X}f^{-}\mathrm{d}\mu<\infty$, then $f$ is called integrable.

> **Theorem 8.2.7** (Fatou's Lemma)<br>Let $\left(X,\mathcal F,\mu\right)$ be a measure space and $\left\{f_{n}\right\}$ a sequence of nonnegative measurable functions. Then $\int_{X}\liminf_{n\to\infty}f_{n}\,\mathrm{d}\mu\le\liminf_{n\to\infty}\int_{X}f_{n}\,\mathrm{d}\mu$.

> **Theorem 8.2.9** (Dominated Convergence Theorem)<br>Let $\left(X,\mathcal F,\mu\right)$ be a measure space, $\left\{f_{n}\right\}$ a sequence of measurable functions, and $f_{n}\to f$ almost everywhere. If there exists an integrable function $g$ such that $\left|f_{n}\right|\le g$ almost everywhere for all $n$, then $\lim_{n\to\infty}\int_{X}f_{n}\,\mathrm{d}\mu=\int_{X}f\,\mathrm{d}\mu$.

> **Lemma 8.2.13** (Termwise Integration of a Series)<br>Let $\left\{f_{n}\right\}$ be a sequence of measurable functions with $\sum_{n=1}^{\infty}\int_{X}\left|f_{n}\right|\mathrm{d}\mu<\infty$. Then $\int_{X}\left(\sum_{n=1}^{\infty}f_{n}\right)\mathrm{d}\mu=\sum_{n=1}^{\infty}\int_{X}f_{n}\,\mathrm{d}\mu$.

> **Theorem 8.2.17** (Integration with a Parameter)<br>Let $f:X\times\left[a,b\right]\to\mathbb R$, and suppose that for each $t\in\left[a,b\right]$, the function $f\left(\cdot,t\right):X\to\mathbb R$ is integrable. Set $F\left(t\right)=\int_{X}f\left(x,t\right)\mathrm{d}\mu\left(x\right)$.
> (a) if there exists $g\in L^{1}\left(\mu\right)$ such that $\left|f\left(x,t\right)\right|\le g\left(x\right)$ for all $x,t$, and for each $x$, $\lim_{t\to t_{0}}f\left(x,t\right)=f\left(x,t_{0}\right)$, then $\lim_{t\to t_{0}}F\left(t\right)=F\left(t_{0}\right)$;
>
> (b) if the partial derivative $\partial f/\partial t$ exists and there exists $g\in L^{1}\left(\mu\right)$ such that $\left|\frac{\partial f}{\partial t}\left(x,t\right)\right|\le g\left(x\right)$ for all $x,t$, then $F$ is differentiable and $F'\left(t\right)=\int\frac{\partial f}{\partial t}\left(x,t\right)\mathrm{d}\mu\left(x\right)$.

> **Basic Knowledge**<br>**If a nonnegative integrable function has integral zero, it vanishes almost everywhere**: let $h\ge0$ be measurable with $\int_{X}h\,\mathrm{d}\mu=0$. Then $h=0$ almost everywhere. Indeed, $\left\{h>0\right\}=\bigcup_{n=1}^{\infty}\left\{h>\frac{1}{n}\right\}$, and $\int h\ge\frac{1}{n}\mu\left(\left\{h>\frac{1}{n}\right\}\right)$, so $\mu\left(\left\{h>\frac{1}{n}\right\}\right)=0$ for all $n$.

> **Basic Knowledge**<br>**The Riemann integral and Darboux sums**: let $f$ be a bounded real-valued function on $\left[a,b\right]$. For a partition $P=\left\{t_{0}<\cdots<t_{n}\right\}$ of $\left[a,b\right]$, set $M_{i}=\sup_{\left[t_{i-1},t_{i}\right]}f$ and $m_{i}=\inf_{\left[t_{i-1},t_{i}\right]}f$; the upper Darboux sum is $\overline S\left(P\right)=\sum_{i}M_{i}\left(t_{i}-t_{i-1}\right)$ and the lower Darboux sum is $\underline S\left(P\right)=\sum_{i}m_{i}\left(t_{i}-t_{i-1}\right)$. The upper integral is $\overline{\int}f=\inf_{P}\overline S\left(P\right)$ and the lower integral is $\underline{\int}f=\sup_{P}\underline S\left(P\right)$. If $\overline{\int}f=\underline{\int}f$, their common value is called the Riemann integral of $f$, and in that case $f$ is called Riemann integrable.

### Problem 1

Let $f$ be a nonnegative simple function. Prove the following: $A\mapsto\int_{A}f\,\mathrm{d}\mu$ is a measure; and if $\mu\left(A\right)=0$, then $\int_{A}f\,\mathrm{d}\mu=0$.

### Solution to Problem 1

Let $f=\sum_{i=1}^{n}c_{i}\chi_{A_{i}}$, where $c_{i}\ge0$, the $A_{i}\in\mathcal F$ are pairwise disjoint, and $\bigcup_{i}A_{i}=X$. For $E\in\mathcal F$, by **Definition 8.1.1**,

$$
\begin{aligned}\int_{E}f\,\mathrm{d}\mu&=\int f\chi_{E}\,\mathrm{d}\mu\\&=\sum_{i=1}^{n}c_{i}\mu\left(E\cap A_{i}\right).
\end{aligned}
$$

Set $\lambda\left(E\right):=\int_{E}f\,\mathrm{d}\mu$. We verify that $\lambda$ is a measure:

- $\lambda\left(\emptyset\right)=\sum_{i=1}^{n}c_{i}\mu\left(\emptyset\cap A_{i}\right)=0$;
- nonnegativity is clear, since $c_{i}\ge0$ and $\mu\ge0$;
- $\sigma$-additivity: let $E=\bigsqcup_{j=1}^{\infty}E_{j}$ (pairwise disjoint). By the $\sigma$-additivity of $\mu$ (**Definition 5.1.2**) and **Proposition 8.1.2** (Linearity),

$$
\begin{aligned}\lambda\left(E\right)&=\sum_{i=1}^{n}c_{i}\mu\left(E\cap A_{i}\right)\\&=\sum_{i=1}^{n}c_{i}\sum_{j=1}^{\infty}\mu\left(E_{j}\cap A_{i}\right)\\&=\sum_{j=1}^{\infty}\sum_{i=1}^{n}c_{i}\mu\left(E_{j}\cap A_{i}\right)\\&=\sum_{j=1}^{\infty}\lambda\left(E_{j}\right).
\end{aligned}
$$

Hence $\lambda$ is a measure on $\mathcal F$. Finally, if $\mu\left(A\right)=0$, then

$$
\begin{aligned}\lambda\left(A\right)&=\sum_{i=1}^{n}c_{i}\mu\left(A\cap A_{i}\right)\\&\le\sum_{i=1}^{n}c_{i}\mu\left(A\right)\\&=0,
\end{aligned}
$$

hence $\lambda\left(A\right)=0$. $\blacksquare$

### Problem 2

Let $f,g$ be integrable functions and $a,b\in\mathbb R$. Prove the following properties:

1. Linearity: $\int_{X}\left(af+bg\right)\mathrm{d}\mu=a\int_{X}f\,\mathrm{d}\mu+b\int_{X}g\,\mathrm{d}\mu$;
2. Monotonicity: if $f\le g$ almost everywhere, then $\int_{X}f\,\mathrm{d}\mu\le\int_{X}g\,\mathrm{d}\mu$;
3. Triangle inequality: $\left|\int_{X}f\,\mathrm{d}\mu\right|\le\int_{X}\left|f\right|\mathrm{d}\mu$;
4. If $f=g$ almost everywhere, then $\int_{X}f\,\mathrm{d}\mu=\int_{X}g\,\mathrm{d}\mu$.

### Solution to Problem 2

We first establish linearity of the integral for nonnegative measurable functions. Let $\phi,\psi$ be nonnegative measurable functions and $\alpha,\beta\ge0$. By **Remark 8.2.3**, there exist simple functions $\phi_{k}\uparrow\phi$, $\psi_{k}\uparrow\psi$. By **Proposition 8.1.2** (linearity for simple functions),

$$
\int\left(\alpha\phi_{k}+\beta\psi_{k}\right)\mathrm{d}\mu=\alpha\int\phi_{k}\,\mathrm{d}\mu+\beta\int\psi_{k}\,\mathrm{d}\mu.
$$

Since $\alpha\phi_{k}+\beta\psi_{k}\uparrow\alpha\phi+\beta\psi$, taking limits on both sides by **Theorem 8.2.2** (Monotone Convergence Theorem) gives

$$
\int\left(\alpha\phi+\beta\psi\right)\mathrm{d}\mu=\alpha\int\phi\,\mathrm{d}\mu+\beta\int\psi\,\mathrm{d}\mu.
$$

Now let $f,g$ be integrable, and let $f^{+},f^{-}$ denote their positive and negative parts (**Definition 8.2.5**).

1. First, scalar multiplication: if $a\ge0$, then $\left(af\right)^{+}=af^{+}$ and $\left(af\right)^{-}=af^{-}$, so $\int\left(af\right)\mathrm{d}\mu=a\int f^{+}\mathrm{d}\mu-a\int f^{-}\mathrm{d}\mu=a\int f\,\mathrm{d}\mu$; if $a<0$, then $\left(af\right)^{+}=\left|a\right|f^{-}$ and $\left(af\right)^{-}=\left|a\right|f^{+}$, and similarly $\int\left(af\right)\mathrm{d}\mu=a\int f\,\mathrm{d}\mu$; the case $a=0$ is trivial. For addition, decompose using the positive and negative parts as $f+g=\left(f^{++}g^{+}\right)-\left(f^{-}+g^{-}\right)$, i.e.

$$
\left(f+g\right)^{+}+f^{-}+g^{-}=\left(f+g\right)^{-}+f^{+}+g^{+},
$$

Both sides are nonnegative measurable functions, and integrating by the nonnegative linearity gives

$$
\int\left(f+g\right)^{+}\mathrm{d}\mu+\int f^{-}\mathrm{d}\mu+\int g^{-}\mathrm{d}\mu=\int\left(f+g\right)^{-}\mathrm{d}\mu+\int f^{+}\mathrm{d}\mu+\int g^{+}\mathrm{d}\mu,
$$

Rearranging (all terms are finite, since $f,g$ are integrable) gives $\int\left(f+g\right)\mathrm{d}\mu=\int f\,\mathrm{d}\mu+\int g\,\mathrm{d}\mu$. Combining the two gives $\int\left(af+bg\right)\mathrm{d}\mu=a\int f\,\mathrm{d}\mu+b\int g\,\mathrm{d}\mu$.

2. By linearity, $\int g\,\mathrm{d}\mu-\int f\,\mathrm{d}\mu=\int\left(g-f\right)\mathrm{d}\mu$. Since $f\le g$ almost everywhere, $g-f\ge0$ almost everywhere. By **Definition 8.2.1**, the integral of a nonnegative measurable function is nonnegative (it is the supremum of integrals of nonnegative simple functions), so $\int\left(g-f\right)\mathrm{d}\mu\ge0$, i.e. $\int f\,\mathrm{d}\mu\le\int g\,\mathrm{d}\mu$.

3. Since $\left|f\right|=f^{+}+f^{-}$, nonnegative linearity gives $\int\left|f\right|\mathrm{d}\mu=\int f^{+}\mathrm{d}\mu+\int f^{-}\mathrm{d}\mu$. And since $\int f\,\mathrm{d}\mu=\int f^{+}\mathrm{d}\mu-\int f^{-}\mathrm{d}\mu$, we have

$$
\begin{aligned}\left|\int f\,\mathrm{d}\mu\right|&=\left|\int f^{+}\mathrm{d}\mu-\int f^{-}\mathrm{d}\mu\right|\\&\le\int f^{+}\mathrm{d}\mu+\int f^{-}\mathrm{d}\mu\\&=\int\left|f\right|\mathrm{d}\mu.
\end{aligned}
$$

4. If $f=g$ almost everywhere, then $f^{+}=g^{+}$ and $f^{-}=g^{-}$ almost everywhere. Then $h:=f^{+}-g^{+}$ is integrable and $h=0$ almost everywhere, and both its positive part $h^{+}$ and negative part $h^{-}$ vanish outside a set of measure zero. By **Proposition 8.2.4** (Absolute Continuity), $\int h^{+}\mathrm{d}\mu=\int_{\left\{h>0\right\}}h^{+}\mathrm{d}\mu=0$ and $\int h^{-}\mathrm{d}\mu=0$, so $\int h\,\mathrm{d}\mu=0$, i.e. $\int f^{+}\mathrm{d}\mu=\int g^{+}\mathrm{d}\mu$; similarly $\int f^{-}\mathrm{d}\mu=\int g^{-}\mathrm{d}\mu$. Therefore $\int f\,\mathrm{d}\mu=\int g\,\mathrm{d}\mu$. $\blacksquare$

### Problem 3

Let $f\in L^{1}$. Prove the following:

(a) the set $\left\{x:f\left(x\right)\ne0\right\}$ is $\sigma$-finite;
(b) for $f,g\in L^{1}$, $\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\mu$ for every measurable set $E$, if and only if $\int\left|f-g\right|\mathrm{d}\mu=0$, if and only if $f=g$ $\mu$-almost everywhere.

### Solution to Problem 3

(a) By **Definition 8.2.5**, $f=f^{+}-f^{-}$, so $\left\{x:f\left(x\right)\ne0\right\}=\left\{x:f^{+}\left(x\right)>0\right\}\cup\left\{x:f^{-}\left(x\right)>0\right\}$. Moreover,

$$
\left\{x:f^{+}\left(x\right)>0\right\}=\bigcup_{n=1}^{\infty}\left\{x:f^{+}\left(x\right)>\frac{1}{n}\right\},
$$

and by **Definition 8.2.1** (the nonnegative integral is a supremum),

$$
\int_{X}f^{+}\mathrm{d}\mu\ge\int_{\left\{f^{+}>\frac{1}{n}\right\}}f^{+}\mathrm{d}\mu\ge\frac{1}{n}\mu\left(\left\{x:f^{+}\left(x\right)>\frac{1}{n}\right\}\right).
$$

Since $f$ is integrable, $\int f^{+}\mathrm{d}\mu<\infty$, so $\mu\left(\left\{x:f^{+}\left(x\right)>\frac{1}{n}\right\}\right)\le n\int f^{+}\mathrm{d}\mu<\infty$. Thus $\left\{f^{+}>0\right\}$ is a countable union of sets of finite measure; similarly for $\left\{f^{-}>0\right\}$. Hence $\left\{x:f\left(x\right)\ne0\right\}$ is also a countable union of sets of finite measure, i.e. $\sigma$-finite in the sense of **Definition 5.1.5**. $\blacksquare$

(b) Set $h:=\left|f-g\right|\in L^{1}$, $h\ge0$. We prove the chain of equivalences.

(1) $\int\left|f-g\right|\mathrm{d}\mu=0\Rightarrow f=g$ almost everywhere: by the Basic Knowledge (if a nonnegative integrable function has integral zero, it vanishes almost everywhere), $h=0$ almost everywhere, i.e. $f=g$ almost everywhere.

(2) $f=g$ almost everywhere $\Rightarrow\int\left|f-g\right|\mathrm{d}\mu=0$: since $h=0$ outside $\left\{f\ne g\right\}$, and $\left\{f\ne g\right\}$ is a null set. By **Proposition 8.2.4** (Absolute Continuity), $\int_{\left\{f\ne g\right\}}h\,\mathrm{d}\mu=0$, and $\int_{\left\{f=g\right\}}h\,\mathrm{d}\mu=0$, so $\int h\,\mathrm{d}\mu=0$.

(3) $\int\left|f-g\right|\mathrm{d}\mu=0\Rightarrow\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\mu$ for all $E$: by Problem 2 (1)(3) (linearity and the triangle inequality),

$$
\begin{aligned}\left|\int_{E}f\,\mathrm{d}\mu-\int_{E}g\,\mathrm{d}\mu\right|&=\left|\int_{E}\left(f-g\right)\mathrm{d}\mu\right|\\&\le\int_{E}\left|f-g\right|\mathrm{d}\mu\\&\le\int_{X}\left|f-g\right|\mathrm{d}\mu\\&=0.
\end{aligned}
$$

(4) $\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\mu$ for all $E$ $\Rightarrow\int\left|f-g\right|\mathrm{d}\mu=0$: take $E:=\left\{x:f\left(x\right)\ge g\left(x\right)\right\}\in\mathcal F$. By the linearity in Problem 2 (1), $\int_{E}\left(f-g\right)\mathrm{d}\mu=\int_{E}f\,\mathrm{d}\mu-\int_{E}g\,\mathrm{d}\mu=0$; on $E$, $f-g\ge0$, so $\int_{E}\left|f-g\right|\mathrm{d}\mu=\int_{E}\left(f-g\right)\mathrm{d}\mu=0$. Similarly, on $E^{c}$, $\int_{E^{c}}\left(g-f\right)\mathrm{d}\mu=0$, and on $E^{c}$, $g-f\ge0$, so $\int_{E^{c}}\left|f-g\right|\mathrm{d}\mu=0$. Hence $\int\left|f-g\right|\mathrm{d}\mu=\int_{E}\left|f-g\right|\mathrm{d}\mu+\int_{E^{c}}\left|f-g\right|\mathrm{d}\mu=0$.

Combining (1)(2)(3)(4), the three conditions are equivalent. $\blacksquare$

### Problem 4

Prove Problems 14 and 16.

**14.** If $f\in L^{+}$, set $\lambda\left(E\right)=\int_{E}f\,\mathrm{d}\mu$ (for $E\in\mathcal M$). Then $\lambda$ is a measure on $\mathcal M$, and for any $g\in L^{+}$, $\int g\,d\lambda=\int fg\,\mathrm{d}\mu$.

**16.** If $f\in L^{+}$ and $\int f<\infty$, then for each $\epsilon>0$ there exists $E\in\mathcal M$ such that $\mu\left(E\right)<\infty$ and $\int_{E}f>\left(\int f\right)-\epsilon$.

### Solution to Problem 4

#### 14

We first prove that $\lambda$ is a measure. By **Definition 8.1.1** and **Definition 8.2.1**, $\lambda\left(\emptyset\right)=0$ and it is nonnegative. For pairwise disjoint measurable sets $\left\{E_{n}\right\}$, since $f\chi_{\bigsqcup E_{n}}=\sum_{n}f\chi_{E_{n}}$ and the partial sums $\sum_{n=1}^{N}f\chi_{E_{n}}\uparrow f\chi_{\bigsqcup E_{n}}$ pointwise, by **Theorem 8.2.2** (Monotone Convergence Theorem),

$$
\begin{aligned}\lambda\left(\bigsqcup_{n=1}^{\infty}E_{n}\right)&=\int f\chi_{\bigsqcup E_{n}}\mathrm{d}\mu\\&=\sum_{n=1}^{\infty}\int f\chi_{E_{n}}\mathrm{d}\mu\\&=\sum_{n=1}^{\infty}\lambda\left(E_{n}\right).
\end{aligned}
$$

Hence $\lambda$ is a measure on $\mathcal M$.

We next prove the change-of-variables formula. If $g=\sum_{j=1}^{m}a_{j}\chi_{E_{j}}$ is a simple function (with the $E_{j}$ pairwise disjoint), by **Definition 8.1.1** and finite linearity,

$$
\begin{aligned}\int g\,\mathrm{d}\lambda&=\sum_{j=1}^{m}a_{j}\lambda\left(E_{j}\right)\\&=\sum_{j=1}^{m}a_{j}\int_{E_{j}}f\,\mathrm{d}\mu\\&=\int\left(\sum_{j=1}^{m}a_{j}\chi_{E_{j}}f\right)\mathrm{d}\mu\\&=\int fg\,\mathrm{d}\mu.
\end{aligned}
$$

For a general $g\in L^{+}$, by **Remark 8.2.3** take simple functions $g_{k}\uparrow g$. Since $f\ge0$, $fg_{k}\uparrow fg$. By **Theorem 8.2.2** (under the measures $\lambda$ and $\mu$, respectively), $\int g_{k}\,d\lambda\uparrow\int g\,d\lambda$ and $\int fg_{k}\,\mathrm{d}\mu\uparrow\int fg\,\mathrm{d}\mu$. For each $k$ the two are equal (the simple case), so their limits are equal: $\int g\,d\lambda=\int fg\,\mathrm{d}\mu$. $\blacksquare$

#### 16

For $n\in\mathbb N$, set $E_{n}:=\left\{x:f\left(x\right)>\frac{1}{n}\right\}\in\mathcal M$. Then $\left\{E_{n}\right\}$ is monotonically increasing and $\bigcup_{n}E_{n}=\left\{x:f\left(x\right)>0\right\}$. By **Definition 8.2.1**,

$$
\int f\,\mathrm{d}\mu\ge\int_{E_{n}}f\,\mathrm{d}\mu\ge\frac{1}{n}\mu\left(E_{n}\right),
$$

so $\mu\left(E_{n}\right)\le n\int f\,\mathrm{d}\mu<\infty$. Also, by **Theorem 8.2.2** (Monotone Convergence Theorem), $\int_{E_{n}}f\,\mathrm{d}\mu\uparrow\int_{\left\{f>0\right\}}f\,\mathrm{d}\mu=\int f\,\mathrm{d}\mu$. Hence for given $\epsilon>0$, choose $n$ large enough that $\int_{E_{n}}f\,\mathrm{d}\mu>\int f\,\mathrm{d}\mu-\epsilon$, and set $E:=E_{n}$; then $\mu\left(E\right)<\infty$ and $\int_{E}f>\int f-\epsilon$. $\blacksquare$

### Problem 5

Prove Problems 20, 23, 27 and 29.

**20.** (Generalized dominated convergence theorem) If $f_{n},g_{n},f,g\in L^{1}$, $f_{n}\to f$ and $g_{n}\to g$ almost everywhere, $\left|f_{n}\right|\le g_{n}$, and $\int g_{n}\to\int g$, then $\int f_{n}\to\int f$.

**23.** Given a bounded function $f:\left[a,b\right]\to\mathbb R$, set

$$
\begin{aligned}H\left(x\right)&=\limsup_{\delta\to0}\sup_{0<\left|y-x\right|\le\delta}f\left(y\right),\\h\left(x\right)&=\liminf_{\delta\to0}\inf_{0<\left|y-x\right|\le\delta}f\left(y\right).
\end{aligned}
$$

Prove Theorem 2.28b (that f is Riemann integrable if and only if the set of points of discontinuity of f on $\left[a,b\right]$ has measure 0) by proving the following lemma:

a. $H\left(x\right)=h\left(x\right)$ if and only if $f$ is continuous at $x$;
b. In the notation of the proof of Theorem 2.28a, $H=G$ almost everywhere, $h=g$ almost everywhere, and $\int_{\left(a,b\right)}h\,\mathrm{d}m=L\left(f\right)$ (the lower Darboux integral).

**27.** Let $f_{n}\left(x\right)=ae^{-nax}-be^{-nbx}$, where $0<a<b$.

a. $\sum_{n=1}^{\infty}\int_{0}^{\infty}\left|f_{n}\left(x\right)\right|\mathrm{d}x=\infty$;
b. $\sum_{n=1}^{\infty}\int_{0}^{\infty}f_{n}\left(x\right)\mathrm{d}x=0$;
c. $\sum_{n=1}^{\infty}f_{n}\in L^{1}\left(\left[0,\infty\right),m\right)$, and $\int_{0}^{\infty}\sum_{n=1}^{\infty}f_{n}\left(x\right)\mathrm{d}x=\log\left(b/a\right)$.

**29.** By differentiating the identity $\int_{0}^{\infty}e^{-tx}\mathrm{d}x=1/t$, prove that $\int_{0}^{\infty}x^{n}e^{-x}\mathrm{d}x=n!$; similarly, by differentiating the identity $\int_{-\infty}^{\infty}e^{-tx^{2}}\mathrm{d}x=\sqrt{\pi/t}$, prove that $\int_{-\infty}^{\infty}x^{2n}e^{-x^{2}}\mathrm{d}x=\frac{\left(2n\right)!\sqrt\pi}{4^{n}n!}$.

### Solution to Problem 5

#### 20

Since $g_{n}\to g$ almost everywhere and $\left|f_{n}\right|\le g_{n}$, taking limits gives $\left|f\right|\le g$ almost everywhere, so $f\in L^{1}$. Since $\left|f_{n}\right|\le g_{n}$ means $-g_{n}\le f_{n}\le g_{n}$, the sequences $\left\{g_{n}+f_{n}\right\}$ and $\left\{g_{n}-f_{n}\right\}$ are nonnegative and converge almost everywhere to $g+f$ and $g-f$, respectively. By **Theorem 8.2.7** (Fatou's Lemma),

$$
\int\left(g+f\right)\mathrm{d}\mu\le\liminf_{n\to\infty}\int\left(g_{n}+f_{n}\right)\mathrm{d}\mu=\int g\,\mathrm{d}\mu+\liminf_{n\to\infty}\int f_{n}\,\mathrm{d}\mu,
$$

since $\int g_{n}\to\int g$ and the integrals are finite (linearity, Problem 2). Subtracting $\int g\,\mathrm{d}\mu$ from both sides gives $\int f\,\mathrm{d}\mu\le\liminf_{n\to\infty}\int f_{n}\,\mathrm{d}\mu$. Similarly, applying Fatou's lemma to $\left\{g_{n}-f_{n}\right\}$,

$$
\int\left(g-f\right)\mathrm{d}\mu\le\liminf_{n\to\infty}\int\left(g_{n}-f_{n}\right)\mathrm{d}\mu=\int g\,\mathrm{d}\mu-\limsup_{n\to\infty}\int f_{n}\,\mathrm{d}\mu,
$$

i.e. $\limsup_{n\to\infty}\int f_{n}\,\mathrm{d}\mu\le\int f\,\mathrm{d}\mu$. Combining,

$$
\int f\,\mathrm{d}\mu\le\liminf_{n\to\infty}\int f_{n}\,\mathrm{d}\mu\le\limsup_{n\to\infty}\int f_{n}\,\mathrm{d}\mu\le\int f\,\mathrm{d}\mu,
$$

Hence

$$\lim_{n\to\infty}\int f_{n}\,\mathrm{d}\mu=\int f\,\mathrm{d}\mu.$$

$\blacksquare$

#### 23

We first use the notation for Darboux sums from the Basic Knowledge. Set $\overline{\int}f=\inf_{P}\overline S\left(P\right)$ and $\underline{\int}f=\sup_{P}\underline S\left(P\right)$; $f$ is Riemann integrable if and only if $\overline{\int}f=\underline{\int}f$.

**a.** Suppose $f$ is continuous at $x$. For $\epsilon>0$ there exists $\delta>0$ such that $\left|y-x\right|<\delta\Rightarrow\left|f\left(y\right)-f\left(x\right)\right|<\epsilon$. Then for $0<\left|y-x\right|\le\delta$, we have $f\left(x\right)-\epsilon<f\left(y\right)<f\left(x\right)+\epsilon$, so

$$
f\left(x\right)-\epsilon\le\inf_{0<\left|y-x\right|\le\delta}f\left(y\right)\le f\left(x\right)\le\sup_{0<\left|y-x\right|\le\delta}f\left(y\right)\le f\left(x\right)+\epsilon.
$$

Letting $\delta\to0$, and since $\epsilon$ is arbitrary, gives $h\left(x\right)\ge f\left(x\right)\ge H\left(x\right)$; but by definition always $h\left(x\right)\le f\left(x\right)\le H\left(x\right)$, so $H\left(x\right)=h\left(x\right)=f\left(x\right)$.

Conversely, suppose $H\left(x\right)=h\left(x\right)=:L$. For $\epsilon>0$, by the definition of the limit there exists $\delta>0$ such that for $0<\delta'<\delta$,

$$
\inf_{0<\left|y-x\right|\le\delta'}f\left(y\right)>L-\epsilon,\ \sup_{0<\left|y-x\right|\le\delta'}f\left(y\right)<L+\epsilon.
$$

Taking $\delta'=\delta$, then for $0<\left|y-x\right|\le\delta$ we have $L-\epsilon<f\left(y\right)<L+\epsilon$; also $f\left(x\right)$ lies between $\inf$ and $\sup$, so $L-\epsilon<f\left(x\right)<L+\epsilon$. Hence $\left|f\left(y\right)-f\left(x\right)\right|<2\epsilon$ for $0<\left|y-x\right|\le\delta$, i.e. $f$ is continuous at $x$.

**b.** We use the notation from the proof of Theorem 2.28a: take a sequence of partitions $\left\{P_{k}\right\}$ such that the mesh $\max_{i}\left(t_{i}-t_{i-1}\right)\to0$ and $P_{k}\subset P_{k+1}$ (refining successively), and define

$$
\begin{aligned}G_{P_{k}}&=\sum_{i}M_{i}^{\left(k\right)}\chi_{\left(t_{i-1}^{\left(k\right)},t_{i}^{\left(k\right)}\right)},\\g_{P_{k}}&=\sum_{i}m_{i}^{\left(k\right)}\chi_{\left(t_{i-1}^{\left(k\right)},t_{i}^{\left(k\right)}\right)},
\end{aligned}
$$

and set $G=\lim_{k}G_{P_{k}}$, $g=\lim_{k}g_{P_{k}}$. Fix $x$ not equal to any partition point of any $P_{k}$ (the union of all partition points is at most countable and has measure 0). Suppose $x\in\left(t_{i-1}^{\left(k\right)},t_{i}^{\left(k\right)}\right)$; then $G_{P_{k}}\left(x\right)=M_{i}^{\left(k\right)}=\sup_{\left[t_{i-1}^{\left(k\right)},t_{i}^{\left(k\right)}\right]}f$. As $k\to\infty$ this small interval shrinks to $\left\{x\right\}$, and the supremum decreases to the limit of $\sup_{0<\left|y-x\right|\le\delta}f\left(y\right)$ as $\delta\to0$, i.e. $H\left(x\right)$. Hence $G\left(x\right)=H\left(x\right)$; similarly $g\left(x\right)=h\left(x\right)$. Therefore, after removing the countable set of partition points from $\left[a,b\right]$, $H=G$ and $h=g$ almost everywhere.

Also, $G_{P_{k}}$ is bounded and $g_{P_{k}}\le f\le G_{P_{k}}$; by **Theorem 8.2.9** (Dominated Convergence Theorem, or monotone convergence),

$$
\begin{aligned}\int H\,\mathrm{d}m&=\int G\,\mathrm{d}m\\&=\lim_{k}\int G_{P_{k}}\mathrm{d}m\\&=\lim_{k}\overline S\left(P_{k}\right)\\&=\overline{\int}f,
\end{aligned}
$$

$$
\begin{aligned}\int h\,\mathrm{d}m&=\int g\,\mathrm{d}m\\&=\lim_{k}\int g_{P_{k}}\mathrm{d}m\\&=\lim_{k}\underline S\left(P_{k}\right)\\&=\underline{\int}f.
\end{aligned}
$$

(In the proof of Theorem 2.28a, the $P_{k}$ are chosen so that $\overline S\left(P_{k}\right)\to\overline{\int}f$ and $\underline S\left(P_{k}\right)\to\underline{\int}f$.) In particular, $\int_{\left(a,b\right)}h\,\mathrm{d}m=L\left(f\right)$. Thus

$$
\begin{aligned}f\text{黎曼可积}\\&\iff\overline{\int}f=\underline{\int}f\\&\iff\int H\,\mathrm{d}m=\int h\,\mathrm{d}m\\&\iff\int\left(H-h\right)\mathrm{d}m=0.
\end{aligned}
$$

Since $H\ge h$, by Problem 3 (b), $\int\left(H-h\right)\mathrm{d}m=0\iff H=h$ almost everywhere. Combining with lemma a ($H=h\iff f$ continuous at $x$), we get that $f$ is Riemann integrable if and only if the set of points of discontinuity of $f$ has measure 0. In that case the Riemann integral is $\overline{\int}f=\int H\,\mathrm{d}m=\int f\,\mathrm{d}m$ (since $H=f$ almost everywhere), and Theorem 2.28b is proved. $\blacksquare$

#### 27

We first find the zeros of $f_{n}$. Setting $f_{n}\left(x\right)=0$ gives $ae^{-nax}=be^{-nbx}$, i.e. $e^{n\left(b-a\right)x}=b/a$, so the unique zero point is

$$
x_{n}=\frac{\log\left(b/a\right)}{n\left(b-a\right)}.
$$

On $\left[0,x_{n}\right)$, $f_{n}<0$, and on $\left(x_{n},\infty\right)$, $f_{n}>0$ (since when $x<x_{n}$, $e^{n\left(b-a\right)x}<b/a$, so $ae^{-nax}<be^{-nbx}$).

**a.** Compute

$$
\int_{0}^{\infty}\left|f_{n}\right|\mathrm{d}x=\int_{0}^{x_{n}}\left(be^{-nbx}-ae^{-nax}\right)\mathrm{d}x+\int_{x_{n}}^{\infty}\left(ae^{-nax}-be^{-nbx}\right)\mathrm{d}x.
$$

Using $\int_{0}^{x_{n}}be^{-nbx}\mathrm{d}x=\frac{1}{n}\left(1-e^{-nbx_{n}}\right)$, $\int_{0}^{x_{n}}ae^{-nax}\mathrm{d}x=\frac{1}{n}\left(1-e^{-nax_{n}}\right)$, $\int_{x_{n}}^{\infty}ae^{-nax}\mathrm{d}x=\frac{1}{n}e^{-nax_{n}}$, and $\int_{x_{n}}^{\infty}be^{-nbx}\mathrm{d}x=\frac{1}{n}e^{-nbx_{n}}$, we get

$$
\int_{0}^{\infty}\left|f_{n}\right|\mathrm{d}x=\frac{2}{n}\left(e^{-nax_{n}}-e^{-nbx_{n}}\right).
$$

Set $t=e^{-nx_{n}}$; then by the zero-point condition $at^{a}=bt^{b}$, i.e. $t^{a-b}=b/a$, so $t=\left(b/a\right)^{1/\left(a-b\right)}\in\left(0,1\right)$. Since $t<1$ and $a<b$, the power function $\lambda\mapsto t^{\lambda}$ is decreasing, so $t^{a}>t^{b}$; the constant $c:=2\left(t^{a}-t^{b}\right)>0$. Therefore

$$
\begin{aligned}\sum_{n=1}^{\infty}\int_{0}^{\infty}\left|f_{n}\right|\mathrm{d}x&=c\sum_{n=1}^{\infty}\frac{1}{n}&=\infty.
\end{aligned}
$$

**b.** Compute term by term:

$$
\begin{aligned}\int_{0}^{\infty}f_{n}\left(x\right)\mathrm{d}x&=\int_{0}^{\infty}ae^{-nax}\mathrm{d}x-\int_{0}^{\infty}be^{-nbx}\mathrm{d}x\\&=\frac{1}{n}-\frac{1}{n}\\&=0,
\end{aligned}
$$

hence $\sum_{n=1}^{\infty}\int_{0}^{\infty}f_{n}\left(x\right)\mathrm{d}x=0$.

**c.** By the geometric series $\sum_{n=1}^{\infty}e^{-nax}=\frac{e^{-ax}}{1-e^{-ax}}=\frac{1}{e^{ax}-1}$,

$$
\begin{aligned}\sum_{n=1}^{\infty}f_{n}\left(x\right)&=a\sum_{n=1}^{\infty}e^{-nax}-b\sum_{n=1}^{\infty}e^{-nbx}\\&=\frac{a}{e^{ax}-1}-\frac{b}{e^{bx}-1}.
\end{aligned}
$$

As $x\to0^{+}$, $\frac{a}{e^{ax}-1}=\frac{1}{x}-\frac{a}{2}+O\left(x\right)$, so the difference $\frac{a}{e^{ax}-1}-\frac{b}{e^{bx}-1}\to\frac{b-a}{2}+O\left(x\right)$ is finite; as $x\to\infty$, there is exponential decay. Hence $\sum f_{n}\in L^{1}\left(\left[0,\infty\right),m\right)$.

For $R>0$, make the substitutions $u=ax$ and $u=bx$:

$$
\begin{aligned}\int_{0}^{R}\frac{a}{e^{ax}-1}\mathrm{d}x&=\int_{0}^{aR}\frac{\mathrm{d}u}{e^{u}-1},\\\int_{0}^{R}\frac{b}{e^{bx}-1}\mathrm{d}x&=\int_{0}^{bR}\frac{\mathrm{d}u}{e^{u}-1}.
\end{aligned}
$$

Hence

$$
\int_{0}^{R}\left(\frac{a}{e^{ax}-1}-\frac{b}{e^{bx}-1}\right)\mathrm{d}x=\int_{aR}^{bR}\frac{\mathrm{d}u}{e^{u}-1}.
$$

Since $\frac{1}{e^{u}-1}-\frac{1}{u}=O\left(e^{-u}\right)$ is integrable at infinity, $\int_{aR}^{bR}\frac{\mathrm{d}u}{e^{u}-1}=\int_{aR}^{bR}\frac{\mathrm{d}u}{u}+o\left(1\right)$; letting $R\to\infty$ gives

$$
\begin{aligned}\int_{0}^{\infty}\sum_{n=1}^{\infty}f_{n}\left(x\right)\mathrm{d}x&=\lim_{R\to\infty}\int_{aR}^{bR}\frac{\mathrm{d}u}{u}\\&=\log\left(b/a\right).
\end{aligned}
$$

Note that here $\sum\int\left|f_{n}\right|=\infty$ (by part a), so the condition $\sum\int\left|f_{n}\right|<\infty$ of **Lemma 8.2.13** (Termwise Integration of a Series) is not satisfied; hence termwise integration cannot be applied. In fact, $\int\sum f_{n}=\log\left(b/a\right)\ne\sum\int f_{n}=0$, which shows that this condition is essential. $\blacksquare$

#### 29

We use **Theorem 8.2.17**(b) (differentiation under the integral sign). Fix $t_{0}>0$, and consider a compact neighborhood $\left[t_{0}/2,t_{0}\right]$ of $t$.

**Case 1.** Let $F\left(t\right)=\int_{0}^{\infty}e^{-tx}\mathrm{d}x=\frac{1}{t}$ ($t>0$). For each $k\ge1$, on $t\in\left[t_{0}/2,t_{0}\right]$, $\left|\frac{\partial^{k}}{\partial t^{k}}e^{-tx}\right|=x^{k}e^{-tx}\le x^{k}e^{-\left(t_{0}/2\right)x}\in L^{1}\left(\left[0,\infty\right)\right)$, so Theorem 8.2.17(b) can be applied repeatedly:

$$
F^{\left(n\right)}\left(t\right)=\int_{0}^{\infty}\left(-x\right)^{n}e^{-tx}\mathrm{d}x.
$$

Also, $F\left(t\right)=1/t$, and its $n$-th derivative is $F^{\left(n\right)}\left(t\right)=\left(-1\right)^{n}n!/t^{n+1}$. Taking $t=1$:

$$
\int_{0}^{\infty}\left(-x\right)^{n}e^{-x}\mathrm{d}x=\left(-1\right)^{n}n!,
$$

i.e. $\int_{0}^{\infty}x^{n}e^{-x}\mathrm{d}x=n!$.

**Case 2.** Let $G\left(s\right)=\int_{-\infty}^{\infty}e^{-sx^{2}}\mathrm{d}x=\sqrt{\pi/s}=\sqrt\pi\,s^{-1/2}$ ($s>0$). For each $k\ge1$, on $s\in\left[s_{0}/2,s_{0}\right]$, $\left|\frac{\partial^{k}}{\partial s^{k}}e^{-sx^{2}}\right|=x^{2k}e^{-sx^{2}}\le x^{2k}e^{-\left(s_{0}/2\right)x^{2}}\in L^{1}\left(\mathbb R\right)$, so we may differentiate repeatedly:

$$
\begin{aligned}G^{\left(n\right)}\left(s\right)&=\int_{-\infty}^{\infty}\left(-x^{2}\right)^{n}e^{-sx^{2}}\mathrm{d}x\\&=\left(-1\right)^{n}\int_{-\infty}^{\infty}x^{2n}e^{-sx^{2}}\mathrm{d}x.
\end{aligned}
$$

Also,

$$G^{\left(n\right)}\left(s\right)=\sqrt\pi\left(-\frac{1}{2}\right)\left(-\frac{3}{2}\right)\cdots\left(-\frac{2n-1}{2}\right)s^{-\frac{2n+1}{2}}.$$

Taking $s=1$:

$$
\left(-1\right)^{n}\int_{-\infty}^{\infty}x^{2n}e^{-x^{2}}\mathrm{d}x=\sqrt\pi\left(-1\right)^{n}\frac{1\cdot3\cdots\left(2n-1\right)}{2^{n}},
$$

i.e. $\int_{-\infty}^{\infty}x^{2n}e^{-x^{2}}\mathrm{d}x=\sqrt\pi\frac{1\cdot3\cdots\left(2n-1\right)}{2^{n}}$. Since $1\cdot3\cdots\left(2n-1\right)=\frac{\left(2n\right)!}{2^{n}n!}$, we get

$$
\int_{-\infty}^{\infty}x^{2n}e^{-x^{2}}\mathrm{d}x=\frac{\left(2n\right)!\sqrt\pi}{4^{n}n!}.
$$

$\blacksquare$
