# Zeta at Even Integers

**Summary**: §168: the systematic table of $\zeta(2k) = \sum_{n=1}^{\infty} 1/n^{2k}$ as a rational multiple of $\pi^{2k}$, computed by [[newtons-identities]] from the [[sine-infinite-product|sine product]]. Euler tabulates through $\zeta(26)$ and notes the "extraordinary usefulness" of the irregular rational sequence that appears.

**Sources**: chapter10.pdf, chapter15.pdf

**Last updated**: 2026-05-11

---

## The table

For each positive integer $k$,

$$\sum_{n=1}^{\infty}\frac{1}{n^{2k}} = \frac{2^{2k-2}}{(2k+1)!}\,c_k\,\pi^{2k},$$

where $c_k$ is a positive rational. Euler tabulates the first thirteen values (source: chapter10.pdf, §168):

| $2k$ | $\sum 1/n^{2k}$ | $c_k$ |
|---|---|---|
| 2  | $\pi^2/6$ | $1$ |
| 4  | $\pi^4/90$ | $1/3$ |
| 6  | $\pi^6/945$ | $1/3$ |
| 8  | $\pi^8/9450$ | $3/5$ |
| 10 | $\pi^{10}/93555$ | $5/3$ |
| 12 | $\frac{691\,\pi^{12}}{638512875}$ | $691/105$ |
| 14 | $\frac{2\,\pi^{14}}{18243225}$ | $35/1$ |
| 16 | $\frac{3617\,\pi^{16}}{325641566250}$ | $3617/15$ |
| 18 | $\frac{43867\,\pi^{18}}{38979295480125}$ | $43867/21$ |
| 20 | $\frac{1222277\,\pi^{20}}{\ldots}$ | $1222277/55$ |
| 22 | $\frac{854513\,\pi^{22}}{\ldots}$ | $854513/3$ |
| 24 | $\frac{1181820455\,\pi^{24}}{\ldots}$ | $1181820455/273$ |
| 26 | $\frac{76977927\,\pi^{26}}{\ldots}$ | $76977927/1$ |

Euler's comment on the $c_k$ sequence: "We could continue with more of these, but we have gone far enough to see a sequence which at first seems quite irregular, $1, 1/3, 1/3, 3/5, 5/3, 691/105, 35/1, \ldots$, but it is of extraordinary usefulness in several places" (source: chapter10.pdf, §168).

## Sums of reciprocal odd squares

The same machinery applied to the [[cosine-infinite-product|cosh product]] (§169) gives

$$\sum_{k=0}^{\infty}\frac{1}{(2k+1)^{2n}}.$$

Setup: from the [[exponential-infinite-product|§157 product]]

$$\frac{e^x + e^{-x}}{2} = 1 + \frac{x^2}{1\cdot 2} + \frac{x^4}{1\cdot 2\cdot 3\cdot 4} + \cdots = \prod_{k=0}^{\infty}\left(1 + \frac{4x^2}{(2k+1)^2\pi^2}\right),$$

substitute $x^2 = \pi^2 z/4$, and read off

$$A = \frac{\pi^2}{1\cdot 2\cdot 4} = \frac{\pi^2}{8},\quad B = \frac{\pi^4}{1\cdot 2\cdot 3\cdot 4\cdot 4^2},\quad C = \frac{\pi^6}{1\cdot 2\cdot\ldots\cdot 6\cdot 4^3},\ \ldots$$

