# Vieta's Formulas

**Summary**: The dictionary between the coefficients of a polynomial and the elementary symmetric functions of its roots. For a monic degree-$n$ polynomial $\prod_{k=1}^n(Z - \alpha_k) = Z^n - PZ^{n-1} + QZ^{n-2} - RZ^{n-3} + \cdots$, the coefficient $P$ is the sum of the roots, $Q$ the sum of pairwise products, $R$ the sum of triple products, and so on, with the final coefficient being $\pm\prod\alpha_k$. Euler uses this identification — without naming Vieta — as a workhorse throughout the *Introductio*: it converts every product expansion into a stack of identities, one for each symmetric polynomial.

**Sources**: chapter1.pdf, chapter9.pdf, chapter10.pdf, chapter14.pdf

**Last updated**: 2026-05-11

---

## Statement

If $\alpha_1, \ldots, \alpha_n$ are the (possibly complex, possibly repeated) roots of

$$Z^n - PZ^{n-1} + QZ^{n-2} - RZ^{n-3} + SZ^{n-4} - \cdots \pm V = 0,$$

then

$$P = \sum_k \alpha_k,\quad Q = \sum_{i<j}\alpha_i\alpha_j,\quad R = \sum_{i<j<k}\alpha_i\alpha_j\alpha_k,\quad \ldots,\quad V = \alpha_1\alpha_2\cdots\alpha_n.$$

The $k$-th coefficient (with the sign convention shown) is the $k$-th [[newtons-identities|elementary symmetric polynomial]] $e_k(\alpha_1, \ldots, \alpha_n)$. The identification follows immediately from expanding the factored form $\prod(Z - \alpha_k)$.

## Where Euler uses it

### Chapter 1 — to define multi-valued functions

In [[single-valued-and-multi-valued-functions|§§11–13]] Euler introduces the $n$-valued function $Z$ as the solution of

$$Z^n - PZ^{n-1} + QZ^{n-2} - \cdots = 0$$

where $P, Q, \ldots$ are single-valued functions of $z$, and states Vieta's relations as the definition of what $P, Q, \ldots$ *mean*: sum of values, sum of pairwise products, etc. This is the first appearance of the formulas in the book and the cleanest statement of them.

### Chapter 9 — to read off product expansions

In [[chapter-9-on-trinomial-factors|Chapter 9]] Euler establishes infinite-product formulas like

$$\sin z = z\prod_{k=1}^{\infty}\left(1 - \frac{z^2}{k^2\pi^2}\right).$$

Comparing the coefficients of the right side (Vieta) with those of the [[sine-and-cosine-series|Taylor series]] of $\sin z$ on the left turns the product into a generator of identities. This is the engine behind the [[basel-problem|Basel problem]] and the entire [[zeta-at-even-integers|even-zeta table]].

### Chapter 10 — combined with Newton

[[newtons-identities|Newton's identities]] convert the elementary symmetric functions $P, Q, R, \ldots$ into the power sums $\sum\alpha_k$, $\sum\alpha_k^2$, $\sum\alpha_k^3$, $\ldots$. The composite "Vieta then Newton" recipe is what Euler runs on the [[exponential-infinite-product|sinh product]] in [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series|Chapter 10]] to read off $\sum 1/k^{2m}$ for every $m$.

### Chapter 14 — to extract trigonometric sums and products

In [[chapter-14-on-the-multiplication-and-division-of-angles|Chapter 14]] Euler factors the [[multiple-angle-polynomials|multiple-angle polynomial]] $\sin nz / \sin z$ as a product over its $n-1$ roots, which are $\sin$ values at equally-spaced angles. Vieta's formulas applied to this factorization give all of the [[sine-cosine-factored-products|factored products]], [[trig-multiple-angle-partial-fractions|partial-fraction sums]] for csc, sec, cot, tan, and the product-of-tangents identity that drops out of [[de-moivre-formula|De Moivre]] in §249. The [[trig-values-as-roots]] page is the umbrella treatment.

## Naming

François Viète (Vieta) stated the formulas in 1579–1591 for specific low degrees; the general statement was systematized by Albert Girard in 1629 and is sometimes called *Newton–Girard* in the symmetric-function literature, but the modern English-language name is **Vieta's formulas**. Euler refers to the relations without attribution; he treats them as a basic property of polynomials.

## A trivial example

For $Z^3 - 6Z^2 + 11Z - 6 = 0$ with roots $1, 2, 3$:

- $P = 1 + 2 + 3 = 6$,
- $Q = 1\cdot 2 + 1\cdot 3 + 2\cdot 3 = 11$,
- $R = 1\cdot 2\cdot 3 = 6$.

## Related pages

- [[single-valued-and-multi-valued-functions]]
- [[newtons-identities]]
- [[factoring-polynomials]]
- [[trig-values-as-roots]]
- [[multiple-angle-polynomials]]
- [[sine-cosine-factored-products]]
- [[trig-multiple-angle-partial-fractions]]
- [[de-moivre-formula]]
- [[basel-problem]]
- [[chapter-1-on-functions-in-general]]
- [[chapter-9-on-trinomial-factors]]
- [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series]]
- [[chapter-14-on-the-multiplication-and-division-of-angles]]
