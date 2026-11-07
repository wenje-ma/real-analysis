# week3

> **Definition 1.3.1 (Limit Superior)**
> 
> The limit superior of a sequence of sets $\left\{E_{n}\right\}$ is

> **Definition 1.3.3 (Limit Inferior)**
> 
> The limit inferior of a sequence of sets $\left\{E_{n}\right\}$ is

> **Definition 4.1.1 (Algebra of Sets)**
> 
> Let $X$ be a nonempty set and $\mathcal{A}\subset\mathcal{P}\left(X\right)$. $\mathcal{A}$ is called an algebra of sets on $X$ if: (1) $X\in\mathcal{A}$; (2) closed under differences: $A,B\in\mathcal{A}\Rightarrow{A}\setminus{B}\in\mathcal{A}$; (3) closed under finite unions: $A,B\in\mathcal{A}\Rightarrow{A}\cup{B}\in\mathcal{A}$.

> **Definition 4.1.3 ($\sigma$-Algebra)**
> 
> Let $X$ be nonempty and $\mathcal{F}\subset\mathcal{P}\left(X\right)$. $\mathcal{F}$ is called a $\sigma$-algebra on $X$ if: (1) $X\in\mathcal{F}$; (2) closed under complements: $A\in\mathcal{F}\Rightarrow{A}^{c}\in\mathcal{F}$; (3) closed under countable unions: $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal{F}$.

> **Definition 4.4.1 (Monotone Class)**
> 
> Let $\mathcal{M}\subset\mathcal{P}\left(X\right)$. $\mathcal{M}$ is called a monotone class if: (1) closed under increasing sequences: $A_{1}\subset{A}_{2}\subset\cdots$ and $A_{n}\in\mathcal{M}\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal{M}$; (2) closed under decreasing sequences: $A_{1}\supset{A}_{2}\supset\cdots$ and $A_{n}\in\mathcal{M}\Rightarrow\bigcap_{n=1}^{\infty}A_{n}\in\mathcal{M}$.

> **Theorem 4.4.2 (Monotone Class Theorem)**
> 
> Let $\mathcal{A}$ be an algebra and $\mathcal{M}$ a monotone class containing $\mathcal{A}$. Then $\sigma\left(\mathcal{A}\right)\subset\mathcal{M}$.

> **Definition 5.1.2 (Measure)**
> 
> Let $\left(X,\mathcal{F}\right)$ be a measurable space. A function $\mu:\mathcal{F}\to\left[0,+\infty\right]$ is called a measure on $\left(X,\mathcal{F}\right)$ if: (1) nonnegativity: $\mu\left(E\right)\ge0$ for all $E\in\mathcal{F}$; (2) empty set: $\mu\left(\emptyset\right)=0$; (3) countable additivity ($\sigma$-additivity): for any countable pairwise-disjoint $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$, $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **Proposition 5.2.1 (Finite Additivity)**
> 
> Let $\mu$ be a measure on $\left(X,\mathcal{F}\right)$ and $E_{1},\dots,E_{n}\in\mathcal{F}$ be pairwise disjoint. Then

> **Proposition 5.2.2 (Monotonicity)**
> 
> Let $\mu$ be a measure and $E,F\in\mathcal{F}$ with $E\subset{F}$. Then $\mu\left(E\right)\le\mu\left(F\right)$. If moreover $\mu\left(E\right)<+\infty$, then $\mu\left(F\setminus{E}\right)=\mu\left(F\right)-\mu\left(E\right)$.

> **Proposition 5.2.3 (Countable Subadditivity)**
> 
> Let $\mu$ be a measure and $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$ be any countable collection of sets (not necessarily pairwise disjoint). Then

> **Proposition 5.2.4 (Continuity from Below)**
> 
> Let $\mu$ be a measure and $\left\{E_{n}\right\}$ increasing. Then $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\lim_{n\to\infty}\mu\left(E_{n}\right)$.

> **Proposition 5.2.5 (Continuity from Above)**
> 
> Let $\mu$ be a measure and $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{F}$ be a decreasing sequence of sets (i.e. $E_{1}\supset{E}_{2}\supset\cdots$), and suppose there exists $m$ with $\mu\left(E_{m}\right)<+\infty$. Then

