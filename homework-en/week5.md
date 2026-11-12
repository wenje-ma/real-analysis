# week5

> **Definition 5.1.2 (Measure)**
> 
> Let $\left(X,\mathcal{F}\right)$ be a measurable space. A function $\mu:\mathcal{F}\to\left[0,+\infty\right]$ is called a measure on $\left(X,\mathcal{F}\right)$ if: (1) nonnegativity: $\mu\left(E\right)\ge0$ for all $E\in\mathcal{F}$; (2) empty set: $\mu\left(\emptyset\right)=0$; (3) countable additivity ($\sigma$-additivity): for any countable pairwise-disjoint $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$, $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **Definition 5.1.5 ($\sigma$-Finite Measure)**
> 
> Let $\left(X,\mathcal{F},\mu\right)$ be a measure space. If there exists a sequence of measurable sets $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$ such that $X=\bigcup_{n=1}^{\infty}E_{n}$ and $\mu\left(E_{n}\right)<+\infty$ for all $n\in\mathbb{N}$, then $\mu$ is called $\sigma$-finite.

> **Definition 8.1.1 (Integral of a Nonnegative Simple Function)**
> 
> Let $f=\sum_{i=1}^{n}c_{i}\chi_{A_{i}}$ be a nonnegative simple function, where $c_{i}\ge0$, the $A_{i}\in\mathcal{F}$ are pairwise disjoint and $\bigcup_{i}A_{i}=X$. The integral of $f$ with respect to $\mu$ is $\int_{X}f\,\mathrm{d}\mu=\sum_{i=1}^{n}c_{i}\mu\left(A_{i}\right)$, with the convention $0\cdot\infty=0$.

> **Proposition 8.1.2 (Linearity of the Integral for Simple Functions)**
> 
> Let $f,g$ be nonnegative simple functions and $\alpha,\beta\ge0$. Then $\int_{X}\left(\alpha{f}+\beta{g}\right)\mathrm{d}\mu=\alpha\int_{X}f\,\mathrm{d}\mu+\beta\int_{X}g\,\mathrm{d}\mu$.

> **Definition 8.2.1 (Integral of a Nonnegative Measurable Function)**
> 
> Let $f:X\to\left[0,+\infty\right]$ be a nonnegative measurable function. The integral of $f$ with respect to $\mu$ is $\int_{X}f\,\mathrm{d}\mu=\sup\left\{\int_{X}\phi\,\mathrm{d}\mu:\phi\text{~simple},0\le\phi\le{f}\right\}$. If $\int_{X}f\,\mathrm{d}\mu<\infty$, $f$ is called integrable.

> **Theorem 8.2.2 (Monotone Convergence Theorem)**
> 
> Let $\left(X,\mathcal{F},\mu\right)$ be a measure space and $\left\{f_{n}\right\}$ a sequence of nonnegative measurable functions with $0\le{f}_{1}\left(x\right)\le{f}_{2}\left(x\right)\le\cdots$ for all $x\in{X}$, and $f_{n}\to{f}$ pointwise. Then $\lim_{n\to\infty}\int_{X}f_{n}\,\mathrm{d}\mu=\int_{X}f\,\mathrm{d}\mu$.

> **Remark 8.2.3 (Approximation by Simple Functions)**
> 
> The monotone convergence theorem tells us that the integral can be approximated by simple functions.

> **Proposition 8.2.4 (Absolute Continuity of the Integral with Respect to the Set)**
> 
> Let $f$ be a nonnegative measurable function. Then $A\mapsto\int_{A}f\,\mathrm{d}\mu$ is a measure; if $\mu\left(A\right)=0$, then $\int_{A}f\,\mathrm{d}\mu=0$.

> **Definition 8.2.5 (Integral of a General Measurable Function)**
> 
> Let $f:X\to\left[-\infty,+\infty\right]$ be measurable. Define its positive and negative parts by $f^{+}\left(x\right)=\max\left\{f\left(x\right),0\right\}$, $f^{-}\left(x\right)=\max\left\{-f\left(x\right),0\right\}$. If at least one of $\int_{X}f^{+}\mathrm{d}\mu$, $\int_{X}f^{-}\mathrm{d}\mu$ is finite, define the integral by $\int_{X}f\,\mathrm{d}\mu=\int_{X}f^{+}\mathrm{d}\mu-\int_{X}f^{-}\mathrm{d}\mu$. If both are finite, $f$ is called integrable.

