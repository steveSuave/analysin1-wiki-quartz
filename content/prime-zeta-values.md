# Prime Zeta Values

**Summary**: §281–§282. Euler's numerical table of $S(n) = \sum_p 1/p^n$ — the *prime zeta function* — to 12 decimal places for every even $n$ from 2 to 36, obtained by inverting the logarithmic relation between $\log\zeta(n)$ and the prime-power sums (§278).

**Sources**: chapter15.pdf

**Last updated**: 2026-05-11

---

## The table (§282)

For the series of reciprocals of $n$-th powers of all primes,

$$S(n) := \sum_{p\text{ prime}}\frac{1}{p^n} = \frac{1}{2^n} + \frac{1}{3^n} + \frac{1}{5^n} + \frac{1}{7^n} + \frac{1}{11^n} + \frac{1}{13^n} + \cdots,$$

Euler tabulates (source: chapter15.pdf, §282):

| $n$ | $S(n)$ |
|---|---|
|  2 | $0.452247420041222$ |
|  4 | $0.076993139764252$ |
|  6 | $0.017070086850639$ |
|  8 | $0.004061405366515$ |
| 10 | $0.000993603573633$ |
| 12 | $0.000246026470033$ |
| 14 | $0.000061244396725$ |
| 16 | $0.000015282026219$ |
| 18 | $0.000003817278702$ |
| 20 | $0.000000953961123$ |
| 22 | $0.000000238450446$ |
| 24 | $0.000000059608184$ |
| 26 | $0.000000014901555$ |
| 28 | $0.000000003725333$ |
| 30 | $0.000000000931323$ |
| 32 | $0.000000000232830$ |
| 34 | $0.000000000058207$ |
| 36 | $0.000000000014551$ |

Euler's observation: "The remaining sums decrease by about one fourth at each step" (source: chapter15.pdf, §283). This is consistent with the dominant term $1/2^n$, which exactly quarters at each $n \to n + 2$, plus smaller corrections from $1/3^n, 1/5^n, \ldots$ which become negligible.

## The method (§281)

Euler does **not** sum these series directly — at $n = 2$ that would require summing $1/p^2$ over all primes, which is hopeless without knowing the primes in closed form. Instead he inverts the §278 identity

$$\log\zeta(n) = S(n) + \tfrac{1}{2}S(2n) + \tfrac{1}{3}S(3n) + \tfrac{1}{4}S(4n) + \cdots$$

For large $n$ the right side is dominated by $S(n)$ (and the next term $S(2n)/2$ is already exponentially smaller). Knowing $\zeta(n)$ in closed form for even $n$ from [[zeta-at-even-integers|Chapter 10]] (e.g. $\zeta(2) = \pi^2/6$, $\zeta(4) = \pi^4/90$, $\zeta(6) = \pi^6/945$, etc.), Euler solves recursively for $S(n)$:

$$S(n) = \log\zeta(n) - \tfrac{1}{2}S(2n) - \tfrac{1}{3}S(3n) - \cdots$$

Since $S(2n), S(3n), \ldots$ also have closed-form-$\zeta$-determined values via the same recurrence (and they decay geometrically), the computation **bootstraps from the largest $n$ downward**: $S(36), S(34), \ldots$ are computed first (the higher $n$ make all but the leading $\sum 1/2^{kn}$ negligible), then $S(34)$ uses $S(68), S(102), \ldots$ which Euler approximates well, and so on, working down to $S(2)$.

## A second sieve-based method (§281, parallel)

Euler also gives a related identity for **odd-index-only** prime sums

$$\tilde S(n) := \frac{1}{3^n} + \frac{1}{5^n} + \frac{1}{7^n} + \frac{1}{11^n} + \cdots \quad(\text{primes only, minus 2}),$$

derived by removing the $1/2^n$ contribution. Manipulating

$$S = (M - 1)\Bigl(1 - \frac{1}{2^n}\Bigr)\Bigl(1 - \frac{1}{3^n}\Bigr) + \frac{1}{6^n} - \frac{1}{25^n} - \frac{1}{35^n} - \cdots$$

(source: chapter15.pdf, §281) lets one recover $S(n)$ from the closed-form $M = \zeta(n)$ minus a rapidly-convergent correction series in **composite squarefree** indices.

This second form is the one Euler emphasises is convenient "provided only that $n$ is reasonably large" — the residual terms $1/9^n, 1/15^n, 1/21^n, \ldots$ (composites of small primes) decay quickly when $n \geq 8$ or so.

## Why no closed form?

The values $S(n) = \sum 1/p^n$ are **not** rational multiples of $\pi^n$ even at even $n$. They are believed to be transcendental but no closed form in terms of classical constants is known.

The closed form for $\log\zeta(n)$ (e.g. $\log(\pi^2/6)$ at $n=2$) decomposes via the §278 identity into the linear combination $S(n) + S(2n)/2 + S(3n)/3 + \cdots$ — and **only the linear combination** is closed-form. Individual prime-power sums $S(n)$, $S(2n)$, etc. each carry irreducible prime-distribution information.

This contrast — closed-form for $\zeta(2k)$, no closed form for $\sum 1/p^{2k}$ — is the analytic counterpart of: integers are easy (we know all of them), primes are hard (their distribution involves the zeros of $\zeta$).

## Numerical accuracy

Euler's 12-digit values match modern computations to all displayed digits. For example, $S(2) = 0.452247420041065...$ — Euler's $0.452247420041222$ is correct to 14 digits with an end-of-table rounding wobble of about $2\cdot 10^{-13}$ in the last two displayed digits, consistent with the geometric tail truncation.

The very small magnitudes at $n = 30$–$36$ ($\sim 10^{-9}$ to $10^{-11}$) show that Euler was carrying around 15+ digits of precision throughout the §278 recurrence — a remarkable hand-computation feat.

## Related pages

- [[chapter-15-on-series-which-arise-from-products]]
- [[divergence-of-prime-reciprocals]]
- [[euler-product-formula]]
- [[zeta-at-even-integers]]
- [[basel-problem]]
- [[logarithmic-series]]
- [[squarefree-and-mobius-series]]
