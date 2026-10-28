# week5

> **Basic Knowledge: Nonnegative Integrable Function with Zero Integral Vanishes Almost Everywhere**<br>If $h\ge0$ is measurable and $\int_{X}h\,\mathrm{d}\mu=0$, then $h=0$ almost everywhere. Indeed $\left\{h> 0\right\}=\bigcup_{n=1}^{\infty}\left\{h> \frac{1}{n}\right\}$, and $\int h\ge\frac{1}{n}\mu\left(\left\{h> \frac{1}{n}\right\}\right)$, so $\mu\left(\left\{h> \frac{1}{n}\right\}\right)=0$ for all $n$.

> **Basic Knowledge: Riemann Integral and Darboux Sums**<br>Let $f$ be a bounded real-valued function on $\left[a,b\right]$. For a partition $P=\left\{t_{0}< \cdots< t_{n}\right\}$ of $\left[a,b\right]$, write $M_{i}=\sup_{\left[t_{i-1},t_{i}\right]}f$, $m_{i}=\inf_{\left[t_{i-1},t_{i}\right]}f$. The upper Darboux sum is $\overline S\left(P\right)=\sum_{i}M_{i}\left(t_{i}-t_{i-1}\right)$ and the lower is $\underline S\left(P\right)=\sum_{i}m_{i}\left(t_{i}-t_{i-1}\right)$. The upper integral is $\overline{\int}f=\inf_{P}\overline S\left(P\right)$ and the lower is $\underline{\int}f=\sup_{P}\underline S\left(P\right)$. If $\overline{\int}f=\underline{\int}f$, the common value is the Riemann integral of $f$, and $f$ is called Riemann integrable.

> **Definition 5.1.2 (Measure)**<br>Let $\left(X,\mathcal F\right)$ be a measurable space. A function $\mu:\mathcal F\to\left[0,+\infty\right]$ is called a measure on $\left(X,\mathcal F\right)$ if: (1) nonnegativity: $\mu\left(E\right)\ge0$ for all $E\in\mathcal F$; (2) empty set: $\mu\left(\emptyset\right)=0$; (3) countable additivity ($\sigma$-additivity): for any countable pairwise-disjoint $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$, $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **Definition 5.1.5 ($\sigma$-Finite Measure)**<br>Let $\left(X,\mathcal F,\mu\right)$ be a measure space. If there exists a sequence of measurable sets $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$ such that $X=\bigcup_{n=1}^{\infty}E_{n}$ and $\mu\left(E_{n}\right)< +\infty$ for all $n\in\mathbb N$, then $\mu$ is called $\sigma$-finite.

> **Definition 8.1.1 (Integral of a Nonnegative Simple Function)**<br>Let $f=\sum_{i=1}^{n}c_{i}\chi_{A_{i}}$ be a nonnegative simple function, where $c_{i}\ge0$, the $A_{i}\in\mathcal F$ are pairwise disjoint and $\bigcup_{i}A_{i}=X$. The integral of $f$ with respect to $\mu$ is $\int_{X}f\,\mathrm{d}\mu=\sum_{i=1}^{n}c_{i}\mu\left(A_{i}\right)$, with the convention $0\cdot\infty=0$.

> **Proposition 8.1.2 (Linearity of the Integral for Simple Functions)**<br>Let $f,g$ be nonnegative simple functions and $\alpha,\beta\ge0$. Then $\int_{X}\left(\alpha f+\beta g\right)\mathrm{d}\mu=\alpha\int_{X}f\,\mathrm{d}\mu+\beta\int_{X}g\,\mathrm{d}\mu$.

> **Definition 8.2.1 (Integral of a Nonnegative Measurable Function)**<br>Let $f:X\to\left[0,+\infty\right]$ be a nonnegative measurable function. The integral of $f$ with respect to $\mu$ is $\int_{X}f\,\mathrm{d}\mu=\sup\left\{\int_{X}\phi\,\mathrm{d}\mu:\phi\text{ simple},0\le\phi\le f\right\}$. If $\int_{X}f\,\mathrm{d}\mu< \infty$, $f$ is called integrable.

> **Theorem 8.2.2 (Monotone Convergence Theorem)**<br>Let $\left(X,\mathcal F,\mu\right)$ be a measure space and $\left\{f_{n}\right\}$ a sequence of nonnegative measurable functions with $0\le f_{1}\left(x\right)\le f_{2}\left(x\right)\le\cdots$ for all $x\in X$, and $f_{n}\to f$ pointwise. Then $\lim_{n\to\infty}\int_{X}f_{n}\,\mathrm{d}\mu=\int_{X}f\,\mathrm{d}\mu$.

> **Remark 8.2.3 (Approximation by Simple Functions)**<br>The monotone convergence theorem tells us that the integral can be approximated by simple functions.

> **Proposition 8.2.4 (Absolute Continuity of the Integral with Respect to the Set)**<br>Let $f$ be a nonnegative measurable function. Then $A\mapsto\int_{A}f\,\mathrm{d}\mu$ is a measure; if $\mu\left(A\right)=0$, then $\int_{A}f\,\mathrm{d}\mu=0$.

> **Definition 8.2.5 (Integral of a General Measurable Function)**<br>Let $f:X\to\left[-\infty,+\infty\right]$ be measurable. Define its positive and negative parts by $f^{+}\left(x\right)=\max\left\{f\left(x\right),0\right\}$, $f^{-}\left(x\right)=\max\left\{-f\left(x\right),0\right\}$. If at least one of $\int_{X}f^{+}\mathrm{d}\mu$, $\int_{X}f^{-}\mathrm{d}\mu$ is finite, define the integral by $\int_{X}f\,\mathrm{d}\mu=\int_{X}f^{+}\mathrm{d}\mu-\int_{X}f^{-}\mathrm{d}\mu$. If both are finite, $f$ is called integrable.

