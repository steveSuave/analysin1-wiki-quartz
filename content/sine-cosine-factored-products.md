# Sine and Cosine Factored Products

**Summary**: §237, §240–§242, §245. The product of the $n$ roots of the [[multiple-angle-polynomials|multiple-angle polynomial]] for $\sin nz$ (or $\cos nz$) yields a factorization of $\sin nz$ (or $\cos nz$) as $2^{n-1}$ times a product of $n$ sines (or cosines) of shifted angles. A single unified formula covers both odd and even $n$.

**Sources**: chapter14 (§237, §240–§242, §245)

**Last updated**: 2026-05-10

---

## Odd $n$: product formula for $\sin nz$ (§237)

From [[trig-values-as-roots|§236–§237]], the $n$ roots of the odd-$n$ polynomial in $x = \sin z$ are $\sin z, \sin(\frac{2\pi}{n}+z), \sin(\frac{4\pi}{n}+z), \ldots$. The leading coefficient of the polynomial is $\pm 2^{n-1}$ (from the table in [[multiple-angle-polynomials|§234/§236]]). The constant term divided by the leading coefficient is $\sin nz / (\pm 2^{n-1})$. Writing out the product of all roots and equating:

$$\sin nz = \pm 2^{n-1}\sin z\cdot\sin\!\Bigl(\frac{2\pi}{n}+z\Bigr)\cdot\sin\!\Bigl(\frac{4\pi}{n}+z\Bigr)\cdots$$

(source: chapter14, §237). Because $\sin v = \sin(\pi - v)$, the root $\sin(\frac{(n-k)\pi}{n}+z)$ equals $\sin(\frac{k\pi}{n}-z)$ for appropriate $k$, so the product telescopes to $n$ factors total.

**Example $n = 3$** (§237):

$$\sin 3z = -4\sin z\cdot\sin\!\Bigl(\frac{2\pi}{3}+z\Bigr)\cdot\sin\!\Bigl(\frac{4\pi}{3}+z\Bigr) = 4\sin z\sin\!\Bigl(\frac{\pi}{3}-z\Bigr)\sin\!\Bigl(\frac{\pi}{3}+z\Bigr)$$

**Example $n = 5$** (§237):

$$\sin 5z = 16\sin z\cdot\sin\!\Bigl(\frac{\pi}{5}-z\Bigr)\sin\!\Bigl(\frac{\pi}{5}+z\Bigr)\sin\!\Bigl(\frac{2\pi}{5}-z\Bigr)\sin\!\Bigl(\frac{2\pi}{5}+z\Bigr)$$

## Even $n$: product formula for $\sin nz$ (§239–§240)

For even $n$, squaring removes the $\sqrt{1-x^2}$ factor. The $2n$ roots of the resulting polynomial come in positive/negative pairs. From the product formula for the squared version, taking the square root and identifying signs:

$$\sin nz = \pm 2^{n-1}\sin z\cdot\sin\!\Bigl(\frac{\pi}{n}-z\Bigr)\sin\!\Bigl(\frac{\pi}{n}+z\Bigr)\sin\!\Bigl(\frac{2\pi}{n}+z\Bigr)\sin\!\Bigl(\frac{2\pi}{n}-z\Bigr)\cdots$$

(source: chapter14, §239–§240). **Example $n = 2$**:

$$\sin 2z = 2\sin z\cdot\sin\!\Bigl(\frac{\pi}{2}-z\Bigr) = 2\sin z\cos z$$

**Example $n = 4$**:

$$\sin 4z = 8\sin z\cdot\sin\!\Bigl(\frac{\pi}{4}-z\Bigr)\sin\!\Bigl(\frac{\pi}{4}+z\Bigr)\sin\!\Bigl(\frac{\pi}{2}-z\Bigr)$$

## Unified formula (§241)

Euler observes that both cases are captured by the single expression (§241):

$$\sin nz = 2^{n-1}\sin z\cdot\sin\!\Bigl(\frac{\pi}{n}-z\Bigr)\sin\!\Bigl(\frac{\pi}{n}+z\Bigr)\cdot\sin\!\Bigl(\frac{2\pi}{n}-z\Bigr)\sin\!\Bigl(\frac{2\pi}{n}+z\Bigr)\cdots$$

