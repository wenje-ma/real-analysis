# week9

> **Theorem 8.2.9 (Dominated Convergence Theorem)**
> 
> Let $\left(X,\mathcal F,\mu\right)$ be a measure space and $\left\{f_{n}\right\}$ a sequence of measurable functions. If there exists an integrable $g$ with $\left|f_{n}\right|\le g$ for all $n$ and $f_{n}\to f$ a.e., then $f$ is integrable and $\int f\,\mathrm{d}\mu=\lim_{n\to\infty}\int f_{n}\,\mathrm{d}\mu$.

> **Theorem 8.2.16 (Integrable Simple Functions Are Dense in $L^{1}$)**
> 
> If $f\in L^{1}\left(\mu\right)$ and $\varepsilon> 0$, then there exists an integrable simple function $\varphi=\sum a_{j}\chi_{E_{j}}$ with $\int\left|f-\varphi\right|\mathrm{d}\mu< \varepsilon$.

> **Theorem 10.2.1 (Fubini's Theorem)**
> 
> Let $\left(X,\mathcal A,\mu\right)$ and $\left(Y,\mathcal B,\nu\right)$ be $\sigma$-finite measure spaces and $f:X\times Y\to\mathbb R$ be $\mathcal A\otimes\mathcal B$-measurable. If $f$ is integrable on $X\times Y$, then for almost every $x$, $y\mapsto f\left(x,y\right)$ is $\nu$-integrable; for almost every $y$, $x\mapsto f\left(x,y\right)$ is $\mu$-integrable; and the iterated integrals agree:

> **Theorem 10.2.2 (Tonelli's Theorem)**
> 
> If $f:X\times Y\to\left[0,\infty\right]$ is $\mathcal A\otimes\mathcal B$-measurable, then

> **Theorem 11.1.1 (Regularity of Lebesgue Measure and Rectangle Approximation)**
> 
> Let $E\in\mathcal L^{n}$. (a)

> **Theorem 11.4.1 (Integration in Polar Coordinates)**
> 
> There is a unique Borel measure $\sigma=\sigma_{n-1}$ on $S^{n-1}$ such that $m^{*}=\rho\times\sigma$. If $f$ is Borel measurable on $\mathbb R^{n}$ and either $f\ge0$ or $f\in L^{1}\left(m\right)$, then

## 1

If $f$ is Lebesgue integrable on $\left(0,a\right)$ and $g\left(x\right)=\int_{x}^{a}t^{-1}f\left(t\right)\mathrm{d}t$, then $g$ is integrable on $\left(0,a\right)$ and $\int_{0}^{a}g\left(x\right)\mathrm{d}x=\int_{0}^{a}f\left(x\right)\mathrm{d}x$.

### Solution to 1

Consider on $\left(0,a\right)\times\left(0,a\right)$ the function $h\left(x,t\right)=t^{-1}f\left(t\right)\chi_{\left\{x< t\right\}}\left(x,t\right)$ (domain $\left\{\left(x,t\right):0< x< t< a\right\}$). By **Theorem 10.2.2 (Tonelli's Theorem)** applied to the nonnegative $\left|h\right|$,

$$
\int_{0}^{a}\int_{x}^{a}t^{-1}\left|f\left(t\right)\right|\mathrm{d}t\,\mathrm{d}x=\int_{0}^{a}\left(\int_{0}^{t}t^{-1}\left|f\left(t\right)\right|\mathrm{d}x\right)\mathrm{d}t=\int_{0}^{a}t^{-1}\left|f\left(t\right)\right|\cdot t\,\mathrm{d}t=\int_{0}^{a}\left|f\left(t\right)\right|\mathrm{d}t< \infty,
$$

where the inner exchange uses **Theorem 10.2.2 (Tonelli's Theorem)** on a nonnegative function. Thus $\left(x,t\right)\mapsto t^{-1}f\left(t\right)\chi_{\left\{x< t\right\}}$ is integrable, and hence $g$ is integrable. Then by **Theorem 10.2.1 (Fubini's Theorem)** exchanging the order,

$$
\int_{0}^{a}g\left(x\right)\mathrm{d}x=\int_{0}^{a}\int_{x}^{a}t^{-1}f\left(t\right)\mathrm{d}t\,\mathrm{d}x=\int_{0}^{a}\left(\int_{0}^{t}t^{-1}f\left(t\right)\mathrm{d}x\right)\mathrm{d}t=\int_{0}^{a}t^{-1}f\left(t\right)\cdot t\,\mathrm{d}t=\int_{0}^{a}f\left(t\right)\mathrm{d}t.
$$

$\blacksquare$

## 2

Let $f\left(x\right)=x^{-1}\sin x$.

(a) Prove $\int_{0}^{\infty}\left|f\left(x\right)\right|\mathrm{d}x=\infty$.

(b) Prove $\lim_{b\to\infty}\int_{0}^{b}f\left(x\right)\mathrm{d}x=\frac{1}{2}\pi$, by integrating $e^{-xy}\sin x$ in $x$ and $y$.

### Solution to 2

**(a).** On $\left[k\pi,\left(k+1\right)\pi\right]$, $\int_{k\pi}^{\left(k+1\right)\pi}\left|\sin x\right|\mathrm{d}x=2$. Since $\frac{1}{x}$ on this interval is $\ge\frac{1}{\left(k+1\right)\pi}$, we have $\int_{k\pi}^{\left(k+1\right)\pi}\frac{\left|\sin x\right|}{x}\mathrm{d}x\ge\frac{2}{\left(k+1\right)\pi}$. Thus for any $N$, $\int_{0}^{\left(N+1\right)\pi}\frac{\left|\sin x\right|}{x}\mathrm{d}x\ge\sum_{k=0}^{N}\frac{2}{\left(k+1\right)\pi}\to\infty$ (harmonic series diverges), so $\int_{0}^{\infty}\left|f\right|\mathrm{d}x=\infty$.

**(b).** For fixed $b> 0$, since $\int_{0}^{b}\int_{0}^{\infty}\left|e^{-xy}\sin x\right|\mathrm{d}y\,\mathrm{d}x=\int_{0}^{b}\frac{\left|\sin x\right|}{x}\mathrm{d}x< \infty$ (for fixed $b$, $x^{-1}\sin x$ is integrable), by **Theorem 10.2.2 (Tonelli's Theorem)** we may exchange the order:

$$
\int_{0}^{b}\frac{\sin x}{x}\mathrm{d}x=\int_{0}^{b}\int_{0}^{\infty}e^{-xy}\sin x\,\mathrm{d}y\,\mathrm{d}x=\int_{0}^{\infty}\left(\int_{0}^{b}e^{-xy}\sin x\,\mathrm{d}x\right)\mathrm{d}y.
$$

For fixed $y$, integrating by parts twice gives $\int_{0}^{b}e^{-xy}\sin x\,\mathrm{d}x=\frac{1-e^{-by}\left(y\sin b+\cos b\right)}{1+y^{2}}$. Hence $\int_{0}^{b}\frac{\sin x}{x}\mathrm{d}x=\int_{0}^{\infty}\frac{1-e^{-by}\left(y\sin b+\cos b\right)}{1+y^{2}}\mathrm{d}y$.

**Taking $b\to\infty$.** Split into $\frac{1}{1+y^{2}}-\frac{e^{-by}\left(y\sin b+\cos b\right)}{1+y^{2}}$. The first integrates to $\int_{0}^{\infty}\frac{1}{1+y^{2}}\mathrm{d}y=\frac{\pi}{2}$. For the second, when $b\ge1$, $\left|\frac{e^{-by}\left(y\sin b+\cos b\right)}{1+y^{2}}\right|\le\frac{e^{-y}\left(y+1\right)}{1+y^{2}}=:g\left(y\right)$, and $\int_{0}^{\infty}g\left(y\right)\mathrm{d}y< \infty$ (dominated by the exponential decay $e^{-y}$). By **Theorem 8.2.9 (Dominated Convergence Theorem)** (applied along any sequence $b_{n}\to\infty$), this term tends to $\int_{0}^{\infty}0\,\mathrm{d}y=0$. Hence $\lim_{b\to\infty}\int_{0}^{b}\frac{\sin x}{x}\mathrm{d}x=\frac{\pi}{2}$. $\blacksquare$

## 3

If $f$ is continuous on $\left[0,\infty\right)$, for $\alpha> 0$ and $x\ge0$ set

$$
I_{\alpha}f\left(x\right)=\frac{1}{\Gamma\left(\alpha\right)}\int_{0}^{x}\left(x-t\right)^{\alpha-1}f\left(t\right)\mathrm{d}t,
$$

called the $\alpha$-th order fractional integral of $f$.

(a) $I_{\alpha+\beta}f=I_{\alpha}\left(I_{\beta}f\right)$ for all $\alpha,\beta> 0$.

(b) If $n\in\mathbb N$, $I_{n}f$ is an $n$-th antiderivative of $f$.

### Solution to 3

**(a).** Expand the composite integral and exchange the order over $\left\{\left(s,t\right):0< t< s< x\right\}$:

$$
I_{\alpha}\left(I_{\beta}f\right)\left(x\right)=\frac{1}{\Gamma\left(\alpha\right)}\int_{0}^{x}\left(x-s\right)^{\alpha-1}\left[\frac{1}{\Gamma\left(\beta\right)}\int_{0}^{s}\left(s-t\right)^{\beta-1}f\left(t\right)\mathrm{d}t\right]\mathrm{d}s.
$$

Since $f$ is continuous, the integrand is integrable; by **Theorem 10.2.1 (Fubini's Theorem)**, exchanging the order gives

$$
=\frac{1}{\Gamma\left(\alpha\right)\Gamma\left(\beta\right)}\int_{0}^{x}f\left(t\right)\left[\int_{t}^{x}\left(x-s\right)^{\alpha-1}\left(s-t\right)^{\beta-1}\mathrm{d}s\right]\mathrm{d}t.
$$

For the inner integral, set $u=\frac{s-t}{x-t}$; then $s=t+u\left(x-t\right)$, $\mathrm{d}s=\left(x-t\right)\mathrm{d}u$, giving

$$
\int_{t}^{x}\left(x-s\right)^{\alpha-1}\left(s-t\right)^{\beta-1}\mathrm{d}s=\left(x-t\right)^{\alpha+\beta-1}\int_{0}^{1}\left(1-u\right)^{\alpha-1}u^{\beta-1}\mathrm{d}u.
$$

By Gamma Function and the Beta Identity, $\int_{0}^{1}\left(1-u\right)^{\alpha-1}u^{\beta-1}\mathrm{d}u=\frac{\Gamma\left(\alpha\right)\Gamma\left(\beta\right)}{\Gamma\left(\alpha+\beta\right)}$. Substituting, $I_{\alpha}\left(I_{\beta}f\right)\left(x\right)=\frac{1}{\Gamma\left(\alpha+\beta\right)}\int_{0}^{x}\left(x-t\right)^{\alpha+\beta-1}f\left(t\right)\mathrm{d}t=I_{\alpha+\beta}f\left(x\right)$.

**(b).** For $\alpha=1$, since $\Gamma\left(1\right)=1$, $I_{1}f\left(x\right)=\int_{0}^{x}f\left(t\right)\mathrm{d}t$, and by the fundamental theorem of calculus $\frac{\mathrm{d}}{\mathrm{d}x}I_{1}f=f$. By (a), iterating gives $I_{n}f=\underbrace{I_{1}\circ\cdots\circ I_{1}}_{n\text{ times}}f$, so $\frac{\mathrm{d}^{n}}{\mathrm{d}x^{n}}I_{n}f=f$. Also, since the lower limit of $I_{\alpha}f$ is $0$, for $k< n$, $\left(\frac{\mathrm{d}}{\mathrm{d}x}\right)^{k}I_{n}f$ takes the value $0$ at $0$. Thus $I_{n}f$ is an $n$-th antiderivative of $f$. $\blacksquare$

## 4

The measure $\sigma$ on $S^{n-1}$ is rotation invariant.

### Solution to 4

Let $R\in O\left(n\right)$, i.e. $R^{\top}R=I$, so $\left|\det R\right|=1$. By Orthogonal Transformations Preserve Lebesgue Measure, $R$ preserves $m$ on $\mathbb R^{n}$. Since $R$ preserves the norm $\left|Rx\right|=\left|x\right|$, under the spherical-coordinate decomposition $\Phi\left(x\right)=\left(r,x'\right)$ it acts on the spherical part: there is a rotation $\rho$ of $S^{n-1}$ with $R\left(rx'\right)=r\rho\left(x'\right)$. Let $m^{*}$ be the polar-coordinate measure ($m^{*}=\rho\times\sigma$ by **Theorem 11.4.1 (Integration in Polar Coordinates)**); for a Borel set $A\subset\left(0,\infty\right)\times S^{n-1}$,

$$
m^{*}\left(\left(\mathrm{id}\times\rho\right)\left(A\right)\right)=m\left(\Phi^{-1}\left(\left(\mathrm{id}\times\rho\right)\left(A\right)\right)\right)=m\left(R\Phi^{-1}\left(A\right)\right)=m\left(\Phi^{-1}\left(A\right)\right)=m^{*}\left(A\right),
$$

so $m^{*}$ is rotation invariant.

Define $\sigma_{R}\left(E\right):=\sigma\left(R^{-1}E\right)=\sigma\left(R^{\top}E\right)$, a Borel measure on $S^{n-1}$. On a rectangle $\left(a,b\right]\times E\subset\left(0,\infty\right)\times S^{n-1}$,

$$
\left(\rho\times\sigma_{R}\right)\left(\left(a,b\right]\times E\right)=\int_{a}^{b}r^{n-1}\mathrm{d}r\cdot\sigma_{R}\left(E\right)=\rho\left(\left(a,b\right]\right)\cdot\sigma\left(R^{-1}E\right).
$$

By $m^{*}=\rho\times\sigma$ (**Theorem 11.4.1 (Integration in Polar Coordinates)**), $\rho\left(\left(a,b\right]\right)\cdot\sigma\left(R^{-1}E\right)=m^{*}\left(\left(a,b\right]\times R^{-1}E\right)$. By rotation invariance of $m^{*}$, $m^{*}\left(\left(a,b\right]\times R^{-1}E\right)=m^{*}\left(\left(a,b\right]\times E\right)=\rho\left(\left(a,b\right]\right)\cdot\sigma\left(E\right)$. Hence on rectangles $\rho\times\sigma_{R}=\rho\times\sigma$. By Uniqueness of Measures on a Generating Rectangle Family, $\rho\times\sigma_{R}=\rho\times\sigma$ on $\left(0,\infty\right)\times S^{n-1}$.

Finally, by the uniqueness in **Theorem 11.4.1 (Integration in Polar Coordinates)** (the measure $\sigma$ with $m^{*}=\rho\times\sigma$ is unique), from $\rho\times\sigma_{R}=m^{*}=\rho\times\sigma$ we get $\sigma_{R}=\sigma$, i.e. $\sigma\left(R^{-1}E\right)=\sigma\left(E\right)$ for all Borel $E$. Thus $\sigma$ is rotation invariant. $\blacksquare$

## 5

For which real $a$ and $b$ is $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ integrable on $\left\{x\in\mathbb R^{n}:\left|x\right|< 1/2\right\}$? On $\left\{x\in\mathbb R^{n}:\left|x\right|> 2\right\}$?

### Solution to 5

The function $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ is radial; by **Theorem 11.4.1 (Integration in Polar Coordinates)**,

$$
\int_{\mathbb R^{n}}\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}\mathrm{d}x=\sigma\left(S^{n-1}\right)\int_{0}^{\infty}r^{a+n-1}\left|\log r\right|^{b}\mathrm{d}r.
$$

**Set $\left\{\left|x\right|< 1/2\right\}$.** Substitute $u=-\log r$ (i.e. $r=e^{-u}$, $\mathrm{d}r=-e^{-u}\mathrm{d}u$, so $r\in\left(0,1/2\right]$ corresponds to $u\in\left[\log 2,\infty\right)$):

$$
\int_{0}^{1/2}r^{a+n-1}\left|\log r\right|^{b}\mathrm{d}r=\int_{\log 2}^{\infty}e^{-u\left(a+n-1\right)}e^{-u}u^{b}\mathrm{d}u=\int_{\log 2}^{\infty}e^{-u\left(a+n\right)}u^{b}\mathrm{d}u.
$$

The convergence is determined by the exponential factor:

$$
\int_{\log 2}^{\infty}e^{-u\left(a+n\right)}u^{b}\mathrm{d}u\text{ converges}\iff\begin{cases}a+n> 0,&\text{exponential decay, any }b,\\a+n=0\text{ and }b< -1,&\int u^{b}\mathrm{d}u\text{ converges},\\a+n< 0,&\text{exponential growth, diverges}.\end{cases}
$$

Thus $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ is integrable on $\left\{\left|x\right|< 1/2\right\}$ iff $a> -n$, or $a=-n$ and $b< -1$.

**Set $\left\{\left|x\right|> 2\right\}$.** For $r\ge2$, $\left|\log r\right|=\log r$. Substitute $r=e^{u}$ ($\mathrm{d}r=e^{u}\mathrm{d}u$, $u\ge\log 2$):

$$
\int_{2}^{\infty}r^{a+n-1}\left(\log r\right)^{b}\mathrm{d}r=\int_{\log 2}^{\infty}e^{u\left(a+n-1\right)}e^{u}u^{b}\mathrm{d}u=\int_{\log 2}^{\infty}e^{u\left(a+n\right)}u^{b}\mathrm{d}u.
$$

Convergence: $\int_{\log 2}^{\infty}e^{u\left(a+n\right)}u^{b}\mathrm{d}u\text{ converges}\iff a+n< 0$ (exponential decay; for $a+n> 0$ exponential growth diverges, for $a+n=0$, $\int u^{b}\mathrm{d}u$ diverges for any $b$). Thus $\left|x\right|^{a}\left|\log\left|x\right|\right|^{b}$ is integrable on $\left\{\left|x\right|> 2\right\}$ iff $a< -n$.

**Conclusion.** Integrable on $\left\{\left|x\right|< 1/2\right\}$ iff $a> -n$ or $\left(a=-n\text{ and }b< -1\right)$; integrable on $\left\{\left|x\right|> 2\right\}$ iff $a< -n$. $\blacksquare$