> **Theorem 8.2.7 (Fatou's Lemma)**<br>Let $\left(X,\mathcal F,\mu\right)$ be a measure space and $\left\{f_{n}\right\}$ a sequence of nonnegative measurable functions. Then $\int_{X}\liminf_{n\to\infty}f_{n}\,\mathrm{d}\mu\le\liminf_{n\to\infty}\int_{X}f_{n}\,\mathrm{d}\mu$.

> **Theorem 8.2.9 (Dominated Convergence Theorem)**<br>Let $\left(X,\mathcal F,\mu\right)$ be a measure space, $\left\{f_{n}\right\}$ a sequence of measurable functions with $f_{n}\to f$ almost everywhere. If there exists an integrable function $g$ such that $\left|f_{n}\right|\le g$ almost everywhere for all $n$, then $\lim_{n\to\infty}\int_{X}f_{n}\,\mathrm{d}\mu=\int_{X}f\,\mathrm{d}\mu$.

> **Lemma 8.2.13 (Termwise Integration of Series)**<br>Let $\left\{f_{n}\right\}$ be a sequence of measurable functions with $\sum_{n=1}^{\infty}\int_{X}\left|f_{n}\right|\mathrm{d}\mu< \infty$. Then $\int_{X}\left(\sum_{n=1}^{\infty}f_{n}\right)\mathrm{d}\mu=\sum_{n=1}^{\infty}\int_{X}f_{n}\,\mathrm{d}\mu$.

> **Theorem 8.2.17 (Parameter Integrals)**<br>Let $f:X\times\left[a,b\right]\to\mathbb R$, and for each $t\in\left[a,b\right]$ let $f\left(\cdot,t\right):X\to\mathbb R$ be integrable. Set $F\left(t\right)=\int_{X}f\left(x,t\right)\mathrm{d}\mu\left(x\right)$. (a) If there exists $g\in L^{1}\left(\mu\right)$ with $\left|f\left(x,t\right)\right|\le g\left(x\right)$ for all $x,t$, and $\lim_{t\to t_{0}}f\left(x,t\right)=f\left(x,t_{0}\right)$ for each $x$, then $\lim_{t\to t_{0}}F\left(t\right)=F\left(t_{0}\right)$; (b) if the partial derivative $\partial f/\partial t$ exists and there is $g\in L^{1}\left(\mu\right)$ with $\left|\frac{\partial f}{\partial t}\left(x,t\right)\right|\le g\left(x\right)$ for all $x,t$, then $F$ is differentiable and $F'\left(t\right)=\int\frac{\partial f}{\partial t}\left(x,t\right)\mathrm{d}\mu\left(x\right)$.

---

## 1

Let $f$ be a nonnegative simple function. Prove that $A\mapsto\int_{A}f\,\mathrm{d}\mu$ is a measure, and that if $\mu\left(A\right)=0$, then $\int_{A}f\,\mathrm{d}\mu=0$.

### Solution 1

Write $f=\sum_{i=1}^{n}c_{i}\chi_{A_{i}}$, where $c_{i}\ge0$, the $A_{i}\in\mathcal F$ are pairwise disjoint and $\bigcup_{i}A_{i}=X$. For $E\in\mathcal F$, by **Definition 8.1.1 (Integral of a Nonnegative Simple Function)**,

$$
\int_{E}f\,\mathrm{d}\mu=\int f\chi_{E}\,\mathrm{d}\mu=\sum_{i=1}^{n}c_{i}\mu\left(E\cap A_{i}\right).
$$

Let $\lambda\left(E\right):=\int_{E}f\,\mathrm{d}\mu$. Verify that $\lambda$ is a measure: $\lambda\left(\emptyset\right)=\sum_{i=1}^{n}c_{i}\mu\left(\emptyset\cap A_{i}\right)=0$; nonnegativity is clear since $c_{i}\ge0$ and $\mu\ge0$; countable additivity: let $E=\bigsqcup_{j=1}^{\infty}E_{j}$ (pairwise disjoint). By countable additivity of $\mu$ (**Definition 5.1.2 (Measure)**) and **Proposition 8.1.2 (Linearity of the Integral for Simple Functions)**,

$$
\lambda\left(E\right)=\sum_{i=1}^{n}c_{i}\mu\left(E\cap A_{i}\right)=\sum_{i=1}^{n}c_{i}\sum_{j=1}^{\infty}\mu\left(E_{j}\cap A_{i}\right)=\sum_{j=1}^{\infty}\sum_{i=1}^{n}c_{i}\mu\left(E_{j}\cap A_{i}\right)=\sum_{j=1}^{\infty}\lambda\left(E_{j}\right).
$$

Thus $\lambda$ is a measure on $\mathcal F$. Finally, if $\mu\left(A\right)=0$, then

$$
\lambda\left(A\right)=\sum_{i=1}^{n}c_{i}\mu\left(A\cap A_{i}\right)\le\sum_{i=1}^{n}c_{i}\mu\left(A\right)=0,
$$

so $\lambda\left(A\right)=0$. $\blacksquare$

---

## 2

Let $f,g$ be integrable and $a,b\in\mathbb R$. Prove:

1. Linearity: $\int_{X}\left(af+bg\right)\mathrm{d}\mu=a\int_{X}f\,\mathrm{d}\mu+b\int_{X}g\,\mathrm{d}\mu$;

2. Monotonicity: if $f\le g$ almost everywhere, then $\int_{X}f\,\mathrm{d}\mu\le\int_{X}g\,\mathrm{d}\mu$;

3. Triangle inequality: $\left|\int_{X}f\,\mathrm{d}\mu\right|\le\int_{X}\left|f\right|\mathrm{d}\mu$;

4. If $f=g$ almost everywhere, then $\int_{X}f\,\mathrm{d}\mu=\int_{X}g\,\mathrm{d}\mu$.

### Solution 2

First establish linearity for nonnegative measurable functions. Let $\phi,\psi$ be nonnegative measurable and $\alpha,\beta\ge0$. By **Remark 8.2.3 (Approximation by Simple Functions)**, there are simple functions $\phi_{k}\uparrow\phi$, $\psi_{k}\uparrow\psi$. By **Proposition 8.1.2 (Linearity of the Integral for Simple Functions)**,

$$
\int\left(\alpha\phi_{k}+\beta\psi_{k}\right)\mathrm{d}\mu=\alpha\int\phi_{k}\,\mathrm{d}\mu+\beta\int\psi_{k}\,\mathrm{d}\mu.
$$

Since $\alpha\phi_{k}+\beta\psi_{k}\uparrow\alpha\phi+\beta\psi$, taking limits by **Theorem 8.2.2 (Monotone Convergence Theorem)** gives

$$
\int\left(\alpha\phi+\beta\psi\right)\mathrm{d}\mu=\alpha\int\phi\,\mathrm{d}\mu+\beta\int\psi\,\mathrm{d}\mu.
$$

Now let $f,g$ be integrable, with positive and negative parts $f^{+},f^{-}$ (**Definition 8.2.5 (Integral of a General Measurable Function)**).

1. First for scalar multiplication: if $a\ge0$, then $\left(af\right)^{+}=af^{+}$, $\left(af\right)^{-}=af^{-}$, so $\int\left(af\right)\mathrm{d}\mu=a\int f^{+}\mathrm{d}\mu-a\int f^{-}\mathrm{d}\mu=a\int f\,\mathrm{d}\mu$; if $a< 0$, then $\left(af\right)^{+}=\left|a\right|f^{-}$, $\left(af\right)^{-}=\left|a\right|f^{+}$, and similarly $\int\left(af\right)\mathrm{d}\mu=a\int f\,\mathrm{d}\mu$; $a=0$ is trivial. For addition, decompose by positive/negative parts: $f+g=\left(f^{+}+g^{+}\right)-\left(f^{-}+g^{-}\right)$, i.e.

$$
\left(f+g\right)^{+}+f^{-}+g^{-}=\left(f+g\right)^{-}+f^{+}+g^{+},
$$

both sides are nonnegative measurable, and integrating by nonneg linearity,

$$
\int\left(f+g\right)^{+}\mathrm{d}\mu+\int f^{-}\mathrm{d}\mu+\int g^{-}\mathrm{d}\mu=\int\left(f+g\right)^{-}\mathrm{d}\mu+\int f^{+}\mathrm{d}\mu+\int g^{+}\mathrm{d}\mu,
$$

and rearranging (all terms finite since $f,g$ are integrable) gives $\int\left(f+g\right)\mathrm{d}\mu=\int f\,\mathrm{d}\mu+\int g\,\mathrm{d}\mu$. Combining gives $\int\left(af+bg\right)\mathrm{d}\mu=a\int f\,\mathrm{d}\mu+b\int g\,\mathrm{d}\mu$.

2. By linearity, $\int g\,\mathrm{d}\mu-\int f\,\mathrm{d}\mu=\int\left(g-f\right)\mathrm{d}\mu$. Since $f\le g$ a.e., $g-f\ge0$ a.e. By **Definition 8.2.1 (Integral of a Nonnegative Measurable Function)**, the integral of a nonnegative measurable function is nonnegative (it is a supremum of integrals of nonnegative simple functions), so $\int\left(g-f\right)\mathrm{d}\mu\ge0$, i.e. $\int f\,\mathrm{d}\mu\le\int g\,\mathrm{d}\mu$.

3. $\left|f\right|=f^{+}+f^{-}$, and by nonneg linearity $\int\left|f\right|\mathrm{d}\mu=\int f^{+}\mathrm{d}\mu+\int f^{-}\mathrm{d}\mu$. Since $\int f\,\mathrm{d}\mu=\int f^{+}\mathrm{d}\mu-\int f^{-}\mathrm{d}\mu$,

$$
\left|\int f\,\mathrm{d}\mu\right|=\left|\int f^{+}\mathrm{d}\mu-\int f^{-}\mathrm{d}\mu\right|\le\int f^{+}\mathrm{d}\mu+\int f^{-}\mathrm{d}\mu=\int\left|f\right|\mathrm{d}\mu.
$$

4. If $f=g$ a.e., then $f^{+}=g^{+}$ and $f^{-}=g^{-}$ a.e. Thus $h:=f^{+}-g^{+}$ is integrable and $h=0$ a.e.; its positive part $h^{+}$ and negative part $h^{-}$ vanish outside a null set. By **Proposition 8.2.4 (Absolute Continuity of the Integral with Respect to the Set)**, $\int h^{+}\mathrm{d}\mu=\int_{\left\{h> 0\right\}}h^{+}\mathrm{d}\mu=0$ and $\int h^{-}\mathrm{d}\mu=0$, so $\int h\,\mathrm{d}\mu=0$, i.e. $\int f^{+}\mathrm{d}\mu=\int g^{+}\mathrm{d}\mu$; similarly $\int f^{-}\mathrm{d}\mu=\int g^{-}\mathrm{d}\mu$. Hence $\int f\,\mathrm{d}\mu=\int g\,\mathrm{d}\mu$. $\blacksquare$

---

## 3

Let $f\in L^{1}$. Prove:

(a) the set $\left\{x:f\left(x\right)\ne0\right\}$ is $\sigma$-finite;

(b) for $f,g\in L^{1}$, $\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\mu$ for every measurable $E$ iff $\int\left|f-g\right|\mathrm{d}\mu=0$ iff $f=g$ almost everywhere.

### Solution 3

(a) By **Definition 8.2.5 (Integral of a General Measurable Function)**, $f=f^{+}-f^{-}$, so $\left\{x:f\left(x\right)\ne0\right\}=\left\{x:f^{+}\left(x\right)> 0\right\}\cup\left\{x:f^{-}\left(x\right)> 0\right\}$. Moreover,

$$
\left\{x:f^{+}\left(x\right)> 0\right\}=\bigcup_{n=1}^{\infty}\left\{x:f^{+}\left(x\right)> \frac{1}{n}\right\},
$$

and by **Definition 8.2.1 (Integral of a Nonnegative Measurable Function)**,

$$
\int_{X}f^{+}\mathrm{d}\mu\ge\int_{\left\{f^{+}> \frac{1}{n}\right\}}f^{+}\mathrm{d}\mu\ge\frac{1}{n}\mu\left(\left\{x:f^{+}\left(x\right)> \frac{1}{n}\right\}\right).
$$

Since $f$ is integrable, $\int f^{+}\mathrm{d}\mu< \infty$, so $\mu\left(\left\{x:f^{+}\left(x\right)> \frac{1}{n}\right\}\right)\le n\int f^{+}\mathrm{d}\mu< \infty$. Thus $\left\{f^{+}> 0\right\}$ is a countable union of finite-measure sets; similarly for $\left\{f^{-}> 0\right\}$. Hence $\left\{x:f\left(x\right)\ne0\right\}$ is also a countable union of finite-measure sets, i.e. $\sigma$-finite in the sense of **Definition 5.1.5 ($\sigma$-Finite Measure)**. $\blacksquare$

(b) Let $h:=\left|f-g\right|\in L^{1}$, $h\ge0$.

(1) $\int\left|f-g\right|\mathrm{d}\mu=0\Rightarrow f=g$ a.e.: by **Basic Knowledge: Nonnegative Integrable Function with Zero Integral Vanishes Almost Everywhere**, $h=0$ a.e., i.e. $f=g$ a.e.

(2) $f=g$ a.e. $\Rightarrow\int\left|f-g\right|\mathrm{d}\mu=0$: since $h=0$ outside $\left\{f\ne g\right\}$ and $\left\{f\ne g\right\}$ is null. By **Proposition 8.2.4 (Absolute Continuity of the Integral with Respect to the Set)**, $\int_{\left\{f\ne g\right\}}h\,\mathrm{d}\mu=0$ and $\int_{\left\{f=g\right\}}h\,\mathrm{d}\mu=0$, so $\int h\,\mathrm{d}\mu=0$.

(3) $\int\left|f-g\right|\mathrm{d}\mu=0\Rightarrow\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\mu$ for all $E$: by Exercise 2, items 1 and 3,

$$
\left|\int_{E}f\,\mathrm{d}\mu-\int_{E}g\,\mathrm{d}\mu\right|=\left|\int_{E}\left(f-g\right)\mathrm{d}\mu\right|\le\int_{E}\left|f-g\right|\mathrm{d}\mu\le\int_{X}\left|f-g\right|\mathrm{d}\mu=0.
$$

(4) $\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\mu$ for all $E$ $\Rightarrow\int\left|f-g\right|\mathrm{d}\mu=0$: take $E:=\left\{x:f\left(x\right)\ge g\left(x\right)\right\}\in\mathcal F$. By linearity (Exercise 2, item 1), $\int_{E}\left(f-g\right)\mathrm{d}\mu=\int_{E}f\,\mathrm{d}\mu-\int_{E}g\,\mathrm{d}\mu=0$; on $E$, $f-g\ge0$, so $\int_{E}\left|f-g\right|\mathrm{d}\mu=\int_{E}\left(f-g\right)\mathrm{d}\mu=0$. Similarly, for $E^{c}$, $\int_{E^{c}}\left(g-f\right)\mathrm{d}\mu=0$, and on $E^{c}$, $g-f\ge0$, so $\int_{E^{c}}\left|f-g\right|\mathrm{d}\mu=0$. Hence $\int\left|f-g\right|\mathrm{d}\mu=\int_{E}\left|f-g\right|\mathrm{d}\mu+\int_{E^{c}}\left|f-g\right|\mathrm{d}\mu=0$.

Combining (1)(2)(3)(4), the three conditions are equivalent. $\blacksquare$

---

## 4

Prove:

**14.** If $f\in L^{+}$, set $\lambda\left(E\right)=\int_{E}f\,\mathrm{d}\mu$ (for $E\in\mathcal M$). Then $\lambda$ is a measure on $\mathcal M$, and for any $g\in L^{+}$, $\int g\,\mathrm{d}\lambda=\int fg\,\mathrm{d}\mu$.

**16.** If $f\in L^{+}$ and $\int f< \infty$, then for every $\varepsilon> 0$ there exists $E\in\mathcal M$ with $\mu\left(E\right)< \infty$ and $\int_{E}f> \left(\int f\right)-\varepsilon$.

### Solution 4

**14.** First show $\lambda$ is a measure. By **Definition 8.1.1 (Integral of a Nonnegative Simple Function)** and **Definition 8.2.1 (Integral of a Nonnegative Measurable Function)**, $\lambda\left(\emptyset\right)=0$ and nonnegativity. For pairwise disjoint measurable sets $\left\{E_{n}\right\}$, since $f\chi_{\bigsqcup E_{n}}=\sum_{n}f\chi_{E_{n}}$ and the partial sums $\sum_{n=1}^{N}f\chi_{E_{n}}\uparrow f\chi_{\bigsqcup E_{n}}$ pointwise, by **Theorem 8.2.2 (Monotone Convergence Theorem)**,

$$
\lambda\left(\bigsqcup_{n=1}^{\infty}E_{n}\right)=\int f\chi_{\bigsqcup E_{n}}\mathrm{d}\mu=\sum_{n=1}^{\infty}\int f\chi_{E_{n}}\mathrm{d}\mu=\sum_{n=1}^{\infty}\lambda\left(E_{n}\right).
$$

Thus $\lambda$ is a measure on $\mathcal M$.

Now prove the change-of-variables formula. If $g=\sum_{j=1}^{m}a_{j}\chi_{E_{j}}$ is simple (with $E_{j}$ pairwise disjoint), by **Definition 8.1.1 (Integral of a Nonnegative Simple Function)** and finite linearity,

$$
\int g\,\mathrm{d}\lambda=\sum_{j=1}^{m}a_{j}\lambda\left(E_{j}\right)=\sum_{j=1}^{m}a_{j}\int_{E_{j}}f\,\mathrm{d}\mu=\int\left(\sum_{j=1}^{m}a_{j}\chi_{E_{j}}f\right)\mathrm{d}\mu=\int fg\,\mathrm{d}\mu.
$$

For general $g\in L^{+}$, take simple $g_{k}\uparrow g$ by **Remark 8.2.3 (Approximation by Simple Functions)**. Since $f\ge0$, $fg_{k}\uparrow fg$. By **Theorem 8.2.2 (Monotone Convergence Theorem)** (under measures $\lambda$ and $\mu$ respectively), $\int g_{k}\,\mathrm{d}\lambda\uparrow\int g\,\mathrm{d}\lambda$ and $\int fg_{k}\,\mathrm{d}\mu\uparrow\int fg\,\mathrm{d}\mu$. For each $k$ the two agree (simple case), so the limits agree: $\int g\,\mathrm{d}\lambda=\int fg\,\mathrm{d}\mu$. $\blacksquare$

**16.** For $n\in\mathbb N$, let $E_{n}:=\left\{x:f\left(x\right)> \frac{1}{n}\right\}\in\mathcal M$. Then $\left\{E_{n}\right\}$ is increasing and $\bigcup_{n}E_{n}=\left\{x:f\left(x\right)> 0\right\}$. By **Definition 8.2.1 (Integral of a Nonnegative Measurable Function)**,

$$
\int f\,\mathrm{d}\mu\ge\int_{E_{n}}f\,\mathrm{d}\mu\ge\frac{1}{n}\mu\left(E_{n}\right),
$$

so $\mu\left(E_{n}\right)\le n\int f\,\mathrm{d}\mu< \infty$. Also by **Theorem 8.2.2 (Monotone Convergence Theorem)**, $\int_{E_{n}}f\,\mathrm{d}\mu\uparrow\int_{\left\{f> 0\right\}}f\,\mathrm{d}\mu=\int f\,\mathrm{d}\mu$. Thus for given $\varepsilon> 0$, choose $n$ large enough that $\int_{E_{n}}f\,\mathrm{d}\mu> \int f\,\mathrm{d}\mu-\varepsilon$, and set $E:=E_{n}$; then $\mu\left(E\right)< \infty$ and $\int_{E}f> \int f-\varepsilon$. $\blacksquare$

---

## 5

Prove:

**20.** (Generalized dominated convergence) If $f_{n},g_{n},f,g\in L^{1}$, $f_{n}\to f$ and $g_{n}\to g$ a.e., $\left|f_{n}\right|\le g_{n}$, and $\int g_{n}\to\int g$, then $\int f_{n}\to\int f$.

**23.** Let $f:\left[a,b\right]\to\mathbb R$ be bounded, and set

$$
H\left(x\right)=\limsup_{\delta\to0}\sup_{0< \left|y-x\right|\le\delta}f\left(y\right),\qquad h\left(x\right)=\liminf_{\delta\to0}\inf_{0< \left|y-x\right|\le\delta}f\left(y\right).
$$

Prove: (a) $H\left(x\right)=h\left(x\right)$ iff $f$ is continuous at $x$; (b) $H=G$ a.e., $h=g$ a.e., and $\int_{\left(a,b\right)}h\,\mathrm{d}m=\underline{\int}f$. Hence $f$ is Riemann integrable iff its set of discontinuities has measure 0.

**27.** Let $f_{n}\left(x\right)=ae^{-nax}-be^{-nbx}$ with $0< a< b$. (a) $\sum_{n=1}^{\infty}\int_{0}^{\infty}\left|f_{n}\left(x\right)\right|\mathrm{d}x=\infty$; (b) $\sum_{n=1}^{\infty}\int_{0}^{\infty}f_{n}\left(x\right)\mathrm{d}x=0$; (c) $\sum_{n=1}^{\infty}f_{n}\in L^{1}\left(\left[0,\infty\right),m\right)$ and $\int_{0}^{\infty}\sum_{n=1}^{\infty}f_{n}\left(x\right)\mathrm{d}x=\log\left(b/a\right)$.

**29.** By differentiating $\int_{0}^{\infty}e^{-tx}\mathrm{d}x=1/t$, prove $\int_{0}^{\infty}x^{n}e^{-x}\mathrm{d}x=n!$; similarly, by differentiating $\int_{-\infty}^{\infty}e^{-tx^{2}}\mathrm{d}x=\sqrt{\pi/t}$, prove $\int_{-\infty}^{\infty}x^{2n}e^{-x^{2}}\mathrm{d}x=\frac{\left(2n\right)!\sqrt\pi}{4^{n}n!}$.

### Solution 5

**20.** Since $g_{n}\to g$ a.e. and $\left|f_{n}\right|\le g_{n}$, taking limits gives $\left|f\right|\le g$ a.e., so $f\in L^{1}$. Since $\left|f_{n}\right|\le g_{n}$ means $-g_{n}\le f_{n}\le g_{n}$, the sequences $\left\{g_{n}+f_{n}\right\}$ and $\left\{g_{n}-f_{n}\right\}$ are nonnegative and converge a.e. to $g+f$ and $g-f$ respectively. By **Theorem 8.2.7 (Fatou's Lemma)**,

$$
\int\left(g+f\right)\mathrm{d}\mu\le\liminf_{n\to\infty}\int\left(g_{n}+f_{n}\right)\mathrm{d}\mu=\int g\,\mathrm{d}\mu+\liminf_{n\to\infty}\int f_{n}\,\mathrm{d}\mu,
$$

since $\int g_{n}\to\int g$ and the integrals are finite (linearity, Exercise 2). Subtracting $\int g\,\mathrm{d}\mu$ gives $\int f\,\mathrm{d}\mu\le\liminf_{n\to\infty}\int f_{n}\,\mathrm{d}\mu$. Similarly, applying Fatou to $\left\{g_{n}-f_{n}\right\}$,

$$
\int\left(g-f\right)\mathrm{d}\mu\le\liminf_{n\to\infty}\int\left(g_{n}-f_{n}\right)\mathrm{d}\mu=\int g\,\mathrm{d}\mu-\limsup_{n\to\infty}\int f_{n}\,\mathrm{d}\mu,
$$

i.e. $\limsup_{n\to\infty}\int f_{n}\,\mathrm{d}\mu\le\int f\,\mathrm{d}\mu$. Combining,

$$
\int f\,\mathrm{d}\mu\le\liminf_{n\to\infty}\int f_{n}\,\mathrm{d}\mu\le\limsup_{n\to\infty}\int f_{n}\,\mathrm{d}\mu\le\int f\,\mathrm{d}\mu,
$$

so $\lim_{n\to\infty}\int f_{n}\,\mathrm{d}\mu=\int f\,\mathrm{d}\mu$. $\blacksquare$

**23.** Use the notation of **Basic Knowledge: Riemann Integral and Darboux Sums**. $f$ is Riemann integrable iff $\overline{\int}f=\underline{\int}f$.

(a) Suppose $f$ is continuous at $x$. For $\varepsilon> 0$ there exists $\delta> 0$ such that $\left|y-x\right|< \delta\Rightarrow\left|f\left(y\right)-f\left(x\right)\right|< \varepsilon$. Then for $0< \left|y-x\right|\le\delta$,

$$
f\left(x\right)-\varepsilon\le\inf_{0< \left|y-x\right|\le\delta}f\left(y\right)\le f\left(x\right)\le\sup_{0< \left|y-x\right|\le\delta}f\left(y\right)\le f\left(x\right)+\varepsilon.
$$

Letting $\delta\to0$ and using the arbitrariness of $\varepsilon$, $h\left(x\right)\ge f\left(x\right)\ge H\left(x\right)$; but by definition always $h\left(x\right)\le f\left(x\right)\le H\left(x\right)$, so $H\left(x\right)=h\left(x\right)=f\left(x\right)$.

Conversely, suppose $H\left(x\right)=h\left(x\right)=:L$. For $\varepsilon> 0$, by the definition of the limits there exists $\delta> 0$ such that for $0< \delta'< \delta$,

$$
\inf_{0< \left|y-x\right|\le\delta'}f\left(y\right)> L-\varepsilon,\qquad\sup_{0< \left|y-x\right|\le\delta'}f\left(y\right)< L+\varepsilon.
$$

Taking $\delta'=\delta$, for $0< \left|y-x\right|\le\delta$ we have $L-\varepsilon< f\left(y\right)< L+\varepsilon$; also $f\left(x\right)$ lies between the inf and sup, so $L-\varepsilon< f\left(x\right)< L+\varepsilon$. Hence $\left|f\left(y\right)-f\left(x\right)\right|< 2\varepsilon$ for $0< \left|y-x\right|\le\delta$, i.e. $f$ is continuous at $x$.

(b) Take a sequence of partitions $\left\{P_{k}\right\}$ with mesh $\max_{i}\left(t_{i}-t_{i-1}\right)\to0$ and $P_{k}\subset P_{k+1}$ (successive refinement), define

$$
G_{P_{k}}=\sum_{i}M_{i}^{\left(k\right)}\chi_{\left(t_{i-1}^{\left(k\right)},t_{i}^{\left(k\right)}\right)},\qquad g_{P_{k}}=\sum_{i}m_{i}^{\left(k\right)}\chi_{\left(t_{i-1}^{\left(k\right)},t_{i}^{\left(k\right)}\right)},
$$

and set $G=\lim_{k}G_{P_{k}}$, $g=\lim_{k}g_{P_{k}}$. Fix $x$ not a partition point of any $P_{k}$ (the union of all partition points is at most countable, measure 0). Suppose $x\in\left(t_{i-1}^{\left(k\right)},t_{i}^{\left(k\right)}\right)$; then $G_{P_{k}}\left(x\right)=M_{i}^{\left(k\right)}=\sup_{\left[t_{i-1}^{\left(k\right)},t_{i}^{\left(k\right)}\right]}f$. As $k\to\infty$ the interval shrinks to $\left\{x\right\}$, and the supremum decreases to the limit of $\sup_{0< \left|y-x\right|\le\delta}f\left(y\right)$ as $\delta\to0$, i.e. $H\left(x\right)$. Hence $G\left(x\right)=H\left(x\right)$; similarly $g\left(x\right)=h\left(x\right)$. Thus after removing the countable set of partition points from $\left[a,b\right]$, $H=G$ and $h=g$ almost everywhere.

Also $G_{P_{k}}$ is bounded and $g_{P_{k}}\le f\le G_{P_{k}}$. By **Theorem 8.2.9 (Dominated Convergence Theorem)**,

$$
\int H\,\mathrm{d}m=\int G\,\mathrm{d}m=\lim_{k}\int G_{P_{k}}\mathrm{d}m=\lim_{k}\overline S\left(P_{k}\right)=\overline{\int}f,
$$

$$
\int h\,\mathrm{d}m=\int g\,\mathrm{d}m=\lim_{k}\int g_{P_{k}}\mathrm{d}m=\lim_{k}\underline S\left(P_{k}\right)=\underline{\int}f.
$$

In particular $\int_{\left(a,b\right)}h\,\mathrm{d}m=\underline{\int}f$. Hence

$$
f\text{ Riemann integrable}\iff\overline{\int}f=\underline{\int}f\iff\int H\,\mathrm{d}m=\int h\,\mathrm{d}m\iff\int\left(H-h\right)\mathrm{d}m=0.
$$

Since $H\ge h$, by Exercise 3(b), $\int\left(H-h\right)\mathrm{d}m=0\iff H=h$ a.e. Combined with (a) ($H=h\iff f$ continuous at $x$), $f$ is Riemann integrable iff its discontinuity set has measure 0. Then the Riemann integral $\overline{\int}f=\int H\,\mathrm{d}m=\int f\,\mathrm{d}m$ (since $H=f$ a.e.). $\blacksquare$

**27.** First find the zero of $f_{n}$. Setting $f_{n}\left(x\right)=0$ gives $ae^{-nax}=be^{-nbx}$, i.e. $e^{n\left(b-a\right)x}=b/a$, so the unique zero is

$$
x_{n}=\frac{\log\left(b/a\right)}{n\left(b-a\right)}.
$$

On $\left[0,x_{n}\right)$, $f_{n}< 0$, and on $\left(x_{n},\infty\right)$, $f_{n}> 0$.

(a) Compute

$$
\int_{0}^{\infty}\left|f_{n}\right|\mathrm{d}x=\int_{0}^{x_{n}}\left(be^{-nbx}-ae^{-nax}\right)\mathrm{d}x+\int_{x_{n}}^{\infty}\left(ae^{-nax}-be^{-nbx}\right)\mathrm{d}x.
$$

Using $\int_{0}^{x_{n}}be^{-nbx}\mathrm{d}x=\frac{1}{n}\left(1-e^{-nbx_{n}}\right)$, $\int_{0}^{x_{n}}ae^{-nax}\mathrm{d}x=\frac{1}{n}\left(1-e^{-nax_{n}}\right)$, $\int_{x_{n}}^{\infty}ae^{-nax}\mathrm{d}x=\frac{1}{n}e^{-nax_{n}}$, $\int_{x_{n}}^{\infty}be^{-nbx}\mathrm{d}x=\frac{1}{n}e^{-nbx_{n}}$, we get

$$
\int_{0}^{\infty}\left|f_{n}\right|\mathrm{d}x=\frac{2}{n}\left(e^{-nax_{n}}-e^{-nbx_{n}}\right).
$$

Let $t=e^{-nx_{n}}$. The zero condition gives $at^{a}=bt^{b}$, i.e. $t^{a-b}=b/a$, so $t=\left(b/a\right)^{1/\left(a-b\right)}\in\left(0,1\right)$. Since $t< 1$ and $a< b$, the power map $\lambda\mapsto t^{\lambda}$ is decreasing, so $t^{a}> t^{b}$, and the constant $c:=2\left(t^{a}-t^{b}\right)> 0$. Therefore

$$
\sum_{n=1}^{\infty}\int_{0}^{\infty}\left|f_{n}\right|\mathrm{d}x=c\sum_{n=1}^{\infty}\frac{1}{n}=\infty.
$$

(b) Termwise,

$$
\int_{0}^{\infty}f_{n}\left(x\right)\mathrm{d}x=\int_{0}^{\infty}ae^{-nax}\mathrm{d}x-\int_{0}^{\infty}be^{-nbx}\mathrm{d}x=\frac{1}{n}-\frac{1}{n}=0,
$$

so $\sum_{n=1}^{\infty}\int_{0}^{\infty}f_{n}\left(x\right)\mathrm{d}x=0$.

(c) By the geometric series $\sum_{n=1}^{\infty}e^{-nax}=\frac{e^{-ax}}{1-e^{-ax}}=\frac{1}{e^{ax}-1}$,

$$
\sum_{n=1}^{\infty}f_{n}\left(x\right)=a\sum_{n=1}^{\infty}e^{-nax}-b\sum_{n=1}^{\infty}e^{-nbx}=\frac{a}{e^{ax}-1}-\frac{b}{e^{bx}-1}.
$$

As $x\to0^{+}$, $\frac{a}{e^{ax}-1}=\frac{1}{x}-\frac{a}{2}+O\left(x\right)$, so the difference tends to $\frac{b-a}{2}+O\left(x\right)$ (finite); as $x\to\infty$, exponential decay. Hence $\sum f_{n}\in L^{1}\left(\left[0,\infty\right),m\right)$.

For $R> 0$, change variables $u=ax$ and $u=bx$:

$$
\int_{0}^{R}\frac{a}{e^{ax}-1}\mathrm{d}x=\int_{0}^{aR}\frac{\mathrm{d}u}{e^{u}-1},\qquad\int_{0}^{R}\frac{b}{e^{bx}-1}\mathrm{d}x=\int_{0}^{bR}\frac{\mathrm{d}u}{e^{u}-1}.
$$

Thus

$$
\int_{0}^{R}\left(\frac{a}{e^{ax}-1}-\frac{b}{e^{bx}-1}\right)\mathrm{d}x=\int_{aR}^{bR}\frac{\mathrm{d}u}{e^{u}-1}.
$$

Since $\frac{1}{e^{u}-1}-\frac{1}{u}=O\left(e^{-u}\right)$ is integrable at infinity, $\int_{aR}^{bR}\frac{\mathrm{d}u}{e^{u}-1}=\int_{aR}^{bR}\frac{\mathrm{d}u}{u}+o\left(1\right)$, and letting $R\to\infty$,

$$
\int_{0}^{\infty}\sum_{n=1}^{\infty}f_{n}\left(x\right)\mathrm{d}x=\lim_{R\to\infty}\int_{aR}^{bR}\frac{\mathrm{d}u}{u}=\log\left(b/a\right).
$$

Note that here $\sum\int\left|f_{n}\right|=\infty$ (by (a)), so the condition $\sum\int\left|f_{n}\right|< \infty$ of **Lemma 8.2.13 (Termwise Integration of Series)** fails, and termwise integration is not allowed; indeed $\int\sum f_{n}=\log\left(b/a\right)\ne\sum\int f_{n}=0$, showing that this condition is essential. $\blacksquare$

**29.** Use **Theorem 8.2.17 (Parameter Integrals)** (b) (differentiation under the integral). Fix $t_{0}> 0$ and work on a compact neighborhood $\left[t_{0}/2,t_{0}\right]$.

**Case 1.** Let $F\left(t\right)=\int_{0}^{\infty}e^{-tx}\mathrm{d}x=\frac{1}{t}$ ($t> 0$). For each $k\ge1$, on $t\in\left[t_{0}/2,t_{0}\right]$, $\left|\frac{\partial^{k}}{\partial t^{k}}e^{-tx}\right|=x^{k}e^{-tx}\le x^{k}e^{-\left(t_{0}/2\right)x}\in L^{1}\left(\left[0,\infty\right)\right)$, so the theorem applies repeatedly:

$$
F^{\left(n\right)}\left(t\right)=\int_{0}^{\infty}\left(-x\right)^{n}e^{-tx}\mathrm{d}x.
$$

Since $F\left(t\right)=1/t$, its $n$-th derivative is $F^{\left(n\right)}\left(t\right)=\left(-1\right)^{n}n!/t^{n+1}$. Setting $t=1$,

$$
\int_{0}^{\infty}\left(-x\right)^{n}e^{-x}\mathrm{d}x=\left(-1\right)^{n}n!,
$$

i.e. $\int_{0}^{\infty}x^{n}e^{-x}\mathrm{d}x=n!$.

**Case 2.** Let $G\left(s\right)=\int_{-\infty}^{\infty}e^{-sx^{2}}\mathrm{d}x=\sqrt{\pi/s}=\sqrt\pi\,s^{-1/2}$ ($s> 0$). For each $k\ge1$, on $s\in\left[s_{0}/2,s_{0}\right]$, $\left|\frac{\partial^{k}}{\partial s^{k}}e^{-sx^{2}}\right|=x^{2k}e^{-sx^{2}}\le x^{2k}e^{-\left(s_{0}/2\right)x^{2}}\in L^{1}\left(\mathbb R\right)$, so we may differentiate repeatedly:

$$
G^{\left(n\right)}\left(s\right)=\int_{-\infty}^{\infty}\left(-x^{2}\right)^{n}e^{-sx^{2}}\mathrm{d}x=\left(-1\right)^{n}\int_{-\infty}^{\infty}x^{2n}e^{-sx^{2}}\mathrm{d}x.
$$

Also,

$$
G^{\left(n\right)}\left(s\right)=\sqrt\pi\left(-\frac{1}{2}\right)\left(-\frac{3}{2}\right)\cdots\left(-\frac{2n-1}{2}\right)s^{-\frac{2n+1}{2}}.
$$

Setting $s=1$,

$$
\left(-1\right)^{n}\int_{-\infty}^{\infty}x^{2n}e^{-x^{2}}\mathrm{d}x=\sqrt\pi\left(-1\right)^{n}\frac{1\cdot3\cdots\left(2n-1\right)}{2^{n}},
$$

i.e. $\int_{-\infty}^{\infty}x^{2n}e^{-x^{2}}\mathrm{d}x=\sqrt\pi\frac{1\cdot3\cdots\left(2n-1\right)}{2^{n}}$. Since $1\cdot3\cdots\left(2n-1\right)=\frac{\left(2n\right)!}{2^{n}n!}$,

$$
\int_{-\infty}^{\infty}x^{2n}e^{-x^{2}}\mathrm{d}x=\frac{\left(2n\right)!\sqrt\pi}{4^{n}n!}.
$$

$\blacksquare$
