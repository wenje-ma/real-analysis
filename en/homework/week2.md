# Assignment 2

> **Definition 1.3.1** (Limit Superior)<br>The limit superior of a sequence of sets $\left\{E_{n}\right\}$ is defined as $$\begin{aligned}\overline{\lim}_{n\to\infty}E_{n}&=\left\{x:x\text{ 属于无穷多个 }E_{n}\right\}\\&=\bigcap_{n=1}^{\infty}\bigcup_{k=n}^{\infty}E_{k}.\end{aligned}$$

> **Definition 1.3.3** (Limit Inferior)<br>$$\begin{aligned}\underline{\lim}_{n\to\infty}E_{n}&=\left\{x:x\text{ 仅不属于有限多个 }E_{n}\right\}\\&=\bigcup_{n=1}^{\infty}\bigcap_{k=n}^{\infty}E_{k}.\end{aligned}$$

> **Definition 4.1.3** ($\sigma$-Algebra)<br>Let $X$ be nonempty and $\mathcal F\subset\mathcal P\left(X\right)$. $\mathcal F$ is called a **$\sigma$-algebra** on $X$ if it satisfies:
> (1) $X\in\mathcal F$;
>
> (2) closed under complementation: $A\in\mathcal F\Rightarrow A^{c}\in\mathcal F$;
>
> (3) closed under countable unions: $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal F\Rightarrow\bigcup_{n=1}^{\infty}A_{n}\in\mathcal F$.
>
> $\left(X,\mathcal F\right)$ is called a **measurable space**, and the elements of $\mathcal F$ are called **measurable sets**.

> **Definition 5.1.2** (Measure)<br>Let $\left(X,\mathcal F\right)$ be a measurable space. A function $\mu:\mathcal F\to\left[0,+\infty\right]$ is called a **measure** on $\left(X,\mathcal F\right)$ if it satisfies:
> (1) nonnegativity: $\mu\left(E\right)\ge0$ for all $E\in\mathcal F$;
>
> (2) the empty set has measure zero: $\mu\left(\varnothing\right)=0$;
>
> (3) countable additivity ($\sigma$-additivity): for any countably many pairwise disjoint sets $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$, we have $\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\sum_{n=1}^{\infty}\mu\left(E_{n}\right)$.

> **Proposition 5.2.1** (Finite Additivity)<br>Let $\mu$ be a measure on $\left(X,\mathcal F\right)$ and let $E_{1},\dots,E_{n}\in\mathcal F$ be pairwise disjoint sets. Then $$\mu\left(\bigcup_{k=1}^{n}E_{k}\right)=\sum_{k=1}^{n}\mu\left(E_{k}\right).$$

> **Proposition 5.2.2** (Monotonicity)<br>Let $\mu$ be a measure and let $E,F\in\mathcal F$ with $E\subset F$. Then $\mu\left(E\right)\le\mu\left(F\right)$. If in addition $\mu\left(E\right)<+\infty$, then $\mu\left(F\setminus E\right)=\mu\left(F\right)-\mu\left(E\right)$.

> **Proposition 5.2.3** (Countable Subadditivity)<br>Let $\mu$ be a measure and let $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$ be any countably many sets (not necessarily pairwise disjoint). Then $$\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)\le\sum_{n=1}^{\infty}\mu\left(E_{n}\right).$$

> **Proposition 5.2.4** (Continuity from Below)<br>Let $\mu$ be a measure and let $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$ be a monotonically increasing sequence of sets (i.e. $E_{1}\subset E_{2}\subset\cdots$). Then $$\mu\left(\bigcup_{n=1}^{\infty}E_{n}\right)=\lim_{n\to\infty}\mu\left(E_{n}\right).$$

> **Proposition 5.2.5** (Continuity from Above)<br>Let $\mu$ be a measure and let $\left\{E_{n}\right\}_{n=1}^{\infty}\subset\mathcal F$ be a monotonically decreasing sequence of sets (i.e. $E_{1}\supset E_{2}\supset\cdots$), and suppose there exists some $m$ such that $\mu\left(E_{m}\right)<+\infty$. Then $$\mu\left(\bigcap_{n=1}^{\infty}E_{n}\right)=\lim_{n\to\infty}\mu\left(E_{n}\right).$$

> **Definition 5.4.1** (Null Set)<br>Let $\left(X,\mathcal F,\mu\right)$ be a measure space. A set $N\in\mathcal F$ is called a null set if $\mu\left(N\right)=0$.

