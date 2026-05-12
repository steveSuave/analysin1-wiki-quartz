# Circular-Arc Series

**Summary**: §171–§180: applying [[newtons-identities|Newton's identities]] to the [[chapter-9-on-trinomial-factors|§164]] arc-form products $\cos(v/2) + \tan(g/2)\sin(v/2)$ and $\cos(v/2) + \cot(g/2)\sin(v/2)$ produces a vast family of closed-form series in which the denominators run over arithmetic progressions modulo $n$, with sign patterns coming from the elementary-symmetric structure. Special cases recover Leibniz's $\pi/4$ series and many of its $\sqrt 2$, $\sqrt 3$ analogues.

**Sources**: chapter10.pdf

**Last updated**: 2026-05-11

---

## The master products

From [[chapter-9-on-trinomial-factors|§164]],

$$\cos\frac{v}{2} + \tan\frac{g}{2}\sin\frac{v}{2} = \left(1 + \frac{v}{\pi - g}\right)\left(1 - \frac{v}{\pi + g}\right)\left(1 + \frac{v}{3\pi - g}\right)\left(1 - \frac{v}{3\pi + g}\right)\left(1 + \frac{v}{5\pi - g}\right)\cdots$$

(source: chapter10.pdf, §171). Substituting $v = \pi x/n$, $g = m\pi/n$:

$$\left(1 + \frac{x}{n - m}\right)\left(1 - \frac{x}{n + m}\right)\left(1 + \frac{x}{3n - m}\right)\left(1 - \frac{x}{3n + m}\right)\cdots = \cos\frac{\pi x}{2n} + \tan\frac{m\pi}{2n}\sin\frac{\pi x}{2n}.$$

Expanding the right side as a power series in $x$:

$$= 1 + \frac{\pi x}{2n}\tan\frac{m\pi}{2n} - \frac{\pi^2 x^2}{2\cdot 4\,n^2} - \frac{\pi^3 x^3}{2\cdot 4\cdot 6\,n^3}\tan\frac{m\pi}{2n} + \frac{\pi^4 x^4}{2\cdot 4\cdot 6\cdot 8\,n^4} + \cdots,$$

so the [[newtons-identities|elementary symmetric coefficients]] of the product are

$$A = \frac{\pi}{2n}\tan\frac{m\pi}{2n},\quad B = \frac{-\pi^2}{2\cdot 4\,n^2},\quad C = \frac{-\pi^3}{2\cdot 4\cdot 6\,n^3}\tan\frac{m\pi}{2n},\quad D = \frac{\pi^4}{2\cdot 4\cdot 6\cdot 8\,n^4},\ \ldots$$

(source: chapter10.pdf, §171). The roots — read off the linear factors — are

$$\alpha = \frac{1}{n-m},\ \beta = -\frac{1}{n+m},\ \gamma = \frac{1}{3n-m},\ \delta = -\frac{1}{3n+m},\ \epsilon = \frac{1}{5n-m},\ \ldots$$

(source: chapter10.pdf, §171), with the alternating sign pattern.

## The power sums

Apply [[newtons-identities|Newton's recurrence]] to obtain $P, Q, R, S, T, V$. With $k = \tan(m\pi/2n)$ for brevity:

$$P = \frac{1}{n-m} - \frac{1}{n+m} + \frac{1}{3n-m} - \frac{1}{3n+m} + \cdots = \frac{\pi k}{2n},$$

$$Q = \frac{1}{(n-m)^2} + \frac{1}{(n+m)^2} + \frac{1}{(3n-m)^2} + \frac{1}{(3n+m)^2} + \cdots = \frac{(k^2 + 1)\pi^2}{4n^2},$$

$$R = \frac{1}{(n-m)^3} - \frac{1}{(n+m)^3} + \frac{1}{(3n-m)^3} - \cdots = \frac{(k^3 + k)\pi^3}{8n^3},$$

$$S = \frac{(3k^4 + 4k^2 + 1)\pi^4}{48n^4},\quad T = \frac{(3k^5 + 5k^3 + 2k)\pi^5}{96n^5}$$

(source: chapter10.pdf, §172). The pattern: even-power sums are positive (each term squared); odd-power sums are alternating, with the alternation matching the sign-pattern of the roots.

## The cot-variant

The §173 partner

$$\cos\frac{v}{2} + \cot\frac{g}{2}\sin\frac{v}{2} = \left(1 + \frac{v}{g}\right)\left(1 - \frac{v}{2\pi - g}\right)\left(1 + \frac{v}{2\pi + g}\right)\left(1 - \frac{v}{4\pi - g}\right)\cdots$$

with the same substitution $v = \pi x/n$, $g = m\pi/n$, gives an analogous family with roots

$$\alpha = \frac{1}{m},\ \beta = -\frac{1}{2n - m},\ \gamma = \frac{1}{2n + m},\ \delta = -\frac{1}{4n - m},\ \epsilon = \frac{1}{4n + m},\ \ldots$$

and

$$P = \frac{1}{m} - \frac{1}{2n-m} + \frac{1}{2n+m} - \frac{1}{4n-m} + \cdots = \frac{\pi}{2nk}$$

(source: chapter10.pdf, §173–§174), and so on for $Q, R, S, T, V$.

## Special values

### $m = 1$, $n = 2$ (§175): the Leibniz series and friends

Here $k = \tan(\pi/4) = 1$, the §172 and §174 series coincide, and:

$$\frac{\pi}{4} = 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \frac{1}{9} - \cdots,$$

$$\frac{\pi^2}{8} = 1 + \frac{1}{3^2} + \frac{1}{5^2} + \frac{1}{7^2} + \frac{1}{9^2} + \cdots,$$

$$\frac{\pi^3}{32} = 1 - \frac{1}{3^3} + \frac{1}{5^3} - \frac{1}{7^3} + \cdots,$$

$$\frac{\pi^4}{96} = 1 + \frac{1}{3^4} + \frac{1}{5^4} + \frac{1}{7^4} + \cdots,\quad\frac{\pi^6}{960} = 1 + \frac{1}{3^6} + \frac{1}{5^6} + \cdots$$

(source: chapter10.pdf, §175). Euler observes: even-exponent series were already obtained in §169 ([[zeta-at-even-integers|cosh product]]); the odd-exponent alternating series

$$1 - \frac{1}{3^{2n+1}} + \frac{1}{5^{2n+1}} - \frac{1}{7^{2n+1}} + \cdots$$

are seen here for the first time. Each equals a rational multiple of $\pi^{2n+1}$.

### $m = 1$, $n = 3$ (§176): $\sqrt 3$ series

Here $k = \tan(\pi/6) = 1/\sqrt 3$:

$$\frac{\pi}{6\sqrt 3} = \frac{1}{2} - \frac{1}{4} + \frac{1}{8} - \frac{1}{10} + \frac{1}{14} - \frac{1}{16} + \cdots,$$

$$\frac{\pi^2}{27} = \frac{1}{2^2} + \frac{1}{4^2} + \frac{1}{8^2} + \frac{1}{10^2} + \frac{1}{14^2} + \cdots,$$

$$\frac{\pi}{3\sqrt 3} = 1 - \frac{1}{2} + \frac{1}{4} - \frac{1}{5} + \frac{1}{7} - \frac{1}{8} + \cdots$$

(source: chapter10.pdf, §176). The pattern of denominators: integers not divisible by 3, with alternating sign.

### $m = 1$, $n = 4$ and $n = 8$ (§179)

$k = \tan(\pi/8) = \sqrt{2} - 1$, etc. After algebra:

$$\frac{\pi}{2\sqrt 2} = 1 + \frac{1}{3} - \frac{1}{5} - \frac{1}{7} + \frac{1}{9} + \frac{1}{11} - \frac{1}{13} - \cdots\quad(n = 4),$$

$$\frac{\pi}{4\,(2 - \sqrt 2)^{1/2}} = 1 + \frac{1}{7} - \frac{1}{9} - \frac{1}{15} + \frac{1}{17} + \cdots\quad(n = 8).$$

(source: chapter10.pdf, §179). §180 extracts further combinations; the sign patterns become genuinely intricate. Euler comments that one "could let $n = 16$ and $m = 1, 3, 5,$ or $7$ which would show the sums of series in which the terms are $1, 1/3, 1/5, 1/7, \ldots$ and in which the various changes of positive and negative signs are different from those already seen" (source: chapter10.pdf, §180) — i.e. the technique generates an unlimited supply of "character sums" in modern terminology.

## Modern footnote: Dirichlet $L$-values

The series above are exactly the values

$$L(\chi, n) = \sum_{k\ge 1}\frac{\chi(k)}{k^n}$$

for a Dirichlet character $\chi$ mod $4n$ (or a divisor thereof) at positive integer $s = n$. Specifically:

- $\pi/4 = L(\chi_4, 1)$ for the non-trivial character mod $4$.
- $\pi/(2\sqrt 2) = L(\chi_8, 1)$ for the real quadratic character mod $8$.
- $\pi/(3\sqrt 3) = L(\chi, 1)$ for one of the characters mod $12$.

The general phenomenon — that $L(\chi, n)\in\overline{\mathbb Q}\cdot\pi^n$ when $\chi$ is even and $n$ even (or $\chi$ odd and $n$ odd) — is the **functional equation for Dirichlet L-functions**. Euler is computing case-by-case examples of a uniform structural theorem first proved by Hurwitz a century later.

## Related pages

- [[newtons-identities]]
- [[basel-problem]]
- [[zeta-at-even-integers]]
- [[odd-and-alternating-zeta-decomposition]]
- [[arctangent-series]]
- [[cotangent-partial-fraction]]
- [[sine-infinite-product]]
- [[cosine-infinite-product]]
- [[chapter-9-on-trinomial-factors]]
- [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series]]
- [[chapter-15-on-series-which-arise-from-products]]
- [[prime-sign-series-for-pi]]
- [[euler-product-formula]]
