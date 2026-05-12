# Reducible Polynomial

**Summary**: Two classifications of multivariate polynomials, stated in §94–§95. The *order* of a polynomial is the greatest degree of any single term (relevant to the study of algebraic curves). A polynomial is *reducible* if it is a product of two or more non-irrational factors, *irreducible* otherwise. Every [[homogeneous-function|homogeneous]] bivariate polynomial is reducible; irreducibility is checked by examining divisors.

**Sources**: chapter5.pdf

**Last updated**: 2026-04-23

---

## Order of a polynomial (§94)

The [[order-of-a-polynomial|order]] of a polynomial is the greatest degree of any single term (source: chapter5.pdf, §94). Equivalently: the highest total degree that appears, ignoring which lower-degree terms may or may not be present.

Examples:

- $z^2 + y^2 + z^2 + ay - a^2$ has order 2 (the $z^2, y^2$ terms are degree 2; the $ay$ is degree 1; the $-a^2$ is degree 0).
- $y^4 + yz^3 - ay^2 x + abyz - a^2 y^2 + b^4$ has order 4.

Order is the classification used in the geometry of algebraic curves — a "second-order curve" is a conic, a "third-order curve" is a cubic, and so on. Order differs from degree only when the polynomial is heterogeneous: a [[homogeneous-function|homogeneous]] polynomial has a single degree, which is also its order.

## Reducibility (§95)

A polynomial is *reducible* if it can be written as a product of two or more non-irrational (i.e. polynomial or rational) factors; otherwise *irreducible* (source: chapter5.pdf, §95).

**Example of reducibility.**

$$y^4 - z^4 + 2az^3 - 2byz^2 - a^2 z^2 + 2abzy - b^2 y^2 = (y^2 + z^2 - az + by)(y^2 - z^2 + az - by).$$

**Every homogeneous bivariate polynomial is reducible.** This follows from §91: any homogeneous polynomial of degree $n$ in $y, z$ is a product of $n$ linear factors $\alpha y + \beta z$ (see [[homogeneous-function]]).

**Example of irreducibility.** $y^2 + z^2 - a^2$ has no non-irrational factorization — it is irreducible (source: chapter5.pdf, §95).

Euler's method for deciding reducibility is to "consider divisors" — i.e. test whether the polynomial has a polynomial factor of lower degree. No systematic algorithm is developed here.

## Related pages

- [[homogeneous-function]]
- [[order-of-a-polynomial]]
- [[factoring-polynomials]]
- [[fundamental-theorem-of-algebra]]
- [[chapter-5-on-functions-of-two-or-more-variables]]
