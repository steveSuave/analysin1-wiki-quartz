# Cosine Infinite Product

**Summary**: §158: $\cos z = \prod_{k=0}^{\infty}\bigl(1 - 4z^2/(2k+1)^2\pi^2\bigr)$. The infinite-product representation of cosine, dual to [[sine-infinite-product|the sine product]] and obtained by substituting $x = iz$ in the [[exponential-infinite-product|hyperbolic-cosine product]].

**Sources**: chapter9

**Last updated**: 2026-04-29

---

## Statement

$$\boxed{\;\cos z = \prod_{k=0}^{\infty}\left(1 - \frac{4z^2}{(2k+1)^2\pi^2}\right) = \left(1 - \frac{4z^2}{\pi^2}\right)\left(1 - \frac{4z^2}{9\pi^2}\right)\left(1 - \frac{4z^2}{25\pi^2}\right)\cdots\;}$$

Equivalently, splitting each quadratic factor into linear factors,

$$\cos z = \left(1 - \frac{2z}{\pi}\right)\left(1 + \frac{2z}{\pi}\right)\left(1 - \frac{2z}{3\pi}\right)\left(1 + \frac{2z}{3\pi}\right)\left(1 - \frac{2z}{5\pi}\right)\left(1 + \frac{2z}{5\pi}\right)\cdots$$

(source: chapter9, §158).

## Derivation

By [[eulers-formula]], $\cos z = (e^{iz} + e^{-iz})/2$. Set $x = iz$ in the [[exponential-infinite-product|§157 formula]]

$$\frac{e^x + e^{-x}}{2} = \prod_{k=0}^{\infty}\left(1 + \frac{4x^2}{(2k+1)^2\pi^2}\right).$$

The left-hand side becomes $(e^{iz} + e^{-iz})/2 = \cos z$, and $x^2 = -z^2$ in each factor.

## Zeros of $\cos z$

$\cos z = 0$ iff $z = \pm(2k+1)\pi/2$ for $k = 0, 1, 2, \ldots$. The product exhibits exactly these zeros: the factor $1 - 4z^2/(2k+1)^2\pi^2 = 0$ when $z = \pm(2k+1)\pi/2$. Euler:

> From this it again becomes obvious that when $z = \pm(2k+1)\pi/2$, then $\cos z = 0$, which is clear from the nature of the circle.

(source: chapter9, §158).

## Compare with the power series

[[sine-and-cosine-series|§134]] gave $\cos z = 1 - z^2/2! + z^4/4! - \cdots$. Equating the coefficient of $z^2$ on both sides:

$$-\frac{1}{2!} = -\sum_{k=0}^{\infty}\frac{4}{(2k+1)^2\pi^2} = -\frac{4}{\pi^2}\sum_{k=0}^{\infty}\frac{1}{(2k+1)^2}.$$

Hence

$$\sum_{k=0}^{\infty}\frac{1}{(2k+1)^2} = \frac{\pi^2}{8},$$

the sum of reciprocals of odd squares. Together with $\sum_{k=1}^{\infty} 1/k^2 = \pi^2/6$ from [[sine-infinite-product|the sine product]] this gives $\sum_{\text{even}} 1/k^2 = \pi^2/24$, i.e. $\frac{1}{4}\sum 1/k^2$, an internal consistency check.

## A unified picture

The two products together give

$$\frac{\sin z}{z} = \prod_{k=1}^{\infty}\left(1 - \frac{z^2}{k^2\pi^2}\right),\qquad \cos z = \prod_{k=0}^{\infty}\left(1 - \frac{4z^2}{(2k+1)^2\pi^2}\right).$$

Multiplying them and using $\sin 2z = 2\sin z\cos z$:

$$\frac{\sin 2z}{2z} = \prod_{k=1}^{\infty}\left(1 - \frac{(2z)^2}{k^2\pi^2}\right) = \prod_{k=1}^{\infty}\left(1 - \frac{4z^2}{k^2\pi^2}\right).$$

So the right-hand product splits into the even-$k$ part (giving $\sin z/z$ at argument $z$, that is the $k = 2m$ terms become $1 - z^2/m^2\pi^2$) and the odd-$k$ part (giving $\cos z$). This is the duplication formula in product form.

## Related pages

- [[sine-infinite-product]]
- [[exponential-infinite-product]]
- [[trinomial-factor]]
- [[factorization-of-an-plus-minus-zn]]
- [[sine-and-cosine-series]]
- [[eulers-formula]]
- [[pi]]
- [[newtons-identities]]
- [[zeta-at-even-integers]]
- [[odd-and-alternating-zeta-decomposition]]
- [[cotangent-partial-fraction]]
- [[linear-factors-of-sine-cosine]]
- [[wallis-product]]
- [[chapter-9-on-trinomial-factors]]
- [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series]]
- [[chapter-11-on-other-infinite-expressions-for-arcs-and-sines]]
