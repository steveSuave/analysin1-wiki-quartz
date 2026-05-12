# Improper Rational Function

**Summary**: A rational function whose numerator has degree at least the degree of the denominator; Euler shows (§38) it can always be split into a polynomial part plus a proper rational remainder.

**Sources**: chapter2.pdf

**Last updated**: 2026-04-23

---

## Definition

By analogy with improper fractions in arithmetic (source: chapter2.pdf, §38):

- A *proper* rational function is one in which the degree of the numerator is **less than** the degree of the denominator.
- An *improper* rational function is one in which the degree of the numerator is **greater than or equal to** the degree of the denominator.

## Reduction by polynomial division (§38)

If a rational function $M / N$ is improper, divide $M$ by $N$ "in the usual way" until the next quotient term would have negative degree. At that point:

$$ \frac{M}{N} = (\text{polynomial part}) + \frac{M'}{N}, $$

where $M'$ has smaller degree than $N$, so that $M' / N$ is proper.

### Euler's example

$$ \frac{1 + z^4}{1 + z^2} = z^2 - 1 + \frac{2}{1 + z^2} \qquad (\text{source: chapter2.pdf, \S 38}). $$

## Why the split matters

[[partial-fraction-decomposition]] applies directly only to proper rational functions. For an improper rational function one first extracts the polynomial part, then decomposes the proper remainder. Euler notes (source: chapter2.pdf, §46) that the polynomial part can equivalently be added before or after the partial fractions are computed, since the same partial fraction arises from an individual linear factor of $N$ whether one uses $M$ or $M$ plus a multiple of $N$.

## Related pages

- [[partial-fraction-decomposition]]
- [[classification-of-functions]]
- [[chapter-2-on-the-transformation-of-functions]]
