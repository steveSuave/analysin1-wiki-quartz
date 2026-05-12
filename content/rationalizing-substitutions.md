# Rationalizing Substitutions

**Summary**: A catalog of substitutions from §47–§51 that express $y = f(z)$ (containing a radical) as a pair $(z(x), y(x))$ of rational — or at least radical-free — functions of a new variable $x$.

**Sources**: chapter3.pdf

**Last updated**: 2026-04-23

---

## The pattern

Each case starts from a specific form of $y(z)$ involving a radical, and gives a substitution that eliminates the radical by expressing both $z$ and $y$ as functions of a new variable $x$.

## §47 — Simple linear radical

$$y = \sqrt{a + bz}.$$

Let $y = bx$. Then $a + bz = b^2 x^2$, so

$$z = bx^2 - \frac{a}{b}, \qquad y = bx.$$

Both are polynomials in $x$ (source: chapter3.pdf, §47).

## §48 — Rational power of a linear expression

$$y = (a + bz)^{m/n}.$$

Let $y = x^m$, so $(a + bz)^{1/n} = x$, giving

$$z = \frac{x^n - a}{b}, \qquad y = x^m$$

(source: chapter3.pdf, §48). Neither $y$ nor $z$ is expressible without a radical in terms of the other, but both are polynomials in $x$.

## §49 — Rational power of a linear-over-linear

$$y = \left( \frac{a + bz}{f + gz} \right)^{m/n}.$$

Let $y = x^m$, so $\frac{a + bz}{f + gz} = x^n$, giving

$$z = \frac{a - f x^n}{g x^n - b}, \qquad y = x^m$$

(source: chapter3.pdf, §49).

Euler also notes a symmetric generalization: if $\left(\frac{\alpha + \beta y}{\gamma + \delta y}\right)^n = \left(\frac{a + bz}{f + gz}\right)^m$, setting both sides equal to $x^{mn}$ gives $y$ and $z$ as linear-fractional functions of $x^m$ and $x^n$ respectively.

## §50 — Radical of two linear factors

$$y = \sqrt{(a + bz)(c + dz)}.$$

Let $\sqrt{(a + bz)(c + dz)} = (a + bz)x$. Squaring and cancelling $(a + bz)$ gives a linear equation for $z$:

$$z = \frac{c - a x^2}{b x^2 - d}, \qquad y = \frac{(bc - ad)\, x}{b x^2 - d}$$

(source: chapter3.pdf, §50). The celebrated special case $b = 1$, $c = a$, $d = -1$ gives $y = \sqrt{a^2 - z^2}$, the circle. See [[rational-parametrization-of-the-circle]].

Euler remarks: *whenever there are two linear real factors under a radical sign, the radical can be removed by this method.*

## §51 — Radical of a general quadratic

$$y = \sqrt{p + qz + rz^2}.$$

The treatment branches on the signs of $p$ and $r$.

**Case I.** $p = a^2 > 0$. Let $\sqrt{a^2 + bz + cz^2} = a + xz$. Then

$$z = \frac{b - 2ax}{x^2 - c}, \qquad y = \frac{bx - ax^2 - ac}{x^2 - c}.$$

**Case II.** $r = a^2 > 0$. Let $\sqrt{a^2 z^2 + bz + c} = az + x$. Then

$$z = \frac{x^2 - c}{b - 2ax}, \qquad y = \frac{-ac + bx - ax^2}{b - 2ax}.$$

**Case III.** $p, r < 0$. If $q^2 > 4pr$, the quadratic factors into two real linear factors and the problem reduces to §50. Otherwise $p + qz + rz^2$ is always negative and $y$ is imaginary for real $z$.

Euler's worked example: $y = \sqrt{-1 + 3z - z^2} = \sqrt{1 - (1 - z)(2 - z)}$. Let $y = 1 - (1 - z)x$; then

$$z = \frac{2 - 2x + x^2}{1 + x^2}, \qquad y = \frac{1 + x - x^2}{1 + x^2}$$

(source: chapter3.pdf, §51).

## Scope and limits

These are the cases where *algebraic substitution alone* suffices. Euler notes explicitly that "other cases, which are not discussed in this treatise, cannot be reduced to a form without radicals by a substitution without radicals" (source: chapter3.pdf, §51). In modern terms: rational parametrizability is special, and not every algebraic curve admits one. It will later be known that this corresponds to the curve having genus zero.

## Related pages

- [[substitution]]
- [[chapter-3-on-the-transformation-of-functions-by-substitution]]
- [[rational-parametrization-of-the-circle]]
- [[homogeneous-substitution]]
- [[factoring-polynomials]] — Case III of §51 uses the real factorization of a quadratic.