> **Definition 5.4.1 (Null Set)**
> 
> Let $\left(X,\mathcal{F},\mu\right)$ be a measure space. A set $N\in\mathcal{F}$ is called a null set if $\mu\left(N\right)=0$.

> **Definition 5.4.2 (Zero-Measure Set)**
> 
> A set $A\subset{X}$ is called a zero-measure set if there exists $N\in\mathcal{F}$ such that $A\subset{N}$ and $\mu\left(N\right)=0$.

> **Definition 5.4.4 (Complete Measure)**
> 
> A measure space $\left(X,\mathcal{F},\mu\right)$ is called complete if for every $N\in\mathcal{F}$ with $\mu\left(N\right)=0$ and every $A\subset{N}$, we have $A\in\mathcal{F}$.

> **Theorem 5.4.6 (Completion Theorem for Measures)**
> 
> Every measure space $\left(X,\mathcal{F},\mu\right)$ can be completed, i.e. there exists a complete measure space $\left(X,\mathcal{M},\overline\mu\right)$ such that: (1) $\mathcal{F}\subset\mathcal{M}$; (2) $\overline\mu|_{\mathcal{F}}=\mu$; (3) $\mathcal{M}$ is the smallest complete $\sigma$-algebra containing $\mathcal{F}$. Explicitly, let $\mathcal{N}=\left\{N\in\mathcal{F}:\mu\left(N\right)=0\right\}$, $\mathcal{M}=\left\{A\subset{X}:\exists\,B\in\mathcal{F},\exists\,N\in\mathcal{N},B\subset{A}\subset{B}\cup{N}\right\}$, and define $\overline\mu\left(A\right)=\mu\left(B\right)$.

> **Definition 6.1.1 (Outer Measure)**
> 
> Let $X$ be nonempty. A function $\mu^{*}:\mathcal{P}\left(X\right)\to\left[0,+\infty\right]$ is called an outer measure on $X$ if: (1) nonnegativity: $\mu^{*}\left(\varnothing\right)=0$ and $\mu^{*}\left(E\right)\ge0$ for all $E\subset{X}$; (2) monotonicity: $E\subset{F}\Rightarrow\mu^{*}\left(E\right)\le\mu^{*}\left(F\right)$; (3) countable subadditivity: $\mu^{*}\left(\bigcup_{n=1}^{\infty}E_{n}\right)\le\sum_{n=1}^{\infty}\mu^{*}\left(E_{n}\right)$.

> **Definition 6.2.1 (Premeasure)**
> 
> Let $X$ be nonempty and $\mathcal{E}\subset\mathcal{P}\left(X\right)$ an algebra. A function $\mu_{0}:\mathcal{E}\to\left[0,+\infty\right]$ is called a premeasure if: (1) $\mu_{0}\left(\varnothing\right)=0$; (2) if $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal{E}$ are pairwise disjoint and $\bigcup_{n=1}^{\infty}E_{n}\in\mathcal{E}$, then $\mu_{0}\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu_{0}\left(E_{n}\right)$.

> **Theorem 6.2.2 (Outer Measure from a Premeasure)**
> 
> Let $\mathcal{E}\subset\mathcal{P}\left(X\right)$ be a covering class and $\mu_{0}:\mathcal{E}\to\left[0,+\infty\right]$ a premeasure. For any $A\subset{X}$, define

$$
\mu^{*}\left(A\right)=\inf\left\{\sum_{n=1}^{\infty}\mu_{0}\left(E_{n}\right):E_{n}\in\mathcal{E},A\subset\bigcup_{n=1}^{\infty}E_{n}\right\}.
$$
Then $\mu^{*}$ is an outer measure on $X$, and $\mu^{*}|_{\mathcal{E}}=\mu_{0}$.

> **Definition 6.3.1 (Carathéodory Condition)**
> 
> Let $\mu^{*}$ be an outer measure on $X$. A subset $A\subset{X}$ is called $\mu^{*}$-measurable if for every $T\subset{X}$,

$$
\mu^{*}\left(T\right)=\mu^{*}\left(T\cap{A}\right)+\mu^{*}\left(T\cap{A}^{c}\right).
$$
The collection of all $\mu^{*}$-measurable sets is denoted $\mathcal{M}_{\mu^{*}}$.

