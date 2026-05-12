# Linear Factors of Sine and Cosine at Rational Angles

**Summary**: §184: evaluating the [[sine-infinite-product|§158 sine]] and [[cosine-infinite-product|cosine]] products at $z = m\pi/(2n)$ rationalizes every quadratic factor $1 - m^2/(kn)^2$ into a pair of linear factors $(kn - m)/kn$ and $(kn + m)/kn$. The result is two linear-factor product expressions for each of $\sin(m\pi/2n)$ and $\cos(m\pi/2n)$ — one direct, one via the co-function identity. This is the engine behind the [[wallis-product|Wallis product]], the [[trig-infinite-products|other trig products]], and the [[log-pi-via-products|log-$\pi$]] / [[log-sine-via-products|log-sine]] computations of Chapter 11.

**Sources**: chapter11

**Last updated**: 2026-05-01

---

## The setup

Recall the §158 products:

$$\sin z = z\prod_{k=1}^{\infty}\left(1 - \frac{z^2}{k^2\pi^2}\right),\qquad \cos z = \prod_{k=0}^{\infty}\left(1 - \frac{4z^2}{(2k+1)^2\pi^2}\right).$$

Substitute $z = m\pi/n$ in the sine product and $z = m\pi/(2n)$ in the cosine product (the factor of two cancels the $4$):

$$\sin\frac{m\pi}{n} = \frac{m\pi}{n}\left(1 - \frac{m^2}{n^2}\right)\!\left(1 - \frac{m^2}{4n^2}\right)\!\left(1 - \frac{m^2}{9n^2}\right)\cdots$$

$$\cos\frac{m\pi}{n} = \left(1 - \frac{4m^2}{n^2}\right)\!\left(1 - \frac{4m^2}{9n^2}\right)\!\left(1 - \frac{4m^2}{25n^2}\right)\cdots$$

Substituting $2n$ for $n$ — i.e. starting from arc $m\pi/(2n)$ instead of $m\pi/n$ — gives expressions with denominators $4n^2, 16n^2, 36n^2, \ldots$ in the sine, and $n^2, 9n^2, 25n^2, \ldots$ in the cosine. Each numerator $4k^2 n^2 - m^2$ or $(2k+1)^2 n^2 - m^2$ is a difference of squares, so factors as $(2kn - m)(2kn + m)$ or $((2k+1)n - m)((2k+1)n + m)$.

## The four products of §184

Cleaning up the bookkeeping yields the **first** pair (source: chapter11, §184):

$$\boxed{\;\sin\frac{m\pi}{2n} = \frac{m\pi}{2n}\cdot\frac{2n - m}{2n}\cdot\frac{2n + m}{2n}\cdot\frac{4n - m}{4n}\cdot\frac{4n + m}{4n}\cdot\frac{6n - m}{6n}\cdot\frac{6n + m}{6n}\cdots\;}$$

$$\boxed{\;\cos\frac{m\pi}{2n} = \frac{n - m}{n}\cdot\frac{n + m}{n}\cdot\frac{3n - m}{3n}\cdot\frac{3n + m}{3n}\cdot\frac{5n - m}{5n}\cdot\frac{5n + m}{5n}\cdots\;}$$

Each factor is a rational number (assuming $m, n$ are integers) close to $1$ for large index, and the convergence is geometric in $1/k^2$.

## The co-function identity gives a second pair

Use $\sin((n - m)\pi/2n) = \cos(m\pi/2n)$, valid because $(n-m)\pi/(2n) + m\pi/(2n) = \pi/2$ (sine and cosine are co-functions across the right angle, [[trigonometric-addition-formulas|§128]]). Apply the *sine* boxed formula above with $m \mapsto n - m$ and read off the result for $\cos(m\pi/2n)$:

$$\cos\frac{m\pi}{2n} = \frac{(n - m)\pi}{2n}\cdot\frac{n + m}{2n}\cdot\frac{3n - m}{2n}\cdot\frac{3n + m}{4n}\cdot\frac{5n - m}{4n}\cdot\frac{5n + m}{6n}\cdot\frac{7n - m}{6n}\cdots$$

(source: chapter11, §184, after the substitution $m \mapsto n - m$.)

Symmetrically, $\cos((n - m)\pi/2n) = \sin(m\pi/2n)$, so applying the cosine boxed formula with $m \mapsto n - m$ gives

$$\sin\frac{m\pi}{2n} = \frac{m}{n}\cdot\frac{2n - m}{3n}\cdot\frac{2n + m}{3n}\cdot\frac{4n - m}{5n}\cdot\frac{4n + m}{5n}\cdot\frac{6n - m}{7n}\cdot\frac{6n + m}{7n}\cdots$$

So each of $\sin(m\pi/2n)$ and $\cos(m\pi/2n)$ has *two* infinite product representations. The redundancy is the source of every result in the rest of [[chapter-11-on-other-infinite-expressions-for-arcs-and-sines|Chapter 11]].

## Where the linear factors come from

The §158 quadratic factor $1 - z^2/k^2\pi^2$ at $z = m\pi/(2n)$ becomes

$$1 - \frac{m^2}{4k^2 n^2} = \frac{4k^2 n^2 - m^2}{4k^2 n^2} = \frac{(2kn - m)(2kn + m)}{(2kn)^2} = \frac{2kn - m}{2kn}\cdot\frac{2kn + m}{2kn}.$$

Each $1 - z^2/k^2\pi^2$ contributes two adjacent factors to the resulting product. The same algebra works for the cosine quadratic at $z = m\pi/(2n)$, with $2k$ replaced by $2k+1$. The whole maneuver is just "rationalize the §158 products at rational angles" — but doing so doubles the number of factors and exhibits each factor as the simplest possible rational number, which is exactly the form needed for the upcoming applications.

## What the four products are good for

| Use | Reference |
| --- | --- |
| Comparing two expressions for $\cos(m\pi/2n)$ → [[wallis-product|Wallis product]] for $\pi/2$ | §185 |
| Quotient of expressions for $\sin$ and $\cos$ → infinite products for $\tan$, $\cot$, $\sec$, $\csc$ | §186 |
| Replacing $m$ with $k$ → product for the ratio $\sin(m\pi/2n)/\sin(k\pi/2n)$ | §187 |
| $\log$ of the products + transposition → [[log-pi-via-products|series for $\log\pi$]] | §188–§190 |
| Same on sine/cosine → [[log-sine-via-products|series for $\log\sin$, $\log\cos$]] | §191–§196 |

## Why the rationalization matters

The §158 products are valid for all complex $z$ but are awkward for *numerical* work because each factor $1 - z^2/k^2\pi^2$ involves $\pi^2$ — and computing $\pi^2$ is the very problem one is trying to solve. Restricting to rational angles eliminates $\pi$ from every factor: each entry in the §184 products is a fraction like $(2n - m)/(2n)$ with integer numerator and denominator. Logarithms of such fractions can be looked up in [[characteristic-and-mantissa|standard tables]], and that is the door Euler walks through in §188–§198 to compute logs of $\pi$ and of trig functions to twenty-plus decimal digits.

## Related pages

- [[sine-infinite-product]]
- [[cosine-infinite-product]]
- [[wallis-product]]
- [[trig-infinite-products]]
- [[log-pi-via-products]]
- [[log-sine-via-products]]
- [[trigonometric-addition-formulas]]
- [[chapter-11-on-other-infinite-expressions-for-arcs-and-sines]]
