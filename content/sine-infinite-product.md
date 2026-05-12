# Sine Infinite Product

**Summary**: §158: $\sin z = z\prod_{k=1}^{\infty}\bigl(1 - z^2/k^2\pi^2\bigr)$. Euler's celebrated infinite-product representation of the sine, obtained by substituting $x = iz$ in the [[exponential-infinite-product|hyperbolic-sine product]].

**Sources**: chapter9

**Last updated**: 2026-04-29

---

## Statement

$$\boxed{\;\sin z = z\prod_{k=1}^{\infty}\left(1 - \frac{z^2}{k^2\pi^2}\right) = z\left(1 - \frac{z^2}{\pi^2}\right)\left(1 - \frac{z^2}{4\pi^2}\right)\left(1 - \frac{z^2}{9\pi^2}\right)\cdots\;}$$

Equivalently, factoring each $1 - z^2/k^2\pi^2 = (1 - z/k\pi)(1 + z/k\pi)$,

$$\sin z = z\left(1 - \frac{z}{\pi}\right)\left(1 + \frac{z}{\pi}\right)\left(1 - \frac{z}{2\pi}\right)\left(1 + \frac{z}{2\pi}\right)\left(1 - \frac{z}{3\pi}\right)\left(1 + \frac{z}{3\pi}\right)\cdots$$

(source: chapter9, §158).

## Derivation

By [[eulers-formula]], $\sin z = (e^{iz} - e^{-iz})/(2i)$. Set $x = iz$ in the [[exponential-infinite-product|§156 formula]]

$$\frac{e^x - e^{-x}}{2} = x\prod_{k=1}^{\infty}\left(1 + \frac{x^2}{k^2\pi^2}\right).$$

The left-hand side becomes $(e^{iz} - e^{-iz})/2 = i\sin z$, and $x = iz$ gives leading factor $iz$ and replaces $x^2 = -z^2$ in each product term. Dividing both sides by $i$:

$$\sin z = z\prod_{k=1}^{\infty}\left(1 - \frac{z^2}{k^2\pi^2}\right).$$

## How the zeros encode the function

$\sin z = 0$ iff $z = k\pi$ for some integer $k$ (positive, negative, or zero). The product exhibits this directly: the leading $z$ vanishes at $z = 0$, and the factor $(1 - z^2/k^2\pi^2)$ vanishes at $z = \pm k\pi$. Every zero of $\sin z$ is accounted for, with the right multiplicity.

Compare the [[sine-and-cosine-series|power series]]

$$\sin z = z - \frac{z^3}{3!} + \frac{z^5}{5!} - \cdots$$

The series side encodes the *behavior near $0$*; the product side encodes the *zeros everywhere on $\mathbb{R}$*. Euler's analytical philosophy — every transcendental function is the limit of a polynomial — makes both representations available.

## Vanishing condition

"Whenever the arc has a length such that any of the factors vanishes, that is when $z = 0$, $\pm \pi$, $\pm 2\pi$, etc., or generally when $z = \pm k\pi$, where $k$ is any integer, then the sine of that arc must equal zero. But this is so obvious, that we might have found the factors from this fact" (source: chapter9, §158). Reading backwards: knowing the zeros suffices to write down the product.

## Why this matters

This is the formula that underlies Euler's solution of the **Basel problem**: $\sum_{k=1}^{\infty} 1/k^2 = \pi^2/6$. Sketch: equate the coefficient of $z^3$ in the power series $\sin z = z - z^3/6 + \cdots$ with the coefficient of $z^3$ obtained by expanding the product. From the product, the $z^3$ coefficient is $-z\sum 1/k^2\pi^2$, hence

$$-\frac{1}{3!} = -\sum_{k=1}^{\infty}\frac{1}{k^2\pi^2}\quad\Longrightarrow\quad \sum_{k=1}^{\infty}\frac{1}{k^2} = \frac{\pi^2}{6}.$$

Higher-order sums $\sum 1/k^4 = \pi^4/90$, etc., follow from comparing higher coefficients. Euler develops these in [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series|Chapter 10]] of the *Introductio* via [[newtons-identities|Newton's identities]] (see [[basel-problem]] and [[zeta-at-even-integers]]).

The same idea (compare power-series coefficients with elementary symmetric polynomials of the reciprocal roots) generalizes to $\cos z$ via [[cosine-infinite-product]], and to many further functions whose zero set is known.

## Modern footnote

Euler's derivation manipulates infinite products as if they were finite, with no convergence checks. The formula nonetheless turns out to be true, and the rigorous version is a special case of the **Weierstrass factorization theorem** for entire functions of order $1$. Euler's instinct that "function = polynomial whose zeros we list" is the origin of that whole branch of complex analysis.

## Related pages

- [[cosine-infinite-product]]
- [[exponential-infinite-product]]
- [[trinomial-factor]]
- [[factorization-of-an-plus-minus-zn]]
- [[sine-and-cosine-series]]
- [[eulers-formula]]
- [[pi]]
- [[newtons-identities]]
- [[basel-problem]]
- [[zeta-at-even-integers]]
- [[cotangent-partial-fraction]]
- [[linear-factors-of-sine-cosine]]
- [[wallis-product]]
- [[chapter-9-on-trinomial-factors]]
- [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series]]
- [[chapter-11-on-other-infinite-expressions-for-arcs-and-sines]]
