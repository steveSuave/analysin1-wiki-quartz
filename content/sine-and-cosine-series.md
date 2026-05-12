# Power Series for Sine and Cosine

**Summary**: §134 of Chapter 8. Letting $z$ be infinitely small (so $\sin z = z$, $\cos z = 1$) and $n$ infinitely large with $nz = v$ a finite arc, the [[de-moivre-formula|De Moivre]] expansions of $\cos nz$ and $\sin nz$ collapse — by the same $(j-m)/(nj) = 1/n$ identity used in [[exponential-series|Chapter 7]] — into the canonical power series

$$\cos v = 1 - \frac{v^2}{2!} + \frac{v^4}{4!} - \frac{v^6}{6!} + \cdots,\qquad \sin v = v - \frac{v^3}{3!} + \frac{v^5}{5!} - \frac{v^7}{7!} + \cdots.$$

Euler immediately tabulates $\sin(m\pi/(2n))$ and $\cos(m\pi/(2n))$ as series in $m/n$ with stunning 28-digit numerical coefficients.

**Sources**: chapter8 (§134)

**Last updated**: 2026-04-27

---

## The infinitesimal/infinite move

The §133 De Moivre expansions

$$\cos nz = (\cos z)^n - \binom{n}{2}(\cos z)^{n-2}(\sin z)^2 + \binom{n}{4}(\cos z)^{n-4}(\sin z)^4 - \cdots,$$

$$\sin nz = n(\cos z)^{n-1}\sin z - \binom{n}{3}(\cos z)^{n-3}(\sin z)^3 + \binom{n}{5}(\cos z)^{n-5}(\sin z)^5 - \cdots$$

hold for every positive integer $n$ and every arc $z$. Euler now does the move that defines the *Introductio*: take $z$ to be infinitely small, so

$$\sin z = z,\qquad \cos z = 1,$$

(an infinitesimal-arc identity Euler accepts as obvious) and take $n$ infinitely large, with $nz$ equal to a *finite* arc $v$. Set $z = v/n$.

Under these substitutions:

- $(\cos z)^{n-k} = 1^{n-k} = 1$ for every $k$.
- $(\sin z)^k = z^k = v^k/n^k$.
- The binomial coefficient $\binom{n}{k} = \frac{n(n-1)(n-2)\cdots(n-k+1)}{k!}$ has $k$ factors in the numerator. With $n$ infinite, each factor $(n - j)/n = 1$ for finite $j$, so $n(n-1)\cdots(n-k+1) = n^k$, and $\binom{n}{k}\cdot 1\cdot v^k/n^k = v^k/k!$.

This is the same coefficient-collapse used to derive $e^z = \sum z^n/n!$ in [[exponential-series|§116]] from $(1 + z/j)^j$ with $j$ infinite.

## The cosine series

Substituting into §133's $\cos nz$ expansion:

$$\cos v = 1 - \frac{v^2}{2!} + \frac{v^4}{4!} - \frac{v^6}{6!} + \frac{v^8}{8!} - \cdots.$$

(source: chapter8, §134). The series is alternating because the §133 expansion alternates in sign on $\binom{n}{2k}(\sin z)^{2k}$.

## The sine series

Substituting into §133's $\sin nz$ expansion:

$$\sin v = v - \frac{v^3}{3!} + \frac{v^5}{5!} - \frac{v^7}{7!} + \frac{v^9}{9!} - \cdots.$$

(source: chapter8, §134). Both series have the form $\sum_{k=0}^\infty (-1)^k v^{2k}/(2k)!$ and $\sum_{k=0}^\infty (-1)^k v^{2k+1}/(2k+1)!$. They converge for all real $v$ — and in fact for all complex $v$, though Euler does not press this point.

## Sample numerics: $\sin(m\pi/(2n))$ and $\cos(m\pi/(2n))$

Setting $v = (m/n)(\pi/2)$ — that is, taking $v$ to be the same fraction $m/n$ of the quarter-arc — Euler substitutes $\pi/2 = 1.5707963267948966\ldots$ and writes the resulting numerical series in powers of $m/n$. The first few coefficients (source: chapter8, §134):

$$\sin\frac{m\pi}{2n} = \frac{m}{n}\cdot 1.5707963267948966192313216916 \;-\; \frac{m^3}{n^3}\cdot 0.6459640975062462536557565838 \;+\; \frac{m^5}{n^5}\cdot 0.0796926262461670451205055488 \;-\; \cdots,$$

$$\cos\frac{m\pi}{2n} = 1 \;-\; \frac{m^2}{n^2}\cdot 1.2337005501361698273543113745 \;+\; \frac{m^4}{n^4}\cdot 0.2536695079010480136385833859 \;-\; \cdots.$$

The leading coefficient of $\sin(m\pi/(2n))$ is $\pi/2$ to 28 digits; the second is $(\pi/2)^3/3! = 0.6459640975\ldots$; etc. Euler tabulates 30 coefficients in each series. Since the formulas suffice for all sines and cosines once $m/n < 1/2$ (i.e., arcs up to $\pi/4$ = 45°, the rest reachable by §128 reflections), and since powers of a fraction $< 1/2$ shrink fast, "a few terms should be sufficient, especially if the number of decimal places is not so large" (source: chapter8, §134).

## Tangent and cotangent

§135 reads off the tangent and cotangent series by long division of the §134 series:

$$\tan v = \frac{v - v^3/3! + v^5/5! - \cdots}{1 - v^2/2! + v^4/4! - \cdots},\qquad \cot v = \frac{1 - v^2/2! + v^4/4! - \cdots}{v - v^3/3! + v^5/5! - \cdots}.$$

Euler quotes 25-digit numerical series for $\tan(m\pi/(2n))$ and $\cot(m\pi/(2n))$ but defers the closed-form derivation to §197 of a later chapter. The first numerical formula reads

$$\tan\frac{m\pi}{2n} = \frac{2mn}{n^2 - m^2}\cdot 0.6366197723675 + \frac{m}{n}\cdot 0.2975567820597 + \frac{m^3}{n^3}\cdot 0.0186886502773 + \cdots,$$

with $0.6366\ldots = 2/\pi$.

## Why this derivation, and not Taylor series?

Calculus had not yet provided Taylor's theorem in the form Euler would later use, and even after Taylor (1715) the convention in the *Introductio* was to derive series by algebraic manipulation rather than by differentiation. Euler's argument is purely algebraic:

1. Identity for *every* integer $n$: §133 De Moivre.
2. Pass to the limit by treating $n$ as infinite and $z$ as infinitesimal: collapse the binomial coefficients.
3. Read off the resulting power series.

The same three-step pattern works for $e^z$ (Chapter 7), for $\log(1+x)$ (Chapter 7), for $\sin v$ and $\cos v$ (here), and for $\arctan t$ ([[arctangent-series|§140]]). The *Introductio*'s analytic engine is this single trick repeated.

## Related pages

- [[de-moivre-formula]]
- [[exponential-series]]
- [[infinitesimal-and-infinite-numbers]]
- [[binomial-series]]
- [[sine-and-cosine]]
- [[eulers-formula]]
- [[arctangent-series]]
- [[chapter-8-on-transcendental-quantities-which-arise-from-the-circle]]
- [[chapter-7-on-exponentials-and-logarithms-expressed-through-series]]