> **Definition 5.4.2** (Set of Measure Zero)<br>A set $A\subset X$ is called a set of measure zero if there exists $N\in\mathcal F$ such that $A\subset N$ and $\mu\left(N\right)=0$.

> **Definition 5.4.4** (Complete Measure)<br>A measure space $\left(X,\mathcal F,\mu\right)$ is called complete if, for any $N\in\mathcal F$ satisfying $\mu\left(N\right)=0$ and any $A\subset N$, we have $A\in\mathcal F$.

### Problem 9

Prove **Theorem 5.4.6 (Completion Theorem for Measures)**: any measure space $\left(X,\mathcal F,\mu\right)$ can be completed. That is, there exists a complete measure space $\left(X,\mathcal M,\overline\mu\right)$ such that:

(1) $\mathcal F\subset\mathcal M$;

(2) $\overline\mu|_{\mathcal F}=\mu$;

(3) $\mathcal M$ is the smallest complete $\sigma$-algebra containing $\mathcal F$.

(Note: in the lecture notes the symbols in this theorem have OCR defects; the original "$\mathcal M\subset\mathcal M$" should read "$\mathcal F\subset\mathcal M$"; the rest has been restored according to the standard conclusion.)

### Solution to Problem 9

Let $\mathcal N=\left\{N\in\mathcal F:\mu\left(N\right)=0\right\}$ be the collection of all null sets (**Definition 5.4.1**). Define

$$
\mathcal M:=\left\{A\subset X:\exists\,B\in\mathcal F,\exists\,N\in\mathcal F,\mu\left(N\right)=0,\text{使 }B\subset A\subset B\cup N\right\},
$$

That is, $A\in\mathcal M$ if and only if $A$ differs from some measurable set $B$ by a set of measure zero (Definition 5.4.2). The proof proceeds in six steps.

**1. $\mathcal M$ is a $\sigma$-algebra.** We verify **Definition 4.1.3** item by item:

(1) **$X\in\mathcal M$**: take $B=X$ and $N=\varnothing$, then $X\subset X\subset X\cup\varnothing$.

(2) **Closed under complementation**: suppose $B\subset A\subset B\cup N$ with $\mu\left(N\right)=0$. Then $\left(B\cup N\right)^{c}\subset A^{c}\subset B^{c}$, and

$$
\begin{aligned}B^{c}\setminus\left(B\cup N\right)^{c}&=B^{c}\cap\left(B\cup N\right)\\&=B^{c}\cap N\subset N,
\end{aligned}
$$

Hence by **Proposition 5.2.2** (Monotonicity), $\mu\left(B^{c}\setminus\left(B\cup N\right)^{c}\right)\le\mu\left(N\right)=0$. Thus $A^{c}\in\mathcal M$ (take $B'=\left(B\cup N\right)^{c}\in\mathcal F$ and $N'=B^{c}\setminus\left(B\cup N\right)^{c}$).

(3) **Closed under countable unions**: suppose $B_{n}\subset A_{n}\subset B_{n}\cup N_{n}$ with $\mu\left(N_{n}\right)=0$. Then $\bigcup_{n}B_{n}\subset\bigcup_{n}A_{n}\subset\left(\bigcup_{n}B_{n}\right)\cup\left(\bigcup_{n}N_{n}\right)$. By **Proposition 5.2.3** (Countable Subadditivity), $\mu\left(\bigcup_{n}N_{n}\right)\le\sum_{n}\mu\left(N_{n}\right)=0$, so $\bigcup_{n}N_{n}$ is a set of measure zero, and hence $\bigcup_{n}A_{n}\in\mathcal M$.

Thus $\mathcal M$ is a $\sigma$-algebra.

**2. Define $\overline\mu:\mathcal M\to\left[0,+\infty\right]$ by $\overline\mu\left(A\right):=\mu\left(B\right)$, where $B\subset A\subset B\cup N$ and $\mu\left(N\right)=0$.** We first prove that this is well-defined: suppose $B_{1}\subset A\subset B_{1}\cup N_{1}$ and $B_{2}\subset A\subset B_{2}\cup N_{2}$ with $\mu\left(N_{1}\right)=\mu\left(N_{2}\right)=0$. From $B_{1}\subset A\subset B_{2}\cup N_{2}$ we get $B_{1}\setminus B_{2}\subset N_{2}$, hence $\mu\left(B_{1}\setminus B_{2}\right)\le\mu\left(N_{2}\right)=0$; similarly $\mu\left(B_{2}\setminus B_{1}\right)=0$. By **Proposition 5.2.1** (Finite Additivity) and **Proposition 5.2.2** (Monotonicity),

