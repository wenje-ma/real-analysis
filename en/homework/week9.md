# week9

> **Theorem 10.2.2 (Tonelli's Theorem)**<br>If $f:X\times Y\to\left[0,\infty\right]$ is $\mathcal A\otimes\mathcal B$-measurable, then

$$
\int_{X\times Y}f\,\mathrm{d}\left(\mu\times\nu\right)=\int_{X}\left(\int_{Y}f\left(x,y\right)\mathrm{d}\nu\left(y\right)\right)\mathrm{d}\mu\left(x\right)=\int_{Y}\left(\int_{X}f\left(x,y\right)\mathrm{d}\mu\left(x\right)\right)\mathrm{d}\nu\left(y\right),
$$

with all integral values in $\left[0,\infty\right]$.

> **Definition 11.1.1 (Signed Measure)**<br>Let $\left(X,\mathcal F\right)$ be a measurable space. A function $\nu:\mathcal F\to\mathbb R\cup\left\{+\infty\right\}$ or $\mathbb R\cup\left\{-\infty\right\}$ is called a signed measure if: (1) $\nu\left(\varnothing\right)=0$; (2) countable additivity: for every sequence of pairwise-disjoint measurable sets $\left\{E_{i}\right\}_{i=1}^{\infty}\subset\mathcal F$, $\nu\left(\bigcup_{i=1}^{\infty}E_{i}\right)=\sum_{i=1}^{\infty}\nu\left(E_{i}\right)$; (3) $\nu$ cannot take both $+\infty$ and $-\infty$.

> **Proposition 11.1.2 (Basic Properties of Signed Measures)**<br>Let $\nu$ be a signed measure. Then: (1) finite additivity: for any finitely many pairwise-disjoint $E_{1},\dots,E_{n}\in\mathcal F$, $\nu\left(\bigcup_{i=1}^{n}E_{i}\right)=\sum_{i=1}^{n}\nu\left(E_{i}\right)$; (2) lower continuity: if $\left\{E_{j}\right\}$ is increasing measurable, then $\lim_{j\to\infty}\nu\left(E_{j}\right)=\nu\left(\bigcup_{j}E_{j}\right)$; (3) upper continuity: if $\left\{E_{j}\right\}$ is decreasing measurable and $\nu\left(E_{1}\right)< \infty$, then $\lim_{j\to\infty}\nu\left(E_{j}\right)=\nu\left(\bigcap_{j}E_{j}\right)$.

> **Definition 11.2.1 (Positive Set, Negative Set, Null Set)**<br>Let $\nu$ be a signed measure on $\left(X,\mathcal F\right)$. A set $P\in\mathcal F$ is positive (written $P\gtrsim0$) if $\nu\left(E\right)\ge0$ for every $E\in\mathcal F$ with $E\subset P$; a set $N\in\mathcal F$ is negative (written $N\lesssim0$) if $\nu\left(E\right)\le0$ for every $E\in\mathcal F$ with $E\subset N$; a set $Z\in\mathcal F$ is a null set if $\nu\left(E\right)=0$ for every $E\in\mathcal F$ with $E\subset Z$.

> **Lemma 11.2.2 (Properties of Positive Sets)**<br>(1) Any measurable subset of a positive set is positive; (2) a countable union of positive sets is positive; (3) if $\left\{P_{n}\right\}$ is a sequence of positive sets, then $\bigcap_{n=1}^{\infty}P_{n}$ is positive. The same holds for negative sets.

> **Lemma 11.2.4 (Criterion for a Non-Negative Set)**<br>Let $\nu$ be a signed measure. If $E$ is not a negative set, then there exists a positive set $F\subset E$ with $\nu\left(F\right)> 0$.

> **Theorem 11.3.2 (Hahn Decomposition Theorem)**<br>Let $\nu$ be a signed measure on $\left(X,\mathcal F\right)$. Then there is a decomposition $X=P\cup N$, where $P$ is positive, $N$ is negative, and $P\cap N=\varnothing$; and this decomposition is unique up to a $\nu$-null set.

> **Definition 11.4.1 (Mutually Singular Signed Measures)**<br>Let $\mu$ and $\nu$ be two signed measures on $\left(X,\mathcal F\right)$. If there exists $E\in\mathcal F$ such that $E$ is a $\mu$-null set and $E^{c}$ is a $\nu$-null set, then $\mu$ and $\nu$ are mutually singular, written $\mu\perp\nu$.

> **Theorem 11.4.3 (Jordan Decomposition Theorem)**<br>Let $\nu$ be a signed measure on $\left(X,\mathcal F\right)$. Then there is a unique pair of mutually singular positive measures $\nu^{+}$ and $\nu^{-}$ such that $\nu=\nu^{+}-\nu^{-}$.

> **Definition 11.4.4 (Variation Measure)**<br>Let $\nu$ be a signed measure with Jordan decomposition $\nu=\nu^{+}-\nu^{-}$. $\nu^{+}$ is the positive variation, $\nu^{-}$ the negative variation, and $\left|\nu\right|=\nu^{+}+\nu^{-}$ the total variation measure.

> **Definition 11.5.1 (Absolute Continuity)**<br>Let $\mu$ be a positive measure and $\nu$ a signed measure. We say $\nu$ is absolutely continuous w.r.t. $\mu$ (written $\nu\ll\mu$) if $\mu\left(E\right)=0\Rightarrow\nu\left(E\right)=0$ for every $E\in\mathcal F$.

> **Remark 11.5.3 (Absolute Continuity of the Integral w.r.t. the Measure)**<br>If $f\in L^{1}\left(\mu\right)$, then $\lim_{\mu\left(E\right)\to0}\int_{E}f\,\mathrm{d}\mu=0$.

> **Theorem 11.5.5 (Radon-Nikodym Theorem)**<br>Let $\mu$ be a $\sigma$-finite positive measure and $\nu$ a signed measure with $\nu\ll\mu$. Then there exists a measurable function $f:X\to\mathbb R$ such that $\nu\left(E\right)=\int_{E}f\,\mathrm{d}\mu$ for every $E\in\mathcal F$; and $\nu^{+}\left(E\right)=\int_{E}f^{+}\mathrm{d}\mu$, $\nu^{-}\left(E\right)=\int_{E}f^{-}\mathrm{d}\mu$, $\left|\nu\right|\left(E\right)=\int_{E}\left|f\right|\mathrm{d}\mu$. The function $f$ is the Radon-Nikodym derivative of $\nu$ w.r.t. $\mu$, written $f=\frac{\mathrm{d}\nu}{\mathrm{d}\mu}$.

---

## 1

Let $\nu$ be a signed measure on $\left(X,\mathcal F\right)$ not taking the value $-\infty$, and let $E$ not be a negative set. Prove there is a measurable set $G\subset E$ with $\nu\left(G\right)=\sup\left\{\nu\left(F\right):F\subset E,\nu\left(F\right)> 0\right\}> 0$, and such that $E\setminus G$ is a negative set.

### Solution 1

Set $\alpha=\sup\left\{\nu\left(F\right):F\subset E,\nu\left(F\right)> 0\right\}$. Since $E$ is not negative, by **Lemma 11.2.4 (Criterion for a Non-Negative Set)** there is a positive set $F_{0}\subset E$ with $\nu\left(F_{0}\right)> 0$, so $\alpha\ge\nu\left(F_{0}\right)> 0$, i.e. $\alpha> 0$.

First show $\alpha$ is attained by a positive set. Let $\beta=\sup\left\{\nu\left(P\right):P\subset E,P\text{ positive}\right\}$; then $\beta\ge\nu\left(F_{0}\right)> 0$. Clearly $\beta\le\alpha$, since a positive set $P\subset E$ with $\nu\left(P\right)> 0$ enters the supremum defining $\alpha$. Conversely, $\alpha\le\beta$: take any $F\subset E$ with $\nu\left(F\right)> 0$. If $F$ is positive, then $\nu\left(F\right)\le\beta$; if $F$ is not positive, there exists $C\subset F$ with $\nu\left(C\right)< 0$. Set $F_{1}=F\setminus C$; then $\nu\left(F_{1}\right)=\nu\left(F\right)-\nu\left(C\right)> \nu\left(F\right)$. Repeating this construction gives an increasing measurable sequence $\left\{F_{n}\right\}$ with $\nu\left(F_{n}\right)$ strictly increasing to some $\gamma$. By **Proposition 11.1.2 (Basic Properties of Signed Measures)** (2) (lower continuity), $\nu\left(\bigcup_{n}F_{n}\right)=\lim_{n}\nu\left(F_{n}\right)=\gamma$. If $\bigcup_{n}F_{n}$ were not positive, one could extract from it a subset of still larger measure, contradicting the convergence to $\gamma$; hence $\bigcup_{n}F_{n}\subset E$ is positive. Thus $\gamma=\nu\left(\bigcup_{n}F_{n}\right)\le\beta$; and since $\nu\left(F_{n}\right)\uparrow\gamma$ with $\nu\left(F_{1}\right)> \nu\left(F\right)$, we get $\nu\left(F\right)< \gamma\le\beta$. Hence $\nu\left(F\right)\le\beta$ for every such $F$, i.e. $\alpha\le\beta$. Combining, $\alpha=\beta$.

By the definition of $\beta$, take a sequence of positive sets $\left\{P_{n}\right\}\subset E$ with $\nu\left(P_{n}\right)\to\beta$. Let $G=\bigcup_{n=1}^{\infty}P_{n}\subset E$; then $G$ is positive (**Lemma 11.2.2 (Properties of Positive Sets)** (2)). Set $Q_{n}=\bigcup_{k=1}^{n}P_{k}$; then $\left\{Q_{n}\right\}$ is an increasing union of positive sets, hence positive, and $\nu\left(Q_{n}\right)\ge\nu\left(P_{n}\right)\to\beta$; also $Q_{n}\subset E$ is positive, so $\nu\left(Q_{n}\right)\le\beta$. Thus $\nu\left(Q_{n}\right)\to\beta$, and by **Proposition 11.1.2 (Basic Properties of Signed Measures)** (2) (lower continuity), $\nu\left(G\right)=\lim_{n\to\infty}\nu\left(Q_{n}\right)=\beta=\alpha> 0$.

Finally show $E\setminus G$ is negative. Suppose otherwise; then by **Lemma 11.2.4 (Criterion for a Non-Negative Set)** there is a positive set $F\subset E\setminus G$ with $\nu\left(F\right)> 0$. Since $G\cap F=\varnothing$, $G\cup F\subset E$ and $G\cup F$ is positive (**Lemma 11.2.2 (Properties of Positive Sets)** (2)); hence $\nu\left(G\cup F\right)=\nu\left(G\right)+\nu\left(F\right)=\alpha+\nu\left(F\right)> \alpha=\beta$, contradicting that $\beta$ is the supremum of the measures of all positive sets in $E$. Thus $E\setminus G$ is negative. $\blacksquare$

---

## 2

Let $\nu$ be a signed measure on $\left(X,\mathcal M\right)$.

(a) $L^{1}\left(\nu\right)=L^{1}\left(\left|\nu\right|\right)$;

(b) if $f\in L^{1}\left(\nu\right)$, then $\left|\int f\,\mathrm{d}\nu\right|\le\int\left|f\right|\mathrm{d}\left|\nu\right|$;

(c) if $E\in\mathcal M$, then $\left|\nu\right|\left(E\right)=\sup\left\{\left|\int_{E}f\,\mathrm{d}\nu\right|:\left|f\right|\le1\right\}$.

### Solution 2

**(a).** By **Definition 11.4.4 (Variation Measure)**, $\left|\nu\right|=\nu^{+}+\nu^{-}$. Thus for any $f$,

$$
\int\left|f\right|\mathrm{d}\left|\nu\right|=\int\left|f\right|\mathrm{d}\nu^{+}+\int\left|f\right|\mathrm{d}\nu^{-}.
$$

All three terms are nonnegative, so the left side is finite iff both right-side terms are finite, i.e. $f\in L^{1}\left(\nu^{+}\right)\cap L^{1}\left(\nu^{-}\right)=L^{1}\left(\nu\right)$. Hence $L^{1}\left(\nu\right)=L^{1}\left(\left|\nu\right|\right)$.

**(b).** By **Theorem 11.4.3 (Jordan Decomposition Theorem)**, $\nu=\nu^{+}-\nu^{-}$. By the triangle inequality and (a),

$$
\left|\int f\,\mathrm{d}\nu\right|=\left|\int f\,\mathrm{d}\nu^{+}-\int f\,\mathrm{d}\nu^{-}\right|\le\int\left|f\right|\mathrm{d}\nu^{+}+\int\left|f\right|\mathrm{d}\nu^{-}=\int\left|f\right|\mathrm{d}\left|\nu\right|.
$$

**(c).** First $\le$: for any measurable $g$ with $\left|g\right|\le1$, by (b), $\left|\int_{E}g\,\mathrm{d}\nu\right|\le\int_{E}\left|g\right|\mathrm{d}\left|\nu\right|\le\int_{E}1\,\mathrm{d}\left|\nu\right|=\left|\nu\right|\left(E\right)$, so the supremum is $\le\left|\nu\right|\left(E\right)$.

Then $\ge$: take a Hahn decomposition $X=P\cup N$ of $\nu$ (**Theorem 11.3.2 (Hahn Decomposition Theorem)**), set $g=\chi_{E\cap P}-\chi_{E\cap N}$; then $\left|g\right|\le1$ and $g$ is measurable. By **Theorem 11.4.3 (Jordan Decomposition Theorem)**, $\nu^{+}\left(E\right)=\nu\left(E\cap P\right)$ and $\nu^{-}\left(E\right)=-\nu\left(E\cap N\right)$. Hence $\int_{E}g\,\mathrm{d}\nu=\nu\left(E\cap P\right)-\nu\left(E\cap N\right)=\nu^{+}\left(E\right)+\nu^{-}\left(E\right)=\left|\nu\right|\left(E\right)$. Thus the supremum is $\ge\left|\nu\right|\left(E\right)$. Equality follows. $\blacksquare$

---

## 3

Let $\nu\left(E\right)=\int_{E}f\,\mathrm{d}\mu$, where $\mu$ is a positive measure and $f$ is an extended $\mu$-integrable function. Describe in terms of $f$ and $\mu$ the Hahn decomposition of $\nu$, and its positive variation, negative variation, and total variation.

### Solution 3

$f$ is real-valued measurable, with at least one of $\int f^{+}\mathrm{d}\mu$, $\int f^{-}\mathrm{d}\mu$ finite. By **Definition 11.2.1 (Positive Set, Negative Set, Null Set)**: for $E\in\mathcal M$, $E$ is a $\nu$-positive set iff for every measurable $F\subset E$, $\nu\left(F\right)=\int_{F}f\,\mathrm{d}\mu\ge0$; since this must hold for both $F=E\cap\left\{f< 0\right\}$ and $F=E\cap\left\{f> 0\right\}$, $E$ is positive iff $f\ge0$ $\mu$-a.e. on $E$. Similarly, $E$ is negative iff $f\le0$ $\mu$-a.e. on $E$; $E$ is a null set iff $f=0$ $\mu$-a.e. on $E$.

Thus $X=P\cup N$, where $P=\left\{x:f\left(x\right)\ge0\right\}$ and $N=\left\{x:f\left(x\right)< 0\right\}$, is a Hahn decomposition of $\nu$ (**Theorem 11.3.2 (Hahn Decomposition Theorem)**): $P$ positive, $N$ negative, $P\cap N=\varnothing$, $P\cup N=X$. (The null set $\left\{f=0\right\}$ may be merged into $P$ or $N$ without changing the decomposition.)

By **Theorem 11.4.3 (Jordan Decomposition Theorem)**, $\nu^{+}\left(E\right)=\nu\left(E\cap P\right)=\int_{E\cap P}f\,\mathrm{d}\mu=\int_{E}f^{+}\mathrm{d}\mu$ (since $f\ge0$ on $P$), and $\nu^{-}\left(E\right)=-\nu\left(E\cap N\right)=-\int_{E\cap N}f\,\mathrm{d}\mu=\int_{E}f^{-}\mathrm{d}\mu$ (since $f\le0$ on $N$). Hence $\nu^{+}\left(E\right)=\int_{E}f^{+}\mathrm{d}\mu$, $\nu^{-}\left(E\right)=\int_{E}f^{-}\mathrm{d}\mu$, $\left|\nu\right|\left(E\right)=\int_{E}\left|f\right|\mathrm{d}\mu$. $\blacksquare$

---

## 4

Let $\nu$ be a signed measure on $\left(X,\mathcal M\right)$ and $E\in\mathcal M$.

(a) $\nu^{+}\left(E\right)=\sup\left\{\nu\left(F\right):F\in\mathcal M,F\subset E\right\}$, and $\nu^{-}\left(E\right)=-\inf\left\{\nu\left(F\right):F\in\mathcal M,F\subset E\right\}$;

(b) $\left|\nu\right|\left(E\right)=\sup\left\{\sum_{i}\left|\nu\left(E_{i}\right)\right|:n\in\mathbb N,E_{1},\dots,E_{n}\text{ pairwise disjoint},\bigcup_{i=1}^{n}E_{i}=E\right\}$.

### Solution 4

**(a).** Take a Hahn decomposition $X=P\cup N$ of $\nu$ (**Theorem 11.3.2 (Hahn Decomposition Theorem)**); then $\nu^{+}\left(E\right)=\nu\left(E\cap P\right)$ and $\nu^{-}\left(E\right)=-\nu\left(E\cap N\right)$ (**Theorem 11.4.3 (Jordan Decomposition Theorem)**).

For any $F\in\mathcal M$ with $F\subset E$, by $\nu=\nu^{+}-\nu^{-}$ and $\nu^{-}\ge0$, $\nu\left(F\right)=\nu^{+}\left(F\right)-\nu^{-}\left(F\right)\le\nu^{+}\left(F\right)\le\nu^{+}\left(E\right)$ (the last by monotonicity of $\nu^{+}$, since $F\subset E$). Hence $\sup\left\{\nu\left(F\right):F\subset E\right\}\le\nu^{+}\left(E\right)$. Taking $F=E\cap P\subset E$, $\nu\left(E\cap P\right)=\nu^{+}\left(E\cap P\right)-\nu^{-}\left(E\cap P\right)=\nu^{+}\left(E\cap P\right)=\nu^{+}\left(E\right)$ (since $E\cap P\subset P$ is positive, $\nu^{-}\left(E\cap P\right)=0$). Hence the supremum is $\ge\nu^{+}\left(E\right)$. Combining, $\nu^{+}\left(E\right)=\sup\left\{\nu\left(F\right):F\subset E\right\}$.

Similarly, for $F\subset E$, $\nu\left(F\right)=\nu^{+}\left(F\right)-\nu^{-}\left(F\right)\ge-\nu^{-}\left(F\right)\ge-\nu^{-}\left(E\right)$, so $\inf\left\{\nu\left(F\right):F\subset E\right\}\ge-\nu^{-}\left(E\right)$, i.e. $-\inf\left\{\nu\left(F\right):F\subset E\right\}\le\nu^{-}\left(E\right)$. Taking $F=E\cap N$, $\nu\left(E\cap N\right)=-\nu^{-}\left(E\cap N\right)=-\nu^{-}\left(E\right)$, so the infimum is $\le-\nu^{-}\left(E\right)$, i.e. $-\inf\ge\nu^{-}\left(E\right)$. Combining, $\nu^{-}\left(E\right)=-\inf\left\{\nu\left(F\right):F\subset E\right\}$.

**(b).** First $\le$: for any pairwise-disjoint $\left\{E_{i}\right\}$ with union $E$, by $\nu=\nu^{+}-\nu^{-}$ and the triangle inequality,

$$
\sum_{i}\left|\nu\left(E_{i}\right)\right|=\sum_{i}\left|\nu^{+}\left(E_{i}\right)-\nu^{-}\left(E_{i}\right)\right|\le\sum_{i}\left[\nu^{+}\left(E_{i}\right)+\nu^{-}\left(E_{i}\right)\right]=\nu^{+}\left(E\right)+\nu^{-}\left(E\right)=\left|\nu\right|\left(E\right),
$$

so the supremum is $\le\left|\nu\right|\left(E\right)$.

Then $\ge$: take a Hahn decomposition $X=P\cup N$ (**Theorem 11.3.2 (Hahn Decomposition Theorem)**), set $E_{1}=E\cap P$, $E_{2}=E\cap N$; then $E_{1},E_{2}$ are pairwise disjoint and $E_{1}\cup E_{2}=E$. Hence $\left|\nu\left(E_{1}\right)\right|+\left|\nu\left(E_{2}\right)\right|=\nu^{+}\left(E\cap P\right)+\nu^{-}\left(E\cap N\right)=\nu^{+}\left(E\right)+\nu^{-}\left(E\right)=\left|\nu\right|\left(E\right)$, so the supremum is $\ge\left|\nu\right|\left(E\right)$. Equality follows. $\blacksquare$

---

## 5

Let $\left\{\nu_{j}\right\}$ be a sequence of positive measures. If $\nu_{j}\perp\mu$ for all $j$, then $\sum_{j}\nu_{j}\perp\mu$; if $\nu_{j}\ll\mu$ for all $j$, then $\sum_{j}\nu_{j}\ll\mu$.

### Solution 5

**(Singular case).** Since $\nu_{j}\perp\mu$ (**Definition 11.4.1 (Mutually Singular Signed Measures)**), for each $j$ there is $E_{j}\in\mathcal M$ such that $E_{j}$ is a $\mu$-null set and $E_{j}^{c}$ is a $\nu_{j}$-null set, i.e. $\mu\left(E_{j}\right)=0$ and $\nu_{j}\left(E_{j}^{c}\right)=0$. Let $E=\bigcup_{j=1}^{\infty}E_{j}$. By countable subadditivity of $\mu$, $\mu\left(E\right)\le\sum_{j=1}^{\infty}\mu\left(E_{j}\right)=0$, so $E$ is a $\mu$-null set. Also $E^{c}=\bigcap_{j=1}^{\infty}E_{j}^{c}\subset E_{k}^{c}$ for every $k$; by monotonicity of $\nu_{k}$, $\nu_{k}\left(E^{c}\right)\le\nu_{k}\left(E_{k}^{c}\right)=0$, so $\nu_{k}\left(E^{c}\right)=0$ for every $k$, and hence $\left(\sum_{j}\nu_{j}\right)\left(E^{c}\right)=\sum_{j}\nu_{j}\left(E^{c}\right)=0$. Thus $\sum_{j}\nu_{j}\perp\mu$.

**(Absolute continuity case).** Let $\nu_{j}\ll\mu$ for all $j$ (**Definition 11.5.1 (Absolute Continuity)**). If $\mu\left(E\right)=0$, then $\nu_{j}\left(E\right)=0$ for all $j$, so $\left(\sum_{j}\nu_{j}\right)\left(E\right)=\sum_{j}\nu_{j}\left(E\right)=0$. Hence $\sum_{j}\nu_{j}\ll\mu$. $\blacksquare$

---

## 6

Let $\mu$ be a positive measure. A family $\left\{f_{\alpha}\right\}_{\alpha\in A}\subset L^{1}\left(\mu\right)$ is called uniformly integrable if for every $\varepsilon> 0$ there exists $\delta> 0$ such that $\left|\int_{E}f_{\alpha}\,\mathrm{d}\mu\right|< \varepsilon$ for all $\alpha\in A$, whenever $\mu\left(E\right)< \delta$.

(a) Any finite subset of $L^{1}\left(\mu\right)$ is uniformly integrable;

(b) if $\left\{f_{n}\right\}$ is a sequence in $L^{1}\left(\mu\right)$ converging to $f\in L^{1}\left(\mu\right)$ in the $L^{1}$ metric, then $\left\{f_{n}\right\}$ is uniformly integrable.

### Solution 6

**(a).** Let $\left\{f_{1},\dots,f_{n}\right\}\subset L^{1}\left(\mu\right)$. For each $j$, by **Remark 11.5.3 (Absolute Continuity of the Integral w.r.t. the Measure)** ($f_{j}\in L^{1}\left(\mu\right)$, $\lim_{\mu\left(E\right)\to0}\int_{E}f_{j}\,\mathrm{d}\mu=0$), there is $\delta_{j}> 0$ such that $\mu\left(E\right)< \delta_{j}\Rightarrow\left|\int_{E}f_{j}\,\mathrm{d}\mu\right|< \varepsilon$. Take $\delta=\min_{1\le j\le n}\delta_{j}> 0$; then whenever $\mu\left(E\right)< \delta$, for all $j$ we have $\mu\left(E\right)< \delta_{j}$, hence $\left|\int_{E}f_{j}\,\mathrm{d}\mu\right|< \varepsilon$. Thus $\left\{f_{1},\dots,f_{n}\right\}$ is uniformly integrable.

**(b).** Since $\int\left|f_{n}-f\right|\mathrm{d}\mu\to0$, there is $N$ such that for $n\ge N$, $\int\left|f_{n}-f\right|\mathrm{d}\mu< \frac{\varepsilon}{2}$. By (a), the singleton $\left\{f\right\}$ is uniformly integrable: there is $\delta_{1}> 0$ such that $\mu\left(E\right)< \delta_{1}\Rightarrow\left|\int_{E}f\,\mathrm{d}\mu\right|< \frac{\varepsilon}{2}$. Also the finite set $\left\{f_{1},\dots,f_{N-1}\right\}$ is uniformly integrable by (a): there is $\delta_{2}> 0$ such that $\mu\left(E\right)< \delta_{2}\Rightarrow\left|\int_{E}f_{n}\,\mathrm{d}\mu\right|< \varepsilon$ for $n< N$. Take $\delta=\min\left\{\delta_{1},\delta_{2}\right\}$. When $\mu\left(E\right)< \delta$, for $n\ge N$,

$$
\left|\int_{E}f_{n}\,\mathrm{d}\mu\right|\le\left|\int_{E}f\,\mathrm{d}\mu\right|+\int_{E}\left|f_{n}-f\right|\mathrm{d}\mu\le\frac{\varepsilon}{2}+\int\left|f_{n}-f\right|\mathrm{d}\mu< \frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon,
$$

and for $n< N$ also $\left|\int_{E}f_{n}\,\mathrm{d}\mu\right|< \varepsilon$. Thus $\left\{f_{n}\right\}$ is uniformly integrable. $\blacksquare$

---

## 7

For $j=1,2$, let $\mu_{j},\nu_{j}$ be $\sigma$-finite measures on $\left(X_{j},\mathcal M_{j}\right)$ with $\nu_{j}\ll\mu_{j}$. Then $\nu_{1}\times\nu_{2}\ll\mu_{1}\times\mu_{2}$, and

$$
\frac{\mathrm{d}\left(\nu_{1}\times\nu_{2}\right)}{\mathrm{d}\left(\mu_{1}\times\mu_{2}\right)}\left(x_{1},x_{2}\right)=\frac{\mathrm{d}\nu_{1}}{\mathrm{d}\mu_{1}}\left(x_{1}\right)\cdot\frac{\mathrm{d}\nu_{2}}{\mathrm{d}\mu_{2}}\left(x_{2}\right).
$$

### Solution 7

Since $\nu_{j}\ll\mu_{j}$ and $\mu_{j}$ is a $\sigma$-finite positive measure, by **Theorem 11.5.5 (Radon-Nikodym Theorem)** there is an $\mathcal M_{j}$-measurable $f_{j}=\frac{\mathrm{d}\nu_{j}}{\mathrm{d}\mu_{j}}\ge0$ with $\nu_{j}\left(E\right)=\int_{E}f_{j}\,\mathrm{d}\mu_{j}$ for every $E\in\mathcal M_{j}$. Define $F:X_{1}\times X_{2}\to\left[0,\infty\right]$ by $F\left(x_{1},x_{2}\right)=f_{1}\left(x_{1}\right)f_{2}\left(x_{2}\right)$; then $F$ is $\mathcal M_{1}\otimes\mathcal M_{2}$-measurable. For a measurable rectangle $A\times B\in\mathcal M_{1}\otimes\mathcal M_{2}$, by **Theorem 10.2.2 (Tonelli's Theorem)**,

$$
\int_{A\times B}F\,\mathrm{d}\left(\mu_{1}\times\mu_{2}\right)=\left(\int_{A}f_{1}\,\mathrm{d}\mu_{1}\right)\left(\int_{B}f_{2}\,\mathrm{d}\mu_{2}\right)=\nu_{1}\left(A\right)\nu_{2}\left(B\right)=\left(\nu_{1}\times\nu_{2}\right)\left(A\times B\right).
$$

By uniqueness of the product measure (agreeing on the generating rectangle family), for every $E\in\mathcal M_{1}\otimes\mathcal M_{2}$, $\left(\nu_{1}\times\nu_{2}\right)\left(E\right)=\int_{E}F\,\mathrm{d}\left(\mu_{1}\times\mu_{2}\right)$. This implies $\nu_{1}\times\nu_{2}\ll\mu_{1}\times\mu_{2}$ (**Definition 11.5.1 (Absolute Continuity)**: if $\left(\mu_{1}\times\mu_{2}\right)\left(E\right)=0$, the right side is $0$). Also $\nu_{1}\times\nu_{2}$ is $\sigma$-finite (since $\nu_{j}$ is $\sigma$-finite); by the uniqueness in **Theorem 11.5.5 (Radon-Nikodym Theorem)**, $F$ is the Radon-Nikodym derivative of $\nu_{1}\times\nu_{2}$ w.r.t. $\mu_{1}\times\mu_{2}$, i.e.

$$
\frac{\mathrm{d}\left(\nu_{1}\times\nu_{2}\right)}{\mathrm{d}\left(\mu_{1}\times\mu_{2}\right)}\left(x_{1},x_{2}\right)=\frac{\mathrm{d}\nu_{1}}{\mathrm{d}\mu_{1}}\left(x_{1}\right)\cdot\frac{\mathrm{d}\nu_{2}}{\mathrm{d}\mu_{2}}\left(x_{2}\right).
$$

$\blacksquare$

---

## 8

Let $\mu,\nu$ be measures on $\left(X,\mathcal M\right)$ with $\nu\ll\mu$, and set $\lambda=\mu+\nu$. If $f=\frac{\mathrm{d}\nu}{\mathrm{d}\lambda}$, then $0\le f< 1$ $\mu$-a.e., and $\frac{\mathrm{d}\nu}{\mathrm{d}\mu}=\frac{f}{1-f}$.

### Solution 8

Since $\lambda=\mu+\nu\ge\mu$ and $\nu\ll\mu$, we have $\nu\ll\lambda$ (if $\lambda\left(E\right)=0$, then $\mu\left(E\right)=0$, hence $\nu\left(E\right)=0$), so $f=\frac{\mathrm{d}\nu}{\mathrm{d}\lambda}$ exists and $f\ge0$ $\lambda$-a.e. (**Theorem 11.5.5 (Radon-Nikodym Theorem)**).

First show $f< 1$ $\mu$-a.e. Suppose otherwise that $\mu\left(\left\{f\ge1\right\}\right)> 0$. Since $\nu\left(\left\{f\ge1\right\}\right)=\int_{\left\{f\ge1\right\}}f\,\mathrm{d}\lambda\ge\lambda\left(\left\{f\ge1\right\}\right)$, and $\lambda=\mu+\nu$, we get $\nu\left(\left\{f\ge1\right\}\right)\ge\lambda\left(\left\{f\ge1\right\}\right)=\mu\left(\left\{f\ge1\right\}\right)+\nu\left(\left\{f\ge1\right\}\right)$, implying $\mu\left(\left\{f\ge1\right\}\right)\le0$, a contradiction. Hence $0\le f< 1$ $\mu$-a.e.

Finally show $\frac{\mathrm{d}\nu}{\mathrm{d}\mu}=\frac{f}{1-f}$. For any $E\in\mathcal M$, by $\lambda=\mu+\nu$ and $f=\frac{\mathrm{d}\nu}{\mathrm{d}\lambda}$,

$$
\nu\left(E\right)=\int_{E}f\,\mathrm{d}\lambda=\int_{E}f\,\mathrm{d}\mu+\int_{E}f\,\mathrm{d}\nu,
$$

i.e. $\int_{E}\left(1-f\right)\mathrm{d}\nu=\int_{E}f\,\mathrm{d}\mu$. Since $1-f> 0$ $\mu$-a.e. (also $\lambda$-a.e.), by the uniqueness in **Theorem 11.5.5 (Radon-Nikodym Theorem)**, $\frac{\mathrm{d}\nu}{\mathrm{d}\mu}=\frac{f}{1-f}$. $\blacksquare$

---

## 9

Let $\left(X,\mathcal M,\mu\right)$ be a $\sigma$-finite measure space, $\mathcal N$ a sub-$\sigma$-algebra of $\mathcal M$, and $\nu=\mu|_{\mathcal N}$. If $f\in L^{1}\left(\mu\right)$, then there exists $g\in L^{1}\left(\nu\right)$ (hence $g$ is $\mathcal N$-measurable) such that $\int_{E}f\,\mathrm{d}\mu=\int_{E}g\,\mathrm{d}\nu$ for every $E\in\mathcal N$; and if $g'$ is another such function, then $g=g'$ $\nu$-a.e.

### Solution 9

For $E\in\mathcal N$, define $\nu_{0}\left(E\right):=\int_{E}f\,\mathrm{d}\mu$. Then $\nu_{0}$ is a signed measure on $\mathcal N$: finite and countable additivity follow from countable additivity of $\mu$ and integrability of $f$ (dominated convergence), and $\left|\nu_{0}\left(E\right)\right|\le\int_{E}\left|f\right|\mathrm{d}\mu\le\int\left|f\right|\mathrm{d}\mu< \infty$, so $\nu_{0}$ is finite. Also $\nu_{0}\ll\nu$ (**Definition 11.5.1 (Absolute Continuity)**): if $E\in\mathcal N$ and $\nu\left(E\right)=\mu\left(E\right)=0$, then $\nu_{0}\left(E\right)=\int_{E}f\,\mathrm{d}\mu=0$ ($f\in L^{1}\left(\mu\right)$, and the integral over a null set is $0$). Since $\nu=\mu|_{\mathcal N}$ is $\sigma$-finite (as $\mu$ is $\sigma$-finite), by **Theorem 11.5.5 (Radon-Nikodym Theorem)** there is an $\mathcal N$-measurable $g=\frac{\mathrm{d}\nu_{0}}{\mathrm{d}\nu}\in L^{1}\left(\nu\right)$ such that $\int_{E}f\,\mathrm{d}\mu=\nu_{0}\left(E\right)=\int_{E}g\,\mathrm{d}\nu$ for every $E\in\mathcal N$.

If $g'\in L^{1}\left(\nu\right)$ also satisfies the same identity, then $\int_{E}\left(g-g'\right)\mathrm{d}\nu=0$ for every $E\in\mathcal N$. Taking $E=\left\{g> g'\right\}\in\mathcal N$, since $g-g'\in L^{1}\left(\nu\right)$ and $\int_{\left\{g> g'\right\}}\left(g-g'\right)\mathrm{d}\nu=0$, by the fact that a nonnegative function with zero integral vanishes a.e., we get $g=g'$ $\nu$-a.e. on $\left\{g> g'\right\}$; similarly on $\left\{g< g'\right\}$. Hence $g=g'$ $\nu$-a.e. $\blacksquare$
