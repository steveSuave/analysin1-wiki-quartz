# Periodic Continued Fractions

**Summary**: If the partial denominators of a simple continued fraction repeat with finite period, the continued fraction satisfies a polynomial equation of degree at most $2$ in itself — so its value is a quadratic irrational. Euler works through the single-letter case ($x = (\sqrt{a^2 + 4} - a)/2$, generating $\sqrt 5, \sqrt 2, \sqrt{13}, \sqrt 5, \sqrt{29}, \ldots$ as $a$ runs over $1, 2, 3, 4, \ldots$), the two-letter case (which extends the catalog to *every* square root), and three- and four-letter cases (whose discriminants reduce to the two-letter case).

**Sources**: `chapter18` (§376–§379).

**Last updated**: 2026-05-11

---

## Why periodic CFs give quadratic irrationals (§376)

The key observation is that *dropping leading periods does not change the value* of a periodic continued fraction. If $x$ is purely periodic with period $k$, then $x$ appears as a tail of itself, and the [[convergents-of-a-continued-fraction|three-term recurrence]] turns this self-reference into a polynomial equation in $x$ of degree at most $2$.

Euler's archetypal example: $x = 1/(2 + 1/(2 + 1/(2 + \cdots)))$ satisfies

$$x = \frac{1}{2 + x},\qquad\text{i.e.,}\qquad x^2 + 2x = 1,\qquad\text{so}\qquad x = \sqrt 2 - 1.$$

The convergents $1/0, 0/1, 1/2, 2/5, 5/12, 12/29, 29/70, \ldots$ approximate $\sqrt 2 - 1 = 0.41421356\ldots$ with $29/70 = 0.41428571\ldots$ — error in the hundred-thousandths place after only six terms.

## Single-letter period (§377)

For arbitrary $a \in \mathbb{Z}_{>0}$, $\;x = 1/(a + x)\;$ gives $\;x^2 + ax = 1$, so

$$x = \frac{\sqrt{a^2 + 4} - a}{2}.$$

Running through $a = 1, 2, 3, 4, \ldots$:

| $a$ | partial quotients | $x$ | $\sqrt{a^2 + 4}$ |
|---|---|---|---|
| $1$ | $1, 1, 1, 1, \ldots$ | $\tfrac{\sqrt 5 - 1}{2}$ | $\sqrt 5$ |
| $2$ | $2, 2, 2, 2, \ldots$ | $\sqrt 2 - 1$ | $\sqrt 8 = 2\sqrt 2$ |
| $3$ | $3, 3, 3, 3, \ldots$ | $\tfrac{\sqrt{13} - 3}{2}$ | $\sqrt{13}$ |
| $4$ | $4, 4, 4, 4, \ldots$ | $\sqrt 5 - 2$ | $\sqrt{20} = 2\sqrt 5$ |
| $5$ | $5, 5, 5, 5, \ldots$ | $\tfrac{\sqrt{29} - 5}{2}$ | $\sqrt{29}$ |

Convergence accelerates as $a$ grows: for $a = 4$ the sixth convergent $305/1292$ approximates $\sqrt 5 - 2$ with error $< 1/(1292\cdot 5473)$.

This method handles exactly the square roots of $a^2 + 4$ — i.e., numbers that are the sum of two squares.

## Two-letter period (§378)

To extend the method to *all* square roots Euler considers $x = 1/(a + 1/(b + x))$, which gives $ax^2 + abx = b$ and

$$x = \frac{-ab + \sqrt{a^2 b^2 + 4ab}}{2a}.$$

Choosing $a = 2, b = 7$: $x = (-7 + 3\sqrt 7)/2$, and the convergent sequence $1/2, 7/15, 15/32, 112/239, 239/510, \ldots$ gives $\sqrt 7 \approx 2024/765 = 2.6457516$ versus the true $\sqrt 7 = 2.64575131\ldots$, error $< 3/10^7$. (Euler's $\sqrt 7$ approximation.)

## Three- and four-letter periods (§379)

A three-letter period gives a quadratic with discriminant $(abc + a + b + c)^2 + 4$, which Euler observes is *again a sum of two squares* — so it does not produce square roots inaccessible to the two-letter method. The same goes for four-letter periods. So purely periodic CFs with periods $\geq 2$ do not enlarge the class of irrationals reachable, only re-parametrise it.

## Modern statement (Lagrange's theorem)

The collection of theorems §376–§379 together establish one direction of what is now called **Lagrange's theorem on periodic continued fractions** (1770): *a real number has a periodic simple continued fraction expansion if and only if it is a quadratic irrational*. The converse direction — every quadratic irrational has a periodic CF — was not stated by Euler in the *Introductio*, but the §381 Euclidean-algorithm method gives a procedure for computing the CF expansion of any real number, and applied to $\sqrt 2$ in §381 Example II it recovers the $2, 2, 2, \ldots$ pattern of §376.

## Related pages

- [[continued-fraction]]
- [[convergents-of-a-continued-fraction]]
- [[euclidean-algorithm-continued-fraction]] — §381 Example II verifies $\sqrt 2 = [1; 2, 2, 2, \ldots]$ by running the algorithm on a decimal
- [[best-rational-approximations]] — periodic CFs give fast best-approximations to quadratic irrationals
- [[chapter-18-on-continued-fractions]]