$$
\begin{aligned}\mu\left(B_{1}\right)&=\mu\left(B_{1}\cap B_{2}\right)+\mu\left(B_{1}\setminus B_{2}\right)\\&=\mu\left(B_{1}\cap B_{2}\right)\\&=\mu\left(B_{2}\right).
\end{aligned}
$$

Thus $\overline\mu$ is well-defined.

**3. $\overline\mu$ is a measure.** We verify **Definition 5.1.2** item by item: nonnegativity is clear. The empty set has measure zero: $\overline\mu\left(\varnothing\right)=\mu\left(\varnothing\right)=0$. Countable additivity: let $\left\{A_{n}\right\}_{n=1}^{\infty}\subset\mathcal M$ be pairwise disjoint, and write $A_{n}=B_{n}\cup N_{n}$ ($B_{n}\in\mathcal F$, $N_{n}\subset N_{n}'\in\mathcal N$). Then $\bigcup_{n}A_{n}=\left(\bigcup_{n}B_{n}\right)\cup\left(\bigcup_{n}N_{n}\right)\in\mathcal M$, and the $\left\{B_{n}\right\}$ are pairwise disjoint (since $B_{n}\subset A_{n}$); by the countable additivity of $\mu$

$$
\begin{aligned}\overline\mu\left(\bigcup_{n}A_{n}\right)&=\mu\left(\bigcup_{n}B_{n}\right)\\&=\sum_{n}\mu\left(B_{n}\right)\\&=\sum_{n}\overline\mu\left(A_{n}\right).
\end{aligned}
$$

**4. Extension property:** for $B\in\mathcal F$, since $B=B\cup\varnothing\in\mathcal M$, we have $\overline\mu\left(B\right)=\mu\left(B\right)$, i.e. $\overline\mu|_{\mathcal F}=\mu$.

**5. Completeness (**Definition 5.4.4**):** suppose $\overline\mu\left(A\right)=0$, i.e. $A=B\cup N$ with $\mu\left(B\right)=0$ and $N\subset N_{0}\in\mathcal N$. Then $A\subset B\cup N_{0}$, and by **Proposition 5.2.3**, $\mu\left(B\cup N_{0}\right)\le\mu\left(B\right)+\mu\left(N_{0}\right)=0$, so $A$ is a subset of a set of measure zero. Hence $A=\varnothing\cup A\in\mathcal M$, and any subset $C\subset A$ of $A$ also satisfies $C\subset B\cup N_{0}$, so $C\in\mathcal M$. Therefore $\mathcal M$ is complete.

**6. Minimality:** let $\mathcal M'$ be any complete $\sigma$-algebra containing $\mathcal F$. For $A=B\cup N\in\mathcal M$ ($B\in\mathcal F$, $N\subset N_{0}\in\mathcal N$), since $N_{0}\in\mathcal F\subset\mathcal M'$ and $\mu\left(N_{0}\right)=0$, the completeness of $\mathcal M'$ gives $N\in\mathcal M'$; also $B\in\mathcal F\subset\mathcal M'$, so $A=B\cup N\in\mathcal M'$. Therefore $\mathcal M\subset\mathcal M'$. Hence $\mathcal M$ is the smallest complete $\sigma$-algebra containing $\mathcal F$.

In summary, $\left(X,\mathcal M,\overline\mu\right)$ is a complete measure space satisfying (1)(2)(3), and the theorem is proved. $\blacksquare$

### Problem 10

Prove Problems 8, 9, 10 and 12.

**8.** Let $\left(X,\mathcal M,\mu\right)$ be a measure space and $\left\{E_{j}\right\}_{j=1}^{\infty}\subset\mathcal M$. Prove that $\mu\left(\liminf_{j\to\infty}E_{j}\right)\le\liminf_{j\to\infty}\mu\left(E_{j}\right)$. Moreover, if $\mu\left(\bigcup_{j=1}^{\infty}E_{j}\right)<\infty$, then $\mu\left(\limsup_{j\to\infty}E_{j}\right)\ge\limsup_{j\to\infty}\mu\left(E_{j}\right)$.

**9.** Let $\left(X,\mathcal M,\mu\right)$ be a measure space and $E,F\in\mathcal M$. Prove that $\mu\left(E\right)+\mu\left(F\right)=\mu\left(E\cup F\right)+\mu\left(E\cap F\right)$.

**10.** Given a measure space $\left(X,\mathcal M,\mu\right)$ and $E\in\mathcal M$, define $\mu_{E}\left(A\right):=\mu\left(A\cap E\right)$ for $A\in\mathcal M$. Prove that $\mu_{E}$ is a measure.

**12.** Let $\left(X,\mathcal M,\mu\right)$ be a finite measure space.

(a) If $E,F\in\mathcal M$ and $\mu\left(E\triangle F\right)=0$, then $\mu\left(E\right)=\mu\left(F\right)$.

(b) Define $E\sim F$ if and only if $\mu\left(E\triangle F\right)=0$; then $\sim$ is an equivalence relation on $\mathcal M$.

(c) For $E,F\in\mathcal M$, define $\rho\left(E,F\right):=\mu\left(E\triangle F\right)$. Prove that $\rho\left(E,F\right)\le\rho\left(E,G\right)+\rho\left(F,G\right)$, so that $\rho$ defines a metric on the quotient space $\mathcal M/\sim$.

### Solution to Problem 10

#### 8

Let $F_{n}:=\bigcap_{j=n}^{\infty}E_{j}$. By **Definition 1.3.3** (Limit Inferior), $\liminf_{j\to\infty}E_{j}=\bigcup_{n=1}^{\infty}F_{n}$, and $\left\{F_{n}\right\}$ is monotonically increasing. By **Proposition 5.2.4** (Continuity from Below),

$$
\begin{aligned}\mu\left(\liminf_{j\to\infty}E_{j}\right)&=\mu\left(\bigcup_{n=1}^{\infty}F_{n}\right)\\&=\lim_{n\to\infty}\mu\left(F_{n}\right).
\end{aligned}
$$

Also, since $F_{n}\subset E_{j}$ for all $j\ge n$, by **Proposition 5.2.2** (Monotonicity) we get $\mu\left(F_{n}\right)\le\inf_{j\ge n}\mu\left(E_{j}\right)$, hence

$$
\begin{aligned}\mu\left(\liminf_{j\to\infty}E_{j}\right)&=\lim_{n\to\infty}\mu\left(F_{n}\right)\\&\le\lim_{n\to\infty}\inf_{j\ge n}\mu\left(E_{j}\right)\\&=\liminf_{j\to\infty}\mu\left(E_{j}\right).
\end{aligned}
$$

Let $G_{n}:=\bigcup_{j=n}^{\infty}E_{j}$. By **Definition 1.3.1** (Limit Superior), $\limsup_{j\to\infty}E_{j}=\bigcap_{n=1}^{\infty}G_{n}$, and $\left\{G_{n}\right\}$ is monotonically decreasing. Since $\mu\left(G_{1}\right)=\mu\left(\bigcup_{j=1}^{\infty}E_{j}\right)<\infty$, by **Proposition 5.2.5** (Continuity from Above),

$$
\begin{aligned}\mu\left(\limsup_{j\to\infty}E_{j}\right)&=\mu\left(\bigcap_{n=1}^{\infty}G_{n}\right)\\&=\lim_{n\to\infty}\mu\left(G_{n}\right).
\end{aligned}
$$

Also, since $G_{n}\supset E_{j}$ for all $j\ge n$, monotonicity gives $\mu\left(G_{n}\right)\ge\sup_{j\ge n}\mu\left(E_{j}\right)$, hence

$$
\begin{aligned}\mu\left(\limsup_{j\to\infty}E_{j}\right)&=\lim_{n\to\infty}\mu\left(G_{n}\right)\\&\ge\lim_{n\to\infty}\sup_{j\ge n}\mu\left(E_{j}\right)\\&=\limsup_{j\to\infty}\mu\left(E_{j}\right).
\end{aligned}
$$

The two inequalities are proved. $\blacksquare$

#### 9

$$
E\cup F=\left(E\cap F\right)\cup\left(E\setminus F\right)\cup\left(F\setminus E\right),
$$

The three sets on the right are pairwise disjoint. By **Proposition 5.2.1** (Finite Additivity),

$$
\mu\left(E\cup F\right)=\mu\left(E\cap F\right)+\mu\left(E\setminus F\right)+\mu\left(F\setminus E\right).
$$

Moreover, $E=\left(E\cap F\right)\cup\left(E\setminus F\right)$ and $F=\left(E\cap F\right)\cup\left(F\setminus E\right)$ are both pairwise disjoint decompositions, hence

$$
\begin{aligned}\mu\left(E\right)+\mu\left(F\right)&=2\mu\left(E\cap F\right)+\mu\left(E\setminus F\right)+\mu\left(F\setminus E\right)\\&=\mu\left(E\cup F\right)+\mu\left(E\cap F\right).
\end{aligned}
$$

The identity is proved. $\blacksquare$

#### 10

We verify **Definition 5.1.2** item by item:

(1) **Nonnegativity**: $\mu_{E}\left(A\right)=\mu\left(A\cap E\right)\ge0$ for all $A\in\mathcal M$.

(2) **The empty set has measure zero**: $\mu_{E}\left(\varnothing\right)=\mu\left(\varnothing\cap E\right)=\mu\left(\varnothing\right)=0$.

(3) **Countable additivity**: let $\left\{A_{j}\right\}_{j=1}^{\infty}\subset\mathcal M$ be pairwise disjoint; then $\left\{A_{j}\cap E\right\}$ are also pairwise disjoint, and by the countable additivity of $\mu$

$$
\begin{aligned}\mu_{E}\left(\bigcup_{j=1}^{\infty}A_{j}\right)&=\mu\left(\left(\bigcup_{j=1}^{\infty}A_{j}\right)\cap E\right)\\&=\mu\left(\bigcup_{j=1}^{\infty}\left(A_{j}\cap E\right)\right)\\&=\sum_{j=1}^{\infty}\mu\left(A_{j}\cap E\right)\\&=\sum_{j=1}^{\infty}\mu_{E}\left(A_{j}\right).
\end{aligned}
$$

Thus $\mu_{E}$ is a measure. $\blacksquare$

#### 12

**(a)** $E=\left(E\cap F\right)\cup\left(E\setminus F\right)$ and $F=\left(E\cap F\right)\cup\left(F\setminus E\right)$ are both pairwise disjoint decompositions; by **Proposition 5.2.1** (Finite Additivity),

$$
\begin{aligned}\mu\left(E\right)&=\mu\left(E\cap F\right)+\mu\left(E\setminus F\right),\\\mu\left(F\right)&=\mu\left(E\cap F\right)+\mu\left(F\setminus E\right).
\end{aligned}
$$

Moreover, $E\setminus F\subset E\triangle F$ and $F\setminus E\subset E\triangle F$; by **Proposition 5.2.2** (Monotonicity), $\mu\left(E\setminus F\right)\le\mu\left(E\triangle F\right)=0$, and similarly $\mu\left(F\setminus E\right)=0$. Hence $\mu\left(E\right)=\mu\left(E\cap F\right)=\mu\left(F\right)$. $\blacksquare$

**(b)** We verify the three properties of an equivalence relation:

(1) **Reflexivity**: $\mu\left(E\triangle E\right)=\mu\left(\varnothing\right)=0$, so $E\sim E$.

(2) **Symmetry**: $E\triangle F=F\triangle E$, so $E\sim F\iff F\sim E$.

(3) **Transitivity**: since $E\triangle G\subset\left(E\triangle F\right)\cup\left(F\triangle G\right)$, by **Proposition 5.2.3** (Countable Subadditivity), $\mu\left(E\triangle G\right)\le\mu\left(E\triangle F\right)+\mu\left(F\triangle G\right)=0$, so $E\sim G$.

Thus $\sim$ is an equivalence relation on $\mathcal M$. $\blacksquare$

**(c)** Symmetry and nonnegativity are clear: $\rho\left(E,F\right)=\rho\left(F,E\right)\ge0$ and $\rho\left(E,E\right)=0$. Also, $E\triangle G\subset\left(E\triangle F\right)\cup\left(F\triangle G\right)$; by **Proposition 5.2.3** (Countable Subadditivity),

$$
\begin{aligned}\rho\left(E,G\right)&=\mu\left(E\triangle G\right)\\&\le\mu\left(E\triangle F\right)+\mu\left(F\triangle G\right)\\&=\rho\left(E,F\right)+\rho\left(F,G\right).
\end{aligned}
$$

Finally, we verify well-definedness and positivity: if $E\sim E'$ and $F\sim F'$ (i.e. $\mu\left(E\triangle E'\right)=\mu\left(F\triangle F'\right)=0$), then

$$
E\triangle F\subset\left(E\triangle E'\right)\cup\left(E'\triangle F'\right)\cup\left(F'\triangle F\right),
$$

hence $\rho\left(E,F\right)\le0+\rho\left(E',F'\right)+0=\rho\left(E',F'\right)$; symmetrically $\rho\left(E',F'\right)\le\rho\left(E,F\right)$, so $\rho\left(E,F\right)=\rho\left(E',F'\right)$, i.e. $\rho$ is well-defined on the quotient space $\mathcal M/\sim$. Also, $\rho\left(E,F\right)=0\iff\mu\left(E\triangle F\right)=0\iff E\sim F$, so $\rho$ is a metric on $\mathcal M/\sim$. $\blacksquare$
