# Euler Product Formula

**Summary**: §270–§277, §283–§284. The identity $\sum_{k=1}^\infty 1/k^n = \prod_p (1-1/p^n)^{-1}$ — a sum over the integers equals a product over the primes. Euler gives two independent derivations: a direct expansion of the reciprocal product using the geometric series and unique factorisation (Movement 2 of [[chapter-15-on-series-which-arise-from-products|Chapter 15]]), and an Eratosthenes-style sieve of the series itself (§283).

**Sources**: chapter15

**Last updated**: 2026-05-11

---

## The identity

For every $n$ for which the sum converges,

$$\sum_{k=1}^{\infty}\frac{1}{k^n} = \prod_{p\text{ prime}}\frac{1}{1-1/p^n} = \prod_{p\text{ prime}}\frac{p^n}{p^n-1}.$$

In Euler's notation (§274), with $P$ for the product and the series fully written out:

$$P = \frac{1}{\bigl(1-\tfrac{1}{2^n}\bigr)\bigl(1-\tfrac{1}{3^n}\bigr)\bigl(1-\tfrac{1}{5^n}\bigr)\bigl(1-\tfrac{1}{7^n}\bigr)\cdots} = 1 + \frac{1}{2^n} + \frac{1}{3^n} + \frac{1}{4^n} + \frac{1}{5^n} + \cdots.$$

Euler notes that "all natural numbers occur with no exception" in the denominators (source: chapter15, §274) — the formula is essentially a restatement of unique factorisation.

## Derivation I — Expansion of the reciprocal product (§270–§274)

Given any factors $\alpha, \beta, \gamma, \delta, \ldots$, the geometric-series expansion of each $1/(1-\alpha_i z)$ followed by multiplication gives

$$\frac{1}{(1-\alpha z)(1-\beta z)(1-\gamma z)\cdots} = 1 + Az + Bz^2 + Cz^3 + \cdots,$$

where $A$ is the sum of the $\alpha_i$, $B$ the sum of products taken two at a time **with repetition allowed**, $C$ three at a time with repetition, etc. (source: chapter15, §270; contrast with §264, where the linear factors $1+\alpha z$ produce only distinct products).

Setting $z = 1$ and $\alpha_i = 1/p_i^n$ over the primes (§274), each entry in the expanded series is

$$\frac{1}{p_1^{n e_1}\,p_2^{n e_2}\,p_3^{n e_3}\cdots} = \frac{1}{(p_1^{e_1}p_2^{e_2}\cdots)^n} = \frac{1}{k^n}$$

for some natural number $k$ with prime factorisation $p_1^{e_1}p_2^{e_2}\cdots$. By unique factorisation each natural number appears **exactly once** as such a product, giving the formula.

The instructive intermediate case (§272) is $\alpha_1 = 1/2$ alone: $1/(1-1/2) = 1 + 1/2 + 1/4 + 1/8 + \cdots$, the powers of $1/2$. Adding $\alpha_2 = 1/3$ gives powers of $1/2$ times powers of $1/3$ — the $\{2,3\}$-smooth numbers. Including all primes covers every natural number.

## Derivation II — Eratosthenes sieve on the series (§283)

Independently and without reference to the product expansion, start from

$$A = 1 + \frac{1}{2^n} + \frac{1}{3^n} + \frac{1}{4^n} + \frac{1}{5^n} + \cdots.$$

Subtracting $A/2^n = 1/2^n + 1/4^n + 1/6^n + \cdots$ removes every even-index term:

$$B = \left(1 - \frac{1}{2^n}\right)A = 1 + \frac{1}{3^n} + \frac{1}{5^n} + \frac{1}{7^n} + \frac{1}{9^n} + \cdots.$$

Subtracting $B/3^n = 1/3^n + 1/9^n + 1/15^n + \cdots$ removes every term whose index is divisible by 3:

$$C = \left(1 - \frac{1}{3^n}\right)B = 1 + \frac{1}{5^n} + \frac{1}{7^n} + \frac{1}{11^n} + \frac{1}{13^n} + \cdots.$$

