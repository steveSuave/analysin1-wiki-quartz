# Euler's Number $e$

**Summary**: §122 of Chapter 7. The base $a$ is at the analyst's disposal; choose it so the constant $k$ in $a^\omega = 1 + k\omega$ equals 1. Then the [[exponential-series|defining series]] $a = \sum k^n/n!$ collapses to

$$e = 1 + \frac{1}{1} + \frac{1}{1\cdot 2} + \frac{1}{1\cdot 2\cdot 3} + \frac{1}{1\cdot 2\cdot 3\cdot 4} + \cdots = 2.71828\,18284\,59045\,23536\,028\ldots$$

This is the first appearance of the symbol $e$ in mathematical history. The resulting logarithms are called *natural* or *hyperbolic* — see [[natural-logarithm]].

**Sources**: chapter7 (§122)

**Last updated**: 2026-04-26

---

## The defining choice

From [[exponential-series|§116]], every base $a > 1$ comes paired with a constant $k$ via

$$a = 1 + \frac{k}{1} + \frac{k^2}{1\cdot 2} + \frac{k^3}{1\cdot 2\cdot 3} + \frac{k^4}{1\cdot 2\cdot 3\cdot 4} + \cdots$$

For $a = 10$, $k \approx 2.30258$. For $a = 2$, $k$ is some other finite value. Euler observes (source: chapter7, §122) that *we are free to choose the base*, and the simplest analytical choice is the one that makes $k = 1$.

Substituting $k = 1$ in the right side gives

$$a = 1 + \frac{1}{1} + \frac{1}{1\cdot 2} + \frac{1}{1\cdot 2\cdot 3} + \frac{1}{1\cdot 2\cdot 3\cdot 4} + \cdots$$

Summing as decimal fractions:

| $n$ | $1/n!$ | partial sum |
|:--|:--|:--|
| 0 | 1.00000 | 1.00000 |
| 1 | 1.00000 | 2.00000 |
| 2 | 0.50000 | 2.50000 |
| 3 | 0.16667 | 2.66667 |
| 4 | 0.04167 | 2.70833 |
| 5 | 0.00833 | 2.71667 |
| 6 | 0.00139 | 2.71806 |
| ... | ... | ... |

Euler reports the value to twenty-three digits:

$$a = 2.71828\,18284\,59045\,23536\,028\ldots$$

(source: chapter7, §122). He denotes it $e$ — *"for the sake of brevity for this number 2.718281828459... we will use the symbol $e$, which will denote the base for natural or hyperbolic logarithms."*

## Why "natural" or "hyperbolic"

Euler gives only a brief etymology: the logarithms with this base are called *natural* because the resulting series are simplest (the factor $1/k$ in [[logarithmic-series|§119]] disappears, and $\log(1+\omega) = \omega$ for infinitely small $\omega$ — a property unique to base $e$, see [[natural-logarithm|§123]]). They are also called *hyperbolic* "since the quadrature of a hyperbola can be expressed through these logarithms" — referring to the fact that the area under $y = 1/x$ from $1$ to $b$ equals $\log_e b$. The hyperbolic terminology is older; the natural-logarithm terminology survives in modern use.

## Why $k = 1$?

The series for $a^z$ is $\sum (kz)^n/n!$ ([[exponential-series|§116]]). With $k = 1$ this becomes the cleanest possible:

$$e^z = 1 + \frac{z}{1} + \frac{z^2}{1\cdot 2} + \frac{z^3}{1\cdot 2\cdot 3} + \frac{z^4}{1\cdot 2\cdot 3\cdot 4} + \cdots$$

Every other base requires the constant $k = \log_e a$ to appear in every term, and inverse logarithm series similarly carry a $1/k$ in front. Picking $k = 1$ is the analyst's choice for simplicity, not a forced choice. Euler is explicit (§122) that *any* base could be used; $e$ is just the most convenient one.

## Status as a constant

By the time Euler writes down the series $\sum 1/n!$, he has already established that:

- The series converges, since $1/n!$ decays faster than any geometric.
- Its sum is a real number, computable to arbitrary decimal precision.
- It is *not* a rational power of any rational base — by [[transcendence-of-logarithms|§105]] applied in reverse, $e$ would have to be transcendental for $\log_e a$ to be transcendental for "generic" $a$. (Euler does not press this, but the argument is implicit.)

He does not prove $e$ is irrational in §122 — but in [[chapter-18-on-continued-fractions|§381 Example III]] Euler discovers (by running the Euclidean algorithm on the decimal expansion of $(e-1)/2$) that $(e-1)/2 = [0; 1, 6, 10, 14, 18, \ldots]$ has partial quotients in arithmetic progression. The infinite, unbounded simple [[continued-fraction-for-e|continued fraction for $e$]] proves irrationality immediately; Euler asserts the pattern "can be confirmed by infinitesimal calculus" and proved it rigorously in 1737 via the Riccati equation. He does not prove $e$ is transcendental either; that is Hermite (1873).

## Connection to $(1 + 1/n)^n$

§125 returns to the [[infinitesimal-and-infinite-numbers|infinite-power]] form:

$$e^z = \left(1 + \frac{z}{j}\right)^j$$

with $j$ infinitely large. Setting $z = 1$:

$$e = \left(1 + \frac{1}{j}\right)^j.$$

In modern notation $e = \lim_{n \to \infty}(1 + 1/n)^n$ — the standard limit definition. Euler's $\sum 1/n!$ definition and the limit definition are the binomial expansion of one another, related by the same $(j-m)/j = 1$ collapse that produced the [[exponential-series|exponential series]].

## What changes once $e$ is on the table

The whole apparatus of Chapter 7 simplifies once the base is $e$:

| Identity (general $a$) | Identity (base $e$) |
|:--|:--|
| $a^z = \sum (kz)^n/n!$ | $e^z = \sum z^n/n!$ |
| $\log(1+x) = (1/k)\sum (-1)^{n+1} x^n/n$ | $\log(1+x) = \sum (-1)^{n+1} x^n/n$ |
| $\log\frac{1+x}{1-x} = (2/k)\sum x^{2n+1}/(2n+1)$ | $\log\frac{1+x}{1-x} = 2\sum x^{2n+1}/(2n+1)$ |
| $b^z = \sum (kz \log b)^n/n!$ | $b^z = \sum (z \log b)^n/n!$ ($= e^{z \log b}$) |

Every other base $a$ is recovered via the conversion factor $k = \log_e a$ — see [[change-of-base]] and [[natural-logarithm|§124]].

## Related pages

- [[exponential-series]]
- [[logarithmic-series]]
- [[natural-logarithm]]
- [[infinitesimal-and-infinite-numbers]]
- [[exponential-function]]
- [[logarithm]]
- [[change-of-base]]
- [[chapter-7-on-exponentials-and-logarithms-expressed-through-series]]
- [[continued-fraction-for-e]] — the §381 Example III simple-CF expansion with arithmetic-progression quotients
- [[chapter-18-on-continued-fractions]]
