# Assignment 10

> **Definition 11.4.1** (Mutual Singularity)<br>Let $\mu$ and $\nu$ be two signed measures on a measurable space $\left(X,\mathcal F\right)$. If there exists a measurable set $E\in\mathcal F$ such that $E$ is a $\mu$-null set and $E^{c}$ is a $\nu$-null set, then $\mu$ and $\nu$ are called mutually singular, denoted $\mu\perp\nu$.

> **Basic Knowledge** (Hardy–Littlewood Maximal Function)<br>Let $f\in L^{1}_{\mathrm{loc}}\left(\mathbb R^{n}\right)$. The Hardy–Littlewood maximal function of $f$ is defined by $$Mf\left(x\right)=\sup_{r> 0}\frac{1}{\left|B\left(x,r\right)\right|}\int_{B\left(x,r\right)}\left|f\left(y\right)\right|\mathrm{d}y,$$ where $B\left(x,r\right)$ is the open ball centered at $x$ with radius $r$, and $\left|B\left(x,r\right)\right|$ denotes its Lebesgue measure.

> **Basic Knowledge** (Ball-Volume Formula)<br>Let $C_{n}=m\left(B\left(1,0\right)\right)$ be the Lebesgue measure of the unit ball. Then for any $x\in\mathbb R^{n}$, $r> 0$,<br>$$m\left(B\left(x,r\right)\right)=C_{n}r^{n}.$$

> **Basic Knowledge** (Regular Borel Measure)<br>Let $\nu$ be a Borel measure on $\mathbb R^{n}$. $\nu$ is called **regular** if:
> (1) for every compact set $K$, $\nu\left(K\right)< \infty$;
> 
> (2) for every $E\in\mathcal B\left(\mathbb R^{n}\right)$, $\nu\left(E\right)=\inf\left\{\nu\left(U\right):U\text{开集},E\subset U\right\}$.

### Problem 1

**22.** Let $f\in L^{1}\left(\mathbb R^{n}\right)$ and $f\ne0$. Prove that there exist $C,R> 0$ such that $Hf\left(x\right)\ge C\left|x\right|^{-n}$ for $\left|x\right|> R$. Consequently, when $\lambda$ is sufficiently small, $m\left(\left\{x:Hf\left(x\right)> \lambda\right\}\right)\ge C'\lambda^{-1}$, so the estimate in the maximal theorem is essentially sharp.

**23.** A useful variant of the Hardy–Littlewood maximal function is

$$
H^{*}f\left(x\right)=\sup\left\{\frac{1}{m\left(B\right)}\int_{B}\left|f\left(y\right)\right|\mathrm{d}y:B\text{是球},x\in B\right\}.
$$

Prove that $Hf\le H^{*}f\le2^{n}Hf$.

**26.** If $\lambda$ and $\mu$ are positive, mutually singular Borel measures on $\mathbb R^{n}$, and $\lambda+\mu$ is regular, then both $\lambda$ and $\mu$ are regular.

### Solution to Problem 1

#### 22

Let $Hf$ denote the Hardy–Littlewood maximal function (Basic Knowledge). Since $f\ne0$ and $f\in L^{1}\left(\mathbb R^{n}\right)$, there exists a ball $K$ (just take some compact set) such that

$$
\int_{K}\left|f\right|\mathrm{d}y> 0;
$$

otherwise $\left|\int_{K}f\right|$ would all be zero, which would imply $f=0$ almost everywhere, a contradiction. Set $c=\int_{K}\left|f\right|\mathrm{d}y> 0$, and take $R> 0$ such that $K\subset B\left(0,R\right)$ (i.e. $\sup_{y\in K}\left|y\right|< R$). For $\left|x\right|> R$, since $K\subset B\left(0,R\right)$ and $R< \left|x\right|$, we have $K\subset B\left(x,2\left|x\right|\right)$. Hence, by the definition of the maximal function and the **Basic Knowledge** (ball-volume formula),

$$
Hf\left(x\right)\ge\frac{1}{\left|B\left(x,2\left|x\right|\right)\right|}\int_{B\left(x,2\left|x\right|\right)}\left|f\right|\mathrm{d}y\ge\frac{1}{\left|B\left(x,2\left|x\right|\right)\right|}\int_{K}\left|f\right|\mathrm{d}y=\frac{c}{C_{n}\left(2\left|x\right|\right)^{n}}=\frac{c}{2^{n}C_{n}}\left|x\right|^{-n}.
$$

Taking $C=\frac{c}{2^{n}C_{n}}> 0$, we obtain $Hf\left(x\right)\ge C\left|x\right|^{-n}$ for $\left|x\right|> R$.

Second part: by the first part, when $0< \lambda< C/R^{n}$, $\left(C/\lambda\right)^{1/n}> R$, so

$$
\left\{x:\left|x\right|> \left(C/\lambda\right)^{1/n}\right\}\subset\left\{x:Hf\left(x\right)> \lambda\right\}.
$$

By the ball-volume formula, the measure of this set is

$$
m\left(\left\{x:\left|x\right|< \left(C/\lambda\right)^{1/n}\right\}\right)=C_{n}\left(\frac{C}{\lambda}\right)^{1/n\cdot n}=\frac{C_{n}C}{\lambda}.
$$

Setting $C'=C_{n}C$, we get $m\left(\left\{x:Hf\left(x\right)> \lambda\right\}\right)\ge C'\lambda^{-1}$ for sufficiently small $\lambda> 0$. $\blacksquare$

#### 23

We first prove $Hf\le H^{*}f$. For any $r> 0$, the ball $B\left(x,r\right)$ is a ball containing $x$, so

