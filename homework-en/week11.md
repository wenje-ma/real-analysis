# week11

> **Theorem 10.2.2 (Tonelli's Theorem)**
> 
> If $f:X\times Y\to\left[0,\infty\right]$ is $\mathcal A\otimes\mathcal B$-measurable, then

> **Definition 11.1.1 (Signed Measure)**
> 
> Let $\left(X,\mathcal F\right)$ be a measurable space. A function $\nu:\mathcal F\to\mathbb R\cup\left\{+\infty\right\}$ or $\mathbb R\cup\left\{-\infty\right\}$ is called a signed measure if: (1) $\nu\left(\varnothing\right)=0$; (2) countable additivity: for every sequence of pairwise-disjoint measurable sets $\left\{E_{i}\right\}_{i=1}^{\infty}\subset\mathcal F$, $\nu\left(\bigcup_{i=1}^{\infty}E_{i}\right)=\sum_{i=1}^{\infty}\nu\left(E_{i}\right)$; (3) $\nu$ cannot take both $+\infty$ and $-\infty$.

> **Proposition 11.1.2 (Basic Properties of Signed Measures)**
> 
> Let $\nu$ be a signed measure. Then: (1) finite additivity: for any finitely many pairwise-disjoint $E_{1},\dots,E_{n}\in\mathcal F$, $\nu\left(\bigcup_{i=1}^{n}E_{i}\right)=\sum_{i=1}^{n}\nu\left(E_{i}\right)$; (2) lower continuity: if $\left\{E_{j}\right\}$ is increasing measurable, then $\lim_{j\to\infty}\nu\left(E_{j}\right)=\nu\left(\bigcup_{j}E_{j}\right)$; (3) upper continuity: if $\left\{E_{j}\right\}$ is decreasing measurable and $\nu\left(E_{1}\right)< \infty$, then $\lim_{j\to\infty}\nu\left(E_{j}\right)=\nu\left(\bigcap_{j}E_{j}\right)$.

> **Definition 11.2.1 (Positive Set, Negative Set, Null Set)**
> 
> Let $\nu$ be a signed measure on $\left(X,\mathcal F\right)$. A set $P\in\mathcal F$ is positive (written $P\gtrsim0$) if $\nu\left(E\right)\ge0$ for every $E\in\mathcal F$ with $E\subset P$; a set $N\in\mathcal F$ is negative (written $N\lesssim0$) if $\nu\left(E\right)\le0$ for every $E\in\mathcal F$ with $E\subset N$; a set $Z\in\mathcal F$ is a null set if $\nu\left(E\right)=0$ for every $E\in\mathcal F$ with $E\subset Z$.

> **Lemma 11.2.2 (Properties of Positive Sets)**
> 
> (1) Any measurable subset of a positive set is positive; (2) a countable union of positive sets is positive; (3) if $\left\{P_{n}\right\}$ is a sequence of positive sets, then $\bigcap_{n=1}^{\infty}P_{n}$ is positive. The same holds for negative sets.

> **Lemma 11.2.4 (Criterion for a Non-Negative Set)**
> 
> Let $\nu$ be a signed measure. If $E$ is not a negative set, then there exists a positive set $F\subset E$ with $\nu\left(F\right)> 0$.

> **Theorem 11.3.2 (Hahn Decomposition Theorem)**
> 
> Let $\nu$ be a signed measure on $\left(X,\mathcal F\right)$. Then there is a decomposition $X=P\cup N$, where $P$ is positive, $N$ is negative, and $P\cap N=\varnothing$; and this decomposition is unique up to a $\nu$-null set.

> **Definition 11.4.1 (Mutually Singular Signed Measures)**
> 
> Let $\mu$ and $\nu$ be two signed measures on $\left(X,\mathcal F\right)$. If there exists $E\in\mathcal F$ such that $E$ is a $\mu$-null set and $E^{c}$ is a $\nu$-null set, then $\mu$ and $\nu$ are mutually singular, written $\mu\perp\nu$.

$$
Mf\left(x\right)=\sup_{r> 0}\frac{1}{\left|B\left(x,r\right)\right|}\int_{B\left(x,r\right)}\left|f\left(y\right)\right|\mathrm{d}y,
$$
where $B\left(x,r\right)$ is the open ball centered at $x$ with radius $r$, and $\left|B\left(x,r\right)\right|$ denotes its Lebesgue measure.

> **Definition 11.4.1 (Mutually Singular)**
> 
> Let $\mu$ and $\nu$ be two signed measures on $\left(X,\mathcal F\right)$. If there exists $E\in\mathcal F$ such that $E$ is a $\mu$-null set and $E^{c}$ is a $\nu$-null set, then $\mu$ and $\nu$ are mutually singular, written $\mu\perp\nu$.

> **Theorem 11.4.3 (Jordan Decomposition Theorem)**
> 
> Let $\nu$ be a signed measure on $\left(X,\mathcal F\right)$. Then there is a unique pair of mutually singular positive measures $\nu^{+}$ and $\nu^{-}$ such that $\nu=\nu^{+}-\nu^{-}$.

> **Definition 11.4.4 (Variation Measure)**
> 
> Let $\nu$ be a signed measure with Jordan decomposition $\nu=\nu^{+}-\nu^{-}$. $\nu^{+}$ is the positive variation, $\nu^{-}$ the negative variation, and $\left|\nu\right|=\nu^{+}+\nu^{-}$ the total variation measure.

> **Definition 11.5.1 (Absolute Continuity)**
> 
> Let $\mu$ be a positive measure and $\nu$ a signed measure. We say $\nu$ is absolutely continuous w.r.t. $\mu$ (written $\nu\ll\mu$) if $\mu\left(E\right)=0\Rightarrow\nu\left(E\right)=0$ for every $E\in\mathcal F$.

> **Remark 11.5.3 (Absolute Continuity of the Integral w.r.t. the Measure)**
> 
> If $f\in L^{1}\left(\mu\right)$, then $\lim_{\mu\left(E\right)\to0}\int_{E}f\,\mathrm{d}\mu=0$.

> **Theorem 11.5.5 (Radon-Nikodym Theorem)**
> 
> Let $\mu$ be a $\sigma$-finite positive measure and $\nu$ a signed measure with $\nu\ll\mu$. Then there exists a measurable function $f:X\to\mathbb R$ such that $\nu\left(E\right)=\int_{E}f\,\mathrm{d}\mu$ for every $E\in\mathcal F$; and $\nu^{+}\left(E\right)=\int_{E}f^{+}\mathrm{d}\mu$, $\nu^{-}\left(E\right)=\int_{E}f^{-}\mathrm{d}\mu$, $\left|\nu\right|\left(E\right)=\int_{E}\left|f\right|\mathrm{d}\mu$. The function $f$ is the Radon-Nikodym derivative of $\nu$ w.r.t. $\mu$, written $f=\frac{\mathrm{d}\nu}{\mathrm{d}\mu}$.

> **Definition 14.0.6 (Functions of Bounded Variation)**
> 
> Let $f:\left[a,b\right]\to\mathbb R$. For any partition $P:a=x_{0}< x_{1}< \cdots< x_{n}=b$ of $\left[a,b\right]$, define the variation $V\left(f,P\right)=\sum_{i=1}^{n}\left|f\left(x_{i}\right)-f\left(x_{i-1}\right)\right|$. The total variation of $f$ on $\left[a,b\right]$ is $V_{a}^{b}\left(f\right)=\sup_{P}V\left(f,P\right)$. If $V_{a}^{b}\left(f\right)< +\infty$, $f$ is called a bounded-variation function, written $f\in BV\left(\left[a,b\right]\right)$.

> **Theorem 14.0.7 (Basic Properties of Bounded-Variation Functions)**
> 
> Let $f,g\in BV\left(\left[a,b\right]\right)$. Then: (1) $BV\left(\left[a,b\right]\right)$ is a linear space; (2) $f$ is bounded; (3) if $f$ satisfies a Lipschitz condition, then $f\in BV\left(\left[a,b\right]\right)$; (4) a monotone function is always of bounded variation.

> **Theorem 14.0.10 (Discontinuity Properties of Bounded-Variation Functions)**
> 
> If $f\in BV\left(\left[a,b\right]\right)$, then: (1) $f$ has at most countably many discontinuities; (2) all discontinuities are jump discontinuities.

## 1

For $j=1,2$, let $\mu_{j},\nu_{j}$ be $\sigma$-finite measures on $\left(X_{j},\mathcal M_{j}\right)$ with $\nu_{j}\ll\mu_{j}$. Then $\nu_{1}\times\nu_{2}\ll\mu_{1}\times\mu_{2}$, and

$$
\frac{\mathrm{d}\left(\nu_{1}\times\nu_{2}\right)}{\mathrm{d}\left(\mu_{1}\times\mu_{2}\right)}\left(x_{1},x_{2}\right)=\frac{\mathrm{d}\nu_{1}}{\mathrm{d}\mu_{1}}\left(x_{1}\right)\cdot\frac{\mathrm{d}\nu_{2}}{\mathrm{d}\mu_{2}}\left(x_{2}\right).
$$

### Solution to 1

Since $\nu_{j}\ll\mu_{j}$ and $\mu_{j}$ is a $\sigma$-finite positive measure, by **Theorem 11.5.5 (Radon-Nikodym Theorem)** there is an $\mathcal M_{j}$-measurable $f_{j}=\frac{\mathrm{d}\nu_{j}}{\mathrm{d}\mu_{j}}\ge0$ with $\nu_{j}\left(E\right)=\int_{E}f_{j}\,\mathrm{d}\mu_{j}$ for every $E\in\mathcal M_{j}$. Define $F:X_{1}\times X_{2}\to\left[0,\infty\right]$ by $F\left(x_{1},x_{2}\right)=f_{1}\left(x_{1}\right)f_{2}\left(x_{2}\right)$; then $F$ is $\mathcal M_{1}\otimes\mathcal M_{2}$-measurable. For a measurable rectangle $A\times B\in\mathcal M_{1}\otimes\mathcal M_{2}$, by **Theorem 10.2.2 (Tonelli's Theorem)**,

$$
\int_{A\times B}F\,\mathrm{d}\left(\mu_{1}\times\mu_{2}\right)=\left(\int_{A}f_{1}\,\mathrm{d}\mu_{1}\right)\left(\int_{B}f_{2}\,\mathrm{d}\mu_{2}\right)=\nu_{1}\left(A\right)\nu_{2}\left(B\right)=\left(\nu_{1}\times\nu_{2}\right)\left(A\times B\right).
$$

By uniqueness of the product measure (agreeing on the generating rectangle family), for every $E\in\mathcal M_{1}\otimes\mathcal M_{2}$, $\left(\nu_{1}\times\nu_{2}\right)\left(E\right)=\int_{E}F\,\mathrm{d}\left(\mu_{1}\times\mu_{2}\right)$. This implies $\nu_{1}\times\nu_{2}\ll\mu_{1}\times\mu_{2}$ (**Definition 11.5.1 (Absolute Continuity)**: if $\left(\mu_{1}\times\mu_{2}\right)\left(E\right)=0$, the right side is $0$). Also $\nu_{1}\times\nu_{2}$ is $\sigma$-finite (since $\nu_{j}$ is $\sigma$-finite); by the uniqueness in **Theorem 11.5.5 (Radon-Nikodym Theorem)**, $F$ is the Radon-Nikodym derivative of $\nu_{1}\times\nu_{2}$ w.r.t. $\mu_{1}\times\mu_{2}$, i.e.

$$
\frac{\mathrm{d}\left(\nu_{1}\times\nu_{2}\right)}{\mathrm{d}\left(\mu_{1}\times\mu_{2}\right)}\left(x_{1},x_{2}\right)=\frac{\mathrm{d}\nu_{1}}{\mathrm{d}\mu_{1}}\left(x_{1}\right)\cdot\frac{\mathrm{d}\nu_{2}}{\mathrm{d}\mu_{2}}\left(x_{2}\right).
$$

$\blacksquare$

## 2

Let $\mu,\nu$ be measures on $\left(X,\mathcal M\right)$ with $\nu\ll\mu$, and set $\lambda=\mu+\nu$. If $f=\frac{\mathrm{d}\nu}{\mathrm{d}\lambda}$, then $0\le f< 1$ $\mu$-a.e., and $\frac{\mathrm{d}\nu}{\mathrm{d}\mu}=\frac{f}{1-f}$.

### Solution to 2

Since $\lambda=\mu+\nu\ge\mu$ and $\nu\ll\mu$, we have $\nu\ll\lambda$ (if $\lambda\left(E\right)=0$, then $\mu\left(E\right)=0$, hence $\nu\left(E\right)=0$), so $f=\frac{\mathrm{d}\nu}{\mathrm{d}\lambda}$ exists and $f\ge0$ $\lambda$-a.e. (**Theorem 11.5.5 (Radon-Nikodym Theorem)**).

First show $f< 1$ $\mu$-a.e. Suppose otherwise that $\mu\left(\left\{f\ge1\right\}\right)> 0$. Since $\nu\left(\left\{f\ge1\right\}\right)=\int_{\left\{f\ge1\right\}}f\,\mathrm{d}\lambda\ge\lambda\left(\left\{f\ge1\right\}\right)$, and $\lambda=\mu+\nu$, we get $\nu\left(\left\{f\ge1\right\}\right)\ge\lambda\left(\left\{f\ge1\right\}\right)=\mu\left(\left\{f\ge1\right\}\right)+\nu\left(\left\{f\ge1\right\}\right)$, implying $\mu\left(\left\{f\ge1\right\}\right)\le0$, a contradiction. Hence $0\le f< 1$ $\mu$-a.e.

Finally show $\frac{\mathrm{d}\nu}{\mathrm{d}\mu}=\frac{f}{1-f}$. For any $E\in\mathcal M$, by $\lambda=\mu+\nu$ and $f=\frac{\mathrm{d}\nu}{\mathrm{d}\lambda}$,

$$
\nu\left(E\right)=\int_{E}f\,\mathrm{d}\lambda=\int_{E}f\,\mathrm{d}\mu+\int_{E}f\,\mathrm{d}\nu,
$$

i.e. $\int_{E}\left(1-f\right)\mathrm{d}\nu=\int_{E}f\,\mathrm{d}\mu$. Since $1-f> 0$ $\mu$-a.e. (also $\lambda$-a.e.), by the uniqueness in **Theorem 11.5.5 (Radon-Nikodym Theorem)**, $\frac{\mathrm{d}\nu}{\mathrm{d}\mu}=\frac{f}{1-f}$. $\blacksquare$

## 3

Let $\left(X,\mathcal M,\mu\right)$ be a $\sigma$-finite measure space, $\mathcal N$ a sub-$\sigma$-algebra of $\mathcal M$, and $\nu=\mu|_{\mathcal N}$. If $f\in L^{1}\left(\mu\right)$, then there exists $g\in L^{1}\left(\nu\right)$ (hence $g$ is $\mathcal N$-measurable) such that $\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\nu$ for every $E\in\mathcal N$; and if $g'$ is another such function, then $g=g'$ $\nu$-a.e.

### Solution to 3

For $E\in\mathcal N$, define $\nu_{0}\left(E\right):=\int_{E}f\,\mathrm{d}\mu$. Then $\nu_{0}$ is a signed measure on $\mathcal N$: finite and countable additivity follow from countable additivity of $\mu$ and integrability of $f$ (dominated convergence), and $\left|\nu_{0}\left(E\right)\right|\le\int_{E}\left|f\right|\mathrm{d}\mu\le\int\left|f\right|\mathrm{d}\mu< \infty$, so $\nu_{0}$ is finite. Also $\nu_{0}\ll\nu$ (**Definition 11.5.1 (Absolute Continuity)**): if $E\in\mathcal N$ and $\nu\left(E\right)=\mu\left(E\right)=0$, then $\nu_{0}\left(E\right)=\int_{E}f\,\mathrm{d}\mu=0$ ($f\in L^{1}\left(\mu\right)$, and the integral over a null set is $0$). Since $\nu=\mu|_{\mathcal N}$ is $\sigma$-finite (as $\mu$ is $\sigma$-finite), by **Theorem 11.5.5 (Radon-Nikodym Theorem)** there is an $\mathcal N$-measurable $g=\frac{\mathrm{d}\nu_{0}}{\mathrm{d}\nu}\in L^{1}\left(\nu\right)$ such that $\int_{E}f\,\mathrm{d}\mu=\nu_{0}\left(E\right)=\int_{E}g\,\mathrm{d}\nu$ for every $E\in\mathcal N$.

If $g'\in L^{1}\left(\nu\right)$ also satisfies the same identity, then $\int_{E}\left(g-g'\right)\mathrm{d}\nu=0$ for every $E\in\mathcal N$. Taking $E=\left\{g> g'\right\}\in\mathcal N$, since $g-g'\in L^{1}\left(\nu\right)$ and $\int_{\left\{g> g'\right\}}\left(g-g'\right)\mathrm{d}\nu=0$, by the fact that a nonnegative function with zero integral vanishes a.e., we get $g=g'$ $\nu$-a.e. on $\left\{g> g'\right\}$; similarly on $\left\{g< g'\right\}$. Hence $g=g'$ $\nu$-a.e. $\blacksquare$

## 4

Let $f\in L^{1}\left(\mathbb R^{n}\right)$ and $f\ne0$. Prove that there exist $C,R> 0$ such that $Hf\left(x\right)\ge C\left|x\right|^{-n}$ for $\left|x\right|> R$. Hence for small $\lambda$, $m\left(\left\{x:Hf\left(x\right)> \lambda\right\}\right)\ge C'\lambda^{-1}$, so the estimate in the maximal theorem is essentially sharp.

### Solution to 4

Write $Hf$ for the Hardy-Littlewood maximal function (Hardy-Littlewood Maximal Function). Since $f\ne0$ and $f\in L^{1}\left(\mathbb R^{n}\right)$, there is a ball $K$ (some compact set suffices) with $\int_{K}\left|f\right|\mathrm{d}y> 0$; otherwise all $\int_{K}f$ vanishing would force $f=0$ a.e., a contradiction. Set $c=\int_{K}\left|f\right|\mathrm{d}y> 0$, and take $R> 0$ with $K\subset B\left(0,R\right)$ (i.e. $\sup_{y\in K}\left|y\right|< R$). For $\left|x\right|> R$, since $K\subset B\left(0,R\right)$ and $R< \left|x\right|$, we have $K\subset B\left(x,2\left|x\right|\right)$. Hence, by the definition of the maximal function and Ball-Volume Formula,

$$
Hf\left(x\right)\ge\frac{1}{\left|B\left(x,2\left|x\right|\right)\right|}\int_{B\left(x,2\left|x\right|\right)}\left|f\right|\mathrm{d}y\ge\frac{1}{\left|B\left(x,2\left|x\right|\right)\right|}\int_{K}\left|f\right|\mathrm{d}y=\frac{c}{C_{n}\left(2\left|x\right|\right)^{n}}=\frac{c}{2^{n}C_{n}}\left|x\right|^{-n}.
$$

Taking $C=\frac{c}{2^{n}C_{n}}> 0$, we get $Hf\left(x\right)\ge C\left|x\right|^{-n}$ for $\left|x\right|> R$.

For the second part, by the first part, when $0< \lambda< C/R^{n}$, $\left(C/\lambda\right)^{1/n}> R$, so $\left\{x:\left|x\right|> \left(C/\lambda\right)^{1/n}\right\}\subset\left\{x:Hf\left(x\right)> \lambda\right\}$. By the ball-volume formula, $m\left(\left\{x:\left|x\right|< \left(C/\lambda\right)^{1/n}\right\}\right)=C_{n}\left(\frac{C}{\lambda}\right)=\frac{C_{n}C}{\lambda}$. Setting $C'=C_{n}C$, we get $m\left(\left\{x:Hf\left(x\right)> \lambda\right\}\right)\ge C'\lambda^{-1}$ for small $\lambda> 0$. $\blacksquare$

## 5

A useful variant of the Hardy-Littlewood maximal function is $H^{*}f\left(x\right)=\sup\left\{\frac{1}{m\left(B\right)}\int_{B}\left|f\left(y\right)\right|\mathrm{d}y:B\text{ a ball},x\in B\right\}$. Prove that $Hf\le H^{*}f\le2^{n}Hf$.

### Solution to 5

First show $Hf\le H^{*}f$. For any $r> 0$, the ball $B\left(x,r\right)$ is a ball containing $x$, so $\frac{1}{\left|B\left(x,r\right)\right|}\int_{B\left(x,r\right)}\left|f\right|\mathrm{d}y\le H^{*}f\left(x\right)$. Taking the supremum over $r> 0$ gives $Hf\left(x\right)\le H^{*}f\left(x\right)$.

Now show $H^{*}f\le2^{n}Hf$. Let $B$ be any ball containing $x$; denote its radius by $\rho$ and center by $c$. Since $x\in B$, $\left|x-c\right|\le\rho$, so for every $y\in B$, $\left|y-x\right|\le\left|y-c\right|+\left|c-x\right|\le\rho+\rho=2\rho$, i.e. $B\subset B\left(x,2\rho\right)$. By Ball-Volume Formula, $\left|B\left(x,2\rho\right)\right|=C_{n}\left(2\rho\right)^{n}=2^{n}C_{n}\rho^{n}=2^{n}\left|B\right|$. Hence

$$
\frac{1}{m\left(B\right)}\int_{B}\left|f\right|\mathrm{d}y\le\frac{1}{m\left(B\right)}\int_{B\left(x,2\rho\right)}\left|f\right|\mathrm{d}y=2^{n}\cdot\frac{1}{m\left(B\left(x,2\rho\right)\right)}\int_{B\left(x,2\rho\right)}\left|f\right|\mathrm{d}y\le2^{n}Hf\left(x\right).
$$

Taking the supremum over all balls $B$ containing $x$ gives $H^{*}f\left(x\right)\le2^{n}Hf\left(x\right)$. Combining, $Hf\le H^{*}f\le2^{n}Hf$. $\blacksquare$

## 6

If $\lambda$ and $\mu$ are positive mutually singular Borel measures on $\mathbb R^{n}$ and $\lambda+\mu$ is regular, then both $\lambda$ and $\mu$ are regular.

### Solution to 6

Set $\nu=\lambda+\mu$. Since $\lambda\perp\mu$ (**Definition 11.4.1 (Mutually Singular)**), there is a Borel set $A$ with $\mu\left(A\right)=0$ and $\lambda\left(A^{c}\right)=0$.

Condition (1) of regularity. For any compact set $K$, since $\lambda,\mu\ge0$ and $\nu$ is regular (Regular Borel Measures), $\lambda\left(K\right)\le\nu\left(K\right)< \infty$, and similarly $\mu\left(K\right)< \infty$.

Condition (2) of regularity for $\lambda$. First note that for any $E\in\mathcal B\left(\mathbb R^{n}\right)$, $\lambda\left(E\right)=\lambda\left(E\cap A\right)=\nu\left(E\cap A\right)$, where the second equality uses $\mu\left(E\cap A\right)\le\mu\left(A\right)=0$; similarly $\mu\left(E\right)=\nu\left(E\cap A^{c}\right)$.

For any open $U\supset E$, $U\cap A\supset E\cap A$, so $\lambda\left(U\right)=\nu\left(U\cap A\right)\ge\nu\left(E\cap A\right)=\lambda\left(E\right)$, hence $\inf\left\{\lambda\left(U\right):U\text{ open},U\supset E\right\}\ge\lambda\left(E\right)$.

For the reverse inequality, given $\varepsilon> 0$, since $\nu$ is regular, there is an open set $W\supset E\cap A$ with $\nu\left(W\cap A\right)< \nu\left(E\cap A\right)+\varepsilon=\lambda\left(E\right)+\varepsilon$ (use outer regularity of $\nu$ to choose open $W'\supset E\cap A$ with $\nu\left(W'\right)< \nu\left(E\cap A\right)+\varepsilon$, set $W=W'$, and note $\nu\left(W'\cap A\right)\le\nu\left(W'\right)$). Also, since $\left(E\cap A^{c}\right)\cap A=\varnothing$ and $\lambda\left(E\cap A^{c}\right)=0$, choose a thin enough open neighborhood $V\supset E\cap A^{c}$ with $\nu\left(V\cap A\right)< \varepsilon$ (e.g. take $V=\left\{x:\mathrm{dist}\left(x,E\cap A^{c}\right)< \delta\right\}$ and let $\delta\to0$; then $V\cap A\downarrow\left(E\cap A^{c}\right)\cap A=\varnothing$, and upper continuity gives $\nu\left(V\cap A\right)\to0$). Set $U=W\cup V$; then $U$ is open, $U\supset E$, and $\lambda\left(U\right)=\nu\left(U\cap A\right)\le\nu\left(W\cap A\right)+\nu\left(V\cap A\right)< \lambda\left(E\right)+2\varepsilon$. Hence $\inf\left\{\lambda\left(U\right):U\text{ open},U\supset E\right\}\le\lambda\left(E\right)$. Combining, $\lambda\left(E\right)=\inf\left\{\lambda\left(U\right):U\text{ open},U\supset E\right\}$.

Condition (2) of regularity for $\mu$. Using $\mu\left(E\right)=\nu\left(E\cap A^{c}\right)$ and the regularity of $\nu|_{A^{c}}$, the argument is entirely symmetric, and $\mu$ also satisfies condition (2).

Thus both $\lambda$ and $\mu$ are regular. $\blacksquare$

## 7

Construct an increasing function on $\mathbb R$ whose set of discontinuities is exactly $\mathbb Q$.

### Solution to 7

Enumerate the rationals $\mathbb Q=\left\{q_{1},q_{2},\dots\right\}$ and define $F\left(x\right)=\sum_{q_{n}\le x}2^{-n}$ for $x\in\mathbb R$. This is a sum of at most countably many nonnegative terms, with values in $\left[0,1\right]$. By Series, $\sum_{n}2^{-n}$ converges, so $F$ takes finite values. If $x< y$, then $\left\{n:q_{n}\le x\right\}\subset\left\{n:q_{n}\le y\right\}$, so $F\left(x\right)\le F\left(y\right)$; hence $F$ is increasing.

Every rational point is a discontinuity. For $q_{k}\in\mathbb Q$, as $x$ approaches $q_{k}$ from the left, $\left\{q_{n}\le x\right\}$ does not contain $q_{k}$, so the left limit $F\left(q_{k}-\right)=\sum_{q_{n}< q_{k}}2^{-n}=\sum_{q_{n}\le q_{k}}2^{-n}-2^{-k}=F\left(q_{k}\right)-2^{-k}< F\left(q_{k}\right)$. The right limit $F\left(q_{k}+\right)=\lim_{x\downarrow q_{k}}F\left(x\right)=F\left(q_{k}\right)$ (since for $x> q_{k}$, $q_{k}$ is still counted). Thus $F$ has unequal left and right limits at $q_{k}$, a jump discontinuity.

Every irrational point is a continuity point. Let $x_{0}\in\mathbb R\setminus\mathbb Q$. Given $\varepsilon> 0$, by Series choose $N$ with $\sum_{n> N}2^{-n}< \varepsilon$. Since $x_{0}$ is irrational, choose $\delta> 0$ small enough that $\left(x_{0}-\delta,x_{0}+\delta\right)$ contains none of $q_{1},\dots,q_{N}$ (finitely many points, separable). Then whenever $\left|x-x_{0}\right|< \delta$, the interval $\left(\min\left(x,x_{0}\right),\max\left(x,x_{0}\right)\right]$ contains at most $q_{N+1},q_{N+2},\dots$, so $\left|F\left(x\right)-F\left(x_{0}\right)\right|=\sum_{x_{0}< q_{n}\le x\text{ or }x< q_{n}\le x_{0}}2^{-n}\le\sum_{n> N}2^{-n}< \varepsilon$. Hence $F$ is continuous at $x_{0}$.

Thus the discontinuity set of $F$ is exactly $\mathbb Q$. By **Theorem 14.0.7 (Basic Properties of Bounded-Variation Functions)** (4) and **Theorem 14.0.10 (Discontinuity Properties of Bounded-Variation Functions)**, $F$ is an increasing bounded function, hence of bounded variation, with at most countably many jump discontinuities, which here are exactly $\mathbb Q$. $\blacksquare$
