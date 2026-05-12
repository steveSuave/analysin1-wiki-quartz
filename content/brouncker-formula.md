# Brouncker's Continued Fraction for $4/\pi$

**Summary**: Applying the §369 reciprocal-series template to the Leibniz series $\pi/4 = 1 - 1/3 + 1/5 - 1/7 + \cdots$ produces William Brouncker's 1655 continued fraction $4/\pi = 1 + 1^2/(2 + 3^2/(2 + 5^2/(2 + 7^2/(2 + \cdots))))$ — the first continued fraction for $\pi$ in the history of mathematics, recovered here by Euler as a particular case of his general series-to-CF dictionary.

**Sources**: `chapter18` (§369 Example II).

**Last updated**: 2026-05-11

---

## Derivation

The [[arctangent-series|Leibniz series]] for $\pi/4$ has the form $1/A - 1/B + 1/C - 1/D + \cdots$ with $A = 1, B = 3, C = 5, D = 7, \ldots$. Applying [[continued-fraction-series-equivalence|Template II of §369]] — set $b = A = 1$, $c = B - A = 2$, $d = C - B = 2$, $e = D - C = 2$, $\ldots$ — gives partial numerators $\alpha = 1, \beta = A^2 = 1, \gamma = B^2 = 9, \delta = C^2 = 25, \epsilon = D^2 = 49, \ldots$ and partial denominators $b = 1, c = d = e = \cdots = 2$. Therefore

$$\frac{\pi}{4} = \cfrac{1}{1 + \cfrac{1}{2 + \cfrac{9}{2 + \cfrac{25}{2 + \cfrac{49}{2 + \cdots}}}}}\,.$$

Inverting (Euler's preferred form, §369 Example II) eliminates the leading $1/(1 + \cdots)$:

$$\boxed{\ \frac{4}{\pi} = 1 + \cfrac{1^2}{2 + \cfrac{3^2}{2 + \cfrac{5^2}{2 + \cfrac{7^2}{2 + \cfrac{9^2}{2 + \cdots}}}}}\ }$$

Numerators are the squares of the odd integers; all partial denominators equal $2$ from the second level onward.

## Historical note

Euler attributes the identity directly: "this is the expression first found by BROUNCKER as a quadrature of the circle." William Brouncker (1620–1684), first president of the Royal Society, communicated it to John Wallis around 1655 in connection with Wallis's *Arithmetica infinitorum*; it was Wallis who in turn proved it equivalent to his own [[wallis-product|infinite product]] $\pi/2 = (2\cdot 2\cdot 4\cdot 4\cdots)/(1\cdot 3\cdot 3\cdot 5\cdots)$. The Brouncker continued fraction was the first ever written down for $\pi$, predating Euler's series-CF dictionary by nearly a century.

## Convergence

Although the form is elegant, convergence is slow — comparable to the Leibniz series itself. The $n$-th convergent has error of order $1/n$, not $1/n^2$ or geometric, because the partial numerators $(2k+1)^2$ grow at exactly the rate that cancels the geometric decay one would expect from a simple CF with bounded partial numerators. So Brouncker's formula is more aesthetic than computational; for fast computation of $\pi$ Euler had already given [[machin-like-formula|Machin's formula]] $\pi/4 = \arctan(1/2) + \arctan(1/3)$ in chapter 8, and §382 will give the convergents of $\pi$ directly via the Euclidean-algorithm method.

## Related pages

- [[continued-fraction-series-equivalence]] — the §369 reciprocal-series template Euler applies here
- [[arctangent-series]] — source of the Leibniz $\pi/4$ series
- [[wallis-product]] — Wallis's product, which Brouncker's CF was derived in connection with
- [[machin-like-formula]] — much faster way of computing $\pi$
- [[best-rational-approximations]] — §382 derives a different (faster) CF for $\pi$ by the Euclidean method
- [[chapter-18-on-continued-fractions]]