Continuing with primes $5, 7, 11, \ldots$, each step kills all multiples of one further prime. After sieving by every prime only the term 1 survives, so

$$A\prod_{p\text{ prime}}\left(1 - \frac{1}{p^n}\right) = 1,$$

equivalent to the formula above.

This is the **Sieve of Eratosthenes lifted to the series level**: where Eratosthenes erases multiples of $p$ from a list of integers, Euler subtracts a scaled copy of the running series.

## The Möbius dual (§275)

Pairing the formula with the §269 product $\prod(1-1/p^n) = 1 - 1/2^n - 1/3^n - 1/5^n + 1/6^n - \cdots$ (Möbius signs over squarefree integers; see [[squarefree-and-mobius-series]]) gives the reciprocal relation

$$P\cdot Q = 1\quad\text{with}\quad P = \sum_k\frac{1}{k^n},\quad Q = \sum_k\frac{\mu(k)}{k^n}.$$

Symbolically, $1/\zeta(n) = \sum \mu(k)/k^n$.

## The alternating variant (§284)

Applying the §283 sieve to the alternating series

$$A = 1 - \frac{1}{3^n} + \frac{1}{5^n} - \frac{1}{7^n} + \frac{1}{9^n} - \cdots$$

(no even terms, since only odd-index terms appear from the start; signs follow the $4m+1$ vs $4m-1$ rule) produces

$$1 = A\,\prod_{p \equiv 1\bmod 4}\!\!\!\Bigl(1 - \frac{1}{p^n}\Bigr)\!\!\!\prod_{p \equiv -1\bmod 4}\!\!\!\Bigl(1 + \frac{1}{p^n}\Bigr),$$

i.e. $A = \prod_p (1 - \chi_4(p)/p^n)^{-1}$ in modern notation, where $\chi_4$ is the non-trivial Dirichlet character mod 4. See [[prime-sign-series-for-pi]] for the $\pi$-series corollaries that fall out at $n=1, 3$.

## Worked first values

| $n$ | $\sum 1/k^n$ | Product over primes |
|---|---|---|
| 1 | $\infty$ | $\prod_p \dfrac{p}{p-1}$ (diverges; see [[divergence-of-prime-reciprocals]]) |
| 2 | $\pi^2/6$ | $\prod_p \dfrac{p^2}{p^2-1} = \dfrac{4}{3}\cdot\dfrac{9}{8}\cdot\dfrac{25}{24}\cdot\dfrac{49}{48}\cdots$ |
| 4 | $\pi^4/90$ | $\prod_p \dfrac{p^4}{p^4-1}$ |
| 6 | $\pi^6/945$ | $\prod_p \dfrac{p^6}{p^6-1}$ |

The right column for $n = 2$ appears in Euler's "Example I" at §277.

## Significance

The Euler product formula is the seed of analytic number theory:

- Equating an additive sum (over integers) with a multiplicative product (over primes) lets one **trade information about integers for information about primes**.
- Logarithmic differentiation gives $\log\zeta(s) = \sum_p\sum_k 1/(k p^{ks})$, which separates $\sum 1/p^s$ from the higher prime-power tail (§278).
- At $s = 1$ this yields the divergence of $\sum 1/p$ (§279), a quantitative refinement of Euclid's theorem.
- Dirichlet (1837) generalised the formula by replacing $1/p^s$ with $\chi(p)/p^s$ for a character $\chi$, recovering Dirichlet's theorem on primes in arithmetic progressions. Euler had already noticed the relevant character series — the §284, §294, §295 variants below — without the general framework.
- Riemann (1859) analytically continued $\zeta(s)$ to $\mathbb{C}\setminus\{1\}$; the Euler product becomes the bridge between the zeros of $\zeta$ and the distribution of primes.

## Related pages

- [[chapter-15-on-series-which-arise-from-products]]
- [[squarefree-and-mobius-series]]
- [[divergence-of-prime-reciprocals]]
- [[prime-zeta-values]]
- [[prime-sign-series-for-pi]]
- [[basel-problem]]
- [[zeta-at-even-integers]]
- [[arctangent-series]]
- [[geometric-series]]
- [[logarithmic-series]]
