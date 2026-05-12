# Basel Problem

**Summary**: §167: Euler's celebrated evaluation $\sum_{k=1}^{\infty} 1/k^2 = \pi^2/6$, obtained by combining the [[exponential-infinite-product|sinh infinite product]] with [[newtons-identities|Newton's identities]]. The first solved member of an infinite family of even-zeta values (see [[zeta-at-even-integers]]).

**Sources**: chapter10, chapter15

**Last updated**: 2026-05-11

---

## Statement

$$\boxed{\;1 + \frac{1}{4} + \frac{1}{9} + \frac{1}{16} + \frac{1}{25} + \cdots = \frac{\pi^2}{6}\;}$$

(source: chapter10, §167). The problem of evaluating this sum was posed by Pietro Mengoli in 1644 and resisted Jacob Bernoulli, Johann Bernoulli, Leibniz, and de Moivre for nearly a century, becoming famous as the *Basel problem* after the city where the Bernoullis worked.

## Euler's derivation

Start from the [[exponential-infinite-product|§156 product]]

$$\frac{e^x - e^{-x}}{2} = x\left(1 + \frac{x^2}{1\cdot 2\cdot 3} + \frac{x^4}{1\cdot 2\cdot 3\cdot 4\cdot 5} + \frac{x^6}{1\cdot 2\cdots 7} + \cdots\right) = x\prod_{k=1}^{\infty}\left(1 + \frac{x^2}{k^2\pi^2}\right).$$

Divide by $x$ and substitute $x^2 = \pi^2 z$:

$$1 + \frac{\pi^2 z}{1\cdot 2\cdot 3} + \frac{\pi^4 z^2}{1\cdot 2\cdot 3\cdot 4\cdot 5} + \frac{\pi^6 z^3}{1\cdot 2\cdot 3\cdot 4\cdot 5\cdot 6\cdot 7} + \cdots = (1 + z)\left(1 + \frac{z}{4}\right)\left(1 + \frac{z}{9}\right)\left(1 + \frac{z}{16}\right)\cdots.$$

Now apply [[newtons-identities|the §165 framework]]. The series side has

$$A = \frac{\pi^2}{6},\quad B = \frac{\pi^4}{120},\quad C = \frac{\pi^6}{5040},\quad D = \frac{\pi^8}{362880},\ \ldots$$

The product side has roots $\alpha_k = 1/k^2$ for $k = 1, 2, 3, \ldots$. By [[newtons-identities|§166]],

$$P = \alpha_1 + \alpha_2 + \alpha_3 + \cdots = 1 + \frac{1}{4} + \frac{1}{9} + \frac{1}{16} + \cdots = A = \frac{\pi^2}{6}.$$

Done.

## Why this is striking

A *real-numbers* sum, with no apparent connection to geometry, equals $\pi^2/6$. The appearance of $\pi$ — a number whose [[pi|definition]] is geometric — in the answer to a purely arithmetic question is the kind of cross-domain coincidence that suggests deep structure.

Euler's resolution: $\pi$ appears because the zeros of $\sin z$ are at $z = k\pi$. The series $\sum 1/k^2$ is encoded in the *coefficients* of the power series of $\sin z$ when read against the *zeros* of $\sin z$ via the [[sine-infinite-product|product expansion]]. The $\pi^2/6$ is, finally, a logarithmic derivative phenomenon — Euler is computing the trace of an operator whose spectrum is geometrically determined.

## A second derivation: the sine product directly

Equivalent to the above, but more direct. From the [[sine-infinite-product|sine product]]

$$\sin z = z\prod_{k=1}^{\infty}\left(1 - \frac{z^2}{k^2\pi^2}\right) = z - z\cdot\sum_{k=1}^{\infty}\frac{z^2}{k^2\pi^2} + (\text{higher})$$

and the [[sine-and-cosine-series|power series]]

$$\sin z = z - \frac{z^3}{6} + \frac{z^5}{120} - \cdots,$$

equate coefficients of $z^3$:

$$-\frac{1}{6} = -\sum_{k=1}^{\infty}\frac{1}{k^2\pi^2}\quad\Longrightarrow\quad \sum_{k=1}^{\infty}\frac{1}{k^2} = \frac{\pi^2}{6}.$$

Euler does not state this version explicitly in §167 (he goes through the sinh product and Newton's identities), but it is the same calculation with the imaginary substitution $x \mapsto iz$ already applied; see [[sine-infinite-product]] for the direct one-line argument.

## Higher powers

The same Newton recurrence yields all even-power sums:

$$Q = \sum_{k=1}^{\infty}\frac{1}{k^4} = \frac{\pi^4}{90},\qquad R = \sum_{k=1}^{\infty}\frac{1}{k^6} = \frac{\pi^6}{945},\qquad S = \sum_{k=1}^{\infty}\frac{1}{k^8} = \frac{\pi^8}{9450},$$

$$T = \sum_{k=1}^{\infty}\frac{1}{k^{10}} = \frac{\pi^{10}}{93555},\quad \ldots$$

(source: chapter10, §167). See [[zeta-at-even-integers]] for the systematic table.

## Re-derivation via primes (Chapter 15)

[[chapter-15-on-series-which-arise-from-products|Chapter 15]] gives a second route into $\zeta(2) = \pi^2/6$: the [[euler-product-formula|Euler product]]

$$\frac{\pi^2}{6} = \prod_{p\text{ prime}}\frac{p^2}{p^2-1} = \frac{4}{3}\cdot\frac{9}{8}\cdot\frac{25}{24}\cdot\frac{49}{48}\cdot\frac{121}{120}\cdots$$

Combined with the [[wallis-product|Wallis product]], this yields the [[prime-sign-series-for-pi|§285 catalogue]] of identities for $\pi/2$, $\pi/4$, etc. as prime-only ratios. Logarithmically, the formula feeds the §278 transposition that produces the [[divergence-of-prime-reciprocals|divergence of $\sum 1/p$]].

## Modern footnote

In modern notation $\sum 1/k^2 = \zeta(2)$, where $\zeta(s) = \sum_{n\ge 1} n^{-s}$ is the **Riemann zeta function**. Euler's result is the first nontrivial value: $\zeta(2) = \pi^2/6$. He later evaluates $\zeta(2k)$ for every positive integer $k$ — see [[zeta-at-even-integers]] — but $\zeta(2k+1)$ for odd indices remains, in 2026 as in Euler's day, almost completely opaque. Apéry showed in 1978 that $\zeta(3)$ is irrational; nothing comparable is known for $\zeta(5), \zeta(7), \ldots$.

The lacuna at odd indices is precisely the gap left by Euler's method: his factorization argument applies to functions whose zeros generate a *geometric* progression in arclength (e.g. $\sin z$ at $k\pi$), and there is no comparable "closed-form" function whose squared-zero sum is $\zeta(3)$.

## Related pages

- [[zeta-at-even-integers]]
- [[odd-and-alternating-zeta-decomposition]]
- [[newtons-identities]]
- [[sine-infinite-product]]
- [[exponential-infinite-product]]
- [[sine-and-cosine-series]]
- [[pi]]
- [[chapter-9-on-trinomial-factors]]
- [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series]]
- [[chapter-15-on-series-which-arise-from-products]]
- [[euler-product-formula]]
- [[divergence-of-prime-reciprocals]]
- [[prime-sign-series-for-pi]]
