# Continued Fraction for $\log 2$

**Summary**: Applying the §369 reciprocal-series template to the alternating harmonic series $\log 2 = 1 - 1/2 + 1/3 - 1/4 + \cdots$ produces a continued fraction whose partial numerators are the squares $1, 1, 4, 9, 16, 25, \ldots$ and whose partial denominators are all $1$ — a structurally simple companion to [[brouncker-formula|Brouncker's continued fraction for $4/\pi$]].

**Sources**: `chapter18` (§369 Example I).

**Last updated**: 2026-05-11

---

## The identity

The [[logarithmic-series|alternating-harmonic series]] $\log 2 = 1 - 1/2 + 1/3 - 1/4 + 1/5 - \cdots$ has the form $1/A - 1/B + 1/C - 1/D + \cdots$ with $A = 1, B = 2, C = 3, D = 4, \ldots$. By [[continued-fraction-series-equivalence|Template II of §369]] — set $b = A = 1$, $c = B - A = 1$, $d = C - B = 1$, $e = D - C = 1$, $\ldots$ — the partial numerators become $\alpha = 1, \beta = A^2 = 1, \gamma = B^2 = 4, \delta = C^2 = 9, \epsilon = D^2 = 16, \ldots$ and all partial denominators are $1$.

Therefore

$$\boxed{\ \log 2 = \cfrac{1}{1 + \cfrac{1}{1 + \cfrac{4}{1 + \cfrac{9}{1 + \cfrac{16}{1 + \cfrac{25}{1 + \cdots}}}}}}\ }$$

with partial numerators $1, 1, 2^2, 3^2, 4^2, 5^2, \ldots$ (i.e., the squares of $1, 1, 2, 3, 4, 5, \ldots$) and partial denominators all $1$.

## Convergence

Like the [[brouncker-formula|Brouncker formula]], this CF inherits slow ($\sim 1/n$) convergence from its parent series — the partial numerators $k^2$ grow at exactly the rate that cancels the geometric decay that bounded partial numerators would have produced. Faster convergence for $\log 2$ comes from the [[logarithmic-series|§120 fast variant]] $\log\bigl(\tfrac{1+x}{1-x}\bigr) = 2(x + x^3/3 + x^5/5 + \cdots)$ evaluated at $x = 1/3$ rather than from this CF.

## Related pages

- [[continued-fraction-series-equivalence]] — the §369 reciprocal-series template Euler applies here
- [[logarithmic-series]] — source of the alternating-harmonic series for $\log 2$
- [[brouncker-formula]] — sister identity, partial numerators odd squares
- [[chapter-18-on-continued-fractions]]