$$
\frac{1}{\left|B\left(x,r\right)\right|}\int_{B\left(x,r\right)}\left|f\right|\mathrm{d}y\le H^{*}f\left(x\right).
$$

Taking the supremum over $r> 0$ gives $Hf\left(x\right)\le H^{*}f\left(x\right)$.

We next prove $H^{*}f\le2^{n}Hf$. Let $B$ be any ball containing $x$, with radius $\rho$ and center $c$. Since $x\in B$, we have $\left|x-c\right|\le\rho$, so for any $y\in B$,

$$
\left|y-x\right|\le\left|y-c\right|+\left|c-x\right|\le\rho+\rho=2\rho,
$$

i.e. $B\subset B\left(x,2\rho\right)$. By the ball-volume formula, $\left|B\left(x,2\rho\right)\right|=C_{n}\left(2\rho\right)^{n}=2^{n}C_{n}\rho^{n}=2^{n}\left|B\right|$. Hence

$$
\frac{1}{m\left(B\right)}\int_{B}\left|f\right|\mathrm{d}y\le\frac{1}{m\left(B\right)}\int_{B\left(x,2\rho\right)}\left|f\right|\mathrm{d}y=\frac{m\left(B\left(x,2\rho\right)\right)}{m\left(B\right)}\cdot\frac{1}{m\left(B\left(x,2\rho\right)\right)}\int_{B\left(x,2\rho\right)}\left|f\right|\mathrm{d}y=2^{n}\cdot\frac{1}{m\left(B\left(x,2\rho\right)\right)}\int_{B\left(x,2\rho\right)}\left|f\right|\mathrm{d}y;\le2^{n}Hf\left(x\right).
$$

Taking the supremum over all balls $B$ containing $x$, we get $H^{*}f\left(x\right)\le2^{n}Hf\left(x\right)$. Combining, $Hf\le H^{*}f\le2^{n}Hf$. $\blacksquare$

#### 26

Let $\nu=\lambda+\mu$. Since $\lambda\perp\mu$ (**Definition 11.4.1**), there exists a Borel set $A$ such that $\mu\left(A\right)=0$ and $\lambda\left(A^{c}\right)=0$.

**Condition (1) of regularity.** For any compact set $K$, since $\lambda,\mu\ge0$ and $\nu$ is regular (Basic Knowledge), $\lambda\left(K\right)\le\nu\left(K\right)< \infty$, and similarly $\mu\left(K\right)< \infty$.

**Condition (2) of regularity for $\lambda$.** First note that for any $E\in\mathcal B\left(\mathbb R^{n}\right)$,

$$
\lambda\left(E\right)=\lambda\left(E\cap A\right)=\nu\left(E\cap A\right),
$$

where the second equality uses $\mu\left(E\cap A\right)\le\mu\left(A\right)=0$; similarly, $\mu\left(E\right)=\nu\left(E\cap A^{c}\right)$.

For any open set $U\supset E$, $U\cap A\supset E\cap A$, so $\lambda\left(U\right)=\nu\left(U\cap A\right)\ge\nu\left(E\cap A\right)=\lambda\left(E\right)$; hence

$$
\inf\left\{\lambda\left(U\right):U\text{开},U\supset E\right\}\ge\lambda\left(E\right).
$$

Reverse inequality: given $\varepsilon> 0$. Since $\nu$ is regular, $\nu|_{A}$ (restricted to $A$) also satisfies regularity conditions (1) and (2): condition (1) is clear; for condition (2), using outer regularity of $\nu|_{A}$, for $E\cap A$ there exists an open set $W\supset E\cap A$ such that $\nu\left(W\cap A\right)< \nu\left(E\cap A\right)+\varepsilon=\lambda\left(E\right)+\varepsilon$ (using the regularity of $\nu$, first take an open set $W'\supset E\cap A$ with $\nu\left(W'\right)< \nu\left(E\cap A\right)+\varepsilon$, then set $W=W'$ and note $\nu\left(W'\cap A\right)\le\nu\left(W'\right)$). Also, since $\left(E\cap A^{c}\right)\cap A=\varnothing$ and $\lambda\left(E\cap A^{c}\right)=0$, one may choose a sufficiently thin open neighborhood $V\supset E\cap A^{c}$ such that $\nu\left(V\cap A\right)< \varepsilon$ (for example, take $V=\left\{x:\mathrm{dist}\left(x,E\cap A^{c}\right)< \delta\right\}$ and let $\delta\to0$; then $V\cap A\downarrow\left(E\cap A^{c}\right)\cap A=\varnothing$, and by continuity from above, $\nu\left(V\cap A\right)\to0$). Set $U=W\cup V$; then $U$ is open, $U\supset E$, and

$$
\lambda\left(U\right)=\nu\left(U\cap A\right)\le\nu\left(W\cap A\right)+\nu\left(V\cap A\right)< \lambda\left(E\right)+2\varepsilon.
$$

Hence $\inf\left\{\lambda\left(U\right):U\text{开},U\supset E\right\}\le\lambda\left(E\right)$. Combining, $\lambda\left(E\right)=\inf\left\{\lambda\left(U\right):U\text{开},U\supset E\right\}$.

**Condition (2) of regularity for $\mu$.** Using $\mu\left(E\right)=\nu\left(E\cap A^{c}\right)$ and the regularity of $\nu|_{A^{c}}$, the argument is entirely symmetric, and we get that $\mu$ also satisfies condition (2).

In summary, both $\lambda$ and $\mu$ are regular. $\blacksquare$
