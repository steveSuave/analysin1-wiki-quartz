# Chapter 15 — On Series Which Arise From Products

**Summary**: §264–§296. Euler develops the duality between an infinite product $\prod(1\pm\alpha_i z)^{\pm 1}$ and the series obtained by multiplying it out. When the $\alpha_i$ range over the primes (or reciprocals of prime powers), the resulting series have number-theoretic meaning: squarefree numbers, all natural numbers, Möbius-style sign patterns. The central result is the **Euler product formula** $\zeta(n) = \prod_p (1-1/p^n)^{-1}$ (§274, §283), and its most famous consequence — the divergence of $\sum 1/p$ obtained by taking logarithms at $n=1$ (§279). The chapter closes with a vast catalogue of series for $\pi/4$, $\pi/2$, $\pi/(2\sqrt 2)$, $\pi/(3\sqrt 3)$ etc. expressed as signed sums or products over primes classified mod 4, mod 6, mod 8 (§285–§296).

**Sources**: chapter15.pdf

**Last updated**: 2026-05-11

---

## Movement 1 — Products as symmetric-coefficient series (§264–§269)

For any (finite or infinite) product of linear factors

$$(1+\alpha z)(1+\beta z)(1+\gamma z)(1+\delta z)\cdots = 1 + Az + Bz^2 + Cz^3 + \cdots,$$

the coefficient $A$ is the sum of the $\alpha_i$, $B$ the sum of products taken two at a time, $C$ three at a time, etc. — the **elementary symmetric polynomials** in the $\alpha_i$ (source: chapter15.pdf, §264). The two specialisations $z = 1$ and $z = -1$ collapse the polynomial coefficients into single signed series (§265–§266).

Letting the $\alpha_i$ range over the primes $2, 3, 5, 7, 11, \ldots$ gives a series listing the squarefree natural numbers; with $\alpha_i = 1/p^n$ the series is $\sum_k 1/k^n$ over squarefree $k$, and with negative factors $(1-1/p^n)$ the signs become **Möbius-style**, depending on the parity of the number of prime factors. See [[squarefree-and-mobius-series]].

## Movement 2 — Inverse products and the Euler product formula (§270–§277)

The reciprocal product

$$\frac{1}{(1-\alpha z)(1-\beta z)(1-\gamma z)\cdots} = 1 + Az + Bz^2 + \cdots$$

now allows each $\alpha_i$ to repeat: $B$ is the sum of products of two factors not necessarily distinct, and so on (§270). At $z = 1$ this is the sum over **all** products of the $\alpha_i$ with repetition (§271).

With $\alpha_i = 1/p$ ranging over the primes, unique factorization of integers gives the **harmonic series** (§273):

$$\frac{1}{(1-\tfrac12)(1-\tfrac13)(1-\tfrac15)(1-\tfrac17)\cdots} = 1 + \frac12 + \frac13 + \frac14 + \cdots.$$

With $\alpha_i = 1/p^n$ for any $n$ this is the **Euler product formula** (§274):

$$\prod_{p\text{ prime}}\frac{1}{1-1/p^n} = 1 + \frac{1}{2^n} + \frac{1}{3^n} + \frac{1}{4^n} + \cdots.$$

Combined with the §269 product, this yields the reciprocal relation $PQ = 1$ (§275): the product $\prod(1-1/p^n)$ and the Möbius series sum to $1/\zeta(n)$. See [[euler-product-formula]].

## Movement 3 — Logarithms: divergence of $\sum 1/p$ (§278–§282)

Taking the natural log of the Euler product and applying the [[logarithmic-series|§118 series]] to each factor yields

$$\log M = \sum_{k=1}^{\infty}\frac{1}{k}\left(\frac{1}{2^{kn}} + \frac{1}{3^{kn}} + \frac{1}{5^{kn}} + \frac{1}{7^{kn}} + \cdots\right),$$

a double sum that **transposes** $\log\zeta(n)$ into a series in prime power sums (§278). At $n=1$ the left side is $\log\log\infty$ but every inner sum except the first is finite, forcing $\sum 1/p = \infty$ (§279). See [[divergence-of-prime-reciprocals]].

