# Heterogeneous Function

**Summary**: A function of $y, z$ is heterogeneous if its terms have at least two different degrees. Euler classifies such functions by the number of distinct degrees: *bifid* (two), *trifid* (three), and so on. Some heterogeneous functions can be made homogeneous by a substitution of the form $z = x^k$ or $z = 1/x$; no general criterion is given.

**Sources**: chapter5.pdf

**Last updated**: 2026-04-23

---

## Classification by number of distinct degrees (§92)

A *bifid* function has terms of exactly two different degrees — it is a sum of two [[homogeneous-function|homogeneous]] pieces. Example (source: chapter5.pdf, §92):

$$y^5 + 2 y^3 z^2 + y^2 + z^2$$

is bifid: the parts $y^5 + 2y^3 z^2$ and $y^2 + z^2$ have degrees 5 and 2 respectively.

A *trifid* function has three distinct degrees — a sum of three homogeneous pieces. Example:

$$y^6 + y^2 z^2 + z^4 + y - z$$

has degrees 6, 4, 1.

Not every rational or irrational function splits cleanly into homogeneous parts. Euler's examples of the "cannot be resolved" kind:

$$\frac{y^3 + ayz}{by + z^2}, \qquad \frac{a + \sqrt{y^2 + z^2}}{y^2 - bz}.$$

For these the degree is genuinely not defined.

## §93 — Reducing to homogeneous by substitution

Sometimes a substitution for one variable converts a heterogeneous expression into a homogeneous one. Euler gives two examples with no general theory (source: chapter5.pdf, §93):

**Example 1.** $V = y^5 + z^2 y + y^3 z + z^3/y$. The substitution $z = x^2$ gives

$$V = y^5 + x^4 y + y^3 x^2 + x^6/y,$$

which is homogeneous of degree 5 in $x, y$.

**Example 2.** $V = y + y^2 x + y^3 x^2 + y^5 x^4 + a/x$. The substitution $x = 1/z$ gives

$$V = y + y^2/z + y^3/z^2 + y^5/z^4 + a z,$$

homogeneous of degree 1.

Euler's comment: "there are much more difficult cases which can be reduced to homogeneity, but with substitutions which are not so simple." No criterion, no algorithm.

## Related pages

- [[homogeneous-function]]
- [[functions-of-several-variables]]
- [[chapter-5-on-functions-of-two-or-more-variables]]
