# Exponential Series

**Summary**: §115–§117 of Chapter 7. From the Chapter-6 [[exponential-function]] $a^z$ Euler derives the power series

$$a^z = 1 + \frac{kz}{1} + \frac{k^2 z^2}{1\cdot 2} + \frac{k^3 z^3}{1\cdot 2 \cdot 3} + \cdots,$$

where the constant $k$ depends on the base $a$ via $a^\omega = 1 + k\omega$ for infinitely small $\omega$. Setting $z = 1$ gives the relation $a = \sum k^n/n!$ between $a$ and $k$. Choosing the base so $k = 1$ produces $e^z = \sum z^n/n!$ — see [[eulers-number]]. The general $b^z$ follows by substituting $b = a^{\log b}$ and reads $b^z = \sum (kz \log b)^n/n!$ (§117).

**Sources**: chapter7.pdf (§115–§117)

**Last updated**: 2026-04-26

---

## Setup: $a^\omega = 1 + k\omega$

Fix a base $a > 1$. For an infinitely small positive $\omega$, the value $a^\omega$ exceeds 1 by an infinitely small amount, written $a^\omega = 1 + k\omega$ with $k$ a finite, base-dependent constant (source: chapter7.pdf, §114). For $a = 10$ Euler computes $k \approx 2.30258$; in modern notation $k = \log_e a$ — see [[natural-logarithm]]. See [[infinitesimal-and-infinite-numbers]] for the status of $\omega$ and the next section's $j$.

## Derivation (§115–§116)

Raise $a^\omega = 1 + k\omega$ to a power $j$:

$$a^{j\omega} = (1 + k\omega)^j.$$

Expand the right side by the binomial theorem ([[binomial-series]]):

$$a^{j\omega} = 1 + \frac{j}{1} k\omega + \frac{j(j-1)}{1 \cdot 2} k^2 \omega^2 + \frac{j(j-1)(j-2)}{1 \cdot 2 \cdot 3} k^3 \omega^3 + \cdots$$

Now let $j = z/\omega$. Then $\omega = z/j$, and substituting:

$$a^z = \left(1 + \frac{kz}{j}\right)^j = 1 + \frac{1}{1}kz + \frac{1(j-1)}{1\cdot 2 j} k^2 z^2 + \frac{1(j-1)(j-2)}{1\cdot 2 j\cdot 3 j} k^3 z^3 + \cdots$$

Since $j$ is infinitely large, $(j - m)/(nj) = 1/n$ for every finite $m, n$ — see [[infinitesimal-and-infinite-numbers]] — and each coefficient collapses:

$$\boxed{\;a^z = 1 + \frac{kz}{1} + \frac{k^2 z^2}{1 \cdot 2} + \frac{k^3 z^3}{1\cdot 2\cdot 3} + \frac{k^4 z^4}{1\cdot 2\cdot 3\cdot 4} + \cdots\;}$$

This is the *exponential series* (source: chapter7.pdf, §116).

## The defining relation between $a$ and $k$

Setting $z = 1$ in the boxed series:

$$a = 1 + \frac{k}{1} + \frac{k^2}{1\cdot 2} + \frac{k^3}{1\cdot 2\cdot 3} + \frac{k^4}{1\cdot 2\cdot 3\cdot 4} + \cdots$$

This is the implicit equation that links $a$ and $k$. For $a = 10$, the series in $k$ must equal 10, recovering $k \approx 2.30258$ from §114 (source: chapter7.pdf, §116). For $k = 1$, the sum is $1 + 1 + 1/2 + 1/6 + 1/24 + \cdots = 2.71828\ldots = e$ — see [[eulers-number]].

## The general exponential $b^z$ (§117)

Suppose $b = a^n$, so $\log_a b = n$. Then $b^z = a^{nz}$, and substituting $nz$ for $z$ in the boxed series:

$$b^z = 1 + \frac{knz}{1} + \frac{k^2 n^2 z^2}{1 \cdot 2} + \frac{k^3 n^3 z^3}{1\cdot 2\cdot 3} + \cdots$$

Now $n = \log b$ (in base $a$), giving Euler's general form:

$$b^z = 1 + \frac{kz \log b}{1} + \frac{k^2 z^2 (\log b)^2}{1\cdot 2} + \frac{k^3 z^3 (\log b)^3}{1\cdot 2 \cdot 3} + \cdots$$

(source: chapter7.pdf, §117). One $k$ — the constant of the chosen base $a$ — and one $\log b$ (in that base) suffice to compute $b^z$ for *every* $b$.

When the chosen base is $e$ (so $k = 1$), $\log = \log_e$ and the formula reduces to $b^z = \sum (z \log b)^n / n!$, which is just $e^{z \log b}$. This is the modern $b^z = e^{z \ln b}$.

## Worked specializations

| Substitute | Series for | Result |
|:--|:--|:--|
| $k = 1$ (so $a = e$) | $e^z$ | $\sum_{n \ge 0} z^n/n!$ |
| $k = 1$, $z = 1$ | $e$ | $\sum_{n \ge 0} 1/n!$ |
| $k = \log 10 \approx 2.30258$, $a = 10$ | $10^z$ | $\sum_n (kz)^n/n!$ |
| $k = 1$, base $e$, $b$ arbitrary | $b^z = e^{z \log b}$ | $\sum_n (z \log b)^n/n!$ |

## Why the series converges

Euler does not state convergence as a theorem in this chapter, but one can read off two structural reasons it works:

- The coefficient of $z^n$ is $k^n/n!$, and $n!$ grows faster than any geometric, so the series converges for *every* $z$ — uniformly on compacts in modern terms.
- The series agrees with $a^z$ at $z = 0$ (both equal 1) and is the formal expansion forced by the algebraic identity $a^z = (1 + kz/j)^j$ as $j$ becomes infinite. Whatever subtleties are lurking, the result must equal $a^z$ on whatever domain the manipulation is valid.

In Chapter 8 Euler will use this series with imaginary $z$ to derive the trigonometric series, and the unbounded convergence radius is exactly what licenses that step.

## Status of the derivation

The derivation rests on the [[infinitesimal-and-infinite-numbers|infinitesimal/infinite identification]]: $j = z/\omega$ is treated as both infinite and as a definite quantity in the binomial coefficients, and $(j - m)/(nj) = 1/n$ is treated as an algebraic identity rather than a limit. Modern analysis recovers the same series via $\lim_{n \to \infty}(1 + z/n)^n = e^z$ and termwise comparison; Euler's argument is the formal antecedent of that limit.

## Related pages

- [[exponential-function]]
- [[logarithmic-series]]
- [[eulers-number]]
- [[natural-logarithm]]
- [[infinitesimal-and-infinite-numbers]]
- [[binomial-series]]
- [[chapter-7-on-exponentials-and-logarithms-expressed-through-series]]
- [[chapter-6-on-exponentials-and-logarithms]]