with exactly $n$ factors, the last factor being $\sin(\frac{\pi}{2}-z) = \cos z$ when $n$ is even, and $\sin z$ itself paired with the outermost product terms when $n$ is odd. The full table from §241:

| $n$ | $\sin nz$ |
|:--:|:--|
| 1 | $\sin z$ |
| 2 | $2\sin z\cos z$ |
| 3 | $4\sin z\cdot\sin(\frac{\pi}{3}-z)\sin(\frac{\pi}{3}+z)$ |
| 4 | $8\sin z\cdot\sin(\frac{\pi}{4}-z)\sin(\frac{\pi}{4}+z)\sin(\frac{2\pi}{4}-z)$ |
| 5 | $16\sin z\cdot\sin(\frac{\pi}{5}-z)\sin(\frac{\pi}{5}+z)\sin(\frac{2\pi}{5}-z)\sin(\frac{2\pi}{5}+z)$ |
| 6 | $32\sin z\cdot\sin(\frac{\pi}{6}-z)\sin(\frac{\pi}{6}+z)\sin(\frac{2\pi}{6}-z)\sin(\frac{2\pi}{6}+z)\sin(\frac{3\pi}{6}-z)$ |

## Cosine products (§242, §245)

Using the identity $\cos nz = \sin 2nz / (2\sin nz)$ (§242), the cosine products follow from the sine products at $n$ and $2n$. Euler lists:

$$\cos nz = 2^{n-1}\sin\!\Bigl(\frac{\pi}{2n}-z\Bigr)\sin\!\Bigl(\frac{\pi}{2n}+z\Bigr)\sin\!\Bigl(\frac{3\pi}{2n}-z\Bigr)\sin\!\Bigl(\frac{3\pi}{2n}+z\Bigr)\cdots$$

where there are $n$ factors (source: chapter14, §242).

In §245 a cosine-only version is derived. Using $\cos v = -\cos(\pi - v)$:

$$\cos nz = 2^{n-1}\cos\!\Bigl(\frac{n-1}{n}\pi+z\Bigr)\cos\!\Bigl(\frac{n-1}{n}\pi-z\Bigr)\cos\!\Bigl(\frac{n-3}{n}\pi+z\Bigr)\cdots$$

Sample cases from §245:
- $\cos z = \cos z$
- $\cos 2z = 2\cos(\frac{\pi}{4}+z)\cos(\frac{\pi}{4}-z)$
- $\cos 3z = 4\cos(\frac{2\pi}{6}+z)\cos(\frac{2\pi}{6}-z)\cos z$
- $\cos 4z = 8\cos(\frac{3\pi}{8}+z)\cos(\frac{3\pi}{8}-z)\cos(\frac{\pi}{8}+z)\cos(\frac{\pi}{8}-z)$

## Relation to the sine-infinite-product

The §241 formula at $z$ fixed and $n \to \infty$ recovers the [[sine-infinite-product|§158 infinite product]] $\sin z = z\prod_{k=1}^{\infty}(1 - z^2/k^2\pi^2)$: each finite factor $\sin(k\pi/n \pm z)$ approximates $(k\pi/n \pm z)$ for large $n$, and the $2^{n-1}$ prefactor accounts for the $z$ in the numerator. Chapter 14's finite products are thus a finite-$n$ refinement of Chapter 9's infinite product.

## Sum of sines of equally-spaced angles (§237)

The penultimate [[vietas-formulas|Vieta formula]] (sum of all roots, §237) gives

$$0 = \sin z + \sin\!\Bigl(\frac{2\pi}{n}+z\Bigr) + \sin\!\Bigl(\frac{4\pi}{n}+z\Bigr) + \cdots$$

(sum of $n$ equally-spaced sines is zero). This is the $n$-point discrete Fourier sum, which Euler derives here for the first time in this generality.

## Related pages

- [[multiple-angle-polynomials]]
- [[trig-values-as-roots]]
- [[trig-multiple-angle-partial-fractions]]
- [[sine-infinite-product]]
- [[cosine-infinite-product]]
- [[factorization-of-an-plus-minus-zn]]
- [[chapter-14-on-the-multiplication-and-division-of-angles]]
