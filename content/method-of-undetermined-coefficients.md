# Method of Undetermined Coefficients

**Summary**: Euler's technique (§60–§61) for expanding a rational function as an infinite series: posit a series $A + Bz + Cz^2 + \cdots$ with unknown coefficients, multiply by the denominator, and match powers of $z$ to determine the coefficients one by one.

**Sources**: chapter4

**Last updated**: 2026-04-23

---

## The method

Given a rational function $\dfrac{N(z)}{D(z)}$ with $D(0) \neq 0$, write

$$ \frac{N(z)}{D(z)} \;=\; A + B z + C z^2 + D z^3 + \cdots $$

with unknown coefficients $A, B, C, \ldots$. Multiply through by $D(z)$ to obtain

$$ N(z) \;=\; D(z) \cdot (A + B z + C z^2 + \cdots). $$

Expanding the right-hand side and collecting powers of $z$ yields an infinite system of linear equations in the unknowns — the coefficients of matching powers on the two sides must be equal. Each equation determines the next coefficient in terms of its predecessors (source: chapter4, §60–§61).

Euler prefers this method to long division because long division is "tedious and there is no easy way to show the nature of the resulting infinite series" (source: chapter4, §61) — the recurrence produced by matching is more informative than the step-by-step quotient.

## Worked examples

### Linear denominator (§60)

For $\dfrac{a}{\alpha + \beta z} = A + B z + C z^2 + \cdots$, multiplication gives $a = (\alpha + \beta z)(A + B z + C z^2 + \cdots)$, i.e.

$$ a = \alpha A + (\alpha B + \beta A) z + (\alpha C + \beta B) z^2 + (\alpha D + \beta C) z^3 + \cdots $$

Matching: $A = a/\alpha$ and $\alpha Q + \beta P = 0$ for any consecutive $P, Q$. This yields the [[geometric-series]].

### Quadratic denominator (§61)

For $\dfrac{a + bz}{\alpha + \beta z + \gamma z^2} = A + B z + C z^2 + \cdots$, the same procedure gives

$$ a + bz = \alpha A + (\alpha B + \beta A) z + (\alpha C + \beta B + \gamma A) z^2 + (\alpha D + \beta C + \gamma B) z^3 + \cdots $$

Matching: $A = a/\alpha$, $B = b/\alpha - a\beta/\alpha^2$, and from the third power onward the three-term recurrence $\alpha R + \beta Q + \gamma P = 0$ (source: chapter4, §61). Hence $R = -(\beta Q + \gamma P)/\alpha$.

### Lucas-number example (§61)

With $a = 1, b = 2, \alpha = 1, \beta = -1, \gamma = -1$: $A = 1, B = 3$, then $R = P + Q$, so

$$ \frac{1 + 2z}{1 - z - z^2} = 1 + 3 z + 4 z^2 + 7 z^3 + 11 z^4 + 18 z^5 + \cdots $$

— every coefficient is the sum of the two preceding ones (source: chapter4, §61).

## Why the method works

Because $D(0) \neq 0$, the power series $A + Bz + Cz^2 + \cdots$ satisfying $N = D \cdot (A + Bz + \cdots)$ is unique: the coefficient of $z^n$ on the left side equals a finite sum involving $A, B, \ldots$ through degree at most $n$, and matching these determines each coefficient in turn. Euler treats uniqueness as obvious; a modern statement would invoke the formal power series ring, where $D(0) \neq 0$ makes $D$ a unit.

## Relationship to other methods

- Long division produces the same series one term at a time, but does not exhibit the recurrence. See [[geometric-series]] §60 for the parallel.
- Once the recurrence is identified, the series is a [[recurrent-series]] and the theory of Chapter 4 applies.
- For irrational functions, the analogue is to assume the binomial form $(P + Q)^{m/n}$ and derive term-to-term relations; see [[binomial-series]].

## Related pages

- [[geometric-series]]
- [[recurrent-series]]
- [[binomial-series]]
- [[chapter-4-on-the-development-of-functions-in-infinite-series]]
