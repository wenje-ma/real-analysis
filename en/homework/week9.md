# Assignment 9

> **Definition 11.1.1** (Signed Measure)<br>Let $\left(X,\mathcal F\right)$ be a measurable space. A function $\nu:\mathcal F\to\mathbb R\cup\left\{+\infty\right\}$ or $\mathbb R\cup\left\{-\infty\right\}$ is called a **signed measure** if it satisfies:
> (1) $\nu\left(\varnothing\right)=0$;
> 
> (2) countable additivity: for any sequence of pairwise disjoint measurable sets $\left\{E_{i}\right\}_{i=1}^{\infty}\subset\mathcal F$, we have $\nu\left(\bigcup_{i=1}^{\infty}E_{i}\right)=\sum_{i=1}^{\infty}\nu\left(E_{i}\right)$;
> 
> (3) $\nu$ cannot take both $+\infty$ and $-\infty$ as values.

> **Proposition 11.1.2** (Basic Properties of a Signed Measure)<br>Let $\nu$ be a signed measure. Then:
> (1) finite additivity: for any finitely many pairwise disjoint $E_{1},\dots,E_{n}\in\mathcal F$, we have $\nu\left(\bigcup_{i=1}^{n}E_{i}\right)=\sum_{i=1}^{n}\nu\left(E_{i}\right)$;
> 
> (2) continuity from below: if $\left\{E_{j}\right\}$ is monotonically increasing and measurable, then $\lim_{j\to\infty}\nu\left(E_{j}\right)=\nu\left(\bigcup_{j}E_{j}\right)$;
> 
> (3) continuity from above: if $\left\{E_{j}\right\}$ is monotonically decreasing and measurable and $\nu\left(E_{1}\right)< \infty$, then $\lim_{j\to\infty}\nu\left(E_{j}\right)=\nu\left(\bigcap_{j}E_{j}\right)$.

> **Definition 11.2.1** (Positive Set, Negative Set, Null Set)<br>Let $\nu$ be a signed measure on $\left(X,\mathcal F\right)$.<br>A set $P\in\mathcal F$ is called a **positive set** (denoted $P\gtrsim0$) if for every $E\in\mathcal F$ with $E\subset P$, we have $\nu\left(E\right)\ge0$;<br>a set $N\in\mathcal F$ is called a **negative set** (denoted $N\lesssim0$) if for every $E\in\mathcal F$ with $E\subset N$, we have $\nu\left(E\right)\le0$;<br>a set $Z\in\mathcal F$ is called a **null set** if for every $E\in\mathcal F$ with $E\subset Z$, we have $\nu\left(E\right)=0$.

> **Lemma 11.2.2** (Properties of Positive Sets)
> (1) every measurable subset of a positive set is a positive set;
> 
> (2) a countable union of positive sets is a positive set;
> 
> (3) if $\left\{P_{n}\right\}$ is a sequence of positive sets, then $\bigcap_{n=1}^{\infty}P_{n}$ is a positive set.
> 
> The above properties also hold for negative sets (Remark 11.2.3).

> **Lemma 11.2.4**<br>Let $\nu$ be a signed measure. If $E$ is not a negative set, then there exists a positive set $F\subset E$ such that $\nu\left(F\right)> 0$.

> **Theorem 11.3.2** (Hahn Decomposition Theorem)<br>Let $\nu$ be a signed measure on $\left(X,\mathcal F\right)$. Then there exists a decomposition $X=P\cup N$ of $X$, where $P$ is a positive set, $N$ is a negative set, and $P\cap N=\varnothing$; and this decomposition is unique up to a $\nu$-null set.

> **Definition 11.4.1** (Mutually Singular Signed Measures)<br>Let $\mu$ and $\nu$ be two signed measures on a measurable space $\left(X,\mathcal F\right)$. If there exists a measurable set $E\in\mathcal F$ such that $E$ is a $\mu$-null set and $E^{c}$ is a $\nu$-null set, then $\mu$ and $\nu$ are called mutually singular, denoted $\mu\perp\nu$.

> **Theorem 11.4.3** (Jordan Decomposition Theorem)<br>Let $\nu$ be a signed measure on $\left(X,\mathcal F\right)$. Then there exists a unique pair of mutually singular positive measures $\nu^{+}$ and $\nu^{-}$ such that $\nu=\nu^{+}-\nu^{-}$.

> **Definition 11.4.4** (Variation Measure)<br>Let $\nu$ be a signed measure with Jordan decomposition $\nu=\nu^{+}-\nu^{-}$.<br>$\nu^{+}$ is called the **positive variation** of $\nu$, $\nu^{-}$ the **negative variation** of $\nu$, and $\left|\nu\right|=\nu^{+}+\nu^{-}$ the **total variation measure** of $\nu$.

