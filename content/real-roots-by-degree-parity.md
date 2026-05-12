# Real Roots by Degree Parity

**Summary**: Euler's §34–§37 results on when a polynomial must have real roots, based on the parity of its degree and the sign of its constant term.

**Sources**: chapter2

**Last updated**: 2026-04-23

---

## Odd-degree polynomials have a real root (§34)

Let $Z = z^{2n+1} + \alpha z^{2n} + \beta z^{2n-1} + \cdots$. As $z \to \infty$ the leading term dominates so $Z \to \infty$, and as $z \to -\infty$ Euler obtains $Z \to -\infty$ (source: chapter2, §34). By the [[intermediate-value-property]], $Z$ takes every intermediate value, including $0$. Hence $Z$ has at least one real linear factor $z - c$.

## Odd number of real linear factors in odd degree (§35)

If $Z$ has degree $2n+1$ and has a real linear factor $z - c$, dividing by $(z - c)(z - d)$ — if $z - d$ is a second real factor — yields a polynomial of odd degree $2n - 1$, which again has a real linear factor. By induction:

> If $Z$ has more than one real linear factor, it will have three, or (since the same argument is valid) five or seven, etc. (source: chapter2, §35)

Consequently the number of complex linear factors is even, consistent with §30.

## Even-degree polynomials have an even number of real factors (§36)

Suppose a degree-$2n$ polynomial had an odd number $2m + 1$ of real linear factors. Dividing by their product gives a quotient of odd degree $2n - 2m - 1$, which by §34 must have another real linear factor. So the count of real linear factors must be even (source: chapter2, §36).

## Even degree with negative constant term (§37)

For $Z = z^{2n} \pm a z^{2n-1} \pm \cdots \pm n z - A$ with $A > 0$:

- $Z \to +\infty$ as $z \to +\infty$,
- $Z = -A < 0$ at $z = 0$,
- $Z \to +\infty$ as $z \to -\infty$.

By the [[intermediate-value-property]], $Z$ has a real root $c$ with $0 < c < \infty$ and another real root $d$ with $-\infty < d < 0$ (source: chapter2, §37).

> Thus the equation $z^4 + \alpha z^3 + \beta z^2 + \gamma z - a^2 = 0$ has two real roots, one positive and the other negative.

## Euler's use of infinity

Euler treats "$z = \infty$" as a legitimate input: he says $Z - \infty$ has linear factor $z - \infty$ and applies the [[intermediate-value-property]] on the interval $(-\infty, +\infty)$. The reasoning is informal by modern standards but captures the right idea — the polynomial's sign change at infinity forces a real root.

## Related pages

- [[intermediate-value-property]]
- [[factoring-polynomials]]
- [[complex-conjugate-factors]]
- [[chapter-2-on-the-transformation-of-functions]]