At even $n$ the same identity expresses $\log(\pi^{2k}/\text{rational})$ as a convergent double sum, and Euler tabulates $S(n) = \sum_p 1/p^n$ to 12 decimal places for $n = 2, 4, 6, \ldots, 36$ (§281–§282). See [[prime-zeta-values]].

## Movement 4 — Sieve derivation of the Euler product (§283–§284)

Independently of Movement 2, §283 derives the Euler product by an **Eratosthenes-style sieve** on the series itself. Starting from $A = \sum 1/k^n$, one subtracts $A/2^n$ to remove even-index terms, then $B/3^n$ to remove multiples of 3, then $C/5^n$, and so on; at the end only the term 1 survives, giving

$$A\,(1-\tfrac{1}{2^n})(1-\tfrac{1}{3^n})(1-\tfrac{1}{5^n})\cdots = 1.$$

The same technique applied in §284 to the alternating odd-denominator series $A = 1 - 1/3^n + 1/5^n - \cdots$ (which equals $\pi/4$ at $n = 1$, by [[arctangent-series|Leibniz]]) sieves out by primes with **signs determined by class mod 4**: primes of the form $4m-1$ contribute $(1+1/p^n)$, primes of the form $4m+1$ contribute $(1-1/p^n)$.

## Movement 5 — Prime-signed series for $\pi$ (§285–§296)

The §284 product expression for $\pi/4$, together with the [[basel-problem|Basel-problem]] product expression for $\pi^2/6$, opens a long catalogue:

- §285–§286: $\pi/4 = \prod_p p/(p\pm 1)$, $\pi/2 = \prod_p p/p^*$, ratios giving prime-only Wallis-style products, and the comparison with [[wallis-product|Wallis]].
- §287: cubic analogue $\pi^3/32 = \prod_p p^3/(p^3\pm 1)$.
- §288–§289: multiplying by individual factors converts a product over **odd** primes into one over **all** primes, yielding $\pi/6 = 1 - 1/2 - 1/3 + \cdots$, $\pi/2 = 1 + 1/2 - 1/3 - \cdots$, etc., with composite signs given multiplicatively.
- §290–§291: similar manipulations give series summing to $3\pi/2$, $0$, and infinity; in general, finite changes to the prime-sign pattern produce 0 if cofinitely many primes are negative and $\infty$ if cofinitely many are positive.
- §292–§294: applying the sieve to the §176 character series with **mod 6** classification yields $\pi/(3\sqrt 3) = \prod p^n/(p^n\pm 1)$ with sign by class mod 6.
- §295: applying the sieve to the §179 series gives $\pi/(2\sqrt 2)$ products and series with signs by class **mod 8**.
- §296: Euler signals that the catalogue is unbounded — the same machinery applied to any of the §171–§180 character series gives a corresponding prime-classified product.

See [[prime-sign-series-for-pi]] for the full taxonomy and worked examples.

## Significance

This chapter is the analytic-number-theory pivot of the *Introductio*. It introduces:

- The **Euler product formula** $\zeta(s) = \prod (1-p^{-s})^{-1}$, the foundational identity that lets one read primes off the zeta function.
- The **divergence of $\sum 1/p$**, the first proof that primes are "denser than squares" — a sharpening of Euclid's theorem that there are infinitely many primes.
- A wealth of **prime-classified series** that are modern Dirichlet $L$-functions in disguise: the §284 product is $L(1,\chi_4) = \pi/4$ in its Euler-product form; the §294 product is $L(1,\chi_6)$; §295 is $L(1,\chi_8)$.

The next chapter (Chapter 16) turns from products to additive representations: partitions of integers.

## Related pages

- [[euler-product-formula]]
- [[squarefree-and-mobius-series]]
- [[divergence-of-prime-reciprocals]]
- [[prime-zeta-values]]
- [[prime-sign-series-for-pi]]
- [[basel-problem]]
- [[zeta-at-even-integers]]
- [[arctangent-series]]
- [[circular-arc-series]]
- [[logarithmic-series]]
- [[wallis-product]]