> **Definition 11.5.1** (Absolute Continuity)<br>Let $\mu$ be a positive measure and $\nu$ a signed measure. $\nu$ is called absolutely continuous with respect to $\mu$ (denoted $\nu\ll\mu$) if for every $E\in\mathcal F$, $\mu\left(E\right)=0\Rightarrow\nu\left(E\right)=0$.

> **Remark 11.5.3**<br>Let $f\in L^{1}\left(\mu\right)$. Then $\lim_{\mu\left(E\right)\to0}\int_{E}f\,\mathrm{d}\mu=0$.

> **Theorem 11.5.5** (Radon–Nikodym Theorem)<br>Let $\mu$ be a $\sigma$-finite positive measure and $\nu$ a signed measure with $\nu\ll\mu$. Then there exists a measurable function $f:X\to\mathbb R$ such that $\nu\left(E\right)=\int_{E}f\,\mathrm{d}\mu$ for every $E\in\mathcal F$; and $\nu^{+}\left(E\right)=\int_{E}f^{+}\mathrm{d}\mu$, $\nu^{-}\left(E\right)=\int_{E}f^{-}\mathrm{d}\mu$, $\left|\nu\right|\left(E\right)=\int_{E}\left|f\right|\mathrm{d}\mu$. The function $f$ is called the Radon–Nikodym derivative of $\nu$ with respect to $\mu$, denoted $f=\frac{\mathrm{d}\nu}{\mathrm{d}\mu}$.

