# Partial Fraction Decomposition

**Summary**: Euler's method (§39–§46) for resolving a proper rational function into a sum of simple fractions, one per linear factor of the denominator (with a tower of fractions when factors repeat).

**Sources**: chapter2

**Last updated**: 2026-04-23

---

## Setup

Let $M/N$ be a proper rational function — that is, $\deg M < \deg N$. See [[improper-rational-function]] for how to reduce the improper case by polynomial division first.

By [[factoring-polynomials]] (and, granted the [[fundamental-theorem-of-algebra]]), $N$ factors over $\mathbb{R}$ into linear and quadratic factors. Euler treats the linear case in detail in this chapter; the quadratic case — needed when $N$ has complex roots and a *real* decomposition is required — is handled in [[chapter-12-on-the-development-of-real-rational-functions|Chapter 12]] (see [[real-partial-fraction-decomposition]]).

## Distinct linear factors (§40–§41)

If $N$ factors into $k$ distinct linear factors, $M/N$ decomposes into $k$ simple fractions, one per factor:

$$ \frac{M}{N} = \sum_{i} \frac{A_i}{p_i - q_i z} \qquad (\text{source: chapter2, \S 40}). $$

### Shortcut formula for $A$ (§41, "cover-up")

For the factor $p - q z$ of $N$, write $N = (p - q z) S$. Then the numerator of the corresponding simple fraction is

$$ A = \left. \frac{M}{S} \right|_{z = p/q}. $$

Euler's derivation: from $M/N = A/(p - qz) + P/S$ one gets $M - A S = (p - q z) P$, which vanishes at $z = p/q$, forcing $A = M/S$ evaluated there (source: chapter2, §41).

### Example (§40–§41)

Decompose $\dfrac{1 + z^2}{z - z^3}$. The denominator factors as $z \cdot (1 - z)(1 + z)$, so

$$ \frac{1 + z^2}{z - z^3} = \frac{A}{z} + \frac{B}{1 - z} + \frac{C}{1 + z}. $$

Applying the §41 shortcut:

- For factor $z$: $S = 1 - z^2$, so $A = \left.\tfrac{1 + z^2}{1 - z^2}\right|_{z = 0} = 1$.
- For factor $1 - z$: $S = z + z^2$, so $B = \left.\tfrac{1 + z^2}{z + z^2}\right|_{z = 1} = 1$.
- For factor $1 + z$: $S = z - z^2$, so $C = \left.\tfrac{1 + z^2}{z - z^2}\right|_{z = -1} = -1$.

Hence

$$ \frac{1 + z^2}{z - z^3} = \frac{1}{z} + \frac{1}{1 - z} - \frac{1}{1 + z}. $$

## Repeated linear factors (§42–§45)

If $(p - q z)^n$ divides $N$, that factor contributes the tower

$$ \frac{A}{(p - qz)^n} + \frac{B}{(p - qz)^{n-1}} + \frac{C}{(p - qz)^{n-2}} + \cdots + \frac{K}{p - qz}. $$

### The iterative algorithm (§45)

Write $N = (p - qz)^n Z$. Compute the numerators in sequence, each time substituting $z = p/q$ after dividing by $p - qz$:

1. $A = \left. \dfrac{M}{Z} \right|_{z = p/q}$, then let $P = \dfrac{M - A Z}{p - qz}$.
2. $B = \left. \dfrac{P}{Z} \right|_{z = p/q}$, then let $Q = \dfrac{P - B Z}{p - qz}$.
3. $C = \left. \dfrac{Q}{Z} \right|_{z = p/q}$, then let $R = \dfrac{Q - C Z}{p - qz}$.
4. $D = \left. \dfrac{R}{Z} \right|_{z = p/q}$, then let $S = \dfrac{R - D Z}{p - qz}$.
5. Continue until all $n$ numerators are obtained (source: chapter2, §45).

Each "$\ldots / (p - q z)$" step is an exact polynomial division — the numerator of the previous step is known to be divisible by $p - q z$, so the division clears out before the next substitution is made.

## General procedure (§46)

To decompose an arbitrary rational function $M/N$:

1. If $M/N$ is improper, extract the polynomial part by division; see [[improper-rational-function]].
2. Factor $N$ into its linear factors (real or complex).
3. For each *distinct* linear factor $p - q z$ not repeated elsewhere, use the shortcut (§41) to produce a single simple fraction.
4. For each *repeated* linear factor $(p - qz)^n$, use the iterative algorithm (§45) to produce the tower of $n$ simple fractions.
5. Sum all simple fractions (plus the polynomial part, if any). The result equals $M/N$ in its simplest form (source: chapter2, §46).

### Worked example (§46)

Decompose $\dfrac{1}{z^3 (1 - z)^2 (1 + z)}$. The denominator has factors $1 + z$ (simple), $(1 - z)^2$, and $z^3$.

- **Factor $1 + z$** (simple): $Z = z^3 - 2 z^4 + z^5$, so at $z = -1$: $A = 1 / (z^3 - 2z^4 + z^5)\big|_{z = -1} = -\tfrac{1}{4}$. Contribution: $\dfrac{-1}{4(1 + z)}$.

- **Factor $(1 - z)^2$**: $Z = z^3 + z^4$. At $z = 1$: $A = \tfrac{1}{2}$. Then $P = (M - \tfrac{1}{2} Z)/(1 - z) = 1 + z + z^2 + \tfrac{1}{2} z^3$, and $B = P/Z\big|_{z=1} = \tfrac{7}{4}$. Contribution: $\dfrac{1}{2(1 - z)^2} + \dfrac{7}{4(1 - z)}$.

- **Factor $z^3$**: $Z = 1 - z - z^2 + z^3$. At $z = 0$: $A = 1$. Then $P = (M - Z)/z = 1 + z - z^2$ gives $B = 1$. Then $Q = (P - Z)/z = 2 - z^2$ gives $C = 2$. Contribution: $\dfrac{1}{z^3} + \dfrac{1}{z^2} + \dfrac{2}{z}$.

Putting it all together:

$$ \frac{1}{z^3 (1 - z)^2 (1 + z)} = \frac{1}{z^3} + \frac{1}{z^2} + \frac{2}{z} + \frac{1}{2(1 - z)^2} + \frac{7}{4(1 - z)} - \frac{1}{4(1 + z)}. $$

There is no polynomial part because the given function is proper (source: chapter2, §46).

## Why this matters

Partial-fraction decomposition turns an arbitrary rational function into a sum of maximally simple pieces. This is what makes rational functions tractable in later chapters of the *Introductio* — for expansions into series, for summation, and (in the *Institutiones calculi integralis*) for integration.

## Related pages

- [[real-partial-fraction-decomposition]]
- [[improper-rational-function]]
- [[factoring-polynomials]]
- [[fundamental-theorem-of-algebra]]
- [[complex-conjugate-factors]]
- [[trinomial-factor]]
- [[chapter-2-on-the-transformation-of-functions]]
- [[chapter-12-on-the-development-of-real-rational-functions]]
