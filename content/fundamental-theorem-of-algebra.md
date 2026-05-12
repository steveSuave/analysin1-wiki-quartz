# Fundamental Theorem of Algebra

**Summary**: Euler's §32 claim that every real polynomial factors into real linear and quadratic factors — an early, non-rigorous statement of the fundamental theorem of algebra over $\mathbb{R}$.

**Sources**: chapter2.pdf

**Last updated**: 2026-04-23

---

## Euler's statement

> Whatever number of complex linear factors a polynomial function $Z$ of $z$ may have, they can always be paired in such a way that the product of such pairs is real. (source: chapter2.pdf, §32)

Equivalently: every polynomial function of $z$ can be written as a product of real linear and real quadratic factors.

## Euler's argument and its gap

For the special case of four complex linear factors, Euler gives an explicit calculation showing they can be paired into two real quadratic factors (source: chapter2.pdf, §31; see [[complex-conjugate-factors]]). Beyond that he concedes:

> Although the same method of proof is not valid for higher powers, nevertheless, there is no doubt that the same property holds for any number of complex factors. (source: chapter2.pdf, §32)

He then admits:

> Granted that this has not been proved with complete rigor, still the truth of the statement will be corroborated in what follows, where functions with the form $a + b z^n$, $a + b z^n + c z^{2n}$, $a + b z^n + c z^{2n} + d z^{3n}$, etc. will actually be resolved into such real quadratic factors. (source: chapter2.pdf, §32)

So for Euler the result is a working hypothesis supported by explicit computations in special families.

## Modern framing

The theorem over $\mathbb{C}$ (every non-constant polynomial has a complex root) is equivalent to Euler's §32 claim once one observes that complex roots of real polynomials come in conjugate pairs and each conjugate pair $(z - \alpha)(z - \bar{\alpha})$ is a real quadratic.

Rigorous proofs came later — notably Gauss's dissertation (1799) — long after the *Introductio* (1748).

## How Euler uses the theorem

The §32 decomposition into real linear and quadratic factors is the structural result behind [[partial-fraction-decomposition]]: a proper rational function with real coefficients decomposes into a sum of simple fractions of the form $A/(p - qz)^k$ and — Euler will show later — simple fractions with real quadratic denominators.

## Related pages

- [[factoring-polynomials]]
- [[complex-conjugate-factors]]
- [[partial-fraction-decomposition]]
- [[chapter-2-on-the-transformation-of-functions]]
