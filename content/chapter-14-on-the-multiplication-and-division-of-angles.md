# Chapter 14 — On the Multiplication and Division of Angles

**Summary**: §234–§263. Euler systematically derives polynomial and product expressions for $\sin nz$, $\cos nz$, $\tan nz$ in terms of trig functions of $z$, identifies the roots of the resulting polynomial equations as trig values at equally-spaced angles, and reads off partial-fraction, sum, and product relations for all six trig functions at multiple angles. He then sums sines and cosines of arithmetic progressions (both infinite and finite), and closes by inverting the multiple-angle polynomials to express any power $(\sin z)^n$, $(\cos z)^n$ as a binomial-weighted linear combination of sines or cosines of multiple angles.

**Sources**: chapter14.pdf

**Last updated**: 2026-05-11

---

## Movement 1 — Multiple-angle polynomials (§234–§238, §243)

Starting from the recurrence $\sin((k+1)z) = 2\cos z\cdot\sin(kz) - \sin((k-1)z)$ (scale of relation $2y, -1$ with $y = \cos z$), Euler builds the tables for $\sin nz$ and $\cos nz$ up to $n = 8$. See [[multiple-angle-polynomials]] for the general formulas.

For **odd** $n$, substituting $y = \sqrt{1-x^2}$ (where $x = \sin z$) collapses $\sin nz$ to a pure polynomial in $x$:

$$\sin nz = nx - \frac{n(n^2-1)}{1\cdot 2\cdot 3}x^3 + \frac{n(n^2-1)(n^2-9)}{1\cdot 2\cdot 3\cdot 4\cdot 5}x^5 - \cdots$$

For **even** $n$, a factor $\sqrt{1-x^2}$ remains; squaring yields a polynomial equation.

For $\cos nz$ (§243), the base variable is $y = \cos z$ and the analogous polynomial is

$$\cos nz = 2^{n-1}y^n - \frac{n}{1}2^{n-3}y^{n-2} + \frac{n(n-3)}{1\cdot 2}2^{n-5}y^{n-4} - \cdots$$

## Movement 2 — Roots as trig values at equally-spaced angles (§235–§236, §239, §243–§244)

The equation $\sin s = \sin nz$ has $n$ solutions

$$z = \frac{s}{n},\quad \frac{\pi - s}{n},\quad \frac{2\pi + s}{n},\quad \frac{3\pi - s}{n},\quad \ldots$$

These are the $n$ roots of the polynomial in $x$. From Vieta's formulas Euler reads off: the sum of all roots is zero; the sum of their reciprocals is $n/\sin nz$; and the product gives $\sin nz$ as a product of shifted sines (§237). See [[trig-values-as-roots]].

## Movement 3 — Factored products for sin and cos (§237, §240–§242, §245)

The central product formula (odd and even $n$ unified in §241):

$$\sin nz = 2^{n-1}\sin z\cdot\sin\!\Bigl(\tfrac{\pi}{n}-z\Bigr)\sin\!\Bigl(\tfrac{\pi}{n}+z\Bigr)\sin\!\Bigl(\tfrac{2\pi}{n}-z\Bigr)\sin\!\Bigl(\tfrac{2\pi}{n}+z\Bigr)\cdots$$

where the number of factors equals $n$. Using $\cos nz = \sin 2nz/(2\sin nz)$ (§242), matching cosine products are derived. See [[sine-cosine-factored-products]].

## Movement 4 — Partial-fraction sums for csc, sec, cot, tan (§237, §246–§256)

From the Vieta reciprocal-root sum, Euler derives:

$$\frac{n}{\sin nz} = \frac{1}{\sin z} + \frac{1}{\sin\!\bigl(\tfrac{2\pi}{n}+z\bigr)} + \frac{1}{\sin\!\bigl(\tfrac{4\pi}{n}+z\bigr)} + \cdots$$

and analogous expansions for $n\cot nz$, $n\sec nz$, $n\csc nz$ (§246–§248). For the tangent (§249–§256), De Moivre gives $\tan nz$ as a rational function of $t = \tan z$, from which $n\cot nz$ splits into $n$ cotangents. See [[trig-multiple-angle-partial-fractions]].

## Movement 5 — Sum of sines/cosines in arithmetic progression (§258–§260)

Since sines of equally-spaced angles form a recurrent series, the infinite sum $\sin a + \sin(a+b) + \sin(a+2b) + \cdots$ is the rational function

$$s = \frac{\sin a - \sin(a - b)}{2 - 2\cos b} = \frac{\sin a - \sin(a-b)}{2(1-\cos b)}$$

obtained by evaluating the generating function at $z = 1$. The finite sum through $\sin(a+nb)$ is then obtained (§259–§260) by subtracting the corresponding tail, giving the standard

$$\sum_{k=0}^{n}\sin(a + kb) = \frac{\sin(a + \tfrac{1}{2}nb)\sin(\tfrac{1}{2}(n+1)b)}{\sin(\tfrac{1}{2}b)}$$

and the analogous cosine formula. See [[sum-of-trig-in-ap]].

## Movement 6 — Powers of sin and cos as multiple-angle sums (§261–§263)

Inverting the chapter's main thread: any power $(\sin z)^n$ is a binomial-weighted finite sum of $\sin kz$ (or $\cos kz$ for even $n$), and similarly for $(\cos z)^n$. Examples:

$$4(\sin z)^3 = 3\sin z - \sin 3z, \qquad 8(\cos z)^4 = 3 + 4\cos 2z + \cos 4z.$$

The reduction is obtained from the four product-to-sum identities of §262. See [[powers-of-sine-and-cosine]].

## Related pages

- [[multiple-angle-polynomials]]
- [[sine-cosine-factored-products]]
- [[trig-values-as-roots]]
- [[trig-multiple-angle-partial-fractions]]
- [[sum-of-trig-in-ap]]
- [[powers-of-sine-and-cosine]]
- [[de-moivre-formula]]
- [[trigonometric-recurrent-progression]]
- [[cotangent-partial-fraction]]
- [[recurrent-series]]
- [[chapter-8-on-transcendental-quantities-which-arise-from-the-circle]]
- [[chapter-13-on-recurrent-series]]
