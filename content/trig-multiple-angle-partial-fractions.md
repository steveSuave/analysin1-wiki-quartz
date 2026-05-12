# Trig Multiple-Angle Partial Fractions

**Summary**: §237, §246–§256. By reading [[vietas-formulas|Vieta's]] reciprocal-root formula off the [[multiple-angle-polynomials|multiple-angle polynomial]], Euler expresses $n/\sin nz$, $n\cot nz$, $n\sec nz$, $n\csc nz$, and $n\cot nz$ (tangent version) each as a sum of $n$ terms involving the same function at equally-spaced shifted angles. These generalize the §181–§183 partial fractions of Chapter 10 from a fixed denominator to a sliding one.

**Sources**: chapter14.pdf (§237, §246–§256)

**Last updated**: 2026-05-10

---

## Cosecant sum (§237)

From the reciprocal-root Vieta formula applied to the odd-$n$ polynomial in $x = \sin z$, the sum of reciprocals of all $n$ roots equals the ratio of the $(n-2)$-degree coefficient to the constant term. Euler writes this as:

$$\frac{n}{\sin nz} = \frac{1}{\sin z} + \frac{1}{\sin\!\bigl(\frac{2\pi}{n}+z\bigr)} + \frac{1}{\sin\!\bigl(\frac{4\pi}{n}+z\bigr)} + \cdots$$

where there are $n$ terms (source: chapter14.pdf, §237). In terms of cosecants:

$$n\csc nz = \csc z + \csc\!\Bigl(\frac{2\pi}{n}+z\Bigr) + \cdots$$

**Example $n = 3$** (§237):
$$\frac{3}{\sin 3z} = \frac{1}{\sin z} + \frac{1}{\sin(\frac{2\pi}{3}+z)} + \frac{1}{\sin(\frac{4\pi}{3}+z)} = \frac{1}{\sin z} + \frac{1}{\sin(\frac{\pi}{3}-z)} - \frac{1}{\sin(\frac{\pi}{3}+z)}$$

The general formula for odd $n = 2m+1$ (§237):
$$n\csc nz = \csc z + \csc\!\Bigl(\frac{\pi}{n}-z\Bigr) - \csc\!\Bigl(\frac{\pi}{n}+z\Bigr) - \csc\!\Bigl(\frac{2\pi}{n}-z\Bigr) + \csc\!\Bigl(\frac{2\pi}{n}+z\Bigr) + \cdots \pm\csc\!\Bigl(\frac{m\pi}{n}+z\Bigr)$$

(source: chapter14.pdf, §248).

## Cotangent sum (§237)

Dividing the cosecant formula by the matching product formula for $\sin nz$ and differentiating with respect to $z$ (implicitly), or equivalently by reading another Vieta coefficient, Euler also states:

$$\frac{n\cos nz}{\sin nz} = \frac{\cos z}{\sin z} + \frac{\cos(\frac{2\pi}{n}+z)}{\sin(\frac{2\pi}{n}+z)} + \cdots$$

i.e., $n\cot nz = \cot z + \cot\!\bigl(\tfrac{2\pi}{n}+z\bigr) + \cdots$ — a sum of $n$ cotangents (source: chapter14.pdf, §250).

The general formula for odd $n = 2m+1$ (§251):
$$n\cot nz = \cot z - \cot\!\Bigl(\frac{\pi}{n}-z\Bigr) + \cot\!\Bigl(\frac{\pi}{n}+z\Bigr) - \cot\!\Bigl(\frac{2\pi}{n}-z\Bigr) + \cot\!\Bigl(\frac{2\pi}{n}+z\Bigr) - \cdots$$

For even $n = 2m$ (§256):
$$n\cot nz = -\tan z + \cot\!\Bigl(\frac{\pi}{n}-z\Bigr) - \cot\!\Bigl(\frac{\pi}{n}+z\Bigr) + \cot\!\Bigl(\frac{2\pi}{n}-z\Bigr) - \cdots + \cot\!\Bigl(\frac{m\pi}{n}-z\Bigr)$$

(source: chapter14.pdf, §256). The alternating signs arise from $\cot v = -\cot(\pi - v)$.

## Secant sum (§246)

From the cosine polynomial (§243), whose leading coefficient is 1 (the equation begins with 1), applying the same Vieta procedure:

$$\frac{n}{\cos nz} = \frac{1}{\cos z} + \frac{1}{\cos(\frac{2\pi}{n}+z)} + \cdots$$

For odd $n = 2m+1$, the general formula (§246):

$$n\sec nz = \sec\!\Bigl(\frac{m}{n}\pi+z\Bigr) + \sec\!\Bigl(\frac{m}{n}\pi-z\Bigr) - \sec\!\Bigl(\frac{m-1}{n}\pi+z\Bigr) - \cdots \pm\sec z$$

(source: chapter14.pdf, §247). Euler works out examples for $n = 1, 3, 5, 7$ explicitly.

## Tangent and cotangent via De Moivre (§249–§256)

Setting $t = \tan z$ and expanding $(1+ti)^n$ via the binomial theorem:

$$\tan nz = \frac{nt - \binom{n}{3}t^3 + \binom{n}{5}t^5 - \cdots}{1 - \binom{n}{2}t^2 + \binom{n}{4}t^4 - \cdots}$$

(source: chapter14.pdf, §249). For odd $n$, the numerator has degree $n$ and the denominator has degree $n-1$. The $n$ roots of the numerator (when $\tan nz$ is set to a fixed value) are $\tan z, \tan(\frac{\pi}{n}+z), \tan(\frac{2\pi}{n}+z), \ldots$

From the coefficient of the second term (§252, §255), the sum of all $n$ roots is $n\cot nz$ when the equation begins with the constant 1. For odd $n = 2m+1$ (§253):

$$n\tan nz = \tan z - \tan\!\Bigl(\frac{\pi}{n}-z\Bigr) + \tan\!\Bigl(\frac{\pi}{n}+z\Bigr) - \cdots + \tan\!\Bigl(\frac{m\pi}{n}+z\Bigr)$$

For even $n = 2m$ (§255–§256), comparing the highest-power equation with the factored form gives:

$$n\cot nz = -\tan z + \tan\!\Bigl(\frac{\pi}{n}-z\Bigr) - \tan\!\Bigl(\frac{\pi}{n}+z\Bigr) + \cdots + \tan\!\Bigl(\frac{m\pi}{n}-z\Bigr)$$

## Product of tangents (§254, §257)

For odd $n$, the product of all $n$ tangent roots equals $\tan nz$ (source: chapter14.pdf, §254):

$$\tan nz = \tan z\cdot\tan\!\Bigl(\frac{\pi}{n}-z\Bigr)\tan\!\Bigl(\frac{\pi}{n}+z\Bigr)\cdots\tan\!\Bigl(\frac{m\pi}{n}-z\Bigr)\tan\!\Bigl(\frac{m\pi}{n}+z\Bigr)$$

For even $n$, the product of all $n$ tangent roots equals $1$ (§257):

$$1 = \tan z\cdot\tan\!\Bigl(\frac{\pi}{n}-z\Bigr)\tan\!\Bigl(\frac{\pi}{n}+z\Bigr)\cdots$$

because the roots come in complementary pairs $\tan\alpha\cdot\tan(\pi/2 - \alpha) = 1$, so each pair has product $1$ (source: chapter14.pdf, §257).

## Comparison with Chapter 10 (§181–§183)

The [[cotangent-partial-fraction|§181–§183]] formulas express $\pi\cot(\pi\sqrt{a})$ and $\pi/\sin(\pi\sqrt{a})$ as series $\sum_{k} 1/(k^2 - a)$. The Chapter 14 formulas are the *finite-$n$* analogue: $n\cot nz$ as a *finite* sum of $n$ cotangents. As $n \to \infty$ with $nz = \pi z_0$ fixed, each term $\cot(k\pi/n + z)$ contributes $\cot(k\pi/n)$, and the sum converges to the Chapter 10 Mittag-Leffler expansion. Chapter 14 thus provides the finite scaffolding from which Chapter 10's infinite partial fractions emerge as a limit.

## Related pages

- [[multiple-angle-polynomials]]
- [[trig-values-as-roots]]
- [[sine-cosine-factored-products]]
- [[cotangent-partial-fraction]]
- [[de-moivre-formula]]
- [[trig-infinite-products]]
- [[chapter-14-on-the-multiplication-and-division-of-angles]]
- [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series]]