> **Theorem 10.2.2** (Tonelli's Theorem)<br>If $f:X\times Y\to\left[0,\infty\right]$ is $\mathcal A\otimes\mathcal B$-measurable, then $$\int_{X\times Y}f\,\mathrm{d}\left(\mu\times\nu\right)=\int_{X}\left(\int_{Y}f\left(x,y\right)\mathrm{d}\nu\left(y\right)\right)\mathrm{d}\mu\left(x\right)=\int_{Y}\left(\int_{X}f\left(x,y\right)\mathrm{d}\mu\left(x\right)\right)\mathrm{d}\nu\left(y\right),$$ where all integral values lie in $\left[0,\infty\right]$.

### Problem 1

Let $\nu$ be a signed measure on $\left(X,\mathcal F\right)$ that does not take the value $-\infty$, and let $E$ not be a negative set. Prove: there exists a measurable set $G\subset E$ such that

$$
\nu\left(G\right)=\sup\left\{\nu\left(F\right):F\subset E,\nu\left(F\right)> 0\right\}> 0,
$$

and $E\setminus G$ is a negative set. (An embedded exercise in the proof of the Hahn decomposition theorem.)

### Solution to Problem 1

Set $\alpha=\sup\left\{\nu\left(F\right):F\subset E,\nu\left(F\right)> 0\right\}$. Since $E$ is not a negative set, by **Lemma 11.2.4** there exists a positive set $F_{0}\subset E$ with $\nu\left(F_{0}\right)> 0$, so $\alpha\ge\nu\left(F_{0}\right)> 0$, i.e. $\alpha> 0$.

We first show that $\alpha$ is attained by a positive set. Let

$$
\beta=\sup\left\{\nu\left(P\right):P\subset E,P\text{是正集}\right\},
$$

Then $\beta\ge\nu\left(F_{0}\right)> 0$. Clearly $\beta\le\alpha$, because a positive set $P\subset E$ with $\nu\left(P\right)> 0$ is counted in the supremum defining $\alpha$. Conversely, we show $\alpha\le\beta$: take any $F\subset E$ with $\nu\left(F\right)> 0$. If $F$ is a positive set, then $\nu\left(F\right)\le\beta$; if $F$ is not a positive set, then there exists $C\subset F$ with $\nu\left(C\right)< 0$. Taking $F_{1}=F\setminus C$, we have $\nu\left(F_{1}\right)=\nu\left(F\right)-\nu\left(C\right)> \nu\left(F\right)$. Applying this construction repeatedly yields a decreasing measurable sequence $\left\{F_{n}\right\}$ such that $\nu\left(F_{n}\right)$ increases strictly and converges to some $\gamma$. By **Proposition 11.1.2**(3) (continuity from above), $\nu\left(\bigcap_{n}F_{n}\right)=\lim_{n}\nu\left(F_{n}\right)=\gamma$. If $\bigcap_{n}F_{n}$ were not a positive set, one could again extract a subset of larger measure from it, contradicting the convergence to $\gamma$; hence $\bigcap_{n}F_{n}\subset E$ is a positive set. Thus $\gamma=\nu\left(\bigcap_{n}F_{n}\right)\le\beta$; and since $\nu\left(F_{n}\right)\uparrow\gamma$ and $\nu\left(F_{1}\right)> \nu\left(F\right)$, we get $\nu\left(F\right)< \gamma\le\beta$. Hence for every such $F$, $\nu\left(F\right)\le\beta$, i.e. $\alpha\le\beta$. Combining gives $\alpha=\beta$.

By the definition of $\beta$, take a sequence of positive sets $\left\{P_{n}\right\}\subset E$ with $\nu\left(P_{n}\right)\to\beta$. Let $G=\bigcup_{n=1}^{\infty}P_{n}\subset E$; then $G$ is a positive set (**Lemma 11.2.2**(2)). Set $Q_{n}=\bigcup_{k=1}^{n}P_{k}$; then $\left\{Q_{n}\right\}$ is an increasing union of positive sets, hence still a positive set, and $\nu\left(Q_{n}\right)\ge\nu\left(P_{n}\right)\to\beta$; also $Q_{n}\subset E$ is a positive set, so $\nu\left(Q_{n}\right)\le\beta$. Hence $\nu\left(Q_{n}\right)\to\beta$, and by **Proposition 11.1.2**(2) (continuity from below),

$$
\nu\left(G\right)=\lim_{n\to\infty}\nu\left(Q_{n}\right)=\beta=\alpha> 0.
$$

Finally, we show that $E\setminus G$ is a negative set. Suppose, for contradiction, that $E\setminus G$ is not a negative set; by **Lemma 11.2.4** there exists a positive set $F\subset E\setminus G$ with $\nu\left(F\right)> 0$. Since $G\cap F=\varnothing$, $G\cup F\subset E$ and $G\cup F$ is a positive set (**Lemma 11.2.2**(2)); hence

$$
\nu\left(G\cup F\right)=\nu\left(G\right)+\nu\left(F\right)=\alpha+\nu\left(F\right)> \alpha=\beta,
$$

contradicting that $\beta$ is the supremum of the measures of all positive sets in $E$. Hence $E\setminus G$ is a negative set. $\blacksquare$

### Problem 2

Prove Problems 3, 6 and 7.

**3.** Let $\nu$ be a signed measure on $\left(X,\mathcal M\right)$.
a. $L^{1}\left(\nu\right)=L^{1}\left(\left|\nu\right|\right)$;
b. If $f\in L^{1}\left(\nu\right)$, then $\left|\int f\,\mathrm{d}\nu\right|\le\int\left|f\right|\mathrm{d}\left|\nu\right|$;
c. If $E\in\mathcal M$, then $\left|\nu\right|\left(E\right)=\sup\left\{\left|\int_{E}f\,\mathrm{d}\nu\right|:\left|f\right|\le1\right\}$.

**6.** Let $\nu\left(E\right)=\int_{E}f\,\mathrm{d}\mu$, where $\mu$ is a positive measure and $f$ is an extended $\mu$-integrable function. Describe, in terms of $f$ and $\mu$, the Hahn decomposition of $\nu$, as well as the positive variation, negative variation and total variation of $\nu$.

**7.** Let $\nu$ be a signed measure on $\left(X,\mathcal M\right)$ and $E\in\mathcal M$.
a. $\nu^{+}\left(E\right)=\sup\left\{\nu\left(F\right):F\in\mathcal M,F\subset E\right\}$, and $\nu^{-}\left(E\right)=-\inf\left\{\nu\left(F\right):F\in\mathcal M,F\subset E\right\}$;
b. $\left|\nu\right|\left(E\right)=\sup\left\{\sum_{i}\left|\nu\left(E_{i}\right)\right|:n\in\mathbb N,E_{1},\dots,E_{n}\text{两两不交},\bigcup_{i=1}^{n}E_{i}=E\right\}$.

### Solution to Problem 2

#### 3

**(a)** By **Definition 11.4.4**, $\left|\nu\right|=\nu^{+}+\nu^{-}$. Hence for any $f$,

$$
\int\left|f\right|\mathrm{d}\left|\nu\right|=\int\left|f\right|\mathrm{d}\nu^{+}+\int\left|f\right|\mathrm{d}\nu^{-}.
$$

All three terms on both sides are nonnegative; hence the left side is finite if and only if both terms on the right are finite, i.e. $f\in L^{1}\left(\nu^{+}\right)\cap L^{1}\left(\nu^{-}\right)=L^{1}\left(\nu\right)$ (by the definition of $L^{1}\left(\nu\right)$). Hence $L^{1}\left(\nu\right)=L^{1}\left(\left|\nu\right|\right)$. $\blacksquare$

**(b)** By **Theorem 11.4.3** (Jordan decomposition), $\nu=\nu^{+}-\nu^{-}$. Hence, by the triangle inequality and (a),

$$
\left|\int f\,\mathrm{d}\nu\right|=\left|\int f\,\mathrm{d}\nu^{+}-\int f\,\mathrm{d}\nu^{-}\right|\le\int\left|f\right|\mathrm{d}\nu^{+}+\int\left|f\right|\mathrm{d}\nu^{-}=\int\left|f\right|\mathrm{d}\left|\nu\right|.
$$

$\blacksquare$

**(c)** We first prove $\le$: for any measurable function $g$ with $\left|g\right|\le1$, by (b),

$$
\left|\int_{E}g\,\mathrm{d}\nu\right|\le\int_{E}\left|g\right|\mathrm{d}\left|\nu\right|\le\int_{E}1\,\mathrm{d}\left|\nu\right|=\left|\nu\right|\left(E\right),
$$

so $\sup\le\left|\nu\right|\left(E\right)$.

We next prove $\ge$: take a Hahn decomposition $X=P\cup N$ of $\nu$ (**Theorem 11.3.2**), and set $g=\chi_{E\cap P}-\chi_{E\cap N}$; then $\left|g\right|\le1$ and $g$ is measurable. By **Theorem 11.4.3** (Jordan decomposition), $\nu^{+}\left(E\right)=\nu\left(E\cap P\right)$ and $\nu^{-}\left(E\right)=-\nu\left(E\cap N\right)$. Hence

$$
\int_{E}g\,\mathrm{d}\nu=\nu\left(E\cap P\right)-\nu\left(E\cap N\right)=\nu^{+}\left(E\right)+\nu^{-}\left(E\right)=\left|\nu\right|\left(E\right).
$$

so $\sup\ge\left|\nu\right|\left(E\right)$. Combining gives equality. $\blacksquare$

#### 6

$f$ is a real-valued measurable function, with at least one of $\int f^{+}\mathrm{d}\mu$, $\int f^{-}\mathrm{d}\mu$ finite. By **Definition 11.2.1**:

For $E\in\mathcal M$, $E$ is a $\nu$-positive set if and only if for every measurable $F\subset E$, $\nu\left(F\right)=\int_{F}f\,\mathrm{d}\mu\ge0$; since this must hold for both $F=E\cap\left\{f< 0\right\}$ and $F=E\cap\left\{f> 0\right\}$, $E$ is a positive set if and only if $f\ge0$ $\mu$-almost everywhere on $E$. Similarly, $E$ is a negative set if and only if $f\le0$ $\mu$-almost everywhere on $E$; $E$ is a null set if and only if $f=0$ $\mu$-almost everywhere on $E$.

Hence $X=P\cup N$, where

$$
P=\left\{x:f\left(x\right)\ge0\right\},;N=\left\{x:f\left(x\right)< 0\right\},
$$

is a Hahn decomposition of $\nu$ (**Theorem 11.3.2**): $P$ is a positive set, $N$ is a negative set, $P\cap N=\varnothing$, $P\cup N=X$. (The null set $\left\{f=0\right\}$ may be merged into $P$ or $N$ without changing the essence of the decomposition.)

By **Theorem 11.4.3** (Jordan decomposition), $\nu^{+}\left(E\right)=\nu\left(E\cap P\right)=\int_{E\cap P}f\,\mathrm{d}\mu=\int_{E}f^{+}\mathrm{d}\mu$ (since $f\ge0$ on $P$), and $\nu^{-}\left(E\right)=-\nu\left(E\cap N\right)=-\int_{E\cap N}f\,\mathrm{d}\mu=\int_{E}f^{-}\mathrm{d}\mu$ (since $f\le0$ on $N$). Hence

$$
\nu^{+}\left(E\right)=\int_{E}f^{+}\mathrm{d}\mu,;\nu^{-}\left(E\right)=\int_{E}f^{-}\mathrm{d}\mu,;\left|\nu\right|\left(E\right)=\int_{E}\left|f\right|\mathrm{d}\mu.
$$

$\blacksquare$

#### 7

**(a)** Take a Hahn decomposition $X=P\cup N$ of $\nu$ (**Theorem 11.3.2**); then $\nu^{+}\left(E\right)=\nu\left(E\cap P\right)$ and $\nu^{-}\left(E\right)=-\nu\left(E\cap N\right)$ (**Theorem 11.4.3**).

For any $F\in\mathcal M$ with $F\subset E$, from $\nu=\nu^{+}-\nu^{-}$ and $\nu^{-}\ge0$, we have $\nu\left(F\right)=\nu^{+}\left(F\right)-\nu^{-}\left(F\right)\le\nu^{+}\left(F\right)\le\nu^{+}\left(E\right)$ (the last inequality by monotonicity of $\nu^{+}$, since $F\subset E$). Hence $\sup\left\{\nu\left(F\right):F\subset E\right\}\le\nu^{+}\left(E\right)$. Taking $F=E\cap P\subset E$, we have $\nu\left(E\cap P\right)=\nu^{+}\left(E\cap P\right)-\nu^{-}\left(E\cap P\right)=\nu^{+}\left(E\cap P\right)=\nu^{+}\left(E\right)$ (since $E\cap P\subset P$ is a positive set, $\nu^{-}\left(E\cap P\right)=0$). Hence $\sup\ge\nu^{+}\left(E\right)$. Combining gives $\nu^{+}\left(E\right)=\sup\left\{\nu\left(F\right):F\subset E\right\}$.

Similarly, for $F\subset E$, $\nu\left(F\right)=\nu^{+}\left(F\right)-\nu^{-}\left(F\right)\ge-\nu^{-}\left(F\right)\ge-\nu^{-}\left(E\right)$, so $\inf\left\{\nu\left(F\right):F\subset E\right\}\ge-\nu^{-}\left(E\right)$, i.e. $-\inf\left\{\nu\left(F\right):F\subset E\right\}\le\nu^{-}\left(E\right)$. Taking $F=E\cap N$, we have $\nu\left(E\cap N\right)=-\nu^{-}\left(E\cap N\right)=-\nu^{-}\left(E\right)$, so $\inf\le-\nu^{-}\left(E\right)$, i.e. $-\inf\ge\nu^{-}\left(E\right)$. Combining gives $\nu^{-}\left(E\right)=-\inf\left\{\nu\left(F\right):F\subset E\right\}$. $\blacksquare$

**(b)** We first prove $\le$: for any pairwise disjoint $\left\{E_{i}\right\}$ whose union is $E$, from $\nu=\nu^{+}-\nu^{-}$ and the triangle inequality,

$$
\sum_{i}\left|\nu\left(E_{i}\right)\right|=\sum_{i}\left|\nu^{+}\left(E_{i}\right)-\nu^{-}\left(E_{i}\right)\right|\le\sum_{i}\left[\nu^{+}\left(E_{i}\right)+\nu^{-}\left(E_{i}\right)\right]=\nu^{+}\left(E\right)+\nu^{-}\left(E\right)=\left|\nu\right|\left(E\right),
$$

so $\sup\le\left|\nu\right|\left(E\right)$.

We next prove $\ge$: take a Hahn decomposition $X=P\cup N$ (**Theorem 11.3.2**), and set $E_{1}=E\cap P$, $E_{2}=E\cap N$; then $E_{1},E_{2}$ are pairwise disjoint and $E_{1}\cup E_{2}=E$. Hence

$$
\left|\nu\left(E_{1}\right)\right|+\left|\nu\left(E_{2}\right)\right|=\nu^{+}\left(E\cap P\right)+\nu^{-}\left(E\cap N\right)=\nu^{+}\left(E\right)+\nu^{-}\left(E\right)=\left|\nu\right|\left(E\right),
$$

so $\sup\ge\left|\nu\right|\left(E\right)$. Combining gives equality. $\blacksquare$

### Problem 3

Prove Problems 9, 11, 12, 16 and 17.

**9.** Let $\left\{\nu_{j}\right\}$ be a sequence of positive measures. If $\nu_{j}\perp\mu$ for all $j$, then $\sum_{j}\nu_{j}\perp\mu$; if $\nu_{j}\ll\mu$ for all $j$, then $\sum_{j}\nu_{j}\ll\mu$.

**11.** Let $\mu$ be a positive measure. A family of functions $\left\{f_{\alpha}\right\}_{\alpha\in A}\subset L^{1}\left(\mu\right)$ is called uniformly integrable if for every $\varepsilon> 0$ there exists $\delta> 0$ such that $\left|\int_{E}f_{\alpha}\,\mathrm{d}\mu\right|< \varepsilon$ for all $\alpha\in A$, whenever $\mu\left(E\right)< \delta$.
a. Any finite subset of $L^{1}\left(\mu\right)$ is uniformly integrable;
b. If $\left\{f_{n}\right\}$ is a sequence in $L^{1}\left(\mu\right)$ converging in the $L^{1}$ metric to $f\in L^{1}\left(\mu\right)$, then $\left\{f_{n}\right\}$ is uniformly integrable.

**12.** For $j=1,2$, let $\mu_{j},\nu_{j}$ be $\sigma$-finite measures on $\left(X_{j},\mathcal M_{j}\right)$ with $\nu_{j}\ll\mu_{j}$. Then $\nu_{1}\times\nu_{2}\ll\mu_{1}\times\mu_{2}$, and

$$
\frac{\mathrm{d}\left(\nu_{1}\times\nu_{2}\right)}{\mathrm{d}\left(\mu_{1}\times\mu_{2}\right)}\left(x_{1},x_{2}\right)=\frac{\mathrm{d}\nu_{1}}{\mathrm{d}\mu_{1}}\left(x_{1}\right)\cdot\frac{\mathrm{d}\nu_{2}}{\mathrm{d}\mu_{2}}\left(x_{2}\right).
$$

**16.** Let $\mu,\nu$ be measures on $\left(X,\mathcal M\right)$ with $\nu\ll\mu$, and set $\lambda=\mu+\nu$. If $f=\frac{\mathrm{d}\nu}{\mathrm{d}\lambda}$, then $0\le f< 1$ $\mu$-almost everywhere, and $\frac{\mathrm{d}\nu}{\mathrm{d}\mu}=\frac{f}{1-f}$.

**17.** Let $\left(X,\mathcal M,\mu\right)$ be a $\sigma$-finite measure space, $\mathcal N$ a sub-$\sigma$-algebra of $\mathcal M$, and $\nu=\mu|_{\mathcal N}$. If $f\in L^{1}\left(\mu\right)$, then there exists $g\in L^{1}\left(\nu\right)$ (hence $g$ is $\mathcal N$-measurable) such that $\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\nu$ for every $E\in\mathcal N$; and if $g'$ is another such function, then $g=g'$ $\nu$-almost everywhere. (In probability theory, $g$ is called the conditional expectation of $f$ with respect to $\mathcal N$.)

### Solution to Problem 3

#### 9

**(The singular case).** Since $\nu_{j}\perp\mu$ (**Definition 11.4.1**), for each $j$ there exists $E_{j}\in\mathcal M$ such that $E_{j}$ is a $\mu$-null set and $E_{j}^{c}$ is a $\nu_{j}$-null set, i.e. $\mu\left(E_{j}\right)=0$, $\nu_{j}\left(E_{j}^{c}\right)=0$. Let $E=\bigcup_{j=1}^{\infty}E_{j}$. By countable subadditivity of $\mu$,

$$
\mu\left(E\right)\le\sum_{j=1}^{\infty}\mu\left(E_{j}\right)=0,
$$

so $E$ is a $\mu$-null set. Also $E^{c}=\bigcap_{j=1}^{\infty}E_{j}^{c}\subset E_{k}^{c}$ for all $k$, and by monotonicity of $\nu_{k}$, $\nu_{k}\left(E^{c}\right)\le\nu_{k}\left(E_{k}^{c}\right)=0$, so $\nu_{k}\left(E^{c}\right)=0$ for all $k$, and hence $\left(\sum_{j}\nu_{j}\right)\left(E^{c}\right)=\sum_{j}\nu_{j}\left(E^{c}\right)=0$. Hence $\sum_{j}\nu_{j}\perp\mu$. $\blacksquare$

**(The absolutely continuous case).** Let $\nu_{j}\ll\mu$ for all $j$ (**Definition 11.5.1**). If $\mu\left(E\right)=0$, then $\nu_{j}\left(E\right)=0$ for all $j$, so $\left(\sum_{j}\nu_{j}\right)\left(E\right)=\sum_{j}\nu_{j}\left(E\right)=0$. Therefore $\sum_{j}\nu_{j}\ll\mu$. $\blacksquare$

#### 11

**(a)** Let $\left\{f_{1},\dots,f_{n}\right\}\subset L^{1}\left(\mu\right)$. For each $j$, by **Remark 11.5.3** ($f_{j}\in L^{1}\left(\mu\right)$, $\lim_{\mu\left(E\right)\to0}\int_{E}f_{j}\,\mathrm{d}\mu=0$), there exists $\delta_{j}> 0$ such that $\mu\left(E\right)< \delta_{j}\Rightarrow\left|\int_{E}f_{j}\,\mathrm{d}\mu\right|< \varepsilon$. Take $\delta=\min_{1\le j\le n}\delta_{j}> 0$; then when $\mu\left(E\right)< \delta$, for all $j$ we have $\mu\left(E\right)< \delta_{j}$, hence $\left|\int_{E}f_{j}\,\mathrm{d}\mu\right|< \varepsilon$. Hence $\left\{f_{1},\dots,f_{n}\right\}$ is uniformly integrable. $\blacksquare$

**(b)** Since $\int\left|f_{n}-f\right|\mathrm{d}\mu\to0$, there exists $N$ such that for $n\ge N$, $\int\left|f_{n}-f\right|\mathrm{d}\mu< \frac{\varepsilon}{2}$. By (a), the singleton $\left\{f\right\}$ is uniformly integrable: there exists $\delta_{1}> 0$ such that $\mu\left(E\right)< \delta_{1}\Rightarrow\left|\int_{E}f\,\mathrm{d}\mu\right|< \frac{\varepsilon}{2}$. Also the finite set $\left\{f_{1},\dots,f_{N-1}\right\}$ is uniformly integrable by (a): there exists $\delta_{2}> 0$ such that $\mu\left(E\right)< \delta_{2}\Rightarrow\left|\int_{E}f_{n}\,\mathrm{d}\mu\right|< \varepsilon$ for $n< N$. Take $\delta=\min\left\{\delta_{1},\delta_{2}\right\}$. When $\mu\left(E\right)< \delta$, for $n\ge N$,

$$
\left|\int_{E}f_{n}\,\mathrm{d}\mu\right|\le\left|\int_{E}f\,\mathrm{d}\mu\right|+\int_{E}\left|f_{n}-f\right|\mathrm{d}\mu\le\frac{\varepsilon}{2}+\int\left|f_{n}-f\right|\mathrm{d}\mu< \frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon,
$$

while for $n< N$, also $\left|\int_{E}f_{n}\,\mathrm{d}\mu\right|< \varepsilon$. Hence $\left\{f_{n}\right\}$ is uniformly integrable. $\blacksquare$

#### 12

Since $\nu_{j}\ll\mu_{j}$ and $\mu_{j}$ is a $\sigma$-finite positive measure, by **Theorem 11.5.5** (Radon–Nikodym theorem), there exists an $\mathcal M_{j}$-measurable function $f_{j}=\frac{\mathrm{d}\nu_{j}}{\mathrm{d}\mu_{j}}\ge0$ such that $\nu_{j}\left(E\right)=\int_{E}f_{j}\,\mathrm{d}\mu_{j}$ for every $E\in\mathcal M_{j}$. Define $F:\left(X_{1}\times X_{2}\right)\to\left[0,\infty\right]$, $F\left(x_{1},x_{2}\right)=f_{1}\left(x_{1}\right)f_{2}\left(x_{2}\right)$; then $F$ is $\mathcal M_{1}\otimes\mathcal M_{2}$-measurable (by measurability on product spaces). For a measurable rectangle $A\times B\in\mathcal M_{1}\otimes\mathcal M_{2}$, by **Theorem 10.2.2** (Tonelli's theorem),

$$
\int_{A\times B}F\,\mathrm{d}\left(\mu_{1}\times\mu_{2}\right)=\int_{A\times B}f_{1}\left(x_{1}\right)f_{2}\left(x_{2}\right)\mathrm{d}\left(\mu_{1}\times\mu_{2}\right)=\left(\int_{A}f_{1}\,\mathrm{d}\mu_{1}\right)\left(\int_{B}f_{2}\,\mathrm{d}\mu_{2}\right)=\nu_{1}\left(A\right)\nu_{2}\left(B\right)=\left(\nu_{1}\times\nu_{2}\right)\left(A\times B\right).
$$

By uniqueness of the product measure (agreement on the rectangle-admissible family), for every $E\in\mathcal M_{1}\otimes\mathcal M_{2}$,

$$
\left(\nu_{1}\times\nu_{2}\right)\left(E\right)=\int_{E}F\,\mathrm{d}\left(\mu_{1}\times\mu_{2}\right).
$$

This implies $\nu_{1}\times\nu_{2}\ll\mu_{1}\times\mu_{2}$ (**Definition 11.5.1**: if $\left(\mu_{1}\times\mu_{2}\right)\left(E\right)=0$, the right side above is $0$). Also $\nu_{1}\times\nu_{2}$ is $\sigma$-finite (since $\nu_{j}$ is $\sigma$-finite); by the uniqueness in **Theorem 11.5.5**, $F$ is the Radon–Nikodym derivative of $\nu_{1}\times\nu_{2}$ with respect to $\mu_{1}\times\mu_{2}$, i.e.

$$
\frac{\mathrm{d}\left(\nu_{1}\times\nu_{2}\right)}{\mathrm{d}\left(\mu_{1}\times\mu_{2}\right)}\left(x_{1},x_{2}\right)=f_{1}\left(x_{1}\right)f_{2}\left(x_{2}\right)=\frac{\mathrm{d}\nu_{1}}{\mathrm{d}\mu_{1}}\left(x_{1}\right)\cdot\frac{\mathrm{d}\nu_{2}}{\mathrm{d}\mu_{2}}\left(x_{2}\right).
$$

$\blacksquare$

#### 16

Since $\lambda=\mu+\nu\ge\mu$ and $\nu\ll\mu$, we have $\nu\ll\lambda$ (if $\lambda\left(E\right)=0$, then $\mu\left(E\right)=0$, and hence $\nu\left(E\right)=0$); thus $f=\frac{\mathrm{d}\nu}{\mathrm{d}\lambda}$ exists and $f\ge0$ $\lambda$-almost everywhere (**Theorem 11.5.5**).

We first show $f< 1$ $\mu$-almost everywhere. Suppose, for contradiction, that $\mu\left(\left\{f\ge1\right\}\right)> 0$. Since $\nu\left(\left\{f\ge1\right\}\right)=\int_{\left\{f\ge1\right\}}f\,\mathrm{d}\lambda\ge\lambda\left(\left\{f\ge1\right\}\right)$, and $\lambda=\mu+\nu$,

$$
\nu\left(\left\{f\ge1\right\}\right)\ge\lambda\left(\left\{f\ge1\right\}\right)=\mu\left(\left\{f\ge1\right\}\right)+\nu\left(\left\{f\ge1\right\}\right),
$$

which implies $\mu\left(\left\{f\ge1\right\}\right)\le0$, a contradiction. Hence $0\le f< 1$ $\mu$-almost everywhere.

Finally, we show $\frac{\mathrm{d}\nu}{\mathrm{d}\mu}=\frac{f}{1-f}$. For any $E\in\mathcal M$, from $\lambda=\mu+\nu$ and $f=\frac{\mathrm{d}\nu}{\mathrm{d}\lambda}$,

$$
\nu\left(E\right)=\int_{E}f\,\mathrm{d}\lambda=\int_{E}f\,\mathrm{d}\mu+\int_{E}f\,\mathrm{d}\nu,
$$

i.e. $\int_{E}\left(1-f\right)\mathrm{d}\nu=\int_{E}f\,\mathrm{d}\mu$. Since $1-f> 0$ $\mu$-almost everywhere (also $\lambda$-almost everywhere), by the uniqueness in **Theorem 11.5.5**,

$$
\frac{\mathrm{d}\nu}{\mathrm{d}\mu}=\frac{f}{1-f}.
$$

$\blacksquare$

#### 17

For $E\in\mathcal N$, define $\nu_{0}\left(E\right):=\int_{E}f\,\mathrm{d}\mu$. Then $\nu_{0}$ is a signed measure on $\mathcal N$: finite additivity and countable additivity are guaranteed by the countable additivity of $\mu$ and the integrability of $f$ (dominated convergence), and $\left|\nu_{0}\left(E\right)\right|\le\int_{E}\left|f\right|\mathrm{d}\mu\le\int\left|f\right|\mathrm{d}\mu< \infty$, so $\nu_{0}$ is finite. Also $\nu_{0}\ll\nu$ (**Definition 11.5.1**: if $E\in\mathcal N$ and $\nu\left(E\right)=\mu\left(E\right)=0$, then $\nu_{0}\left(E\right)=\int_{E}f\,\mathrm{d}\mu=0$ ($f\in L^{1}\left(\mu\right)$, and the integral over a null set is $0$). Since $\nu=\mu|_{\mathcal N}$ is $\sigma$-finite (since $\mu$ is $\sigma$-finite), by **Theorem 11.5.5** (Radon–Nikodym theorem), there exists an $\mathcal N$-measurable function $g=\frac{\mathrm{d}\nu_{0}}{\mathrm{d}\nu}\in L^{1}\left(\nu\right)$ such that

$$
\int_{E}f\,\mathrm{d}\mu=\nu_{0}\left(E\right)=\int_{E}g\,\mathrm{d}\nu,
\ \forall E\in\mathcal N.
$$

If $g'\in L^{1}\left(\nu\right)$ also satisfies the same identity, then $\int_{E}\left(g-g'\right)\mathrm{d}\nu=0$ for every $E\in\mathcal N$. Take $E=\left\{g> g'\right\}\in\mathcal N$; since $g-g'\in L^{1}\left(\nu\right)$ and $\int_{\left\{g> g'\right\}}\left(g-g'\right)\mathrm{d}\nu=0$, by the fact that a nonnegative function with integral zero vanishes almost everywhere, we get $g=g'$ $\nu$-almost everywhere on $\left\{g> g'\right\}$; and similarly on $\left\{g< g'\right\}$. Hence $g=g'$ $\nu$-almost everywhere. $\blacksquare$
