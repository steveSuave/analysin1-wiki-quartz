# Trig Values as Roots

**Summary**: §235–§236, §239, §243–§244, §250–§256. The [[multiple-angle-polynomials|multiple-angle polynomial]] equation $\sin nz = \sin s$ has exactly $n$ distinct roots, which are the sines of equally-spaced arcs $s/n, (\pi-s)/n, (2\pi+s)/n, \ldots$. [[vietas-formulas|Vieta's formulas]] on these roots produce the partial-fraction sums and products of trig functions that occupy §237–§257.

**Sources**: chapter14 (§235–§256)

**Last updated**: 2026-05-10

---

## The $n$ roots of $\sin nz = \sin s$ (§235)

If we set $\sin nz = \sin s$, then $nz = s, \pi - s, 2\pi + s, 3\pi - s, \ldots$, so

$$z = \frac{s}{n},\quad \frac{\pi-s}{n},\quad \frac{2\pi+s}{n},\quad \frac{3\pi-s}{n},\quad \frac{4\pi+s}{n},\quad \ldots$$

There are exactly $n$ distinct values of $\sin z$ corresponding to these arcs, namely

$$\sin\frac{s}{n},\quad \sin\frac{\pi-s}{n},\quad \sin\frac{2\pi+s}{n},\quad \sin\frac{3\pi-s}{n},\quad \ldots$$

(source: chapter14, §235). These are the $n$ roots of the polynomial in $x = \sin z$ obtained from $\sin nz = \sin s$ (the [[multiple-angle-polynomials|§236 polynomial]] for odd $n$, or the squared version for even $n$).

## Roots of the odd-$n$ polynomial (§236)

For odd $n$, the polynomial $\sin nz = \sin s$ in $x$ can be rewritten (shifting $z$ so that $\sin s = 0$, i.e. taking $s = 0$) as the equation

$$0 = \sin nz = nx - \frac{n(n^2-1)}{1\cdot 2\cdot 3}x^3 + \cdots$$

whose $n$ roots are $\sin z, \sin\bigl(\frac{2\pi}{n}+z\bigr), \sin\bigl(\frac{4\pi}{n}+z\bigr), \ldots$ (source: chapter14, §236).

Euler notes that in order to express things in terms of arcs less than $\pi$, one may use the identity $\sin v = -\sin(v - \pi)$; this is how the examples in §237 (Example I, $n = 3$; Example II, $n = 5$; Example III, $n = 2m+1$) simplify the list of roots to angles between $0$ and $\pi$.

## Vieta's formulas on the roots (§237)

Euler does not invoke Vieta explicitly by name, but the procedure is identical. Let the $n$ roots be $r_1, r_2, \ldots, r_n$. From the polynomial:

- **Sum of roots**: The coefficient of $x^{n-2}$ (the second-highest degree) in the odd-$n$ polynomial is zero (the term is absent), so $\sum r_k = 0$.

- **Sum of reciprocals**: The ratio of the constant term to the linear coefficient gives
$$\frac{1}{r_1} + \frac{1}{r_2} + \cdots + \frac{1}{r_n} = \frac{n}{\sin nz}$$
(source: chapter14, §237). This is the partial-fraction formula for cosecant; see [[trig-multiple-angle-partial-fractions]].

- **Product**: The product of all $n$ roots equals $\pm\sin nz / 2^{n-1}$, which after rearrangement gives the [[sine-cosine-factored-products|product formula for $\sin nz$]].

## Roots of the cosine polynomial (§243–§244)

For the polynomial in $y = \cos z$ (§243), the $n$ roots are

$$\cos z,\quad \cos\!\Bigl(\frac{2\pi}{n} - z\Bigr),\quad \cos\!\Bigl(\frac{2\pi}{n} + z\Bigr),\quad \cos\!\Bigl(\frac{4\pi}{n} - z\Bigr),\quad \ldots$$

(source: chapter14, §243). Their sum (§244): for $n > 1$, the sum of all $n$ roots is zero,

$$0 = \cos z + \cos\!\Bigl(\frac{2\pi}{n} - z\Bigr) + \cos\!\Bigl(\frac{2\pi}{n} + z\Bigr) + \cos\!\Bigl(\frac{4\pi}{n} - z\Bigr) + \cdots$$

For even $n$, each positive term is paired with an equal negative term. For odd $n > 1$, Euler verifies case by case using $\cos v = -\cos(\pi - v)$ (source: chapter14, §244).

## Roots of the tangent equation (§249–§252)

Setting $t = \tan z$ and using [[de-moivre-formula|De Moivre]]:

$$\tan nz = \frac{(1+ti)^n - (1-ti)^n}{(1+ti)^n\,i + (1-ti)^n\,i}$$

(source: chapter14, §249). The $n$ roots of $\tan nz = \tan nz$ (i.e., of the numerator polynomial in $t$ when $\tan nz$ is fixed) are

$$\tan z,\quad \tan\!\Bigl(\frac{\pi}{n}+z\Bigr),\quad \tan\!\Bigl(\frac{2\pi}{n}+z\Bigr),\quad \ldots$$

(source: chapter14, §249). The sum of these $n$ roots equals $n\cot nz$ (§250), and their product is determined by the constant term of the polynomial (§254).

For $n = 2m+1$ (odd), comparing with the equation's highest-degree coefficient gives
$$n\tan nz = \tan z + \tan\!\Bigl(\frac{\pi}{n}+z\Bigr) + \tan\!\Bigl(\frac{2\pi}{n}+z\Bigr) + \cdots + \tan\!\Bigl(\frac{n-1}{n}\pi+z\Bigr)$$

## Special cases (§237 Example I, II; §243–§244)

**$n = 3$** (§237):
$$0 = \sin z + \sin\!\Bigl(\frac{2\pi}{3}+z\Bigr) + \sin\!\Bigl(\frac{4\pi}{3}+z\Bigr)$$

$$0 = \cos z + \cos\!\Bigl(\frac{2\pi}{3}-z\Bigr) + \cos\!\Bigl(\frac{2\pi}{3}+z\Bigr)$$

**$n = 5$** (§237):
$$0 = \sin z + \sin\!\Bigl(\frac{2\pi}{5}+z\Bigr) + \sin\!\Bigl(\frac{\pi}{5}-z\Bigr) - \sin\!\Bigl(\frac{\pi}{5}+z\Bigr) - \sin\!\Bigl(\frac{2\pi}{5}-z\Bigr)$$

## Why it matters

The identification of trig values at arithmetic progressions of angles as the roots of a single polynomial is the algebraic engine that generates essentially all of the identities in Chapter 14. Every partial-fraction expansion of $n\cot nz$, $n/\sin nz$, etc., follows by reading one of Vieta's formulas off the same polynomial — Euler is systematically mining a single algebraic object.

## Related pages

- [[multiple-angle-polynomials]]
- [[sine-cosine-factored-products]]
- [[trig-multiple-angle-partial-fractions]]
- [[de-moivre-formula]]
- [[factoring-polynomials]]
- [[single-valued-and-multi-valued-functions]]
- [[chapter-14-on-the-multiplication-and-division-of-angles]]