The roots are $\alpha_k = 1/(2k+1)^2$ for $k = 0, 1, 2, \ldots$. By [[newtons-identities|Newton's recurrence]]:

$$P = \sum_{k=0}^{\infty}\frac{1}{(2k+1)^2} = \frac{\pi^2}{8},$$

$$Q = \sum_{k=0}^{\infty}\frac{1}{(2k+1)^4} = \frac{\pi^4}{96},\quad R = \sum_{k=0}^{\infty}\frac{1}{(2k+1)^6} = \frac{\pi^6}{960},$$

and so on. (The full table requires §170's even/odd splits to interleave with the even-zeta values; see [[odd-and-alternating-zeta-decomposition]].)

## The qualitative pattern

Euler observes in §168: *any* infinite series of the form $1 + 1/2^n + 1/3^n + \cdots$ with $n$ even is a rational multiple of $\pi^n$. The same is conjectured true (and remains true today) for every even $n$, and the rational coefficient grows exuberantly: $c_{13} = 76977927$ has eight digits.

The qualitative conclusion: $\zeta(2k)/\pi^{2k}$ is rational for every positive integer $k$.

## Modern footnote: Bernoulli numbers

Euler's $c_k$ are essentially the **Bernoulli numbers**. The modern formula is

$$\zeta(2k) = \frac{(-1)^{k+1}(2\pi)^{2k}}{2\,(2k)!}\,B_{2k},$$

where $B_{2k}$ are the Bernoulli numbers $B_2 = 1/6$, $B_4 = -1/30$, $B_6 = 1/42$, $B_8 = -1/30$, $B_{10} = 5/66$, $B_{12} = -691/2730$, ... Comparing with Euler's parametrization $c_k = 2(2k+1)\,|B_{2k}|$:

$$\zeta(2k) = \frac{2^{2k-2}\,c_k}{(2k+1)!}\,\pi^{2k} = \frac{2^{2k-2}\cdot 2(2k+1)\,|B_{2k}|}{(2k+1)!}\,\pi^{2k} = \frac{2^{2k-1}\,|B_{2k}|}{(2k)!}\,\pi^{2k}.$$

Verification: $c_1 = 2\cdot 3\cdot 1/6 = 1$, $c_2 = 2\cdot 5\cdot 1/30 = 1/3$, $c_3 = 2\cdot 7\cdot 1/42 = 1/3$, $c_4 = 2\cdot 9\cdot 1/30 = 3/5$, $c_6 = 2\cdot 13\cdot 691/2730 = 691/105$. The "irregularity" Euler noticed is the genuine irregularity of the Bernoulli sequence — a sequence whose number-theoretic density (via Kummer's congruences and the Herbrand–Ribet theorem) is one of the central topics of $p$-adic analytic number theory.

The Bernoulli numbers were known to Jakob Bernoulli (in connection with sums of $k$-th powers of consecutive integers) before Euler's *Introductio*, but the link between them and the zeta values is Euler's discovery — recorded here, computed term-by-term in §168 without a closed form. Euler returned to the subject decades later and produced the modern formula; the $\pi^{2k}$ scaling is already evident in the table above.

## What is *not* solved here

The series $\zeta(2k+1)$ at odd indices — $\sum 1/n^3$, $\sum 1/n^5$, $\ldots$ — are conspicuously absent from the table. They cannot be obtained by Euler's method: the [[sine-infinite-product|sine product]] gives even-power sums via the Newton recurrence, never odd-power sums of $1/k$ (the *odd* powers of $\alpha_k = 1/k^2$ are $1/k^{2(\text{odd})} = 1/k^{\text{even}}$, so the recurrence still produces even-zeta values). Apéry (1978) proved $\zeta(3)$ irrational; in 2026 it remains unknown whether $\zeta(3)/\pi^3$ is rational, and similarly for $\zeta(5), \zeta(7), \ldots$.

## Re-derivation via primes (Chapter 15)

The closed-form $\zeta(2k)$ values are also the **inputs** for [[chapter-15-on-series-which-arise-from-products|Chapter 15]]'s [[euler-product-formula|Euler product formula]] $\zeta(2k) = \prod_p (1-1/p^{2k})^{-1}$ and the [[prime-zeta-values|§281 inversion]] that computes $\sum_p 1/p^{2k}$ numerically by bootstrapping from $\log\zeta(2k)$. The §285 prime-only Wallis-style product for $\pi^2/6$ — see [[prime-sign-series-for-pi]] — is the simplest non-trivial consequence.

## Related pages

- [[basel-problem]]
- [[newtons-identities]]
- [[odd-and-alternating-zeta-decomposition]]
- [[sine-infinite-product]]
- [[cosine-infinite-product]]
- [[exponential-infinite-product]]
- [[pi]]
- [[log-pi-via-products]]
- [[log-sine-via-products]]
- [[chapter-10-on-the-use-of-the-discovered-factors-to-sum-infinite-series]]
- [[chapter-11-on-other-infinite-expressions-for-arcs-and-sines]]
- [[chapter-15-on-series-which-arise-from-products]]
- [[euler-product-formula]]
- [[prime-zeta-values]]
- [[prime-sign-series-for-pi]]
