# Geometric Series

**Summary**: The infinite series expansion of $a/(\alpha + \beta z)$, obtained by Euler in §60 by long division or by undetermined coefficients. Its defining property is that the ratio of two successive terms is constant. The geometric series reappears throughout the *Introductio* as a building block — most strikingly in [[chapter-16-on-the-partition-of-numbers|Chapter 16]], where the binary identity $\prod(1+x^{2^k}) = 1/(1-x)$ is the simplest non-trivial infinite product whose expansion is the geometric series.

**Sources**: chapter4.pdf, chapter16.pdf

**Last updated**: 2026-05-11

---

## The series (§60)

For the rational function $y = \dfrac{a}{\alpha + \beta z}$, successive long division of $a$ by $\alpha + \beta z$ produces

$$ \frac{a}{\alpha + \beta z} = \frac{a}{\alpha} - \frac{a \beta z}{\alpha^2} + \frac{a \beta^2 z^2}{\alpha^3} - \frac{a \beta^3 z^3}{\alpha^4} + \frac{a \beta^4 z^4}{\alpha^5} - \cdots $$

The quotient of any two successive terms is $-\beta z / \alpha$, a constant in $z$ — this is what makes the series *geometric* (source: chapter4.pdf, §60). Equivalently, the coefficient of $z^n$ is

$$ \frac{(-1)^n a \beta^n}{\alpha^{n+1}} \;=\; \frac{a}{\alpha}\left(- \frac{\beta}{\alpha}\right)^n. $$

## Derivation by undetermined coefficients (§60)

Set $\dfrac{a}{\alpha + \beta z} = A + Bz + Cz^2 + Dz^3 + \cdots$ and clear the denominator. Matching powers of $z$ in

$$ a = \alpha A + (\alpha B + \beta A) z + (\alpha C + \beta B) z^2 + (\alpha D + \beta C) z^3 + \cdots $$

gives $A = a/\alpha$ and the two-term recurrence $\alpha Q + \beta P = 0$ for any consecutive coefficients $P, Q$. Hence $Q = -\beta P / \alpha$, which reproduces the geometric series and identifies it as the simplest [[recurrent-series]] — the case of a linear denominator. See [[method-of-undetermined-coefficients]].

## Role in the chapter

Every more elaborate recurrent series in Chapter 4 is a direct generalization of this one:

- Quadratic denominator (§61) $\leadsto$ three-term recurrence $\alpha R + \beta Q + \gamma P = 0$.
- Higher-degree denominator (§62–§63) $\leadsto$ longer recurrence. See [[recurrent-series]].
- Denominator a power $(1 - \alpha z)^n$ (§64–§67) $\leadsto$ progressions of higher order. See [[higher-order-arithmetic-progressions]].

The geometric series is also the engine behind the §71 binomial expansion in the special case $m/n = -1$: $(1 + Z)^{-1} = 1 - Z + Z^2 - Z^3 + \cdots$ — the geometric series in disguise. See [[binomial-series]].

## Used in Chapter 16

[[chapter-16-on-the-partition-of-numbers|Chapter 16]] builds the [[partition-generating-functions|partition generating functions]] factor by factor: each $1/(1 - x^k z)$ in the unrestricted product is a geometric series in the variable $x^k z$ (§302), and each $(1 + x^k z)$ in the distinct-parts product is the truncated two-term geometric. The [[binary-representation-theorem|binary identity]] $\prod_{k\geq 0}(1 + x^{2^k}) = 1/(1 - x)$ (§329) gives the geometric series $1 + x + x^2 + \cdots$ as an infinite product — the cleanest possible "every integer once" statement.

## Related pages

- [[recurrent-series]]
- [[method-of-undetermined-coefficients]]
- [[higher-order-arithmetic-progressions]]
- [[binomial-series]]
- [[chapter-4-on-the-development-of-functions-in-infinite-series]]
- [[partition-generating-functions]]
- [[binary-representation-theorem]]
- [[balanced-ternary-representation]]
- [[chapter-16-on-the-partition-of-numbers]]