> **Lemma 6.3.2 (Algebra Contained in Measurable Sets)**
> 
> If $\mathcal{E}$ is an algebra and $\mu_{0}$ is a premeasure, then $\mathcal{E}\subset\mathcal{M}_{\mu^{*}}$.

> **Theorem 6.3.3 (Carathéodory's Theorem)**
> 
> Let $\mu^{*}$ be an outer measure on $X$. Then: (1) $\mathcal{M}$ is a $\sigma$-algebra; (2) $\mu^{*}|_{\mathcal{M}}$ is a complete measure; (3) if $\mu^{*}$ is generated by a premeasure $\mu_{0}$ and $\mu_{0}$ is $\sigma$-finite, then $\mu^{*}|_{\mathcal{M}}$ is the unique extension of $\mu_{0}$.

> **Definition 6.4.1 (h-Interval)**
> 
> Let $-\infty\le{a}<{}b<\infty$. All half-open intervals $\left(a,b\right]$, together with $\left(a,\infty\right)$ and $\varnothing$, are called h-intervals. The family of finite disjoint unions of h-intervals forms an algebra $\mathcal{E}$.

> **Proposition 6.4.2 (Premeasure on $\mathcal{E}$)**
> 
> Let $F:\mathbb{R}\to\mathbb{R}$ be increasing and right-continuous. For disjoint intervals $\left(a_{i},b_{i}\right]$, $i=1,\dots,n$, define $\mu_{0}\left(\bigcup_{i=1}^{n}\left(a_{i},b_{i}\right]\right):=\sum_{i=1}^{n}\left[F\left(b_{i}\right)-F\left(a_{i}\right)\right]$, and set $\mu_{0}\left(\varnothing\right)=0$. Then $\mu_{0}$ is a premeasure on $\mathcal{E}$.

> **Theorem 6.4.5 (Regularity of Lebesgue-Stieltjes Measure)**
> 
> Let $F:\mathbb{R}\to\mathbb{R}$ be right-continuous and increasing, $\mu_{F}$ the Lebesgue-Stieltjes measure generated by $F$, and $\mathcal{M}^{*}$ the $\sigma$-algebra of $\mu_{F}$-measurable sets. If $E\in\mathcal{M}^{*}$, then

$$
\mu_{F}\left(E\right)=\inf\left\{\mu_{F}\left(U\right):E\subset{U},U\text{~open}\right\}=\sup\left\{\mu_{F}\left(K\right):K\subset{E},K\text{~compact}\right\}.
$$

> **Definition 6.4.6 (Lebesgue Measure)**
> 
> The measure generated by $F\left(x\right)=x$ is called Lebesgue measure, denoted $m$; the measurable sets defined via the corresponding outer measure are called Lebesgue measurable sets, and their collection is denoted $\mathcal{L}$.

> **Definition 6.5.1 (Recursive Construction of the Cantor Set)**
> 
> Let $C_{0}=\left[0,1\right]$. For each $n\ge0$, define $C_{n+1}=\frac{1}{3}C_{n}\cup\left(\frac{2}{3}+\frac{1}{3}C_{n}\right)$. The Cantor set is defined as $C=\bigcap_{n=0}^{\infty}C_{n}$.

> **Theorem 6.5.2 (Ternary Characterization of the Cantor Set)**
> 
> A point $x\in\left[0,1\right]$ belongs to the Cantor set $C$ iff its ternary expansion $x=\sum_{k=1}^{\infty}\frac{a_{k}}{3^{k}}$ contains no digit $1$ (i.e. $a_{k}\in\left\{0,2\right\}$).

## 1

Let $\left(X,\mathcal{M},\mu\right)$ be a finite measure space.

(a) If $E,F\in\mathcal{M}$ and $\mu\left(E\triangle{F}\right)=0$, then $\mu\left(E\right)=\mu\left(F\right)$.

(b) Define $E\sim{F}$ iff $\mu\left(E\triangle{F}\right)=0$. Then $\sim$ is an equivalence relation on $\mathcal{M}$.

(c) For $E,F\in\mathcal{M}$, define $\rho\left(E,F\right):=\mu\left(E\triangle{F}\right)$. Prove that $\rho\left(E,F\right)\le\rho\left(E,G\right)+\rho\left(F,G\right)$, so that $\rho$ defines a metric on the quotient space $\mathcal{M}/\sim$.

### Solution to 1

(a) $E=\left(E\cap{F}\right)\cup\left(E\setminus{F}\right)$ and $F=\left(E\cap{F}\right)\cup\left(F\setminus{E}\right)$ are disjoint decompositions. By **Proposition 5.2.1 (Finite Additivity)**,

$$
\mu\left(E\right)=\mu\left(E\cap{F}\right)+\mu\left(E\setminus{F}\right),\quad\mu\left(F\right)=\mu\left(E\cap{F}\right)+\mu\left(F\setminus{E}\right).
$$

Since $E\setminus{F}\subset{E}\triangle{F}$ and $F\setminus{E}\subset{E}\triangle{F}$, by **Proposition 5.2.2 (Monotonicity)**, $\mu\left(E\setminus{F}\right)\le\mu\left(E\triangle{F}\right)=0$, and similarly $\mu\left(F\setminus{E}\right)=0$. Hence $\mu\left(E\right)=\mu\left(E\cap{F}\right)=\mu\left(F\right)$. $\blacksquare$

(b) Verify the three properties of an equivalence relation:

(1) Reflexivity: $\mu\left(E\triangle{E}\right)=\mu\left(\varnothing\right)=0$, so $E\sim{E}$.

(2) Symmetry: $E\triangle{F}=F\triangle{E}$, so $E\sim{F}\Leftrightarrow{F}\sim{E}$.

(3) Transitivity: since $E\triangle{G}\subset\left(E\triangle{F}\right)\cup\left(F\triangle{G}\right)$, by **Proposition 5.2.3 (Countable Subadditivity)**, $\mu\left(E\triangle{G}\right)\le\mu\left(E\triangle{F}\right)+\mu\left(F\triangle{G}\right)=0$, so $E\sim{G}$.

Thus $\sim$ is an equivalence relation on $\mathcal{M}$. $\blacksquare$

(c) Symmetry and nonnegativity are clear: $\rho\left(E,F\right)=\rho\left(F,E\right)\ge0$ and $\rho\left(E,E\right)=0$. Since $E\triangle{G}\subset\left(E\triangle{F}\right)\cup\left(F\triangle{G}\right)$, by **Proposition 5.2.3 (Countable Subadditivity)**,

$$
\rho\left(E,G\right)=\mu\left(E\triangle{G}\right)\le\mu\left(E\triangle{F}\right)+\mu\left(F\triangle{G}\right)=\rho\left(E,F\right)+\rho\left(F,G\right).
$$

Finally, verify well-definedness and positivity: if $E\sim{E}'$ and $F\sim{F}'$ (i.e. $\mu\left(E\triangle{E}'\right)=\mu\left(F\triangle{F}'\right)=0$), then

$$
E\triangle{F}\subset\left(E\triangle{E}'\right)\cup\left(E'\triangle{F}'\right)\cup\left(F'\triangle{F}\right),
$$

so $\rho\left(E,F\right)\le0+\rho\left(E',F'\right)+0=\rho\left(E',F'\right)$; symmetrically $\rho\left(E',F'\right)\le\rho\left(E,F\right)$, hence $\rho\left(E,F\right)=\rho\left(E',F'\right)$, i.e. $\rho$ is well-defined on the quotient $\mathcal{M}/\sim$. Moreover, $\rho\left(E,F\right)=0\Leftrightarrow\mu\left(E\triangle{F}\right)=0\Leftrightarrow{E}\sim{F}$, so $\rho$ is a metric on $\mathcal{M}/\sim$. $\blacksquare$

## 2

Prove the uniqueness in part (3) of **Theorem 6.3.3 (Carathéodory's Theorem)**, and prove exercises 17 and 24.

(1) Let $\mathcal{E}\subset\mathcal{P}\left(X\right)$ be an algebra, $\mu_{0}$ a $\sigma$-finite premeasure on $\mathcal{E}$, $\mu^{*}$ the outer measure generated by $\mu_{0}$, and $\mathcal{M}$ the collection of $\mu^{*}$-measurable sets. Prove that $\mu^{*}|_{\mathcal{M}}$ is the unique extension of $\mu_{0}$ to $\mathcal{M}$.

17. Let $\mu^{*}$ be an outer measure on $X$ and $\left\{A_{j}\right\}_{j=1}^{\infty}$ a sequence of pairwise disjoint $\mu^{*}$-measurable sets. Prove that for any $E\subset{X}$,

$$
\mu^{*}\left(E\cap\bigcup_{j=1}^{\infty}A_{j}\right)=\sum_{j=1}^{\infty}\mu^{*}\left(E\cap{A}_{j}\right).
$$

24. Let $\mu$ be a finite measure on $\left(X,\mathcal{M}\right)$ and $\mu^{*}$ the outer measure induced by $\mu$. Let $E\subset{X}$ satisfy $\mu^{*}\left(E\right)=\mu^{*}\left(X\right)$ (but $E$ need not belong to $\mathcal{M}$).

(a) If $A,B\in\mathcal{M}$ and $A\cap{E}=B\cap{E}$, then $\mu\left(A\right)=\mu\left(B\right)$.

(b) Let $\mathcal{M}_{E}=\left\{A\cap{E}:A\in\mathcal{M}\right\}$ and define $\nu\left(A\cap{E}\right)=\mu\left(A\right)$ on $\mathcal{M}_{E}$ (well-defined by (a)). Prove that $\mathcal{M}_{E}$ is a $\sigma$-algebra on $E$ and $\nu$ is a measure on $\mathcal{M}_{E}$.

### Solution to 2

(1) Uniqueness. By **Definition 6.2.1 (Premeasure)**, $\mu_{0}$ is a premeasure on the algebra $\mathcal{E}$. First show that $\mu^{*}|_{\mathcal{M}}$ is indeed an extension of $\mu_{0}$: by **Theorem 6.2.2 (Outer Measure from a Premeasure)**, $\mu^{*}|_{\mathcal{E}}=\mu_{0}$; by **Lemma 6.3.2 (Algebra Contained in Measurable Sets)**, $\mathcal{E}\subset\mathcal{M}$; by **Theorem 6.3.3 (Carathéodory's Theorem)** (1)(2), $\mathcal{M}$ is a $\sigma$-algebra and $\mu^{*}|_{\mathcal{M}}$ is a complete measure. Thus $\mu^{*}|_{\mathcal{M}}$ is a measure extension of $\mu_{0}$ to $\mathcal{M}$.

Now prove uniqueness. Let $\nu$ be any measure on $\mathcal{M}$ with $\nu|_{\mathcal{E}}=\mu_{0}$; we show $\nu=\mu^{*}|_{\mathcal{M}}$. First assume $\mu_{0}\left(X\right)<\infty$.

Step 1: $\nu\le\mu^{*}$ on $\mathcal{M}$. For any $A\in\mathcal{M}$ and $\varepsilon>0$, by the definition of $\mu^{*}$ in **Theorem 6.2.2 (Outer Measure from a Premeasure)**, there exists $\left\{E_{n}\right\}\subset\mathcal{E}$ covering $A$ with $\sum_{n}\mu_{0}\left(E_{n}\right)\le\mu^{*}\left(A\right)+\varepsilon$. By countable subadditivity of $\nu$ (**Proposition 5.2.3 (Countable Subadditivity)**) and $\nu|_{\mathcal{E}}=\mu_{0}$,

$$
\nu\left(A\right)\le\sum_{n}\nu\left(E_{n}\right)=\sum_{n}\mu_{0}\left(E_{n}\right)\le\mu^{*}\left(A\right)+\varepsilon.
$$

By the arbitrariness of $\varepsilon$, $\nu\left(A\right)\le\mu^{*}\left(A\right)$.

Step 2: $\nu=\mu^{*}$ on $\sigma\left(\mathcal{E}\right)$. Let $\mathcal{H}=\left\{A\in\sigma\left(\mathcal{E}\right):\nu\left(A\right)=\mu^{*}\left(A\right)\right\}$. For $E\in\mathcal{E}$, by **Theorem 6.2.2 (Outer Measure from a Premeasure)** and $\nu|_{\mathcal{E}}=\mu_{0}$, $\mu^{*}\left(E\right)=\mu_{0}\left(E\right)=\nu\left(E\right)$, so $\mathcal{E}\subset\mathcal{H}$. Verify that $\mathcal{H}$ is a monotone class (**Definition 4.4.1 (Monotone Class)**): if $\left\{A_{n}\right\}\subset\mathcal{H}$ and $A_{n}\uparrow{A}$, by continuity from below of $\nu,\mu^{*}|_{\mathcal{M}}$ (**Proposition 5.2.4 (Continuity from Below)**; $\sigma\left(\mathcal{E}\right)\subset\mathcal{M}$), $\nu\left(A\right)=\lim_{n}\nu\left(A_{n}\right)=\lim_{n}\mu^{*}\left(A_{n}\right)=\mu^{*}\left(A\right)$, so $A\in\mathcal{H}$; the decreasing case is analogous (here $\mu^{*}\left(A_{1}\right)\le\mu^{*}\left(X\right)=\mu_{0}\left(X\right)<\infty$, so continuity from above applies). Thus $\mathcal{H}$ is a monotone class containing the algebra $\mathcal{E}$, and by **Theorem 4.4.2 (Monotone Class Theorem)**, $\sigma\left(\mathcal{E}\right)\subset\mathcal{H}$, i.e. $\nu=\mu^{*}$ on $\sigma\left(\mathcal{E}\right)$.

Step 3: $\nu=\mu^{*}$ on $\mathcal{M}$. For any $A\in\mathcal{M}$, Step 1 gives $\nu\left(A\right)\le\mu^{*}\left(A\right)$. Since $X\in\mathcal{E}$ (**Definition 4.1.1 (Algebra of Sets)**), $\nu\left(X\right)=\mu_{0}\left(X\right)=\mu^{*}\left(X\right)$. Applying Step 1 to $A^{c}\in\mathcal{M}$ (since $\mathcal{M}$ is a $\sigma$-algebra, **Theorem 6.3.3 (Carathéodory's Theorem)** (1)), and using $A\in\mathcal{M}$ to get $\mu^{*}\left(X\right)=\mu^{*}\left(A\right)+\mu^{*}\left(A^{c}\right)$ (**Definition 6.3.1 (Carathéodory Condition)** at $T=X$),

$$
\nu\left(A\right)=\nu\left(X\right)-\nu\left(A^{c}\right)=\mu^{*}\left(X\right)-\nu\left(A^{c}\right)\ge\mu^{*}\left(X\right)-\mu^{*}\left(A^{c}\right)=\mu^{*}\left(A\right).
$$

Hence $\nu\left(A\right)=\mu^{*}\left(A\right)$. This proves uniqueness when $\mu_{0}\left(X\right)<\infty$.

$\sigma$-finite case. Suppose $\mu_{0}$ is $\sigma$-finite, i.e. there exist pairwise disjoint $X_{k}\in\mathcal{E}$ with $X=\bigcup_{k=1}^{\infty}X_{k}$ and $\mu_{0}\left(X_{k}\right)<\infty$. For any $A\in\mathcal{M}$, by countable additivity and continuity from below,

$$
\mu^{*}\left(A\right)=\sum_{k}\mu^{*}\left(A\cap{X}_{k}\right),\quad\nu\left(A\right)=\sum_{k}\nu\left(A\cap{X}_{k}\right).
$$

For each $k$, restricting the finite measures $\mu_{0}\left(\cdot\cap{X}_{k}\right)$ and $\nu\left(\cdot\cap{X}_{k}\right)$ to $X_{k}$ reduces to the finite case, giving $\nu\left(A\cap{X}_{k}\right)=\mu^{*}\left(A\cap{X}_{k}\right)$. Summing yields $\nu\left(A\right)=\mu^{*}\left(A\right)$. Thus $\mu^{*}|_{\mathcal{M}}$ is the unique extension of $\mu_{0}$ to $\mathcal{M}$. $\blacksquare$

(2) Exercise 17. On one hand, by **Definition 6.1.1 (Outer Measure)** (3) (countable subadditivity),

$$
\mu^{*}\left(E\cap\bigcup_{j=1}^{\infty}A_{j}\right)\le\sum_{j=1}^{\infty}\mu^{*}\left(E\cap{A}_{j}\right).
$$

On the other hand, since each $A_{j}$ is measurable (**Definition 6.3.1 (Carathéodory Condition)**), for any $T\subset{X}$ and any $N$, inductively applying the Carathéodory condition to $T$ gives

$$
\mu^{*}\left(T\right)=\sum_{j=1}^{N}\mu^{*}\left(T\cap{A}_{j}\right)+\mu^{*}\left(T\cap\left(\bigcup_{j=1}^{N}A_{j}\right)^{c}\right).
$$

Taking $T=E\cap\bigcup_{j=1}^{\infty}A_{j}$, we have $T\cap{A}_{j}=E\cap{A}_{j}$ and $T\cap\left(\bigcup_{j=1}^{N}A_{j}\right)^{c}=E\cap\bigcup_{j=N+1}^{\infty}A_{j}$. Hence

$$
\mu^{*}\left(E\cap\bigcup_{j=1}^{\infty}A_{j}\right)=\sum_{j=1}^{N}\mu^{*}\left(E\cap{A}_{j}\right)+\mu^{*}\left(E\cap\bigcup_{j=N+1}^{\infty}A_{j}\right)\ge\sum_{j=1}^{N}\mu^{*}\left(E\cap{A}_{j}\right).
$$

Letting $N\to\infty$,

$$
\mu^{*}\left(E\cap\bigcup_{j=1}^{\infty}A_{j}\right)\ge\sum_{j=1}^{\infty}\mu^{*}\left(E\cap{A}_{j}\right).
$$

Combining gives equality. $\blacksquare$

(3) Exercise 24. (a) From $A\cap{E}=B\cap{E}$ we get $\left(A\setminus{B}\right)\cap{E}=\varnothing$, and $A\setminus{B}\in\mathcal{M}$. Since $A\setminus{B}$ is measurable, apply the **Definition 6.3.1 (Carathéodory Condition)** at $T=X$:

$$
\mu^{*}\left(X\right)=\mu^{*}\left(X\cap\left(A\setminus{B}\right)\right)+\mu^{*}\left(X\cap\left(A\setminus{B}\right)^{c}\right)=\mu\left(A\setminus{B}\right)+\mu^{*}\left(X\setminus\left(A\setminus{B}\right)\right).
$$

Since $\left(A\setminus{B}\right)\cap{E}=\varnothing$, we have $E\subset{X}\setminus\left(A\setminus{B}\right)$. By monotonicity of the outer measure (**Definition 6.1.1 (Outer Measure)** (2)), $\mu^{*}\left(X\setminus\left(A\setminus{B}\right)\right)\ge\mu^{*}\left(E\right)=\mu^{*}\left(X\right)$. Substituting gives $\mu\left(A\setminus{B}\right)\le0$, hence $\mu\left(A\setminus{B}\right)=0$. Similarly $\mu\left(B\setminus{A}\right)=0$. Thus by **Proposition 5.2.1 (Finite Additivity)**,

$$
\mu\left(A\right)=\mu\left(A\cap{B}\right)+\mu\left(A\setminus{B}\right)=\mu\left(A\cap{B}\right)=\mu\left(B\right).
$$

$\blacksquare$

(b) First show $\nu$ is well-defined: if $A\cap{E}=B\cap{E}$, then by (a), $\mu\left(A\right)=\mu\left(B\right)$, so $\nu$ does not depend on the representative.

Next show $\mathcal{M}_{E}$ is a $\sigma$-algebra on $E$ (**Definition 4.1.3 ($\sigma$-Algebra)**): since $E=X\cap{E}\in\mathcal{M}_{E}$; for $A\cap{E}\in\mathcal{M}_{E}$, its complement within $E$ is $E\setminus\left(A\cap{E}\right)=\left(X\setminus{A}\right)\cap{E}\in\mathcal{M}_{E}$; and $\bigcup_{n}\left(A_{n}\cap{E}\right)=\left(\bigcup_{n}A_{n}\right)\cap{E}\in\mathcal{M}_{E}$. Thus $\mathcal{M}_{E}$ is a $\sigma$-algebra on $E$.

Finally show $\nu$ is a measure on $\mathcal{M}_{E}$ (**Definition 5.1.2 (Measure)**). Nonnegativity follows from $\mu\ge0$; $\nu\left(\varnothing\right)=\mu\left(\varnothing\right)=0$. Let $\left\{A_{n}\cap{E}\right\}$ be pairwise disjoint. Then for $n\ne{m}$, $\left(A_{n}\cap{A}_{m}\right)\cap{E}=\left(A_{n}\cap{E}\right)\cap\left(A_{m}\cap{E}\right)=\varnothing$, and by (a), $\mu\left(A_{n}\cap{A}_{m}\right)=0$. Thus by **Proposition 5.2.1 (Finite Additivity)** and **Proposition 5.2.4 (Continuity from Below)**,

$$
\nu\left(\bigcup_{n}\left(A_{n}\cap{E}\right)\right)=\nu\left(\left(\bigcup_{n}A_{n}\right)\cap{E}\right)=\mu\left(\bigcup_{n}A_{n}\right)=\sum_{n}\mu\left(A_{n}\right)=\sum_{n}\nu\left(A_{n}\cap{E}\right).
$$

Hence $\nu$ is a measure. $\blacksquare$

## 3

Let $-\infty\le{a}<{}b<\infty$. All half-open intervals $\left(a,b\right]$, together with $\left(a,\infty\right)$ and $\varnothing$, are called h-intervals. Prove that the family $\mathcal{E}$ of finite disjoint unions of h-intervals is an algebra (**Definition 6.4.1 (h-Interval)**).

### Solution to 3

Verify using **Definition 4.1.1 (Algebra of Sets)**.

First show the intersection of two h-intervals is an h-interval. Indeed, $\left(a,b\right]\cap\left(c,d\right]=\left(\max\left(a,c\right),\min\left(b,d\right)\right]$ (if nonempty), $\left(a,b\right]\cap\left(c,\infty\right)=\left(\max\left(a,c\right),b\right]$, $\left(a,\infty\right)\cap\left(c,\infty\right)=\left(\max\left(a,c\right),\infty\right)$, and the intersection with $\varnothing$ is $\varnothing$. Thus the intersection of h-intervals is an h-interval. Consequently, the intersection of any two finite disjoint unions in $\mathcal{E}$ can be expanded as a finite disjoint union of h-intervals, so $\mathcal{E}$ is closed under finite intersections.

Next show $\mathcal{E}$ is closed under complements. The complement of a single h-interval:

$$
\varnothing^{c}=\mathbb{R}=\left(-\infty,\infty\right),\quad\left(a,\infty\right)^{c}=\left(-\infty,a\right],\quad\left(a,b\right]^{c}=\left(-\infty,a\right]\cup\left(b,\infty\right),
$$

where $\left(-\infty,a\right]$ and $\left(b,\infty\right)$ are h-intervals and are pairwise disjoint. Thus the complement of each h-interval belongs to $\mathcal{E}$. For an element $A=\bigcup_{i=1}^{n}I_{i}\in\mathcal{E}$ ($I_{i}$ disjoint h-intervals), by De Morgan's laws,

$$
A^{c}=\left(\bigcup_{i=1}^{n}I_{i}\right)^{c}=\bigcap_{i=1}^{n}I_{i}^{c}\in\mathcal{E},
$$

since each $I_{i}^{c}\in\mathcal{E}$ and $\mathcal{E}$ is closed under finite intersections.

Finally, $X\in\mathcal{E}$: since $\mathbb{R}=\left(-\infty,\infty\right)$ is an h-interval of type $\left(a,\infty\right)$ ($a=-\infty$), $\mathbb{R}\in\mathcal{E}$. For $A,B\in\mathcal{E}$, by De Morgan's laws $A\cup{B}=\left(A^{c}\cap{B}^{c}\right)^{c}\in\mathcal{E}$. Thus $\mathcal{E}$ is closed under finite unions.

Therefore $\mathcal{E}$ is an algebra. $\blacksquare$
