# Even and Odd Functions

**Summary**: Euler defines even and odd functions by their behavior under $z \to -z$, and derives their multiplicative rules. The modern definitions appear here essentially unchanged.

**Sources**: chapter1.pdf

**Last updated**: 2026-04-23

---

## Definitions

**Even function** (§18): $Z$ is even in $z$ if $Z(+k) = Z(-k)$ for every $k$. Equivalently, $z$ appears everywhere with even exponent.

**Odd function** (§21): $Z$ is odd in $z$ if $Z(-z) = -Z(z)$. Equivalently, $z$ appears everywhere with odd exponent.

## Examples

**Even** (source: chapter1.pdf, §18):

- Powers $z^m$ with $m$ an even integer (positive or negative).
- $z^{m/n}$ with $m$ even, $n$ odd.
- Polynomials in even powers only: $a + b z^2 + c z^4 + d z^6 + \dots$
- Rational functions whose numerator and denominator are even:
  $\frac{a + b z^2 + c z^4 + \dots}{\alpha + \beta z^2 + \gamma z^4 + \dots}$
- Fractional-exponent variants like $a + b z^{2/3} + c z^{4/7} + \dots$, provided every exponent is an even integer divided by an odd integer.

**Odd** (source: chapter1.pdf, §21):

- $z, z^3, z^5, z^7, \dots; z^{-1}, z^{-3}, z^{-5}, \dots$
- $z^{m/n}$ with $m$ and $n$ both odd integers.
- $az + bz^3, az + a z^{-1}, z^{1/3} + a z^{3/5} + b z^{-5/3}$.

## Multiplicative rules

From §§22-23:

| Operation   | Result |
|-------------|--------|
| even $\times$ $z$  | odd    |
| even $\times$ odd  | odd    |
| even $\div$ odd  | odd    |
| odd $\div$ even  | odd    |
| odd $\times$ odd   | even   |
| odd $\div$ odd   | even   |
| (odd)$^2$     | even   |
| (odd)$^3$     | odd    |

These are just the familiar parity rules. Euler's proofs are direct substitutions of $-z$ for $z$.

## Even functions as functions of $z^2$ (§20)

An even function of $z$ can be obtained by starting with any function $Z = f(y)$ and substituting $y = z^2$. The caveat: if $f$ contains $\sqrt{y}$ or any form that disappears under the substitution, the result is not actually even. Euler's counterexample is $y + \sqrt{ay}$, which becomes $z^2 + z \sqrt{a}$ under $y = z^2$ — odd and even terms mixed.

## Multi-valued even and odd functions

A multi-valued function $Z$ of $z$ is **even** (§19) if the defining equation has $z$ appearing only with even exponents. Examples:

- $Z^2 = az Z^4 + b z^2$ — but this is not purely even, since it has $az$. Euler's actual examples are along the lines of $Z^3 - a z^2 Z^2 + b z^4 Z - c z^8 = 0$ for three-valued even.
- General template: $Z^2 - P Z + Q = 0$ with $P, Q$ single-valued even functions gives a two-valued even $Z$; $Z^3 - P Z^2 + Q Z - R = 0$ analogously gives three-valued even.

## Reciprocity for odd functions (§24)

If $y$ is an odd function of $z$, then $z$ is an odd function of $y$. Example: $y = z^3$ gives $z = y^{1/3}$.

## Parity from the defining equation (§25)

If $y$ is defined implicitly by an equation in $y$ and $z$ such that in every term the sum of the exponents of $y$ and $z$ has the same parity (all even, or all odd), then $y$ is an odd function of $z$. Example: $y^3 + a y^2 z = b y z^2 + c y + d z$ — each term has exponent-sum 3, 3, 3, 1, 1 (all odd), so $y$ is odd in $z$.

## Related pages

- [[function]]
- [[single-valued-and-multi-valued-functions]]
- [[chapter-1-on-functions-in-general]]