> **Theorem 8.2.7 (Fatou's Lemma)**
> 
> Let $\left(X,\mathcal{F},\mu\right)$ be a measure space and $\left\{f_{n}\right\}$ a sequence of nonnegative measurable functions. Then $\int_{X}\liminf_{n\to\infty}f_{n}\,\mathrm{d}\mu\le\liminf_{n\to\infty}\int_{X}f_{n}\,\mathrm{d}\mu$.

> **Theorem 8.2.9 (Dominated Convergence Theorem)**
> 
> Let $\left(X,\mathcal{F},\mu\right)$ be a measure space and $\left\{f_{n}\right\}$ a sequence of measurable functions. If there exists an integrable $g$ with $\left|f_{n}\right|\le{g}$ for all $n$ and $f_{n}\to{f}$ a.e., then $f$ is integrable and $\int{f}\,\mathrm{d}\mu=\lim_{n\to\infty}\int{f}_{n}\,\mathrm{d}\mu$.

> **Lemma 8.2.13 (Termwise Integration of Series)**
> 
> Let $\left\{f_{n}\right\}$ be a sequence of measurable functions with $\sum_{n=1}^{\infty}\int_{X}\left|f_{n}\right|\mathrm{d}\mu<\infty$. Then $\int_{X}\left(\sum_{n=1}^{\infty}f_{n}\right)\mathrm{d}\mu=\sum_{n=1}^{\infty}\int_{X}f_{n}\,\mathrm{d}\mu$.

> **Theorem 8.2.17 (Parameter Integrals)**
> 
> Let $f:X\times\left[a,b\right]\to\mathbb{R}$, and for each $t\in\left[a,b\right]$ let $f\left(\cdot,t\right):X\to\mathbb{R}$ be integrable. Set $F\left(t\right)=\int_{X}f\left(x,t\right)\mathrm{d}\mu\left(x\right)$. (a) If there exists $g\in{L}^{1}\left(\mu\right)$ with $\left|f\left(x,t\right)\right|\le{g}\left(x\right)$ for all $x,t$, and $\lim_{t\to{t}_{0}}f\left(x,t\right)=f\left(x,t_{0}\right)$ for each $x$, then $\lim_{t\to{t}_{0}}F\left(t\right)=F\left(t_{0}\right)$; (b) if the partial derivative $\partial{f}/\partial{t}$ exists and there is $g\in{L}^{1}\left(\mu\right)$ with $\left|\frac{\partial{f}}{\partial{t}}\left(x,t\right)\right|\le{g}\left(x\right)$ for all $x,t$, then $F$ is differentiable and $F'\left(t\right)=\int\frac{\partial{f}}{\partial{t}}\left(x,t\right)\mathrm{d}\mu\left(x\right)$.

## 1

Let $f$ be a nonnegative simple function. Prove that $A\mapsto\int_{A}f\,\mathrm{d}\mu$ is a measure, and that if $\mu\left(A\right)=0$, then $\int_{A}f\,\mathrm{d}\mu=0$.

### Solution to 1

Write $f=\sum_{i=1}^{n}c_{i}\chi_{A_{i}}$, where $c_{i}\ge0$, the $A_{i}\in\mathcal{F}$ are pairwise disjoint and $\bigcup_{i}A_{i}=X$. For $E\in\mathcal{F}$, by **Definition 8.1.1 (Integral of a Nonnegative Simple Function)**,

$$
\int_{E}f\,\mathrm{d}\mu=\int{f}\chi_{E}\,\mathrm{d}\mu=\sum_{i=1}^{n}c_{i}\mu\left(E\cap{A}_{i}\right).
$$

Let $\lambda\left(E\right):=\int_{E}f\,\mathrm{d}\mu$. Verify that $\lambda$ is a measure: $\lambda\left(\emptyset\right)=\sum_{i=1}^{n}c_{i}\mu\left(\emptyset\cap{A}_{i}\right)=0$; nonnegativity is clear since $c_{i}\ge0$ and $\mu\ge0$; countable additivity: let $E=\bigsqcup_{j=1}^{\infty}E_{j}$ (pairwise disjoint). By countable additivity of $\mu$ (**Definition 5.1.2 (Measure)**) and **Proposition 8.1.2 (Linearity of the Integral for Simple Functions)**,

$$
\lambda\left(E\right)=\sum_{i=1}^{n}c_{i}\mu\left(E\cap{A}_{i}\right)=\sum_{i=1}^{n}c_{i}\sum_{j=1}^{\infty}\mu\left(E_{j}\cap{A}_{i}\right)=\sum_{j=1}^{\infty}\sum_{i=1}^{n}c_{i}\mu\left(E_{j}\cap{A}_{i}\right)=\sum_{j=1}^{\infty}\lambda\left(E_{j}\right).
$$

Thus $\lambda$ is a measure on $\mathcal{F}$. Finally, if $\mu\left(A\right)=0$, then

$$
\lambda\left(A\right)=\sum_{i=1}^{n}c_{i}\mu\left(A\cap{A}_{i}\right)\le\sum_{i=1}^{n}c_{i}\mu\left(A\right)=0,
$$

so $\lambda\left(A\right)=0$.

$\blacksquare$

## 2

Let $f,g$ be integrable and $a,b\in\mathbb{R}$. Prove:

1. Linearity: $\int_{X}\left(af+bg\right)\mathrm{d}\mu=a\int_{X}f\,\mathrm{d}\mu+b\int_{X}g\,\mathrm{d}\mu$;

2. Monotonicity: if $f\le{g}$ almost everywhere, then $\int_{X}f\,\mathrm{d}\mu\le\int_{X}g\,\mathrm{d}\mu$;

3. Triangle inequality: $\left|\int_{X}f\,\mathrm{d}\mu\right|\le\int_{X}\left|f\right|\mathrm{d}\mu$;

4. If $f=g$ almost everywhere, then $\int_{X}f\,\mathrm{d}\mu=\int_{X}g\,\mathrm{d}\mu$.

### Solution to 2

First establish linearity for nonnegative measurable functions. Let $\phi,\psi$ be nonnegative measurable and $\alpha,\beta\ge0$. By **Remark 8.2.3 (Approximation by Simple Functions)**, there are simple functions $\phi_{k}\uparrow\phi$, $\psi_{k}\uparrow\psi$. By **Proposition 8.1.2 (Linearity of the Integral for Simple Functions)**,

$$
\int\left(\alpha\phi_{k}+\beta\psi_{k}\right)\mathrm{d}\mu=\alpha\int\phi_{k}\,\mathrm{d}\mu+\beta\int\psi_{k}\,\mathrm{d}\mu.
$$

Since $\alpha\phi_{k}+\beta\psi_{k}\uparrow\alpha\phi+\beta\psi$, taking limits by **Theorem 8.2.2 (Monotone Convergence Theorem)** gives

$$
\int\left(\alpha\phi+\beta\psi\right)\mathrm{d}\mu=\alpha\int\phi\,\mathrm{d}\mu+\beta\int\psi\,\mathrm{d}\mu.
$$

Now let $f,g$ be integrable, with positive and negative parts $f^{+},f^{-}$ (**Definition 8.2.5 (Integral of a General Measurable Function)**).

1. First for scalar multiplication: if $a\ge0$, then $\left(af\right)^{+}=af^{+}$, $\left(af\right)^{-}=af^{-}$, so $\int\left(af\right)\mathrm{d}\mu=a\int{f}^{+}\mathrm{d}\mu-a\int{f}^{-}\mathrm{d}\mu=a\int{f}\,\mathrm{d}\mu$; if $a<0$, then $\left(af\right)^{+}=\left|a\right|f^{-}$, $\left(af\right)^{-}=\left|a\right|f^{+}$, and similarly $\int\left(af\right)\mathrm{d}\mu=a\int{f}\,\mathrm{d}\mu$; $a=0$ is trivial. For addition, decompose by positive/negative parts: $f+g=\left(f^{+}+g^{+}\right)-\left(f^{-}+g^{-}\right)$, i.e.

$$
\left(f+g\right)^{+}+f^{-}+g^{-}=\left(f+g\right)^{-}+f^{+}+g^{+},
$$

both sides are nonnegative measurable, and integrating by nonneg linearity,

$$
\int\left(f+g\right)^{+}\mathrm{d}\mu+\int{f}^{-}\mathrm{d}\mu+\int{g}^{-}\mathrm{d}\mu=\int\left(f+g\right)^{-}\mathrm{d}\mu+\int{f}^{+}\mathrm{d}\mu+\int{g}^{+}\mathrm{d}\mu,
$$

and rearranging (all terms finite since $f,g$ are integrable) gives $\int\left(f+g\right)\mathrm{d}\mu=\int{f}\,\mathrm{d}\mu+\int{g}\,\mathrm{d}\mu$. Combining gives $\int\left(af+bg\right)\mathrm{d}\mu=a\int{f}\,\mathrm{d}\mu+b\int{g}\,\mathrm{d}\mu$.

2. By linearity, $\int{g}\,\mathrm{d}\mu-\int{f}\,\mathrm{d}\mu=\int\left(g-f\right)\mathrm{d}\mu$. Since $f\le{g}$ a.e., $g-f\ge0$ a.e. By **Definition 8.2.1 (Integral of a Nonnegative Measurable Function)**, the integral of a nonnegative measurable function is nonnegative (it is a supremum of integrals of nonnegative simple functions), so $\int\left(g-f\right)\mathrm{d}\mu\ge0$, i.e. $\int{f}\,\mathrm{d}\mu\le\int{g}\,\mathrm{d}\mu$.

3. $\left|f\right|=f^{+}+f^{-}$, and by nonneg linearity $\int\left|f\right|\mathrm{d}\mu=\int{f}^{+}\mathrm{d}\mu+\int{f}^{-}\mathrm{d}\mu$. Since $\int{f}\,\mathrm{d}\mu=\int{f}^{+}\mathrm{d}\mu-\int{f}^{-}\mathrm{d}\mu$,

$$
\left|\int{f}\,\mathrm{d}\mu\right|=\left|\int{f}^{+}\mathrm{d}\mu-\int{f}^{-}\mathrm{d}\mu\right|\le\int{f}^{+}\mathrm{d}\mu+\int{f}^{-}\mathrm{d}\mu=\int\left|f\right|\mathrm{d}\mu.
$$

4. If $f=g$ a.e., then $f^{+}=g^{+}$ and $f^{-}=g^{-}$ a.e. Thus $h:=f^{+}-g^{+}$ is integrable and $h=0$ a.e.; its positive part $h^{+}$ and negative part $h^{-}$ vanish outside a null set. By **Proposition 8.2.4 (Absolute Continuity of the Integral with Respect to the Set)**, $\int{h}^{+}\mathrm{d}\mu=\int_{\left\{h>0\right\}}h^{+}\mathrm{d}\mu=0$ and $\int{h}^{-}\mathrm{d}\mu=0$, so $\int{h}\,\mathrm{d}\mu=0$, i.e. $\int{f}^{+}\mathrm{d}\mu=\int{g}^{+}\mathrm{d}\mu$; similarly $\int{f}^{-}\mathrm{d}\mu=\int{g}^{-}\mathrm{d}\mu$. Hence $\int{f}\,\mathrm{d}\mu=\int{g}\,\mathrm{d}\mu$.

$\blacksquare$

## 3

Let $f\in{L}^{1}$. Prove:

(a) the set $\left\{x:f\left(x\right)\ne0\right\}$ is $\sigma$-finite;

(b) for $f,g\in{L}^{1}$, $\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\mu$ for every measurable $E$ iff $\int\left|f-g\right|\mathrm{d}\mu=0$ iff $f=g$ almost everywhere.

### Solution to 3

(a) By **Definition 8.2.5 (Integral of a General Measurable Function)**, $f=f^{+}-f^{-}$, so $\left\{x:f\left(x\right)\ne0\right\}=\left\{x:f^{+}\left(x\right)>0\right\}\cup\left\{x:f^{-}\left(x\right)>0\right\}$. Moreover,

$$
\left\{x:f^{+}\left(x\right)>0\right\}=\bigcup_{n=1}^{\infty}\left\{x:f^{+}\left(x\right)>\frac{1}{n}\right\},
$$

and by **Definition 8.2.1 (Integral of a Nonnegative Measurable Function)**,

$$
\int_{X}f^{+}\mathrm{d}\mu\ge\int_{\left\{f^{+}>\frac{1}{n}\right\}}f^{+}\mathrm{d}\mu\ge\frac{1}{n}\mu\left(\left\{x:f^{+}\left(x\right)>\frac{1}{n}\right\}\right).
$$

Since $f$ is integrable, $\int{f}^{+}\mathrm{d}\mu<\infty$, so $\mu\left(\left\{x:f^{+}\left(x\right)>\frac{1}{n}\right\}\right)\le{n}\int{f}^{+}\mathrm{d}\mu<\infty$. Thus $\left\{f^{+}>0\right\}$ is a countable union of finite-measure sets; similarly for $\left\{f^{-}>0\right\}$. Hence $\left\{x:f\left(x\right)\ne0\right\}$ is also a countable union of finite-measure sets, i.e. $\sigma$-finite in the sense of **Definition 5.1.5 ($\sigma$-Finite Measure)**.

$\blacksquare$

(b) Let $h:=\left|f-g\right|\in{L}^{1}$, $h\ge0$.

(1) $\int\left|f-g\right|\mathrm{d}\mu=0\Rightarrow{f}=g$ a.e.: by Nonnegative Integrable Function with Zero Integral Vanishes Almost Everywhere, $h=0$ a.e., i.e. $f=g$ a.e.

(2) $f=g$ a.e. $\Rightarrow\int\left|f-g\right|\mathrm{d}\mu=0$: since $h=0$ outside $\left\{f\ne{g}\right\}$ and $\left\{f\ne{g}\right\}$ is null. By **Proposition 8.2.4 (Absolute Continuity of the Integral with Respect to the Set)**, $\int_{\left\{f\ne{g}\right\}}h\,\mathrm{d}\mu=0$ and $\int_{\left\{f=g\right\}}h\,\mathrm{d}\mu=0$, so $\int{h}\,\mathrm{d}\mu=0$.

(3) $\int\left|f-g\right|\mathrm{d}\mu=0\Rightarrow\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\mu$ for all $E$: by Exercise 2, items 1 and 3,

$$
\left|\int_{E}f\,\mathrm{d}\mu-\int_{E}g\,\mathrm{d}\mu\right|=\left|\int_{E}\left(f-g\right)\mathrm{d}\mu\right|\le\int_{E}\left|f-g\right|\mathrm{d}\mu\le\int_{X}\left|f-g\right|\mathrm{d}\mu=0.
$$

(4) $\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\mu$ for all $E$ $\Rightarrow\int\left|f-g\right|\mathrm{d}\mu=0$: take $E:=\left\{x:f\left(x\right)\ge{g}\left(x\right)\right\}\in\mathcal{F}$. By linearity (Exercise 2, item 1), $\int_{E}\left(f-g\right)\mathrm{d}\mu=\int_{E}f\,\mathrm{d}\mu-\int_{E}g\,\mathrm{d}\mu=0$; on $E$, $f-g\ge0$, so $\int_{E}\left|f-g\right|\mathrm{d}\mu=\int_{E}\left(f-g\right)\mathrm{d}\mu=0$. Similarly, for $E^{c}$, $\int_{E^{c}}\left(g-f\right)\mathrm{d}\mu=0$, and on $E^{c}$, $g-f\ge0$, so $\int_{E^{c}}\left|f-g\right|\mathrm{d}\mu=0$. Hence $\int\left|f-g\right|\mathrm{d}\mu=\int_{E}\left|f-g\right|\mathrm{d}\mu+\int_{E^{c}}\left|f-g\right|\mathrm{d}\mu=0$.

Combining (1)(2)(3)(4), the three conditions are equivalent.

$\blacksquare$

## 4

Prove:

14. If $f\in{L}^{+}$, set $\lambda\left(E\right)=\int_{E}f\,\mathrm{d}\mu$ (for $E\in\mathcal{M}$). Then $\lambda$ is a measure on $\mathcal{M}$, and for any $g\in{L}^{+}$, $\int{g}\,\mathrm{d}\lambda=\int{f}g\,\mathrm{d}\mu$.

16. If $f\in{L}^{+}$ and $\int{f}<\infty$, then for every $\varepsilon>0$ there exists $E\in\mathcal{M}$ with $\mu\left(E\right)<\infty$ and $\int_{E}f>\left(\int{f}\right)-\varepsilon$.

### Solution to 4

14. First show $\lambda$ is a measure. By **Definition 8.1.1 (Integral of a Nonnegative Simple Function)** and **Definition 8.2.1 (Integral of a Nonnegative Measurable Function)**, $\lambda\left(\emptyset\right)=0$ and nonnegativity. For pairwise disjoint measurable sets $\left\{E_{n}\right\}$, since $f\chi_{\bigsqcup{E}_{n}}=\sum_{n}f\chi_{E_{n}}$ and the partial sums $\sum_{n=1}^{N}f\chi_{E_{n}}\uparrow{f}\chi_{\bigsqcup{E}_{n}}$ pointwise, by **Theorem 8.2.2 (Monotone Convergence Theorem)**,

$$
\lambda\left(\bigsqcup_{n=1}^{\infty}E_{n}\right)=\int{f}\chi_{\bigsqcup{E}_{n}}\mathrm{d}\mu=\sum_{n=1}^{\infty}\int{f}\chi_{E_{n}}\mathrm{d}\mu=\sum_{n=1}^{\infty}\lambda\left(E_{n}\right).
$$

Thus $\lambda$ is a measure on $\mathcal{M}$.

Now prove the change-of-variables formula. If $g=\sum_{j=1}^{m}a_{j}\chi_{E_{j}}$ is simple (with $E_{j}$ pairwise disjoint), by **Definition 8.1.1 (Integral of a Nonnegative Simple Function)** and finite linearity,

$$
\int{g}\,\mathrm{d}\lambda=\sum_{j=1}^{m}a_{j}\lambda\left(E_{j}\right)=\sum_{j=1}^{m}a_{j}\int_{E_{j}}f\,\mathrm{d}\mu=\int\left(\sum_{j=1}^{m}a_{j}\chi_{E_{j}}f\right)\mathrm{d}\mu=\int{f}g\,\mathrm{d}\mu.
$$

For general $g\in{L}^{+}$, take simple $g_{k}\uparrow{g}$ by **Remark 8.2.3 (Approximation by Simple Functions)**. Since $f\ge0$, $fg_{k}\uparrow{f}g$. By **Theorem 8.2.2 (Monotone Convergence Theorem)** (under measures $\lambda$ and $\mu$ respectively), $\int{g}_{k}\,\mathrm{d}\lambda\uparrow\int{g}\,\mathrm{d}\lambda$ and $\int{f}g_{k}\,\mathrm{d}\mu\uparrow\int{f}g\,\mathrm{d}\mu$. For each $k$ the two agree (simple case), so the limits agree: $\int{g}\,\mathrm{d}\lambda=\int{f}g\,\mathrm{d}\mu$.

$\blacksquare$

16. For $n\in\mathbb{N}$, let $E_{n}:=\left\{x:f\left(x\right)>\frac{1}{n}\right\}\in\mathcal{M}$. Then $\left\{E_{n}\right\}$ is increasing and $\bigcup_{n}E_{n}=\left\{x:f\left(x\right)>0\right\}$. By **Definition 8.2.1 (Integral of a Nonnegative Measurable Function)**,

$$
\int{f}\,\mathrm{d}\mu\ge\int_{E_{n}}f\,\mathrm{d}\mu\ge\frac{1}{n}\mu\left(E_{n}\right),
$$

so $\mu\left(E_{n}\right)\le{n}\int{f}\,\mathrm{d}\mu<\infty$. Also by **Theorem 8.2.2 (Monotone Convergence Theorem)**, $\int_{E_{n}}f\,\mathrm{d}\mu\uparrow\int_{\left\{f>0\right\}}f\,\mathrm{d}\mu=\int{f}\,\mathrm{d}\mu$. Thus for given $\varepsilon>0$, choose $n$ large enough that $\int_{E_{n}}f\,\mathrm{d}\mu>\int{f}\,\mathrm{d}\mu-\varepsilon$, and set $E:=E_{n}$; then $\mu\left(E\right)<\infty$ and $\int_{E}f>\int{f}-\varepsilon$.

$\blacksquare$
